---
title: Inhoudsrijke-blokmodule
description: In dit onderwerp wordt beschreven wat inhoudsrijke-blokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785416"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="143d3-103">Inhoudsrijke-blokmodule</span><span class="sxs-lookup"><span data-stu-id="143d3-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="143d3-104">In dit onderwerp wordt beschreven wat inhoudsrijke-blokmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="143d3-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="143d3-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="143d3-105">Overview</span></span>

<span data-ttu-id="143d3-106">Een inhoudsrijke-blokmodule is een speciale container waarin een of meer inhoudsrijke-blokitems kunnen worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="143d3-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="143d3-107">Inhoudsrijke-blokmodules worden gebruikt voor tekstinhoud op een pagina.</span><span class="sxs-lookup"><span data-stu-id="143d3-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="143d3-108">Deze inhoud kan informatief of promotioneel zijn.</span><span class="sxs-lookup"><span data-stu-id="143d3-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="143d3-109">Inhoudsrijke-blokmodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="143d3-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="143d3-110">Ze zijn zelfstandige modules die niet afhankelijk is van andere paginacontext of andere modules.</span><span class="sxs-lookup"><span data-stu-id="143d3-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="143d3-111">Voorbeelden van inhoudsrijke-blokmodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="143d3-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="143d3-112">Inhoudsrijke-blokmodules kunnen op de volgende manieren worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="143d3-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="143d3-113">Voor het presenteren van productfuncties op een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="143d3-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="143d3-114">Voor informatieve doeleinden op elke willekeurige pagina.</span><span class="sxs-lookup"><span data-stu-id="143d3-114">For informational purposes on any page.</span></span> <span data-ttu-id="143d3-115">Ze kunnen bijvoorbeeld de voordelen van loyaliteitsprogramma's toelichten, verzend- en retourbeleid beschrijven, veelgestelde vragen beantwoorden of informatie over het bedrijf invullen.</span><span class="sxs-lookup"><span data-stu-id="143d3-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="143d3-116">Aangepaste berichten toevoegen aan een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="143d3-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="143d3-117">(bijvoorbeeld "gratis verzending voor bestellingen boven $50").</span><span class="sxs-lookup"><span data-stu-id="143d3-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="143d3-118">Voor disclaimers en contactgegevens op pagina's met productdetails, winkelwagens, kassa en andere pagina's (bijvoorbeeld "verzending en retouren vallen onder het winkelbeleid").</span><span class="sxs-lookup"><span data-stu-id="143d3-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="143d3-119">Eigenschappen van inhoudsrijke-blokmodules</span><span class="sxs-lookup"><span data-stu-id="143d3-119">Content rich block module properties</span></span>

| <span data-ttu-id="143d3-120">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="143d3-120">Property name</span></span>     | <span data-ttu-id="143d3-121">Waarde</span><span class="sxs-lookup"><span data-stu-id="143d3-121">Value</span></span>                                 | <span data-ttu-id="143d3-122">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="143d3-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="143d3-123">Aantal kolommen</span><span class="sxs-lookup"><span data-stu-id="143d3-123">Number of columns</span></span> | <span data-ttu-id="143d3-124">Een getal tussen **1** en **4**</span><span class="sxs-lookup"><span data-stu-id="143d3-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="143d3-125">Het aantal kolommen in het Inhoudsrijke blok.</span><span class="sxs-lookup"><span data-stu-id="143d3-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="143d3-126">Er kunnen maximaal vier kolommen zijn.</span><span class="sxs-lookup"><span data-stu-id="143d3-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="143d3-127">Breedte</span><span class="sxs-lookup"><span data-stu-id="143d3-127">Width</span></span>             | <span data-ttu-id="143d3-128">**Passen in container** of **Scherm vullen**</span><span class="sxs-lookup"><span data-stu-id="143d3-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="143d3-129">Als de waarde wordt ingesteld op **Passen in container**, zijn de items in de container beperkt tot de breedte van de container.</span><span class="sxs-lookup"><span data-stu-id="143d3-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="143d3-130">Als de waarde is ingesteld op **Scherm vullen**, zijn de items niet beperkt tot de breedte van de container voor de plaatsing van inhoud, maar gebruiken ze de modus Volledig scherm.</span><span class="sxs-lookup"><span data-stu-id="143d3-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="143d3-131">U kunt de waarde wijzigen om de gewenste indeling te bereiken.</span><span class="sxs-lookup"><span data-stu-id="143d3-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="143d3-132">Eigenschappen van modules met inhoudsrijke blokitems</span><span class="sxs-lookup"><span data-stu-id="143d3-132">Content rich block item module properties</span></span>

