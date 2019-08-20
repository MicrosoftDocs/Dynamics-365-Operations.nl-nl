---
title: Werkelijke projectwaarden rechtstreeks vanuit Project Service Automation synchroniseren met het projectintegratiejournaal in Finance and Operations
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om werkelijke waarden van projecten rechtstreeks van Microsoft Dynamics 365 for Project Service Automation naar Microsoft Dynamics 365 for Finance and Operations te synchroniseren.
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
ms.openlocfilehash: 3b6427d7eede8fe35fcd86928c3d5b8507876e2e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846070"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Werkelijke projectwaarden rechtstreeks vanuit Project Service Automation synchroniseren met het projectintegratiejournaal in Finance and Operations

[!include[banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om werkelijke waarden van projecten rechtstreeks van Microsoft Dynamics 365 for Project Service Automation naar Microsoft Dynamics 365 for Finance and Operations te synchroniseren.

De sjabloon synchroniseert transacties vanuit Project Service Automation in een faseringstabel in Finance and Operations. Nadat de synchronisatie is voltooid, **moet** u de gegevens importeren uit de faseringstabel naar het integratiejournaal.

> [!NOTE]
> - Integratie van werkelijke waarden van het project is mogelijk in Microsoft Dynamics 365 for Finance and Operations versie 8.0.1 of hoger.
> - Als u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren. Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.
> - Als u gebruikmaakt van Finance and Operations 7.3.0 en u bijzondere-kostentransacties overbrengt vanuit Project Service Automation, moet u KB 4345320 installeren om deze kosten op te nemen in de projectfactuur.
> - Als u btw-bedragen op tijd invoert of onkostentransacties in Project Service Automation, moet u Project Service Automation Update 7 installeren. Anders worden de werkelijke btw-waarden niet gekoppeld aan de bijbehorende werkelijke tijd- of onkostenwaarden en worden zij niet gesynchroniseerd met Finance and Operations. Neem voor meer informatie contact op met de ondersteuning.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gegevensstroom voor Project Service Automation naar Finance and Operations

De oplossing Project Service Automation-integratie met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations. De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over werkelijke projectwaarden van Project Service Automation naar Finance and Operations mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.

[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Werkelijke projectwaarden vanuit Project Service Automation

### <a name="template-and-tasks"></a>Sjabloon en taken

Selecteer voor toegang tot de beschikbare sjablonen in het Microsoft PowerApps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van werkelijke projectwaarden vanuit Project Service Automation naar Finance and Operations:

- **Naam van de sjabloon in Gegevensintegratie:** Werkelijke projectwaarden (PSA naar Fin and Ops)
- **Naam van de taken in het project:**

    - Werkelijke kosten
    - Transactieverbindingen

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Finance en Operations                                   |
|----------------------------|----------------------------------------------------------|
| Werkelijke kosten                    | Integratie-entiteit voor werkelijke projectwaarden                   |
| Transactieverbindingen    | Integratie-entiteit voor projectransactierelaties |

### <a name="entity-flow"></a>Entiteitstroom

Werkelijke projectwaarden worden beheerd in Project Service Automation en worden gesynchroniseerd naar het projectintegratiejournaal in Finance and Operations. De boekhouding wordt toegepast op basis van de standaard financiële dimensies en de boekingsinstelling.

### <a name="prerequisites"></a>Vereisten

Voordat de synchronisatie van werkelijke waarden plaatsvinden kan, moet u de integratieparameters van Project Service Automation configureren en projecten, projecttaken en categorieën projectonkostentransacties synchroniseren.

### <a name="power-query"></a>Power Query

In de sjabloon voor werkelijke projectwaarden moet u Microsoft Power Query voor Excel gebruiken om het volgende te doen:

- Het transactietype Project Service Automation transformeren naar het juiste transactietype in Finance and Operations. Deze transformatie is al gedefinieerd in de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops).
- Het factureringstype in Project Service Automation transformeren naar het juiste factureringstype in Finance and Operations. Deze transformatie is al gedefinieerd in de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops). Het factureringstype wordt vervolgens toegewezen aan de regeleigenschap op basis van de configuratie op de pagina **Project Service Automation-integratieparameters**.
- Filteren op specifieke resourceorganisatie-eenheden die moeten worden gesynchroniseerd met deze sjabloon.
- Als intercompany tijd of werkelijke intercompany onkostenwaarden worden gesynchroniseerd met Finance and Operations, moet u de organisatie-eenheid van het contract transformeren naar de juiste rechtspersoon in Finance and Operations. In de sjabloon Werkelijke projectwaarden (PSA naar Fin and Ops) is een voorwaardelijke kolom gedefinieerd op basis van demogegevens. U moet de laatst ingevoegde voorwaardelijke kolom bijwerken naar de juiste rechtspersonen. Anders treedt mogelijk een integratiefout op of worden mogelijk onjuiste werkelijke transacties geïmporteerd in Finance and Operations.
- Als intercompany tijd of werkelijke intercompany onkosten niet worden gesynchroniseerd met Finance and Operations, moet u de laatst ingevoegde voorwaardelijke kolom verwijderen uit uw sjabloon. Anders treedt mogelijk een integratiefout op of worden mogelijk onjuiste werkelijke transacties geïmporteerd in Finance and Operations.

#### <a name="contract-organizational-unit"></a>Organisatie-eenheid van contract
Als u de ingevoegde voorwaardelijke kolom in de sjabloon wilt bijwerken, klikt u op de pijl **Toewijzen** om de toewijzing te openen. Selecteer de koppeling **Geavanceerde query en filtering** om Power Query te openen.

- Als u de standaardsjabloon Werkelijke Project-waarden (PSA naar Fin and Ops) in Power Query gebruikt, selecteert u de laatste **Ingevoegde voorwaarde** uit de sectie **Toegepaste stappen**. Vervang in de vermelding **Functie** de waarde **USSI** door de naam van de rechtspersoon die moet worden gebruikt met de integratie. Voeg benodigde aanvullende voorwaarden toe aan de vermelding **Functie** en werk de **else**-voorwaarde uit **USMF** bij naar de juiste rechtspersoon.
- Als u een nieuwe sjabloon maakt, moet u de kolom toevoegen ter ondersteuning van intercompany uren en onkosten. Selecteer **Voorwaardelijke kolom toevoegen** en voer een naam in voor de kolom, zoals **LegalEntity**. Geef een voorwaarde voor de kolom, waarbij als **msdyn\_contractorganizationalunitid.msdyn\_name** is \<organisatie-eenheid\>, dan \<voert u de rechtspersoon in\>; anders null.

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen laten een voorbeeld zioen van sjabloontaaktoewijzing in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Sjabloontoewijzing](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importeren vanuit de staging-tabel na integratie vanuit Project Service Automation

Het periodieke proces Importeren uit faseringstabel moet worden uitgevoerd na de synchronisatie van werkelijke waarden uit Project Service Automation naar Finance and Operations. Dit proces importeert de projecttransacties uit de faseringstabel in het Project Service Automation-integratiejournaal, waar de boekhouding wordt toegepast en de geïmporteerde transacties kunnen worden geboekt. We adviseren dit proces uit te voeren in batchmodus en eventueel in te stellen op uitvoering als terugkerende batch.

## <a name="update-actuals-from-finance-and-operations"></a>Werkelijke waarden vanuit Finance and Operations bijwerken

### <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van het boekstuknummer en btw voor geboekte projecttransacties van Finance and Operations naar Project Service Automation:

- **Naam van de sjabloon in Gegevensintegratie:** Update van werkelijke projectwaarden (Fin Ops naar PSA)
- **Naam van de taken in het project:**

    - Werkelijke kosten 
    - Transactieverbindingen

### <a name="entity-set"></a>Entiteitset

| Finance en Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integratie-entiteit voor werkelijke projectwaarden                   | Werkelijke kosten                    |
| Integratie-entiteit voor projectransactierelaties | Transactieverbindingen    |

### <a name="entity-flow"></a>Entiteitstroom

Werkelijke projectwaarden worden beheerd in Project Service Automation en worden gesynchroniseerd naar het projectintegratiejournaal in Finance and Operations. Nadat werkelijke waarden zijn geboekt in Finance and Operations, worden deze bijgewerkt in Project Service Automation met het boekstuknummer uit Finance and Operations. Als er btw is toegevoegd in Finance and Operations, worden er nieuwe werkelijke btw-waarden gemaakt in Project Service Automation.

### <a name="power-query"></a>Power Query

In de sjabloon voor het bijwerken van werkelijke projectwaarden moet u Power Query gebruiken om het volgende te doen:

- Het transactietype in Finance and Operations transformeren naar het juiste transactietype in Project Service Automation. Deze transformatie is al gedefinieerd in de sjabloon voor het bijwerken van werkelijke projectwaarden (PSA naar Fin and Ops).
- Het factureringstype in Finance and Operations transformeren naar het juiste factureringstype in Project Service Automation. Deze transformatie is al gedefinieerd in de sjabloon voor het bijwerken van werkelijke projectwaarden (PSA naar Fin and Ops).

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u voorbeelden van de sjabloontaaktoewijzingen in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Finance and Operations naar Project Service Automation worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Sjabloontoewijzing](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
