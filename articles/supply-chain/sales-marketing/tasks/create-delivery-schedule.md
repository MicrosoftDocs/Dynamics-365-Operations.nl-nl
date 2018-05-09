--- 
title: Een afleveringsschema maken
description: Deze procedure toont hoe een afleveringsschema voor een verkooporder wordt gemaakt.
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 407337d31e0aa68217a27a5709da16ddc7d6e4a1
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="d6c02-103">Een afleveringsschema maken</span><span class="sxs-lookup"><span data-stu-id="d6c02-103">Create a delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6c02-104">Deze procedure toont hoe een afleveringsschema voor een verkooporder wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6c02-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="d6c02-105">Een afleveringsschema wordt gebruikt wanneer een hoeveelheid op een order of offerte wordt gevraagd in meerdere zendingen te leveren.</span><span class="sxs-lookup"><span data-stu-id="d6c02-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="d6c02-106">U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="d6c02-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="d6c02-107">Afleveringsschema maken</span><span class="sxs-lookup"><span data-stu-id="d6c02-107">Create delivery schedule</span></span>
1. <span data-ttu-id="d6c02-108">Ga naar Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="d6c02-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="d6c02-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d6c02-109">Click New.</span></span>
3. <span data-ttu-id="d6c02-110">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="d6c02-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="d6c02-111">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d6c02-111">Click OK.</span></span>
5. <span data-ttu-id="d6c02-112">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="d6c02-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="d6c02-113">Voer in het veld Hoeveelheid een aantal in dat groter is dan 1.</span><span class="sxs-lookup"><span data-stu-id="d6c02-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="d6c02-114">Klik op Verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="d6c02-114">Click Sales order line.</span></span>
8. <span data-ttu-id="d6c02-115">Klik op Afleveringsschema.</span><span class="sxs-lookup"><span data-stu-id="d6c02-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="d6c02-116">De pagina Afleveringsschema is de plaats waar u het aantal zendingen kunt opgeven waarin de totale hoeveelheid van de orderregel aan de klant wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="d6c02-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="d6c02-117">Standaard kopieert het systeem de totale hoeveelheid en andere leveringsdetails van de oorspronkelijke verkoopregel in de eerste afleveringsschemaregel.</span><span class="sxs-lookup"><span data-stu-id="d6c02-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="d6c02-118">In dit voorbeeld wordt er een planning voor twee zendingen gemaakt, met de datum van de tweede zending een week later dan de eerste.</span><span class="sxs-lookup"><span data-stu-id="d6c02-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="d6c02-119">Voer in het veld Hoeveelheid een aantal in dat deel is van de totale hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="d6c02-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="d6c02-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d6c02-120">Click New.</span></span>
11. <span data-ttu-id="d6c02-121">Voer in het veld Hoeveelheid de resterende hoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="d6c02-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="d6c02-122">Voer in het veld Gewenste verzenddatum een datum in die één week verder is dan de datum van de eerste leveringsregel.</span><span class="sxs-lookup"><span data-stu-id="d6c02-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="d6c02-123">De twee opties op het sneltabblad Toeslagenconversie bepalen hoe u wilt dat de kosten worden verdeeld over de afleveringsschemaregels, zodra ze aan de oorspronkelijke orderregel zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d6c02-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="d6c02-124">Als u Brutobedragen kopiëren selecteert, wordt hetzelfde toeslagbedrag gekopieerd naar elke regel.</span><span class="sxs-lookup"><span data-stu-id="d6c02-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="d6c02-125">De optie Toewijzen aan afleveringsregels verdeelt de toeslagen gelijk over de leveringsregels.</span><span class="sxs-lookup"><span data-stu-id="d6c02-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="d6c02-126">Alleen vaste toeslagen kunnen worden verdeeld, terwijl variabele toeslagen nog steeds naar de regels worden gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="d6c02-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="d6c02-127">Verplaats de cursor weg van de tweede leveringsregel om de pagina bijwerken.</span><span class="sxs-lookup"><span data-stu-id="d6c02-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="d6c02-128">U kunt bijhouden welke totale hoeveelheid is toegewezen aan de afleveringsschemaregels door te kijken naar de velden Totaal en Resterend.</span><span class="sxs-lookup"><span data-stu-id="d6c02-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="d6c02-129">Als de resterende hoeveelheid nul is, is de volledige hoeveelheid van de oorspronkelijke regel toegewezen aan het schema.</span><span class="sxs-lookup"><span data-stu-id="d6c02-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="d6c02-130">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d6c02-130">Click OK.</span></span>
    * <span data-ttu-id="d6c02-131">Het afleveringsschema is nu gekopieerd naar de orderregels.</span><span class="sxs-lookup"><span data-stu-id="d6c02-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="d6c02-132">De oorspronkelijke orderregel, de commerciële regel genoemd, is omgezet in een orderregel met meerdere leveringen.</span><span class="sxs-lookup"><span data-stu-id="d6c02-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="d6c02-133">Het is gemarkeerd met een ander pictogram en dient als de kop voor de leveringsregels.</span><span class="sxs-lookup"><span data-stu-id="d6c02-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="d6c02-134">De twee nieuwe regels, die leveringsregels worden genoemd, vormen één afleveringsschema.</span><span class="sxs-lookup"><span data-stu-id="d6c02-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="d6c02-135">De order wordt met deze regels en niet de oorspronkelijke regel verwerkt.</span><span class="sxs-lookup"><span data-stu-id="d6c02-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="d6c02-136">Als documenten zoals bevestigingsbonnen, orderverzamellijsten, pakbonnen, of facturen worden afgedrukt, worden alleen de leveringsregels weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d6c02-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="d6c02-137">De leveringsregels kunnen verschillende leveringsdatums, hoeveelheden, leveringsmethoden en opslagdimensies, zoals locatie en magazijn, bevatten.</span><span class="sxs-lookup"><span data-stu-id="d6c02-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="d6c02-138">De productdimensies moeten echter altijd overeenkomen met de productdimensies op de commerciële regel en kunnen niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="d6c02-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="d6c02-139">Voer in het veld Hoeveelheid een aantal in dat groter is dan het huidige aantal.</span><span class="sxs-lookup"><span data-stu-id="d6c02-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="d6c02-140">Selecteer de commerciële regel om het effect van de hoeveelheidsherberekening te bekijken.</span><span class="sxs-lookup"><span data-stu-id="d6c02-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="d6c02-141">Klik in het actievenster op Verzamelen en inpakken.</span><span class="sxs-lookup"><span data-stu-id="d6c02-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="d6c02-142">Klik op Pakbon boeken.</span><span class="sxs-lookup"><span data-stu-id="d6c02-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="d6c02-143">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="d6c02-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="d6c02-144">Selecteer in het veld Hoeveelheid de optie 'Alle'.</span><span class="sxs-lookup"><span data-stu-id="d6c02-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="d6c02-145">Merk op dat de pakbon voor de twee afleveringsschemaregels en niet de oorspronkelijke orderregel wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d6c02-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="d6c02-146">Selecteer Ja in het veld Pakbon afdrukken.</span><span class="sxs-lookup"><span data-stu-id="d6c02-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="d6c02-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d6c02-147">Click OK.</span></span>
23. <span data-ttu-id="d6c02-148">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="d6c02-148">Click Yes.</span></span>
24. <span data-ttu-id="d6c02-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d6c02-149">Close the page.</span></span>


