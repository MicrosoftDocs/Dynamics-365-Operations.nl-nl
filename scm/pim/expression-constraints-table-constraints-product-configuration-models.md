---
title: Expressiebeperkingen en tabelbeperkingen in productconfiguratiemodellen
description: Dit onderwerp beschrijft het gebruik van expressiebeperkingen en tabelbeperkingen. U gebruikt beperkingen om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert. U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 66d5ec61c1d69ebc8a8fc10d0b9b2a4b174729ee
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="584dc-105">Expressiebeperkingen en tabelbeperkingen in productconfiguratiemodellen</span><span class="sxs-lookup"><span data-stu-id="584dc-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="584dc-106">Dit onderwerp beschrijft het gebruik van expressiebeperkingen en tabelbeperkingen.</span><span class="sxs-lookup"><span data-stu-id="584dc-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="584dc-107">U gebruikt beperkingen om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert.</span><span class="sxs-lookup"><span data-stu-id="584dc-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="584dc-108">U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.</span><span class="sxs-lookup"><span data-stu-id="584dc-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="584dc-109">Beperkingen worden gebruikt om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert.</span><span class="sxs-lookup"><span data-stu-id="584dc-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="584dc-110">U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.</span><span class="sxs-lookup"><span data-stu-id="584dc-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="584dc-111">Wat zijn expressiebeperkingen?</span><span class="sxs-lookup"><span data-stu-id="584dc-111">What are expression constraints?</span></span>
<span data-ttu-id="584dc-112">Expressiebeperkingen worden gekenmerkt door een expressie met rekenkundige en Booleaanse operatoren en functies.</span><span class="sxs-lookup"><span data-stu-id="584dc-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="584dc-113">Een expressiebeperking wordt geschreven voor een bepaald onderdeel in een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="584dc-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="584dc-114">De beperking kan niet worden hergebruikt door of gedeeld met een ander onderdeel.</span><span class="sxs-lookup"><span data-stu-id="584dc-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="584dc-115">Expressiebeperkingen voor een onderdeel kunnen echter verwijzen naar kenmerken van subonderdelen van het onderdeel.</span><span class="sxs-lookup"><span data-stu-id="584dc-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="584dc-116">Wat zijn tabelbeperkingen?</span><span class="sxs-lookup"><span data-stu-id="584dc-116">What are table constraints?</span></span>
<span data-ttu-id="584dc-117">Tabelbeperkingen maken een lijst met de combinaties van waarden die zijn toegestaan voor kenmerken wanneer u een product configureert.</span><span class="sxs-lookup"><span data-stu-id="584dc-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="584dc-118">De definities van tabelbeperkingen kunnen algemeen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="584dc-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="584dc-119">Wanneer u een tabelbeperking voor een component maakt in een productconfiguratiemodel, selecteert u een definitie voor de tabelbeperking.</span><span class="sxs-lookup"><span data-stu-id="584dc-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="584dc-120">Om de combinaties te maken die worden toegestaan, voegt u kenmerken van specifieke typen aan de onderdelen toe.</span><span class="sxs-lookup"><span data-stu-id="584dc-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="584dc-121">Elk kenmerktype heeft een specifieke waarde.</span><span class="sxs-lookup"><span data-stu-id="584dc-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="584dc-122">Voorbeeld van een tabelbeperking.</span><span class="sxs-lookup"><span data-stu-id="584dc-122">Example of a table constraint</span></span>

