---
title: Kostprijs retour en retourpartij-id
description: U wilt dat de kosten van de geretourneerde producten gelijk zijn aan de kosten van de producten op het moment waarop u de producten aan de klant verkocht. U kunt dit bewerkstelligen met behulp van de **Retourpartij-id**.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33cd3d50fe342ba12a17419f4e759c243a60b3e0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "335135"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="d0f64-104">Kostprijs retour en retourpartij-id</span><span class="sxs-lookup"><span data-stu-id="d0f64-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="d0f64-105">De kosten van de producten die worden geretourneerd aan de voorraad, worden berekend met behulp van de huidige kosten van de producten.</span><span class="sxs-lookup"><span data-stu-id="d0f64-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="d0f64-106">U wilt echter dat de kosten van de geretourneerde producten gelijk zijn aan de kosten van de producten op het moment waarop u de producten aan de klant verkocht.</span><span class="sxs-lookup"><span data-stu-id="d0f64-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="d0f64-107">U kunt dit doen met behulp van de **Retourpartij-id** op het sneltabblad **Regeldetails** in het formulier **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="d0f64-108">Neem bijvoorbeeld het volgende scenario.</span><span class="sxs-lookup"><span data-stu-id="d0f64-108">For example, consider the following scenario.</span></span> <span data-ttu-id="d0f64-109">U maakt een klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="d0f64-109">You invoice a customer.</span></span> <span data-ttu-id="d0f64-110">Vervolgens geeft de klant de geleverde producten aan u terug.</span><span class="sxs-lookup"><span data-stu-id="d0f64-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="d0f64-111">U kunt producten terug in voorraad brengen.</span><span class="sxs-lookup"><span data-stu-id="d0f64-111">You return the products to stock.</span></span> <span data-ttu-id="d0f64-112">Wanneer u in dit geval de klant crediteert voor de geretourneerde producten, worden de kosten van deze producten berekend met behulp van de huidige kosten van de producten.</span><span class="sxs-lookup"><span data-stu-id="d0f64-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="d0f64-113">Als u echter het veld **Retourpartij-id** gebruikt, wordt de kostprijs van de geretourneerde producten berekend met behulp van de kosten op de factuur van de oorspronkelijke verkoop aan de klant.</span><span class="sxs-lookup"><span data-stu-id="d0f64-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="d0f64-114">Gebruik een van de volgende methoden om een andere dan de huidige kostprijs voor een klantenretour te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d0f64-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="d0f64-115">Methode 1: De kostprijs retour handmatig invoeren</span><span class="sxs-lookup"><span data-stu-id="d0f64-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="d0f64-116">Wanneer u items aan een retourorder toevoegt, worden items standaard geretourneerd naar de voorraad met de huidige kostprijs.</span><span class="sxs-lookup"><span data-stu-id="d0f64-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="d0f64-117">Voer de volgende stappen uit om een andere kostprijs retour op te geven.</span><span class="sxs-lookup"><span data-stu-id="d0f64-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="d0f64-118">Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="d0f64-119">Klik in het **Actievenster** in de groep **Nieuw** op **Retourorder**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="d0f64-120">Selecteer in het formulier **Retourorder maken** een klantrekening en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="d0f64-121">Selecteer in het formulier **Retourorder - RMA-nummer: %1, %2** een artikel en voer vervolgens een negatieve hoeveelheid in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="d0f64-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="d0f64-122">Klik op het sneltabblad **Regeldetails**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="d0f64-123">Voer op het tabblad **Algemeen** een waarde in het veld **Kostprijs retour** in.</span><span class="sxs-lookup"><span data-stu-id="d0f64-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="d0f64-124">Deze waarde wordt gebruikt wanneer de goederen worden geretourneerd naar de voorraad.</span><span class="sxs-lookup"><span data-stu-id="d0f64-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="d0f64-125">Als u geen waarde invoert, wordt de huidige kostprijs gebruikt wanneer de goederen worden geretourneerd naar de voorraad.</span><span class="sxs-lookup"><span data-stu-id="d0f64-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="d0f64-126">Methode 2: De kostprijs op basis van de klantenfactuurregel automatisch genereren</span><span class="sxs-lookup"><span data-stu-id="d0f64-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="d0f64-127">Dit is de aanbevolen methode om retourregels te maken.</span><span class="sxs-lookup"><span data-stu-id="d0f64-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="d0f64-128">Gebruik de kosten van de producten op de tijd wanneer u de producten aan de klant verkocht, maak een retourorder en geef een verkoopregel om te retourneren.</span><span class="sxs-lookup"><span data-stu-id="d0f64-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="d0f64-129">Klik op **Verkoop en marketing** \> **Algemeen** \> **Retourorders** \> **Alle retourorders**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="d0f64-130">Klik in het **Actievenster** in de groep **Nieuw** op **Retourorder**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="d0f64-131">Selecteer in het formulier **Retourorder maken** een klantrekening en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="d0f64-132">Klik in het formulier **Retourorder - RMA-nummer: %1, %2** in het **Actievenster** op **Verkooporder** zoeken.</span><span class="sxs-lookup"><span data-stu-id="d0f64-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="d0f64-133">Selecteer in het formulier **Verkooporder zoeken** de te retourneren factuurregel en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="d0f64-134">Op het sneltabblad **Regeldetails** op het tabblad **Algemeen** wordt in het veld **Retourpartij-id** de waarde van de oorspronkelijke verkoopregel weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d0f64-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="d0f64-135">Bovendien bevat het veld **Kostprijs retour** de kostprijs van de oorspronkelijke verkoopregel.</span><span class="sxs-lookup"><span data-stu-id="d0f64-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="d0f64-136">Voorbeeld van de kostenberekening</span><span class="sxs-lookup"><span data-stu-id="d0f64-136">Cost calculation example</span></span>

