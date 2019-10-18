---
title: Projectramingen rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om projectuurschattingen en projectonkostenschattingen rechtstreeks van Microsoft Dynamics 365 Project Service Automation naar Dynamics 365 Finance te synchroniseren.
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
ms.openlocfilehash: 3b885610ac9ca8645358ba8ab6d46ab82143a534
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250479"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projectramingen rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations

[!include[banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om projectuurschattingen en projectonkostenschattingen rechtstreeks van Dynamics 365 Project Service Automation naar Dynamics 365 Finance te synchroniseren.

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling is beschikbaar in versie 8.0.
> - Integratie van werkelijke waarden is mogelijk in versie 8.0.1 of hoger.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Gegevensstroom voor Project Service Automation naar Finance

De integratieoplossing voor Project Service Automation naar Finance gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance. De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over projectuurramingen en projectkostenramingen van Project Service Automation naar Finance mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.

[![Gegevensstroom voor Project Service Automation-integratie met Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Ramingen voor projecturen

### <a name="template-and-tasks"></a>Sjabloon en taken

Selecteer voor toegang tot de beschikbare sjablonen in het Microsoft PowerApps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projectuurramingen vanuit Project Service Automation naar Finance:

- **Naam van de sjabloon in Gegevensintegratie:** Projectuurramingen (PSA naar Fin and Ops)
- **Naam van de taken in het project:**

    - Transactierelaties
    - Onkostenramingen

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Financiën                                       |
|----------------------------|-----------------------------------------------|
| Projecttaken              | Integratie-entiteit voor projectuurramingen |

### <a name="entity-flow"></a>Entiteitstroom

Projectuurramingen worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance als projectuurprognoses.

### <a name="prerequisites"></a>Vereisten

Voordat synchronisatie van projectuurramingen kan plaatsvinden, moet u projecten, projecttaken en projectkostentransactiecategorieën synchroniseren.

### <a name="power-query"></a>Power Query

In de sjabloon voor de raming van projecturen moet u Microsoft Power Query voor Excel gebruiken om het volgende te doen:

- De standaardprognosemodel-id instellen die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.
- Alle resourcespecifieke records in de taak uitfilteren waarvoor integratie tot uurramingen zal mislukken.
- Alle lege transactiecategorierijen uitfilteren. Als u deze taak niet uitvoert, kan dit leiden tot onjuiste uurramingen.

#### <a name="set-the-default-forecast-model-id"></a>De standaardprognosemodel-id instellen

Als u de standaardprognosemodel-id in de sjabloon wilt bijwerken, klikt u op de pijl **Toewijzen** om de toewijzing te openen. Selecteer vervolgens de koppeling **Geavanceerde query en filtering**.

- Als u de standaardsjabloon Project-uurramingen (PSA naar Fin and Ops) gebruikt, selecteert u de **Ingevoegde voorwaarde** in de lijst **Toegepaste stappen**. Vervang in de vermelding **Functie** de waarde **O\_forecast** door de naam van de prognosemodel-id die moet worden gebruikt met de integratie. De standaardsjabloon heeft een prognosemodel-ID vanuit de demonstratiegegevens.
- Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen. Selecteer in Power Query de optie **Voorwaardelijke kolom toevoegen** en voer een naam voor de nieuwe kolom in, zoals **Model-id**. Voer de voorwaarde in voor de kolom waarin als Projecttaak niet null is, dan \<voer de prognosemodel-id in\>; anders null.

#### <a name="filter-out-resource-specific-records"></a>Resourcespecifieke records uitfilteren

De sjabloon voor projectuurramingen (PSA naar Fin and Ops) heeft een standaardfilter waarmee resourcespecifieke records worden verwijderd. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen. Selecteer de koppeling **Geavanceerde query en filtering** om te filteren op de kolom **msdyn\_islinetask** zodat alleen **onware** records worden opgenomen.

#### <a name="filter-out-empty-transaction-category-rows"></a>Lege transactiecategorierijen uitfilteren

U moet een filter toevoegen om rijen te verwijderen die lege transactiecategorieën bevat. Deze taak is verplicht, ongeacht of u de standaardsjabloon gebruikt of uw eigen sjabloon maakt. Dit filter verwijdert overzichtrijen die afkomstig zijn van Project Service Automation die ertoe kunnen leiden dat de uurprognoses in Finance onjuist zijn. Selecteer de koppeling **Geavanceerde query en filtering** om null-records uit te filteren in de kolom **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projectkostenramingen

### <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projectkostenramingen vanuit Project Service Automation naar Finance:

- **Naam van de sjabloon in Gegevensintegratie:** Projectkostenramingen (PSA naar Fin and Ops)
- **Naam van de taken in het project:**

    - Transactierelaties 
    - Onkostenramingen

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Financiën                                                  |
|----------------------------|----------------------------------------------------------|
| Transactieverbindingen    | Integratie-entiteit voor projectransactierelaties |
| Ramingsregels             | Integratie-entiteit voor projectkostenramingen         |

### <a name="entity-flow"></a>Entiteitstroom

Projectkostenramingen worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance als projectkostenprognoses.

### <a name="prerequisites"></a>Vereisten

Voordat synchronisatie van projectkostenramingen kan plaatsvinden, moet u projecten, projecttaken en projectkostentransactiecategorieën synchroniseren.

### <a name="power-query"></a>Power Query

In de projectkostenramingssjabloon moet u Power Query gebruiken om de volgende taken uit te voeren:

- Filteren om alleen onkostenramingsrecords op te nemen.
- De standaardprognosemodel-id instellen die wordt gebruikt wanneer de integratie nieuwe uurprognoses maakt.
- De factureringstypen transformeren.
- De transactietypen transformeren.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filteren om alleen onkostenramingsregels op te nemen

De sjabloon voor projectonkostenramingen (PSA naar Fin and Ops) heeft een standaardfilter waarmee alleen onkostenregels in de integratie worden opgenomen. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen. Selecteer de taak **Transactierelaties** en klik vervolgens op de pijl **Toewijzen** om de toewijzing te openen. Selecteer de koppeling **Geavanceerde query en filtering**. Filter de kolom **msdyn\_transactiontype1** zodat deze alleen **msdyn\_estimateline** bevat.

#### <a name="set-the-default-forecast-model-id"></a>De standaardprognosemodel-id instellen

Als u de standaardprognosemodel-id in de sjabloon wilt bijwerken, selecteert u de taak **Onkostenramingen** en klikt u vervolgens op de pijl **Toewijzen** om de toewijzing te openen. Selecteer de koppeling **Geavanceerde query en filtering**.

- Als u de standaardsjabloon Microsoft Project-onkostenramingen (PSA naar Fin and Ops) gebruikt, selecteert u in Power Query eerst de **Ingevoegde voorwaarde** in de sectie **Toegepaste stappen**. Vervang in de vermelding **Functie** de waarde **O\_forecast** door de naam van de prognosemodel-id die moet worden gebruikt met de integratie. De standaardsjabloon heeft een prognosemodel-ID vanuit de demonstratiegegevens.
- Als u een nieuwe sjabloon maakt, moet u deze kolom toevoegen. Selecteer in Power Query de optie **Voorwaardelijke kolom toevoegen** en voer een naam voor de nieuwe kolom in, zoals **Model-id**. Voer de voorwaarde in voor de kolom waarin als ramingsregel-ID niet null is, dan \<voer de prognosemodel-id in\>; anders null.

#### <a name="transform-the-billing-types"></a>De factureringstypen transformeren

De sjabloon Projectonkostenramingen (PSA naar Fin and Ops) bevat een voorwaardelijke kolom die wordt gebruikt voor het transformeren van de factureringstypen die tijdens de integratie van Project Service Automation zijn ontvangen. Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen. Selecteer de koppeling **Geavanceerde query en filtering** en selecteer vervolgens **Voorwaardelijke kolom toevoegen**. Voer naam in voor de nieuwe kolom, zoals **Factureringstype**. Voer daarna de volgende voorwaarde in:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>De transactietypen transformeren

De sjabloon Projectonkostenramingen (PSA naar Fin and Ops) bevat een voorwaardelijke kolom die wordt gebruikt voor het transformeren van de transactietypen die tijdens de integratie van Project Service Automation zijn ontvangen. Als u uw eigen sjabloon maakt, moet u deze voorwaardelijke kolom toevoegen. Selecteer de koppeling **Geavanceerde query en filtering** en selecteer vervolgens **Voorwaardelijke kolom toevoegen**. Voer naam in voor de nieuwe kolom, zoals **Transactietype**. Voer daarna de volgende voorwaarde in:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u voorbeelden van de sjabloontaaktoewijzingen in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Sjabloontoewijzing](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)
