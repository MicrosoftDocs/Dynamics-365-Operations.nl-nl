---
title: Een proceskanbantaak voorbereiden wanneer de materialen niet beschikbaar zijn voor de werkcel
description: Deze procedure is gericht op het voorbereiden van een proceskanbantaak wanneer bepaalde materialen niet beschikbaar zijn voor de werkcel. Daarom is het noodzakelijk om materialen in het magazijn te verzamelen.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72fd083edc48504b35f540ea7bdc8c8c736418f3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828629"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="97f35-103">Een proceskanbantaak voorbereiden wanneer de materialen niet beschikbaar zijn voor de werkcel</span><span class="sxs-lookup"><span data-stu-id="97f35-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="97f35-104">Deze procedure is gericht op het voorbereiden van een proceskanbantaak wanneer bepaalde materialen niet beschikbaar zijn voor de werkcel. Daarom is het noodzakelijk om materialen in het magazijn te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="97f35-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="97f35-105">De procedure "Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn" is een vereiste voor het maken van deze procedure.</span><span class="sxs-lookup"><span data-stu-id="97f35-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="97f35-106">Deze procedure is bedoeld voor de machineoperator.</span><span class="sxs-lookup"><span data-stu-id="97f35-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="97f35-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="97f35-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="97f35-108">Ga naar Productiebeheer > Kanban > Kanbanplanbord voor procestaken.</span><span class="sxs-lookup"><span data-stu-id="97f35-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="97f35-109">Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="97f35-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="97f35-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="97f35-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="97f35-111">Selecteer werkcel 1250.</span><span class="sxs-lookup"><span data-stu-id="97f35-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="97f35-112">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="97f35-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="97f35-113">Selecteer Kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="97f35-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="97f35-114">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="97f35-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="97f35-115">Heft de selectie van rij 4 in de lijst op.</span><span class="sxs-lookup"><span data-stu-id="97f35-115">In the list, deselect row 4.</span></span> <span data-ttu-id="97f35-116">Of selecteer rij 4 als u de taak "Een proceskanbantaak voorbereiden wanneer de materialen voor de werkcel beschikbaar zijn" niet hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="97f35-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="97f35-117">Schakel de uitbreiding van de sectie Orderverzamellijst om.</span><span class="sxs-lookup"><span data-stu-id="97f35-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="97f35-118">Het pictogram Geen vermelding in de aanbodstatus geeft aan dat 48 ea van artikel P0002 ontbreken voor de werkcel.</span><span class="sxs-lookup"><span data-stu-id="97f35-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="97f35-119">Materialen overboeken naar werkcel</span><span class="sxs-lookup"><span data-stu-id="97f35-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="97f35-120">Schakel de uitbreiding van de sectie Overboekingstaken om.</span><span class="sxs-lookup"><span data-stu-id="97f35-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="97f35-121">Gebruik het snelfilter om te filteren op het veld Artikelnummer met de waarde 'P0002'.</span><span class="sxs-lookup"><span data-stu-id="97f35-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="97f35-122">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="97f35-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="97f35-123">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="97f35-123">Click Start.</span></span>
    * <span data-ttu-id="97f35-124">Bezig met overboeken.</span><span class="sxs-lookup"><span data-stu-id="97f35-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="97f35-125">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="97f35-125">Click Complete.</span></span>
    * <span data-ttu-id="97f35-126">Het artikel P0002 is nu beschikbaar in de orderverzamellijst voor de kanbantaak.</span><span class="sxs-lookup"><span data-stu-id="97f35-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="97f35-127">Dit betekent dat we de kanban kunnen voorbereiden met alle benodigde materialen.</span><span class="sxs-lookup"><span data-stu-id="97f35-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="97f35-128">Klik op Voorbereiden.</span><span class="sxs-lookup"><span data-stu-id="97f35-128">Click Prepare.</span></span>
    * <span data-ttu-id="97f35-129">Merk op dat een pictogram in de Taakstatus aangeeft dat de taak nu gereed is.</span><span class="sxs-lookup"><span data-stu-id="97f35-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]