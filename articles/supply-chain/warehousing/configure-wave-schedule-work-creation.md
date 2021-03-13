---
title: Het maken van werk plannen tijdens waves
description: In dit onderwerp wordt beschreven hoe u de waveverwerkingsmethode Werk maken plannen instelt en gebruikt.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078248"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="86e9e-103">Het maken van werk plannen tijdens waves</span><span class="sxs-lookup"><span data-stu-id="86e9e-103">Schedule work creation during wave</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86e9e-104">Gebruik de functie *Werk maken plannen* als onderdeel van uw waveproces om de waveverwerkingsdoorvoer te verbeteren door het systeem werk te laten maken met parallelle verwerking.</span><span class="sxs-lookup"><span data-stu-id="86e9e-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="86e9e-105">Wanneer de functionaliteit is ingeschakeld, wordt automatisch gepland werk gemaakt, waarmee uiteindelijk werkelijk werk wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="86e9e-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="86e9e-106">Als het aantal waveladingregels een vooraf bepaalde drempel bereikt, wordt het werkelijke werk sneller gemaakt door parallelle asynchrone verwerking toe te passen.</span><span class="sxs-lookup"><span data-stu-id="86e9e-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="86e9e-107">De functie Werk maken plannen inschakelen</span><span class="sxs-lookup"><span data-stu-id="86e9e-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="86e9e-108">De functie in Functiebeheer inschakelen</span><span class="sxs-lookup"><span data-stu-id="86e9e-108">Enable the feature in feature management</span></span>

<span data-ttu-id="86e9e-109">Voordat u de functie *Werk maken plannen* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="86e9e-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="86e9e-110">Beheerders kunnen het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="86e9e-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="86e9e-111">De functie wordt daar op de volgende manier weergegeven:</span><span class="sxs-lookup"><span data-stu-id="86e9e-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="86e9e-112">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="86e9e-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="86e9e-113">**Functienaam:** *Werk maken plannen*</span><span class="sxs-lookup"><span data-stu-id="86e9e-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="86e9e-114">De functie *Werk blokkeren voor de hele organisatie* moet zijn ingeschakeld voordat u *Werk maken plannen* kunt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="86e9e-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="86e9e-115">Batchverwerking van waves handmatig inschakelen</span><span class="sxs-lookup"><span data-stu-id="86e9e-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="86e9e-116">Als u wilt profiteren van een parallelle asynchrone methode voor het maken van magazijnwerk, moet uw waveproces worden uitgevoerd in batch.</span><span class="sxs-lookup"><span data-stu-id="86e9e-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="86e9e-117">Dit instellen:</span><span class="sxs-lookup"><span data-stu-id="86e9e-117">To set this up:</span></span>

1. <span data-ttu-id="86e9e-118">Ga naar  **Magazijnbeheer \> Instellen \> Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="86e9e-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="86e9e-119">Stel op het tabblad **Algemeen** de optie **Waves verwerken in batch** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="86e9e-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="86e9e-120">U kunt eventueel ook een specifieke **Batchgroep voor waveverwerking** selecteren om te voorkomen dat de batchwachtrijverwerking wordt uitgevoerd op hetzelfde moment als andere processen.</span><span class="sxs-lookup"><span data-stu-id="86e9e-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="86e9e-121">Stel de **tijd Wachten op vergrendeling (ms)** in. Dit is van toepassing wanneer verschillende waves tegelijkertijd worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="86e9e-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="86e9e-122">Voor de meeste grotere waveprocessen raden we een waarde van *60000* aan.</span><span class="sxs-lookup"><span data-stu-id="86e9e-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="86e9e-123">De nieuwe wave-stapmethode voor bestaande wavesjablonen handmatig inschakelen</span><span class="sxs-lookup"><span data-stu-id="86e9e-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="86e9e-124">Begin met het maken van de nieuwe wave-stapmethode en het inschakelen van deze methode voor parallelle asynchrone taakverwerking.</span><span class="sxs-lookup"><span data-stu-id="86e9e-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="86e9e-125">Ga naar  **Magazijnbeheer \> Instellen \> Waves \> Methoden voor verwerking van waves**.</span><span class="sxs-lookup"><span data-stu-id="86e9e-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="86e9e-126">Selecteer  **Methoden opnieuw genereren** en merk op dat *WHSScheduleWorkCreationWaveStepMethod* is toegevoegd aan de lijst met waveprocesmethoden die u kunt gebruiken in uw verzendwavesjablonen.</span><span class="sxs-lookup"><span data-stu-id="86e9e-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="86e9e-127">Selecteer de record met de **methodenaam** *WHSScheduleWorkCreationWaveStepMethod* en selecteer **Taakconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="86e9e-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="86e9e-128">Selecteer in het actievenster **Nieuw** om een rij toe te voegen aan het raster en gebruik de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="86e9e-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="86e9e-129">**Magazijn**: selecteer het magazijn dat u wilt gebruiken voor de verwerking van de planning voor het maken van werk.</span><span class="sxs-lookup"><span data-stu-id="86e9e-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="86e9e-130">**Maximum aantal batchtaken**: een maximum aantal batchtaken opgeven.</span><span class="sxs-lookup"><span data-stu-id="86e9e-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="86e9e-131">In de meeste gevallen moet deze waarde binnen het bereik van 8-16 liggen, maar we raden u aan om te experimenteren met de optimale instelling voor uw scenario's.</span><span class="sxs-lookup"><span data-stu-id="86e9e-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="86e9e-132">**Batchgroep voor verwerking van waves**: selecteer een specifieke batchgroep voor verwerking van uw waves om de batchwachtrijverwerking te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="86e9e-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="86e9e-133">U kunt nu een bestaande wavesjabloon bijwerken (of een nieuwe sjabloon maken) om de waveverwerkingsmethode *Werk maken plannen* te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="86e9e-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="86e9e-134">Ga naar  **Magazijnbeheer  \> Instellen \> Waves \> Wavesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="86e9e-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="86e9e-135">Selecteer **Bewerken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="86e9e-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="86e9e-136">Selecteer in het lijstdeelvenster de wavesjabloon die u wilt bijwerken (als u test met demonstratiegegevens, kunt u *24 Standaardverzending* gebruiken).</span><span class="sxs-lookup"><span data-stu-id="86e9e-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="86e9e-137">Vouw het sneltabblad **Methoden** uit en selecteer de rij met de **naam** *Werk maken plannen* in het raster **Resterende methoden**.</span><span class="sxs-lookup"><span data-stu-id="86e9e-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="86e9e-138">Selecteer de pijl die naar de kolom **Geselecteerde methoden** verwijst om de geselecteerde rij naar die kolom te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="86e9e-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="86e9e-139">(U kunt slechts één geselecteerde methode tegelijk gebruiken waarbij ofwel *WHSScheduleWorkCreationWaveStepMethod* of *createWork* wordt gebruikt zodat de bestaande rij met **Methodenaam** *createWork* automatisch wordt verplaatst naar het raster **Resterende methoden**.)</span><span class="sxs-lookup"><span data-stu-id="86e9e-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="86e9e-140">Drempelgegevens voor wavetaakverwerking instellen</span><span class="sxs-lookup"><span data-stu-id="86e9e-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="86e9e-141">Het systeem maakt standaarddrempelgegevens voor wave-taakverwerking wanneer een waveproces voor de eerste keer met behulp van op taken gebaseerde verwerking wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="86e9e-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="86e9e-142">De gegevens worden gebruikt om te bepalen wanneer waveverwerking asynchroon wordt uitgevoerd en op taken is gebaseerd, waardoor werk parallel kan worden verwerkt en gemaakt.</span><span class="sxs-lookup"><span data-stu-id="86e9e-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="86e9e-143">De standaardgegevens gebruiken in eerste instantie een drempelwaarde van 15 voor het minimum aantal belastingregels (MINIMUMLOADLINES).</span><span class="sxs-lookup"><span data-stu-id="86e9e-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="86e9e-144">Dit betekent dat wanneer het systeem een wave met meer dan 15 belastingregels verwerkt, asynchrone taakverwerking wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="86e9e-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="86e9e-145">U kunt deze gegevens handmatig invoegen/bijwerken in de tabel **WHSWaveTaskProcessingThresholdParameters** in uw testomgevingen. Als u deze instelling in een productieomgeving wilt wijzigen, moet u contact opnemen met Microsoft Support om de update aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="86e9e-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="86e9e-146">Werken met de functie</span><span class="sxs-lookup"><span data-stu-id="86e9e-146">Work with the feature</span></span>

