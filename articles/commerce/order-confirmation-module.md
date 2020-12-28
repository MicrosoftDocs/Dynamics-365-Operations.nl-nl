---
title: Orderbevestigingsmodule
description: In dit onderwerp wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze gebruikt in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bf33ebf9c0c5136f40fcd7e1012988d186c4169b
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/07/2020
ms.locfileid: "4411540"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="c79ae-103">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="c79ae-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c79ae-104">In dit onderwerp wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze gebruikt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c79ae-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c79ae-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="c79ae-105">Overview</span></span>

<span data-ttu-id="c79ae-106">De module voor orderbevestiging wordt gebruikt om orderbevestigingsdetails weer te geven nadat een order is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="c79ae-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="c79ae-107">De id van de orderbevestiging, de contactgegevens van de order en andere ordergegevens worden weergegeven, zoals de gekochte artikelen, betalingsgegevens, ophaalopties en de verzendmethode.</span><span class="sxs-lookup"><span data-stu-id="c79ae-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="c79ae-108">Eigenschappen van orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="c79ae-108">Order confirmation module properties</span></span>

| <span data-ttu-id="c79ae-109">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="c79ae-109">Property name</span></span>  | <span data-ttu-id="c79ae-110">Waarden</span><span class="sxs-lookup"><span data-stu-id="c79ae-110">Values</span></span> | <span data-ttu-id="c79ae-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c79ae-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="c79ae-112">Koptekst</span><span class="sxs-lookup"><span data-stu-id="c79ae-112">Heading</span></span>        | <span data-ttu-id="c79ae-113">Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="c79ae-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="c79ae-114">De orderbevestigingsmodule kan een koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="c79ae-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="c79ae-115">Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="c79ae-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="c79ae-116">De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="c79ae-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="c79ae-117">Contactnummer</span><span class="sxs-lookup"><span data-stu-id="c79ae-117">Contact number</span></span> | <span data-ttu-id="c79ae-118">Text</span><span class="sxs-lookup"><span data-stu-id="c79ae-118">Text</span></span> | <span data-ttu-id="c79ae-119">Er kan een contactnummer worden opgegeven voor vragen met betrekking tot de order.</span><span class="sxs-lookup"><span data-stu-id="c79ae-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="c79ae-120">Informatie over tijdvak voor ophalen weergeven</span><span class="sxs-lookup"><span data-stu-id="c79ae-120">Show pickup timeslot information</span></span> | <span data-ttu-id="c79ae-121">Waar of onwaar</span><span class="sxs-lookup"><span data-stu-id="c79ae-121">True or False</span></span> | <span data-ttu-id="c79ae-122">Deze eigenschap is beschikbaar in Dynamics 365 Commerce 10.0.15 en hoger.</span><span class="sxs-lookup"><span data-stu-id="c79ae-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="c79ae-123">Indien van toepassing, wordt de informatie over het tijdvak voor ophalen weergegeven als deze is opgegeven voor een op te halen artikel</span><span class="sxs-lookup"><span data-stu-id="c79ae-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="c79ae-124">Modules die kunnen worden gebruikt op een pagina met orderbevestiging</span><span class="sxs-lookup"><span data-stu-id="c79ae-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="c79ae-125">Wanneer u een pagina met orderbevestiging maakt, kunt u behalve de module voor orderdetails ook andere relevante bevestigingsmodules toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c79ae-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="c79ae-126">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="c79ae-126">Here are some examples:</span></span>

- <span data-ttu-id="c79ae-127">**Aanbevelingsmodule**: de aanbevelingsmodule kan aan de pagina met orderbevestiging worden toegevoegd om suggesties voor andere producten te doen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="c79ae-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="c79ae-128">**Marketingmodules**: elke marketingmodule kan worden toegevoegd aan de pagina met orderbevestiging om marketinginhoud weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c79ae-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="c79ae-129">Een module voor orderbevestiging toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="c79ae-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="c79ae-130">Voer de volgende stappen uit om een module voor orderbevestiging aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="c79ae-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c79ae-131">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="c79ae-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c79ae-132">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** de naam in voor **Sjabloon voor orderbevestiging** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c79ae-133">Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c79ae-134">Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c79ae-135">Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c79ae-136">Selecteer in het dialoogvenster **Module toevoegen** de **Module voor orderbevestiging** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c79ae-137">Selecteer **Opslaan** en vervolgens **Preview** om de sjabloon te bekijken.</span><span class="sxs-lookup"><span data-stu-id="c79ae-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="c79ae-138">De orderbevestigingsmodule wordt niet weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.</span><span class="sxs-lookup"><span data-stu-id="c79ae-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="c79ae-139">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="c79ae-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c79ae-140">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="c79ae-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c79ae-141">Selecteer in het dialoogvenster **Een sjabloon kiezen** de **Sjabloon voor orderbevestiging**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="c79ae-142">Voer onder **Paginanaam** **Pagina voor orderbevestiging** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c79ae-143">Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c79ae-144">Selecteer in het dialoogvenster **Module toevoegen** de **Module voor orderbevestiging** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c79ae-145">Selecteer in het eigenschappenvenster van de module voor orderbevestiging de optie **Kop** naast het potloodsymbool.</span><span class="sxs-lookup"><span data-stu-id="c79ae-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="c79ae-146">Voer in het veld **Koptekst** van het dialoogvenster **Koptekst** de koptekst **Orderbevestiging** in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c79ae-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="c79ae-147">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="c79ae-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="c79ae-148">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="c79ae-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c79ae-149">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c79ae-149">Additional resources</span></span>

[<span data-ttu-id="c79ae-150">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="c79ae-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c79ae-151">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="c79ae-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c79ae-152">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="c79ae-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c79ae-153">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="c79ae-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="c79ae-154">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="c79ae-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="c79ae-155">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="c79ae-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="c79ae-156">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="c79ae-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="c79ae-157">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="c79ae-157">Gift card module</span></span>](add-giftcard.md)
