---
title: Beoordelings- en recensiemodules
description: In dit onderwerp worden de modules voor beoordelingen en recensies beschreven die worden gebruikt op de pagina's met productdetails in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: a243399536fec3f5361104289c38e550bf8b1144
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193277"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="da82d-103">Beoordelings- en recensiemodules</span><span class="sxs-lookup"><span data-stu-id="da82d-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da82d-104">In dit onderwerp worden de modules voor beoordelingen en recensies beschreven die worden gebruikt op de pagina's met productdetails (PDP's) in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="da82d-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="da82d-105">Beoordelingen en recensies over e-commerce-websites geven klanten meer informatie over producten voordat ze een aankoopbeslissing nemen en vormen tevens een mechanisme voor het verzamelen van feedback van klanten over producten.</span><span class="sxs-lookup"><span data-stu-id="da82d-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="da82d-106">Beoordelingen worden weergegeven op pagina's met productlijsten, lijstpagina's categorieën of zoekresultaten en andere sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="da82d-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="da82d-107">Beoordelingshistogrammen en productrecensies worden weergegeven op PDP's.</span><span class="sxs-lookup"><span data-stu-id="da82d-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="da82d-108">Met een knop **Schrijf een recensie** kunnen klanten beoordelingen en recensies voor een product verzenden.</span><span class="sxs-lookup"><span data-stu-id="da82d-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="da82d-109">Deze PDP-functies worden geregeld door middel van modules voor beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="da82d-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="da82d-110">Beoordelings- en recensiemodules op pagina's met productgegevens</span><span class="sxs-lookup"><span data-stu-id="da82d-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="da82d-111">Drie modules geven een overzicht van beoordelingen en recensies voor pagina's met productgegevens:</span><span class="sxs-lookup"><span data-stu-id="da82d-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="da82d-112">Module voor recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="da82d-112">Write review module</span></span>
- <span data-ttu-id="da82d-113">Module met productrecensie</span><span class="sxs-lookup"><span data-stu-id="da82d-113">Product reviews list module</span></span>
- <span data-ttu-id="da82d-114">Module met beoordelingshistogram</span><span class="sxs-lookup"><span data-stu-id="da82d-114">Ratings histogram module</span></span>
 
<span data-ttu-id="da82d-115">In de volgende afbeelding ziet u hoe de modules voor beoordelingen en recensies er uitzien op een PDP.</span><span class="sxs-lookup"><span data-stu-id="da82d-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Beoordelings- en recensiemodules op een PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="da82d-117">Zie [Overzicht van sjablonen en indelingen](templates-layouts-overview.md) voor informatie over het optimaliseren van de PDP-sjablonen en -indelingen zodat u de configuraties voor beoordelingen en revisies kunt delen tussen meerdere PDP-pagina's op uw e-commerce-site.</span><span class="sxs-lookup"><span data-stu-id="da82d-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="da82d-118">In de volgende afbeelding ziet u hoe in het dialoogvenster **Module toevoegen** modules voor beoordelingen en recensies in Dynamics 365 Commerce worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="da82d-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="da82d-119">![Het dialoogvenster Module toevoegen](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="da82d-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="da82d-120">Module voor recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="da82d-120">Write review module</span></span>

<span data-ttu-id="da82d-121">De module voor het schrijven van een recensie bevat een knop **Schrijf een recensie** waarmee gebruikers zich kunnen aanmelden, een beoordeling kunnen toewijzen en een recensie van een product kunnen schrijven.</span><span class="sxs-lookup"><span data-stu-id="da82d-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="da82d-122">Met deze module kunnen gebruikers ook een beoordeling of een recensie bewerken die ze eerder hebben ingediend.</span><span class="sxs-lookup"><span data-stu-id="da82d-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="da82d-123">Deze module wordt meestal weergegeven boven het beoordelingshistogram en de lijstmodules met productrecensies op een PDP.</span><span class="sxs-lookup"><span data-stu-id="da82d-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="da82d-124">In de volgende afbeelding ziet u het dialoogvenster **Schrijf een recensie** dat wordt weergegeven wanneer een klant **Schrijf een recensie** selecteert.</span><span class="sxs-lookup"><span data-stu-id="da82d-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="da82d-125">De klant kan dit dialoog venster gebruiken om een beoordeling en een recensie in te dienen.</span><span class="sxs-lookup"><span data-stu-id="da82d-125">The customer can use this dialog box to submit a rating and a review.</span></span>

