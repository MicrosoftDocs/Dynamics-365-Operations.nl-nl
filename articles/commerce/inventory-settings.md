---
title: Voorraadinstellingen toepassen
description: In dit onderwerp worden voorraadinstellingen beschreven en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b2c44eb5ece74de15e22180abc6d9d0448ab401b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798884"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="8d8ff-103">Voorraadinstellingen toepassen</span><span class="sxs-lookup"><span data-stu-id="8d8ff-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8d8ff-104">In dit onderwerp worden voorraadinstellingen beschreven en wordt beschreven hoe u deze toepast in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8d8ff-105">Met voorraadinstellingen wordt opgegeven of voorraad moet worden gecontroleerd voordat producten aan de winkelwagen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="8d8ff-106">Ze definiëren ook voorraadgerelateerde merchandisingberichten, zoals In voorraad en Slechts een paar over.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="8d8ff-107">Deze instellingen zorgen ervoor dat een product niet kan worden aangeschaft als het niet op voorraad is.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="8d8ff-108">Dynamics 365 Commerce biedt schattingen van voorhanden voorraad voor producten.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="8d8ff-109">Zie [Voorraadbeschikbaarheid voor detailhandelafzetkanalen berekenen](calculated-inventory-retail-channels.md) voor informatie over de berekening van geschatte voorhanden voorraad .</span><span class="sxs-lookup"><span data-stu-id="8d8ff-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="8d8ff-110">In Commerce Site Builder kunt u voorraaddrempels en -bereiken definiëren voor een product of een categorie.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="8d8ff-111">Ze bepalen of voorraad kan worden geclassificeerd als in voorraad, weinig voorraad of niet op vorraad.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="8d8ff-112">Zie [Voorraadbuffers en voorraadniveaus configureren](inventory-buffers-levels.md) voor meer informatie</span><span class="sxs-lookup"><span data-stu-id="8d8ff-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8d8ff-113">Ondersteuning voor voorraaddrempels en -bereiken is beschikbaar in de release van Dynamics 365 Commerce 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="8d8ff-114">Voorraadinstellingen</span><span class="sxs-lookup"><span data-stu-id="8d8ff-114">Inventory settings</span></span>

