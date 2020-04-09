---
title: Winkelwagenmodule
description: In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154012"
---
# <a name="cart-module"></a><span data-ttu-id="7d07b-103">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d07b-104">In dit onderwerp wordt beschreven wat winkelwagenmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7d07b-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d07b-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="7d07b-105">Overview</span></span>

<span data-ttu-id="7d07b-106">Een winkelwagenmodule geeft de artikelen weer die aan de winkelwagen zijn toegevoegd voordat de klant verder gaat met betalen.</span><span class="sxs-lookup"><span data-stu-id="7d07b-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="7d07b-107">De module geeft ook een orderoverzicht weer en de klant kan promotiecodes toepassen of verwijderen.</span><span class="sxs-lookup"><span data-stu-id="7d07b-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="7d07b-108">De winkelwagenmodule ondersteunt aangemelde betalingen en gastbetalingen.</span><span class="sxs-lookup"><span data-stu-id="7d07b-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="7d07b-109">De module ondersteunt ook een koppeling **Terug naar winkelen**.</span><span class="sxs-lookup"><span data-stu-id="7d07b-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="7d07b-110">U kunt de route voor deze koppeling configureren via **Site-instellingen \> Extensies \> Routes**.</span><span class="sxs-lookup"><span data-stu-id="7d07b-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="7d07b-111">In de winkelwagenmodule worden gegevens weergegeven op basis van de winkelwagen-id. Dit is een browsercookie die op de hele site beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="7d07b-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="7d07b-112">Eigenschappen en vakken van de winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-112">Cart module properties and slots</span></span>

<span data-ttu-id="7d07b-113">De winkelwagenmodule heeft een eigenschap **Koptekst** die kan worden ingesteld op waarden als **Boodschappentas** en **Artikelen in uw winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="7d07b-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="7d07b-114">Modules die in de winkelwagenmodule kunnen worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="7d07b-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="7d07b-115">**Tekstblok**: deze module ondersteunt aangepaste berichten in de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="7d07b-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="7d07b-116">De berichten worden aangestuurd door het Content Management System (CMS).</span><span class="sxs-lookup"><span data-stu-id="7d07b-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="7d07b-117">U kunt een bericht toevoegen, zoals "Voor problemen met uw order neemt u contact op met 1-800-Fabrikam".</span><span class="sxs-lookup"><span data-stu-id="7d07b-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="7d07b-118">**Winkelselectie**: deze module toont een lijst met nabijgelegen winkels waar een artikel beschikbaar is voor ophalen.</span><span class="sxs-lookup"><span data-stu-id="7d07b-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="7d07b-119">Hiermee kunnen gebruikers een locatie invoeren om te zoeken naar winkels in de buurt.</span><span class="sxs-lookup"><span data-stu-id="7d07b-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="7d07b-120">Zie [Winkelselectiemodule](store-selector.md) voor meer informatie over deze module.</span><span class="sxs-lookup"><span data-stu-id="7d07b-120">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="7d07b-121">Instellingen voor winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-121">Cart module settings</span></span>

