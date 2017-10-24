---
title: Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopfacturen tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopfacturen tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>Sjablonen en taken

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkoopfacturen tussen Finance and Operations en Sales:

- **Naam van de sjabloon in Gegevensintegratie** 

     - Verkoopfacturen (Fin en Ops naar Sales)

- **Namen van de taken in het project Gegevensintegratie**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Taken die nodig zijn voor het synchroniseren van koptekst en regels van verkoopfacturen:
-   Producten (Fin en Ops naar Sales)
-   Rekeningen (Sales naar Fin and Ops) (indien gebruikt)
-   Contactpersonen (Sales naar Fin and Ops) (indien gebruikt)
-   Koptekst en regels van verkooporder (Fin and Ops naar Sales)

## <a name="entity-set"></a>Entiteitset

| Finance en Operations                               | Common Data Service (CDS)              | Verkoop          |
|------------------------------------------------------|------------------|----------------|
| Extern onderhouden kopteksten van klantverkoopfacturen | SalesInvoice     | Facturen       |
| Extern onderhouden klantverkoopfactuurregels   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Entiteitstroom

Verkoopfacturen worden gemaakt in Finance and Operations en gesynchroniseerd met Sales.

> [!NOTE]
> Belastingen met betrekking tot toeslagen in de **koptekst van de verkoopfactuur** worden niet opgenomen bij de synchronisatie van Finance and Operations met Sales. Sales biedt namelijk geen ondersteuning voor belastinggegevens op koptekstniveau. Belastingen met betrekking tot kosten op het regelniveau worden opgenomen.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

-  Het veld **Factuurnummer** wordt aan de entiteit **Factuur** toegevoegd en weergegeven op de pagina.
 
-  De knop **Factuur maken** op de pagina **Verkooporder** is verborgen omdat de facturen in Finance and Operations worden gemaakt en worden gesynchroniseerd met Sales. De pagina **Factuur** kan niet worden bewerkt omdat facturen vanuit Finance and Operations worden gesynchroniseerd.
 
-  De **verkooporderstatus** wordt automatisch in **Gefactureerd** gewijzigd wanneer de bijbehorende factuur vanuit Finance and Operations is gesynchroniseerd met Sales. Daarnaast wordt de eigenaar van de verkooporder op basis waarvan de factuur is gemaakt aangewezen als de eigenaar van de factuur. Zo kan de eigenaar van de verkooporder de factuur weergeven.
 
## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

Voordat u verkoopfacturen synchroniseert, is het belangrijk de systemen bij te werken met de volgende instellingen:

### <a name="setup-in-sales"></a>Instellingen in Sales

- Controleer of onder **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** de optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**. 

- Controleer of onder **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** de optie **Berekeningsmethode korting** is ingesteld op **Regelartikel**. 

### <a name="setup-in-the-data-integration-project"></a>Instellingen in het project Gegevensintegratie

#### <a name="salesinvoiceheader-task"></a>Taak SalesInvoiceHeader

- Werk de toewijzing voor **CDS-organisatie-id** bij in **Bron** > **CDS**. 

    -  De standaardsjabloonwaarde voor **SalesOrder_Organization_OrganizationId** is ORG001.
    -  De standaardsjabloonwaarde voor **Account_Organization_OrganizationId** is ORG001.
    -  De standaardsjabloonwaarde voor **Organization_OrganizationId** is ORG001.

- Zorg ervoor dat de benodigde toewijzing aanwezig is in **Bron** > **CDS voor InvoiceCountryRegionId** tot **BillingAddress_Country**.

    -  De waarde van de sjabloon is **ValueMap** met een aantal landen die zijn toegewezen.

- **Prijslijst** is vereist voor het maken van facturen in Sales. Werk **ValueMap** in **CDS** > **Bestemming voor pricelevelid.name [Price List Name]** per valuta bij naar de gebruikte **prijslijst** in Sales. U kunt de standaard **prijslijst** voor één valuta of **ValueMap** gebruiken als u **prijslijsten** in meerdere valuta's hebt.

    -  De waarde van de sjabloon voor **pricelevelid.name [Price List Name]** is **ValueMap** op basis van **Valuta**.
    -  usd: CRM Service USA (voorbeeld). 

#### <a name="salesinvoiceline-task"></a>Taak SalesInvoiceLine

- Controleer of de benodigde toewijzing aanwezig is in **Bron** > **CDS voor maateenheid**.

- Controleer of de benodigde **ValueMap** voor **SalesUnitSymbol** in Finance and Operations aanwezig is in **Bron** > **CDS-toewijzing**. 
    
    - Waarde van de sjabloon met **ValueMap** is gedefinieerd voor **SalesUnitSymbol naar Quantity_UOM**.
    
-  Werk de toewijzing voor **CDS-organisatie-id bij in Bron** > **CDS**. 

    -  De standaardsjabloonwaarde voor **SalesInvoicer_Organization_OrganizationId** is ORG001.
    -  De standaardsjabloonwaarde voor **Product_Organization_OrganizationId** is ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Sjabloontoewijzing in Gegevensintegrator

> [!NOTE]
> **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.

![Sjabloontoewijzing in gegevensintegrator](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Verwante onderwerpen

[Producten uit Finance and Operations synchroniseren met producten in Sales](products-template-mapping.md)

[Accounts in Sales synchroniseren met klanten in Finance and Operations](accounts-template-mapping.md)

[Contactpersonen in Sales synchroniseren naar contactpersonen of klanten in Finance and Operations](contacts-template-mapping.md)

[Kopteksten en regels in verkoopoffertes vanuit Sales synchroniseren naar Finance and Operations](sales-quotation-template-mapping.md)

[Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales](sales-order-template-mapping.md)


