---
title: Carrouselmodule
description: In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025776"
---
# <a name="carousel-module"></a><span data-ttu-id="88ca8-103">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="88ca8-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="88ca8-104">In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="88ca8-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="88ca8-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="88ca8-105">Overview</span></span>

<span data-ttu-id="88ca8-106">Een carrouselmodule wordt gebruikt voor het plaatsen van meerdere promotieartikelen (met afbeeldingen) in een draaiende carrouselbanner waar klanten doorheen kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="88ca8-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="88ca8-107">Een detailhandelaar kan bijvoorbeeld een carrouselmodule op een startpagina gebruiken om meerdere nieuwe producten of promoties te presenteren.</span><span class="sxs-lookup"><span data-stu-id="88ca8-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="88ca8-108">U kunt inhoudsblokmodules in een carrouselmodule toevoegen.</span><span class="sxs-lookup"><span data-stu-id="88ca8-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="88ca8-109">De eigenschappen van de carrouselmodule bepalen vervolgens hoe deze modules worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="88ca8-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="88ca8-110">Voorbeelden van carrouselmodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="88ca8-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="88ca8-111">Een carrousel met meerdere promotiemodules kan worden gebruikt op een startpagina.</span><span class="sxs-lookup"><span data-stu-id="88ca8-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="88ca8-112">Een carrousel met meerdere promotiemodules kan worden gebruikt op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="88ca8-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="88ca8-113">Een carrousel kan op elke marketingpagina worden gebruikt om meerdere promoties of producten te promoten.</span><span class="sxs-lookup"><span data-stu-id="88ca8-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="88ca8-114">Eigenschappen van carrouselmodules</span><span class="sxs-lookup"><span data-stu-id="88ca8-114">Carousel module properties</span></span>

| <span data-ttu-id="88ca8-115">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="88ca8-115">Property name</span></span>             | <span data-ttu-id="88ca8-116">Waarde</span><span class="sxs-lookup"><span data-stu-id="88ca8-116">Value</span></span>                 | <span data-ttu-id="88ca8-117">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="88ca8-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="88ca8-118">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="88ca8-118">Autoplay</span></span>                  | <span data-ttu-id="88ca8-119">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="88ca8-119">**True** or **False**</span></span> | <span data-ttu-id="88ca8-120">Als de waarde is ingesteld op **True**, vindt de overgang tussen items binnen de carrousel automatisch plaats.</span><span class="sxs-lookup"><span data-stu-id="88ca8-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="88ca8-121">Als de waarde is ingesteld op **False**, vindt er geen overgang plaats tenzij de klant het toetsenbord of de muis gebruikt om van het ene naar het volgende item te gaan.</span><span class="sxs-lookup"><span data-stu-id="88ca8-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="88ca8-122">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="88ca8-122">Slide transition interval</span></span> | <span data-ttu-id="88ca8-123">Een waarde in seconden</span><span class="sxs-lookup"><span data-stu-id="88ca8-123">A value in seconds</span></span>    | <span data-ttu-id="88ca8-124">Het interval voor overgangen tussen items.</span><span class="sxs-lookup"><span data-stu-id="88ca8-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="88ca8-125">Overgangstype</span><span class="sxs-lookup"><span data-stu-id="88ca8-125">Transition type</span></span>           | <span data-ttu-id="88ca8-126">**Verschuiven** of **Vervagen**</span><span class="sxs-lookup"><span data-stu-id="88ca8-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="88ca8-127">Het overgangseffect tussen artikelen.</span><span class="sxs-lookup"><span data-stu-id="88ca8-127">The transition effect between items.</span></span> |
| <span data-ttu-id="88ca8-128">Carrouselflipper verbergen</span><span class="sxs-lookup"><span data-stu-id="88ca8-128">Hide carousel flipper</span></span>     | <span data-ttu-id="88ca8-129">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="88ca8-129">**True** or **False**</span></span> | <span data-ttu-id="88ca8-130">Als de waarde is ingesteld op **True**, worden de carrouselflipper en reeksindicator verborgen.</span><span class="sxs-lookup"><span data-stu-id="88ca8-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="88ca8-131">Sluiten van carrousel toestaan</span><span class="sxs-lookup"><span data-stu-id="88ca8-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="88ca8-132">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="88ca8-132">**True** or **False**</span></span> | <span data-ttu-id="88ca8-133">Als de waarde is ingesteld op **True**, kunnen gebruikers de carrousel sluiten.</span><span class="sxs-lookup"><span data-stu-id="88ca8-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="88ca8-134">Een carrouselmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="88ca8-134">Add a carousel module to a page</span></span>

<span data-ttu-id="88ca8-135">Voer de volgende stappen uit om een carrouselmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="88ca8-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="88ca8-136">Maak een paginasjabloon met de naam **Carrouselsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="88ca8-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="88ca8-137">Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.</span><span class="sxs-lookup"><span data-stu-id="88ca8-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="88ca8-138">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="88ca8-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="88ca8-139">Gebruik de carrouselsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Carrouselpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="88ca8-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="88ca8-140">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="88ca8-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="88ca8-141">Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Scherm vullen**.</span><span class="sxs-lookup"><span data-stu-id="88ca8-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="88ca8-142">Voeg onder **Paginaoverzicht** een carrouselmodule aan de containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="88ca8-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="88ca8-143">Voeg aan de carrouselmodule een inhoudsblokmodule toe.</span><span class="sxs-lookup"><span data-stu-id="88ca8-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="88ca8-144">Stel de eigenschappen van de inhoudsblokmodule in door **Koptekst**, **Koppeling**, **Indeling** en andere eigenschappen op te geven.</span><span class="sxs-lookup"><span data-stu-id="88ca8-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="88ca8-145">U kunt nog een inhoudsblokmodule toevoegen en configureren.</span><span class="sxs-lookup"><span data-stu-id="88ca8-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="88ca8-146">Stel zo nodig aanvullende eigenschappen in voor de carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="88ca8-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="88ca8-147">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="88ca8-147">Save and preview the page.</span></span> <span data-ttu-id="88ca8-148">Op de pagina ziet u een carrousel met twee modules (een heldmodule en een functiemodule).</span><span class="sxs-lookup"><span data-stu-id="88ca8-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="88ca8-149">U kunt aanvullende eigenschappen voor de modules carrousel, held en functie wijzigen om het gewenste effect te bereiken.</span><span class="sxs-lookup"><span data-stu-id="88ca8-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="88ca8-150">Voltooi het bewerken van de pagina en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="88ca8-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88ca8-151">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="88ca8-151">Additional resources</span></span>

[<span data-ttu-id="88ca8-152">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="88ca8-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="88ca8-153">Promospandoekmodule</span><span class="sxs-lookup"><span data-stu-id="88ca8-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="88ca8-154">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="88ca8-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="88ca8-155">Inhoudsblokmodule</span><span class="sxs-lookup"><span data-stu-id="88ca8-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="88ca8-156">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="88ca8-156">Video player module</span></span>](add-video-player.md)
