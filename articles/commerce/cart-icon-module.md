---
title: Module winkelwagenpictogram
description: In dit onderwerp wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 138c256b56593c4fafb20050a97e614fa584597c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997820"
---
# <a name="cart-icon-module"></a><span data-ttu-id="57781-103">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="57781-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57781-104">In dit onderwerp wordt beschreven wat de module winkelwagenpictogram is en hoe u deze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="57781-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="57781-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="57781-105">Overview</span></span>

<span data-ttu-id="57781-106">De module winkelwagenpictogram geeft de winkelwagen weer in de koptekstmodule van de pagina en toont het aantal artikelen in de winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="57781-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="57781-107">De module winkelwagenpictogram geeft ook een overzicht van winkelwagen (ook wel minikar genoemd) wanneer de cursor boven het winkelwagenpictogram wordt gehouden.</span><span class="sxs-lookup"><span data-stu-id="57781-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="57781-108">De minikar geeft de gebruiker een overzicht van de artikelen in de winkelwagen zonder dat u naar de pagina Winkelwagen hoeft te navigeren.</span><span class="sxs-lookup"><span data-stu-id="57781-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="57781-109">Daarnaast kunnen gebruikers ook rechtstreeks naar de afhandelingspagina gaan als ze tevreden zijn over het overzicht.</span><span class="sxs-lookup"><span data-stu-id="57781-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="57781-110">Hierdoor is er minder paginanavigatie nodig en wordt de afhandeling versneld.</span><span class="sxs-lookup"><span data-stu-id="57781-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="57781-111">Ondersteuning voor de winkelwagenpictogrammodule is beschikbaar in Dynamics 365 Commerce versie 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="57781-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="57781-112">De volgende afbeelding toont een voorbeeld van een winkelwagenpictogrammodule waarin een minikar wordt weergegeven in de Fabrikam-koptekst.</span><span class="sxs-lookup"><span data-stu-id="57781-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Voorbeeld van een winkelwagenpictogrammodule](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="57781-114">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="57781-114">Module properties</span></span>

- <span data-ttu-id="57781-115">**Minikar weergeven**: indien waar, kan met deze eigenschap een winkelwagenoverzicht (minikar) worden weergegeven wanneer de cursor boven het winkelwagenpictogram wordt gehouden.</span><span class="sxs-lookup"><span data-stu-id="57781-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="57781-116">Deze functionaliteit wordt alleen ondersteund voor viewports op een bureaublad.</span><span class="sxs-lookup"><span data-stu-id="57781-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="57781-117">Een module winkelwagenpictogram toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="57781-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="57781-118">Zie [Koptekstmodule](author-header-module.md) om een module winkelwagenpictogram toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="57781-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57781-119">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="57781-119">Additional resources</span></span>

[<span data-ttu-id="57781-120">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="57781-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="57781-121">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="57781-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="57781-122">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="57781-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="57781-123">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="57781-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="57781-124">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="57781-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="57781-125">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="57781-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="57781-126">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="57781-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="57781-127">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="57781-127">Gift card module</span></span>](add-giftcard.md)
