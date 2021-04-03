---
title: Siteselectiemodule
description: In dit onderwerp wordt beschreven wat de siteselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e24590d4a8f172809704aab0d761f6db0fb0e11b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234336"
---
# <a name="site-selector-module"></a><span data-ttu-id="0c808-103">Siteselectiemodule</span><span class="sxs-lookup"><span data-stu-id="0c808-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c808-104">In dit onderwerp wordt beschreven wat de siteselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0c808-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0c808-105">Wanneer een bedrijf verschillende sites heeft voor verschillende markten, regio's en landen, hebben sitegebruikers een eenvoudige manier nodig om tussen sites te schakelen en hun favoriete winkelsite te selecteren.</span><span class="sxs-lookup"><span data-stu-id="0c808-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="0c808-106">Voor dit scenario kunnen gebruikers met de siteselectiemodule bladeren door meerdere sites.</span><span class="sxs-lookup"><span data-stu-id="0c808-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="0c808-107">De siteselectiemodule moet worden geconfigureerd met de lijst met sites (markten, regio's of landinstellingen) waarin sitegebruikers kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="0c808-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="0c808-108">De siteselectiemodule is beschikbaar in Dynamics 365 Commerce versie 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="0c808-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="0c808-109">In de volgende afbeelding ziet u een voorbeeld van een siteselectiemodule die wordt weergegeven in de koptekst van een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="0c808-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Voorbeeld van een siteselectiemodule in de koptekst van een sitepagina](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="0c808-111">Eigenschappen van siteselectiemodule</span><span class="sxs-lookup"><span data-stu-id="0c808-111">Site selector module properties</span></span>

| <span data-ttu-id="0c808-112">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="0c808-112">Property name</span></span> | <span data-ttu-id="0c808-113">Waarde</span><span class="sxs-lookup"><span data-stu-id="0c808-113">Value</span></span>                 | <span data-ttu-id="0c808-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0c808-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="0c808-115">Kop</span><span class="sxs-lookup"><span data-stu-id="0c808-115">Heading</span></span>       | <span data-ttu-id="0c808-116">Tekst</span><span class="sxs-lookup"><span data-stu-id="0c808-116">Text</span></span>                  | <span data-ttu-id="0c808-117">De koptekst voor de module.</span><span class="sxs-lookup"><span data-stu-id="0c808-117">The heading for the module.</span></span> |
| <span data-ttu-id="0c808-118">Siteopties</span><span class="sxs-lookup"><span data-stu-id="0c808-118">Site options</span></span>  | <span data-ttu-id="0c808-119">Naam, afbeelding, URL</span><span class="sxs-lookup"><span data-stu-id="0c808-119">Name, Image, URL</span></span>      | <span data-ttu-id="0c808-120">Met deze eigenschap worden een naam, een koppeling naar de startpagina van de site en een optionele afbeelding opgegeven voor elke site die in de module is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="0c808-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="0c808-121">De afbeelding kan een vlag zijn of een bepaalde voorstelling van een markt, regio of landinstelling.</span><span class="sxs-lookup"><span data-stu-id="0c808-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="0c808-122">Een siteselectiemodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="0c808-122">Add a site selector module to a page</span></span>

<span data-ttu-id="0c808-123">De siteselectiemodule kan aan de [Koptekstmodule](author-header-module.md) onder de sleuf van de siteselectie worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="0c808-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="0c808-124">Nadat deze is toegevoegd, kunt u de modulekop en de siteopties definiëren.</span><span class="sxs-lookup"><span data-stu-id="0c808-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c808-125">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0c808-125">Additional resources</span></span>

[<span data-ttu-id="0c808-126">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="0c808-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0c808-127">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="0c808-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0c808-128">Breadcrumb-module</span><span class="sxs-lookup"><span data-stu-id="0c808-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="0c808-129">Navigatiemenumodule</span><span class="sxs-lookup"><span data-stu-id="0c808-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]