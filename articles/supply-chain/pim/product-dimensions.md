---
title: Productdimensies
description: 'Er zijn vier productdimensies: stijl, configuratie, grootte en kleur. U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe. De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.'
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb9d47bf6f081dbcc9590bddd4516cf7385ec23
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563569"
---
# <a name="product-dimensions"></a><span data-ttu-id="48cad-105">Productdimensies</span><span class="sxs-lookup"><span data-stu-id="48cad-105">Product dimensions</span></span>

[!include [banner](../includes/banner.md)]

[!include [Retail name](../includes/retail-name.md)]

<span data-ttu-id="48cad-106">Er zijn vier productdimensies: stijl, configuratie, grootte en kleur.</span><span class="sxs-lookup"><span data-stu-id="48cad-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="48cad-107">U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe.</span><span class="sxs-lookup"><span data-stu-id="48cad-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="48cad-108">De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="48cad-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="48cad-109">Productdimensies zijn kenmerkend als ze dienen ter identificatie van de variant van een product.</span><span class="sxs-lookup"><span data-stu-id="48cad-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="48cad-110">U kunt combinaties van productdimensies gebruiken om varianten van het product te definiëren.</span><span class="sxs-lookup"><span data-stu-id="48cad-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="48cad-111">Als u een productvariant wilt maken, moet u ten minste één productdimensie definiëren voor een productmodel.</span><span class="sxs-lookup"><span data-stu-id="48cad-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="48cad-112">Productvarianten</span><span class="sxs-lookup"><span data-stu-id="48cad-112">Product variants</span></span>
----------------

<span data-ttu-id="48cad-113">Productvarianten worden ook artikelen genoemd.</span><span class="sxs-lookup"><span data-stu-id="48cad-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="48cad-114">Een artikel is een tastbaar product, dat niet hetzelfde is als een service.</span><span class="sxs-lookup"><span data-stu-id="48cad-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="48cad-115">Het is echter ook mogelijk om een productmodel te definiëren van het type Service.</span><span class="sxs-lookup"><span data-stu-id="48cad-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="48cad-116">Met behulp van het type Service kunt u productvarianten specificeren die services omvatten.</span><span class="sxs-lookup"><span data-stu-id="48cad-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="48cad-117">U kunt bijvoorbeeld een productmodel opgeven voor advieswerk en productvarianten voor werk dat is uitgevoerd door senior en junior consultants.</span><span class="sxs-lookup"><span data-stu-id="48cad-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="48cad-118">Productdimensies</span><span class="sxs-lookup"><span data-stu-id="48cad-118">Product dimensions</span></span>
<span data-ttu-id="48cad-119">De volgende vier productdimensies zijn beschikbaar: stijl, configuratie, grootte en kleur.</span><span class="sxs-lookup"><span data-stu-id="48cad-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="48cad-120">Een productvarianten kan worden gegenereerd op basis van de waarden van de productdimensies.</span><span class="sxs-lookup"><span data-stu-id="48cad-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="48cad-121">Waarden voor productdimensies, zoals Grootte, Kleur en Stijl kunnen worden gemaakt op de pagina's **Maat**, **Kleur** en **Stijl**, die toegankelijk zijn vanaf de volgende locaties: **Productgegevensbeheer** &gt; **Instellingen** &gt; **Dimensie- en variantgroepen** &gt; **Maten/kleuren/stijlen**.</span><span class="sxs-lookup"><span data-stu-id="48cad-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="48cad-122">Waarden voor productdimensies voor de Configuratiedimensie worden doorgaans gemaakt met de functie voor productconfiguratie of op dimensies gebaseerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="48cad-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="48cad-123">Productdimensies kunnen tevens worden gemaakt en beheerd op de pagina **Productdimensies**, die kan worden geopend vanaf de volgende locaties:</span><span class="sxs-lookup"><span data-stu-id="48cad-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="48cad-124">Klik op **Productgegevensbeheer** &gt; **Producten** &gt; **Productmodellen**.</span><span class="sxs-lookup"><span data-stu-id="48cad-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="48cad-125">Klik in het **Actievenster** op **Productdimensies**.</span><span class="sxs-lookup"><span data-stu-id="48cad-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="48cad-126">Klik op **Productgegevensbeheer** &gt; **Producten** &gt; **Alle producten en productmodellen**.</span><span class="sxs-lookup"><span data-stu-id="48cad-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="48cad-127">Een productmodel selecteren.</span><span class="sxs-lookup"><span data-stu-id="48cad-127">Select a product master.</span></span> <span data-ttu-id="48cad-128">Klik in het **Actievenster** op **Productdimensies**.</span><span class="sxs-lookup"><span data-stu-id="48cad-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="48cad-129">Klik op **Productgegevensbeheer** &gt; **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="48cad-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="48cad-130">Een productmodel selecteren.</span><span class="sxs-lookup"><span data-stu-id="48cad-130">Select a product master.</span></span> <span data-ttu-id="48cad-131">Klik in het **Actievenster** op **Product**.</span><span class="sxs-lookup"><span data-stu-id="48cad-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="48cad-132">Klik in de groep **Productmodel** op **Productdimensies**.</span><span class="sxs-lookup"><span data-stu-id="48cad-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="48cad-133">Het aantal varianten dat u voor een artikel maakt, wordt beperkt door het aantal mogelijke productdimensiecombinaties.</span><span class="sxs-lookup"><span data-stu-id="48cad-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>

