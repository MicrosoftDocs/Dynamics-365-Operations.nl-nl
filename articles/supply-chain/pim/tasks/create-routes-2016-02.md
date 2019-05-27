---
title: Routes maken (februari 2016)
description: Deze taak is gericht op het maken van de productieroutes voor een eindproduct en een halffabricaat.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567837"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="23494-103">Routes maken (februari 2016)</span><span class="sxs-lookup"><span data-stu-id="23494-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23494-104">Deze taak is gericht op het maken van de productieroutes voor een eindproduct en een halffabricaat.</span><span class="sxs-lookup"><span data-stu-id="23494-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="23494-105">Dit is de vijfde taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="23494-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="23494-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="23494-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="23494-107">Een route voor een halffabricaat maken</span><span class="sxs-lookup"><span data-stu-id="23494-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="23494-108">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="23494-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="23494-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="23494-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23494-110">Selecteer het artikelnummer Stuklijst_2.</span><span class="sxs-lookup"><span data-stu-id="23494-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="23494-111">Klik op Technicus in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="23494-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="23494-112">Klik op Route.</span><span class="sxs-lookup"><span data-stu-id="23494-112">Click Route.</span></span>
5. <span data-ttu-id="23494-113">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="23494-113">Click New.</span></span>
6. <span data-ttu-id="23494-114">Klik op Route en routeversie.</span><span class="sxs-lookup"><span data-stu-id="23494-114">Click Route and route version.</span></span>
7. <span data-ttu-id="23494-115">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="23494-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="23494-116">Typ voor dit voorbeeld ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="23494-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="23494-117">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="23494-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="23494-118">Typ of selecteer voor dit voorbeeld Locatie 1.</span><span class="sxs-lookup"><span data-stu-id="23494-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="23494-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23494-119">Click OK.</span></span>
10. <span data-ttu-id="23494-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="23494-120">Click New.</span></span>
11. <span data-ttu-id="23494-121">Typ of selecteer een waarde in het veld Bewerking.</span><span class="sxs-lookup"><span data-stu-id="23494-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="23494-122">Selecteer voor dit voorbeeld Assembleren.</span><span class="sxs-lookup"><span data-stu-id="23494-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="23494-123">Voer een getal in het veld Uitvoeringstijd in.</span><span class="sxs-lookup"><span data-stu-id="23494-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="23494-124">Typ bijvoorbeeld 1.</span><span class="sxs-lookup"><span data-stu-id="23494-124">For example, type 1.</span></span> <span data-ttu-id="23494-125">Uitvoeringstijden maken vaak deel uit van de prijs die voor een artikel wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="23494-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="23494-126">Typ of selecteer een waarde in het veld Routegroep.</span><span class="sxs-lookup"><span data-stu-id="23494-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="23494-127">Selecteer voor dit voorbeeld 'Std'.</span><span class="sxs-lookup"><span data-stu-id="23494-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="23494-128">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="23494-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="23494-129">Typ of selecteer een waarde in het veld Instelcategorie.</span><span class="sxs-lookup"><span data-stu-id="23494-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="23494-130">Selecteer voor dit voorbeeld Assembleren.</span><span class="sxs-lookup"><span data-stu-id="23494-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="23494-131">Klik op het tabblad Tijden.</span><span class="sxs-lookup"><span data-stu-id="23494-131">Click the Times tab.</span></span>
17. <span data-ttu-id="23494-132">Voer in het veld Insteltijd een getal in.</span><span class="sxs-lookup"><span data-stu-id="23494-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="23494-133">Typ voor dit voorbeeld 1.</span><span class="sxs-lookup"><span data-stu-id="23494-133">For this example, type 1.</span></span> <span data-ttu-id="23494-134">Insteltijden maken vaak deel uit van de prijs die voor een artikel wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="23494-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="23494-135">Klik in het actievenster op Routeversie.</span><span class="sxs-lookup"><span data-stu-id="23494-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="23494-136">Klik op Goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="23494-136">Click Approve.</span></span>
20. <span data-ttu-id="23494-137">Selecteer Ja bij de vraag Wilt u ook de route goedkeuren?.</span><span class="sxs-lookup"><span data-stu-id="23494-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="23494-138">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23494-138">Click OK.</span></span>
22. <span data-ttu-id="23494-139">Klik in het actievenster op Routeversie.</span><span class="sxs-lookup"><span data-stu-id="23494-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="23494-140">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="23494-140">Click Activate.</span></span>
24. <span data-ttu-id="23494-141">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23494-141">Close the page.</span></span>
25. <span data-ttu-id="23494-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23494-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="23494-143">Een route voor een eindproduct maken</span><span class="sxs-lookup"><span data-stu-id="23494-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="23494-144">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="23494-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="23494-145">Selecteer het artikelnummer Stuklijst_1.</span><span class="sxs-lookup"><span data-stu-id="23494-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="23494-146">Klik op Technicus in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="23494-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="23494-147">Klik op Route.</span><span class="sxs-lookup"><span data-stu-id="23494-147">Click Route.</span></span>
4. <span data-ttu-id="23494-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="23494-148">Click New.</span></span>
5. <span data-ttu-id="23494-149">Klik op Route en routeversie.</span><span class="sxs-lookup"><span data-stu-id="23494-149">Click Route and route version.</span></span>
6. <span data-ttu-id="23494-150">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="23494-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="23494-151">Typ voor dit voorbeeld ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="23494-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="23494-152">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="23494-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="23494-153">Typ of selecteer voor dit voorbeeld Locatie 1.</span><span class="sxs-lookup"><span data-stu-id="23494-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="23494-154">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23494-154">Click OK.</span></span>
9. <span data-ttu-id="23494-155">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="23494-155">Click New.</span></span>
10. <span data-ttu-id="23494-156">Typ of selecteer een waarde in het veld Bewerking.</span><span class="sxs-lookup"><span data-stu-id="23494-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="23494-157">Selecteer voor dit voorbeeld Verpakken.</span><span class="sxs-lookup"><span data-stu-id="23494-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="23494-158">Voer een getal in het veld Uitvoeringstijd in.</span><span class="sxs-lookup"><span data-stu-id="23494-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="23494-159">Typ voor dit voorbeeld 1.</span><span class="sxs-lookup"><span data-stu-id="23494-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="23494-160">Typ of selecteer een waarde in het veld Routegroep.</span><span class="sxs-lookup"><span data-stu-id="23494-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="23494-161">Selecteer voor dit voorbeeld 'Std'.</span><span class="sxs-lookup"><span data-stu-id="23494-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="23494-162">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="23494-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="23494-163">Typ of selecteer een waarde in het veld Instelcategorie.</span><span class="sxs-lookup"><span data-stu-id="23494-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="23494-164">Selecteer voor dit voorbeeld Verpakken.</span><span class="sxs-lookup"><span data-stu-id="23494-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="23494-165">Klik op het tabblad Tijden.</span><span class="sxs-lookup"><span data-stu-id="23494-165">Click the Times tab.</span></span>
16. <span data-ttu-id="23494-166">Voer in het veld Insteltijd een getal in.</span><span class="sxs-lookup"><span data-stu-id="23494-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="23494-167">Typ voor dit voorbeeld 1.</span><span class="sxs-lookup"><span data-stu-id="23494-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="23494-168">Klik in het actievenster op Routeversie.</span><span class="sxs-lookup"><span data-stu-id="23494-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="23494-169">Klik op Goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="23494-169">Click Approve.</span></span>
19. <span data-ttu-id="23494-170">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="23494-170">Click OK.</span></span>
20. <span data-ttu-id="23494-171">Klik in het actievenster op Routeversie.</span><span class="sxs-lookup"><span data-stu-id="23494-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="23494-172">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="23494-172">Click Activate.</span></span>
22. <span data-ttu-id="23494-173">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23494-173">Close the page.</span></span>
23. <span data-ttu-id="23494-174">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23494-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="23494-175">Automatisch verbruik van de insteltijd inschakelen</span><span class="sxs-lookup"><span data-stu-id="23494-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="23494-176">Ga naar Productiebeheer > Instellingen > Routes > Routegroepen.</span><span class="sxs-lookup"><span data-stu-id="23494-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="23494-177">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="23494-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="23494-178">Selecteer in de lijst 'Std'.</span><span class="sxs-lookup"><span data-stu-id="23494-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="23494-179">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="23494-179">Click Edit.</span></span>
4. <span data-ttu-id="23494-180">Selecteer Ja in het veld Insteltijd.</span><span class="sxs-lookup"><span data-stu-id="23494-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="23494-181">Insteltijden maken vaak deel uit van de prijs die voor een artikel wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="23494-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="23494-182">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="23494-182">Click Save.</span></span>
6. <span data-ttu-id="23494-183">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="23494-183">Close the page.</span></span>

