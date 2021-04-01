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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6505d658103a4c34dfe7c7eb86ad4ea41515ccfb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261279"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="4ec04-103">Beleid voor totalisering van kosten maken</span><span class="sxs-lookup"><span data-stu-id="4ec04-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4ec04-104">Deze procedure laat zien hoe u een beleid voor het totaliseren van kosten maakt en regels voor het beleid maakt.</span><span class="sxs-lookup"><span data-stu-id="4ec04-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="4ec04-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.</span><span class="sxs-lookup"><span data-stu-id="4ec04-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="4ec04-106">Een beleid maken</span><span class="sxs-lookup"><span data-stu-id="4ec04-106">Create a policy</span></span>
1. <span data-ttu-id="4ec04-107">Ga naar Kostprijsboekhouding > Beleid > Beleidslijnen voor totalisering van kosten.</span><span class="sxs-lookup"><span data-stu-id="4ec04-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="4ec04-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4ec04-108">Click New.</span></span>
3. <span data-ttu-id="4ec04-109">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="4ec04-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="4ec04-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="4ec04-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4ec04-111">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="4ec04-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-112">Selecteer Kosten totaliseren CC.</span><span class="sxs-lookup"><span data-stu-id="4ec04-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="4ec04-113">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="4ec04-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-114">Selecteer Kosten totaliseren CC.</span><span class="sxs-lookup"><span data-stu-id="4ec04-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="4ec04-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4ec04-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="4ec04-116">Regels maken voor het beleid voor totalisering van kosten</span><span class="sxs-lookup"><span data-stu-id="4ec04-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="4ec04-117">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4ec04-117">Click New.</span></span>
2. <span data-ttu-id="4ec04-118">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4ec04-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4ec04-119">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="4ec04-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-120">Selecteer 007.</span><span class="sxs-lookup"><span data-stu-id="4ec04-120">Select 007.</span></span>  
4. <span data-ttu-id="4ec04-121">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="4ec04-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-122">Selecteer Kosten totaliseren CE.</span><span class="sxs-lookup"><span data-stu-id="4ec04-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="4ec04-123">Typ of selecteer een waarde in het veld Secundair kostenelement.</span><span class="sxs-lookup"><span data-stu-id="4ec04-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-124">Wijs voor dit voorbeeld het secundaire kostenelement CC-007 toe aan de kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="4ec04-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="4ec04-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4ec04-125">Click New.</span></span>
7. <span data-ttu-id="4ec04-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4ec04-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4ec04-127">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="4ec04-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-128">Selecteer 008.</span><span class="sxs-lookup"><span data-stu-id="4ec04-128">Select 008.</span></span>  
9. <span data-ttu-id="4ec04-129">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="4ec04-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-130">Selecteer Kosten totaliseren CE.</span><span class="sxs-lookup"><span data-stu-id="4ec04-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="4ec04-131">Typ of selecteer een waarde in het veld Secundair kostenelement.</span><span class="sxs-lookup"><span data-stu-id="4ec04-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-132">Wijs voor dit voorbeeld het secundaire kostenelement CC-008 toe aan de kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="4ec04-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="4ec04-133">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4ec04-133">Click New.</span></span>
12. <span data-ttu-id="4ec04-134">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4ec04-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="4ec04-135">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="4ec04-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-136">Selecteer 009.</span><span class="sxs-lookup"><span data-stu-id="4ec04-136">Select 009.</span></span>  
14. <span data-ttu-id="4ec04-137">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="4ec04-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-138">Selecteer Kosten totaliseren CE.</span><span class="sxs-lookup"><span data-stu-id="4ec04-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="4ec04-139">Typ of selecteer een waarde in het veld Secundair kostenelement.</span><span class="sxs-lookup"><span data-stu-id="4ec04-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="4ec04-140">Wijs voor dit voorbeeld het secundaire kostenelement CC-009 toe aan de kostenplaats.</span><span class="sxs-lookup"><span data-stu-id="4ec04-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="4ec04-141">Ga door totdat alle kostenplaatsen zijn toegewezen aan de overeenkomstige secundaire kostenelementen.</span><span class="sxs-lookup"><span data-stu-id="4ec04-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="4ec04-142">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4ec04-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]