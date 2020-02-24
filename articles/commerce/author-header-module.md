---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: efadd19681bbb21ea5b2b469e55bc6f4b0535046
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025649"
---
# <a name="header-module"></a><span data-ttu-id="290a9-103">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="290a9-104">In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="290a9-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="290a9-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="290a9-105">Overview</span></span>

<span data-ttu-id="290a9-106">In Dynamics 365 Commerce bestaat een paginakoptekst uit meerdere modules, zoals modules voor de koptekst, het navigatiemenu, zoeken, promotiebanner en cookietoestemming.</span><span class="sxs-lookup"><span data-stu-id="290a9-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="290a9-107">De koptekstmodule bevat een sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site, een winkelwagensymbool, een verlanglijstsymbool, aanmeldingsopties en de zoekbalk.</span><span class="sxs-lookup"><span data-stu-id="290a9-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="290a9-108">Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (met andere woorden, voor een desktopapparaat of een mobiel apparaat).</span><span class="sxs-lookup"><span data-stu-id="290a9-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="290a9-109">Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).</span><span class="sxs-lookup"><span data-stu-id="290a9-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="290a9-110">Eigenschappen van een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-110">Properties of a header module</span></span>

<span data-ttu-id="290a9-111">Een koptekstmodule ondersteunt de eigenschappen **Logoafbeelding**, **Logokoppeling** en **Mijn account-koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="290a9-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="290a9-112">De eigenschappen **Logoafbeelding** en **Logokoppeling** worden gebruikt om een logo op de pagina te definiëren.</span><span class="sxs-lookup"><span data-stu-id="290a9-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="290a9-113">Zie voor meer informatie [Een logo toevoegen](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="290a9-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="290a9-114">De eigenschap **Mijn accounts-koppeling** kan worden gebruikt om accountpagina's te definiëren waarop de site-eigenaar snelkoppelingen wil weergeven in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="290a9-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="290a9-115">Modules die beschikbaar zijn in een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-115">Modules that are available in a header module</span></span>

<span data-ttu-id="290a9-116">De volgende modules kunnen in een koptekstmodule worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="290a9-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="290a9-117">**Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen.</span><span class="sxs-lookup"><span data-stu-id="290a9-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="290a9-118">De navigatiehiërarchie voor het afzetkanaal kan worden geconfigureerd in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="290a9-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="290a9-119">Het navigatiemenu heeft een eigenschap **Navigatiebron** die wordt gebruikt om menuopdrachten voor Retail Server-navigatie en statische menu-opdrachten op te geven als een bron.</span><span class="sxs-lookup"><span data-stu-id="290a9-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="290a9-120">Als statische menu-items als bron zijn opgegeven, kunnen er relatieve koppelingen naar andere pagina's op de site worden gegeven.</span><span class="sxs-lookup"><span data-stu-id="290a9-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="290a9-121">Geconfigureerde artikelen worden vervolgens weergegeven als koptekstnavigatie.</span><span class="sxs-lookup"><span data-stu-id="290a9-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="290a9-122">**Zoeken** : met de zoekbalkmodule kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken.</span><span class="sxs-lookup"><span data-stu-id="290a9-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="290a9-123">De URL van de standaardzoekpagina en de zoekqueryparameters moeten worden opgegeven via **Site-instellingen \> Extensies**.</span><span class="sxs-lookup"><span data-stu-id="290a9-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="290a9-124">De zoekmodule bevat eigenschappen waarmee u de zoekknop of het zoeklabel kunt onderdrukken zoals u dat nodig acht.</span><span class="sxs-lookup"><span data-stu-id="290a9-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="290a9-125">De zoekmodule ondersteunt ook opties voor automatisch suggesties, zoals zoekresultaten voor product, trefwoord en categorie.</span><span class="sxs-lookup"><span data-stu-id="290a9-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="290a9-126">Een koptekstmodule maken voor een pagina</span><span class="sxs-lookup"><span data-stu-id="290a9-126">Create a header module for a page</span></span>

<span data-ttu-id="290a9-127">Volg deze stappen om een koptekstmodule te maken.</span><span class="sxs-lookup"><span data-stu-id="290a9-127">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="290a9-128">Maak een fragment met de naam **Koptekstfragment** en voeg hieraan een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="290a9-128">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="290a9-129">Stel in het eigenschappenvenster voor de containermodule de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="290a9-129">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="290a9-130">Voeg promobannermodules en cookietoestemmingsmodules toe aan de containermodule.</span><span class="sxs-lookup"><span data-stu-id="290a9-130">Add promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="290a9-131">Voeg nog een containermodule toe aan het fragment en stel de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="290a9-131">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="290a9-132">Voeg een koptekstmodule toe aan de tweede containermodule.</span><span class="sxs-lookup"><span data-stu-id="290a9-132">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="290a9-133">Voeg in de **Navigatiemenu**sleuf van de koptekstmodule een navigatiemenumodule toe.</span><span class="sxs-lookup"><span data-stu-id="290a9-133">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="290a9-134">Configureer de eigenschappen van de navigatiemenumodule in het eigenschappenvenster van de navigatiemenumodule.</span><span class="sxs-lookup"><span data-stu-id="290a9-134">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="290a9-135">Voeg in de sleuf **Zoeken** van de koptekstmodule een zoekmodule toe.</span><span class="sxs-lookup"><span data-stu-id="290a9-135">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="290a9-136">Configureer de eigenschappen van de zoekmodule in het eigenschappenvenster van de zoekmodule.</span><span class="sxs-lookup"><span data-stu-id="290a9-136">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="290a9-137">Sla het paginafragment op, voltooi de bewerking ervan en publiceer het fragment.</span><span class="sxs-lookup"><span data-stu-id="290a9-137">Save the page fragment, finish editing it, and publish it.</span></span> 

<span data-ttu-id="290a9-138">Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="290a9-138">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="290a9-139">Voeg in de **Hoofd**sleuf van de standaardpagina het koptekstpaginafragment met de koptekstmodule toe aan de koptekst.</span><span class="sxs-lookup"><span data-stu-id="290a9-139">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="290a9-140">Sla de sjabloon op, voltooi de bewerking ervan en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="290a9-140">Save the template, finish editing it, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="290a9-141">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="290a9-141">Additional resources</span></span>

[<span data-ttu-id="290a9-142">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="290a9-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="290a9-143">Module Container</span><span class="sxs-lookup"><span data-stu-id="290a9-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="290a9-144">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="290a9-145">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="290a9-146">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="290a9-147">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-147">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="290a9-148">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-148">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="290a9-149">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="290a9-149">Footer module</span></span>](author-footer-module.md)
