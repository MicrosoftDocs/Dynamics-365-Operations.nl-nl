---
title: De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites
description: In dit onderwerp wordt beschreven hoe u de betalingsmethode voor klantrekeningen configureert voor B2B-e-commercesites (business-to-business).
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
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799800"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="3179b-103">De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites</span><span class="sxs-lookup"><span data-stu-id="3179b-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3179b-104">In dit onderwerp wordt beschreven hoe u de betalingsmethode voor klantrekeningen configureert voor B2B-e-commercesites (business-to-business).</span><span class="sxs-lookup"><span data-stu-id="3179b-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="3179b-105">Detailhandelaren kunnen verschillende typen betalingen accepteren voor de producten en diensten die ze verkopen in een e-commercekanaal.</span><span class="sxs-lookup"><span data-stu-id="3179b-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="3179b-106">Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd in Microsoft Dynamics 365 Commerce wanneer het systeem wordt ingesteld.</span><span class="sxs-lookup"><span data-stu-id="3179b-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="3179b-107">De betalingsmethode voor de klantrekening (of 'a conto') moet worden ondersteund op B2B-e-commercesites.</span><span class="sxs-lookup"><span data-stu-id="3179b-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="3179b-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="3179b-108">Prerequisites</span></span>

1. <span data-ttu-id="3179b-109">Voeg de betalingsmethode voor klantrekeningen toe in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3179b-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="3179b-110">Koppel de betalingsmethode voor de klantrekening aan het e-commercekanaal.</span><span class="sxs-lookup"><span data-stu-id="3179b-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="3179b-111">Zorg ervoor dat **Op rekening toestaan** is ingeschakeld voor de klant bij **Retail en commerce \> Klanten \> Alle klanten \> Standaardwaarden betalingen** in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3179b-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="3179b-112">Zorg er ook voor dat de parameters voor **Kredietlimiet** goed zijn ingesteld voor de klant bij **Retail en commerce \> Klanten \> Alle klnanten \> Crediteringen en aanmaningen** in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="3179b-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="3179b-113">De betalingsmethode voor de klantrekening inschakelen in Commerce-site builder</span><span class="sxs-lookup"><span data-stu-id="3179b-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="3179b-114">Volg deze stappen om de betalingsmethode voor de klantrekening in te schakelen in Commerce-site builder.</span><span class="sxs-lookup"><span data-stu-id="3179b-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="3179b-115">Ga naar **Site-instellingen \> Extensies**.</span><span class="sxs-lookup"><span data-stu-id="3179b-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="3179b-116">Stel de eigenschap **Betalingen van klantrekeningen inschakelen** in op **Ingeschakeld voor B2B-klanten**.</span><span class="sxs-lookup"><span data-stu-id="3179b-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="3179b-117">Selecteer **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="3179b-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="3179b-118">De nieuwe site-instellingen worden pas van kracht nadat het bestand app.settings.json is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="3179b-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="3179b-119">Zie [Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3179b-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="3179b-120">De betalingsmethode voor de klantrekening inschakelen op de uitcheckpagina voor de B2B-e-commercesite</span><span class="sxs-lookup"><span data-stu-id="3179b-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="3179b-121">Volg deze stappen om de betalingsmethode voor de klantrekening in te schakelen op de uitcheckpagina voor de B2B-e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="3179b-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="3179b-122">In de Commerce-site builder kunt u de uitcheckpagina of het fragment bekijken en bewerken met de uitcheckmodule voor de B2B-e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="3179b-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="3179b-123">Selecteer in het vak **Container van uitchecksectie** de optie **Module toevoegen** en voeg vervolgens een module **Betaling van klantrekening** toe.</span><span class="sxs-lookup"><span data-stu-id="3179b-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="3179b-124">Plaats de module **Betalingen van klantrekening** door de ellipen (**...**) te selecteren en vervolgens **Omhoog** of **Omlaag** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="3179b-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="3179b-125">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="3179b-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="3179b-126">Controleren of de betalingsmethode voor de klantrekening is ingeschakeld en gepubliceerd</span><span class="sxs-lookup"><span data-stu-id="3179b-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="3179b-127">Volg deze stappen om te controleren of de betalingsmethode voor de klantrekening is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="3179b-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="3179b-128">Meld u aan bij de e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="3179b-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="3179b-129">Voeg een product aan de winkelwagen toe.</span><span class="sxs-lookup"><span data-stu-id="3179b-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="3179b-130">Ga naar de uitcheckpagina.</span><span class="sxs-lookup"><span data-stu-id="3179b-130">Go to the checkout page.</span></span> <span data-ttu-id="3179b-131">U ziet nu de nieuwe betalingsmethode voor de **Klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="3179b-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3179b-132">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="3179b-132">Additional resources</span></span>

[<span data-ttu-id="3179b-133">Een B2B-e-commercesite instellen</span><span class="sxs-lookup"><span data-stu-id="3179b-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="3179b-134">Hiërarchieën voor organisatiemodellering voor B2B-organisaties maken</span><span class="sxs-lookup"><span data-stu-id="3179b-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="3179b-135">Gebruikers van zakenpartners op B2B-sites voor e-commerce beheren</span><span class="sxs-lookup"><span data-stu-id="3179b-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="3179b-136">De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites</span><span class="sxs-lookup"><span data-stu-id="3179b-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="3179b-137">Updates voor SDK's en modulebibliotheken</span><span class="sxs-lookup"><span data-stu-id="3179b-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]