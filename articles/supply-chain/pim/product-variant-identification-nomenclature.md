---
title: Nomenclatuur van productvariantnummers en -namen
description: In dit onderwerp wordt beschreven hoe u een productnummernomenclatuur instelt om de vaste indeling [productmodelnummer - configuratie - maat - kleur - stijl] te vervangen.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f84b6982af8b81ff83086d163a77e1c2f58ca478
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="5cc88-103">Nomenclatuur van productvariantnummers en -namen</span><span class="sxs-lookup"><span data-stu-id="5cc88-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cc88-104">In dit onderwerp wordt beschreven hoe u een productnummernomenclatuur instelt om de vaste indeling [productmodelnummer - configuratie - maat - kleur - stijl] te vervangen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="5cc88-105">De nieuwe nomenclatuur heeft een beoogde indeling die het productmodelnummer, de actieve productdimensies en tekstscheidingstekens van uw keuze bevat.</span><span class="sxs-lookup"><span data-stu-id="5cc88-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="5cc88-106">U kunt ook een nomenclatuur maken voor productnamen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="5cc88-107">Ten slotte kunt u een nomenclatuur maken om configuraties te identificeren die worden gemaakt door de op beperkingen gebaseerde productconfigurator.</span><span class="sxs-lookup"><span data-stu-id="5cc88-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="5cc88-108">Deze nomenclaturen kunnen kenmerken van uw keuze bevatten.</span><span class="sxs-lookup"><span data-stu-id="5cc88-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="5cc88-109">Met de nieuwe nomenclaturen voor productvariantnummers en productvariantnamen kunt u segmenten in de id's opnemen voor productvarianten.</span><span class="sxs-lookup"><span data-stu-id="5cc88-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="5cc88-110">Deze segmenten kunnen productmodelnummer en -naam, productdimensie-id's en -namen, nummerreeksen, tekstconstanten en kenmerken omvatten.</span><span class="sxs-lookup"><span data-stu-id="5cc88-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="5cc88-111">Met deze functionaliteit kunt u snel een specifieke productvariant vinden wanneer u een verkooporder of een inkooporder maakt.</span><span class="sxs-lookup"><span data-stu-id="5cc88-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="5cc88-112">U maakt nomenclaturen voor zowel productvariantnummers als productvariantnamen met behulp van de pagina **Productnomenclatuur**.</span><span class="sxs-lookup"><span data-stu-id="5cc88-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="5cc88-113">Als u deze pagina wilt openen, klikt u op **Productgegevensbeheer** &gt; **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="5cc88-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="5cc88-114">Nomenclatuur met vooraf gedefinieerde productvarianten</span><span class="sxs-lookup"><span data-stu-id="5cc88-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="5cc88-115">De productvarianten worden gegenereerd voor productmodellen volgens drie configuratietechnologieën:</span><span class="sxs-lookup"><span data-stu-id="5cc88-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="5cc88-116">Vooraf gedefinieerde varianten</span><span class="sxs-lookup"><span data-stu-id="5cc88-116">Predefined variants</span></span>
-   <span data-ttu-id="5cc88-117">Op basis van beperkingen</span><span class="sxs-lookup"><span data-stu-id="5cc88-117">Constraint-based</span></span>
-   <span data-ttu-id="5cc88-118">Op basis van dimensies</span><span class="sxs-lookup"><span data-stu-id="5cc88-118">Dimension-based</span></span>

<span data-ttu-id="5cc88-119">Elke productvariant heeft een nummer en een naam en in de nomenclatuur van de productvariant-id's kunt u de segmenten selecteren die in elk productvariantnummer of -naam worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="5cc88-120">U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:</span><span class="sxs-lookup"><span data-stu-id="5cc88-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="5cc88-121">Nummer van basismaster</span><span class="sxs-lookup"><span data-stu-id="5cc88-121">Product master number</span></span>
-   <span data-ttu-id="5cc88-122">Naam van productmodel</span><span class="sxs-lookup"><span data-stu-id="5cc88-122">Product master name</span></span>
-   <span data-ttu-id="5cc88-123">Nummerreekswaarde</span><span class="sxs-lookup"><span data-stu-id="5cc88-123">Number sequence value</span></span>
-   <span data-ttu-id="5cc88-124">Tekstconstante</span><span class="sxs-lookup"><span data-stu-id="5cc88-124">Text constant</span></span>
-   <span data-ttu-id="5cc88-125">Productdimensies</span><span class="sxs-lookup"><span data-stu-id="5cc88-125">Product dimensions</span></span>
    -   <span data-ttu-id="5cc88-126">Configuratie-id of -naam</span><span class="sxs-lookup"><span data-stu-id="5cc88-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="5cc88-127">Kleur-id of -naam</span><span class="sxs-lookup"><span data-stu-id="5cc88-127">Color ID or name</span></span>
    -   <span data-ttu-id="5cc88-128">Maat-id of -naam</span><span class="sxs-lookup"><span data-stu-id="5cc88-128">Size ID or name</span></span>
    -   <span data-ttu-id="5cc88-129">Stijl-id of -naam</span><span class="sxs-lookup"><span data-stu-id="5cc88-129">Style ID or name</span></span>

