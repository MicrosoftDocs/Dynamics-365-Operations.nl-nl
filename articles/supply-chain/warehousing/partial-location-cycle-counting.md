---
title: Gedeeltelijke cyclustelling van locatie
description: Cyclustellingsplannen sturen de werkelijke telbewerkingen aan. U kunt verzoeken dat alleen specifieke producten en productvarianten worden geteld, in plaats van alle voorhanden voorraad op een locatie.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0e0f9d81f4d5943a89d8ac87776e05acb32cb8d9
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="partial-location-cycle-counting"></a><span data-ttu-id="c7d3d-104">Gedeeltelijke cyclustelling van locatie</span><span class="sxs-lookup"><span data-stu-id="c7d3d-104">Partial location cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c7d3d-105">Cyclustellingsplannen sturen de werkelijke telbewerkingen aan.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-105">Cycle count plans guide the actual counting operations.</span></span> <span data-ttu-id="c7d3d-106">U kunt verzoeken dat alleen specifieke producten en productvarianten worden geteld, in plaats van alle voorhanden voorraad op een locatie.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-106">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span>

<span data-ttu-id="c7d3d-107">Als u telwerk maakt door middel van cyclustellingsplannen, kunt u de werkelijke telbewerkingen aansturen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-107">By using cycle count plans to create counting work, you can guide the actual counting operations.</span></span> <span data-ttu-id="c7d3d-108">U kunt verzoeken dat alleen specifieke producten en productvarianten worden geteld, in plaats van alle voorhanden voorraad op een locatie.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-108">You can request that only specific products and product variants be counted instead of all on-hand inventory in a location.</span></span> <span data-ttu-id="c7d3d-109">Door te filteren op specifieke producten, kan de magazijnbeheerder de overhead voor controle verminderen, fouten bij consolidatie vermijden en tijd besparen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-109">By filtering on specific products, the warehouse manager can reduce review overhead, avoid consolidation mistakes, and save time.</span></span>

## <a name="how-to-configure-partial-location-cycle-counting"></a><span data-ttu-id="c7d3d-110">Gedeeltelijke cyclustelling van locatie instellen</span><span class="sxs-lookup"><span data-stu-id="c7d3d-110">How to configure partial location cycle counting</span></span>
<span data-ttu-id="c7d3d-111">Wanneer u het magazijnwerkproces gebruikt voor telbewerkingen, wordt een werkkoptekst gemaakt voor elke locatie.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-111">When you use the warehouse work process for counting operations, a work header is created for each location.</span></span> <span data-ttu-id="c7d3d-112">Wanneer u het cyclustellingsplan definieert, kunt u met de query **Locaties selecteren** het cyclustellingswerk beperken dat wordt aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-112">When you define the cycle count plan, you can use the **Select locations** query to limit the cycle counting work that is created.</span></span> <span data-ttu-id="c7d3d-113">Wanneer u producten voor het cyclustellingsplan selecteert, selecteert u query's voor zowel producten als productvarianten om te verfijnen wat moet worden geteld.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-113">When you select products for the cycle count plan, you can select both product and product variant queries to refine what is counted.</span></span> 

<span data-ttu-id="c7d3d-114">U kunt een **werksjabloon** aan een cyclustellingsplan koppelen, om te definiëren hoe het cyclustellingswerk moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-114">You can associate a **work template** with a cycle count plan to define how the cycle count work should be created.</span></span> <span data-ttu-id="c7d3d-115">De werksjabloon voor telbewerkingen wordt rechtstreeks aangeroepen vanuit het cyclustellingsplan.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-115">The work template for counting operations is directly referenced from the cycle count plan.</span></span> 

<span data-ttu-id="c7d3d-116">Wanneer u de gegevens van de werksjabloon definieert, kunt u met de optie **Werkregelopsplitsingen** opgeven of de telwerkregels moeten worden gegroepeerd op artikelnummer of op productvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-116">When you define the work template details, you can use the **Work line breaks** option to specify whether the counting work lines must be grouped by item number or product variant number.</span></span> <span data-ttu-id="c7d3d-117">Deze instelling is vereist als u alleen voorhanden voorraad wilt tellen voor bepaalde producten op een locatie.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-117">This setup is required if you want to count on-hand inventory only for specific products in a location.</span></span> <span data-ttu-id="c7d3d-118">De cyclustellingswerkregels die zijn gemaakt, hebben het niveau van de informatie die u hier definieert en de begeleide telbewerking worden afgewerkt op basis van dit niveau.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-118">The cycle counting work lines that are created will have the level of information that you define here, and the guided counting operation will be handled based on this level.</span></span> 

