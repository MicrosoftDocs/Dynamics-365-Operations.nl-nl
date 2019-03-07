---
title: Een materiaalplan voor coproducten maken
description: De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "337136"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e60a6-103">Een materiaalplan voor coproducten maken</span><span class="sxs-lookup"><span data-stu-id="e60a6-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e60a6-104">De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.</span><span class="sxs-lookup"><span data-stu-id="e60a6-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="e60a6-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.</span><span class="sxs-lookup"><span data-stu-id="e60a6-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="e60a6-106">Vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="e60a6-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="e60a6-107">Ga naar Standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="e60a6-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="e60a6-108">Klik op Verkooporderverwerking en -onderzoek.</span><span class="sxs-lookup"><span data-stu-id="e60a6-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="e60a6-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e60a6-109">Click New.</span></span>
4. <span data-ttu-id="e60a6-110">Klik op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="e60a6-110">Click Sales order.</span></span>
5. <span data-ttu-id="e60a6-111">Typ een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="e60a6-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="e60a6-112">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="e60a6-112">Example: US-001</span></span>  
6. <span data-ttu-id="e60a6-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e60a6-113">Click OK.</span></span>
7. <span data-ttu-id="e60a6-114">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e60a6-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="e60a6-115">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="e60a6-115">Example: P6003</span></span>  
8. <span data-ttu-id="e60a6-116">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="e60a6-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e60a6-117">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="e60a6-117">Example: 50000</span></span>  
9. <span data-ttu-id="e60a6-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e60a6-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e60a6-119">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="e60a6-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="e60a6-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e60a6-120">Close the page.</span></span>
2. <span data-ttu-id="e60a6-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e60a6-121">Close the page.</span></span>
3. <span data-ttu-id="e60a6-122">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e60a6-122">Click Master planning.</span></span>
4. <span data-ttu-id="e60a6-123">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e60a6-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e60a6-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e60a6-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e60a6-125">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="e60a6-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="e60a6-126">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e60a6-126">Click Run.</span></span>
7. <span data-ttu-id="e60a6-127">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="e60a6-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="e60a6-128">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="e60a6-128">Click Filter.</span></span>
9. <span data-ttu-id="e60a6-129">Selecteer in de lijst de rij voor het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e60a6-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="e60a6-130">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="e60a6-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="e60a6-131">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="e60a6-131">Example: P6003</span></span>  
11. <span data-ttu-id="e60a6-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e60a6-132">Click OK.</span></span>
12. <span data-ttu-id="e60a6-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e60a6-133">Click OK.</span></span>
13. <span data-ttu-id="e60a6-134">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="e60a6-134">Click Planned orders.</span></span>
14. <span data-ttu-id="e60a6-135">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="e60a6-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e60a6-136">Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".</span><span class="sxs-lookup"><span data-stu-id="e60a6-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="e60a6-137">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e60a6-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="e60a6-138">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e60a6-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e60a6-139">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e60a6-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="e60a6-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e60a6-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="e60a6-141">Vouw de sectie Tracering van behoefte uit of samen.</span><span class="sxs-lookup"><span data-stu-id="e60a6-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="e60a6-142">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e60a6-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e60a6-143">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="e60a6-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="e60a6-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e60a6-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="e60a6-145">Vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="e60a6-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="e60a6-146">Ga naar Standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="e60a6-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="e60a6-147">Klik op Verkooporderverwerking en -onderzoek.</span><span class="sxs-lookup"><span data-stu-id="e60a6-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="e60a6-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e60a6-148">Click New.</span></span>
4. <span data-ttu-id="e60a6-149">Klik op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="e60a6-149">Click Sales order.</span></span>
5. <span data-ttu-id="e60a6-150">Typ een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="e60a6-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="e60a6-151">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="e60a6-151">Example: US-001</span></span>  
6. <span data-ttu-id="e60a6-152">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e60a6-152">Click OK.</span></span>
7. <span data-ttu-id="e60a6-153">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e60a6-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="e60a6-154">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="e60a6-154">Example: P6003</span></span>  
8. <span data-ttu-id="e60a6-155">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="e60a6-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e60a6-156">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="e60a6-156">Example: 50000</span></span>  
9. <span data-ttu-id="e60a6-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="e60a6-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e60a6-158">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="e60a6-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="e60a6-159">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e60a6-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="e60a6-160">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e60a6-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e60a6-161">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="e60a6-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="e60a6-162">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="e60a6-162">Click Run.</span></span>
4. <span data-ttu-id="e60a6-163">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="e60a6-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="e60a6-164">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="e60a6-164">Click Filter.</span></span>
6. <span data-ttu-id="e60a6-165">Selecteer in de lijst de rij voor het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e60a6-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="e60a6-166">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="e60a6-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="e60a6-167">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="e60a6-167">Example: P6003</span></span>  
8. <span data-ttu-id="e60a6-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e60a6-168">Click OK.</span></span>
9. <span data-ttu-id="e60a6-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e60a6-169">Click OK.</span></span>
10. <span data-ttu-id="e60a6-170">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="e60a6-170">Click Planned orders.</span></span>
11. <span data-ttu-id="e60a6-171">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="e60a6-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e60a6-172">Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".</span><span class="sxs-lookup"><span data-stu-id="e60a6-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="e60a6-173">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e60a6-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="e60a6-174">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e60a6-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e60a6-175">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e60a6-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="e60a6-176">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e60a6-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="e60a6-177">Vouw de sectie Tracering van behoefte uit of samen.</span><span class="sxs-lookup"><span data-stu-id="e60a6-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="e60a6-178">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e60a6-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e60a6-179">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="e60a6-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="e60a6-180">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e60a6-180">Close the page.</span></span>
17. <span data-ttu-id="e60a6-181">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e60a6-181">Click Master planning.</span></span>
18. <span data-ttu-id="e60a6-182">Ga naar Hoofdplanning > Instellen > Hoofdplanning > Parameters hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="e60a6-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="e60a6-183">Selecteer Nee in het veld Alle planningsprocessen uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="e60a6-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="e60a6-184">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e60a6-184">Close the page.</span></span>

