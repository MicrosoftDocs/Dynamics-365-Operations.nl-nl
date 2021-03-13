---
title: Een planningstaak annuleren
description: In dit onderwerp wordt uitgelegd hoe u een actieve planningstaak kunt annuleren die gebruikmaakt van de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 7cee11e6d9e8bc2fe83f5369554ae9ff9ee2b741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008211"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="436cc-103">Een planningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="436cc-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="436cc-104">In Microsoft Dynamics 365 Supply Chain Management kunt u een actieve planningstaak annuleren die gebruikmaakt van de functionaliteit Planningsoptimalisatie.</span><span class="sxs-lookup"><span data-stu-id="436cc-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="436cc-105">Wanneer u **Annuleren** selecteert in het dialoogvenster wanneer een taak voor Planningsoptimalisatie rechtstreeks vanuit de gebruikersinterface wordt geactiveerd (niet op de achtergrond), wordt de taak voor Planningsoptimalisatie niet geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="436cc-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="436cc-106">Zelfs als u een waarschuwing ontvangt zoals 'Bewerking geannuleerd', moet u nog steeds de volgende stappen uitvoeren om een planningstaak met Planningsoptimalisatie te annuleren.</span><span class="sxs-lookup"><span data-stu-id="436cc-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="436cc-107">Voer de volgende stappen uit om een actieve planningstaak te annuleren.</span><span class="sxs-lookup"><span data-stu-id="436cc-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="436cc-108">Alleen actieve taken kunnen worden geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="436cc-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="436cc-109">Ga naar **Hoofdplanning \> Instellingen \> Plannen**.</span><span class="sxs-lookup"><span data-stu-id="436cc-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="436cc-110">Selecteer een geschikt plan voor de planningsuitvoering.</span><span class="sxs-lookup"><span data-stu-id="436cc-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="436cc-111">Selecteer **Historie**.</span><span class="sxs-lookup"><span data-stu-id="436cc-111">Select **History**.</span></span>
4. <span data-ttu-id="436cc-112">Selecteer de planningstaak die u wilt annuleren</span><span class="sxs-lookup"><span data-stu-id="436cc-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="436cc-113">Selecteer **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="436cc-113">Select **Cancel**.</span></span>

<span data-ttu-id="436cc-114">De taakstatus is **Annuleren** totdat de service Optimalisatie van planning bevestigt dat de taak is geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="436cc-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="436cc-115">De status wordt vervolgens gewijzigd in **Geannuleerd**.</span><span class="sxs-lookup"><span data-stu-id="436cc-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="436cc-116">Als u statuswijzigingen wilt bekijken, moet u de pagina vernieuwen door op de knop **Vernieuwen** te klikken.</span><span class="sxs-lookup"><span data-stu-id="436cc-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="436cc-117">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="436cc-117">Additional resources</span></span>

[<span data-ttu-id="436cc-118">Overzicht van Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="436cc-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="436cc-119">Aan de slag met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="436cc-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="436cc-120">Analyse voor passende Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="436cc-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="436cc-121">Planhistorie en planningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="436cc-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="436cc-122">Filters op een plan toepassen</span><span class="sxs-lookup"><span data-stu-id="436cc-122">Apply filters to a plan</span></span>](plan-filters.md)
