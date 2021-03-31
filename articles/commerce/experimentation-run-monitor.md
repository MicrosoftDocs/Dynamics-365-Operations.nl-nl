---
title: Een experiment uitvoeren en controleren
description: In dit onderwerp wordt beschreven hoe u een experiment in een service van derden uitvoert en controleert. Verder wordt beschreven hoe u wijzigingen aanbrengt in variaties nadat het experiment is gestart.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 956a9168ed7bf9282d9eeec39587d8e1f2d1856c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224877"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="92c20-104">Een experiment uitvoeren en controleren</span><span class="sxs-lookup"><span data-stu-id="92c20-104">Run and monitor an experiment</span></span>

<span data-ttu-id="92c20-105">In dit onderwerp wordt beschreven hoe u uw experiment in een app van derden uitvoert en controleert en zo nodig variaties wijzigt.</span><span class="sxs-lookup"><span data-stu-id="92c20-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="92c20-106">Voordat u de stappen in dit onderwerp uitvoert, moet u uw experiment eerst [publiceren](experimentation-preview-publish.md) in Commerce.</span><span class="sxs-lookup"><span data-stu-id="92c20-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="92c20-107">In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="92c20-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="92c20-108">Extra stappen worden in afzonderlijke onderwerpen behandeld.</span><span class="sxs-lookup"><span data-stu-id="92c20-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="92c20-109">[ ![Traject van gebruiker voor experimenten - uitvoeren en controleren](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="92c20-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="92c20-110">Nadat u uw variaties hebt gepubliceerd, zijn alle stappen gereed die u moet uitvoeren in Commerce om uw experiment uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="92c20-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="92c20-111">De volgende stap bestaat eruit te bepalen welke variatie wordt weergegeven voor elke gebruiker wanneer hij of zij een pagina aanvraagt.</span><span class="sxs-lookup"><span data-stu-id="92c20-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="92c20-112">Dit wordt door de service van derden bepaald, maar eerst moet u het experiment binnen de service activeren.</span><span class="sxs-lookup"><span data-stu-id="92c20-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="92c20-113">Omdat de stappen voor het activeren van een experiment van service tot service verschillen, moet u de instructies volgen die door uw service of provider zijn geleverd.</span><span class="sxs-lookup"><span data-stu-id="92c20-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="92c20-114">Als het experiment niet wordt geactiveerd, zien gebruikers alleen de standaardversie van de pagina (er worden geen variaties weergegeven).</span><span class="sxs-lookup"><span data-stu-id="92c20-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="92c20-115">U moet het experiment lang genoeg blijven uitvoeren om gegevens te verzamelen voor statistisch geldige resultaten.</span><span class="sxs-lookup"><span data-stu-id="92c20-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="92c20-116">Gebruik de service van derden om de experimentgerelateerde gegevens en analyse te controleren terwijl het experiment wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="92c20-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="92c20-117">Uw variaties aanpassen</span><span class="sxs-lookup"><span data-stu-id="92c20-117">Adjust your variations</span></span>
<span data-ttu-id="92c20-118">Als u om welke reden dan ook wijzigingen moet aanbrengen in uw variaties, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="92c20-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92c20-119">Als u wijzigingen aanbrengt in een live experiment in Commerce of de service van derden, kunnen uw resultaten aanzienlijk worden beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="92c20-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="92c20-120">Overweeg om het experiment te laten uitvoeren en vervolgens een nieuw experiment te maken voor belangrijke wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="92c20-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="92c20-121">Selecteer **Experimenten** in het linkernavigatievenster in Commerce Site Builder en selecteer het experiment vervolgens.</span><span class="sxs-lookup"><span data-stu-id="92c20-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="92c20-122">Selecteer de variatie die u wilt bijwerken in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="92c20-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="92c20-123">Voer eventuele noodzakelijke wijzigingen door en bekijk vervolgens de variaties en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="92c20-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="92c20-124">Zie [Preview van een experiment weergeven en een experiment publiceren](experimentation-preview-publish.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="92c20-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="92c20-125">Ga naar de service van derden om alle wijzigingen aan te brengen die betrekking hebben op het instellen van het experiment.</span><span class="sxs-lookup"><span data-stu-id="92c20-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="92c20-126">Vorige stap</span><span class="sxs-lookup"><span data-stu-id="92c20-126">Previous step</span></span>
[<span data-ttu-id="92c20-127">Preview van een experiment weergeven en een experiment publiceren</span><span class="sxs-lookup"><span data-stu-id="92c20-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="92c20-128">Volgende stap</span><span class="sxs-lookup"><span data-stu-id="92c20-128">Next step</span></span>
[<span data-ttu-id="92c20-129">Een variant promoveren en een experiment voltooien</span><span class="sxs-lookup"><span data-stu-id="92c20-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]