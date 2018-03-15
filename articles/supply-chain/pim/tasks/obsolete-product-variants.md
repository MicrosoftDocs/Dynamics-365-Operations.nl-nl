--- 
title: Verouderde productvarianten zoeken
description: In deze procedure wordt aangegeven hoe u verouderde vrijgegeven producten of productvarianten kunt vinden en de status van een productlevenscyclus kunt koppelen aan de verouderde producten.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 3a59f988de5290d1d69d013b762f87d0cce10e39
ms.contentlocale: nl-nl
ms.lasthandoff: 02/08/2018

---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="8f8c4-103">Verouderde productvarianten zoeken</span><span class="sxs-lookup"><span data-stu-id="8f8c4-103">Find obsolete product variants</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f8c4-104">In deze procedure wordt aangegeven hoe u verouderde vrijgegeven producten of productvarianten kunt vinden en de status van een productlevenscyclus kunt koppelen aan de verouderde producten.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="8f8c4-105">Vereiste: u moet minimaal één status van productlevenscyclus definiëren die inactief is voor de planning voordat u deze taakbegeleiding kunt afspelen.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="8f8c4-106">Een simulatie uitvoeren</span><span class="sxs-lookup"><span data-stu-id="8f8c4-106">Run a simulation</span></span>
1. <span data-ttu-id="8f8c4-107">Ga naar Productgegevensbeheer > Periodieke taken > Status van levenscyclus voor verouderde producten wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="8f8c4-108">Typ of selecteer een waarde in het veld Nieuwe status van levenscyclus van producten.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="8f8c4-109">Selecteer Ja in het veld Simulatie uitvoeren zonder productgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="8f8c4-110">Typ een aantal in het veld Producten uitsluiten die binnen dit aantal dagen zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="8f8c4-111">Typ een aantal in het veld Producten uitsluiten die worden gebruikt in transacties (in aantal dagen).</span><span class="sxs-lookup"><span data-stu-id="8f8c4-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="8f8c4-112">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="8f8c4-113">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-113">Click Filter.</span></span>
8. <span data-ttu-id="8f8c4-114">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="8f8c4-115">Typ een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="8f8c4-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-116">Click OK.</span></span>
11. <span data-ttu-id="8f8c4-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="8f8c4-118">Het wordt aanbevolen om de simulatie in batch uit te voeren als u verwacht dat een groot aantal producten moet worden gezocht.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="8f8c4-119">Zorg ook dat de simulatie niet wordt uitgevoerd tijdens de drukste werktijden van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="8f8c4-120">De simulatieresultaten beoordelen</span><span class="sxs-lookup"><span data-stu-id="8f8c4-120">Review the simulation results</span></span>
1. <span data-ttu-id="8f8c4-121">Ga naar Productgegevensbeheer > Query's en rapporten > Onderhoudsgeschiedenis van status van productlevenscyclus.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="8f8c4-122">Op deze pagina kunt u de simulatieresultaten bekijken en beoordelen hoeveel producten en productvarianten worden gekoppeld aan een nieuwe status voor de productlevenscyclus wanneer u de update zonder simulatie uitvoert.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="8f8c4-123">De update van de levenscyclusstatus van producten uitvoeren voor verouderde producten</span><span class="sxs-lookup"><span data-stu-id="8f8c4-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="8f8c4-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-124">Close the page.</span></span>
2. <span data-ttu-id="8f8c4-125">Ga naar Productgegevensbeheer > Periodieke taken > Status van levenscyclus voor verouderde producten wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="8f8c4-126">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="8f8c4-127">Houd er rekening mee dat de laatste selectie is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="8f8c4-128">Selecteer Nee in het veld Simulatie uitvoeren zonder productgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="8f8c4-129">Vouw de sectie Op de achtergrond uitvoeren uit.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="8f8c4-130">Afhankelijk van de hoeveelheid producten en productvarianten kunt u overwegen om deze taak in batch uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="8f8c4-131">Zorg ervoor dat u geen grote updatetaak uitvoert tijdens de meest drukste werkuren in het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="8f8c4-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-132">Click OK.</span></span>
7. <span data-ttu-id="8f8c4-133">Ga naar Productgegevensbeheer > Query's en rapporten > Onderhoudsgeschiedenis van status van productlevenscyclus.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="8f8c4-134">Controleer de gewijzigde vrijgegeven producten en productvarianten.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="8f8c4-135">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="8f8c4-135">In the list, find and select the desired record.</span></span>


