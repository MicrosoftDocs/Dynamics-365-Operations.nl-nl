---
title: Een nieuwe sitepagina toevoegen
description: In dit onderwerp wordt beschreven hoe u een nieuwe sitepagina toevoegt in Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d5ab90343220e427a80cc4dde17c628ba64ac69e
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696733"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="eda56-103">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="eda56-103">Add a new site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="eda56-104">In dit onderwerp wordt beschreven hoe u een nieuwe sitepagina toevoegt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eda56-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="eda56-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="eda56-105">Overview</span></span>

<span data-ttu-id="eda56-106">Nadat u sjablonen en fragmenten voor uw site hebt gemaakt, is de volgende stap het maken van pagina's die deze gebruiken.</span><span class="sxs-lookup"><span data-stu-id="eda56-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="eda56-107">Om aan de slag te gaan moet u een sjabloon of indeling, een paginanaam en een pagina-URL selecteren.</span><span class="sxs-lookup"><span data-stu-id="eda56-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="eda56-108">Sjabloon of indeling</span><span class="sxs-lookup"><span data-stu-id="eda56-108">Template or layout</span></span>

<span data-ttu-id="eda56-109">U kunt een sjabloon of een indeling gebruiken voor uw nieuwe pagina.</span><span class="sxs-lookup"><span data-stu-id="eda56-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="eda56-110">Zie voor meer informatie [Overzicht met sjablonen en indelingen](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eda56-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="eda56-111">Paginanaam</span><span class="sxs-lookup"><span data-stu-id="eda56-111">Page name</span></span>

<span data-ttu-id="eda56-112">De paginanaam moet uniek zijn voor de pagina.</span><span class="sxs-lookup"><span data-stu-id="eda56-112">The page name must be unique to your page.</span></span> <span data-ttu-id="eda56-113">Het moet een duidelijke omschrijving zijn, zodat u deze gemakkelijk kunt terugvinden en andere mensen weten waarvoor de pagina bedoeld is.</span><span class="sxs-lookup"><span data-stu-id="eda56-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="eda56-114">U kunt de paginanaam zorgvuldig kiezen, omdat deze later niet kan worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="eda56-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="eda56-115">Pagina-URL</span><span class="sxs-lookup"><span data-stu-id="eda56-115">Page URL</span></span>

<span data-ttu-id="eda56-116">U kunt kiezen of u een URL wilt invoeren voor uw nieuwe pagina.</span><span class="sxs-lookup"><span data-stu-id="eda56-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="eda56-117">Wanneer u een pagina maakt, kunt u een tekenreeks invoeren die wordt gebruikt om een volledige URL te vormen.</span><span class="sxs-lookup"><span data-stu-id="eda56-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="eda56-118">De tekenreeks staat bekend als relatieve URL of URL-slug genoemd.</span><span class="sxs-lookup"><span data-stu-id="eda56-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="eda56-119">Vervolgens wordt een volledige URL gegenereerd op basis van de URL-slug en wordt de nieuwe pagina hieraan toegewezen.</span><span class="sxs-lookup"><span data-stu-id="eda56-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="eda56-120">U kunt de URL-slug later wijzigen voordat u de pagina publiceert.</span><span class="sxs-lookup"><span data-stu-id="eda56-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="eda56-121">Zie [Een pagina-URL maken](create-page-URL.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eda56-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="eda56-122">in Dynamics 365 Commerce worden URL's en inhoud losgekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eda56-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="eda56-123">Dit betekent dat een pagina kan worden gemaakt die niet is gekoppeld aan een URL en een URL die niet aan een pagina is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eda56-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="eda56-124">Daarom kan de inhoudomwisseling voor een URL worden uitgevoerd zonder dat uitvaltijd nodig is en zijn omleidingen eenvoudiger te beheren.</span><span class="sxs-lookup"><span data-stu-id="eda56-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="eda56-125">Een nieuwe pagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="eda56-125">Add a new page</span></span>

<span data-ttu-id="eda56-126">Voer de volgende stappen uit om een nieuwe sitepagina aan uw site toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="eda56-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="eda56-127">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="eda56-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="eda56-128">Selecteer **Nieuwe pagina**.</span><span class="sxs-lookup"><span data-stu-id="eda56-128">Select **New Page**.</span></span>
1. <span data-ttu-id="eda56-129">Selecteer in het dialoogvenster **Nieuwe pagina** een sjabloon en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="eda56-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="eda56-130">Voer in het veld **Paginanaam** een paginanaam in (bijvoorbeeld **Mijn nieuwe pagina**).</span><span class="sxs-lookup"><span data-stu-id="eda56-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="eda56-131">Voer in het veld **URL** een tekenreeks (de URL-slug) in om de URL te voltooien (bijvoorbeeld **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="eda56-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="eda56-132">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="eda56-132">Select **OK**.</span></span> <span data-ttu-id="eda56-133">De pagina-editor wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eda56-133">The page editor appears.</span></span> <span data-ttu-id="eda56-134">U ziet dat een koptekst en een voettekst automatisch worden toegevoegd aan de pagina op basis van de sjabloon die u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="eda56-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="eda56-135">Selecteer in het paginaoverzicht het vak **Hoofd** de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="eda56-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="eda56-136">Selecteer **Container** en vervolgens **OK**</span><span class="sxs-lookup"><span data-stu-id="eda56-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="eda56-137">Selecteer in **Vloeibare container** de knop met het weglatingsteken en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="eda56-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="eda56-138">Selecteer **Blok met uitgebreide inhoud**en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="eda56-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="eda56-139">Selecteer **Blok met uitgebreide inhoud**, de knop met het weglatingsteken en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="eda56-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="eda56-140">Selecteer **Blokitem met uitgebreide inhoud**en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="eda56-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="eda56-141">Selecteer **Alinea** in het deelvenster Eigenschappen aan de rechterkant en voer vervolgens **Mijn testtekst** in het veld in.</span><span class="sxs-lookup"><span data-stu-id="eda56-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="eda56-142">Selecteer **Opslaan** en vervolgens **Inchecken**.</span><span class="sxs-lookup"><span data-stu-id="eda56-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="eda56-143">Voer in het veld **Opmerkingen** **Toegevoegde nieuwe pagina** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="eda56-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="eda56-144">Selecteer **Voorbeeld** om uw pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="eda56-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="eda56-145">Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="eda56-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="eda56-146">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="eda56-146">Select **Publish**.</span></span>
1. <span data-ttu-id="eda56-147">Selecteer **Fabrikam** (of de naam van uw site) in het navigatiepad (broodkruimels).</span><span class="sxs-lookup"><span data-stu-id="eda56-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="eda56-148">Selecteer **URL's** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="eda56-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="eda56-149">Zoek en selecteer uw URL (**mynewpage**) in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eda56-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="eda56-150">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="eda56-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eda56-151">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="eda56-151">Additional resources</span></span>

[<span data-ttu-id="eda56-152">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="eda56-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="eda56-153">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="eda56-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="eda56-154">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="eda56-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="eda56-155">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="eda56-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="eda56-156">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="eda56-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="eda56-157">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="eda56-157">Enrich a category landing page</span></span>](enrich-category-page.md)

