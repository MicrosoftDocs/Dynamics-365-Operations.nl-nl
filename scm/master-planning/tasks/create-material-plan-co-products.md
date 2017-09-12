--- 
title: Een materiaalplan voor co-producten maken
description: De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1ab8a-103">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="1ab8a-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ab8a-104">De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="1ab8a-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="1ab8a-106">Vereiste voor een co-product maken</span><span class="sxs-lookup"><span data-stu-id="1ab8a-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="1ab8a-107">Ga naar Standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="1ab8a-108">Klik op Verkooporderverwerking en -onderzoek.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="1ab8a-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-109">Click New.</span></span>
4. <span data-ttu-id="1ab8a-110">Klik op Verkooporder.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-110">Click Sales order.</span></span>
5. <span data-ttu-id="1ab8a-111">Typ een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="1ab8a-112">Voorbeeld: US-001</span><span class="sxs-lookup"><span data-stu-id="1ab8a-112">Example: US-001</span></span>  
6. <span data-ttu-id="1ab8a-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-113">Click OK.</span></span>
7. <span data-ttu-id="1ab8a-114">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1ab8a-115">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="1ab8a-115">Example: P6003</span></span>  
8. <span data-ttu-id="1ab8a-116">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1ab8a-117">Voorbeeld: 50000</span><span class="sxs-lookup"><span data-stu-id="1ab8a-117">Example: 50000</span></span>  
9. <span data-ttu-id="1ab8a-118">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1ab8a-119">Een materiaalplan voor co-producten maken</span><span class="sxs-lookup"><span data-stu-id="1ab8a-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="1ab8a-120">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-120">Click Master planning.</span></span>
2. <span data-ttu-id="1ab8a-121">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="1ab8a-122">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1ab8a-123">Voorbeeld: Hoofdplan</span><span class="sxs-lookup"><span data-stu-id="1ab8a-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="1ab8a-124">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-124">Click Run.</span></span>
5. <span data-ttu-id="1ab8a-125">Vouw de sectie Op te nemen records uit of samen.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="1ab8a-126">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-126">Click Filter.</span></span>
7. <span data-ttu-id="1ab8a-127">Selecteer in de lijst de rij voor het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="1ab8a-128">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="1ab8a-129">Voorbeeld: P6003</span><span class="sxs-lookup"><span data-stu-id="1ab8a-129">Example: P6003</span></span>  
9. <span data-ttu-id="1ab8a-130">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-130">Click OK.</span></span>
10. <span data-ttu-id="1ab8a-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-131">Click OK.</span></span>
11. <span data-ttu-id="1ab8a-132">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-132">Click Planned orders.</span></span>
12. <span data-ttu-id="1ab8a-133">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1ab8a-134">Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".</span><span class="sxs-lookup"><span data-stu-id="1ab8a-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="1ab8a-135">Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="1ab8a-136">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1ab8a-137">Selecteer een van de rijen die door het filter worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="1ab8a-138">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="1ab8a-139">Vouw de sectie Tracering van behoefte uit of samen.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="1ab8a-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1ab8a-141">De geplande order is getraceerd naar de verkooporder van het co-product.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="1ab8a-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1ab8a-142">Close the page.</span></span>


