---
title: Tekstblokmodule
description: In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817373"
---
# <a name="text-block-module"></a><span data-ttu-id="558b3-103">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="558b3-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="558b3-104">In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="558b3-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="558b3-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="558b3-105">Overview</span></span>

<span data-ttu-id="558b3-106">Een tekstblokmodule is een module die wordt gebruikt om tekstuele inhoud toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="558b3-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="558b3-107">Deze inhoud kan informatief of promotioneel zijn.</span><span class="sxs-lookup"><span data-stu-id="558b3-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="558b3-108">Tekstblokmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="558b3-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="558b3-109">Ze zijn zelfstandige modules die niet afhankelijk is van andere paginacontext of andere modules.</span><span class="sxs-lookup"><span data-stu-id="558b3-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="558b3-110">Voorbeelden van tekstblokmodules in e-Commerce</span><span class="sxs-lookup"><span data-stu-id="558b3-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="558b3-111">Tekstblokmodules kunnen op de volgende manieren worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="558b3-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="558b3-112">Voor het presenteren van productfuncties op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="558b3-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="558b3-113">Voor informatieve doeleinden op elke willekeurige pagina.</span><span class="sxs-lookup"><span data-stu-id="558b3-113">For informational purposes on any page.</span></span> <span data-ttu-id="558b3-114">Ze kunnen bijvoorbeeld de voordelen van loyaliteitsprogramma's toelichten, verzend- en retourbeleid beschrijven, veelgestelde vragen beantwoorden of informatie over het bedrijf invullen.</span><span class="sxs-lookup"><span data-stu-id="558b3-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="558b3-115">Aangepaste berichten toevoegen aan een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="558b3-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="558b3-116">(bijvoorbeeld "gratis verzending voor bestellingen boven $50").</span><span class="sxs-lookup"><span data-stu-id="558b3-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="558b3-117">Voor disclaimers en contactgegevens op pagina's met productdetails, winkelwagens, kassa en andere pagina's (bijvoorbeeld "verzending en retouren vallen onder het winkelbeleid").</span><span class="sxs-lookup"><span data-stu-id="558b3-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="558b3-118">De volgende afbeelding toont een voorbeeld van een tekstblokmodule die wordt gebruikt op een introductiepagina.</span><span class="sxs-lookup"><span data-stu-id="558b3-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Voorbeeld van een tekstblokmodule](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="558b3-120">Eigenschappen van tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="558b3-120">Text block module properties</span></span>

| <span data-ttu-id="558b3-121">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="558b3-121">Property name</span></span>     | <span data-ttu-id="558b3-122">Waarde</span><span class="sxs-lookup"><span data-stu-id="558b3-122">Value</span></span>                                            | <span data-ttu-id="558b3-123">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="558b3-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="558b3-124">RTF</span><span class="sxs-lookup"><span data-stu-id="558b3-124">Rich text</span></span>         | <span data-ttu-id="558b3-125">RTF</span><span class="sxs-lookup"><span data-stu-id="558b3-125">Rich text</span></span>                                        | <span data-ttu-id="558b3-126">Alineatekst.</span><span class="sxs-lookup"><span data-stu-id="558b3-126">Paragraph text.</span></span> <span data-ttu-id="558b3-127">Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst.</span><span class="sxs-lookup"><span data-stu-id="558b3-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="558b3-128">Naam van aangepaste klasse</span><span class="sxs-lookup"><span data-stu-id="558b3-128">Custom class name</span></span> | <span data-ttu-id="558b3-129">Een naam voor een CSS-klasse (trapsgewijs opmaakmodel)</span><span class="sxs-lookup"><span data-stu-id="558b3-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="558b3-130">De naam van een aangepaste CSS-klasse die een ontwikkelaar biedt om deze module te formatteren.</span><span class="sxs-lookup"><span data-stu-id="558b3-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="558b3-131">De klassenaam moet worden gedefinieerd in het themapakket.</span><span class="sxs-lookup"><span data-stu-id="558b3-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="558b3-132">Lettergrootte</span><span class="sxs-lookup"><span data-stu-id="558b3-132">Font size</span></span>         | <span data-ttu-id="558b3-133">**Klein**, **Normaal**, **Groot** of **X-Large**</span><span class="sxs-lookup"><span data-stu-id="558b3-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="558b3-134">De lettergrootte van de inhoud.</span><span class="sxs-lookup"><span data-stu-id="558b3-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="558b3-135">Een tekstblokmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="558b3-135">Add a text block module to a page</span></span>

<span data-ttu-id="558b3-136">Voer de volgende stappen uit om een tekstblokmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="558b3-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="558b3-137">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="558b3-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="558b3-138">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Inhoudsjabloon** in.</span><span class="sxs-lookup"><span data-stu-id="558b3-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="558b3-139">Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="558b3-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="558b3-140">Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="558b3-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="558b3-141">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="558b3-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="558b3-142">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="558b3-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="558b3-143">Selecteer in het dialoogvenster **Een sjabloon kiezen** de **Inhoudsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="558b3-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="558b3-144">Voer onder **Paginanaam** **Inhoudpagina** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="558b3-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="558b3-145">Selecteer in het vak **Hoofd** van de nieuwe pagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="558b3-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="558b3-146">Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="558b3-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="558b3-147">Stel in het eigenschappenvenster voor de containermodule de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="558b3-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="558b3-148">Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="558b3-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="558b3-149">Selecteer in het dialoogvenster **Module toevoegen** de module **Tekstblok** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="558b3-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="558b3-150">Voeg in het eigenschappenvenster van de tekstblokmodule tekst toe aan het veld **RTF**.</span><span class="sxs-lookup"><span data-stu-id="558b3-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="558b3-151">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="558b3-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="558b3-152">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="558b3-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="558b3-153">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="558b3-153">Additional resources</span></span>

[<span data-ttu-id="558b3-154">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="558b3-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="558b3-155">Promotiebanner-module</span><span class="sxs-lookup"><span data-stu-id="558b3-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="558b3-156">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="558b3-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="558b3-157">Inhoudsblokkenmodule</span><span class="sxs-lookup"><span data-stu-id="558b3-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="558b3-158">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="558b3-158">Video player module</span></span>](add-video-player.md)

