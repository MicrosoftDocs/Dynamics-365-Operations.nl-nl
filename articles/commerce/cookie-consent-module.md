---
title: Cookietoestemmingsmodule
description: In dit onderwerp wordt beschreven wat cookietoestemmingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817277"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="ea8c1-103">Cookietoestemmingsmodule</span><span class="sxs-lookup"><span data-stu-id="ea8c1-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea8c1-104">In dit onderwerp wordt beschreven wat cookietoestemmingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ea8c1-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="ea8c1-105">Overview</span></span>

<span data-ttu-id="ea8c1-106">In de cookietoestemmingsmodule wordt aan sitegebruikers gevraagd expliciet cookies toe te staan voor alle functies of modules die browsercookies bijhouden.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="ea8c1-107">De toestemming is vereist wanneer een sitegebruiker de site voor het eerst bezoekt in een nieuwe browsersessie.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="ea8c1-108">Wanneer toestemming wordt ontvangen, wordt deze getraceerd en wordt de sitegebruiker niet nogmaals om toestemming gevraagd.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="ea8c1-109">Zie [Conformiteit van cookie](cookie-compliance.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="ea8c1-110">Als de cookietoestemming niet is ontvangen van de sitegebruiker, worden de functies of modules waarvoor cookietoestemming vereist is niet weergegeven op de pagina.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="ea8c1-111">Voor de kassamodule, de module voor sociaal delen en de functie voor de voorkeurswinkel is bijvoorbeeld cookietoestemming vereist en deze worden niet weergegeven als de gebruiker geen toestemming heeft gekregen.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="ea8c1-112">Een cookietoestemmingsmodule kan worden geconfigureerd in het koptekstfragment van een pagina, zodat deze kan worden afgedwongen wanneer de pagina wordt geladen.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="ea8c1-113">De cookietoestemmingsmodule moet een duidelijk bericht bevatten waarin de sitegebruiker wordt geïnformeerd over het gebruik van cookies op de site en een koppeling naar de privacypagina van de site moet bieden.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="ea8c1-114">In de volgende afbeelding ziet u een voorbeeld van een cookietoestemmingsbericht met een koppeling naar de pagina met het privacybeleid van de site in de koptekst van een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="ea8c1-115">![Voorbeeld van een cookietoestemmingsmodule](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="ea8c1-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="ea8c1-116">Eigenschappen van cookietoestemmingsmodule</span><span class="sxs-lookup"><span data-stu-id="ea8c1-116">Cookie consent module properties</span></span>

| <span data-ttu-id="ea8c1-117">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-117">Property name</span></span>             | <span data-ttu-id="ea8c1-118">Waarde</span><span class="sxs-lookup"><span data-stu-id="ea8c1-118">Value</span></span>                 | <span data-ttu-id="ea8c1-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ea8c1-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="ea8c1-120">RTF</span><span class="sxs-lookup"><span data-stu-id="ea8c1-120">Rich Text</span></span>                  | <span data-ttu-id="ea8c1-121">RTF</span><span class="sxs-lookup"><span data-stu-id="ea8c1-121">Rich Text</span></span> | <span data-ttu-id="ea8c1-122">Hiermee geeft u een RTF-bericht op voor sitegebruikers dat de site gebruikmaakt van browsercookies en dat gebruikers het gebruik van cookies moeten accepteren om toegang te krijgen tot een volledig functionele site.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="ea8c1-123">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="ea8c1-123">Links</span></span> | <span data-ttu-id="ea8c1-124">URL</span><span class="sxs-lookup"><span data-stu-id="ea8c1-124">URL</span></span> | <span data-ttu-id="ea8c1-125">U kunt een of meer koppelingen toevoegen aan de privacypagina van een site die de typen cookies beschrijft die op de site worden bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="ea8c1-126">Een cookietoestemmingsmodule toevoegen aan sitepagina's</span><span class="sxs-lookup"><span data-stu-id="ea8c1-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="ea8c1-127">Als u een cookietoestemmingsmodule efficiënt wilt toevoegen aan meerdere sitepagina's, kan deze worden toegevoegd aan een koptekstfragment van een gedeelde pagina.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="ea8c1-128">Als het koptekstfragment aan alle sitepagina's is toegevoegd, wordt automatisch een cookietoestemmingsmelding weergegeven wanneer een sitegebruiker voor het eerst naar sitepagina gaat.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="ea8c1-129">Zie [Koptekstmodule](author-header-module.md) voor meer informatie over koptekstfragmenten en modules.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea8c1-130">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="ea8c1-130">Additional resources</span></span>

[<span data-ttu-id="ea8c1-131">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="ea8c1-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ea8c1-132">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="ea8c1-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="ea8c1-133">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="ea8c1-133">Cookie compliance</span></span>](cookie-compliance.md)