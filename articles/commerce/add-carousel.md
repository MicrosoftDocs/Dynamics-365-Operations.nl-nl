---
title: Carrouselmodule
description: In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785232"
---
# <a name="carousel-module"></a><span data-ttu-id="c1f42-103">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="c1f42-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c1f42-104">In dit onderwerp worden carrouselmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c1f42-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c1f42-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="c1f42-105">Overview</span></span>

<span data-ttu-id="c1f42-106">Een carrouselmodule wordt gebruikt voor het plaatsen van meerdere promotiepunten in een carrousel waarin klanten kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="c1f42-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="c1f42-107">Het is een speciale containermodule waarin andere modules worden gehost.</span><span class="sxs-lookup"><span data-stu-id="c1f42-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="c1f42-108">Een detailhandelaar kan bijvoorbeeld een carrouselmodule op een startpagina gebruiken om meerdere nieuwe producten of promoties te presenteren.</span><span class="sxs-lookup"><span data-stu-id="c1f42-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="c1f42-109">U kunt held- en functiemodules toevoegen binnen een carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="c1f42-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="c1f42-110">De eigenschappen van de carrouselmodule bepalen vervolgens hoe deze modules worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c1f42-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="c1f42-111">Voorbeelden van carrouselmodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="c1f42-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="c1f42-112">Een carrousel met meerdere promotiemodules kan worden gebruikt op een startpagina.</span><span class="sxs-lookup"><span data-stu-id="c1f42-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="c1f42-113">Een carrousel met meerdere promotiemodules kan worden gebruikt op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="c1f42-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="c1f42-114">Een carrousel kan op elke marketingpagina worden gebruikt om meerdere promoties of producten te promoten.</span><span class="sxs-lookup"><span data-stu-id="c1f42-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="c1f42-115">Eigenschappen van carrouselmodules</span><span class="sxs-lookup"><span data-stu-id="c1f42-115">Carousel module properties</span></span>

| <span data-ttu-id="c1f42-116">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="c1f42-116">Property name</span></span>             | <span data-ttu-id="c1f42-117">Waarde</span><span class="sxs-lookup"><span data-stu-id="c1f42-117">Value</span></span>                                | <span data-ttu-id="c1f42-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c1f42-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="c1f42-119">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="c1f42-119">Autoplay</span></span>                  | <span data-ttu-id="c1f42-120">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="c1f42-120">**True** or **False**</span></span>                | <span data-ttu-id="c1f42-121">Als de waarde is ingesteld op **True**, vindt de overgang tussen items binnen de carrousel automatisch plaats.</span><span class="sxs-lookup"><span data-stu-id="c1f42-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="c1f42-122">Als de waarde is ingesteld op **False**, vindt er geen overgang plaats tenzij de klant het toetsenbord of de muis gebruikt om van het ene naar het volgende item te gaan.</span><span class="sxs-lookup"><span data-stu-id="c1f42-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="c1f42-123">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="c1f42-123">Slide transition interval</span></span> | <span data-ttu-id="c1f42-124">Een waarde in seconden</span><span class="sxs-lookup"><span data-stu-id="c1f42-124">A value in seconds</span></span>                   | <span data-ttu-id="c1f42-125">Het interval voor overgangen tussen items.</span><span class="sxs-lookup"><span data-stu-id="c1f42-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="c1f42-126">Overgangsanimatie</span><span class="sxs-lookup"><span data-stu-id="c1f42-126">Transition animation</span></span>      | <span data-ttu-id="c1f42-127">**Verschuiven** of **Vervagen**</span><span class="sxs-lookup"><span data-stu-id="c1f42-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="c1f42-128">Het overgangseffect.</span><span class="sxs-lookup"><span data-stu-id="c1f42-128">The transition effect.</span></span> |
| <span data-ttu-id="c1f42-129">Breedte</span><span class="sxs-lookup"><span data-stu-id="c1f42-129">Width</span></span>                     | <span data-ttu-id="c1f42-130">**Passen in container** of **Scherm vullen**</span><span class="sxs-lookup"><span data-stu-id="c1f42-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="c1f42-131">Als de waarde wordt ingesteld op **Passen in container**, zijn de items in de carrousel beperkt tot de breedte van de carrousel.</span><span class="sxs-lookup"><span data-stu-id="c1f42-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="c1f42-132">Als de waarde is ingesteld op **Scherm vullen**, zijn de items niet beperkt tot de breedte van de carrousel voor de plaatsing van inhoud, maar gebruiken ze de modus Volledig scherm.</span><span class="sxs-lookup"><span data-stu-id="c1f42-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="c1f42-133">U kunt de waarde wijzigen om de gewenste indeling te bereiken.</span><span class="sxs-lookup"><span data-stu-id="c1f42-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="c1f42-134">Een carrouselmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="c1f42-134">Add a carousel module to a page</span></span>

