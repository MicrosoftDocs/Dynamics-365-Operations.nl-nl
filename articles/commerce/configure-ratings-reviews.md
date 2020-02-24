---
title: Beoordelingen en recensies configureren
description: In dit onderwerp wordt beschreven hoe u uw e-commerce site kunt configureren voor het weergeven van beoordelingen en recensies van klanten in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002192"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="48974-103">Beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="48974-103">Configure ratings and reviews</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="48974-104">In dit onderwerp wordt beschreven hoe u uw e-commerce site kunt configureren voor het weergeven van beoordelingen en recensies van klanten in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48974-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="48974-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="48974-105">Overview</span></span>

<span data-ttu-id="48974-106">Beoordelingen en recensies over e-commerce-websites geven klanten meer informatie over producten voordat ze een inkoopbeslissing nemen, door te laten zien wat andere klanten van deze producten vinden.</span><span class="sxs-lookup"><span data-stu-id="48974-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="48974-107">Voor e-commerce-websites zijn beoordelingen en recensies ook een mechanisme voor het verzamelen van klantfeedback over producten.</span><span class="sxs-lookup"><span data-stu-id="48974-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="48974-108">Beoordelingen worden weergegeven op pagina's met productlijsten, lijstpagina's categorieën of zoekresultaten en andere sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="48974-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="48974-109">Beoordelingshistogrammen en productrecensies worden weergegeven op pagina's met productgegevens (PDP).</span><span class="sxs-lookup"><span data-stu-id="48974-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="48974-110">Met een knop **Schrijf een recensie** kunnen klanten beoordelingen en recensies voor een product verzenden.</span><span class="sxs-lookup"><span data-stu-id="48974-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="48974-111">Beoordelings- en recensiemodules op pagina's met productgegevens</span><span class="sxs-lookup"><span data-stu-id="48974-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="48974-112">Drie modules geven een overzicht van beoordelingen en recensies voor pagina's met productgegevens:</span><span class="sxs-lookup"><span data-stu-id="48974-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="48974-113">Module voor recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="48974-113">Write review module</span></span>
- <span data-ttu-id="48974-114">Module met productrecensie</span><span class="sxs-lookup"><span data-stu-id="48974-114">Product reviews list module</span></span>
- <span data-ttu-id="48974-115">Module met beoordelingshistogram</span><span class="sxs-lookup"><span data-stu-id="48974-115">Ratings histogram module</span></span>
 
<span data-ttu-id="48974-116">In de volgende afbeelding ziet u hoe de modules voor beoordelingen en recensies er uitzien op een PDP.</span><span class="sxs-lookup"><span data-stu-id="48974-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Beoordelings- en recensiemodules op een PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="48974-118">Zie [Overzicht van sjablonen en indelingen](templates-layouts-overview.md) voor informatie over het optimaliseren van de PDP-sjablonen en -indelingen zodat u de configuraties voor beoordelingen en revisies kunt delen tussen meerdere PDP-pagina's op uw e-commerce-site.</span><span class="sxs-lookup"><span data-stu-id="48974-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="48974-119">In de volgende afbeelding ziet u hoe in het dialoogvenster **Module toevoegen** modules voor beoordelingen en recensies in Dynamics 365 Commerce worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="48974-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Het dialoogvenster Module toevoegen](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="48974-121">Module voor recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="48974-121">Write review module</span></span>

