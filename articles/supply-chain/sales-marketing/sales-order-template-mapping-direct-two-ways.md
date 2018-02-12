---
title: Verkooporders direct synchroniseren tussen Sales en Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van verkooporders tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2017
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
ms.sourcegitcommit: 7a828090fa34eb96d2b557eb06e48ad05b421ae8
ms.openlocfilehash: 9aa8c78f5aea5a818d517c2baa9051750b132fc6
ms.contentlocale: nl-nl
ms.lasthandoff: 11/20/2017

---

# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Verkooporders direct synchroniseren tussen Sales en Finance and Operations

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het direct synchroniseren van verkooporders tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [PowerApps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjablonen en onderliggende taken worden gebruikt voor het direct synchroniseren van verkooporders tussen Sales en Finance and Operations:

- **Namen van de sjablonen in Gegevensintegratie:** 

    - Verkooporders (Sales naar Fin and Ops) - Direct
    - Verkooporders (Fin and Ops naar Sales) - Direct

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

Verkooporders worden gemaakt in Sales en gesynchroniseerd naar Finance and Operations als **Project uitvoeren** voor een project wordt geactiveerd op basis van de sjabloon **Verkooporders (Sales naar Fin and Ops) - Direct**. U kunt verkooporders alleen vanuit Sales activeren en synchroniseren als alle **orderproducten** volledig uit extern beheerde producten bestaan. Er kunnen dus geen toe te voegen producten zijn. Nadat de order is geactiveerd, wordt de verkooporder alleen-lezen in de gebruikersinterface (UI). Op dat moment worden de updates uitgevoerd vanuit Finance and Operations. Als de verkooporder de status **Bevestigd** heeft, kan het project op basis van de sjabloon **Verkooporders (Fin and Ops naar Sales) - Direct** worden gebruikt om updates of de afhandelingsstatus vanuit Finance and Operations te synchroniseren naar Sales.

U hoeft geen orders in Sales te maken. U kunt nieuwe verkooporders in Finance and Operations maken. Als een verkooporder de status **Bevestigd** heeft, wordt deze gesynchroniseerd naar Sales, zoals wordt beschreven in de vorige alinea.

In Finance and Operations zorgen filters in de sjabloon ervoor dat alleen de relevante verkooporders worden opgenomen in de synchronisatie:

- Als zowel de bestellende als de facturerende klant op de verkooporder uit Sales afkomstig is, worden beide opgenomen in de synchronisatie. In Finance and Operations worden de velden **OrderingCustomerIsExternallyMaintained** en **InvoiceCustomerIsExternallyMaintained** gebruikt om verkooporders te filteren op basis van de gegevensentiteiten.
- De verkooporder in Finance and Operations moet worden bevestigd. Alleen bevestigde verkooporders of verkooporders met een hogere verwerkingsstatus, bijvoorbeeld met de status **Verzonden** of **Gefactureerd**, worden gesynchroniseerd naar Sales.
- Na het maken of wijzigen van een verkooporder moet de batchtaak **Verkooptotalen berekenen** in Finance and Operations worden uitgevoerd. Alleen verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd naar Sales.

## <a name="freight-tax"></a>Transportbelasting

Sales ondersteunt geen btw op koptekstniveau omdat btw op regelniveau wordt opgeslagen. Om belastingen op koptekstniveau te ondersteunen vanuit Finance and Operations, bijvoorbeeld vrachtbelastingen, worden de belastingen als toe te voegen product met de naam **Transportbelasting** gesynchroniseerd naar Sales. Op deze manier kan de standaardprijsberekening in Sales worden gebruikt om totalen te berekenen, zelfs als er belastingen op koptekstniveau aanwezig zijn vanuit Finance and Operations.

## <a name="discount-calculation-and-rounding"></a>Berekening en afronding van korting

Het model voor het berekenen van korting in Sales wijkt af van het model in Finance and Operations. In Finance and Operations kan het uiteindelijke kortingsbedrag op een verkoopregel het resultaat zijn van een combinatie van kortingsbedragen en -percentages. Als dit uiteindelijke kortingsbedrag wordt gedeeld door de hoeveelheid op de regel, kan er afronding plaatsvinden. Deze afronding wordt echter niet gebruikt als een afgerond kortingsbedrag per eenheid wordt gesynchroniseerd naar Sales. Het volledige kortingsbedrag op een verkoopregel in Finance and Operations kan alleen correct worden gesynchroniseerd naar Sales als het volledige bedrag wordt gesynchroniseerd, zonder het te delen door de regelhoeveelheid. Daarom moet u in Sales de optie **Berekeningsmethode korting** instellen op **Regelartikel**.

Als een verkooporderregel vanuit Sales naar Finance and Operations wordt gesynchroniseerd, wordt het volledige regelkortingsbedrag gebruikt. Omdat in Finance and Operations geen veld beschikbaar is waarin het volledige kortingsbedrag voor een regel kan worden opgeslagen, wordt het bedrag gedeeld door de hoeveelheid en opgeslagen in het veld **Regelkorting**. Afronding die tijdens deze deling plaatsvindt, wordt opgeslagen in het veld **Verkooptoeslagen** op de verkoopregel.

### <a name="example"></a>Voorbeeld

**Synchronisatie vanuit Sales naar Finance and Operations**

- **Sales:** Hoeveelheid = 3, korting per regel = € 10,00
- **Finance and Operations:** Hoeveelheid = 3, regelkortingsbedrag = € 3,33, verkooptoeslag = -€ 0,01 

**Synchronisatie vanuit Finance and Operations naar Sales**

- **Finance and Operations:** Hoeveelheid = 3, regelkortingsbedrag = € 3,33, verkooptoeslag = -€ 0,01
- **Sales:** Hoeveelheid = 3, korting per regel = = (3 × € 3,33) + € 0,01 = € 10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Nieuwe velden zijn toegevoegd aan de entiteit **Order** en worden weergegeven op de pagina:

- **Wordt extern beheerd**: stel deze optie in op **Ja** wanneer de order afkomstig is uit Finance and Operations.
- **Verwerkingsstatus**: in dit veld wordt de verwerkingsstatus weergegeven van de order in Finance and Operations. De volgende waarden zijn beschikbaar:

    - **Concept**: de beginstatus wanneer een order wordt gemaakt in Sales. In Sales kunnen alleen orders met deze status worden bewerkt.
    - **Actief**: de status nadat de order is geactiveerd met de knop **Activeren** in Sales.
    - **Bevestigd**
    - **Pakbon**
    - **Gefactureerd**
    - **Opgenomen**
    - **Gedeeltelijk opgenomen**
    - **Gedeeltelijk ingepakt**
    - **Verzonden**
    - **Gedeeltelijk verzonden**
    - **Gedeeltelijk gefactureerd**
    - **Geannuleerd**

De instelling **Heeft alleen extern onderhouden producten** wordt tijdens orderactivering gebruikt om consistent bij te houden of een verkooporder geheel bestaat uit extern beheerde producten. Als een verkooporder alleen uit extern beheerde producten bestaat, worden de producten beheerd in Finance and Operations. Met deze instelling garandeert u dat u niet verkooporderregels probeert te activeren en te synchroniseren die producten bevatten die onbekend zijn in Finance and Operations.

Voor extern beheerde orders zijn de knoppen **Factuur maken**, **Order annuleren**, **Opnieuw berekenen**, **Producten ophalen** en **Adres opzoeken** op de pagina **Verkooporder** verborgen omdat facturen worden gemaakt in Finance and Operations en vervolgens worden gesynchroniseerd naar Sales. Deze orders kunnen niet worden bewerkt omdat verkoopordergegevens na activering vanuit Finance and Operations worden gesynchroniseerd.

De verkooporderstatus blijft **Actief** om ervoor te zorgen dat wijzigingen vanuit Finance and Operations naar de verkooporder in Sales kunnen stromen. U stelt dit gedrag in door de standaardwaarde voor **Statuscode \[Status\]** op **Actief** in te stellen in het project Gegevensintegratie.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

Voordat u verkooporders synchroniseert, is het belangrijk de volgende instellingen in de systemen bij te werken.

### <a name="setup-in-sales"></a>Instellingen in Sales

- Zorg ervoor dat er machtigingen zijn ingesteld voor het team waaraan de gebruiker uit uw verbindingsset in Sales is toegewezen. Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar het team niet. Als het team geen beheerderstoegang heeft wanneer u het project uitvoert vanuit Gegevensintegratie, wordt een foutbericht weergegeven waarin wordt aangegeven dat het hoofdteam ontbreekt.

    Ga naar **Instellingen** &gt; **Beveiliging** &gt; **Teams**, selecteer het relevante team, selecteer **Rollen beheren** en selecteer een rol met de gewenste machtigingen, bijvoorbeeld **Systeembeheerder**.

- Ga naar **Instellingen** &gt; **Beheer** &gt; **Systeeminstellingen** &gt; **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:

    - De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.
    - Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.

### <a name="setup-in-finance-and-operations"></a>Instellingen In Finance and Operations

- Ga naar **Verkoopbeheer en marketing** &gt; **Periodieke taken** &gt; **Verkooptotalen berekenen** en stel de taak zo in dat deze wordt uitgevoerd als batchtaak. Stel de optie **Totalen berekenen voor verkooporders** in op **Ja**. Deze stap is belangrijk omdat alleen verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd naar Sales. De frequentie van de batchtaak moet worden uitgelijnd met de frequentie van de verkoopordersynchronisatie.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Instellingen in het project Gegevensintegratie voor verkooporders (Sales naar Fin and Ops) - Direct

- Zorg ervoor dat de vereiste toewijzing bestaat voor **Shipto\_country** naar **DeliveryAddressCountryRegionISOCode**. U kunt een lege standaardwaarde in de waardetoewijzing instellen om geen land te hoeven typen voor nationale orders. Stel de linkerkant in op Leeg en stel de rechterkant in op het gewenste land of de gewenste regio.

    De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen en waarbij Leeg = VS.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Instellingen in het project Gegevensintegratie voor verkooporders (Fin and Ops naar Sales) - Direct

#### <a name="salesheader-task"></a>Taak SalesHeader

- Een prijslijst is vereist voor het maken van orders in Sales. Werk de waardetoewijzing voor **pricelevelid.name \[Price List Name\]** per valuta bij naar de gebruikte prijslijst in Sales. U kunt de standaardprijslijst gebruiken voor één valuta. Als u prijslijsten in meerdere valuta's hebt, kunt u een waardetoewijzing gebruiken.

    De standaardsjabloonwaarde van de sjabloon voor **pricelevelid.name \[Price List Name\]** is **CRM Service USA (voorbeeld)**.

#### <a name="salesline-task"></a>Taak SalesLine

- Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Finance and Operations bestaat.
- Zorg ervoor dat de vereiste eenheden zijn gedefinieerd in Sales.

    Er wordt een sjabloonwaarde met een waardetoewijzing voor **SalesUnitSymbol** naar **oumid.name** gedefinieerd.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

> [!NOTE]
> De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie.

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Finance and Operations of andersom worden gesynchroniseerd.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Verkooporders (Fin and Ops naar Sales) - Direct: OrderHeader

[![Sjabloontoewijzing in Gegevensintegratie](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Verkooporders (Fin and Ops naar Sales) - Direct: OrderLine

[![Sjabloontoewijzing in Gegevensintegratie](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Verkooporders (Sales naar Fin and Ops) - Direct: OrderHeader

[![Sjabloontoewijzing in Gegevensintegratie](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Verkooporders (Sales naar Fin and Ops) - Direct: OrderLine

[![Sjabloontoewijzing in Gegevensintegratie](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Verwante onderwerpen

[Prospect naar contant geld](prospect-to-cash.md)

