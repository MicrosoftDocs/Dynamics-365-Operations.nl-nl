---
title: Btw voor online orders configureren
description: Dit onderwerp biedt een overzicht van de selectie van btw-groepen voor verschillende typen online orders in Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 68b7e59a1e1ea18bdcd4e7a9117e4892407f40ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791842"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="d9038-103">Btw voor online orders configureren</span><span class="sxs-lookup"><span data-stu-id="d9038-103">Configure sales tax for online orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9038-104">Dit onderwerp biedt een overzicht van de selectie van btw-groepen voor verschillende typen online orders.</span><span class="sxs-lookup"><span data-stu-id="d9038-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="d9038-105">Uw e-commercekanaal kan opties, zoals levering of ophalen, ondersteunen voor online bestellingen.</span><span class="sxs-lookup"><span data-stu-id="d9038-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="d9038-106">De btw-toepasselijkheid is gebaseerd op de optie die door uw online gebruikers is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="d9038-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="d9038-107">Wanneer een klant ervoor kiest een artikel online te kopen en het naar een adres wordt verzonden, wordt de btw bepaald op basis van de btw-groep voor de klant.</span><span class="sxs-lookup"><span data-stu-id="d9038-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="d9038-108">Wanneer een klant een ingekocht artikel ophaalt in een winkel, wordt de btw bepaald op basis van de instelling van de btw-groep voor het ophalen in de winkel.</span><span class="sxs-lookup"><span data-stu-id="d9038-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="d9038-109">Orders die naar een klantadres zijn verzonden</span><span class="sxs-lookup"><span data-stu-id="d9038-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="d9038-110">In het algemeen wordt de btw voor online orders die naar klantadressen worden verzonden, gedefinieerd door de bestemming.</span><span class="sxs-lookup"><span data-stu-id="d9038-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="d9038-111">Elke btw-groep bevat een btw-configuratie op basis van de detailhandel waaronder uw bedrijf bestemmingsgegevens kan definiëren, zoals land/regio, staat, regio en plaats in een hiërarchische vorm.</span><span class="sxs-lookup"><span data-stu-id="d9038-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="d9038-112">Wanneer een online order wordt geplaatst, gebruikt de commerce-belastingservice het afleveradres van alle regelartikelen in de order en zoekt naar btw-groepen met dezelfde btw-criteria op basis van de bestemming.</span><span class="sxs-lookup"><span data-stu-id="d9038-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="d9038-113">Voor een online order met het afleveradres voor het artikel naar San Francisco, Californië, wordt de btw-groep en btw-code voor Californië automatisch berekend en wordt de btw voor elk artikel dienovereenkomstig berekend.</span><span class="sxs-lookup"><span data-stu-id="d9038-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="d9038-114">Op klanten gebaseerde btw-groepen</span><span class="sxs-lookup"><span data-stu-id="d9038-114">Customer-based tax groups</span></span>

<span data-ttu-id="d9038-115">In Commerce Headquarters zijn twee locaties waar btw-groepen voor klanten worden geconfigureerd:</span><span class="sxs-lookup"><span data-stu-id="d9038-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="d9038-116">**Klantprofiel**</span><span class="sxs-lookup"><span data-stu-id="d9038-116">**Customer's profile**</span></span>
- <span data-ttu-id="d9038-117">**Het verzendadres van de klant**</span><span class="sxs-lookup"><span data-stu-id="d9038-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="d9038-118">Als het klantprofiel een btw-groep heeft geconfigureerd</span><span class="sxs-lookup"><span data-stu-id="d9038-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="d9038-119">Voor het profielrecord van een klant in Headquarters is het mogelijk een btw-groep te configureren, maar voor online orders wordt de btw-groep die in het profiel van een klant is geconfigureerd, niet gebruikt voor de belastingservice.</span><span class="sxs-lookup"><span data-stu-id="d9038-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="d9038-120">Als het verzendadres van de klant een btw-groep heeft geconfigureerd</span><span class="sxs-lookup"><span data-stu-id="d9038-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="d9038-121">Als voor de verzendadres van een klant een btw-groep is geconfigureerd en daar een online order (of artikel) naartoe wordt verzonden, wordt de btw-groep die is geconfigureerd in het adresrecord van de klant gebruikt door de belastingservice voor belastingberekeningen.</span><span class="sxs-lookup"><span data-stu-id="d9038-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="d9038-122">Een btw-groep configureren voor het verzendadres van een klant</span><span class="sxs-lookup"><span data-stu-id="d9038-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="d9038-123">Voer de volgende stappen uit om een btw-groep te configureren voor het verzendadres van een klant in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="d9038-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d9038-124">Ga naar **Alle klanten** en selecteer de gewenste klant.</span><span class="sxs-lookup"><span data-stu-id="d9038-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="d9038-125">Selecteer op het sneltabblad **Adressen** het gewenste adres en selecteer vervolgens **Meer opties \> Geavanceerd**.</span><span class="sxs-lookup"><span data-stu-id="d9038-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="d9038-126">Stel onder het tabblad **Algemeen** op de pagina **Adressen beheren** de btw-waarde naar wens in.</span><span class="sxs-lookup"><span data-stu-id="d9038-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="d9038-127">De btw-groep wordt gedefinieerd met behulp van het afleveradres van de orderregel en de op bestemming gebaseerde btw wordt geconfigureerd in de btw-groep zelf.</span><span class="sxs-lookup"><span data-stu-id="d9038-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="d9038-128">Zie [Belastingen voor online winkels instellen op basis van de bestemming](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d9038-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="d9038-129">Order ophalen in de winkel</span><span class="sxs-lookup"><span data-stu-id="d9038-129">Order pickup in store</span></span>

<span data-ttu-id="d9038-130">Voor orderregels met ophalen in winkel of bij een afhaallocatie, wordt de btw-groep van de geselecteerde ophaalwinkel toegepast.</span><span class="sxs-lookup"><span data-stu-id="d9038-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="d9038-131">Zie [Andere btw-opties voor winkels instellen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores) voor meer informatie over het configureren van de btw-groep voor een bepaalde winkel.</span><span class="sxs-lookup"><span data-stu-id="d9038-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="d9038-132">Wanneer een orderregel wordt opgenomen in een winkel, worden de btw-instellingen voor het adres van de klant (indien ingesteld) genegeerd door de belastingservice en wordt de btw-configuratie van de ophaalwinkel toegepast.</span><span class="sxs-lookup"><span data-stu-id="d9038-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d9038-133">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="d9038-133">Additional resources</span></span>

[<span data-ttu-id="d9038-134">Btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="d9038-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="d9038-135">Btw-berekeningsmethoden in het veld Oorsprong</span><span class="sxs-lookup"><span data-stu-id="d9038-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="d9038-136">Btw-overeenkomst en -overschrijvingen</span><span class="sxs-lookup"><span data-stu-id="d9038-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="d9038-137">Berekeningsopties Volledige bedrag en interval voor btw-codes</span><span class="sxs-lookup"><span data-stu-id="d9038-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="d9038-138">Berekening van btw-vrijstelling</span><span class="sxs-lookup"><span data-stu-id="d9038-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]