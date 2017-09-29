---
title: Ondersteuning van kanbanoverboekingsbord voor streepjescodescanners
description: Het kanbanoverboekingsbord ondersteunt scannerinvoer vanuit een widgetstreepjescodescanner om een kanbantaak te selecteren, starten, voltooien en legen.
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1dc40de2b77be5c5c2399fd55c3c3bd15a9f24ec
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="8aa91-103">Ondersteuning van kanbanoverboekingsbord voor streepjescodescanners</span><span class="sxs-lookup"><span data-stu-id="8aa91-103">Kanban transfer board support for barcode scanners</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8aa91-104">Het kanbanoverboekingsbord ondersteunt scannerinvoer vanuit een widgetstreepjescodescanner om een kanbantaak te selecteren, starten, voltooien en legen.</span><span class="sxs-lookup"><span data-stu-id="8aa91-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="8aa91-105">Registratiemodi</span><span class="sxs-lookup"><span data-stu-id="8aa91-105">Registration modes</span></span>
------------------

<span data-ttu-id="8aa91-106">Op het sneltabblad **Scannerregistratie** kunt u de registratiemodus selecteren die de actie bepaalt bij het scannen van een kanbankaartnummer of het handmatig invoeren van het nummer in het veld Kanbankaartnummer.</span><span class="sxs-lookup"><span data-stu-id="8aa91-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>
| <span data-ttu-id="8aa91-107">Registratiemodus instellen</span><span class="sxs-lookup"><span data-stu-id="8aa91-107">Set registration mode</span></span> | <span data-ttu-id="8aa91-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8aa91-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa91-109">Beginnen</span><span class="sxs-lookup"><span data-stu-id="8aa91-109">Start</span></span>                 | <span data-ttu-id="8aa91-110">Registreert een kanbanoverboekingstaak als in uitvoering.</span><span class="sxs-lookup"><span data-stu-id="8aa91-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="8aa91-111">Voltooid</span><span class="sxs-lookup"><span data-stu-id="8aa91-111">Complete</span></span>              | <span data-ttu-id="8aa91-112">Registreert een kanbanoverboekingstaak als voltooid.</span><span class="sxs-lookup"><span data-stu-id="8aa91-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="8aa91-113">Leeg</span><span class="sxs-lookup"><span data-stu-id="8aa91-113">Empty</span></span>                 | <span data-ttu-id="8aa91-114">Registreert de materiaalverwerkingseenheid waarnaar door een kanbankaart wordt verwezen als leeg.</span><span class="sxs-lookup"><span data-stu-id="8aa91-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="8aa91-115">Selecteren</span><span class="sxs-lookup"><span data-stu-id="8aa91-115">Select</span></span>                | <span data-ttu-id="8aa91-116">Registreert een kanbankaartnummer en selecteert automatisch de taak waarnaar wordt verwezen in de kanbanlijst.</span><span class="sxs-lookup"><span data-stu-id="8aa91-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="8aa91-117">Registratiemodus Selecteren</span><span class="sxs-lookup"><span data-stu-id="8aa91-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="8aa91-118">Wanneer u een streepjescodelezer gebruikt om een taak te selecteren, wordt de weergavemodus van het kanbanbord gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="8aa91-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="8aa91-119">In deze modus gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="8aa91-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="8aa91-120">Alleen de gescande kanbantaak wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8aa91-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="8aa91-121">De details van de geselecteerde taak worden weergegeven op het sneltabblad **Details**.</span><span class="sxs-lookup"><span data-stu-id="8aa91-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="8aa91-122">Het sneltabblad **Berichten** geeft alleen berichten weer voor de geselecteerde taak.</span><span class="sxs-lookup"><span data-stu-id="8aa91-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="8aa91-123">U kunt de status van de taak wijzigen met de functies die beschikbaar zijn in het Actievenster.</span><span class="sxs-lookup"><span data-stu-id="8aa91-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="8aa91-124">Het kanbanoverboekingsbord blijft één taak weergeven tijdens deze periode.</span><span class="sxs-lookup"><span data-stu-id="8aa91-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="8aa91-125">U kunt de gegevens in de lijst met taken handmatig bijwerken door te klikken op **Vernieuwen** (Shift+F5) in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="8aa91-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="8aa91-126">Nadat u de gegevens hebt vernieuwd, worden de volledige resultaten voor het taakfilter opnieuw weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8aa91-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="8aa91-127">Taakstatus en mogelijke acties</span><span class="sxs-lookup"><span data-stu-id="8aa91-127">Job status and possible actions</span></span>
<span data-ttu-id="8aa91-128">De status van de geselecteerde taak en de status van alle getraceerde taken voor gebeurteniskanbans bepalen of u de taak verder kunt verwerken.</span><span class="sxs-lookup"><span data-stu-id="8aa91-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="8aa91-129">De volgende tabel bevat informatie over deze statussen en taken:</span><span class="sxs-lookup"><span data-stu-id="8aa91-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="8aa91-130">De statussen die beschikbaar zijn voor taken of voor de materiaalverwerkingseenheden waarnaar wordt verwezen door de taken.</span><span class="sxs-lookup"><span data-stu-id="8aa91-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="8aa91-131">Elke taak die u voor de taak kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8aa91-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8aa91-132">Functietype</span><span class="sxs-lookup"><span data-stu-id="8aa91-132">Job type</span></span></th>
<th><span data-ttu-id="8aa91-133">Taakstatus of de status van materiaalverwerkingseenheid</span><span class="sxs-lookup"><span data-stu-id="8aa91-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="8aa91-134">Orderverzamellijst bijwerken</span><span class="sxs-lookup"><span data-stu-id="8aa91-134">Update picking list</span></span></th>
<th><span data-ttu-id="8aa91-135">Beginnen</span><span class="sxs-lookup"><span data-stu-id="8aa91-135">Start</span></span></th>
<th><span data-ttu-id="8aa91-136">Registratie bijwerken</span><span class="sxs-lookup"><span data-stu-id="8aa91-136">Update registration</span></span></th>
<th><span data-ttu-id="8aa91-137">Voltooid</span><span class="sxs-lookup"><span data-stu-id="8aa91-137">Complete</span></span></th>
<th><span data-ttu-id="8aa91-138">Leeg</span><span class="sxs-lookup"><span data-stu-id="8aa91-138">Empty</span></span></th>
<th><span data-ttu-id="8aa91-139">Gebeurteniskanbans maken</span><span class="sxs-lookup"><span data-stu-id="8aa91-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8aa91-140">Overboeken</span><span class="sxs-lookup"><span data-stu-id="8aa91-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="8aa91-141">Niet gepland</span><span class="sxs-lookup"><span data-stu-id="8aa91-141">Not planned</span></span></li>
<li><span data-ttu-id="8aa91-142">Er zijn geen getraceerde taken of getraceerde taken zijn Voltooid</span><span class="sxs-lookup"><span data-stu-id="8aa91-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="8aa91-143">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-143">Yes</span></span></td>
<td><span data-ttu-id="8aa91-144">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-144">Yes</span></span></td>
<td><span data-ttu-id="8aa91-145">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-145">Yes</span></span></td>
<td><span data-ttu-id="8aa91-146">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-146">Yes</span></span></td>
<td><span data-ttu-id="8aa91-147">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-147">No</span></span></td>
<td><span data-ttu-id="8aa91-148">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8aa91-149">Overboeken</span><span class="sxs-lookup"><span data-stu-id="8aa91-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="8aa91-150">Niet gepland</span><span class="sxs-lookup"><span data-stu-id="8aa91-150">Not planned</span></span></li>
<li><span data-ttu-id="8aa91-151">De getraceerde taak is niet Voltooid</span><span class="sxs-lookup"><span data-stu-id="8aa91-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="8aa91-152">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-152">Yes</span></span></td>
<td><span data-ttu-id="8aa91-153">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-153">No</span></span></td>
<td><span data-ttu-id="8aa91-154">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-154">Yes</span></span></td>
<td><span data-ttu-id="8aa91-155">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-155">No</span></span></td>
<td><span data-ttu-id="8aa91-156">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-156">No</span></span></td>
<td><span data-ttu-id="8aa91-157">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8aa91-158">Overboeken</span><span class="sxs-lookup"><span data-stu-id="8aa91-158">Transfer</span></span></td>
<td><span data-ttu-id="8aa91-159">In uitvoering</span><span class="sxs-lookup"><span data-stu-id="8aa91-159">In progress</span></span></td>
<td><span data-ttu-id="8aa91-160">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-160">Yes</span></span></td>
<td><span data-ttu-id="8aa91-161">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-161">No</span></span></td>
<td><span data-ttu-id="8aa91-162">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-162">Yes</span></span></td>
<td><span data-ttu-id="8aa91-163">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-163">Yes</span></span></td>
<td><span data-ttu-id="8aa91-164">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-164">No</span></span></td>
<td><span data-ttu-id="8aa91-165">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8aa91-166">Overboeken</span><span class="sxs-lookup"><span data-stu-id="8aa91-166">Transfer</span></span></td>
<td><span data-ttu-id="8aa91-167">Voltooid</span><span class="sxs-lookup"><span data-stu-id="8aa91-167">Completed</span></span></td>
<td><span data-ttu-id="8aa91-168">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-168">No</span></span></td>
<td><span data-ttu-id="8aa91-169">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-169">No</span></span></td>
<td><span data-ttu-id="8aa91-170">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-170">No</span></span></td>
<td><span data-ttu-id="8aa91-171">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-171">No</span></span></td>
<td><span data-ttu-id="8aa91-172">Ja</span><span class="sxs-lookup"><span data-stu-id="8aa91-172">Yes</span></span></td>
<td><span data-ttu-id="8aa91-173">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8aa91-174">Overboeken of verwerken</span><span class="sxs-lookup"><span data-stu-id="8aa91-174">Transfer or process</span></span></td>
<td><span data-ttu-id="8aa91-175">Leeg</span><span class="sxs-lookup"><span data-stu-id="8aa91-175">Empty</span></span></td>
<td><span data-ttu-id="8aa91-176">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-176">No</span></span></td>
<td><span data-ttu-id="8aa91-177">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-177">No</span></span></td>
<td><span data-ttu-id="8aa91-178">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-178">No</span></span></td>
<td><span data-ttu-id="8aa91-179">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-179">No</span></span></td>
<td><span data-ttu-id="8aa91-180">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-180">No</span></span></td>
<td><span data-ttu-id="8aa91-181">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8aa91-182">Overboeken of verwerken</span><span class="sxs-lookup"><span data-stu-id="8aa91-182">Transfer or process</span></span></td>
<td><span data-ttu-id="8aa91-183">Er is geen kanbankaart gevonden</span><span class="sxs-lookup"><span data-stu-id="8aa91-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="8aa91-184">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-184">No</span></span></td>
<td><span data-ttu-id="8aa91-185">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-185">No</span></span></td>
<td><span data-ttu-id="8aa91-186">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-186">No</span></span></td>
<td><span data-ttu-id="8aa91-187">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-187">No</span></span></td>
<td><span data-ttu-id="8aa91-188">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-188">No</span></span></td>
<td><span data-ttu-id="8aa91-189">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8aa91-190">Overboeken of verwerken</span><span class="sxs-lookup"><span data-stu-id="8aa91-190">Transfer or process</span></span></td>
<td><span data-ttu-id="8aa91-191">Er is een kanbankaart gevonden, maar deze is niet toegewezen aan een kanban</span><span class="sxs-lookup"><span data-stu-id="8aa91-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="8aa91-192">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-192">No</span></span></td>
<td><span data-ttu-id="8aa91-193">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-193">No</span></span></td>
<td><span data-ttu-id="8aa91-194">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-194">No</span></span></td>
<td><span data-ttu-id="8aa91-195">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-195">No</span></span></td>
<td><span data-ttu-id="8aa91-196">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-196">No</span></span></td>
<td><span data-ttu-id="8aa91-197">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8aa91-198">Verwerken</span><span class="sxs-lookup"><span data-stu-id="8aa91-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="8aa91-199">Niet gepland</span><span class="sxs-lookup"><span data-stu-id="8aa91-199">Not planned</span></span></li>
<li><span data-ttu-id="8aa91-200">Voorbereid</span><span class="sxs-lookup"><span data-stu-id="8aa91-200">Prepared</span></span></li>
<li><span data-ttu-id="8aa91-201">In uitvoering</span><span class="sxs-lookup"><span data-stu-id="8aa91-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="8aa91-202">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-202">No</span></span></td>
<td><span data-ttu-id="8aa91-203">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-203">No</span></span></td>
<td><span data-ttu-id="8aa91-204">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-204">No</span></span></td>
<td><span data-ttu-id="8aa91-205">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-205">No</span></span></td>
<td><span data-ttu-id="8aa91-206">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-206">No</span></span></td>
<td><span data-ttu-id="8aa91-207">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8aa91-208">Verwerken</span><span class="sxs-lookup"><span data-stu-id="8aa91-208">Process</span></span></td>
<td><span data-ttu-id="8aa91-209">Voltooid</span><span class="sxs-lookup"><span data-stu-id="8aa91-209">Completed</span></span></td>
<td><span data-ttu-id="8aa91-210">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-210">No</span></span></td>
<td><span data-ttu-id="8aa91-211">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-211">No</span></span></td>
<td><span data-ttu-id="8aa91-212">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-212">No</span></span></td>
<td><span data-ttu-id="8aa91-213">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-213">No</span></span></td>
<td><span data-ttu-id="8aa91-214">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-214">No</span></span></td>
<td><span data-ttu-id="8aa91-215">Nee</span><span class="sxs-lookup"><span data-stu-id="8aa91-215">No</span></span></td>
</tr>
</tbody>
</table>






