---
title: Geschenkbonmodule
description: In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9626f33ced0433bc96ed58429e95d4f75af6508
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980377"
---
# <a name="gift-card-module"></a><span data-ttu-id="f1e89-103">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="f1e89-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1e89-104">In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1e89-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f1e89-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="f1e89-105">Overview</span></span>

<span data-ttu-id="f1e89-106">Geschenkbonmodules kunnen worden gebruikt in kasmodules om geschenkbonnen te accepteren, een algemene betalingswijze voor e-Commerce-transacties.</span><span class="sxs-lookup"><span data-stu-id="f1e89-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="f1e89-107">De geschenkbonmodule ondersteunt Dynamics 365, SVS en Givex-geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="f1e89-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="f1e89-108">SVS- en Givex geschenkbonnen worden ingewisseld via de Adyen-betalingsprovider.</span><span class="sxs-lookup"><span data-stu-id="f1e89-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="f1e89-109">Zie [Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md) voor meer informatie over ondersteuning voor externe geschenkbonnen, zoals SVS en Givex.</span><span class="sxs-lookup"><span data-stu-id="f1e89-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f1e89-110">Ondersteuning voor het inwisselen van SVS- en Givex-geschenkbonnen tijdens de afrekenstroom is beschikbaar in Dynamics 365 Commerce versie 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="f1e89-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="f1e89-111">Er zijn twee geschenkbonmodules beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="f1e89-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="f1e89-112">**Geschenkbon**: deze module kan worden gebruikt op een kassapagina om een geschenkbon als betalingsmethode in te wisselen.</span><span class="sxs-lookup"><span data-stu-id="f1e89-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="f1e89-113">**Saldocontrole geschenkbon**: deze module kan op elke pagina worden gebruikt om het saldo op een geschenkbon te controleren.</span><span class="sxs-lookup"><span data-stu-id="f1e89-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="f1e89-114">Deze module is beschikbaar in Commerce-versies 10.0.14 en hoger.</span><span class="sxs-lookup"><span data-stu-id="f1e89-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="f1e89-115">Ondersteuning voor de module saldocontrole voor geschenkbonnen is beschikbaar in Dynamics 365 Commerce versie 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="f1e89-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="f1e89-116">De volgende afbeelding toont een voorbeeld van een geschenkbonmodule op een betalingspagina.</span><span class="sxs-lookup"><span data-stu-id="f1e89-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Voorbeeld van een geschenkbonmodule](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="f1e89-118">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="f1e89-118">Module properties</span></span>

- <span data-ttu-id="f1e89-119">**Extra velden weergeven**: met deze eigenschap wordt gedefinieerd welke velden voor geschenkbonnen moeten worden weergegeven naast het nummer van de geschenkbon, dat altijd standaard wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f1e89-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="f1e89-120">Sommige geschenkbonnen ondersteunen bijvoorbeeld het weergeven van een persoonlijk identificatienummer (PIN) en andere bieden ondersteuning voor het weergeven van een pincode en een vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="f1e89-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="f1e89-121">Het kan ook zijn dat deze eigenschap is ingesteld op "Geen", zodat alleen het nummer van de geschenkbon en geen extra velden worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f1e89-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="f1e89-122">Ondersteunde waarden:</span><span class="sxs-lookup"><span data-stu-id="f1e89-122">Supported values:</span></span>
-   <span data-ttu-id="f1e89-123">Pincode</span><span class="sxs-lookup"><span data-stu-id="f1e89-123">PIN</span></span>
-   <span data-ttu-id="f1e89-124">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="f1e89-124">Expiration date</span></span>
-   <span data-ttu-id="f1e89-125">PIN en vervaldatum</span><span class="sxs-lookup"><span data-stu-id="f1e89-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="f1e89-126">None</span><span class="sxs-lookup"><span data-stu-id="f1e89-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="f1e89-127">Site-instellingen voor geschenkbonmodules</span><span class="sxs-lookup"><span data-stu-id="f1e89-127">Site settings for gift card modules</span></span>

<span data-ttu-id="f1e89-128">In Commerce Site Builder onder **Site-instellingen \> Uitbreidingen** is er een geschenkbonmodule met de naam **Ondersteund geschenkbontype**.</span><span class="sxs-lookup"><span data-stu-id="f1e89-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="f1e89-129">Deze instelling ondersteunt drie waarden:</span><span class="sxs-lookup"><span data-stu-id="f1e89-129">This setting supports three values:</span></span>
- <span data-ttu-id="f1e89-130">**Dynamics 365-geschenkbon**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="f1e89-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="f1e89-131">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="f1e89-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="f1e89-132">**SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="f1e89-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="f1e89-133">Deze instelling wordt alleen ondersteund voor aangemelde en anonieme gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="f1e89-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="f1e89-134">**Dynamics 365-, SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-, SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="f1e89-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="f1e89-135">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="f1e89-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1e89-136">Deze instellingen zijn beschikbaar in Dynamics 365 Commerce versie 10.0.11 en zijn alleen vereist als u ondersteuning nodig hebt voor SVS- of Givex-geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="f1e89-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="f1e89-137">Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken.</span><span class="sxs-lookup"><span data-stu-id="f1e89-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="f1e89-138">Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor instructies voor het bijwerken van het appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="f1e89-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="f1e89-139">Een geschenkbonmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="f1e89-139">Add a gift card module to a page</span></span>

<span data-ttu-id="f1e89-140">Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een geschenkbonmodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="f1e89-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1e89-141">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="f1e89-141">Additional resources</span></span>

[<span data-ttu-id="f1e89-142">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="f1e89-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f1e89-143">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="f1e89-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f1e89-144">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="f1e89-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f1e89-145">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="f1e89-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f1e89-146">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="f1e89-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="f1e89-147">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="f1e89-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f1e89-148">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="f1e89-148">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="f1e89-149">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="f1e89-149">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f1e89-150">Ondersteuning voor externe geschenkbonnen</span><span class="sxs-lookup"><span data-stu-id="f1e89-150">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="f1e89-151">Updates voor SDK's en modulebibliotheken</span><span class="sxs-lookup"><span data-stu-id="f1e89-151">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
