---
title: Opgenomen hoeveelheid onvoldoende tijdens genereren pakbon
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een opgenomen hoeveelheid die niet gelijk is aan de gemaakte werkhoeveelheid die in de ladingsregel is gedefinieerd.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249084"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="0f449-103">Opgenomen hoeveelheid onvoldoende tijdens genereren pakbon</span><span class="sxs-lookup"><span data-stu-id="0f449-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="0f449-104">Foutcode: SYS54073</span><span class="sxs-lookup"><span data-stu-id="0f449-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="0f449-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="0f449-105">Symptoms</span></span>

<span data-ttu-id="0f449-106">Wanneer u een pakbon genereert, bevat de uitgaande lading een opgenomen hoeveelheid die niet gelijk is aan de gemaakte werkhoeveelheid die in de ladingsregel is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="0f449-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="0f449-107">Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="0f449-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="0f449-108">Aangezien %1 zijn opgenomen, is het niet voldoende om %2 bij te werken wanneer de rest vervolgens %3 moet zijn.</span><span class="sxs-lookup"><span data-stu-id="0f449-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="0f449-109">U kunt de pakbon voor de lading daarom nog niet genereren.</span><span class="sxs-lookup"><span data-stu-id="0f449-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="0f449-110">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="0f449-110">Cause</span></span>

<span data-ttu-id="0f449-111">De pakbon kan niet in de huidige status worden gegenereerd, omdat mogelijk een van de volgende voorwaarden van toepassing is:</span><span class="sxs-lookup"><span data-stu-id="0f449-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="0f449-112">Het gerelateerde werk is nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.</span><span class="sxs-lookup"><span data-stu-id="0f449-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="0f449-113">De verzamelde werkhoeveelheid komt niet overeen met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="0f449-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="0f449-114">De ladingsregelhoeveelheid, gemaakte werkhoeveelheid en opgenomen hoeveelheid komen niet overeen.</span><span class="sxs-lookup"><span data-stu-id="0f449-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="0f449-115">Oplossing</span><span class="sxs-lookup"><span data-stu-id="0f449-115">Resolution</span></span>

<span data-ttu-id="0f449-116">Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt.</span><span class="sxs-lookup"><span data-stu-id="0f449-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="0f449-117">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="0f449-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="0f449-118">Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="0f449-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="0f449-119">Pas de hoeveelheid voor de ladingsregel aan.</span><span class="sxs-lookup"><span data-stu-id="0f449-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="0f449-120">Keer alle orderverzamelregistraties om en voer de orderverzameling opnieuw uit.</span><span class="sxs-lookup"><span data-stu-id="0f449-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="0f449-121">Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen</span><span class="sxs-lookup"><span data-stu-id="0f449-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="0f449-122">Gebruik de volgende procedure om de ladingsregels te controleren en ervoor te zorgen dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="0f449-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="0f449-123">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="0f449-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0f449-124">Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0f449-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0f449-125">Selecteer de ladingsregel op het sneltabblad **Laadregels**.</span><span class="sxs-lookup"><span data-stu-id="0f449-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="0f449-126">Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.</span><span class="sxs-lookup"><span data-stu-id="0f449-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="0f449-127">Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.</span><span class="sxs-lookup"><span data-stu-id="0f449-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="0f449-128">Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="0f449-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="0f449-129">Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.</span><span class="sxs-lookup"><span data-stu-id="0f449-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="0f449-130">De hoeveelheid voor de ladingsregel aanpassen</span><span class="sxs-lookup"><span data-stu-id="0f449-130">Adjust the load line quantity</span></span>

<span data-ttu-id="0f449-131">Met de volgende procedure kunt u de hoeveelheid op de ladingsregel aanpassen.</span><span class="sxs-lookup"><span data-stu-id="0f449-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="0f449-132">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="0f449-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0f449-133">Selecteer de lading waarvoor geen pakbon kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="0f449-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="0f449-134">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.</span><span class="sxs-lookup"><span data-stu-id="0f449-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="0f449-135">Selecteer op het tabblad  **Ladingsregels** de ladingsregel voor het artikel dat een probleem veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="0f449-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="0f449-136">Selecteer **Opgenomen hoeveelheid reduceren** om de opgenomen hoeveelheid aan te passen.</span><span class="sxs-lookup"><span data-stu-id="0f449-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="0f449-137">Stel het veld **Ladingsregel verminderen** zo in dat correcties op de ladingsregel worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0f449-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="0f449-138">Alle orderverzamelregistraties omkeren en voer de orderverzameling opnieuw uitvoeren</span><span class="sxs-lookup"><span data-stu-id="0f449-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="0f449-139">Het probleem kan zich voordoen omdat iemand orderverzamelingsregistratie heeft gebruikt om een ladingsregel zonder werk af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="0f449-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="0f449-140">In dit geval moet handmatige orderverzamelregistratie worden omgekeerd en moet het verzamelen vervolgens worden uitgevoerd met de mobiele app Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="0f449-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="0f449-141">Gebruik de volgende procedure om de orderverzamelregistratie om te keren.</span><span class="sxs-lookup"><span data-stu-id="0f449-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="0f449-142">Ga naar **Klanten \> Orders \> Alle orders**.</span><span class="sxs-lookup"><span data-stu-id="0f449-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="0f449-143">Selecteer de verkooporder waarvoor u geen pakbon voor de lading kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="0f449-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="0f449-144">Selecteer op het tabblad  **Verkooporderregels** de verkooporderregel waar de orderverzamelregistratie voor is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0f449-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="0f449-145">Selecteer **Regel bijwerken \> Orderverzamelen** om het verzamelen van de artikelen ongedaan te maken.</span><span class="sxs-lookup"><span data-stu-id="0f449-145">Select **Update line \> Pick** to unpick the items.</span></span>
