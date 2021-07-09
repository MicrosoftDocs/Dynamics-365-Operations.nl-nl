---
title: De hoeveelheid die u probeert bij te werken, overschrijdt de ontvangen/geleverde hoeveelheid.
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die groter is dan de werkhoeveelheid die is verzameld en gereserveerd voor de verkooporder.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249085"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="9bfd5-103">De hoeveelheid die u probeert bij te werken, overschrijdt de ontvangen/geleverde hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="9bfd5-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="9bfd5-104">Foutcode: SYS7676</span><span class="sxs-lookup"><span data-stu-id="9bfd5-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="9bfd5-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="9bfd5-105">Symptoms</span></span>

<span data-ttu-id="9bfd5-106">Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die groter is dan de werkhoeveelheid die is verzameld en gereserveerd voor de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="9bfd5-107">Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="9bfd5-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="9bfd5-108">De hoeveelheid die u probeert bij te werken, overschrijdt de ontvangen/geleverde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="9bfd5-109">U kunt de pakbon voor de lading daarom nog niet genereren.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="9bfd5-110">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="9bfd5-110">Cause</span></span>

<span data-ttu-id="9bfd5-111">De verzamelde werkhoeveelheid komt niet overeen met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="9bfd5-112">Dit probleem kan zich bijvoorbeeld voordoen als de hoeveelheid op de ladingsregel, de gemaakte werkhoeveelheid of de verzamelde hoeveelheid niet nauwkeurig is.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="9bfd5-113">Oplossing</span><span class="sxs-lookup"><span data-stu-id="9bfd5-113">Resolution</span></span>

<span data-ttu-id="9bfd5-114">Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="9bfd5-115">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="9bfd5-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="9bfd5-116">Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="9bfd5-117">Pas de hoeveelheid voor de ladingsregel aan.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="9bfd5-118">Keer alle orderverzamelregistraties om en voer de orderverzameling opnieuw uit.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="9bfd5-119">Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen</span><span class="sxs-lookup"><span data-stu-id="9bfd5-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="9bfd5-120">Gebruik de volgende procedure om de ladingsregels te controleren en ervoor te zorgen dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="9bfd5-121">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="9bfd5-122">Selecteer de lading waarvoor de zending niet kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="9bfd5-123">Selecteer de ladingsregel op het sneltabblad **Laadregels**.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="9bfd5-124">Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="9bfd5-125">Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="9bfd5-126">Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="9bfd5-127">Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="9bfd5-128">De hoeveelheid voor de ladingsregel aanpassen</span><span class="sxs-lookup"><span data-stu-id="9bfd5-128">Adjust the load line quantity</span></span>

<span data-ttu-id="9bfd5-129">Met de volgende procedure kunt u de hoeveelheid op de ladingsregel aanpassen.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="9bfd5-130">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="9bfd5-131">Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="9bfd5-132">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="9bfd5-133">Selecteer op het tabblad  **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="9bfd5-134">Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="9bfd5-135">Stel het veld **Ladingsregel verminderen** zo in dat correcties op de ladingsregel worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="9bfd5-136">Alle orderverzamelregistraties omkeren en voer de orderverzameling opnieuw uitvoeren</span><span class="sxs-lookup"><span data-stu-id="9bfd5-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="9bfd5-137">Als iemand de orderverzamelregistratie heeft gebruikt om een ladingsregel zonder werk af te sluiten, kan er een verschil optreden tussen de hoeveelheid op de ladingsregel en de verzamelde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="9bfd5-138">In dit geval moet handmatige orderverzamelregistratie worden omgekeerd en moet het verzamelen vervolgens worden uitgevoerd met de mobiele app Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="9bfd5-139">Gebruik de volgende procedure om de orderverzamelregistratie om te keren.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="9bfd5-140">Ga naar **Klanten \> Orders \> Alle orders**.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="9bfd5-141">Selecteer de verkooporder waarvoor u geen pakbon voor de lading kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="9bfd5-142">Selecteer op het tabblad  **Verkooporderregels** de verkooporderregel waar de orderverzamelregistratie voor is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="9bfd5-143">Selecteer **Regel bijwerken \> Orderverzamelen** om het verzamelen van de artikelen ongedaan te maken.</span><span class="sxs-lookup"><span data-stu-id="9bfd5-143">Select **Update line \> Pick** to unpick the items.</span></span>
