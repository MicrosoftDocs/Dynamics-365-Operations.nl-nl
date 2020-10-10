---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: d9a15f85838849796d6ce4674712636251c75bf3
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818270"
---
# <a name="cart-module"></a><span data-ttu-id="b45b7-103">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="b45b7-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b45b7-104">In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b45b7-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b45b7-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="b45b7-105">Overview</span></span>

<span data-ttu-id="b45b7-106">Een winkelwagenmodule geeft de artikelen weer die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen.</span><span class="sxs-lookup"><span data-stu-id="b45b7-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="b45b7-107">De module geeft ook een orderoverzicht weer en de klant kan promotiecodes toepassen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b45b7-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="b45b7-108">De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen.</span><span class="sxs-lookup"><span data-stu-id="b45b7-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="b45b7-109">De module ondersteunt ook een koppeling **Terug naar winkelen**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="b45b7-110">U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="b45b7-111">In de winkelwagenmodule worden gegevens weergegeven op basis van de winkelwagen-id. Dit is een browsercookie die op de hele site beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="b45b7-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="b45b7-112">De volgende afbeelding toont een voorbeeld van een winkelwagenpagina module op de Fabrikam-site.</span><span class="sxs-lookup"><span data-stu-id="b45b7-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Voorbeeld van een winkelwagenmodule op de Fabrikam-site](./media/cart2.PNG)

<span data-ttu-id="b45b7-114">De volgende afbeelding toont een voorbeeld van een winkelwagenpagina module op de Fabrikam-site.</span><span class="sxs-lookup"><span data-stu-id="b45b7-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="b45b7-115">In dit voorbeeld zijn er verwerkingskosten voor een regelartikel.</span><span class="sxs-lookup"><span data-stu-id="b45b7-115">In this example, there is a handling fee for a line item.</span></span>

