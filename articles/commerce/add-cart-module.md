---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261416"
---
# <a name="cart-module"></a><span data-ttu-id="62e31-103">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="62e31-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62e31-104">In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="62e31-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="62e31-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="62e31-105">Overview</span></span>

<span data-ttu-id="62e31-106">Een winkelwagenmodule geeft de artikelen weer die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen.</span><span class="sxs-lookup"><span data-stu-id="62e31-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="62e31-107">De module geeft ook een orderoverzicht weer en de klant kan promotiecodes toepassen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="62e31-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="62e31-108">De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen.</span><span class="sxs-lookup"><span data-stu-id="62e31-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="62e31-109">De module ondersteunt ook een koppeling **Terug naar winkelen**.</span><span class="sxs-lookup"><span data-stu-id="62e31-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="62e31-110">U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.</span><span class="sxs-lookup"><span data-stu-id="62e31-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="62e31-111">In de winkelwagenmodule worden gegevens weergegeven op basis van de winkelwagen-id. Dit is een browsercookie die op de hele site beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="62e31-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="62e31-112">Eigenschappen en vakken van de winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="62e31-112">Cart module properties and slots</span></span>

<span data-ttu-id="62e31-113">De winkelwagenmodule heeft een eigenschap **Koptekst** die kan worden ingesteld op waarden als **Boodschappentas** en **Artikelen in uw winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="62e31-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="62e31-114">Modules die in de winkelwagenmodule kunnen worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="62e31-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="62e31-115">**Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="62e31-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="62e31-116">De berichten worden aangestuurd door het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="62e31-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="62e31-117">U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="62e31-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="62e31-118">**Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="62e31-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="62e31-119">Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt.</span><span class="sxs-lookup"><span data-stu-id="62e31-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="62e31-120">Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.</span><span class="sxs-lookup"><span data-stu-id="62e31-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="62e31-121">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="62e31-121">Module properties</span></span>

<span data-ttu-id="62e31-122">Winkelwagenmodules hebben de volgende instellingen die kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:</span><span class="sxs-lookup"><span data-stu-id="62e31-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="62e31-123">**Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="62e31-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="62e31-124">Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="62e31-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="62e31-125">**Voorraadcontrole**: wanneer de waarde is ingesteld op **True**, wordt een artikel alleen aan de winkelwagen toegevoegd nadat de koopvakmodule heeft gecontroleerd dat het op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="62e31-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="62e31-126">Deze voorraadcontrole wordt uitgevoerd voor scenario's waarin het artikel wordt verzonden en voor scenario's waarin het wordt opgehaald in de winkel.</span><span class="sxs-lookup"><span data-stu-id="62e31-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="62e31-127">Als de waarde is ingesteld op **False**, wordt er geen voorraadcontrole uitgevoerd voordat een artikel aan de winkelwagen wordt toegevoegd en de order wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="62e31-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="62e31-128">Zie [Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md) voor informatie over het configureren van voorraadinstellingen in de backoffice .</span><span class="sxs-lookup"><span data-stu-id="62e31-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="62e31-129">**Voorraadbuffer**: deze eigenschap wordt gebruikt om een bufferhoeveelheid op te geven voor de voorraad op te geven.</span><span class="sxs-lookup"><span data-stu-id="62e31-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="62e31-130">Voorraad wordt in realtime bijgehouden en wanneer een groot aantal klanten orders plaatst, kan het lastig zijn om een nauwkeurige voorraadtelling bij te houden.</span><span class="sxs-lookup"><span data-stu-id="62e31-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="62e31-131">Wanneer een voorraadcontrole wordt uitgevoerd en de voorraad kleiner is dan de bufferhoeveelheid, wordt het product verwerkt als niet op voorraad.</span><span class="sxs-lookup"><span data-stu-id="62e31-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="62e31-132">Dus wanneer verkopen snel plaatsvinden via verschillende kanalen en de voorraadtelling niet volledig is gesynchroniseerd, is er minder risico dat een artikel wordt verkocht dat niet op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="62e31-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="62e31-133">**Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven.</span><span class="sxs-lookup"><span data-stu-id="62e31-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="62e31-134">De route kan op siteniveau worden geconfigureerd, zodat detailhandelaren de klant kunnen terugbrengen naar de startpagina of een willekeurige andere pagina op de site.</span><span class="sxs-lookup"><span data-stu-id="62e31-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="62e31-135">Interactie met Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="62e31-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="62e31-136">De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's.</span><span class="sxs-lookup"><span data-stu-id="62e31-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="62e31-137">De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="62e31-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="62e31-138">Een winkelwagenmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="62e31-138">Add a cart module to a page</span></span>

<span data-ttu-id="62e31-139">Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="62e31-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="62e31-140">Maak een fragment met de naam **Winkelwagenfragment** en voeg een winkelwagenmodule toe aan het nieuwe fragment.</span><span class="sxs-lookup"><span data-stu-id="62e31-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="62e31-141">Voeg een koptekst toe aan de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="62e31-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="62e31-142">Voeg een winkelselectiemodule toe aan de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="62e31-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="62e31-143">Sla het fragment op, voltooi de bewerking en publiceer het fragment.</span><span class="sxs-lookup"><span data-stu-id="62e31-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="62e31-144">Maak een sjabloon met de naam **Winkelwagensjabloon** en voeg het winkelwagenfragment toe dat u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="62e31-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="62e31-145">Sla de sjabloon op, voltooi de bewerking en publiceer de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="62e31-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="62e31-146">Maak een pagina die gebruikmaakt van de nieuwe sjabloon.</span><span class="sxs-lookup"><span data-stu-id="62e31-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="62e31-147">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="62e31-147">Save and preview the page.</span></span>
1. <span data-ttu-id="62e31-148">Voltooi de bewerking van de pagina en publiceer de pagina.</span><span class="sxs-lookup"><span data-stu-id="62e31-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62e31-149">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="62e31-149">Additional resources</span></span>

[<span data-ttu-id="62e31-150">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="62e31-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="62e31-151">Containermodule</span><span class="sxs-lookup"><span data-stu-id="62e31-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="62e31-152">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="62e31-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="62e31-153">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="62e31-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="62e31-154">Module winkelwagenpictogram</span><span class="sxs-lookup"><span data-stu-id="62e31-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="62e31-155">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="62e31-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="62e31-156">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="62e31-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="62e31-157">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="62e31-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="62e31-158">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="62e31-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="62e31-159">Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen</span><span class="sxs-lookup"><span data-stu-id="62e31-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
