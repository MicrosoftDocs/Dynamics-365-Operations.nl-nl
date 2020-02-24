---
title: Module voor orderdetails
description: In dit onderwerp wordt beschreven wat modules voor orderdetails zijn en hoe u deze gebruikt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026012"
---
# <a name="order-details-module"></a><span data-ttu-id="df648-103">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="df648-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="df648-104">In dit onderwerp wordt beschreven wat modules voor orderdetails zijn en hoe u deze gebruikt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="df648-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="df648-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="df648-105">Overview</span></span>

<span data-ttu-id="df648-106">De module voor orderdetails wordt gebruikt om orderbevestigingsdetails weer te geven nadat een order is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="df648-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="df648-107">De id van de orderbevestiging, de contactgegevens van de order en andere ordergegevens worden weergegeven, zoals de gekochte artikelen, betalingsgegevens en verzendmethode.</span><span class="sxs-lookup"><span data-stu-id="df648-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="df648-108">Eigenschappen van orderbevestigingsmodule</span><span class="sxs-lookup"><span data-stu-id="df648-108">Order confirmation module properties</span></span>

| <span data-ttu-id="df648-109">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="df648-109">Property name</span></span>  | <span data-ttu-id="df648-110">Waarden</span><span class="sxs-lookup"><span data-stu-id="df648-110">Values</span></span> | <span data-ttu-id="df648-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="df648-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="df648-112">Koptekst</span><span class="sxs-lookup"><span data-stu-id="df648-112">Heading</span></span>        | <span data-ttu-id="df648-113">Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="df648-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="df648-114">De orderbevestigingsmodule kan een koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="df648-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="df648-115">Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="df648-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="df648-116">De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="df648-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="df648-117">Contactnummer</span><span class="sxs-lookup"><span data-stu-id="df648-117">Contact number</span></span> | <span data-ttu-id="df648-118">Text</span><span class="sxs-lookup"><span data-stu-id="df648-118">Text</span></span> | <span data-ttu-id="df648-119">Er kan een contactnummer worden opgegeven voor vragen met betrekking tot de order.</span><span class="sxs-lookup"><span data-stu-id="df648-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="df648-120">Modules die kunnen worden gebruikt op een pagina met orderdetails</span><span class="sxs-lookup"><span data-stu-id="df648-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="df648-121">Wanneer u een pagina met orderdetails maakt, kunt u behalve de module voor orderdetails ook andere relevante modules toevoegen.</span><span class="sxs-lookup"><span data-stu-id="df648-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="df648-122">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="df648-122">Here are some examples:</span></span>

- <span data-ttu-id="df648-123">**Aanbevelingsmodule**: de aanbevelingsmodule kan aan de pagina met orderdetails worden toegevoegd om suggesties voor andere producten te doen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="df648-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="df648-124">**Marketingmodules**: elke marketingmodule kan worden toegevoegd aan de pagina met orderdetails om marketinginhoud weer te geven.</span><span class="sxs-lookup"><span data-stu-id="df648-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="df648-125">Een module voor de pagina met orderdetails maken</span><span class="sxs-lookup"><span data-stu-id="df648-125">Create an order details page module</span></span>

1. <span data-ttu-id="df648-126">Maak een paginasjabloon met de naam **Sjabloon voor orderdetails**.</span><span class="sxs-lookup"><span data-stu-id="df648-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="df648-127">Voeg in het **hoofdvak** van de standaardpagina een module voor orderdetails toe.</span><span class="sxs-lookup"><span data-stu-id="df648-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="df648-128">Voeg in de module orderdetails een aanbevelingsmodule toe.</span><span class="sxs-lookup"><span data-stu-id="df648-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="df648-129">Sla de sjabloon op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="df648-129">Save and preview the template.</span></span> <span data-ttu-id="df648-130">De module voor orderdetails wordt niet weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.</span><span class="sxs-lookup"><span data-stu-id="df648-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="df648-131">Voltooi het bewerken van de sjabloon en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="df648-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="df648-132">Gebruik de sjabloon voor orderdetails die u zojuist hebt gemaakt om een pagina met de naam **Pagina met orderdetails** te maken.</span><span class="sxs-lookup"><span data-stu-id="df648-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="df648-133">Voeg de standaardpagina toe aan het paginaoverzicht.</span><span class="sxs-lookup"><span data-stu-id="df648-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="df648-134">Voeg in het vak **Koptekst** een koptekstfragment toe.</span><span class="sxs-lookup"><span data-stu-id="df648-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="df648-135">Voeg in het vak **Voettekst** een voettekstfragment toe.</span><span class="sxs-lookup"><span data-stu-id="df648-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="df648-136">Voeg in het **hoofdvak** een module voor orderdetails toe.</span><span class="sxs-lookup"><span data-stu-id="df648-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="df648-137">Voeg in het eigenschappenvenster van de module voor orderdetails de kop **Orderdetails** toe.</span><span class="sxs-lookup"><span data-stu-id="df648-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="df648-138">Voeg onder de module voor orderdetails een aanbevelingsmodule toe en configureer deze zo dat de instellingen **Nieuw** en **Best verkocht** worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="df648-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="df648-139">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="df648-139">Save and preview the page.</span></span>
1. <span data-ttu-id="df648-140">Voltooi het bewerken van de pagina en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="df648-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df648-141">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="df648-141">Additional resources</span></span>

[<span data-ttu-id="df648-142">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="df648-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="df648-143">Module Container</span><span class="sxs-lookup"><span data-stu-id="df648-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="df648-144">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="df648-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="df648-145">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="df648-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="df648-146">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="df648-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="df648-147">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="df648-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="df648-148">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="df648-148">Footer module</span></span>](author-footer-module.md)
