---
title: Nomenclatuur van productvariantnummers en -namen
description: In dit onderwerp wordt beschreven hoe u een productnummernomenclatuur instelt om de vaste indeling [productmodelnummer - configuratie - maat - kleur - stijl] te vervangen. De nieuwe nomenclatuur heeft een beoogde indeling die het productmodelnummer, de actieve productdimensies en tekstscheidingstekens van uw keuze bevat. U kunt ook een nomenclatuur maken voor productnamen. Ten slotte kunt u een nomenclatuur maken om configuraties te identificeren die worden gemaakt door de op beperkingen gebaseerde productconfigurator. Deze nomenclaturen kunnen kenmerken van uw keuze bevatten.
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 4ebebc1d287908dbe8ac7557c34fc6693c88bfae
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="74cdb-107">Nomenclatuur van productvariantnummers en -namen</span><span class="sxs-lookup"><span data-stu-id="74cdb-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="74cdb-108">In dit onderwerp wordt beschreven hoe u een productnummernomenclatuur instelt om de vaste indeling [productmodelnummer - configuratie - maat - kleur - stijl] te vervangen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="74cdb-109">De nieuwe nomenclatuur heeft een beoogde indeling die het productmodelnummer, de actieve productdimensies en tekstscheidingstekens van uw keuze bevat.</span><span class="sxs-lookup"><span data-stu-id="74cdb-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="74cdb-110">U kunt ook een nomenclatuur maken voor productnamen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="74cdb-111">Ten slotte kunt u een nomenclatuur maken om configuraties te identificeren die worden gemaakt door de op beperkingen gebaseerde productconfigurator.</span><span class="sxs-lookup"><span data-stu-id="74cdb-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="74cdb-112">Deze nomenclaturen kunnen kenmerken van uw keuze bevatten.</span><span class="sxs-lookup"><span data-stu-id="74cdb-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="74cdb-113">Met de nieuwe nomenclaturen voor productvariantnummers en productvariantnamen kunt u segmenten in de id's opnemen voor productvarianten.</span><span class="sxs-lookup"><span data-stu-id="74cdb-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="74cdb-114">Deze segmenten kunnen productmodelnummer en -naam, productdimensie-id's en -namen, nummerreeksen, tekstconstanten en kenmerken omvatten.</span><span class="sxs-lookup"><span data-stu-id="74cdb-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="74cdb-115">Met deze functionaliteit kunt u snel een specifieke productvariant vinden wanneer u een verkooporder of een inkooporder maakt.</span><span class="sxs-lookup"><span data-stu-id="74cdb-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="74cdb-116">U maakt nomenclaturen voor zowel productvariantnummers als productvariantnamen met behulp van de pagina **Productnomenclatuur**.</span><span class="sxs-lookup"><span data-stu-id="74cdb-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="74cdb-117">Als u deze pagina wilt openen, klikt u op **Productgegevensbeheer** &gt; **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="74cdb-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="74cdb-118">Nomenclatuur met vooraf gedefinieerde productvarianten</span><span class="sxs-lookup"><span data-stu-id="74cdb-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="74cdb-119">De productvarianten worden gegenereerd voor productmodellen volgens drie configuratietechnologieën:</span><span class="sxs-lookup"><span data-stu-id="74cdb-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="74cdb-120">Vooraf gedefinieerde varianten</span><span class="sxs-lookup"><span data-stu-id="74cdb-120">Predefined variants</span></span>
-   <span data-ttu-id="74cdb-121">Op basis van beperkingen</span><span class="sxs-lookup"><span data-stu-id="74cdb-121">Constraint-based</span></span>
-   <span data-ttu-id="74cdb-122">Op basis van dimensies</span><span class="sxs-lookup"><span data-stu-id="74cdb-122">Dimension-based</span></span>

