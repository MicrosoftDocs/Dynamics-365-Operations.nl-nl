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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 29523d03fb687684dae7d0ce08208905cce702df
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206626"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="ca6c7-103">Accountbeheerpagina's en -modules</span><span class="sxs-lookup"><span data-stu-id="ca6c7-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ca6c7-104">In dit onderwerp worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ca6c7-105">Accountbeheer verwijst naar een groep pagina's die wordt gebruikt voor het beheren van informatie met betrekking tot gebruikersaccounts in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ca6c7-106">De pagina's voor accountbeheer bevatten de landingspagina, het gebruikersprofiel, het gebruikersadres, de orderhistorie, bestellingsgegevens, loyaliteitspagina en verlanglijstpagina.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="ca6c7-107">Landingspagina accountbeheer</span><span class="sxs-lookup"><span data-stu-id="ca6c7-107">Account management landing page</span></span>

<span data-ttu-id="ca6c7-108">Op de landingspagina accountbeheer worden de volgende modules gebruikt:</span><span class="sxs-lookup"><span data-stu-id="ca6c7-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="ca6c7-109">**Container**: alle landingspaginamodules voor accountbeheer moeten in een container worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="ca6c7-110">**Welkomsttegel voor account**: deze module wordt gebruikt om een welkomstbericht te geven op de pagina voor accountbeheer.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="ca6c7-111">Deze bevat eigenschappen voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="ca6c7-112">**Algemene accounttegel**: deze module kan worden gebruikt voor het verstrekken van kopteksten en koppelingen voor pagina's voor accountbeheer, zoals de pagina's Ordergeschiedenis of Mijn profiel.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="ca6c7-113">De algemene tegelmodule kan worden gebruikt om een tegel voor elke pagina te configureren.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="ca6c7-114">In Fabrikam wordt deze module gebruikt voor koppelingen op de pagina Ordergeschiedenis en Mijn profiel op de landingspagina voor accountbeheer.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="ca6c7-115">**Verlanglijsttegel voor account**: deze module wordt gebruikt om een overzicht te geven van de artikelen op de verlanglijst van de klant.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="ca6c7-116">Het heeft bijvoorbeeld de status "U hebt 10 artikelen op uw verlanglijst".</span><span class="sxs-lookup"><span data-stu-id="ca6c7-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="ca6c7-117">Deze bevat eigenschappen voor de koptekst en de koppeling Details weergeven.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="ca6c7-118">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Verlanglijst.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="ca6c7-119">**Adrestegel voor account**: deze module wordt gebruikt om een overzicht van de adressen van de gebruiker te bieden.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="ca6c7-120">Het heeft bijvoorbeeld de status "U hebt twee adressen toegevoegd aan uw account".</span><span class="sxs-lookup"><span data-stu-id="ca6c7-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="ca6c7-121">Deze bevat eigenschappen voor de koptekst en de koppeling Details weergeven.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="ca6c7-122">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Gebruikersadres.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="ca6c7-123">**Loyaliteitstegel voor account**: deze module wordt gebruikt om informatie over loyaliteitsprogramma's weer te geven en te koppelen.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="ca6c7-124">Deze tegel heeft twee statussen: de ene status bevat koppelingen om deel te nemen aan een loyaliteitsprogramma als de gebruiker nog geen lid is.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-124">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="ca6c7-125">De andere status toont koppelingen om de pagina met loyaliteitsgegevens weer te geven als de gebruiker al lid is.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="ca6c7-126">Eigenschappen zijn onder andere de koptekst, de koppeling Aanmelden en de koppeling Loyaliteit weergeven.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="ca6c7-127">De koppeling Loyaliteit weergeven moet zijn geconfigureerd voor omleiding naar de loyaliteitspagina.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="ca6c7-128">De koppeling Aanmelden moet zijn geconfigureerd voor het omleiden naar een pagina waar gebruikers kunnen deelnemen aan het loyaliteitsprogramma.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="ca6c7-129">Pagina Orderhistorie</span><span class="sxs-lookup"><span data-stu-id="ca6c7-129">Order history page</span></span>

