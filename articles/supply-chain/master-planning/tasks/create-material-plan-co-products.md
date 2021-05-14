---
title: Een materiaalplan voor coproducten maken
description: De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920724"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="558dd-103">Een materiaalplan voor coproducten maken</span><span class="sxs-lookup"><span data-stu-id="558dd-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="558dd-104">De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.</span><span class="sxs-lookup"><span data-stu-id="558dd-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="558dd-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.</span><span class="sxs-lookup"><span data-stu-id="558dd-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="558dd-106">Vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="558dd-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="558dd-107">Ga naar **Verkoop en marketing \> Werkgebieden \> Verkooporderverwerking en -onderzoek**.</span><span class="sxs-lookup"><span data-stu-id="558dd-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="558dd-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="558dd-108">Select **New**.</span></span>
1. <span data-ttu-id="558dd-109">Selecteer **Verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="558dd-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="558dd-110">Typ een waarde in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="558dd-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="558dd-111">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="558dd-111">Example: US-001</span></span>  
1. <span data-ttu-id="558dd-112">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="558dd-112">Select **OK**.</span></span>
1. <span data-ttu-id="558dd-113">Typ een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="558dd-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="558dd-114">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="558dd-114">Example: P6003</span></span>  
1. <span data-ttu-id="558dd-115">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="558dd-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="558dd-116">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="558dd-116">Example: 50000</span></span>  
1. <span data-ttu-id="558dd-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="558dd-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="558dd-118">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="558dd-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="558dd-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="558dd-119">Close the page.</span></span>
1. <span data-ttu-id="558dd-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="558dd-120">Close the page.</span></span>
1. <span data-ttu-id="558dd-121">Selecteer **Hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="558dd-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="558dd-122">Selecteer in het veld **Plan** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="558dd-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="558dd-123">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="558dd-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="558dd-124">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="558dd-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="558dd-125">Selecteer **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="558dd-125">Select **Run**.</span></span>
1. <span data-ttu-id="558dd-126">Vouw de sectie **Op te nemen records** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="558dd-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="558dd-127">Selecteer **Filter**.</span><span class="sxs-lookup"><span data-stu-id="558dd-127">Select **Filter**.</span></span>
1. <span data-ttu-id="558dd-128">Selecteer in de lijst de rij voor **Veld** = *Artikelnummer*.</span><span class="sxs-lookup"><span data-stu-id="558dd-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="558dd-129">Typ een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="558dd-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="558dd-130">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="558dd-130">Example: P6003</span></span>  
1. <span data-ttu-id="558dd-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="558dd-131">Select **OK**.</span></span>
1. <span data-ttu-id="558dd-132">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="558dd-132">Select **OK**.</span></span>
1. <span data-ttu-id="558dd-133">Selecteer **Geplande orders**.</span><span class="sxs-lookup"><span data-stu-id="558dd-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="558dd-134">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="558dd-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="558dd-135">Filter bijvoorbeeld op het Veld **Artikelnummer** op de waarde 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="558dd-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="558dd-136">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="558dd-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="558dd-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="558dd-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="558dd-138">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="558dd-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="558dd-139">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="558dd-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="558dd-140">Vouw de sectie **Tracering van behoefte** uit.</span><span class="sxs-lookup"><span data-stu-id="558dd-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="558dd-141">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="558dd-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="558dd-142">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="558dd-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="558dd-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="558dd-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="558dd-144">Een tweede vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="558dd-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="558dd-145">Ga naar **Verkoop en marketing \> Werkgebieden \> Verkooporderverwerking en -onderzoek**.</span><span class="sxs-lookup"><span data-stu-id="558dd-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="558dd-146">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="558dd-146">Select **New**.</span></span>
1. <span data-ttu-id="558dd-147">Selecteer **Verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="558dd-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="558dd-148">Typ een waarde in het veld **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="558dd-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="558dd-149">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="558dd-149">Example: US-001</span></span>  
1. <span data-ttu-id="558dd-150">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="558dd-150">Select **OK**.</span></span>
1. <span data-ttu-id="558dd-151">Typ een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="558dd-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="558dd-152">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="558dd-152">Example: P6003</span></span>  
1. <span data-ttu-id="558dd-153">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="558dd-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="558dd-154">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="558dd-154">Example: 50000</span></span>  
1. <span data-ttu-id="558dd-155">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="558dd-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="558dd-156">Een tweede materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="558dd-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="558dd-157">Selecteer in het veld **Plan** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="558dd-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="558dd-158">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="558dd-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="558dd-159">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="558dd-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="558dd-160">Selecteer **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="558dd-160">Select **Run**.</span></span>
4. <span data-ttu-id="558dd-161">Vouw de sectie **Op te nemen records** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="558dd-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="558dd-162">Selecteer **Filter**.</span><span class="sxs-lookup"><span data-stu-id="558dd-162">Select **Filter**.</span></span>
6. <span data-ttu-id="558dd-163">Selecteer in de lijst de rij voor **Veld** = *Artikelnummer*.</span><span class="sxs-lookup"><span data-stu-id="558dd-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="558dd-164">Typ een waarde in het veld *Criteria*.</span><span class="sxs-lookup"><span data-stu-id="558dd-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="558dd-165">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="558dd-165">Example: P6003</span></span>  
8. <span data-ttu-id="558dd-166">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="558dd-166">Select **OK**.</span></span>
9. <span data-ttu-id="558dd-167">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="558dd-167">Select **OK**.</span></span>
10. <span data-ttu-id="558dd-168">Selecteer **Geplande orders**.</span><span class="sxs-lookup"><span data-stu-id="558dd-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="558dd-169">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="558dd-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="558dd-170">Filter bijvoorbeeld op het Veld **Artikelnummer** op de waarde 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="558dd-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="558dd-171">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="558dd-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="558dd-172">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="558dd-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="558dd-173">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="558dd-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="558dd-174">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="558dd-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="558dd-175">Vouw de sectie **Tracering van behoefte** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="558dd-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="558dd-176">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="558dd-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="558dd-177">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="558dd-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="558dd-178">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="558dd-178">Close the page.</span></span>
17. <span data-ttu-id="558dd-179">Selecteer **Hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="558dd-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="558dd-180">Ga naar **Hoofdplanning \> Instellen \> Parameters hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="558dd-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="558dd-181">Selecteer *Nee* in het veld **Alle planningsprocessen uitschakelen**.</span><span class="sxs-lookup"><span data-stu-id="558dd-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="558dd-182">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="558dd-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]