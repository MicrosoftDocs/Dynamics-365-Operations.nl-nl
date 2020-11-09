---
title: Een preview van een experiment weergeven en een experiment publiceren
description: In dit onderwerp wordt beschreven hoe u een preview van een experiment weergeeft en een experiment publiceert in Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
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
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097111"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="db235-103">Een preview van een experiment weergeven en een experiment publiceren</span><span class="sxs-lookup"><span data-stu-id="db235-103">Preview and publish an experiment</span></span>

<span data-ttu-id="db235-104">In dit onderwerp wordt beschreven hoe u een preview van uw experiment kunt weergeven en uw experiment kunt publiceren in Dynamics 365 Commerce nadat u [uw experiment hebt verbonden en uw variaties hebt bewerkt](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="db235-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="db235-105">In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="db235-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="db235-106">Extra stappen worden in afzonderlijke onderwerpen behandeld.</span><span class="sxs-lookup"><span data-stu-id="db235-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="db235-107">[ ![Traject van gebruiker voor experimenten - preview weergeven en publiceren](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="db235-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="db235-108">Een preview van uw experimentvariaties weergeven</span><span class="sxs-lookup"><span data-stu-id="db235-108">Preview your experiment variations</span></span>
<span data-ttu-id="db235-109">U kunt een preview van uw variaties weergeven en ze verder bewerken totdat ze er naar wens uitzien.</span><span class="sxs-lookup"><span data-stu-id="db235-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="db235-110">Voer de volgende stappen uit om een voorbeeld te bekijken van uw experimentvariaties in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="db235-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="db235-111">Selecteer in het vervolgkeuzemenu voor variaties onder de opdrachtbalk de inhoud die u wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="db235-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="db235-112">Selecteer **Voorbeeld** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="db235-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="db235-113">Er wordt een preview weergegeven van hoe de inhoud eruit ziet wanneer deze wordt gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="db235-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="db235-114">Als u een preview van een andere variatie wilt weergeven, selecteert u deze in het vervolgkeuzemenu voor variaties en selecteert u opnieuw **Preview**.</span><span class="sxs-lookup"><span data-stu-id="db235-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="db235-115">Uw experiment publiceren</span><span class="sxs-lookup"><span data-stu-id="db235-115">Publish your experiment</span></span>
<span data-ttu-id="db235-116">Als u geen publicatiegroep gebruikt om te plannen wanneer het experiment live gaat en u onmiddellijk wilt publiceren, selecteert u **Publiceren** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="db235-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="db235-117">Alle variaties die bij het experiment horen, worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="db235-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="db235-118">Als de pagina een niet-gepubliceerde URL heeft, moet u de URL eerst publiceren. Anders is deze niet zichtbaar voor de gebruikers van uw website.</span><span class="sxs-lookup"><span data-stu-id="db235-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="db235-119">Zie [Een pagina opslaan, voorvertonen en publiceren](save-preview-publish-page.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="db235-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="db235-120">Publicatiegroepen gebruiken om te plannen wanneer uw experiment live gaat</span><span class="sxs-lookup"><span data-stu-id="db235-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="db235-121">Variaties die in Site Builder zijn gemaakt, kunnen worden gepland voor publicatie met behulp van een publicatiegroep.</span><span class="sxs-lookup"><span data-stu-id="db235-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="db235-122">Binnen een publicatiegroep kunt u een pagina of fragment verbinden met uw experiment door **Experimenten** te selecteren in het linkernavigatievenster.</span><span class="sxs-lookup"><span data-stu-id="db235-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="db235-123">U kunt dit ook doen door **Pagina's** of **Fragmenten** te selecteren en de instructies te volgen in [Een experiment verbinden en variaties bewerken](experimentation-connect-edit.md).</span><span class="sxs-lookup"><span data-stu-id="db235-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="db235-124">Zie [Werken met publicatiegroepen](publish-groups.md) voor informatie over publicatiegroepen.</span><span class="sxs-lookup"><span data-stu-id="db235-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="db235-125">Wanneer u publicatiegroepen gebruikt bij experimenten, moet u rekening houden met een aantal belangrijke aandachtspunten.</span><span class="sxs-lookup"><span data-stu-id="db235-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="db235-126">Wanneer u een pagina of fragment toevoegt waarop een experiment wordt uitgevoerd naar een publicatiegroep, wordt het experiment verwijderd uit de pagina of het fragment in de publicatiegroep.</span><span class="sxs-lookup"><span data-stu-id="db235-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="db235-127">Experimenten die zijn verbonden met pagina's op een live site, zijn niet beschikbaar voor pagina's binnen publicatiegroepen en andersom.</span><span class="sxs-lookup"><span data-stu-id="db235-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="db235-128">Op dezelfde manier zijn pagina's waarop experimenten zijn uitgevoerd op een live site niet beschikbaar voor andere experimenten in publicatiegroepen en andersom.</span><span class="sxs-lookup"><span data-stu-id="db235-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="db235-129">Wanneer u een publicatiegroep publiceert of plant, wordt alle inhoud in de publicatiegroep gepubliceerd, ongeacht of er een experiment aan de publicatiegroep is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="db235-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="db235-130">Omdat een publicatiegroep blijft behouden nadat deze naar een live site is gepubliceerd, blijven experimenten in de publicatiegroep ook behouden.</span><span class="sxs-lookup"><span data-stu-id="db235-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="db235-131">Daarom kunt u geen andere experimenten koppelen aan dezelfde pagina of hetzelfde fragment.</span><span class="sxs-lookup"><span data-stu-id="db235-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="db235-132">Om deze beperking te voorkomen moet u alle publicatiegroepen met persistente experimenten verwijderen.</span><span class="sxs-lookup"><span data-stu-id="db235-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="db235-133">Zo geldt ook dat als u een experiment op een live site wilt verwijderen dat ook in een publicatiegroep bestaat, u het eerst moet verwijderen uit de publicatiegroep.</span><span class="sxs-lookup"><span data-stu-id="db235-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="db235-134">Vorige stap</span><span class="sxs-lookup"><span data-stu-id="db235-134">Previous step</span></span>
[<span data-ttu-id="db235-135">Een experiment verbinden en bewerken</span><span class="sxs-lookup"><span data-stu-id="db235-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="db235-136">Volgende stap</span><span class="sxs-lookup"><span data-stu-id="db235-136">Next step</span></span>
[<span data-ttu-id="db235-137">Een experiment uitvoeren en controleren</span><span class="sxs-lookup"><span data-stu-id="db235-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
