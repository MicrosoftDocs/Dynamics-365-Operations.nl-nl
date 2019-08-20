---
title: Een plan met beperkingen genereren
description: Deze procedure laat zien hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845283"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="56105-103">Een plan met beperkingen genereren</span><span class="sxs-lookup"><span data-stu-id="56105-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56105-104">Deze procedure laat zien hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.</span><span class="sxs-lookup"><span data-stu-id="56105-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="56105-105">Het plan garandeert dat de productie niet start voordat de materialen beschikbaar zijn en dat resources niet worden overboekt.</span><span class="sxs-lookup"><span data-stu-id="56105-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="56105-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="56105-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="56105-107">Deze procedure is bedoeld voor de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="56105-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="56105-108">Een plan met beperkingen instellen</span><span class="sxs-lookup"><span data-stu-id="56105-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="56105-109">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="56105-109">Click Master planning.</span></span>
2. <span data-ttu-id="56105-110">Klik op Hoofdplannen.</span><span class="sxs-lookup"><span data-stu-id="56105-110">Click Master plans.</span></span>
3. <span data-ttu-id="56105-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="56105-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="56105-112">Voorbeeld: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="56105-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="56105-113">Selecteer Ja in het veld Eindige capaciteit.</span><span class="sxs-lookup"><span data-stu-id="56105-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="56105-114">Voer 30 in het veld Tijdlimiet beperkte capaciteit in.</span><span class="sxs-lookup"><span data-stu-id="56105-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="56105-115">Vouw de sectie Time fences in dagen uit.</span><span class="sxs-lookup"><span data-stu-id="56105-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="56105-116">Selecteer Ja in het veld Capaciteit.</span><span class="sxs-lookup"><span data-stu-id="56105-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="56105-117">Voer in het veld Time fence capaciteitsplanning (dagen) een nummer in.</span><span class="sxs-lookup"><span data-stu-id="56105-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="56105-118">Voorbeeld: 60</span><span class="sxs-lookup"><span data-stu-id="56105-118">Example: 60</span></span>  
9. <span data-ttu-id="56105-119">Selecteer Ja in het veld Berekende vertragingen.</span><span class="sxs-lookup"><span data-stu-id="56105-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="56105-120">Voer in het veld Time fence vertragingen berekenen (dagen) een nummer in.</span><span class="sxs-lookup"><span data-stu-id="56105-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="56105-121">Voorbeeld: 60</span><span class="sxs-lookup"><span data-stu-id="56105-121">Example: 60</span></span>  
11. <span data-ttu-id="56105-122">Vouw de sectie Berekende vertragingen uit.</span><span class="sxs-lookup"><span data-stu-id="56105-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="56105-123">Selecteer Ja in het veld De berekende vertraging optellen bij de behoeftedatum.</span><span class="sxs-lookup"><span data-stu-id="56105-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="56105-124">Selecteer Ja in het veld De berekende vertraging optellen bij de behoeftedatum.</span><span class="sxs-lookup"><span data-stu-id="56105-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="56105-125">Selecteer Ja in het veld De berekende vertraging optellen bij de behoeftedatum.</span><span class="sxs-lookup"><span data-stu-id="56105-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="56105-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="56105-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="56105-127">Plan met beperkingen maken</span><span class="sxs-lookup"><span data-stu-id="56105-127">Create a constrained plan</span></span>
1. <span data-ttu-id="56105-128">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="56105-128">Click Run.</span></span>
2. <span data-ttu-id="56105-129">Typ of selecteer een waarde in het veld Hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="56105-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="56105-130">Selecteer het plan waarvoor u beperkingen hebt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="56105-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="56105-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="56105-131">Click OK.</span></span>
    * <span data-ttu-id="56105-132">Dit kan enige tijd duren.</span><span class="sxs-lookup"><span data-stu-id="56105-132">This may take a while.</span></span>  
4. <span data-ttu-id="56105-133">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="56105-133">Click Planned orders.</span></span>

