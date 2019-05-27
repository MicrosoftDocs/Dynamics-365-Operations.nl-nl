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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555995"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="abf59-103">Een materiaalplan voor coproducten maken</span><span class="sxs-lookup"><span data-stu-id="abf59-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="abf59-104">De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.</span><span class="sxs-lookup"><span data-stu-id="abf59-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="abf59-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.</span><span class="sxs-lookup"><span data-stu-id="abf59-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="abf59-106">Vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="abf59-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="abf59-107">Ga naar Standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="abf59-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="abf59-108">Klik op Verkooporderverwerking en -onderzoek.</span><span class="sxs-lookup"><span data-stu-id="abf59-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="abf59-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="abf59-109">Click New.</span></span>
4. <span data-ttu-id="abf59-110">Klik op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="abf59-110">Click Sales order.</span></span>
5. <span data-ttu-id="abf59-111">Typ een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="abf59-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="abf59-112">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="abf59-112">Example: US-001</span></span>  
6. <span data-ttu-id="abf59-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="abf59-113">Click OK.</span></span>
7. <span data-ttu-id="abf59-114">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="abf59-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="abf59-115">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="abf59-115">Example: P6003</span></span>  
8. <span data-ttu-id="abf59-116">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="abf59-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="abf59-117">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="abf59-117">Example: 50000</span></span>  
9. <span data-ttu-id="abf59-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="abf59-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="abf59-119">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="abf59-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="abf59-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="abf59-120">Close the page.</span></span>
2. <span data-ttu-id="abf59-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="abf59-121">Close the page.</span></span>
3. <span data-ttu-id="abf59-122">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="abf59-122">Click Master planning.</span></span>
4. <span data-ttu-id="abf59-123">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="abf59-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="abf59-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="abf59-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="abf59-125">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="abf59-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="abf59-126">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="abf59-126">Click Run.</span></span>
7. <span data-ttu-id="abf59-127">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="abf59-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="abf59-128">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="abf59-128">Click Filter.</span></span>
9. <span data-ttu-id="abf59-129">Selecteer in de lijst de rij voor het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="abf59-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="abf59-130">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="abf59-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="abf59-131">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="abf59-131">Example: P6003</span></span>  
11. <span data-ttu-id="abf59-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="abf59-132">Click OK.</span></span>
12. <span data-ttu-id="abf59-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="abf59-133">Click OK.</span></span>
13. <span data-ttu-id="abf59-134">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="abf59-134">Click Planned orders.</span></span>
14. <span data-ttu-id="abf59-135">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="abf59-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="abf59-136">Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".</span><span class="sxs-lookup"><span data-stu-id="abf59-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="abf59-137">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="abf59-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="abf59-138">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="abf59-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="abf59-139">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="abf59-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="abf59-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="abf59-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="abf59-141">Vouw de sectie Tracering van behoefte uit of samen.</span><span class="sxs-lookup"><span data-stu-id="abf59-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="abf59-142">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="abf59-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="abf59-143">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="abf59-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="abf59-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="abf59-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="abf59-145">Vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="abf59-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="abf59-146">Ga naar Standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="abf59-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="abf59-147">Klik op Verkooporderverwerking en -onderzoek.</span><span class="sxs-lookup"><span data-stu-id="abf59-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="abf59-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="abf59-148">Click New.</span></span>
4. <span data-ttu-id="abf59-149">Klik op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="abf59-149">Click Sales order.</span></span>
5. <span data-ttu-id="abf59-150">Typ een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="abf59-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="abf59-151">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="abf59-151">Example: US-001</span></span>  
6. <span data-ttu-id="abf59-152">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="abf59-152">Click OK.</span></span>
7. <span data-ttu-id="abf59-153">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="abf59-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="abf59-154">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="abf59-154">Example: P6003</span></span>  
8. <span data-ttu-id="abf59-155">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="abf59-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="abf59-156">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="abf59-156">Example: 50000</span></span>  
9. <span data-ttu-id="abf59-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="abf59-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="abf59-158">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="abf59-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="abf59-159">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="abf59-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="abf59-160">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="abf59-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="abf59-161">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="abf59-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="abf59-162">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="abf59-162">Click Run.</span></span>
4. <span data-ttu-id="abf59-163">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="abf59-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="abf59-164">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="abf59-164">Click Filter.</span></span>
6. <span data-ttu-id="abf59-165">Selecteer in de lijst de rij voor het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="abf59-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="abf59-166">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="abf59-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="abf59-167">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="abf59-167">Example: P6003</span></span>  
8. <span data-ttu-id="abf59-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="abf59-168">Click OK.</span></span>
9. <span data-ttu-id="abf59-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="abf59-169">Click OK.</span></span>
10. <span data-ttu-id="abf59-170">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="abf59-170">Click Planned orders.</span></span>
11. <span data-ttu-id="abf59-171">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="abf59-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="abf59-172">Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".</span><span class="sxs-lookup"><span data-stu-id="abf59-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="abf59-173">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="abf59-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="abf59-174">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="abf59-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="abf59-175">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="abf59-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="abf59-176">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="abf59-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="abf59-177">Vouw de sectie Tracering van behoefte uit of samen.</span><span class="sxs-lookup"><span data-stu-id="abf59-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="abf59-178">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="abf59-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="abf59-179">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="abf59-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="abf59-180">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="abf59-180">Close the page.</span></span>
17. <span data-ttu-id="abf59-181">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="abf59-181">Click Master planning.</span></span>
18. <span data-ttu-id="abf59-182">Ga naar Hoofdplanning > Instellen > Hoofdplanning > Parameters hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="abf59-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="abf59-183">Selecteer Nee in het veld Alle planningsprocessen uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="abf59-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="abf59-184">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="abf59-184">Close the page.</span></span>

