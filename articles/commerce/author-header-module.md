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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885473"
---
# <a name="header-module"></a><span data-ttu-id="60652-103">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="60652-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="60652-104">In dit onderwerp wordt beschreven wat koptekstmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="60652-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="60652-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="60652-105">Overview</span></span>

<span data-ttu-id="60652-106">Een koptekstmodule is een speciale container die wordt gebruikt om alle modules te hosten die worden weergegeven in de koptekst van een pagina.</span><span class="sxs-lookup"><span data-stu-id="60652-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="60652-107">De module kan bijvoorbeeld uw sitelogo, koppelingen naar de navigatiehiërarchie, koppelingen naar andere pagina's op de site en de zoekbalk bevatten.</span><span class="sxs-lookup"><span data-stu-id="60652-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="60652-108">Een koptekstmodule wordt automatisch geoptimaliseerd voor het apparaat waarop de site wordt weergegeven (dat wil zeggen: een desktopapparaat of een mobiel apparaat).</span><span class="sxs-lookup"><span data-stu-id="60652-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="60652-109">Op een mobiel apparaat wordt de navigatiebalk bijvoorbeeld samengevouwen in een **Menu**-knop (soms een *hamburgermenu* genoemd).</span><span class="sxs-lookup"><span data-stu-id="60652-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="60652-110">Eigenschappen van een koptekst</span><span class="sxs-lookup"><span data-stu-id="60652-110">Properties of a header</span></span>

<span data-ttu-id="60652-111">Net als algemene containers ondersteunt een koptekstmodule de eigenschappen **kop** en **breedte**.</span><span class="sxs-lookup"><span data-stu-id="60652-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="60652-112">Een koptekstmodule heeft meerdere vakken.</span><span class="sxs-lookup"><span data-stu-id="60652-112">A header module has multiple slots.</span></span> <span data-ttu-id="60652-113">Er zijn bijvoorbeeld vakken voor informatiebericht, navigatiemenu, logo, zoekbalk, winkelwagenpictogram, verlanglijstpictogram en accountgegevens.</span><span class="sxs-lookup"><span data-stu-id="60652-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="60652-114">Elk vak ondersteunt een specifieke set modules.</span><span class="sxs-lookup"><span data-stu-id="60652-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="60652-115">Modules die beschikbaar zijn in een koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="60652-115">Modules that are available in a header module</span></span>

