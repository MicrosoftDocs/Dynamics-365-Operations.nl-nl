---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411196"
---
# <a name="header-module"></a><span data-ttu-id="a4c67-103">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a4c67-104">In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a4c67-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a4c67-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="a4c67-105">Overview</span></span>

<span data-ttu-id="a4c67-106">In Dynamics 365 Commerce bestaat een paginakoptekst uit meerdere modules, zoals modules voor de koptekst, het navigatiemenu, zoeken, promotiebanner en cookietoestemming.</span><span class="sxs-lookup"><span data-stu-id="a4c67-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="a4c67-107">De koptekstmodule bevat een sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site, een winkelwagensymbool, een verlanglijstsymbool, aanmeldingsopties en de zoekbalk.</span><span class="sxs-lookup"><span data-stu-id="a4c67-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="a4c67-108">Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (met andere woorden, voor een desktopapparaat of een mobiel apparaat).</span><span class="sxs-lookup"><span data-stu-id="a4c67-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="a4c67-109">Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).</span><span class="sxs-lookup"><span data-stu-id="a4c67-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="a4c67-110">De volgende afbeelding toont een voorbeeld van een koptekstmodule op een introductiepagina.</span><span class="sxs-lookup"><span data-stu-id="a4c67-110">The following image shows an example of a header module on a home page.</span></span>

![Voorbeeld van een koptekstmodule](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="a4c67-112">Eigenschappen van een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-112">Properties of a header module</span></span>

<span data-ttu-id="a4c67-113">Een koptekstmodule ondersteunt de eigenschappen **Logoafbeelding**, **Logokoppeling** en **Mijn account-koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="a4c67-114">De eigenschappen **Logoafbeelding** en **Logokoppeling** worden gebruikt om een logo op de pagina te definiëren.</span><span class="sxs-lookup"><span data-stu-id="a4c67-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="a4c67-115">Zie voor meer informatie [Een logo toevoegen](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="a4c67-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="a4c67-116">De eigenschap **Mijn accounts-koppeling** kan worden gebruikt om accountpagina's te definiëren waarop de site-eigenaar snelkoppelingen wil weergeven in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="a4c67-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="a4c67-117">Modules die beschikbaar zijn in een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-117">Modules that are available in a header module</span></span>

<span data-ttu-id="a4c67-118">De volgende modules kunnen in een koptekstmodule worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="a4c67-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="a4c67-119">**Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen.</span><span class="sxs-lookup"><span data-stu-id="a4c67-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="a4c67-120">De navigatiehiërarchie voor het afzetkanaal kan worden geconfigureerd in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a4c67-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a4c67-121">Het navigatiemenu heeft een eigenschap **Navigatiebron** die wordt gebruikt om menuopdrachten voor Retail Server-navigatie en statische menu-opdrachten op te geven als een bron.</span><span class="sxs-lookup"><span data-stu-id="a4c67-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="a4c67-122">Als statische menu-items als bron zijn opgegeven, kunnen er relatieve koppelingen naar andere pagina's op de site worden gegeven.</span><span class="sxs-lookup"><span data-stu-id="a4c67-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="a4c67-123">Geconfigureerde artikelen worden vervolgens weergegeven als koptekstnavigatie.</span><span class="sxs-lookup"><span data-stu-id="a4c67-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="a4c67-124">**Zoeken** : met de zoekbalkmodule kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken.</span><span class="sxs-lookup"><span data-stu-id="a4c67-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="a4c67-125">De URL van de standaardzoekpagina en de zoekqueryparameters moeten worden opgegeven via **Site-instellingen \> Extensies**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="a4c67-126">De zoekmodule bevat eigenschappen waarmee u de zoekknop of het zoeklabel kunt onderdrukken zoals u dat nodig acht.</span><span class="sxs-lookup"><span data-stu-id="a4c67-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="a4c67-127">De zoekmodule ondersteunt ook opties voor automatisch suggesties, zoals zoekresultaten voor product, trefwoord en categorie.</span><span class="sxs-lookup"><span data-stu-id="a4c67-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="a4c67-128">**Pictogram winkelwagen**: de module winkelwagenpictogram vertegenwoordigt dat het aantal artikelen in de winkelwagen op een bepaald moment weergeeft.</span><span class="sxs-lookup"><span data-stu-id="a4c67-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="a4c67-129">Zie [Module winkelwagenpictogram](cart-icon-module.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="a4c67-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="a4c67-130">Een koptekstmodule maken voor een pagina</span><span class="sxs-lookup"><span data-stu-id="a4c67-130">Create a header module for a page</span></span>

<span data-ttu-id="a4c67-131">Volg deze stappen om een koptekstmodule te maken.</span><span class="sxs-lookup"><span data-stu-id="a4c67-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="a4c67-132">Ga naar **Paginafragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="a4c67-132">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="a4c67-133">Selecteer in het dialoogvenster **Nieuw paginafragment** de module **Container**, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-133">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="a4c67-134">Selecteer het vak **Standaardcontainer** en stel vervolgens in het deelvenster Eigenschappen rechts de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="a4c67-135">Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a4c67-136">Selecteer in het dialoogvenster **Module toevoegen** de modules **Promotiebanner** en **Cookietoestemming** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="a4c67-137">Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a4c67-138">Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a4c67-139">Selecteer het vak **Container** en stel vervolgens in het deelvenster Eigenschappen rechts de eigenschap **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="a4c67-140">Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a4c67-141">Selecteer in het dialoogvenster **Module toevoegen** de **Koptekstmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a4c67-142">Selecteer in het vak **Navigatiemenu** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a4c67-143">Selecteer in het dialoogvenster **Module toevoegen** de module **Navigatiemenu** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a4c67-144">Configureer desgewenst de eigenschappen van de navigatiemenumodule in het eigenschappenvenster.</span><span class="sxs-lookup"><span data-stu-id="a4c67-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="a4c67-145">Selecteer in het vak **Zoeken** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a4c67-146">Selecteer in het dialoogvenster **Module toevoegen** de module **Zoeken** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a4c67-147">Configureer desgewenst de eigenschappen van de zoekmodule in het eigenschappenvenster.</span><span class="sxs-lookup"><span data-stu-id="a4c67-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="a4c67-148">Selecteer in het vak **Winkelwagenpictogram** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a4c67-149">Selecteer in het dialoogvenster **Module toevoegen** de module **Winkelwagenpictogram** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a4c67-150">Configureer desgewenst de eigenschappen van de module Winkelwagenpictogram in het eigenschappenvenster.</span><span class="sxs-lookup"><span data-stu-id="a4c67-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="a4c67-151">Als u wilt dat het winkelwagenpictogram een overzicht van de winkelwagen toont (ook wel een minikar genoemd), wanneer gebruikers de muis erboven houden, selecteert u **Minikar tonen**.</span><span class="sxs-lookup"><span data-stu-id="a4c67-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="a4c67-152">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.</span><span class="sxs-lookup"><span data-stu-id="a4c67-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="a4c67-153">Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a4c67-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="a4c67-154">Voeg in het vak **Koptekst** van de module **Standaardpagina** in de voettekstmodule het voettekstfragment toe dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a4c67-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="a4c67-155">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="a4c67-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a4c67-156">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="a4c67-156">Additional resources</span></span>

[<span data-ttu-id="a4c67-157">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="a4c67-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a4c67-158">Containermodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a4c67-159">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="a4c67-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a4c67-160">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a4c67-161">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="a4c67-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a4c67-162">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a4c67-163">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a4c67-164">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a4c67-165">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="a4c67-165">Footer module</span></span>](author-footer-module.md)
