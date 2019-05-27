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
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92f41eb99b84bbc596e79b413971f9d92f2555b6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543905"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="3e342-103">Een kostentoewijzingsbeleid maken en toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="3e342-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e342-104">Gebruik deze procedure om een kostentoewijzingsbeleid en de corresponderende regels te maken en toe te wijzen aan een kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="3e342-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="3e342-105">Deze registratie gebruikt het USP2-demogegevensbedrijf.</span><span class="sxs-lookup"><span data-stu-id="3e342-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="3e342-106">Een beleid maken</span><span class="sxs-lookup"><span data-stu-id="3e342-106">Create a policy</span></span>
1. <span data-ttu-id="3e342-107">Ga naar Kostprijsboekhouding > Beleid > Beleidslijnen voor kostprijstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="3e342-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="3e342-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3e342-108">Click New.</span></span>
3. <span data-ttu-id="3e342-109">Typ een waarde in het veld Beleid.</span><span class="sxs-lookup"><span data-stu-id="3e342-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="3e342-110">Typ of selecteer een waarde in het veld Dimensiehiërarchie van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="3e342-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="3e342-111">Selecteer Organisatie.</span><span class="sxs-lookup"><span data-stu-id="3e342-111">Select Organization.</span></span>  
5. <span data-ttu-id="3e342-112">Typ of selecteer een waarde in het veld Statistische dimensie.</span><span class="sxs-lookup"><span data-stu-id="3e342-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="3e342-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3e342-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="3e342-114">Toewijzingsregels maken</span><span class="sxs-lookup"><span data-stu-id="3e342-114">Create allocation rules</span></span>
1. <span data-ttu-id="3e342-115">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3e342-115">Click New.</span></span>
2. <span data-ttu-id="3e342-116">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="3e342-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3e342-117">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="3e342-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="3e342-118">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="3e342-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="3e342-119">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="3e342-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="3e342-120">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3e342-120">Click New.</span></span>
7. <span data-ttu-id="3e342-121">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="3e342-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="3e342-122">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="3e342-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="3e342-123">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="3e342-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="3e342-124">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="3e342-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="3e342-125">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3e342-125">Click New.</span></span>
12. <span data-ttu-id="3e342-126">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="3e342-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3e342-127">Typ of selecteer een waarde in het veld Dimensiehiërarchieknooppunt van een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="3e342-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="3e342-128">Selecteer 'Totaal' in het veld Kostengedrag.</span><span class="sxs-lookup"><span data-stu-id="3e342-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="3e342-129">Typ of selecteer een waarde in het veld Toewijzingsgrondslag.</span><span class="sxs-lookup"><span data-stu-id="3e342-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="3e342-130">Ga door totdat u alle regels hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3e342-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="3e342-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3e342-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="3e342-132">Het beleid toewijzen aan een kostenbeheereenheid</span><span class="sxs-lookup"><span data-stu-id="3e342-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="3e342-133">Klik op Beleidstoewijzingen voor kostenbeheereenheid.</span><span class="sxs-lookup"><span data-stu-id="3e342-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="3e342-134">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="3e342-134">Click New.</span></span>
3. <span data-ttu-id="3e342-135">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="3e342-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3e342-136">Typ een datum in het veld Geldig vanaf boekhouddatum.</span><span class="sxs-lookup"><span data-stu-id="3e342-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="3e342-137">De regels zijn datumregels.</span><span class="sxs-lookup"><span data-stu-id="3e342-137">The rules are date-effective.</span></span> <span data-ttu-id="3e342-138">Een gebruiker of het systeem kan de regels laten vervallen wanneer een nieuwere versie wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3e342-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="3e342-139">Typ of selecteer een waarde in het veld Kostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="3e342-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="3e342-140">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="3e342-140">Click Save.</span></span>