<span data-ttu-id="60652-116">De volgende modules kunnen in een koptekstmodule worden gebruikt:</span><span class="sxs-lookup"><span data-stu-id="60652-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="60652-117">**Navigatiemenu** : het navigatiemenu vertegenwoordigt de navigatiehiërarchie in het afzetkanaal en andere statische navigatiekoppelingen.</span><span class="sxs-lookup"><span data-stu-id="60652-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="60652-118">De navigatiehiërarchie voor het afzetkanaal kan worden geconfigureerd in Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="60652-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="60652-119">Geconfigureerde artikelen worden vervolgens weergegeven als koptekstnavigatie.</span><span class="sxs-lookup"><span data-stu-id="60652-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="60652-120">Daarnaast kunnen statische navigatiekoppelingen worden geconfigureerd en kunnen relatieve koppelingen naar andere pagina's op de e-commerce-site worden aangeleverd.</span><span class="sxs-lookup"><span data-stu-id="60652-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="60652-121">De koptekst zelf kan links, rechts of in het midden worden uitgelijnd.</span><span class="sxs-lookup"><span data-stu-id="60652-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="60652-122">**Winkelwagenpictogram**: het winkelwagenpictogram is een speciaal pictogram dat de winkelwagen vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="60652-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="60652-123">Het wordt weergegeven in de koptekst en geeft het aantal artikelen in de winkelwagen aan.</span><span class="sxs-lookup"><span data-stu-id="60652-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="60652-124">Een koppeling naar de pagina Winkelwagen moet aan het winkelwagenpictogram zijn gekoppeld, zodat klanten worden omgeleid naar de pagina Winkelwagen wanneer ze het pictogram selecteren.</span><span class="sxs-lookup"><span data-stu-id="60652-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="60652-125">**Verlanglijstpictogram**: het verlanglijstpictogram wordt weergegeven in de koptekst en geeft het aantal artikelen aan dat aan de verlanglijst van de klant is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="60652-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="60652-126">Een koppeling naar de pagina Verlanglijst moet aan dit pictogram zijn gekoppeld, zodat klanten worden omgeleid naar de pagina Verlanglijst wanneer ze het pictogram selecteren.</span><span class="sxs-lookup"><span data-stu-id="60652-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="60652-127">**Aanmeldmodule** : de aanmeldmodule wordt weergegeven in de koptekst.</span><span class="sxs-lookup"><span data-stu-id="60652-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="60652-128">Klanten kunnen zich aanmelden bij hun account of zich registreren voor een account.</span><span class="sxs-lookup"><span data-stu-id="60652-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="60652-129">Als de klant al is aangemeld, kan de module worden geconfigureerd voor het weergeven van koppelingen naar de pagina Account, de pagina Orderhistorie of een andere pagina.</span><span class="sxs-lookup"><span data-stu-id="60652-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="60652-130">**Logomodule**: deze module toont het logo dat de detailhandelaar en het merk vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="60652-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="60652-131">Het is een afbeelding met een koppeling.</span><span class="sxs-lookup"><span data-stu-id="60652-131">It's an image that has a link.</span></span> <span data-ttu-id="60652-132">De koppeling wordt doorgaans zo geconfigureerd dat deze een omleiding naar de startpagina heeft. Zo kunnen klanten snel terugkeren naar de startpagina vanaf een willekeurige pagina op de site.</span><span class="sxs-lookup"><span data-stu-id="60652-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="60652-133">**Waarschuwing**: er wordt een waarschuwing weergegeven in de koptekst om een inline bericht weer te geven dat van toepassing is op alle pagina's op de site.</span><span class="sxs-lookup"><span data-stu-id="60652-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="60652-134">Een waarschuwing kan bijvoorbeeld een bericht weergeven als 'Jaarlijkse uitverkoop eindigt over 2 dagen'.</span><span class="sxs-lookup"><span data-stu-id="60652-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="60652-135">**Zoekbalk** : in de zoekbalk kunnen gebruikers zoekwoorden invoeren om naar producten te zoeken.</span><span class="sxs-lookup"><span data-stu-id="60652-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="60652-136">De module moet worden geconfigureerd met de URL van de pagina met zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="60652-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="60652-137">De parameter voor de querytekenreeks kan worden geconfigureerd (met de standaardwaarde **"q"**).</span><span class="sxs-lookup"><span data-stu-id="60652-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="60652-138">De zoekbalk heeft een vak voor automatisch suggesties waar de module voor automatische suggesties moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="60652-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="60652-139">**Autosuggest** : de module Autosuggest geeft automatisch de voorgestelde resultaten weer.</span><span class="sxs-lookup"><span data-stu-id="60652-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="60652-140">Deze resultaten kunnen trefwoorden, producten of categorieën zijn waarin de zoekterm wordt gevonden.</span><span class="sxs-lookup"><span data-stu-id="60652-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="60652-141">Een koptekstmodule maken</span><span class="sxs-lookup"><span data-stu-id="60652-141">Create a header module</span></span>

<span data-ttu-id="60652-142">Volg deze stappen om een koptekstmodule te maken.</span><span class="sxs-lookup"><span data-stu-id="60652-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="60652-143">Maak een paginafragment dat een koptekstmodule bevat.</span><span class="sxs-lookup"><span data-stu-id="60652-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="60652-144">Voeg modules toe aan de vakken in de koptekstmodule.</span><span class="sxs-lookup"><span data-stu-id="60652-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="60652-145">Werk de instellingen voor elke module bij.</span><span class="sxs-lookup"><span data-stu-id="60652-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="60652-146">Sla het paginafragment op.</span><span class="sxs-lookup"><span data-stu-id="60652-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="60652-147">Check de pagina in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="60652-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="60652-148">Volg deze stappen op elke paginasjabloon die voor de site wordt gemaakt om te garanderen dat een koptekst op elke pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="60652-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="60652-149">Voeg op de standaardpagina het paginafragment met de koptekstmodule toe aan de koptekst in het hoofdvak.</span><span class="sxs-lookup"><span data-stu-id="60652-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="60652-150">Sla de sjabloon op.</span><span class="sxs-lookup"><span data-stu-id="60652-150">Save the template.</span></span> 
1. <span data-ttu-id="60652-151">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="60652-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60652-152">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="60652-152">Additional resources</span></span>

[<span data-ttu-id="60652-153">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="60652-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="60652-154">Module Container</span><span class="sxs-lookup"><span data-stu-id="60652-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="60652-155">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="60652-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="60652-156">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="60652-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="60652-157">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="60652-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="60652-158">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="60652-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="60652-159">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="60652-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="60652-160">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="60652-160">Footer module</span></span>](author-footer-module.md)