| <span data-ttu-id="48cad-134">**Tip**</span><span class="sxs-lookup"><span data-stu-id="48cad-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48cad-135">Wanneer u een product bijvoorbeeld op een orderregel gebruikt, selecteert u de productdimensies om de productvariant waarmee u wilt werken, te identificeren.</span><span class="sxs-lookup"><span data-stu-id="48cad-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="48cad-136">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="48cad-136">Example</span></span>
<span data-ttu-id="48cad-137">Een bedrijf verkoopt spijkerbroeken.</span><span class="sxs-lookup"><span data-stu-id="48cad-137">A company sells denim jeans.</span></span> <span data-ttu-id="48cad-138">Het artikel Spijkerbroeken gebruikt de productdimensies Kleur en Maat.</span><span class="sxs-lookup"><span data-stu-id="48cad-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="48cad-139">De spijkerbroeken worden in drie verschillende kleuren en in zes verschillende maten verkocht.</span><span class="sxs-lookup"><span data-stu-id="48cad-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="48cad-140">Kleuren: Blauw, Zwart, Bruin Maten: XS, S, M, L, XL, XXL Niet alle maten zijn beschikbaar in alle drie kleuren.</span><span class="sxs-lookup"><span data-stu-id="48cad-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="48cad-141">Als alle combinaties beschikbaar zijn, zijn er 18 typen spijkerbroeken.</span><span class="sxs-lookup"><span data-stu-id="48cad-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="48cad-142">In dit voorbeeld worden alleen de volgende negen combinaties van productvarianten geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="48cad-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="48cad-143">Kleur</span><span class="sxs-lookup"><span data-stu-id="48cad-143">Color</span></span> | <span data-ttu-id="48cad-144">Grootte</span><span class="sxs-lookup"><span data-stu-id="48cad-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="48cad-145">Blauw</span><span class="sxs-lookup"><span data-stu-id="48cad-145">Blue</span></span>  | <span data-ttu-id="48cad-146">XS</span><span class="sxs-lookup"><span data-stu-id="48cad-146">XS</span></span>   |
| <span data-ttu-id="48cad-147">Blauw</span><span class="sxs-lookup"><span data-stu-id="48cad-147">Blue</span></span>  | <span data-ttu-id="48cad-148">Z</span><span class="sxs-lookup"><span data-stu-id="48cad-148">S</span></span>    |
| <span data-ttu-id="48cad-149">Blauw</span><span class="sxs-lookup"><span data-stu-id="48cad-149">Blue</span></span>  | <span data-ttu-id="48cad-150">M</span><span class="sxs-lookup"><span data-stu-id="48cad-150">M</span></span>    |
| <span data-ttu-id="48cad-151">Zwart</span><span class="sxs-lookup"><span data-stu-id="48cad-151">Black</span></span> | <span data-ttu-id="48cad-152">M</span><span class="sxs-lookup"><span data-stu-id="48cad-152">M</span></span>    |
| <span data-ttu-id="48cad-153">Zwart</span><span class="sxs-lookup"><span data-stu-id="48cad-153">Black</span></span> | <span data-ttu-id="48cad-154">L</span><span class="sxs-lookup"><span data-stu-id="48cad-154">L</span></span>    |
| <span data-ttu-id="48cad-155">Zwart</span><span class="sxs-lookup"><span data-stu-id="48cad-155">Black</span></span> | <span data-ttu-id="48cad-156">XL</span><span class="sxs-lookup"><span data-stu-id="48cad-156">XL</span></span>   |
| <span data-ttu-id="48cad-157">Bruin</span><span class="sxs-lookup"><span data-stu-id="48cad-157">Brown</span></span> | <span data-ttu-id="48cad-158">L</span><span class="sxs-lookup"><span data-stu-id="48cad-158">L</span></span>    |
| <span data-ttu-id="48cad-159">Bruin</span><span class="sxs-lookup"><span data-stu-id="48cad-159">Brown</span></span> | <span data-ttu-id="48cad-160">XL</span><span class="sxs-lookup"><span data-stu-id="48cad-160">XL</span></span>   |
| <span data-ttu-id="48cad-161">Bruin</span><span class="sxs-lookup"><span data-stu-id="48cad-161">Brown</span></span> | <span data-ttu-id="48cad-162">XXL</span><span class="sxs-lookup"><span data-stu-id="48cad-162">XXL</span></span>  |





