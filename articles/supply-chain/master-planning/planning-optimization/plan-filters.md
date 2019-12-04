---
title: Filters op een plan toepassen
description: In dit onderwerp wordt uitgelegd hoe u filters gebruikt voor een plan wanneer de functionaliteit Planningsoptimalisatie wordt gebruikt.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773935"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="f8d81-103">Filters op een plan toepassen</span><span class="sxs-lookup"><span data-stu-id="f8d81-103">Apply filters to a plan</span></span>

<span data-ttu-id="f8d81-104">Wanneer de functionaliteit Planningsoptimalisatie wordt gebruikt, kunt u een filter toepassen op een plan.</span><span class="sxs-lookup"><span data-stu-id="f8d81-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="f8d81-105">Het planfilter wordt altijd toegepast tijdens de uitvoering van een hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="f8d81-105">The plan filter will always be applied during a master planning run.</span></span> <span data-ttu-id="f8d81-106">Een planfilter is handig als u een plan wilt beperken tot een bepaalde groep artikelen en als u ervoor wilt zorgen dat er geen andere artikelen worden opgenomen als onderdeel van de resulterende hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="f8d81-106">A plan filter is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="f8d81-107">Als er een planfilter wordt toegepast en er tijdens de uitvoering van een hoofdplanning ook een runtimefilter wordt toegepast, wordt alleen het snijpunt van de twee filters opgenomen in de planningsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="f8d81-107">If a plan filter is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="f8d81-108">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="f8d81-108">Example scenario</span></span>

<span data-ttu-id="f8d81-109">Er is een planfilter ingesteld met de artikelen A, B en C. Vervolgens vinden voor hetzelfde plan hoofdplanningsuitvoeringen plaats, maar worden er verschillende runtimefilters toegepast:</span><span class="sxs-lookup"><span data-stu-id="f8d81-109">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="f8d81-110">**Runtimefilter dat artikel D bevat:** er zijn geen artikelen gepland omdat er geen snijpunt tussen het planfilter en runtimefilter bestaat.</span><span class="sxs-lookup"><span data-stu-id="f8d81-110">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="f8d81-111">**Runtimefilter dat artikel A en D bevat:** alleen artikel A wordt opgenomen in de planningsuitvoering omdat artikel D geen deel uitmaakt van het planfilter.</span><span class="sxs-lookup"><span data-stu-id="f8d81-111">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="f8d81-112">**Runtimefilter dat artikel B bevat:** alleen artikel B wordt opgenomen in de planningsuitvoering en de eerdere planningsuitvoer voor artikel A wordt behouden.</span><span class="sxs-lookup"><span data-stu-id="f8d81-112">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="f8d81-113">**Runtimefilter dat alle artikelen bevat (leeg filter):** artikelen A, B en C worden opgenomen in de planningsuitvoering en de eerdere planningsuitvoer voor artikelen A en B wordt overschreven.</span><span class="sxs-lookup"><span data-stu-id="f8d81-113">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="f8d81-114">Stel geen planfilter in voor het plan dat als **Huidig dynamisch hoofdplan** is geselecteerd op de pagina **Parameters hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="f8d81-114">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="f8d81-115">Anders wordt de functionaliteit voor dynamische hoofdplannen beperkt tot de gefilterde artikelen.</span><span class="sxs-lookup"><span data-stu-id="f8d81-115">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="f8d81-116">Als de nettobehoeften bijvoorbeeld worden bijgewerkt voor een artikel dat geen deel uitmaakt van het planfilter, wordt er geen resultaat gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="f8d81-116">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="f8d81-117">Gerelateerde bronnen</span><span class="sxs-lookup"><span data-stu-id="f8d81-117">Related resources</span></span>

[<span data-ttu-id="f8d81-118">Overzicht van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="f8d81-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="f8d81-119">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="f8d81-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="f8d81-120">Analyse voor passende Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="f8d81-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="f8d81-121">Planhistorie en planningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="f8d81-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="f8d81-122">Een planningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="f8d81-122">Cancel a planning job</span></span>](cancel-planning-job.md)