<span data-ttu-id="74cdb-123">Elke productvariant heeft een nummer en een naam en in de nomenclatuur van de productvariant-id's kunt u de segmenten selecteren die in elk productvariantnummer of -naam worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="74cdb-124">U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:</span><span class="sxs-lookup"><span data-stu-id="74cdb-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="74cdb-125">Nummer van basismaster</span><span class="sxs-lookup"><span data-stu-id="74cdb-125">Product master number</span></span>
-   <span data-ttu-id="74cdb-126">Naam van productmodel</span><span class="sxs-lookup"><span data-stu-id="74cdb-126">Product master name</span></span>
-   <span data-ttu-id="74cdb-127">Nummerreekswaarde</span><span class="sxs-lookup"><span data-stu-id="74cdb-127">Number sequence value</span></span>
-   <span data-ttu-id="74cdb-128">Tekstconstante</span><span class="sxs-lookup"><span data-stu-id="74cdb-128">Text constant</span></span>
-   <span data-ttu-id="74cdb-129">Productdimensies</span><span class="sxs-lookup"><span data-stu-id="74cdb-129">Product dimensions</span></span>
    -   <span data-ttu-id="74cdb-130">Configuratie-id of -naam</span><span class="sxs-lookup"><span data-stu-id="74cdb-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="74cdb-131">Kleur-id of -naam</span><span class="sxs-lookup"><span data-stu-id="74cdb-131">Color ID or name</span></span>
    -   <span data-ttu-id="74cdb-132">Maat-id of -naam</span><span class="sxs-lookup"><span data-stu-id="74cdb-132">Size ID or name</span></span>
    -   <span data-ttu-id="74cdb-133">Stijl-id of -naam</span><span class="sxs-lookup"><span data-stu-id="74cdb-133">Style ID or name</span></span>

<span data-ttu-id="74cdb-134">Nadat een productvariant-id hebt gedefinieerd, kunt u deze koppelen aan een productdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="74cdb-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="74cdb-135">Aan alle productmodellen die verwijzen naar deze productdimensiegroep, worden vervolgens productvariantnummers toegewezen op basis van de nomenclatuur.</span><span class="sxs-lookup"><span data-stu-id="74cdb-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="74cdb-136">Nomenclaturen van productvariantnamen kunnen echter niet worden gekoppeld aan productdimensiegroepen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="74cdb-137">U kunt ook een nomenclatuur voor productvariant-id's direct aan een productmodel toewijzen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="74cdb-138">In dit geval worden aan de productvarianten die behoren tot het productmodel, productvariantnummers en -namen toegewezen volgens de nomenclaturen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="74cdb-139">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="74cdb-139">Example</span></span>

<span data-ttu-id="74cdb-140">Een T-shirt (TS1234) wordt geproduceerd in drie maten (S, M, L), vier kleuren (rood, groen, blauw, geel) en twee stijlen (Polo, V).</span><span class="sxs-lookup"><span data-stu-id="74cdb-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="74cdb-141">Daarom zijn 24 productvarianten mogelijk (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="74cdb-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="74cdb-142">U maakt een productvariantnummernomenclatuur met de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="74cdb-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="74cdb-143">Nummer van basismaster</span><span class="sxs-lookup"><span data-stu-id="74cdb-143">Product master number</span></span>
2.  <span data-ttu-id="74cdb-144">Tekstconstante: "-"</span><span class="sxs-lookup"><span data-stu-id="74cdb-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="74cdb-145">Kleur</span><span class="sxs-lookup"><span data-stu-id="74cdb-145">Color</span></span>
4.  <span data-ttu-id="74cdb-146">Tekstconstante: "-"</span><span class="sxs-lookup"><span data-stu-id="74cdb-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="74cdb-147">Grootte</span><span class="sxs-lookup"><span data-stu-id="74cdb-147">Size</span></span>
6.  <span data-ttu-id="74cdb-148">Tekstconstante: "-"</span><span class="sxs-lookup"><span data-stu-id="74cdb-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="74cdb-149">Opmaakmodel</span><span class="sxs-lookup"><span data-stu-id="74cdb-149">Style</span></span>

