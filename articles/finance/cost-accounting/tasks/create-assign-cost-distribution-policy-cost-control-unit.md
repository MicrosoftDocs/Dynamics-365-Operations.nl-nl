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
ms.openlocfilehash: 1d040f9495c7fb36985b5f96c15ac43aa226da24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177164"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="38557-103">Een kostenverdelingsbeleid maken en toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="38557-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38557-104">Kostenverdelingsregels worden gebruikt om kosten te verdelen die financieel zijn geteld in een collectieve kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="38557-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="38557-105">De kostenaccountant zorgt dat de kosten worden gedistribueerd naar de kostencentra, op basis van de geselecteerde toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="38557-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="38557-106">Een beleid en de bijbehorende regels worden toegewezen aan een kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="38557-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="38557-107">Deze taakbegeleider gebruikt een voorbeeld om te laten zien hoe u een beleid voor distributie van kosten en de bijbehorende regels maakt.</span><span class="sxs-lookup"><span data-stu-id="38557-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="38557-108">Een beleid maken</span><span class="sxs-lookup"><span data-stu-id="38557-108">Create a policy</span></span>
1. <span data-ttu-id="38557-109">Ga naar Kostprijsboekhouding > Beleid > Kostenverdelingsbeleid.</span><span class="sxs-lookup"><span data-stu-id="38557-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="38557-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="38557-110">Click New.</span></span>
3. <span data-ttu-id="38557-111">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="38557-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="38557-112">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="38557-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="38557-113">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="38557-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="38557-114">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="38557-114">Select Organization.</span></span>  
6. <span data-ttu-id="38557-115">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="38557-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="38557-116">Selecteer CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="38557-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="38557-117">Typ of selecteer een waarde in het veld Statistische dimensie.</span><span class="sxs-lookup"><span data-stu-id="38557-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="38557-118">Selecteer Statistische elementen.</span><span class="sxs-lookup"><span data-stu-id="38557-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="38557-119">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="38557-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="38557-120">Regels voor het beleid maken</span><span class="sxs-lookup"><span data-stu-id="38557-120">Create rules for the policy</span></span>
1. <span data-ttu-id="38557-121">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="38557-121">Click New.</span></span>
2. <span data-ttu-id="38557-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="38557-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="38557-123">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="38557-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="38557-124">Vouw de sectie te selecteren hiërarchie 094 uit.</span><span class="sxs-lookup"><span data-stu-id="38557-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="38557-125">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="38557-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="38557-126">Selecteer Overige bedrijfsonkosten en selecteer vervolgens 605110 Reiniging.</span><span class="sxs-lookup"><span data-stu-id="38557-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="38557-127">Selecteer een optie in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="38557-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="38557-128">Selecteer Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="38557-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="38557-129">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="38557-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="38557-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="38557-130">Click New.</span></span>
8. <span data-ttu-id="38557-131">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="38557-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="38557-132">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="38557-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="38557-133">Vouw de sectie te selecteren hiërarchie 094 uit.</span><span class="sxs-lookup"><span data-stu-id="38557-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="38557-134">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="38557-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="38557-135">Selecteer Overige bedrijfsonkosten en selecteer vervolgens 605150 Huur.</span><span class="sxs-lookup"><span data-stu-id="38557-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="38557-136">Selecteer een optie in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="38557-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="38557-137">Selecteer Vaste kosten</span><span class="sxs-lookup"><span data-stu-id="38557-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="38557-138">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="38557-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="38557-139">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="38557-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="38557-140">Regels aan een kostenbeheereenheid toewijzen</span><span class="sxs-lookup"><span data-stu-id="38557-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="38557-141">Klik op Beleidstoewijzingen voor kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="38557-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="38557-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="38557-142">Click New.</span></span>
3. <span data-ttu-id="38557-143">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="38557-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="38557-144">Typ een datum in het veld Geldig vanaf boekhouddatum.</span><span class="sxs-lookup"><span data-stu-id="38557-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="38557-145">Selecteer 1 september in het geldige boekjaar.</span><span class="sxs-lookup"><span data-stu-id="38557-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="38557-146">Typ of selecteer een waarde in het veld Kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="38557-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="38557-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="38557-147">Click Save.</span></span>

