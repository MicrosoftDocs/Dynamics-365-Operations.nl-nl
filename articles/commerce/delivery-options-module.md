---
title: Module voor leveringsopties
description: In dit onderwerp worden modules voor leveringsopties beschreven en toegelicht hoe u ze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: 8342afefa6eeda3a53decb39caddb62d1e4e1963
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270856"
---
# <a name="delivery-options-module"></a><span data-ttu-id="514c7-103">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="514c7-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="514c7-104">In dit onderwerp worden modules voor leveringsopties beschreven en toegelicht hoe u ze configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="514c7-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="514c7-105">Met de modules voor leveringsopties kunnen klanten een leveringsmethode selecteren voor hun online bestelling, zoals verzending of ophalen.</span><span class="sxs-lookup"><span data-stu-id="514c7-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="514c7-106">Voor het bepalen van de leveringsmethode is een verzendadres vereist.</span><span class="sxs-lookup"><span data-stu-id="514c7-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="514c7-107">Als het verzendadres wordt gewijzigd, moeten de leveringsopties weer worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="514c7-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="514c7-108">Als een order alleen de artikelen bevat die worden opgehaald in een winkel, wordt deze module automatisch verborgen.</span><span class="sxs-lookup"><span data-stu-id="514c7-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="514c7-109">Zie [Online kanaal instellen](channel-setup-online.md) en [Leveringsmethoden instellen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor informatie over het configureren van leveringsmethoden.</span><span class="sxs-lookup"><span data-stu-id="514c7-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="514c7-110">Aan elke leveringsmethode kunnen kosten zijn verbonden.</span><span class="sxs-lookup"><span data-stu-id="514c7-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="514c7-111">Zie [Geavanceerde automatische toeslagen voor meerdere kanalen](omni-auto-charges.md) voor meer informatie over het configureren van toeslagen voor een online winkel.</span><span class="sxs-lookup"><span data-stu-id="514c7-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="514c7-112">In Commerce versie 10.0.13 is de module voor leveringsopties bijgewerkt met ondersteuning voor de functies **Toeslagen voor koptekst zonder afstemming naar rato** en **Verzending als regelkosten**.</span><span class="sxs-lookup"><span data-stu-id="514c7-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="514c7-113">Als de betaling naar rato is uitgeschakeld, staat de e-Commerce-werkstroom geen gecombineerde leveringsmethode voor artikelen in de winkelwagen toe (dat wil zeggen dat sommige artikelen voor verzending zijn geselecteerd, maar andere zijn geselecteerd om te worden opgehaald).</span><span class="sxs-lookup"><span data-stu-id="514c7-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="514c7-114">Voor de functie **Toeslagen voor koptekst zonder afstemming naar rato** is vereist dat de markering **Consistente afhandeling van afleveringsmodus in kanaal inschakelen** in Commerce Headquarters is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="514c7-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="514c7-115">Wanneer deze functiemarkering is ingeschakeld, worden de verzendkosten toegepast op het koptekstniveau of op regelniveau, afhankelijk van de configuratie in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="514c7-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="514c7-116">Het Fabrikam-thema ondersteunt een gemengde leveringsmethode, waarbij sommige artikelen voor verzending zijn geselecteerd, maar andere voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="514c7-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="514c7-117">Bij deze methode worden de verzendkosten evenredig verdeeld over alle artikelen die zijn geselecteerd voor de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="514c7-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="514c7-118">Voor een gemengde leveringsmethode moet u eerst de functie **Toeslagen voor koptekst zonder afstemming naar rato** in Commerce Headquarters configureren.</span><span class="sxs-lookup"><span data-stu-id="514c7-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="514c7-119">Zie [Toeslagen voor koptekst naar rato afstemmen op verkoopregels](pro-rate-charges-matching-lines.md) voor meer informatie over deze configuratie.</span><span class="sxs-lookup"><span data-stu-id="514c7-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="514c7-120">Als verzendkosten van toepassing zijn op regelartikelen, kunnen deze worden weergegeven op de winkelwagenregel voor elk artikel.</span><span class="sxs-lookup"><span data-stu-id="514c7-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="514c7-121">Voor deze functionaliteit moet de eigenschap **Verzendkosten voor regelartikel weergeven** worden ingeschakeld voor zowel de winkelwagenmodule als de kassamodule.</span><span class="sxs-lookup"><span data-stu-id="514c7-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="514c7-122">Zie [Winkelwagenmodule](add-cart-module.md) en [Kassamodule](add-checkout-module.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="514c7-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="514c7-123">De volgende afbeelding toont een voorbeeld van een leveringsoptiemodule op een uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="514c7-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Voorbeeld van een module voor leveringsopties op een uitcheckpagina](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="514c7-125">Eigenschappen van module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="514c7-125">Delivery options module properties</span></span>

