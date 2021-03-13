---
title: Dynamische e-commercepagina's maken op basis van URL-parameters
description: In dit onderwerp wordt beschreven hoe u een Microsoft Dynamics 365 Commerce-e-commercepagina kunt instellen die dynamische inhoud kan aanbieden op basis van URL-parameters.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098619"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="939bd-103">Dynamische e-commercepagina's maken op basis van URL-parameters</span><span class="sxs-lookup"><span data-stu-id="939bd-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="939bd-104">In dit onderwerp wordt beschreven hoe u een Microsoft Dynamics 365 Commerce-e-commercepagina kunt instellen die dynamische inhoud kan aanbieden op basis van URL-parameters.</span><span class="sxs-lookup"><span data-stu-id="939bd-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="939bd-105">Een e-commercepagina kan worden geconfigureerd voor verschillende soorten inhoud, gebaseerd op een segment in het URL-pad.</span><span class="sxs-lookup"><span data-stu-id="939bd-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="939bd-106">Daarom staat de pagina bekend als een dynamische pagina.</span><span class="sxs-lookup"><span data-stu-id="939bd-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="939bd-107">Het segment wordt gebruikt als parameter om de pagina-inhoud op te halen.</span><span class="sxs-lookup"><span data-stu-id="939bd-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="939bd-108">Een pagina met de naam **blog\_viewer** wordt bijvoorbeeld gemaakt en aan de URL `https://fabrikam.com/blog` gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="939bd-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="939bd-109">Deze pagina kan vervolgens worden gebruikt om andere inhoud weer te geven, gebaseerd op het laatste segment in het URL-pad.</span><span class="sxs-lookup"><span data-stu-id="939bd-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="939bd-110">Het laatste segment in de URL `https://fabrikam.com/blog/article-1` is bijvoorbeeld **artikel-1**.</span><span class="sxs-lookup"><span data-stu-id="939bd-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="939bd-111">Aparte aangepaste pagina's die de dynamische pagina overschrijven, kunnen ook aan segmenten in het URL-pad worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="939bd-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="939bd-112">Een pagina met de naam **blog\_overzicht** wordt bijvoorbeeld gemaakt en aan de URL `https://fabrikam.com/blog/about-this-blog` gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="939bd-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="939bd-113">Wanneer deze URL wordt aangevraagd, wordt de pagina **blog\_overzicht** die is gekoppeld aan de parameter **/over-dit-blog** geretourneerd in plaats van de pagina **blog\_viewer**.</span><span class="sxs-lookup"><span data-stu-id="939bd-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="939bd-114">De functionaliteit voor het hosten, ophalen en weergeven van dynamische pagina-inhoud is geïmplementeerd met een aangepaste module.</span><span class="sxs-lookup"><span data-stu-id="939bd-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="939bd-115">Zie [Uitbreidbaarheid van online kanalen](e-commerce-extensibility/overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="939bd-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="939bd-116">Een dynamische e-commercepagina instellen</span><span class="sxs-lookup"><span data-stu-id="939bd-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="939bd-117">Als u een dynamische e-commercepagina wilt instellen, moet u de dynamische pagina maken, de basis-URL maken en de route naar de dynamische pagina configureren.</span><span class="sxs-lookup"><span data-stu-id="939bd-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="939bd-118">De pagina maken die dynamische inhoud zal aanbieden</span><span class="sxs-lookup"><span data-stu-id="939bd-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="939bd-119">Volg de stappen in [Een nieuwe sitepagina toevoegen](add-new-page.md) om een pagina te maken voor dynamische inhoud.</span><span class="sxs-lookup"><span data-stu-id="939bd-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="939bd-120">Voor de pagina die u maakt, moet een module worden uitgevoerd die gebruikmaakt van het laatste segment in het URL-pad om inhoud op te halen uit een externe gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="939bd-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="939bd-121">Zie [Uitbreidbaarheid van online kanalen](e-commerce-extensibility/overview.md) voor meer informatie over aangepaste moduleontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="939bd-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="939bd-122">De basis-URL voor de dynamische pagina maken</span><span class="sxs-lookup"><span data-stu-id="939bd-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="939bd-123">Volg deze stappen om de basis-URL voor de dynamische pagina in Commerce Site Builder te maken.</span><span class="sxs-lookup"><span data-stu-id="939bd-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="939bd-124">Ga naar **URL's** en selecteer **Nieuw \> Nieuwe URL**.</span><span class="sxs-lookup"><span data-stu-id="939bd-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="939bd-125">Selecteer in het dialoogvenster **Nieuwe URL maken** de optie **Interne pagina**.</span><span class="sxs-lookup"><span data-stu-id="939bd-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="939bd-126">Voer onder **URL-pad** het pad in dat zal fungeren als basis voor de dynamische pagina (in dit voorbeeld **/blog**).</span><span class="sxs-lookup"><span data-stu-id="939bd-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="939bd-127">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="939bd-127">Then select **Next**.</span></span>
1. <span data-ttu-id="939bd-128">Selecteer in het dialoogvenster **Een pagina selecteren** de pagina die u als de dynamische pagina hebt gemaakt, en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="939bd-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="939bd-129">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="939bd-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="939bd-130">De route naar de dynamische pagina configureren</span><span class="sxs-lookup"><span data-stu-id="939bd-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="939bd-131">Volg deze stappen om de route naar de dynamische pagina in Commerce Site Builder te maken.</span><span class="sxs-lookup"><span data-stu-id="939bd-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="939bd-132">Ga naar **Site-instellingen \> Extensies**.</span><span class="sxs-lookup"><span data-stu-id="939bd-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="939bd-133">Selecteer onder **Parameter-URL-paden** de optie **Toevoegen** en voer het URL-pad in dat u hebt ingevoerd toen u de URL hebt gemaakt (in dit voorbeeld **/blog**).</span><span class="sxs-lookup"><span data-stu-id="939bd-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="939bd-134">Selecteer **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="939bd-134">Select **Save and publish**.</span></span>

