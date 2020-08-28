---
title: Geschenkbonmodule
description: In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 41f808d671bf5e7425390484ea30470e044899d8
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661237"
---
# <a name="gift-card-module"></a><span data-ttu-id="434f7-103">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="434f7-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="434f7-104">In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="434f7-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="434f7-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="434f7-105">Overview</span></span>

<span data-ttu-id="434f7-106">Geschenkbonnen vormen een algemene betalingswijze en de geschenkbonmodule kan in een kassamodule worden gebruikt om geschenkbonnen te accepteren.</span><span class="sxs-lookup"><span data-stu-id="434f7-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="434f7-107">De geschenkbonmodule ondersteunt Dynamics 365, SVS en Givex-geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="434f7-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="434f7-108">SVS- en Givex geschenkbonnen worden ingewisseld via de Adyen-betalingsprovider.</span><span class="sxs-lookup"><span data-stu-id="434f7-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="434f7-109">Zie [Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md) voor meer informatie over ondersteuning voor externe geschenkbonnen, zoals SVS en Givex.</span><span class="sxs-lookup"><span data-stu-id="434f7-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="434f7-110">De volgende afbeelding toont een voorbeeld van een geschenkbonmodule op een betalingspagina.</span><span class="sxs-lookup"><span data-stu-id="434f7-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Voorbeeld van een geschenkbonmodule](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="434f7-112">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="434f7-112">Module properties</span></span>

- <span data-ttu-id="434f7-113">**Extra velden weergeven**: met deze eigenschap wordt gedefinieerd welke velden voor geschenkbonnen moeten worden weergegeven naast het nummer van de geschenkbon, dat altijd standaard wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="434f7-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="434f7-114">Sommige geschenkbonnen ondersteunen bijvoorbeeld het weergeven van een persoonlijk identificatienummer (PIN) en andere bieden ondersteuning voor het weergeven van een pincode en een vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="434f7-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="434f7-115">Het kan ook zijn dat deze eigenschap is ingesteld op "Geen", zodat alleen het nummer van de geschenkbon en geen extra velden worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="434f7-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="434f7-116">Ondersteunde waarden:</span><span class="sxs-lookup"><span data-stu-id="434f7-116">Supported values:</span></span>
-   <span data-ttu-id="434f7-117">Pincode</span><span class="sxs-lookup"><span data-stu-id="434f7-117">PIN</span></span>
-   <span data-ttu-id="434f7-118">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="434f7-118">Expiration date</span></span>
-   <span data-ttu-id="434f7-119">PIN en vervaldatum</span><span class="sxs-lookup"><span data-stu-id="434f7-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="434f7-120">None</span><span class="sxs-lookup"><span data-stu-id="434f7-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="434f7-121">Site-instellingen voor geschenkbonmodules</span><span class="sxs-lookup"><span data-stu-id="434f7-121">Site settings for gift card modules</span></span>

<span data-ttu-id="434f7-122">In Commerce Site Builder onder **Site-instellingen \> Uitbreidingen** is er een geschenkbonmodule met de naam **Ondersteund geschenkbontype**.</span><span class="sxs-lookup"><span data-stu-id="434f7-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="434f7-123">Deze instelling ondersteunt drie waarden:</span><span class="sxs-lookup"><span data-stu-id="434f7-123">This setting supports three values:</span></span>
- <span data-ttu-id="434f7-124">**Dynamics 365-geschenkbon**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="434f7-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="434f7-125">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="434f7-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="434f7-126">**SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="434f7-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="434f7-127">Deze instelling wordt alleen ondersteund voor aangemelde en anonieme gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="434f7-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="434f7-128">**Dynamics 365-, SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-, SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="434f7-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="434f7-129">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="434f7-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="434f7-130">Een geschenkbonmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="434f7-130">Add a gift card module to a page</span></span>

<span data-ttu-id="434f7-131">Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een geschenkbonmodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="434f7-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="434f7-132">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="434f7-132">Additional resources</span></span>

[<span data-ttu-id="434f7-133">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="434f7-133">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="434f7-134">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="434f7-134">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="434f7-135">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="434f7-135">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="434f7-136">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="434f7-136">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="434f7-137">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="434f7-137">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="434f7-138">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="434f7-138">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="434f7-139">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="434f7-139">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="434f7-140">Ondersteuning voor externe geschenkbonnen</span><span class="sxs-lookup"><span data-stu-id="434f7-140">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
