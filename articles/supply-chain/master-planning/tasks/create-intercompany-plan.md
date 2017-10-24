--- 
title: Een intercompany-plan maken
description: Deze procedure laat zien hoe u een intercompany-plan maakt.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="60da2-103">Een intercompany-plan maken</span><span class="sxs-lookup"><span data-stu-id="60da2-103">Create an intercompany plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60da2-104">Deze procedure laat zien hoe u een intercompany-plan maakt.</span><span class="sxs-lookup"><span data-stu-id="60da2-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="60da2-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="60da2-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="60da2-106">Intercompany-planningsgroep instellen</span><span class="sxs-lookup"><span data-stu-id="60da2-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="60da2-107">Ga naar Intercompany-planningsgroepen.</span><span class="sxs-lookup"><span data-stu-id="60da2-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="60da2-108">Hoofdplanning > Instellingen > Intercompany-planningsgroepen</span><span class="sxs-lookup"><span data-stu-id="60da2-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="60da2-109">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="60da2-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="60da2-110">Filter bijvoorbeeld op het Veld Naam met een waarde van "10".</span><span class="sxs-lookup"><span data-stu-id="60da2-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="60da2-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="60da2-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="60da2-112">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="60da2-112">Click Delete.</span></span>
    * <span data-ttu-id="60da2-113">Deze stap is nodig om het maken van de intercompany-planning in te korten.</span><span class="sxs-lookup"><span data-stu-id="60da2-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="60da2-114">Intercompany-planning voert hoofdplanning uit in alle bedrijven in een planningsgroep, te beginnen met de laagste schemareeks.</span><span class="sxs-lookup"><span data-stu-id="60da2-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="60da2-115">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="60da2-115">Click Yes.</span></span>
6. <span data-ttu-id="60da2-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="60da2-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="60da2-117">Een intercompany-plan maken</span><span class="sxs-lookup"><span data-stu-id="60da2-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="60da2-118">Klik op Intercompany-hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="60da2-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="60da2-119">Dit is in het Hoofdplanningwerkgebied.</span><span class="sxs-lookup"><span data-stu-id="60da2-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="60da2-120">Klik in het veld Intercompany-planningsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="60da2-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="60da2-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="60da2-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="60da2-122">Selecteer Intercompany-planningsgroep 10.</span><span class="sxs-lookup"><span data-stu-id="60da2-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="60da2-123">Typ 2 in het veld Aantal intercompany-planningsherhalingen.</span><span class="sxs-lookup"><span data-stu-id="60da2-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="60da2-124">Intercompany-planningsgroep 10 heeft twee leden.</span><span class="sxs-lookup"><span data-stu-id="60da2-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="60da2-125">Om de vertragingen van het bronbedrijf (USMF) door te voeren naar het klantbedrijf (DEMF), moet u intercompany in beide bedrijven twee keer uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="60da2-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="60da2-126">De eerste herhaling voert de vraag door en geeft de vertragingen in het bronbedrijf (USMF) aan.</span><span class="sxs-lookup"><span data-stu-id="60da2-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="60da2-127">Bij de tweede herhaling worden de vertragingen van de USMF naar DEMF doorgevoerd.</span><span class="sxs-lookup"><span data-stu-id="60da2-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="60da2-128">Selecteer een optie in het veld Eerste iteratie.</span><span class="sxs-lookup"><span data-stu-id="60da2-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="60da2-129">Selecteer Opnieuw genereren in het veld Eerste iteratie.</span><span class="sxs-lookup"><span data-stu-id="60da2-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="60da2-130">Selecteer Opnieuw genereren in het veld Volgende iteraties.</span><span class="sxs-lookup"><span data-stu-id="60da2-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="60da2-131">Voer een getal in het veld Aantal threads in.</span><span class="sxs-lookup"><span data-stu-id="60da2-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="60da2-132">Dit geeft het aantal parallelle threads aan dat voor planning wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="60da2-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="60da2-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="60da2-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="60da2-134">Het resultaat van het plan weergeven</span><span class="sxs-lookup"><span data-stu-id="60da2-134">View the result of the plan</span></span>
1. <span data-ttu-id="60da2-135">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="60da2-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="60da2-136">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="60da2-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="60da2-137">Klik op de koppeling voor StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="60da2-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="60da2-138">U moet in het bedrijf USMF zijn.</span><span class="sxs-lookup"><span data-stu-id="60da2-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="60da2-139">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="60da2-139">Click Planned orders.</span></span>


