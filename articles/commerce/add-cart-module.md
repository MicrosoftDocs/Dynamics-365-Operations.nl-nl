---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
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
ms.openlocfilehash: 5b0ce69f57e6ba691803752280466b41ced7c521
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206482"
---
# <a name="cart-module"></a><span data-ttu-id="ed121-103">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="ed121-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed121-104">In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ed121-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ed121-105">Een winkelwagenmodule geeft de artikelen weer die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen.</span><span class="sxs-lookup"><span data-stu-id="ed121-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="ed121-106">De module geeft ook een orderoverzicht weer en de klant kan promotiecodes toepassen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="ed121-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="ed121-107">De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen.</span><span class="sxs-lookup"><span data-stu-id="ed121-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="ed121-108">De module ondersteunt ook een koppeling **Terug naar winkelen**.</span><span class="sxs-lookup"><span data-stu-id="ed121-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="ed121-109">U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.</span><span class="sxs-lookup"><span data-stu-id="ed121-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="ed121-110">In de winkelwagenmodule worden gegevens weergegeven op basis van de winkelwagen-id. Dit is een browsercookie die op de hele site beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="ed121-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="ed121-111">De volgende afbeelding toont een voorbeeld van een winkelwagenpagina module op de Fabrikam-site.</span><span class="sxs-lookup"><span data-stu-id="ed121-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Voorbeeld van een winkelwagenmodule op de Fabrikam-site](./media/cart2.PNG)

<span data-ttu-id="ed121-113">De volgende afbeelding toont een voorbeeld van een winkelwagenpagina module op de Fabrikam-site.</span><span class="sxs-lookup"><span data-stu-id="ed121-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="ed121-114">In dit voorbeeld zijn er verwerkingskosten voor een regelartikel.</span><span class="sxs-lookup"><span data-stu-id="ed121-114">In this example, there is a handling fee for a line item.</span></span>

