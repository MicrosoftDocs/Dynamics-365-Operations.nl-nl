---
title: Koptekstmodule
description: In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697270"
---
# <a name="header-module"></a><span data-ttu-id="3a1e8-103">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="3a1e8-103">Header module</span></span>

<span data-ttu-id="3a1e8-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="3a1e8-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="3a1e8-105">In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3a1e8-106">Overzicht</span><span class="sxs-lookup"><span data-stu-id="3a1e8-106">Overview</span></span>

<span data-ttu-id="3a1e8-107">Een koptekstmodule is een speciale container die wordt gebruikt om alle modules te hosten die worden weergegeven in de koptekst van een pagina.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="3a1e8-108">De module kan bijvoorbeeld uw sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site en de zoekbalk bevatten.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="3a1e8-109">Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (dat wil zeggen: een desktopapparaat of een mobiel apparaat).</span><span class="sxs-lookup"><span data-stu-id="3a1e8-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="3a1e8-110">Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).</span><span class="sxs-lookup"><span data-stu-id="3a1e8-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="3a1e8-111">Eigenschappen van een koptekst</span><span class="sxs-lookup"><span data-stu-id="3a1e8-111">Properties of a header</span></span>

<span data-ttu-id="3a1e8-112">Net als algemene containers ondersteunt een koptekstmodule de eigenschappen **kop** en **breedte**.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="3a1e8-113">Een koptekstmodule heeft meerdere vakken.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-113">A header module has multiple slots.</span></span> <span data-ttu-id="3a1e8-114">Er zijn bijvoorbeeld vakken voor informatiebericht, navigatiemenu, logo, zoekbalk, winkelwagenpictogram, verlanglijstpictogram en accountgegevens.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="3a1e8-115">Elk vak ondersteunt een specifieke set modules.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="3a1e8-116">Modules die beschikbaar zijn in een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="3a1e8-116">Modules that are available in a header module</span></span>

<span data-ttu-id="3a1e8-117">De volgende modules kunnen in een koptekstmodule worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="3a1e8-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="3a1e8-118">**Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="3a1e8-119">De navigatiehiërarchie voor het afzetkanaal kan worden geconfigureerd in Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="3a1e8-120">Geconfigureerde artikelen worden vervolgens weergegeven als koptekstnavigatie.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="3a1e8-121">Daarnaast kunnen statische navigatiekoppelingen worden geconfigureerd en kunnen relatieve koppelingen naar andere pagina's op de e-commerce-site worden aangeleverd.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="3a1e8-122">De koptekst zelf kan links, rechts of in het midden worden uitgelijnd.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="3a1e8-123">**Winkelwagenpictogram**: het winkelwagenpictogram is een speciaal pictogram dat de winkelwagen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="3a1e8-124">Het wordt weergegeven in de koptekst en geeft het aantal artikelen in de winkelwagen aan.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="3a1e8-125">Een koppeling naar de pagina Winkelwagen moet aan het winkelwagenpictogram zijn gekoppeld, zodat klanten worden omgeleid naar de pagina Winkelwagen wanneer ze het pictogram selecteren.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="3a1e8-126">**Verlanglijstpictogram**: het verlanglijstpictogram wordt weergegeven in de koptekst en geeft het aantal artikelen aan dat aan de verlanglijst van de klant is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="3a1e8-127">Een koppeling naar de pagina Verlanglijst moet aan dit pictogram zijn gekoppeld, zodat klanten worden omgeleid naar de pagina Verlanglijst wanneer ze het pictogram selecteren.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="3a1e8-128">**Aanmeldmodule** : de aanmeldmodule wordt weergegeven in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="3a1e8-129">Klanten kunnen zich aanmelden bij hun account of zich registreren voor een account.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="3a1e8-130">Als de klant al is aangemeld, kan de module worden geconfigureerd voor het weergeven van koppelingen naar de pagina Account, de pagina Orderhistorie of een andere pagina.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="3a1e8-131">**Logomodule**: deze module toont het logo dat de detailhandelaar en het merk vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="3a1e8-132">Het is een afbeelding met een koppeling.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-132">It's an image that has a link.</span></span> <span data-ttu-id="3a1e8-133">De koppeling wordt doorgaans zo geconfigureerd dat deze een omleiding naar de startpagina heeft. Zo kunnen klanten snel terugkeren naar de startpagina vanaf een willekeurige pagina op de site.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="3a1e8-134">**Waarschuwing**: er wordt een waarschuwing weergegeven in de koptekst om een inline bericht weer te geven dat van toepassing is op alle pagina's op de site.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="3a1e8-135">Een waarschuwing kan bijvoorbeeld een bericht weergeven als 'Jaarlijkse uitverkoop eindigt over 2 dagen'.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="3a1e8-136">**Zoekbalk** : in de zoekbalk kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="3a1e8-137">De module moet worden geconfigureerd met de URL van de pagina met zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="3a1e8-138">De parameter voor de querytekenreeks kan worden geconfigureerd (met de standaardwaarde **"q"**).</span><span class="sxs-lookup"><span data-stu-id="3a1e8-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="3a1e8-139">De zoekbalk heeft een vak voor automatisch suggesties waar de module voor automatische suggesties moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="3a1e8-140">**Autosuggest** : de module Autosuggest geeft automatisch de voorgestelde resultaten weer.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="3a1e8-141">Deze resultaten kunnen trefwoorden, producten of categorieën zijn waarin de zoekterm wordt gevonden.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="3a1e8-142">Een koptekstmodule maken</span><span class="sxs-lookup"><span data-stu-id="3a1e8-142">Create a header module</span></span>

<span data-ttu-id="3a1e8-143">Volg deze stappen om een koptekstmodule te maken.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="3a1e8-144">Maak een paginafragment dat een koptekstmodule bevat.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="3a1e8-145">Voeg modules toe aan de vakken in de koptekstmodule.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="3a1e8-146">Werk de instellingen voor elke module bij.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="3a1e8-147">Sla het paginafragment op.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="3a1e8-148">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="3a1e8-149">Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="3a1e8-150">Voeg op de standaardpagina het paginafragment met de koptekstmodule toe aan de koptekst in het hoofdvak.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="3a1e8-151">Sla de sjabloon op.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-151">Save the template.</span></span> 
1. <span data-ttu-id="3a1e8-152">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="3a1e8-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a1e8-153">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3a1e8-153">Additional resources</span></span>

[<span data-ttu-id="3a1e8-154">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="3a1e8-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3a1e8-155">Module Container</span><span class="sxs-lookup"><span data-stu-id="3a1e8-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3a1e8-156">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="3a1e8-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3a1e8-157">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="3a1e8-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3a1e8-158">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="3a1e8-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3a1e8-159">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="3a1e8-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3a1e8-160">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="3a1e8-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3a1e8-161">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="3a1e8-161">Footer module</span></span>](author-footer-module.md)