<span data-ttu-id="d0f64-137">Wanneer u het veld **Kostprijs retour** op een retourorderregel gebruikt om de retourkostprijs op te geven, wordt de kostprijs op de retourorderregel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d0f64-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="d0f64-138">Als u de functionaliteit voorraad sluiten of herberekenen uitvoert, wordt de kostprijs aangepast naar de oorspronkelijke verkoopregel.</span><span class="sxs-lookup"><span data-stu-id="d0f64-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="d0f64-139">De kosten op de retourorderregel worden automatisch aangepast aan dezelfde kosten per stuk.</span><span class="sxs-lookup"><span data-stu-id="d0f64-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="d0f64-140">Maak een product met de naam Test en geef het weer vrij.</span><span class="sxs-lookup"><span data-stu-id="d0f64-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="d0f64-141">Geef in het formulier **Vrijgegeven productdetails** de volgende informatie op:</span><span class="sxs-lookup"><span data-stu-id="d0f64-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="d0f64-142">Selecteer op het sneltabblad **Kosten beheren** in het veld **Artikelgroep** de groep **Onderdelen**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="d0f64-143">Selecteer op het sneltabblad **Algemeen** in het veld **Artikelmodelgroep** **DEF**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="d0f64-144">Typ op het sneltabblad **Inkoop** in het veld **Prijs** 10,00 als de kostprijs van het artikel.</span><span class="sxs-lookup"><span data-stu-id="d0f64-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="d0f64-145">Klik in het **Actievenster** op **Dimensiegroepen**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="d0f64-146">Selecteer in het veld **Opslagdimensiegroep** **Alleen locatie en magazijn**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="d0f64-147">Selecteer in het veld **Traceringsdimensiegroep** **Geen actieve traceringsdimensies**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="d0f64-148">Maak een inkooporder voor 10 stuks van het artikel Test op 6,00 per stuk en boek vervolgens een factuur voor de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="d0f64-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="d0f64-149">Maak een tweede inkooporder voor 10 stuks van het artikel Test op 8,00 per stuk en boek vervolgens een factuur voor de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="d0f64-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="d0f64-150">Boek een factuur voor een verkooporder voor vijf stuks van het artikel Test.</span><span class="sxs-lookup"><span data-stu-id="d0f64-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="d0f64-151">In dit geval wordt de kostprijs van de verkooporderregel berekend op 35,00 (5 stuks \* 7,00 gemiddelde kostprijs per stuk).</span><span class="sxs-lookup"><span data-stu-id="d0f64-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="d0f64-152">Maak een retourorder maken voor de klant.</span><span class="sxs-lookup"><span data-stu-id="d0f64-152">Create a return order for the customer.</span></span> <span data-ttu-id="d0f64-153">Selecteer in het formulier **Verkooporder zoeken** de factuurregel en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="d0f64-154">Controleer in het formulier **Retourorder - RMA-nummer: %1, %2** of een retourorder wordt gegenereerd om het testartikel te retourneren.</span><span class="sxs-lookup"><span data-stu-id="d0f64-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="d0f64-155">De hoeveelheid van de retourorder wordt ingesteld op-5,00.</span><span class="sxs-lookup"><span data-stu-id="d0f64-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="d0f64-156">Het veld **Retourpartij-id** bevat een partij-ID.</span><span class="sxs-lookup"><span data-stu-id="d0f64-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="d0f64-157">Deze partij-ID is overgenomen uit de oorspronkelijke verkooporder van het artikel dat aan de klant is verkocht.</span><span class="sxs-lookup"><span data-stu-id="d0f64-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="d0f64-158">Het veld **Kostprijs retour** bevat de kostprijs van de oorspronkelijke verkoopregel.</span><span class="sxs-lookup"><span data-stu-id="d0f64-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="d0f64-159">Registreer de ontvangst van de retourartikelen.</span><span class="sxs-lookup"><span data-stu-id="d0f64-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="d0f64-160">Boek een pakbon voor de geretourneerde artikelen.</span><span class="sxs-lookup"><span data-stu-id="d0f64-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="d0f64-161">Boek een factuur voor de retourorder.</span><span class="sxs-lookup"><span data-stu-id="d0f64-161">Post an invoice for the return order.</span></span> <span data-ttu-id="d0f64-162">Selecteer op de lijstpagina **Alle verkooporders** een verkooporder waarvoor **Geretourneerde order** het ordertype is.</span><span class="sxs-lookup"><span data-stu-id="d0f64-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="d0f64-163">Open het formulier **Voorraadtransacties**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="d0f64-164">Controleer of de kosten van de retour bepaald zijn op 7,00 per stuk door de waarde in het veld **Kostprijs retour** te gebruiken voor een totaal van 35,00 in het veld **Kosten**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="d0f64-165">U kunt het formulier **Voorraadtransacties** via het formulier **Retourorder - RMA-nummer: %1, %2** openen.</span><span class="sxs-lookup"><span data-stu-id="d0f64-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="d0f64-166">Klik in het raster **Regels** op **Voorraad** \> **Transacties**.</span><span class="sxs-lookup"><span data-stu-id="d0f64-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="d0f64-167">Gebruik in voorraad- en magazijnbeheer het formulier **Afsluiten en corrigeren** om de procedure **3. Sluiten** uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d0f64-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="d0f64-168">Met deze actie worden de kosten gecorrigeerd op de oorspronkelijke verkoopregel waarvan de kostprijs was berekend op -35,00 (5 stuks \* 7,00) naar -30,00 (5 stuks \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="d0f64-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="d0f64-169">Dit is omdat de voorraadmodelgroep First in, First out (FIFO gebruikt) en 6,00 per stuk de FIFO-kosten van de eerste inkooporder is.</span><span class="sxs-lookup"><span data-stu-id="d0f64-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="d0f64-170">De actie past bovendien de kosten op de retourverkoopregel aan naar de kostprijs per stuk op de oorspronkelijke verkoopregel.</span><span class="sxs-lookup"><span data-stu-id="d0f64-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="d0f64-171">Dus wordt de kostprijs van de retourregel aangepast van 35,00 naar 30,00.</span><span class="sxs-lookup"><span data-stu-id="d0f64-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