<span data-ttu-id="939bd-135">Nadat de route is geconfigureerd, retourneren alle aanvragen naar het pad met de parameter-URL de pagina die aan die URL is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="939bd-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="939bd-136">Als er aanvragen zijn die een extra segment bevatten, wordt de bijbehorende pagina geretourneerd en wordt de pagina-inhoud opgehaald door het segment als parameter te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="939bd-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="939bd-137">`https://fabrikam.com/blog/article-1` retourneert bijvoorbeeld de pagina **blog\_overzicht**, waarna de pagina-inhoud wordt opgehaald met de parameter **/artikel-1**.</span><span class="sxs-lookup"><span data-stu-id="939bd-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="939bd-138">Een parameter-URL met een aangepaste pagina overschrijven</span><span class="sxs-lookup"><span data-stu-id="939bd-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="939bd-139">Volg deze stappen om een parameter-URL met een aangepaste pagina in Commerce Site Builder te overschrijven.</span><span class="sxs-lookup"><span data-stu-id="939bd-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="939bd-140">Ga naar **URL's** en selecteer **Nieuw \> Nieuwe URL**.</span><span class="sxs-lookup"><span data-stu-id="939bd-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="939bd-141">Selecteer in het dialoogvenster **Nieuwe URL maken** de optie **Interne pagina**.</span><span class="sxs-lookup"><span data-stu-id="939bd-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="939bd-142">Voer onder **URL-pad** het pad in dat het segment bevat dat u wilt overschrijven (in dit voorbeeld **/blog/over-dit-blog**).</span><span class="sxs-lookup"><span data-stu-id="939bd-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="939bd-143">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="939bd-143">Then select **Next**.</span></span>
1. <span data-ttu-id="939bd-144">Selecteer in het dialoogvenster **Een pagina selecteren** de aangepaste pagina en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="939bd-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="939bd-145">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="939bd-145">Select **Publish**.</span></span>
1. <span data-ttu-id="939bd-146">Als de aangepaste pagina nog niet is gepubliceerd, gaat u naar **Pagina's**, selecteert u de aangepaste pagina en selecteert u **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="939bd-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="939bd-147">Nadat de aangepaste pagina is gepubliceerd, wordt deze gebruikt in plaats van de dynamische pagina met parameterinhoud.</span><span class="sxs-lookup"><span data-stu-id="939bd-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="939bd-148">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="939bd-148">Additional resources</span></span>

[<span data-ttu-id="939bd-149">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="939bd-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="939bd-150">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="939bd-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="939bd-151">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="939bd-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="939bd-152">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="939bd-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="939bd-153">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="939bd-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="939bd-154">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="939bd-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="939bd-155">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="939bd-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="939bd-156">Toegankelijkheid van pagina-inhoud controleren</span><span class="sxs-lookup"><span data-stu-id="939bd-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="939bd-157">Uitbreidbaarheid van online afzetkanaal</span><span class="sxs-lookup"><span data-stu-id="939bd-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)
