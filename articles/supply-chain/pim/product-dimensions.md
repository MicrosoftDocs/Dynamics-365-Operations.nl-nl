---
title: Productdimensies
description: 'Er zijn vier productdimensies: stijl, configuratie, grootte en kleur. U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe. De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.'
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 9cb4bded4b8d841c6d164e6b8ded2cb3fb4d0978
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---

# <a name="product-dimensions"></a><span data-ttu-id="3129f-105">Productdimensies</span><span class="sxs-lookup"><span data-stu-id="3129f-105">Product dimensions</span></span>

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


<span data-ttu-id="3129f-106">Er zijn vier productdimensies: stijl, configuratie, grootte en kleur.</span><span class="sxs-lookup"><span data-stu-id="3129f-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="3129f-107">U combineert productdimensies in dimensiegroepen en wijst dimensiegroepen aan productmodellen toe.</span><span class="sxs-lookup"><span data-stu-id="3129f-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="3129f-108">De combinaties van productdimensies bepalen hoe productvarianten worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="3129f-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="3129f-109">Productdimensies zijn kenmerkend als ze dienen ter identificatie van de variant van een product.</span><span class="sxs-lookup"><span data-stu-id="3129f-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="3129f-110">U kunt combinaties van productdimensies gebruiken om varianten van het product te definiëren.</span><span class="sxs-lookup"><span data-stu-id="3129f-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="3129f-111">Als u een productvariant wilt maken, moet u ten minste één productdimensie definiëren voor een productmodel.</span><span class="sxs-lookup"><span data-stu-id="3129f-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="3129f-112">Productvarianten</span><span class="sxs-lookup"><span data-stu-id="3129f-112">Product variants</span></span>
----------------

