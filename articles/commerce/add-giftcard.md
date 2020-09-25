---
title: Geschenkbonmodule
description: In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761076"
---
# <a name="gift-card-module"></a><span data-ttu-id="d5e0d-103">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="d5e0d-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d5e0d-104">In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d5e0d-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="d5e0d-105">Overview</span></span>

<span data-ttu-id="d5e0d-106">Geschenkbonmodules kunnen worden gebruikt in kasmodules om geschenkbonnen te accepteren, een algemene betalingswijze voor e-Commerce-transacties.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="d5e0d-107">De geschenkbonmodule ondersteunt Dynamics 365, SVS en Givex-geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="d5e0d-108">SVS- en Givex geschenkbonnen worden ingewisseld via de Adyen-betalingsprovider.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="d5e0d-109">Zie [Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md) voor meer informatie over ondersteuning voor externe geschenkbonnen, zoals SVS en Givex.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="d5e0d-110">Er zijn twee geschenkbonmodules beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="d5e0d-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="d5e0d-111">**Geschenkbon**: deze module kan worden gebruikt op een kassapagina om een geschenkbon als betalingsmethode in te wisselen.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="d5e0d-112">**Saldocontrole geschenkbon**: deze module kan op elke pagina worden gebruikt om het saldo op een geschenkbon te controleren.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="d5e0d-113">Deze module is beschikbaar in Commerce-versies 10.0.14 en hoger.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="d5e0d-114">De volgende afbeelding toont een voorbeeld van een geschenkbonmodule op een betalingspagina.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Voorbeeld van een geschenkbonmodule](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="d5e0d-116">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="d5e0d-116">Module properties</span></span>

- <span data-ttu-id="d5e0d-117">**Extra velden weergeven**: met deze eigenschap wordt gedefinieerd welke velden voor geschenkbonnen moeten worden weergegeven naast het nummer van de geschenkbon, dat altijd standaard wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="d5e0d-118">Sommige geschenkbonnen ondersteunen bijvoorbeeld het weergeven van een persoonlijk identificatienummer (PIN) en andere bieden ondersteuning voor het weergeven van een pincode en een vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="d5e0d-119">Het kan ook zijn dat deze eigenschap is ingesteld op "Geen", zodat alleen het nummer van de geschenkbon en geen extra velden worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="d5e0d-120">Ondersteunde waarden:</span><span class="sxs-lookup"><span data-stu-id="d5e0d-120">Supported values:</span></span>
-   <span data-ttu-id="d5e0d-121">Pincode</span><span class="sxs-lookup"><span data-stu-id="d5e0d-121">PIN</span></span>
-   <span data-ttu-id="d5e0d-122">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d5e0d-122">Expiration date</span></span>
-   <span data-ttu-id="d5e0d-123">PIN en vervaldatum</span><span class="sxs-lookup"><span data-stu-id="d5e0d-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="d5e0d-124">None</span><span class="sxs-lookup"><span data-stu-id="d5e0d-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="d5e0d-125">Site-instellingen voor geschenkbonmodules</span><span class="sxs-lookup"><span data-stu-id="d5e0d-125">Site settings for gift card modules</span></span>

<span data-ttu-id="d5e0d-126">In Commerce Site Builder onder **Site-instellingen \> Uitbreidingen** is er een geschenkbonmodule met de naam **Ondersteund geschenkbontype**.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="d5e0d-127">Deze instelling ondersteunt drie waarden:</span><span class="sxs-lookup"><span data-stu-id="d5e0d-127">This setting supports three values:</span></span>
- <span data-ttu-id="d5e0d-128">**Dynamics 365-geschenkbon**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="d5e0d-129">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="d5e0d-130">**SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="d5e0d-131">Deze instelling wordt alleen ondersteund voor aangemelde en anonieme gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="d5e0d-132">**Dynamics 365-, SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-, SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="d5e0d-133">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="d5e0d-134">Een geschenkbonmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="d5e0d-134">Add a gift card module to a page</span></span>

<span data-ttu-id="d5e0d-135">Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een geschenkbonmodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="d5e0d-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5e0d-136">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d5e0d-136">Additional resources</span></span>

[<span data-ttu-id="d5e0d-137">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="d5e0d-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d5e0d-138">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="d5e0d-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d5e0d-139">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="d5e0d-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d5e0d-140">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="d5e0d-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d5e0d-141">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="d5e0d-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d5e0d-142">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="d5e0d-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d5e0d-143">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="d5e0d-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d5e0d-144">Ondersteuning voor externe geschenkbonnen</span><span class="sxs-lookup"><span data-stu-id="d5e0d-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
