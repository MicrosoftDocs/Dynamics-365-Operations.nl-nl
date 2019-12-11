---
title: Functiemodule
description: In dit onderwerp worden modules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785278"
---
# <a name="feature-module"></a><span data-ttu-id="561d8-103">Functiemodule</span><span class="sxs-lookup"><span data-stu-id="561d8-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="561d8-104">In dit onderwerp worden modules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="561d8-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="561d8-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="561d8-105">Overview</span></span>

<span data-ttu-id="561d8-106">Een functiemodule wordt gebruikt voor de marketing van producten of promoties via een combinatie van afbeeldingen en tekst.</span><span class="sxs-lookup"><span data-stu-id="561d8-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="561d8-107">Een detailhandelaar kan bijvoorbeeld een functiemodule aan een pagina met productgegevens toevoegen om de functies van het product te markeren.</span><span class="sxs-lookup"><span data-stu-id="561d8-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="561d8-108">Een functiemodule wordt gestuurd door gegevens uit het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="561d8-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="561d8-109">Het is een zelfstandige module die niet afhankelijk is van andere modules op de pagina.</span><span class="sxs-lookup"><span data-stu-id="561d8-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="561d8-110">Een functiemodule kan op elke sitepagina worden geplaatst waar een detailhandelaar iets wil verhandelen of promoten (bijvoorbeeld producten, verkoop of functies).</span><span class="sxs-lookup"><span data-stu-id="561d8-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="561d8-111">Voorbeelden van functiemodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="561d8-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="561d8-112">Een functiemodule kan op de volgende pagina's worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="561d8-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="561d8-113">Een pagina met productgegevens om productfuncties te presenteren</span><span class="sxs-lookup"><span data-stu-id="561d8-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="561d8-114">De startpagina om producten te promoten</span><span class="sxs-lookup"><span data-stu-id="561d8-114">The home page, to promote products</span></span>
- <span data-ttu-id="561d8-115">Een categoriepagina om een categorie met producten te markeren</span><span class="sxs-lookup"><span data-stu-id="561d8-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="561d8-116">Eigenschappen van functiemodule</span><span class="sxs-lookup"><span data-stu-id="561d8-116">Feature module properties</span></span>

