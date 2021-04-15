---
title: Module winkelwagenpictogram
description: In dit onderwerp wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793076"
---
# <a name="cart-icon-module"></a><span data-ttu-id="b2cc1-103">Module voor winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="b2cc1-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2cc1-104">In dit onderwerp wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b2cc1-105">De module winkelwagenpictogram geeft de winkelwagen weer in de koptekstmodule van de pagina en toont het aantal artikelen in de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="b2cc1-106">De module winkelwagenpictogram geeft ook een overzicht van winkelwagen (ook wel minikar genoemd) wanneer de cursor boven het winkelwagenpictogram wordt gehouden.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="b2cc1-107">De minikar geeft de gebruiker een overzicht van de artikelen in de winkelwagen zonder dat u naar de pagina Winkelwagen hoeft te navigeren.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="b2cc1-108">Daarnaast kunnen gebruikers ook rechtstreeks naar de afhandelingspagina gaan als ze tevreden zijn over het overzicht.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="b2cc1-109">Hierdoor is er minder paginanavigatie nodig en wordt de afhandeling versneld.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="b2cc1-110">Ondersteuning voor de winkelwagenpictogrammodule is beschikbaar in Dynamics 365 Commerce versie 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="b2cc1-111">De volgende afbeelding toont een voorbeeld van een winkelwagenpictogrammodule waarin een minikar wordt weergegeven in de Fabrikam-koptekst.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Voorbeeld van een winkelwagenpictogrammodule](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="b2cc1-113">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="b2cc1-113">Module properties</span></span>

- <span data-ttu-id="b2cc1-114">**Minikar weergeven**: indien waar, kan met deze eigenschap een winkelwagenoverzicht (minikar) worden weergegeven wanneer de cursor boven het winkelwagenpictogram wordt gehouden.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="b2cc1-115">Deze functionaliteit wordt alleen ondersteund voor viewports op een bureaublad.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="b2cc1-116">Een module winkelwagenpictogram toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="b2cc1-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="b2cc1-117">Zie [Koptekstmodule](author-header-module.md) om een module winkelwagenpictogram toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b2cc1-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2cc1-118">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b2cc1-118">Additional resources</span></span>

[<span data-ttu-id="b2cc1-119">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="b2cc1-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b2cc1-120">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="b2cc1-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b2cc1-121">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="b2cc1-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b2cc1-122">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="b2cc1-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b2cc1-123">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="b2cc1-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b2cc1-124">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="b2cc1-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b2cc1-125">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="b2cc1-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b2cc1-126">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="b2cc1-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]