---
title: Accountbeheerpagina's en -modules
description: In dit onderwerp worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.
author: v-chgri
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411297"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="4ecb7-103">Accountbeheerpagina's en -modules</span><span class="sxs-lookup"><span data-stu-id="4ecb7-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ecb7-104">In dit onderwerp worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4ecb7-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="4ecb7-105">Overview</span></span>

<span data-ttu-id="4ecb7-106">Accountbeheer verwijst naar een groep pagina's die wordt gebruikt voor het beheren van informatie met betrekking tot gebruikersaccounts in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="4ecb7-107">De pagina's voor accountbeheer bevatten de landingspagina, het gebruikersprofiel, het gebruikersadres, de orderhistorie, bestellingsgegevens, loyaliteitspagina en verlanglijstpagina.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="4ecb7-108">Landingspagina accountbeheer</span><span class="sxs-lookup"><span data-stu-id="4ecb7-108">Account management landing page</span></span>

<span data-ttu-id="4ecb7-109">Op de landingspagina accountbeheer worden de volgende modules gebruikt:</span><span class="sxs-lookup"><span data-stu-id="4ecb7-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="4ecb7-110">**Container**: alle landingspaginamodules voor accountbeheer moeten in een container worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="4ecb7-111">**Welkomsttegel voor account**: deze module wordt gebruikt om een welkomstbericht te geven op de pagina voor accountbeheer.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="4ecb7-112">Deze bevat eigenschappen voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="4ecb7-113">**Algemene accounttegel**: deze module kan worden gebruikt voor het verstrekken van kopteksten en koppelingen voor pagina's voor accountbeheer, zoals de pagina's Ordergeschiedenis of Mijn profiel.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="4ecb7-114">De algemene tegelmodule kan worden gebruikt om een tegel voor elke pagina te configureren.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="4ecb7-115">In Fabrikam wordt deze module gebruikt voor koppelingen op de pagina Ordergeschiedenis en Mijn profiel op de landingspagina voor accountbeheer.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="4ecb7-116">**Verlanglijsttegel voor account**: deze module wordt gebruikt om een overzicht te geven van de artikelen op de verlanglijst van de klant.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="4ecb7-117">Het heeft bijvoorbeeld de status "U hebt 10 artikelen op uw verlanglijst".</span><span class="sxs-lookup"><span data-stu-id="4ecb7-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="4ecb7-118">Deze bevat eigenschappen voor de koptekst en de koppeling Details weergeven.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="4ecb7-119">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Verlanglijst.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="4ecb7-120">**Adrestegel voor account**: deze module wordt gebruikt om een overzicht van de adressen van de gebruiker te bieden.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="4ecb7-121">Het heeft bijvoorbeeld de status "U hebt twee adressen toegevoegd aan uw account".</span><span class="sxs-lookup"><span data-stu-id="4ecb7-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="4ecb7-122">Deze bevat eigenschappen voor de koptekst en de koppeling Details weergeven.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="4ecb7-123">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Gebruikersadres.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="4ecb7-124">**Loyaliteitstegel voor account**: deze module wordt gebruikt om informatie over loyaliteitsprogramma's weer te geven en te koppelen.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="4ecb7-125">Deze tegel heeft twee statussen: de ene status bevat koppelingen om deel te nemen aan een loyaliteitsprogramma als de gebruiker nog geen lid is.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="4ecb7-126">De andere status toont koppelingen om de pagina met loyaliteitsgegevens weer te geven als de gebruiker al lid is.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="4ecb7-127">Eigenschappen zijn onder andere de koptekst, de koppeling Aanmelden en de koppeling Loyaliteit weergeven.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="4ecb7-128">De koppeling Loyaliteit weergeven moet zijn geconfigureerd voor omleiding naar de loyaliteitspagina.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="4ecb7-129">De koppeling Aanmelden moet zijn geconfigureerd voor het omleiden naar een pagina waar gebruikers kunnen deelnemen aan het loyaliteitsprogramma.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="4ecb7-130">Pagina Orderhistorie</span><span class="sxs-lookup"><span data-stu-id="4ecb7-130">Order history page</span></span>

