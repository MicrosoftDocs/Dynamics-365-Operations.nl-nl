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
ms.openlocfilehash: cf163968474e91da7e3d47fd638a857a76179645
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148960"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="02273-103">Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn</span><span class="sxs-lookup"><span data-stu-id="02273-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02273-104">Deze taak richt zich op het voorbereiden van een proceskanbantaak wanneer alle materialen voor de werkcel beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="02273-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="02273-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="02273-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="02273-106">Deze taak is bedoeld voor de machineoperator.</span><span class="sxs-lookup"><span data-stu-id="02273-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="02273-107">Ga naar Kanbanplanbord voor procestaken.</span><span class="sxs-lookup"><span data-stu-id="02273-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="02273-108">Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="02273-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="02273-109">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="02273-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="02273-110">Selecteer werkcel 1250 en klik op OK.</span><span class="sxs-lookup"><span data-stu-id="02273-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="02273-111">Selecteer rij 4 in de lijst.</span><span class="sxs-lookup"><span data-stu-id="02273-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="02273-112">In het schone demobedrijf, is Kanban 000329 in rij 4 de eerste taak die nog niet is voltooid.</span><span class="sxs-lookup"><span data-stu-id="02273-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="02273-113">Schakel de uitbreiding van de sectie Orderverzamellijst om.</span><span class="sxs-lookup"><span data-stu-id="02273-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="02273-114">Controleer of de voorraadstatus beschikbaar is voor alle artikelen in de orderverzamellijst.</span><span class="sxs-lookup"><span data-stu-id="02273-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="02273-115">Als meerdere taken zijn geselecteerd, geeft de orderverzamellijst de som weer van alle artikelen die nodig zijn voor de geselecteerde taken.</span><span class="sxs-lookup"><span data-stu-id="02273-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="02273-116">Klik op Voorbereiden.</span><span class="sxs-lookup"><span data-stu-id="02273-116">Click Prepare.</span></span>
    * <span data-ttu-id="02273-117">Het voorbereidingsproces wordt nu voltooid.</span><span class="sxs-lookup"><span data-stu-id="02273-117">The preparation process is now completed.</span></span> <span data-ttu-id="02273-118">Het ingeschakelde selectievakje voor alle rijen in de orderverzamellijst geeft aan dat de voorraadstatus wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="02273-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

