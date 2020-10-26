---
title: Overwegingen bij SEO (Search Engine Optimization) voor uw site
description: In dit onderwerp komen overwegingen aan de orde voor uw site over SEO (Search Engine Optimization), van ontwikkeling tot productie.
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
ms.openlocfilehash: 6ffc772addb330abe7205007662a3f3e08a3e47f
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961581"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="cef6b-103">Overwegingen bij SEO (Search Engine Optimization) voor uw site</span><span class="sxs-lookup"><span data-stu-id="cef6b-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cef6b-104">In dit onderwerp komen overwegingen aan de orde voor uw site over SEO (Search Engine Optimization), van ontwikkeling tot productie.</span><span class="sxs-lookup"><span data-stu-id="cef6b-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="cef6b-105">Een site die wordt ontwikkeld</span><span class="sxs-lookup"><span data-stu-id="cef6b-105">A site that is under development</span></span>

<span data-ttu-id="cef6b-106">Terwijl een site in ontwikkeling is, moeten alle site pagina's de metatags **NOINDEX** en **NOFOLLOW** hebben, zodat zoekmachines de pagina's niet indexeren en ontwikkelingsversies van uw site in hun cache opslaan.</span><span class="sxs-lookup"><span data-stu-id="cef6b-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="cef6b-107">Als u deze configuratie wilt uitvoeren, moet u de standaardmodule met metatags aan de paginasjabloon voor de site toevoegen.</span><span class="sxs-lookup"><span data-stu-id="cef6b-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="cef6b-108">De standaardeigenschappen voor metatags zijn dan beschikbaar in het gedeelte SEO-eigenschappen van de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="cef6b-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="cef6b-109">U kunt deze eigenschappen gebruiken om de metatags te beheren.</span><span class="sxs-lookup"><span data-stu-id="cef6b-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="cef6b-110">Een zachte start voor een site</span><span class="sxs-lookup"><span data-stu-id="cef6b-110">Soft launch of a site</span></span>

<span data-ttu-id="cef6b-111">Tijdens een "zachte start" wordt een website beschikbaar gemaakt voor een beperkt publiek of een beperkte markt voordat de volledige start wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="cef6b-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="cef6b-112">Als u uw website zacht wilt starten, moet u overwegen om de metatags **NOINDEX** te laten staan.</span><span class="sxs-lookup"><span data-stu-id="cef6b-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="cef6b-113">Op deze manier zorgt u ervoor dat de zachte start beperkt blijft tot de beperkte doelgroep die u wilt bereiken.</span><span class="sxs-lookup"><span data-stu-id="cef6b-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="cef6b-114">Een site in productie</span><span class="sxs-lookup"><span data-stu-id="cef6b-114">A site that is in production</span></span>

<span data-ttu-id="cef6b-115">Wanneer een site in productie is, moet u controleren of alle sitepagina's juist zijn gelabeld.</span><span class="sxs-lookup"><span data-stu-id="cef6b-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="cef6b-116">Microsoft Dynamics 365 Commerce gebruikt de gegevens die voor een pagina zijn ingevoerd, om alle SEO-informatie op die pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="cef6b-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="cef6b-117">De volgende modules bieden deze functionaliteit: overzicht van de categoriepagina, samenvatting van de lijstpagina en overzicht van de productpagina.</span><span class="sxs-lookup"><span data-stu-id="cef6b-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="cef6b-118">Om de indexering van zoekmachines te optimaliseren, wordt bij de weergave zowel informatie uit de SEO-eigenschappen die zijn geconfigureerd in Dynamics 365 Commerce, als modulespecifieke informatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cef6b-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="cef6b-119">Voor een site die in productie is, moet u ervoor zorgen dat het bestand robots.txt de indexering van uw gehele site mogelijk maakt en dat het bestand koppelingen bevat naar het gepubliceerde document met het siteoverzicht.</span><span class="sxs-lookup"><span data-stu-id="cef6b-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="cef6b-120">U moet de functionaliteit voor het genereren van siteoverzichten inschakelen in **Site-instellingen \> Siteoverzichten ingeschakeld**.</span><span class="sxs-lookup"><span data-stu-id="cef6b-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="cef6b-121">SEO-instellingen voor een interne voorvertoning, beperkte doelgroepen en alle doelgroepen</span><span class="sxs-lookup"><span data-stu-id="cef6b-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="cef6b-122">Omdat Dynamics 365 Commerce ondersteuning biedt voor WYSIWYG-voorbeelden in visuele paginabouwer, kunnen ontwerpers de pagina-inhoud voorbereiden zonder dat de informatie zichtbaar wordt voor bezoekers van de site.</span><span class="sxs-lookup"><span data-stu-id="cef6b-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="cef6b-123">Als een pagina moet worden gepubliceerd voor een beperkte doelgroep, moet deze de metatag **NOINDEX** hebben, zodat de pagina niet door zoekmachines wordt geïndexeerd.</span><span class="sxs-lookup"><span data-stu-id="cef6b-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="cef6b-124">Wanneer de pagina vervolgens gereed is voor alle doelgroepen, moeten alle basis SEO-metagegevens aanwezig zijn om de efficiëntie van de indexering van de zoekmachine te optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="cef6b-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="cef6b-125">Bovendien moet de metatag **NOLIMIT** worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="cef6b-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cef6b-126">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="cef6b-126">Additional resources</span></span>

[<span data-ttu-id="cef6b-127">e-Commerce-gebruikers en -rollen beheren</span><span class="sxs-lookup"><span data-stu-id="cef6b-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="cef6b-128">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="cef6b-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="cef6b-129">Beveiligingsbeleid voor inhoud (CSP) beheren</span><span class="sxs-lookup"><span data-stu-id="cef6b-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
