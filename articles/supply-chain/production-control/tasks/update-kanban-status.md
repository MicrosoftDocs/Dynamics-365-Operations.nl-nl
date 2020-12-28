---
title: Kanbanstatus bijwerken
description: Wanneer een kanban per ongeluk is geleegd of als een ontvangen kanban moet worden leeggemaakt, moet u de kanbanstatus bijwerken.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8559c0843d7e6e538b5b29dc394a50d05462ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425610"
---
# <a name="update-kanban-status"></a><span data-ttu-id="ccb24-103">Kanbanstatus bijwerken</span><span class="sxs-lookup"><span data-stu-id="ccb24-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccb24-104">Wanneer een kanban per ongeluk is geleegd of als een ontvangen kanban moet worden leeggemaakt, moet u de kanbanstatus bijwerken.</span><span class="sxs-lookup"><span data-stu-id="ccb24-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="ccb24-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="ccb24-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ccb24-106">Deze procedure is bedoeld voor de winkelchef.</span><span class="sxs-lookup"><span data-stu-id="ccb24-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="ccb24-107">Zoek de kanban.</span><span class="sxs-lookup"><span data-stu-id="ccb24-107">Find the kanban.</span></span>
1. <span data-ttu-id="ccb24-108">Ga naar Productiebeheer > Kanban > Kanbans.</span><span class="sxs-lookup"><span data-stu-id="ccb24-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="ccb24-109">Open de kolomfilter Status materiaalverwerkingseenheid.</span><span class="sxs-lookup"><span data-stu-id="ccb24-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="ccb24-110">Klik op Wissen.</span><span class="sxs-lookup"><span data-stu-id="ccb24-110">Click Clear.</span></span>
    * <span data-ttu-id="ccb24-111">Hiermee worden de filters opnieuw ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ccb24-111">This resets the filters.</span></span>  
4. <span data-ttu-id="ccb24-112">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ccb24-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ccb24-113">Filter bijvoorbeeld op het veld Kaartnummer met een waarde van '000149'.</span><span class="sxs-lookup"><span data-stu-id="ccb24-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="ccb24-114">Status Geleegd in Ontvangen wijzigen</span><span class="sxs-lookup"><span data-stu-id="ccb24-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="ccb24-115">Klik op Omgekeerde lege materiaalverwerkingseenheid.</span><span class="sxs-lookup"><span data-stu-id="ccb24-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="ccb24-116">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="ccb24-116">Click OK.</span></span>
    * <span data-ttu-id="ccb24-117">De status van de materiaalverwerkingseenheid is Ontvangen.</span><span class="sxs-lookup"><span data-stu-id="ccb24-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="ccb24-118">Status Ontvangen in Geleegd wijzigen</span><span class="sxs-lookup"><span data-stu-id="ccb24-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="ccb24-119">Klik op Lege Kanban.</span><span class="sxs-lookup"><span data-stu-id="ccb24-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="ccb24-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ccb24-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ccb24-121">De status van de materiaalverwerkingseenheid is Geleegd.</span><span class="sxs-lookup"><span data-stu-id="ccb24-121">Notice that the Handling unit status is Emptied.</span></span>  

