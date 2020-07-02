---
title: Module voor orderdetails
description: In dit onderwerp wordt beschreven wat modules voor orderdetails zijn en hoe u deze gebruikt in Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464925"
---
# <a name="order-details-module"></a><span data-ttu-id="0c95b-103">Module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="0c95b-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0c95b-104">In dit onderwerp wordt beschreven wat modules voor orderdetails zijn en hoe u deze gebruikt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0c95b-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0c95b-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="0c95b-105">Overview</span></span>

<span data-ttu-id="0c95b-106">De module voor orderdetails wordt gebruikt om orderbevestigingsdetails weer te geven nadat een order is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="0c95b-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="0c95b-107">De id van de orderbevestiging, de contactgegevens van de order en andere ordergegevens worden weergegeven, zoals de gekochte artikelen, betalingsgegevens en verzendmethode.</span><span class="sxs-lookup"><span data-stu-id="0c95b-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="0c95b-108">Eigenschappen van module voor orderdetails</span><span class="sxs-lookup"><span data-stu-id="0c95b-108">Order details module properties</span></span>

| <span data-ttu-id="0c95b-109">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="0c95b-109">Property name</span></span>  | <span data-ttu-id="0c95b-110">Waarden</span><span class="sxs-lookup"><span data-stu-id="0c95b-110">Values</span></span> | <span data-ttu-id="0c95b-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="0c95b-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0c95b-112">Kop</span><span class="sxs-lookup"><span data-stu-id="0c95b-112">Heading</span></span>        | <span data-ttu-id="0c95b-113">Koptekst en tag voor koptekst (**H1**, **H2**, **H3**, **H4**, **H5** of **H6**)</span><span class="sxs-lookup"><span data-stu-id="0c95b-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0c95b-114">De module voor orderdetails kan een koptekst hebben.</span><span class="sxs-lookup"><span data-stu-id="0c95b-114">The order details module can have a heading.</span></span> <span data-ttu-id="0c95b-115">Standaard wordt de kopteksttag **H2** gebruikt voor de koptekst.</span><span class="sxs-lookup"><span data-stu-id="0c95b-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0c95b-116">De tag kan echter worden gewijzigd om aan de toegankelijkheidsvereisten te voldoen.</span><span class="sxs-lookup"><span data-stu-id="0c95b-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0c95b-117">Contactnummer</span><span class="sxs-lookup"><span data-stu-id="0c95b-117">Contact number</span></span> | <span data-ttu-id="0c95b-118">Text</span><span class="sxs-lookup"><span data-stu-id="0c95b-118">Text</span></span> | <span data-ttu-id="0c95b-119">Er kan een contactnummer worden opgegeven voor vragen met betrekking tot de order.</span><span class="sxs-lookup"><span data-stu-id="0c95b-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="0c95b-120">Modules die kunnen worden gebruikt op een pagina met orderdetails</span><span class="sxs-lookup"><span data-stu-id="0c95b-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="0c95b-121">Wanneer u een pagina met orderdetails maakt, kunt u behalve de module voor orderdetails ook andere relevante modules toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0c95b-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="0c95b-122">Hieronder volgen een aantal voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="0c95b-122">Here are some examples:</span></span>

- <span data-ttu-id="0c95b-123">**Aanbevelingsmodule**: de aanbevelingsmodule kan aan de pagina met orderdetails worden toegevoegd om suggesties voor andere producten te doen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="0c95b-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="0c95b-124">**Marketingmodules**: elke marketingmodule kan worden toegevoegd aan de pagina met orderdetails om marketinginhoud weer te geven.</span><span class="sxs-lookup"><span data-stu-id="0c95b-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="0c95b-125">Een module voor orderdetails toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="0c95b-125">Add an order details module to a page</span></span>

<span data-ttu-id="0c95b-126">Voer de volgende stappen uit om een module voor orderdetails aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="0c95b-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0c95b-127">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="0c95b-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0c95b-128">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** de naam in voor **Sjabloon voor orderdetails** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0c95b-129">Selecteer het weglatingsteken (**...**) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0c95b-130">Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0c95b-131">Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0c95b-132">Selecteer in het dialoogvenster **Module toevoegen** de **Module voor orderdetails** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0c95b-133">Selecteer **Opslaan** en vervolgens **Preview** om de sjabloon te bekijken.</span><span class="sxs-lookup"><span data-stu-id="0c95b-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="0c95b-134">De module voor orderdetails wordt niet weergegeven omdat hiervoor de context van het bevestigingsnummer is vereist.</span><span class="sxs-lookup"><span data-stu-id="0c95b-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="0c95b-135">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="0c95b-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0c95b-136">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="0c95b-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0c95b-137">Selecteer in het dialoogvenster **Een sjabloon kiezen** de **Sjabloon voor orderdetails**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="0c95b-138">Voer onder **Paginanaam** **Pagina voor orderdetails** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0c95b-139">Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0c95b-140">Selecteer in het dialoogvenster **Module toevoegen** de **Module voor orderdetails** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0c95b-141">Selecteer in het eigenschappenvenster van de module voor orderdetails de optie **Kop** naast het potloodsymbool.</span><span class="sxs-lookup"><span data-stu-id="0c95b-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="0c95b-142">Voer in het veld **Koptekst** van het dialoogvenster **Koptekst** de koptekst **OrderDetails** in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c95b-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="0c95b-143">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="0c95b-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0c95b-144">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="0c95b-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c95b-145">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="0c95b-145">Additional resources</span></span>

[<span data-ttu-id="0c95b-146">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="0c95b-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0c95b-147">Containermodule</span><span class="sxs-lookup"><span data-stu-id="0c95b-147">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0c95b-148">Koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="0c95b-148">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0c95b-149">Winkelwagenmodule</span><span class="sxs-lookup"><span data-stu-id="0c95b-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0c95b-150">Kassamodule</span><span class="sxs-lookup"><span data-stu-id="0c95b-150">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0c95b-151">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="0c95b-151">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0c95b-152">Voettekstmodule</span><span class="sxs-lookup"><span data-stu-id="0c95b-152">Footer module</span></span>](author-footer-module.md)