<span data-ttu-id="5cc88-130">Nadat een productvariant-id hebt gedefinieerd, kunt u deze koppelen aan een productdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="5cc88-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="5cc88-131">Aan alle productmodellen die verwijzen naar deze productdimensiegroep, worden vervolgens productvariantnummers toegewezen op basis van de nomenclatuur.</span><span class="sxs-lookup"><span data-stu-id="5cc88-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="5cc88-132">Nomenclaturen van productvariantnamen kunnen echter niet worden gekoppeld aan productdimensiegroepen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="5cc88-133">U kunt ook een nomenclatuur voor productvariant-id's direct aan een productmodel toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="5cc88-134">In dit geval worden aan de productvarianten die behoren tot het productmodel, productvariantnummers en -namen toegewezen volgens de nomenclaturen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="5cc88-135">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5cc88-135">Example</span></span>

<span data-ttu-id="5cc88-136">Een T-shirt (TS1234) wordt geproduceerd in drie maten (S, M, L), vier kleuren (rood, groen, blauw, geel) en twee stijlen (Polo, V).</span><span class="sxs-lookup"><span data-stu-id="5cc88-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="5cc88-137">Daarom zijn 24 productvarianten mogelijk (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="5cc88-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="5cc88-138">U maakt een productvariantnummernomenclatuur met de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="5cc88-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="5cc88-139">Nummer van basismaster</span><span class="sxs-lookup"><span data-stu-id="5cc88-139">Product master number</span></span>
2.  <span data-ttu-id="5cc88-140">Tekstconstante: "-"</span><span class="sxs-lookup"><span data-stu-id="5cc88-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="5cc88-141">Kleur</span><span class="sxs-lookup"><span data-stu-id="5cc88-141">Color</span></span>
4.  <span data-ttu-id="5cc88-142">Tekstconstante: "-"</span><span class="sxs-lookup"><span data-stu-id="5cc88-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="5cc88-143">Grootte</span><span class="sxs-lookup"><span data-stu-id="5cc88-143">Size</span></span>
6.  <span data-ttu-id="5cc88-144">Tekstconstante: "-"</span><span class="sxs-lookup"><span data-stu-id="5cc88-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="5cc88-145">Opmaakmodel</span><span class="sxs-lookup"><span data-stu-id="5cc88-145">Style</span></span>

<span data-ttu-id="5cc88-146">In dit geval is het productvariantnummer voor een rood, klein polo T-shirt TS1234-Rood-Klein-Polo.</span><span class="sxs-lookup"><span data-stu-id="5cc88-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="5cc88-147">Nomenclatuur met op beperkingen gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="5cc88-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="5cc88-148">Voor op beperkingen gebaseerde configuraties kunt u een specifieke nomenclatuur maken voor de configuratieproductdimensie.</span><span class="sxs-lookup"><span data-stu-id="5cc88-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="5cc88-149">U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:</span><span class="sxs-lookup"><span data-stu-id="5cc88-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="5cc88-150">Nummerreekswaarde</span><span class="sxs-lookup"><span data-stu-id="5cc88-150">Number sequence value</span></span>
-   <span data-ttu-id="5cc88-151">Tekstconstante</span><span class="sxs-lookup"><span data-stu-id="5cc88-151">Text constant</span></span>
-   <span data-ttu-id="5cc88-152">Kenmerkwaarde</span><span class="sxs-lookup"><span data-stu-id="5cc88-152">Attribute value</span></span>

<span data-ttu-id="5cc88-153">Elke component in een productconfiguratiemodel kan een eigen configuratienomenclatuur hebben.</span><span class="sxs-lookup"><span data-stu-id="5cc88-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="5cc88-154">Alleen kenmerken die bij de component horen, kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5cc88-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="5cc88-155">Kenmerken van subcomponenten of gebruikersvereisten kunnen niet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5cc88-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="5cc88-156">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5cc88-156">Example</span></span>