<span data-ttu-id="8d8ff-115">In Commerce worden voorraadinstellingen gedefinieerd via **Site-instellingen \> Extensies \> Voorraadbeheer** in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="8d8ff-116">Er zijn vier voorraadinstellingen, waarvan er een is verouderd (afgeschaft):</span><span class="sxs-lookup"><span data-stu-id="8d8ff-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="8d8ff-117">**Voorraadcontrole in app inschakelen**: met deze instelling wordt de voorraadcontrole van een product ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="8d8ff-118">De modules voor koopvak, winkelwagen en ophalen in winkel comntroleren vervolgens de productvoorraad en zorgen ervoor dat een product alleen aan de winkelwagen kan worden toegevoegd als er voorraad beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="8d8ff-119">**Voorraadniveau gebaseerd op**: deze instelling bepaalt hoe voorraadniveaus worden berekend.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="8d8ff-120">De beschikbare waarden zijn **Totaal beschikbaar**, **Fysiek beschikbaar** en **Drempelwaarde voor niet op voorraad**.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="8d8ff-121">In Commerce kunt u drempelwaarden en bereiken definiëren voor elk product en elke categorie.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="8d8ff-122">De voorraad-API's geven productvoorraadinformatie als resultaat voor de eigenschappen **Totaal beschikbaar** en **Fysiek beschikbaar**.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="8d8ff-123">De detailhandelaar beslist of de waarde **Totaal beschikbaar** of **Fysiek beschikbaar** moet worden gebruikt om de voorraadtelling en de bijbehorende bereiken voor op voorraad en niet op voorraad te bepalen.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="8d8ff-124">De waarde **Drempelwaarde voor niet op voorraad** van de instelling **Voorraadniveau gebaseerd op** is een oude (verouderde) waarde.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="8d8ff-125">Wanneer deze wordt geselecteerd, wordt de voorraadtelling bepaald op basis van de resultaten van de waarde **Totaal beschikbaar**, de drempel wordt gedefinieerd door de numerieke instelling **Drempelwaarde voor niet op voorraad** die later wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="8d8ff-126">Deze drempelwaarde-instelling is van toepassing op alle producten voor een e-commerce-site.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="8d8ff-127">Als voorraad lager is dan de drempelwaarde, wordt een product als niet op voorraad beschouwd.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="8d8ff-128">Anders wordt het beschouwd als op voorraad.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="8d8ff-129">De mogelijkheden van de waarde **Drempel waarde voor niet op voorraad** zijn beperkt en wij raden u aan om deze niet meer te gebruiken in versie 10.0.12 en hoger.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="8d8ff-130">**Voorraadbereiken**: met deze instelling definieert u de voorraadbereiken waarvoor berichten worden weergegeven in sitemodules.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="8d8ff-131">Deze is alleen van toepassing als de waarde **Totaal beschikbaar** of **Fysiek beschikbaar** is geselecteerd voor de instelling **Voorraadniveau gebaseerd op**.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="8d8ff-132">De beschikbare waarden zijn **Alle**, **Weinig en niet op voorraad** en **Niet op voorraad**.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="8d8ff-133">Wanneer **Alle** is geselecteerd, worden berichten voor alle voorraadbereiken, van op voorraad (Beschikbaar) tot niet op voorraad (Niet op voorraad), weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="8d8ff-134">Wanneer **Weinig en niet op voorraad** is geselecteerd, worden berichten voor alle voorraadbereiken, behalve op voorraad (Beschikbaar), weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="8d8ff-135">Wanneer **Niet op voorraad** is geselecteerd, wordt alleen het bericht Niet op vooraad weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="8d8ff-136">**Drempelwaarde voor niet op voorraad**: deze oude numerieke instelling wordt alleen van kracht als de waarde **Drempelwaarde voor niet op voorraad** is geselecteerd voor de instelling **Voorraadniveau gebaseerd op**.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="8d8ff-137">Deze instellingen zijn beschikbaar in Dynamics 365 Commerce versie 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-137">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="8d8ff-138">Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-138">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="8d8ff-139">Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor instructies voor het bijwerken van het appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-139">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="8d8ff-140">Modules die voorraadinstellingen gebruiken</span><span class="sxs-lookup"><span data-stu-id="8d8ff-140">Modules that use inventory settings</span></span>

<span data-ttu-id="8d8ff-141">De modules voor koopvak, wensenlijst, winkelselectie en winkelwagen gebruiken voorraadinstellingen om de voorraadbereiken en berichten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-141">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="8d8ff-142">De volgende afbeelding toont een voorbeeld van een pagina met productgegevens (PDP) met een bericht over voorhanden voorraad (Beschikbaar).</span><span class="sxs-lookup"><span data-stu-id="8d8ff-142">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Voorbeeld van een PDP-module met een bericht over voorhanden voorraad](./media/pdp-InStock.png)

<span data-ttu-id="8d8ff-144">De volgende afbeelding toont een voorbeeld van een PDP met het bericht Niet op voorraad.</span><span class="sxs-lookup"><span data-stu-id="8d8ff-144">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Voorbeeld van een PDP-module met het bericht dat er geen voorraad beschikbaar is](./media/pdp-outofstock.png)

<span data-ttu-id="8d8ff-146&quot;>De volgende afbeelding toont een voorbeeld van een winkelwagen met het bericht Beschikbaar.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;8d8ff-146&quot;>The following image shows an example of a cart that is showing an in-stock (&quot;Available") message.</span></span>

![Voorbeeld van een winkelwagenmodule met een bericht over voorhanden voorraad](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="8d8ff-148">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="8d8ff-148">Additional resources</span></span>

[<span data-ttu-id="8d8ff-149">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="8d8ff-149">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8d8ff-150">Voorraadbuffers en voorraadniveaus configureren</span><span class="sxs-lookup"><span data-stu-id="8d8ff-150">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="8d8ff-151">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="8d8ff-151">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8d8ff-152">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="8d8ff-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8d8ff-153">Accountbeheerpagina's en -modules</span><span class="sxs-lookup"><span data-stu-id="8d8ff-153">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="8d8ff-154">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="8d8ff-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="8d8ff-155">Updates voor SDK's en modulebibliotheken</span><span class="sxs-lookup"><span data-stu-id="8d8ff-155">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
