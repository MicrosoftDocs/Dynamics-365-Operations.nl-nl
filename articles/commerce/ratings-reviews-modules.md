---
title: Beoordelings- en recensiemodules
description: In dit onderwerp worden de modules voor beoordelingen en recensies beschreven die worden gebruikt op de pagina's met productdetails in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: ee2a2a781537b592fb5f80ce424a7331c4e21d41
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071851"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="8a926-103">Beoordelings- en recensiemodules</span><span class="sxs-lookup"><span data-stu-id="8a926-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a926-104">In dit onderwerp worden de modules voor beoordelingen en recensies beschreven die worden gebruikt op de pagina's met productdetails (PDP's) in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a926-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8a926-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="8a926-105">Overview</span></span>

<span data-ttu-id="8a926-106">Beoordelingen en recensies over e-commerce-websites geven klanten meer informatie over producten voordat ze een aankoopbeslissing nemen en vormen tevens een mechanisme voor het verzamelen van feedback van klanten over producten.</span><span class="sxs-lookup"><span data-stu-id="8a926-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="8a926-107">Beoordelingen worden weergegeven op pagina's met productlijsten, lijstpagina's categorieën of zoekresultaten en andere sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="8a926-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="8a926-108">Beoordelingshistogrammen en productrecensies worden weergegeven op PDP's.</span><span class="sxs-lookup"><span data-stu-id="8a926-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="8a926-109">Met een knop **Schrijf een recensie** kunnen klanten beoordelingen en recensies voor een product verzenden.</span><span class="sxs-lookup"><span data-stu-id="8a926-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="8a926-110">Deze PDP-functies worden geregeld door middel van modules voor beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="8a926-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="8a926-111">Beoordelings- en recensiemodules op pagina's met productgegevens</span><span class="sxs-lookup"><span data-stu-id="8a926-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="8a926-112">Drie modules geven een overzicht van beoordelingen en recensies voor pagina's met productgegevens:</span><span class="sxs-lookup"><span data-stu-id="8a926-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="8a926-113">Module voor recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="8a926-113">Write review module</span></span>
- <span data-ttu-id="8a926-114">Module met productrecensie</span><span class="sxs-lookup"><span data-stu-id="8a926-114">Product reviews list module</span></span>
- <span data-ttu-id="8a926-115">Module met beoordelingshistogram</span><span class="sxs-lookup"><span data-stu-id="8a926-115">Ratings histogram module</span></span>
 
