---
title: Een pagina-URL maken
description: In dit onderwerp worden de basisconcepten en procedures beschreven voor het maken van een pagina-URL op uw site.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98743d8948669f32d3c74e1915c7ed53db81141c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795686"
---
# <a name="create-a-page-url"></a><span data-ttu-id="69ed4-103">Een pagina-URL maken</span><span class="sxs-lookup"><span data-stu-id="69ed4-103">Create a page URL</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="69ed4-104">In dit onderwerp worden de basisconcepten en procedures beschreven voor het maken van een pagina-URL op uw site.</span><span class="sxs-lookup"><span data-stu-id="69ed4-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

<span data-ttu-id="69ed4-105">De volledige of absolute URL die naar een pagina op uw site verwijst, bestaat uit verschillende onderdelen.</span><span class="sxs-lookup"><span data-stu-id="69ed4-105">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="69ed4-106">De URL `https://www.contoso.com/en-us/contactus` heeft bijvoorbeeld de volgende onderdelen:</span><span class="sxs-lookup"><span data-stu-id="69ed4-106">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="69ed4-107">`https://www.contoso.com`: het HTTP-protocol en het domein van de site.</span><span class="sxs-lookup"><span data-stu-id="69ed4-107">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="69ed4-108">`/en-us`: het taalpad van de site.</span><span class="sxs-lookup"><span data-stu-id="69ed4-108">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="69ed4-109">`/contactus`: de relatieve URL voor de pagina **Contact opnemen**.</span><span class="sxs-lookup"><span data-stu-id="69ed4-109">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="69ed4-110">Een relatieve URL wordt ook wel een *tijdelijke aanduiding* (slug) voor een URL genoemd.</span><span class="sxs-lookup"><span data-stu-id="69ed4-110">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="69ed4-111">U kunt het domein en het pad naar de optionele taal van de site instellen wanneer u de site instelt.</span><span class="sxs-lookup"><span data-stu-id="69ed4-111">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="69ed4-112">U kunt meer domeinen en taalpaden aan uw site toevoegen via de online winkelpagina in de instellingen van de site.</span><span class="sxs-lookup"><span data-stu-id="69ed4-112">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="69ed4-113">De URL-slug voor een pagina bestaat als een zelfstandige entiteit in de ontwerpomgeving van de site.</span><span class="sxs-lookup"><span data-stu-id="69ed4-113">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="69ed4-114">Een pagina-URL bestaat uit twee delen: een naam die de URL-slug vertegenwoordigt en een verwijzing naar een pagina op uw site of een externe site.</span><span class="sxs-lookup"><span data-stu-id="69ed4-114">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="69ed4-115">Een pagina-URL kan ook worden geconfigureerd om te fungeren als een omleiding naar een andere pagina op uw site of een externe site.</span><span class="sxs-lookup"><span data-stu-id="69ed4-115">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="69ed4-116">Een pagina-URL maken</span><span class="sxs-lookup"><span data-stu-id="69ed4-116">Create a page URL</span></span>

<span data-ttu-id="69ed4-117">Er zijn twee manieren om pagina-URL's te maken:</span><span class="sxs-lookup"><span data-stu-id="69ed4-117">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="69ed4-118">Automatisch, wanneer u een pagina maakt</span><span class="sxs-lookup"><span data-stu-id="69ed4-118">Automatically, when you create a page</span></span>
- <span data-ttu-id="69ed4-119">Handmatig, op de pagina **URL's**</span><span class="sxs-lookup"><span data-stu-id="69ed4-119">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="69ed4-120">Een pagina-URL maken wanneer u een pagina maakt</span><span class="sxs-lookup"><span data-stu-id="69ed4-120">Create a page URL when you create a page</span></span>

