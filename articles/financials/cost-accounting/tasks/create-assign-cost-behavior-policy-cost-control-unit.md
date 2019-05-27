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
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7b39b7649aaef0d354b61e3d70b6cac887282ed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543882"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="9e10f-103">Een kostengedragsbeleid maken en toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="9e10f-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e10f-104">Kostengedrag is de classificatie van kosten als vast of variabel.</span><span class="sxs-lookup"><span data-stu-id="9e10f-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="9e10f-105">Een beleid en de bijbehorende regels moeten worden toegewezen aan een kostenbeheereenheid wil het beleid van kracht worden.</span><span class="sxs-lookup"><span data-stu-id="9e10f-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="9e10f-106">Gebruik deze procedure om een beleid te maken en het vervolgens toe te wijzen aan een kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="9e10f-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="9e10f-107">Een kostengedraghiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="9e10f-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="9e10f-108">Ga naar Kostprijsboekhouding > Dimensies > Dimensiehiërarchieën.</span><span class="sxs-lookup"><span data-stu-id="9e10f-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="9e10f-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9e10f-109">Click New.</span></span>
3. <span data-ttu-id="9e10f-110">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="9e10f-110">Click Create.</span></span>
4. <span data-ttu-id="9e10f-111">Typ in het veld Naam van dimensiehiërarchie 'Kostengedraghiërarchie'.</span><span class="sxs-lookup"><span data-stu-id="9e10f-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="9e10f-112">Typ of selecteer een waarde in het veld Dimensie.</span><span class="sxs-lookup"><span data-stu-id="9e10f-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-113">Selecteer Kostenelementen.</span><span class="sxs-lookup"><span data-stu-id="9e10f-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="9e10f-114">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9e10f-114">Click Save.</span></span>
7. <span data-ttu-id="9e10f-115">Klik op Hiërarchie weergeven.</span><span class="sxs-lookup"><span data-stu-id="9e10f-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="9e10f-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9e10f-116">Click New.</span></span>
9. <span data-ttu-id="9e10f-117">Typ een waarde in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="9e10f-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="9e10f-118">Voer Vaste kosten in.</span><span class="sxs-lookup"><span data-stu-id="9e10f-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="9e10f-119">Selecteer in de structuur 'Kostengedraghiërarchie'.</span><span class="sxs-lookup"><span data-stu-id="9e10f-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="9e10f-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9e10f-120">Click New.</span></span>
12. <span data-ttu-id="9e10f-121">Typ een waarde in het veld Naam knooppunt.</span><span class="sxs-lookup"><span data-stu-id="9e10f-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="9e10f-122">Voer Variabele kosten in.</span><span class="sxs-lookup"><span data-stu-id="9e10f-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="9e10f-123">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9e10f-123">Click Save.</span></span>
14. <span data-ttu-id="9e10f-124">Selecteer in de structuur 'Kostengedraghiërarchie\Vaste kosten'.</span><span class="sxs-lookup"><span data-stu-id="9e10f-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="9e10f-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9e10f-125">Click New.</span></span>
16. <span data-ttu-id="9e10f-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9e10f-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="9e10f-127">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="9e10f-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-128">Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="9e10f-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="9e10f-129">Typ of selecteer een waarde in het veld Tot dimensielid.</span><span class="sxs-lookup"><span data-stu-id="9e10f-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-130">Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="9e10f-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="9e10f-131">Selecteer in de structuur 'Kostengedraghiërarchie\Variabele kosten'.</span><span class="sxs-lookup"><span data-stu-id="9e10f-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="9e10f-132">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9e10f-132">Click New.</span></span>
21. <span data-ttu-id="9e10f-133">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9e10f-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="9e10f-134">Typ of selecteer een waarde in het veld Van dimensielid.</span><span class="sxs-lookup"><span data-stu-id="9e10f-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-135">Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="9e10f-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="9e10f-136">Typ of selecteer een waarde in het veld Tot dimensielid.</span><span class="sxs-lookup"><span data-stu-id="9e10f-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-137">Het bereik van dimensieleden kan gaten bevatten, maar de leden kunnen niet overlappen.</span><span class="sxs-lookup"><span data-stu-id="9e10f-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="9e10f-138">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9e10f-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="9e10f-139">Het beleid en regels maken</span><span class="sxs-lookup"><span data-stu-id="9e10f-139">Create the policy and rules</span></span>
1. <span data-ttu-id="9e10f-140">Ga naar Kostprijsboekhouding > Beleid > Kostengedragbeleidslijnen.</span><span class="sxs-lookup"><span data-stu-id="9e10f-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="9e10f-141">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9e10f-141">Click New.</span></span>
3. <span data-ttu-id="9e10f-142">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="9e10f-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="9e10f-143">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="9e10f-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-144">Selecteer de beleidshiërarchie die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e10f-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="9e10f-145">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="9e10f-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-146">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="9e10f-146">Select Organization.</span></span>  
6. <span data-ttu-id="9e10f-147">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9e10f-147">Click Save.</span></span>
7. <span data-ttu-id="9e10f-148">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9e10f-148">Click New.</span></span>
8. <span data-ttu-id="9e10f-149">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9e10f-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="9e10f-150">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenelement.</span><span class="sxs-lookup"><span data-stu-id="9e10f-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-151">Vouw de hiërarchie uit om Variabele kosten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="9e10f-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="9e10f-152">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="9e10f-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="9e10f-153">Standaard is het variabele percentage 100 procent.</span><span class="sxs-lookup"><span data-stu-id="9e10f-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="9e10f-154">Klik op Beleidstoewijzingen voor kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="9e10f-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="9e10f-155">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="9e10f-155">Click New.</span></span>
13. <span data-ttu-id="9e10f-156">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="9e10f-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="9e10f-157">Typ een datum in het veld Geldig vanaf boekhouddatum.</span><span class="sxs-lookup"><span data-stu-id="9e10f-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="9e10f-158">De regels zijn datumregels en een regel kan vervallen door een gebruiker of door het systeem, als een nieuwere versie wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="9e10f-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="9e10f-159">Typ of selecteer een waarde in het veld Kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="9e10f-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="9e10f-160">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="9e10f-160">Click Save.</span></span>