<span data-ttu-id="584dc-123">Dit voorbeeld toont hoe u de configuratie van een speaker tot specifieke afwerkingen van de behuizingen en voorkanten kunt beperken.</span><span class="sxs-lookup"><span data-stu-id="584dc-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="584dc-124">De eerste tabel laat de afwerkingen van de behuizingen en voorkanten zien die algemeen beschikbaar zijn voor configuratie.</span><span class="sxs-lookup"><span data-stu-id="584dc-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="584dc-125">De waarden zijn gedefinieerd voor **Afwerking behuizing** en **Voorgrill**.</span><span class="sxs-lookup"><span data-stu-id="584dc-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="584dc-126">Kenmerktype</span><span class="sxs-lookup"><span data-stu-id="584dc-126">Attribute type</span></span> | <span data-ttu-id="584dc-127">Waarden</span><span class="sxs-lookup"><span data-stu-id="584dc-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="584dc-128">Afwerking behuizing</span><span class="sxs-lookup"><span data-stu-id="584dc-128">Cabinet finish</span></span> | <span data-ttu-id="584dc-129">Zwart, Eiken, Rozenhout, Wit</span><span class="sxs-lookup"><span data-stu-id="584dc-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="584dc-130">Voorgrill</span><span class="sxs-lookup"><span data-stu-id="584dc-130">Front grill</span></span>    | <span data-ttu-id="584dc-131">Zwart, Metaal, Wit</span><span class="sxs-lookup"><span data-stu-id="584dc-131">Black, Metal, White</span></span>         |

<span data-ttu-id="584dc-132">De volgende tabel geeft de combinaties weer die door de tabelbeperking **Kleur en afwerking** zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="584dc-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="584dc-133">Door deze tabelbeperking te gebruiken, kunt u een speaker configureren met een eiken afwerking en een zwarte grill, een rozenhouten afwerking en een witte grill, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="584dc-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="584dc-134">Voltooien</span><span class="sxs-lookup"><span data-stu-id="584dc-134">Finish</span></span>         | <span data-ttu-id="584dc-135">Grill</span><span class="sxs-lookup"><span data-stu-id="584dc-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="584dc-136">Eiken</span><span class="sxs-lookup"><span data-stu-id="584dc-136">Oak</span></span>            | <span data-ttu-id="584dc-137">Zwart</span><span class="sxs-lookup"><span data-stu-id="584dc-137">Black</span></span>                       |
| <span data-ttu-id="584dc-138">Rozenhout</span><span class="sxs-lookup"><span data-stu-id="584dc-138">Rosewood</span></span>       | <span data-ttu-id="584dc-139">Wit</span><span class="sxs-lookup"><span data-stu-id="584dc-139">White</span></span>                       |
| <span data-ttu-id="584dc-140">Wit</span><span class="sxs-lookup"><span data-stu-id="584dc-140">White</span></span>          | <span data-ttu-id="584dc-141">Zwart</span><span class="sxs-lookup"><span data-stu-id="584dc-141">Black</span></span>                       |
| <span data-ttu-id="584dc-142">Wit</span><span class="sxs-lookup"><span data-stu-id="584dc-142">White</span></span>          | <span data-ttu-id="584dc-143">Wit</span><span class="sxs-lookup"><span data-stu-id="584dc-143">White</span></span>                       |
| <span data-ttu-id="584dc-144">Zwart</span><span class="sxs-lookup"><span data-stu-id="584dc-144">Black</span></span>          | <span data-ttu-id="584dc-145">Zwart</span><span class="sxs-lookup"><span data-stu-id="584dc-145">Black</span></span>                       |
| <span data-ttu-id="584dc-146">Zwart</span><span class="sxs-lookup"><span data-stu-id="584dc-146">Black</span></span>          | <span data-ttu-id="584dc-147">Metaal</span><span class="sxs-lookup"><span data-stu-id="584dc-147">Metal</span></span>                       | 

