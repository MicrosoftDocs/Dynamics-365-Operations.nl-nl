---
title: Overzicht van Planningsoptimalisatie
description: Dit onderwerp bevat een overzicht van de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 110045d4c7e4f32c29b73096dd4df3a09b5434ac
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323388"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="90092-103">Overzicht van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="90092-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90092-104">Met de invoegtoepassing Planningsoptimalisatie voor Microsoft Dynamics 365 Supply Chain Management kan de berekening van de hoofdplanning buiten Dynamics 365 Supply Chain Management en de gerelateerde SQL-database plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="90092-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="90092-105">De voordelen die zijn gekoppeld aan de functionaliteit Planningsoptimalisatie omvatten betere prestaties en minimale gevolgen voor de SQL-database tijdens uitvoeringen van de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="90092-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="90092-106">Snelle planningsuitvoeringen kunnen zelfs tijdens kantooruren worden uitgevoerd, zodat planners direct kunnen reageren op vraag- of parameterwijzigingen.</span><span class="sxs-lookup"><span data-stu-id="90092-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="90092-107">Als u Planningsoptimalisatie wilt gebruiken, moet u de invoegtoepassing vanuit uw project in Microsoft Dynamics Lifecycle Services (LCS) installeren en de functionaliteit Planningsoptimalisatie inschakelen in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="90092-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="90092-108">Zie [Aan de slag met Planningsoptimalisatie](get-started.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="90092-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="90092-109">In de volgende afbeelding wordt het voordeel van het uitvoeren van Planningsoptimalisatie tijdens kantooruren weergegeven.</span><span class="sxs-lookup"><span data-stu-id="90092-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Voordeel van het uitvoeren van Planningsoptimalisatie tijdens kantoor uren](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="90092-111">Betere prestaties</span><span class="sxs-lookup"><span data-stu-id="90092-111">Improved performance</span></span>

<span data-ttu-id="90092-112">Planningsoptimalisatie kan worden gebruikt in scenario's met langlopende hoofdplannen.</span><span class="sxs-lookup"><span data-stu-id="90092-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="90092-113">De functie is speciaal ontworpen voor zeer snelle berekeningen met zeer grote hoeveelheden gegevens.</span><span class="sxs-lookup"><span data-stu-id="90092-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="90092-114">Omdat deze functie is gebouwd als een hyperschaalbare service voor meerdere tenants, kunnen meerdere exemplaren tegelijk samenwerken om het plan te berekenen.</span><span class="sxs-lookup"><span data-stu-id="90092-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="90092-115">Bovendien verwijdert de planningsservice de belasting van de hoofdplanning van uw systeem en werkt deze met een gegevensstroom waarmee de serverbelasting van de server wordt geminimaliseerd.</span><span class="sxs-lookup"><span data-stu-id="90092-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="90092-116">Met Planningsoptimalisatie kunt u de volgende doelstellingen bereiken:</span><span class="sxs-lookup"><span data-stu-id="90092-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="90092-117">Verbeter de planningsprestaties met een kortere uitvoeringstijd.</span><span class="sxs-lookup"><span data-stu-id="90092-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="90092-118">Verminder het effect op andere processen tijdens de uitvoering van de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="90092-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="90092-119">Voer vaker planningsuitvoeringen uit.</span><span class="sxs-lookup"><span data-stu-id="90092-119">Do more frequent planning runs.</span></span> <span data-ttu-id="90092-120">(U bent niet beperkt tot dagelijkse uitvoeringen.)</span><span class="sxs-lookup"><span data-stu-id="90092-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="90092-121">Zorg ervoor dat de toekomstige bedrijfsgroei het planningssysteem niet overbelast.</span><span class="sxs-lookup"><span data-stu-id="90092-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="90092-122">Architectuur en gegevensstroom</span><span class="sxs-lookup"><span data-stu-id="90092-122">Architecture and data flow</span></span>

<span data-ttu-id="90092-123">Wanneer de invoegtoepassing Planningsoptimalisatie vanuit LCS is geïnstalleerd, wordt een beveiligde verbinding met de service Planningsoptimalisatie tot stand gebracht.</span><span class="sxs-lookup"><span data-stu-id="90092-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="90092-124">De service bevindt zich in hetzelfde datacenterland (of regio) als het gerelateerde Supply Chain Management-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="90092-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="90092-125">Als Planningsoptimalisatie is ingesteld en de hoofdplanning wordt uitgevoerd, worden hoofdgegevens en transactiegegevens vanuit Supply Chain Management naar de service Planningsoptimalisatie verzonden.</span><span class="sxs-lookup"><span data-stu-id="90092-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="90092-126">Als de invoegtoepassing Planningsoptimalisatie wordt verwijderd, worden alle gerelateerde gegevens in de service Planningsoptimalisatie verwijderd.</span><span class="sxs-lookup"><span data-stu-id="90092-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="90092-127">Algemene gegevensstroom voor regeneratie-uitvoeringen</span><span class="sxs-lookup"><span data-stu-id="90092-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="90092-128">De Supply Chain Management-client verzendt een signaal om een planningsuitvoering vanuit Planningsoptimalisatie aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="90092-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="90092-129">Planningsoptimalisatie vraagt de vereiste gegevens aan via de geïntegreerde connector.</span><span class="sxs-lookup"><span data-stu-id="90092-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="90092-130">De SQL-database verzendt de gevraagde informatie over de instellings-, hoofd- en transactiegegevens naar Planningsoptimalisatie via de connector.</span><span class="sxs-lookup"><span data-stu-id="90092-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="90092-131">De connector zet gegevens tussen Supply Chain Management en de service Planningsoptimalisatie om.</span><span class="sxs-lookup"><span data-stu-id="90092-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="90092-132">De service Planningsoptimalisatie behoudt planningsgerelateerde gegevens in het geheugen en voert de vereiste berekeningen uit.</span><span class="sxs-lookup"><span data-stu-id="90092-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="90092-133">Het resultaat van de planning wordt via de connector naar de Supply Chain Management-data base verzonden.</span><span class="sxs-lookup"><span data-stu-id="90092-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="90092-134">De resultaten omvatten informatie, zoals geplande orders en behoeftetraceringsinformatie.</span><span class="sxs-lookup"><span data-stu-id="90092-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="90092-135">Met Planningsoptimalisatie wordt een signaal verzonden naar Supply Chain Management om aan te geven dat de planningsuitvoering is voltooid.</span><span class="sxs-lookup"><span data-stu-id="90092-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="90092-136">Ook worden relevante berichten en waarschuwingen verzonden.</span><span class="sxs-lookup"><span data-stu-id="90092-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="90092-137">In de volgende afbeelding wordt de gegevensstroom weergegeven.</span><span class="sxs-lookup"><span data-stu-id="90092-137">The following illustration shows the data flow.</span></span>

![Gegevensstroom voor regeneratie-uitvoeringen](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="90092-139">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="90092-139">Related resources</span></span>

[<span data-ttu-id="90092-140">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="90092-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="90092-141">Analyse voor passende Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="90092-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="90092-142">Planhistorie en planningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="90092-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="90092-143">Filters op een plan toepassen</span><span class="sxs-lookup"><span data-stu-id="90092-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="90092-144">Een planningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="90092-144">Cancel a planning job</span></span>](cancel-planning-job.md)
