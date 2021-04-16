---
title: Geschenkbonmodule
description: In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797666"
---
# <a name="gift-card-module"></a><span data-ttu-id="4c7ad-103">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="4c7ad-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4c7ad-104">In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4c7ad-105">Geschenkbonmodules kunnen worden gebruikt in kasmodules om geschenkbonnen te accepteren, een algemene betalingswijze voor e-Commerce-transacties.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="4c7ad-106">De geschenkbonmodule ondersteunt Dynamics 365, SVS en Givex-geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="4c7ad-107">SVS- en Givex geschenkbonnen worden ingewisseld via de Adyen-betalingsprovider.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="4c7ad-108">Zie [Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md) voor meer informatie over ondersteuning voor externe geschenkbonnen, zoals SVS en Givex.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4c7ad-109">Ondersteuning voor het inwisselen van SVS- en Givex-geschenkbonnen tijdens de afrekenstroom is beschikbaar in Dynamics 365 Commerce versie 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="4c7ad-110">Er zijn twee geschenkbonmodules beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="4c7ad-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="4c7ad-111">**Geschenkbon**: deze module kan worden gebruikt op een kassapagina om een geschenkbon als betalingsmethode in te wisselen.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="4c7ad-112">**Saldocontrole geschenkbon**: deze module kan op elke pagina worden gebruikt om het saldo op een geschenkbon te controleren.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="4c7ad-113">Deze module is beschikbaar in Commerce-versies 10.0.14 en hoger.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="4c7ad-114">Ondersteuning voor de module saldocontrole voor geschenkbonnen is beschikbaar in Dynamics 365 Commerce versie 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="4c7ad-115">De volgende afbeelding toont een voorbeeld van een geschenkbonmodule op een betalingspagina.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Voorbeeld van een geschenkbonmodule](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="4c7ad-117">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="4c7ad-117">Module properties</span></span>

- <span data-ttu-id="4c7ad-118">**Extra velden weergeven**: met deze eigenschap wordt gedefinieerd welke velden voor geschenkbonnen moeten worden weergegeven naast het nummer van de geschenkbon, dat altijd standaard wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="4c7ad-119">Sommige geschenkbonnen ondersteunen bijvoorbeeld het weergeven van een persoonlijk identificatienummer (PIN) en andere bieden ondersteuning voor het weergeven van een pincode en een vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="4c7ad-120">Het kan ook zijn dat deze eigenschap is ingesteld op "Geen", zodat alleen het nummer van de geschenkbon en geen extra velden worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="4c7ad-121">Ondersteunde waarden:</span><span class="sxs-lookup"><span data-stu-id="4c7ad-121">Supported values:</span></span>
-   <span data-ttu-id="4c7ad-122">Pincode</span><span class="sxs-lookup"><span data-stu-id="4c7ad-122">PIN</span></span>
-   <span data-ttu-id="4c7ad-123">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="4c7ad-123">Expiration date</span></span>
-   <span data-ttu-id="4c7ad-124">PIN en vervaldatum</span><span class="sxs-lookup"><span data-stu-id="4c7ad-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="4c7ad-125">None</span><span class="sxs-lookup"><span data-stu-id="4c7ad-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="4c7ad-126">Site-instellingen voor geschenkbonmodules</span><span class="sxs-lookup"><span data-stu-id="4c7ad-126">Site settings for gift card modules</span></span>

<span data-ttu-id="4c7ad-127">In Commerce Site Builder onder **Site-instellingen \> Uitbreidingen** is er een geschenkbonmodule met de naam **Ondersteund geschenkbontype**.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="4c7ad-128">Deze instelling ondersteunt drie waarden:</span><span class="sxs-lookup"><span data-stu-id="4c7ad-128">This setting supports three values:</span></span>
- <span data-ttu-id="4c7ad-129">**Dynamics 365-geschenkbon**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="4c7ad-130">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="4c7ad-131">**SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="4c7ad-132">Deze instelling wordt alleen ondersteund voor aangemelde en anonieme gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="4c7ad-133">**Dynamics 365-, SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-, SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="4c7ad-134">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c7ad-135">Deze instellingen zijn beschikbaar in Dynamics 365 Commerce versie 10.0.11 en zijn alleen vereist als u ondersteuning nodig hebt voor SVS- of Givex-geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="4c7ad-136">Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="4c7ad-137">Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor instructies voor het bijwerken van het appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="4c7ad-138">Een geschenkbonmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="4c7ad-138">Add a gift card module to a page</span></span>

<span data-ttu-id="4c7ad-139">Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een geschenkbonmodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="4c7ad-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c7ad-140">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="4c7ad-140">Additional resources</span></span>

[<span data-ttu-id="4c7ad-141">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="4c7ad-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4c7ad-142">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="4c7ad-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4c7ad-143">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="4c7ad-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4c7ad-144">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="4c7ad-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="4c7ad-145">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="4c7ad-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="4c7ad-146">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="4c7ad-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="4c7ad-147">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="4c7ad-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="4c7ad-148">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="4c7ad-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4c7ad-149">Ondersteuning voor externe geschenkbonnen</span><span class="sxs-lookup"><span data-stu-id="4c7ad-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="4c7ad-150">Updates voor SDK's en modulebibliotheken</span><span class="sxs-lookup"><span data-stu-id="4c7ad-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]