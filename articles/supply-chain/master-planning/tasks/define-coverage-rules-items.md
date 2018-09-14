--- 
title: "Behoefteplanningsregels voor artikelen definiëren"
description: Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="9997e-103">Behoefteplanningsregels voor artikelen definiëren</span><span class="sxs-lookup"><span data-stu-id="9997e-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9997e-104">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="9997e-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9997e-105">Deze procedure toont hoe u behoefteplanningsregels maakt en behoefteplanningsinstellingen voor een specifiek artikel overschrijft.</span><span class="sxs-lookup"><span data-stu-id="9997e-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="9997e-106">Het toont ook hoe u standaardvoorraadinstellingen opgeeft.</span><span class="sxs-lookup"><span data-stu-id="9997e-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="9997e-107">Een behoefteplanningsgroep maken</span><span class="sxs-lookup"><span data-stu-id="9997e-107">Create a coverage group</span></span>
1. <span data-ttu-id="9997e-108">Ga naar Behoefteplanningsgroepen.</span><span class="sxs-lookup"><span data-stu-id="9997e-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="9997e-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9997e-109">Click New.</span></span>
3. <span data-ttu-id="9997e-110">Typ een waarde in het veld Dekkingsgroep.</span><span class="sxs-lookup"><span data-stu-id="9997e-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="9997e-111">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="9997e-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9997e-112">Typ een waarde in het veld Agenda.</span><span class="sxs-lookup"><span data-stu-id="9997e-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="9997e-113">Kies de agenda die tijdens hoofdplanning wordt gebruikt om aanvullingssuggesties te doen voor artikelen in deze groep.</span><span class="sxs-lookup"><span data-stu-id="9997e-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="9997e-114">Selecteer een optie in het veld Bestelmethode.</span><span class="sxs-lookup"><span data-stu-id="9997e-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="9997e-115">Selecteer Vereisten voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="9997e-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="9997e-116">Voer 90 in het veld Time fence dekking (dagen) in.</span><span class="sxs-lookup"><span data-stu-id="9997e-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="9997e-117">Voor artikelen in deze groep maakt de hoofdplanning aanvullingssuggesties tot maximaal 90 dagen in de toekomst.</span><span class="sxs-lookup"><span data-stu-id="9997e-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="9997e-118">Voer 1 in het veld Negatieve dagen in.</span><span class="sxs-lookup"><span data-stu-id="9997e-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="9997e-119">Voer 1 in het veld Positieve dagen in.</span><span class="sxs-lookup"><span data-stu-id="9997e-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="9997e-120">Vouw de sectie Overige uit of samen.</span><span class="sxs-lookup"><span data-stu-id="9997e-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="9997e-121">Typ 1 in het veld Ontvangstmarge opgeteld bij behoeftedatum.</span><span class="sxs-lookup"><span data-stu-id="9997e-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="9997e-122">Als bijvoorbeeld de ontvangstmarge is ingesteld op 1 dag en een inkooporderregel is gepland voor ontvangst op 15 mei, berekent de hoofdplanning de aangepaste ontvangstdatum als 16 mei.</span><span class="sxs-lookup"><span data-stu-id="9997e-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="9997e-123">Typ 1 in het veld Uitgiftemarge afgetrokken van behoeftedatum.</span><span class="sxs-lookup"><span data-stu-id="9997e-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="9997e-124">Als bijvoorbeeld de veiligheidsmarge is ingesteld op 1 dag en een verkooporderregel is gepland voor levering op 15 mei, berekent de hoofdplanning de aangepaste leveringsdatum als 14 mei.</span><span class="sxs-lookup"><span data-stu-id="9997e-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="9997e-125">Typ 1 in het veld Bestelmarge opgeteld bij doorlooptijd van artikel.</span><span class="sxs-lookup"><span data-stu-id="9997e-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="9997e-126">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9997e-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="9997e-127">Een nieuw product maken</span><span class="sxs-lookup"><span data-stu-id="9997e-127">Create a new product</span></span>
1. <span data-ttu-id="9997e-128">Ga naar Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="9997e-128">Go to Released products.</span></span>
2. <span data-ttu-id="9997e-129">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9997e-129">Click New.</span></span>
3. <span data-ttu-id="9997e-130">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="9997e-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="9997e-131">Typ een waarde in het veld Productnaam.</span><span class="sxs-lookup"><span data-stu-id="9997e-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="9997e-132">Klik in het veld Artikelmodelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="9997e-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9997e-133">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9997e-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9997e-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9997e-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9997e-135">Klik in het veld Artikelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="9997e-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9997e-136">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9997e-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9997e-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9997e-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="9997e-138">Klik in het veld Opslagdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="9997e-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="9997e-139">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9997e-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="9997e-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9997e-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9997e-141">Klik in het veld Traceringsdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="9997e-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="9997e-142">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="9997e-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="9997e-143">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9997e-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9997e-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="9997e-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="9997e-145">Standaard orderinstellingen instellen</span><span class="sxs-lookup"><span data-stu-id="9997e-145">Setup default order settings</span></span>
1. <span data-ttu-id="9997e-146">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="9997e-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="9997e-147">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="9997e-147">Click Default order settings.</span></span>
3. <span data-ttu-id="9997e-148">Typ in het veld Inkoopvestiging de locatie die als standaard wordt gebruikt wanneer de inkooporders worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9997e-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="9997e-149">Typ in het veld Voorraadvestiging de locatie waar het artikel wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="9997e-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="9997e-150">Vouw de sectie Voorraad uit of samen.</span><span class="sxs-lookup"><span data-stu-id="9997e-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="9997e-151">Stel Meerdere in op 10.</span><span class="sxs-lookup"><span data-stu-id="9997e-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="9997e-152">Stel Min.</span><span class="sxs-lookup"><span data-stu-id="9997e-152">Set Min.</span></span> <span data-ttu-id="9997e-153">bestelhoeveelheid in op 10.</span><span class="sxs-lookup"><span data-stu-id="9997e-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="9997e-154">Stel Max.</span><span class="sxs-lookup"><span data-stu-id="9997e-154">Set Max.</span></span> <span data-ttu-id="9997e-155">bestelhoeveelheid in op 100.</span><span class="sxs-lookup"><span data-stu-id="9997e-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="9997e-156">Stel Standaardbestelhoeveelheid in op 10.</span><span class="sxs-lookup"><span data-stu-id="9997e-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="9997e-157">Voer een nummer in het veld Inkoopdoorlooptijd in.</span><span class="sxs-lookup"><span data-stu-id="9997e-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="9997e-158">Schakel het selectievakje Werkdagen in of uit.</span><span class="sxs-lookup"><span data-stu-id="9997e-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="9997e-159">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9997e-159">Click Save.</span></span>
13. <span data-ttu-id="9997e-160">Selecteer Inkooporder in het veld Standaardordertype.</span><span class="sxs-lookup"><span data-stu-id="9997e-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="9997e-161">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9997e-161">Click Save.</span></span>
15. <span data-ttu-id="9997e-162">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="9997e-162">Close the page.</span></span>
    * <span data-ttu-id="9997e-163">Sluit de pagina Standaard orderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="9997e-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="9997e-164">Een artikel aan een dekkingsgroep toevoegen</span><span class="sxs-lookup"><span data-stu-id="9997e-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="9997e-165">Vouw de sectie Planning uit of samen.</span><span class="sxs-lookup"><span data-stu-id="9997e-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="9997e-166">Klik in het veld Dekkingsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="9997e-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9997e-167">Zoek in de lijst de Dekkingsgroep die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9997e-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="9997e-168">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9997e-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="9997e-169">Regels artikelbehoefteplanning maken</span><span class="sxs-lookup"><span data-stu-id="9997e-169">Create item coverage rules</span></span>