<span data-ttu-id="74cdb-150">In dit geval is het productvariantnummer voor een rood, klein polo T-shirt TS1234-Rood-Klein-Polo.</span><span class="sxs-lookup"><span data-stu-id="74cdb-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="74cdb-151">Op beperkingen gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="74cdb-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="74cdb-152">Voor op beperkingen gebaseerde configuraties kunt u een specifieke nomenclatuur maken voor de configuratieproductdimensie.</span><span class="sxs-lookup"><span data-stu-id="74cdb-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="74cdb-153">U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:</span><span class="sxs-lookup"><span data-stu-id="74cdb-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="74cdb-154">Nummerreekswaarde</span><span class="sxs-lookup"><span data-stu-id="74cdb-154">Number sequence value</span></span>
-   <span data-ttu-id="74cdb-155">Tekstconstante</span><span class="sxs-lookup"><span data-stu-id="74cdb-155">Text constant</span></span>
-   <span data-ttu-id="74cdb-156">Kenmerkwaarde</span><span class="sxs-lookup"><span data-stu-id="74cdb-156">Attribute value</span></span>

<span data-ttu-id="74cdb-157">Elke component in een productconfiguratiemodel kan een eigen configuratienomenclatuur hebben.</span><span class="sxs-lookup"><span data-stu-id="74cdb-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="74cdb-158">Alleen kenmerken die bij de component horen, kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="74cdb-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="74cdb-159">Kenmerken van subcomponenten of gebruikersvereisten kunnen niet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="74cdb-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="74cdb-160">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="74cdb-160">Example</span></span>

<span data-ttu-id="74cdb-161">Een productconfiguratiemodel heeft een hoofdcomponent met twee kenmerken:</span><span class="sxs-lookup"><span data-stu-id="74cdb-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="74cdb-162">Materiaal (plastic, hout, staal)</span><span class="sxs-lookup"><span data-stu-id="74cdb-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="74cdb-163">Lengte (10... 100)</span><span class="sxs-lookup"><span data-stu-id="74cdb-163">Length (10...100)</span></span>

<span data-ttu-id="74cdb-164">U maakt een configuratienomenclatuur met de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="74cdb-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="74cdb-165">Kenmerkwaarde: materiaal</span><span class="sxs-lookup"><span data-stu-id="74cdb-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="74cdb-166">Tekstconstante: "AAA"</span><span class="sxs-lookup"><span data-stu-id="74cdb-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="74cdb-167">Kenmerkwaarde: lengte</span><span class="sxs-lookup"><span data-stu-id="74cdb-167">Attribute value: Length</span></span>

<span data-ttu-id="74cdb-168">In dit geval is de configuratie-id voor houten materiaal met een lengte van 78 WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="74cdb-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="74cdb-169">Nomenclatuur van op dimensies gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="74cdb-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="74cdb-170">Voor op dimensies gebaseerde configuraties kunt u een specifieke nomenclatuur maken voor de configuratieproductdimensie.</span><span class="sxs-lookup"><span data-stu-id="74cdb-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="74cdb-171">U kunt de volgende segmenten selecteren op de pagina **Productnomenclatuur**:</span><span class="sxs-lookup"><span data-stu-id="74cdb-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="74cdb-172">Nummerreekswaarde</span><span class="sxs-lookup"><span data-stu-id="74cdb-172">Number sequence value</span></span>
-   <span data-ttu-id="74cdb-173">Tekstconstante</span><span class="sxs-lookup"><span data-stu-id="74cdb-173">Text constant</span></span>
-   <span data-ttu-id="74cdb-174">Configuratiegroepitem</span><span class="sxs-lookup"><span data-stu-id="74cdb-174">Configuration group item</span></span>

