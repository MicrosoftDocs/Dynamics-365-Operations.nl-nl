---
title: Metagegevens SEO beheren
description: In dit onderwerp wordt beschreven hoe u SEO-metagegevens (Search Engine Optimization) in Microsoft Dynamics 365 Commerce kunt beheren.
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
ms.openlocfilehash: 3ea06713af69659c205686a971393892fa584072
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945715"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="6a525-103">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="6a525-103">Manage SEO metadata</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6a525-104">In dit onderwerp wordt beschreven hoe u SEO-metagegevens (Search Engine Optimization) in Microsoft Dynamics 365 Commerce kunt beheren.</span><span class="sxs-lookup"><span data-stu-id="6a525-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6a525-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="6a525-105">Overview</span></span>

<span data-ttu-id="6a525-106">SEO-metagegevens voor een site kunnen worden beheerd met siteoverzichten en metagegevens van de pagina.</span><span class="sxs-lookup"><span data-stu-id="6a525-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="6a525-107">Siteoverzichten</span><span class="sxs-lookup"><span data-stu-id="6a525-107">Site maps</span></span>

<span data-ttu-id="6a525-108">Een siteoverzicht is een machine-leesbare lijst, in XML-indeling, van de pagina's op uw website.</span><span class="sxs-lookup"><span data-stu-id="6a525-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="6a525-109">Het is bedoeld voor gebruik door zoekmachines, zodat ze betere zoekresultaten van uw site kunnen bieden.</span><span class="sxs-lookup"><span data-stu-id="6a525-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="6a525-110">Siteoverzichten kunnen handmatig worden opgenomen in zoekmachines of worden gepubliceerd in een robots.txt-bestand.</span><span class="sxs-lookup"><span data-stu-id="6a525-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="6a525-111">Dynamics 365 Commerce ondersteunt het automatisch genereren van siteoverzichten.</span><span class="sxs-lookup"><span data-stu-id="6a525-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="6a525-112">Siteoverzichten worden automatisch bijgewerkt wanneer pagina's worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="6a525-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="6a525-113">Genereren van siteoverzicht inschakelen</span><span class="sxs-lookup"><span data-stu-id="6a525-113">Turn on site map generation</span></span>

1. <span data-ttu-id="6a525-114">Meld u aan bij het ontwerpprogramma.</span><span class="sxs-lookup"><span data-stu-id="6a525-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="6a525-115">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="6a525-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="6a525-116">Selecteer **Sitebeheer** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="6a525-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="6a525-117">Controleer of de optie **Siteoverzichten ingeschakeld** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6a525-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="6a525-118">Metagegevens van pagina</span><span class="sxs-lookup"><span data-stu-id="6a525-118">Page metadata</span></span>

<span data-ttu-id="6a525-119">In Dynamics 365 Commerce kunt u SEO-metagegevens voor afzonderlijke pagina's beheren.</span><span class="sxs-lookup"><span data-stu-id="6a525-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="6a525-120">U kunt deze gegevens weergeven en wijzigen in de sectie **SEO-eigenschappen** van een paginacontainer.</span><span class="sxs-lookup"><span data-stu-id="6a525-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="6a525-121">De volgende eigenschappen voor SEO-metagegevens worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="6a525-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="6a525-122">Titel</span><span class="sxs-lookup"><span data-stu-id="6a525-122">Title</span></span>
- <span data-ttu-id="6a525-123">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6a525-123">Description</span></span>
- <span data-ttu-id="6a525-124">SEO-trefwoorden</span><span class="sxs-lookup"><span data-stu-id="6a525-124">SEO keywords</span></span>
- <span data-ttu-id="6a525-125">Aria-labels</span><span class="sxs-lookup"><span data-stu-id="6a525-125">Aria labels</span></span>
- <span data-ttu-id="6a525-126">noindex</span><span class="sxs-lookup"><span data-stu-id="6a525-126">noindex</span></span>
- <span data-ttu-id="6a525-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="6a525-127">nofollow</span></span>
- <span data-ttu-id="6a525-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="6a525-128">noarchive</span></span>
- <span data-ttu-id="6a525-129">nocache</span><span class="sxs-lookup"><span data-stu-id="6a525-129">nocache</span></span>
- <span data-ttu-id="6a525-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="6a525-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="6a525-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="6a525-131">nosnippet</span></span>
- <span data-ttu-id="6a525-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="6a525-132">noImageIndex</span></span>
- <span data-ttu-id="6a525-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="6a525-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="6a525-134">Metagegevens van de pagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="6a525-134">Modify page metadata</span></span>

<span data-ttu-id="6a525-135">Volg deze stappen om metagegevens te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6a525-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="6a525-136">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="6a525-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="6a525-137">Selecteer **Pagina's** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="6a525-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="6a525-138">Selecteer de startpagina om deze te openen in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="6a525-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="6a525-139">Selecteer **Uitchecken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="6a525-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="6a525-140">Vouw **Standaard metatags** uit in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="6a525-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="6a525-141">Als u een nieuwe metatag wilt toevoegen, selecteert u **Toevoegen** en geeft u de tag op in het veld.</span><span class="sxs-lookup"><span data-stu-id="6a525-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="6a525-142">Als u een bestaande metatag wilt verwijderen, selecteert u het prullenbaksymbool rechts ervan.</span><span class="sxs-lookup"><span data-stu-id="6a525-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="6a525-143">Selecteer **Opslaan** en vervolgens **Inchecken**.</span><span class="sxs-lookup"><span data-stu-id="6a525-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="6a525-144">Voer in het veld **Opmerkingen** **Metatags bijgewerkt** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a525-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="6a525-145">Selecteer **Voorbeeld** om uw pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="6a525-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="6a525-146">Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="6a525-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="6a525-147">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="6a525-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a525-148">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6a525-148">Additional resources</span></span>

[<span data-ttu-id="6a525-149">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="6a525-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="6a525-150">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="6a525-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="6a525-151">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="6a525-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="6a525-152">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="6a525-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="6a525-153">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="6a525-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="6a525-154">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="6a525-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="6a525-155">Toegankelijkheid van pagina-inhoud controleren</span><span class="sxs-lookup"><span data-stu-id="6a525-155">Verify page content accessibility</span></span>](verify-accessibility.md)