![Voorbeeld van een winkelwagenmodule met verwerkingskosten voor een regelartikel](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="ed121-116">Eigenschappen en vakken van de winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="ed121-116">Cart module properties and slots</span></span>

| <span data-ttu-id="ed121-117">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="ed121-117">Property</span></span> | <span data-ttu-id="ed121-118">Waarden</span><span class="sxs-lookup"><span data-stu-id="ed121-118">Values</span></span> | <span data-ttu-id="ed121-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ed121-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="ed121-120">Kop</span><span class="sxs-lookup"><span data-stu-id="ed121-120">Heading</span></span> | <span data-ttu-id="ed121-121">Koptekst en een tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="ed121-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="ed121-122">De kop voor de winkelwagen zoals Boodschappentas of Artikelen in uw winkelwagen.</span><span class="sxs-lookup"><span data-stu-id="ed121-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="ed121-123">Fouten voor niet op voorraad weergeven</span><span class="sxs-lookup"><span data-stu-id="ed121-123">Show out of stock errors</span></span> | <span data-ttu-id="ed121-124">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="ed121-124">**True** or **False**</span></span> | <span data-ttu-id="ed121-125">Als deze eigenschap is ingesteld op **Waar**, worden op de pagina Winkelwagen fouten met betrekking tot de voorraad weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ed121-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="ed121-126">We raden u aan deze eigenschap in te stellen op **Waar** als voorraadcontrole wordt toegepast op de locatie.</span><span class="sxs-lookup"><span data-stu-id="ed121-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="ed121-127">Verzendkosten voor regelartikelen weergeven</span><span class="sxs-lookup"><span data-stu-id="ed121-127">Show shipping charges for line items</span></span> | <span data-ttu-id="ed121-128">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="ed121-128">**True** or **False**</span></span> | <span data-ttu-id="ed121-129">Als deze eigenschap is ingesteld op **Waar**, worden de verzendkosten voor de artikelen op de winkelwagenregels weergegeven als deze informatie beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="ed121-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="ed121-130">Deze functie wordt niet ondersteund in het thema Fabrikam omdat gebruikers alleen verzending in de kassastroom selecteren.</span><span class="sxs-lookup"><span data-stu-id="ed121-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="ed121-131">Deze functie kan echter worden ingeschakeld in andere werkstromen als dat van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="ed121-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="ed121-132">Beschikbare aanbiedingen weergeven</span><span class="sxs-lookup"><span data-stu-id="ed121-132">Show available promotions</span></span>| <span data-ttu-id="ed121-133">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="ed121-133">**True** or **False**</span></span> | <span data-ttu-id="ed121-134">Als deze eigenschap is ingesteld op **Waar**, worden er op basis van de artikelen in de winkelwagen beschikbare promoties uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ed121-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="ed121-135">Deze mogelijkheid is beschikbaar in Dynamics 365 Commerce versie 10.0.16.</span><span class="sxs-lookup"><span data-stu-id="ed121-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="ed121-136">Modules die in de winkelwagenmodule kunnen worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="ed121-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="ed121-137">**Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="ed121-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="ed121-138">De berichten worden aangestuurd door het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="ed121-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="ed121-139">U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="ed121-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="ed121-140">**Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="ed121-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="ed121-141">Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt.</span><span class="sxs-lookup"><span data-stu-id="ed121-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="ed121-142">Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.</span><span class="sxs-lookup"><span data-stu-id="ed121-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="ed121-143">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="ed121-143">Module properties</span></span>

<span data-ttu-id="ed121-144">De volgende instellingen voor de winkelwagenmodule kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:</span><span class="sxs-lookup"><span data-stu-id="ed121-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="ed121-145">**Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="ed121-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="ed121-146">Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="ed121-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="ed121-147">**Voorraad**: zie [Voorraadinstellingen toepassen](inventory-settings.md) voor informatie over het toepassen van voorraadinstellingen.</span><span class="sxs-lookup"><span data-stu-id="ed121-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="ed121-148">**Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven.</span><span class="sxs-lookup"><span data-stu-id="ed121-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="ed121-149">De route kan op siteniveau worden geconfigureerd, zodat detailhandelaren de klant kunnen terugbrengen naar de startpagina of een willekeurige andere pagina op de site.</span><span class="sxs-lookup"><span data-stu-id="ed121-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed121-150">In de Dynamics 365 Commerce 10.0.14-release en later worden artikelen in de winkelwagen samengevoegd op basis van de instellingen die zijn gedefinieerd in het online functionaliteitsprofiel voor de online winkel in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ed121-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="ed121-151">Zie [Een online functionaliteitsprofiel maken](online-functionality-profile.md) voor meer informatie over het maken van een online functionaliteitsprofiel en het instellen van de eigenschappen die zijn vereist voor samenvoeging.</span><span class="sxs-lookup"><span data-stu-id="ed121-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="ed121-152">Interactie met Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="ed121-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="ed121-153">De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's.</span><span class="sxs-lookup"><span data-stu-id="ed121-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="ed121-154">De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="ed121-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="ed121-155">Een winkelwagenmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="ed121-155">Add a cart module to a page</span></span>

<span data-ttu-id="ed121-156">Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="ed121-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ed121-157">Ga naar **Fragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="ed121-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="ed121-158">Selecteer in het dialoogvenster **Nieuw fragment** de module **Winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="ed121-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="ed121-159">Voer onder **Naam fragment** de naam **Winkelwagenfragment** in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed121-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="ed121-160">Selecteer het vak **Winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="ed121-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="ed121-161">Selecteer in het venster Eigenschappen rechts het potloodsymbool, voer de koptekst in het veld in en selecteer vervolgens het symbool voor het selectievinkje.</span><span class="sxs-lookup"><span data-stu-id="ed121-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="ed121-162">Selecteer het weglatingsteken (**...**) in het vak **Winkelwagen** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ed121-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="ed121-163">Selecteer in het dialoogvenster **Module toevoegen** de **Winkelselectiemodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed121-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="ed121-164">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.</span><span class="sxs-lookup"><span data-stu-id="ed121-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="ed121-165">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="ed121-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="ed121-166">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** een naam voor de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="ed121-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="ed121-167">Selecteer in de overzichtsstructuur het vak **Hoofdtekst**, selecteer de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ed121-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="ed121-168">Selecteer in het dialoogvenster **Fragment selecteren** het fragment **Winkelwagenfragment** dat u eerder hebt gemaakt en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed121-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="ed121-169">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="ed121-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="ed121-170">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="ed121-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="ed121-171">Selecteer in het dialoogvenster **Sjabloon kiezen** de sjabloon die u eerder hebt gemaakt, voer een paginanaam in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed121-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="ed121-172">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="ed121-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="ed121-173">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="ed121-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed121-174">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="ed121-174">Additional resources</span></span>

[<span data-ttu-id="ed121-175">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="ed121-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="ed121-176">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="ed121-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ed121-177">Betalingsmodule</span><span class="sxs-lookup"><span data-stu-id="ed121-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="ed121-178">Module voor verzendadressen</span><span class="sxs-lookup"><span data-stu-id="ed121-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="ed121-179">Module voor leveringsopties</span><span class="sxs-lookup"><span data-stu-id="ed121-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="ed121-180">Module ophaalinformatie</span><span class="sxs-lookup"><span data-stu-id="ed121-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="ed121-181">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="ed121-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ed121-182">Geschenkbonmodule</span><span class="sxs-lookup"><span data-stu-id="ed121-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="ed121-183">Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen</span><span class="sxs-lookup"><span data-stu-id="ed121-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="ed121-184">Een online functionaliteitsprofiel maken</span><span class="sxs-lookup"><span data-stu-id="ed121-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]