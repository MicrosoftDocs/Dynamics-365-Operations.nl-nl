---
title: Analyse voor passende Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u uw huidige instellingen en gegevens kunt controleren op basis van de mogelijkheden van de functionaliteit Optimalisatieplanning.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
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
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208749"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="5d257-103">Analyse voor passende Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="5d257-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d257-104">Als u wilt zien hoe compatibel uw huidige instellingen en gegevens zijn met de functie Planningsoptimalisatie, gaat u naar **Hoofdplanning** \> **Instellingen** \> **Analyse voor passende Planningsoptimalisatie** en selecteert u **Analyse uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="5d257-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="5d257-105">Als in de analyse inconsistenties worden gevonden, worden deze op dezelfde pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5d257-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="5d257-106">(Het kan enkele minuten duren voordat de analyse is uitgevoerd.)</span><span class="sxs-lookup"><span data-stu-id="5d257-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="5d257-107">Als er inconsistenties worden gevonden, kunt u Planningsoptimalisatie nog steeds gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5d257-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="5d257-108">De resultaten van de aanpassingsanalyse geven alleen de plaatsen aan waar de planningsservice de huidige instellingen niet kan inwilligen.</span><span class="sxs-lookup"><span data-stu-id="5d257-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="5d257-109">Met andere woorden, de plaatsen worden weergegeven waar bepaalde processen mogelijk worden genegeerd of niet worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="5d257-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="5d257-110">Resultaten van analyse: voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="5d257-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="5d257-111">**Functie:** productie</span><span class="sxs-lookup"><span data-stu-id="5d257-111">**Feature:** Production</span></span>
- <span data-ttu-id="5d257-112">**Probleem:** artikelen met stuklijstniveau hoger dan nul: 56</span><span class="sxs-lookup"><span data-stu-id="5d257-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="5d257-113">**Uitleg:** de aanpassingsanalyse heeft 56 artikelen gevonden met een ingestelde stuklijst voor productie.</span><span class="sxs-lookup"><span data-stu-id="5d257-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="5d257-114">Omdat de huidige versie van Planningsoptimalisatie productie niet ondersteunt, worden in Planningsoptimalisatie geplande inkooporders gegenereerd in plaats van geplande productieorders.</span><span class="sxs-lookup"><span data-stu-id="5d257-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="5d257-115">Er wordt ook een waarschuwing weergegeven waarin de betreffende artikelen worden vermeld.</span><span class="sxs-lookup"><span data-stu-id="5d257-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="5d257-116">Resultaten van analyse: voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="5d257-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="5d257-117">**Functie:** acties</span><span class="sxs-lookup"><span data-stu-id="5d257-117">**Feature:** Actions</span></span>
- <span data-ttu-id="5d257-118">**Probleem:** behoefteplanningsgroepen waarvoor actieberekening is ingeschakeld: 6</span><span class="sxs-lookup"><span data-stu-id="5d257-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="5d257-119">**Uitleg:** de aanpassingsanalyse heeft zes behoefteplanningsgroepen gevonden waarvoor actieberekeningen zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="5d257-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="5d257-120">Omdat de huidige versie van Planningsoptimalisatie acties niet ondersteunt, worden er geen acties gegenereerd tijdens de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="5d257-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="5d257-121">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="5d257-121">Related resources</span></span>

[<span data-ttu-id="5d257-122">Overzicht van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="5d257-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="5d257-123">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="5d257-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="5d257-124">Planhistorie en planningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="5d257-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="5d257-125">Filters op een plan toepassen</span><span class="sxs-lookup"><span data-stu-id="5d257-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="5d257-126">Een planningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="5d257-126">Cancel a planning job</span></span>](cancel-planning-job.md)
