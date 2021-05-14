---
title: Geschenkbonmodule
description: In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/29/2021
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
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962758"
---
# <a name="gift-card-module"></a><span data-ttu-id="22a74-103">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="22a74-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="22a74-104">In dit onderwerp worden geschenkbonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="22a74-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="22a74-105">Geschenkbonmodules kunnen worden gebruikt in kasmodules om geschenkbonnen te accepteren, een algemene betalingswijze voor e-Commerce-transacties.</span><span class="sxs-lookup"><span data-stu-id="22a74-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="22a74-106">De geschenkbonmodule ondersteunt Dynamics 365, SVS en Givex-geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="22a74-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="22a74-107">SVS- en Givex geschenkbonnen worden ingewisseld via de Adyen-betalingsprovider.</span><span class="sxs-lookup"><span data-stu-id="22a74-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="22a74-108">Zie [Ondersteuning voor externe geschenkbonnen](./dev-itpro/gift-card.md) voor meer informatie over ondersteuning voor externe geschenkbonnen, zoals SVS en Givex.</span><span class="sxs-lookup"><span data-stu-id="22a74-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="22a74-109">Ondersteuning voor het inwisselen van SVS- en Givex-geschenkbonnen tijdens de afrekenstroom is beschikbaar in Dynamics 365 Commerce versie 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="22a74-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="22a74-110">Er zijn twee geschenkbonmodules beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="22a74-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="22a74-111">**Geschenkbon**: deze module kan worden gebruikt op een kassapagina om een geschenkbon als betalingsmethode in te wisselen.</span><span class="sxs-lookup"><span data-stu-id="22a74-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="22a74-112">**Saldocontrole geschenkbon**: deze module kan op elke pagina worden gebruikt om het saldo op een geschenkbon te controleren.</span><span class="sxs-lookup"><span data-stu-id="22a74-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="22a74-113">Deze module is beschikbaar in Commerce-versies 10.0.14 en hoger.</span><span class="sxs-lookup"><span data-stu-id="22a74-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="22a74-114">Ondersteuning voor de module saldocontrole voor geschenkbonnen is beschikbaar in Dynamics 365 Commerce versie 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="22a74-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="22a74-115">De volgende afbeelding toont een voorbeeld van een geschenkbonmodule op een betalingspagina.</span><span class="sxs-lookup"><span data-stu-id="22a74-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Voorbeeld van een geschenkbonmodule](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="22a74-117">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="22a74-117">Module properties</span></span>

- <span data-ttu-id="22a74-118">**Extra velden weergeven**: met deze eigenschap wordt gedefinieerd welke velden voor geschenkbonnen moeten worden weergegeven naast het nummer van de geschenkbon, dat altijd standaard wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22a74-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="22a74-119">Sommige geschenkbonnen ondersteunen bijvoorbeeld het weergeven van een persoonlijk identificatienummer (PIN) en andere bieden ondersteuning voor het weergeven van een pincode en een vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="22a74-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="22a74-120">Het kan ook zijn dat deze eigenschap is ingesteld op "Geen", zodat alleen het nummer van de geschenkbon en geen extra velden worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="22a74-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="22a74-121">Ondersteunde waarden:</span><span class="sxs-lookup"><span data-stu-id="22a74-121">Supported values:</span></span>
-   <span data-ttu-id="22a74-122">Pincode</span><span class="sxs-lookup"><span data-stu-id="22a74-122">PIN</span></span>
-   <span data-ttu-id="22a74-123">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="22a74-123">Expiration date</span></span>
-   <span data-ttu-id="22a74-124">PIN en vervaldatum</span><span class="sxs-lookup"><span data-stu-id="22a74-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="22a74-125">None</span><span class="sxs-lookup"><span data-stu-id="22a74-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="22a74-126">Site-instellingen voor geschenkbonmodules</span><span class="sxs-lookup"><span data-stu-id="22a74-126">Site settings for gift card modules</span></span>

