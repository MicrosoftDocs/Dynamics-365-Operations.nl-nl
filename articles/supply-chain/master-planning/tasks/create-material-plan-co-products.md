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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148073"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="78033-103">Een materiaalplan voor coproducten maken</span><span class="sxs-lookup"><span data-stu-id="78033-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78033-104">De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.</span><span class="sxs-lookup"><span data-stu-id="78033-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="78033-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.</span><span class="sxs-lookup"><span data-stu-id="78033-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="78033-106">Vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="78033-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="78033-107">Ga naar Standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="78033-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="78033-108">Klik op Verkooporderverwerking en -onderzoek.</span><span class="sxs-lookup"><span data-stu-id="78033-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="78033-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="78033-109">Click New.</span></span>
4. <span data-ttu-id="78033-110">Klik op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="78033-110">Click Sales order.</span></span>
5. <span data-ttu-id="78033-111">Typ een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="78033-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="78033-112">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="78033-112">Example: US-001</span></span>  
6. <span data-ttu-id="78033-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="78033-113">Click OK.</span></span>
7. <span data-ttu-id="78033-114">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="78033-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="78033-115">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="78033-115">Example: P6003</span></span>  
8. <span data-ttu-id="78033-116">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="78033-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="78033-117">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="78033-117">Example: 50000</span></span>  
9. <span data-ttu-id="78033-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="78033-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="78033-119">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="78033-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="78033-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="78033-120">Close the page.</span></span>
2. <span data-ttu-id="78033-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="78033-121">Close the page.</span></span>
3. <span data-ttu-id="78033-122">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="78033-122">Click Master planning.</span></span>
4. <span data-ttu-id="78033-123">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="78033-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="78033-124">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="78033-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78033-125">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="78033-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="78033-126">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="78033-126">Click Run.</span></span>
7. <span data-ttu-id="78033-127">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="78033-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="78033-128">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="78033-128">Click Filter.</span></span>
9. <span data-ttu-id="78033-129">Selecteer in de lijst de rij voor het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="78033-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="78033-130">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="78033-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="78033-131">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="78033-131">Example: P6003</span></span>  
11. <span data-ttu-id="78033-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="78033-132">Click OK.</span></span>
12. <span data-ttu-id="78033-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="78033-133">Click OK.</span></span>
13. <span data-ttu-id="78033-134">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="78033-134">Click Planned orders.</span></span>
14. <span data-ttu-id="78033-135">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="78033-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="78033-136">Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".</span><span class="sxs-lookup"><span data-stu-id="78033-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="78033-137">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="78033-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="78033-138">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="78033-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="78033-139">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="78033-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="78033-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="78033-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="78033-141">Vouw de sectie Tracering van behoefte uit of samen.</span><span class="sxs-lookup"><span data-stu-id="78033-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="78033-142">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="78033-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78033-143">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="78033-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="78033-144">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="78033-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="78033-145">Vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="78033-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="78033-146">Ga naar Standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="78033-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="78033-147">Klik op Verkooporderverwerking en -onderzoek.</span><span class="sxs-lookup"><span data-stu-id="78033-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="78033-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="78033-148">Click New.</span></span>
4. <span data-ttu-id="78033-149">Klik op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="78033-149">Click Sales order.</span></span>
5. <span data-ttu-id="78033-150">Typ een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="78033-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="78033-151">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="78033-151">Example: US-001</span></span>  
6. <span data-ttu-id="78033-152">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="78033-152">Click OK.</span></span>
7. <span data-ttu-id="78033-153">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="78033-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="78033-154">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="78033-154">Example: P6003</span></span>  
8. <span data-ttu-id="78033-155">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="78033-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="78033-156">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="78033-156">Example: 50000</span></span>  
9. <span data-ttu-id="78033-157">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="78033-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="78033-158">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="78033-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="78033-159">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="78033-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="78033-160">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="78033-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78033-161">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="78033-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="78033-162">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="78033-162">Click Run.</span></span>
4. <span data-ttu-id="78033-163">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="78033-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="78033-164">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="78033-164">Click Filter.</span></span>
6. <span data-ttu-id="78033-165">Selecteer in de lijst de rij voor het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="78033-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="78033-166">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="78033-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="78033-167">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="78033-167">Example: P6003</span></span>  
8. <span data-ttu-id="78033-168">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="78033-168">Click OK.</span></span>
9. <span data-ttu-id="78033-169">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="78033-169">Click OK.</span></span>
10. <span data-ttu-id="78033-170">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="78033-170">Click Planned orders.</span></span>
11. <span data-ttu-id="78033-171">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="78033-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="78033-172">Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".</span><span class="sxs-lookup"><span data-stu-id="78033-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="78033-173">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="78033-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="78033-174">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="78033-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="78033-175">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="78033-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="78033-176">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="78033-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="78033-177">Vouw de sectie Tracering van behoefte uit of samen.</span><span class="sxs-lookup"><span data-stu-id="78033-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="78033-178">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="78033-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="78033-179">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="78033-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="78033-180">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="78033-180">Close the page.</span></span>
17. <span data-ttu-id="78033-181">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="78033-181">Click Master planning.</span></span>
18. <span data-ttu-id="78033-182">Ga naar Hoofdplanning > Instellen > Hoofdplanning > Parameters hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="78033-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="78033-183">Selecteer Nee in het veld Alle planningsprocessen uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="78033-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="78033-184">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="78033-184">Close the page.</span></span>

