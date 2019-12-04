---
title: Werkelijke projectwaarden rechtstreeks vanuit Project Service Automation synchroniseren met het projectintegratiejournaal in Finance and Operations
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om werkelijke projectwaarden rechtstreeks van Microsoft Dynamics 365 Project Service Automation met Finance and Operations te synchroniseren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 302ac0f456dd8a24dc02948ee657e359f5a9c844
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770330"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Werkelijke projectwaarden rechtstreeks vanuit Project Service Automation synchroniseren met het projectintegratiejournaal in Finance and Operations

[!include[banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om werkelijke waarden van projecten rechtstreeks van Dynamics 365 Project Service Automation naar Dynamics 365 Finance te synchroniseren.

De sjabloon synchroniseert transacties vanuit Project Service Automation in een faseringstabel in Finance. Nadat de synchronisatie is voltooid, **moet** u de gegevens importeren uit de faseringstabel naar het integratiejournaal.

> [!NOTE]
> - Integratie van werkelijke waarden van het project is mogelijk vanaf versie 8.0.1.
> - Als u Enterprise edition 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren. Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.
> - Als u gebruikmaakt van versie 7.3.0 en u bijzondere-kostentransacties overbrengt vanuit Project Service Automation, moet u KB 4345320 installeren om deze kosten op te nemen in de projectfactuur.
> - Als u btw-bedragen op tijd invoert of onkostentransacties in Project Service Automation, moet u Project Service Automation Update 7 installeren. Anders worden de werkelijke btw-waarden niet gekoppeld aan de bijbehorende werkelijke tijd- of onkostenwaarden en worden zij niet gesynchroniseerd met Finance. Neem voor meer informatie contact op met de ondersteuning.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Gegevensstroom voor Project Service Automation naar Finance

De integratieoplossing voor Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance. De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over werkelijke projectwaarden van Project Service Automation naar Finance mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.

[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Werkelijke projectwaarden vanuit Project Service Automation

### <a name="template-and-tasks"></a>Sjabloon en taken

Selecteer voor toegang tot de beschikbare sjablonen in het Microsoft Power Apps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van werkelijke projectwaarden vanuit Project Service Automation naar Finance:

- **Naam van de sjabloon in Gegevensintegratie:** Werkelijke projectwaarden (PSA naar Fin and Ops)
- **Naam van de taken in het project:**

    - Werkelijke kosten
    - Transactieverbindingen

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Financiën                                   |
|----------------------------|----------------------------------------------------------|
| Werkelijke kosten                    | Integratie-entiteit voor werkelijke projectwaarden                   |
| Transactieverbindingen    | Integratie-entiteit voor projectransactierelaties |

### <a name="entity-flow"></a>Entiteitstroom

Werkelijke projectwaarden worden beheerd in Project Service Automation en worden gesynchroniseerd naar het projectintegratiejournaal in Finance. De boekhouding wordt toegepast op basis van de standaard financiële dimensies en de boekingsinstelling.

### <a name="prerequisites"></a>Vereisten

Voordat de synchronisatie van werkelijke waarden plaatsvinden kan, moet u de integratieparameters van Project Service Automation configureren en projecten, projecttaken en categorieën projectonkostentransacties synchroniseren.

### <a name="power-query"></a>Power Query

In de sjabloon voor werkelijke projectwaarden moet u Microsoft Power Query voor Excel gebruiken om het volgende te doen:

- Het transactietype Project Service Automation transformeren naar het juiste transactietype in Finance. Deze transformatie is al gedefinieerd in de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops).
- Het factureringstype in Project Service Automation transformeren naar het juiste factureringstype in Finance. Deze transformatie is al gedefinieerd in de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops). Het factureringstype wordt vervolgens toegewezen aan de regeleigenschap op basis van de configuratie op de pagina **Project Service Automation-integratieparameters**.
- Filteren op specifieke resourceorganisatie-eenheden die moeten worden gesynchroniseerd met deze sjabloon.
- Als intercompany tijd of werkelijke intercompany onkostenwaarden worden gesynchroniseerd met Finance, moet u de organisatie-eenheid van het contract transformeren naar de juiste rechtspersoon in Finance. In de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops) is een voorwaardelijke kolom gedefinieerd op basis van demogegevens. U moet de laatst ingevoegde voorwaardelijke kolom bijwerken naar de juiste rechtspersonen. Anders treedt mogelijk een integratiefout op of worden mogelijk onjuiste werkelijke transacties geïmporteerd in Finance.
- Als intercompany tijd of werkelijke intercompany onkosten niet worden gesynchroniseerd met Finance, moet u de laatst ingevoegde voorwaardelijke kolom verwijderen uit uw sjabloon. Anders treedt mogelijk een integratiefout op of worden mogelijk onjuiste werkelijke transacties geïmporteerd in Finance.

