---
title: Veelvoorkomende oorzaken van productieafwijkingen
description: In dit artikel worden verschillende bronnen van elk type productieafwijking beschreven.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f8eea27edaa97150ceb2c36996177395cba8bdb9
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="common-sources-of-production-variances"></a><span data-ttu-id="51be1-103">Veelvoorkomende oorzaken van productieafwijkingen</span><span class="sxs-lookup"><span data-stu-id="51be1-103">Common sources of production variances</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="51be1-104">In dit artikel worden verschillende bronnen van elk type productieafwijking beschreven.</span><span class="sxs-lookup"><span data-stu-id="51be1-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="51be1-105">Hier volgen enkele veelvoorkomende bronnen van een afwijking in **partijgrootte**:</span><span class="sxs-lookup"><span data-stu-id="51be1-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="51be1-106">De goede hoeveelheid voor een productieorder wijkt af van de berekeningshoeveelheid die wordt gebruikt in de standaardkostenberekening.</span><span class="sxs-lookup"><span data-stu-id="51be1-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="51be1-107">De hoeveelheid vormt de basis voor het afschrijven van constante kosten.</span><span class="sxs-lookup"><span data-stu-id="51be1-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="51be1-108">De waarde van constante kosten op de productieorder wijkt af van de constante kosten die worden gebruikt in de standaardkostenberekening.</span><span class="sxs-lookup"><span data-stu-id="51be1-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="51be1-109">Het verschil in constante kosten op de productieorder kan verschillende redenen hebben.</span><span class="sxs-lookup"><span data-stu-id="51be1-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="51be1-110">Zo reflecteren de constante kosten bijvoorbeeld mogelijk de volgende factoren:</span><span class="sxs-lookup"><span data-stu-id="51be1-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="51be1-111">Handmatige wijzigingen in de productiestuklijst of de route</span><span class="sxs-lookup"><span data-stu-id="51be1-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="51be1-112">De selectie van een andere stuklijstversie of routeversie tijdens het maken van de productieorder</span><span class="sxs-lookup"><span data-stu-id="51be1-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="51be1-113">Geplande engineeringwijzigingen in de stuklijstversie of routeversie die aan het artikel is toegewezen</span><span class="sxs-lookup"><span data-stu-id="51be1-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="51be1-114">Hier volgen enkele veelvoorkomende bronnen van een afwijking in **productieprijs**:</span><span class="sxs-lookup"><span data-stu-id="51be1-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="51be1-115">De kostencategorie (en kostencategorieprijs) voor het gemelde verbruik van een routebewerking wijkt af van de kostencategorie die wordt gebruikt in de standaardkostenberekening.</span><span class="sxs-lookup"><span data-stu-id="51be1-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="51be1-116">De actieve kosten voor de kostencategorieprijs wijkt af van de kostencategorieprijs die wordt gebruikt in de standaardkostenberekening.</span><span class="sxs-lookup"><span data-stu-id="51be1-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="51be1-117">Hier volgen enkele veelvoorkomende bronnen van een afwijking in **productiehoeveelheid**:</span><span class="sxs-lookup"><span data-stu-id="51be1-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="51be1-118">U geeft te veel of te weinig materiaalcomponenten uit.</span><span class="sxs-lookup"><span data-stu-id="51be1-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="51be1-119">U meldt te veel of te weinig tijd voor een routebewerking.</span><span class="sxs-lookup"><span data-stu-id="51be1-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="51be1-120">U ontvangt te veel of te weinig goederen van het bovenliggende artikel, ten opzichte van de orderhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="51be1-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="51be1-121">U geeft componenten echter volledig uit en meldt bewerkingen volledig, op basis van de orderhoeveelheid voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="51be1-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="51be1-122">Hier volgen enkele veelvoorkomende bronnen van een afwijking in **productievervanging**:</span><span class="sxs-lookup"><span data-stu-id="51be1-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="51be1-123">U geeft een materiaalcomponent uit die niet voorkomt op de productiestuklijst.</span><span class="sxs-lookup"><span data-stu-id="51be1-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="51be1-124">U voegt handmatig een component toe aan de productiestuklijst en rapporteert die component als verbruikt.</span><span class="sxs-lookup"><span data-stu-id="51be1-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="51be1-125">U meldt een artikel als verbruikt maar voegt het niet handmatig toe aan de productiestuklijst.</span><span class="sxs-lookup"><span data-stu-id="51be1-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="51be1-126">U voegt handmatig een bewerking toe aan de productieroute en meldt die bewerking als verbruikt.</span><span class="sxs-lookup"><span data-stu-id="51be1-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="51be1-127">Bij het maken van de productieorder selecteert u een andere stuklijstversie dan de versie die wordt gebruikt in de standaardkostenberekening.</span><span class="sxs-lookup"><span data-stu-id="51be1-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="51be1-128">Bij het maken van de productieorder selecteert u een routeversie die afwijkt van de routeversie die wordt gebruikt in de standaardkostenberekening.</span><span class="sxs-lookup"><span data-stu-id="51be1-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>





