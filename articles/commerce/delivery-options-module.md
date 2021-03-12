---
title: Module voor leveringsopties
description: In dit onderwerp worden modules voor leveringsopties beschreven en toegelicht hoe u ze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 9d8945348cbe3255ecc497f129d125ad11e9ceab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000844"
---
# <a name="delivery-options-module"></a><span data-ttu-id="361cd-103">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="361cd-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="361cd-104">In dit onderwerp worden modules voor leveringsopties beschreven en toegelicht hoe u ze configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="361cd-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="361cd-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="361cd-105">Overview</span></span>

<span data-ttu-id="361cd-106">Met de modules voor leveringsopties kunnen klanten een leveringsmethode selecteren voor hun online bestelling, zoals verzending of ophalen.</span><span class="sxs-lookup"><span data-stu-id="361cd-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="361cd-107">Voor het bepalen van de leveringsmethode is een verzendadres vereist.</span><span class="sxs-lookup"><span data-stu-id="361cd-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="361cd-108">Als het verzendadres wordt gewijzigd, moeten de leveringsopties weer worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="361cd-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="361cd-109">Als een order alleen de artikelen bevat die worden opgehaald in een winkel, wordt deze module automatisch verborgen.</span><span class="sxs-lookup"><span data-stu-id="361cd-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="361cd-110">Zie [Online kanaal instellen](channel-setup-online.md) en [Leveringsmethoden instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) voor informatie over het configureren van leveringsmethoden.</span><span class="sxs-lookup"><span data-stu-id="361cd-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="361cd-111">Aan elke leveringsmethode kunnen kosten zijn verbonden.</span><span class="sxs-lookup"><span data-stu-id="361cd-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="361cd-112">Zie [Geavanceerde automatische toeslagen voor meerdere kanalen](omni-auto-charges.md) voor meer informatie over het configureren van toeslagen voor een online winkel.</span><span class="sxs-lookup"><span data-stu-id="361cd-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="361cd-113">In Commerce versie 10.0.13 is de module voor leveringsopties bijgewerkt met ondersteuning voor de functies **Toeslagen voor koptekst zonder afstemming naar rato** en **Verzending als regelkosten**.</span><span class="sxs-lookup"><span data-stu-id="361cd-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="361cd-114">Als de betaling naar rato is uitgeschakeld, staat de e-Commerce-werkstroom geen gecombineerde leveringsmethode voor artikelen in de winkelwagen toe (dat wil zeggen dat sommige artikelen voor verzending zijn geselecteerd, maar andere zijn geselecteerd om te worden opgehaald).</span><span class="sxs-lookup"><span data-stu-id="361cd-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="361cd-115">Voor de functie **Toeslagen voor koptekst zonder afstemming naar rato** is vereist dat de markering **Consistente afhandeling van afleveringsmodus in kanaal inschakelen** in Commerce Headquarters is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="361cd-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="361cd-116">Wanneer deze markering is ingeschakeld, worden de verzendkosten toegepast op het koptekstniveau of op regelniveau, afhankelijk van de configuratie in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="361cd-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="361cd-117">Het Fabrikam-thema ondersteunt een gemengde leveringsmethode, waarbij sommige artikelen voor verzending zijn geselecteerd, maar andere voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="361cd-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="361cd-118">Bij deze methode worden de verzendkosten evenredig verdeeld over alle artikelen die zijn geselecteerd voor de leveringsmethode.</span><span class="sxs-lookup"><span data-stu-id="361cd-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="361cd-119">Voor een gemengde leveringsmethode moet u eerst de functie **Toeslagen voor koptekst zonder afstemming naar rato** in Commerce Headquarters configureren.</span><span class="sxs-lookup"><span data-stu-id="361cd-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="361cd-120">Zie [Toeslagen voor koptekst naar rato afstemmen op verkoopregels](pro-rate-charges-matching-lines.md) voor meer informatie over deze configuratie.</span><span class="sxs-lookup"><span data-stu-id="361cd-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="361cd-121">Als verzendkosten van toepassing zijn op regelartikelen, kunnen deze worden weergegeven op de winkelwagenregel voor elk artikel.</span><span class="sxs-lookup"><span data-stu-id="361cd-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="361cd-122">Voor deze functionaliteit moet de eigenschap **Verzendkosten voor regelartikel weergeven** worden ingeschakeld voor zowel de winkelwagenmodule als de kassamodule.</span><span class="sxs-lookup"><span data-stu-id="361cd-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="361cd-123">Zie [Winkelwagenmodule](add-cart-module.md) en [Kassamodule](add-checkout-module.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="361cd-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="361cd-124">De volgende afbeelding toont een voorbeeld van een leveringsoptiemodule op een uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="361cd-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Voorbeeld van een module voor leveringsopties op een uitcheckpagina](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="361cd-126">Eigenschappen van module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="361cd-126">Delivery options module properties</span></span>

| <span data-ttu-id="361cd-127">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="361cd-127">Property</span></span> | <span data-ttu-id="361cd-128">Waarden</span><span class="sxs-lookup"><span data-stu-id="361cd-128">Values</span></span> | <span data-ttu-id="361cd-129">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="361cd-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="361cd-130">Kop</span><span class="sxs-lookup"><span data-stu-id="361cd-130">Heading</span></span> | <span data-ttu-id="361cd-131">Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="361cd-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="361cd-132">Een optionele koptekst voor de module voor leveringsopties.</span><span class="sxs-lookup"><span data-stu-id="361cd-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="361cd-133">Naam aangepaste CSS-klasse</span><span class="sxs-lookup"><span data-stu-id="361cd-133">Custom CSS class name</span></span> | <span data-ttu-id="361cd-134">Tekst</span><span class="sxs-lookup"><span data-stu-id="361cd-134">Text</span></span> | <span data-ttu-id="361cd-135">Een aangepaste klassenaam voor Cascading Style Sheets (CSS) die wordt gebruikt om deze module weer te geven, indien van toepassing.</span><span class="sxs-lookup"><span data-stu-id="361cd-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="361cd-136">Optie voor filteren op leveringsmodus</span><span class="sxs-lookup"><span data-stu-id="361cd-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="361cd-137">**Niet filteren** of **Niet-verzendmethoden**</span><span class="sxs-lookup"><span data-stu-id="361cd-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="361cd-138">Een waarde die aangeeft of de module voor leveringsopties alle afleveringsmodi voor niet-verzending eruit moet filteren.</span><span class="sxs-lookup"><span data-stu-id="361cd-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="361cd-139">Een module voor leveringsopties aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen</span><span class="sxs-lookup"><span data-stu-id="361cd-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="361cd-140">Een module voor leveringsopties kan alleen aan een uitcheckmodule worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="361cd-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="361cd-141">Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van de module voor leveringsopties en het toevoegen ervan aan een uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="361cd-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="361cd-142">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="361cd-142">Additional resources</span></span>

[<span data-ttu-id="361cd-143">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="361cd-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="361cd-144">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="361cd-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="361cd-145">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="361cd-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="361cd-146">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="361cd-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="361cd-147">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="361cd-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="361cd-148">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="361cd-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="361cd-149">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="361cd-149">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="361cd-150">Online afzetkanaal instellen</span><span class="sxs-lookup"><span data-stu-id="361cd-150">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="361cd-151">Geavanceerde automatische toeslagen voor meerdere kanalen</span><span class="sxs-lookup"><span data-stu-id="361cd-151">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="361cd-152">Toeslagen voor koptekst naar rato afstemmen op verkoopregels</span><span class="sxs-lookup"><span data-stu-id="361cd-152">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="361cd-153">Leveringsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="361cd-153">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
