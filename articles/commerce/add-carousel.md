---
title: Carrouselmodule
description: In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269723"
---
# <a name="carousel-module"></a><span data-ttu-id="35cc1-103">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="35cc1-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="35cc1-104">In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="35cc1-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="35cc1-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="35cc1-105">Overview</span></span>

<span data-ttu-id="35cc1-106">Een carrouselmodule wordt gebruikt voor het plaatsen van meerdere promotieartikelen (met afbeeldingen) in een draaiende carrouselbanner waar klanten doorheen kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="35cc1-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="35cc1-107">Een detailhandelaar kan bijvoorbeeld een carrouselmodule op een startpagina gebruiken om meerdere nieuwe producten of promoties te presenteren.</span><span class="sxs-lookup"><span data-stu-id="35cc1-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="35cc1-108">U kunt inhoudsblokmodules in een carrouselmodule toevoegen.</span><span class="sxs-lookup"><span data-stu-id="35cc1-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="35cc1-109">De eigenschappen van de carrouselmodule bepalen vervolgens hoe deze modules worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="35cc1-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="35cc1-110">Voorbeelden van carrouselmodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="35cc1-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="35cc1-111">Een carrousel met meerdere promotiemodules kan worden gebruikt op een startpagina.</span><span class="sxs-lookup"><span data-stu-id="35cc1-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="35cc1-112">Een carrousel met meerdere promotiemodules kan worden gebruikt op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="35cc1-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="35cc1-113">Een carrousel kan op elke marketingpagina worden gebruikt om meerdere promoties of producten te promoten.</span><span class="sxs-lookup"><span data-stu-id="35cc1-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="35cc1-114">Eigenschappen van carrouselmodules</span><span class="sxs-lookup"><span data-stu-id="35cc1-114">Carousel module properties</span></span>

| <span data-ttu-id="35cc1-115">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="35cc1-115">Property name</span></span>             | <span data-ttu-id="35cc1-116">Waarde</span><span class="sxs-lookup"><span data-stu-id="35cc1-116">Value</span></span>                 | <span data-ttu-id="35cc1-117">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="35cc1-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="35cc1-118">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="35cc1-118">Autoplay</span></span>                  | <span data-ttu-id="35cc1-119">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="35cc1-119">**True** or **False**</span></span> | <span data-ttu-id="35cc1-120">Als de waarde is ingesteld op **True**, vindt de overgang tussen items binnen de carrousel automatisch plaats.</span><span class="sxs-lookup"><span data-stu-id="35cc1-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="35cc1-121">Als de waarde is ingesteld op **False**, vindt er geen overgang plaats tenzij de klant het toetsenbord of de muis gebruikt om van het ene naar het volgende item te gaan.</span><span class="sxs-lookup"><span data-stu-id="35cc1-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="35cc1-122">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="35cc1-122">Slide transition interval</span></span> | <span data-ttu-id="35cc1-123">Een waarde in seconden</span><span class="sxs-lookup"><span data-stu-id="35cc1-123">A value in seconds</span></span>    | <span data-ttu-id="35cc1-124">Het interval voor overgangen tussen items.</span><span class="sxs-lookup"><span data-stu-id="35cc1-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="35cc1-125">Overgangstype</span><span class="sxs-lookup"><span data-stu-id="35cc1-125">Transition type</span></span>           | <span data-ttu-id="35cc1-126">**Verschuiven** of **Vervagen**</span><span class="sxs-lookup"><span data-stu-id="35cc1-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="35cc1-127">Het overgangseffect tussen artikelen.</span><span class="sxs-lookup"><span data-stu-id="35cc1-127">The transition effect between items.</span></span> |
| <span data-ttu-id="35cc1-128">Carrouselflipper verbergen</span><span class="sxs-lookup"><span data-stu-id="35cc1-128">Hide carousel flipper</span></span>     | <span data-ttu-id="35cc1-129">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="35cc1-129">**True** or **False**</span></span> | <span data-ttu-id="35cc1-130">Als de waarde is ingesteld op **True**, worden de carrouselflipper en reeksindicator verborgen.</span><span class="sxs-lookup"><span data-stu-id="35cc1-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="35cc1-131">Sluiten van carrousel toestaan</span><span class="sxs-lookup"><span data-stu-id="35cc1-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="35cc1-132">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="35cc1-132">**True** or **False**</span></span> | <span data-ttu-id="35cc1-133">Als de waarde is ingesteld op **True**, kunnen gebruikers de carrousel sluiten.</span><span class="sxs-lookup"><span data-stu-id="35cc1-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="35cc1-134">Een carrouselmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="35cc1-134">Add a carousel module to a page</span></span>

<span data-ttu-id="35cc1-135">Voer de volgende stappen uit om een carrouselmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="35cc1-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="35cc1-136">Selecteer **Nieuw** om een paginasjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="35cc1-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="35cc1-137">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Carrouselsjabloon** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="35cc1-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="35cc1-138">Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.</span><span class="sxs-lookup"><span data-stu-id="35cc1-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="35cc1-139">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="35cc1-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="35cc1-140">Gebruik de carrouselsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Carrouselpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="35cc1-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="35cc1-141">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="35cc1-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="35cc1-142">Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Scherm vullen**.</span><span class="sxs-lookup"><span data-stu-id="35cc1-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="35cc1-143">Voeg onder **Paginaoverzicht** een carrouselmodule aan de containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="35cc1-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="35cc1-144">Voeg aan de carrouselmodule een inhoudsblokmodule toe.</span><span class="sxs-lookup"><span data-stu-id="35cc1-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="35cc1-145">Stel de eigenschappen van de inhoudsblokmodule in door **Koptekst**, **Koppeling**, **Indeling** en andere eigenschappen op te geven.</span><span class="sxs-lookup"><span data-stu-id="35cc1-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="35cc1-146">U kunt nog een inhoudsblokmodule toevoegen en configureren.</span><span class="sxs-lookup"><span data-stu-id="35cc1-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="35cc1-147">Stel zo nodig aanvullende eigenschappen in voor de carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="35cc1-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="35cc1-148">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="35cc1-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="35cc1-149">Op de pagina ziet u een carrousel met twee modules (een heldmodule en een functiemodule).</span><span class="sxs-lookup"><span data-stu-id="35cc1-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="35cc1-150">U kunt aanvullende eigenschappen voor de modules carrousel, held en functie wijzigen om het gewenste effect te bereiken.</span><span class="sxs-lookup"><span data-stu-id="35cc1-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="35cc1-151">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="35cc1-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35cc1-152">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="35cc1-152">Additional resources</span></span>

[<span data-ttu-id="35cc1-153">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="35cc1-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="35cc1-154">Promotiebanner-module</span><span class="sxs-lookup"><span data-stu-id="35cc1-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="35cc1-155">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="35cc1-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="35cc1-156">Inhoudsblokmodule</span><span class="sxs-lookup"><span data-stu-id="35cc1-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="35cc1-157">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="35cc1-157">Video player module</span></span>](add-video-player.md)
