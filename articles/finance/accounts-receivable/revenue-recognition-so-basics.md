---
title: Opbrengsttoerekening op verkooporders
description: In dit artikel wordt de basisfunctionaliteit beschreven voor het toerekenen van opbrengst op verkooporders en facturen. Opbrengsttoerekening is beschikbaar op de verkooporder en op de bijbehorende factuur die op basis van de verkooporder wordt gemaakt.
author: bking
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: bb031b41c07aaff06b41830fb0c322503e9f27ec
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348233"
---
# <a name="revenue-recognition-on-sales-orders"></a>Opbrengsttoerekening op verkooporders

[!include [banner](../includes/banner.md)]

> [!NOTE]
> De functie voor opbrengsttoerekening kan niet worden ingeschakeld via Functiebeheer. Momenteel moet u configuratiesleutels gebruiken om deze functie in te schakelen.

In dit artikel wordt de basisfunctionaliteit beschreven voor het toerekenen van opbrengst op verkooporders en facturen. Opbrengsttoerekening is beschikbaar op een verkooporder en op de bijbehorende factuur die op basis van de verkooporder wordt gemaakt. De verkooporder kan ook worden gemaakt via een tijd- en materiaalproject.

> [!NOTE]
> In de afbeeldingen in dit artikel zijn kolommen in rasters verborgen of eraan toegevoegd om de concepten beter te kunnen weergeven. Daarom kunnen de pagina's en gegevens in de afbeeldingen afwijken van wat u in het product ziet.

## <a name="enter-a-sales-order"></a>Een verkooporder invoeren

De volgende verkooporder wordt ingevoerd en bevat drie artikelen die zijn ingesteld voor opbrengsttoerekening.

