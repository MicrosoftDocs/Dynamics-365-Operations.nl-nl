--- 
title: "Gedeeltelijk locatieproces voor cyclustelling definiëren "
description: Wanneer u cyclustellingsplannen gebruikt om telwerk te maken, kunt u de werkelijke telbewerkingen leiden door aan te vragen dat alleen specifieke producten en productvarianten worden geteld in plaats van alle voorhanden voorraad op de locatie.
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e92b5cd4d903a68d30f7c25fd7e3df8989bb82d1
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="1c7ae-103">Gedeeltelijk locatieproces voor cyclustelling definiëren </span><span class="sxs-lookup"><span data-stu-id="1c7ae-103">Define partial location cycle counting process</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c7ae-104">Wanneer u cyclustellingsplannen gebruikt om telwerk te maken, kunt u de werkelijke telbewerkingen leiden door aan te vragen dat alleen specifieke producten en productvarianten worden geteld in plaats van alle voorhanden voorraad op de locatie.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="1c7ae-105">Door te filteren op specifieke producten kan de magazijnbeheerder de overhead voor controle helpen verminderen, fouten bij consolidatie vermijden en tijd besparen.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="1c7ae-106">Normaal gesproken voert een magazijnbeheerder de instellingstaken uit.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="1c7ae-107">U kunt deze procedure doorlopen in het demobedrijf USMF of in uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="1c7ae-108">Een cyclustelwerksjabloon maken</span><span class="sxs-lookup"><span data-stu-id="1c7ae-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="1c7ae-109">Ga naar Magazijnbeheer > Instellingen > Werk > Werksjablonen.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="1c7ae-110">Selecteer 'Cyclustelling' in het veld Werkordertype.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="1c7ae-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-111">Click New.</span></span>
4. <span data-ttu-id="1c7ae-112">Voer een getal in het veld Volgnummer in.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="1c7ae-113">De sorteervolgorde is van het kleinste getal naar het grootste getal.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="1c7ae-114">De waarde moet groter zijn dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="1c7ae-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="1c7ae-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="1c7ae-116">Typ een waarde in het veld Werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="1c7ae-117">Typ een waarde in het veld Omschrijving van werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="1c7ae-118">Typ of selecteer een waarde in het veld Werkgroep-id.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="1c7ae-119">Voer een getal in het veld Werkprioriteit in.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="1c7ae-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-120">Click Save.</span></span>
11. <span data-ttu-id="1c7ae-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-121">Click New.</span></span>
12. <span data-ttu-id="1c7ae-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1c7ae-123">Selecteer 'Tellen' in het veld Werktype.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="1c7ae-124">Typ of selecteer een waarde in het veld Werkklasse-id.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="1c7ae-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-125">Click Save.</span></span>
16. <span data-ttu-id="1c7ae-126">Klik op Werkregelopsplitsingen.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="1c7ae-127">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-127">Click New.</span></span>
18. <span data-ttu-id="1c7ae-128">Voer een getal in het veld Volgnummer in.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="1c7ae-129">De sorteervolgorde is van het kleinste getal naar het grootste getal.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="1c7ae-130">De waarde moet groter zijn dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="1c7ae-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="1c7ae-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-131">Click Save.</span></span>
20. <span data-ttu-id="1c7ae-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-132">Close the page.</span></span>
21. <span data-ttu-id="1c7ae-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="1c7ae-134">Een cyclustellingsplan maken</span><span class="sxs-lookup"><span data-stu-id="1c7ae-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="1c7ae-135">Ga naar Magazijnbeheer > Instellingen > Cyclustelling > Cyclustelplannen.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="1c7ae-136">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-136">Click New.</span></span>
3. <span data-ttu-id="1c7ae-137">Typ een waarde in het veld Id cyclustelplan.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="1c7ae-138">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1c7ae-139">Voer een getal in het veld Maximumaantal cyclustellingen in.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="1c7ae-140">Typ of selecteer een waarde in het veld Werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="1c7ae-141">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-141">Click New.</span></span>
8. <span data-ttu-id="1c7ae-142">Voer een getal in het veld Volgnummer in.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="1c7ae-143">De sorteervolgorde is van het kleinste getal naar het grootste getal.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="1c7ae-144">De waarde moet groter zijn dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="1c7ae-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="1c7ae-145">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="1c7ae-146">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-146">Click Save.</span></span>
11. <span data-ttu-id="1c7ae-147">Klik op Productquery definiëren.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-147">Click Define product query.</span></span>
12. <span data-ttu-id="1c7ae-148">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1c7ae-149">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="1c7ae-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-150">Click OK.</span></span>
15. <span data-ttu-id="1c7ae-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="1c7ae-151">Close the page.</span></span>