| <span data-ttu-id="561d8-117">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="561d8-117">Property name</span></span>     | <span data-ttu-id="561d8-118">Waarden</span><span class="sxs-lookup"><span data-stu-id="561d8-118">Values</span></span> | <span data-ttu-id="561d8-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="561d8-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="561d8-120">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="561d8-120">Image</span></span>             | <span data-ttu-id="561d8-121">Afbeeldingbestand</span><span class="sxs-lookup"><span data-stu-id="561d8-121">Image file</span></span> | <span data-ttu-id="561d8-122">Een afbeelding kan worden gebruikt voor marketing van het product of de promotie.</span><span class="sxs-lookup"><span data-stu-id="561d8-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="561d8-123">Een afbeelding kan naar de afbeeldingengalerie worden geüpload, of er kan een bestaande afbeelding worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="561d8-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="561d8-124">Koptekst</span><span class="sxs-lookup"><span data-stu-id="561d8-124">Heading</span></span>           | <span data-ttu-id="561d8-125">Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="561d8-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="561d8-126">Elke functiemodule kan een koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="561d8-126">Every feature module can have a heading.</span></span> <span data-ttu-id="561d8-127">Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="561d8-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="561d8-128">De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="561d8-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="561d8-129">Alinea</span><span class="sxs-lookup"><span data-stu-id="561d8-129">Paragraph</span></span>         | <span data-ttu-id="561d8-130">Alineatekst</span><span class="sxs-lookup"><span data-stu-id="561d8-130">Paragraph text</span></span> | <span data-ttu-id="561d8-131">Functiemodules ondersteunen alineatekst in RTF-indeling.</span><span class="sxs-lookup"><span data-stu-id="561d8-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="561d8-132">Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst en hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="561d8-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="561d8-133">Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="561d8-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="561d8-134">Koppeling</span><span class="sxs-lookup"><span data-stu-id="561d8-134">Link</span></span>              | <span data-ttu-id="561d8-135">Koppelingstekst, koppelings-URL, het label Accessible Rich internet Applications (ARIA) en **Koppeling in nieuw tabblad openen**</span><span class="sxs-lookup"><span data-stu-id="561d8-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="561d8-136">Functiemodules ondersteunen een of meer koppelingen met oproep tot actie.</span><span class="sxs-lookup"><span data-stu-id="561d8-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="561d8-137">Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist.</span><span class="sxs-lookup"><span data-stu-id="561d8-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="561d8-138">ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="561d8-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="561d8-139">U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad.</span><span class="sxs-lookup"><span data-stu-id="561d8-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="561d8-140">Plaatsing van afbeelding</span><span class="sxs-lookup"><span data-stu-id="561d8-140">Image placement</span></span>   | <span data-ttu-id="561d8-141">**Rechts**, **Links**, **Boven** of **Onder**</span><span class="sxs-lookup"><span data-stu-id="561d8-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="561d8-142">Met deze eigenschap wordt de positie van de afbeelding ten opzichte van de tekst bepaald.</span><span class="sxs-lookup"><span data-stu-id="561d8-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="561d8-143">Als bijvoorbeeld **Rechts** is geselecteerd, wordt de afbeelding rechts van de tekst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="561d8-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="561d8-144">Grootte afbeeldingskolom</span><span class="sxs-lookup"><span data-stu-id="561d8-144">Image column size</span></span> | <span data-ttu-id="561d8-145">Een waarde tussen **1** en **12**</span><span class="sxs-lookup"><span data-stu-id="561d8-145">A value from **1** through **12**</span></span> | <span data-ttu-id="561d8-146">Met deze eigenschap wordt de grootte van de afbeelding ten opzichte van de tekst bepaald.</span><span class="sxs-lookup"><span data-stu-id="561d8-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="561d8-147">De grootte wordt uitgedrukt als een aantal kolommen op de pagina.</span><span class="sxs-lookup"><span data-stu-id="561d8-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="561d8-148">Een pagina bevat 12 kolommen.</span><span class="sxs-lookup"><span data-stu-id="561d8-148">There are 12 columns on a page.</span></span> <span data-ttu-id="561d8-149">De afbeelding en tekst hebben standaard dezelfde grootte (zes kolommen elk).</span><span class="sxs-lookup"><span data-stu-id="561d8-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="561d8-150">De grootte kan echter zo nodig worden aangepast.</span><span class="sxs-lookup"><span data-stu-id="561d8-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="561d8-151">Een functiemodule toevoegen aan een nieuwe pagina</span><span class="sxs-lookup"><span data-stu-id="561d8-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="561d8-152">Voer de volgende stappen uit om een functiemodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="561d8-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="561d8-153">Ga naar **Sjablonen** en maak een paginasjabloon met de naam **functiesjabloon**.</span><span class="sxs-lookup"><span data-stu-id="561d8-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="561d8-154">Voeg in het **hoofdvak** van de standaardpagina een functiemodule toe.</span><span class="sxs-lookup"><span data-stu-id="561d8-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="561d8-155">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="561d8-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="561d8-156">Gebruik de functiesjabloon die u zojuist hebt gemaakt om een pagina met de naam **functiepagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="561d8-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="561d8-157">Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="561d8-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="561d8-158">Selecteer in het dialoogvenster **Module toevoegen** onder **Modules selecteren** een functiemodule en selecteer vervolgens **OK.**</span><span class="sxs-lookup"><span data-stu-id="561d8-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="561d8-159">Selecteer in de overzichtsstructuur aan de linkerkant de functiemodule.</span><span class="sxs-lookup"><span data-stu-id="561d8-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="561d8-160">Selecteer **Een afbeelding toevoegen** in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="561d8-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="561d8-161">Selecteer vervolgens een bestaande afbeelding of upload een nieuwe afbeelding.</span><span class="sxs-lookup"><span data-stu-id="561d8-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="561d8-162">Selecteer **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="561d8-162">Select **Heading**.</span></span>
1. <span data-ttu-id="561d8-163">Voeg in het dialoogvenster **Koptekst** de koptekst toe, selecteer het kopniveau en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="561d8-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="561d8-164">Voeg onder **RTF-indeling** de gewenste tekst toe.</span><span class="sxs-lookup"><span data-stu-id="561d8-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="561d8-165">Selecteer **Actiekoppeling toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="561d8-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="561d8-166">Voeg in het dialoogvenster **Actiekoppeling** de koppelingstekst, een koppelings-URL en een ARIA-label voor de koppeling toe en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="561d8-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="561d8-167">Sla de pagina op en bekijk uw wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="561d8-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="561d8-168">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="561d8-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="561d8-169">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="561d8-169">Additional resources</span></span>

[<span data-ttu-id="561d8-170">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="561d8-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="561d8-171">Waarschuwingsmodule</span><span class="sxs-lookup"><span data-stu-id="561d8-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="561d8-172">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="561d8-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="561d8-173">Inhoudsrijke-blokmodule</span><span class="sxs-lookup"><span data-stu-id="561d8-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="561d8-174">Module voor het plaatsen van inhoud</span><span class="sxs-lookup"><span data-stu-id="561d8-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="561d8-175">Heldmodule</span><span class="sxs-lookup"><span data-stu-id="561d8-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="561d8-176">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="561d8-176">Video player module</span></span>](add-video-player.md)
