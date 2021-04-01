---
title: Beoordelings- en recensiemodules
description: In dit onderwerp worden de modules voor beoordelingen en recensies beschreven die worden gebruikt op de pagina's met productdetails in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 26658ebdbc70613baf30c344664133b9cf5911ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243764"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="c9107-103">Beoordelings- en recensiemodules</span><span class="sxs-lookup"><span data-stu-id="c9107-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c9107-104">In dit onderwerp worden de modules voor beoordelingen en recensies beschreven die worden gebruikt op de pagina's met productdetails (PDP's) in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9107-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c9107-105">Beoordelingen en recensies over e-commerce-websites geven klanten meer informatie over producten voordat ze een aankoopbeslissing nemen en vormen tevens een mechanisme voor het verzamelen van feedback van klanten over producten.</span><span class="sxs-lookup"><span data-stu-id="c9107-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="c9107-106">Beoordelingen worden weergegeven op pagina's met productlijsten, lijstpagina's categorieën of zoekresultaten en andere sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="c9107-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="c9107-107">Beoordelingshistogrammen en productrecensies worden weergegeven op PDP's.</span><span class="sxs-lookup"><span data-stu-id="c9107-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="c9107-108">Met een knop **Schrijf een recensie** kunnen klanten beoordelingen en recensies voor een product verzenden.</span><span class="sxs-lookup"><span data-stu-id="c9107-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="c9107-109">Deze PDP-functies worden geregeld door middel van modules voor beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="c9107-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="c9107-110">Beoordelings- en recensiemodules op pagina's met productgegevens</span><span class="sxs-lookup"><span data-stu-id="c9107-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="c9107-111">Drie modules geven een overzicht van beoordelingen en recensies voor pagina's met productgegevens:</span><span class="sxs-lookup"><span data-stu-id="c9107-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="c9107-112">Module voor recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="c9107-112">Write review module</span></span>
- <span data-ttu-id="c9107-113">Module met productrecensie</span><span class="sxs-lookup"><span data-stu-id="c9107-113">Product reviews list module</span></span>
- <span data-ttu-id="c9107-114">Module met beoordelingshistogram</span><span class="sxs-lookup"><span data-stu-id="c9107-114">Ratings histogram module</span></span>
 
<span data-ttu-id="c9107-115">In de volgende afbeelding ziet u hoe de modules voor beoordelingen en recensies er uitzien op een PDP.</span><span class="sxs-lookup"><span data-stu-id="c9107-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Beoordelings- en recensiemodules op een PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="c9107-117">Zie [Overzicht van sjablonen en indelingen](templates-layouts-overview.md) voor informatie over het optimaliseren van de PDP-sjablonen en -indelingen zodat u de configuraties voor beoordelingen en revisies kunt delen tussen meerdere PDP-pagina's op uw e-commerce-site.</span><span class="sxs-lookup"><span data-stu-id="c9107-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="c9107-118">In de volgende afbeelding ziet u hoe in het dialoogvenster **Module toevoegen** modules voor beoordelingen en recensies in Dynamics 365 Commerce worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c9107-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="c9107-119">![Het dialoogvenster Module toevoegen](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="c9107-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="c9107-120">Module voor recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="c9107-120">Write review module</span></span>

<span data-ttu-id="c9107-121">De module voor het schrijven van een recensie bevat een knop **Schrijf een recensie** waarmee gebruikers zich kunnen aanmelden, een beoordeling kunnen toewijzen en een recensie van een product kunnen schrijven.</span><span class="sxs-lookup"><span data-stu-id="c9107-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="c9107-122">Met deze module kunnen gebruikers ook een beoordeling of een recensie bewerken die ze eerder hebben ingediend.</span><span class="sxs-lookup"><span data-stu-id="c9107-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="c9107-123">Deze module wordt meestal weergegeven boven het beoordelingshistogram en de lijstmodules met productrecensies op een PDP.</span><span class="sxs-lookup"><span data-stu-id="c9107-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="c9107-124">In de volgende afbeelding ziet u het dialoogvenster **Schrijf een recensie** dat wordt weergegeven wanneer een klant **Schrijf een recensie** selecteert.</span><span class="sxs-lookup"><span data-stu-id="c9107-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="c9107-125">De klant kan dit dialoog venster gebruiken om een beoordeling en een recensie in te dienen.</span><span class="sxs-lookup"><span data-stu-id="c9107-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="c9107-126">![Dialoogvenster Schrijf een recensie](media/rnr-eCommerce-write-review-module.png) In de volgende tabel wordt de eigenschap van de module voor het schrijven van een recensie weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="c9107-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="c9107-127">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="c9107-127">Property name</span></span> | <span data-ttu-id="c9107-128">Waarde</span><span class="sxs-lookup"><span data-stu-id="c9107-128">Value</span></span>        | <span data-ttu-id="c9107-129">Beschrijving eigenschap</span><span class="sxs-lookup"><span data-stu-id="c9107-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="c9107-130">Naam</span><span class="sxs-lookup"><span data-stu-id="c9107-130">Name</span></span>          | <span data-ttu-id="c9107-131">Recensie schrijven</span><span class="sxs-lookup"><span data-stu-id="c9107-131">Write review</span></span> | <span data-ttu-id="c9107-132">De naam van de module voor het schrijven van een recensie.</span><span class="sxs-lookup"><span data-stu-id="c9107-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="c9107-133">Module met beoordelingshistogram</span><span class="sxs-lookup"><span data-stu-id="c9107-133">Ratings histogram module</span></span>

<span data-ttu-id="c9107-134">In de module met het beoordelingshistogram wordt een beoordelingshistogram weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c9107-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="c9107-135">Deze module wordt meestal weergegeven tussen de module Schrijf een recensie en de module met de productrecensielijst op een PDP-pagina.</span><span class="sxs-lookup"><span data-stu-id="c9107-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="c9107-136">Voor de module met het beoordelingshistogram is geen configuratie vereist.</span><span class="sxs-lookup"><span data-stu-id="c9107-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="c9107-137">U hoeft de module alleen aan de PDP-sjabloon toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c9107-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="c9107-138">De volgende illustraties laten zien hoe een PDP-sjabloon eruitziet in Dynamics 365 Commerce wanneer de modules voor beoordelingen en recensies zijn geconfigureerd voor weergave op productbeschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="c9107-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="c9107-139">![PDP-sjabloon wanneer beoordelingen en recensies zijn geconfigureerd voor weergave in productbeschrijvingen](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="c9107-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="c9107-140">Module met productrecensie</span><span class="sxs-lookup"><span data-stu-id="c9107-140">Product reviews list module</span></span>

<span data-ttu-id="c9107-141">In de module met productrecensies wordt een lijst met productrecensies weergegeven met opties voor sorteren, filteren en paginering.</span><span class="sxs-lookup"><span data-stu-id="c9107-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="c9107-142">Deze module wordt normaal gesproken weergegeven na de module met het beoordelingshistogram.</span><span class="sxs-lookup"><span data-stu-id="c9107-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="c9107-143">In de volgende tabel worden de eigenschappen van de module voor productrecensielijsten weergegeven die moet worden geconfigureerd in het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="c9107-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="c9107-144">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="c9107-144">Property name</span></span>              | <span data-ttu-id="c9107-145">Waarde</span><span class="sxs-lookup"><span data-stu-id="c9107-145">Value</span></span> | <span data-ttu-id="c9107-146">Beschrijving eigenschap</span><span class="sxs-lookup"><span data-stu-id="c9107-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="c9107-147">Recensies die op elke pagina worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="c9107-147">Reviews shown on each page</span></span> | <span data-ttu-id="c9107-148">10</span><span class="sxs-lookup"><span data-stu-id="c9107-148">10</span></span>    | <span data-ttu-id="c9107-149">Het aantal recensies dat tegelijk op een PDP moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c9107-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="c9107-150">De knoppen **Volgende** en **Vorige** zijn opgenomen, zodat gebruikers door de pagina's met recensies kunnen navigeren.</span><span class="sxs-lookup"><span data-stu-id="c9107-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="c9107-151">Beoordelingshistogram – overzichtsweergave</span><span class="sxs-lookup"><span data-stu-id="c9107-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="c9107-152">De module met de productrecensielijst bevat een vak waarin u een beoordelingshistogrammodule kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c9107-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="c9107-153">In de volgende afbeelding ziet u hoe u een beoordelingshistogrammodule in de module met de productrecensielijst kunt toevoegen in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9107-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Een beoordelingshistogrammodule toevoegen aan de module met de productrecensielijst](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="c9107-155">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c9107-155">Additional resources</span></span>

[<span data-ttu-id="c9107-156">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="c9107-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c9107-157">Containermodule</span><span class="sxs-lookup"><span data-stu-id="c9107-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c9107-158">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="c9107-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c9107-159">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="c9107-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c9107-160">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="c9107-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c9107-161">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="c9107-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c9107-162">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="c9107-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]