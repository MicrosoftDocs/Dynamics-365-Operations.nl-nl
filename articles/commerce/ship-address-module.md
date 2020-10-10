---
title: Module voor verzendadressen
description: In dit onderwerp wordt de module voor verzendadressen beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7233b23020e6c82f39981d530095642902461807
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818393"
---
# <a name="shipping-address-module"></a><span data-ttu-id="dff43-103">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="dff43-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dff43-104">In dit onderwerp wordt de module voor verzendadressen beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dff43-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dff43-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="dff43-105">Overview</span></span>

<span data-ttu-id="dff43-106">Met de module voor verzendadressen kan een klant het verzendadres voor een order toevoegen of selecteren tijdens de betalingsstroom.</span><span class="sxs-lookup"><span data-stu-id="dff43-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="dff43-107">Als een klant is aangemeld, worden alle adressen weergegeven die eerder voor die klant zijn opgeslagen en de klant kan een adres selecteren.</span><span class="sxs-lookup"><span data-stu-id="dff43-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="dff43-108">De klant kan ook een nieuw adres toevoegen.</span><span class="sxs-lookup"><span data-stu-id="dff43-108">The customer can also add a new address.</span></span> <span data-ttu-id="dff43-109">De module voor verzendadressen wordt gebruikt voor alle artikelen in de order waarvoor verzending is vereist.</span><span class="sxs-lookup"><span data-stu-id="dff43-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="dff43-110">U kunt verzendadresnotaties definiëren in Commerce Headquarters voor elk land of elke regio en met de module voor verzendadressen worden de land-/regiospecifieke regels afgedwongen.</span><span class="sxs-lookup"><span data-stu-id="dff43-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="dff43-111">Wanneer klanten een verzendadres invoeren tijdens de betalingsstroom, hebben ze de optie om het adres op te slaan als een primair adres.</span><span class="sxs-lookup"><span data-stu-id="dff43-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="dff43-112">Deze optie wordt alleen weergegeven als een klant is aangemeld.</span><span class="sxs-lookup"><span data-stu-id="dff43-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="dff43-113">Hoewel de module voor verzendadressen geen adresvalidatie biedt, kunt u deze functie implementeren via aanpassingen.</span><span class="sxs-lookup"><span data-stu-id="dff43-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="dff43-114">De volgende afbeelding toont een voorbeeld van een nieuwe verzendadresmodule op een betalingspagina.</span><span class="sxs-lookup"><span data-stu-id="dff43-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Voorbeeld van een module voor verzendadressen op een betalingspagina](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="dff43-116">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="dff43-116">Module properties</span></span>

| <span data-ttu-id="dff43-117">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="dff43-117">Property name</span></span> | <span data-ttu-id="dff43-118">Waarden</span><span class="sxs-lookup"><span data-stu-id="dff43-118">Values</span></span> | <span data-ttu-id="dff43-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dff43-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="dff43-120">Kop</span><span class="sxs-lookup"><span data-stu-id="dff43-120">Heading</span></span> | <span data-ttu-id="dff43-121">Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="dff43-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="dff43-122">Een optionele koptekst voor de module voor verzendadressen.</span><span class="sxs-lookup"><span data-stu-id="dff43-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="dff43-123">Adrestype weergeven</span><span class="sxs-lookup"><span data-stu-id="dff43-123">Show address type</span></span> | <span data-ttu-id="dff43-124">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="dff43-124">**True** or **False**</span></span> | <span data-ttu-id="dff43-125">Als deze eigenschap is ingesteld op **Waar**, wordt een adrestype weergegeven, zoals **Thuis** of **Werk**.</span><span class="sxs-lookup"><span data-stu-id="dff43-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="dff43-126">Als u geen adrestype opgeeft, wordt het adres automatisch opgeslagen als **Type**=**Overig**.</span><span class="sxs-lookup"><span data-stu-id="dff43-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="dff43-127">Een module voor verzendadressen aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen</span><span class="sxs-lookup"><span data-stu-id="dff43-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="dff43-128">Een module voor verzendadressen kan alleen aan een uitcheckmodule worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="dff43-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="dff43-129">Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van de module voor verzendadressen en het toevoegen ervan aan een uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="dff43-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dff43-130">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="dff43-130">Additional resources</span></span>

[<span data-ttu-id="dff43-131">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="dff43-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="dff43-132">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="dff43-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="dff43-133">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="dff43-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="dff43-134">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="dff43-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="dff43-135">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="dff43-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="dff43-136">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="dff43-136">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="dff43-137">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="dff43-137">Gift card module</span></span>](add-giftcard.md)
