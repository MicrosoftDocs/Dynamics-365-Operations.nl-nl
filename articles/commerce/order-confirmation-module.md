---
title: Orderbevestigingsmodule
description: In dit onderwerp wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698321"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="23aab-103">Orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="23aab-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="23aab-104">In dit onderwerp wordt beschreven wat orderbevestigingsmodules zijn en hoe u ze maakt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="23aab-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="23aab-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="23aab-105">Overview</span></span>

<span data-ttu-id="23aab-106">Er wordt een orderbevestigingsmodule gebruikt om een bevestigingsbericht weer te geven op de pagina orderbevestiging nadat een order is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="23aab-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="23aab-107">In de orderbevestigingsmodule wordt het nummer van de orderbevestiging en het e-mailadres van de klant weergegeven dat tijdens het uitchecken is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="23aab-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="23aab-108">Wanneer een order tijdens het uitchecken wordt geplaatst, worden het orderbevestigingsnummer en het e-mailadres van de klant doorgegeven aan de orderbevestigingspagina als een queryreeks in de URL van de pagina.</span><span class="sxs-lookup"><span data-stu-id="23aab-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="23aab-109">De orderbevestigingsmodule ontvangt deze informatie en geeft de orderstatus weer op de orderbevestigingspagina.</span><span class="sxs-lookup"><span data-stu-id="23aab-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="23aab-110">De orderbevestigingsmodule vereist deze paginacontext om de status van de order op te geven.</span><span class="sxs-lookup"><span data-stu-id="23aab-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="23aab-111">Eigenschappen van orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="23aab-111">Order confirmation module properties</span></span>

| <span data-ttu-id="23aab-112">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="23aab-112">Property name</span></span> | <span data-ttu-id="23aab-113">Waarden</span><span class="sxs-lookup"><span data-stu-id="23aab-113">Values</span></span> | <span data-ttu-id="23aab-114">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="23aab-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="23aab-115">Koptekst</span><span class="sxs-lookup"><span data-stu-id="23aab-115">Heading</span></span>       | <span data-ttu-id="23aab-116">Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="23aab-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="23aab-117">De orderbevestigingsmodule kan een koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="23aab-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="23aab-118">Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="23aab-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="23aab-119">De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="23aab-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="23aab-120">Modules die kunnen worden gebruikt in de pagina van de orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="23aab-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="23aab-121">**Aanbevelingen**: de aanbevelingsmodule kan op de orderbevestigingspagina worden geplaatst om andere producten voor te stellen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="23aab-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="23aab-122">**Marketing** : de module marketing kan marketinginhoud toevoegen aan de pagina orderbevestiging.</span><span class="sxs-lookup"><span data-stu-id="23aab-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="23aab-123">Een module voor de orderbevestigingspagina maken</span><span class="sxs-lookup"><span data-stu-id="23aab-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="23aab-124">Maak een paginasjabloon met de naam **orderbevestigingssjabloon**.</span><span class="sxs-lookup"><span data-stu-id="23aab-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="23aab-125">Voeg in het **hoofdvak** van de standaardpagina een orderbevestigingsmodule toe.</span><span class="sxs-lookup"><span data-stu-id="23aab-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="23aab-126">Voeg in de module orderbevestiging een aanbevelingsmodule toe.</span><span class="sxs-lookup"><span data-stu-id="23aab-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="23aab-127">Sla de sjabloon op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="23aab-127">Save and preview the template.</span></span> <span data-ttu-id="23aab-128">De orderbevestigingsmodule kan niet worden weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.</span><span class="sxs-lookup"><span data-stu-id="23aab-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="23aab-129">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="23aab-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="23aab-130">Gebruik de orderbevestigingssjabloon die u zojuist hebt gemaakt om een pagina met de naam **Orderbevestigingspagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="23aab-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="23aab-131">Voeg de standaardpagina toe aan het paginaoverzicht.</span><span class="sxs-lookup"><span data-stu-id="23aab-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="23aab-132">Voeg in het vak **Koptekst** een koptekstfragment toe.</span><span class="sxs-lookup"><span data-stu-id="23aab-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="23aab-133">Voeg in het vak **Voettekst** een voettekstfragment toe.</span><span class="sxs-lookup"><span data-stu-id="23aab-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="23aab-134">Voeg in het **hoofdvak** een orderbevestigingsmodule toe.</span><span class="sxs-lookup"><span data-stu-id="23aab-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="23aab-135">Voeg in het eigenschappenvenster van de orderbevestigingsmodule de kop **Orderbevestiging** toe.</span><span class="sxs-lookup"><span data-stu-id="23aab-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="23aab-136">Voeg onder de orderbevestigingsmodule een aanbevelingsmodule toe en configureer deze zo dat de instellingen **Nieuw** en **Best verkocht** worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="23aab-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="23aab-137">Sla de pagina op, geef een voorbeeld weer, check in en publiceer de pagina.</span><span class="sxs-lookup"><span data-stu-id="23aab-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23aab-138">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="23aab-138">Additional resources</span></span>

[<span data-ttu-id="23aab-139">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="23aab-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="23aab-140">Module Container</span><span class="sxs-lookup"><span data-stu-id="23aab-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="23aab-141">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="23aab-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="23aab-142">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="23aab-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="23aab-143">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="23aab-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="23aab-144">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="23aab-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="23aab-145">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="23aab-145">Footer module</span></span>](author-footer-module.md)
