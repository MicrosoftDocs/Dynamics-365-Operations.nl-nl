---
title: Een variant promoveren en een experiment voltooien
description: In dit onderwerp wordt beschreven hoe u een geslaagde variant kunt promoveren en een experiment kunt voltooien in Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0ea0fc8d50c25312b184ec1d3bd613695870d121
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792554"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="3c9d1-103">Een variant promoveren en een experiment voltooien</span><span class="sxs-lookup"><span data-stu-id="3c9d1-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="3c9d1-104">In dit onderwerp wordt beschreven hoe u de variatie die de beste resultaten heeft opgeleverd in uw experiment kunt promoveren en hoe u het experiment kunt voltooien.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="3c9d1-105">In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="3c9d1-106">Extra stappen worden in afzonderlijke onderwerpen behandeld.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="3c9d1-107">[ ![Traject van gebruiker voor experimenten - controleren en voltooien](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="3c9d1-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="3c9d1-108">Nadat u [uw experiment hebt uitgevoerd](experimentation-run-monitor.md) en voldoende gegevens hebt verzameld om te bepalen welke variatie u op uw live site wilt gebruiken, promoveert u de variatie en beëindigt u het experiment.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="3c9d1-109">Een variatie promoveren</span><span class="sxs-lookup"><span data-stu-id="3c9d1-109">Promote a variation</span></span>
<span data-ttu-id="3c9d1-110">Gebruik de gegevens en analyse met betrekking tot het experiment in de service van derden om te bepalen welke variatie de beste resultaten heeft opgeleverd.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="3c9d1-111">U kunt de variatie vervolgens promoveren door de huidige inhoud op de live site te vervangen met de winnende variatie zodat deze beschikbaar is voor alle gebruikers van uw website.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="3c9d1-112">Voer de volgende stappen uit om de winnende variatie te promoveren.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="3c9d1-113">Selecteer **Experimenten** in het linkernavigatievenster in Commerce Site Builder en selecteer het experiment vervolgens.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="3c9d1-114">Selecteer **Experiment voltooien** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="3c9d1-115">Selecteer in het dialoogvenster **Experiment voltooien** de optie **Experimentgegevens controleren**.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="3c9d1-116">De service van derden wordt geopend, waar u de metrische gegevens kunt valideren en kunt bepalen welke variatie de beste resultaten geeft.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="3c9d1-117">Selecteer in het dialoogvenster **Experiment voltooien** de winnende variatie en selecteer vervolgens **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="3c9d1-118">Open de service van derden en stop het experiment.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="3c9d1-119">Selecteer in Site Builder de functie **Voltooien** om de oorspronkelijke live pagina te overschrijven en de winnende variatie te publiceren zodat deze beschikbaar is voor alle gebruikers van uw website.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="3c9d1-120">Als u de huidige live pagina wilt behouden en geen variatie wilt publiceren, selecteert u **De oorspronkelijke pagina opnieuw publiceren**.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="3c9d1-121">Uw experiment verwijderen</span><span class="sxs-lookup"><span data-stu-id="3c9d1-121">Delete your experiment</span></span>
<span data-ttu-id="3c9d1-122">Hoewel het niet nodig is om een voltooid experiment te verwijderen in Commerce, kunt u het verwijderen om ruimte te besparen of om uw werkruimte op te schonen.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="3c9d1-123">Voer de volgende stappen uit om een experiment te verwijderen in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="3c9d1-124">Selecteer **Experimenten** in het linkernavigatievenster en selecteer het experiment vervolgens.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="3c9d1-125">Als het experiment nog steeds actief is, stopt u het experiment in de service van derden voordat u verder gaat.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="3c9d1-126">Selecteer **Publicatie ongedaan maken** op de opdrachtbalk om de variatie-inhoud van de live site te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="3c9d1-127">Selecteer **Verwijderen** om het experiment te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="3c9d1-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="3c9d1-128">Vorige stap</span><span class="sxs-lookup"><span data-stu-id="3c9d1-128">Previous step</span></span>
[<span data-ttu-id="3c9d1-129">Een experiment uitvoeren en controleren</span><span class="sxs-lookup"><span data-stu-id="3c9d1-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]