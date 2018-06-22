---
title: Werkelijke projectwaarden vanuit Project Service Automation rechtstreeks synchroniseren met het projectintegratiejournaal in Finance and Operations
description: In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om werkelijke projectwaarden rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: nl-nl
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Werkelijke projectwaarden vanuit Project Service Automation rechtstreeks synchroniseren met het projectintegratiejournaal in Finance and Operations

In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om werkelijke projectwaarden rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Dynamics 365 for Finance and Operations.

De sjabloon synchroniseert transacties vanuit Project Service Automation in een faseringstabel in Finance and Operations. Nadat de synchronisatie is voltooid, moet u importeren uit de faseringstabel naar het integratiejournaal.

> [!NOTE]
> Werkelijke projectwaarden zijn beschikbaar in Dynamics 365 for Finance and Operations versie 8.01.

> [!NOTE]
> Als u btw-bedragen op tijd invoert of onkostentransacties in Project Service Automation, moet u Project Service Automation Update 7 installeren. Als deze update niet is geïnstalleerd, worden de werkelijke btw-waarden niet gekoppeld aan de bijbehorende werkelijke tijd- of onkostenwaarden en niet gesynchroniseerd met Finance and Operations. Neem contact met de ondersteuning op voor meer informatie.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gegevensstroom voor Project Service Automation naar Finance and Operations

De oplossing Project Service Automation-integratie met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations. De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over werkelijke projectwaarden van Project Service Automation naar Finance and Operations mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.

[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Sjablonen en taken

Selecteer voor toegang tot de beschikbare sjablonen in het Microsoft PowerApps Beheercentrum **Projecten** en selecteer vervolgens in de rechterbovenhoek **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van werkelijke projectwaarden vanuit Project Service Automation naar Finance and Operations:

-  **Naam van de sjabloon in Gegevensintegratie:** Werkelijke projectwaarden (PSA naar Fin and Ops)

-  **Naam van de taken in het project:** 
    - Werkelijke kosten 
    - Transactieverbindingen

## <a name="entity-set"></a>Entiteitset

| Project Service Automation      | Finance en Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Werkelijke kosten                         | Integratie-entiteit voor werkelijke projectwaarden                      |
| Transactieverbindingen         | Integratie-entiteit voor projectransactierelaties    |

## <a name="entity-flow"></a>Entiteitstroom

Werkelijke projectwaarden worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations, naar het projectintegratiejournaal. De boekhouding wordt toegepast op basis van de standaard financiële dimensies en de boekingsinstelling.

## <a name="preconditions"></a>Voorwaarden vooraf:

Voordat de synchronisatie van werkelijke waarden plaatsvinden kan, moet u de integratieparameters van Project Service Automation configureren en projecten, projecttaken en categorieën projectonkostentransacties synchroniseren.

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query in de sjabloon voor werkelijke projectwaarden gebruiken om het volgende te doen:
- Het **transactietype** Project Service Automation transformeren naar het juiste **transactietype** in Finance and Operations. In de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops) is deze transformatie al gedefinieerd.
- Het **factureringstype** van Project Service Automation transformeren naar het juiste **factureringstype** in Finance and Operations. In de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops) is deze transformatie al gedefinieerd. Het factureringstype wordt vervolgens toegewezen aan de **regeleigenschap** op basis van de configuratie in het formulier met integratieparameters van Dynamics 365 for Project Service Automation.
- Filteren op specifieke **resourceorganisatie-eenheden** die moet worden gesynchroniseerd met deze sjabloon.
- Als **intercompany tijd of werkelijke intercompany onkostenwaarden** worden gesynchroniseerd met Finance and Operations, moet u de **organisatie-eenheid** van het contract transformeren naar de juiste **rechtspersoon** in Finance and Operations. In de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops) is een voorwaardelijke kolom gedefinieerd op basis van demonstratiegegevens. U moet de laatst ingevoegde kolom bijwerken naar de juiste rechtspersonen. Nalaten hiervan kan leiden tot een integratiefout of onjuiste werkelijke transacties, geïmporteerd in Finance and Operations.
- Als **intercompany tijd of werkelijke intercompany onkosten** niet worden gesynchroniseerd met Finance and Operations, moet u de laatst ingevoegde voorwaardekolom verwijderen uit uw sjabloon. Nalaten hiervan kan leiden tot een integratiefout of onjuiste werkelijke transacties, geïmporteerd in Finance and Operations.

