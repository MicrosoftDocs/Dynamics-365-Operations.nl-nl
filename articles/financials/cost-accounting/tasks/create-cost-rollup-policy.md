---
title: Beleid voor totalisering van kosten maken
description: Deze procedure laat zien hoe u een beleid voor het totaliseren van kosten maakt en regels voor het beleid maakt.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f1fa434061832bd306cef13afc46c7f3adab0c0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "362597"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="00e2e-103">Beleid voor totalisering van kosten maken</span><span class="sxs-lookup"><span data-stu-id="00e2e-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00e2e-104">Deze procedure laat zien hoe u een beleid voor het totaliseren van kosten maakt en regels voor het beleid maakt.</span><span class="sxs-lookup"><span data-stu-id="00e2e-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="00e2e-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.</span><span class="sxs-lookup"><span data-stu-id="00e2e-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="00e2e-106">Een beleid maken</span><span class="sxs-lookup"><span data-stu-id="00e2e-106">Create a policy</span></span>
1. <span data-ttu-id="00e2e-107">Ga naar Kostprijsboekhouding > Beleid > Beleidslijnen voor totalisering van kosten.</span><span class="sxs-lookup"><span data-stu-id="00e2e-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="00e2e-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="00e2e-108">Click New.</span></span>
3. <span data-ttu-id="00e2e-109">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="00e2e-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="00e2e-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="00e2e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="00e2e-111">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="00e2e-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-112">Selecteer Kosten totaliseren CC.</span><span class="sxs-lookup"><span data-stu-id="00e2e-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="00e2e-113">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="00e2e-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-114">Selecteer Kosten totaliseren CC.</span><span class="sxs-lookup"><span data-stu-id="00e2e-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="00e2e-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="00e2e-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="00e2e-116">Regels maken voor het beleid voor totalisering van kosten</span><span class="sxs-lookup"><span data-stu-id="00e2e-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="00e2e-117">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="00e2e-117">Click New.</span></span>
2. <span data-ttu-id="00e2e-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="00e2e-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="00e2e-119">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="00e2e-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-120">Selecteer 007.</span><span class="sxs-lookup"><span data-stu-id="00e2e-120">Select 007.</span></span>  
4. <span data-ttu-id="00e2e-121">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="00e2e-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-122">Selecteer Kosten totaliseren CE.</span><span class="sxs-lookup"><span data-stu-id="00e2e-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="00e2e-123">Typ of selecteer een waarde in het veld Secundair kostenelement.</span><span class="sxs-lookup"><span data-stu-id="00e2e-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-124">Wijs voor dit voorbeeld het secundaire kostenelement CC-007 toe aan de kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="00e2e-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="00e2e-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="00e2e-125">Click New.</span></span>
7. <span data-ttu-id="00e2e-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="00e2e-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="00e2e-127">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="00e2e-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-128">Selecteer 008.</span><span class="sxs-lookup"><span data-stu-id="00e2e-128">Select 008.</span></span>  
9. <span data-ttu-id="00e2e-129">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="00e2e-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-130">Selecteer Kosten totaliseren CE.</span><span class="sxs-lookup"><span data-stu-id="00e2e-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="00e2e-131">Typ of selecteer een waarde in het veld Secundair kostenelement.</span><span class="sxs-lookup"><span data-stu-id="00e2e-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-132">Wijs voor dit voorbeeld het secundaire kostenelement CC-008 toe aan de kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="00e2e-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="00e2e-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="00e2e-133">Click New.</span></span>
12. <span data-ttu-id="00e2e-134">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="00e2e-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="00e2e-135">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="00e2e-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-136">Selecteer 009.</span><span class="sxs-lookup"><span data-stu-id="00e2e-136">Select 009.</span></span>  
14. <span data-ttu-id="00e2e-137">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="00e2e-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-138">Selecteer Kosten totaliseren CE.</span><span class="sxs-lookup"><span data-stu-id="00e2e-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="00e2e-139">Typ of selecteer een waarde in het veld Secundair kostenelement.</span><span class="sxs-lookup"><span data-stu-id="00e2e-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="00e2e-140">Wijs voor dit voorbeeld het secundaire kostenelement CC-009 toe aan de kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="00e2e-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="00e2e-141">Ga door totdat alle kostenplaatsen zijn toegewezen aan de overeenkomstige secundaire kostenelementen.</span><span class="sxs-lookup"><span data-stu-id="00e2e-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="00e2e-142">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="00e2e-142">Click Save.</span></span>

