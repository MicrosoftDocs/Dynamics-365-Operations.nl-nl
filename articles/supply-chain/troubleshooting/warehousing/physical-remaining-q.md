---
title: De fysieke resterende hoeveelheid in de eenheid mag niet nul zijn
description: Wanneer u een pakbon genereert, bevatten de gegevens naar de pakbon een voorraadhoeveelheid die groter is dan nul, maar een verkoophoeveelheid van nul.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248774"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="0e524-103">De fysieke resterende hoeveelheid in de eenheid mag niet nul zijn</span><span class="sxs-lookup"><span data-stu-id="0e524-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="0e524-104">Foutcode: SYS19591</span><span class="sxs-lookup"><span data-stu-id="0e524-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="0e524-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="0e524-105">Symptoms</span></span>

<span data-ttu-id="0e524-106">Wanneer u een pakbon genereert, bevatten de gegevens naar de pakbon een voorraadhoeveelheid die groter is dan nul, maar een verkoophoeveelheid van nul.</span><span class="sxs-lookup"><span data-stu-id="0e524-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="0e524-107">Wanneer u de pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="0e524-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="0e524-108">Resterende fysieke hoeveelheid in de eenheid %1 mag niet gelijk zijn aan nul.</span><span class="sxs-lookup"><span data-stu-id="0e524-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="0e524-109">U kunt de pakbon voor de lading daarom nog niet genereren.</span><span class="sxs-lookup"><span data-stu-id="0e524-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="0e524-110">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="0e524-110">Cause</span></span>

<span data-ttu-id="0e524-111">Het systeem evalueert de fysieke resterende hoeveelheid in de voorraadeenheid en de fysieke resterende hoeveelheid in de verzendeenheid.</span><span class="sxs-lookup"><span data-stu-id="0e524-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="0e524-112">Als in het systeem wordt gevonden dat de fysieke resterende hoeveelheid in de verzendeenheid 0 (nul) is, maar de fysieke resterende hoeveelheid in de voorraadeenheid niet 0 is, kunt u de pakbon niet genereren.</span><span class="sxs-lookup"><span data-stu-id="0e524-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="0e524-113">Dit probleem kan zich bijvoorbeeld voordoen als de verkoopeenheid en voorraadeenheid voor het artikel verschillen en de omrekening tussen eenheden niet correct is.</span><span class="sxs-lookup"><span data-stu-id="0e524-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="0e524-114">Oplossing</span><span class="sxs-lookup"><span data-stu-id="0e524-114">Resolution</span></span>

<span data-ttu-id="0e524-115">Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt.</span><span class="sxs-lookup"><span data-stu-id="0e524-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="0e524-116">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="0e524-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="0e524-117">Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="0e524-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="0e524-118">Controleer de ladingsregels en breng correcties aan om ervoor te zorgen dat de hoeveelheid correct kan worden geconverteerd zonder afrondingskwesties.</span><span class="sxs-lookup"><span data-stu-id="0e524-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="0e524-119">Controleer uw ladingsregels en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid.</span><span class="sxs-lookup"><span data-stu-id="0e524-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="0e524-120">Zorg ervoor dat de voorraadmaateenheid kleiner is dan de verkoopmaateenheid.</span><span class="sxs-lookup"><span data-stu-id="0e524-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="0e524-121">Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen</span><span class="sxs-lookup"><span data-stu-id="0e524-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="0e524-122">Gebruik de volgende procedure om de ladingsregels te controleren en ervoor te zorgen dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="0e524-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="0e524-123">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="0e524-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0e524-124">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="0e524-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="0e524-125">Selecteer de ladingsregel op het sneltabblad **Laadregels**.</span><span class="sxs-lookup"><span data-stu-id="0e524-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="0e524-126">Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.</span><span class="sxs-lookup"><span data-stu-id="0e524-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="0e524-127">Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.</span><span class="sxs-lookup"><span data-stu-id="0e524-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="0e524-128">Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="0e524-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="0e524-129">Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.</span><span class="sxs-lookup"><span data-stu-id="0e524-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="0e524-130">Controleer de ladingsregels en breng correcties aan om ervoor te zorgen dat de hoeveelheid correct kan worden geconverteerd zonder afrondingskwesties</span><span class="sxs-lookup"><span data-stu-id="0e524-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="0e524-131">Gebruik de volgende procedure om de ladingsregels te controleren en correcties aan te brengen om er zeker van te zijn dat de hoeveelheid correct kan worden geconverteerd zonder afrondingskwesties.</span><span class="sxs-lookup"><span data-stu-id="0e524-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="0e524-132">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="0e524-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0e524-133">Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0e524-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0e524-134">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.</span><span class="sxs-lookup"><span data-stu-id="0e524-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="0e524-135">Selecteer op het tabblad  **Ladingsregels** de ladingsregel voor het artikel dat de meerlevering overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="0e524-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="0e524-136">Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.</span><span class="sxs-lookup"><span data-stu-id="0e524-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="0e524-137">Selecteer op het tabblad  **Regeldetails** de optie **Order**.</span><span class="sxs-lookup"><span data-stu-id="0e524-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="0e524-138">Stel veld **Hoeveelheid** in op de opgenomen hoeveelheid (dat wil zeggen, op de waarde van het veld **Hoeveelheid gemaakt werk**), zodat de pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0e524-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="0e524-139">Controleer uw ladingsregels en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid</span><span class="sxs-lookup"><span data-stu-id="0e524-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="0e524-140">Gebruik de volgende procedure om de ladingsregels te controleren en breng correcties aan om ervoor te zorgen dat de eenheid en hoeveelheid worden afgestemd op de precisie van decimalen van de eenheid.</span><span class="sxs-lookup"><span data-stu-id="0e524-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="0e524-141">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="0e524-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0e524-142">Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0e524-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0e524-143">Selecteer op het sneltabblad **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="0e524-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="0e524-144">Maak een notitie van de waarde in de velden **Hoeveelheid** en **Eenheid**.</span><span class="sxs-lookup"><span data-stu-id="0e524-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="0e524-145">Ga naar **Organisatiebeheer \> Eenheden \> Eenheden**.</span><span class="sxs-lookup"><span data-stu-id="0e524-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="0e524-146">Selecteer de eenheid waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0e524-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0e524-147">Pas de waarde van het veld **Precisie van decimalen** zo nodig aan.</span><span class="sxs-lookup"><span data-stu-id="0e524-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="0e524-148">Zorg ervoor dat de voorraadmaateenheid kleiner is dan de verkoopmaateenheid</span><span class="sxs-lookup"><span data-stu-id="0e524-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="0e524-149">Zorg ervoor dat de voorraadmaateenheid kleiner is dan de verkoopmaateenheid.</span><span class="sxs-lookup"><span data-stu-id="0e524-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="0e524-150">Overweeg om de maateenheid voor het artikel zo nodig opnieuw te configureren.</span><span class="sxs-lookup"><span data-stu-id="0e524-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
