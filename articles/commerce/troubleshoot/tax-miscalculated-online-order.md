---
title: De btw op online orders wordt onjuist berekend
description: Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen bij het foutief berekenen van btw op online orders of wanneer de btw-groep op de verkoopregel niet juist is ingesteld.
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
ms.openlocfilehash: f7cef533d76bdddfbad2e8c5f84f81ef62bccc38
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021098"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="713be-103">De btw op online orders wordt onjuist berekend</span><span class="sxs-lookup"><span data-stu-id="713be-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="713be-104">Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen bij het foutief berekenen van btw op online orders of wanneer de btw-groep op de verkoopregel niet juist is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="713be-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="713be-105">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="713be-105">Description</span></span>

<span data-ttu-id="713be-106">Wanneer een e-commerce-order wordt geplaatst, wordt de btw onjuist berekend of wordt de btw-groep op de verkoopregel onjuist ingesteld.</span><span class="sxs-lookup"><span data-stu-id="713be-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="713be-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="713be-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="713be-108">De btw configureren voor een detailhandelwinkel in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="713be-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="713be-109">Voer deze stappen uit om btw te configureren voor een detailhandelwinkel in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="713be-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="713be-110">Ga naar **Retail en commerce \> Afzetkanalen \> Alle winkels**.</span><span class="sxs-lookup"><span data-stu-id="713be-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="713be-111">Selecteer de winkel waarvoor u btw wilt configureren.</span><span class="sxs-lookup"><span data-stu-id="713be-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="713be-112">Configureer op het sneltabblad **Algemeen** in de sectie **Btw** de btw-gegevens voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="713be-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="713be-113">Als een product uit een winkel wordt opgehaald, wordt de btw-groep opgehaald uit de winkel die is geselecteerd om bij op te halen.</span><span class="sxs-lookup"><span data-stu-id="713be-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="713be-114">Zie [Andere btw-opties voor winkels instellen](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="713be-114">For more information, see [Set other tax options for stores](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="713be-115">De btw configureren voor het adres van een klant in Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="713be-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="713be-116">Voer deze stappen uit om btw te configureren voor het adres van een klant in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="713be-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="713be-117">Ga naar **Klanten \> Klanten \> Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="713be-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="713be-118">Selecteer de klant voor wie u btw wilt configureren.</span><span class="sxs-lookup"><span data-stu-id="713be-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="713be-119">Selecteer op het sneltabblad **Adressen** het adres waarvoor u btw wilt configureren, selecteer **Meer opties** en selecteer vervolgens **Geavanceerd**.</span><span class="sxs-lookup"><span data-stu-id="713be-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="713be-120">Selecteer de optie **Btw-groep** op het tabblad **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="713be-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="713be-121">Selecteer de juiste waarde in het veld **Btw**.</span><span class="sxs-lookup"><span data-stu-id="713be-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="713be-122">Voor verzending waarbij btw op het adres van de klant is betrokken, bepaalt het afleveradres van de regel de btw-groep voor de regel.</span><span class="sxs-lookup"><span data-stu-id="713be-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="713be-123">Als de klant verzendt naar een bestaand adres dat al een btw-groep heeft geconfigureerd, wordt de bestaande btw-groep gebruikt.</span><span class="sxs-lookup"><span data-stu-id="713be-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="713be-124">Adressen hebben standaard geen btw-groep wanneer ze worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="713be-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="713be-125">Algemene btw-groepen configureren in Commerce headquarters</span><span class="sxs-lookup"><span data-stu-id="713be-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="713be-126">Voer deze stappen uit om algemene btw-groepen te configureren in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="713be-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="713be-127">Ga naar **Btw \> Indirecte belastingen \> Btw \> Btw-groep**.</span><span class="sxs-lookup"><span data-stu-id="713be-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="713be-128">Selecteer in de linkernavigatie de btw-groep die u wilt configureren.</span><span class="sxs-lookup"><span data-stu-id="713be-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="713be-129">Configureer op het sneltabblad **Op retailbestemming gebaseerde btw** de btw voor de btw-groep.</span><span class="sxs-lookup"><span data-stu-id="713be-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="713be-130">Voor verzending waarbij geen btw op het adres van de klant is betrokken, wordt de btw-groep bepaald door het afleveradres van de regel en de op bestemming gebaseerde btw die zijn geconfigureerd voor de btw-groep.</span><span class="sxs-lookup"><span data-stu-id="713be-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="713be-131">Zie [Belastingen voor online winkels instellen op basis van de bestemming](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="713be-131">For more information, see [Set up taxes for online stores based on destination](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="713be-132">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="713be-132">Additional resources</span></span>

[<span data-ttu-id="713be-133">Btw voor online orders configureren</span><span class="sxs-lookup"><span data-stu-id="713be-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)