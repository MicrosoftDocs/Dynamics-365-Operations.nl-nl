---
title: 'Gedeeltelijk locatieproces voor cyclustelling definiëren '
description: Wanneer u cyclustellingsplannen gebruikt om telwerk te maken, kunt u de werkelijke telbewerkingen leiden door aan te vragen dat alleen specifieke producten en productvarianten worden geteld in plaats van alle voorhanden voorraad op de locatie.
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568253"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="88ae3-103">Gedeeltelijk locatieproces voor cyclustelling definiëren </span><span class="sxs-lookup"><span data-stu-id="88ae3-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="88ae3-104">Wanneer u cyclustellingsplannen gebruikt om telwerk te maken, kunt u de werkelijke telbewerkingen leiden door aan te vragen dat alleen specifieke producten en productvarianten worden geteld in plaats van alle voorhanden voorraad op de locatie.</span><span class="sxs-lookup"><span data-stu-id="88ae3-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="88ae3-105">Door te filteren op specifieke producten kan de magazijnbeheerder de overhead voor controle helpen verminderen, fouten bij consolidatie vermijden en tijd besparen.</span><span class="sxs-lookup"><span data-stu-id="88ae3-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="88ae3-106">Normaal gesproken voert een magazijnbeheerder de instellingstaken uit.</span><span class="sxs-lookup"><span data-stu-id="88ae3-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="88ae3-107">U kunt deze procedure doorlopen in het demobedrijf USMF of in uw eigen gegevens.</span><span class="sxs-lookup"><span data-stu-id="88ae3-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="88ae3-108">Een cyclustelwerksjabloon maken</span><span class="sxs-lookup"><span data-stu-id="88ae3-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="88ae3-109">Ga naar Magazijnbeheer > Instellingen > Werk > Werksjablonen.</span><span class="sxs-lookup"><span data-stu-id="88ae3-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="88ae3-110">Selecteer 'Cyclustelling' in het veld Werkordertype.</span><span class="sxs-lookup"><span data-stu-id="88ae3-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="88ae3-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="88ae3-111">Click New.</span></span>
4. <span data-ttu-id="88ae3-112">Voer een getal in het veld Volgnummer in.</span><span class="sxs-lookup"><span data-stu-id="88ae3-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="88ae3-113">De sorteervolgorde is van het kleinste getal naar het grootste getal.</span><span class="sxs-lookup"><span data-stu-id="88ae3-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="88ae3-114">De waarde moet groter zijn dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="88ae3-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="88ae3-115">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="88ae3-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="88ae3-116">Typ een waarde in het veld Werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="88ae3-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="88ae3-117">Typ een waarde in het veld Omschrijving van werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="88ae3-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="88ae3-118">Typ of selecteer een waarde in het veld Werkgroep-id.</span><span class="sxs-lookup"><span data-stu-id="88ae3-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="88ae3-119">Voer een getal in het veld Werkprioriteit in.</span><span class="sxs-lookup"><span data-stu-id="88ae3-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="88ae3-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88ae3-120">Click Save.</span></span>
11. <span data-ttu-id="88ae3-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="88ae3-121">Click New.</span></span>
12. <span data-ttu-id="88ae3-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="88ae3-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="88ae3-123">Selecteer 'Tellen' in het veld Werktype.</span><span class="sxs-lookup"><span data-stu-id="88ae3-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="88ae3-124">Typ of selecteer een waarde in het veld Werkklasse-id.</span><span class="sxs-lookup"><span data-stu-id="88ae3-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="88ae3-125">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88ae3-125">Click Save.</span></span>
16. <span data-ttu-id="88ae3-126">Klik op Werkregelopsplitsingen.</span><span class="sxs-lookup"><span data-stu-id="88ae3-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="88ae3-127">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="88ae3-127">Click New.</span></span>
18. <span data-ttu-id="88ae3-128">Voer een getal in het veld Volgnummer in.</span><span class="sxs-lookup"><span data-stu-id="88ae3-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="88ae3-129">De sorteervolgorde is van het kleinste getal naar het grootste getal.</span><span class="sxs-lookup"><span data-stu-id="88ae3-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="88ae3-130">De waarde moet groter zijn dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="88ae3-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="88ae3-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88ae3-131">Click Save.</span></span>
20. <span data-ttu-id="88ae3-132">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88ae3-132">Close the page.</span></span>
21. <span data-ttu-id="88ae3-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88ae3-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="88ae3-134">Een cyclustellingsplan maken</span><span class="sxs-lookup"><span data-stu-id="88ae3-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="88ae3-135">Ga naar Magazijnbeheer > Instellingen > Cyclustelling > Cyclustelplannen.</span><span class="sxs-lookup"><span data-stu-id="88ae3-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="88ae3-136">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="88ae3-136">Click New.</span></span>
3. <span data-ttu-id="88ae3-137">Typ een waarde in het veld Id cyclustelplan.</span><span class="sxs-lookup"><span data-stu-id="88ae3-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="88ae3-138">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="88ae3-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="88ae3-139">Voer een getal in het veld Maximumaantal cyclustellingen in.</span><span class="sxs-lookup"><span data-stu-id="88ae3-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="88ae3-140">Typ of selecteer een waarde in het veld Werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="88ae3-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="88ae3-141">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="88ae3-141">Click New.</span></span>
8. <span data-ttu-id="88ae3-142">Voer een getal in het veld Volgnummer in.</span><span class="sxs-lookup"><span data-stu-id="88ae3-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="88ae3-143">De sorteervolgorde is van het kleinste getal naar het grootste getal.</span><span class="sxs-lookup"><span data-stu-id="88ae3-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="88ae3-144">De waarde moet groter zijn dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="88ae3-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="88ae3-145">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="88ae3-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="88ae3-146">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="88ae3-146">Click Save.</span></span>
11. <span data-ttu-id="88ae3-147">Klik op Productquery definiëren.</span><span class="sxs-lookup"><span data-stu-id="88ae3-147">Click Define product query.</span></span>
12. <span data-ttu-id="88ae3-148">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="88ae3-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="88ae3-149">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="88ae3-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="88ae3-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="88ae3-150">Click OK.</span></span>
15. <span data-ttu-id="88ae3-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="88ae3-151">Close the page.</span></span>