![Het dialoogvenster Schrijf een recensie](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="da82d-127">In de volgende tabel wordt de eigenschap van de module voor het schrijven van een recensie weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="da82d-127">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="da82d-128">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="da82d-128">Property name</span></span> | <span data-ttu-id="da82d-129">Waarde</span><span class="sxs-lookup"><span data-stu-id="da82d-129">Value</span></span>        | <span data-ttu-id="da82d-130">Beschrijving eigenschap</span><span class="sxs-lookup"><span data-stu-id="da82d-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="da82d-131">Naam</span><span class="sxs-lookup"><span data-stu-id="da82d-131">Name</span></span>          | <span data-ttu-id="da82d-132">Recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="da82d-132">Write review</span></span> | <span data-ttu-id="da82d-133">De naam van de module voor het schrijven van een recensie.</span><span class="sxs-lookup"><span data-stu-id="da82d-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="da82d-134">Module met beoordelingshistogram</span><span class="sxs-lookup"><span data-stu-id="da82d-134">Ratings histogram module</span></span>

<span data-ttu-id="da82d-135">In de module met het beoordelingshistogram wordt een beoordelingshistogram weergegeven.</span><span class="sxs-lookup"><span data-stu-id="da82d-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="da82d-136">Deze module wordt meestal weergegeven tussen de module Schrijf een recensie en de module met de productrecensielijst op een PDP-pagina.</span><span class="sxs-lookup"><span data-stu-id="da82d-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="da82d-137">Voor de module met het beoordelingshistogram is geen configuratie vereist.</span><span class="sxs-lookup"><span data-stu-id="da82d-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="da82d-138">U hoeft de module alleen aan de PDP-sjabloon toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="da82d-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="da82d-139">De volgende illustraties laten zien hoe een PDP-sjabloon eruitziet in Dynamics 365 Commerce wanneer de modules voor beoordelingen en recensies zijn geconfigureerd voor weergave op productbeschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="da82d-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="da82d-140">![PDP-sjabloon wanneer beoordelingen en recensies zijn geconfigureerd voor weergave in productbeschrijvingen](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="da82d-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="da82d-141">Module met productrecensie</span><span class="sxs-lookup"><span data-stu-id="da82d-141">Product reviews list module</span></span>

<span data-ttu-id="da82d-142">In de module met productrecensies wordt een lijst met productrecensies weergegeven met opties voor sorteren, filteren en paginering.</span><span class="sxs-lookup"><span data-stu-id="da82d-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="da82d-143">Deze module wordt normaal gesproken weergegeven na de module met het beoordelingshistogram.</span><span class="sxs-lookup"><span data-stu-id="da82d-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="da82d-144">In de volgende tabel worden de eigenschappen van de module voor productrecensielijsten weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="da82d-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="da82d-145">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="da82d-145">Property name</span></span>              | <span data-ttu-id="da82d-146">Waarde</span><span class="sxs-lookup"><span data-stu-id="da82d-146">Value</span></span> | <span data-ttu-id="da82d-147">Beschrijving eigenschap</span><span class="sxs-lookup"><span data-stu-id="da82d-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="da82d-148">Recensies die op elke pagina worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="da82d-148">Reviews shown on each page</span></span> | <span data-ttu-id="da82d-149">10</span><span class="sxs-lookup"><span data-stu-id="da82d-149">10</span></span>    | <span data-ttu-id="da82d-150">Het aantal recensies dat tegelijk op een PDP moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="da82d-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="da82d-151">De knoppen **Volgende** en **Vorige** zijn opgenomen, zodat gebruikers door de pagina's met recensies kunnen navigeren.</span><span class="sxs-lookup"><span data-stu-id="da82d-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="da82d-152">Beoordelingshistogram – overzichtsweergave</span><span class="sxs-lookup"><span data-stu-id="da82d-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="da82d-153">De module met de productrecensielijst bevat een vak waarin u een beoordelingshistogrammodule kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="da82d-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="da82d-154">In de volgende afbeelding ziet u hoe u een beoordelingshistogrammodule in de module met de productrecensielijst kunt toevoegen in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="da82d-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Een beoordelingshistogrammodule toevoegen aan de module met de productrecensielijst](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="da82d-156">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="da82d-156">Additional resources</span></span>

[<span data-ttu-id="da82d-157">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="da82d-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="da82d-158">Containermodule</span><span class="sxs-lookup"><span data-stu-id="da82d-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="da82d-159">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="da82d-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="da82d-160">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="da82d-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="da82d-161">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="da82d-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="da82d-162">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="da82d-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="da82d-163">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="da82d-163">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]