| <span data-ttu-id="514c7-126">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="514c7-126">Property</span></span> | <span data-ttu-id="514c7-127">Waarden</span><span class="sxs-lookup"><span data-stu-id="514c7-127">Values</span></span> | <span data-ttu-id="514c7-128">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="514c7-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="514c7-129">Kop</span><span class="sxs-lookup"><span data-stu-id="514c7-129">Heading</span></span> | <span data-ttu-id="514c7-130">Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="514c7-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="514c7-131">Een optionele koptekst voor de module voor leveringsopties.</span><span class="sxs-lookup"><span data-stu-id="514c7-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="514c7-132">Naam aangepaste CSS-klasse</span><span class="sxs-lookup"><span data-stu-id="514c7-132">Custom CSS class name</span></span> | <span data-ttu-id="514c7-133">Tekst</span><span class="sxs-lookup"><span data-stu-id="514c7-133">Text</span></span> | <span data-ttu-id="514c7-134">Een aangepaste klassenaam voor Cascading Style Sheets (CSS) die wordt gebruikt om deze module weer te geven, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="514c7-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="514c7-135">Optie voor filteren op leveringsmodus</span><span class="sxs-lookup"><span data-stu-id="514c7-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="514c7-136">**Niet filteren** of **Niet-verzendmethoden**</span><span class="sxs-lookup"><span data-stu-id="514c7-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="514c7-137">Een waarde die aangeeft of de module voor leveringsopties alle afleveringsmodi voor niet-verzending eruit moet filteren.</span><span class="sxs-lookup"><span data-stu-id="514c7-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="514c7-138">Automatisch een leveringsoptie selecteren</span><span class="sxs-lookup"><span data-stu-id="514c7-138">Auto select a delivery option</span></span> | <span data-ttu-id="514c7-139">**Niet filteren**, **Leveringsoptie automatisch selecteren en overzicht tonen** of **Leveringsoptie automatisch selecteren en geen overzicht tonen**</span><span class="sxs-lookup"><span data-stu-id="514c7-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="514c7-140">Deze eigenschap past automatisch de eerste beschikbare leveringsoptie toe bij het afrekenen zonder dat de gebruiker deze moet selecteren.</span><span class="sxs-lookup"><span data-stu-id="514c7-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="514c7-141">Gebruik deze optie alleen als er één leveringsoptie beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="514c7-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="514c7-142">Deze eigenschap wordt ondersteund in Commerce vanaf versie 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="514c7-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="514c7-143">Een module voor leveringsopties aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen</span><span class="sxs-lookup"><span data-stu-id="514c7-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="514c7-144">Een module voor leveringsopties kan alleen aan een uitcheckmodule worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="514c7-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="514c7-145">Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van de module voor leveringsopties en het toevoegen ervan aan een uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="514c7-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="514c7-146">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="514c7-146">Additional resources</span></span>

[<span data-ttu-id="514c7-147">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="514c7-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="514c7-148">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="514c7-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="514c7-149">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="514c7-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="514c7-150">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="514c7-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="514c7-151">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="514c7-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="514c7-152">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="514c7-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="514c7-153">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="514c7-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="514c7-154">Online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="514c7-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="514c7-155">Geavanceerde automatische toeslagen voor meerdere kanalen</span><span class="sxs-lookup"><span data-stu-id="514c7-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="514c7-156">Toeslagen voor koptekst naar rato afstemmen op verkoopregels</span><span class="sxs-lookup"><span data-stu-id="514c7-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="514c7-157">Leveringsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="514c7-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
