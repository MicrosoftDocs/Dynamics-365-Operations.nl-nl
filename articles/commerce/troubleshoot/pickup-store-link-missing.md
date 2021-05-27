---
title: Optie Dit ophalen wordt niet weergegeven op winkelwagen- of productdetailpagina's
description: Dit onderwerp bevat richtlijnen voor probleemoplossing die kunnen helpen wanneer de optie voor ophalen in een winkel niet wordt weergegeven op de winkelwagen- of productdetailpagina's.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f692d73bf1755422e9bfc8314c1156e043ccf761
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020800"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="0b511-103">Optie 'Dit ophalen' wordt niet weergegeven op winkelwagen- of productdetailpagina's</span><span class="sxs-lookup"><span data-stu-id="0b511-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b511-104">Dit onderwerp bevat richtlijnen voor probleemoplossing die kunnen helpen wanneer de optie voor ophalen in een winkel niet wordt weergegeven op de winkelwagen- of productdetailpagina's.</span><span class="sxs-lookup"><span data-stu-id="0b511-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="0b511-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0b511-105">Description</span></span>

<span data-ttu-id="0b511-106">De knop **Dit ophalen** wordt niet weergegeven op de winkelwagen- of productdetailpagina's.</span><span class="sxs-lookup"><span data-stu-id="0b511-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="0b511-107">In de volgende afbeelding ziet u een voorbeeld van een pagina met de knop **Dit ophalen**.</span><span class="sxs-lookup"><span data-stu-id="0b511-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Knop Dit ophalen](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="0b511-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="0b511-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="0b511-110">De BOPIS-extensie inschakelen in Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="0b511-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="0b511-111">Volg deze stappen om de extensie 'online kopen, ophalen in winkel' (BOPIS) in Commerce Site Builder in te stellen.</span><span class="sxs-lookup"><span data-stu-id="0b511-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0b511-112">Selecteer uw site.</span><span class="sxs-lookup"><span data-stu-id="0b511-112">Select your site.</span></span>
1. <span data-ttu-id="0b511-113">Selecteer **Site-instellingen** en selecteer vervolgens **Uitbreidingen**.</span><span class="sxs-lookup"><span data-stu-id="0b511-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="0b511-114">Zorg ervoor dat de optie **BOPIS uitschakelen** is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0b511-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="0b511-115">Leveringsmethoden configureren in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="0b511-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="0b511-116">Voer deze stappen uit om leveringsmethoden te configureren in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0b511-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0b511-117">Ga naar **Inkoop en sourcing \> Instellingen \> Leveringsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="0b511-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="0b511-118">Zorg ervoor dat er een leveringsmodus **Ophalen door klant** is gemaakt en dat er producten en adressen aan zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="0b511-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="0b511-119">Ga naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters**.</span><span class="sxs-lookup"><span data-stu-id="0b511-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="0b511-120">Selecteer **Klantorders** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="0b511-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="0b511-121">Controleer of **Ophaalmodus van levering** correct is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="0b511-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="0b511-122">Betalingen van klantorders configureren</span><span class="sxs-lookup"><span data-stu-id="0b511-122">Configure customer orders payments</span></span>

<span data-ttu-id="0b511-123">Voer deze stappen uit om betalingen van klantorders te configureren in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0b511-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0b511-124">Ga naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters**.</span><span class="sxs-lookup"><span data-stu-id="0b511-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="0b511-125">Selecteer **Klantorders** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="0b511-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="0b511-126">Ga naar het sneltabblad **Betalingen** en controleer of de velden **Betalingstermijn** en **Betalingsmethode** correct zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0b511-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b511-127">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0b511-127">Additional resources</span></span>

[<span data-ttu-id="0b511-128">BOPIS configureren</span><span class="sxs-lookup"><span data-stu-id="0b511-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="0b511-129">Meerdere ophaal- en bezorgmethodes inschakelen voor klantorders</span><span class="sxs-lookup"><span data-stu-id="0b511-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="0b511-130">Commerce-orderbetalingen voor meerdere kanalen</span><span class="sxs-lookup"><span data-stu-id="0b511-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="0b511-131">Winkelselectiemodule</span><span class="sxs-lookup"><span data-stu-id="0b511-131">Store selector module</span></span>](../store-selector.md)