<span data-ttu-id="c1f42-135">Voer de volgende stappen uit om een carrouselmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="c1f42-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c1f42-136">Maak een paginasjabloon met de naam **Carrouselsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="c1f42-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="c1f42-137">Voeg in het **hoofdvak** van de standaardpagina een carrouselmodule toe.</span><span class="sxs-lookup"><span data-stu-id="c1f42-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="c1f42-138">Voeg een heldmodule toe aan de carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="c1f42-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="c1f42-139">Voeg een functiemodule toe aan de carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="c1f42-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="c1f42-140">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="c1f42-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="c1f42-141">Gebruik de carrouselsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Carrouselpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="c1f42-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="c1f42-142">Voeg in het **hoofdvak** van de nieuwe pagina een carrouselmodule toe.</span><span class="sxs-lookup"><span data-stu-id="c1f42-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="c1f42-143">Stel de eigenschap **Breedte** van de carrouselmodule in op **Scherm vullen**.</span><span class="sxs-lookup"><span data-stu-id="c1f42-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="c1f42-144">Stel de eigenschap **Overgangsanimatie** in op **Verschuiven**.</span><span class="sxs-lookup"><span data-stu-id="c1f42-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="c1f42-145">Voeg een heldmodule toe aan de carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="c1f42-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="c1f42-146">Voeg in de heldmodule een afbeelding en een koptekst toe en selecteer vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c1f42-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="c1f42-147">Voeg een functiemodule toe aan de carrouselmodule.</span><span class="sxs-lookup"><span data-stu-id="c1f42-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="c1f42-148">Voeg in de functiemodule een afbeelding, een kop en een alineatekst toe.</span><span class="sxs-lookup"><span data-stu-id="c1f42-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="c1f42-149">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="c1f42-149">Save and preview the page.</span></span> <span data-ttu-id="c1f42-150">Op de pagina ziet u een carrousel met twee modules (een heldmodule en een functiemodule).</span><span class="sxs-lookup"><span data-stu-id="c1f42-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="c1f42-151">U kunt aanvullende eigenschappen voor de modules carrousel, held en functie wijzigen om het gewenste effect te bereiken.</span><span class="sxs-lookup"><span data-stu-id="c1f42-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="c1f42-152">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="c1f42-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1f42-153">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c1f42-153">Additional resources</span></span>

[<span data-ttu-id="c1f42-154">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="c1f42-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c1f42-155">Waarschuwingsmodule</span><span class="sxs-lookup"><span data-stu-id="c1f42-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="c1f42-156">Inhoudsrijke-blokmodule</span><span class="sxs-lookup"><span data-stu-id="c1f42-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="c1f42-157">Module voor het plaatsen van inhoud</span><span class="sxs-lookup"><span data-stu-id="c1f42-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="c1f42-158">Functiemodule</span><span class="sxs-lookup"><span data-stu-id="c1f42-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="c1f42-159">Heldmodule</span><span class="sxs-lookup"><span data-stu-id="c1f42-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="c1f42-160">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="c1f42-160">Video player module</span></span>](add-video-player.md)
