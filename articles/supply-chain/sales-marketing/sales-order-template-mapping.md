---
title: Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkooporders tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Kopteksten en regels in verkooporders synchroniseren vanuit Finance and Operations naar Sales

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkooporders tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales. 

## <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkooporders tussen Finance and Operations en Sales:

- **Naam van sjabloon in Gegevensintegratie** 

    - Verkooporders (Fin and Ops naar Sales)
    
- **Namen van taken in het project Gegevensintegratie**

    - OrderHeader
    - OrderLine

Taken die nodig zijn voor het synchroniseren van koptekst en regels van verkoopfacturen:

- Producten (Fin en Ops naar Sales)
- Rekeningen (Sales naar Fin and Ops) (indien gebruikt)
- Contactpersonen naar klanten (Sales naar Fin and Ops) (indien gebruikt)

## <a name="entity-set"></a>Entiteitset

| Finance en Operations |    Common Data Service (CDS)         |     Verkoop      |
|------------------------|----------------|----------------|
| CDS-verkooporderkoppen| SalesOrder     | SalesOrders |
| CDS-verkooporderregels  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Entiteitstroom

Verkooporders worden gemaakt in Finance and Operations en gesynchroniseerd met Sales.

Filters in de sjabloon zorgen ervoor dat alleen relevante verkooporders worden opgenomen in de synchronisatie:

- Zowel de bestellende als de facturerende klant op de verkooporder uit Sales wordt opgenomen in de synchronisatie. In Finance and Operations worden de velden **OrderingCustomerIsExternallyMaintained** en **InvoiceCustomerIsExternallyMaintained** gebruikt om de synchronisatie in de gegevensentiteiten bij te houden.

- De **verkooporder** in Finance and Operations moet worden bevestigd. Alleen de bevestigde verkooporders of verkooporders met een hogere verwerkingsstatus, bijvoorbeeld met de status Verzonden of Gefactureerd, worden gesynchroniseerd met Sales.

- Na het maken of wijzigen van een verkooporder moet de batchtaak **Verkooptotalen berekenen** in Finance and Operations worden uitgevoerd. Alleen de verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd met CDS en Sales.

> [!NOTE]
> Belastingen met betrekking tot toeslagen in de **koptekst van de verkooporder** worden niet opgenomen bij de synchronisatie van Finance and Operations met Sales. Sales biedt namelijk geen ondersteuning voor belastinggegevens op koptekstniveau. Belastingen met betrekking tot kosten op het regelniveau worden opgenomen.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Nieuwe velden worden toegevoegd aan de entiteit **Order** en weergegeven op de pagina:

- **Wordt extern beheerd**: ingesteld op **Ja** wanneer de order afkomstig is van Finance and Operations.

- **Verwerkingsstatus**: wordt gebruikt om de verwerkingsstatus weer te geven van de order in Finance and Operations. De volgende waarden zijn mogelijk:

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

De instelling **Heeft alleen extern onderhouden producten** wordt gebruikt in andere verkooporderscenario's (synchronisatie van Sales met Finance and Operation) om consequent bij te houden of de verkooporder geheel uit **extern onderhouden producten** bestaat, in welk geval producten worden onderhouden in Finance and Operations. Zo garandeert u dat u niet verkooporderregels probeert te synchroniseren met producten die onbekend zijn in Finance and Operations.
 
De knoppen **Factuur maken**, **Order annuleren**, **Opnieuw berekenen**, **Producten ophalen** en **Adres opzoeken** op de pagina **Verkooporder** zijn verborgen voor extern onderhouden orders omdat facturen worden gemaakt in Finance and Operations en deze worden gesynchroniseerd met Sales. De bestelpagina kan niet worden bewerkt omdat verkoopordergegevens vanuit Finance and Operations worden gesynchroniseerd.
 
De **verkooporderstatus** blijft actief om ervoor te zorgen dat wijzigingen vanuit Finance and Operations naar de **verkooporder** in Sales kunnen stromen. U doet dit door **Statuscode [Status]** in te stellen op **Actief** in het project Gegevensintegratie.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing 

Voordat u verkooporders synchroniseert, is het belangrijk de systemen bij te werken met de volgende instellingen:

### <a name="setup-in-sales"></a>Instellingen in Sales

