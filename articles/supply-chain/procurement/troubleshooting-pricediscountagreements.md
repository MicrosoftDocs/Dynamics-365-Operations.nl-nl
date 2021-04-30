---
title: Problemen met prijzen, kortingen, overeenkomsten en aftrek oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met prijzen, kortingen, overeenkomsten en aftrek.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2ccc1d52b83f9319af1c6336c1876c795c70028a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908514"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="d8617-103">Problemen met prijzen, kortingen, overeenkomsten en aftrek oplossen</span><span class="sxs-lookup"><span data-stu-id="d8617-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="d8617-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden terwijl u werkt met prijzen, kortingen, overeenkomsten en aftrek.</span><span class="sxs-lookup"><span data-stu-id="d8617-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="d8617-105">Ik kan een inkoopovereenkomst niet koppelen aan een inkooporderregel nadat de inkooporder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d8617-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="d8617-106">Een inkoopovereenkomst moet aan een inkooporderregel worden gekoppeld wanneer de inkooporder wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d8617-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="d8617-107">Anders kunnen inkooporderregels niet aan inkoopovereenkomstregels worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d8617-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="d8617-108">Welke controle activeert het bericht 'Prijzen en kortingen bijwerken die handmatig zijn ingevoerd of extern document'?</span><span class="sxs-lookup"><span data-stu-id="d8617-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="d8617-109">Wanneer u de verzenddatum wijzigt, ontvangt u mogelijk het bericht 'Prijzen en kortingen bijwerken die handmatig zijn ingevoerd of extern document'.</span><span class="sxs-lookup"><span data-stu-id="d8617-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="d8617-110">U ontvangt dit bericht omdat er mogelijk een andere handels- of verkoopovereenkomst wordt geactiveerd als de verzenddatum wordt gewijzigd, wat een prijswijziging kan veroorzaken.</span><span class="sxs-lookup"><span data-stu-id="d8617-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="d8617-111">Een wijziging van de verzenddatum kan ook van invloed zijn op magazijnplanningen en andere gerelateerde informatie.</span><span class="sxs-lookup"><span data-stu-id="d8617-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="d8617-112">Het bericht wordt geactiveerd wanneer een van de datums of andere parameters wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="d8617-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="d8617-113">Het doel van het bericht is er zeker van te zijn dat u op de hoogte bent van prijswijzigingen die kunnen optreden als gevolg van deze wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="d8617-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="d8617-114">Het bericht is de TAE-prompt (handelsovereenkomst).</span><span class="sxs-lookup"><span data-stu-id="d8617-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="d8617-115">Zie [Evaluatiebeleid voor handelsovereenkomsten](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) voor een volledige beschrijving.</span><span class="sxs-lookup"><span data-stu-id="d8617-115">For a full description, see [Trade agreement evaluation policies](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="d8617-116">Een inkooporderontvangst bevat niet alle toeslagen.</span><span class="sxs-lookup"><span data-stu-id="d8617-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="d8617-117">Het probleem reproduceren</span><span class="sxs-lookup"><span data-stu-id="d8617-117">Reproduce the issue</span></span>

<span data-ttu-id="d8617-118">In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.</span><span class="sxs-lookup"><span data-stu-id="d8617-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="d8617-119">Controleer op de pagina **Parameters voor inkoopbeheer** op het tabblad **Levering** op de optie **Toeslagen genereren op productontvangstbon** is ingesteld op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="d8617-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="d8617-120">Maak een inkooporder die toeslagen bevat.</span><span class="sxs-lookup"><span data-stu-id="d8617-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="d8617-121">Bevestig de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="d8617-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="d8617-122">Ontvang de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="d8617-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="d8617-123">Bekijk het totaal van de ontvangst en vergelijk dit met het verwachte totaal.</span><span class="sxs-lookup"><span data-stu-id="d8617-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="d8617-124">U ziet dat niet alle toeslagen zijn opgenomen in de inkooporderontvangst.</span><span class="sxs-lookup"><span data-stu-id="d8617-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d8617-125">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d8617-125">Issue resolution</span></span>

