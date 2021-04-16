---
title: Raming van productieorderkosten
description: Dit artikel biedt informatie over ramingen van productiekosten. Door de productiekosten te ramen, weet u wat de verwachte materiaal- en capaciteitverbruikskosten zijn van het fabriceren van een artikel in de geplande productieorderhoeveelheid.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59b93b41b74bd3f4cc480c8e60e8c69b25e40e51
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830239"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="ac0ed-104">Raming van productieorderkosten</span><span class="sxs-lookup"><span data-stu-id="ac0ed-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac0ed-105">Dit artikel biedt informatie over ramingen van productiekosten.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="ac0ed-106">Door de productiekosten te ramen, weet u wat de verwachte materiaal- en capaciteitverbruikskosten zijn van het fabriceren van een artikel in de geplande productieorderhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="ac0ed-107">Nadat u een productieorder hebt gemaakt, moet u productiekosten ramen.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="ac0ed-108">Het belangrijkste doel hiervan is het ramen van het artikel- en routeverbruik voor het productieproces, omdat deze ramingen de basis vormen voor volgende plannings- en productieprocessen.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="ac0ed-109">Raming van productiekosten</span><span class="sxs-lookup"><span data-stu-id="ac0ed-109">Production cost estimation</span></span>
<span data-ttu-id="ac0ed-110">Ramingen van productiekosten zijn gebaseerd op de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="ac0ed-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="ac0ed-111">De hoeveelheid van de productieorder</span><span class="sxs-lookup"><span data-stu-id="ac0ed-111">The quantity on the production order</span></span>
-   <span data-ttu-id="ac0ed-112">De onderdelen in de productiestuklijsten</span><span class="sxs-lookup"><span data-stu-id="ac0ed-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="ac0ed-113">De routebewerkingen in de productieroute</span><span class="sxs-lookup"><span data-stu-id="ac0ed-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="ac0ed-114">de indirecte kosten die van toepassing zijn op deze onderdelen en bewerkingen</span><span class="sxs-lookup"><span data-stu-id="ac0ed-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="ac0ed-115">De actieve kostengegevens op de datum van berekening</span><span class="sxs-lookup"><span data-stu-id="ac0ed-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="ac0ed-116">Als er een phantom-regelartikel in de productiestuklijsten staat, weerspiegelen de berekeningen de onderdelen en routebewerkingen van het phantom-artikel.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="ac0ed-117">U kunt de ramingstaak gebruiken om geschatte kosten opnieuw te berekenen zodat bijgewerkte informatie wordt gereflecteerd.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="ac0ed-118">De bijgewerkte informatie kan bijvoorbeeld bestaan uit wijzigingen in de productieorderhoeveelheid, de onderdelen in de productiestuklijsten, de routebewerkingen in de productieroute, de indirecte kosten die van toepassing zijn op deze onderdelen en bewerkingen, of de actieve kostengegevens op de datum van herberekening.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="ac0ed-119">De berekeningen van de geschatte kosten stellen ook een verkoopprijs voor het productieartikel voor op basis van een kostprijs-plus-verhoging-benadering.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="ac0ed-120">De berekeningen van de kostenraming kunnen eventueel worden toegepast op referentieorders die andere productieorders reflecteren die aan de productieorder zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="ac0ed-121">De kostenramingen weergeven</span><span class="sxs-lookup"><span data-stu-id="ac0ed-121">View the estimated costs</span></span>
<span data-ttu-id="ac0ed-122">Nadat u de raming hebt uitgevoerd, kunt u de resultaten op de pagina **Prijsberekening** weergeven.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="ac0ed-123">Bij de raming worden de volgende waarden berekend:</span><span class="sxs-lookup"><span data-stu-id="ac0ed-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="ac0ed-124">**Productiekosten**: de bovenste regel van de raming.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="ac0ed-125">Hier worden de volledige kosten van het uitvoeren van de productieorder en de totale verkoopprijs voor de productie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="ac0ed-126">Dit is de som van alle kostenregels van de raming.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="ac0ed-127">**Route- of resourcekosten**: de kosten voor de productiebewerkingen.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="ac0ed-128">Dit zijn onder andere de kosten van elementen als de insteltijd, de uitvoeringstijd en overhead.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="ac0ed-129">**Materiaalkosten**: de kosten en prijzen van de stuklijstonderdelen die nodig zijn om het artikel te fabriceren.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="ac0ed-130">Deze kosten zijn al eerder gemaakt en ingevoerd in het systeem.</span><span class="sxs-lookup"><span data-stu-id="ac0ed-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="ac0ed-131">Andere functies van kostenramingen</span><span class="sxs-lookup"><span data-stu-id="ac0ed-131">Other uses of cost estimation</span></span>
<span data-ttu-id="ac0ed-132">Een kostenraming biedt ook de volgende informatie:</span><span class="sxs-lookup"><span data-stu-id="ac0ed-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="ac0ed-133">Onderbouwde prijsoffertes</span><span class="sxs-lookup"><span data-stu-id="ac0ed-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="ac0ed-134">Ramingen van de rentabiliteit van de order</span><span class="sxs-lookup"><span data-stu-id="ac0ed-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="ac0ed-135">Ramingen van het grondstofverbruik</span><span class="sxs-lookup"><span data-stu-id="ac0ed-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="ac0ed-136">Vergelijkingen van kostengegevens van eerdere producties</span><span class="sxs-lookup"><span data-stu-id="ac0ed-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="ac0ed-137">Budget- en prognosegegevens</span><span class="sxs-lookup"><span data-stu-id="ac0ed-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="ac0ed-138">Ramingen van de productiegrootte die nodig zijn om bepaalde kosten te beheren</span><span class="sxs-lookup"><span data-stu-id="ac0ed-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]