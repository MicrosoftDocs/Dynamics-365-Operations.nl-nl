---
title: Carrouselmodule
description: In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5bc2227e08dbbf5f76a37180114e5affff131658
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797882"
---
# <a name="carousel-module"></a><span data-ttu-id="f29f9-103">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="f29f9-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f29f9-104">In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f29f9-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f29f9-105">Een carrouselmodule wordt gebruikt voor het plaatsen van meerdere promotieartikelen (met afbeeldingen) in een draaiende carrouselbanner waar klanten doorheen kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="f29f9-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="f29f9-106">Een detailhandelaar kan bijvoorbeeld een carrouselmodule op een startpagina gebruiken om meerdere nieuwe producten of promoties te presenteren.</span><span class="sxs-lookup"><span data-stu-id="f29f9-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="f29f9-107">U kunt inhoudsblokmodules in een carrouselmodule toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f29f9-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="f29f9-108">De eigenschappen van de carrouselmodule bepalen vervolgens hoe deze modules worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f29f9-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="f29f9-109">Voorbeelden van carrouselmodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="f29f9-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="f29f9-110">Een carrousel met meerdere promotiemodules kan worden gebruikt op een startpagina.</span><span class="sxs-lookup"><span data-stu-id="f29f9-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="f29f9-111">Een carrousel met meerdere promotiemodules kan worden gebruikt op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="f29f9-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="f29f9-112">Een carrousel kan op elke marketingpagina worden gebruikt om meerdere promoties of producten te promoten.</span><span class="sxs-lookup"><span data-stu-id="f29f9-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="f29f9-113">De volgende afbeelding toont een voorbeeld van een carrouselmodule die wordt gebruikt op een introductiepagina.</span><span class="sxs-lookup"><span data-stu-id="f29f9-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="f29f9-114">Deze carrouselmodule bevat meerdere inhoudsblokitems.</span><span class="sxs-lookup"><span data-stu-id="f29f9-114">This carousel module contains multiple content block items.</span></span>

![Voorbeeld van een carrouselmodule](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="f29f9-116">Eigenschappen van carrouselmodules</span><span class="sxs-lookup"><span data-stu-id="f29f9-116">Carousel module properties</span></span>

| <span data-ttu-id="f29f9-117">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="f29f9-117">Property name</span></span>             | <span data-ttu-id="f29f9-118">Waarde</span><span class="sxs-lookup"><span data-stu-id="f29f9-118">Value</span></span>                 | <span data-ttu-id="f29f9-119">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f29f9-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f29f9-120">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="f29f9-120">Autoplay</span></span>                  | <span data-ttu-id="f29f9-121">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="f29f9-121">**True** or **False**</span></span> | <span data-ttu-id="f29f9-122">Als de waarde is ingesteld op **True**, vindt de overgang tussen items binnen de carrousel automatisch plaats.</span><span class="sxs-lookup"><span data-stu-id="f29f9-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="f29f9-123">Als de waarde is ingesteld op **False**, vindt er geen overgang plaats tenzij de klant het toetsenbord of de muis gebruikt om van het ene naar het volgende item te gaan.</span><span class="sxs-lookup"><span data-stu-id="f29f9-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="f29f9-124">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="f29f9-124">Slide transition interval</span></span> | <span data-ttu-id="f29f9-125">Een waarde in seconden</span><span class="sxs-lookup"><span data-stu-id="f29f9-125">A value in seconds</span></span>    | <span data-ttu-id="f29f9-126">Het interval voor overgangen tussen items.</span><span class="sxs-lookup"><span data-stu-id="f29f9-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="f29f9-127">Overgangstype</span><span class="sxs-lookup"><span data-stu-id="f29f9-127">Transition type</span></span>           | <span data-ttu-id="f29f9-128">**Verschuiven** of **Vervagen**</span><span class="sxs-lookup"><span data-stu-id="f29f9-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="f29f9-129">Het overgangseffect tussen artikelen.</span><span class="sxs-lookup"><span data-stu-id="f29f9-129">The transition effect between items.</span></span> |
| <span data-ttu-id="f29f9-130">Carrouselflipper verbergen</span><span class="sxs-lookup"><span data-stu-id="f29f9-130">Hide carousel flipper</span></span>     | <span data-ttu-id="f29f9-131">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="f29f9-131">**True** or **False**</span></span> | <span data-ttu-id="f29f9-132">Als de waarde is ingesteld op **True**, worden de carrouselflipper en reeksindicator verborgen.</span><span class="sxs-lookup"><span data-stu-id="f29f9-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="f29f9-133">Sluiten van carrousel toestaan</span><span class="sxs-lookup"><span data-stu-id="f29f9-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="f29f9-134">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="f29f9-134">**True** or **False**</span></span> | <span data-ttu-id="f29f9-135">Als de waarde is ingesteld op **True**, kunnen gebruikers de carrousel sluiten.</span><span class="sxs-lookup"><span data-stu-id="f29f9-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="f29f9-136">Een carrouselmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="f29f9-136">Add a carousel module to a page</span></span>

<span data-ttu-id="f29f9-137">Voer de volgende stappen uit om een carrouselmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="f29f9-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f29f9-138">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="f29f9-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f29f9-139">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Carrouselsjabloon** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f29f9-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f29f9-140">Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.</span><span class="sxs-lookup"><span data-stu-id="f29f9-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="f29f9-141">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="f29f9-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="f29f9-142">Gebruik de carrouselsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Carrouselpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="f29f9-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="f29f9-143">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="f29f9-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="f29f9-144">Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Scherm vullen**.</span><span class="sxs-lookup"><span data-stu-id="f29f9-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="f29f9-145">Voeg onder **Paginaoverzicht** een carrouselmodule aan de containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="f29f9-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="f29f9-146">Voeg aan de carrouselmodule een inhoudsblokmodule toe.</span><span class="sxs-lookup"><span data-stu-id="f29f9-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="f29f9-147">Stel de eigenschappen van de inhoudsblokmodule in door **Koptekst**, **Koppeling**, **Indeling** en andere eigenschappen op te geven.</span><span class="sxs-lookup"><span data-stu-id="f29f9-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="f29f9-148">U kunt nog een inhoudsblokmodule toevoegen en configureren.</span><span class="sxs-lookup"><span data-stu-id="f29f9-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="f29f9-149">Stel zo nodig aanvullende eigenschappen in voor de carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="f29f9-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="f29f9-150">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="f29f9-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f29f9-151">Op de pagina ziet u een carrousel met twee modules (een heldmodule en een functiemodule).</span><span class="sxs-lookup"><span data-stu-id="f29f9-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="f29f9-152">U kunt aanvullende eigenschappen voor de modules carrousel, held en functie wijzigen om het gewenste effect te bereiken.</span><span class="sxs-lookup"><span data-stu-id="f29f9-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="f29f9-153">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="f29f9-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f29f9-154">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="f29f9-154">Additional resources</span></span>

[<span data-ttu-id="f29f9-155">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="f29f9-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f29f9-156">Promotiebanner-module</span><span class="sxs-lookup"><span data-stu-id="f29f9-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f29f9-157">Text Block-module</span><span class="sxs-lookup"><span data-stu-id="f29f9-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f29f9-158">Inhoudsblokkenmodule</span><span class="sxs-lookup"><span data-stu-id="f29f9-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f29f9-159">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="f29f9-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]