<span data-ttu-id="7d07b-122">Winkelwagenmodules hebben de volgende instellingen die kunnen worden geconfigureerd via **Site-instellingen \> Extensies**:</span><span class="sxs-lookup"><span data-stu-id="7d07b-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="7d07b-123">**Maximumhoeveelheid**: deze eigenschap wordt gebruikt om voor elk artikel het maximumaantal op te geven dat aan de winkelwagen kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="7d07b-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="7d07b-124">Een detailhandelaar kan bijvoorbeeld besluiten dat slechts 10 stuks van elk product in één transactie mogen worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="7d07b-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="7d07b-125">**Voorraadcontrole**: wanneer de waarde is ingesteld op **True**, wordt een artikel alleen aan de winkelwagen toegevoegd nadat de koopvakmodule heeft gecontroleerd dat het op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="7d07b-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="7d07b-126">Deze voorraadcontrole wordt uitgevoerd voor scenario's waarin het artikel wordt verzonden en voor scenario's waarin het wordt opgehaald in de winkel.</span><span class="sxs-lookup"><span data-stu-id="7d07b-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="7d07b-127">Als de waarde is ingesteld op **False**, wordt er geen voorraadcontrole uitgevoerd voordat een artikel aan de winkelwagen wordt toegevoegd en de order wordt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="7d07b-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="7d07b-128">**Voorraadbuffer**: deze eigenschap wordt gebruikt om een bufferhoeveelheid op te geven voor de voorraad op te geven.</span><span class="sxs-lookup"><span data-stu-id="7d07b-128">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="7d07b-129">Voorraad wordt in realtime bijgehouden en wanneer een groot aantal klanten orders plaatst, kan het lastig zijn om een nauwkeurige voorraadtelling bij te houden.</span><span class="sxs-lookup"><span data-stu-id="7d07b-129">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="7d07b-130">Wanneer een voorraadcontrole wordt uitgevoerd en de voorraad kleiner is dan de bufferhoeveelheid, wordt het product verwerkt als niet op voorraad.</span><span class="sxs-lookup"><span data-stu-id="7d07b-130">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="7d07b-131">Dus wanneer verkopen snel plaatsvinden via verschillende kanalen en de voorraadtelling niet volledig is gesynchroniseerd, is er minder risico dat een artikel wordt verkocht dat niet op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="7d07b-131">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="7d07b-132">**Terug naar winkelen**: deze eigenschap wordt gebruikt om de route voor de koppeling **Terug naar winkelen** op te geven.</span><span class="sxs-lookup"><span data-stu-id="7d07b-132">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="7d07b-133">De route kan op siteniveau worden geconfigureerd, zodat detailhandelaren de klant kunnen terugbrengen naar de startpagina of een willekeurige andere pagina op de site.</span><span class="sxs-lookup"><span data-stu-id="7d07b-133">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="7d07b-134">Interactie met Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="7d07b-134">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="7d07b-135">De winkelwagenmodule haalt productinformatie op met behulp van Commerce Scale Unit-API's.</span><span class="sxs-lookup"><span data-stu-id="7d07b-135">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="7d07b-136">De winkelwagen-id van de browsercookie wordt gebruikt om alle productgegevens op te halen uit Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="7d07b-136">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="7d07b-137">Een winkelwagenmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="7d07b-137">Add a cart module to a page</span></span>

<span data-ttu-id="7d07b-138">Voer de volgende stappen uit om een winkelwagenmodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="7d07b-138">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7d07b-139">Maak een fragment met de naam **Winkelwagenfragment** en voeg een winkelwagenmodule toe aan het nieuwe fragment.</span><span class="sxs-lookup"><span data-stu-id="7d07b-139">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="7d07b-140">Voeg een koptekst toe aan de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="7d07b-140">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="7d07b-141">Voeg een winkelselectiemodule toe aan de winkelwagenmodule.</span><span class="sxs-lookup"><span data-stu-id="7d07b-141">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="7d07b-142">Sla het fragment op, voltooi de bewerking en publiceer het fragment.</span><span class="sxs-lookup"><span data-stu-id="7d07b-142">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="7d07b-143">Maak een sjabloon met de naam **Winkelwagensjabloon** en voeg het winkelwagenfragment toe dat u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7d07b-143">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="7d07b-144">Sla de sjabloon op, voltooi de bewerking en publiceer de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="7d07b-144">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="7d07b-145">Maak een pagina die gebruikmaakt van de nieuwe sjabloon.</span><span class="sxs-lookup"><span data-stu-id="7d07b-145">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="7d07b-146">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="7d07b-146">Save and preview the page.</span></span>
1. <span data-ttu-id="7d07b-147">Voltooi de bewerking van de pagina en publiceer de pagina.</span><span class="sxs-lookup"><span data-stu-id="7d07b-147">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d07b-148">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="7d07b-148">Additional resources</span></span>

[<span data-ttu-id="7d07b-149">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="7d07b-149">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7d07b-150">Containermodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-150">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7d07b-151">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-151">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="7d07b-152">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="7d07b-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7d07b-153">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-153">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7d07b-154">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-154">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7d07b-155">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-155">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7d07b-156">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="7d07b-156">Footer module</span></span>](author-footer-module.md)