![Voorbeeld van een winkelwagenmodule met verwerkingskosten voor een regelartikel](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="b45b7-117">Eigenschappen en vakken van de winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="b45b7-117">Cart module properties and slots</span></span>

| <span data-ttu-id="b45b7-118">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="b45b7-118">Property</span></span> | <span data-ttu-id="b45b7-119">Waarden</span><span class="sxs-lookup"><span data-stu-id="b45b7-119">Values</span></span> | <span data-ttu-id="b45b7-120">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b45b7-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b45b7-121">Kop</span><span class="sxs-lookup"><span data-stu-id="b45b7-121">Heading</span></span> | <span data-ttu-id="b45b7-122">Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="b45b7-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b45b7-123">De kop voor de winkelwagen zoals Boodschappentas of Artikelen in uw winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="b45b7-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="b45b7-124">Fouten voor niet op voorraad weergeven</span><span class="sxs-lookup"><span data-stu-id="b45b7-124">Show out of stock errors</span></span> | <span data-ttu-id="b45b7-125">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="b45b7-125">**True** or **False**</span></span> | <span data-ttu-id="b45b7-126">Als deze eigenschap is ingesteld op **Waar**, worden op de pagina Winkelwagen fouten met betrekking tot de voorraad weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b45b7-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="b45b7-127">We raden u aan deze eigenschap in te stellen op **Waar** als voorraadcontrole wordt toegepast op de locatie.</span><span class="sxs-lookup"><span data-stu-id="b45b7-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="b45b7-128">Verzendkosten voor regelartikelen weergeven</span><span class="sxs-lookup"><span data-stu-id="b45b7-128">Show shipping charges for line items</span></span> | <span data-ttu-id="b45b7-129">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="b45b7-129">**True** or **False**</span></span> | <span data-ttu-id="b45b7-130">Als deze eigenschap is ingesteld op **Waar**, worden de verzendkosten voor de artikelen op de winkelwagenregels weergegeven als deze informatie beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="b45b7-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="b45b7-131">Deze functie wordt niet ondersteund in het thema Fabrikam omdat gebruikers alleen verzending in de kassastroom selecteren.</span><span class="sxs-lookup"><span data-stu-id="b45b7-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="b45b7-132">Deze functie kan echter worden ingeschakeld in andere werkstromen als dat van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="b45b7-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="b45b7-133">Modules die in de winkelwagenmodule kunnen worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="b45b7-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="b45b7-134">**Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="b45b7-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="b45b7-135">De berichten worden aangestuurd door het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="b45b7-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="b45b7-136">U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="b45b7-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="b45b7-137">**Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="b45b7-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="b45b7-138">Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt.</span><span class="sxs-lookup"><span data-stu-id="b45b7-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="b45b7-139">Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.</span><span class="sxs-lookup"><span data-stu-id="b45b7-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="b45b7-140">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="b45b7-140">Module properties</span></span>

<span data-ttu-id="b45b7-141">De volgende instellingen voor de winkelwagenmodule kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:</span><span class="sxs-lookup"><span data-stu-id="b45b7-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="b45b7-142">**Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b45b7-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="b45b7-143">Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="b45b7-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="b45b7-144">**Voorraad**: zie [Voorraadinstellingen toepassen](inventory-settings.md) voor informatie over het toepassen van voorraadinstellingen.</span><span class="sxs-lookup"><span data-stu-id="b45b7-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="b45b7-145">**Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven.</span><span class="sxs-lookup"><span data-stu-id="b45b7-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="b45b7-146">De route kan op siteniveau worden geconfigureerd, zodat detailhandelaren de klant kunnen terugbrengen naar de startpagina of een willekeurige andere pagina op de site.</span><span class="sxs-lookup"><span data-stu-id="b45b7-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="b45b7-147">Interactie met Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="b45b7-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="b45b7-148">De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's.</span><span class="sxs-lookup"><span data-stu-id="b45b7-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="b45b7-149">De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="b45b7-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="b45b7-150">Een winkelwagenmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="b45b7-150">Add a cart module to a page</span></span>

<span data-ttu-id="b45b7-151">Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="b45b7-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b45b7-152">Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="b45b7-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b45b7-153">Selecteer in het dialoogvenster **Nieuw fragment** de module **Winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="b45b7-154">Voer onder **Naam fragment** de naam **Winkelwagenfragment** in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="b45b7-155">Selecteer het vak **Winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="b45b7-156">Selecteer in het venster Eigenschappen rechts het potloodsymbool, voer de koptekst in het veld in en selecteer vervolgens het symbool voor het selectievinkje.</span><span class="sxs-lookup"><span data-stu-id="b45b7-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="b45b7-157">Selecteer het weglatingsteken (**...**) in het vak **Winkelwagen** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b45b7-158">Selecteer in het dialoogvenster **Module toevoegen** de **Winkelselectiemodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b45b7-159">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.</span><span class="sxs-lookup"><span data-stu-id="b45b7-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b45b7-160">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="b45b7-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b45b7-161">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** een naam voor de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="b45b7-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="b45b7-162">Selecteer in de overzichtsstructuur het vak **Hoofdtekst**, selecteer de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="b45b7-163">Selecteer in het dialoogvenster **Fragment selecteren** het fragment **Winkelwagenfragment** dat u eerder hebt gemaakt en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b45b7-164">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="b45b7-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b45b7-165">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="b45b7-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b45b7-166">Selecteer in het dialoogvenster **Sjabloon kiezen** de sjabloon die u eerder hebt gemaakt, voer een paginanaam in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45b7-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="b45b7-167">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="b45b7-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="b45b7-168">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="b45b7-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b45b7-169">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b45b7-169">Additional resources</span></span>

[<span data-ttu-id="b45b7-170">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="b45b7-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b45b7-171">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="b45b7-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b45b7-172">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="b45b7-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b45b7-173">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="b45b7-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b45b7-174">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="b45b7-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b45b7-175">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="b45b7-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b45b7-176">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="b45b7-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="b45b7-177">Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen</span><span class="sxs-lookup"><span data-stu-id="b45b7-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
