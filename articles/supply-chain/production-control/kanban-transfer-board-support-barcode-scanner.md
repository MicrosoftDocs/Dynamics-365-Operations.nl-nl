---
title: Ondersteuning van kanbanoverboekingsbord voor streepjescodescanners
description: Het kanbanoverboekingsbord ondersteunt scannerinvoer vanuit een widgetstreepjescodescanner om een kanbantaak te selecteren, starten, voltooien en legen.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b6d65430d09c293fd5bca032b8b0e88c971d5a9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246088"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="de269-103">Ondersteuning van kanbanoverboekingsbord voor streepjescodescanners</span><span class="sxs-lookup"><span data-stu-id="de269-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de269-104">Het kanbanoverboekingsbord ondersteunt scannerinvoer vanuit een widgetstreepjescodescanner om een kanbantaak te selecteren, starten, voltooien en legen.</span><span class="sxs-lookup"><span data-stu-id="de269-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="de269-105">Registratiemodi</span><span class="sxs-lookup"><span data-stu-id="de269-105">Registration modes</span></span>
------------------

<span data-ttu-id="de269-106">Op het sneltabblad **Scannerregistratie** kunt u de registratiemodus selecteren die de actie bepaalt bij het scannen van een kanbankaartnummer of het handmatig invoeren van het nummer in het veld Kanbankaartnummer.</span><span class="sxs-lookup"><span data-stu-id="de269-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="de269-107">Registratiemodus instellen</span><span class="sxs-lookup"><span data-stu-id="de269-107">Set registration mode</span></span> | <span data-ttu-id="de269-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="de269-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de269-109">Beginnen</span><span class="sxs-lookup"><span data-stu-id="de269-109">Start</span></span>                 | <span data-ttu-id="de269-110">Registreert een kanbanoverboekingstaak als in uitvoering.</span><span class="sxs-lookup"><span data-stu-id="de269-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="de269-111">Voltooid</span><span class="sxs-lookup"><span data-stu-id="de269-111">Complete</span></span>              | <span data-ttu-id="de269-112">Registreert een kanbanoverboekingstaak als voltooid.</span><span class="sxs-lookup"><span data-stu-id="de269-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="de269-113">Leeg</span><span class="sxs-lookup"><span data-stu-id="de269-113">Empty</span></span>                 | <span data-ttu-id="de269-114">Registreert de materiaalverwerkingseenheid waarnaar door een kanbankaart wordt verwezen als leeg.</span><span class="sxs-lookup"><span data-stu-id="de269-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="de269-115">Selecteren</span><span class="sxs-lookup"><span data-stu-id="de269-115">Select</span></span>                | <span data-ttu-id="de269-116">Registreert een kanbankaartnummer en selecteert automatisch de taak waarnaar wordt verwezen in de kanbanlijst.</span><span class="sxs-lookup"><span data-stu-id="de269-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="de269-117">Registratiemodus Selecteren</span><span class="sxs-lookup"><span data-stu-id="de269-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="de269-118">Wanneer u een streepjescodelezer gebruikt om een taak te selecteren, wordt de weergavemodus van het kanbanbord gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="de269-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="de269-119">In deze modus gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="de269-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="de269-120">Alleen de gescande kanbantaak wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="de269-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="de269-121">De details van de geselecteerde taak worden weergegeven op het sneltabblad **Details**.</span><span class="sxs-lookup"><span data-stu-id="de269-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="de269-122">Het sneltabblad **Berichten** geeft alleen berichten weer voor de geselecteerde taak.</span><span class="sxs-lookup"><span data-stu-id="de269-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="de269-123">U kunt de status van de taak wijzigen met de functies die beschikbaar zijn in het Actievenster.</span><span class="sxs-lookup"><span data-stu-id="de269-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="de269-124">Het kanbanoverboekingsbord blijft één taak weergeven tijdens deze periode.</span><span class="sxs-lookup"><span data-stu-id="de269-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="de269-125">U kunt de gegevens in de lijst met taken handmatig bijwerken door te klikken op **Vernieuwen** (Shift+F5) in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="de269-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="de269-126">Nadat u de gegevens hebt vernieuwd, worden de volledige resultaten voor het taakfilter opnieuw weergegeven.</span><span class="sxs-lookup"><span data-stu-id="de269-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="de269-127">Taakstatus en mogelijke acties</span><span class="sxs-lookup"><span data-stu-id="de269-127">Job status and possible actions</span></span>
<span data-ttu-id="de269-128">De status van de geselecteerde taak en de status van alle getraceerde taken voor gebeurteniskanbans bepalen of u de taak verder kunt verwerken.</span><span class="sxs-lookup"><span data-stu-id="de269-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="de269-129">De volgende tabel bevat informatie over deze statussen en taken:</span><span class="sxs-lookup"><span data-stu-id="de269-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="de269-130">De statussen die beschikbaar zijn voor taken of voor de materiaalverwerkingseenheden waarnaar wordt verwezen door de taken.</span><span class="sxs-lookup"><span data-stu-id="de269-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="de269-131">Elke taak die u voor de taak kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="de269-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="de269-132">Functietype</span><span class="sxs-lookup"><span data-stu-id="de269-132">Job type</span></span></th>
<th><span data-ttu-id="de269-133">Taakstatus of de status van materiaalverwerkingseenheid</span><span class="sxs-lookup"><span data-stu-id="de269-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="de269-134">Orderverzamellijst bijwerken</span><span class="sxs-lookup"><span data-stu-id="de269-134">Update picking list</span></span></th>
<th><span data-ttu-id="de269-135">Beginnen</span><span class="sxs-lookup"><span data-stu-id="de269-135">Start</span></span></th>
<th><span data-ttu-id="de269-136">Registratie bijwerken</span><span class="sxs-lookup"><span data-stu-id="de269-136">Update registration</span></span></th>
<th><span data-ttu-id="de269-137">Voltooid</span><span class="sxs-lookup"><span data-stu-id="de269-137">Complete</span></span></th>
<th><span data-ttu-id="de269-138">Leeg</span><span class="sxs-lookup"><span data-stu-id="de269-138">Empty</span></span></th>
<th><span data-ttu-id="de269-139">Gebeurteniskanbans maken</span><span class="sxs-lookup"><span data-stu-id="de269-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de269-140">Overboeken</span><span class="sxs-lookup"><span data-stu-id="de269-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="de269-141">Niet gepland</span><span class="sxs-lookup"><span data-stu-id="de269-141">Not planned</span></span></li>
<li><span data-ttu-id="de269-142">Er zijn geen getraceerde taken of getraceerde taken zijn Voltooid</span><span class="sxs-lookup"><span data-stu-id="de269-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="de269-143">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-143">Yes</span></span></td>
<td><span data-ttu-id="de269-144">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-144">Yes</span></span></td>
<td><span data-ttu-id="de269-145">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-145">Yes</span></span></td>
<td><span data-ttu-id="de269-146">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-146">Yes</span></span></td>
<td><span data-ttu-id="de269-147">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-147">No</span></span></td>
<td><span data-ttu-id="de269-148">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de269-149">Overboeken</span><span class="sxs-lookup"><span data-stu-id="de269-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="de269-150">Niet gepland</span><span class="sxs-lookup"><span data-stu-id="de269-150">Not planned</span></span></li>
<li><span data-ttu-id="de269-151">De getraceerde taak is niet Voltooid</span><span class="sxs-lookup"><span data-stu-id="de269-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="de269-152">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-152">Yes</span></span></td>
<td><span data-ttu-id="de269-153">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-153">No</span></span></td>
<td><span data-ttu-id="de269-154">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-154">Yes</span></span></td>
<td><span data-ttu-id="de269-155">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-155">No</span></span></td>
<td><span data-ttu-id="de269-156">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-156">No</span></span></td>
<td><span data-ttu-id="de269-157">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de269-158">Overboeken</span><span class="sxs-lookup"><span data-stu-id="de269-158">Transfer</span></span></td>
<td><span data-ttu-id="de269-159">In uitvoering</span><span class="sxs-lookup"><span data-stu-id="de269-159">In progress</span></span></td>
<td><span data-ttu-id="de269-160">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-160">Yes</span></span></td>
<td><span data-ttu-id="de269-161">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-161">No</span></span></td>
<td><span data-ttu-id="de269-162">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-162">Yes</span></span></td>
<td><span data-ttu-id="de269-163">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-163">Yes</span></span></td>
<td><span data-ttu-id="de269-164">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-164">No</span></span></td>
<td><span data-ttu-id="de269-165">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de269-166">Overboeken</span><span class="sxs-lookup"><span data-stu-id="de269-166">Transfer</span></span></td>
<td><span data-ttu-id="de269-167">Voltooid</span><span class="sxs-lookup"><span data-stu-id="de269-167">Completed</span></span></td>
<td><span data-ttu-id="de269-168">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-168">No</span></span></td>
<td><span data-ttu-id="de269-169">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-169">No</span></span></td>
<td><span data-ttu-id="de269-170">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-170">No</span></span></td>
<td><span data-ttu-id="de269-171">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-171">No</span></span></td>
<td><span data-ttu-id="de269-172">Ja</span><span class="sxs-lookup"><span data-stu-id="de269-172">Yes</span></span></td>
<td><span data-ttu-id="de269-173">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de269-174">Overboeken of verwerken</span><span class="sxs-lookup"><span data-stu-id="de269-174">Transfer or process</span></span></td>
<td><span data-ttu-id="de269-175">Leeg</span><span class="sxs-lookup"><span data-stu-id="de269-175">Empty</span></span></td>
<td><span data-ttu-id="de269-176">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-176">No</span></span></td>
<td><span data-ttu-id="de269-177">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-177">No</span></span></td>
<td><span data-ttu-id="de269-178">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-178">No</span></span></td>
<td><span data-ttu-id="de269-179">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-179">No</span></span></td>
<td><span data-ttu-id="de269-180">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-180">No</span></span></td>
<td><span data-ttu-id="de269-181">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de269-182">Overboeken of verwerken</span><span class="sxs-lookup"><span data-stu-id="de269-182">Transfer or process</span></span></td>
<td><span data-ttu-id="de269-183">Er is geen kanbankaart gevonden</span><span class="sxs-lookup"><span data-stu-id="de269-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="de269-184">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-184">No</span></span></td>
<td><span data-ttu-id="de269-185">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-185">No</span></span></td>
<td><span data-ttu-id="de269-186">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-186">No</span></span></td>
<td><span data-ttu-id="de269-187">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-187">No</span></span></td>
<td><span data-ttu-id="de269-188">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-188">No</span></span></td>
<td><span data-ttu-id="de269-189">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de269-190">Overboeken of verwerken</span><span class="sxs-lookup"><span data-stu-id="de269-190">Transfer or process</span></span></td>
<td><span data-ttu-id="de269-191">Er is een kanbankaart gevonden, maar deze is niet toegewezen aan een kanban</span><span class="sxs-lookup"><span data-stu-id="de269-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="de269-192">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-192">No</span></span></td>
<td><span data-ttu-id="de269-193">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-193">No</span></span></td>
<td><span data-ttu-id="de269-194">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-194">No</span></span></td>
<td><span data-ttu-id="de269-195">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-195">No</span></span></td>
<td><span data-ttu-id="de269-196">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-196">No</span></span></td>
<td><span data-ttu-id="de269-197">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de269-198">Verwerken</span><span class="sxs-lookup"><span data-stu-id="de269-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="de269-199">Niet gepland</span><span class="sxs-lookup"><span data-stu-id="de269-199">Not planned</span></span></li>
<li><span data-ttu-id="de269-200">Voorbereid</span><span class="sxs-lookup"><span data-stu-id="de269-200">Prepared</span></span></li>
<li><span data-ttu-id="de269-201">In uitvoering</span><span class="sxs-lookup"><span data-stu-id="de269-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="de269-202">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-202">No</span></span></td>
<td><span data-ttu-id="de269-203">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-203">No</span></span></td>
<td><span data-ttu-id="de269-204">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-204">No</span></span></td>
<td><span data-ttu-id="de269-205">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-205">No</span></span></td>
<td><span data-ttu-id="de269-206">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-206">No</span></span></td>
<td><span data-ttu-id="de269-207">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de269-208">Verwerken</span><span class="sxs-lookup"><span data-stu-id="de269-208">Process</span></span></td>
<td><span data-ttu-id="de269-209">Voltooid</span><span class="sxs-lookup"><span data-stu-id="de269-209">Completed</span></span></td>
<td><span data-ttu-id="de269-210">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-210">No</span></span></td>
<td><span data-ttu-id="de269-211">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-211">No</span></span></td>
<td><span data-ttu-id="de269-212">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-212">No</span></span></td>
<td><span data-ttu-id="de269-213">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-213">No</span></span></td>
<td><span data-ttu-id="de269-214">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-214">No</span></span></td>
<td><span data-ttu-id="de269-215">Nee</span><span class="sxs-lookup"><span data-stu-id="de269-215">No</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]