---
title: Conversie van maateenheid per productvariant
description: In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 196b68db02867f8d864be8bcc593aa01f554f7c3
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249443"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="1d638-103">Conversie van maateenheid per productvariant</span><span class="sxs-lookup"><span data-stu-id="1d638-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="1d638-104">In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten.</span><span class="sxs-lookup"><span data-stu-id="1d638-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="1d638-105">Het bevat een voorbeeld van de instellingen.</span><span class="sxs-lookup"><span data-stu-id="1d638-105">It includes an example of the setup.</span></span>

<span data-ttu-id="1d638-106">Met deze functie kunnen bedrijven verschillende eenheidconversies tussen de varianten van hetzelfde product definiëren.</span><span class="sxs-lookup"><span data-stu-id="1d638-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="1d638-107">Het volgende voorbeeld wordt gebruikt in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="1d638-107">The following example is used in this topic.</span></span> <span data-ttu-id="1d638-108">Een bedrijf verkoopt T-shirts in de maten Small, Medium, Large en Extra large.</span><span class="sxs-lookup"><span data-stu-id="1d638-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="1d638-109">Het T-shirt is gedefinieerd als een product en de verschillende maten zijn gedefinieerd als varianten van het product.</span><span class="sxs-lookup"><span data-stu-id="1d638-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="1d638-110">De T-shirts zijn verpakt in dozen en er passen vijf T-shirts in een doos, met uitzondering van de T-shirts met de maat Extra large, waarvan er maar vier passen in een doos.</span><span class="sxs-lookup"><span data-stu-id="1d638-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="1d638-111">Het bedrijf wil de verschillende varianten van de T-shirts in de eenheid **Stuks** bijhouden, maar verkoopt de T-shirts in de eenheid **Dozen**.</span><span class="sxs-lookup"><span data-stu-id="1d638-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="1d638-112">De conversie tussen de voorraadeenheid en de verkoopeenheid is 1 doos = 5 stuks, met uitzondering van de variant Extra large waarvoor de conversie 1 doos = 4 stuks geldt.</span><span class="sxs-lookup"><span data-stu-id="1d638-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="1d638-113">Instellen</span><span class="sxs-lookup"><span data-stu-id="1d638-113">Setup</span></span>

<span data-ttu-id="1d638-114">U kunt de parameters configureren voor het gebruik van de functie voor producten die zijn ingeschakeld voor **Alle processen** of alleen voor het product dat is ingeschakeld voor **Magazijnprocessen**. Gebruik hiervoor de optie **Maateenheidconversies inschakelen** op de pagina **Productgegevensparameters instellen**.</span><span class="sxs-lookup"><span data-stu-id="1d638-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="1d638-115">Een product voor eenheidconversie per variant instellen</span><span class="sxs-lookup"><span data-stu-id="1d638-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="1d638-116">Productvarianten kunnen alleen worden gemaakt voor producten van het **productsubtype** **Productmodel**.</span><span class="sxs-lookup"><span data-stu-id="1d638-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="1d638-117">Zie [Een productmodel maken](tasks/create-product-master.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1d638-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="1d638-118">De functie is niet ingeschakeld voor producten die zijn ingesteld voor processen van het type Variabel gewicht.</span><span class="sxs-lookup"><span data-stu-id="1d638-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="1d638-119">Schakel tijdens het maken van een productmodel maateenheidconversie in met de optie **Maateenheidconversies inschakelen** op de pagina **Productdetails**.</span><span class="sxs-lookup"><span data-stu-id="1d638-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="1d638-120">Wanneer het productmodel met vrijgegeven productvarianten is gemaakt, kunnen eenheidconversies per variant worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="1d638-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="1d638-121">U kunt het menu-item voor het openen van de pagina voor eenheidconversie in de context van een product of productvariant vinden op de volgende pagina's.</span><span class="sxs-lookup"><span data-stu-id="1d638-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="1d638-122">De pagina **Productgegevens**</span><span class="sxs-lookup"><span data-stu-id="1d638-122">**Product details** page</span></span>
-   <span data-ttu-id="1d638-123">De pagina **Details van vrijgegeven producten**</span><span class="sxs-lookup"><span data-stu-id="1d638-123">**Released products details** page</span></span>
-   <span data-ttu-id="1d638-124">De pagina **Vrijgegeven productvarianten**</span><span class="sxs-lookup"><span data-stu-id="1d638-124">**Released product variants** page</span></span>

<span data-ttu-id="1d638-125">Wanneer u de pagina **Eenheidsomrekening** in de context van een productmodel of vrijgegeven productvariant opent, kunt u opgeven of u de eenheidconversie voor het product of een productvariant wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="1d638-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="1d638-126">U doet dit door **Productvariant** of **Product** te selecteren in het veld **Conversie maken voor**.</span><span class="sxs-lookup"><span data-stu-id="1d638-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="1d638-127">Productvariant</span><span class="sxs-lookup"><span data-stu-id="1d638-127">Product variant</span></span>

<span data-ttu-id="1d638-128">Als u **Productvariant** selecteert, kunt u in het veld **Productvariant** opgeven voor welke variant u de eenheidconversie wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="1d638-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="1d638-129">Artikel</span><span class="sxs-lookup"><span data-stu-id="1d638-129">Product</span></span>

<span data-ttu-id="1d638-130">Als u **Product** selecteert, kunt u een eenheidconversie instellen voor het productmodel.</span><span class="sxs-lookup"><span data-stu-id="1d638-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="1d638-131">Deze eenheidconversie geldt voor alle productvarianten zonder gedefinieerde eenheidconversie.</span><span class="sxs-lookup"><span data-stu-id="1d638-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="1d638-132">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="1d638-132">Example</span></span>

