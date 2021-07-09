---
title: U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld
description: U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301300"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="24496-103">U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld</span><span class="sxs-lookup"><span data-stu-id="24496-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="24496-104">Foutcode: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="24496-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="24496-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="24496-105">Symptoms</span></span>

<span data-ttu-id="24496-106">Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="24496-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="24496-107">Enkele artikelen die nodig zijn voor lading %1 zijn nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.</span><span class="sxs-lookup"><span data-stu-id="24496-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="24496-108">U kunt de zending voor de lading daarom nog niet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="24496-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="24496-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="24496-109">Cause</span></span>

<span data-ttu-id="24496-110">De lading of zending kan niet in de huidige status worden bevestigd, omdat mogelijk een van de volgende voorwaarden van toepassing is:</span><span class="sxs-lookup"><span data-stu-id="24496-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="24496-111">Het gerelateerde werk is nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.</span><span class="sxs-lookup"><span data-stu-id="24496-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="24496-112">De verzamelde werkhoeveelheid komt niet overeen met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="24496-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="24496-113">De locatie-instructie is met de verpakkingslocatie geconfigureerd als de uiteindelijke verzendlocatie tijdens het gebruik van wavesjablonen voor containervorming.</span><span class="sxs-lookup"><span data-stu-id="24496-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="24496-114">Oplossing</span><span class="sxs-lookup"><span data-stu-id="24496-114">Resolution</span></span>

<span data-ttu-id="24496-115">Daarom bevindt de lading of zending zich momenteel in een staat waarbij de verzendingsbevestiging mislukt.</span><span class="sxs-lookup"><span data-stu-id="24496-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="24496-116">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="24496-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="24496-117">Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="24496-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="24496-118">Annuleer de werk-id's die zijn gemaakt met de verpakkingslocatie als de uiteindelijke verzendlocatie, configureer de locatierichtlijn opnieuw en verzend de lading opnieuw.</span><span class="sxs-lookup"><span data-stu-id="24496-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="24496-119">Controleer uw ladingsregels en zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen</span><span class="sxs-lookup"><span data-stu-id="24496-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="24496-120">Gebruik de volgende procedure om de ladingsregels te controleren en ervoor te zorgen dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="24496-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="24496-121">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="24496-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="24496-122">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="24496-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="24496-123">Selecteer de ladingsregel op het sneltabblad **Laadregels**.</span><span class="sxs-lookup"><span data-stu-id="24496-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="24496-124">Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.</span><span class="sxs-lookup"><span data-stu-id="24496-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="24496-125">Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.</span><span class="sxs-lookup"><span data-stu-id="24496-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="24496-126">Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="24496-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="24496-127">Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.</span><span class="sxs-lookup"><span data-stu-id="24496-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="24496-128">Annuleer de werk-id's die zijn gemaakt met de verpakkingslocatie als de uiteindelijke verzendlocatie, configureer de locatierichtlijn opnieuw en verzend de lading opnieuw</span><span class="sxs-lookup"><span data-stu-id="24496-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="24496-129">Gebruik de volgende procedure om de werk-id's te annuleren die de verpakkingslocatie hebben als definitieve wegzetlocatie, waarbij geautomatiseerde containervorming is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="24496-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="24496-130">Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="24496-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="24496-131">Het dialoogvenster **Werk annuleren** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="24496-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="24496-132">In het veld **Werk-id** geeft de id op van het werk dat u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="24496-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="24496-133">De geselecteerde werk-id moet bij **Werkstatus** de waarde *Openstaand*, *In uitvoering*, *Geannuleerd*, *Gecombineerd* of *Afgesloten* hebben.</span><span class="sxs-lookup"><span data-stu-id="24496-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="24496-134">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="24496-134">Select **OK**.</span></span>
1. <span data-ttu-id="24496-135">Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="24496-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="24496-136">Herhaal deze procedure zo nodig voor de andere werk-id's.</span><span class="sxs-lookup"><span data-stu-id="24496-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="24496-137">Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="24496-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="24496-138">Gebruik de volgende procedure om de locatie-instructie opnieuw te configureren, zodat de verpakkingslocatie niet wordt gebruikt als de uiteindelijke verzendlocatie wanneer geautomatiseerde containerization is ingesteld voor de wavesjabloon.</span><span class="sxs-lookup"><span data-stu-id="24496-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="24496-139">Ga naar **Magazijnbeheer \> Instellen \> Locatie-instructies**.</span><span class="sxs-lookup"><span data-stu-id="24496-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="24496-140">Selecteer *Verkooporders* in het veld **Werkordertype**.</span><span class="sxs-lookup"><span data-stu-id="24496-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="24496-141">Hier kunt u de locatie-instructie selecteren die voor geautomatiseerde containvorming wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="24496-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="24496-142">Selecteer op de werkbalk van het sneltabblad **Locatie-instructieacties** de optie **Query bewerken**.</span><span class="sxs-lookup"><span data-stu-id="24496-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="24496-143">Zoek in het dialoogvenster van de query-editor op het tabblad **Bereik** naar de rij waar **Veld** is ingesteld op *Locatieprofiel* en controleer of het veld **Criteria** voor die rij niet is ingesteld op een locatieprofiel met *Verpakking* als **Locatietype**.</span><span class="sxs-lookup"><span data-stu-id="24496-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="24496-144">Pas het veld **Criteria** aan om de uiteindelijke wegzetlocatie te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="24496-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="24496-145">Met de volgende procedure kunt u de lading opnieuw vrijgeven en werk-id's maken met de juiste uiteindelijke verzendlocatie.</span><span class="sxs-lookup"><span data-stu-id="24496-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="24496-146">Ga naar **Magazijnbeheer \> Ladingen \> Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="24496-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="24496-147">Zoek in de sectie **Ladingen** de lading die moet worden vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="24496-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="24496-148">Selecteer **Vrijgeven \> Vrijgeven aan magazijn** op de werkbalk in de sectie **Laden** om de geselecteerde lading vrij te geven aan het magazijn.</span><span class="sxs-lookup"><span data-stu-id="24496-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="24496-149">Herhaal deze procedure zo nodig voor de andere ladingen.</span><span class="sxs-lookup"><span data-stu-id="24496-149">Repeat this procedure for the other loads as needed.</span></span>
