---
title: Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Kostenverdelingsregels worden gebruikt om kosten te verdelen die financieel zijn geteld in een collectieve kostenplaats.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 348bca5504a633c7b3f158a667a85d36eace52a0
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138440"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="59ab6-103">Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="59ab6-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59ab6-104">Kostenverdelingsregels worden gebruikt om kosten te verdelen die financieel zijn geteld in een collectieve kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="59ab6-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="59ab6-105">De kostenaccountant zorgt dat de kosten worden gedistribueerd naar de kostencentra, op basis van de geselecteerde toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="59ab6-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="59ab6-106">Een beleid en de bijbehorende regels worden toegewezen aan een kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="59ab6-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="59ab6-107">Deze taakbegeleider gebruikt een voorbeeld om te laten zien hoe u een beleid voor distributie van kosten en de bijbehorende regels maakt.</span><span class="sxs-lookup"><span data-stu-id="59ab6-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="59ab6-108">Een beleid maken</span><span class="sxs-lookup"><span data-stu-id="59ab6-108">Create a policy</span></span>
1. <span data-ttu-id="59ab6-109">Ga naar Kostprijsboekhouding > Beleid > Kostenverdelingsbeleid.</span><span class="sxs-lookup"><span data-stu-id="59ab6-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="59ab6-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="59ab6-110">Click New.</span></span>
3. <span data-ttu-id="59ab6-111">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="59ab6-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="59ab6-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="59ab6-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="59ab6-113">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="59ab6-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="59ab6-114">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="59ab6-114">Select Organization.</span></span>  
6. <span data-ttu-id="59ab6-115">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="59ab6-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="59ab6-116">Selecteer CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="59ab6-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="59ab6-117">Typ of selecteer een waarde in het veld Statistische dimensie.</span><span class="sxs-lookup"><span data-stu-id="59ab6-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="59ab6-118">Selecteer Statistische elementen.</span><span class="sxs-lookup"><span data-stu-id="59ab6-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="59ab6-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="59ab6-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="59ab6-120">Regels voor het beleid maken</span><span class="sxs-lookup"><span data-stu-id="59ab6-120">Create rules for the policy</span></span>
1. <span data-ttu-id="59ab6-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="59ab6-121">Click New.</span></span>
2. <span data-ttu-id="59ab6-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="59ab6-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="59ab6-123">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="59ab6-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="59ab6-124">Vouw de sectie te selecteren hiërarchie 094 uit.</span><span class="sxs-lookup"><span data-stu-id="59ab6-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="59ab6-125">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="59ab6-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="59ab6-126">Selecteer Overige bedrijfsonkosten en selecteer vervolgens 605110 Reiniging.</span><span class="sxs-lookup"><span data-stu-id="59ab6-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="59ab6-127">Selecteer een optie in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="59ab6-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="59ab6-128">Selecteer Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="59ab6-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="59ab6-129">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="59ab6-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="59ab6-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="59ab6-130">Click New.</span></span>
8. <span data-ttu-id="59ab6-131">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="59ab6-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="59ab6-132">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="59ab6-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="59ab6-133">Vouw de sectie te selecteren hiërarchie 094 uit.</span><span class="sxs-lookup"><span data-stu-id="59ab6-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="59ab6-134">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="59ab6-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="59ab6-135">Selecteer Overige bedrijfsonkosten en selecteer vervolgens 605150 Huur.</span><span class="sxs-lookup"><span data-stu-id="59ab6-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="59ab6-136">Selecteer een optie in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="59ab6-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="59ab6-137">Selecteer Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="59ab6-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="59ab6-138">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="59ab6-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="59ab6-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="59ab6-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="59ab6-140">Regels aan een kostenbeheereenheid toewijzen</span><span class="sxs-lookup"><span data-stu-id="59ab6-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="59ab6-141">Klik op Beleidstoewijzingen voor kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="59ab6-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="59ab6-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="59ab6-142">Click New.</span></span>
3. <span data-ttu-id="59ab6-143">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="59ab6-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="59ab6-144">Typ een datum in het veld Geldig vanaf boekhouddatum.</span><span class="sxs-lookup"><span data-stu-id="59ab6-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="59ab6-145">Selecteer 1 september in het geldige boekjaar.</span><span class="sxs-lookup"><span data-stu-id="59ab6-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="59ab6-146">Typ of selecteer een waarde in het veld Kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="59ab6-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="59ab6-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="59ab6-147">Click Save.</span></span>