<span data-ttu-id="d8617-126">De oplossing is afhankelijk van de manier waarop de diverse toeslagen zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d8617-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="d8617-127">Zie het volgende blogbericht voor informatie over het instellen van diverse toeslagen voor uw behoeften: [Diverse toeslagen boeken op het moment van ontvangst van het product](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="d8617-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="d8617-128">Prijzen en kortingen van handelsovereenkomsten worden niet toegepast op verkoop- of inkooporderregels die via gegevensbeheer worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="d8617-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d8617-129">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d8617-129">Issue description</span></span>

<span data-ttu-id="d8617-130">Handelsovereenkomsten die van toepassing zijn op verkoop- of inkooporderregels, worden niet toegepast op regels die via gegevensbeheer worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="d8617-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="d8617-131">Dezelfde handelsovereenkomsten worden echter wel toegepast op verkoop- of inkooporderregels die handmatig zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d8617-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="d8617-132">Reden van het probleem</span><span class="sxs-lookup"><span data-stu-id="d8617-132">Reason for the issue</span></span>

<span data-ttu-id="d8617-133">Als inkooporderregels die zijn geïmporteerd via gegevensbeheer al prijsgegevens bevatten, wordt de handelsovereenkomst niet opnieuw geëvalueerd voor deze regels.</span><span class="sxs-lookup"><span data-stu-id="d8617-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="d8617-134">Als bijvoorbeeld **Regelkortingspercentage** of een van de prijs- en kortingswaarden voor een regel is ingesteld, worden er geen handelsovereenkomsten opgezocht voor die regel.</span><span class="sxs-lookup"><span data-stu-id="d8617-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="d8617-135">Tijdelijke oplossing voor probleem</span><span class="sxs-lookup"><span data-stu-id="d8617-135">Issue workaround</span></span>

<span data-ttu-id="d8617-136">Dit gedrag is verwacht en treedt op voor zowel verkoop- als inkooporders.</span><span class="sxs-lookup"><span data-stu-id="d8617-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="d8617-137">U kunt dit probleem vermijden door de inkooporderregels te importeren zonder prijsgegevens in te stellen.</span><span class="sxs-lookup"><span data-stu-id="d8617-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="d8617-138">De handelsovereenkomsten worden dan toegepast en de inkooporderregels worden bijgewerkt op basis van de gedefinieerde handelsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="d8617-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="d8617-139">Een leverancierskorting wordt niet gecumuleerd op basis van facturen.</span><span class="sxs-lookup"><span data-stu-id="d8617-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d8617-140">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d8617-140">Issue description</span></span>

<span data-ttu-id="d8617-141">Als facturen die zijn geboekt verschillende vervaldatums hebben, worden deze facturen niet weergegeven in leverancierskortingen die daaruit worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d8617-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d8617-142">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d8617-142">Issue resolution</span></span>

<span data-ttu-id="d8617-143">Vanuit het ontwerp wordt de vervaldatum niet meegenomen wanneer de leverancierskorting wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="d8617-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="d8617-144">U zou het systeem zo kunnen aanpassen dat de vervaldatum en de relatie met de factuur duidelijker zijn ten opzichte van de feitelijke leverancierskorting.</span><span class="sxs-lookup"><span data-stu-id="d8617-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="d8617-145">Eenheidsprijzen op inkooporders worden niet berekend op basis van de eenheidsomrekening.</span><span class="sxs-lookup"><span data-stu-id="d8617-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d8617-146">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d8617-146">Issue description</span></span>

<span data-ttu-id="d8617-147">Wanneer een eenheid op een inkooporder wordt gewijzigd, worden de prijzen van handelsovereenkomsten niet opnieuw berekend volgens de definities van eenheidsomrekeningen.</span><span class="sxs-lookup"><span data-stu-id="d8617-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d8617-148">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d8617-148">Issue resolution</span></span>

<span data-ttu-id="d8617-149">Prijzen worden altijd opgehaald uit handelsovereenkomsten (of andere prijsinstellingen in het systeem, zoals verkoopovereenkomsten of artikelprijzen) en worden ingesteld voor een eenheid.</span><span class="sxs-lookup"><span data-stu-id="d8617-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="d8617-150">Als de eenheid op een orderregel wordt gewijzigd, zoekt het systeem naar een prijs voor de nieuwe eenheid, waarna die prijs wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="d8617-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="d8617-151">Als er geen prijs voor de eenheid wordt gevonden, past het systeem geen prijs toe.</span><span class="sxs-lookup"><span data-stu-id="d8617-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="d8617-152">De eenheidsomrekening kan niet worden gebruikt om de prijs opnieuw te berekenen in een andere eenheid.</span><span class="sxs-lookup"><span data-stu-id="d8617-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="d8617-153">Theoretisch gezien zou de prijs voor één doos van tien niet gelijk kunnen zijn aan tien maal de prijs van één doos.</span><span class="sxs-lookup"><span data-stu-id="d8617-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="d8617-154">Tijdelijke oplossing voor probleem</span><span class="sxs-lookup"><span data-stu-id="d8617-154">Issue workaround</span></span>

<span data-ttu-id="d8617-155">Een manier om dit probleem te omzeilen is ervoor te zorgen dat er handelsovereenkomsten bestaan voor de eenheden die u verwacht op orderregels voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="d8617-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="d8617-156">Er treden valutaomrekeningsfouten op met handelsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="d8617-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="d8617-157">Handelsovereenkomstprijzen worden niet opnieuw berekend op basis van de valuta als de valuta op een inkooporder verschilt.</span><span class="sxs-lookup"><span data-stu-id="d8617-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="d8617-158">Met de functie *Algemene valuta* kunt u prijzen en kortingen in slechts één valuta definiëren.</span><span class="sxs-lookup"><span data-stu-id="d8617-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="d8617-159">Daarna kunt u naar andere valuta's converteren als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="d8617-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="d8617-160">Bovendien kan de functie na de omzetting automatisch slimme afronding toepassen.</span><span class="sxs-lookup"><span data-stu-id="d8617-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="d8617-161">Wanneer ik de pagina Inkoopovereenkomst in een regelweergavemodus open, kan ik de pagina niet aanpassen door het veld Prijseenheid toe te voegen in het overzicht van de regel.</span><span class="sxs-lookup"><span data-stu-id="d8617-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="d8617-162">Een aantal gedeelde velden in het overeenkomstraamwerk kunnen niet worden opgenomen in personalisaties.</span><span class="sxs-lookup"><span data-stu-id="d8617-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="d8617-163">Deze beperking heeft te maken met het gegevensmodel dat is geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="d8617-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="d8617-164">Hierdoor kunt u het veld **Prijseenheid** niet aanpassen.</span><span class="sxs-lookup"><span data-stu-id="d8617-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="d8617-165">De maximumlimiet vanuit een inkoopovereenkomst is niet van kracht op een opdracht tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="d8617-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="d8617-166">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="d8617-166">Issue description</span></span>

<span data-ttu-id="d8617-167">Wanneer een opdracht tot inkoop aan een inkoopovereenkomst is gekoppeld, is de maximumlimiet van de inkoopovereenkomst niet van kracht op de opdracht tot inkoop.</span><span class="sxs-lookup"><span data-stu-id="d8617-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="d8617-168">De standaardprijsgegevens zijn juist ingevoerd, maar in de opdracht tot inkoop kan meer dan de maximumlimiet van de inkoopovereenkomst worden besteld.</span><span class="sxs-lookup"><span data-stu-id="d8617-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="d8617-169">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="d8617-169">Issue resolution</span></span>

<span data-ttu-id="d8617-170">Dit gedrag is verwacht.</span><span class="sxs-lookup"><span data-stu-id="d8617-170">This behavior is expected.</span></span> <span data-ttu-id="d8617-171">Omdat opdrachten niet altijd worden goedgekeurd, moet een hoeveelheid of aantal niet worden gereserveerd in de inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="d8617-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="d8617-172">Daarom voldoet u niet aan de maximumlimiet van de inkoopovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="d8617-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="d8617-173">Er kunnen geen handelsovereenkomsten worden gemaakt vanuit afgewezen offerteaanvragen.</span><span class="sxs-lookup"><span data-stu-id="d8617-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="d8617-174">Daarom voorkomt het systeem niet dat handelsovereenkomstjournalen worden gemaakt als de offerteaanvraagregel niet wordt geaccepteerd.</span><span class="sxs-lookup"><span data-stu-id="d8617-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="d8617-175">U kunt handelsovereenkomsten maken voor eventuele antwoorden op een offerteaanvraag (RFQ), ongeacht of deze zijn geaccepteerd of afgewezen.</span><span class="sxs-lookup"><span data-stu-id="d8617-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="d8617-176">Zie [Overzicht van Offerteaanvragen](request-quotations.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d8617-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]