<span data-ttu-id="c7d3d-119">Als u cyclustellingsplannen koppelt aan werksjablonen met behulp van de optie **Werkregels afbreken**, wordt het veld **Gedeeltelijke cyclustelling** ingeschakeld voor het cyclustellingswerk dat is gemaakt en meerdere cyclustellingswerkregels worden gemaakt op basis van de definitie van de werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-119">If you associate cycle count plans with work templates by using the **Work lines breaks** option, the **Partial cycle count** field is selected for the cycle counting work that is created, and multiple cycle counting work lines will be created based on the definition of the work template.</span></span> 

<span data-ttu-id="c7d3d-120">Voordat gedeeltelijk cyclustellingswerk kan worden verwerkt, moet u ten minste **Artikelnummer weergeven** selecteren voor het mobiele menuonderdeel als onderdeel van de instellingen voor cyclustelling.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-120">Before partial cycle count work can be processed, you must, at a minimum, select **Display item number** for the mobile device menu item as part of the cycle counting setup.</span></span> <span data-ttu-id="c7d3d-121">De magazijnoperator wordt gevraagd om alleen telinformatie vast te leggen die is gekoppeld aan de tellingsregels (artikelnummers en productdimensies).</span><span class="sxs-lookup"><span data-stu-id="c7d3d-121">The warehouse operator will be asked to record only counting information that is related to the counting lines (item numbers and product dimensions).</span></span> <span data-ttu-id="c7d3d-122">Alle overige voorhanden voorraad wordt voor dit telproces genegeerd.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-122">All other on-hand inventory will be ignored for this counting process.</span></span> 

<span data-ttu-id="c7d3d-123">Voor het gedeeltelijke cyclustellingsproces wordt de datum/tijd **Laatste cyclustelling** voor de locatie niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-123">For the partial cycle count process, the **Last cycle count** date/time won’t be updated for the location.</span></span>

## <a name="example"></a><span data-ttu-id="c7d3d-124">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c7d3d-124">Example</span></span>
<span data-ttu-id="c7d3d-125">In dit voorbeeld moet alleen artikelnummer A0001 in magazijn 61 worden geteld.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-125">For this example, only item number A0001 must be counted in warehouse 61.</span></span>

1.  <span data-ttu-id="c7d3d-126">Een nieuwe werksjabloon voor cyclustelling wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-126">A new work template for cycle counting is created.</span></span> <span data-ttu-id="c7d3d-127">Met de optie **Opsplitsing werkregels** worden telwerkregels gegroepeerd op artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-127">The **Work line breaks** option is used to group counting work lines by item number.</span></span> <span data-ttu-id="c7d3d-128">Daarom heeft het aangemaakte cyclustellingswerk regels op artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-128">Therefore, the cycle counting work that is created will have lines per item number.</span></span> <span data-ttu-id="c7d3d-129">U kunt de regels ook groeperen op productvariantnummer.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-129">You can also group the lines by product variant number.</span></span>
2.  <span data-ttu-id="c7d3d-130">Een nieuw cyclustellingsplan wordt gemaakt, dat verwijst naar de zojuist gemaakte werksjabloon.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-130">A new cycle counting plan is created that references the newly created work template.</span></span> <span data-ttu-id="c7d3d-131">Het cyclustellingsplan bevat alle locaties in magazijn 61 (query **Locaties selecteren**) die voorraad bevatten voor artikelnummer A0001.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-131">The cycle counting plan includes all locations in warehouse 61 (**Select locations** query) that hold inventory for item number A0001.</span></span> <span data-ttu-id="c7d3d-132">De selectie van specifieke producten wordt gedefinieerd in de sectie **Productselecties voor cyclustellingsplan**.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-132">The selection of specific products is defined in the **Cycle count product selections** section.</span></span>
3.  <span data-ttu-id="c7d3d-133">U kunt producten voor cyclustellingsplannen selecteren door het veld **Lege locaties** in te stellen op **Lege uitsluiten**.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-133">You can select products for cycle counting plans by setting the **Empty locations** field to **Exclude empty**.</span></span> <span data-ttu-id="c7d3d-134">Wanneer het cyclustellingsplan wordt verwerkt, wordt gedeeltelijk cyclustellingswerk aangemaakt voor artikelnummer A0001.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-134">When the cycle counting plan is processed, partial cycle count work for item number A0001 is created.</span></span> <span data-ttu-id="c7d3d-135">Het werkelijke telproces kan worden uitgevoerd via een mobiel menu-item voor geleide cyclustelling.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-135">The actual counting process can be performed by using a mobile device menu item for guided cycle counting.</span></span>



<a name="see-also"></a><span data-ttu-id="c7d3d-136">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c7d3d-136">See also</span></span>
--------

[<span data-ttu-id="c7d3d-137">Cyclustelling</span><span class="sxs-lookup"><span data-stu-id="c7d3d-137">Cycle counting</span></span>](cycle-counting.md)


