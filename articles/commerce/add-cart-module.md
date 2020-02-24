---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025431"
---
# <a name="cart-module"></a><span data-ttu-id="ecc50-103">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="ecc50-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ecc50-104">In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ecc50-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ecc50-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="ecc50-105">Overview</span></span>

<span data-ttu-id="ecc50-106">Een winkelwagenmodule wordt gebruikt om de artikelen weer te geven die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen.</span><span class="sxs-lookup"><span data-stu-id="ecc50-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="ecc50-107">De module bevat bijvoorbeeld alle artikelen die zijn toegevoegd aan de winkelwagen en een orderoverzicht.</span><span class="sxs-lookup"><span data-stu-id="ecc50-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="ecc50-108">De module biedt de klant ook de mogelijkheid om promotiecodes toe te passen of te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="ecc50-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="ecc50-109">De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen.</span><span class="sxs-lookup"><span data-stu-id="ecc50-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="ecc50-110">De module ondersteunt ook een koppeling **Terug naar winkelen**.</span><span class="sxs-lookup"><span data-stu-id="ecc50-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="ecc50-111">U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.</span><span class="sxs-lookup"><span data-stu-id="ecc50-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="ecc50-112">Een winkelwagenmodule geeft gegevens weer op basis van de winkelwagen-id.</span><span class="sxs-lookup"><span data-stu-id="ecc50-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="ecc50-113">De winkelwagen-id is een browsercookie die overal in de site beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="ecc50-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="ecc50-114">Eigenschappen en vakken van de winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="ecc50-114">Cart module properties and slots</span></span>

<span data-ttu-id="ecc50-115">De winkelwagenmodule heeft een eigenschap **Koptekst** die kan worden ingesteld op waarden als **Boodschappentas** en **Artikelen in uw winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="ecc50-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="ecc50-116">Modules die in de winkelwagenmodule kunnen worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="ecc50-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="ecc50-117">**Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="ecc50-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="ecc50-118">De berichten worden aangestuurd door het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="ecc50-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="ecc50-119">U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="ecc50-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="ecc50-120">**Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="ecc50-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="ecc50-121">Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt.</span><span class="sxs-lookup"><span data-stu-id="ecc50-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="ecc50-122">De winkelselectiemodule is geïntegreerd in de API (Application Programming Interface) van Bing Kaarten om de locatie te converteren naar een breedtegraad en een lengtegraad.</span><span class="sxs-lookup"><span data-stu-id="ecc50-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="ecc50-123">Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina Gedeelde Retail-parameters in Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="ecc50-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="ecc50-124">Deze module ondersteunt twee eigenschappen, **Zoekradius** en **Koppeling naar servicevoorwaarden**.</span><span class="sxs-lookup"><span data-stu-id="ecc50-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="ecc50-125">De eigenschap **Zoekradius** bepaalt (in mijl) binnen welke straal naar winkels moet worden gezocht.</span><span class="sxs-lookup"><span data-stu-id="ecc50-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="ecc50-126">Als er geen waarde is opgegeven, wordt de standaardzoekradius van 50 mijl gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ecc50-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="ecc50-127">Als u Bing Kaarten of een externe service gebruikt, kunt u de eigenschap **Koppeling naar servicevoorwaarden** gebruiken om een koppeling naar de servicevoorwaarden te verstrekken.</span><span class="sxs-lookup"><span data-stu-id="ecc50-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="ecc50-128">Er is een koppeling naar servicevoorwaarden vereist voor de Bing Kaarten-service.</span><span class="sxs-lookup"><span data-stu-id="ecc50-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="ecc50-129">Instellingen voor winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="ecc50-129">Cart module settings</span></span>

