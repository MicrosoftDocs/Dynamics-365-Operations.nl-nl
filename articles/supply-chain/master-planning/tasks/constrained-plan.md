---
title: Een plan met beperkingen genereren
description: In dit onderwerp ziet u hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808011"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="42c50-103">Een plan met beperkingen genereren</span><span class="sxs-lookup"><span data-stu-id="42c50-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42c50-104">In dit onderwerp ziet u hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.</span><span class="sxs-lookup"><span data-stu-id="42c50-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="42c50-105">Het plan garandeert dat de productie niet start voordat de materialen beschikbaar zijn en dat resources niet worden overboekt.</span><span class="sxs-lookup"><span data-stu-id="42c50-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="42c50-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="42c50-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="42c50-107">Deze procedure is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="42c50-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="42c50-108">Een plan met beperkingen instellen</span><span class="sxs-lookup"><span data-stu-id="42c50-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="42c50-109">Selecteer op de startpagina het werkgebied **Hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="42c50-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="42c50-110">Selecteer **Hoofdplannen** in de lijst met koppelingen aan de rechterkant van het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="42c50-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="42c50-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="42c50-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="42c50-112">Voorbeeld: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="42c50-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="42c50-113">Selecteer **Ja** in het veld **Eindige capaciteit**.</span><span class="sxs-lookup"><span data-stu-id="42c50-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="42c50-114">Voer `30` in het veld **Tijdlimiet beperkte capaciteit** in.</span><span class="sxs-lookup"><span data-stu-id="42c50-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="42c50-115">Vouw de sectie **Time fences in dagen** uit.</span><span class="sxs-lookup"><span data-stu-id="42c50-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="42c50-116">Selecteer **Ja** in het veld **Capaciteit**.</span><span class="sxs-lookup"><span data-stu-id="42c50-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="42c50-117">Voer in het veld **Time fence capaciteitsplanning (dagen)** een getal in.</span><span class="sxs-lookup"><span data-stu-id="42c50-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="42c50-118">Voorbeeld: `60`</span><span class="sxs-lookup"><span data-stu-id="42c50-118">Example: `60`</span></span>  
9. <span data-ttu-id="42c50-119">Selecteer **Ja** in het veld **Berekende vertragingen**.</span><span class="sxs-lookup"><span data-stu-id="42c50-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="42c50-120">Voer in het veld **Time fence vertragingen berekenen (dagen)** een getal in.</span><span class="sxs-lookup"><span data-stu-id="42c50-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="42c50-121">Voorbeeld: `60`</span><span class="sxs-lookup"><span data-stu-id="42c50-121">Example: `60`</span></span> 
11. <span data-ttu-id="42c50-122">Vouw de sectie **Berekende vertragingen** uit.</span><span class="sxs-lookup"><span data-stu-id="42c50-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="42c50-123">Selecteer **Ja** in alle velden van **De berekende vertraging optellen bij de behoeftedatum**.</span><span class="sxs-lookup"><span data-stu-id="42c50-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="42c50-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="42c50-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="42c50-125">Plan met beperkingen maken</span><span class="sxs-lookup"><span data-stu-id="42c50-125">Create a constrained plan</span></span>
1. <span data-ttu-id="42c50-126">Selecteer **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="42c50-126">Select **Run**.</span></span>
2. <span data-ttu-id="42c50-127">Typ of selecteer in het veld **Hoofdplan** het plan waarvoor u beperkingen hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="42c50-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="42c50-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="42c50-128">Select **OK**.</span></span>
4. <span data-ttu-id="42c50-129">Selecteer **Geplande orders**.</span><span class="sxs-lookup"><span data-stu-id="42c50-129">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]