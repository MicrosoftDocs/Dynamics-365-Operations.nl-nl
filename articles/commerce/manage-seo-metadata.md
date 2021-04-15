---
title: Metagegevens SEO beheren
description: In dit onderwerp wordt beschreven hoe u SEO-metagegevens (Search Engine Optimization) in Microsoft Dynamics 365 Commerce kunt beheren.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794206"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="dd687-103">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="dd687-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dd687-104">In dit onderwerp wordt beschreven hoe u SEO-metagegevens (Search Engine Optimization) in Microsoft Dynamics 365 Commerce kunt beheren.</span><span class="sxs-lookup"><span data-stu-id="dd687-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dd687-105">SEO-metagegevens voor een site kunnen worden beheerd met siteoverzichten en metagegevens van de pagina.</span><span class="sxs-lookup"><span data-stu-id="dd687-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="dd687-106">Siteoverzichten</span><span class="sxs-lookup"><span data-stu-id="dd687-106">Site maps</span></span>

<span data-ttu-id="dd687-107">Een siteoverzicht is een machine-leesbare lijst, in XML-indeling, van de pagina's op uw website.</span><span class="sxs-lookup"><span data-stu-id="dd687-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="dd687-108">Het is bedoeld voor gebruik door zoekmachines, zodat ze betere zoekresultaten van uw site kunnen bieden.</span><span class="sxs-lookup"><span data-stu-id="dd687-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="dd687-109">Siteoverzichten kunnen handmatig worden opgenomen in zoekmachines of worden gepubliceerd in een robots.txt-bestand.</span><span class="sxs-lookup"><span data-stu-id="dd687-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="dd687-110">Dynamics 365 Commerce ondersteunt het automatisch genereren van siteoverzichten.</span><span class="sxs-lookup"><span data-stu-id="dd687-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="dd687-111">Siteoverzichten worden automatisch bijgewerkt wanneer pagina's worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="dd687-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="dd687-112">Genereren van siteoverzicht inschakelen</span><span class="sxs-lookup"><span data-stu-id="dd687-112">Turn on site map generation</span></span>

1. <span data-ttu-id="dd687-113">Meld u aan bij het ontwerpprogramma.</span><span class="sxs-lookup"><span data-stu-id="dd687-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="dd687-114">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="dd687-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="dd687-115">Selecteer **Sitebeheer** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="dd687-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="dd687-116">Controleer of de optie **Siteoverzichten ingeschakeld** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="dd687-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="dd687-117">Metagegevens van pagina</span><span class="sxs-lookup"><span data-stu-id="dd687-117">Page metadata</span></span>

<span data-ttu-id="dd687-118">In Dynamics 365 Commerce kunt u SEO-metagegevens voor afzonderlijke pagina's beheren.</span><span class="sxs-lookup"><span data-stu-id="dd687-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="dd687-119">U kunt deze gegevens weergeven en wijzigen in de sectie **SEO-eigenschappen** van een paginacontainer.</span><span class="sxs-lookup"><span data-stu-id="dd687-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="dd687-120">De volgende eigenschappen voor SEO-metagegevens worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="dd687-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="dd687-121">Titel</span><span class="sxs-lookup"><span data-stu-id="dd687-121">Title</span></span>
- <span data-ttu-id="dd687-122">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dd687-122">Description</span></span>
- <span data-ttu-id="dd687-123">SEO-trefwoorden</span><span class="sxs-lookup"><span data-stu-id="dd687-123">SEO keywords</span></span>
- <span data-ttu-id="dd687-124">Aria-labels</span><span class="sxs-lookup"><span data-stu-id="dd687-124">Aria labels</span></span>
- <span data-ttu-id="dd687-125">noindex</span><span class="sxs-lookup"><span data-stu-id="dd687-125">noindex</span></span>
- <span data-ttu-id="dd687-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="dd687-126">nofollow</span></span>
- <span data-ttu-id="dd687-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="dd687-127">noarchive</span></span>
- <span data-ttu-id="dd687-128">nocache</span><span class="sxs-lookup"><span data-stu-id="dd687-128">nocache</span></span>
- <span data-ttu-id="dd687-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="dd687-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="dd687-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="dd687-130">nosnippet</span></span>
- <span data-ttu-id="dd687-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="dd687-131">noImageIndex</span></span>
- <span data-ttu-id="dd687-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="dd687-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="dd687-133">Metagegevens van de pagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="dd687-133">Modify page metadata</span></span>

<span data-ttu-id="dd687-134">Volg deze stappen om metagegevens te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="dd687-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="dd687-135">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="dd687-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="dd687-136">Selecteer **Pagina's** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="dd687-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="dd687-137">Selecteer de startpagina om deze te openen in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="dd687-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="dd687-138">Selecteer **Bewerken** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="dd687-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="dd687-139">Vouw **Standaard metatags** uit in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="dd687-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="dd687-140">Als u een nieuwe metatag wilt toevoegen, selecteert u **Toevoegen** en geeft u de tag op in het veld.</span><span class="sxs-lookup"><span data-stu-id="dd687-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="dd687-141">Als u een bestaande metatag wilt verwijderen, selecteert u het prullenbaksymbool rechts ervan.</span><span class="sxs-lookup"><span data-stu-id="dd687-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="dd687-142">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="dd687-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="dd687-143">Voer in het veld **Opmerkingen** **Metatags bijgewerkt** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd687-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="dd687-144">Selecteer **Voorbeeld** om uw pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="dd687-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="dd687-145">Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="dd687-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="dd687-146">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="dd687-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd687-147">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="dd687-147">Additional resources</span></span>

[<span data-ttu-id="dd687-148">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="dd687-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="dd687-149">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="dd687-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="dd687-150">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="dd687-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="dd687-151">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="dd687-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="dd687-152">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="dd687-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="dd687-153">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="dd687-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="dd687-154">Toegankelijkheid van pagina-inhoud controleren</span><span class="sxs-lookup"><span data-stu-id="dd687-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="dd687-155">Dynamische e-commercepagina's maken op basis van URL-parameters</span><span class="sxs-lookup"><span data-stu-id="dd687-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
