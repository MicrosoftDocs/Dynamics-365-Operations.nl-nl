---
title: Een kanbantaak uit de planning verwijderen
description: Deze procedure richt zich op het verwijderen van een geplande proceskanbantaak uit de planning door de taakstatus terug te zetten op Niet gepland.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcd9247e24323ba606377d7e51bd4447ab51c905
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961610"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="e2b02-103">Een kanbantaak uit de planning verwijderen</span><span class="sxs-lookup"><span data-stu-id="e2b02-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2b02-104">Deze procedure richt zich op het verwijderen van een geplande proceskanbantaak uit de planning door de taakstatus terug te zetten op Niet gepland.</span><span class="sxs-lookup"><span data-stu-id="e2b02-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="e2b02-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="e2b02-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e2b02-106">Deze procedure is bedoeld voor de werkvloersupervisor of de productieplanner.</span><span class="sxs-lookup"><span data-stu-id="e2b02-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="e2b02-107">Een geplande kanbantaak zoeken</span><span class="sxs-lookup"><span data-stu-id="e2b02-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="e2b02-108">Ga naar Productiebeheer > Kanban > Kanbantaakplanning.</span><span class="sxs-lookup"><span data-stu-id="e2b02-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="e2b02-109">Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e2b02-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e2b02-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e2b02-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2b02-111">Selecteer werkcel 1250.</span><span class="sxs-lookup"><span data-stu-id="e2b02-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="e2b02-112">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="e2b02-112">Click Select.</span></span>
5. <span data-ttu-id="e2b02-113">Selecteer in het veld Taakstatus weergeven de optie Gepland.</span><span class="sxs-lookup"><span data-stu-id="e2b02-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="e2b02-114">De geplande kanbantaak uit de planning verwijderen</span><span class="sxs-lookup"><span data-stu-id="e2b02-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="e2b02-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e2b02-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e2b02-116">Selecteer een taak met de status Gepland, bijvoorbeeld een taak van 19 december 2012.</span><span class="sxs-lookup"><span data-stu-id="e2b02-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="e2b02-117">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="e2b02-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="e2b02-118">Klik op Taakstatus terugdraaien</span><span class="sxs-lookup"><span data-stu-id="e2b02-118">Click Revert job status.</span></span>
4. <span data-ttu-id="e2b02-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e2b02-119">Click OK.</span></span>
    * <span data-ttu-id="e2b02-120">Hiermee wordt de huidige taakstatus teruggedraaid van Gepland naar Niet-gepland en wordt de taak verwijderd van het verwerkingsbord.</span><span class="sxs-lookup"><span data-stu-id="e2b02-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   

