---
title: Cookietoestemmingsmodule
description: In dit onderwerp wordt beschreven wat cookietoestemmingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2f0118b197f465113bb894e3e57b3e682e04ef36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795998"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="aa325-103">Module voor cookietoestemming</span><span class="sxs-lookup"><span data-stu-id="aa325-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aa325-104">In dit onderwerp wordt beschreven wat cookietoestemmingsmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aa325-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="aa325-105">In de cookietoestemmingsmodule wordt aan sitegebruikers gevraagd expliciet cookies toe te staan voor alle functies of modules die browsercookies bijhouden.</span><span class="sxs-lookup"><span data-stu-id="aa325-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="aa325-106">De toestemming is vereist wanneer een sitegebruiker de site voor het eerst bezoekt in een nieuwe browsersessie.</span><span class="sxs-lookup"><span data-stu-id="aa325-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="aa325-107">Wanneer toestemming wordt ontvangen, wordt deze getraceerd en wordt de sitegebruiker niet nogmaals om toestemming gevraagd.</span><span class="sxs-lookup"><span data-stu-id="aa325-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="aa325-108">Zie [Conformiteit van cookie](cookie-compliance.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="aa325-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="aa325-109">Als de cookietoestemming niet is ontvangen van de sitegebruiker, worden de functies of modules waarvoor cookietoestemming vereist is niet weergegeven op de pagina.</span><span class="sxs-lookup"><span data-stu-id="aa325-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="aa325-110">Voor de kassamodule, de module voor sociaal delen en de functie voor de voorkeurswinkel is bijvoorbeeld cookietoestemming vereist en deze worden niet weergegeven als de gebruiker geen toestemming heeft gekregen.</span><span class="sxs-lookup"><span data-stu-id="aa325-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="aa325-111">Een cookietoestemmingsmodule kan worden geconfigureerd in het koptekstfragment van een pagina, zodat deze kan worden afgedwongen wanneer de pagina wordt geladen.</span><span class="sxs-lookup"><span data-stu-id="aa325-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="aa325-112">De cookietoestemmingsmodule moet een duidelijk bericht bevatten waarin de sitegebruiker wordt geïnformeerd over het gebruik van cookies op de site en een koppeling naar de privacypagina van de site moet bieden.</span><span class="sxs-lookup"><span data-stu-id="aa325-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="aa325-113">In de volgende afbeelding ziet u een voorbeeld van een cookietoestemmingsbericht met een koppeling naar de pagina met het privacybeleid van de site in de koptekst van een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="aa325-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="aa325-114">![Voorbeeld van een cookietoestemmingsmodule](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="aa325-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="aa325-115">Eigenschappen van cookietoestemmingsmodule</span><span class="sxs-lookup"><span data-stu-id="aa325-115">Cookie consent module properties</span></span>

| <span data-ttu-id="aa325-116">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="aa325-116">Property name</span></span>             | <span data-ttu-id="aa325-117">Waarde</span><span class="sxs-lookup"><span data-stu-id="aa325-117">Value</span></span>                 | <span data-ttu-id="aa325-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="aa325-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="aa325-119">RTF</span><span class="sxs-lookup"><span data-stu-id="aa325-119">Rich Text</span></span>                  | <span data-ttu-id="aa325-120">RTF</span><span class="sxs-lookup"><span data-stu-id="aa325-120">Rich Text</span></span> | <span data-ttu-id="aa325-121">Hiermee geeft u een RTF-bericht op voor sitegebruikers dat de site gebruikmaakt van browsercookies en dat gebruikers het gebruik van cookies moeten accepteren om toegang te krijgen tot een volledig functionele site.</span><span class="sxs-lookup"><span data-stu-id="aa325-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="aa325-122">Koppelingen</span><span class="sxs-lookup"><span data-stu-id="aa325-122">Links</span></span> | <span data-ttu-id="aa325-123">URL</span><span class="sxs-lookup"><span data-stu-id="aa325-123">URL</span></span> | <span data-ttu-id="aa325-124">U kunt een of meer koppelingen toevoegen aan de privacypagina van een site die de typen cookies beschrijft die op de site worden bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="aa325-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="aa325-125">Een cookietoestemmingsmodule toevoegen aan sitepagina's</span><span class="sxs-lookup"><span data-stu-id="aa325-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="aa325-126">Als u een cookietoestemmingsmodule efficiënt wilt toevoegen aan meerdere sitepagina's, kan deze worden toegevoegd aan een koptekstfragment van een gedeelde pagina.</span><span class="sxs-lookup"><span data-stu-id="aa325-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="aa325-127">Als het koptekstfragment aan alle sitepagina's is toegevoegd, wordt automatisch een cookietoestemmingsmelding weergegeven wanneer een sitegebruiker voor het eerst naar sitepagina gaat.</span><span class="sxs-lookup"><span data-stu-id="aa325-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="aa325-128">Zie [Koptekstmodule](author-header-module.md) voor meer informatie over koptekstfragmenten en modules.</span><span class="sxs-lookup"><span data-stu-id="aa325-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa325-129">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="aa325-129">Additional resources</span></span>

[<span data-ttu-id="aa325-130">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="aa325-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aa325-131">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="aa325-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="aa325-132">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="aa325-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]