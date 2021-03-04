---
title: Problemen met prijzen, kortingen, overeenkomsten en aftrek oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met prijzen, kortingen, overeenkomsten en aftrek.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b4349eeba285492202b5df8481b277a06708a4c8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425867"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>Problemen met prijzen, kortingen, overeenkomsten en aftrek oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met prijzen, kortingen, overeenkomsten en aftrek.

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>Ik kan een inkoopovereenkomst niet koppelen aan een inkooporderregel nadat de inkooporder is gemaakt.

Een inkoopovereenkomst moet aan een inkooporderregel worden gekoppeld wanneer de inkooporder wordt gemaakt. Anders kunnen inkooporderregels niet aan inkoopovereenkomstregels worden gekoppeld.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Welke controle activeert het bericht 'Prijzen en kortingen bijwerken die handmatig zijn ingevoerd of extern document'?

Wanneer u de verzenddatum wijzigt, ontvangt u mogelijk het bericht 'Prijzen en kortingen bijwerken die handmatig zijn ingevoerd of extern document'. U ontvangt dit bericht omdat er mogelijk een andere handels- of verkoopovereenkomst wordt geactiveerd als de verzenddatum wordt gewijzigd, wat een prijswijziging kan veroorzaken. Een wijziging van de verzenddatum kan ook van invloed zijn op magazijnplanningen en andere gerelateerde informatie.

Het bericht wordt geactiveerd wanneer een van de datums of andere parameters wordt gewijzigd. Het doel van het bericht is er zeker van te zijn dat u op de hoogte bent van prijswijzigingen die kunnen optreden als gevolg van deze wijzigingen.

Het bericht is de TAE-prompt (handelsovereenkomst). Zie [Evaluatiebeleid voor handelsovereenkomsten](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) voor een volledige beschrijving.

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Een inkooporderontvangst bevat niet alle toeslagen.

### <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Controleer op de pagina **Parameters voor inkoopbeheer** op het tabblad **Levering** op de optie **Toeslagen genereren op productontvangstbon** is ingesteld op *Ja*.
1. Maak een inkooporder die toeslagen bevat.
1. Bevestig de inkooporder.
1. Ontvang de inkooporder.
1. Bekijk het totaal van de ontvangst en vergelijk dit met het verwachte totaal.
1. U ziet dat niet alle toeslagen zijn opgenomen in de inkooporderontvangst.

### <a name="issue-resolution"></a>Probleemoplossing