<span data-ttu-id="86e9e-147">Wanneer de functie *Werk maken plannen* is ingeschakeld, wordt er door waveverwerking gepland werk gemaakt, dat uiteindelijk wordt gebruikt door het nieuwe werkaanmaakproces.</span><span class="sxs-lookup"><span data-stu-id="86e9e-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="86e9e-148">Tijdens het maken van het werk wordt het werk geblokkeerd met de functie *Werk blokkeren voor de hele organisatie*.</span><span class="sxs-lookup"><span data-stu-id="86e9e-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="86e9e-149">In het volgende stroomdiagram is te zien hoe gepland werk tijdens de verwerking van waves wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="86e9e-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Werk maken plannen](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="86e9e-151">Gepland werk</span><span class="sxs-lookup"><span data-stu-id="86e9e-151">Planned work</span></span>

<span data-ttu-id="86e9e-152">Op de pagina **Details gepland werk** (**Magazijnbeheer \> Werk \> Details gepland werk**) ziet u info over het geplande werk dat aanvankelijk is gemaakt tijdens waveverwerking.</span><span class="sxs-lookup"><span data-stu-id="86e9e-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="86e9e-153">De volgende waarden **Processtatus** zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="86e9e-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="86e9e-154">**In de wachtrij**: het geplande werk wacht om te worden gebruikt om werk te maken.</span><span class="sxs-lookup"><span data-stu-id="86e9e-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="86e9e-155">**Voltooid** - Het geplande werk is gebruikt om werk te maken.</span><span class="sxs-lookup"><span data-stu-id="86e9e-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="86e9e-156">**Mislukt:** de waveverwerking is mislukt.</span><span class="sxs-lookup"><span data-stu-id="86e9e-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="86e9e-157">Houd er rekening mee dat het geplande werk een status **Mislukt** kan hebben met of zonder bijbehorend werkelijk werk.</span><span class="sxs-lookup"><span data-stu-id="86e9e-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="86e9e-158">Wanneer het daadwerkelijke maken van het werk mislukt, blijft de status van het werkelijke werk *Geannuleerd*.</span><span class="sxs-lookup"><span data-stu-id="86e9e-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="86e9e-159">Batchtaak voor werk maken</span><span class="sxs-lookup"><span data-stu-id="86e9e-159">Batch job for the work creation process</span></span>

<span data-ttu-id="86e9e-160">Als u de batchtaken voor het verwerken van waves wilt weergeven, selecteert u **Batchtaken** in het actievenster op de pagina **Alle waves**.</span><span class="sxs-lookup"><span data-stu-id="86e9e-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="86e9e-161">In deze weergave kunt u alle details van de batchtaak voor elk van de batchtaak-ID´s weergeven.</span><span class="sxs-lookup"><span data-stu-id="86e9e-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>
