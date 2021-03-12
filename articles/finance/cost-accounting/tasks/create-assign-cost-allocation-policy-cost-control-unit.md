---
title: Een kostentoewijzingsbeleid maken en toewijzen aan een kostenbeheereenheid
description: Gebruik deze procedure om een kostentoewijzingsbeleid en de corresponderende regels te maken en toe te wijzen aan een kostenbeheereenheid.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006310d07dfa5b75941ca248736800bbb9e8e7b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969323"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="ed59d-103">Een kostentoewijzingsbeleid maken en toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="ed59d-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed59d-104">Gebruik deze procedure om een kostentoewijzingsbeleid en de corresponderende regels te maken en toe te wijzen aan een kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="ed59d-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="ed59d-105">Deze registratie gebruikt het USP2-demogegevensbedrijf.</span><span class="sxs-lookup"><span data-stu-id="ed59d-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="ed59d-106">Een beleid maken</span><span class="sxs-lookup"><span data-stu-id="ed59d-106">Create a policy</span></span>
1. <span data-ttu-id="ed59d-107">Ga naar Kostprijsboekhouding > Beleid > Beleidslijnen voor kostprijstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="ed59d-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="ed59d-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ed59d-108">Click New.</span></span>
3. <span data-ttu-id="ed59d-109">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="ed59d-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="ed59d-110">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="ed59d-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="ed59d-111">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="ed59d-111">Select Organization.</span></span>  
5. <span data-ttu-id="ed59d-112">Typ of selecteer een waarde in het veld Statistische dimensie.</span><span class="sxs-lookup"><span data-stu-id="ed59d-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="ed59d-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ed59d-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="ed59d-114">Toewijzingsregels maken</span><span class="sxs-lookup"><span data-stu-id="ed59d-114">Create allocation rules</span></span>
1. <span data-ttu-id="ed59d-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ed59d-115">Click New.</span></span>
2. <span data-ttu-id="ed59d-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ed59d-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ed59d-117">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="ed59d-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="ed59d-118">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="ed59d-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="ed59d-119">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="ed59d-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="ed59d-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ed59d-120">Click New.</span></span>
7. <span data-ttu-id="ed59d-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ed59d-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ed59d-122">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="ed59d-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="ed59d-123">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="ed59d-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="ed59d-124">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="ed59d-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="ed59d-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ed59d-125">Click New.</span></span>
12. <span data-ttu-id="ed59d-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ed59d-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="ed59d-127">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="ed59d-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="ed59d-128">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="ed59d-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="ed59d-129">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="ed59d-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="ed59d-130">Ga door totdat u alle regels hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ed59d-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="ed59d-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ed59d-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="ed59d-132">Het beleid toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="ed59d-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="ed59d-133">Klik op Beleidstoewijzingen voor kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="ed59d-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="ed59d-134">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ed59d-134">Click New.</span></span>
3. <span data-ttu-id="ed59d-135">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ed59d-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ed59d-136">Typ een datum in het veld Geldig vanaf boekhouddatum.</span><span class="sxs-lookup"><span data-stu-id="ed59d-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="ed59d-137">De regels zijn datumregels.</span><span class="sxs-lookup"><span data-stu-id="ed59d-137">The rules are date-effective.</span></span> <span data-ttu-id="ed59d-138">Een gebruiker of het systeem kan de regels laten vervallen wanneer een nieuwere versie wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ed59d-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="ed59d-139">Typ of selecteer een waarde in het veld Kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="ed59d-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="ed59d-140">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ed59d-140">Click Save.</span></span>

