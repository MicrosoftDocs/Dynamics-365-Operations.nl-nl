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
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f0422a9aaf95184b556293bf6ebcaf4dcfb5b59
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841388"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="2c745-103">Een kostentoewijzingsbeleid maken en toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="2c745-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c745-104">Gebruik deze procedure om een kostentoewijzingsbeleid en de corresponderende regels te maken en toe te wijzen aan een kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="2c745-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="2c745-105">Deze registratie gebruikt het USP2-demogegevensbedrijf.</span><span class="sxs-lookup"><span data-stu-id="2c745-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="2c745-106">Een beleid maken</span><span class="sxs-lookup"><span data-stu-id="2c745-106">Create a policy</span></span>
1. <span data-ttu-id="2c745-107">Ga naar Kostprijsboekhouding > Beleid > Beleidslijnen voor kostprijstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="2c745-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="2c745-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2c745-108">Click New.</span></span>
3. <span data-ttu-id="2c745-109">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="2c745-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="2c745-110">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="2c745-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="2c745-111">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="2c745-111">Select Organization.</span></span>  
5. <span data-ttu-id="2c745-112">Typ of selecteer een waarde in het veld Statistische dimensie.</span><span class="sxs-lookup"><span data-stu-id="2c745-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="2c745-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="2c745-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="2c745-114">Toewijzingsregels maken</span><span class="sxs-lookup"><span data-stu-id="2c745-114">Create allocation rules</span></span>
1. <span data-ttu-id="2c745-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2c745-115">Click New.</span></span>
2. <span data-ttu-id="2c745-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2c745-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2c745-117">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="2c745-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="2c745-118">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="2c745-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="2c745-119">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="2c745-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="2c745-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2c745-120">Click New.</span></span>
7. <span data-ttu-id="2c745-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2c745-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="2c745-122">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="2c745-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="2c745-123">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="2c745-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="2c745-124">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="2c745-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="2c745-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2c745-125">Click New.</span></span>
12. <span data-ttu-id="2c745-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2c745-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="2c745-127">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="2c745-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="2c745-128">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="2c745-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="2c745-129">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="2c745-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="2c745-130">Ga door totdat u alle regels hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2c745-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="2c745-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="2c745-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="2c745-132">Het beleid toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="2c745-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="2c745-133">Klik op Beleidstoewijzingen voor kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="2c745-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="2c745-134">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2c745-134">Click New.</span></span>
3. <span data-ttu-id="2c745-135">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2c745-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2c745-136">Typ een datum in het veld Geldig vanaf boekhouddatum.</span><span class="sxs-lookup"><span data-stu-id="2c745-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="2c745-137">De regels zijn datumregels.</span><span class="sxs-lookup"><span data-stu-id="2c745-137">The rules are date-effective.</span></span> <span data-ttu-id="2c745-138">Een gebruiker of het systeem kan de regels laten vervallen wanneer een nieuwere versie wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2c745-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="2c745-139">Typ of selecteer een waarde in het veld Kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="2c745-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="2c745-140">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="2c745-140">Click Save.</span></span>

