---
title: Kopteksten en regels in verkoopfacturen direct vanuit Finance and Operations synchroniseren naar Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopfacturen tussen Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Kopteksten en regels in verkoopfacturen rechtstreeks synchroniseren vanuit Finance and Operations naar Sales

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopfacturen tussen Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Finance and Operations en Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Finance and Operations en Sales.

[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkoopfacturen vanuit Finance and Operations naar Sales:

- **Naam van de sjabloon in Gegevensintegratie:** Verkoopfacturen (Fin and Ops naar Sales) - Direct
- **Namen van de taken in het project Gegevensintegratie:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopfacturen kan plaatsvinden:

- Producten (Fin and Ops naar Sales) - Direct
- Rekeningen (Sales naar Fin and Ops) - Direct (indien gebruikt)
- Contactpersonen (Sales naar Fin and Ops) - Direct (indien gebruikt)
- Koptekst en regels van verkooporder (Fin and Ops naar Sales) - Direct

## <a name="entity-set"></a>Entiteitset

| Finance en Operations                               | Verkoop          |
|------------------------------------------------------|----------------|
| Extern onderhouden kopteksten van klantverkoopfacturen | Facturen       |
| Extern onderhouden klantverkoopfactuurregels   | InvoiceDetails |

## <a name="entity-flow"></a>Entiteitstroom

Verkoopfacturen worden gemaakt in Finance and Operations en gesynchroniseerd met Sales.

> [!NOTE]
> Momenteel worden belastingen met betrekking tot toeslagen in de koptekst van de verkoopfactuur niet opgenomen bij de synchronisatie van Finance and Operations naar Sales. Sales biedt geen ondersteuning voor belastinggegevens op koptekstniveau. Belastingen gerelateerd aan toeslagen op regelniveau worden echter wel opgenomen in de synchronisatie.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

- Het veld **Factuurnummer** is aan de entiteit **Factuur** toegevoegd en wordt weergegeven op de pagina.
- De knop **Factuur maken** op de pagina **Verkooporder** is verborgen omdat facturen in Finance and Operations worden gemaakt en worden gesynchroniseerd naar Sales. De pagina **Factuur** kan niet worden bewerkt omdat facturen vanuit Finance and Operations worden gesynchroniseerd.
- De waarde voor **Verkooporderstatus** wordt automatisch in **Gefactureerd** gewijzigd wanneer de bijbehorende factuur vanuit Finance and Operations is gesynchroniseerd naar Sales. Daarnaast wordt de eigenaar van de verkooporder op basis waarvan de factuur is gemaakt, aangewezen als de eigenaar van de factuur. De eigenaar van de verkooporder kan de factuur dus weergeven.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

Voordat u verkoopfacturen synchroniseert, is het belangrijk de volgende instellingen in de systemen bij te werken.

### <a name="setup-in-sales"></a>Instellingen in Sales

Ga naar **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:

- De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.
- Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.

### <a name="setup-in-the-data-integration-project"></a>Instellingen in het project Gegevensintegratie

#### <a name="salesinvoiceheader-task"></a>Taak SalesInvoiceHeader

- Zorg ervoor dat de vereiste toewijzing bestaat voor **InvoiceCountryRegionId** naar **BillingAddress\_Country**.

    De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen.

- Een prijslijst is vereist voor het maken van facturen in Sales. Werk de waardetoewijzing voor **pricelevelid.name \[Price List Name\]** per valuta bij naar de gebruikte prijslijst in Sales. U kunt de standaardprijslijst gebruiken voor één valuta. Als u prijslijsten in meerdere valuta's hebt, kunt u een waardetoewijzing gebruiken.

    De sjabloonwaarde voor **pricelevelid.name \[Prijs List Name\]** is een waardetoewijzing die is gebaseerd op valuta met USD = CRM Service USA (voorbeeld).  
    
#### <a name="salesinvoiceline-task"></a>Taak SalesInvoiceLine

- Zorg ervoor dat de vereiste toewijzing bestaat voor **Maateenheid**.
- Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Finance and Operations bestaat.

    Er wordt een sjabloonwaarde met een waardetoewijzing voor **SalesUnitSymbol** naar **Quantity\_UOM** gedefinieerd.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

> [!NOTE]
> De velden **Vetalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie. 

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations worden gesynchroniseerd.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Sjabloontoewijzing in Gegevensintegratie](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Sjabloontoewijzing in Gegevensintegratie](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Verwante onderwerpen

[Prospect naar contant geld](prospect-to-cash.md)

[Rekeningen in Sales direct synchroniseren naar klanten in Finance and Operations](accounts-template-mapping-direct.md)

[Producten van Finance and Operations rechtstreeks synchroniseren met producten in Sales](products-template-mapping-direct.md)

[Contactpersonen in Sales rechtstreeks synchroniseren met contactpersonen of klanten in Finance and Operations](contacts-template-mapping-direct.md)

[Kopteksten en regels in verkooporders direct vanuit Finance and Operations synchroniseren naar Sales](sales-order-template-mapping-direct-two-ways.md)







