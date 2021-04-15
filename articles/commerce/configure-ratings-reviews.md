---
title: Beoordelingen en recensies configureren
description: In dit onderwerp wordt beschreven hoe u uw e-commerce site kunt configureren voor het weergeven van beoordelingen en recensies van klanten in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5161755b9e15e93fbb5eeb6404ea0820f7068ea7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796070"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="ad0dc-103">Beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="ad0dc-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad0dc-104">In dit onderwerp wordt beschreven hoe u uw e-commerce site kunt configureren voor het weergeven van beoordelingen en recensies van klanten in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ad0dc-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="ad0dc-105">Overview</span></span>

<span data-ttu-id="ad0dc-106">Beoordelingen en recensies over e-commerce-websites geven klanten meer informatie over producten voordat ze een inkoopbeslissing nemen, door te laten zien wat andere klanten van deze producten vinden.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="ad0dc-107">Voor e-commerce-websites zijn beoordelingen en recensies ook een mechanisme voor het verzamelen van klantfeedback over producten.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="ad0dc-108">Een site met beoordelingen en recensies configureren</span><span class="sxs-lookup"><span data-stu-id="ad0dc-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="ad0dc-109">Configuratiewaarden voor beoordelingen en recensies, zoals de tenant-id, de lengte van de recensietekst en de lengte van de recensietitel worden op siteniveau geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="ad0dc-110">Voer de volgende stappen uit om een site te configureren voor het weergeven van beoordelingen en recensies.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="ad0dc-111">Ga naar **Startpagina \> Sites**.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="ad0dc-112">Selecteer de naam van uw site.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="ad0dc-113">Ga naar **Vestigingsinstellingen \> Uitbreidingen**.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="ad0dc-114">Voer in het veld **Maximale lengte recensietekst** het maximumaantal tekens in dat de recensietekst kan bevatten (bijvoorbeeld **1000**).</span><span class="sxs-lookup"><span data-stu-id="ad0dc-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="ad0dc-115">Voer in het veld **Maximale lengte recensietitel** het maximumaantal tekens in dat de recensietitel kan bevatten (bijvoorbeeld **55**).</span><span class="sxs-lookup"><span data-stu-id="ad0dc-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="ad0dc-116">Selecteer **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="ad0dc-117">In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Een site met beoordelingen en recensies configureren](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="ad0dc-119">Een productbeoordeling koppelen aan de sectie Recensies van een PDP</span><span class="sxs-lookup"><span data-stu-id="ad0dc-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="ad0dc-120">Een productbeoordeling wordt onder de producttitel boven aan de PDP weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="ad0dc-121">De productbeoordeling kan zo worden geconfigureerd dat deze wordt gekoppeld aan de sectie **Recensies** van dezelfde PDP.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="ad0dc-122">Voer de volgende stappen uit om een productbeoordeling te koppelen aan de sectie **Recensies** van de PDP.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="ad0dc-123">Open de PDP-sjabloon.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="ad0dc-124">Ga naar **Instellingen van module voor koopvakcontainer**.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="ad0dc-125">Selecteer onder **Koopvak** de optie **Productbeoordelingen** en schakel vervolgens het selectievakje **Klikken koppelen aan module met volledige recensies** in.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="ad0dc-126">In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Een productbeoordeling koppelen aan de sectie Recensies van een PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="ad0dc-128">De koppeling naar de pagina Privacy en beleid configureren</span><span class="sxs-lookup"><span data-stu-id="ad0dc-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="ad0dc-129">Volg deze stappen om de koppeling naar de pagina Privacy en beleid te configureren</span><span class="sxs-lookup"><span data-stu-id="ad0dc-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="ad0dc-130">Ga naar **Startpagina \> Sites**.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="ad0dc-131">Selecteer de naam van uw site.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="ad0dc-132">Ga naar **Vestigingsinstellingen \> Uitbreidingen**.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="ad0dc-133">Selecteer op het tabblad **Routes** onder **RNR privacy en beleid** de optie **Een koppeling toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="ad0dc-134">Als er al een koppeling is ingevoerd en u deze wilt vervangen, selecteert u de koppeling.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="ad0dc-135">Selecteer in het dialoogvenster **Een koppeling toevoegen** de koppeling voor de pagina Privacy en beleid en selecteer vervolgens **OK.**</span><span class="sxs-lookup"><span data-stu-id="ad0dc-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="ad0dc-136">Selecteer **Opslaan en publiceren**.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="ad0dc-137">In de volgende afbeelding ziet u hoe deze configuratie uitziet in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![De koppeling naar de pagina Privacy en beleid configureren](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="ad0dc-139">Modules voor beoordelingen en recensies configureren op pagina's met productdetails</span><span class="sxs-lookup"><span data-stu-id="ad0dc-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="ad0dc-140">Zie [Modules voor beoordelingen en recensies](ratings-reviews-modules.md) voor meer informatie over het configureren van de modules voor beoordelingen en recensies op pagina's met productdetails.</span><span class="sxs-lookup"><span data-stu-id="ad0dc-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad0dc-141">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ad0dc-141">Additional resources</span></span>

[<span data-ttu-id="ad0dc-142">Overzicht beoordelingen en recensies</span><span class="sxs-lookup"><span data-stu-id="ad0dc-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="ad0dc-143">Aanmelden om beoordelingen en recensies te gebruiken</span><span class="sxs-lookup"><span data-stu-id="ad0dc-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="ad0dc-144">Beoordelingen en recensies beheren</span><span class="sxs-lookup"><span data-stu-id="ad0dc-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="ad0dc-145">Modules voor beoordelingen en recensies configureren op pagina's met productdetails</span><span class="sxs-lookup"><span data-stu-id="ad0dc-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="ad0dc-146">Productbeoordelingen synchroniseren in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="ad0dc-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]