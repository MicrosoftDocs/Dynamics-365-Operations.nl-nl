---
title: Betalingsmodule
description: In dit onderwerp wordt de betalingsmodule beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818321"
---
# <a name="payment-module"></a><span data-ttu-id="a39a1-103">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="a39a1-103">Payment module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a39a1-104">In dit onderwerp wordt de betalingsmodule beschreven en uitgelegd hoe u deze configureert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a39a1-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a39a1-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="a39a1-105">Overview</span></span>

<span data-ttu-id="a39a1-106">De betalingsmodule laat klanten betalen voor orders met behulp van creditcards of debitcards.</span><span class="sxs-lookup"><span data-stu-id="a39a1-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="a39a1-107">Integratie van betalingen voor deze module wordt verzorgd door de Dynamics 365-betalingsconnector voor Adyen.</span><span class="sxs-lookup"><span data-stu-id="a39a1-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="a39a1-108">Raadpleeg [Dynamics 365-betalingsconnector voor Adyen](dev-itpro/adyen-connector.md) voor meer informatie over het instellen en configureren van de Adyen-betalingsconnector.</span><span class="sxs-lookup"><span data-stu-id="a39a1-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="a39a1-109">De betalingsmodule beheert de betalingsgegevens die via Adyen in een HTML inline frame (iFrame) worden aangeleverd.</span><span class="sxs-lookup"><span data-stu-id="a39a1-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="a39a1-110">De betalingsmodule communiceert met de Commerce Scale Unit om de Adyen-betalingsgegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="a39a1-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="a39a1-111">Als onderdeel van de Commerce Scale Unit-interactie kan de betalingsmodule toestaan dat factuuradresgegevens worden verwerkt in het iFrame of als een afzonderlijke module.</span><span class="sxs-lookup"><span data-stu-id="a39a1-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="a39a1-112">In het thema Fabrikam wordt het factuuradres in een aparte module weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a39a1-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="a39a1-113">Deze aanpak biedt meer flexibele opmaakmogelijkheden, omdat de adresregels zo kunnen worden weergegeven dat ze lijken op de regels van het verzendadres.</span><span class="sxs-lookup"><span data-stu-id="a39a1-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="a39a1-114">Aangemelde klanten kunnen in de betalingsmodule ook hun betalingsgegevens opslaan.</span><span class="sxs-lookup"><span data-stu-id="a39a1-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="a39a1-115">De betalingsgegevens en het factuuradres worden opgeslagen en beheerd via de Adyen-betalingsconnector.</span><span class="sxs-lookup"><span data-stu-id="a39a1-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="a39a1-116">De betalingsmodule omvat alle orderkosten die nog niet zijn gedekt door loyaliteitspunten of een geschenkbon.</span><span class="sxs-lookup"><span data-stu-id="a39a1-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="a39a1-117">Als het totaal van een order volledig wordt gedekt door loyaliteitspunten of geschenkbonnen, wordt de betalingsmodule verborgen en kan de klant de order zonder de module plaatsen.</span><span class="sxs-lookup"><span data-stu-id="a39a1-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="a39a1-118">De Adyen-betalingsconnector ondersteunt ook sterke klantverificatie (SCA).</span><span class="sxs-lookup"><span data-stu-id="a39a1-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="a39a1-119">Als onderdeel van de EU-richtlijn voor betalingsdiensten 2.0 (PSD 2.0) van de Europese Unie is vereist dat online klanten worden geverifieerd buiten hun online winkelervaring wanneer ze een elektronische betalingsmethode gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a39a1-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="a39a1-120">Tijdens het afhandelingsverkeer worden klanten omgeleid naar hun banksite.</span><span class="sxs-lookup"><span data-stu-id="a39a1-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="a39a1-121">Na de verificatie worden ze vervolgens omgeleid naar de Commerce-afhandelingsstroom.</span><span class="sxs-lookup"><span data-stu-id="a39a1-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="a39a1-122">Tijdens deze omleiding blijft de informatie behouden die een klant heeft ingevoerd in de checkoutstroom (bijvoorbeeld het verzendadres, de leveringsopties, informatie over geschenkbonnen en loyaliteitsgegevens).</span><span class="sxs-lookup"><span data-stu-id="a39a1-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="a39a1-123">Voordat u deze functie kunt inschakelen, moet de betalingsconnector worden geconfigureerd voor SCA in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="a39a1-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="a39a1-124">Zie voor meer informatie [Sterke klantverificatie met Adyen](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="a39a1-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="a39a1-125">De volgende afbeelding toont een voorbeeld van de modules voor geschenkbon, loyaliteitspunten en betaling op een uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="a39a1-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Voorbeeld van modules voor geschenkbonnen, loyaliteitspunten en betalingen op een uitcheckpagina](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="a39a1-127">Eigenschappen van betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="a39a1-127">Payment module properties</span></span>

| <span data-ttu-id="a39a1-128">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="a39a1-128">Property name</span></span> | <span data-ttu-id="a39a1-129">Waarden</span><span class="sxs-lookup"><span data-stu-id="a39a1-129">Values</span></span> | <span data-ttu-id="a39a1-130">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a39a1-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="a39a1-131">Kop</span><span class="sxs-lookup"><span data-stu-id="a39a1-131">Heading</span></span> | <span data-ttu-id="a39a1-132">Koptekst</span><span class="sxs-lookup"><span data-stu-id="a39a1-132">Heading text</span></span> | <span data-ttu-id="a39a1-133">Een optionele koptekst voor de betalingsmodule.</span><span class="sxs-lookup"><span data-stu-id="a39a1-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="a39a1-134">De hoogte van het iFrame.</span><span class="sxs-lookup"><span data-stu-id="a39a1-134">Height of the iframe</span></span> | <span data-ttu-id="a39a1-135">Pixel</span><span class="sxs-lookup"><span data-stu-id="a39a1-135">Pixels</span></span> | <span data-ttu-id="a39a1-136">De hoogte van het iFrame, in pixels.</span><span class="sxs-lookup"><span data-stu-id="a39a1-136">The iframe height, in pixels.</span></span> <span data-ttu-id="a39a1-137">De hoogte kan zo nodig worden aangepast.</span><span class="sxs-lookup"><span data-stu-id="a39a1-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="a39a1-138">Factureringsadres weergeven</span><span class="sxs-lookup"><span data-stu-id="a39a1-138">Show billing address</span></span> | <span data-ttu-id="a39a1-139">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="a39a1-139">**True** or **False**</span></span> | <span data-ttu-id="a39a1-140">Als deze eigenschap is ingesteld op **Waar**, wordt het factuuradres door Adyen geleverd binnen het iFrame van de betalingsmodule.</span><span class="sxs-lookup"><span data-stu-id="a39a1-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="a39a1-141">Als de eigenschap is ingesteld op **Onwaar**, wordt het factuuradres niet aangeleverd door Adyen en moet een Commerce-gebruiker een module configureren om het factuuradres op de uitcheckpagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="a39a1-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="a39a1-142">Betalingsstijl overschrijven</span><span class="sxs-lookup"><span data-stu-id="a39a1-142">Payment style override</span></span> | <span data-ttu-id="a39a1-143">Cascading Style Sheets-code (CSS)</span><span class="sxs-lookup"><span data-stu-id="a39a1-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="a39a1-144">Omdat de betalingsmodule wordt gehost in een iFrame, zijn er beperkte opmaakmogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="a39a1-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="a39a1-145">U kunt opmaak aanbrengen met behulp van deze eigenschap.</span><span class="sxs-lookup"><span data-stu-id="a39a1-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="a39a1-146">Als u sitestijlen wilt overschrijven, plakt u de CSS-code als waarde voor deze eigenschap.</span><span class="sxs-lookup"><span data-stu-id="a39a1-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="a39a1-147">Overschrijvingen en stijlen van site builder-CSS zijn niet van toepassing op deze module.</span><span class="sxs-lookup"><span data-stu-id="a39a1-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="a39a1-148">Factureringsadres</span><span class="sxs-lookup"><span data-stu-id="a39a1-148">Billing address</span></span>

<span data-ttu-id="a39a1-149">De betalingsmodule laat klanten een factuuradres opgeven voor hun betalingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="a39a1-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="a39a1-150">Ook kunnen ze hun verzendadres gebruiken als het factuuradres, zodat de afhandelingsprocedure eenvoudiger en sneller wordt.</span><span class="sxs-lookup"><span data-stu-id="a39a1-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="a39a1-151">Als de eigenschap **Factureringsadres weergeven** is ingesteld op **Onwaar**, moet de betalingsmodule worden geconfigureerd op de uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="a39a1-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="a39a1-152">Een betalingsmodule aan een uitcheckpagina toevoegen en de vereiste eigenschappen instellen</span><span class="sxs-lookup"><span data-stu-id="a39a1-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="a39a1-153">Een betalingsmodule kan alleen aan een uitcheckmodule worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="a39a1-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="a39a1-154">Zie [Kassamodule](add-checkout-module.md) voor meer informatie over het configureren van een betalingsmodule voor een kassapagina.</span><span class="sxs-lookup"><span data-stu-id="a39a1-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a39a1-155">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="a39a1-155">Additional resources</span></span>

[<span data-ttu-id="a39a1-156">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="a39a1-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a39a1-157">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="a39a1-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a39a1-158">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="a39a1-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a39a1-159">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="a39a1-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a39a1-160">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="a39a1-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a39a1-161">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="a39a1-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a39a1-162">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="a39a1-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="a39a1-163">Dynamics 365-betalingsconnector voor Adyen</span><span class="sxs-lookup"><span data-stu-id="a39a1-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="a39a1-164">SCA (sterke klantverificatie) met Adyen-connector</span><span class="sxs-lookup"><span data-stu-id="a39a1-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
