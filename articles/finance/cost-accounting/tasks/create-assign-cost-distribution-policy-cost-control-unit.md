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
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f51350acbb838724e0a953547f6488bc1df8578
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759347"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="8b674-103">Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="8b674-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b674-104">Kostenverdelingsregels worden gebruikt om kosten te verdelen die financieel zijn geteld in een collectieve kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="8b674-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="8b674-105">De kostenaccountant zorgt dat de kosten worden gedistribueerd naar de kostencentra, op basis van de geselecteerde toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="8b674-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="8b674-106">Een beleid en de bijbehorende regels worden toegewezen aan een kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="8b674-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="8b674-107">Deze taakbegeleider gebruikt een voorbeeld om te laten zien hoe u een beleid voor distributie van kosten en de bijbehorende regels maakt.</span><span class="sxs-lookup"><span data-stu-id="8b674-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="8b674-108">Een beleid maken</span><span class="sxs-lookup"><span data-stu-id="8b674-108">Create a policy</span></span>
1. <span data-ttu-id="8b674-109">Ga naar Kostprijsboekhouding > Beleid > Kostenverdelingsbeleid.</span><span class="sxs-lookup"><span data-stu-id="8b674-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="8b674-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8b674-110">Click New.</span></span>
3. <span data-ttu-id="8b674-111">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="8b674-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="8b674-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="8b674-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8b674-113">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="8b674-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8b674-114">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="8b674-114">Select Organization.</span></span>  
6. <span data-ttu-id="8b674-115">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="8b674-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="8b674-116">Selecteer CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="8b674-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="8b674-117">Typ of selecteer een waarde in het veld Statistische dimensie.</span><span class="sxs-lookup"><span data-stu-id="8b674-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="8b674-118">Selecteer Statistische elementen.</span><span class="sxs-lookup"><span data-stu-id="8b674-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="8b674-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8b674-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="8b674-120">Regels voor het beleid maken</span><span class="sxs-lookup"><span data-stu-id="8b674-120">Create rules for the policy</span></span>
1. <span data-ttu-id="8b674-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8b674-121">Click New.</span></span>
2. <span data-ttu-id="8b674-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8b674-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="8b674-123">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="8b674-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b674-124">Vouw de sectie te selecteren hiërarchie 094 uit.</span><span class="sxs-lookup"><span data-stu-id="8b674-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="8b674-125">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="8b674-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b674-126">Selecteer Overige bedrijfsonkosten en selecteer vervolgens 605110 Reiniging.</span><span class="sxs-lookup"><span data-stu-id="8b674-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="8b674-127">Selecteer een optie in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="8b674-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="8b674-128">Selecteer Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="8b674-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="8b674-129">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="8b674-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="8b674-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8b674-130">Click New.</span></span>
8. <span data-ttu-id="8b674-131">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8b674-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="8b674-132">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="8b674-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b674-133">Vouw de sectie te selecteren hiërarchie 094 uit.</span><span class="sxs-lookup"><span data-stu-id="8b674-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="8b674-134">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="8b674-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="8b674-135">Selecteer Overige bedrijfsonkosten en selecteer vervolgens 605150 Huur.</span><span class="sxs-lookup"><span data-stu-id="8b674-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="8b674-136">Selecteer een optie in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="8b674-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="8b674-137">Selecteer Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="8b674-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="8b674-138">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="8b674-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="8b674-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8b674-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="8b674-140">Regels aan een kostenbeheereenheid toewijzen</span><span class="sxs-lookup"><span data-stu-id="8b674-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="8b674-141">Klik op Beleidstoewijzingen voor kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="8b674-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="8b674-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="8b674-142">Click New.</span></span>
3. <span data-ttu-id="8b674-143">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="8b674-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8b674-144">Typ een datum in het veld Geldig vanaf boekhouddatum.</span><span class="sxs-lookup"><span data-stu-id="8b674-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="8b674-145">Selecteer 1 september in het geldige boekjaar.</span><span class="sxs-lookup"><span data-stu-id="8b674-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="8b674-146">Typ of selecteer een waarde in het veld Kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="8b674-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="8b674-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8b674-147">Click Save.</span></span>

