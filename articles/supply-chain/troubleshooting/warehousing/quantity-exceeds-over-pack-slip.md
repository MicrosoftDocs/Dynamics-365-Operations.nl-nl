---
title: Hoeveelheid overschrijdt meerleveringspercentage tijdens genereren pakbon
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die het percentage van de meerlevering overschrijdt.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249082"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="b4669-103">Hoeveelheid overschrijdt meerleveringspercentage tijdens genereren pakbon</span><span class="sxs-lookup"><span data-stu-id="b4669-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="b4669-104">Foutcode: SYS24920</span><span class="sxs-lookup"><span data-stu-id="b4669-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="b4669-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="b4669-105">Symptoms</span></span>

<span data-ttu-id="b4669-106">Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die het percentage van de meerlevering overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="b4669-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="b4669-107">Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="b4669-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="b4669-108">Meerlevering van regel is %1 percent, maar de toegestane overlevering is slechts %2 percent.</span><span class="sxs-lookup"><span data-stu-id="b4669-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="b4669-109">U kunt de pakbon voor de lading daarom nog niet genereren.</span><span class="sxs-lookup"><span data-stu-id="b4669-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="b4669-110">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="b4669-110">Cause</span></span>

<span data-ttu-id="b4669-111">De opgenomen hoeveelheid voor de lading of zending is meer dan de bestelde hoeveelheid en valt niet binnen het bereik van het meerleveringspercentage.</span><span class="sxs-lookup"><span data-stu-id="b4669-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="b4669-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="b4669-112">Resolution</span></span>

<span data-ttu-id="b4669-113">Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt.</span><span class="sxs-lookup"><span data-stu-id="b4669-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="b4669-114">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="b4669-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="b4669-115">Pas de hoeveelheid voor de ladingsregel aan.</span><span class="sxs-lookup"><span data-stu-id="b4669-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="b4669-116">Pas het meerleveringspercentage aan.</span><span class="sxs-lookup"><span data-stu-id="b4669-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="b4669-117">Keer het om en breng correcties aan.</span><span class="sxs-lookup"><span data-stu-id="b4669-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="b4669-118">De hoeveelheid voor de ladingsregel aanpassen</span><span class="sxs-lookup"><span data-stu-id="b4669-118">Adjust the load line quantity</span></span>

<span data-ttu-id="b4669-119">Met de volgende procedure kunt u de hoeveelheid op de ladingsregel aanpassen.</span><span class="sxs-lookup"><span data-stu-id="b4669-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="b4669-120">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="b4669-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b4669-121">Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="b4669-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="b4669-122">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.</span><span class="sxs-lookup"><span data-stu-id="b4669-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="b4669-123">Selecteer op het tabblad  **Ladingsregels** de ladingsregel voor het artikel dat het meerleveringspercentage overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="b4669-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="b4669-124">Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.</span><span class="sxs-lookup"><span data-stu-id="b4669-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="b4669-125">Selecteer op het tabblad  **Regeldetails** de optie **Order**.</span><span class="sxs-lookup"><span data-stu-id="b4669-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="b4669-126">Stel veld **Hoeveelheid** in op de opgenomen hoeveelheid (dat wil zeggen, op de waarde van het veld **Hoeveelheid gemaakt werk**), zodat de pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="b4669-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="b4669-127">Het meerleveringspercentage aanpassen</span><span class="sxs-lookup"><span data-stu-id="b4669-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="b4669-128">Met de volgende procedure kunt u het meerleveringspercentage aanpassen.</span><span class="sxs-lookup"><span data-stu-id="b4669-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="b4669-129">Ga naar **Klanten \> Orders \> Alle orders**.</span><span class="sxs-lookup"><span data-stu-id="b4669-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="b4669-130">Selecteer de verkooporder waarvoor u geen pakbon voor de lading kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="b4669-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="b4669-131">Selecteer op het tabblad  **Verkooporderregels** de verkooporderregel voor het artikel dat het percentage voor meerleveringen overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="b4669-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="b4669-132">Selecteer op het tabblad  **Regeldetails** de optie **Levering**.</span><span class="sxs-lookup"><span data-stu-id="b4669-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="b4669-133">Stel in het veld **Meerlevering** de waarde in op een groter percentage dat geschikt is voor de hoeveelheid die voor de ladinghoeveelheid was verzameld, zodat het genereren van de pakbon doorgang kan vinden.</span><span class="sxs-lookup"><span data-stu-id="b4669-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="b4669-134">Omkeren en correcties aanbrengen</span><span class="sxs-lookup"><span data-stu-id="b4669-134">Reverse and make adjustments</span></span>

<span data-ttu-id="b4669-135">Keer alles om dat voor de lading is geboekt (bijvoorbeeld de pakbon, bevestiging van zending en werk), breng correcties in de verkooporder aan, geef de order opnieuw vrij aan het magazijn en voer de zendingsprocedure uit.</span><span class="sxs-lookup"><span data-stu-id="b4669-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="b4669-136">Gebruik de volgende procedure om een pakbon te annuleren.</span><span class="sxs-lookup"><span data-stu-id="b4669-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="b4669-137">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="b4669-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b4669-138">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Pakbonnen annuleren**.</span><span class="sxs-lookup"><span data-stu-id="b4669-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="b4669-139">Gebruik de volgende procedure om een verzendingsbevestiging om te keren.</span><span class="sxs-lookup"><span data-stu-id="b4669-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="b4669-140">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="b4669-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b4669-141">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.</span><span class="sxs-lookup"><span data-stu-id="b4669-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="b4669-142">Gebruik de volgende procedure om werk om te keren.</span><span class="sxs-lookup"><span data-stu-id="b4669-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="b4669-143">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="b4669-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b4669-144">Selecteer in het actievenster op het tabblad  **Ladingen** in de groep  **Werk** de optie  **Werk omkeren**.</span><span class="sxs-lookup"><span data-stu-id="b4669-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
