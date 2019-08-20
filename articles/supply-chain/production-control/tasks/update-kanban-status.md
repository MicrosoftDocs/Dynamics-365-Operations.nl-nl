---
title: Kanbanstatus bijwerken
description: Wanneer een kanban per ongeluk is geleegd of als een ontvangen kanban moet worden leeggemaakt, moet u de kanbanstatus bijwerken.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97b6eea4e93967dbe1eea5eac9fe3fbf6b336a49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838458"
---
# <a name="update-kanban-status"></a><span data-ttu-id="952f3-103">Kanbanstatus bijwerken</span><span class="sxs-lookup"><span data-stu-id="952f3-103">Update kanban status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="952f3-104">Wanneer een kanban per ongeluk is geleegd of als een ontvangen kanban moet worden leeggemaakt, moet u de kanbanstatus bijwerken.</span><span class="sxs-lookup"><span data-stu-id="952f3-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="952f3-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="952f3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="952f3-106">Deze procedure is bedoeld voor de winkelchef.</span><span class="sxs-lookup"><span data-stu-id="952f3-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="952f3-107">Zoek de kanban.</span><span class="sxs-lookup"><span data-stu-id="952f3-107">Find the kanban.</span></span>
1. <span data-ttu-id="952f3-108">Ga naar Productiebeheer > Kanban > Kanbans.</span><span class="sxs-lookup"><span data-stu-id="952f3-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="952f3-109">Open de kolomfilter Status materiaalverwerkingseenheid.</span><span class="sxs-lookup"><span data-stu-id="952f3-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="952f3-110">Klik op Wissen.</span><span class="sxs-lookup"><span data-stu-id="952f3-110">Click Clear.</span></span>
    * <span data-ttu-id="952f3-111">Hiermee worden de filters opnieuw ingesteld.</span><span class="sxs-lookup"><span data-stu-id="952f3-111">This resets the filters.</span></span>  
4. <span data-ttu-id="952f3-112">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="952f3-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="952f3-113">Filter bijvoorbeeld op het veld Kaartnummer met een waarde van '000149'.</span><span class="sxs-lookup"><span data-stu-id="952f3-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="952f3-114">Status Geleegd in Ontvangen wijzigen</span><span class="sxs-lookup"><span data-stu-id="952f3-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="952f3-115">Klik op Omgekeerde lege materiaalverwerkingseenheid.</span><span class="sxs-lookup"><span data-stu-id="952f3-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="952f3-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="952f3-116">Click OK.</span></span>
    * <span data-ttu-id="952f3-117">De status van de materiaalverwerkingseenheid is Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="952f3-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="952f3-118">Status Ontvangen in Geleegd wijzigen</span><span class="sxs-lookup"><span data-stu-id="952f3-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="952f3-119">Klik op Lege Kanban.</span><span class="sxs-lookup"><span data-stu-id="952f3-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="952f3-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="952f3-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="952f3-121">De status van de materiaalverwerkingseenheid is Geleegd.</span><span class="sxs-lookup"><span data-stu-id="952f3-121">Notice that the Handling unit status is Emptied.</span></span>  