| <span data-ttu-id="143d3-133">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="143d3-133">Property name</span></span> | <span data-ttu-id="143d3-134">Waarde</span><span class="sxs-lookup"><span data-stu-id="143d3-134">Value</span></span>          | <span data-ttu-id="143d3-135">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="143d3-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="143d3-136">Alinea</span><span class="sxs-lookup"><span data-stu-id="143d3-136">Paragraph</span></span>     | <span data-ttu-id="143d3-137">Alineatekst</span><span class="sxs-lookup"><span data-stu-id="143d3-137">Paragraph text</span></span> | <span data-ttu-id="143d3-138">De tekst die bij elk item in het inhoudsrijke blok wordt getoond.</span><span class="sxs-lookup"><span data-stu-id="143d3-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="143d3-139">Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst.</span><span class="sxs-lookup"><span data-stu-id="143d3-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="143d3-140">Een inhoudsrijke-blokmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="143d3-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="143d3-141">Voer de volgende stappen uit om een inhoudsrijke-blokmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="143d3-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="143d3-142">Maak een paginasjabloon met de naam **Inhoudsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="143d3-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="143d3-143">Voeg in het **hoofdvak** van de standaardpagina een inhoudsrijke-blokmodule toe.</span><span class="sxs-lookup"><span data-stu-id="143d3-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="143d3-144">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="143d3-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="143d3-145">Gebruik de inhoudsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Inhoudpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="143d3-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="143d3-146">Voeg in het **hoofdvak** van de nieuwe pagina een inhoudsrijke-blokmodule toe.</span><span class="sxs-lookup"><span data-stu-id="143d3-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="143d3-147">Stel in de eigenschappen van de inhoudsrijke-blokmodule het aantal kolommen in op **2**.</span><span class="sxs-lookup"><span data-stu-id="143d3-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="143d3-148">Selecteer in de inhoudsrijke-blokmodule de optie **Een module toevoegen** en voeg een inhoudsrijk blokitem (bijvoorbeeld **Item1**) toe.</span><span class="sxs-lookup"><span data-stu-id="143d3-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="143d3-149">Voeg in het nieuwe inhoudsrijke blokitem een alineatekst toe.</span><span class="sxs-lookup"><span data-stu-id="143d3-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="143d3-150">Selecteer in de inhoudsrijke-blokmodule de optie **Een module toevoegen** en voeg een inhoudsrijk blokitem (bijvoorbeeld **Item2**) toe.</span><span class="sxs-lookup"><span data-stu-id="143d3-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="143d3-151">Voeg in het nieuwe inhoudsrijke blokitem een alineatekst toe.</span><span class="sxs-lookup"><span data-stu-id="143d3-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="143d3-152">Sla de pagina op en bekijk de wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="143d3-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="143d3-153">In een weergave met twee kolommen ziet u twee inhoudsrijke blokken.</span><span class="sxs-lookup"><span data-stu-id="143d3-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="143d3-154">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="143d3-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="143d3-155">Als u een derde inhoudsrijk blokitem toevoegt, wordt deze onder de twee items geplaatst die u eerder hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="143d3-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="143d3-156">Door het aantal kolommen en items in de container te wijzigen, kunt u verschillende indelingen voor tekstinhoud bereiken.</span><span class="sxs-lookup"><span data-stu-id="143d3-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="143d3-157">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="143d3-157">Additional resources</span></span>

[<span data-ttu-id="143d3-158">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="143d3-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="143d3-159">Waarschuwingsmodule</span><span class="sxs-lookup"><span data-stu-id="143d3-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="143d3-160">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="143d3-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="143d3-161">Module voor het plaatsen van inhoud</span><span class="sxs-lookup"><span data-stu-id="143d3-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="143d3-162">Functiemodule</span><span class="sxs-lookup"><span data-stu-id="143d3-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="143d3-163">Heldmodule</span><span class="sxs-lookup"><span data-stu-id="143d3-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="143d3-164">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="143d3-164">Video player module</span></span>](add-video-player.md)