- Zorg voor machtigingen voor het team waaraan de gebruiker (vanuit **Verbindingsset** in Sales) is toegewezen. Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar niet het team. Zonder beheerderstoegang ontvangt u een fout dat het hoofdteam ontbreekt wanneer u het project uitvoert vanuit Gegevensintegrator. 

    - Selecteer onder **Instellingen** > **Beveiliging** > **Teams** het relevante team, klik op **Rollen beheren** en selecteer een rol met de gewenste machtigingen, bijvoorbeeld Systeembeheerder.

- Controleer of onder **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** de optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**. 

- Controleer of onder **Instellingen** > **Beheer** > **Systeeminstellingen** > **Sales** de optie **Berekeningsmethode korting** is ingesteld op **Regelartikel**. 

### <a name="setup-in-finance-and-operations"></a>Instellingen In Finance and Operations

Stel **Verkoop en marketing** > **Periodieke taken** > **Verkooptotalen berekenen** in om te worden uitgevoerd als batchtaak, met **Totalen berekenen voor verkooporders** ingesteld op **Ja**. Dit is belangrijk omdat alleen de verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd met CDS en Sales. De frequentie van de batchtaak moet worden uitgelijnd met de frequentie van de verkoopordersynchronisatie.

### <a name="setup-in-the-data-integration-project"></a>Instellingen in het project Gegevensintegratie

#### <a name="salesheader-task"></a>Taak SalesHeader

- Werk de toewijzing voor **CDS-organisatie-id bij in Bron** > **CDS**.

    - De standaardsjabloonwaarde voor **Account_Organization_OrganizationId** is ORG001.
    - De standaardsjabloonwaarde voor **InvoiceAccount_Organization_OrganizationId** is ORG001.
    - De standaardsjabloonwaarde voor **Organization_OrganizationId** is ORG001.

- Zorg ervoor dat de benodigde toewijzing bestaat in **Bron** > **CDS voor InvoiceCountryRegionId to BillingAddress_Country** en voor **DeliveryCountryRegionId to DeliveryAddress_Country**.

    - De waarde van de sjabloon is **ValueMap** met een aantal landen die zijn toegewezen.

- **Prijslijst** is vereist voor het maken van orders in Sales. Werk **ValueMap** in **CDS** > **Bestemming** voor **pricelevelid.name [Price List Name]** per valuta bij naar de gebruikte **prijslijst** in Sales. U kunt de gebruikte **prijslijst** voor één valuta of **ValueMap** gebruiken als u **prijslijsten** in meerdere valuta's hebt.
    
    - De standaardwaarde van de sjabloon voor **pricelevelid.name [Price List Name]** is CRM Service USA (voorbeeld). 

#### <a name="salesline-task"></a>Taak SalesLine

- Werk de toewijzing voor **CDS-organisatie-id bij in Bron** > **CDS**. 
    
    - De standaardsjabloonwaarde voor **SalesOrder_Organization_OrganizationId** is ORG001.
    - De standaardsjabloonwaarde voor **Product_Organization_OrganizationId** is ORG001.

- Zorg ervoor dat de benodigde toewijzing aanwezig is in **Bron** > **CDS** voor **DeliveryCountryRegionId** tot **DeliveryAddress_Country**.

    - De waarde van de sjabloon is **ValueMap** met een aantal landen die zijn toegewezen.
    
- Controleer of de benodigde **ValueMap** voor **SalesUnitSymbol** in Finance and Operations aanwezig is in **Bron** > **CDS-toewijzing**.

    - Waarde van de sjabloon met **ValueMap** is gedefinieerd voor **SalesUnitSymbol naar Quantity_UOM**.

## <a name="template-mapping-in-data-integrator"></a>Sjabloontoewijzing in gegevensintegrator

> [!NOTE]
> De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.

### <a name="orderheader"></a>OrderHeader

![Sjabloontoewijzing in gegevensintegrator](./media/sales-order-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Sjabloontoewijzing in gegevensintegrator](./media/sales-order-template-mapping-data-integrator-3.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Verwante onderwerpen

[Producten uit Finance and Operations synchroniseren met producten in Sales](products-template-mapping.md)

[Accounts in Sales synchroniseren met klanten in Finance and Operations](accounts-template-mapping.md)

[Contactpersonen in Sales synchroniseren naar contactpersonen of klanten in Finance and Operations](contacts-template-mapping.md)

[Kopteksten en regels in verkoopoffertes vanuit Sales synchroniseren naar Finance and Operations](sales-quotation-template-mapping.md)

[Kopteksten en regels in verkoopfacturen synchroniseren vanuit Finance and Operations naar Sales](sales-invoice-template-mapping.md)