<span data-ttu-id="48974-122">De module voor het schrijven van een recensie bevat een knop **Schrijf een recensie** waarmee gebruikers zich kunnen aanmelden, een beoordeling kunnen toewijzen en een recensie van een product kunnen schrijven.</span><span class="sxs-lookup"><span data-stu-id="48974-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="48974-123">Met deze module kunnen gebruikers ook een beoordeling of een recensie bewerken die ze eerder hebben ingediend.</span><span class="sxs-lookup"><span data-stu-id="48974-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="48974-124">Deze module wordt meestal weergegeven boven het beoordelingshistogram en de lijstmodules met productrecensies op een PDP.</span><span class="sxs-lookup"><span data-stu-id="48974-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="48974-125">In de volgende afbeelding ziet u het dialoogvenster **Schrijf een recensie** dat wordt weergegeven wanneer een klant **Schrijf een recensie** selecteert.</span><span class="sxs-lookup"><span data-stu-id="48974-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="48974-126">De klant kan dit dialoog venster gebruiken om een beoordeling en een recensie in te dienen.</span><span class="sxs-lookup"><span data-stu-id="48974-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Het dialoogvenster Schrijf een recensie](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="48974-128">In de volgende tabel wordt de eigenschap van de module voor het schrijven van een recensie weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="48974-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="48974-129">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="48974-129">Property name</span></span> | <span data-ttu-id="48974-130">Waarde</span><span class="sxs-lookup"><span data-stu-id="48974-130">Value</span></span>        | <span data-ttu-id="48974-131">Beschrijving eigenschap</span><span class="sxs-lookup"><span data-stu-id="48974-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="48974-132">Naam</span><span class="sxs-lookup"><span data-stu-id="48974-132">Name</span></span>          | <span data-ttu-id="48974-133">Recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="48974-133">Write review</span></span> | <span data-ttu-id="48974-134">De naam van de module voor het schrijven van een recensie.</span><span class="sxs-lookup"><span data-stu-id="48974-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="48974-135">Module met beoordelingshistogram</span><span class="sxs-lookup"><span data-stu-id="48974-135">Ratings histogram module</span></span>

<span data-ttu-id="48974-136">In de module met het beoordelingshistogram wordt een beoordelingshistogram weergegeven.</span><span class="sxs-lookup"><span data-stu-id="48974-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="48974-137">Deze module wordt meestal weergegeven tussen de module Schrijf een recensie en de module met de productrecensielijst op een PDP-pagina.</span><span class="sxs-lookup"><span data-stu-id="48974-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="48974-138">Voor de module met het beoordelingshistogram is geen configuratie vereist.</span><span class="sxs-lookup"><span data-stu-id="48974-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="48974-139">U hoeft de module alleen aan de PDP-sjabloon toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="48974-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="48974-140">De volgende illustraties laten zien hoe een PDP-sjabloon eruitziet in Dynamics 365 Commerce wanneer de modules voor beoordelingen en recensies zijn geconfigureerd voor weergave op productbeschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="48974-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP-sjabloon wanneer beoordelingen en recensies zijn geconfigureerd voor weergave in productbeschrijvingen](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="48974-142">Module met productrecensie</span><span class="sxs-lookup"><span data-stu-id="48974-142">Product reviews list module</span></span>

