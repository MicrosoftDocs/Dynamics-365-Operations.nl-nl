---
title: Een plan met beperkingen genereren
description: In dit onderwerp ziet u hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b5d37de41fe68845cec3f2285aed2484ac117aa
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867168"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="87af4-103">Een plan met beperkingen genereren</span><span class="sxs-lookup"><span data-stu-id="87af4-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87af4-104">In dit onderwerp ziet u hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.</span><span class="sxs-lookup"><span data-stu-id="87af4-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="87af4-105">Het plan garandeert dat de productie niet start voordat de materialen beschikbaar zijn en dat resources niet worden overboekt.</span><span class="sxs-lookup"><span data-stu-id="87af4-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="87af4-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="87af4-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="87af4-107">Deze procedure is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="87af4-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="87af4-108">Een plan met beperkingen instellen</span><span class="sxs-lookup"><span data-stu-id="87af4-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="87af4-109">Selecteer op de startpagina het werkgebied **Hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="87af4-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="87af4-110">Selecteer **Hoofdplannen** in de lijst met koppelingen aan de rechterkant van het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="87af4-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="87af4-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="87af4-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="87af4-112">Voorbeeld: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="87af4-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="87af4-113">Selecteer **Ja** in het veld **Eindige capaciteit**.</span><span class="sxs-lookup"><span data-stu-id="87af4-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="87af4-114">Voer `30` in het veld **Tijdlimiet beperkte capaciteit** in.</span><span class="sxs-lookup"><span data-stu-id="87af4-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="87af4-115">Vouw de sectie **Time fences in dagen** uit.</span><span class="sxs-lookup"><span data-stu-id="87af4-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="87af4-116">Selecteer **Ja** in het veld **Capaciteit**.</span><span class="sxs-lookup"><span data-stu-id="87af4-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="87af4-117">Voer in het veld **Time fence capaciteitsplanning (dagen)** een getal in.</span><span class="sxs-lookup"><span data-stu-id="87af4-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="87af4-118">Voorbeeld: `60`</span><span class="sxs-lookup"><span data-stu-id="87af4-118">Example: `60`</span></span>  
9. <span data-ttu-id="87af4-119">Selecteer **Ja** in het veld **Berekende vertragingen**.</span><span class="sxs-lookup"><span data-stu-id="87af4-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="87af4-120">Voer in het veld **Time fence vertragingen berekenen (dagen)** een getal in.</span><span class="sxs-lookup"><span data-stu-id="87af4-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="87af4-121">Voorbeeld: `60`</span><span class="sxs-lookup"><span data-stu-id="87af4-121">Example: `60`</span></span> 
11. <span data-ttu-id="87af4-122">Vouw de sectie **Berekende vertragingen** uit.</span><span class="sxs-lookup"><span data-stu-id="87af4-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="87af4-123">Selecteer **Ja** in alle velden van **De berekende vertraging optellen bij de behoeftedatum**.</span><span class="sxs-lookup"><span data-stu-id="87af4-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="87af4-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="87af4-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="87af4-125">Plan met beperkingen maken</span><span class="sxs-lookup"><span data-stu-id="87af4-125">Create a constrained plan</span></span>
1. <span data-ttu-id="87af4-126">Selecteer **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="87af4-126">Select **Run**.</span></span>
2. <span data-ttu-id="87af4-127">Typ of selecteer in het veld **Hoofdplan** het plan waarvoor u beperkingen hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="87af4-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="87af4-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="87af4-128">Select **OK**.</span></span>
4. <span data-ttu-id="87af4-129">Selecteer **Geplande orders**.</span><span class="sxs-lookup"><span data-stu-id="87af4-129">Select **Planned orders**.</span></span>

