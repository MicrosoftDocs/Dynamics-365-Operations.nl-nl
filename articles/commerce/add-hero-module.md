---
title: Heldmodule
description: In dit onderwerp wordt beschreven wat heldmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785381"
---
# <a name="hero-module"></a><span data-ttu-id="1763f-103">Heldmodule</span><span class="sxs-lookup"><span data-stu-id="1763f-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1763f-104">In dit onderwerp wordt beschreven wat heldmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1763f-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1763f-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="1763f-105">Overview</span></span>

<span data-ttu-id="1763f-106">Een heldmodule wordt gebruikt voor de marketing van producten of promoties via een combinatie van afbeeldingen en tekst.</span><span class="sxs-lookup"><span data-stu-id="1763f-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="1763f-107">Een detailhandelaar kan bijvoorbeeld een heldmodule toevoegen aan de startpagina van een e-commerce-site om een nieuw product te promoten en de aandacht van klanten te trekken.</span><span class="sxs-lookup"><span data-stu-id="1763f-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="1763f-108">Een heldmodule wordt gestuurd door gegevens uit het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="1763f-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="1763f-109">Het is een zelfstandige module die niet afhankelijk is van andere modules op de pagina.</span><span class="sxs-lookup"><span data-stu-id="1763f-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="1763f-110">Een heldmodule kan op elke sitepagina worden geplaatst waar een detailhandelaar iets wil verhandelen of promoten (bijvoorbeeld producten, verkoop of functies).</span><span class="sxs-lookup"><span data-stu-id="1763f-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="1763f-111">Voorbeelden van heldmodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="1763f-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="1763f-112">U kunt een heldmodule gebruiken op de startpagina van een e-commerce-site om promoties en nieuwe producten te markeren.</span><span class="sxs-lookup"><span data-stu-id="1763f-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="1763f-113">U kunt een heldmodule op een pagina met productgegevens gebruiken om productinformatie te presenteren.</span><span class="sxs-lookup"><span data-stu-id="1763f-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="1763f-114">Er kunnen meerdere heldmodules in een carrouselmodule worden geplaatst om meerdere producten of promoties te markeren.</span><span class="sxs-lookup"><span data-stu-id="1763f-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="1763f-115">Eigenschappen van heldmodule</span><span class="sxs-lookup"><span data-stu-id="1763f-115">Hero module properties</span></span>

| <span data-ttu-id="1763f-116">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="1763f-116">Property name</span></span>  | <span data-ttu-id="1763f-117">Waarden</span><span class="sxs-lookup"><span data-stu-id="1763f-117">Values</span></span> | <span data-ttu-id="1763f-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="1763f-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="1763f-119">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="1763f-119">Image</span></span>          | <span data-ttu-id="1763f-120">Afbeeldingbestand</span><span class="sxs-lookup"><span data-stu-id="1763f-120">Image file</span></span> | <span data-ttu-id="1763f-121">Een afbeelding kan worden gebruikt voor de presentatie van een product of promotie.</span><span class="sxs-lookup"><span data-stu-id="1763f-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="1763f-122">Een afbeelding kan naar de afbeeldingengalerie worden geüpload, of er kan een bestaande afbeelding worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1763f-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="1763f-123">Koptekst</span><span class="sxs-lookup"><span data-stu-id="1763f-123">Heading</span></span>        | <span data-ttu-id="1763f-124">Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="1763f-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1763f-125">Elke heldmodule kan een koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="1763f-125">Every hero module can have a heading.</span></span> <span data-ttu-id="1763f-126">Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="1763f-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="1763f-127">De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="1763f-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="1763f-128">Alinea</span><span class="sxs-lookup"><span data-stu-id="1763f-128">Paragraph</span></span>      | <span data-ttu-id="1763f-129">Alineatekst</span><span class="sxs-lookup"><span data-stu-id="1763f-129">Paragraph text</span></span> | <span data-ttu-id="1763f-130">Heldmodules ondersteunen alineatekst in RTF-indeling.</span><span class="sxs-lookup"><span data-stu-id="1763f-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="1763f-131">Sommige basisfuncties voor tekstopmaak worden ondersteund, zoals vetgedrukte, onderstreepte en cursieve tekst en hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="1763f-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="1763f-132">Sommige van deze mogelijkheden kunnen worden overschreven door het paginathema dat op de module wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="1763f-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="1763f-133">Koppeling</span><span class="sxs-lookup"><span data-stu-id="1763f-133">Link</span></span>           | <span data-ttu-id="1763f-134">Koppelingstekst, koppelings-URL, het label Accessible Rich internet Applications (ARIA) en **Koppeling in nieuw tabblad openen**</span><span class="sxs-lookup"><span data-stu-id="1763f-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="1763f-135">Heldmodules ondersteunen een of meer koppelingen met oproep tot actie.</span><span class="sxs-lookup"><span data-stu-id="1763f-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="1763f-136">Als er een koppeling wordt toegevoegd, zijn een koppelingstekst, een URL en een ARIA-label vereist.</span><span class="sxs-lookup"><span data-stu-id="1763f-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="1763f-137">ARIA-labels moeten een omschrijving hebben om aan toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="1763f-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="1763f-138">U kunt koppelingen zo configureren dat deze worden geopend op een nieuw tabblad.</span><span class="sxs-lookup"><span data-stu-id="1763f-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="1763f-139">Tekstplaatsing</span><span class="sxs-lookup"><span data-stu-id="1763f-139">Text placement</span></span> | <span data-ttu-id="1763f-140">**Linksboven**, **rechtsboven**, **middenboven**, **linksonder**, **rechtsonder**, **middenonder**, **midden links**, **midden rechts** of **midden rechts**</span><span class="sxs-lookup"><span data-stu-id="1763f-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="1763f-141">Met deze eigenschap wordt de positie van de afbeelding ten opzichte van de tekst bepaald.</span><span class="sxs-lookup"><span data-stu-id="1763f-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="1763f-142">Als bijvoorbeeld **Rechts** is geselecteerd, wordt de afbeelding rechts van de tekst weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1763f-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="1763f-143">Tekstthema</span><span class="sxs-lookup"><span data-stu-id="1763f-143">Text theme</span></span>     | <span data-ttu-id="1763f-144">**Licht** of **donker**</span><span class="sxs-lookup"><span data-stu-id="1763f-144">**Light** or **Dark**</span></span> | <span data-ttu-id="1763f-145">Er kan een kleurenschema worden gedefinieerd voor de tekst op basis van de achtergrondafbeelding.</span><span class="sxs-lookup"><span data-stu-id="1763f-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="1763f-146">Als de afbeelding bijvoorbeeld een donkere achtergrond heeft, kan een licht thema worden toegepast om de tekst beter zichtbaar te maken en om te voldoen aan de kleurcontrastverhoudingen voor toegankelijkheidsdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="1763f-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="1763f-147">Kleurovergang</span><span class="sxs-lookup"><span data-stu-id="1763f-147">Gradient</span></span>       | <span data-ttu-id="1763f-148">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="1763f-148">**True** or **False**</span></span> | <span data-ttu-id="1763f-149">Er kan een kleurverloop op de afbeelding worden toegepast om te voldoen aan de kleurcontrastverhouding voor toegankelijkheidsdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="1763f-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="1763f-150">Een heldmodule toevoegen aan een nieuwe pagina</span><span class="sxs-lookup"><span data-stu-id="1763f-150">Add a hero module to a new page</span></span>

