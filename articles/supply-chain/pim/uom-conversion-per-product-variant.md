---
title: Conversie van maateenheid per productvariant
description: In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204488"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="f348d-103">Conversie van maateenheid per productvariant</span><span class="sxs-lookup"><span data-stu-id="f348d-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f348d-104">In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten.</span><span class="sxs-lookup"><span data-stu-id="f348d-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="f348d-105">Het bevat een voorbeeld van de instellingen.</span><span class="sxs-lookup"><span data-stu-id="f348d-105">It includes an example of the setup.</span></span>

<span data-ttu-id="f348d-106">Met deze functie kunnen bedrijven verschillende eenheidconversies tussen de varianten van hetzelfde product definiëren.</span><span class="sxs-lookup"><span data-stu-id="f348d-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="f348d-107">Het volgende voorbeeld wordt gebruikt in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="f348d-107">The following example is used in this topic.</span></span> <span data-ttu-id="f348d-108">Een bedrijf verkoopt T-shirts in de maten Small, Medium, Large en Extra large.</span><span class="sxs-lookup"><span data-stu-id="f348d-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="f348d-109">Het T-shirt is gedefinieerd als een product en de verschillende maten zijn gedefinieerd als varianten van het product.</span><span class="sxs-lookup"><span data-stu-id="f348d-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="f348d-110">De T-shirts zijn verpakt in dozen en er passen vijf T-shirts in een doos, met uitzondering van de T-shirts met de maat Extra large, waarvan er maar vier passen in een doos.</span><span class="sxs-lookup"><span data-stu-id="f348d-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="f348d-111">Het bedrijf wil de verschillende varianten van de T-shirts in de eenheid **Stuks** bijhouden, maar verkoopt de T-shirts in de eenheid **Dozen**.</span><span class="sxs-lookup"><span data-stu-id="f348d-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="f348d-112">De conversie tussen de voorraadeenheid en de verkoopeenheid is 1 doos = 5 stuks, met uitzondering van de variant Extra large waarvoor de conversie 1 doos = 4 stuks geldt.</span><span class="sxs-lookup"><span data-stu-id="f348d-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="f348d-113">Een product voor eenheidconversie per variant instellen</span><span class="sxs-lookup"><span data-stu-id="f348d-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="f348d-114">Productvarianten kunnen alleen worden gemaakt voor producten van het **productsubtype** **Productmodel**.</span><span class="sxs-lookup"><span data-stu-id="f348d-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="f348d-115">Zie [Een productmodel maken](tasks/create-product-master.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f348d-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="f348d-116">De functie is niet ingeschakeld voor producten die zijn ingesteld voor processen van het type Variabel gewicht.</span><span class="sxs-lookup"><span data-stu-id="f348d-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="f348d-117">Wanneer het productmodel met vrijgegeven productvarianten is gemaakt, kunnen eenheidconversies per variant worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="f348d-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="f348d-118">U kunt het menu-item voor het openen van de pagina voor eenheidconversie in de context van een product of productvariant vinden op de volgende pagina's.</span><span class="sxs-lookup"><span data-stu-id="f348d-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="f348d-119">De pagina **Productgegevens**</span><span class="sxs-lookup"><span data-stu-id="f348d-119">**Product details** page</span></span>
-   <span data-ttu-id="f348d-120">De pagina **Details van vrijgegeven producten**</span><span class="sxs-lookup"><span data-stu-id="f348d-120">**Released products details** page</span></span>
-   <span data-ttu-id="f348d-121">De pagina **Vrijgegeven productvarianten**</span><span class="sxs-lookup"><span data-stu-id="f348d-121">**Released product variants** page</span></span>

<span data-ttu-id="f348d-122">Wanneer u de pagina **Eenheidsomrekening** in de context van een productmodel of vrijgegeven productvariant opent, kunt u opgeven of u de eenheidconversie voor het product of een productvariant wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="f348d-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="f348d-123">U doet dit door **Productvariant** of **Product** te selecteren in het veld **Conversie maken voor**.</span><span class="sxs-lookup"><span data-stu-id="f348d-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="f348d-124">Productvariant</span><span class="sxs-lookup"><span data-stu-id="f348d-124">Product variant</span></span>

<span data-ttu-id="f348d-125">Als u **Productvariant** selecteert, kunt u in het veld **Productvariant** opgeven voor welke variant u de eenheidconversie wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="f348d-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="f348d-126">Artikel</span><span class="sxs-lookup"><span data-stu-id="f348d-126">Product</span></span>

<span data-ttu-id="f348d-127">Als u **Product** selecteert, kunt u een eenheidconversie instellen voor het productmodel.</span><span class="sxs-lookup"><span data-stu-id="f348d-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="f348d-128">Deze eenheidconversie geldt voor alle productvarianten zonder gedefinieerde eenheidconversie.</span><span class="sxs-lookup"><span data-stu-id="f348d-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="f348d-129">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f348d-129">Example</span></span>

<span data-ttu-id="f348d-130">Een productmodel, **T-Shirt**, heeft vier vrijgegeven productvarianten: Small, Medium, Large en Extra large.</span><span class="sxs-lookup"><span data-stu-id="f348d-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="f348d-131">De T-shirts zijn verpakt in dozen en er passen vijf T-shirts in een doos, met uitzondering van de T-shirts met de maat Extra large, waarvan er maar vier passen in een doos.</span><span class="sxs-lookup"><span data-stu-id="f348d-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="f348d-132">Open eerst de pagina **Eenheidsomrekening** via de pagina met vrijgegeven productgegevens voor **T-shirt**.</span><span class="sxs-lookup"><span data-stu-id="f348d-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="f348d-133">Stel op de pagina **Eenheidsomrekening** de eenheidconversie voor de productvariant Extra large in.</span><span class="sxs-lookup"><span data-stu-id="f348d-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="f348d-134">**Veld**</span><span class="sxs-lookup"><span data-stu-id="f348d-134">**Field**</span></span>             | <span data-ttu-id="f348d-135">**Instelling**</span><span class="sxs-lookup"><span data-stu-id="f348d-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="f348d-136">Conversie maken voor</span><span class="sxs-lookup"><span data-stu-id="f348d-136">Create conversion for</span></span> | <span data-ttu-id="f348d-137">Productvariant</span><span class="sxs-lookup"><span data-stu-id="f348d-137">Product variant</span></span>         |
| <span data-ttu-id="f348d-138">Productvariant</span><span class="sxs-lookup"><span data-stu-id="f348d-138">Product variant</span></span>       | <span data-ttu-id="f348d-139">T-Shirt : : Extra large : :</span><span class="sxs-lookup"><span data-stu-id="f348d-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="f348d-140">Van eenheid</span><span class="sxs-lookup"><span data-stu-id="f348d-140">From unit</span></span>             | <span data-ttu-id="f348d-141">Dozen</span><span class="sxs-lookup"><span data-stu-id="f348d-141">Boxes</span></span>                   |
| <span data-ttu-id="f348d-142">Factor</span><span class="sxs-lookup"><span data-stu-id="f348d-142">Factor</span></span>                | <span data-ttu-id="f348d-143">4</span><span class="sxs-lookup"><span data-stu-id="f348d-143">4</span></span>                       |
| <span data-ttu-id="f348d-144">Naar eenheid</span><span class="sxs-lookup"><span data-stu-id="f348d-144">To Unit</span></span>               | <span data-ttu-id="f348d-145">Stuks</span><span class="sxs-lookup"><span data-stu-id="f348d-145">Pieces</span></span>                  |

<span data-ttu-id="f348d-146">Voor de vrijgegeven productvarianten Small, Medium en Large geldt dezelfde eenheidconversie tussen de eenheden Dozen en Stuks, wat betekent dat u de eenheidconversie voor deze productvarianten in het productmodel kunt definiëren.</span><span class="sxs-lookup"><span data-stu-id="f348d-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="f348d-147">**Veld**</span><span class="sxs-lookup"><span data-stu-id="f348d-147">**Field**</span></span>             | <span data-ttu-id="f348d-148">**Instelling**</span><span class="sxs-lookup"><span data-stu-id="f348d-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f348d-149">Conversie maken voor</span><span class="sxs-lookup"><span data-stu-id="f348d-149">Create conversion for</span></span> | <span data-ttu-id="f348d-150">Artikel</span><span class="sxs-lookup"><span data-stu-id="f348d-150">Product</span></span>     |
| <span data-ttu-id="f348d-151">Artikel</span><span class="sxs-lookup"><span data-stu-id="f348d-151">Product</span></span>               | <span data-ttu-id="f348d-152">T-shirt</span><span class="sxs-lookup"><span data-stu-id="f348d-152">T-Shirt</span></span>     |
| <span data-ttu-id="f348d-153">Van eenheid</span><span class="sxs-lookup"><span data-stu-id="f348d-153">From unit</span></span>             | <span data-ttu-id="f348d-154">Dozen</span><span class="sxs-lookup"><span data-stu-id="f348d-154">Boxes</span></span>       |
| <span data-ttu-id="f348d-155">Factor</span><span class="sxs-lookup"><span data-stu-id="f348d-155">Factor</span></span>                | <span data-ttu-id="f348d-156">5</span><span class="sxs-lookup"><span data-stu-id="f348d-156">5</span></span>           |
| <span data-ttu-id="f348d-157">Naar eenheid</span><span class="sxs-lookup"><span data-stu-id="f348d-157">To Unit</span></span>               | <span data-ttu-id="f348d-158">Stuks</span><span class="sxs-lookup"><span data-stu-id="f348d-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="f348d-159">De eenheidconversies bijwerken met Excel</span><span class="sxs-lookup"><span data-stu-id="f348d-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="f348d-160">Als een product veel productvarianten met verschillende eenheidsconversies heeft, is het verstandig om de eenheidsconversies van de pagina **Eenheidsconversie** te exporteren naar een Excel-werkblad, de conversies bij te werken en deze vervolgens weer te publiceren naar Supply Chain Mangement.</span><span class="sxs-lookup"><span data-stu-id="f348d-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="f348d-161">De optie voor het exporteren naar Excel en het publiceren van de bewerkingen naar Supply Chain Mangement. kan worden ingeschakeld via het menu-item **Openen in Microsoft Office** in het actievenster op de pagina **Eenheidsconversie**.</span><span class="sxs-lookup"><span data-stu-id="f348d-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