<span data-ttu-id="48974-143">In de module met productrecensies wordt een lijst met productrecensies weergegeven met opties voor sorteren, filteren en paginering.</span><span class="sxs-lookup"><span data-stu-id="48974-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="48974-144">Deze module wordt normaal gesproken weergegeven na de module met het beoordelingshistogram.</span><span class="sxs-lookup"><span data-stu-id="48974-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="48974-145">In de volgende tabel worden de eigenschappen van de module voor productrecensielijsten weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="48974-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="48974-146">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="48974-146">Property name</span></span>              | <span data-ttu-id="48974-147">Waarde</span><span class="sxs-lookup"><span data-stu-id="48974-147">Value</span></span> | <span data-ttu-id="48974-148">Beschrijving eigenschap</span><span class="sxs-lookup"><span data-stu-id="48974-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="48974-149">Recensies die op elke pagina worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="48974-149">Reviews shown on each page</span></span> | <span data-ttu-id="48974-150">10</span><span class="sxs-lookup"><span data-stu-id="48974-150">10</span></span>    | <span data-ttu-id="48974-151">Het aantal recensies dat tegelijk op een PDP moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="48974-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="48974-152">De knoppen **Volgende** en **Vorige** zijn opgenomen, zodat gebruikers door de pagina's met recensies kunnen navigeren.</span><span class="sxs-lookup"><span data-stu-id="48974-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="48974-153">Beoordelingshistogram – overzichtsweergave</span><span class="sxs-lookup"><span data-stu-id="48974-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="48974-154">De module met de productrecensielijst bevat een vak waarin u een beoordelingshistogrammodule kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="48974-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="48974-155">In de volgende afbeelding ziet u hoe u een beoordelingshistogrammodule in de module met de productrecensielijst kunt toevoegen in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48974-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Een beoordelingshistogrammodule toevoegen aan de module met de productrecensielijst](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="48974-157">Een site met beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="48974-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="48974-158">Configuratiewaarden voor beoordelingen en recensies, zoals de tenant-id, de lengte van de recensietekst en de lengte van de recensietitel worden op siteniveau geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="48974-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="48974-159">Voer de volgende stappen uit om een site te configureren voor het weergeven van beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="48974-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="48974-160">Ga naar **Startpagina \> Sites**.</span><span class="sxs-lookup"><span data-stu-id="48974-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="48974-161">Selecteer de naam van uw site.</span><span class="sxs-lookup"><span data-stu-id="48974-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="48974-162">Ga naar **Sitebeheer \> Uitbreidbaarheid**.</span><span class="sxs-lookup"><span data-stu-id="48974-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="48974-163">Voer in het veld **Maximale lengte recensietekst** het maximumaantal tekens in dat de recensietekst kan bevatten (bijvoorbeeld **1000**).</span><span class="sxs-lookup"><span data-stu-id="48974-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="48974-164">Voer in het veld **Maximale lengte recensietitel** het maximumaantal tekens in dat de recensietitel kan bevatten (bijvoorbeeld **55**).</span><span class="sxs-lookup"><span data-stu-id="48974-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="48974-165">Selecteer **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="48974-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="48974-166">In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48974-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Een site met beoordelingen en recensies configureren](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="48974-168">Een productbeoordeling koppelen aan de sectie Recensies van een PDP</span><span class="sxs-lookup"><span data-stu-id="48974-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="48974-169">Een productbeoordeling wordt onder de producttitel boven aan de PDP weergegeven.</span><span class="sxs-lookup"><span data-stu-id="48974-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="48974-170">De productbeoordeling kan zo worden geconfigureerd dat deze wordt gekoppeld aan de sectie **Recensies** van dezelfde PDP.</span><span class="sxs-lookup"><span data-stu-id="48974-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="48974-171">Voer de volgende stappen uit om een productbeoordeling te koppelen aan de sectie **Recensies** van de PDP.</span><span class="sxs-lookup"><span data-stu-id="48974-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="48974-172">Open de PDP-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="48974-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="48974-173">Ga naar **Instellingen van module voor koopvakcontainer**.</span><span class="sxs-lookup"><span data-stu-id="48974-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="48974-174">Selecteer onder **Koopvak** de optie **Productbeoordelingen** en schakel vervolgens het selectievakje **Klikken koppelen aan module met volledige recensies** in.</span><span class="sxs-lookup"><span data-stu-id="48974-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="48974-175">In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48974-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Een productbeoordeling koppelen aan de sectie Recensies van een PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="48974-177">De koppeling naar de pagina Privacy en beleid configureren</span><span class="sxs-lookup"><span data-stu-id="48974-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="48974-178">Volg deze stappen om de koppeling naar de pagina Privacy en beleid te configureren</span><span class="sxs-lookup"><span data-stu-id="48974-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="48974-179">Ga naar **Startpagina \> Sites**.</span><span class="sxs-lookup"><span data-stu-id="48974-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="48974-180">Selecteer de naam van uw site.</span><span class="sxs-lookup"><span data-stu-id="48974-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="48974-181">Ga naar **Sitebeheer \> Uitbreidbaarheid**</span><span class="sxs-lookup"><span data-stu-id="48974-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="48974-182">Selecteer op het tabblad **Routes** onder **RNR privacy en beleid** de optie **Een koppeling toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="48974-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="48974-183">Als er al een koppeling is ingevoerd en u deze wilt vervangen, selecteert u de koppeling.</span><span class="sxs-lookup"><span data-stu-id="48974-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="48974-184">Selecteer in het dialoogvenster **Een koppeling toevoegen** de koppeling voor de pagina Privacy en beleid en selecteer vervolgens **OK.**</span><span class="sxs-lookup"><span data-stu-id="48974-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="48974-185">Selecteer **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="48974-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="48974-186">In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="48974-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![De koppeling naar de pagina Privacy en beleid configureren](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="48974-188">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="48974-188">Additional resources</span></span>

[<span data-ttu-id="48974-189">Overzicht beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="48974-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="48974-190">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="48974-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="48974-191">Beoordelingen en recensies beheren</span><span class="sxs-lookup"><span data-stu-id="48974-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="48974-192">Productbeoordelingen synchroniseren in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="48974-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
