---
title: Module voor het plaatsen van inhoud
description: In dit onderwerp worden modules voor het plaatsen van inhoud of inhoudsitems beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785295"
---
# <a name="content-placement-module"></a><span data-ttu-id="fcfe0-103">Module voor het plaatsen van inhoud</span><span class="sxs-lookup"><span data-stu-id="fcfe0-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fcfe0-104">In dit onderwerp worden modules voor het plaatsen van inhoud of inhoudsitems beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fcfe0-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="fcfe0-105">Overview</span></span>

<span data-ttu-id="fcfe0-106">Een module voor het plaatsen van inhoud is een speciale container waarin andere modules in een specifieke indeling kunnen worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="fcfe0-107">Modules voor plaatsing van inhoud ondersteunen de volgende typen modules als onderliggende modules: item voor inhoudplaatsing, welkomstitem voor account, item voor accountorders, item voor verlanglijst van account en items voor accountprofiel.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="fcfe0-108">Met modules voor plaatsing van inhoud worden gegevens afgeleid uit de onderliggende modules die ze ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="fcfe0-109">Daarom kunnen modules voor het plaatsen van inhoud op verschillende manieren worden gebruikt, afhankelijk van de modules die eraan zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="fcfe0-110">Voor de modules voor het plaatsen van inhoud worden zowel afbeeldingen als tekst gebruikt om acties, beleid en productfuncties te presenteren.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="fcfe0-111">U kunt bijvoorbeeld een module voor het plaatsen van inhoud op een startpagina gebruiken om winkelbeleid of verzendgegevens weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="fcfe0-112">Modules voor het plaatsen van inhoud worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="fcfe0-113">Ze kunnen echter alleen worden gebruikt binnen een module voor de plaatsing van inhoud.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="fcfe0-114">Voorbeelden van modules voor het plaatsen van inhoud in e-commerce</span><span class="sxs-lookup"><span data-stu-id="fcfe0-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="fcfe0-115">Modules voor het plaatsen van specifieke inhouditems kunnen op een startpagina of marketingpagina's worden gebruikt om productfuncties, promoties, winkelinformatie en andere informatie te presenteren via afbeeldingen en tekst.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="fcfe0-116">Modules voor het plaatsen van inhoudsitems kunnen op de pagina's met productgegevens worden gebruikt om productfuncties te presenteren.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="fcfe0-117">Modules voor plaatsing van inhoud met een welkomstitem of orders voor het account kunnen worden gebruikt op accountbeheerpagina's.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="fcfe0-118">Eigenschappen van modules voor het plaatsen van inhoud</span><span class="sxs-lookup"><span data-stu-id="fcfe0-118">Content placement module properties</span></span>

| <span data-ttu-id="fcfe0-119">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-119">Property name</span></span> | <span data-ttu-id="fcfe0-120">Waarde</span><span class="sxs-lookup"><span data-stu-id="fcfe0-120">Value</span></span> | <span data-ttu-id="fcfe0-121">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="fcfe0-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="fcfe0-122">Breedte</span><span class="sxs-lookup"><span data-stu-id="fcfe0-122">Width</span></span>         | <span data-ttu-id="fcfe0-123">**Passen in container** of **Scherm vullen**</span><span class="sxs-lookup"><span data-stu-id="fcfe0-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="fcfe0-124">Als de waarde op **Passen in container** wordt ingesteld, worden de items binnen de module voor het plaatsen van inhoud beperkt tot de breedte van de module.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="fcfe0-125">Als de waarde is ingesteld op **Scherm vullen**, zijn de items niet beperkt tot de breedte van de module voor de plaatsing van inhoud, maar gebruiken ze de modus Volledig scherm.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="fcfe0-126">Eigenschappen van modules voor het plaatsen van inhoudsitems</span><span class="sxs-lookup"><span data-stu-id="fcfe0-126">Content placement item module properties</span></span>

