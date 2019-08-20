---
title: Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn
description: Deze taak richt zich op het voorbereiden van een proceskanbantaak wanneer alle materialen voor de werkcel beschikbaar zijn.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 011c542d360309fdeb539c85a68f2a5691022e37
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836142"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="42248-103">Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn</span><span class="sxs-lookup"><span data-stu-id="42248-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42248-104">Deze taak richt zich op het voorbereiden van een proceskanbantaak wanneer alle materialen voor de werkcel beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="42248-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="42248-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="42248-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="42248-106">Deze taak is bedoeld voor de machineoperator.</span><span class="sxs-lookup"><span data-stu-id="42248-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="42248-107">Ga naar Kanbanplanbord voor procestaken.</span><span class="sxs-lookup"><span data-stu-id="42248-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="42248-108">Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="42248-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="42248-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="42248-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="42248-110">Selecteer werkcel 1250 en klik op OK.</span><span class="sxs-lookup"><span data-stu-id="42248-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="42248-111">Selecteer rij 4 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="42248-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="42248-112">In het schone demobedrijf, is Kanban 000329 in rij 4 de eerste taak die nog niet is voltooid.</span><span class="sxs-lookup"><span data-stu-id="42248-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="42248-113">Schakel de uitbreiding van de sectie Orderverzamellijst om.</span><span class="sxs-lookup"><span data-stu-id="42248-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="42248-114">Controleer of de voorraadstatus beschikbaar is voor alle artikelen in de orderverzamellijst.</span><span class="sxs-lookup"><span data-stu-id="42248-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="42248-115">Als meerdere taken zijn geselecteerd, geeft de orderverzamellijst de som weer van alle artikelen die nodig zijn voor de geselecteerde taken.</span><span class="sxs-lookup"><span data-stu-id="42248-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="42248-116">Klik op Voorbereiden.</span><span class="sxs-lookup"><span data-stu-id="42248-116">Click Prepare.</span></span>
    * <span data-ttu-id="42248-117">Het voorbereidingsproces wordt nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="42248-117">The preparation process is now completed.</span></span> <span data-ttu-id="42248-118">Het ingeschakelde selectievakje voor alle rijen in de orderverzamellijst geeft aan dat de voorraadstatus wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="42248-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

