---
title: Tekstblokmodule
description: In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7dbeb8785641960cc2680335436aea10775759d3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797762"
---
# <a name="text-block-module"></a><span data-ttu-id="7d7aa-103">Text Block-module</span><span class="sxs-lookup"><span data-stu-id="7d7aa-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d7aa-104">In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7d7aa-105">Een tekstblokmodule is een module die wordt gebruikt om tekstuele inhoud toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="7d7aa-106">Deze inhoud kan informatief of promotioneel zijn.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="7d7aa-107">Tekstblokmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="7d7aa-108">Ze zijn zelfstandige modules die niet afhankelijk is van andere paginacontext of andere modules.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="7d7aa-109">Voorbeelden van tekstblokmodules in e-Commerce</span><span class="sxs-lookup"><span data-stu-id="7d7aa-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="7d7aa-110">Tekstblokmodules kunnen op de volgende manieren worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="7d7aa-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="7d7aa-111">Voor het presenteren van productfuncties op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="7d7aa-112">Voor informatieve doeleinden op elke willekeurige pagina.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-112">For informational purposes on any page.</span></span> <span data-ttu-id="7d7aa-113">Ze kunnen bijvoorbeeld de voordelen van loyaliteitsprogramma's toelichten, verzend- en retourbeleid beschrijven, veelgestelde vragen beantwoorden of informatie over het bedrijf invullen.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="7d7aa-114">Aangepaste berichten toevoegen aan een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="7d7aa-115">(bijvoorbeeld "gratis verzending voor bestellingen boven $50").</span><span class="sxs-lookup"><span data-stu-id="7d7aa-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="7d7aa-116">Voor disclaimers en contactgegevens op pagina's met productdetails, winkelwagens, kassa en andere pagina's (bijvoorbeeld "verzending en retouren vallen onder het winkelbeleid").</span><span class="sxs-lookup"><span data-stu-id="7d7aa-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="7d7aa-117">De volgende afbeelding toont een voorbeeld van een tekstblokmodule die wordt gebruikt op een introductiepagina.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Voorbeeld van een tekstblokmodule](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="7d7aa-119">Eigenschappen van tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="7d7aa-119">Text block module properties</span></span>

| <span data-ttu-id="7d7aa-120">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-120">Property name</span></span>     | <span data-ttu-id="7d7aa-121">Waarde</span><span class="sxs-lookup"><span data-stu-id="7d7aa-121">Value</span></span>                                            | <span data-ttu-id="7d7aa-122">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="7d7aa-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="7d7aa-123">RTF</span><span class="sxs-lookup"><span data-stu-id="7d7aa-123">Rich text</span></span>         | <span data-ttu-id="7d7aa-124">RTF</span><span class="sxs-lookup"><span data-stu-id="7d7aa-124">Rich text</span></span>                                        | <span data-ttu-id="7d7aa-125">Alineatekst.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-125">Paragraph text.</span></span> <span data-ttu-id="7d7aa-126">Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="7d7aa-127">Naam van aangepaste klasse</span><span class="sxs-lookup"><span data-stu-id="7d7aa-127">Custom class name</span></span> | <span data-ttu-id="7d7aa-128">Een naam voor een CSS-klasse (trapsgewijs opmaakmodel)</span><span class="sxs-lookup"><span data-stu-id="7d7aa-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="7d7aa-129">De naam van een aangepaste CSS-klasse die een ontwikkelaar biedt om deze module te formatteren.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="7d7aa-130">De klassenaam moet worden gedefinieerd in het themapakket.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="7d7aa-131">Lettergrootte</span><span class="sxs-lookup"><span data-stu-id="7d7aa-131">Font size</span></span>         | <span data-ttu-id="7d7aa-132">**Klein**, **Normaal**, **Groot** of **X-Large**</span><span class="sxs-lookup"><span data-stu-id="7d7aa-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="7d7aa-133">De lettergrootte van de inhoud.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="7d7aa-134">Een tekstblokmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="7d7aa-134">Add a text block module to a page</span></span>

<span data-ttu-id="7d7aa-135">Voer de volgende stappen uit om een tekstblokmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7d7aa-136">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7d7aa-137">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Inhoudsjabloon** in.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="7d7aa-138">Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7d7aa-139">Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7d7aa-140">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7d7aa-141">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="7d7aa-142">Selecteer in het dialoogvenster **Een sjabloon kiezen** de **Inhoudsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="7d7aa-143">Voer onder **Paginanaam** **Inhoudpagina** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="7d7aa-144">Selecteer in het vak **Hoofd** van de nieuwe pagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7d7aa-145">Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7d7aa-146">Stel in het eigenschappenvenster voor de containermodule de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="7d7aa-147">Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7d7aa-148">Selecteer in het dialoogvenster **Module toevoegen** de module **Tekstblok** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="7d7aa-149">Voeg in het eigenschappenvenster van de tekstblokmodule tekst toe aan het veld **RTF**.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="7d7aa-150">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="7d7aa-151">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="7d7aa-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d7aa-152">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="7d7aa-152">Additional resources</span></span>

[<span data-ttu-id="7d7aa-153">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="7d7aa-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7d7aa-154">Promotiebanner-module</span><span class="sxs-lookup"><span data-stu-id="7d7aa-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="7d7aa-155">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="7d7aa-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="7d7aa-156">Inhoudsblokkenmodule</span><span class="sxs-lookup"><span data-stu-id="7d7aa-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="7d7aa-157">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="7d7aa-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]