<span data-ttu-id="5cc88-157">Een productconfiguratiemodel heeft een hoofdcomponent met twee kenmerken:</span><span class="sxs-lookup"><span data-stu-id="5cc88-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="5cc88-158">Materiaal (plastic, hout, staal)</span><span class="sxs-lookup"><span data-stu-id="5cc88-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="5cc88-159">Lengte (10... 100)</span><span class="sxs-lookup"><span data-stu-id="5cc88-159">Length (10...100)</span></span>

<span data-ttu-id="5cc88-160">U maakt een configuratienomenclatuur met de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="5cc88-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="5cc88-161">Kenmerkwaarde: materiaal</span><span class="sxs-lookup"><span data-stu-id="5cc88-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="5cc88-162">Tekstconstante: "AAA"</span><span class="sxs-lookup"><span data-stu-id="5cc88-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="5cc88-163">Kenmerkwaarde: lengte</span><span class="sxs-lookup"><span data-stu-id="5cc88-163">Attribute value: Length</span></span>

<span data-ttu-id="5cc88-164">In dit geval is de configuratie-id voor houten materiaal met een lengte van 78 WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="5cc88-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="5cc88-165">Nomenclatuur met op dimensies gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="5cc88-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="5cc88-166">Voor op dimensies gebaseerde configuraties kunt u een specifieke nomenclatuur maken voor de configuratieproductdimensie.</span><span class="sxs-lookup"><span data-stu-id="5cc88-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="5cc88-167">U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:</span><span class="sxs-lookup"><span data-stu-id="5cc88-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="5cc88-168">Nummerreekswaarde</span><span class="sxs-lookup"><span data-stu-id="5cc88-168">Number sequence value</span></span>
-   <span data-ttu-id="5cc88-169">Tekstconstante</span><span class="sxs-lookup"><span data-stu-id="5cc88-169">Text constant</span></span>
-   <span data-ttu-id="5cc88-170">Configuratiegroepitem</span><span class="sxs-lookup"><span data-stu-id="5cc88-170">Configuration group item</span></span>

<span data-ttu-id="5cc88-171">U kunt een configuratienomenclatuur definiëren voor een stuklijst (BOM).</span><span class="sxs-lookup"><span data-stu-id="5cc88-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="5cc88-172">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5cc88-172">Example</span></span>

<span data-ttu-id="5cc88-173">Een stuklijst heeft vier stuklijstregels die worden onderverdeeld in twee configuratiegroepen:</span><span class="sxs-lookup"><span data-stu-id="5cc88-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="5cc88-174">Stuklijstregel: M0007, standaardbehuizing</span><span class="sxs-lookup"><span data-stu-id="5cc88-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="5cc88-175">Configuratiegroep: behuizing</span><span class="sxs-lookup"><span data-stu-id="5cc88-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="5cc88-176">Stuklijstregel: M0008, geavanceerde behuizing</span><span class="sxs-lookup"><span data-stu-id="5cc88-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="5cc88-177">Configuratiegroep: behuizing</span><span class="sxs-lookup"><span data-stu-id="5cc88-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="5cc88-178">Stuklijstregel: M0021, voorgrill van stof</span><span class="sxs-lookup"><span data-stu-id="5cc88-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="5cc88-179">Configuratiegroep: Voorgrill</span><span class="sxs-lookup"><span data-stu-id="5cc88-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="5cc88-180">Stuklijstregel: M0022, metalen voorgrill</span><span class="sxs-lookup"><span data-stu-id="5cc88-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="5cc88-181">Configuratiegroep: Voorgrill</span><span class="sxs-lookup"><span data-stu-id="5cc88-181">Configuration group: Front grill</span></span>

<span data-ttu-id="5cc88-182">U maakt een configuratienomenclatuur met de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="5cc88-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="5cc88-183">Configuratiegroep: behuizing</span><span class="sxs-lookup"><span data-stu-id="5cc88-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="5cc88-184">Tekstconstante: "&"</span><span class="sxs-lookup"><span data-stu-id="5cc88-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="5cc88-185">Configuratiegroep: Voorgrill</span><span class="sxs-lookup"><span data-stu-id="5cc88-185">Configuration group: Front grill</span></span>

