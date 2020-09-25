---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: eb440a8fb67888c9411ad5998fead4d00982b436
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761219"
---
# <a name="header-module"></a><span data-ttu-id="59438-103">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="59438-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="59438-104">In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u paginakopteksten maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="59438-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="59438-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="59438-105">Overview</span></span>

<span data-ttu-id="59438-106">In Dynamics 365 Commerce wordt een paginakoptekst geconfigureerd als een paginafragment dat de modules voor koptekst, promotiebanner en cookietoestemming bevat.</span><span class="sxs-lookup"><span data-stu-id="59438-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="59438-107">De koptekstmodule bevat een sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site, een winkelwagenpictogrammodule, een verlanglijstsymbool, aanmeldingsopties en de zoekbalk.</span><span class="sxs-lookup"><span data-stu-id="59438-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="59438-108">Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (met andere woorden, voor een desktopapparaat of een mobiel apparaat).</span><span class="sxs-lookup"><span data-stu-id="59438-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="59438-109">Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).</span><span class="sxs-lookup"><span data-stu-id="59438-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="59438-110">De volgende afbeelding toont een voorbeeld van een koptekstmodule op een introductiepagina.</span><span class="sxs-lookup"><span data-stu-id="59438-110">The following image shows an example of a header module on a home page.</span></span>