<span data-ttu-id="ca6c7-130">De pagina Orderhistorie werkt met de module Orderhistorie om alle recente orders weer te geven die de gebruiker heeft geplaatst.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="ca6c7-131">Pagina met orderdetails</span><span class="sxs-lookup"><span data-stu-id="ca6c7-131">Order details page</span></span>

<span data-ttu-id="ca6c7-132">De pagina Orderdetails bevat gedetailleerde informatie voor elke order en wordt geopend vanuit de pagina Orderhistorie.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="ca6c7-133">Er wordt gebruikgemaakt van de module Orderdetails, die met de verkoop-id of transactie-id de orderdetails ophalen.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="ca6c7-134">Pagina Gebruikersprofiel</span><span class="sxs-lookup"><span data-stu-id="ca6c7-134">User profile page</span></span>

<span data-ttu-id="ca6c7-135">Op de pagina Gebruikersprofiel worden de gegevens van een gebruikersaccount weergegeven, zoals naam en e-mailadres van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-135">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="ca6c7-136">Deze gebruikt gebruikersprofielgegevens en gebruikersprofielbewerkingsmodules.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-136">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="ca6c7-137">Het e-mailadres kan niet worden verwijderd, maar wel worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-137">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="ca6c7-138">De gebruikersprofielpagina bevat ook gebruikersvoorkeuren waarmee een gebruiker zich kan aan- of afmelden voor bepaalde functies, zoals personalisatie van aanbevelingslijsten.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-138">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="ca6c7-139">Pagina Gebruikersadres</span><span class="sxs-lookup"><span data-stu-id="ca6c7-139">User address page</span></span>

<span data-ttu-id="ca6c7-140">Op de pagina Gebruikersadres wordt de lijst met adressen weergegeven die zijn gekoppeld aan het gebruikersaccount.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="ca6c7-141">De gebruiker heeft deze adressen opgegeven tijdens het uitchecken of rechtstreeks toegevoegd op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="ca6c7-142">De module met gebruikersadressen wordt gebruikt om adressen toe te voegen en te bewerken, het primaire adres in te stellen en bestaande adressen op de pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="ca6c7-143">Pagina Verlanglijst</span><span class="sxs-lookup"><span data-stu-id="ca6c7-143">Wish list page</span></span>

<span data-ttu-id="ca6c7-144">Op de pagina Verlanglijst worden de artikelen weergegeven die zijn toegevoegd aan de verlanglijst van de klant.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="ca6c7-145">Met de module Verlanglijst kunt u verlanglijstitems weergeven.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="ca6c7-146">Loyaliteitspagina</span><span class="sxs-lookup"><span data-stu-id="ca6c7-146">Loyalty page</span></span>

<span data-ttu-id="ca6c7-147">Op de loyaliteitspagina kunnen klanten hun loyaliteitsgegevens bekijken als ze al lid zijn van een loyaliteitsprogramma.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="ca6c7-148">Ze kunnen ook de punten bekijken die zij hebben verdiend en in recente transacties hebben ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="ca6c7-149">Op de pagina wordt de loyaliteitsgegevensmodule gebruikt om de loyaliteitsgegevens te presenteren.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="ca6c7-150">Om deel te nemen aan een loyaliteitsprogramma, kan een marketingpagina worden gemaakt met modules voor aanmelden en loyaliteitsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="ca6c7-151">Als de gebruiker geen lid is van een loyaliteitsprogramma, bieden deze modules de gebruiker de gelegenheid om zich te registreren.</span><span class="sxs-lookup"><span data-stu-id="ca6c7-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca6c7-152">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="ca6c7-152">Additional resources</span></span>

[<span data-ttu-id="ca6c7-153">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="ca6c7-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ca6c7-154">Containermodule</span><span class="sxs-lookup"><span data-stu-id="ca6c7-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ca6c7-155">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="ca6c7-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ca6c7-156">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="ca6c7-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ca6c7-157">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="ca6c7-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ca6c7-158">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="ca6c7-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ca6c7-159">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="ca6c7-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ca6c7-160">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="ca6c7-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]