<span data-ttu-id="584dc-148">U kunt door het systeem gedefinieerde en door de gebruiker gedefinieerde tabelbeperkingen maken.</span><span class="sxs-lookup"><span data-stu-id="584dc-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="584dc-149">Voor meer informatie, zie [Door het systeem gedefinieerde en door gebruiker gedefinieerde tabelbeperkingen](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="584dc-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="584dc-150">Welke syntaxis moet worden gebruikt om beperkingen te schrijven?</span><span class="sxs-lookup"><span data-stu-id="584dc-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="584dc-151">Gebruik de OML-syntaxis (Optimization Modeling Language) wanneer u beperkingen opstelt.</span><span class="sxs-lookup"><span data-stu-id="584dc-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="584dc-152">Microsoft Solver Foundation-beperkingsoplosser wordt gebruikt om de beperkingen op te lossen.</span><span class="sxs-lookup"><span data-stu-id="584dc-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="584dc-153">Moet ik tabelbeperkingen of expressiebeperkingen gebruiken?</span><span class="sxs-lookup"><span data-stu-id="584dc-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="584dc-154">U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.</span><span class="sxs-lookup"><span data-stu-id="584dc-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="584dc-155">U maakt een tabelbeperking als matrix, terwijl een expressiebeperking een afzonderlijke statement is.</span><span class="sxs-lookup"><span data-stu-id="584dc-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="584dc-156">Wanneer u een product configureert, is het niet van belang welk type beperking wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="584dc-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="584dc-157">In het volgende voorbeeld kunt u zien hoe de twee methoden verschillen.</span><span class="sxs-lookup"><span data-stu-id="584dc-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="584dc-158">Wanneer u een product met de volgende beperkingsinstellingen configureert, worden deze combinaties toegestaan:</span><span class="sxs-lookup"><span data-stu-id="584dc-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="584dc-159">Een product in de kleur Zwart, in grootte 30 of 50</span><span class="sxs-lookup"><span data-stu-id="584dc-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="584dc-160">Een product in de kleur Rood, in grootte 20</span><span class="sxs-lookup"><span data-stu-id="584dc-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="584dc-161">Tabelbeperkingsinstelling</span><span class="sxs-lookup"><span data-stu-id="584dc-161">Table constraint setup</span></span>

| <span data-ttu-id="584dc-162">Kleur</span><span class="sxs-lookup"><span data-stu-id="584dc-162">Color</span></span> | <span data-ttu-id="584dc-163">Grootte</span><span class="sxs-lookup"><span data-stu-id="584dc-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="584dc-164">Zwart</span><span class="sxs-lookup"><span data-stu-id="584dc-164">Black</span></span> | <span data-ttu-id="584dc-165">30</span><span class="sxs-lookup"><span data-stu-id="584dc-165">30</span></span>   |
| <span data-ttu-id="584dc-166">Zwart</span><span class="sxs-lookup"><span data-stu-id="584dc-166">Black</span></span> | <span data-ttu-id="584dc-167">50</span><span class="sxs-lookup"><span data-stu-id="584dc-167">50</span></span>   |
| <span data-ttu-id="584dc-168">Rood</span><span class="sxs-lookup"><span data-stu-id="584dc-168">Red</span></span>   | <span data-ttu-id="584dc-169">20</span><span class="sxs-lookup"><span data-stu-id="584dc-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="584dc-170">Instelling expressiebeperking</span><span class="sxs-lookup"><span data-stu-id="584dc-170">Expression constraint setup</span></span>