![Voorbeeld van een koptekstmodule](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="59438-112">Eigenschappen van een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="59438-112">Properties of a header module</span></span>

<span data-ttu-id="59438-113">Een koptekstmodule ondersteunt de eigenschappen **Logoafbeelding**, **Logokoppeling** en **Mijn account-koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="59438-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="59438-114">De eigenschappen **Logoafbeelding** en **Logokoppeling** worden gebruikt om een logo op de pagina te definiëren.</span><span class="sxs-lookup"><span data-stu-id="59438-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="59438-115">Zie voor meer informatie [Een logo toevoegen](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="59438-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="59438-116">De eigenschap **Mijn accounts-koppeling** kan worden gebruikt om accountpagina's te definiëren waarop de site-eigenaar snelkoppelingen wil weergeven in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="59438-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="59438-117">Modules die beschikbaar zijn in een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="59438-117">Modules that are available within a header module</span></span>

<span data-ttu-id="59438-118">De volgende modules kunnen in een koptekstmodule worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="59438-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="59438-119">**Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen.</span><span class="sxs-lookup"><span data-stu-id="59438-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="59438-120">Zie [Navigatiemenumodule](nav-menu-module.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="59438-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="59438-121">**Zoeken** : met de zoekbalkmodule kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken.</span><span class="sxs-lookup"><span data-stu-id="59438-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="59438-122">De URL van de standaardzoekpagina en de zoekqueryparameters moeten worden opgegeven via **Site-instellingen \> Extensies**.</span><span class="sxs-lookup"><span data-stu-id="59438-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="59438-123">De zoekmodule bevat eigenschappen waarmee u de zoekknop of het zoeklabel kunt onderdrukken zoals u dat nodig acht.</span><span class="sxs-lookup"><span data-stu-id="59438-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="59438-124">De zoekmodule ondersteunt ook opties voor automatisch suggesties, zoals zoekresultaten voor product, trefwoord en categorie.</span><span class="sxs-lookup"><span data-stu-id="59438-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="59438-125">**Pictogram winkelwagen**: de module winkelwagenpictogram vertegenwoordigt dat het aantal artikelen in de winkelwagen op een bepaald moment weergeeft.</span><span class="sxs-lookup"><span data-stu-id="59438-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="59438-126">Zie [Module winkelwagenpictogram](cart-icon-module.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="59438-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="59438-127">Een koptekstfragment maken voor een pagina</span><span class="sxs-lookup"><span data-stu-id="59438-127">Create a header fragment for a page</span></span>

<span data-ttu-id="59438-128">Volg deze stappen om een koptekstfragment te maken.</span><span class="sxs-lookup"><span data-stu-id="59438-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="59438-129">Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="59438-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="59438-130">Selecteer in het dialoogvenster **Nieuw fragment** de module **Container**, voer een naam in voor het fragment en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="59438-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="59438-131">Selecteer het vak **Standaardcontainer** en stel vervolgens in het deelvenster Eigenschappen rechts de eigenschap **Breedte** in op **Scherm vullen**.</span><span class="sxs-lookup"><span data-stu-id="59438-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="59438-132">Selecteer het weglatingsteken (**...**) in het vak **Standaardcontainer** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="59438-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="59438-133">Selecteer in het dialoogvenster **Module toevoegen** de modules **Cookietoestemming**, **Koptekst** en **Promotiebanner** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="59438-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="59438-134">Selecteer **Bericht toevoegen** in het deelvenster Eigenschappen van de module **Promotiebanner** en selecteer vervolgens **Bericht**.</span><span class="sxs-lookup"><span data-stu-id="59438-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="59438-135">Voeg in het dialoogvenster **Bericht** tekst en koppelingen voor de promotie-inhoud toe en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="59438-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="59438-136">Voeg in het deelvenster Eigenschappen van de module **Cookietoestemming** tekst en een koppeling naar de privacypagina van de site toe en configureer deze.</span><span class="sxs-lookup"><span data-stu-id="59438-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="59438-137">Selecteer in het vak **Navigatiemenu** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="59438-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="59438-138">Selecteer in het dialoogvenster **Module toevoegen** de module **Navigatiemenu** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="59438-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="59438-139">Selecteer in het deelvenster Eigenschappen voor de navigatiemenumodule de optie **Detailhandelserver** onder **Bron voor navigatiemenu**.</span><span class="sxs-lookup"><span data-stu-id="59438-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="59438-140">Selecteer in het deelvenster Eigenschappen voor de navigatiemenumodule onder **Statische menuopdrachten** de optie **Menuopdracht toevoegen** en **Menuopdracht**.</span><span class="sxs-lookup"><span data-stu-id="59438-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="59438-141">Typ in het dialoogvenster **Menuopdracht** onder **Tekst van menuopdracht** de tekst Contact.</span><span class="sxs-lookup"><span data-stu-id="59438-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="59438-142">Selecteer in het dialoogvenster **Menuopdracht** onder **Koppelingsdoel menuopdracht** de optie **Een koppeling toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="59438-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="59438-143">Selecteer in het dialoogvenster **Een koppeling toevoegen** de URL voor de pagina Contact van de site en selecteer vervolgens **OK.**</span><span class="sxs-lookup"><span data-stu-id="59438-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="59438-144">Selecteer **OK** in het dialoogvenster **Menuopdracht**.</span><span class="sxs-lookup"><span data-stu-id="59438-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="59438-145">Selecteer in het vak **Zoeken** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="59438-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="59438-146">Selecteer in het dialoogvenster **Module toevoegen** de module **Zoeken** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="59438-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="59438-147">Configureer desgewenst de eigenschappen van de zoekmodule in het eigenschappenvenster.</span><span class="sxs-lookup"><span data-stu-id="59438-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="59438-148">Selecteer in het vak **Winkelwagenpictogram** van de koptekstmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="59438-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="59438-149">Selecteer in het dialoogvenster **Module toevoegen** de module **Winkelwagenpictogram** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="59438-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="59438-150">Configureer desgewenst de eigenschappen van de module Winkelwagenpictogram in het eigenschappenvenster.</span><span class="sxs-lookup"><span data-stu-id="59438-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="59438-151">Als u wilt dat het winkelwagenpictogram een overzicht van de winkelwagen toont (ook wel een minikar genoemd), wanneer gebruikers de muis erboven houden, selecteert u **Minikar tonen**.</span><span class="sxs-lookup"><span data-stu-id="59438-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="59438-152">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.</span><span class="sxs-lookup"><span data-stu-id="59438-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="59438-153">Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="59438-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="59438-154">Voeg in het vak **Koptekst** van de module **Standaardpagina** in de voettekstmodule het voettekstfragment toe dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="59438-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="59438-155">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="59438-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59438-156">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="59438-156">Additional resources</span></span>

[<span data-ttu-id="59438-157">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="59438-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="59438-158">Containermodule</span><span class="sxs-lookup"><span data-stu-id="59438-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="59438-159">Module voor winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="59438-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="59438-160">Promotiebanner-module</span><span class="sxs-lookup"><span data-stu-id="59438-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="59438-161">Navigatiemenumodule</span><span class="sxs-lookup"><span data-stu-id="59438-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="59438-162">Toestemming voor cookies</span><span class="sxs-lookup"><span data-stu-id="59438-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="59438-163">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="59438-163">Footer module</span></span>](author-footer-module.md)