### <a name="contract-organizational-unit"></a>Organisatie-eenheid van contract
Als u de ingevoegde voorwaardekolom in de sjabloon wilt bijwerken, klikt u op de pijl **Toewijzen** om de toewijzing te openen. Selecteer om de Geavanceerde query en filtering te openen.
- Als u de standaardsjabloon Werkelijke Microsoft Project-waarden (PSA naar Fin and Ops) gebruikt, selecteert u de laatste **Ingevoegde voorwaarde** in de sectie **Toegepaste stappen**. Vervang in de vermelding **Functie** **USSI** door de naam van de **Rechtspersoon** die moet worden gebruikt met de integratie. Voeg benodigde aanvullende voorwaarden toe aan de vermelding **Functie** en werk de **else**-voorwaarde uit **USMF** bij naar de juiste **Rechtspersoon**.
- Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen ter ondersteuning van intercompany uren en onkosten. Selecteer **Voorwaardelijke kolom toevoegen** en geef de kolom een naam, zoals LegalEntity. Voer de voorwaarde voor de kolom in waarbij als msdyn_contractorganizationalunitid.msdyn_name is <organizational unit>, dan <enter the Legal entity>; anders null.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Sjabloontoewijzing](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Importeren uit faseringstabel

Het periodieke proces Importeren uit faseringstabel moet worden uitgevoerd na de synchronisatie van werkelijke waarden uit Project Service Automation naar Finance and Operations. Dit proces importeert de projecttransacties uit de faseringstabel in het Project Service Automation-integratiejournaal, waar de boekhouding wordt toegepast en de geïmporteerde transacties kunnen worden geboekt. Het wordt aanbevolen dat u dit proces in batchmodus uitvoert en eventueel kan het worden ingesteld om te worden uitgevoerd als een terugkerende batch.

## <a name="update-actuals"></a>Werkelijke waarden bijwerken

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van het boekstuknummer en btw voor geboekte projecttransacties van Finance and Operations naar Project Service Automation:

-  **Naam van de sjabloon in Gegevensintegratie:** Update van werkelijke projectwaarden (Fin Ops naar PSA)
-  **Naam van de taken in het project:** 
     - Werkelijke kosten 
     - Transactieverbindingen

## <a name="entity-set"></a>Entiteitset

| Finance en Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Integratie-entiteit voor werkelijke projectwaarden                         | Werkelijke kosten                           |
| Integratie-entiteit voor projectransactierelaties       | Transactieverbindingen           |

## <a name="entity-flow"></a>Entiteitstroom

Werkelijke projectwaarden worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations, naar het projectintegratiejournaal. Zodra in Finance and Operations geboekt, worden werkelijke waarden in Project Service Automation bijgewerkt met het boekstuknummer uit Finance and Operations. Als er btw werd toegevoegd in Finance and Operations, worden er nieuwe werkelijke btw-waarden in Project Service Automation gemaakt.

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query in de updatesjabloon voor werkelijke projectwaarden gebruiken om het volgende te doen:
- Het **transactietype** van Finance and Operations transformeren naar het juiste **transactietype** in Project Service Automation. In de sjabloon Update van werkelijke projectwaarden (Fin and Ops naar PSA) is deze transformatie al gedefinieerd.
- Het **factureringstype** van Finance and Operations transformeren naar het juiste **factureringstype** in Project Service Automation. In de sjabloon Update van werkelijke projectwaarden (Fin and Ops naar PSA) is deze transformatie al gedefinieerd.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u voorbeelden van de sjabloontaaktoewijzingen in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Finance and Operations naar Project Service Automation worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Sjabloontoewijzing](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




