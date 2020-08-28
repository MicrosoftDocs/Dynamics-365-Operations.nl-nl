---
title: Klantorders in Modern POS (MPOS)
description: Dit onderwerp biedt informatie over klantorders in Modern POS (MPOS). Klantorders worden ook wel speciale orders genoemd. In dit onderwerp worden de gerelateerde parameters en transactiestromen besproken.
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 87d1217204e0c5cb22f567793b043bf399ca5685
ms.sourcegitcommit: b07434f2bd6db67d8dd712f096329acc902751ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699364"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="2d8fc-105">Klantorders in Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="2d8fc-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d8fc-106">Dit onderwerp biedt informatie over klantorders in Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="2d8fc-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="2d8fc-107">Klantorders worden ook wel speciale orders genoemd.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="2d8fc-108">In dit onderwerp worden de gerelateerde parameters en transactiestromen besproken.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="2d8fc-109">Veel detailhandelaren bieden de optie van klantorders, oftewel speciale orders, om aan verschillende product- en afhandelingsbehoeften te voldoen.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="2d8fc-110">Hierna vindt u enkele typische scenario's:</span><span class="sxs-lookup"><span data-stu-id="2d8fc-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="2d8fc-111">Een klant wil dat de producten worden afgeleverd op een specifiek adres op een specifieke datum.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="2d8fc-112">Een klant wil producten bij een andere winkel of locatie ophalen dan de winkel of locatie waar de klant deze producten heeft gekocht.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="2d8fc-113">Een klant wil dat iemand anders de gekochte producten ophaalt.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="2d8fc-114">Detailhandelaren gebruiken klantorders ook om verloren verkoop te minimaliseren waarmee anders voorraadtekorten kunnen worden veroorzaakt, omdat de producten op een ander tijdstip of een andere plaats kunnen worden afgeleverd of opgehaald.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="2d8fc-115">Klantorders instellen</span><span class="sxs-lookup"><span data-stu-id="2d8fc-115">Set up customer orders</span></span>

<span data-ttu-id="2d8fc-116">Hierna vindt u enkele parameters die kunnen worden ingesteld op de pagina **Commerce-parameters** om te definiëren hoe klantorders worden afgehandeld:</span><span class="sxs-lookup"><span data-stu-id="2d8fc-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="2d8fc-117">**Standaard aanbetalingspercentage**: geef het bedrag op dat de klant moet betalen als een aanbetaling voordat een order kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="2d8fc-118">Het standaardaanbetalingsbedrag wordt als een percentage van de orderwaarde berekend.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="2d8fc-119">Afhankelijk van de bevoegdheden kan een winkelmedewerker het bedrag overschrijven met behulp van **Deposito overschrijven**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="2d8fc-120">**Percentage annuleringskosten**: als een toeslag wordt toegepast wanneer een klantorder wordt geannuleerd, geeft u het bedrag van die toeslag op.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="2d8fc-121">**Code annuleringskosten**: als een toeslag wordt toegepast wanneer een klantorder wordt geannuleerd, wordt die toeslag weergegeven onder een toeslagcode in de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="2d8fc-122">Met deze parameter kunt u de annuleringstoeslagcode definiëren.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="2d8fc-123">**Code verzendkosten**: detailhandelaren kunnen extra kosten in rekening brengen voor het verzenden van producten aan een klant.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="2d8fc-124">Het bedrag van de verzendkosten wordt weergegeven onder een toeslagcode in de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="2d8fc-125">Gebruik deze parameter om de verzendkostencode toe te wijzen aan verzendkosten op de klantorder.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="2d8fc-126">**Verzendkosten terugbetalen**: geef op of verzendkosten die zijn gekoppeld aan een klantorder, kunnen worden gerestitueerd.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="2d8fc-127">**Maximumbedrag zonder toestemming**: als de verzendkosten kunnen worden gerestitueerd, geeft u het maximale bedrag van verzendkostenrestituties voor retourorders op.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="2d8fc-128">Als dit bedrag wordt overschreden, is overschrijving door de manager nodig is om met de restitutie te kunnen doorgaan.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="2d8fc-129">Voor de volgende scenario's kan restitutie van verzendkosten hoger zijn dan het bedrag dat oorspronkelijk is betaald:</span><span class="sxs-lookup"><span data-stu-id="2d8fc-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="2d8fc-130">Kosten worden toegepast op het niveau van de verkooporderkoptekst en wanneer een bepaalde hoeveelheid van een productregel wordt geretourneerd, kan de maximale restitutie van verzendkosten die is toegestaan voor de producten en de hoeveelheid, niet worden bepaald op een manier die werkt voor alle klanten.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="2d8fc-131">Verzendkosten worden voor elke verzending gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="2d8fc-132">Als een klant producten meerdere keren retourneert en de detailhandelaar volgens het detailhandelaarsbeleid de kosten van gerestitueerde verzendkosten voor rekening neemt, zijn de gerestitueerde verzendkosten hoger dan de werkelijke verzendkosten.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    
- <span data-ttu-id="2d8fc-133">**Btw-berekeningsgedrag** - **Opnieuw berekenen** is de standaardwaarde en de traditionele instelling voor de manier waarop btw wordt herberekend wanneer de order wordt geïmporteerd in het back-office.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-133">**Tax calculation behavior** - **Recalculate** is the default and traditional setting for how taxes are recalculated when the order is imported into the back office.</span></span> <span data-ttu-id="2d8fc-134">Met **Niet opnieuw berekenen** wordt de btw niet opnieuw berekend tot of tenzij de order wordt bewerkt in het back-office, wanneer de herberekening wordt geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-134">**Don't recalculate** disables tax recalculation until or unless the order is edited in the back office, when recalculation is triggered.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="2d8fc-135">Transactiestroom voor klantorders</span><span class="sxs-lookup"><span data-stu-id="2d8fc-135">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="2d8fc-136">Een klantorder maken in Modern POS</span><span class="sxs-lookup"><span data-stu-id="2d8fc-136">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="2d8fc-137">Voeg een klant aan de transactie toe.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-137">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="2d8fc-138">Voeg producten aan de winkelwagen toe.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-138">Add products to the cart.</span></span>
3. <span data-ttu-id="2d8fc-139">Klik op **Klantorder maken** en selecteer vervolgens het ordertype.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-139">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="2d8fc-140">Het ordertype kan een **Klantorder** of **Offerte** zijn.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-140">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="2d8fc-141">Klik op **Selectie verzenden** of **Alles verzenden** als u de producten wilt verzenden naar een adres op de klantrekening, geef de gevraagde verzenddatum en de verzendkosten op.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-141">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="2d8fc-142">Klik op **Selectie ophalen** of **Alles ophalen** om producten te selecteren die worden opgehaald vanuit de huidige winkel of een andere winkel op een bepaalde datum.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-142">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="2d8fc-143">Het gestorte bedrag innen als een aanbetaling vereist is.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-143">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="2d8fc-144">Een bestaande klantorder bewerken</span><span class="sxs-lookup"><span data-stu-id="2d8fc-144">Edit an existing customer order</span></span>