<span data-ttu-id="74cdb-175">U kunt een configuratienomenclatuur definiëren voor een stuklijst (BOM).</span><span class="sxs-lookup"><span data-stu-id="74cdb-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="74cdb-176">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="74cdb-176">Example</span></span>

<span data-ttu-id="74cdb-177">Een stuklijst heeft vier stuklijstregels die worden onderverdeeld in twee configuratiegroepen:</span><span class="sxs-lookup"><span data-stu-id="74cdb-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="74cdb-178">Stuklijstregel: M0007, standaardbehuizing</span><span class="sxs-lookup"><span data-stu-id="74cdb-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="74cdb-179">Configuratiegroep: behuizing</span><span class="sxs-lookup"><span data-stu-id="74cdb-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="74cdb-180">Stuklijstregel: M0008, geavanceerde behuizing</span><span class="sxs-lookup"><span data-stu-id="74cdb-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="74cdb-181">Configuratiegroep: behuizing</span><span class="sxs-lookup"><span data-stu-id="74cdb-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="74cdb-182">Stuklijstregel: M0021, voorgrill van stof</span><span class="sxs-lookup"><span data-stu-id="74cdb-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="74cdb-183">Configuratiegroep: Voorgrill</span><span class="sxs-lookup"><span data-stu-id="74cdb-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="74cdb-184">Stuklijstregel: M0022, metalen voorgrill</span><span class="sxs-lookup"><span data-stu-id="74cdb-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="74cdb-185">Configuratiegroep: Voorgrill</span><span class="sxs-lookup"><span data-stu-id="74cdb-185">Configuration group: Front grill</span></span>

<span data-ttu-id="74cdb-186">U maakt een configuratienomenclatuur met de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="74cdb-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="74cdb-187">Configuratiegroep: behuizing</span><span class="sxs-lookup"><span data-stu-id="74cdb-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="74cdb-188">Tekstconstante: "&"</span><span class="sxs-lookup"><span data-stu-id="74cdb-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="74cdb-189">Configuratiegroep: Voorgrill</span><span class="sxs-lookup"><span data-stu-id="74cdb-189">Configuration group: Front grill</span></span>

<span data-ttu-id="74cdb-190">In dit geval is de configuratie-id voor een standaardbehuizing met een voorgrill van stof M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="74cdb-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="74cdb-191">Nomenclatuur voor een combinatie van productvarianten en configuraties</span><span class="sxs-lookup"><span data-stu-id="74cdb-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="74cdb-192">Als u de op beperkingen of dimensies gebaseerde configuratietechnologie gebruikt om productvarianten voor een productmodel te configureren, kunnen de productvariantnummers van de productvarianten de nomenclatuur bevatten van de configuratiedimensie.</span><span class="sxs-lookup"><span data-stu-id="74cdb-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="74cdb-193">Volg deze stappen om varianten te configureren.</span><span class="sxs-lookup"><span data-stu-id="74cdb-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="74cdb-194">Definieer op de pagina **Productnomenclatuur** een nomenclatuur van productvariantnummers die de configuratiedimensie omvat.</span><span class="sxs-lookup"><span data-stu-id="74cdb-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="74cdb-195">Wijs de nomenclatuur toe aan een productdimensiegroep die de configuratiedimensie heeft.</span><span class="sxs-lookup"><span data-stu-id="74cdb-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="74cdb-196">Definieer een configuratienomenclatuur voor de componenten of de stuklijsten die worden gebruikt voor het configureren van de productvarianten.</span><span class="sxs-lookup"><span data-stu-id="74cdb-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="74cdb-197">U kunt ook nomenclaturen maken voor de productvariantnamen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="74cdb-198">De productvariantnamen kunnen worden geconfigureerd voor het opnemen van de configuratie-ID of -naam.</span><span class="sxs-lookup"><span data-stu-id="74cdb-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="74cdb-199">Voorbeeld van op beperkingen gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="74cdb-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="74cdb-200">In dit voorbeeld gebruikt u een productvariantnummernomenclatuur die bestaat uit de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="74cdb-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="74cdb-201">Nummer van basismaster</span><span class="sxs-lookup"><span data-stu-id="74cdb-201">Product master number</span></span>
2.  <span data-ttu-id="74cdb-202">Tekstconstante "\_"</span><span class="sxs-lookup"><span data-stu-id="74cdb-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="74cdb-203">Configuratie</span><span class="sxs-lookup"><span data-stu-id="74cdb-203">Configuration</span></span>

