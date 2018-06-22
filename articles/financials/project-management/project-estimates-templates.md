---
title: Projectramingen vanuit Project Service Automation rechtstreeks synchroniseren met projectramingen in Finance and Operations
description: In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om ramingen van projecturen en projectkosten rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
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
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: nl-nl
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Projectramingen vanuit Project Service Automation rechtstreeks synchroniseren met projectramingen in Finance and Operations

In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om ramingen van projecturen en projectkosten rechtstreeks vanuit Microsoft Dynamics 365 for Project Service Automation te synchroniseren met Dynamics 365 for Finance and Operations.

> [!NOTE]
> Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling is beschikbaar in Dynamics 365 for Finance and Operations, versie 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gegevensstroom voor Project Service Automation naar Finance and Operations

De oplossing Project Service Automation-integratie met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations. De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over projectuurramingen en projectkostenramingen van Project Service Automation naar Finance and Operations mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.

[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Sjablonen en taken

Selecteer voor toegang tot de beschikbare sjablonen in het Microsoft PowerApps Beheercentrum **Projecten** en selecteer vervolgens in de rechterbovenhoek **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projectuurramingen vanuit Project Service Automation naar Finance and Operations:

-  **Naam van de sjabloon in Gegevensintegratie:** Projectuurramingen (PSA naar Fin and Ops)

-  **Naam van de taken in het project:** 
    - Transactierelaties 
    - Onkostenramingen

## <a name="entity-set"></a>Entiteitset

| Project Service Automation      | Finance en Operations                          |
|---------------------------------|-------------------------------------------------|
| Projecttaken                   | Integratie-entiteit voor projectuurramingen   |

## <a name="entity-flow"></a>Entiteitstroom

Projectuurramingen worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projectuurprognoses.

## <a name="preconditions"></a>Voorwaarden vooraf:

Voordat synchronisatie van projectuurramingen kan plaatsvinden, moet u projecten, projecttaken en projectkostentransactiecategorieën synchroniseren.

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query in de projectuurramingssjabloon gebruiken om het volgende te doen:
- De **Prognosemodel-id** instellen die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.
- Alle resourcespecifieke records in de taak uitfilteren waarvoor integratie tot uurramingen zal mislukken
- Alle lege transactiecategorierijen uitfilteren. Als u dat niet doet, kan dit leiden tot onjuiste uurramingen.

### <a name="forecast-model-id"></a>Prognosemodel-id
Als u de standaardprognosemodel-id in de sjabloon wilt bijwerken, klikt u op de pijl **Toewijzen** om de toewijzing te openen. Selecteer om de Geavanceerde query en filtering te openen.
- Als u de standaardsjabloon Microsoft Project-uurramingen (PSA naar Fin and Ops) gebruikt, selecteert u de **Ingevoegde voorwaarde** in de sectie **Toegepaste stappen**. Vervang in de vermelding **Functie** **O_forecast** door de naam van de **Prognosemodel-id** die moet worden gebruikt met de integratie. De standaardsjabloon heeft een prognosemodel-ID vanuit de demonstratiegegevens.
- Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen. Selecteer **Voorwaardelijke kolom toevoegen** en geef de kolom een naam, zoals ModelID. Voer de voorwaarde voor de kolom in waarbij als projecttaak is niet null, dan <enter the forecast model ID>; anders null.

### <a name="filter-out-resource-specific-records"></a>Resourcespecifieke records uitfilteren
De sjabloon Projectuurramingen (PSA naar Fin and Ops) heeft een standaardfilter waarmee resourcespecifieke records worden verwijderd. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen. Selecteer in het formulier Geavanceerde query en filtering dat u wilt filteren op de kolom **msdyn_islinetask** om alleen **onware** records op te nemen.

### <a name="filter-out-empty-transaction-category-rows"></a>Lege transactiecategorierijen uitfilteren
U moet een filter toevoegen om rijen te verwijderen met lege transactiecategorieën. Dit is nodig als u de standaardsjabloon gebruikt of uw eigen sjabloon maakt. Dit filter verwijdert overzichtrijen die afkomstig zijn van Project Service Automation die ertoe kunnen leiden dat de uurprognoses in Finance and Operations onjuist zijn. Selecteer in het formulier Geavanceerde query en filtering om de null-records uit te filteren in de kolom **msdyn_transactioncategory_value**.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostenramingen vanuit Project Service Automation naar Finance and Operations:

-  **Naam van de sjabloon in Gegevensintegratie:** Projectkostenramingen (PSA naar Fin and Ops)
-  **Naam van de taken in het project:** 
     - Transactierelaties 
     - Onkostenramingen

## <a name="entity-set"></a>Entiteitset

| Project Service Automation      | Finance en Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Transactieverbindingen         | Integratie-entiteit voor projectransactierelaties.   |
| Ramingsregels                  | Integratie-entiteit voor projectkostenramingen.           |

## <a name="entity-flow"></a>Entiteitstroom

Projectkostenramingen worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projectkostenprognoses.

## <a name="prerequisites"></a>Vereisten

Voordat synchronisatie van projectkostenramingen kan plaatsvinden, moet u projecten, projecttaken en projectkostentransactiecategorieën synchroniseren.

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query in de projectkostenramingssjabloon gebruiken om het volgende te doen:
- Filteren om alleen onkostenramingsrecords op te nemen
- De **Prognosemodel-id** instellen die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.
- De factureringstypen transformeren.
- De transactietypen transformeren.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Filteren om alleen onkostenramingsregels op te nemen
De sjabloon Projectonkostenramingen (PSA naar Fin and Ops) heeft een standaardfilter waarmee alleen onkostenregels in de integratie worden opgenomen. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen. Selecteer de transactierelatietaak en klik op de pijl **Toewijzen**. Selecteer **Geavanceerde query en filtering**. Filter de kolom **msdyn_transactiontype1** zodat deze alleen **msdyn_estimateline** bevat.

### <a name="forecast-model-id"></a>Prognosemodel-id
Als u de standaardprognosemodel-id in de sjabloon voor de onkostenramingstaak wilt bijwerken, klikt u op de pijl **Toewijzen** om de toewijzing te openen. Selecteer om de Geavanceerde query en filtering te openen.
- Als u de standaardsjabloon Microsoft Project-onkostenramingen (PSA naar Fin and Ops) gebruikt, selecteert u eerst de **Ingevoegde voorwaarde** in de sectie **Toegepaste stappen**. Vervang in de vermelding **Functie** **O_forecast** door de naam van de **Prognosemodel-id** die moet worden gebruikt met de integratie. De standaardsjabloon heeft een prognosemodel-ID vanuit de demonstratiegegevens.
- Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen. Selecteer **Voorwaardelijke kolom toevoegen** en geef de kolom een naam, zoals ModelID. Voer de voorwaarde in voor de kolom waarin als ramingsregel-ID niet null is, dan <voer de prognosemodel-id in>; anders null.

### <a name="transform-the-billing-types"></a>De factureringstypen transformeren
De sjabloon Projectonkostenramingen (PSA naar Fin and Ops) bevat een voorwaardelijke kolom om de factureringstypen die tijdens de integratie van Project Service Automation zijn ontvangen, te transformeren.
- Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen. Selecteer in het formulier Geavanceerde query en filtering **Voorwaardelijke kolom toevoegen**. Geef de kolom een naam, zoals 'Factureringstype'. De in te voeren voorwaarde is als volgt:

    If **msdyn_billingtype** = 192350000, then **NonChargeable** else if **msdyn_billingtype** = 192350001, then **Chargeable** else if **msdyn_billingtype** = 192350002, then **Complimentary** else **NotAvailable**

### <a name="transform-the-transaction-types"></a>De transactietypen transformeren
De sjabloon Projectonkostenramingen (PSA naar Fin and Ops) bevat een voorwaardelijke kolom om de transactietypen die tijdens de integratie van Project Service Automation zijn ontvangen, te transformeren.
- Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen. Selecteer in het formulier Geavanceerde query en filtering **Voorwaardelijke kolom toevoegen**. Geef de kolom een naam, zoals 'Transactietype'. De in te voeren voorwaarde is als volgt: If **msdyn_transactiontypecode** = 192350000, then **Cost** else if **msdyn_transactiontypecode** = 192350005, then **Sales** else **null**

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u voorbeelden van de sjabloontaaktoewijzingen in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Sjabloontoewijzing](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