<span data-ttu-id="4ecb7-131">De pagina Orderhistorie werkt met de module Orderhistorie om alle recente orders weer te geven die de gebruiker heeft geplaatst.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="4ecb7-132">Pagina met orderdetails</span><span class="sxs-lookup"><span data-stu-id="4ecb7-132">Order details page</span></span>

<span data-ttu-id="4ecb7-133">De pagina Orderdetails bevat gedetailleerde informatie voor elke order en wordt geopend vanuit de pagina Orderhistorie.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="4ecb7-134">Er wordt gebruikgemaakt van de module Orderdetails, die met de verkoop-id of transactie-id de orderdetails ophalen.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="4ecb7-135">Pagina Gebruikersprofiel</span><span class="sxs-lookup"><span data-stu-id="4ecb7-135">User profile page</span></span>

<span data-ttu-id="4ecb7-136">Op de pagina Gebruikersprofiel worden de gegevens van een gebruikersaccount weergegeven, zoals naam en e-mailadres van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="4ecb7-137">Deze gebruikt gebruikersprofielgegevens en gebruikersprofielbewerkingsmodules.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="4ecb7-138">Het e-mailadres kan niet worden verwijderd, maar wel worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="4ecb7-139">De gebruikersprofielpagina bevat ook gebruikersvoorkeuren waarmee een gebruiker zich kan aan- of afmelden voor bepaalde functies, zoals personalisatie van aanbevelingslijsten.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="4ecb7-140">Pagina Gebruikersadres</span><span class="sxs-lookup"><span data-stu-id="4ecb7-140">User address page</span></span>

<span data-ttu-id="4ecb7-141">Op de pagina Gebruikersadres wordt de lijst met adressen weergegeven die zijn gekoppeld aan het gebruikersaccount.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="4ecb7-142">De gebruiker heeft deze adressen opgegeven tijdens het uitchecken of rechtstreeks toegevoegd op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="4ecb7-143">De module met gebruikersadressen wordt gebruikt om adressen toe te voegen en te bewerken, het primaire adres in te stellen en bestaande adressen op de pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="4ecb7-144">Pagina Verlanglijst</span><span class="sxs-lookup"><span data-stu-id="4ecb7-144">Wish list page</span></span>

<span data-ttu-id="4ecb7-145">Op de pagina Verlanglijst worden de artikelen weergegeven die zijn toegevoegd aan de verlanglijst van de klant.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="4ecb7-146">Met de module Verlanglijst kunt u verlanglijstitems weergeven.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="4ecb7-147">Loyaliteitspagina</span><span class="sxs-lookup"><span data-stu-id="4ecb7-147">Loyalty page</span></span>

<span data-ttu-id="4ecb7-148">Op de loyaliteitspagina kunnen klanten hun loyaliteitsgegevens bekijken als ze al lid zijn van een loyaliteitsprogramma.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="4ecb7-149">Ze kunnen ook de punten bekijken die zij hebben verdiend en in recente transacties hebben ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="4ecb7-150">Op de pagina wordt de loyaliteitsgegevensmodule gebruikt om de loyaliteitsgegevens te presenteren.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="4ecb7-151">Om deel te nemen aan een loyaliteitsprogramma, kan een marketingpagina worden gemaakt met modules voor aanmelden en loyaliteitsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="4ecb7-152">Als de gebruiker geen lid is van een loyaliteitsprogramma, bieden deze modules de gebruiker de gelegenheid om zich te registreren.</span><span class="sxs-lookup"><span data-stu-id="4ecb7-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ecb7-153">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="4ecb7-153">Additional resources</span></span>

[<span data-ttu-id="4ecb7-154">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="4ecb7-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4ecb7-155">Containermodule</span><span class="sxs-lookup"><span data-stu-id="4ecb7-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4ecb7-156">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="4ecb7-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4ecb7-157">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="4ecb7-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4ecb7-158">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="4ecb7-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4ecb7-159">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="4ecb7-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4ecb7-160">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="4ecb7-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4ecb7-161">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="4ecb7-161">Footer module</span></span>](author-footer-module.md)
