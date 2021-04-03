---
title: Module voor snelle weergave
description: In dit onderwerp wordt beschreven wat modules voor snelle weergave zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 07fbf8d4115561808b7c61489b343e1c72dd1b6d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243788"
---
# <a name="quick-view-module"></a><span data-ttu-id="2c3dc-103">Snelweergavemodule</span><span class="sxs-lookup"><span data-stu-id="2c3dc-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2c3dc-104">In dit onderwerp wordt beschreven wat modules voor snelle weergave zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2c3dc-105">Met de module voor snelle weergave kunnen gebruikers snel productgegevens weergeven wanneer ze door producten bladeren op een lijstpagina en een of meer producten aan het winkelwagentje toevoegen vanaf de lijstpagina, zonder naar de pagina met productgegevens te hoeven gaan.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="2c3dc-106">De module voor snelle weergave biedt een overzicht van de productgegevens die gebruikers nodig hebben om een beslissing over een toevoeging aan een winkelwagen te nemen.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="2c3dc-107">Daarnaast biedt de module een koppeling naar de pagina met productgegevens, zodat gebruikers aanvullende productdetails en inkoopopties kunnen bekijken.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="2c3dc-108">De module voor snelle weergave wordt ondersteund door de modules voor [productverzameling](product-collection-module-overview.md) en [zoekresultaten](search-result-module.md).</span><span class="sxs-lookup"><span data-stu-id="2c3dc-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c3dc-109">De module voor snelle weergave is beschikbaar vanaf Commerce 10.0.17.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="2c3dc-110">De volgende afbeelding toont een voorbeeld van een module voor snelle weergave op een pagina met een productlijst.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Voorbeeld van een module voor snelle weergave op een pagina met een productlijst](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="2c3dc-112">Module-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="2c3dc-112">Module properties</span></span>

<span data-ttu-id="2c3dc-113">De module voor snelle weergave ondersteunt enkele van dezelfde functies als de koopvakmodule.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="2c3dc-114">Daarom lijken de eigenschappen van een module voor snelle weergave op die van een koopvakmodule.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="2c3dc-115">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="2c3dc-115">Property</span></span> | <span data-ttu-id="2c3dc-116">Waarden</span><span class="sxs-lookup"><span data-stu-id="2c3dc-116">Values</span></span> | <span data-ttu-id="2c3dc-117">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2c3dc-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="2c3dc-118">Koptekstlabel</span><span class="sxs-lookup"><span data-stu-id="2c3dc-118">Heading tag</span></span> | <span data-ttu-id="2c3dc-119">**H1**, **H2**, **H3**, **H4**, **H5** of **H6**</span><span class="sxs-lookup"><span data-stu-id="2c3dc-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="2c3dc-120">Deze eigenschap bepaalt het koptekstlabel voor de producttitel.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="2c3dc-121">Als de module voor snelle weergave boven aan de pagina staat, moet deze eigenschap worden ingesteld op **H1** om te voldoen aan toegankelijkheidsstandaarden.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="2c3dc-122">Aangepaste prijs toestaan</span><span class="sxs-lookup"><span data-stu-id="2c3dc-122">Allow custom price</span></span> | <span data-ttu-id="2c3dc-123">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="2c3dc-123">**True** or **False**</span></span> | <span data-ttu-id="2c3dc-124">Als deze eigenschap is ingesteld op **Waar**, kan de gebruiker een aangepaste prijs invoeren.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="2c3dc-125">Minimumprijs</span><span class="sxs-lookup"><span data-stu-id="2c3dc-125">Minimum price</span></span> | <span data-ttu-id="2c3dc-126">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="2c3dc-126">Integer</span></span> | <span data-ttu-id="2c3dc-127">Deze eigenschap is alleen van toepassing als de eigenschap **Aangepaste prijs toestaan** is ingesteld op **Waar**.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="2c3dc-128">Hiermee wordt de minimumprijs bepaald die de gebruiker kan invoeren (bijvoorbeeld $ 1).</span><span class="sxs-lookup"><span data-stu-id="2c3dc-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="2c3dc-129">Maximumprijs</span><span class="sxs-lookup"><span data-stu-id="2c3dc-129">Maximum price</span></span> | <span data-ttu-id="2c3dc-130">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="2c3dc-130">Integer</span></span> | <span data-ttu-id="2c3dc-131">Deze eigenschap is alleen van toepassing als de eigenschap **Aangepaste prijs toestaan** is ingesteld op **Waar**.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="2c3dc-132">Hiermee wordt de maximumprijs bepaald die de gebruiker kan invoeren (bijvoorbeeld $ 1000).</span><span class="sxs-lookup"><span data-stu-id="2c3dc-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="2c3dc-133">Commerce Site Builder-instellingen</span><span class="sxs-lookup"><span data-stu-id="2c3dc-133">Commerce site builder settings</span></span>

<span data-ttu-id="2c3dc-134">Net als voor de koopvakmodule gelden voor de module voor snelle weergave de instellingen in **Site-instellingen \> Extensies \> Product toevoegen aan winkelwagen**.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="2c3dc-135">De instelling van **Navigeren naar winkelwagen** wordt echter genegeerd omdat deze niet past bij het doel van de module voor snelle weergave, namelijk gebruikers in staat stellen meerdere producten op een lijstpagina te bekijken en deze aan de winkelwagen toe te voegen zonder de lijstpagina te verlaten.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="2c3dc-136">Een module voor snelle weergave aan een productverzamelingsmodule toevoegen</span><span class="sxs-lookup"><span data-stu-id="2c3dc-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="2c3dc-137">Een module voor snelle weergave kan worden toegevoegd aan de modules voor productverzameling en zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="2c3dc-138">Voer de volgende stappen uit om een module voor snelle weergave toe te voegen aan productverzamelingsmodule in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2c3dc-139">Ga naar **Pagina's** en selecteer de startpagina voor de Fabrikam-site.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="2c3dc-140">Ga naar een module **Productverzameling** op de startpagina, selecteer het weglatingsteken (**...**) en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2c3dc-141">Selecteer in het dialoogvenster **Module toevoegen** de module **Snelle weergave** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2c3dc-142">Selecteer **Koptekst** in het eigenschappenvenster van de module **Snelle weergave**.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="2c3dc-143">Stel in het dialoogvenster **Koptekst** het veld **Koptekstniveau** in op **H2** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="2c3dc-144">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="2c3dc-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c3dc-145">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="2c3dc-145">Additional resources</span></span>

[<span data-ttu-id="2c3dc-146">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="2c3dc-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2c3dc-147">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="2c3dc-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2c3dc-148">Productverzamelingsmodule</span><span class="sxs-lookup"><span data-stu-id="2c3dc-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="2c3dc-149">Module voor zoekresultaten</span><span class="sxs-lookup"><span data-stu-id="2c3dc-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]