<span data-ttu-id="1d638-133">Een productmodel, **T-Shirt**, heeft vier vrijgegeven productvarianten: Small, Medium, Large en Extra large.</span><span class="sxs-lookup"><span data-stu-id="1d638-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="1d638-134">De T-shirts zijn verpakt in dozen en er passen vijf T-shirts in een doos, met uitzondering van de T-shirts met de maat Extra large, waarvan er maar vier passen in een doos.</span><span class="sxs-lookup"><span data-stu-id="1d638-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="1d638-135">Open eerst de pagina **Eenheidsomrekening** via de pagina met vrijgegeven productgegevens voor **T-shirt**.</span><span class="sxs-lookup"><span data-stu-id="1d638-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="1d638-136">Stel op de pagina **Eenheidsomrekening** de eenheidconversie voor de productvariant Extra large in.</span><span class="sxs-lookup"><span data-stu-id="1d638-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="1d638-137">**Veld**</span><span class="sxs-lookup"><span data-stu-id="1d638-137">**Field**</span></span>             | <span data-ttu-id="1d638-138">**Instelling**</span><span class="sxs-lookup"><span data-stu-id="1d638-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="1d638-139">Conversie maken voor</span><span class="sxs-lookup"><span data-stu-id="1d638-139">Create conversion for</span></span> | <span data-ttu-id="1d638-140">Productvariant</span><span class="sxs-lookup"><span data-stu-id="1d638-140">Product variant</span></span>         |
| <span data-ttu-id="1d638-141">Productvariant</span><span class="sxs-lookup"><span data-stu-id="1d638-141">Product variant</span></span>       | <span data-ttu-id="1d638-142">T-Shirt : : Extra large : :</span><span class="sxs-lookup"><span data-stu-id="1d638-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="1d638-143">Van eenheid</span><span class="sxs-lookup"><span data-stu-id="1d638-143">From unit</span></span>             | <span data-ttu-id="1d638-144">Dozen</span><span class="sxs-lookup"><span data-stu-id="1d638-144">Boxes</span></span>                   |
| <span data-ttu-id="1d638-145">Factor</span><span class="sxs-lookup"><span data-stu-id="1d638-145">Factor</span></span>                | <span data-ttu-id="1d638-146">4</span><span class="sxs-lookup"><span data-stu-id="1d638-146">4</span></span>                       |
| <span data-ttu-id="1d638-147">Naar eenheid</span><span class="sxs-lookup"><span data-stu-id="1d638-147">To Unit</span></span>               | <span data-ttu-id="1d638-148">Stuks</span><span class="sxs-lookup"><span data-stu-id="1d638-148">Pieces</span></span>                  |

<span data-ttu-id="1d638-149">Voor de vrijgegeven productvarianten Small, Medium en Large geldt dezelfde eenheidconversie tussen de eenheden Dozen en Stuks, wat betekent dat u de eenheidconversie voor deze productvarianten in het productmodel kunt definiëren.</span><span class="sxs-lookup"><span data-stu-id="1d638-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="1d638-150">**Veld**</span><span class="sxs-lookup"><span data-stu-id="1d638-150">**Field**</span></span>             | <span data-ttu-id="1d638-151">**Instelling**</span><span class="sxs-lookup"><span data-stu-id="1d638-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="1d638-152">Conversie maken voor</span><span class="sxs-lookup"><span data-stu-id="1d638-152">Create conversion for</span></span> | <span data-ttu-id="1d638-153">Artikel</span><span class="sxs-lookup"><span data-stu-id="1d638-153">Product</span></span>     |
| <span data-ttu-id="1d638-154">Artikel</span><span class="sxs-lookup"><span data-stu-id="1d638-154">Product</span></span>               | <span data-ttu-id="1d638-155">T-shirt</span><span class="sxs-lookup"><span data-stu-id="1d638-155">T-Shirt</span></span>     |
| <span data-ttu-id="1d638-156">Van eenheid</span><span class="sxs-lookup"><span data-stu-id="1d638-156">From unit</span></span>             | <span data-ttu-id="1d638-157">Dozen</span><span class="sxs-lookup"><span data-stu-id="1d638-157">Boxes</span></span>       |
| <span data-ttu-id="1d638-158">Factor</span><span class="sxs-lookup"><span data-stu-id="1d638-158">Factor</span></span>                | <span data-ttu-id="1d638-159">5</span><span class="sxs-lookup"><span data-stu-id="1d638-159">5</span></span>           |
| <span data-ttu-id="1d638-160">Naar eenheid</span><span class="sxs-lookup"><span data-stu-id="1d638-160">To Unit</span></span>               | <span data-ttu-id="1d638-161">Stuks</span><span class="sxs-lookup"><span data-stu-id="1d638-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="1d638-162">De eenheidconversies bijwerken met Excel</span><span class="sxs-lookup"><span data-stu-id="1d638-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="1d638-163">Als een product veel productvarianten met verschillende eenheidsconversies heeft, is het verstandig om de eenheidsconversies van de pagina **Eenheidsconversie** te exporteren naar een Excel-werkblad, de conversies bij te werken en deze vervolgens weer te publiceren naar Supply Chain Mangement.</span><span class="sxs-lookup"><span data-stu-id="1d638-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="1d638-164">De optie voor het exporteren naar Excel en het publiceren van de bewerkingen naar Supply Chain Mangement. kan worden ingeschakeld via het menu-item **Openen in Microsoft Office** in het actievenster op de pagina **Eenheidsconversie**.</span><span class="sxs-lookup"><span data-stu-id="1d638-164">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