<span data-ttu-id="74cdb-204">De configuratienomenclatuur bestaat uit de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="74cdb-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="74cdb-205">Kenmerkwaarde: materiaal</span><span class="sxs-lookup"><span data-stu-id="74cdb-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="74cdb-206">Tekstconstante: "AAA"</span><span class="sxs-lookup"><span data-stu-id="74cdb-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="74cdb-207">Kenmerkwaarde: lengte</span><span class="sxs-lookup"><span data-stu-id="74cdb-207">Attribute value: Length</span></span>

<span data-ttu-id="74cdb-208">U kunt de volgende waarden voor segmenten invoeren:</span><span class="sxs-lookup"><span data-stu-id="74cdb-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="74cdb-209">Productmodelnummer = **M0099**</span><span class="sxs-lookup"><span data-stu-id="74cdb-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="74cdb-210">Materiaal = **Plastic**</span><span class="sxs-lookup"><span data-stu-id="74cdb-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="74cdb-211">Lengte = **12**</span><span class="sxs-lookup"><span data-stu-id="74cdb-211">Length = **12**</span></span>

<span data-ttu-id="74cdb-212">In dit geval is het productvariantnummer M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="74cdb-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="74cdb-213">Voorbeeld van op dimensies gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="74cdb-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="74cdb-214">In dit voorbeeld gebruikt u een productvariantnummernomenclatuur die bestaat uit de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="74cdb-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="74cdb-215">Nummer van basismaster</span><span class="sxs-lookup"><span data-stu-id="74cdb-215">Product master number</span></span>
2.  <span data-ttu-id="74cdb-216">Tekstconstante "//"</span><span class="sxs-lookup"><span data-stu-id="74cdb-216">Text constant "//"</span></span>
3.  <span data-ttu-id="74cdb-217">Configuratie</span><span class="sxs-lookup"><span data-stu-id="74cdb-217">Configuration</span></span>

<span data-ttu-id="74cdb-218">De configuratienomenclatuur bestaat uit de volgende segmenten:</span><span class="sxs-lookup"><span data-stu-id="74cdb-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="74cdb-219">Configuratiegroep: behuizing</span><span class="sxs-lookup"><span data-stu-id="74cdb-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="74cdb-220">Tekstconstante: "&"</span><span class="sxs-lookup"><span data-stu-id="74cdb-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="74cdb-221">Configuratiegroep: Voorgrill</span><span class="sxs-lookup"><span data-stu-id="74cdb-221">Configuration group: Front grill</span></span>

<span data-ttu-id="74cdb-222">U kunt de volgende waarden voor segmenten invoeren:</span><span class="sxs-lookup"><span data-stu-id="74cdb-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="74cdb-223">Productmodelnummer = **D0123**</span><span class="sxs-lookup"><span data-stu-id="74cdb-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="74cdb-224">Behuizing = **M0008**</span><span class="sxs-lookup"><span data-stu-id="74cdb-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="74cdb-225">Voorgrill = **M0022**</span><span class="sxs-lookup"><span data-stu-id="74cdb-225">Front grill = **M0022**</span></span>

