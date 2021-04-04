---
title: Een batchtaak maken
description: Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 753a78dd140ca82c8c42ff8fdd3772e66b5a1cb0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571072"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="13c82-103">Een batchtaak maken</span><span class="sxs-lookup"><span data-stu-id="13c82-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13c82-104">Een batchtaak is een groep taken die voor automatische verwerking naar een AOS-exemplaar (Application Object Server) worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="13c82-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="13c82-105">Batchtaken worden uitgevoerd met behulp van de beveiligingsgegevens van de gebruiker die de taak heeft gemaakt.</span><span class="sxs-lookup"><span data-stu-id="13c82-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="13c82-106">Voer de volgende procedure uit om een batchtaak te maken.</span><span class="sxs-lookup"><span data-stu-id="13c82-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="13c82-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="13c82-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="13c82-108">De batchtaak maken</span><span class="sxs-lookup"><span data-stu-id="13c82-108">Create the batch job</span></span>
1. <span data-ttu-id="13c82-109">Ga naar **Navigatievenster > Modules > Systeembeheer > Query's > Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="13c82-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="13c82-110">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="13c82-110">Click **New**.</span></span>
3. <span data-ttu-id="13c82-111">Typ een waarde in het veld **Taakomschrijving**.</span><span class="sxs-lookup"><span data-stu-id="13c82-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="13c82-112">Typ een datum en een tijd in het veld **Geplande begindatum/tijd**.</span><span class="sxs-lookup"><span data-stu-id="13c82-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="13c82-113">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="13c82-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="13c82-114">Een terugkeerpatroon maken</span><span class="sxs-lookup"><span data-stu-id="13c82-114">Create a recurrence</span></span>
1. <span data-ttu-id="13c82-115">Klik in het actievenster op **Batchtaak**.</span><span class="sxs-lookup"><span data-stu-id="13c82-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="13c82-116">Klik op **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="13c82-116">Click **Recurrence**.</span></span> <span data-ttu-id="13c82-117">Gebruik deze opties om een bereik en terugkeerpatroon in te voeren.</span><span class="sxs-lookup"><span data-stu-id="13c82-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="13c82-118">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="13c82-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="13c82-119">Waarschuwingen toevoegen</span><span class="sxs-lookup"><span data-stu-id="13c82-119">Add alerts</span></span>
1. <span data-ttu-id="13c82-120">Klik in het actievenster op **Batchtaak**.</span><span class="sxs-lookup"><span data-stu-id="13c82-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="13c82-121">Klik op **Waarschuwingen**.</span><span class="sxs-lookup"><span data-stu-id="13c82-121">Click **Alerts**.</span></span> <span data-ttu-id="13c82-122">Geef aan of u waarschuwingsberichten wilt laten verzenden wanneer de batchtaak is voltooid, wanneer er een fout optreedt of wanneer de batchtaak wordt geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="13c82-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="13c82-123">Geef vervolgens op of u waarschuwingen wilt laten weergeven als pop-upberichten.</span><span class="sxs-lookup"><span data-stu-id="13c82-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="13c82-124">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="13c82-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="13c82-125">Status van batchtaak aanpassen</span><span class="sxs-lookup"><span data-stu-id="13c82-125">Adjust batch job status</span></span>
1. <span data-ttu-id="13c82-126">Ga naar **Systeembeheer > Query's > Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="13c82-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="13c82-127">Selecteer de gewenste batchtaak.</span><span class="sxs-lookup"><span data-stu-id="13c82-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="13c82-128">Klik in het actievenster op **Batchtaak > Functies > Status wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="13c82-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="13c82-129">Selecteer de gewenste status:</span><span class="sxs-lookup"><span data-stu-id="13c82-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="13c82-130">**Inhouden**: stel de batchtaak in op **Inhouden**, zodat deze niet wordt opgenomen in de planner van batchtaken.</span><span class="sxs-lookup"><span data-stu-id="13c82-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="13c82-131">Staat gelijk aan *Stoppen*.</span><span class="sxs-lookup"><span data-stu-id="13c82-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="13c82-132">**Wachten**: stel de batchtaak in op **Wachten** om deze in de wachtrij voor de planner van batchtaken te zetten.</span><span class="sxs-lookup"><span data-stu-id="13c82-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="13c82-133">Staat gelijk aan *Gaan*.</span><span class="sxs-lookup"><span data-stu-id="13c82-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="13c82-134">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="13c82-134">Click **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]