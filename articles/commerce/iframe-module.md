---
title: Iframe-module
description: In dit onderwerp wordt beschreven wat de iframe-module is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0616a772a416a7c9d9756a840c93b8601c08c3d0
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646901"
---
# <a name="iframe-module"></a><span data-ttu-id="2086a-103">Iframe-module</span><span class="sxs-lookup"><span data-stu-id="2086a-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2086a-104">In dit onderwerp wordt beschreven wat de iframe-module is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2086a-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2086a-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="2086a-105">Overview</span></span>

<span data-ttu-id="2086a-106">Een iframe-module biedt een iframe (inline frame) dat de host is van externe inhoud op een site.</span><span class="sxs-lookup"><span data-stu-id="2086a-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="2086a-107">Het kan bijvoorbeeld worden gebruikt om een YouTube-video of PDF-bestandsviewer te hosten op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="2086a-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="2086a-108">Voor een iframe-module is een doel-URL vereist.</span><span class="sxs-lookup"><span data-stu-id="2086a-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="2086a-109">Vervolgens wordt de inhoud van de doelpagina binnen een HTML **iframe**-element gehost.</span><span class="sxs-lookup"><span data-stu-id="2086a-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="2086a-110">Externe URL's moeten worden vermeld in de toegestane lijst (ook wel 'whitelist' genoemd) volgens de CSP-instructies (Content Security Policy) van de site.</span><span class="sxs-lookup"><span data-stu-id="2086a-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="2086a-111">Voor iframe-inhoud moeten URL's worden toegestaan met behulp van de instructie **frame-ancestor**.</span><span class="sxs-lookup"><span data-stu-id="2086a-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="2086a-112">Zie voor meer informatie [Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="2086a-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

<span data-ttu-id="2086a-113">De volgende afbeelding laat voorbeelden van iframe-modules zien waarin externe video's op sitepagina's worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="2086a-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Voorbeeld van iframe-modules met externe video's](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="2086a-115">Eigenschappen van iframe-module</span><span class="sxs-lookup"><span data-stu-id="2086a-115">Iframe module properties</span></span>

| <span data-ttu-id="2086a-116">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="2086a-116">Property name</span></span>             | <span data-ttu-id="2086a-117">Waarde</span><span class="sxs-lookup"><span data-stu-id="2086a-117">Value</span></span>                 | <span data-ttu-id="2086a-118">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="2086a-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2086a-119">Kop</span><span class="sxs-lookup"><span data-stu-id="2086a-119">Heading</span></span> | <span data-ttu-id="2086a-120">Tekst</span><span class="sxs-lookup"><span data-stu-id="2086a-120">Text</span></span> | <span data-ttu-id="2086a-121">De koptekst voor de module.</span><span class="sxs-lookup"><span data-stu-id="2086a-121">The heading for the module.</span></span> |
| <span data-ttu-id="2086a-122">Doel-URL</span><span class="sxs-lookup"><span data-stu-id="2086a-122">Target URL</span></span> | <span data-ttu-id="2086a-123">URL</span><span class="sxs-lookup"><span data-stu-id="2086a-123">URL</span></span> | <span data-ttu-id="2086a-124">De URL die wordt gehost in de module.</span><span class="sxs-lookup"><span data-stu-id="2086a-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="2086a-125">Hoogte</span><span class="sxs-lookup"><span data-stu-id="2086a-125">Height</span></span> | <span data-ttu-id="2086a-126">Getal of percentage</span><span class="sxs-lookup"><span data-stu-id="2086a-126">Number or percentage</span></span> | <span data-ttu-id="2086a-127">De hoogte van de module, in pixels of als een percentage.</span><span class="sxs-lookup"><span data-stu-id="2086a-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="2086a-128">De waarde **100** wordt bijvoorbeeld behandeld als een aantal pixels en de waarde **100%** wordt beschouwd als een percentage.</span><span class="sxs-lookup"><span data-stu-id="2086a-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="2086a-129">Aria-label</span><span class="sxs-lookup"><span data-stu-id="2086a-129">Aria label</span></span> | <span data-ttu-id="2086a-130">Tekst</span><span class="sxs-lookup"><span data-stu-id="2086a-130">Text</span></span> | <span data-ttu-id="2086a-131">Een toegankelijk ARIA-label (Accessible Rich internet Applications) kan worden gedefinieerd voor toegankelijkheidsdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="2086a-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="2086a-132">Een iframe-module toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="2086a-132">Add an iframe module to a page</span></span>

<span data-ttu-id="2086a-133">Voer de volgende stappen uit om een iframe-module aan een pagina toe te voegen om een externe video weer te geven.</span><span class="sxs-lookup"><span data-stu-id="2086a-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="2086a-134">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="2086a-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2086a-135">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Marketingsjabloon** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="2086a-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2086a-136">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="2086a-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2086a-137">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="2086a-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2086a-138">Selecteer in het dialoogvenster **Een sjabloon kiezen** de sjabloon **Marketingsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="2086a-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="2086a-139">Voer onder **Paginanaam** **Marketingpagina** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="2086a-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="2086a-140">Selecteer in het vak **Hoofd** van de nieuwe pagina het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2086a-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2086a-141">Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="2086a-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2086a-142">Stel in het eigenschappenvenster van de module de **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="2086a-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="2086a-143">Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2086a-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2086a-144">Selecteer in het dialoogvenster **Module toevoegen** de **iframe**-module en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="2086a-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2086a-145">Stel in het eigenschappenvenster van de module de waarde van de **Doel-URL** in op een externe URL voor een video.</span><span class="sxs-lookup"><span data-stu-id="2086a-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="2086a-146">Stel zo nodig andere eigenschappen, zoals **koptekst** en **Hoogte** in.</span><span class="sxs-lookup"><span data-stu-id="2086a-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="2086a-147">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="2086a-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2086a-148">Ga naar de marketingpagina op uw site.</span><span class="sxs-lookup"><span data-stu-id="2086a-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="2086a-149">U ziet dat de video wordt weergegeven in de iframe-module.</span><span class="sxs-lookup"><span data-stu-id="2086a-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="2086a-150">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="2086a-150">Additional resources</span></span>

[<span data-ttu-id="2086a-151">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="2086a-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2086a-152">Beveiligingsbeleid voor inhoud (CSP) beheren</span><span class="sxs-lookup"><span data-stu-id="2086a-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
