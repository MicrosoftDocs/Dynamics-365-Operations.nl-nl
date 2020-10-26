---
title: Een preview van een experiment weergeven en een experiment publiceren
description: In dit onderwerp wordt beschreven hoe u een preview van een experiment weergeeft en een experiment publiceert in Dynamics 365 Commerce.
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
ms.openlocfilehash: 91e2e4840a2d53f195d881279050b6415d48b070
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930173"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="8c371-103">Een preview van een experiment weergeven en een experiment publiceren</span><span class="sxs-lookup"><span data-stu-id="8c371-103">Preview and publish an experiment</span></span>

<span data-ttu-id="8c371-104">In dit onderwerp wordt beschreven hoe u een preview van uw experiment kunt weergeven en uw experiment kunt publiceren in Dynamics 365 Commerce nadat u [uw experiment hebt verbonden en uw variaties hebt bewerkt](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="8c371-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="8c371-105">In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8c371-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8c371-106">Extra stappen worden in afzonderlijke onderwerpen behandeld.</span><span class="sxs-lookup"><span data-stu-id="8c371-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="8c371-107">[ ![Traject van gebruiker voor experimenten - preview weergeven en publiceren](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="8c371-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="8c371-108">Een preview van uw experimentvariaties weergeven</span><span class="sxs-lookup"><span data-stu-id="8c371-108">Preview your experiment variations</span></span>
<span data-ttu-id="8c371-109">U kunt een preview van uw variaties weergeven en ze verder bewerken totdat ze er naar wens uitzien.</span><span class="sxs-lookup"><span data-stu-id="8c371-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

1. <span data-ttu-id="8c371-110">Gebruik in Site Builder het vervolgkeuzemenu voor variaties onder de opdrachtbalk om de inhoud te selecteren die u wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="8c371-110">In site builder, use the variations drop-down menu below the command bar to select the content you want to preview.</span></span> 
1. <span data-ttu-id="8c371-111">Selecteer **Preview** op de bovenste balk.</span><span class="sxs-lookup"><span data-stu-id="8c371-111">Select **Preview** in the top bar.</span></span> <span data-ttu-id="8c371-112">Er wordt een preview weergegeven van hoe de inhoud eruit ziet wanneer deze wordt gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="8c371-112">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="8c371-113">Als u een preview van een andere variatie wilt weergeven, selecteert u deze in het vervolgkeuzemenu voor variaties en selecteert u opnieuw **Preview**.</span><span class="sxs-lookup"><span data-stu-id="8c371-113">To preview a different variation, select it from the variation drop-down and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="8c371-114">Uw experiment publiceren</span><span class="sxs-lookup"><span data-stu-id="8c371-114">Publish your experiment</span></span>
<span data-ttu-id="8c371-115">Als u geen publicatiegroep gebruikt om te plannen wanneer het experiment live gaat en u onmiddellijk wilt publiceren, selecteert u **Publiceren** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="8c371-115">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="8c371-116">Alle variaties die bij het experiment horen, worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="8c371-116">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="8c371-117">Als de pagina een niet-gepubliceerde URL heeft, moet u de URL eerst publiceren. Anders is deze niet zichtbaar voor de gebruikers van uw website.</span><span class="sxs-lookup"><span data-stu-id="8c371-117">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="8c371-118">Zie [Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8c371-118">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="8c371-119">Publicatiegroepen gebruiken om te plannen wanneer uw experiment live gaat</span><span class="sxs-lookup"><span data-stu-id="8c371-119">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="8c371-120">Variaties die in Site Builder zijn gemaakt, kunnen worden gepland voor publicatie met behulp van een publicatiegroep.</span><span class="sxs-lookup"><span data-stu-id="8c371-120">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="8c371-121">Binnen een publicatiegroep kunt u een pagina of een fragment verbinden met uw experiment door naar het tabblad **Experimenten** of het tabblad **Pagina´s** of **Fragmenten** te gaan. Zie het onderwerp [Een experiment verbinden en variaties bewerken](experimentation-connect-edit.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8c371-121">Within a publish group, you can connect a page or fragment to your experiment by going to the **Experiments** tab or the **Pages** or **Fragments** tab. For more information, see [Connect an experiment and edit variations](experimentation-connect-edit.md) topic.</span></span> <span data-ttu-id="8c371-122">Zie [Werken met publicatiegroepen](publish-groups.md) voor informatie over publicatiegroepen.</span><span class="sxs-lookup"><span data-stu-id="8c371-122">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="8c371-123">Wanneer u publicatiegroepen gebruikt bij experimenten, moet u rekening houden met een aantal belangrijke aandachtspunten.</span><span class="sxs-lookup"><span data-stu-id="8c371-123">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="8c371-124">Wanneer u een pagina of fragment toevoegt waarop een experiment wordt uitgevoerd naar een publicatiegroep, wordt het experiment verwijderd uit de pagina of het fragment in de publicatiegroep.</span><span class="sxs-lookup"><span data-stu-id="8c371-124">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="8c371-125">Experimenten die zijn verbonden met pagina's op een live site, zijn niet beschikbaar voor pagina's binnen publicatiegroepen en andersom.</span><span class="sxs-lookup"><span data-stu-id="8c371-125">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="8c371-126">Op dezelfde manier zijn pagina's waarop experimenten zijn uitgevoerd op een live site niet beschikbaar voor andere experimenten in publicatiegroepen en andersom.</span><span class="sxs-lookup"><span data-stu-id="8c371-126">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="8c371-127">Wanneer u een publicatiegroep publiceert of plant, wordt alle inhoud in de publicatiegroep gepubliceerd, ongeacht of er een experiment aan de publicatiegroep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="8c371-127">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="8c371-128">Omdat een publicatiegroep blijft behouden nadat deze naar een live site is gepubliceerd, blijven experimenten in de publicatiegroep ook behouden.</span><span class="sxs-lookup"><span data-stu-id="8c371-128">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="8c371-129">Daarom kunt u geen andere experimenten koppelen aan dezelfde pagina of hetzelfde fragment.</span><span class="sxs-lookup"><span data-stu-id="8c371-129">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="8c371-130">Om deze beperking te voorkomen moet u alle publicatiegroepen met persistente experimenten verwijderen.</span><span class="sxs-lookup"><span data-stu-id="8c371-130">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="8c371-131">Zo geldt ook dat als u een experiment op een live site wilt verwijderen dat ook in een publicatiegroep bestaat, u het eerst moet verwijderen uit de publicatiegroep.</span><span class="sxs-lookup"><span data-stu-id="8c371-131">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="8c371-132">Vorige stap</span><span class="sxs-lookup"><span data-stu-id="8c371-132">Previous step</span></span>
[<span data-ttu-id="8c371-133">Een experiment verbinden en bewerken</span><span class="sxs-lookup"><span data-stu-id="8c371-133">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="8c371-134">Volgende stap</span><span class="sxs-lookup"><span data-stu-id="8c371-134">Next step</span></span>
[<span data-ttu-id="8c371-135">Een experiment uitvoeren en controleren</span><span class="sxs-lookup"><span data-stu-id="8c371-135">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
