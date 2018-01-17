---
title: Kopteksten en regels in verkooporders direct vanuit Finance and Operations synchroniseren naar Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van kopteksten en regels van verkooporders vanuit Microsoft Dynamics 365 for Finance and Operations, Enterprise edition naar Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Kopteksten en regels in verkooporders direct vanuit Finance and Operations synchroniseren naar Sales

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van kopteksten en regels van verkooporders vanuit Microsoft Dynamics 365 for Finance and Operations, Enterprise edition naar Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.

[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkooporders vanuit Finance and Operations naar Sales:

- **Naam van de sjabloon in Gegevensintegratie:** Verkooporders (Fin and Ops naar Sales) - Direct
- **Namen van de taken in het project Gegevensintegratie:**

    - OrderHeader
    - OrderLine

De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopfacturen kan plaatsvinden:

- Producten (Fin and Ops naar Sales) - Direct
- Rekeningen (Sales naar Fin and Ops) - Direct (indien gebruikt)
- Contactpersonen naar klanten (Sales naar Fin and Ops) - Direct (indien gebruikt)

## <a name="entity-set"></a>Entiteitset

| Finance en Operations  | Verkoop             |
|-------------------------|-------------------|
| CDS-verkooporderkoppen | SalesOrders       |
| CDS-verkooporderregels   | SalesOrderDetails |

## <a name="entity-flow"></a>Entiteitstroom

Verkooporders worden gemaakt in Finance and Operations en gesynchroniseerd met Sales.

Filters in de sjabloon zorgen ervoor dat alleen relevante verkooporders worden opgenomen in de synchronisatie:

- Als zowel de bestellende als de facturerende klant op de verkooporder uit Sales afkomstig is, worden beide opgenomen in de synchronisatie. In Finance and Operations worden de velden **OrderingCustomerIsExternallyMaintained** en **InvoiceCustomerIsExternallyMaintained** gebruikt om de synchronisatie in de gegevensentiteiten bij te houden.
- De verkooporder in Finance and Operations moet worden bevestigd. Alleen bevestigde verkooporders of verkooporders met een hogere verwerkingsstatus, bijvoorbeeld met de status **Verzonden** of **Gefactureerd**, worden gesynchroniseerd naar Sales.
- Na het maken of wijzigen van een verkooporder moet de batchtaak **Verkooptotalen berekenen** in Finance and Operations worden uitgevoerd. Alleen verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd naar Sales.

> [!NOTE]
> Momenteel worden belastingen met betrekking tot toeslagen in de koptekst van de verkooporder niet opgenomen bij de synchronisatie van Finance and Operations naar Sales. Sales biedt geen ondersteuning voor belastinggegevens op koptekstniveau. Belastingen gerelateerd aan toeslagen op regelniveau worden echter wel opgenomen in de synchronisatie.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Nieuwe velden zijn toegevoegd aan de entiteit **Order** en worden weergegeven op de pagina:

- **Wordt extern beheerd**: stel deze optie in op **Ja** wanneer de order afkomstig is uit Finance and Operations.
- **Verwerkingsstatus**: in dit veld wordt de verwerkingsstatus weergegeven van de order in Finance and Operations. De volgende waarden zijn beschikbaar:

    - Actief
    - Bevestigd
    - Pakbon
    - Gefactureerd
    - Opgenomen
    - Gedeeltelijk opgenomen
    - Gedeeltelijk ingepakt
    - Verzonden
    - Gedeeltelijk verzonden
    - Gedeeltelijk gefactureerd
    - Geannuleerd

De instelling **Heeft alleen extern onderhouden producten** wordt gebruikt in andere verkooporderscenario's (bijvoorbeeld voor de synchronisatie van Sales naar Finance and Operations) om consequent bij te houden of een verkooporder geheel uit extern onderhouden producten bestaat. Als een verkooporder alleen uit extern beheerde producten bestaat, worden de producten beheerd in Finance and Operations. Met deze instelling garandeert u dat u geen verkooporderregels probeert te synchroniseren die producten bevatten die onbekend zijn in Finance and Operations.

Voor extern beheerde orders zijn de knoppen **Factuur maken**, **Order annuleren**, **Opnieuw berekenen**, **Producten ophalen** en **Adres opzoeken** op de pagina **Verkooporder** verborgen omdat facturen worden gemaakt in Finance and Operations en vervolgens worden gesynchroniseerd naar Sales. De bestelpagina kan niet worden bewerkt omdat verkoopordergegevens vanuit Finance and Operations worden gesynchroniseerd.

De status van een verkooporder blijft **Actief** om ervoor te zorgen dat wijzigingen vanuit Finance and Operations naar de verkooporder in Sales kunnen stromen. U stelt dit gedrag in door de standaardwaarde voor **Statuscode \[Status\]** op **Actief** in te stellen in het project Gegevensintegratie.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

Voordat u verkooporders synchroniseert, is het belangrijk de volgende instellingen in de systemen bij te werken.

### <a name="setup-in-sales"></a>Instellingen in Sales

- Zorg ervoor dat er machtigingen zijn ingesteld voor het team waaraan de gebruiker uit uw verbindingsset in Sales is toegewezen. Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar het team niet. Als het team niet ook beheerderstoegang heeft wanneer u het project uitvoert vanuit Gegevensintegratie, wordt een foutbericht weergegeven waarin wordt aangegeven dat het hoofdteam ontbreekt.

    Ga naar **Instellingen** > **Beveiliging** > **Teams**, selecteer het relevante team, selecteer **Rollen beheren** en selecteer een rol met de gewenste machtigingen, bijvoorbeeld **Systeembeheerder**.

- Ga naar **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:

    - De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.
    - Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.

### <a name="setup-in-finance-and-operations"></a>Instellingen In Finance and Operations

Ga naar **Verkoopbeheer en marketing** > **Periodieke taken** > **Verkooptotalen berekenen** en stel de taak zo in dat deze wordt uitgevoerd als batchtaak. Stel de optie **Totalen berekenen voor verkooporders** in op **Ja**. Deze stap is belangrijk omdat alleen verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd naar Sales. De frequentie van de batchtaak moet worden uitgelijnd met de frequentie van de verkoopordersynchronisatie.

### <a name="setup-in-the-data-integration-project"></a>Instellingen in het project Gegevensintegratie

#### <a name="salesheader-task"></a>Taak SalesHeader

- Zorg ervoor dat de vereiste toewijzing bestaat voor **InvoiceCountryRegionId** naar **BillingAddress\_Country** en voor **DeliveryCountryRegionId** naar **DeliveryAddress\_Country**.

    De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen.

- Een prijslijst is vereist voor het maken van orders in Sales. Werk de waardetoewijzing voor **pricelevelid.name \[Price List Name\]** per valuta bij naar de gebruikte prijslijst in Sales. U kunt de standaardprijslijst gebruiken voor één valuta. Als u prijslijsten in meerdere valuta's hebt, kunt u een waardetoewijzing gebruiken.

    De standaardsjabloonwaarde van de sjabloon voor **pricelevelid.name \[Price List Name\]** is **CRM Service USA (voorbeeld)**.

#### <a name="salesline-task"></a>Taak SalesLine

- Zorg ervoor dat de vereiste toewijzing bestaat voor **DeliveryCountryRegionId** naar **DeliveryAddress\_Country**.

    De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen.

- Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Finance and Operations bestaat.

    Er wordt een sjabloonwaarde met een waardetoewijzing voor **SalesUnitSymbol** naar **Quantity\_UOM** gedefinieerd.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

> [!NOTE]
> De velden **Vetalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie. 

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations worden gesynchroniseerd.

### <a name="orderheader"></a>OrderHeader

![Sjabloontoewijzing in Gegevensintegrator](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Sjabloontoewijzing in Gegevensintegrator](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Verwante onderwerpen

[Prospect naar contant geld](prospect-to-cash.md)

[Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations](accounts-template-mapping-direct.md)

[Producten vanuit Finance and Operations direct synchroniseren met producten in Sales](products-template-mapping-direct.md)

[Contactpersonen vanuit Sales direct synchroniseren naar contactpersonen of klanten in Finance and Operations](contacts-template-mapping-direct.md)

[Kopteksten en regels in verkoopfacturen direct vanuit Finance and Operations synchroniseren naar Sales](sales-invoice-template-mapping-direct.md)




