---
title: Een intercompany-plan maken
description: Deze procedure laat zien hoe u een intercompany-plan maakt.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978268"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="b59d3-103">Een intercompany-plan maken</span><span class="sxs-lookup"><span data-stu-id="b59d3-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b59d3-104">Deze procedure laat zien hoe u een intercompany-plan maakt.</span><span class="sxs-lookup"><span data-stu-id="b59d3-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="b59d3-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="b59d3-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="b59d3-106">Intercompany-planningsgroep instellen</span><span class="sxs-lookup"><span data-stu-id="b59d3-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="b59d3-107">Ga in het **navigatievenster** naar **Modules > Hoofdplanning > Instellingen > Intercompany-planningsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="b59d3-108">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="b59d3-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b59d3-109">Filter bijvoorbeeld op het Veld Naam met een waarde van "10".</span><span class="sxs-lookup"><span data-stu-id="b59d3-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="b59d3-110">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b59d3-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b59d3-111">Klik op **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-111">Click **Delete**.</span></span> <span data-ttu-id="b59d3-112">Deze stap is nodig om het maken van de intercompany-planning in te korten.</span><span class="sxs-lookup"><span data-stu-id="b59d3-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="b59d3-113">Intercompany-planning voert hoofdplanning uit in alle bedrijven in een planningsgroep, te beginnen met de laagste schemareeks.</span><span class="sxs-lookup"><span data-stu-id="b59d3-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="b59d3-114">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-114">Click **Yes**.</span></span>
6. <span data-ttu-id="b59d3-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b59d3-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="b59d3-116">Een intercompany-plan maken</span><span class="sxs-lookup"><span data-stu-id="b59d3-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="b59d3-117">Ga in het **navigatievenster** naar **Modules > Hoofdplanning > Werkgebieden > Hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="b59d3-118">Klik op **Intercompany-hoofdplanning**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="b59d3-119">Klik in het veld **Intercompany-planningsgroep** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b59d3-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b59d3-120">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b59d3-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="b59d3-121">Selecteer Intercompany-planningsgroep 10.</span><span class="sxs-lookup"><span data-stu-id="b59d3-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="b59d3-122">Typ 2 in het veld **Aantal intercompany-planningsherhalingen**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="b59d3-123">Intercompany-planningsgroep 10 heeft twee leden.</span><span class="sxs-lookup"><span data-stu-id="b59d3-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="b59d3-124">Om de vertragingen van het bronbedrijf (USMF) door te voeren naar het klantbedrijf (DEMF), moet u intercompany in beide bedrijven twee keer uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b59d3-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="b59d3-125">De eerste herhaling voert de vraag door en geeft de vertragingen in het bronbedrijf (USMF) aan.</span><span class="sxs-lookup"><span data-stu-id="b59d3-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="b59d3-126">Bij de tweede herhaling worden de vertragingen van de USMF naar DEMF doorgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b59d3-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="b59d3-127">Selecteer Opnieuw genereren in het veld **Eerste iteratie**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="b59d3-128">Selecteer Opnieuw genereren in het veld **Volgende iteraties**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="b59d3-129">Voer een getal in het veld **Aantal threads** in.</span><span class="sxs-lookup"><span data-stu-id="b59d3-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="b59d3-130">Dit geeft het aantal parallelle threads aan dat voor planning wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b59d3-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="b59d3-131">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="b59d3-132">Het resultaat van het plan weergeven</span><span class="sxs-lookup"><span data-stu-id="b59d3-132">View the result of the plan</span></span>
1. <span data-ttu-id="b59d3-133">Klik in het veld **Plan** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="b59d3-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="b59d3-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="b59d3-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="b59d3-135">Klik op de koppeling voor StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="b59d3-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="b59d3-136">U moet in het bedrijf USMF zijn.</span><span class="sxs-lookup"><span data-stu-id="b59d3-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="b59d3-137">Klik op **Geplande orders**.</span><span class="sxs-lookup"><span data-stu-id="b59d3-137">Click **Planned orders**.</span></span>

