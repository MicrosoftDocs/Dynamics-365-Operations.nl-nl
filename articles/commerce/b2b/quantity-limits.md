---
title: De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites
description: In dit onderwerp wordt beschreven hoe u limieten voor producthoeveelheid instelt voor B2B-e-commercesites (business-to-business).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e9f14bc9aa6586e87f3e8ccb82e63d0ec2e46534
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799776"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="7c83b-103">De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites</span><span class="sxs-lookup"><span data-stu-id="7c83b-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c83b-104">In dit onderwerp wordt beschreven hoe u limieten voor producthoeveelheid instelt voor B2B-e-commercesites (business-to-business).</span><span class="sxs-lookup"><span data-stu-id="7c83b-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="7c83b-105">De meeste producten hebben een maateenheid die hun groepering bepaalt.</span><span class="sxs-lookup"><span data-stu-id="7c83b-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="7c83b-106">De groepering heeft invloed op de manier waarop de producten kunnen worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="7c83b-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="7c83b-107">Sommige producten hebben mogelijk een extra groepering voor hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="7c83b-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="7c83b-108">Deze groepering bepaalt of de producten kunnen worden verkocht als afzonderlijke eenheden of veelvouden en of er een minimale of maximale orderhoeveelheidlimiet is die moet worden gevolgd.</span><span class="sxs-lookup"><span data-stu-id="7c83b-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="7c83b-109">De functionaliteit voor het beperken van hoeveelheden zorgt ervoor dat de minimale, maximale, meervoudige en standaardhoeveelheden die in Microsoft Dynamics 365 Commerce zijn geconfigureerd (in de standaardorderinstellingen of de site-instellingen van Commerce Site Builder), worden toegepast op klantorders die op een e-commercesite worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="7c83b-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="7c83b-110">Producthoeveelheidslimieten worden momenteel niet ondersteund voor het POS (Point of Sale) en callcenters.</span><span class="sxs-lookup"><span data-stu-id="7c83b-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="7c83b-111">Veel detailhandelaren bieden de optie van klantorders, oftewel speciale orders, om aan verschillende product- en afhandelingsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="7c83b-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="7c83b-112">Hierna vindt u enkele typische scenario's:</span><span class="sxs-lookup"><span data-stu-id="7c83b-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="7c83b-113">Een klant wil dat bepaalde varianten van producten in veelvouden van een paar worden verkocht.</span><span class="sxs-lookup"><span data-stu-id="7c83b-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="7c83b-114">Een klant wil producten bij een andere winkel of locatie ophalen dan de winkel of locatie waar de klant deze producten heeft gekocht.</span><span class="sxs-lookup"><span data-stu-id="7c83b-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="7c83b-115">De verpakkingsstandaarden voor de winkels verschillen echter van de verpakkingsstandaarden voor online verkoopdistributie.</span><span class="sxs-lookup"><span data-stu-id="7c83b-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="7c83b-116">Een klant wil een limited-edition product kopen met een maximale hoeveelheidslimiet voor artikelen die kunnen worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="7c83b-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="7c83b-117">De functie voor standaardorderinstellingen in Commerce Headquarters inschakelen</span><span class="sxs-lookup"><span data-stu-id="7c83b-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="7c83b-118">Voordat u limieten voor producthoeveelheden kunt instellen, moet de standaardfunctie voor orderinstellingen zijn ingeschakeld in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7c83b-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="7c83b-119">Voer de volgende stappen uit om de functie voor standaardorderinstellingen in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="7c83b-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="7c83b-120">Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="7c83b-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="7c83b-121">Zoek en selecteer de functie **De site- en standaardorderinstellingen in de klantorder ondersteunen**.</span><span class="sxs-lookup"><span data-stu-id="7c83b-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="7c83b-122">Selecteer **Nu inschakelen** onder in het rechterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="7c83b-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="7c83b-123">Kwaliteitsinstellingen definiëren</span><span class="sxs-lookup"><span data-stu-id="7c83b-123">Define quantity settings</span></span> 

<span data-ttu-id="7c83b-124">U definieert de kwaliteitsinstellingen op de pagina **Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="7c83b-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="7c83b-125">Voer de volgende stappen uit om de kwaliteitsinstellingen op te geven.</span><span class="sxs-lookup"><span data-stu-id="7c83b-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="7c83b-126">Ga naar Product **Retail en Commerce \> Producten en categorieën \> Vrijgegeven producten per categorie**.</span><span class="sxs-lookup"><span data-stu-id="7c83b-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="7c83b-127">Selecteer een vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="7c83b-127">Select a released product.</span></span>
1. <span data-ttu-id="7c83b-128">Selecteer in het actievenster op het tabblad **Voorraadbeheer** in de groep **Orderinstellingen** de optie **Standaardorderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="7c83b-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="7c83b-129">Stel op de pagina **Standaardorderinstellingen** op het sneltabblad **Verkooporder** in de sectie **Verkoophoeveelheid** de hoeveelheden voor productverkoop in:</span><span class="sxs-lookup"><span data-stu-id="7c83b-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="7c83b-130">**Veelvoud**: de hoeveelheid waarvoor het product in veelvouden kan worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="7c83b-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="7c83b-131">**Minimumorderhoeveelheid**: het minimum aantal producten dat moet worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="7c83b-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="7c83b-132">**Maximumorderhoeveelheid**: het maximum aantal producten dat kan worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="7c83b-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="7c83b-133">**Standaardorderhoeveelheid**: de standaardhoeveelheid die automatisch wordt ingevoerd wanneer het product wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="7c83b-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="7c83b-134">De functionaliteit voor hoeveelheidslimieten voor B2B-orders inschakelen in Commerce Site Builder</span><span class="sxs-lookup"><span data-stu-id="7c83b-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="7c83b-135">Voer deze stappen uit om de functionaliteit voor hoeveelheidslimieten voor B2B-orders in te schakelen in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="7c83b-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="7c83b-136">Ga naar **Site-instellingen \> Extensies**</span><span class="sxs-lookup"><span data-stu-id="7c83b-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="7c83b-137">Selecteer onder **Limieten voor orderhoeveelheid inschakelen** de optie **Ingeschakeld voor B2B-klanten** in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="7c83b-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="7c83b-138">Bijgewerkte Site Builder-instellingen worden pas van kracht nadat het bestand app.settings.json is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="7c83b-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="7c83b-139">Zie [Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7c83b-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c83b-140">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="7c83b-140">Additional resources</span></span>

[<span data-ttu-id="7c83b-141">Een B2B-e-commercesite instellen</span><span class="sxs-lookup"><span data-stu-id="7c83b-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="7c83b-142">Hiërarchieën voor organisatiemodellering voor B2B-organisaties maken</span><span class="sxs-lookup"><span data-stu-id="7c83b-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="7c83b-143">Gebruikers van zakelijke partners beheren op e-commercesites voor B2B</span><span class="sxs-lookup"><span data-stu-id="7c83b-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="7c83b-144">De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites</span><span class="sxs-lookup"><span data-stu-id="7c83b-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]