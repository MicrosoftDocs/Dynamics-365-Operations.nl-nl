---
title: Een experiment verbinden en variaties bewerken
description: In dit onderwerp wordt beschreven hoe u een experiment in een service van derden verbindt met Dynamics 365 Commerce en hoe u variaties voor het experiment bewerkt.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930174"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="02cde-103">Een experiment verbinden en variaties bewerken</span><span class="sxs-lookup"><span data-stu-id="02cde-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="02cde-104">In dit onderwerp wordt beschreven hoe u uw experiment in Commerce verbindt en hoe u wijzigingen in uw variaties kunt aanpassen zodat u ze op één lijn kunt brengen met uw hypothese.</span><span class="sxs-lookup"><span data-stu-id="02cde-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so they align with your hypothesis.</span></span> <span data-ttu-id="02cde-105">In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="02cde-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="02cde-106">Extra stappen worden in afzonderlijke onderwerpen behandeld.</span><span class="sxs-lookup"><span data-stu-id="02cde-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="02cde-107">[ ![Traject van gebruiker voor experimenten - verbinden en bewerken](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="02cde-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="02cde-108">Nadat u [uw experiment hebt ingesteld](experimentation-setup.md) in een service van derden, verbindt u het experiment in Dynamics 365 Commerce en bewerkt u de experimentvariaties.</span><span class="sxs-lookup"><span data-stu-id="02cde-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="02cde-109">Overwegingen bij het plannen</span><span class="sxs-lookup"><span data-stu-id="02cde-109">Planning considerations</span></span>

<span data-ttu-id="02cde-110">Voordat u uw experiment in Commerce verbindt, moet u enkele beslissingen nemen die van invloed zijn op de manier waarop uw inhoud door Commerce wordt beheerd.</span><span class="sxs-lookup"><span data-stu-id="02cde-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="02cde-111">Het bereik van uw experiment bepalen</span><span class="sxs-lookup"><span data-stu-id="02cde-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="02cde-112">Wanneer u een experiment verbindt, wordt u gevraagd het bereik van het experiment te definiëren.</span><span class="sxs-lookup"><span data-stu-id="02cde-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="02cde-113">Experimenten worden gedefinieerd als een **gedeeltelijk** bereik of een **volledig** bereik.</span><span class="sxs-lookup"><span data-stu-id="02cde-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="02cde-114">Kies **gedeeltelijk** als u een experiment wilt uitvoeren op een specifiek gedeelte van een pagina.</span><span class="sxs-lookup"><span data-stu-id="02cde-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="02cde-115">Als u deze optie selecteert, moet u bepalen welke modules in het experiment worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="02cde-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="02cde-116">Wijzigingen die worden aangebracht in delen van de standaardpagina of het fragment die niet zijn gerelateerd aan het experiment, worden automatisch gesynchroniseerd in verschillende variaties.</span><span class="sxs-lookup"><span data-stu-id="02cde-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="02cde-117">Kies **volledig** als u een experiment wilt uitvoeren op een volledige pagina of in een volledig fragment.</span><span class="sxs-lookup"><span data-stu-id="02cde-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="02cde-118">Er worden afzonderlijke kopieën van de standaardpagina of het standaardfragment gemaakt.</span><span class="sxs-lookup"><span data-stu-id="02cde-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="02cde-119">U hoeft niet te selecteren welke modules in het experiment worden opgenomen, omdat het gehele bewerkingsoppervlak kan worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="02cde-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="02cde-120">U kunt modules naar behoefte toevoegen, verwijderen en opnieuw rangschikken.</span><span class="sxs-lookup"><span data-stu-id="02cde-120">You can add, delete, and re-order modules as needed.</span></span> <span data-ttu-id="02cde-121">Als er echter wijzigingen zijn aangebracht in de standaardpagina of het standaardfragment waaraan het experiment is gekoppeld, moeten deze wijzigingen handmatig worden gesynchroniseerd in alle variaties.</span><span class="sxs-lookup"><span data-stu-id="02cde-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="02cde-122">Als u uw experiment koppelt aan een pagina waarin een indeling wordt gebruikt, kunt u als bereik voor het experiment alleen **volledig** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="02cde-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="02cde-123">Bepaal of u wilt plannen wanneer uw experiment wordt gepubliceerd</span><span class="sxs-lookup"><span data-stu-id="02cde-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="02cde-124">Als u wilt plannen wanneer uw experiment wordt gepubliceerd naar uw live site, moet u ervoor zorgen dat de inhoud die u aan het experiment wilt koppelen, beschikbaar is in een publicatiegroep *voordat* u het experiment verbindt.</span><span class="sxs-lookup"><span data-stu-id="02cde-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="02cde-125">Zie [Werken met publicatiegroepen](publish-groups.md) voor meer informatie over publicatiegroepen.</span><span class="sxs-lookup"><span data-stu-id="02cde-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="02cde-126">Uw experiment verbinden</span><span class="sxs-lookup"><span data-stu-id="02cde-126">Connect your experiment</span></span>
<span data-ttu-id="02cde-127">Als u uw experiment wilt verbinden, start u de wizard **Experiment verbinden**.</span><span class="sxs-lookup"><span data-stu-id="02cde-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="02cde-128">De wizard leidt u door de stappen die nodig zijn om uw experiment te verbinden.</span><span class="sxs-lookup"><span data-stu-id="02cde-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="02cde-129">Wanneer u de wizard voltooit, wordt uw experiment verbonden en worden variaties gemaakt en kunnen ze worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="02cde-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