[![Een verkooporder invoeren.](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Er zijn twee concepten voor het toerekenen van opbrengst:

- **De opbrengstprijs bepalen.** De opbrengstprijs wordt berekend op basis van de instellingen voor de vrijgegeven producten. De opbrengstprijs wordt nooit aan de klant getoond, maar wordt alleen gebruikt voor de boekhoudkundige verwerking van de verkooporderfactuur. Op de verkooporderregels en de documenten die worden afgedrukt als onderdeel van de verkoop, blijven de eenheidsprijs/catalogusprijs zichtbaar.
- **Bepalen wanneer opbrengsttoerekening moet plaatsvinden.** Een opbrengstschema wordt gebruikt om te bepalen wanneer de opbrengst moet worden toegerekend.

    In dit voorbeeld wordt het eerste artikel, S0001, toegewezen aan een opbrengstschema van **1O** (één voorval). Deze regel vertegenwoordigt een scenario van het type mijlpaal waarin de opbrengst wordt toegerekend nadat de installatie in de toekomst heeft plaatsgevonden. Daarom zal de opbrengst worden uitgesteld totdat de installatie is voltooid.

    Het tweede artikel, S0008, is een serviceartikel dat is ingesteld als een PCS-artikel (Contractondersteuning boeken). De doorlopende technische diensten worden over een periode van twaalf maanden aan de klant geleverd. Daarom wordt standaard een opbrengstschema **12M** aan het product toegewezen. Omdat dit artikel een PCS-artikel is, moeten de begin- en einddatum van het contract worden gedefinieerd. De begin- en einddatum van het contract zijn standaard bij de artikelgegevens te vinden – tabblad Instellingen. In het opbrengstschema wordt de instelling voor **12M** opgegeven, zodat de contractvoorwaarden automatisch worden ingevuld, zoals wordt weergegeven in de volgende afbeelding.

    [![Opbrengstschema's.](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Het derde artikel, S0012, is hardware en er wordt standaard geen opbrengstschema toegewezen. De opbrengst van de hardware wordt toegerekend zodra het artikel wordt gefactureerd.

## <a name="confirm-the-sales-order"></a>De verkooporder bevestigen

Als u meer details wilt zien over de opbrengstprijs en het opbrengstschema, kunt u daarvoor de knoppen in de groep **Opbrengsttoerekening** op het tabblad **Beheren** in het actiepaneel van de verkooporder gebruiken. Omdat de verkooporder op dit moment niet is bevestigd, zijn de knoppen die voor opbrengsttoerekening worden gebruikt niet beschikbaar. Deze knoppen worden beschikbaar of niet beschikbaar tijdens de verschillende fasen die de verkooporder doorloopt totdat deze is afgehandeld.

[![Koptekst van verkooporder.](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

De eerste drie knoppen kunnen worden gebruikt voor het weergeven van informatie over de opbrengstprijs voor de artikelen op de verkooporder die zijn ingesteld voor opbrengsttoerekening.

- **Opbrengstprijstoewijzing**: deze knop wordt beschikbaar nadat de verkooporder is bevestigd of de factuur is geboekt. Zowel tijdens de verkooporderbevestiging als de factuurboeking wordt de opbrengst berekend om de prijs toe te rekenen die wordt toegerekend of uitgesteld op de journaalregel. Afhankelijk van de instellingen kan de opbrengstprijs die wordt berekend verschillen van de eenheidsprijs die voor de klant wordt weergegeven.
- **Prijs opnieuw toewijzen bij nieuwe orderregels**: deze knop wordt beschikbaar nadat de verkooporder is bevestigd of de factuur is geboekt. Het hertoewijzingsproces wordt gebruikt om de opbrengst opnieuw te berekenen die moet worden toegerekend nadat een nieuwe regel is toegevoegd aan de huidige verkooporder nadat deze is gefactureerd, of aan een nieuwe verkooporder. In beide scenario's veroorzaakt de toevoeging van een nieuw artikel een wijziging in het contract. Daarom moet de opbrengstprijs opnieuw worden toegewezen.
- **Opbrengstprijstoewijzing bijwerken**: deze knop wordt beschikbaar nadat de verkooporder is bevestigd, maar wordt niet meer weergegeven nadat de verkooporder is gefactureerd. Deze bijwerkactie wordt gebruikt om de toewijzing van de opbrengstprijs opnieuw uit te voeren zonder dat de verkooporder hoeft te worden bevestigd. Nadat de verkooporder is gefactureerd, kan de opbrengstprijs niet opnieuw worden berekend.

De laatste twee knoppen bieden informatie over het opbrengstschema voor de artikelen op de verkooporder waarvoor een opbrengstschema bestaat.

- **Schema voor verwachte opbrengsttoerekening**: deze knop wordt beschikbaar nadat de verkooporder is bevestigd, maar wordt niet meer weergegeven nadat de verkooporder is gefactureerd. Er wordt een pagina geopend waarop het schema met de verwachte opbrengst wordt weergegeven. Het definitieve schema kan veranderen omdat in het schema met de verwachte opbrengst de gewenste verzenddatum wordt gebruikt, terwijl in het definitieve schema de werkelijke verzenddatum wordt gebruikt.
- **Opbrengsttoerekeningsschema**: deze knop wordt beschikbaar nadat de verkooporder is gefactureerd. Het definitieve schema voor de toerekening van opbrengst wordt niet gemaakt wanneer er een bevestiging wordt gegeven of wanneer een pakbon wordt gemaakt. Dit wordt alleen gemaakt als de verkooporder wordt gefactureerd.

In het volgende voorbeeld is de opbrengstprijs toegewezen toen de verkooporder werd bevestigd. Hoewel de opbrengstprijzen anders worden toegewezen, moet het totale bedrag in het veld **Opbrengst voor toerekening** nog steeds gelijk zijn aan de som van de verkooporderregels die aan de klant worden gefactureerd. De som van de verkooporderregels, exclusief btw, is bijvoorbeeld € 1499. Daarom moet de som van de waarden bij **Opbrengst voor toerekening** ook € 1499 zijn.

[![Opbrengstprijstoewijzing.](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Het schema voor de verwachte toerekening van opbrengst wordt ook gemaakt. In het opbrengstschema wordt de waarde bij **Opbrengst voor toerekening** gebruikt als het bedrag dat moet worden uitgesteld. Voor artikel S0001 wordt € 321,21 in plaats van € 300 uitgesteld, en voor artikel S0008 wordt € 160,61 in plaats van € 100 uitgesteld. Artikel S0012 wordt niet weergegeven in het schema met de verwachte opbrengst omdat de opbrengst niet wordt uitgesteld. Bij het boeken wordt voor artikel S0012 € 1017,18 rechtstreeks naar de grootboekrekening voor opbrengst geboekt.

[![Schema voor verwachte opbrengsttoerekening.](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>De pakbon maken

Vervolgens kan de pakbon voor de verkooporder worden gemaakt. Er wordt geen opbrengst toegerekend als de pakbon wordt geboekt. Als de verkooporder niet is bevestigd, wordt de berekening van de opbrengstprijs niet geactiveerd als de pakbon wordt geboekt. Ook het maken van het schema met verwachte of definitieve opbrengsttoerekening wordt hierdoor niet geactiveerd. Als de artikelmodelgroep is ingesteld om de opbrengst op de pakbon uit te stellen, wordt het boeken voortgezet via de huidige grootboekrekeningen van het boekingsprofiel, en niet via de nieuwe rekeningen voor uitgestelde opbrengst die worden gebruikt bij het boeken van de factuur.

## <a name="create-the-invoice"></a>De factuur maken

De laatste stap is het factureren van de verkooporder. Als u het boekstuk van de factuur bekijkt, zult u zien dat de opbrengst voor de artikelen S0001 en S0008 is uitgesteld (€ 321,21 + 160,61 = 481,82) en dat het resterende bedrag voor artikel S0012 is geboekt als opbrengst (1017,18). Deze waarden zijn bij elkaar opgeteld € 1499, wat overeenkomt met de som van de verkooporderregels.

[![Boekstuktransacties.](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Nadat de factuur is gemaakt, worden de knoppen **Opbrengstprijstoewijzing**, **Prijs opnieuw toewijzen bij nieuwe orderregels** en **Opbrengsttoerekeningsschema** voor het toerekenen van opbrengst beschikbaar, maar zijn de knoppen **Opbrengstprijstoewijzing bijwerken** en **Schema voor verwachte opbrengsttoerekening** niet beschikbaar.

[![Beschikbaarheid van knop voor opbrengsttoerekening.](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

De knop **Opbrengstprijstoewijzing** is nog steeds beschikbaar, zodat u de berekening van de opbrengstprijs kunt bekijken. Als er niets is gewijzigd op de verkooporder nadat deze is bevestigd, wordt het berekende bedrag in het veld **Opbrengst voor toerekening** niet gewijzigd als de factuur wordt geboekt.

Het schema voor verwachte opbrengsttoerekening wordt verwijderd en vervangen door het definitieve schema voor opbrengsttoerekening. De details van het opbrengstschema worden bijgehouden voor elke verkooporderregel en worden gebruikt om de uitgestelde opbrengst vrij te geven naar werkelijke opbrengst als aan de contractuele verplichtingen wordt voldaan.

[![Definitieve schema voor opbrengsttoerekening.](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
