---
title: Accountbeheerpagina's en -modules
description: In dit onderwerp worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885804"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="8ec1c-103">Accountbeheerpagina's en -modules</span><span class="sxs-lookup"><span data-stu-id="8ec1c-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8ec1c-104">In dit onderwerp worden de pagina's en modules voor accountbeheer in Microsoft Dynamics 365 Commerce besproken.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ec1c-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="8ec1c-105">Overview</span></span>

<span data-ttu-id="8ec1c-106">Accountbeheer verwijst naar een groep pagina's die wordt gebruikt voor het beheren van informatie met betrekking tot gebruikersaccounts in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="8ec1c-107">De pagina's voor accountbeheer bevatten de landingspagina, het gebruikersprofiel, het gebruikersadres, de orderhistorie, bestellingsgegevens, loyaliteitspagina en verlanglijstpagina.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="8ec1c-108">Landingspagina accountbeheer</span><span class="sxs-lookup"><span data-stu-id="8ec1c-108">Account management landing page</span></span>

<span data-ttu-id="8ec1c-109">Op de landingspagina accountbeheer worden de volgende modules gebruikt:</span><span class="sxs-lookup"><span data-stu-id="8ec1c-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="8ec1c-110">**Plaatsing van inhoud**: deze module is een containermodule die alle modules op de landingspagina voor accountbeheer bevat.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="8ec1c-111">**Welkomstitem voor account**: deze module wordt gebruikt om een welkomstbericht te geven op de pagina voor accountbeheer.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="8ec1c-112">Het bevat eigenschappen voor de koptekst en de tegelgrootte.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="8ec1c-113">De eigenschap **Tegelgrootte** definieert de breedte van de module in de inhoudplaatsingsmodule.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="8ec1c-114">De waarden lopen uiteen van **1** tot **12**, waarbij **12** de volledige breedte van de container voor inhoudplaatsing aangeeft.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="8ec1c-115">**Item voor plaatsing van accountorders**: deze module wordt gebruikt om een overzicht te bieden van het aantal orders dat door het gebruikersaccount is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="8ec1c-116">Het bevat eigenschappen voor de koptekst, de tegelgrootte en de koppeling voor details weergeven.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="8ec1c-117">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Orderhistorie.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="8ec1c-118">**Item voor plaatsing van accountprofiel**: deze module wordt gebruikt om een overzicht van het gebruikersprofiel te bieden.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="8ec1c-119">Het bevat eigenschappen voor de koptekst, de tegelgrootte en de koppeling voor details weergeven.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="8ec1c-120">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Gebruikersprofiel.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="8ec1c-121">**Item met verlanglijst voor account** : deze module wordt gebruikt om een overzicht te bieden van de artikelen op de verlanglijst van de klant.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="8ec1c-122">Het heeft bijvoorbeeld de status "U hebt 10 artikelen op uw verlanglijst".</span><span class="sxs-lookup"><span data-stu-id="8ec1c-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="8ec1c-123">Het bevat eigenschappen voor de koptekst, de tegelgrootte en de koppeling voor details weergeven.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="8ec1c-124">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Verlanglijst.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="8ec1c-125">**Item voor accountadres**: deze module wordt gebruikt om een overzicht van de adressen van de gebruiker te bieden.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="8ec1c-126">Het heeft bijvoorbeeld de status "U hebt twee adressen toegevoegd aan uw account".</span><span class="sxs-lookup"><span data-stu-id="8ec1c-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="8ec1c-127">Het bevat eigenschappen voor de koptekst, de tegelgrootte en de koppeling voor details weergeven.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="8ec1c-128">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de pagina Gebruikersadres.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="8ec1c-129">**Item voor accountloyaliteit**: deze module wordt gebruikt om informatie over loyaliteitsprogramma's weer te geven en te koppelen.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="8ec1c-130">Het bevat eigenschappen voor de koptekst, de tegelgrootte en koppelingen voor details weergeven en lid worden.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="8ec1c-131">De koppeling Details weergeven moet zijn geconfigureerd voor omleiding naar de loyaliteitspagina.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="8ec1c-132">De koppeling voor lid worden moet zijn geconfigureerd voor het omleiden naar een pagina waar gebruikers kunnen deelnemen aan het loyaliteitsprogramma.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="8ec1c-133">Pagina Orderhistorie</span><span class="sxs-lookup"><span data-stu-id="8ec1c-133">Order history page</span></span>