De oplossing is afhankelijk van de manier waarop de diverse toeslagen zijn ingesteld. Zie het volgende blogbericht voor informatie over het instellen van diverse toeslagen voor uw behoeften: [Diverse toeslagen boeken op het moment van ontvangst van het product](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>Prijzen en kortingen van handelsovereenkomsten worden niet toegepast op verkoop- of inkooporderregels die via gegevensbeheer worden geïmporteerd.

### <a name="issue-description"></a>Probleembeschrijving

Handelsovereenkomsten die van toepassing zijn op verkoop- of inkooporderregels, worden niet toegepast op regels die via gegevensbeheer worden geïmporteerd. Dezelfde handelsovereenkomsten worden echter wel toegepast op verkoop- of inkooporderregels die handmatig zijn gemaakt.

### <a name="reason-for-the-issue"></a>Reden van het probleem

Als inkooporderregels die zijn geïmporteerd via gegevensbeheer al prijsgegevens bevatten, wordt de handelsovereenkomst niet opnieuw geëvalueerd voor deze regels. Als bijvoorbeeld **Regelkortingspercentage** of een van de prijs- en kortingswaarden voor een regel is ingesteld, worden er geen handelsovereenkomsten opgezocht voor die regel.

### <a name="issue-workaround"></a>Tijdelijke oplossing voor probleem

Dit gedrag is verwacht en treedt op voor zowel verkoop- als inkooporders.

U kunt dit probleem vermijden door de inkooporderregels te importeren zonder prijsgegevens in te stellen. De handelsovereenkomsten worden dan toegepast en de inkooporderregels worden bijgewerkt op basis van de gedefinieerde handelsovereenkomsten.

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Een leverancierskorting wordt niet gecumuleerd op basis van facturen.

### <a name="issue-description"></a>Probleembeschrijving

Als facturen die zijn geboekt verschillende vervaldatums hebben, worden deze facturen niet weergegeven in leverancierskortingen die daaruit worden gegenereerd.

### <a name="issue-resolution"></a>Probleemoplossing

Vanuit het ontwerp wordt de vervaldatum niet meegenomen wanneer de leverancierskorting wordt berekend. U zou het systeem zo kunnen aanpassen dat de vervaldatum en de relatie met de factuur duidelijker zijn ten opzichte van de feitelijke leverancierskorting.

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Eenheidsprijzen op inkooporders worden niet berekend op basis van de eenheidsomrekening.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer een eenheid op een inkooporder wordt gewijzigd, worden de prijzen van handelsovereenkomsten niet opnieuw berekend volgens de definities van eenheidsomrekeningen.

### <a name="issue-resolution"></a>Probleemoplossing

Prijzen worden altijd opgehaald uit handelsovereenkomsten (of andere prijsinstellingen in het systeem, zoals verkoopovereenkomsten of artikelprijzen) en worden ingesteld voor een eenheid.

Als de eenheid op een orderregel wordt gewijzigd, zoekt het systeem naar een prijs voor de nieuwe eenheid, waarna die prijs wordt toegepast. Als er geen prijs voor de eenheid wordt gevonden, past het systeem geen prijs toe. De eenheidsomrekening kan niet worden gebruikt om de prijs opnieuw te berekenen in een andere eenheid. Theoretisch gezien zou de prijs voor één doos van tien niet gelijk kunnen zijn aan tien maal de prijs van één doos.

### <a name="issue-workaround"></a>Tijdelijke oplossing voor probleem

Een manier om dit probleem te omzeilen is ervoor te zorgen dat er handelsovereenkomsten bestaan voor de eenheden die u verwacht op orderregels voor het artikel.

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>Er treden valutaomrekeningsfouten op met handelsovereenkomsten.

Handelsovereenkomstprijzen worden niet opnieuw berekend op basis van de valuta als de valuta op een inkooporder verschilt.

Met de functie *Algemene valuta* kunt u prijzen en kortingen in slechts één valuta definiëren. Daarna kunt u naar andere valuta's converteren als dat nodig is. Bovendien kan de functie na de omzetting automatisch slimme afronding toepassen.

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>Wanneer ik de pagina Inkoopovereenkomst in een regelweergavemodus open, kan ik de pagina niet aanpassen door het veld Prijseenheid toe te voegen in het overzicht van de regel.

Een aantal gedeelde velden in het overeenkomstraamwerk kunnen niet worden opgenomen in personalisaties. Deze beperking heeft te maken met het gegevensmodel dat is geïmplementeerd. Hierdoor kunt u het veld **Prijseenheid** niet aanpassen.

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>De maximumlimiet vanuit een inkoopovereenkomst is niet van kracht op een opdracht tot inkoop.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer een opdracht tot inkoop aan een inkoopovereenkomst is gekoppeld, is de maximumlimiet van de inkoopovereenkomst niet van kracht op de opdracht tot inkoop. De standaardprijsgegevens zijn juist ingevoerd, maar in de opdracht tot inkoop kan meer dan de maximumlimiet van de inkoopovereenkomst worden besteld.

### <a name="issue-resolution"></a>Probleemoplossing

Dit gedrag is verwacht. Omdat opdrachten niet altijd worden goedgekeurd, moet een hoeveelheid of aantal niet worden gereserveerd in de inkoopovereenkomst. Daarom voldoet u niet aan de maximumlimiet van de inkoopovereenkomst.

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>Er kunnen geen handelsovereenkomsten worden gemaakt vanuit afgewezen offerteaanvragen. Daarom voorkomt het systeem niet dat handelsovereenkomstjournalen worden gemaakt als de offerteaanvraagregel niet wordt geaccepteerd.

U kunt handelsovereenkomsten maken voor eventuele antwoorden op een offerteaanvraag (RFQ), ongeacht of deze zijn geaccepteerd of afgewezen. Zie [Overzicht van Offerteaanvragen](request-quotations.md) voor meer informatie.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]