---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621031"
---
# <a name="cart-module"></a><span data-ttu-id="0e081-103">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="0e081-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e081-104">In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e081-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0e081-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="0e081-105">Overview</span></span>

<span data-ttu-id="0e081-106">Een winkelwagenmodule geeft de artikelen weer die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen.</span><span class="sxs-lookup"><span data-stu-id="0e081-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="0e081-107">De module geeft ook een orderoverzicht weer en de klant kan promotiecodes toepassen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="0e081-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="0e081-108">De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen.</span><span class="sxs-lookup"><span data-stu-id="0e081-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="0e081-109">De module ondersteunt ook een koppeling **Terug naar winkelen**.</span><span class="sxs-lookup"><span data-stu-id="0e081-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="0e081-110">U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.</span><span class="sxs-lookup"><span data-stu-id="0e081-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="0e081-111">In de winkelwagenmodule worden gegevens weergegeven op basis van de winkelwagen-id. Dit is een browsercookie die op de hele site beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="0e081-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="0e081-112">De volgende afbeelding toont een voorbeeld van een winkelwagenpagina module op de Fabrikam-site.</span><span class="sxs-lookup"><span data-stu-id="0e081-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Voorbeeld van een winkelwagenmodule](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="0e081-114">Eigenschappen en vakken van de winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="0e081-114">Cart module properties and slots</span></span>

<span data-ttu-id="0e081-115">De winkelwagenmodule heeft een eigenschap **Koptekst** die kan worden ingesteld op waarden als **Boodschappentas** en **Artikelen in uw winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="0e081-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="0e081-116">Modules die in de winkelwagenmodule kunnen worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="0e081-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="0e081-117">**Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="0e081-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="0e081-118">De berichten worden aangestuurd door het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="0e081-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="0e081-119">U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="0e081-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="0e081-120">**Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="0e081-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="0e081-121">Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt.</span><span class="sxs-lookup"><span data-stu-id="0e081-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="0e081-122">Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.</span><span class="sxs-lookup"><span data-stu-id="0e081-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="0e081-123">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="0e081-123">Module properties</span></span>

<span data-ttu-id="0e081-124">De volgende instellingen voor de winkelwagenmodule kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:</span><span class="sxs-lookup"><span data-stu-id="0e081-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="0e081-125">**Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="0e081-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="0e081-126">Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="0e081-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="0e081-127">**Voorraad**: zie [Voorraadinstellingen toepassen](inventory-settings.md) voor informatie over het toepassen van voorraadinstellingen.</span><span class="sxs-lookup"><span data-stu-id="0e081-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="0e081-128">**Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven.</span><span class="sxs-lookup"><span data-stu-id="0e081-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="0e081-129">De route kan op siteniveau worden geconfigureerd, zodat detailhandelaren de klant kunnen terugbrengen naar de startpagina of een willekeurige andere pagina op de site.</span><span class="sxs-lookup"><span data-stu-id="0e081-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="0e081-130">Interactie met Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="0e081-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="0e081-131">De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's.</span><span class="sxs-lookup"><span data-stu-id="0e081-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="0e081-132">De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="0e081-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="0e081-133">Een winkelwagenmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="0e081-133">Add a cart module to a page</span></span>

<span data-ttu-id="0e081-134">Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="0e081-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0e081-135">Ga naar **Paginafragmenten** en selecteer **Nieuw** om een nieuw paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="0e081-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="0e081-136">Selecteer in het dialoogvenster **Nieuw paginafragment** de module **Winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="0e081-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="0e081-137">Voer onder **Naam paginafragment** de naam in voor het **Winkelwagenfragment** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e081-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="0e081-138">Selecteer het vak **Winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="0e081-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="0e081-139">Selecteer in het venster Eigenschappen rechts het potloodsymbool, voer de koptekst in het veld in en selecteer vervolgens het symbool voor het selectievinkje.</span><span class="sxs-lookup"><span data-stu-id="0e081-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="0e081-140">Selecteer het weglatingsteken (**...**) in het vak **Winkelwagen** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0e081-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0e081-141">Selecteer in het dialoogvenster **Module toevoegen** de **Winkelselectiemodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e081-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0e081-142">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.</span><span class="sxs-lookup"><span data-stu-id="0e081-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0e081-143">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="0e081-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0e081-144">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** een naam voor de sjabloon in.</span><span class="sxs-lookup"><span data-stu-id="0e081-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="0e081-145">Selecteer in de overzichtsstructuur het vak **Hoofdtekst**, selecteer de knop met het weglatingsteken (**...**) en vervolgens **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0e081-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="0e081-146">Selecteer in het dialoogvenster **Paginafragment selecteren** het **Winkelwagenfragment** dat u eerder hebt gemaakt en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e081-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0e081-147">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="0e081-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0e081-148">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="0e081-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0e081-149">Selecteer in het dialoogvenster **Sjabloon kiezen** de sjabloon die u eerder hebt gemaakt, voer een paginanaam in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0e081-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="0e081-150">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="0e081-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0e081-151">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="0e081-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e081-152">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0e081-152">Additional resources</span></span>

[<span data-ttu-id="0e081-153">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="0e081-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0e081-154">Containermodule</span><span class="sxs-lookup"><span data-stu-id="0e081-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0e081-155">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="0e081-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="0e081-156">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="0e081-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0e081-157">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="0e081-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0e081-158">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="0e081-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0e081-159">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="0e081-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0e081-160">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="0e081-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0e081-161">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="0e081-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="0e081-162">Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen</span><span class="sxs-lookup"><span data-stu-id="0e081-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