| <span data-ttu-id="fcfe0-127">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-127">Property name</span></span> | <span data-ttu-id="fcfe0-128">Waarde</span><span class="sxs-lookup"><span data-stu-id="fcfe0-128">Value</span></span> | <span data-ttu-id="fcfe0-129">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="fcfe0-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="fcfe0-130">Koptekst</span><span class="sxs-lookup"><span data-stu-id="fcfe0-130">Heading</span></span>       | <span data-ttu-id="fcfe0-131">Koptekst en tags voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="fcfe0-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="fcfe0-132">Elke module voor plaatsing van inhoudsitems kan een koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="fcfe0-133">De eigenschap **Koptekst** ondersteunt labels voor kopteksten.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="fcfe0-134">Standaard wordt het koptekstlabel **H2** gebruikt, maar dit kan desgewenst worden gewijzigd voor toegankelijkheidsvereisten.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="fcfe0-135">Alinea</span><span class="sxs-lookup"><span data-stu-id="fcfe0-135">Paragraph</span></span>     | <span data-ttu-id="fcfe0-136">Alineatekst</span><span class="sxs-lookup"><span data-stu-id="fcfe0-136">Paragraph text</span></span> | <span data-ttu-id="fcfe0-137">Modules voor het plaatsen inhoudsitems ondersteunen alineatekst in RTF-indeling.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="fcfe0-138">Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst en hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="fcfe0-139">Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="fcfe0-140">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="fcfe0-140">Image</span></span>         | <span data-ttu-id="fcfe0-141">Afbeeldingbestand</span><span class="sxs-lookup"><span data-stu-id="fcfe0-141">Image file</span></span> | <span data-ttu-id="fcfe0-142">Er kan een afbeelding aan de tekst worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="fcfe0-143">Koppeling</span><span class="sxs-lookup"><span data-stu-id="fcfe0-143">Link</span></span>          | <span data-ttu-id="fcfe0-144">URL van koppeling en koppelingstekst</span><span class="sxs-lookup"><span data-stu-id="fcfe0-144">Link URL and link text</span></span> | <span data-ttu-id="fcfe0-145">U kunt een koppeling toevoegen aan de tekst om gebruikers om te leiden naar een specifieke pagina.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="fcfe0-146">Tegelgrootte</span><span class="sxs-lookup"><span data-stu-id="fcfe0-146">Tile size</span></span>     | <span data-ttu-id="fcfe0-147">Een getal tussen **1** en **12**</span><span class="sxs-lookup"><span data-stu-id="fcfe0-147">A number from **1** through **12**</span></span> | <span data-ttu-id="fcfe0-148">Voor elk item voor inhoudsplaatsing wordt met deze eigenschap het aantal vakken gedefinieerd dat de inhoud van het item moet invullen.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="fcfe0-149">De maximum grootte van de module voor het plaatsen van inhoud is 12 vakken.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="fcfe0-150">Als de totale grootte van de tegel voor de eerste *n* items in de module voor inhoudplaatsing meer dan 12 vakken bevat, worden de items verplaatst naar de volgende rij.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="fcfe0-151">Een module voor het plaatsen van inhoud met inhoudsitems toevoegen op een pagina</span><span class="sxs-lookup"><span data-stu-id="fcfe0-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="fcfe0-152">Voer de volgende stappen uit om een module voor het plaatsen van inhoud met inhoudsitems toe te voegen aan een nieuwe pagina en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fcfe0-153">Maak een paginasjabloon met de naam **sjabloon voor het plaatsen van inhoud**.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="fcfe0-154">Voeg in het **hoofdvak** van de standaardpagina een module voor het plaatsen van inhoud toe.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="fcfe0-155">Voeg in de module voor het plaatsen van inhoud een module toe voor inhoudsitems.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="fcfe0-156">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="fcfe0-157">Gebruik de sjabloon voor het plaatsen van inhoud die u zojuist hebt gemaakt om een pagina met de naam **Pagina voor het plaatsen van inhoud** te maken.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="fcfe0-158">Voeg in het **hoofdvak** van de nieuwe pagina een module voor het plaatsen van inhoud toe.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="fcfe0-159">Voeg in de module voor het plaatsen van inhoud een module toe voor inhoudsitems.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="fcfe0-160">Selecteer een afbeelding in het eigenschappenvenster voor de module voor plaatsing van inhoudsitems. Voeg vervolgens een kop, een alinea en een koppeling toe, stel de URL van de koppeling in en stel de grootte van de tegel in op **6**.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="fcfe0-161">Herhaal stap 7 en 8 om nog een module voor plaatsing van inhoudsitems met dezelfde tegelgrootte toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="fcfe0-162">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-162">Save and preview the page.</span></span> <span data-ttu-id="fcfe0-163">U ziet nu twee inhoudplaatsingitems die naast elkaar worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="fcfe0-164">U kunt de eigenschap voor de **Tegelgrootte** van elke module voor de plaatsing van inhoudsitems aanpassen of meer modules toevoegen om de gewenste indeling te bereiken.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="fcfe0-165">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="fcfe0-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcfe0-166">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="fcfe0-166">Additional resources</span></span>

[<span data-ttu-id="fcfe0-167">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="fcfe0-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fcfe0-168">Waarschuwingsmodule</span><span class="sxs-lookup"><span data-stu-id="fcfe0-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="fcfe0-169">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="fcfe0-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="fcfe0-170">Inhoudsrijke-blokmodule</span><span class="sxs-lookup"><span data-stu-id="fcfe0-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="fcfe0-171">Functiemodule</span><span class="sxs-lookup"><span data-stu-id="fcfe0-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="fcfe0-172">Heldmodule</span><span class="sxs-lookup"><span data-stu-id="fcfe0-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="fcfe0-173">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="fcfe0-173">Video player module</span></span>](add-video-player.md)