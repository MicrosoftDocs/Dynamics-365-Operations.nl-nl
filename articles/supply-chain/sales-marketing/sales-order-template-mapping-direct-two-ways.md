---
title: Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren
description: Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt voor het synchroniseren van verkooporders tussen Dynamics 365 Sales en Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 05/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 3eaa25f0befcff448250ba2cce8e568fa4a4c707
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425637"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren

[!include [banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt voor het synchroniseren van verkooporders tussen Dynamics 365 Sales en Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Gegevensstroom in Prospect naar contant geld

De oplossing Prospect naar contant geld gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Supply Chain Management en Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Supply Chain Management en Sales. De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Supply Chain Management en Sales.

[![Gegevensstroom in Prospect naar contant geld](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Open het [Power Apps-beheercentrum](https://preview.admin.powerapps.com/dataintegration) om toegang te krijgen tot de beschikbare sjablonen. Selecteer **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjablonen en onderliggende taken worden gebruikt voor het direct synchroniseren van verkooporders tussen Sales en Supply Chain Management.

- **Namen van de sjablonen in Gegevensintegratie:** 

    - Verkooporders (Sales naar Supply Chain Management) - Direct
    - Verkooporders (Supply Chain Management naar Sales) - Direct

- **Namen van de taken in het project Gegevensintegratie:**

    - OrderHeader
    - OrderLine

De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopfacturen kan plaatsvinden:

- Producten (Supply Chain Management naar Sales) - Direct
- Rekeningen (Supply Chain Management naar Sales) - Direct (wanneer gebruikt)
- Contactpersonen naar klanten (Sales naar Supply Chain Management) - Direct (indien gebruikt)

## <a name="entity-set"></a>Entiteitset

| Supply Chain Management  | Verkoop             |
|-------------------------|-------------------|
| CDS-verkooporderkopteksten | SalesOrders       |
| CDS-verkooporderregels   | SalesOrderDetails |

## <a name="entity-flow"></a>Entiteitstroom

Verkooporders worden gemaakt in Sales en gesynchroniseerd naar Supply Chain Management als **Project uitvoeren** voor een project wordt geactiveerd op basis van de sjabloon **Verkooporders (Sales naar Supply Chain Management) - Direct**. U kunt verkooporders alleen vanuit Sales activeren en synchroniseren als alle **orderproducten** volledig uit extern beheerde producten bestaan. Er kunnen dus geen toe te voegen producten zijn. Nadat de order is geactiveerd, wordt de verkooporder alleen-lezen in de gebruikersinterface (UI). Op dat moment worden de updates uitgevoerd vanuit Supply Chain Management. Als de verkooporder de status **Bevestigd** heeft, kan het project op basis van de sjabloon **Verkooporders (Supply Chain Management naar Sales) - Direct** worden gebruikt om updates of de afhandelingsstatus vanuit Supply Chain Management te synchroniseren naar Sales.

U hoeft geen orders in Sales te maken. U kunt in plaats daarvan nieuwe verkooporders in Supply Chain Management maken. Als een verkooporder de status **Bevestigd** heeft, wordt deze gesynchroniseerd naar Sales, zoals wordt beschreven in de vorige alinea.

In Supply Chain Management zorgen filters in de sjabloon ervoor dat alleen de relevante verkooporders worden opgenomen in de synchronisatie:

- Als zowel de bestellende als de facturerende klant op de verkooporder uit Sales afkomstig is, worden beide opgenomen in de synchronisatie. In Supply Chain Management worden de velden **OrderingCustomerIsExternallyMaintained** en **InvoiceCustomerIsExternallyMaintained** gebruikt om verkooporders te filteren op basis van de gegevensentiteiten.
- De verkooporder in Supply Chain Management moet worden bevestigd. Alleen bevestigde verkooporders of verkooporders met een hogere verwerkingsstatus, bijvoorbeeld met de status **Verzonden** of **Gefactureerd**, worden gesynchroniseerd naar Sales.
- Na het maken of wijzigen van een verkooporder moet de batchtaak **Verkooptotalen berekenen** in Supply Chain Management worden uitgevoerd. Alleen verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd naar Sales.

## <a name="freight-tax"></a>Transportbelasting

Sales ondersteunt geen btw op koptekstniveau omdat btw op regelniveau wordt opgeslagen. Om belastingen op koptekstniveau te ondersteunen vanuit Supply Chain Management, bijvoorbeeld vrachtbelastingen, worden de belastingen gesynchroniseerd naar Sales als toe te voegen product met de naam **Transportbelasting** dat het belastingbedrag van Supply Chain Management heeft. Op deze manier kan de standaardprijsberekening in Sales worden gebruikt om totalen te berekenen, zelfs als er belastingen op koptekstniveau aanwezig zijn vanuit Supply Chain Management.

## <a name="discount-calculation-and-rounding"></a>Berekening en afronding van korting

Het model voor het berekenen van korting in Sales wijkt af van het model voor het berekenen van korting in Supply Chain Management. In Supply Chain Management kan het uiteindelijke kortingsbedrag op een verkoopregel het resultaat zijn van een combinatie van kortingsbedragen en -percentages. Als dit uiteindelijke kortingsbedrag wordt gedeeld door de hoeveelheid op de regel, kan er afronding plaatsvinden. Deze afronding wordt echter niet gebruikt als een afgerond kortingsbedrag per eenheid wordt gesynchroniseerd naar Sales. Het volledige kortingsbedrag op een verkoopregel in Supply Chain Management kan alleen correct worden gesynchroniseerd naar Sales als het volledige bedrag wordt gesynchroniseerd, zonder het te delen door de regelhoeveelheid. Daarom moet u in Sales de optie **Berekeningsmethode korting** instellen op **Regelartikel**.

Als een verkooporderregel vanuit Sales naar Supply Chain Management wordt gesynchroniseerd, wordt het volledige regelkortingsbedrag gebruikt. Omdat in Supply Chain Management geen veld beschikbaar is waarin het volledige kortingsbedrag voor een regel kan worden opgeslagen, wordt het bedrag gedeeld door de hoeveelheid en opgeslagen in het veld **Regelkorting**. Afronding die tijdens deze deling plaatsvindt, wordt opgeslagen in het veld **Verkooptoeslagen** op de verkoopregel.

### <a name="example"></a>Voorbeeld

**Synchronisatie van Sales naar Supply Chain Management**

- **Sales:** Hoeveelheid = 3, korting per regel = € 10,00
- **Supply Chain Management:** Hoeveelheid = 3, regel kortingsbedrag = $ 3,33, verkoopkosten =-$ 0,01 

**Synchronisatie van Supply Chain Management naar Sales**

- **Supply Chain Management:** Hoeveelheid = 3, regel kortingsbedrag = $ 3,33, verkoopkosten =-$ 0,01
- **Sales:** Hoeveelheid = 3, korting per regel = = (3 × € 3,33) + € 0,01 = € 10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Nieuwe velden zijn toegevoegd aan de entiteit **Order** en worden weergegeven op de pagina:

- **Wordt extern beheerd** – stel deze optie in op **Ja** wanneer de order afkomstig is uit Supply Chain Management.
- **Verwerkingsstatus** – in dit veld wordt de verwerkingsstatus weergegeven van de order in Supply Chain Management. De volgende waarden zijn beschikbaar:

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

De instelling **Heeft alleen extern onderhouden producten** wordt tijdens orderactivering gebruikt om consistent bij te houden of een verkooporder geheel bestaat uit extern beheerde producten. Als een verkooporder alleen uit extern beheerde producten bestaat, worden de producten beheerd in Supply Chain Management. Met deze instelling garandeert u dat u niet verkooporderregels probeert te activeren en te synchroniseren die producten bevatten die onbekend zijn in Supply Chain Management.

Voor extern beheerde orders zijn de knoppen **Factuur maken**, **Order annuleren**, **Opnieuw berekenen**, **Producten ophalen** en **Adres opzoeken** op de pagina **Verkooporder** verborgen omdat facturen worden gemaakt in Supply Chain Management en vervolgens worden gesynchroniseerd naar Sales. Deze orders kunnen niet worden bewerkt omdat verkoopordergegevens na activering vanuit Supply Chain Management worden gesynchroniseerd.

De verkooporderstatus blijft **Actief** om ervoor te zorgen dat wijzigingen vanuit Supply Chain Management naar de verkooporder in Sales kunnen stromen. U stelt dit gedrag in door de standaardwaarde voor **Statuscode \[Status\]** op **Actief** in te stellen in het project Gegevensintegratie.

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

Voordat u verkooporders synchroniseert, is het belangrijk de volgende instellingen in de systemen bij te werken.

### <a name="setup-in-sales"></a>Instellingen in Sales

- Zorg ervoor dat er machtigingen zijn ingesteld voor het team waaraan de gebruiker uit uw verbindingsset in Sales is toegewezen. Als u voorbeeldgegevens gebruikt, heeft de gebruiker meestal beheerderstoegang, maar het team niet. Als het team geen beheerderstoegang heeft wanneer u het project uitvoert vanuit Gegevensintegratie, wordt een foutbericht weergegeven waarin wordt aangegeven dat het hoofdteam ontbreekt.

    Ga naar **Instellingen** &gt; **Beveiliging** &gt; **Teams**, selecteer het relevante team, selecteer **Rollen beheren** en selecteer een rol met de gewenste machtigingen, bijvoorbeeld **Systeembeheerder**.

- Voor een juiste berekening van kortingen in Sales en Supply Chain Management moet de **Berekeningsmethode voor korting** zijn ingesteld op **Regelartikel**.
- Ga naar **Instellingen** &gt; **Beheer** &gt; **Systeeminstellingen** &gt; **Sales** en zorg ervoor dat de volgende instellingen worden gebruikt:

    - De optie **Systeem voor berekenen van systeemprijzen gebruiken** is ingesteld op **Ja**.
    - Het veld **Berekeningsmethode korting** is ingesteld op **Regelartikel**.

### <a name="setup-in-supply-chain-management"></a>Supply Chain Management instellen

- Ga naar **Verkoopbeheer en marketing** &gt; **Periodieke taken** &gt; **Verkooptotalen berekenen** en stel de taak zo in dat deze wordt uitgevoerd als batchtaak. Stel de optie **Totalen berekenen voor verkooporders** in op **Ja**. Deze stap is belangrijk omdat alleen verkooporders waarvoor verkooptotalen zijn berekend, worden gesynchroniseerd naar Sales. De frequentie van de batchtaak moet worden uitgelijnd met de frequentie van de verkoopordersynchronisatie.

Als u ook integratie werkorder gebruikt, moet u de verkoopoorsprong instellen. De verkoopoorsprong wordt gebruikt om onderscheid te maken tussen verkooporders in Supply Chain Management die zijn gemaakt op basis van werkorders in Field Service. Wanneer een verkooporder een verkoopoorsprong heeft van het type **Integratie werkorder**, wordt het veld **Externe werkorderstatus** weergegeven in de verkooporderkoptekst. Bovendien zorgt de verkoopoorsprong ervoor dat verkooporders die zijn gemaakt op basis van werkorders in Field Service worden uitgefilterd tijdens de synchronisatie van verkooporders van Supply Chain Management naar Field Service.

1. Ga naar **Verkoop en marketing** \> **Instellen** \> **Verkooporders** \> **Verkoopoorsprong**.
2. Selecteer **Nieuw** voor het maken van een nieuwe verkoopoorsprong.
3. Voer in het veld **Verkoopoorsprong** een naam in voor de verkoopoorsprong, zoals **Verkooporder**.
4. Voer in het veld **Beschrijving** een beschrijving in, zoals **Verkooporder vanuit Sales**.
5. Schakel het selectievakje **Toewijzing van oorsprongtype** in.
6. Stel het veld **Type verkoopoorsprong** in op **Integratie verkooporder**.
7. Selecteer **Opslaan**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Instellingen in het project Gegevensintegratie voor Verkooporders (Sales naar Supply Chain Management) - Direct

- Zorg ervoor dat de vereiste toewijzing bestaat voor **Shipto\_country** naar **DeliveryAddressCountryRegionISOCode**. U kunt een lege standaardwaarde in de waardetoewijzing instellen om geen land te hoeven typen voor nationale orders. Stel de linkerkant in op Leeg en stel de rechterkant in op het gewenste land of de gewenste regio.

    De sjabloonwaarde is een toewijzingswaarde waarbij verschillende landen of regio's worden toegewezen en waarbij Leeg = VS.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Instellingen in het project Gegevensintegratie voor Verkooporders (Supply Chain Management naar Salest) - Direct

#### <a name="salesheader-task"></a>Taak SalesHeader

- Een prijslijst is vereist voor het maken van orders in Sales. Werk de waardetoewijzing voor **pricelevelid.name \[Price List Name\]** per valuta bij naar de gebruikte prijslijst in Sales. U kunt de standaardprijslijst gebruiken voor één valuta. Als u prijslijsten in meerdere valuta's hebt, kunt u een waardetoewijzing gebruiken.

    De standaardsjabloonwaarde van de sjabloon voor **pricelevelid.name \[Price List Name\]** is **CRM Service USA (voorbeeld)**.

#### <a name="salesline-task"></a>Taak SalesLine

- Zorg ervoor dat de vereiste waardetoewijzing voor **SalesUnitSymbol** in Supply Chain Management bestaat.
- Zorg ervoor dat de vereiste eenheden zijn gedefinieerd in Sales.

    Er wordt een sjabloonwaarde met een waardetoewijzing voor **SalesUnitSymbol** naar **oumid.name** gedefinieerd.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

> [!NOTE]
> De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van sjabloontoewijzing in Gegevensintegratie.

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Sales naar Supply Chain Management of andersom worden gesynchroniseerd.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Verkooporders (Supply Chain Management naar Sales) - Direct: OrderHeader

[![Sjabloontoewijzing in Gegevensintegratie](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Verkooporders (Supply Chain Management naar Sales) - Direct: OrderLine

[![Sjabloontoewijzing in Gegevensintegratie](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Verkooporders (Sales naar Supply Chain Management) - Direct: OrderHeader

[![Sjabloontoewijzing in Gegevensintegratie](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Verkooporders (Sales naar Supply Chain Management) - Direct: OrderLine

[![Sjabloontoewijzing in Gegevensintegratie](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Verwante onderwerpen

[Prospect naar contant geld](prospect-to-cash.md)