<span data-ttu-id="8ec1c-134">De pagina Orderhistorie werkt met de module Orderhistorie om alle recente orders weer te geven die de gebruiker heeft geplaatst.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="8ec1c-135">Pagina met orderdetails</span><span class="sxs-lookup"><span data-stu-id="8ec1c-135">Order details page</span></span>

<span data-ttu-id="8ec1c-136">De pagina Orderdetails bevat gedetailleerde informatie voor elke order en wordt geopend vanuit de pagina Orderhistorie.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="8ec1c-137">Er wordt gebruikgemaakt van de module Orderdetails, die met de verkoop-id of transactie-id de orderdetails ophalen.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="8ec1c-138">Pagina Gebruikersprofiel</span><span class="sxs-lookup"><span data-stu-id="8ec1c-138">User profile page</span></span>

<span data-ttu-id="8ec1c-139">Op de pagina Gebruikersprofiel worden de gegevens van een gebruikersaccount weergegeven, zoals naam en e-mailadres van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="8ec1c-140">Hiervoor wordt de gebruikersprofielmodule gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-140">It uses the user profile module.</span></span> <span data-ttu-id="8ec1c-141">Het e-mailadres kan niet worden verwijderd, maar wel worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="8ec1c-142">De gebruikersprofielpagina bevat ook gebruikersvoorkeuren waarmee een gebruiker zich kan aan- of afmelden voor bepaalde functies, zoals personalisatie van aanbevelingslijsten.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="8ec1c-143">Pagina Gebruikersadres</span><span class="sxs-lookup"><span data-stu-id="8ec1c-143">User address page</span></span>

<span data-ttu-id="8ec1c-144">Op de pagina Gebruikersadres wordt de lijst met adressen weergegeven die zijn gekoppeld aan het gebruikersaccount.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="8ec1c-145">De gebruiker heeft deze adressen opgegeven tijdens het uitchecken of rechtstreeks toegevoegd op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="8ec1c-146">De module met gebruikersadressen wordt gebruikt om adressen toe te voegen en te bewerken, het primaire adres in te stellen en bestaande adressen op de pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="8ec1c-147">Pagina Verlanglijst</span><span class="sxs-lookup"><span data-stu-id="8ec1c-147">Wish list page</span></span>

<span data-ttu-id="8ec1c-148">Op de pagina Verlanglijst worden de artikelen weergegeven die zijn toegevoegd aan de verlanglijst van de klant.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="8ec1c-149">Met de module Verlanglijst kunt u verlanglijstitems weergeven.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="8ec1c-150">Loyaliteitspagina</span><span class="sxs-lookup"><span data-stu-id="8ec1c-150">Loyalty page</span></span>

<span data-ttu-id="8ec1c-151">Met de loyaliteitspagina kunnen klanten deelnemen aan een loyaliteitsprogramma of, als ze al lid zijn, de programmadetails weergeven.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="8ec1c-152">Ze kunnen ook de punten bekijken die zij hebben verdiend en in recente transacties hebben ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="8ec1c-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ec1c-153">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8ec1c-153">Additional resources</span></span>

[<span data-ttu-id="8ec1c-154">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="8ec1c-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8ec1c-155">Module Container</span><span class="sxs-lookup"><span data-stu-id="8ec1c-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8ec1c-156">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="8ec1c-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8ec1c-157">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="8ec1c-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8ec1c-158">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="8ec1c-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8ec1c-159">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="8ec1c-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8ec1c-160">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="8ec1c-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8ec1c-161">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="8ec1c-161">Footer module</span></span>](author-footer-module.md)