<span data-ttu-id="74cdb-226">In dit geval is het productvariantnummer D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="74cdb-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="74cdb-227">Nummeringsconflicten</span><span class="sxs-lookup"><span data-stu-id="74cdb-227">Numbering conflicts</span></span>
<span data-ttu-id="74cdb-228">In sommige gevallen is het mogelijk dat een nomenclatuur voor productvariantnummers die u instelt, geen unieke productvariantnummers produceert.</span><span class="sxs-lookup"><span data-stu-id="74cdb-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="74cdb-229">De productvariantnummers zijn bijvoorbeeld niet uniek als één actieve productdimensie niet wordt opgenomen in de nomenclatuur van een productmodel dat de vooraf gedefinieerde variantconfiguratietechnologie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="74cdb-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="74cdb-230">De manier waarop u conflicten verwerken, varieert afhankelijk van de configuratietechnologie.</span><span class="sxs-lookup"><span data-stu-id="74cdb-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="74cdb-231">Vooraf gedefinieerde varianten</span><span class="sxs-lookup"><span data-stu-id="74cdb-231">Predefined variants</span></span>

<span data-ttu-id="74cdb-232">Er treedt een fout op als u handmatig of automatisch probeert productvarianten te genereren, en meerdere productvarianten hetzelfde productvariantnummer krijgen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="74cdb-233">Als u dit scenario wilt voorkomen, moet u alle actieve productdimensies in de productdimensiegroep gebruiken.</span><span class="sxs-lookup"><span data-stu-id="74cdb-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="74cdb-234">U kunt ook een nummerreeks opnemen om te garanderen dat de productvariantnummers uniek zijn.</span><span class="sxs-lookup"><span data-stu-id="74cdb-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="74cdb-235">Op beperkingen gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="74cdb-235">Constraint-based configurations</span></span>

<span data-ttu-id="74cdb-236">Afhankelijk van de nomenclatuur kan het systeem proberen een niet-uniek productvariantnummer aan een configuratie toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="74cdb-237">In dit geval gebruikt het systeem de nummerreeks voor de configuratiedimensie als productvariantnummer. Als dit gebeurt, ontvangt u een waarschuwing.</span><span class="sxs-lookup"><span data-stu-id="74cdb-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="74cdb-238">Als u dit scenario wilt voorkomen, moet u voldoende kenmerken opnemen in de nomenclatuur om unieke productvariantnummers te garanderen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="74cdb-239">U moet tevens zorgen dat de optie **Opnieuw gebruiken** is ingeschakeld voor het onderdeel.</span><span class="sxs-lookup"><span data-stu-id="74cdb-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="74cdb-240">Op dimensie gebaseerde configuraties</span><span class="sxs-lookup"><span data-stu-id="74cdb-240">Dimension-based configurations</span></span>

<span data-ttu-id="74cdb-241">Tijdens een stap van het configuratieproces suggereert het systeem een configuratiewaarde volgens de nomenclatuur.</span><span class="sxs-lookup"><span data-stu-id="74cdb-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="74cdb-242">In deze stap kunt u de configuratiewaarde handmatig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="74cdb-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="74cdb-243">Wanneer u de configuratie opslaat, controleert het systeem of de configuratiewaarde uniek is.</span><span class="sxs-lookup"><span data-stu-id="74cdb-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="74cdb-244">Als de waarde die u hebt ingevoerd niet uniek is, ontvangt u een foutbericht.</span><span class="sxs-lookup"><span data-stu-id="74cdb-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="74cdb-245">Als u de configuratie wilt opslaan, moet u een unieke configuratiewaarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="74cdb-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="74cdb-246">Zie ook</span><span class="sxs-lookup"><span data-stu-id="74cdb-246">See also</span></span>
--------

[<span data-ttu-id="74cdb-247">Een productnummernomenclatuur voor vooraf bepaalde productvarianten maken</span><span class="sxs-lookup"><span data-stu-id="74cdb-247">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="74cdb-248">Een productnummernomenclatuur voor geconfigureerde productvarianten maken</span><span class="sxs-lookup"><span data-stu-id="74cdb-248">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