<span data-ttu-id="5cc88-186">In dit geval is de configuratie-id voor een standaardbehuizing met een voorgrill van stof M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="5cc88-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="5cc88-187">Nomenclatuur voor een combinatie van productvarianten en configuraties</span><span class="sxs-lookup"><span data-stu-id="5cc88-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="5cc88-188">Als u de op beperkingen of dimensies gebaseerde configuratietechnologie gebruikt om productvarianten voor een productmodel te configureren, kunnen de productvariantnummers van de productvarianten de nomenclatuur bevatten van de configuratiedimensie.</span><span class="sxs-lookup"><span data-stu-id="5cc88-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="5cc88-189">Volg deze stappen om varianten te configureren.</span><span class="sxs-lookup"><span data-stu-id="5cc88-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="5cc88-190">Definieer op de pagina **Productnomenclatuur** een nomenclatuur van productvariantnummers die de configuratiedimensie omvat.</span><span class="sxs-lookup"><span data-stu-id="5cc88-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="5cc88-191">Wijs de nomenclatuur toe aan een productdimensiegroep die de configuratiedimensie heeft.</span><span class="sxs-lookup"><span data-stu-id="5cc88-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="5cc88-192">Definieer een configuratienomenclatuur voor de componenten of de stuklijsten die worden gebruikt voor het configureren van de productvarianten.</span><span class="sxs-lookup"><span data-stu-id="5cc88-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="5cc88-193">U kunt ook nomenclaturen maken voor de productvariantnamen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="5cc88-194">De productvariantnamen kunnen worden geconfigureerd voor het opnemen van de configuratie-ID of -naam.</span><span class="sxs-lookup"><span data-stu-id="5cc88-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="5cc88-195">Voorbeeld van op beperkingen gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="5cc88-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="5cc88-196">In dit voorbeeld gebruikt u een productvariantnummernomenclatuur die bestaat uit de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="5cc88-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="5cc88-197">Nummer van basismaster</span><span class="sxs-lookup"><span data-stu-id="5cc88-197">Product master number</span></span>
2.  <span data-ttu-id="5cc88-198">Tekstconstante "\_"</span><span class="sxs-lookup"><span data-stu-id="5cc88-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="5cc88-199">Configuratie</span><span class="sxs-lookup"><span data-stu-id="5cc88-199">Configuration</span></span>

<span data-ttu-id="5cc88-200">De configuratienomenclatuur bestaat uit de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="5cc88-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="5cc88-201">Kenmerkwaarde: materiaal</span><span class="sxs-lookup"><span data-stu-id="5cc88-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="5cc88-202">Tekstconstante: "AAA"</span><span class="sxs-lookup"><span data-stu-id="5cc88-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="5cc88-203">Kenmerkwaarde: lengte</span><span class="sxs-lookup"><span data-stu-id="5cc88-203">Attribute value: Length</span></span>

<span data-ttu-id="5cc88-204">U kunt de volgende waarden voor segmenten invoeren:</span><span class="sxs-lookup"><span data-stu-id="5cc88-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="5cc88-205">Productmodelnummer = **M0099**</span><span class="sxs-lookup"><span data-stu-id="5cc88-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="5cc88-206">Materiaal = **Plastic**</span><span class="sxs-lookup"><span data-stu-id="5cc88-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="5cc88-207">Lengte = **12**</span><span class="sxs-lookup"><span data-stu-id="5cc88-207">Length = **12**</span></span>

<span data-ttu-id="5cc88-208">In dit geval is het productvariantnummer M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="5cc88-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="5cc88-209">Voorbeeld van op dimensies gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="5cc88-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="5cc88-210">In dit voorbeeld gebruikt u een productvariantnummernomenclatuur die bestaat uit de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="5cc88-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="5cc88-211">Nummer van basismaster</span><span class="sxs-lookup"><span data-stu-id="5cc88-211">Product master number</span></span>
2.  <span data-ttu-id="5cc88-212">Tekstconstante "//"</span><span class="sxs-lookup"><span data-stu-id="5cc88-212">Text constant "//"</span></span>
3.  <span data-ttu-id="5cc88-213">Configuratie</span><span class="sxs-lookup"><span data-stu-id="5cc88-213">Configuration</span></span>

<span data-ttu-id="5cc88-214">De configuratienomenclatuur bestaat uit de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="5cc88-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="5cc88-215">Configuratiegroep: behuizing</span><span class="sxs-lookup"><span data-stu-id="5cc88-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="5cc88-216">Tekstconstante: "&"</span><span class="sxs-lookup"><span data-stu-id="5cc88-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="5cc88-217">Configuratiegroep: Voorgrill</span><span class="sxs-lookup"><span data-stu-id="5cc88-217">Configuration group: Front grill</span></span>

