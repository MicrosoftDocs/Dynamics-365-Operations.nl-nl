---
title: Prestaties optimaliseren door batchtaken na werktijd te plannen
description: In dit onderwerp wordt uitgelegd hoe u prestatieproblemen met Microsoft Dynamics 365 Human Resources kunt oplossen door de batchtaken met een lange uitvoeringsduur na werktijd in te plannen.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 452a87cf5ba6c1ac73636584d75b2ec2ac555e02
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527760"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="28b0c-103">Prestaties optimaliseren door batchtaken na werktijd te plannen</span><span class="sxs-lookup"><span data-stu-id="28b0c-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="28b0c-104">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="28b0c-104">Issue</span></span>

<span data-ttu-id="28b0c-105">De prestaties van Microsoft Dynamics 365 Human Resources kunnen problemen ondervinden als langlopende batchtaken tijdens normale werktijden worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="28b0c-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="28b0c-106">Oplossing</span><span class="sxs-lookup"><span data-stu-id="28b0c-106">Resolution</span></span>

<span data-ttu-id="28b0c-107">Plan de volgende batchtaken in na werktijd.</span><span class="sxs-lookup"><span data-stu-id="28b0c-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="28b0c-108">We raden ook aan de frequentie te evalueren van batchtaken die regelmatig worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="28b0c-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="28b0c-109">Verminder zo mogelijk het herhalingspatroon van de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="28b0c-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="28b0c-110">In veel gevallen is de standaardfrequentie voldoende.</span><span class="sxs-lookup"><span data-stu-id="28b0c-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="28b0c-111">De volgende batchtaken kunnen beter 's nachts of na werktijd worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="28b0c-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="28b0c-112">Controleer ook de tijdzone voor deze herhalende batchtaken.</span><span class="sxs-lookup"><span data-stu-id="28b0c-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="28b0c-113">Er zijn batchtaken die mogelijk een andere tijdzone gebruiken.</span><span class="sxs-lookup"><span data-stu-id="28b0c-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="28b0c-114">Batchtaak</span><span class="sxs-lookup"><span data-stu-id="28b0c-114">Batch job</span></span> | <span data-ttu-id="28b0c-115">Standaard herhalingspatroon</span><span class="sxs-lookup"><span data-stu-id="28b0c-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="28b0c-116">Batchtaakhistorie opschonen</span><span class="sxs-lookup"><span data-stu-id="28b0c-116">Batch job history cleanup</span></span> | <span data-ttu-id="28b0c-117">1 keer per maand</span><span class="sxs-lookup"><span data-stu-id="28b0c-117">1 time per month</span></span> |
| <span data-ttu-id="28b0c-118">Exportfasering opschonen</span><span class="sxs-lookup"><span data-stu-id="28b0c-118">Export staging cleanup</span></span> | <span data-ttu-id="28b0c-119">1 keer per dag</span><span class="sxs-lookup"><span data-stu-id="28b0c-119">1 time per day</span></span> |
| <span data-ttu-id="28b0c-120">Gemist synchronisatieverzoek Common Data Service-integratie</span><span class="sxs-lookup"><span data-stu-id="28b0c-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="28b0c-121">1 keer per dag</span><span class="sxs-lookup"><span data-stu-id="28b0c-121">1 time per day</span></span> |
| <span data-ttu-id="28b0c-122">Systeemtaak voor databasecompressie die regelmatig moet worden uitgevoerd buiten kantooruren</span><span class="sxs-lookup"><span data-stu-id="28b0c-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="28b0c-123">1 keer per dag</span><span class="sxs-lookup"><span data-stu-id="28b0c-123">1 time per day</span></span> |
| <span data-ttu-id="28b0c-124">Systeemtaak voor opnieuw samenstellen van de database-index die regelmatig moet worden uitgevoerd buiten kantooruren</span><span class="sxs-lookup"><span data-stu-id="28b0c-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="28b0c-125">1 keer per dag</span><span class="sxs-lookup"><span data-stu-id="28b0c-125">1 time per day</span></span> |

1. <span data-ttu-id="28b0c-126">Selecteer in Human Resources de optie **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="28b0c-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="28b0c-127">Zoek in de **Zoek**-balk naar een van de bovenstaande batchtaken.</span><span class="sxs-lookup"><span data-stu-id="28b0c-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="28b0c-128">Selecteer **Uitvoeren op de achtergrond** en selecteer **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="28b0c-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Stel terugkeerpatroon in](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="28b0c-130">Geef onder **Terugkeerpatroon definiëren** de **Begindatum** en **Begintijd** op die buiten werktijd of in het weekend vallen.</span><span class="sxs-lookup"><span data-stu-id="28b0c-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="28b0c-131">Selecteer **Geen einddatum**.</span><span class="sxs-lookup"><span data-stu-id="28b0c-131">Select **No end date**.</span></span> 

   ![Definieer begindatum en -tijd van het terugkeerpatroon](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="28b0c-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="28b0c-133">Select **OK**.</span></span>

6. <span data-ttu-id="28b0c-134">Wijzig zo nodig andere parameters onder **Uitvoeren op de achtergrond** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="28b0c-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28b0c-135">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="28b0c-135">Additional resources</span></span>

[<span data-ttu-id="28b0c-136">Prestaties optimaliseren met automatische opschoningstaken</span><span class="sxs-lookup"><span data-stu-id="28b0c-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