<span data-ttu-id="22a74-127">In Commerce Site Builder onder **Site-instellingen \> Uitbreidingen** is er een geschenkbonmodule met de naam **Ondersteund geschenkbontype**.</span><span class="sxs-lookup"><span data-stu-id="22a74-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="22a74-128">Deze instelling ondersteunt drie waarden:</span><span class="sxs-lookup"><span data-stu-id="22a74-128">This setting supports three values:</span></span>
- <span data-ttu-id="22a74-129">**Dynamics 365-geschenkbon**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="22a74-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="22a74-130">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="22a74-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="22a74-131">**SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="22a74-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="22a74-132">Deze instelling wordt alleen ondersteund voor aangemelde en anonieme gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="22a74-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="22a74-133">**Dynamics 365-, SVS- en Givex-geschenkbonnen**: wanneer deze instelling wordt toegepast, staat de geschenkbonmodule alleen toe dat er Dynamics 365-, SVS- en Givex-geschenkbonnen worden ingewisseld.</span><span class="sxs-lookup"><span data-stu-id="22a74-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="22a74-134">Deze instelling wordt alleen ondersteund voor aangemelde gebruikers op de e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="22a74-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22a74-135">Deze instellingen zijn beschikbaar in Dynamics 365 Commerce versie 10.0.11 en zijn alleen vereist als u ondersteuning nodig hebt voor SVS- of Givex-geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="22a74-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="22a74-136">Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken.</span><span class="sxs-lookup"><span data-stu-id="22a74-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="22a74-137">Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor instructies voor het bijwerken van het appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="22a74-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="22a74-138">Interne geschenkbonnen uitbreiden voor gebruik in webwinkels</span><span class="sxs-lookup"><span data-stu-id="22a74-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="22a74-139">Interne geschenkbonnen zijn standaard niet geoptimaliseerd voor gebruik in webwinkels.</span><span class="sxs-lookup"><span data-stu-id="22a74-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="22a74-140">Voordat u toestaat dat interne geschenkbonnen worden gebruikt voor betaling, moet u deze daarom configureren met uitbreidingen die ze veiliger maken.</span><span class="sxs-lookup"><span data-stu-id="22a74-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="22a74-141">Dit zijn de gebieden voor geschenkbonnen die u moet uitbreiden voordat u toestaat dat interne geschenkbonnen worden gebruikt in de productie:</span><span class="sxs-lookup"><span data-stu-id="22a74-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="22a74-142">**Nummer geschenkbon**: nummerreeksen worden gebruikt om geschenkkaartnummers te genereren voor interne geschenkbonnen.</span><span class="sxs-lookup"><span data-stu-id="22a74-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="22a74-143">Aangezien nummerreeksen kunnen worden voorspeld, moet u het genereren van geschenkbonnummers uitbreiden zodat willekeurige, cryptografisch beveiligde tekenreeksen worden gebruikt voor de uitgegeven geschenkbonnummers.</span><span class="sxs-lookup"><span data-stu-id="22a74-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="22a74-144">**GetBalance**: De **GetBalance**-API wordt gebruikt om saldi van geschenkbonnen op te zoeken.</span><span class="sxs-lookup"><span data-stu-id="22a74-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="22a74-145">Deze API is standaard openbaar.</span><span class="sxs-lookup"><span data-stu-id="22a74-145">By default, this API public.</span></span> <span data-ttu-id="22a74-146">Als geen pincode vereist is om geschenkbonsaldi op te zoeken, kan het risico bestaan dat met de **GetBalance**-API wordt geprobeerd geschenkbonnummers met saldo op te zoeken.</span><span class="sxs-lookup"><span data-stu-id="22a74-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="22a74-147">Als u de pincode vereist stelt voor interne geschenkbonnen en ook API-beperking implementeert, kunt u dit risico beperken.</span><span class="sxs-lookup"><span data-stu-id="22a74-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="22a74-148">**Pincode**: Interne geschenkbonnen ondersteunen standaard geen pincode.</span><span class="sxs-lookup"><span data-stu-id="22a74-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="22a74-149">U moet interne geschenkbonnen uitbreiden zodat een pincode nodig is om het saldo op te zoeken.</span><span class="sxs-lookup"><span data-stu-id="22a74-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="22a74-150">Deze functionaliteit kan ook worden gebruikt om geschenkbonnen te vergrendelen nadat enkele malen achter elkaar een verkeerde pincode is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="22a74-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="22a74-151">Geschenkbonbetalingen voor gastbetalingen inschakelen</span><span class="sxs-lookup"><span data-stu-id="22a74-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="22a74-152">Betalingen van geschenkbonnen zijn standaard niet ingeschakeld voor gastbetalingen (anonieme betalingen).</span><span class="sxs-lookup"><span data-stu-id="22a74-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="22a74-153">U kunt deze als volgt inschakelen:</span><span class="sxs-lookup"><span data-stu-id="22a74-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="22a74-154">Ga in Commerce Headquarters naar **Retail en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> POS-bewerkingen**.</span><span class="sxs-lookup"><span data-stu-id="22a74-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="22a74-155">Selecteer de koptekst van het raster en houd deze vast (of klik met de rechtermuisknop) en selecteer **Kolommen invoegen**.</span><span class="sxs-lookup"><span data-stu-id="22a74-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="22a74-156">Schakel in het dialoogvenster **Kolommen invoegen** het selectievakje **AllowAnonymousAccess** in.</span><span class="sxs-lookup"><span data-stu-id="22a74-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="22a74-157">Selecteer **Bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="22a74-157">Select **Update**.</span></span>
1. <span data-ttu-id="22a74-158">Stel voor bewerkingen **520** (Geschenkbonsaldo) en **214** de waarde **AllowAnonymousAccess** in op **1**.</span><span class="sxs-lookup"><span data-stu-id="22a74-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="22a74-159">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="22a74-159">Select **Save**.</span></span>
1. <span data-ttu-id="22a74-160">Voer de planningstaak **1090** uit om wijzigingen te synchroniseren naar de kanaaldatabase.</span><span class="sxs-lookup"><span data-stu-id="22a74-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="22a74-161">Een geschenkbonmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="22a74-161">Add a gift card module to a page</span></span>

<span data-ttu-id="22a74-162">Zie [Kassamodule](add-checkout-module.md) voor instructies over het toevoegen van een geschenkbonmodule aan een uitcheckpagina en het instellen van de vereiste eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="22a74-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22a74-163">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="22a74-163">Additional resources</span></span>

[<span data-ttu-id="22a74-164">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="22a74-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="22a74-165">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="22a74-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="22a74-166">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="22a74-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="22a74-167">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="22a74-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="22a74-168">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="22a74-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="22a74-169">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="22a74-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="22a74-170">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="22a74-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="22a74-171">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="22a74-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="22a74-172">Ondersteuning voor externe geschenkbonnen</span><span class="sxs-lookup"><span data-stu-id="22a74-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="22a74-173">Updates voor SDK's en modulebibliotheken</span><span class="sxs-lookup"><span data-stu-id="22a74-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