<span data-ttu-id="5cc88-218">U kunt de volgende waarden voor segmenten invoeren:</span><span class="sxs-lookup"><span data-stu-id="5cc88-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="5cc88-219">Productmodelnummer = **D0123**</span><span class="sxs-lookup"><span data-stu-id="5cc88-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="5cc88-220">Behuizing = **M0008**</span><span class="sxs-lookup"><span data-stu-id="5cc88-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="5cc88-221">Voorgrill = **M0022**</span><span class="sxs-lookup"><span data-stu-id="5cc88-221">Front grill = **M0022**</span></span>

<span data-ttu-id="5cc88-222">In dit geval is het productvariantnummer D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="5cc88-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="5cc88-223">Nummeringsconflicten</span><span class="sxs-lookup"><span data-stu-id="5cc88-223">Numbering conflicts</span></span>
<span data-ttu-id="5cc88-224">In sommige gevallen is het mogelijk dat een nomenclatuur voor productvariantnummers die u instelt, geen unieke productvariantnummers produceert.</span><span class="sxs-lookup"><span data-stu-id="5cc88-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="5cc88-225">De productvariantnummers zijn bijvoorbeeld niet uniek als één actieve productdimensie niet wordt opgenomen in de nomenclatuur van een productmodel dat de vooraf gedefinieerde variantconfiguratietechnologie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5cc88-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="5cc88-226">De manier waarop u conflicten verwerken, varieert afhankelijk van de configuratietechnologie.</span><span class="sxs-lookup"><span data-stu-id="5cc88-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="5cc88-227">Vooraf gedefinieerde varianten</span><span class="sxs-lookup"><span data-stu-id="5cc88-227">Predefined variants</span></span>

<span data-ttu-id="5cc88-228">Er treedt een fout op als u handmatig of automatisch probeert productvarianten te genereren, en meerdere productvarianten hetzelfde productvariantnummer krijgen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="5cc88-229">Als u dit scenario wilt voorkomen, moet u alle actieve productdimensies in de productdimensiegroep gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5cc88-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="5cc88-230">U kunt ook een nummerreeks opnemen om te garanderen dat de productvariantnummers uniek zijn.</span><span class="sxs-lookup"><span data-stu-id="5cc88-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="5cc88-231">Op beperkingen gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="5cc88-231">Constraint-based configurations</span></span>

<span data-ttu-id="5cc88-232">Afhankelijk van de nomenclatuur kan het systeem proberen een niet-uniek productvariantnummer aan een configuratie toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="5cc88-233">In dit geval gebruikt het systeem de nummerreeks voor de configuratiedimensie als productvariantnummer. Als dit gebeurt, ontvangt u een waarschuwing.</span><span class="sxs-lookup"><span data-stu-id="5cc88-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="5cc88-234">Als u dit scenario wilt voorkomen, moet u voldoende kenmerken opnemen in de nomenclatuur om unieke productvariantnummers te garanderen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="5cc88-235">U moet tevens zorgen dat de optie **Opnieuw gebruiken** is ingeschakeld voor het onderdeel.</span><span class="sxs-lookup"><span data-stu-id="5cc88-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="5cc88-236">Op dimensie gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="5cc88-236">Dimension-based configurations</span></span>

<span data-ttu-id="5cc88-237">Tijdens een stap van het configuratieproces suggereert het systeem een configuratiewaarde volgens de nomenclatuur.</span><span class="sxs-lookup"><span data-stu-id="5cc88-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="5cc88-238">In deze stap kunt u de configuratiewaarde handmatig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="5cc88-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="5cc88-239">Wanneer u de configuratie opslaat, controleert het systeem of de configuratiewaarde uniek is.</span><span class="sxs-lookup"><span data-stu-id="5cc88-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="5cc88-240">Als de waarde die u hebt ingevoerd niet uniek is, ontvangt u een foutbericht.</span><span class="sxs-lookup"><span data-stu-id="5cc88-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="5cc88-241">Als u de configuratie wilt opslaan, moet u een unieke configuratiewaarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="5cc88-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="5cc88-242">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5cc88-242">Additional resources</span></span>
--------

[<span data-ttu-id="5cc88-243">Een nomenclatuur met productnummers maken voor vooraf gedefinieerde productvarianten</span><span class="sxs-lookup"><span data-stu-id="5cc88-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="5cc88-244">Een productnummernomenclatuur voor geconfigureerde productvarianten maken</span><span class="sxs-lookup"><span data-stu-id="5cc88-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


