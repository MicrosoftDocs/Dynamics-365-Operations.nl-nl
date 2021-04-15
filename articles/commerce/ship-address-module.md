---
title: Module voor verzendadressen
description: In dit onderwerp wordt de module voor verzendadressen beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795424"
---
# <a name="shipping-address-module"></a><span data-ttu-id="8e68b-103">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="8e68b-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e68b-104">In dit onderwerp wordt de module voor verzendadressen beschreven en wordt uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8e68b-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8e68b-105">Met de module voor verzendadressen kan een klant het verzendadres voor een order toevoegen of selecteren tijdens de betalingsstroom.</span><span class="sxs-lookup"><span data-stu-id="8e68b-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="8e68b-106">Als een klant is aangemeld, worden alle adressen weergegeven die eerder voor die klant zijn opgeslagen en de klant kan een adres selecteren.</span><span class="sxs-lookup"><span data-stu-id="8e68b-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="8e68b-107">De klant kan ook een nieuw adres toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8e68b-107">The customer can also add a new address.</span></span> <span data-ttu-id="8e68b-108">De module voor verzendadressen wordt gebruikt voor alle artikelen in de order waarvoor verzending is vereist.</span><span class="sxs-lookup"><span data-stu-id="8e68b-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="8e68b-109">U kunt verzendadresnotaties definiëren in Commerce Headquarters voor elk land of elke regio en met de module voor verzendadressen worden de land-/regiospecifieke regels afgedwongen.</span><span class="sxs-lookup"><span data-stu-id="8e68b-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="8e68b-110">Wanneer klanten een verzendadres invoeren tijdens de betalingsstroom, hebben ze de optie om het adres op te slaan als een primair adres.</span><span class="sxs-lookup"><span data-stu-id="8e68b-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="8e68b-111">Deze optie wordt alleen weergegeven als een klant is aangemeld.</span><span class="sxs-lookup"><span data-stu-id="8e68b-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="8e68b-112">Hoewel de module voor verzendadressen geen adresvalidatie biedt, kunt u deze functie implementeren via aanpassingen.</span><span class="sxs-lookup"><span data-stu-id="8e68b-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="8e68b-113">De volgende afbeelding toont een voorbeeld van een nieuwe verzendadresmodule op een betalingspagina.</span><span class="sxs-lookup"><span data-stu-id="8e68b-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Voorbeeld van een module voor verzendadressen op een betalingspagina](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="8e68b-115">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="8e68b-115">Module properties</span></span>

| <span data-ttu-id="8e68b-116">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="8e68b-116">Property name</span></span> | <span data-ttu-id="8e68b-117">Waarden</span><span class="sxs-lookup"><span data-stu-id="8e68b-117">Values</span></span> | <span data-ttu-id="8e68b-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8e68b-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8e68b-119">Kop</span><span class="sxs-lookup"><span data-stu-id="8e68b-119">Heading</span></span> | <span data-ttu-id="8e68b-120">Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="8e68b-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="8e68b-121">Een optionele koptekst voor de module voor verzendadressen.</span><span class="sxs-lookup"><span data-stu-id="8e68b-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="8e68b-122">Adrestype weergeven</span><span class="sxs-lookup"><span data-stu-id="8e68b-122">Show address type</span></span> | <span data-ttu-id="8e68b-123">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="8e68b-123">**True** or **False**</span></span> | <span data-ttu-id="8e68b-124">Als deze eigenschap is ingesteld op **Waar**, wordt een adrestype weergegeven, zoals **Thuis** of **Werk**.</span><span class="sxs-lookup"><span data-stu-id="8e68b-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="8e68b-125">Als u geen adrestype opgeeft, wordt het adres automatisch opgeslagen als **Type**=**Overig**.</span><span class="sxs-lookup"><span data-stu-id="8e68b-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="8e68b-126">Automatische suggestie inschakelen</span><span class="sxs-lookup"><span data-stu-id="8e68b-126">Enable auto suggestion</span></span>| <span data-ttu-id="8e68b-127">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="8e68b-127">**True** or **False**</span></span> | <span data-ttu-id="8e68b-128">Als deze optionele eigenschap is ingesteld op **True**, worden automatische adressuggesties geleverd.</span><span class="sxs-lookup"><span data-stu-id="8e68b-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="8e68b-129">Deze suggesties worden aangeboden door Bing Kaarten.</span><span class="sxs-lookup"><span data-stu-id="8e68b-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="8e68b-130">Zie [Winkelselectiemodule](store-selector.md) voor informatie over het instellen van integratie met Bing Kaarten voor uw site.</span><span class="sxs-lookup"><span data-stu-id="8e68b-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="8e68b-131">Deze functie is beschikbaar vanaf Commerce-versie 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="8e68b-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="8e68b-132">Opties voor automatische suggesties</span><span class="sxs-lookup"><span data-stu-id="8e68b-132">Auto suggest options</span></span>| <span data-ttu-id="8e68b-133">Aantal</span><span class="sxs-lookup"><span data-stu-id="8e68b-133">A number</span></span>| <span data-ttu-id="8e68b-134">Als automatische adressuggesties zijn ingeschakeld, kunt u aanvullende opties opgeven, zoals het maximale aantal suggesties dat moet worden verstrekt.</span><span class="sxs-lookup"><span data-stu-id="8e68b-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="8e68b-135">Een module voor verzendadressen aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen</span><span class="sxs-lookup"><span data-stu-id="8e68b-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="8e68b-136">Een module voor verzendadressen kan alleen aan een uitcheckmodule worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="8e68b-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="8e68b-137">Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van de module voor verzendadressen en het toevoegen ervan aan een uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="8e68b-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e68b-138">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="8e68b-138">Additional resources</span></span>

[<span data-ttu-id="8e68b-139">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="8e68b-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8e68b-140">Module voor winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="8e68b-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8e68b-141">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="8e68b-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8e68b-142">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="8e68b-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="8e68b-143">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="8e68b-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="8e68b-144">Module met afhaalinformatie</span><span class="sxs-lookup"><span data-stu-id="8e68b-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="8e68b-145">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="8e68b-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8e68b-146">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="8e68b-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="8e68b-147">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="8e68b-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]