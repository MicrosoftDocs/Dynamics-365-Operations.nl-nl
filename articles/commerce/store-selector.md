---
title: Winkelselectiemodule
description: In dit onderwerp wordt beschreven wat de winkelselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378203"
---
# <a name="store-selector-module"></a><span data-ttu-id="4d738-103">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="4d738-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d738-104">In dit onderwerp wordt beschreven wat de winkelselectiemodule is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d738-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d738-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="4d738-105">Overview</span></span>

<span data-ttu-id="4d738-106">Een winkelselectiemodule wordt gebruikt voor het klantscenario Online kopen, ophalen in winkel.</span><span class="sxs-lookup"><span data-stu-id="4d738-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="4d738-107">Er wordt een lijst weergegeven met winkels waar een product kan worden opgehaald, met de openingstijden en productvoorraad voor elke winkel.</span><span class="sxs-lookup"><span data-stu-id="4d738-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="4d738-108">Voor de winkelselectiemodule is de context van een product en een zoeklocatie nodig om winkels te kunnen vinden.</span><span class="sxs-lookup"><span data-stu-id="4d738-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="4d738-109">Als er geen zoeklocatie is, wordt standaard de locatie van de browser van de klant ingesteld, op voorwaarde dat de klant toestemming geeft.</span><span class="sxs-lookup"><span data-stu-id="4d738-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="4d738-110">De module bevat een invoervak waarin de klant een locatie (postcode of plaats en provincie) kan invoeren om winkels in de buurt te vinden.</span><span class="sxs-lookup"><span data-stu-id="4d738-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="4d738-111">De winkelselectiemodule is geïntegreerd in de API (Application Programming Interface) van Bing Kaarten om de locatie te converteren naar een breedtegraad en een lengtegraad.</span><span class="sxs-lookup"><span data-stu-id="4d738-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="4d738-112">Er is een API-sleutel voor Bing Kaarten vereist. Deze moet worden toegevoegd aan de pagina Gedeelde Commerce-parameters in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d738-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4d738-113">U kunt de winkelselectiemodule toevoegen aan een koopvakmodule op de pagina met productgegevens om winkels weer te geven waar een product kan worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="4d738-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="4d738-114">De winkelselectiemodule kan ook aan een winkelwagenmodule worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="4d738-114">It can also be added to a cart module.</span></span> <span data-ttu-id="4d738-115">Wanneer de winkelselectiemodule aan een winkelwagenmodule wordt toegevoegd, worden in de winkelselectiemodule opties voor ophalen weergegeven voor elk item in de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="4d738-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="4d738-116">Daarnaast kan deze module met aangepaste codering worden toegevoegd aan andere pagina's of modules via extensies en aanpassingen.</span><span class="sxs-lookup"><span data-stu-id="4d738-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="4d738-117">Het scenario Online kopen, ophalen in winkel werkt alleen als producten zijn geconfigureerd met de leveringsmethode 'ophalen door klant'.</span><span class="sxs-lookup"><span data-stu-id="4d738-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="4d738-118">Anders wordt de module niet op de desbetreffende pagina's weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4d738-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="4d738-119">Zie [Leveringsmethoden instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor meer informatie over het configureren van de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="4d738-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="4d738-120">De volgende afbeelding toont een voorbeeld van een winkelselectiemodule die wordt gebruikt voor een pagina met productgegevens.</span><span class="sxs-lookup"><span data-stu-id="4d738-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Voorbeeld van een winkelselectiemodule](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="4d738-122">Gebruik van winkelselectiemodule in e-Commerce</span><span class="sxs-lookup"><span data-stu-id="4d738-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="4d738-123">Een winkelselectiemodule kan op een pagina met productgegevens worden gebruikt om winkels in de buurt weer te geven waar een product kan worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="4d738-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="4d738-124">Een winkelselectiemodule kan op een winkelwagenpagina worden gebruikt om winkels in de buurt weer te geven waar een product uit de winkelwagen kan worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="4d738-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="4d738-125">Eigenschappen van winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="4d738-125">Store selector module properties</span></span>

| <span data-ttu-id="4d738-126">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="4d738-126">Property name</span></span>             | <span data-ttu-id="4d738-127">Waarde</span><span class="sxs-lookup"><span data-stu-id="4d738-127">Value</span></span>                 | <span data-ttu-id="4d738-128">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="4d738-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="4d738-129">Zoekstraal</span><span class="sxs-lookup"><span data-stu-id="4d738-129">Search radius</span></span> | <span data-ttu-id="4d738-130">Nummer</span><span class="sxs-lookup"><span data-stu-id="4d738-130">Number</span></span> | <span data-ttu-id="4d738-131">Hiermee definieert u de zoekradius voor winkels in kilometers.</span><span class="sxs-lookup"><span data-stu-id="4d738-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="4d738-132">Als er geen waarde is opgegeven, wordt de standaardzoekradius van 50 kilometer gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4d738-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="4d738-133">Servicevoorwaarden</span><span class="sxs-lookup"><span data-stu-id="4d738-133">Terms of Service</span></span> | <span data-ttu-id="4d738-134">URL</span><span class="sxs-lookup"><span data-stu-id="4d738-134">URL</span></span>    |  <span data-ttu-id="4d738-135">De URL naar de servicevoorwaarden die vereist is voor de Bing Kaarten-service.</span><span class="sxs-lookup"><span data-stu-id="4d738-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="4d738-136">Een winkelselectiemodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="4d738-136">Add a store selector module to a page</span></span>

<span data-ttu-id="4d738-137">Een winkelselectiemodule heeft de context van een product nodig, dus kan alleen worden gebruikt binnen koopvak- en winkelwagenmodules.</span><span class="sxs-lookup"><span data-stu-id="4d738-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="4d738-138">Winkelselectiemodules functioneren niet buiten deze modules.</span><span class="sxs-lookup"><span data-stu-id="4d738-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="4d738-139">Zie [Module met vakje voor kopen](add-buy-box.md) voor informatie over het toevoegen van een winkelselectiemodule aan een koopvakmodule.</span><span class="sxs-lookup"><span data-stu-id="4d738-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="4d738-140">Zie [Winkelwagenmodule](add-cart-module.md) voor informatie over het toevoegen van een winkelselectiemodule aan een winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="4d738-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d738-141">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="4d738-141">Additional resources</span></span>

[<span data-ttu-id="4d738-142">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="4d738-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4d738-143">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="4d738-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4d738-144">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="4d738-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4d738-145">Snelle rondleiding door de pagina met productgegevens</span><span class="sxs-lookup"><span data-stu-id="4d738-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="4d738-146">Snelle rondleiding door winkelwagen en kassa</span><span class="sxs-lookup"><span data-stu-id="4d738-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="4d738-147">Leveringsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="4d738-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="4d738-148">Bing Kaarten voor uw organisatie beheren</span><span class="sxs-lookup"><span data-stu-id="4d738-148">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)