1. <span data-ttu-id="2d8fc-145">Klik op de startpagina op **Een order zoeken**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-145">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2d8fc-146">Zoek en selecteer de order om te bewerken.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-146">Find and select the order to edit.</span></span> <span data-ttu-id="2d8fc-147">Klik onder aan de pagina op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-147">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="2d8fc-148">Een order ophalen</span><span class="sxs-lookup"><span data-stu-id="2d8fc-148">Pick up an order</span></span>

1. <span data-ttu-id="2d8fc-149">Klik op de startpagina op **Een order zoeken**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2d8fc-150">Selecteer de order die moet worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-150">Select the order to pick up.</span></span> <span data-ttu-id="2d8fc-151">Klik onder aan de pagina op **Verzamelen en verpakken**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-151">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="2d8fc-152">Klik op **Ophalen**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-152">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="2d8fc-153">Een order annuleren</span><span class="sxs-lookup"><span data-stu-id="2d8fc-153">Cancel an order</span></span>

1. <span data-ttu-id="2d8fc-154">Klik op de startpagina op **Een order zoeken**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-154">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2d8fc-155">Selecteer de order die u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-155">Select the order to cancel.</span></span> <span data-ttu-id="2d8fc-156">Klik onder aan de pagina op **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-156">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="2d8fc-157">Retourorder maken</span><span class="sxs-lookup"><span data-stu-id="2d8fc-157">Create a return order</span></span>

1. <span data-ttu-id="2d8fc-158">Klik op de startpagina op **Een order zoeken**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2d8fc-159">Selecteer de order die u wilt retourneren, selecteer de factuur voor de order en selecteer vervolgens de productregel voor de producten die moeten worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-159">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="2d8fc-160">Klik onder aan de pagina op **Retourorder**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-160">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="2d8fc-161">Asynchrone transactiestroom voor klantorders</span><span class="sxs-lookup"><span data-stu-id="2d8fc-161">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="2d8fc-162">Klantorders kunnen worden gemaakt via de POS-client (point of sale) in synchrone modus of de asynchrone modus.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-162">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="2d8fc-163">Mogelijk maken dat klantorders in de asynchrone modus worden gemaakt</span><span class="sxs-lookup"><span data-stu-id="2d8fc-163">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="2d8fc-164">Klik op **Retail en Commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profiel** &gt; **Functionaliteitsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-164">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="2d8fc-165">Stel op het sneltabblad **Algemeen** de optie **Klantorder maken in asynchrone modus** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-165">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="2d8fc-166">Wanneer de optie **Klantorder maken in asynchrone modus** is ingesteld op **Ja**, worden klantorders altijd in de asynchrone modus gemaakt, zelfs als Retail Transaction Service (RTS) beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-166">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="2d8fc-167">Als u deze optie instelt op **Nee**, worden klantorders altijd gemaakt in de synchrone modus via RTS.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-167">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="2d8fc-168">Wanneer klantorders in de asynchrone modus worden gemaakt, worden ze opgehaald en ingevoegd in Commerce door taken op te vragen met Pull (P).</span><span class="sxs-lookup"><span data-stu-id="2d8fc-168">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="2d8fc-169">De bijbehorende verkooporders worden gemaakt wanneer **Orders synchroniseren** handmatig of via een batchproces wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2d8fc-169">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d8fc-170">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2d8fc-170">Additional resources</span></span>

[<span data-ttu-id="2d8fc-171">Hybride klantorders</span><span class="sxs-lookup"><span data-stu-id="2d8fc-171">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