<span data-ttu-id="1763f-151">Voer de volgende stappen uit om een heldmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="1763f-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1763f-152">Ga naar **Sjablonen** en maak een paginasjabloon met de naam **heldsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="1763f-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="1763f-153">Voeg in het **hoofdvak** van de standaardpagina een heldmodule toe.</span><span class="sxs-lookup"><span data-stu-id="1763f-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="1763f-154">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="1763f-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="1763f-155">Gebruik de heldsjabloon die u zojuist hebt gemaakt om een pagina met de naam **Heldpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="1763f-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="1763f-156">Selecteer in het vak **Hoofd** van de standaardpagina de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="1763f-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1763f-157">Selecteer in het dialoogvenster **Module toevoegen** onder **Modules selecteren** een heldmodule en selecteer vervolgens **OK.**</span><span class="sxs-lookup"><span data-stu-id="1763f-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="1763f-158">Selecteer in de overzichtsstructuur aan de linkerkant de heldmodule.</span><span class="sxs-lookup"><span data-stu-id="1763f-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="1763f-159">Selecteer **Een afbeelding toevoegen** in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="1763f-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="1763f-160">Selecteer vervolgens een bestaande afbeelding of upload een nieuwe afbeelding.</span><span class="sxs-lookup"><span data-stu-id="1763f-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="1763f-161">Selecteer **Koptekst**.</span><span class="sxs-lookup"><span data-stu-id="1763f-161">Select **Heading**.</span></span>
1. <span data-ttu-id="1763f-162">Voeg in het dialoogvenster **Koptekst** de koptekst toe, selecteer het kopniveau en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="1763f-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="1763f-163">Voeg onder **RTF-indeling** de gewenste tekst toe.</span><span class="sxs-lookup"><span data-stu-id="1763f-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="1763f-164">Selecteer **Actiekoppeling toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="1763f-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="1763f-165">Voeg in het dialoogvenster **Actiekoppeling** de koppelingstekst, een koppelings-URL en een ARIA-label voor de koppeling toe en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="1763f-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="1763f-166">Sla de pagina op en bekijk uw wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="1763f-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="1763f-167">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="1763f-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1763f-168">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1763f-168">Additional resources</span></span>

[<span data-ttu-id="1763f-169">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="1763f-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1763f-170">Waarschuwingsmodule</span><span class="sxs-lookup"><span data-stu-id="1763f-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="1763f-171">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="1763f-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="1763f-172">Inhoudsrijke-blokmodule</span><span class="sxs-lookup"><span data-stu-id="1763f-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="1763f-173">Module voor het plaatsen van inhoud</span><span class="sxs-lookup"><span data-stu-id="1763f-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="1763f-174">Functiemodule</span><span class="sxs-lookup"><span data-stu-id="1763f-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="1763f-175">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="1763f-175">Video player module</span></span>](add-video-player.md)