1. <span data-ttu-id="02cde-130">Als u de wizard wilt starten, selecteert u het tabblad **Experimenten** in Site Builder en selecteert u vervolgens **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="02cde-130">To launch the wizard, select the **Experiments** tab in site builder and then select **Connect**.</span></span> <span data-ttu-id="02cde-131">U kunt de wizard ook openen via een pagina- of fragmenteditor.</span><span class="sxs-lookup"><span data-stu-id="02cde-131">Alternatively, the wizard can be accessed from a page or fragment editor.</span></span> <span data-ttu-id="02cde-132">Selecteer **Experiment verbinden** op de opdrachtbalk in de bewerkingsmodus.</span><span class="sxs-lookup"><span data-stu-id="02cde-132">In edit mode, select **Connect experiment** in the command bar.</span></span>

> [!NOTE]
> <span data-ttu-id="02cde-133">Een pagina kan slechts met één experiment tegelijk worden verbonden.</span><span class="sxs-lookup"><span data-stu-id="02cde-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="02cde-134">Als u een pagina wilt verbinden met een ander experiment, verwijdert u eerst het experiment waarmee de pagina momenteel is verbonden.</span><span class="sxs-lookup"><span data-stu-id="02cde-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="02cde-135">Kies de pagina of het fragment waarop u het experiment wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="02cde-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="02cde-136">Stel het experimentbereik in op **gedeeltelijk** of **volledig**, afhankelijk van de keuze die u hebt gemaakt in de sectie [Het bereik van uw experiment bepalen](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="02cde-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="02cde-137">De functievlag **Experimenten op pagina's of fragmenten** moet zijn ingeschakeld als u een experiment op een volledige pagina of in een volledig fragment wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="02cde-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="02cde-138">Raadpleeg het onderwerp [Experimenten in Dynamics 365 Commerce](experimentation-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="02cde-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="02cde-139">In de laatste stap van de wizard selecteert u de optie **Variaties genereren en wizard afsluiten**.</span><span class="sxs-lookup"><span data-stu-id="02cde-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="02cde-140">Er worden variaties voor het experiment gemaakt.</span><span class="sxs-lookup"><span data-stu-id="02cde-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="02cde-141">Uw variaties bewerken</span><span class="sxs-lookup"><span data-stu-id="02cde-141">Edit your variations</span></span>
<span data-ttu-id="02cde-142">Wanneer u de wizard afsluit, worden er variaties voor u gemaakt.</span><span class="sxs-lookup"><span data-stu-id="02cde-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="02cde-143">Vervolgens bewerkt u de variaties zodat deze de keuzes weergeven die u in de experimenthypothese moet controleren.</span><span class="sxs-lookup"><span data-stu-id="02cde-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="02cde-144">Kies een van de volgende procedures die overeenkomen met het bereik dat u voor uw experiment hebt gekozen in de bovenstaande sectie [Het bereik van uw experiment bepalen](#determine-the-scope-of-your-experiment).</span><span class="sxs-lookup"><span data-stu-id="02cde-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="02cde-145">Variaties bewerken voor experimenten met een gedeeltelijk bereik</span><span class="sxs-lookup"><span data-stu-id="02cde-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="02cde-146">Voer de volgende stappen uit als u het bereik van uw experiment als **gedeeltelijk** hebt gedefinieerd in de wizard **Experiment verbinden**.</span><span class="sxs-lookup"><span data-stu-id="02cde-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="02cde-147">Gebruik in de editorweergave het vervolgkeuzemenu voor variaties onder de opdrachtbalk om elke variatie te bewerken op basis van uw oorspronkelijke hypothese.</span><span class="sxs-lookup"><span data-stu-id="02cde-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="02cde-148">U kunt ook een besturingselement of basisvariatie instellen door een van de variaties ongewijzigd te laten.</span><span class="sxs-lookup"><span data-stu-id="02cde-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="02cde-149">Selecteer de module waarop u een experiment wilt uitvoeren, selecteer het weglatingsteken (...) en selecteer vervolgens **Toevoegen aan experiment**.</span><span class="sxs-lookup"><span data-stu-id="02cde-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="02cde-150">Variaties bewerken voor experimenten met een volledig bereik</span><span class="sxs-lookup"><span data-stu-id="02cde-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="02cde-151">Als u het bereik van uw experiment als **volledig** hebt gedefinieerd in de wizard **Experiment verbinden** terwijl u in de editorweergave werkt, gebruikt u het vervolgkeuzemenu voor variaties onder de opdrachtbalk om elke variatie te bewerken op basis van uw oorspronkelijke hypothese.</span><span class="sxs-lookup"><span data-stu-id="02cde-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="02cde-152">In beide gevallen kunt u ook een besturingselement of basisvariatie instellen door een van de variaties ongewijzigd te laten.</span><span class="sxs-lookup"><span data-stu-id="02cde-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="02cde-153">Vorige stap</span><span class="sxs-lookup"><span data-stu-id="02cde-153">Previous step</span></span>
[<span data-ttu-id="02cde-154">Een experiment instellen</span><span class="sxs-lookup"><span data-stu-id="02cde-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="02cde-155">Volgende stap</span><span class="sxs-lookup"><span data-stu-id="02cde-155">Next step</span></span>
[<span data-ttu-id="02cde-156">Preview van een experiment weergeven en een experiment publiceren</span><span class="sxs-lookup"><span data-stu-id="02cde-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)