1. <span data-ttu-id="9997e-170">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="9997e-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="9997e-171">Klik op Artikelbehoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="9997e-171">Click Item coverage.</span></span>
3. <span data-ttu-id="9997e-172">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9997e-172">Click New.</span></span>
4. <span data-ttu-id="9997e-173">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="9997e-173">Click the General tab.</span></span>
5. <span data-ttu-id="9997e-174">Schakel het vakje in de kop van Instellingen behoefteplanningsgroep overschrijven in.</span><span class="sxs-lookup"><span data-stu-id="9997e-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="9997e-175">Voer 60 in het veld Time fence dekking (dagen) in.</span><span class="sxs-lookup"><span data-stu-id="9997e-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="9997e-176">Hoewel artikelen in een behoefteplanningsgroep 90 dagen vooruit worden gepland, wordt dit artikel 60 dagen vooruit gepland.</span><span class="sxs-lookup"><span data-stu-id="9997e-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="9997e-177">Voer 2 in het veld Negatieve dagen in.</span><span class="sxs-lookup"><span data-stu-id="9997e-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="9997e-178">Voer 2 in het veld Positieve dagen in.</span><span class="sxs-lookup"><span data-stu-id="9997e-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="9997e-179">Klik op het tabblad Levertijd.</span><span class="sxs-lookup"><span data-stu-id="9997e-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="9997e-180">Schakel het vakje in de kop van Inkoop in.</span><span class="sxs-lookup"><span data-stu-id="9997e-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="9997e-181">Voer in het veld Inkooptijd 5 in.</span><span class="sxs-lookup"><span data-stu-id="9997e-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="9997e-182">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9997e-182">Click Save.</span></span>


