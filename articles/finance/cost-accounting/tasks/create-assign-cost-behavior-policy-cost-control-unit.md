---
title: Een kostengedragsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Kostengedrag is de classificatie van kosten als vast of variabel.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58f888a373af33832c24518fbb5483c3de2d1a58
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208698"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="df888-103">Een kostengedragsbeleid maken en toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="df888-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df888-104">Kostengedrag is de classificatie van kosten als vast of variabel.</span><span class="sxs-lookup"><span data-stu-id="df888-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="df888-105">Een beleid en de bijbehorende regels moeten worden toegewezen aan een kostenbeheereenheid wil het beleid van kracht worden.</span><span class="sxs-lookup"><span data-stu-id="df888-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="df888-106">Gebruik deze procedure om een beleid te maken en het vervolgens toe te wijzen aan een kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="df888-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="df888-107">Een kostengedraghiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="df888-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="df888-108">Ga naar Kostprijsboekhouding > Dimensies > Dimensiehiërarchieën.</span><span class="sxs-lookup"><span data-stu-id="df888-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="df888-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="df888-109">Click New.</span></span>
3. <span data-ttu-id="df888-110">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="df888-110">Click Create.</span></span>
4. <span data-ttu-id="df888-111">Typ in het veld Naam van dimensiehiërarchie 'Kostengedraghiërarchie'.</span><span class="sxs-lookup"><span data-stu-id="df888-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="df888-112">Typ of selecteer een waarde in het veld Dimensie.</span><span class="sxs-lookup"><span data-stu-id="df888-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-113">Selecteer Kostenelementen.</span><span class="sxs-lookup"><span data-stu-id="df888-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="df888-114">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="df888-114">Click Save.</span></span>
7. <span data-ttu-id="df888-115">Klik op Hiërarchie weergeven.</span><span class="sxs-lookup"><span data-stu-id="df888-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="df888-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="df888-116">Click New.</span></span>
9. <span data-ttu-id="df888-117">Typ een waarde in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="df888-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="df888-118">Voer Vaste kosten in.</span><span class="sxs-lookup"><span data-stu-id="df888-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="df888-119">Selecteer in de structuur 'Kostengedraghiërarchie'.</span><span class="sxs-lookup"><span data-stu-id="df888-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="df888-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="df888-120">Click New.</span></span>
12. <span data-ttu-id="df888-121">Typ een waarde in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="df888-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="df888-122">Voer Variabele kosten in.</span><span class="sxs-lookup"><span data-stu-id="df888-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="df888-123">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="df888-123">Click Save.</span></span>
14. <span data-ttu-id="df888-124">Selecteer in de structuur 'Kostengedraghiërarchie\Vaste kosten'.</span><span class="sxs-lookup"><span data-stu-id="df888-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="df888-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="df888-125">Click New.</span></span>
16. <span data-ttu-id="df888-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df888-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="df888-127">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="df888-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-128">Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="df888-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="df888-129">Typ of selecteer een waarde in het veld Tot dimensielid.</span><span class="sxs-lookup"><span data-stu-id="df888-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-130">Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="df888-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="df888-131">Selecteer in de structuur 'Kostengedraghiërarchie\Variabele kosten'.</span><span class="sxs-lookup"><span data-stu-id="df888-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="df888-132">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="df888-132">Click New.</span></span>
21. <span data-ttu-id="df888-133">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df888-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="df888-134">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="df888-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-135">Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="df888-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="df888-136">Typ of selecteer een waarde in het veld Tot dimensielid.</span><span class="sxs-lookup"><span data-stu-id="df888-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-137">Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="df888-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="df888-138">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="df888-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="df888-139">Het beleid en regels maken</span><span class="sxs-lookup"><span data-stu-id="df888-139">Create the policy and rules</span></span>
1. <span data-ttu-id="df888-140">Ga naar Kostprijsboekhouding > Beleid > Kostengedragbeleidslijnen.</span><span class="sxs-lookup"><span data-stu-id="df888-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="df888-141">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="df888-141">Click New.</span></span>
3. <span data-ttu-id="df888-142">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="df888-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="df888-143">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="df888-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-144">Selecteer de beleidshiërarchie die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="df888-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="df888-145">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="df888-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-146">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="df888-146">Select Organization.</span></span>  
6. <span data-ttu-id="df888-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="df888-147">Click Save.</span></span>
7. <span data-ttu-id="df888-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="df888-148">Click New.</span></span>
8. <span data-ttu-id="df888-149">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df888-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="df888-150">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="df888-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-151">Vouw de hiërarchie uit om Variabele kosten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="df888-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="df888-152">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="df888-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="df888-153">Standaard is het variabele percentage 100 procent.</span><span class="sxs-lookup"><span data-stu-id="df888-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="df888-154">Klik op Beleidstoewijzingen voor kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="df888-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="df888-155">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="df888-155">Click New.</span></span>
13. <span data-ttu-id="df888-156">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="df888-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="df888-157">Typ een datum in het veld Geldig vanaf boekhouddatum.</span><span class="sxs-lookup"><span data-stu-id="df888-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="df888-158">De regels zijn datumregels en een regel kan vervallen door een gebruiker of door het systeem, als een nieuwere versie wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="df888-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="df888-159">Typ of selecteer een waarde in het veld Kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="df888-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="df888-160">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="df888-160">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]