<span data-ttu-id="69ed4-121">Als u een naam opgeeft in het veld **URL** wanneer u een nieuwe pagina maakt, wordt er automatisch een pagina-URL gemaakt die naar die pagina verwijst op de pagina **URL's**.</span><span class="sxs-lookup"><span data-stu-id="69ed4-121">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="69ed4-122">Nadat u de URL hebt gepubliceerd en de pagina waarnaar deze verwijst, hebben sitegebruikers (uw klanten) toegang tot de pagina die aan de URL is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="69ed4-122">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="69ed4-123">Als u een URL publiceert zonder de pagina te publiceren waarnaar deze verwijst, ontvangen sitegebruikers een 404-fout wanneer ze proberen toegang te krijgen tot de pagina.</span><span class="sxs-lookup"><span data-stu-id="69ed4-123">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="69ed4-124">Als u een pagina publiceert zonder de URL te publiceren die naar deze pagina verwijst, wordt de pagina niet geopend met behulp van een URL.</span><span class="sxs-lookup"><span data-stu-id="69ed4-124">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="69ed4-125">Handmatig een pagina-URL maken</span><span class="sxs-lookup"><span data-stu-id="69ed4-125">Manually create a page URL</span></span>

<span data-ttu-id="69ed4-126">Wanneer u nieuwe pagina's maakt, hoeft u geen pagina-URL op te geven.</span><span class="sxs-lookup"><span data-stu-id="69ed4-126">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="69ed4-127">Als u het URL-veld leeg laat, wordt de pagina in een niet-gekoppelde status gemaakt.</span><span class="sxs-lookup"><span data-stu-id="69ed4-127">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="69ed4-128">In dit geval hebben klanten geen toegang tot de pagina, zelfs als deze is gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="69ed4-128">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="69ed4-129">Als u de pagina toegankelijk wilt maken, moet u de URL handmatig maken en aan de pagina koppelen.</span><span class="sxs-lookup"><span data-stu-id="69ed4-129">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="69ed4-130">Voer de volgende stappen uit om handmatig de pagina-URL voor een pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="69ed4-130">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="69ed4-131">Selecteer **Nieuw** op de pagina **URL's**.</span><span class="sxs-lookup"><span data-stu-id="69ed4-131">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="69ed4-132">Selecteer de sitepagina waaraan de URL moet worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="69ed4-132">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="69ed4-133">Voer de URL-slug in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="69ed4-133">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="69ed4-134">Op dit moment bevindt de URL zich in een conceptstatus.</span><span class="sxs-lookup"><span data-stu-id="69ed4-134">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="69ed4-135">De URL moet worden gepubliceerd voordat de sitegebruikers toegang kunnen krijgen tot de bijbehorende pagina.</span><span class="sxs-lookup"><span data-stu-id="69ed4-135">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="69ed4-136">Een pagina-URL bijwerken</span><span class="sxs-lookup"><span data-stu-id="69ed4-136">Update a page URL</span></span>

<span data-ttu-id="69ed4-137">Voer de volgende stappen uit om de doelpagina van een pagina-URL bij te werken.</span><span class="sxs-lookup"><span data-stu-id="69ed4-137">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="69ed4-138">Selecteer op de pagina **URL's** de URL die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="69ed4-138">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="69ed4-139">Selecteer in het eigenschappenvenster aan de rechterkant de knop met het weglatingsteken (**...**) naast het veld van de doelpagina.</span><span class="sxs-lookup"><span data-stu-id="69ed4-139">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="69ed4-140">Selecteer in het dialoogvenster een andere pagina en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="69ed4-140">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="69ed4-141">Sla de URL op en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="69ed4-141">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="69ed4-142">Omleiding instellen voor een pagina-URL</span><span class="sxs-lookup"><span data-stu-id="69ed4-142">Redirect a page URL</span></span>

