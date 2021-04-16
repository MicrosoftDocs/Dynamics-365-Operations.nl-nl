---
title: Kanbanregels wijzigen voor een procestaak
description: Deze procedure is gericht op het wijzigen van de gebruikte kanbanregel voor een bepaalde kanban.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bdbbbf8a8b3d1596c251224cba996c0631050c4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829301"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="a6e29-103">Kanbanregels wijzigen voor een procestaak</span><span class="sxs-lookup"><span data-stu-id="a6e29-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6e29-104">Deze procedure is gericht op het wijzigen van de gebruikte kanbanregel voor een bepaalde kanban.</span><span class="sxs-lookup"><span data-stu-id="a6e29-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="a6e29-105">Dit is handig om de belasting van resources te effenen of in het geval van opsplitsing.</span><span class="sxs-lookup"><span data-stu-id="a6e29-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="a6e29-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="a6e29-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a6e29-107">Deze procedure is bedoeld voor de planner, die in een lean manufacturingbedrijf werkt en verantwoordelijk is voor de waardestroom.</span><span class="sxs-lookup"><span data-stu-id="a6e29-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="a6e29-108">Kanbanregel kopiëren</span><span class="sxs-lookup"><span data-stu-id="a6e29-108">Copy kanban rule</span></span>
1. <span data-ttu-id="a6e29-109">Ga naar Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="a6e29-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="a6e29-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a6e29-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a6e29-111">Selecteer gebeurteniskanbanregel 000022 voor L0001.</span><span class="sxs-lookup"><span data-stu-id="a6e29-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="a6e29-112">Klik op Dubbele kanbanregel.</span><span class="sxs-lookup"><span data-stu-id="a6e29-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="a6e29-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a6e29-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="a6e29-114">Kanbanregel wijzigen</span><span class="sxs-lookup"><span data-stu-id="a6e29-114">Change kanban rule</span></span>
1. <span data-ttu-id="a6e29-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a6e29-115">Close the page.</span></span>
2. <span data-ttu-id="a6e29-116">Ga naar Kanbantaakplanning.</span><span class="sxs-lookup"><span data-stu-id="a6e29-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="a6e29-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a6e29-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a6e29-118">Selecteer regel met kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="a6e29-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="a6e29-119">KIik op Alternatieve kanbanregel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a6e29-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="a6e29-120">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="a6e29-120">Click Next.</span></span>
6. <span data-ttu-id="a6e29-121">Typ of selecteer een waarde in het veld Kanbanregel.</span><span class="sxs-lookup"><span data-stu-id="a6e29-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="a6e29-122">Selecteer de kanbanregel die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a6e29-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="a6e29-123">Dit is de kanbanregel met het hoogste cijfer.</span><span class="sxs-lookup"><span data-stu-id="a6e29-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="a6e29-124">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="a6e29-124">Click Finish.</span></span>
    * <span data-ttu-id="a6e29-125">Nu gebruikt de kanbantaak een andere kanbanregel.</span><span class="sxs-lookup"><span data-stu-id="a6e29-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="a6e29-126">Dit kan nuttig zijn om de belasting van de werkcellen te effenen.</span><span class="sxs-lookup"><span data-stu-id="a6e29-126">This can be useful to level load work cells.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]