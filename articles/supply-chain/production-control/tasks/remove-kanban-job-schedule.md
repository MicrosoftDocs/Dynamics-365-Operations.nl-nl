---
title: Een kanbantaak uit de planning verwijderen
description: Deze procedure richt zich op het verwijderen van een geplande proceskanbantaak uit de planning door de taakstatus terug te zetten op Niet gepland.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e9a512e7f391e08a35fd0eea449af12d81e644
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828581"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="babf7-103">Een kanbantaak uit de planning verwijderen</span><span class="sxs-lookup"><span data-stu-id="babf7-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="babf7-104">Deze procedure richt zich op het verwijderen van een geplande proceskanbantaak uit de planning door de taakstatus terug te zetten op Niet gepland.</span><span class="sxs-lookup"><span data-stu-id="babf7-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="babf7-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="babf7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="babf7-106">Deze procedure is bedoeld voor de werkvloersupervisor of de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="babf7-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="babf7-107">Een geplande kanbantaak zoeken</span><span class="sxs-lookup"><span data-stu-id="babf7-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="babf7-108">Ga naar Productiebeheer > Kanban > Kanbantaakplanning.</span><span class="sxs-lookup"><span data-stu-id="babf7-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="babf7-109">Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="babf7-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="babf7-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="babf7-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="babf7-111">Selecteer werkcel 1250.</span><span class="sxs-lookup"><span data-stu-id="babf7-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="babf7-112">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="babf7-112">Click Select.</span></span>
5. <span data-ttu-id="babf7-113">Selecteer in het veld Taakstatus weergeven de optie Gepland.</span><span class="sxs-lookup"><span data-stu-id="babf7-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="babf7-114">De geplande kanbantaak uit de planning verwijderen</span><span class="sxs-lookup"><span data-stu-id="babf7-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="babf7-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="babf7-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="babf7-116">Selecteer een taak met de status Gepland, bijvoorbeeld een taak van 19 december 2012.</span><span class="sxs-lookup"><span data-stu-id="babf7-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="babf7-117">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="babf7-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="babf7-118">Klik op Taakstatus terugdraaien</span><span class="sxs-lookup"><span data-stu-id="babf7-118">Click Revert job status.</span></span>
4. <span data-ttu-id="babf7-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="babf7-119">Click OK.</span></span>
    * <span data-ttu-id="babf7-120">Hiermee wordt de huidige taakstatus teruggedraaid van Gepland naar Niet-gepland en wordt de taak verwijderd van het verwerkingsbord.</span><span class="sxs-lookup"><span data-stu-id="babf7-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]