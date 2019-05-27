---
title: Een intercompany-plan maken
description: Deze procedure laat zien hoe u een intercompany-plan maakt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555972"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="2692f-103">Een intercompany-plan maken</span><span class="sxs-lookup"><span data-stu-id="2692f-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2692f-104">Deze procedure laat zien hoe u een intercompany-plan maakt.</span><span class="sxs-lookup"><span data-stu-id="2692f-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="2692f-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="2692f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="2692f-106">Intercompany-planningsgroep instellen</span><span class="sxs-lookup"><span data-stu-id="2692f-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="2692f-107">Ga naar Intercompany-planningsgroepen.</span><span class="sxs-lookup"><span data-stu-id="2692f-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="2692f-108">Hoofdplanning > Instellingen > Intercompany-planningsgroepen</span><span class="sxs-lookup"><span data-stu-id="2692f-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="2692f-109">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="2692f-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2692f-110">Filter bijvoorbeeld op het Veld Naam met een waarde van "10".</span><span class="sxs-lookup"><span data-stu-id="2692f-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="2692f-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2692f-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2692f-112">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="2692f-112">Click Delete.</span></span>
    * <span data-ttu-id="2692f-113">Deze stap is nodig om het maken van de intercompany-planning in te korten.</span><span class="sxs-lookup"><span data-stu-id="2692f-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="2692f-114">Intercompany-planning voert hoofdplanning uit in alle bedrijven in een planningsgroep, te beginnen met de laagste schemareeks.</span><span class="sxs-lookup"><span data-stu-id="2692f-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="2692f-115">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="2692f-115">Click Yes.</span></span>
6. <span data-ttu-id="2692f-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2692f-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="2692f-117">Een intercompany-plan maken</span><span class="sxs-lookup"><span data-stu-id="2692f-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="2692f-118">Klik op Intercompany-hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="2692f-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="2692f-119">Dit is in het Hoofdplanningwerkgebied.</span><span class="sxs-lookup"><span data-stu-id="2692f-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="2692f-120">Klik in het veld Intercompany-planningsgroep op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2692f-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="2692f-121">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2692f-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2692f-122">Selecteer Intercompany-planningsgroep 10.</span><span class="sxs-lookup"><span data-stu-id="2692f-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="2692f-123">Typ 2 in het veld Aantal intercompany-planningsherhalingen.</span><span class="sxs-lookup"><span data-stu-id="2692f-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="2692f-124">Intercompany-planningsgroep 10 heeft twee leden.</span><span class="sxs-lookup"><span data-stu-id="2692f-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="2692f-125">Om de vertragingen van het bronbedrijf (USMF) door te voeren naar het klantbedrijf (DEMF), moet u intercompany in beide bedrijven twee keer uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="2692f-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="2692f-126">De eerste herhaling voert de vraag door en geeft de vertragingen in het bronbedrijf (USMF) aan.</span><span class="sxs-lookup"><span data-stu-id="2692f-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="2692f-127">Bij de tweede herhaling worden de vertragingen van de USMF naar DEMF doorgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2692f-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="2692f-128">Selecteer een optie in het veld Eerste iteratie.</span><span class="sxs-lookup"><span data-stu-id="2692f-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="2692f-129">Selecteer Opnieuw genereren in het veld Eerste iteratie.</span><span class="sxs-lookup"><span data-stu-id="2692f-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="2692f-130">Selecteer Opnieuw genereren in het veld Volgende iteraties.</span><span class="sxs-lookup"><span data-stu-id="2692f-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="2692f-131">Voer een getal in het veld Aantal threads in.</span><span class="sxs-lookup"><span data-stu-id="2692f-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="2692f-132">Dit geeft het aantal parallelle threads aan dat voor planning wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2692f-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="2692f-133">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2692f-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="2692f-134">Het resultaat van het plan weergeven</span><span class="sxs-lookup"><span data-stu-id="2692f-134">View the result of the plan</span></span>
1. <span data-ttu-id="2692f-135">Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="2692f-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="2692f-136">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2692f-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2692f-137">Klik op de koppeling voor StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="2692f-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="2692f-138">U moet in het bedrijf USMF zijn.</span><span class="sxs-lookup"><span data-stu-id="2692f-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="2692f-139">Klik op Geplande orders.</span><span class="sxs-lookup"><span data-stu-id="2692f-139">Click Planned orders.</span></span>