<span data-ttu-id="69ed4-143">Soms wilt u dat uw klanten een andere pagina zien wanneer ze een specifieke URL opvragen.</span><span class="sxs-lookup"><span data-stu-id="69ed4-143">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="69ed4-144">In deze gevallen is de beste en eenvoudigste methode vaak de pagina te wijzigen waarnaar de URL van de pagina verwijst.</span><span class="sxs-lookup"><span data-stu-id="69ed4-144">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="69ed4-145">U kunt echter goede redenen hebben voor het gebruik van HTTP 301- of 3023-omleidingen om aanvragen voor een URL om te leiden naar een andere URL.</span><span class="sxs-lookup"><span data-stu-id="69ed4-145">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="69ed4-146">Voer de volgende stappen uit om een URL om te leiden naar een andere URL.</span><span class="sxs-lookup"><span data-stu-id="69ed4-146">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="69ed4-147">Selecteer op de pagina **URL's** de URL die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="69ed4-147">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="69ed4-148">Selecteer in het eigenschappenvenster aan de rechterkant de optie **Omleiden**.</span><span class="sxs-lookup"><span data-stu-id="69ed4-148">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="69ed4-149">Selecteer een bestemming voor de omleiding:</span><span class="sxs-lookup"><span data-stu-id="69ed4-149">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="69ed4-150">Als u naar een andere pagina op uw site wilt verwijzen, selecteert u **Interne URL**, de knop met het weglatingsteken (**...**) en vervolgens de URL waarnaar u wilt omleiden.</span><span class="sxs-lookup"><span data-stu-id="69ed4-150">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="69ed4-151">Als u naar een pagina op een externe site wilt verwijzen, selecteert u **Externe URL** en voert u vervolgens de volledige URL voor die pagina in.</span><span class="sxs-lookup"><span data-stu-id="69ed4-151">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="69ed4-152">Zorg ervoor dat u het protocol opneemt.</span><span class="sxs-lookup"><span data-stu-id="69ed4-152">Be sure to include the protocol.</span></span> <span data-ttu-id="69ed4-153">Voer bijvoorbeeld `https://domain.com/new/page` in.</span><span class="sxs-lookup"><span data-stu-id="69ed4-153">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="69ed4-154">Als de URL al omleidt naar een interne URL, moet u **Selectie wissen** selecteren voordat u een externe URL kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="69ed4-154">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="69ed4-155">Selecteer een omleidingstype:</span><span class="sxs-lookup"><span data-stu-id="69ed4-155">Select a redirect type:</span></span>

    - <span data-ttu-id="69ed4-156">**Permanente omleiding (301)**: selecteer deze optie wanneer u weet dat de inhoud permanent wordt verplaatst en de vorige URL niet wordt hersteld.</span><span class="sxs-lookup"><span data-stu-id="69ed4-156">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="69ed4-157">In zoekmachines wordt de SEO-waarde (Search Engine Optimization) van de omgeleide URL toegewezen aan de URL waarnaar wordt omgeleid. Ook wordt de record bijgewerkt om de nieuwe URL weer te geven.</span><span class="sxs-lookup"><span data-stu-id="69ed4-157">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="69ed4-158">**Tijdelijke omleiding (302)**: selecteer deze optie om verkeer om te leiden zonder de zoekmachines bij te werken.</span><span class="sxs-lookup"><span data-stu-id="69ed4-158">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="69ed4-159">Deze benadering wordt meestal gebruikt als de inhoud binnenkort teruggaat naar de vorige URL.</span><span class="sxs-lookup"><span data-stu-id="69ed4-159">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="69ed4-160">Wanneer u klaar bent om de omleiding uit te voeren, moet u de URL opslaan en publiceren.</span><span class="sxs-lookup"><span data-stu-id="69ed4-160">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69ed4-161">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="69ed4-161">Additional resources</span></span>

[<span data-ttu-id="69ed4-162">Sitenavigatie aanpassen</span><span class="sxs-lookup"><span data-stu-id="69ed4-162">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="69ed4-163">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="69ed4-163">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="69ed4-164">Uw domeinnaam configureren</span><span class="sxs-lookup"><span data-stu-id="69ed4-164">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="69ed4-165">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="69ed4-165">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