<span data-ttu-id="3129f-113">Productvarianten worden ook artikelen genoemd.</span><span class="sxs-lookup"><span data-stu-id="3129f-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="3129f-114">Een artikel is een tastbaar product, dat niet hetzelfde is als een service.</span><span class="sxs-lookup"><span data-stu-id="3129f-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="3129f-115">Het is echter ook mogelijk om een productmodel te definiëren van het type Service.</span><span class="sxs-lookup"><span data-stu-id="3129f-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="3129f-116">Met behulp van het type Service kunt u productvarianten specificeren die services omvatten.</span><span class="sxs-lookup"><span data-stu-id="3129f-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="3129f-117">U kunt bijvoorbeeld een productmodel opgeven voor advieswerk en productvarianten voor werk dat is uitgevoerd door senior en junior consultants.</span><span class="sxs-lookup"><span data-stu-id="3129f-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="3129f-118">Productdimensies</span><span class="sxs-lookup"><span data-stu-id="3129f-118">Product dimensions</span></span>
<span data-ttu-id="3129f-119">De volgende vier productdimensies zijn beschikbaar: stijl, configuratie, grootte en kleur.</span><span class="sxs-lookup"><span data-stu-id="3129f-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="3129f-120">Een productvarianten kan worden gegenereerd op basis van de waarden van de productdimensies.</span><span class="sxs-lookup"><span data-stu-id="3129f-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="3129f-121">Waarden voor productdimensies, zoals Grootte, Kleur en Stijl kunnen worden gemaakt op de pagina's **Maat**, **Kleur** en **Stijl**, die toegankelijk zijn vanaf de volgende locaties: **Productgegevensbeheer** &gt; **Instellingen** &gt; **Dimensie- en variantgroepen** &gt; **Maten/kleuren/stijlen**.</span><span class="sxs-lookup"><span data-stu-id="3129f-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="3129f-122">Waarden voor productdimensies voor de Configuratiedimensie worden doorgaans gemaakt met de functie voor productconfiguratie of op dimensies gebaseerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="3129f-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="3129f-123">Productdimensies kunnen tevens worden gemaakt en beheerd op de pagina **Productdimensies**, die kan worden geopend vanaf de volgende locaties:</span><span class="sxs-lookup"><span data-stu-id="3129f-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="3129f-124">Klik op **Productgegevensbeheer** &gt; **Producten** &gt; **Productmodellen**.</span><span class="sxs-lookup"><span data-stu-id="3129f-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="3129f-125">Klik in het **Actievenster** op **Productdimensies**.</span><span class="sxs-lookup"><span data-stu-id="3129f-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="3129f-126">Klik op **Productgegevensbeheer** &gt; **Producten** &gt; **Alle producten en productmodellen**.</span><span class="sxs-lookup"><span data-stu-id="3129f-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="3129f-127">Een productmodel selecteren.</span><span class="sxs-lookup"><span data-stu-id="3129f-127">Select a product master.</span></span> <span data-ttu-id="3129f-128">Klik in het **Actievenster** op **Productdimensies**.</span><span class="sxs-lookup"><span data-stu-id="3129f-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="3129f-129">Klik op **Productgegevensbeheer** &gt; **Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="3129f-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="3129f-130">Een productmodel selecteren.</span><span class="sxs-lookup"><span data-stu-id="3129f-130">Select a product master.</span></span> <span data-ttu-id="3129f-131">Klik in het **Actievenster** op **Product**.</span><span class="sxs-lookup"><span data-stu-id="3129f-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="3129f-132">Klik in de groep **Productmodel** op **Productdimensies**.</span><span class="sxs-lookup"><span data-stu-id="3129f-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="3129f-133">Het aantal varianten dat u voor een artikel maakt, wordt beperkt door het aantal mogelijke productdimensiecombinaties.</span><span class="sxs-lookup"><span data-stu-id="3129f-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>
| <span data-ttu-id="3129f-134">**Tip**</span><span class="sxs-lookup"><span data-stu-id="3129f-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3129f-135">Wanneer u een product bijvoorbeeld op een orderregel gebruikt, selecteert u de productdimensies om de productvariant waarmee u wilt werken, te identificeren.</span><span class="sxs-lookup"><span data-stu-id="3129f-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="3129f-136">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="3129f-136">Example</span></span>
<span data-ttu-id="3129f-137">Een bedrijf verkoopt spijkerbroeken.</span><span class="sxs-lookup"><span data-stu-id="3129f-137">A company sells denim jeans.</span></span> <span data-ttu-id="3129f-138">Het artikel Spijkerbroeken gebruikt de productdimensies Kleur en Maat.</span><span class="sxs-lookup"><span data-stu-id="3129f-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="3129f-139">De spijkerbroeken worden in drie verschillende kleuren en in zes verschillende maten verkocht.</span><span class="sxs-lookup"><span data-stu-id="3129f-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="3129f-140">Kleuren: Blauw, Zwart, Bruin Maten: XS, S, M, L, XL, XXL Niet alle maten zijn beschikbaar in alle drie kleuren.</span><span class="sxs-lookup"><span data-stu-id="3129f-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="3129f-141">Als alle combinaties beschikbaar zijn, zijn er 18 typen spijkerbroeken.</span><span class="sxs-lookup"><span data-stu-id="3129f-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="3129f-142">In dit voorbeeld worden alleen de volgende negen combinaties van productvarianten geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="3129f-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="3129f-143">Kleur</span><span class="sxs-lookup"><span data-stu-id="3129f-143">Color</span></span> | <span data-ttu-id="3129f-144">Grootte</span><span class="sxs-lookup"><span data-stu-id="3129f-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="3129f-145">Blauw</span><span class="sxs-lookup"><span data-stu-id="3129f-145">Blue</span></span>  | <span data-ttu-id="3129f-146">XS</span><span class="sxs-lookup"><span data-stu-id="3129f-146">XS</span></span>   |
| <span data-ttu-id="3129f-147">Blauw</span><span class="sxs-lookup"><span data-stu-id="3129f-147">Blue</span></span>  | <span data-ttu-id="3129f-148">Z</span><span class="sxs-lookup"><span data-stu-id="3129f-148">S</span></span>    |
| <span data-ttu-id="3129f-149">Blauw</span><span class="sxs-lookup"><span data-stu-id="3129f-149">Blue</span></span>  | <span data-ttu-id="3129f-150">M</span><span class="sxs-lookup"><span data-stu-id="3129f-150">M</span></span>    |
| <span data-ttu-id="3129f-151">Zwart</span><span class="sxs-lookup"><span data-stu-id="3129f-151">Black</span></span> | <span data-ttu-id="3129f-152">M</span><span class="sxs-lookup"><span data-stu-id="3129f-152">M</span></span>    |
| <span data-ttu-id="3129f-153">Zwart</span><span class="sxs-lookup"><span data-stu-id="3129f-153">Black</span></span> | <span data-ttu-id="3129f-154">L</span><span class="sxs-lookup"><span data-stu-id="3129f-154">L</span></span>    |
| <span data-ttu-id="3129f-155">Zwart</span><span class="sxs-lookup"><span data-stu-id="3129f-155">Black</span></span> | <span data-ttu-id="3129f-156">XL</span><span class="sxs-lookup"><span data-stu-id="3129f-156">XL</span></span>   |
| <span data-ttu-id="3129f-157">Bruin</span><span class="sxs-lookup"><span data-stu-id="3129f-157">Brown</span></span> | <span data-ttu-id="3129f-158">L</span><span class="sxs-lookup"><span data-stu-id="3129f-158">L</span></span>    |
| <span data-ttu-id="3129f-159">Bruin</span><span class="sxs-lookup"><span data-stu-id="3129f-159">Brown</span></span> | <span data-ttu-id="3129f-160">XL</span><span class="sxs-lookup"><span data-stu-id="3129f-160">XL</span></span>   |
| <span data-ttu-id="3129f-161">Bruin</span><span class="sxs-lookup"><span data-stu-id="3129f-161">Brown</span></span> | <span data-ttu-id="3129f-162">XXL</span><span class="sxs-lookup"><span data-stu-id="3129f-162">XXL</span></span>  |






