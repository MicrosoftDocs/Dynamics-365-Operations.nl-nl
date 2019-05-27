---
title: Een hoofdplanningsuitvoering controleren
description: De productieplanner wil zien of er een hoofdplanning wordt uitgevoerd.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565599"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="34ba6-103">Een hoofdplanningsuitvoering controleren</span><span class="sxs-lookup"><span data-stu-id="34ba6-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34ba6-104">De productieplanner wil zien of er een hoofdplanning wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="34ba6-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="34ba6-105">Gebruik het demobedrijf USMF om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="34ba6-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="34ba6-106">Hoofdplanning uitvoeren</span><span class="sxs-lookup"><span data-stu-id="34ba6-106">Run master planning</span></span>
1. <span data-ttu-id="34ba6-107">Klik op Hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="34ba6-107">Click Master planning.</span></span>
    * <span data-ttu-id="34ba6-108">U vindt dit in het standaarddashboard.</span><span class="sxs-lookup"><span data-stu-id="34ba6-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="34ba6-109">Typ of selecteer een waarde in het veld Plan.</span><span class="sxs-lookup"><span data-stu-id="34ba6-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="34ba6-110">Voorbeeld: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="34ba6-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="34ba6-111">Klik op Uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="34ba6-111">Click Run.</span></span>
4. <span data-ttu-id="34ba6-112">Selecteer Ja in het veld Verwerkingstijd traceren.</span><span class="sxs-lookup"><span data-stu-id="34ba6-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="34ba6-113">Als het veld al is geselecteerd, slaat u deze stap over.</span><span class="sxs-lookup"><span data-stu-id="34ba6-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="34ba6-114">Voer een getal in het veld Aantal threads in.</span><span class="sxs-lookup"><span data-stu-id="34ba6-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="34ba6-115">Breid de sectie Op te nemen records uit.</span><span class="sxs-lookup"><span data-stu-id="34ba6-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="34ba6-116">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="34ba6-116">Click Filter.</span></span>
8. <span data-ttu-id="34ba6-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="34ba6-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="34ba6-118">Markeer de rij waarin Veld = Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="34ba6-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="34ba6-119">Typ of selecteer een waarde in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="34ba6-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="34ba6-120">Voorbeeld: T0001</span><span class="sxs-lookup"><span data-stu-id="34ba6-120">Example: T0001</span></span>  
10. <span data-ttu-id="34ba6-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="34ba6-121">Click OK.</span></span>
11. <span data-ttu-id="34ba6-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="34ba6-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="34ba6-123">De hoofdplanningsuitvoering controleren</span><span class="sxs-lookup"><span data-stu-id="34ba6-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="34ba6-124">Klik op Historie.</span><span class="sxs-lookup"><span data-stu-id="34ba6-124">Click History.</span></span>
2. <span data-ttu-id="34ba6-125">Klik op Query's.</span><span class="sxs-lookup"><span data-stu-id="34ba6-125">Click Inquiries.</span></span>
3. <span data-ttu-id="34ba6-126">Klik op Duur procestaak.</span><span class="sxs-lookup"><span data-stu-id="34ba6-126">Click Process task duration.</span></span>
4. <span data-ttu-id="34ba6-127">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="34ba6-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="34ba6-128">Voor elk artikel kunt u een overzicht krijgen van de tijd die de voltooiing van elke planningsstap in beslag nam.</span><span class="sxs-lookup"><span data-stu-id="34ba6-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

