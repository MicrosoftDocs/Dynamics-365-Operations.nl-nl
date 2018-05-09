--- 
title: Lean tracering van de behoefte vanuit verkooporders
description: Deze procedure is gericht op het valideren van de behoeftetraceringsstructuur van een verkoopregel waarin het artikel met kanbans wordt geproduceerd.
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dbab5ade75aa8999f7e91c5d27f896242f6c7604
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="d7a98-103">Lean tracering van de behoefte vanuit verkooporders</span><span class="sxs-lookup"><span data-stu-id="d7a98-103">Lean pegging from sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7a98-104">Deze procedure is gericht op het valideren van de behoeftetraceringsstructuur van een verkoopregel waarin het artikel met kanbans wordt geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="d7a98-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="d7a98-105">Nadat de behoeftetraceringsstructuur is gevalideerd, zijn alle kanbantaken gepland.</span><span class="sxs-lookup"><span data-stu-id="d7a98-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="d7a98-106">Dit is handig voor orderscenario's waarbij de ordermedewerker ervoor moet zorgen dat de productie direct kan starten.</span><span class="sxs-lookup"><span data-stu-id="d7a98-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="d7a98-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="d7a98-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d7a98-108">Deze procedure is bedoeld voor de gevorderde ordermedewerker die in lean bedrijf werkt.</span><span class="sxs-lookup"><span data-stu-id="d7a98-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="d7a98-109">Een verkooporder maken voor een door kanban gestuurd artikel</span><span class="sxs-lookup"><span data-stu-id="d7a98-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="d7a98-110">Ga naar Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="d7a98-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="d7a98-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d7a98-111">Click New.</span></span>
3. <span data-ttu-id="d7a98-112">Typ of selecteer een waarde in het veld Klantrekening.</span><span class="sxs-lookup"><span data-stu-id="d7a98-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="d7a98-113">Gebruik US-001.</span><span class="sxs-lookup"><span data-stu-id="d7a98-113">Use US-001.</span></span>  
4. <span data-ttu-id="d7a98-114">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d7a98-114">Click OK.</span></span>
5. <span data-ttu-id="d7a98-115">Typ in het veld Artikelnummer de waarde 'L0001'.</span><span class="sxs-lookup"><span data-stu-id="d7a98-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="d7a98-116">Stel Hoeveelheid in op '30'.</span><span class="sxs-lookup"><span data-stu-id="d7a98-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="d7a98-117">Het is belangrijk dat de hoeveelheid hoger is dan 24 om de gebeurteniskanbanregel te activeren.</span><span class="sxs-lookup"><span data-stu-id="d7a98-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="d7a98-118">Een behoeftetraceringsstructuur openen</span><span class="sxs-lookup"><span data-stu-id="d7a98-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="d7a98-119">Klik op Product en voorraad.</span><span class="sxs-lookup"><span data-stu-id="d7a98-119">Click Product and supply.</span></span>
2. <span data-ttu-id="d7a98-120">Klik op Behoeftetraceringsstructuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="d7a98-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="d7a98-121">De behoeftetraceringsstructuur toont alle niveaus van de tracering van de behoefte die nodig is voor de verkooporderregel.</span><span class="sxs-lookup"><span data-stu-id="d7a98-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="d7a98-122">In dit geval zijn er twee niveaus van kanbans en alle vereiste onderdelen.</span><span class="sxs-lookup"><span data-stu-id="d7a98-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="d7a98-123">De behoeftetraceringsstructuur plannen</span><span class="sxs-lookup"><span data-stu-id="d7a98-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="d7a98-124">Selecteer in de structuur 'Verkoopregel 000832\Kanban 000558'.</span><span class="sxs-lookup"><span data-stu-id="d7a98-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="d7a98-125">Vouw de sectie Kanbantaken uit.</span><span class="sxs-lookup"><span data-stu-id="d7a98-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="d7a98-126">De taakstatus voor de kanbantaak is Niet gepland.</span><span class="sxs-lookup"><span data-stu-id="d7a98-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="d7a98-127">Klik op Volledige behoeftetraceringsstructuur plannen.</span><span class="sxs-lookup"><span data-stu-id="d7a98-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="d7a98-128">Op die manier worden alle kanbantaken in de behoeftetraceringsstructuur gepland, wat de taakstatus wijzigt van Niet gepland in Gepland.</span><span class="sxs-lookup"><span data-stu-id="d7a98-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="d7a98-129">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="d7a98-129">Refresh the page.</span></span>
    * <span data-ttu-id="d7a98-130">De kanbantaakstatus is gewijzigd van Niet gepland in Gepland.</span><span class="sxs-lookup"><span data-stu-id="d7a98-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="d7a98-131">Selecteer in de structuur 'Verkoopregel 000832\Kanban 000558\Probleem voor L0001\Kanban 000559'.</span><span class="sxs-lookup"><span data-stu-id="d7a98-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="d7a98-132">De taak voor de tweede kanban is ook gepland, omdat de volledige behoeftetraceringsstructuur is gepland.</span><span class="sxs-lookup"><span data-stu-id="d7a98-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="d7a98-133">De kanbantaakstatus is gewijzigd van Niet gepland in Gepland.</span><span class="sxs-lookup"><span data-stu-id="d7a98-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  


