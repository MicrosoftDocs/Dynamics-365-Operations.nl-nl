---
title: Vastgelopen batchtaken opnieuw instellen
description: In dit onderwerp wordt uitgelegd hoe u problemen met vastgelopen batchtaken oplost.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 01ef0bf8ccc486614eec42d3fb6f0b2941fc47c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794944"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="e8b5d-103">Vastgelopen batchtaken opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="e8b5d-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="e8b5d-104">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="e8b5d-104">Issue</span></span>

<span data-ttu-id="e8b5d-105">Microsoft Dynamics 365 Human Resources kan problemen ondervinden met batchtaken die vastlopen in de status **Uitvoeren** of **Annuleren** en niet worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="e8b5d-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="e8b5d-106">Resolution</span></span>

<span data-ttu-id="e8b5d-107">Wanneer een batchtaak vastloopt in de status **Uitvoeren** of **Annuleren**, u de status opnieuw instellen door de annulering van de taak af te dwingen.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="e8b5d-108">Nadat u deze hebt geannuleerd, kunt u de batchtaak opnieuw instellen door de status **Wachten** in te stellen.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="e8b5d-109">De taak wordt vervolgens weer opgehaald voor uitvoering in de volgende geplande batchrun.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="e8b5d-110">Selecteer in de werkruimte **Systeembeheer** de pagina **Koppelingen** en selecteer **Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="e8b5d-111">Selecteer op de lijstpagina **Batchtaak** de taak die opnieuw moet worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="e8b5d-112">Selecteer op het actielint de optie **Annuleren afdwingen** en bevestig de actie.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e8b5d-113">De actie **Annuleren afdwingen** is alleen beschikbaar als de geselecteerde batchtaak de status **Uitvoeren** of **Annuleren** heeft en er geen processen voor batchuitvoering of -annulering worden uitgevoerd voor de taak.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="e8b5d-114">Selecteer op het actielint de optie **Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="e8b5d-115">Selecteer op de pagina **Nieuwe status selecteren** de optie **Wachten** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8b5d-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Een nieuwe batchtaakstatus selecteren](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="e8b5d-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e8b5d-117">See also</span></span>

[<span data-ttu-id="e8b5d-118">Prestaties optimaliseren door batchtaken buiten werktijd te plannen</span><span class="sxs-lookup"><span data-stu-id="e8b5d-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="e8b5d-119">Prestaties optimaliseren met automatische opschoningstaken</span><span class="sxs-lookup"><span data-stu-id="e8b5d-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
