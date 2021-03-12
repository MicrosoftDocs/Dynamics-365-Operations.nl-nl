---
title: Behoefteplanningsregels voor artikelen definiëren
description: Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c156ae4a8a19a428378581a0d5c7dc01d86b5ec7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999876"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="44239-103">Behoefteplanningsregels voor artikelen definiëren</span><span class="sxs-lookup"><span data-stu-id="44239-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44239-104">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="44239-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="44239-105">Deze procedure toont hoe u behoefteplanningsregels maakt en behoefteplanningsinstellingen voor een specifiek artikel overschrijft.</span><span class="sxs-lookup"><span data-stu-id="44239-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="44239-106">Het toont ook hoe u standaardvoorraadinstellingen opgeeft.</span><span class="sxs-lookup"><span data-stu-id="44239-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="44239-107">Een behoefteplanningsgroep maken</span><span class="sxs-lookup"><span data-stu-id="44239-107">Create a coverage group</span></span>
1. <span data-ttu-id="44239-108">Ga naar **Navigatievenster > Modules > Hoofdplanning > Instellen >Behoefteplanningsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="44239-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="44239-109">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="44239-109">Click **New**.</span></span>
3. <span data-ttu-id="44239-110">Typ een waarde in het veld **Behoefteplanningsgroep**.</span><span class="sxs-lookup"><span data-stu-id="44239-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="44239-111">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="44239-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="44239-112">Typ een waarde in het veld **Agenda**.</span><span class="sxs-lookup"><span data-stu-id="44239-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="44239-113">Kies de agenda die tijdens hoofdplanning wordt gebruikt om aanvullingssuggesties te doen voor artikelen in deze groep.</span><span class="sxs-lookup"><span data-stu-id="44239-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="44239-114">Selecteer een optie in het veld **Behoefteplanningscode**.</span><span class="sxs-lookup"><span data-stu-id="44239-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="44239-115">Selecteer 'Vereiste' voor deze procedure.</span><span class="sxs-lookup"><span data-stu-id="44239-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="44239-116">Voer 90 in het veld **Time fence behoefteplanning (dagen)** in.</span><span class="sxs-lookup"><span data-stu-id="44239-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="44239-117">Voor artikelen in deze groep maakt de hoofdplanning aanvullingssuggesties tot maximaal 90 dagen in de toekomst.</span><span class="sxs-lookup"><span data-stu-id="44239-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="44239-118">Voer 1 in het veld **Negatieve dagen** in.</span><span class="sxs-lookup"><span data-stu-id="44239-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="44239-119">Voer 1 in het veld **Positieve dagen** in.</span><span class="sxs-lookup"><span data-stu-id="44239-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="44239-120">Vouw de sectie **Overige** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="44239-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="44239-121">Ga naar de sectie **Veiligheidsmarges in dagen** en voer in het veld **Ontvangstmarge toegevoegd aan behoeftedatum** 1 in.</span><span class="sxs-lookup"><span data-stu-id="44239-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="44239-122">Als bijvoorbeeld de ontvangstmarge is ingesteld op 1 dag en een inkooporderregel is gepland voor ontvangst op 15 mei, berekent de hoofdplanning de aangepaste ontvangstdatum als 16 mei.</span><span class="sxs-lookup"><span data-stu-id="44239-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="44239-123">Typ 1 in het veld **Uitgiftemarge afgetrokken van behoeftedatum**.</span><span class="sxs-lookup"><span data-stu-id="44239-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="44239-124">Als bijvoorbeeld de veiligheidsmarge is ingesteld op 1 dag en een verkooporderregel is gepland voor levering op 15 mei, berekent de hoofdplanning de aangepaste leveringsdatum als 14 mei.</span><span class="sxs-lookup"><span data-stu-id="44239-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="44239-125">Typ 1 in het veld **Bestelmarge opgeteld bij doorlooptijd van artikel**.</span><span class="sxs-lookup"><span data-stu-id="44239-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="44239-126">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="44239-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="44239-127">Een nieuw product maken</span><span class="sxs-lookup"><span data-stu-id="44239-127">Create a new product</span></span>
1. <span data-ttu-id="44239-128">Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="44239-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="44239-129">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="44239-129">Click **New**.</span></span>
3. <span data-ttu-id="44239-130">Typ een waarde in het veld **Productnummer**.</span><span class="sxs-lookup"><span data-stu-id="44239-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="44239-131">Typ een waarde in het veld **Productnaam**.</span><span class="sxs-lookup"><span data-stu-id="44239-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="44239-132">Klik in het veld **Artikelmodelgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="44239-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="44239-133">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="44239-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="44239-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="44239-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="44239-135">Klik in het veld **Artikelgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="44239-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="44239-136">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="44239-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="44239-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="44239-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="44239-138">Klik in het veld **Opslagdimensiegroep** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="44239-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="44239-139">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="44239-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="44239-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="44239-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="44239-141">Klik in het veld **Traceringsdimensiegroep** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="44239-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="44239-142">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="44239-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="44239-143">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="44239-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="44239-144">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="44239-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="44239-145">Standaard orderinstellingen instellen</span><span class="sxs-lookup"><span data-stu-id="44239-145">Setup default order settings</span></span>
1. <span data-ttu-id="44239-146">Klik op **Plannen** in het **actievenster**.</span><span class="sxs-lookup"><span data-stu-id="44239-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="44239-147">Klik onder **Orderinstellingen** op **Standaardorderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="44239-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="44239-148">Ga naar **Inkooporder** en typ in het veld **Standaardvestiging** de vestiging die als standaard moet worden gebruikt wanneer de inkooporders worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="44239-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="44239-149">Typ in het veld **Standaardmagazijn** de vestiging waar het artikel is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="44239-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="44239-150">Vouw de sectie **Voorraad** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="44239-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="44239-151">Typ 10 in het veld **Meerdere**.</span><span class="sxs-lookup"><span data-stu-id="44239-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="44239-152">Typ 10 in het veld **Min.bestelhoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="44239-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="44239-153">Typ 100 in het veld **Max.bestelhoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="44239-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="44239-154">Typ 10 in het veld **Standaardbestelhoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="44239-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="44239-155">Voer een numerieke waarde in het veld **Inkoopdoorlooptijd** in.</span><span class="sxs-lookup"><span data-stu-id="44239-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="44239-156">Schakel het selectievakje **Werkdagen** in of uit.</span><span class="sxs-lookup"><span data-stu-id="44239-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="44239-157">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="44239-157">Click **Save**.</span></span>
13. <span data-ttu-id="44239-158">Selecteer Inkooporder in het veld **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="44239-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="44239-159">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="44239-159">Click **Save**.</span></span>
15. <span data-ttu-id="44239-160">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="44239-160">Close the page.</span></span> <span data-ttu-id="44239-161">Sluit de pagina Standaard orderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="44239-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="44239-162">Een artikel aan een behoefteplanningsgroep toevoegen</span><span class="sxs-lookup"><span data-stu-id="44239-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="44239-163">Vouw de sectie **Planning** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="44239-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="44239-164">Klik in het veld **Behoefteplanningsgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="44239-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="44239-165">Zoek in de lijst de **Behoefteplanningssgroep** die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="44239-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="44239-166">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="44239-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="44239-167">Regels artikelbehoefteplanning maken</span><span class="sxs-lookup"><span data-stu-id="44239-167">Create item coverage rules</span></span>
1. <span data-ttu-id="44239-168">Klik op **Plannen** in het **actievenster**.</span><span class="sxs-lookup"><span data-stu-id="44239-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="44239-169">Klik onder **Behoefteplanning** op **Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="44239-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="44239-170">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="44239-170">Click **New**.</span></span>
4. <span data-ttu-id="44239-171">Klik op het tabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="44239-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="44239-172">Schakel het vakje in de kop van **Instellingen behoefteplanningsgroep overschrijven** in.</span><span class="sxs-lookup"><span data-stu-id="44239-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="44239-173">Voer 60 in het veld **Time fence behoefteplanning (dagen)** in.</span><span class="sxs-lookup"><span data-stu-id="44239-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="44239-174">Hoewel artikelen in een behoefteplanningsgroep 90 dagen vooruit worden gepland, wordt dit artikel 60 dagen vooruit gepland.</span><span class="sxs-lookup"><span data-stu-id="44239-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="44239-175">Voer 2 in het veld **Negatieve dagen** in.</span><span class="sxs-lookup"><span data-stu-id="44239-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="44239-176">Voer 2 in het veld **Positieve dagen** in.</span><span class="sxs-lookup"><span data-stu-id="44239-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="44239-177">Klik op het tabblad **Levertijd**.</span><span class="sxs-lookup"><span data-stu-id="44239-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="44239-178">Schakel het vakje in de kop van **Inkoop** in.</span><span class="sxs-lookup"><span data-stu-id="44239-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="44239-179">Voer in het veld **Inkooptijd** 5 in.</span><span class="sxs-lookup"><span data-stu-id="44239-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="44239-180">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="44239-180">Click **Save**.</span></span>