<span data-ttu-id="ecc50-130">Winkelwagenmodules hebben de volgende instellingen die kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:</span><span class="sxs-lookup"><span data-stu-id="ecc50-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="ecc50-131">**Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="ecc50-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="ecc50-132">Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="ecc50-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="ecc50-133">**Voorraadcontrole**: wanneer de waarde is ingesteld op **True**, wordt een artikel alleen aan de winkelwagen toegevoegd nadat de koopvakmodule heeft gecontroleerd dat het op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="ecc50-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="ecc50-134">Deze voorraadcontrole wordt uitgevoerd voor scenario's waarin het artikel wordt verzonden en voor scenario's waarin het wordt opgehaald in de winkel.</span><span class="sxs-lookup"><span data-stu-id="ecc50-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="ecc50-135">Als de waarde is ingesteld op **False**, wordt er geen voorraadcontrole uitgevoerd voordat een artikel aan de winkelwagen wordt toegevoegd en de order wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="ecc50-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="ecc50-136">**Voorraadbuffer**: deze eigenschap wordt gebruikt om een bufferhoeveelheid op te geven voor de voorraad op te geven.</span><span class="sxs-lookup"><span data-stu-id="ecc50-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="ecc50-137">Voorraad wordt in realtime bijgehouden en wanneer een groot aantal klanten orders plaatst, kan het lastig zijn om een nauwkeurige voorraadtelling bij te houden.</span><span class="sxs-lookup"><span data-stu-id="ecc50-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="ecc50-138">Wanneer een voorraadcontrole wordt uitgevoerd en de voorraad kleiner is dan de bufferhoeveelheid, wordt het product verwerkt als niet op voorraad.</span><span class="sxs-lookup"><span data-stu-id="ecc50-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="ecc50-139">Dus wanneer verkopen snel plaatsvinden via verschillende kanalen en de voorraadtelling niet volledig is gesynchroniseerd, is er minder risico dat een artikel wordt verkocht dat niet op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="ecc50-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="ecc50-140">**Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven.</span><span class="sxs-lookup"><span data-stu-id="ecc50-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="ecc50-141">Deze route kan op siteniveau worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="ecc50-141">This route can be configured at the site level.</span></span> <span data-ttu-id="ecc50-142">Met deze configuratie kunnen detailhandelaren de klant terugbrengen naar de startpagina of naar een andere pagina op de site.</span><span class="sxs-lookup"><span data-stu-id="ecc50-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="ecc50-143">Interactie met Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="ecc50-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="ecc50-144">De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's.</span><span class="sxs-lookup"><span data-stu-id="ecc50-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="ecc50-145">De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="ecc50-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="ecc50-146">Een winkelwagenmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="ecc50-146">Add a cart module to a page</span></span>

<span data-ttu-id="ecc50-147">Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="ecc50-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ecc50-148">Maak een fragment met de naam **Winkelwagenfragment** en voeg hieraan een winkelwagenmodule toe.</span><span class="sxs-lookup"><span data-stu-id="ecc50-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="ecc50-149">Voeg een koptekst toe aan de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="ecc50-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="ecc50-150">Voeg een winkelselectiemodule toe aan de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="ecc50-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="ecc50-151">Sla het fragment op, voltooi de bewerking ervan en publiceer het fragment.</span><span class="sxs-lookup"><span data-stu-id="ecc50-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="ecc50-152">Maak een sjabloon met de naam **Winkelwagensjabloon** en voeg het winkelwagenfragment toe dat u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ecc50-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="ecc50-153">Sla de sjabloon op, voltooi de bewerking ervan en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="ecc50-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="ecc50-154">Maak een pagina die gebruikmaakt van de nieuwe sjabloon.</span><span class="sxs-lookup"><span data-stu-id="ecc50-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="ecc50-155">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="ecc50-155">Save and preview the page.</span></span>
1. <span data-ttu-id="ecc50-156">Voltooi het bewerken van de pagina en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="ecc50-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ecc50-157">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ecc50-157">Additional resources</span></span>

[<span data-ttu-id="ecc50-158">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="ecc50-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ecc50-159">Module Container</span><span class="sxs-lookup"><span data-stu-id="ecc50-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ecc50-160">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="ecc50-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ecc50-161">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="ecc50-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ecc50-162">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="ecc50-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ecc50-163">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="ecc50-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ecc50-164">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="ecc50-164">Footer module</span></span>](author-footer-module.md)