<span data-ttu-id="584dc-171">(Kleur == "Zwart" & (afmeting == "30" | afmeting == "50")) | (kleur == "Rood" & afmeting = "20")</span><span class="sxs-lookup"><span data-stu-id="584dc-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="584dc-172">Moet ik operators gebruiken of tussenvoegselaantekening gebruiken wanneer ik expressiebeperkingen schrijf?</span><span class="sxs-lookup"><span data-stu-id="584dc-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="584dc-173">U kunt een expressiebeperking opstellen met behulp van de beschikbare voorvoegseloperatoren of met tussenvoegselnotatie.</span><span class="sxs-lookup"><span data-stu-id="584dc-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="584dc-174">Voor de operatoren **Min**, **Max**, en **Abs** kunt u de tussenvoegselnotatie niet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="584dc-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="584dc-175">Deze operatoren zijn opgenomen als standaardoperatoren in de meeste programmeertalen.</span><span class="sxs-lookup"><span data-stu-id="584dc-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="584dc-176">Welke operators en tussenvoegselnotatie kan ik gebruiken wanneer ik expressiebeperkingen schrijf?</span><span class="sxs-lookup"><span data-stu-id="584dc-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="584dc-177">In de volgende tabel worden de operatoren en de tussenvoegselnotatie vermeld die u kunt gebruiken voor het schrijven van een expressiebeperking voor een onderdeel van een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="584dc-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="584dc-178">In de voorbeelden in de eerste tabel kunt u zien hoe u een expressie maakt door tussenvoegselnotaties of operators te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="584dc-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="584dc-179">Operator</span><span class="sxs-lookup"><span data-stu-id="584dc-179">Operator</span></span></th>
<th><span data-ttu-id="584dc-180">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="584dc-180">Description</span></span></th>
<th><span data-ttu-id="584dc-181">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="584dc-181">Syntax</span></span></th>
<th><span data-ttu-id="584dc-182">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="584dc-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="584dc-183">Heeft</span><span class="sxs-lookup"><span data-stu-id="584dc-183">Implies</span></span></td>
<td><span data-ttu-id="584dc-184">Dit is waar als de eerste voorwaarde onwaar is, de tweede voorwaarde waar, of beide.</span><span class="sxs-lookup"><span data-stu-id="584dc-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="584dc-185">Heeft[a, b], tussenvoegselaantekening: a -: b</span><span class="sxs-lookup"><span data-stu-id="584dc-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="584dc-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="584dc-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="584dc-187"><strong>Tussenvoegselnotatie:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="584dc-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="584dc-188">En</span><span class="sxs-lookup"><span data-stu-id="584dc-188">And</span></span></td>
<td><span data-ttu-id="584dc-189">Dit is alleen waar als alle voorwaarden waar zijn.</span><span class="sxs-lookup"><span data-stu-id="584dc-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="584dc-190">Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>Waar</strong>.</span><span class="sxs-lookup"><span data-stu-id="584dc-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="584dc-191">And[args], tussenvoegsel: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="584dc-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="584dc-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="584dc-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="584dc-193"><strong>Tussenvoegselnotatie:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="584dc-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="584dc-194">Of</span><span class="sxs-lookup"><span data-stu-id="584dc-194">Or</span></span></td>
<td><span data-ttu-id="584dc-195">Dit is waar als een van de voorwaarden waar is.</span><span class="sxs-lookup"><span data-stu-id="584dc-195">This is true if any condition is true.</span></span> <span data-ttu-id="584dc-196">Als het aantal condities 0 is (nul), is het product <strong>Onwaar</strong>.</span><span class="sxs-lookup"><span data-stu-id="584dc-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="584dc-197">Or[args], tussenvoegsel: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="584dc-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="584dc-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="584dc-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="584dc-199"><strong>Tussenvoegselnotatie:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="584dc-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="584dc-200">Plus</span><span class="sxs-lookup"><span data-stu-id="584dc-200">Plus</span></span></td>
<td><span data-ttu-id="584dc-201">Dit is de som van de voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="584dc-201">This sums its conditions.</span></span> <span data-ttu-id="584dc-202">Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="584dc-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="584dc-203">Plus[args], tussenvoegsel: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="584dc-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="584dc-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="584dc-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="584dc-205"><strong>Tussenvoegselnotatie:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="584dc-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="584dc-206">Min</span><span class="sxs-lookup"><span data-stu-id="584dc-206">Minus</span></span></td>
<td><span data-ttu-id="584dc-207">Het argument wordt genegeerd.</span><span class="sxs-lookup"><span data-stu-id="584dc-207">This negates its argument.</span></span> <span data-ttu-id="584dc-208">Het moet precies één voorwaarde hebben.</span><span class="sxs-lookup"><span data-stu-id="584dc-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="584dc-209">Minus[expr], tussenvoegselaantekening: -expr</span><span class="sxs-lookup"><span data-stu-id="584dc-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="584dc-210"><strong>Operator:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="584dc-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="584dc-211"><strong>Tussenvoegselnotatie:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="584dc-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="584dc-212">Abs</span><span class="sxs-lookup"><span data-stu-id="584dc-212">Abs</span></span></td>
<td><span data-ttu-id="584dc-213">Hiervoor is de absolute waarde van de voorwaarde vereist.</span><span class="sxs-lookup"><span data-stu-id="584dc-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="584dc-214">Het moet precies één voorwaarde hebben.</span><span class="sxs-lookup"><span data-stu-id="584dc-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="584dc-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="584dc-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="584dc-216"><strong>Operator:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="584dc-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="584dc-217">Tijden</span><span class="sxs-lookup"><span data-stu-id="584dc-217">Times</span></span></td>
<td><span data-ttu-id="584dc-218">Hiervoor is het product van de voorwaarden vereist.</span><span class="sxs-lookup"><span data-stu-id="584dc-218">This takes the product of its conditions.</span></span> <span data-ttu-id="584dc-219">Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="584dc-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="584dc-220">Times[args], tussenvoegsel: a * b * ... * z</span><span class="sxs-lookup"><span data-stu-id="584dc-220">Times[args], infix: a * b * ... * z</span></span></td>
<td><ul>
<li><span data-ttu-id="584dc-221"><strong>Operator:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="584dc-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="584dc-222"><strong>Tussenvoegselnotatie:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="584dc-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="584dc-223">Vermogen</span><span class="sxs-lookup"><span data-stu-id="584dc-223">Power</span></span></td>
<td><span data-ttu-id="584dc-224">Hiervoor is een exponentiële waarde vereist.</span><span class="sxs-lookup"><span data-stu-id="584dc-224">This takes an exponential.</span></span> <span data-ttu-id="584dc-225">Hiermee wordt machtsverheffen van rechts naar links toegepast.</span><span class="sxs-lookup"><span data-stu-id="584dc-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="584dc-226">(Dat wil zeggen dat het rechts associatief is) Hierdoor is <strong>Power[a, b, c]</strong> gelijk aan <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="584dc-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="584dc-227"><strong>Power</strong> kan alleen worden gebruikt als de exponent een positieve constante is.</span><span class="sxs-lookup"><span data-stu-id="584dc-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="584dc-228">Power[args], tussenvoegsel: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="584dc-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="584dc-229"><strong>Operator:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="584dc-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="584dc-230"><strong>Tussenvoegselnotatie:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="584dc-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="584dc-231">Max.</span><span class="sxs-lookup"><span data-stu-id="584dc-231">Max</span></span></td>
<td><span data-ttu-id="584dc-232">Dit levert de grootste voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="584dc-232">This produces the largest condition.</span></span> <span data-ttu-id="584dc-233">Als het aantal condities 0 is (nul), resulteert dit in <strong>Oneindigheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="584dc-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="584dc-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="584dc-234">Max[args]</span></span></td>
<td><span data-ttu-id="584dc-235"><strong>Operator:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="584dc-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="584dc-236">Min.</span><span class="sxs-lookup"><span data-stu-id="584dc-236">Min</span></span></td>
<td><span data-ttu-id="584dc-237">Dit levert de kleinste voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="584dc-237">This produces the smallest condition.</span></span> <span data-ttu-id="584dc-238">Als het aantal condities 0 is (nul), resulteert dit in <strong>Oneindigheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="584dc-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="584dc-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="584dc-239">Min[args]</span></span></td>
<td><span data-ttu-id="584dc-240"><strong>Operator:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="584dc-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="584dc-241">Niet</span><span class="sxs-lookup"><span data-stu-id="584dc-241">Not</span></span></td>
<td><span data-ttu-id="584dc-242">Dit resulteert in de logische inverse van de voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="584dc-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="584dc-243">Het moet precies één voorwaarde hebben.</span><span class="sxs-lookup"><span data-stu-id="584dc-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="584dc-244">Niet[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="584dc-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="584dc-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="584dc-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="584dc-246"><strong>Tussenvoegselnotatie:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="584dc-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="584dc-247">De voorbeelden in de volgende tabel geven weer hoe een tussenvoegselnotatie moet worden geschreven.</span><span class="sxs-lookup"><span data-stu-id="584dc-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="584dc-248">Infix-notatie</span><span class="sxs-lookup"><span data-stu-id="584dc-248">Infix notation</span></span>    | <span data-ttu-id="584dc-249">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="584dc-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="584dc-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="584dc-250">x + y + z</span></span>         | <span data-ttu-id="584dc-251">Optelling</span><span class="sxs-lookup"><span data-stu-id="584dc-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="584dc-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="584dc-252">x \* y \* z</span></span>       | <span data-ttu-id="584dc-253">Vermenigvuldigen</span><span class="sxs-lookup"><span data-stu-id="584dc-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="584dc-254">x - y</span><span class="sxs-lookup"><span data-stu-id="584dc-254">x - y</span></span>             | <span data-ttu-id="584dc-255">Binair aftrekken wordt op dezelfde manier vertaald als binaire optelling waarbij er een genegeerde tweede is.</span><span class="sxs-lookup"><span data-stu-id="584dc-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="584dc-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="584dc-256">x ^ y ^ z</span></span>         | <span data-ttu-id="584dc-257">Machtsverheffen met associatie naar rechts</span><span class="sxs-lookup"><span data-stu-id="584dc-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="584dc-258">!x</span><span class="sxs-lookup"><span data-stu-id="584dc-258">!x</span></span>                | <span data-ttu-id="584dc-259">Booleaans niet</span><span class="sxs-lookup"><span data-stu-id="584dc-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="584dc-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="584dc-260">x -: y</span></span>            | <span data-ttu-id="584dc-261">Booleaanse implicatie</span><span class="sxs-lookup"><span data-stu-id="584dc-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="584dc-262">x</span><span class="sxs-lookup"><span data-stu-id="584dc-262">x</span></span> | <span data-ttu-id="584dc-263">y</span><span class="sxs-lookup"><span data-stu-id="584dc-263">y</span></span> | <span data-ttu-id="584dc-264">z</span><span class="sxs-lookup"><span data-stu-id="584dc-264">z</span></span>         | <span data-ttu-id="584dc-265">Booleaans of</span><span class="sxs-lookup"><span data-stu-id="584dc-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="584dc-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="584dc-266">x & y & z</span></span>         | <span data-ttu-id="584dc-267">Booleaans en</span><span class="sxs-lookup"><span data-stu-id="584dc-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="584dc-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="584dc-268">x == y == z</span></span>       | <span data-ttu-id="584dc-269">Gelijkheid</span><span class="sxs-lookup"><span data-stu-id="584dc-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="584dc-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="584dc-270">x != y != z</span></span>       | <span data-ttu-id="584dc-271">Afzonderlijk</span><span class="sxs-lookup"><span data-stu-id="584dc-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="584dc-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="584dc-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="584dc-273">Kleiner dan</span><span class="sxs-lookup"><span data-stu-id="584dc-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="584dc-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="584dc-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="584dc-275">Groter dan</span><span class="sxs-lookup"><span data-stu-id="584dc-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="584dc-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="584dc-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="584dc-277">Kleiner dan of gelijk aan</span><span class="sxs-lookup"><span data-stu-id="584dc-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="584dc-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="584dc-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="584dc-279">Groter dan of gelijk aan</span><span class="sxs-lookup"><span data-stu-id="584dc-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="584dc-280">(x)</span><span class="sxs-lookup"><span data-stu-id="584dc-280">(x)</span></span>               | <span data-ttu-id="584dc-281">Haakjes overschrijven standaard voorrang.</span><span class="sxs-lookup"><span data-stu-id="584dc-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="584dc-282">Waarom worden mijn expressiebeperkingen niet correct gevalideerd?</span><span class="sxs-lookup"><span data-stu-id="584dc-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="584dc-283">U kunt geen gereserveerde sleutelwoorden gebruiken als oplossernamen voor kenmerken, onderdelen of subonderdelen in een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="584dc-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="584dc-284">Hierna vindt u een lijst met de gereserveerde woorden die u niet kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="584dc-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="584dc-285">Plafond</span><span class="sxs-lookup"><span data-stu-id="584dc-285">Ceiling</span></span>
-   <span data-ttu-id="584dc-286">Element</span><span class="sxs-lookup"><span data-stu-id="584dc-286">Element</span></span>
-   <span data-ttu-id="584dc-287">Gelijk</span><span class="sxs-lookup"><span data-stu-id="584dc-287">Equal</span></span>
-   <span data-ttu-id="584dc-288">Etage</span><span class="sxs-lookup"><span data-stu-id="584dc-288">Floor</span></span>
-   <span data-ttu-id="584dc-289">Als</span><span class="sxs-lookup"><span data-stu-id="584dc-289">If</span></span>
-   <span data-ttu-id="584dc-290">Kleiner</span><span class="sxs-lookup"><span data-stu-id="584dc-290">Less</span></span>
-   <span data-ttu-id="584dc-291">Groter</span><span class="sxs-lookup"><span data-stu-id="584dc-291">Greater</span></span>
-   <span data-ttu-id="584dc-292">Heeft</span><span class="sxs-lookup"><span data-stu-id="584dc-292">Implies</span></span>
-   <span data-ttu-id="584dc-293">Logboek</span><span class="sxs-lookup"><span data-stu-id="584dc-293">Log</span></span>
-   <span data-ttu-id="584dc-294">Max.</span><span class="sxs-lookup"><span data-stu-id="584dc-294">Max</span></span>
-   <span data-ttu-id="584dc-295">Min.</span><span class="sxs-lookup"><span data-stu-id="584dc-295">Min</span></span>
-   <span data-ttu-id="584dc-296">Min</span><span class="sxs-lookup"><span data-stu-id="584dc-296">Minus</span></span>
-   <span data-ttu-id="584dc-297">Plus</span><span class="sxs-lookup"><span data-stu-id="584dc-297">Plus</span></span>
-   <span data-ttu-id="584dc-298">Vermogen</span><span class="sxs-lookup"><span data-stu-id="584dc-298">Power</span></span>
-   <span data-ttu-id="584dc-299">Tijden</span><span class="sxs-lookup"><span data-stu-id="584dc-299">Times</span></span>
-   <span data-ttu-id="584dc-300">Tijd</span><span class="sxs-lookup"><span data-stu-id="584dc-300">Slot</span></span>
-   <span data-ttu-id="584dc-301">Model</span><span class="sxs-lookup"><span data-stu-id="584dc-301">Model</span></span>
-   <span data-ttu-id="584dc-302">Beslissing</span><span class="sxs-lookup"><span data-stu-id="584dc-302">Decision</span></span>
-   <span data-ttu-id="584dc-303">Doel</span><span class="sxs-lookup"><span data-stu-id="584dc-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="584dc-304">Zie ook</span><span class="sxs-lookup"><span data-stu-id="584dc-304">See also</span></span>
--------

<span data-ttu-id="584dc-305">[Een expressiebeperking maken (Taakbegeleiding)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span><span class="sxs-lookup"><span data-stu-id="584dc-305">[Create an expression constraint (Task guide)(/dynamics365/unified-operations/supply-chain/pim/tasks/add-expression-constraint-product-configuration-model)</span></span>

[<span data-ttu-id="584dc-306">Een berekening toevoegen aan een productconfiguratiemodel (taakbegeleider)</span><span class="sxs-lookup"><span data-stu-id="584dc-306">Add a calculation to a product configuration model (Task guide)</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/add-calculation-product-configuration-model)




