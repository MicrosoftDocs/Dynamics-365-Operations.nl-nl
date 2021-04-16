---
title: Orderbevestigingsmodule
description: In dit onderwerp wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze gebruikt in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f8742637cc8ed29abcfb9a8061a8d2602762d4f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804572"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="c1894-103">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="c1894-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c1894-104">In dit onderwerp wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze gebruikt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c1894-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c1894-105">De module voor orderbevestiging wordt gebruikt om orderbevestigingsdetails weer te geven nadat een order is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="c1894-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="c1894-106">De id van de orderbevestiging, de contactgegevens van de order en andere ordergegevens worden weergegeven, zoals de gekochte artikelen, betalingsgegevens, ophaalopties en de verzendmethode.</span><span class="sxs-lookup"><span data-stu-id="c1894-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="c1894-107">Eigenschappen van orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="c1894-107">Order confirmation module properties</span></span>

| <span data-ttu-id="c1894-108">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="c1894-108">Property name</span></span>  | <span data-ttu-id="c1894-109">Waarden</span><span class="sxs-lookup"><span data-stu-id="c1894-109">Values</span></span> | <span data-ttu-id="c1894-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c1894-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="c1894-111">Koptekst</span><span class="sxs-lookup"><span data-stu-id="c1894-111">Heading</span></span>        | <span data-ttu-id="c1894-112">Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="c1894-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="c1894-113">De orderbevestigingsmodule kan een koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="c1894-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="c1894-114">Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="c1894-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="c1894-115">De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="c1894-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="c1894-116">Contactnummer</span><span class="sxs-lookup"><span data-stu-id="c1894-116">Contact number</span></span> | <span data-ttu-id="c1894-117">Text</span><span class="sxs-lookup"><span data-stu-id="c1894-117">Text</span></span> | <span data-ttu-id="c1894-118">Er kan een contactnummer worden opgegeven voor vragen met betrekking tot de order.</span><span class="sxs-lookup"><span data-stu-id="c1894-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="c1894-119">Informatie over tijdvak voor ophalen weergeven</span><span class="sxs-lookup"><span data-stu-id="c1894-119">Show pickup timeslot information</span></span> | <span data-ttu-id="c1894-120">Waar of onwaar</span><span class="sxs-lookup"><span data-stu-id="c1894-120">True or False</span></span> | <span data-ttu-id="c1894-121">Deze eigenschap is beschikbaar in Dynamics 365 Commerce 10.0.15 en hoger.</span><span class="sxs-lookup"><span data-stu-id="c1894-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="c1894-122">Indien van toepassing, wordt de informatie over het tijdvak voor ophalen weergegeven als deze is opgegeven voor een op te halen artikel</span><span class="sxs-lookup"><span data-stu-id="c1894-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="c1894-123">Modules die kunnen worden gebruikt op een pagina met orderbevestiging</span><span class="sxs-lookup"><span data-stu-id="c1894-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="c1894-124">Wanneer u een pagina met orderbevestiging maakt, kunt u behalve de module voor orderdetails ook andere relevante bevestigingsmodules toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c1894-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="c1894-125">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="c1894-125">Here are some examples:</span></span>

- <span data-ttu-id="c1894-126">**Aanbevelingsmodule**: de aanbevelingsmodule kan aan de pagina met orderbevestiging worden toegevoegd om suggesties voor andere producten te doen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="c1894-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="c1894-127">**Marketingmodules**: elke marketingmodule kan worden toegevoegd aan de pagina met orderbevestiging om marketinginhoud weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c1894-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="c1894-128">Een module voor orderbevestiging toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="c1894-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="c1894-129">Voer de volgende stappen uit om een module voor orderbevestiging aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="c1894-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c1894-130">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="c1894-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c1894-131">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** de naam in voor **Sjabloon voor orderbevestiging** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1894-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c1894-132">Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c1894-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c1894-133">Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1894-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c1894-134">Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c1894-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c1894-135">Selecteer in het dialoogvenster **Module toevoegen** de **Module voor orderbevestiging** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1894-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c1894-136">Selecteer **Opslaan** en vervolgens **Preview** om de sjabloon te bekijken.</span><span class="sxs-lookup"><span data-stu-id="c1894-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="c1894-137">De orderbevestigingsmodule wordt niet weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.</span><span class="sxs-lookup"><span data-stu-id="c1894-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="c1894-138">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="c1894-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c1894-139">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="c1894-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c1894-140">Selecteer in het dialoogvenster **Een sjabloon kiezen** de **Sjabloon voor orderbevestiging**.</span><span class="sxs-lookup"><span data-stu-id="c1894-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="c1894-141">Voer onder **Paginanaam** **Pagina voor orderbevestiging** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1894-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c1894-142">Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c1894-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c1894-143">Selecteer in het dialoogvenster **Module toevoegen** de **Module voor orderbevestiging** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1894-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c1894-144">Selecteer in het eigenschappenvenster van de module voor orderbevestiging de optie **Kop** naast het potloodsymbool.</span><span class="sxs-lookup"><span data-stu-id="c1894-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="c1894-145">Voer in het veld **Koptekst** van het dialoogvenster **Koptekst** de koptekst **Orderbevestiging** in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1894-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="c1894-146">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="c1894-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="c1894-147">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="c1894-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1894-148">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c1894-148">Additional resources</span></span>

[<span data-ttu-id="c1894-149">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="c1894-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c1894-150">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="c1894-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c1894-151">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="c1894-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c1894-152">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="c1894-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="c1894-153">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="c1894-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="c1894-154">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="c1894-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="c1894-155">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="c1894-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="c1894-156">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="c1894-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]