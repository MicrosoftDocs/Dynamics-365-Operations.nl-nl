---
title: Tekstblokmodule
description: In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025592"
---
# <a name="text-block-module"></a><span data-ttu-id="98d3e-103">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="98d3e-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="98d3e-104">In dit onderwerp wordt beschreven wat tekstblokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="98d3e-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="98d3e-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="98d3e-105">Overview</span></span>

<span data-ttu-id="98d3e-106">Een tekstblokmodule is een module die wordt gebruikt om tekstuele inhoud toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="98d3e-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="98d3e-107">Deze inhoud kan informatief of promotioneel zijn.</span><span class="sxs-lookup"><span data-stu-id="98d3e-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="98d3e-108">Tekstblokmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="98d3e-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="98d3e-109">Ze zijn zelfstandige modules die niet afhankelijk is van andere paginacontext of andere modules.</span><span class="sxs-lookup"><span data-stu-id="98d3e-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="98d3e-110">Voorbeelden van tekstblokmodules in e-Commerce</span><span class="sxs-lookup"><span data-stu-id="98d3e-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="98d3e-111">Tekstblokmodules kunnen op de volgende manieren worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="98d3e-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="98d3e-112">Voor het presenteren van productfuncties op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="98d3e-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="98d3e-113">Voor informatieve doeleinden op elke willekeurige pagina.</span><span class="sxs-lookup"><span data-stu-id="98d3e-113">For informational purposes on any page.</span></span> <span data-ttu-id="98d3e-114">Ze kunnen bijvoorbeeld de voordelen van loyaliteitsprogramma's toelichten, verzend- en retourbeleid beschrijven, veelgestelde vragen beantwoorden of informatie over het bedrijf invullen.</span><span class="sxs-lookup"><span data-stu-id="98d3e-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="98d3e-115">Aangepaste berichten toevoegen aan een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="98d3e-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="98d3e-116">(bijvoorbeeld "gratis verzending voor bestellingen boven $50").</span><span class="sxs-lookup"><span data-stu-id="98d3e-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="98d3e-117">Voor disclaimers en contactgegevens op pagina's met productdetails, winkelwagens, kassa en andere pagina's (bijvoorbeeld "verzending en retouren vallen onder het winkelbeleid").</span><span class="sxs-lookup"><span data-stu-id="98d3e-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="98d3e-118">Eigenschappen van tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="98d3e-118">Text block module properties</span></span>

| <span data-ttu-id="98d3e-119">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="98d3e-119">Property name</span></span>     | <span data-ttu-id="98d3e-120">Value</span><span class="sxs-lookup"><span data-stu-id="98d3e-120">Value</span></span>                                            | <span data-ttu-id="98d3e-121">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="98d3e-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="98d3e-122">RTF</span><span class="sxs-lookup"><span data-stu-id="98d3e-122">Rich text</span></span>         | <span data-ttu-id="98d3e-123">RTF</span><span class="sxs-lookup"><span data-stu-id="98d3e-123">Rich text</span></span>                                        | <span data-ttu-id="98d3e-124">Alineatekst.</span><span class="sxs-lookup"><span data-stu-id="98d3e-124">Paragraph text.</span></span> <span data-ttu-id="98d3e-125">Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst.</span><span class="sxs-lookup"><span data-stu-id="98d3e-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="98d3e-126">Naam van aangepaste klasse</span><span class="sxs-lookup"><span data-stu-id="98d3e-126">Custom class name</span></span> | <span data-ttu-id="98d3e-127">Een naam voor een CSS-klasse (trapsgewijs opmaakmodel)</span><span class="sxs-lookup"><span data-stu-id="98d3e-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="98d3e-128">De naam van een aangepaste CSS-klasse die een ontwikkelaar biedt om deze module te formatteren.</span><span class="sxs-lookup"><span data-stu-id="98d3e-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="98d3e-129">De klassenaam moet worden gedefinieerd in het themapakket.</span><span class="sxs-lookup"><span data-stu-id="98d3e-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="98d3e-130">Lettergrootte</span><span class="sxs-lookup"><span data-stu-id="98d3e-130">Font size</span></span>         | <span data-ttu-id="98d3e-131">**Klein**, **Normaal**, **Groot** of **X-Large**</span><span class="sxs-lookup"><span data-stu-id="98d3e-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="98d3e-132">De lettergrootte van de inhoud.</span><span class="sxs-lookup"><span data-stu-id="98d3e-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="98d3e-133">Een tekstblokmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="98d3e-133">Add a text block module to a page</span></span>

<span data-ttu-id="98d3e-134">Voer de volgende stappen uit om een tekstblokmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="98d3e-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="98d3e-135">Maak een paginasjabloon met de naam **Inhoudsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="98d3e-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="98d3e-136">Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.</span><span class="sxs-lookup"><span data-stu-id="98d3e-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="98d3e-137">Voltooi het bewerken van de sjabloon en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="98d3e-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="98d3e-138">Gebruik de inhoudsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Inhoudpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="98d3e-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="98d3e-139">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="98d3e-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="98d3e-140">Stel in het eigenschappenvenster voor de containermodule de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="98d3e-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="98d3e-141">Voeg een tekstblokmodule toe aan de containermodule.</span><span class="sxs-lookup"><span data-stu-id="98d3e-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="98d3e-142">Voeg in het eigenschappenvenster van de tekstblokmodule tekst toe aan het veld **RTF**.</span><span class="sxs-lookup"><span data-stu-id="98d3e-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="98d3e-143">Voltooi het bewerken van de pagina en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="98d3e-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98d3e-144">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="98d3e-144">Additional resources</span></span>

[<span data-ttu-id="98d3e-145">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="98d3e-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="98d3e-146">Promospandoekmodule</span><span class="sxs-lookup"><span data-stu-id="98d3e-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="98d3e-147">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="98d3e-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="98d3e-148">Inhoudsblokmodule</span><span class="sxs-lookup"><span data-stu-id="98d3e-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="98d3e-149">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="98d3e-149">Video player module</span></span>](add-video-player.md)

