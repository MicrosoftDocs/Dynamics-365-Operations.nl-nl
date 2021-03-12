---
title: Een kanbanregel maken voor meerdere activiteiten
description: Deze procedure laat zien hoe u een kanbanregel kunt maken die meerdere activiteiten van een productiestroom bevat.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c25d47a78d1cc91ee2625ef628d7b9ba345b097
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977908"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="ab245-103">Een kanbanregel maken voor meerdere activiteiten</span><span class="sxs-lookup"><span data-stu-id="ab245-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab245-104">Deze procedure laat zien hoe u een kanbanregel kunt maken die meerdere activiteiten van een productiestroom bevat.</span><span class="sxs-lookup"><span data-stu-id="ab245-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="ab245-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="ab245-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="ab245-106">Deze taak is bedoeld voor de procestechnicus of de waardestroombeheerder bij het voorbereiden van de productie van een nieuw of gewijzigd product in een lean-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ab245-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="ab245-107">Een nieuwe kanbanregel maken</span><span class="sxs-lookup"><span data-stu-id="ab245-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="ab245-108">Ga naar Productgegevensbeheer > Lean manufacturing > Kanbanregels.</span><span class="sxs-lookup"><span data-stu-id="ab245-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="ab245-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ab245-109">Click New.</span></span>
3. <span data-ttu-id="ab245-110">Selecteer 'Gepland' in het veld Aanvullingsstrategie.</span><span class="sxs-lookup"><span data-stu-id="ab245-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="ab245-111">Typ of selecteer een waarde in het veld Eerste planactiviteit.</span><span class="sxs-lookup"><span data-stu-id="ab245-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ab245-112">Selecteer SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="ab245-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="ab245-113">Schakel het selectievakje Meerdere activiteiten in.</span><span class="sxs-lookup"><span data-stu-id="ab245-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="ab245-114">Het doel is meer dan één activiteit in de kanbanregel op te nemen.</span><span class="sxs-lookup"><span data-stu-id="ab245-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="ab245-115">U kiest een pad in de productiestroom wanneer u de laatste planactiviteit selecteert.</span><span class="sxs-lookup"><span data-stu-id="ab245-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="ab245-116">Typ of selecteer een waarde in het veld Laatste planactiviteit.</span><span class="sxs-lookup"><span data-stu-id="ab245-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ab245-117">Selecteer SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="ab245-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="ab245-118">Nadat u de waarde hebt geselecteerd, wordt automatisch een pagina geopend.</span><span class="sxs-lookup"><span data-stu-id="ab245-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="ab245-119">Selecteer de kanbanwerkstroom SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="ab245-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="ab245-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ab245-120">Click OK.</span></span>  
7. <span data-ttu-id="ab245-121">Vouw de sectie Details uit.</span><span class="sxs-lookup"><span data-stu-id="ab245-121">Expand the Details section.</span></span>
8. <span data-ttu-id="ab245-122">Typ of selecteer een waarde in het veld Product.</span><span class="sxs-lookup"><span data-stu-id="ab245-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="ab245-123">Selecteer artikel L0006.</span><span class="sxs-lookup"><span data-stu-id="ab245-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="ab245-124">Kanban maken en taken weergeven</span><span class="sxs-lookup"><span data-stu-id="ab245-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="ab245-125">Vouw de sectie Kanbans uit.</span><span class="sxs-lookup"><span data-stu-id="ab245-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="ab245-126">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="ab245-126">Click Add.</span></span>
3. <span data-ttu-id="ab245-127">Typ '1' in het veld Aantal nieuwe kanbans.</span><span class="sxs-lookup"><span data-stu-id="ab245-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="ab245-128">Hierdoor wordt één kanban gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ab245-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="ab245-129">Stel Producthoeveelheid in op "3".</span><span class="sxs-lookup"><span data-stu-id="ab245-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="ab245-130">Door de kanban worden 3 producten verwerkt.</span><span class="sxs-lookup"><span data-stu-id="ab245-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="ab245-131">Typ een datum en tijd in het veld Vervaldatum/-tijd.</span><span class="sxs-lookup"><span data-stu-id="ab245-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="ab245-132">U kunt Vandaag invoeren.</span><span class="sxs-lookup"><span data-stu-id="ab245-132">You can enter Today.</span></span>  
6. <span data-ttu-id="ab245-133">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="ab245-133">Click Create.</span></span>
7. <span data-ttu-id="ab245-134">Klik op Details.</span><span class="sxs-lookup"><span data-stu-id="ab245-134">Click Details.</span></span>
    * <span data-ttu-id="ab245-135">Merk op dat de kanban twee procestaken van de productiestroom bevat.</span><span class="sxs-lookup"><span data-stu-id="ab245-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="ab245-136">De eerste is SpeakerAssemblyAndPolish, en de tweede is SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="ab245-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="ab245-137">Dit is de laatste stap.</span><span class="sxs-lookup"><span data-stu-id="ab245-137">This is the last step!</span></span>  