<span data-ttu-id="8a926-116">In de volgende afbeelding ziet u hoe de modules voor beoordelingen en recensies er uitzien op een PDP.</span><span class="sxs-lookup"><span data-stu-id="8a926-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Beoordelings- en recensiemodules op een PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="8a926-118">Zie [Overzicht van sjablonen en indelingen](templates-layouts-overview.md) voor informatie over het optimaliseren van de PDP-sjablonen en -indelingen zodat u de configuraties voor beoordelingen en revisies kunt delen tussen meerdere PDP-pagina's op uw e-commerce-site.</span><span class="sxs-lookup"><span data-stu-id="8a926-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="8a926-119">In de volgende afbeelding ziet u hoe in het dialoogvenster **Module toevoegen** modules voor beoordelingen en recensies in Dynamics 365 Commerce worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8a926-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="8a926-120">![Het dialoogvenster Module toevoegen](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="8a926-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="8a926-121">Module voor recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="8a926-121">Write review module</span></span>

<span data-ttu-id="8a926-122">De module voor het schrijven van een recensie bevat een knop **Schrijf een recensie** waarmee gebruikers zich kunnen aanmelden, een beoordeling kunnen toewijzen en een recensie van een product kunnen schrijven.</span><span class="sxs-lookup"><span data-stu-id="8a926-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="8a926-123">Met deze module kunnen gebruikers ook een beoordeling of een recensie bewerken die ze eerder hebben ingediend.</span><span class="sxs-lookup"><span data-stu-id="8a926-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="8a926-124">Deze module wordt meestal weergegeven boven het beoordelingshistogram en de lijstmodules met productrecensies op een PDP.</span><span class="sxs-lookup"><span data-stu-id="8a926-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="8a926-125">In de volgende afbeelding ziet u het dialoogvenster **Schrijf een recensie** dat wordt weergegeven wanneer een klant **Schrijf een recensie** selecteert.</span><span class="sxs-lookup"><span data-stu-id="8a926-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="8a926-126">De klant kan dit dialoog venster gebruiken om een beoordeling en een recensie in te dienen.</span><span class="sxs-lookup"><span data-stu-id="8a926-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="8a926-127">![Dialoogvenster Schrijf een recensie](media/rnr-eCommerce-write-review-module.png) In de volgende tabel wordt de eigenschap van de module voor het schrijven van een recensie weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="8a926-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="8a926-128">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="8a926-128">Property name</span></span> | <span data-ttu-id="8a926-129">Waarde</span><span class="sxs-lookup"><span data-stu-id="8a926-129">Value</span></span>        | <span data-ttu-id="8a926-130">Beschrijving eigenschap</span><span class="sxs-lookup"><span data-stu-id="8a926-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="8a926-131">Naam</span><span class="sxs-lookup"><span data-stu-id="8a926-131">Name</span></span>          | <span data-ttu-id="8a926-132">Recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="8a926-132">Write review</span></span> | <span data-ttu-id="8a926-133">De naam van de module voor het schrijven van een recensie.</span><span class="sxs-lookup"><span data-stu-id="8a926-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="8a926-134">Module met beoordelingshistogram</span><span class="sxs-lookup"><span data-stu-id="8a926-134">Ratings histogram module</span></span>

<span data-ttu-id="8a926-135">In de module met het beoordelingshistogram wordt een beoordelingshistogram weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8a926-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="8a926-136">Deze module wordt meestal weergegeven tussen de module Schrijf een recensie en de module met de productrecensielijst op een PDP-pagina.</span><span class="sxs-lookup"><span data-stu-id="8a926-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="8a926-137">Voor de module met het beoordelingshistogram is geen configuratie vereist.</span><span class="sxs-lookup"><span data-stu-id="8a926-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="8a926-138">U hoeft de module alleen aan de PDP-sjabloon toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="8a926-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="8a926-139">De volgende illustraties laten zien hoe een PDP-sjabloon eruitziet in Dynamics 365 Commerce wanneer de modules voor beoordelingen en recensies zijn geconfigureerd voor weergave op productbeschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="8a926-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="8a926-140">![PDP-sjabloon wanneer beoordelingen en recensies zijn geconfigureerd voor weergave in productbeschrijvingen](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="8a926-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="8a926-141">Module met productrecensie</span><span class="sxs-lookup"><span data-stu-id="8a926-141">Product reviews list module</span></span>

<span data-ttu-id="8a926-142">In de module met productrecensies wordt een lijst met productrecensies weergegeven met opties voor sorteren, filteren en paginering.</span><span class="sxs-lookup"><span data-stu-id="8a926-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="8a926-143">Deze module wordt normaal gesproken weergegeven na de module met het beoordelingshistogram.</span><span class="sxs-lookup"><span data-stu-id="8a926-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="8a926-144">In de volgende tabel worden de eigenschappen van de module voor productrecensielijsten weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="8a926-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="8a926-145">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="8a926-145">Property name</span></span>              | <span data-ttu-id="8a926-146">Waarde</span><span class="sxs-lookup"><span data-stu-id="8a926-146">Value</span></span> | <span data-ttu-id="8a926-147">Beschrijving eigenschap</span><span class="sxs-lookup"><span data-stu-id="8a926-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="8a926-148">Recensies die op elke pagina worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="8a926-148">Reviews shown on each page</span></span> | <span data-ttu-id="8a926-149">10</span><span class="sxs-lookup"><span data-stu-id="8a926-149">10</span></span>    | <span data-ttu-id="8a926-150">Het aantal recensies dat tegelijk op een PDP moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8a926-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="8a926-151">De knoppen **Volgende** en **Vorige** zijn opgenomen, zodat gebruikers door de pagina's met recensies kunnen navigeren.</span><span class="sxs-lookup"><span data-stu-id="8a926-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="8a926-152">Beoordelingshistogram – overzichtsweergave</span><span class="sxs-lookup"><span data-stu-id="8a926-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="8a926-153">De module met de productrecensielijst bevat een vak waarin u een beoordelingshistogrammodule kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8a926-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="8a926-154">In de volgende afbeelding ziet u hoe u een beoordelingshistogrammodule in de module met de productrecensielijst kunt toevoegen in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8a926-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Een beoordelingshistogrammodule toevoegen aan de module met de productrecensielijst](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="8a926-156">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8a926-156">Additional resources</span></span>

[<span data-ttu-id="8a926-157">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="8a926-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8a926-158">Containermodule</span><span class="sxs-lookup"><span data-stu-id="8a926-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8a926-159">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="8a926-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8a926-160">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="8a926-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8a926-161">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="8a926-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8a926-162">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="8a926-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8a926-163">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="8a926-163">Footer module</span></span>](author-footer-module.md)
