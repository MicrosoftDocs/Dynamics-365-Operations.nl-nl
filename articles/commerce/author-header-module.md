---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261439"
---
# <a name="header-module"></a><span data-ttu-id="2e787-103">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="2e787-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2e787-104">In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e787-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2e787-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="2e787-105">Overview</span></span>

<span data-ttu-id="2e787-106">In Dynamics 365 Commerce bestaat een paginakoptekst uit meerdere modules, zoals modules voor de koptekst, het navigatiemenu, zoeken, promotiebanner en cookietoestemming.</span><span class="sxs-lookup"><span data-stu-id="2e787-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="2e787-107">De koptekstmodule bevat een sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site, een winkelwagensymbool, een verlanglijstsymbool, aanmeldingsopties en de zoekbalk.</span><span class="sxs-lookup"><span data-stu-id="2e787-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="2e787-108">Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (met andere woorden, voor een desktopapparaat of een mobiel apparaat).</span><span class="sxs-lookup"><span data-stu-id="2e787-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="2e787-109">Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).</span><span class="sxs-lookup"><span data-stu-id="2e787-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="2e787-110">Eigenschappen van een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="2e787-110">Properties of a header module</span></span>

<span data-ttu-id="2e787-111">Een koptekstmodule ondersteunt de eigenschappen **Logoafbeelding**, **Logokoppeling** en **Mijn account-koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="2e787-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="2e787-112">De eigenschappen **Logoafbeelding** en **Logokoppeling** worden gebruikt om een logo op de pagina te definiëren.</span><span class="sxs-lookup"><span data-stu-id="2e787-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="2e787-113">Zie voor meer informatie [Een logo toevoegen](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="2e787-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="2e787-114">De eigenschap **Mijn accounts-koppeling** kan worden gebruikt om accountpagina's te definiëren waarop de site-eigenaar snelkoppelingen wil weergeven in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="2e787-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="2e787-115">Modules die beschikbaar zijn in een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="2e787-115">Modules that are available in a header module</span></span>

<span data-ttu-id="2e787-116">De volgende modules kunnen in een koptekstmodule worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="2e787-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="2e787-117">**Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen.</span><span class="sxs-lookup"><span data-stu-id="2e787-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="2e787-118">De navigatiehiërarchie voor het afzetkanaal kan worden geconfigureerd in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e787-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="2e787-119">Het navigatiemenu heeft een eigenschap **Navigatiebron** die wordt gebruikt om menuopdrachten voor Retail Server-navigatie en statische menu-opdrachten op te geven als een bron.</span><span class="sxs-lookup"><span data-stu-id="2e787-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="2e787-120">Als statische menu-items als bron zijn opgegeven, kunnen er relatieve koppelingen naar andere pagina's op de site worden gegeven.</span><span class="sxs-lookup"><span data-stu-id="2e787-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="2e787-121">Geconfigureerde artikelen worden vervolgens weergegeven als koptekstnavigatie.</span><span class="sxs-lookup"><span data-stu-id="2e787-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="2e787-122">**Zoeken** : met de zoekbalkmodule kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken.</span><span class="sxs-lookup"><span data-stu-id="2e787-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="2e787-123">De URL van de standaardzoekpagina en de zoekqueryparameters moeten worden opgegeven via **Site-instellingen \> Extensies**.</span><span class="sxs-lookup"><span data-stu-id="2e787-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="2e787-124">De zoekmodule bevat eigenschappen waarmee u de zoekknop of het zoeklabel kunt onderdrukken zoals u dat nodig acht.</span><span class="sxs-lookup"><span data-stu-id="2e787-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="2e787-125">De zoekmodule ondersteunt ook opties voor automatisch suggesties, zoals zoekresultaten voor product, trefwoord en categorie.</span><span class="sxs-lookup"><span data-stu-id="2e787-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="2e787-126">**Pictogram winkelwagen**: de module winkelwagenpictogram vertegenwoordigt dat het aantal artikelen in de winkelwagen op een bepaald moment weergeeft.</span><span class="sxs-lookup"><span data-stu-id="2e787-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="2e787-127">Zie [Module winkelwagenpictogram](cart-icon-module.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="2e787-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="2e787-128">Een koptekstmodule maken voor een pagina</span><span class="sxs-lookup"><span data-stu-id="2e787-128">Create a header module for a page</span></span>

<span data-ttu-id="2e787-129">Volg deze stappen om een koptekstmodule te maken.</span><span class="sxs-lookup"><span data-stu-id="2e787-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="2e787-130">Maak een fragment met de naam **Koptekstfragment** en voeg hieraan een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="2e787-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="2e787-131">Stel in het eigenschappenvenster voor de containermodule de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="2e787-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="2e787-132">Voeg een promobannermodules en cookietoestemmingsmodules toe aan de containermodule.</span><span class="sxs-lookup"><span data-stu-id="2e787-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="2e787-133">Voeg nog een containermodule toe aan het fragment en stel de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="2e787-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="2e787-134">Voeg een koptekstmodule toe aan de tweede containermodule.</span><span class="sxs-lookup"><span data-stu-id="2e787-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="2e787-135">Voeg in de **Navigatiemenu**sleuf van de koptekstmodule een navigatiemenumodule toe.</span><span class="sxs-lookup"><span data-stu-id="2e787-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="2e787-136">Configureer de eigenschappen van de navigatiemenumodule in het eigenschappenvenster van de navigatiemenumodule.</span><span class="sxs-lookup"><span data-stu-id="2e787-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="2e787-137">Voeg in de sleuf **Zoeken** van de koptekstmodule een zoekmodule toe.</span><span class="sxs-lookup"><span data-stu-id="2e787-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="2e787-138">Configureer de eigenschappen van de zoekmodule in het eigenschappenvenster van de zoekmodule.</span><span class="sxs-lookup"><span data-stu-id="2e787-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="2e787-139">Voeg in de sleuf **Winkelwagenpictogram** van de koptekstmodule een module winkelwagenpictogram toe.</span><span class="sxs-lookup"><span data-stu-id="2e787-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="2e787-140">Configureer de eigenschappen van de module winkelwagenpictogram in het eigenschappenvenster van de module winkelwagenpictogram.</span><span class="sxs-lookup"><span data-stu-id="2e787-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="2e787-141">Als u wilt dat het pictogram winkelwagen een minikarweergeeft wanneer de muis aanwijzer erop wordt geplaatst , selecteert u **Waar** voor **Minikar weergeven**.</span><span class="sxs-lookup"><span data-stu-id="2e787-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="2e787-142">Sla het paginafragment op, voltooi de bewerking en publiceer het fragment.</span><span class="sxs-lookup"><span data-stu-id="2e787-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="2e787-143">Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="2e787-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="2e787-144">Voeg in de **Hoofd**sleuf van de standaardpagina het koptekstpaginafragment met de koptekstmodule toe aan de koptekst.</span><span class="sxs-lookup"><span data-stu-id="2e787-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="2e787-145">Sla de sjabloon op, voltooi de bewerking en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="2e787-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e787-146">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="2e787-146">Additional resources</span></span>

[<span data-ttu-id="2e787-147">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="2e787-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2e787-148">Containermodule</span><span class="sxs-lookup"><span data-stu-id="2e787-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2e787-149">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="2e787-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2e787-150">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="2e787-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2e787-151">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="2e787-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="2e787-152">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="2e787-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2e787-153">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="2e787-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2e787-154">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="2e787-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2e787-155">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="2e787-155">Footer module</span></span>](author-footer-module.md)
