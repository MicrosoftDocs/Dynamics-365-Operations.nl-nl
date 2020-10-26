---
title: Een variant promoveren en een experiment voltooien
description: In dit onderwerp wordt beschreven hoe u een geslaagde variant kunt promoveren en een experiment kunt voltooien in Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930168"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="24b17-103">Een variant promoveren en een experiment voltooien</span><span class="sxs-lookup"><span data-stu-id="24b17-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="24b17-104">In dit onderwerp wordt beschreven hoe u de variatie die de beste resultaten heeft opgeleverd in uw experiment kunt promoveren en hoe u het experiment kunt voltooien.</span><span class="sxs-lookup"><span data-stu-id="24b17-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="24b17-105">In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="24b17-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="24b17-106">Extra stappen worden in afzonderlijke onderwerpen behandeld.</span><span class="sxs-lookup"><span data-stu-id="24b17-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="24b17-107">[ ![Traject van gebruiker voor experimenten - controleren en voltooien](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="24b17-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="24b17-108">Nadat u [uw experiment hebt uitgevoerd](experimentation-run-monitor.md) en voldoende gegevens hebt verzameld om te bepalen welke variatie u op uw live site wilt gebruiken, promoveert u de variatie en beëindigt u het experiment.</span><span class="sxs-lookup"><span data-stu-id="24b17-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="24b17-109">Een variatie promoveren</span><span class="sxs-lookup"><span data-stu-id="24b17-109">Promote a variation</span></span>
<span data-ttu-id="24b17-110">Gebruik de gegevens en analyse met betrekking tot het experiment in de service van derden om te bepalen welke variatie de beste resultaten heeft opgeleverd.</span><span class="sxs-lookup"><span data-stu-id="24b17-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="24b17-111">Als u de huidige inhoud op de live site wilt vervangen met de winnende variatie zodat deze beschikbaar is voor alle gebruikers van uw website, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="24b17-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="24b17-112">Ga naar het tabblad **Experimenten** in Site Builder en selecteer het experiment.</span><span class="sxs-lookup"><span data-stu-id="24b17-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="24b17-113">Selecteer **Experiment voltooien** op de bovenste balk.</span><span class="sxs-lookup"><span data-stu-id="24b17-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="24b17-114">Selecteer in het dialoogvenster **Experiment voltooien** de optie **Experimentgegevens controleren**.</span><span class="sxs-lookup"><span data-stu-id="24b17-114">In the **Complete the experiment** dialog menu, select **Review the experiment data**.</span></span> <span data-ttu-id="24b17-115">De service van derden wordt geopend, waar u de metrische gegevens kunt valideren en kunt bepalen welke variatie de beste resultaten geeft.</span><span class="sxs-lookup"><span data-stu-id="24b17-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="24b17-116">Selecteer in het menu van het dialoogvenster **Experiment voltooien** in Site Builder de winnende variatie en selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="24b17-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next**.</span></span>
1. <span data-ttu-id="24b17-117">Open de service van derden en stop het experiment.</span><span class="sxs-lookup"><span data-stu-id="24b17-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="24b17-118">Selecteer in Site Builder de functie **Voltooien** om de oorspronkelijke live pagina te overschrijven en de winnende variatie te publiceren zodat deze beschikbaar is voor alle gebruikers van uw website.</span><span class="sxs-lookup"><span data-stu-id="24b17-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="24b17-119">Als u de huidige live pagina wilt behouden en geen variatie wilt publiceren, selecteert u **De oorspronkelijke pagina opnieuw publiceren**.</span><span class="sxs-lookup"><span data-stu-id="24b17-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="24b17-120">Uw experiment verwijderen</span><span class="sxs-lookup"><span data-stu-id="24b17-120">Delete your experiment</span></span>
<span data-ttu-id="24b17-121">Hoewel het niet nodig is om een voltooid experiment te verwijderen in Commerce, kunt u het verwijderen om ruimte te besparen of om uw werkruimte op te schonen.</span><span class="sxs-lookup"><span data-stu-id="24b17-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="24b17-122">Ga als volgt te werk om een experiment te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="24b17-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="24b17-123">Ga naar het tabblad **Experimenten** in Site Builder en selecteer het experiment.</span><span class="sxs-lookup"><span data-stu-id="24b17-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="24b17-124">Als het experiment nog steeds actief is, stopt u het experiment in de service van derden voordat u verder gaat.</span><span class="sxs-lookup"><span data-stu-id="24b17-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="24b17-125">Selecteer **Publicatie ongedaan maken** op de opdrachtbalk om de variatie-inhoud van de live site te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="24b17-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="24b17-126">Selecteer **Verwijderen** op de opdrachtbalk om het experiment te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="24b17-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="24b17-127">Vorige stap</span><span class="sxs-lookup"><span data-stu-id="24b17-127">Previous step</span></span>
[<span data-ttu-id="24b17-128">Een experiment uitvoeren en controleren</span><span class="sxs-lookup"><span data-stu-id="24b17-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
