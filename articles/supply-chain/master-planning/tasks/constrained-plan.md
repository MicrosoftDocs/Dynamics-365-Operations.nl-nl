---
title: Een plan met beperkingen genereren
description: In dit onderwerp ziet u hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4af946a8dd4e5311bcb90386c88d5e7f205c4eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999851"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="a6bae-103">Een plan met beperkingen genereren</span><span class="sxs-lookup"><span data-stu-id="a6bae-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6bae-104">In dit onderwerp ziet u hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.</span><span class="sxs-lookup"><span data-stu-id="a6bae-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="a6bae-105">Het plan garandeert dat de productie niet start voordat de materialen beschikbaar zijn en dat resources niet worden overboekt.</span><span class="sxs-lookup"><span data-stu-id="a6bae-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="a6bae-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="a6bae-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a6bae-107">Deze procedure is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="a6bae-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="a6bae-108">Een plan met beperkingen instellen</span><span class="sxs-lookup"><span data-stu-id="a6bae-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="a6bae-109">Selecteer op de startpagina het werkgebied **Hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="a6bae-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="a6bae-110">Selecteer **Hoofdplannen** in de lijst met koppelingen aan de rechterkant van het werkgebied.</span><span class="sxs-lookup"><span data-stu-id="a6bae-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="a6bae-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a6bae-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="a6bae-112">Voorbeeld: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="a6bae-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="a6bae-113">Selecteer **Ja** in het veld **Eindige capaciteit**.</span><span class="sxs-lookup"><span data-stu-id="a6bae-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="a6bae-114">Voer `30` in het veld **Tijdlimiet beperkte capaciteit** in.</span><span class="sxs-lookup"><span data-stu-id="a6bae-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="a6bae-115">Vouw de sectie **Time fences in dagen** uit.</span><span class="sxs-lookup"><span data-stu-id="a6bae-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="a6bae-116">Selecteer **Ja** in het veld **Capaciteit**.</span><span class="sxs-lookup"><span data-stu-id="a6bae-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="a6bae-117">Voer in het veld **Time fence capaciteitsplanning (dagen)** een getal in.</span><span class="sxs-lookup"><span data-stu-id="a6bae-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="a6bae-118">Voorbeeld: `60`</span><span class="sxs-lookup"><span data-stu-id="a6bae-118">Example: `60`</span></span>  
9. <span data-ttu-id="a6bae-119">Selecteer **Ja** in het veld **Berekende vertragingen**.</span><span class="sxs-lookup"><span data-stu-id="a6bae-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="a6bae-120">Voer in het veld **Time fence vertragingen berekenen (dagen)** een getal in.</span><span class="sxs-lookup"><span data-stu-id="a6bae-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="a6bae-121">Voorbeeld: `60`</span><span class="sxs-lookup"><span data-stu-id="a6bae-121">Example: `60`</span></span> 
11. <span data-ttu-id="a6bae-122">Vouw de sectie **Berekende vertragingen** uit.</span><span class="sxs-lookup"><span data-stu-id="a6bae-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="a6bae-123">Selecteer **Ja** in alle velden van **De berekende vertraging optellen bij de behoeftedatum**.</span><span class="sxs-lookup"><span data-stu-id="a6bae-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="a6bae-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a6bae-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="a6bae-125">Plan met beperkingen maken</span><span class="sxs-lookup"><span data-stu-id="a6bae-125">Create a constrained plan</span></span>
1. <span data-ttu-id="a6bae-126">Selecteer **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="a6bae-126">Select **Run**.</span></span>
2. <span data-ttu-id="a6bae-127">Typ of selecteer in het veld **Hoofdplan** het plan waarvoor u beperkingen hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="a6bae-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="a6bae-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6bae-128">Select **OK**.</span></span>
4. <span data-ttu-id="a6bae-129">Selecteer **Geplande orders**.</span><span class="sxs-lookup"><span data-stu-id="a6bae-129">Select **Planned orders**.</span></span>