#### <a name="contract-organizational-unit"></a>Organisatie-eenheid van contract
Als u de ingevoegde voorwaardelijke kolom in de sjabloon wilt bijwerken, klikt u op de pijl **Toewijzen** om de toewijzing te openen. Selecteer de koppeling **Geavanceerde query en filtering** om Power Query te openen.

- Als u de standaardsjabloon Werkelijke Project-waarden (PSA naar Fin and Ops) in Power Query gebruikt, selecteert u de laatste **Ingevoegde voorwaarde** uit de sectie **Toegepaste stappen**. Vervang in de vermelding **Functie** de waarde **USSI** door de naam van de rechtspersoon die moet worden gebruikt met de integratie. Voeg benodigde aanvullende voorwaarden toe aan de vermelding **Functie** en werk de **else**-voorwaarde uit **USMF** bij naar de juiste rechtspersoon.
- Als u een nieuwe sjabloon maakt, moet u de kolom toevoegen ter ondersteuning van intercompany uren en onkosten. Selecteer **Voorwaardelijke kolom toevoegen** en voer een naam in voor de kolom, zoals **LegalEntity**. Geef een voorwaarde voor de kolom, waarbij als **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organisatie-eenheid\>, dan \<voert u de rechtspersoon in\>; anders null.

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen laten een voorbeeld zioen van sjabloontaaktoewijzing in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Sjabloontoewijzing](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importeren vanuit de staging-tabel na integratie vanuit Project Service Automation

Het periodieke proces Importeren uit faseringstabel moet worden uitgevoerd na de synchronisatie van werkelijke waarden uit Project Service Automation naar Finance. Dit proces importeert de projecttransacties uit de faseringstabel in het Project Service Automation-integratiejournaal, waar de boekhouding wordt toegepast en de geïmporteerde transacties kunnen worden geboekt. We adviseren dit proces uit te voeren in batchmodus en het eventueel in te stellen op uitvoering als terugkerende batch.

## <a name="update-actuals-from-finance"></a>Werkelijke waarden bijwerken vanuit Finance

### <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van het boekstuknummer en btw voor geboekte projecttransacties van Finance naar Project Service Automation:

- **Naam van de sjabloon in Gegevensintegratie:** Update van werkelijke projectwaarden (Fin Ops naar PSA)
- **Naam van de taken in het project:**

    - Werkelijke kosten 
    - Transactieverbindingen

### <a name="entity-set"></a>Entiteitset

| Financiën                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integratie-entiteit voor werkelijke projectwaarden                   | Werkelijke kosten                    |
| Integratie-entiteit voor projectransactierelaties | Transactieverbindingen    |

### <a name="entity-flow"></a>Entiteitstroom

Werkelijke projectwaarden worden beheerd in Project Service Automation en worden gesynchroniseerd naar het projectintegratiejournaal in Finance. Nadat werkelijke waarden zijn geboekt in Finance, worden deze bijgewerkt in Project Service Automation met het boekstuknummer uit Finance. Als er btw is toegevoegd in Finance, worden er nieuwe werkelijke btw-waarden gemaakt in Project Service Automation.

### <a name="power-query"></a>Power Query

In de sjabloon voor het bijwerken van werkelijke projectwaarden moet u Power Query gebruiken om het volgende te doen:

- Het transactietype in Finance transformeren naar het juiste transactietype in Project Service Automation. Deze transformatie is al gedefinieerd in de sjabloon voor het bijwerken van werkelijke projectwaarden (PSA naar Fin and Ops).
- Het factureringstype in Finance transformeren naar het juiste factureringstype in Project Service Automation. Deze transformatie is al gedefinieerd in de sjabloon voor het bijwerken van werkelijke projectwaarden (PSA naar Fin and Ops).

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u voorbeelden van de sjabloontaaktoewijzingen in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Finance naar Project Service Automation worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Sjabloontoewijzing](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
