---
title: Carrouselmodule
description: In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 10ff0cd566a1a8d89ccadce9571dafc5a592520b
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/27/2020
ms.locfileid: "3620981"
---
# <a name="carousel-module"></a><span data-ttu-id="06eb7-103">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="06eb7-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="06eb7-104">In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="06eb7-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="06eb7-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="06eb7-105">Overview</span></span>

<span data-ttu-id="06eb7-106">Een carrouselmodule wordt gebruikt voor het plaatsen van meerdere promotieartikelen (met afbeeldingen) in een draaiende carrouselbanner waar klanten doorheen kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="06eb7-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="06eb7-107">Een detailhandelaar kan bijvoorbeeld een carrouselmodule op een startpagina gebruiken om meerdere nieuwe producten of promoties te presenteren.</span><span class="sxs-lookup"><span data-stu-id="06eb7-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="06eb7-108">U kunt inhoudsblokmodules in een carrouselmodule toevoegen.</span><span class="sxs-lookup"><span data-stu-id="06eb7-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="06eb7-109">De eigenschappen van de carrouselmodule bepalen vervolgens hoe deze modules worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="06eb7-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="06eb7-110">Voorbeelden van carrouselmodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="06eb7-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="06eb7-111">Een carrousel met meerdere promotiemodules kan worden gebruikt op een startpagina.</span><span class="sxs-lookup"><span data-stu-id="06eb7-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="06eb7-112">Een carrousel met meerdere promotiemodules kan worden gebruikt op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="06eb7-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="06eb7-113">Een carrousel kan op elke marketingpagina worden gebruikt om meerdere promoties of producten te promoten.</span><span class="sxs-lookup"><span data-stu-id="06eb7-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="06eb7-114">De volgende afbeelding toont een voorbeeld van een carrouselmodule die wordt gebruikt op een introductiepagina.</span><span class="sxs-lookup"><span data-stu-id="06eb7-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="06eb7-115">Deze carrouselmodule bevat meerdere inhoudsblokitems.</span><span class="sxs-lookup"><span data-stu-id="06eb7-115">This carousel module contains multiple content block items.</span></span>

![Voorbeeld van een carrouselmodule](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="06eb7-117">Eigenschappen van carrouselmodules</span><span class="sxs-lookup"><span data-stu-id="06eb7-117">Carousel module properties</span></span>

| <span data-ttu-id="06eb7-118">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="06eb7-118">Property name</span></span>             | <span data-ttu-id="06eb7-119">Waarde</span><span class="sxs-lookup"><span data-stu-id="06eb7-119">Value</span></span>                 | <span data-ttu-id="06eb7-120">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="06eb7-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="06eb7-121">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="06eb7-121">Autoplay</span></span>                  | <span data-ttu-id="06eb7-122">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="06eb7-122">**True** or **False**</span></span> | <span data-ttu-id="06eb7-123">Als de waarde is ingesteld op **True**, vindt de overgang tussen items binnen de carrousel automatisch plaats.</span><span class="sxs-lookup"><span data-stu-id="06eb7-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="06eb7-124">Als de waarde is ingesteld op **False**, vindt er geen overgang plaats tenzij de klant het toetsenbord of de muis gebruikt om van het ene naar het volgende item te gaan.</span><span class="sxs-lookup"><span data-stu-id="06eb7-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="06eb7-125">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="06eb7-125">Slide transition interval</span></span> | <span data-ttu-id="06eb7-126">Een waarde in seconden</span><span class="sxs-lookup"><span data-stu-id="06eb7-126">A value in seconds</span></span>    | <span data-ttu-id="06eb7-127">Het interval voor overgangen tussen items.</span><span class="sxs-lookup"><span data-stu-id="06eb7-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="06eb7-128">Overgangstype</span><span class="sxs-lookup"><span data-stu-id="06eb7-128">Transition type</span></span>           | <span data-ttu-id="06eb7-129">**Verschuiven** of **Vervagen**</span><span class="sxs-lookup"><span data-stu-id="06eb7-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="06eb7-130">Het overgangseffect tussen artikelen.</span><span class="sxs-lookup"><span data-stu-id="06eb7-130">The transition effect between items.</span></span> |
| <span data-ttu-id="06eb7-131">Carrouselflipper verbergen</span><span class="sxs-lookup"><span data-stu-id="06eb7-131">Hide carousel flipper</span></span>     | <span data-ttu-id="06eb7-132">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="06eb7-132">**True** or **False**</span></span> | <span data-ttu-id="06eb7-133">Als de waarde is ingesteld op **True**, worden de carrouselflipper en reeksindicator verborgen.</span><span class="sxs-lookup"><span data-stu-id="06eb7-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="06eb7-134">Sluiten van carrousel toestaan</span><span class="sxs-lookup"><span data-stu-id="06eb7-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="06eb7-135">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="06eb7-135">**True** or **False**</span></span> | <span data-ttu-id="06eb7-136">Als de waarde is ingesteld op **True**, kunnen gebruikers de carrousel sluiten.</span><span class="sxs-lookup"><span data-stu-id="06eb7-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="06eb7-137">Een carrouselmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="06eb7-137">Add a carousel module to a page</span></span>

<span data-ttu-id="06eb7-138">Voer de volgende stappen uit om een carrouselmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="06eb7-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="06eb7-139">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="06eb7-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="06eb7-140">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Carrouselsjabloon** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="06eb7-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="06eb7-141">Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.</span><span class="sxs-lookup"><span data-stu-id="06eb7-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="06eb7-142">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="06eb7-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="06eb7-143">Gebruik de carrouselsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Carrouselpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="06eb7-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="06eb7-144">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="06eb7-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="06eb7-145">Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Scherm vullen**.</span><span class="sxs-lookup"><span data-stu-id="06eb7-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="06eb7-146">Voeg onder **Paginaoverzicht** een carrouselmodule aan de containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="06eb7-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="06eb7-147">Voeg aan de carrouselmodule een inhoudsblokmodule toe.</span><span class="sxs-lookup"><span data-stu-id="06eb7-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="06eb7-148">Stel de eigenschappen van de inhoudsblokmodule in door **Koptekst**, **Koppeling**, **Indeling** en andere eigenschappen op te geven.</span><span class="sxs-lookup"><span data-stu-id="06eb7-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="06eb7-149">U kunt nog een inhoudsblokmodule toevoegen en configureren.</span><span class="sxs-lookup"><span data-stu-id="06eb7-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="06eb7-150">Stel zo nodig aanvullende eigenschappen in voor de carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="06eb7-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="06eb7-151">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="06eb7-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="06eb7-152">Op de pagina ziet u een carrousel met twee modules (een heldmodule en een functiemodule).</span><span class="sxs-lookup"><span data-stu-id="06eb7-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="06eb7-153">U kunt aanvullende eigenschappen voor de modules carrousel, held en functie wijzigen om het gewenste effect te bereiken.</span><span class="sxs-lookup"><span data-stu-id="06eb7-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="06eb7-154">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="06eb7-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06eb7-155">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="06eb7-155">Additional resources</span></span>

[<span data-ttu-id="06eb7-156">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="06eb7-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="06eb7-157">Promotiebanner-module</span><span class="sxs-lookup"><span data-stu-id="06eb7-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="06eb7-158">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="06eb7-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="06eb7-159">Inhoudsblokmodule</span><span class="sxs-lookup"><span data-stu-id="06eb7-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="06eb7-160">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="06eb7-160">Video player module</span></span>](add-video-player.md)
