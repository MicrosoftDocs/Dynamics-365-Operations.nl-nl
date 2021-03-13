---
title: Prestaties optimaliseren door batchtaken na werktijd te plannen
description: In dit onderwerp wordt uitgelegd hoe u prestatieproblemen met Microsoft Dynamics 365 Human Resources kunt oplossen door de batchtaken met een lange uitvoeringsduur na werktijd in te plannen.
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 219537aab2015469b6ca6ebed5c00af0190c5187
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112108"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="017cc-103">Prestaties optimaliseren door batchtaken na werktijd te plannen</span><span class="sxs-lookup"><span data-stu-id="017cc-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="017cc-104">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="017cc-104">Issue</span></span>

<span data-ttu-id="017cc-105">De prestaties van Microsoft Dynamics 365 Human Resources kunnen problemen ondervinden als langlopende batchtaken tijdens normale werktijden worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="017cc-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="017cc-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="017cc-106">Resolution</span></span>

<span data-ttu-id="017cc-107">Plan de volgende batchtaken in na werktijd.</span><span class="sxs-lookup"><span data-stu-id="017cc-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="017cc-108">We raden ook aan de frequentie te evalueren van batchtaken die regelmatig worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="017cc-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="017cc-109">Verminder zo mogelijk het herhalingspatroon van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="017cc-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="017cc-110">In veel gevallen is de standaardfrequentie voldoende.</span><span class="sxs-lookup"><span data-stu-id="017cc-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="017cc-111">De volgende batchtaken kunnen beter 's nachts of na werktijd worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="017cc-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="017cc-112">Controleer ook de tijdzone voor deze herhalende batchtaken.</span><span class="sxs-lookup"><span data-stu-id="017cc-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="017cc-113">Er zijn batchtaken die mogelijk een andere tijdzone gebruiken.</span><span class="sxs-lookup"><span data-stu-id="017cc-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="017cc-114">Batchtaak</span><span class="sxs-lookup"><span data-stu-id="017cc-114">Batch job</span></span> | <span data-ttu-id="017cc-115">Standaard herhalingspatroon</span><span class="sxs-lookup"><span data-stu-id="017cc-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="017cc-116">Batchtaakhistorie opschonen</span><span class="sxs-lookup"><span data-stu-id="017cc-116">Batch job history cleanup</span></span> | <span data-ttu-id="017cc-117">1 keer per maand</span><span class="sxs-lookup"><span data-stu-id="017cc-117">1 time per month</span></span> |
| <span data-ttu-id="017cc-118">Exportfasering opschonen</span><span class="sxs-lookup"><span data-stu-id="017cc-118">Export staging cleanup</span></span> | <span data-ttu-id="017cc-119">1 keer per dag</span><span class="sxs-lookup"><span data-stu-id="017cc-119">1 time per day</span></span> |
| <span data-ttu-id="017cc-120">Gemist synchronisatieverzoek Common Data Service-integratie</span><span class="sxs-lookup"><span data-stu-id="017cc-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="017cc-121">1 keer per dag</span><span class="sxs-lookup"><span data-stu-id="017cc-121">1 time per day</span></span> |
| <span data-ttu-id="017cc-122">Systeemtaak voor databasecompressie die regelmatig moet worden uitgevoerd buiten kantooruren</span><span class="sxs-lookup"><span data-stu-id="017cc-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="017cc-123">1 keer per dag</span><span class="sxs-lookup"><span data-stu-id="017cc-123">1 time per day</span></span> |
| <span data-ttu-id="017cc-124">Systeemtaak voor opnieuw samenstellen van de database-index die regelmatig moet worden uitgevoerd buiten kantooruren</span><span class="sxs-lookup"><span data-stu-id="017cc-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="017cc-125">1 keer per dag</span><span class="sxs-lookup"><span data-stu-id="017cc-125">1 time per day</span></span> |

1. <span data-ttu-id="017cc-126">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="017cc-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="017cc-127">Zoek in de **Zoek**-balk naar een van de bovenstaande batchtaken.</span><span class="sxs-lookup"><span data-stu-id="017cc-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="017cc-128">Selecteer **Uitvoeren op de achtergrond** en selecteer **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="017cc-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Stel terugkeerpatroon in](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="017cc-130">Geef onder **Terugkeerpatroon definiëren** de **Begindatum** en **Begintijd** op die buiten werktijd of in het weekend vallen.</span><span class="sxs-lookup"><span data-stu-id="017cc-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="017cc-131">Selecteer **Geen einddatum**.</span><span class="sxs-lookup"><span data-stu-id="017cc-131">Select **No end date**.</span></span> 

   ![Definieer begindatum en -tijd van het terugkeerpatroon](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="017cc-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="017cc-133">Select **OK**.</span></span>

6. <span data-ttu-id="017cc-134">Wijzig zo nodig andere parameters onder **Uitvoeren op de achtergrond** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="017cc-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="017cc-135">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="017cc-135">Additional resources</span></span>

[<span data-ttu-id="017cc-136">Prestaties optimaliseren met automatische opschoningstaken</span><span class="sxs-lookup"><span data-stu-id="017cc-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
