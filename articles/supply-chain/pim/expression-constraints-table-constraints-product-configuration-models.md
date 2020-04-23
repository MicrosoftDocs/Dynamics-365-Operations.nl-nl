---
title: Expressiebeperkingen en tabelbeperkingen in productconfiguratiemodellen
description: Dit onderwerp beschrijft het gebruik van expressiebeperkingen en tabelbeperkingen. U gebruikt beperkingen om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert. U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d85d10113e7cc4e95a25efe7fee6d1f23990694
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208458"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="1b0b7-105">Expressiebeperkingen en tabelbeperkingen in productconfiguratiemodellen</span><span class="sxs-lookup"><span data-stu-id="1b0b7-105">Expression constraints and table constraints in product configuration models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b0b7-106">Dit onderwerp beschrijft het gebruik van expressiebeperkingen en tabelbeperkingen.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="1b0b7-107">U gebruikt beperkingen om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="1b0b7-108">U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="1b0b7-109">Beperkingen worden gebruikt om de kenmerkwaarden te beheren die u kunt gebruiken wanneer u producten voor een verkooporder, verkoopofferte, inkooporder, of een productieorder configureert.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="1b0b7-110">U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="1b0b7-111">Wat zijn expressiebeperkingen?</span><span class="sxs-lookup"><span data-stu-id="1b0b7-111">What are expression constraints?</span></span>
<span data-ttu-id="1b0b7-112">Expressiebeperkingen worden gekenmerkt door een expressie met rekenkundige en Booleaanse operatoren en functies.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="1b0b7-113">Een expressiebeperking wordt geschreven voor een bepaald onderdeel in een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="1b0b7-114">De beperking kan niet worden hergebruikt door of gedeeld met een ander onderdeel.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="1b0b7-115">Expressiebeperkingen voor een onderdeel kunnen echter verwijzen naar kenmerken van subonderdelen van het onderdeel.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="1b0b7-116">Wat zijn tabelbeperkingen?</span><span class="sxs-lookup"><span data-stu-id="1b0b7-116">What are table constraints?</span></span>
<span data-ttu-id="1b0b7-117">Tabelbeperkingen maken een lijst met de combinaties van waarden die zijn toegestaan voor kenmerken wanneer u een product configureert.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="1b0b7-118">De definities van tabelbeperkingen kunnen algemeen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="1b0b7-119">Wanneer u een tabelbeperking voor een component maakt in een productconfiguratiemodel, selecteert u een definitie voor de tabelbeperking.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="1b0b7-120">Om de combinaties te maken die worden toegestaan, voegt u kenmerken van specifieke typen aan de onderdelen toe.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="1b0b7-121">Elk kenmerktype heeft een specifieke waarde.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="1b0b7-122">Voorbeeld van een tabelbeperking.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-122">Example of a table constraint</span></span>

<span data-ttu-id="1b0b7-123">Dit voorbeeld toont hoe u de configuratie van een speaker tot specifieke afwerkingen van de behuizingen en voorkanten kunt beperken.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="1b0b7-124">De eerste tabel laat de afwerkingen van de behuizingen en voorkanten zien die algemeen beschikbaar zijn voor configuratie.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="1b0b7-125">De waarden zijn gedefinieerd voor **Afwerking behuizing** en **Voorgrill**.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="1b0b7-126">Kenmerktype</span><span class="sxs-lookup"><span data-stu-id="1b0b7-126">Attribute type</span></span> | <span data-ttu-id="1b0b7-127">Waarden</span><span class="sxs-lookup"><span data-stu-id="1b0b7-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="1b0b7-128">Afwerking behuizing</span><span class="sxs-lookup"><span data-stu-id="1b0b7-128">Cabinet finish</span></span> | <span data-ttu-id="1b0b7-129">Zwart, Eiken, Rozenhout, Wit</span><span class="sxs-lookup"><span data-stu-id="1b0b7-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="1b0b7-130">Voorgrill</span><span class="sxs-lookup"><span data-stu-id="1b0b7-130">Front grill</span></span>    | <span data-ttu-id="1b0b7-131">Zwart, Metaal, Wit</span><span class="sxs-lookup"><span data-stu-id="1b0b7-131">Black, Metal, White</span></span>         |

<span data-ttu-id="1b0b7-132">De volgende tabel geeft de combinaties weer die door de tabelbeperking **Kleur en afwerking** zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="1b0b7-133">Door deze tabelbeperking te gebruiken, kunt u een speaker configureren met een eiken afwerking en een zwarte grill, een rozenhouten afwerking en een witte grill, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="1b0b7-134">Voltooien</span><span class="sxs-lookup"><span data-stu-id="1b0b7-134">Finish</span></span>         | <span data-ttu-id="1b0b7-135">Grill</span><span class="sxs-lookup"><span data-stu-id="1b0b7-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="1b0b7-136">Eiken</span><span class="sxs-lookup"><span data-stu-id="1b0b7-136">Oak</span></span>            | <span data-ttu-id="1b0b7-137">Zwart</span><span class="sxs-lookup"><span data-stu-id="1b0b7-137">Black</span></span>                       |
| <span data-ttu-id="1b0b7-138">Rozenhout</span><span class="sxs-lookup"><span data-stu-id="1b0b7-138">Rosewood</span></span>       | <span data-ttu-id="1b0b7-139">Wit</span><span class="sxs-lookup"><span data-stu-id="1b0b7-139">White</span></span>                       |
| <span data-ttu-id="1b0b7-140">Wit</span><span class="sxs-lookup"><span data-stu-id="1b0b7-140">White</span></span>          | <span data-ttu-id="1b0b7-141">Zwart</span><span class="sxs-lookup"><span data-stu-id="1b0b7-141">Black</span></span>                       |
| <span data-ttu-id="1b0b7-142">Wit</span><span class="sxs-lookup"><span data-stu-id="1b0b7-142">White</span></span>          | <span data-ttu-id="1b0b7-143">Wit</span><span class="sxs-lookup"><span data-stu-id="1b0b7-143">White</span></span>                       |
| <span data-ttu-id="1b0b7-144">Zwart</span><span class="sxs-lookup"><span data-stu-id="1b0b7-144">Black</span></span>          | <span data-ttu-id="1b0b7-145">Zwart</span><span class="sxs-lookup"><span data-stu-id="1b0b7-145">Black</span></span>                       |
| <span data-ttu-id="1b0b7-146">Zwart</span><span class="sxs-lookup"><span data-stu-id="1b0b7-146">Black</span></span>          | <span data-ttu-id="1b0b7-147">Metaal</span><span class="sxs-lookup"><span data-stu-id="1b0b7-147">Metal</span></span>                       | 

<span data-ttu-id="1b0b7-148">U kunt door het systeem gedefinieerde en door de gebruiker gedefinieerde tabelbeperkingen maken.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="1b0b7-149">Voor meer informatie, zie [Door het systeem gedefinieerde en door gebruiker gedefinieerde tabelbeperkingen](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="1b0b7-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="1b0b7-150">Welke syntaxis moet worden gebruikt om beperkingen te schrijven?</span><span class="sxs-lookup"><span data-stu-id="1b0b7-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="1b0b7-151">Gebruik de OML-syntaxis (Optimization Modeling Language) wanneer u beperkingen opstelt.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="1b0b7-152">Microsoft Solver Foundation-beperkingsoplosser wordt gebruikt om de beperkingen op te lossen.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="1b0b7-153">Moet ik tabelbeperkingen of expressiebeperkingen gebruiken?</span><span class="sxs-lookup"><span data-stu-id="1b0b7-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="1b0b7-154">U kunt expressiebeperkingen of tabelbeperkingen gebruiken, afhankelijk van hoe u de beperkingen wenst te maken.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="1b0b7-155">U maakt een tabelbeperking als matrix, terwijl een expressiebeperking een afzonderlijke statement is.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="1b0b7-156">Wanneer u een product configureert, is het niet van belang welk type beperking wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="1b0b7-157">In het volgende voorbeeld kunt u zien hoe de twee methoden verschillen.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="1b0b7-158">Wanneer u een product met de volgende beperkingsinstellingen configureert, worden deze combinaties toegestaan:</span><span class="sxs-lookup"><span data-stu-id="1b0b7-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="1b0b7-159">Een product in de kleur Zwart, in grootte 30 of 50</span><span class="sxs-lookup"><span data-stu-id="1b0b7-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="1b0b7-160">Een product in de kleur Rood, in grootte 20</span><span class="sxs-lookup"><span data-stu-id="1b0b7-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="1b0b7-161">Tabelbeperkingsinstelling</span><span class="sxs-lookup"><span data-stu-id="1b0b7-161">Table constraint setup</span></span>

| <span data-ttu-id="1b0b7-162">Kleur</span><span class="sxs-lookup"><span data-stu-id="1b0b7-162">Color</span></span> | <span data-ttu-id="1b0b7-163">Grootte</span><span class="sxs-lookup"><span data-stu-id="1b0b7-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="1b0b7-164">Zwart</span><span class="sxs-lookup"><span data-stu-id="1b0b7-164">Black</span></span> | <span data-ttu-id="1b0b7-165">30</span><span class="sxs-lookup"><span data-stu-id="1b0b7-165">30</span></span>   |
| <span data-ttu-id="1b0b7-166">Zwart</span><span class="sxs-lookup"><span data-stu-id="1b0b7-166">Black</span></span> | <span data-ttu-id="1b0b7-167">50</span><span class="sxs-lookup"><span data-stu-id="1b0b7-167">50</span></span>   |
| <span data-ttu-id="1b0b7-168">Rood</span><span class="sxs-lookup"><span data-stu-id="1b0b7-168">Red</span></span>   | <span data-ttu-id="1b0b7-169">20</span><span class="sxs-lookup"><span data-stu-id="1b0b7-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="1b0b7-170">Instelling expressiebeperking</span><span class="sxs-lookup"><span data-stu-id="1b0b7-170">Expression constraint setup</span></span>

<span data-ttu-id="1b0b7-171">(Kleur == "Zwart" & (afmeting == "30" | afmeting == "50")) | (kleur == "Rood" & afmeting = "20")</span><span class="sxs-lookup"><span data-stu-id="1b0b7-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="1b0b7-172">Moet ik operators gebruiken of tussenvoegselaantekening gebruiken wanneer ik expressiebeperkingen schrijf?</span><span class="sxs-lookup"><span data-stu-id="1b0b7-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="1b0b7-173">U kunt een expressiebeperking opstellen met behulp van de beschikbare voorvoegseloperatoren of met tussenvoegselnotatie.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="1b0b7-174">Voor de operatoren **Min**, **Max**, en **Abs** kunt u de tussenvoegselnotatie niet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="1b0b7-175">Deze operatoren zijn opgenomen als standaardoperatoren in de meeste programmeertalen.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="1b0b7-176">Welke operators en tussenvoegselnotatie kan ik gebruiken wanneer ik expressiebeperkingen schrijf?</span><span class="sxs-lookup"><span data-stu-id="1b0b7-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="1b0b7-177">In de volgende tabel worden de operatoren en de tussenvoegselnotatie vermeld die u kunt gebruiken voor het schrijven van een expressiebeperking voor een onderdeel van een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="1b0b7-178">In de voorbeelden in de eerste tabel kunt u zien hoe u een expressie maakt door tussenvoegselnotaties of operators te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b0b7-179">Operator</span><span class="sxs-lookup"><span data-stu-id="1b0b7-179">Operator</span></span></th>
<th><span data-ttu-id="1b0b7-180">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="1b0b7-180">Description</span></span></th>
<th><span data-ttu-id="1b0b7-181">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="1b0b7-181">Syntax</span></span></th>
<th><span data-ttu-id="1b0b7-182">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1b0b7-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b0b7-183">Heeft</span><span class="sxs-lookup"><span data-stu-id="1b0b7-183">Implies</span></span></td>
<td><span data-ttu-id="1b0b7-184">Dit is waar als de eerste voorwaarde onwaar is, de tweede voorwaarde waar, of beide.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="1b0b7-185">Heeft[a, b], tussenvoegselaantekening: a -: b</span><span class="sxs-lookup"><span data-stu-id="1b0b7-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="1b0b7-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="1b0b7-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="1b0b7-187"><strong>Tussenvoegselnotatie:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="1b0b7-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b0b7-188">En</span><span class="sxs-lookup"><span data-stu-id="1b0b7-188">And</span></span></td>
<td><span data-ttu-id="1b0b7-189">Dit is alleen waar als alle voorwaarden waar zijn.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="1b0b7-190">Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>Waar</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="1b0b7-191">And[args], tussenvoegsel: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="1b0b7-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="1b0b7-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="1b0b7-193"><strong>Tussenvoegselnotatie:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="1b0b7-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b0b7-194">Of</span><span class="sxs-lookup"><span data-stu-id="1b0b7-194">Or</span></span></td>
<td><span data-ttu-id="1b0b7-195">Dit is waar als een van de voorwaarden waar is.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-195">This is true if any condition is true.</span></span> <span data-ttu-id="1b0b7-196">Als het aantal condities 0 is (nul), is het product <strong>Onwaar</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="1b0b7-197">Or[args], tussenvoegsel: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="1b0b7-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="1b0b7-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="1b0b7-199"><strong>Tussenvoegselnotatie:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="1b0b7-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b0b7-200">Plus</span><span class="sxs-lookup"><span data-stu-id="1b0b7-200">Plus</span></span></td>
<td><span data-ttu-id="1b0b7-201">Dit is de som van de voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-201">This sums its conditions.</span></span> <span data-ttu-id="1b0b7-202">Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="1b0b7-203">Plus[args], tussenvoegsel: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="1b0b7-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="1b0b7-205"><strong>Tussenvoegselnotatie:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b0b7-206">Min</span><span class="sxs-lookup"><span data-stu-id="1b0b7-206">Minus</span></span></td>
<td><span data-ttu-id="1b0b7-207">Het argument wordt genegeerd.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-207">This negates its argument.</span></span> <span data-ttu-id="1b0b7-208">Het moet precies één voorwaarde hebben.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="1b0b7-209">Minus[expr], tussenvoegselaantekening: -expr</span><span class="sxs-lookup"><span data-stu-id="1b0b7-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="1b0b7-210"><strong>Operator:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="1b0b7-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="1b0b7-211"><strong>Tussenvoegselnotatie:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="1b0b7-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b0b7-212">Abs</span><span class="sxs-lookup"><span data-stu-id="1b0b7-212">Abs</span></span></td>
<td><span data-ttu-id="1b0b7-213">Hiervoor is de absolute waarde van de voorwaarde vereist.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="1b0b7-214">Het moet precies één voorwaarde hebben.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="1b0b7-215">Abs[expr]</span><span class="sxs-lookup"><span data-stu-id="1b0b7-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="1b0b7-216"><strong>Operator:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="1b0b7-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b0b7-217">Tijden</span><span class="sxs-lookup"><span data-stu-id="1b0b7-217">Times</span></span></td>
<td><span data-ttu-id="1b0b7-218">Hiervoor is het product van de voorwaarden vereist.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-218">This takes the product of its conditions.</span></span> <span data-ttu-id="1b0b7-219">Als het aantal voorwaarden 0 (nul) is, is het resultaat <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="1b0b7-220">Times[args], tussenvoegsel: a \* b \* ... \* z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-220">Times[args], infix: a \* b \* ... \* z</span></span></td>
<td><ul>
<li><span data-ttu-id="1b0b7-221"><strong>Operator:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="1b0b7-222"><strong>Tussenvoegselnotatie:</strong> x \* y \* 2 == z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-222"><strong>Infix notation:</strong> x \* y \* 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b0b7-223">Vermogen</span><span class="sxs-lookup"><span data-stu-id="1b0b7-223">Power</span></span></td>
<td><span data-ttu-id="1b0b7-224">Hiervoor is een exponentiële waarde vereist.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-224">This takes an exponential.</span></span> <span data-ttu-id="1b0b7-225">Hiermee wordt machtsverheffen van rechts naar links toegepast.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="1b0b7-226">(Dat wil zeggen dat het rechts associatief is) Hierdoor is <strong>Power[a, b, c]</strong> gelijk aan <strong>Power[a, Power[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-226">(In other words, it&#39;s right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="1b0b7-227"><strong>Power</strong> kan alleen worden gebruikt als de exponent een positieve constante is.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="1b0b7-228">Power[args], tussenvoegsel: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="1b0b7-229"><strong>Operator:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="1b0b7-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="1b0b7-230"><strong>Tussenvoegselnotatie:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="1b0b7-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b0b7-231">Max.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-231">Max</span></span></td>
<td><span data-ttu-id="1b0b7-232">Dit levert de grootste voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-232">This produces the largest condition.</span></span> <span data-ttu-id="1b0b7-233">Als het aantal condities 0 is (nul), resulteert dit in <strong>Oneindigheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="1b0b7-234">Max[args]</span><span class="sxs-lookup"><span data-stu-id="1b0b7-234">Max[args]</span></span></td>
<td><span data-ttu-id="1b0b7-235"><strong>Operator:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b0b7-236">Min.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-236">Min</span></span></td>
<td><span data-ttu-id="1b0b7-237">Dit levert de kleinste voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-237">This produces the smallest condition.</span></span> <span data-ttu-id="1b0b7-238">Als het aantal condities 0 is (nul), resulteert dit in <strong>Oneindigheid</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="1b0b7-239">Min[args]</span><span class="sxs-lookup"><span data-stu-id="1b0b7-239">Min[args]</span></span></td>
<td><span data-ttu-id="1b0b7-240"><strong>Operator:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b0b7-241">Niet</span><span class="sxs-lookup"><span data-stu-id="1b0b7-241">Not</span></span></td>
<td><span data-ttu-id="1b0b7-242">Dit resulteert in de logische inverse van de voorwaarde.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="1b0b7-243">Het moet precies één voorwaarde hebben.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="1b0b7-244">Niet[expr], infix: !expr</span><span class="sxs-lookup"><span data-stu-id="1b0b7-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="1b0b7-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span><span class="sxs-lookup"><span data-stu-id="1b0b7-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="1b0b7-246"><strong>Tussenvoegselnotatie:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="1b0b7-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1b0b7-247">De voorbeelden in de volgende tabel geven weer hoe een tussenvoegselnotatie moet worden geschreven.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-247">The examples in the next table show how to write infix notation.</span></span>


|  <span data-ttu-id="1b0b7-248">Infix-notatie</span><span class="sxs-lookup"><span data-stu-id="1b0b7-248">Infix notation</span></span>   |                                          <span data-ttu-id="1b0b7-249">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="1b0b7-249">Description</span></span>                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     <span data-ttu-id="1b0b7-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-250">x + y + z</span></span>     |                                           <span data-ttu-id="1b0b7-251">Optelling</span><span class="sxs-lookup"><span data-stu-id="1b0b7-251">Addition</span></span>                                            |
|    <span data-ttu-id="1b0b7-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-252">x \* y \* z</span></span>    |                                        <span data-ttu-id="1b0b7-253">Vermenigvuldigen</span><span class="sxs-lookup"><span data-stu-id="1b0b7-253">Multiplication</span></span>                                         |
|       <span data-ttu-id="1b0b7-254">x - y</span><span class="sxs-lookup"><span data-stu-id="1b0b7-254">x - y</span></span>       | <span data-ttu-id="1b0b7-255">Binair aftrekken wordt op dezelfde manier vertaald als binaire optelling waarbij er een genegeerde tweede is.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
|     <span data-ttu-id="1b0b7-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-256">x ^ y ^ z</span></span>     |                          <span data-ttu-id="1b0b7-257">Machtsverheffen met associatie naar rechts</span><span class="sxs-lookup"><span data-stu-id="1b0b7-257">Exponentiation that has right associativity</span></span>                          |
|        <span data-ttu-id="1b0b7-258">!x</span><span class="sxs-lookup"><span data-stu-id="1b0b7-258">!x</span></span>         |                                          <span data-ttu-id="1b0b7-259">Booleaans niet</span><span class="sxs-lookup"><span data-stu-id="1b0b7-259">Boolean not</span></span>                                          |
|      <span data-ttu-id="1b0b7-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="1b0b7-260">x -: y</span></span>       |                                      <span data-ttu-id="1b0b7-261">Booleaanse implicatie</span><span class="sxs-lookup"><span data-stu-id="1b0b7-261">Boolean implication</span></span>                                      |
|         <span data-ttu-id="1b0b7-262">x</span><span class="sxs-lookup"><span data-stu-id="1b0b7-262">x</span></span>         |                                               <span data-ttu-id="1b0b7-263">y</span><span class="sxs-lookup"><span data-stu-id="1b0b7-263">y</span></span>                                               |
|     <span data-ttu-id="1b0b7-264">x & y & z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-264">x & y & z</span></span>     |                                          <span data-ttu-id="1b0b7-265">Booleaans en</span><span class="sxs-lookup"><span data-stu-id="1b0b7-265">Boolean and</span></span>                                          |
|    <span data-ttu-id="1b0b7-266">x == y == z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-266">x == y == z</span></span>    |                                           <span data-ttu-id="1b0b7-267">Gelijkheid</span><span class="sxs-lookup"><span data-stu-id="1b0b7-267">Equality</span></span>                                            |
|    <span data-ttu-id="1b0b7-268">x != y != z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-268">x != y != z</span></span>    |                                           <span data-ttu-id="1b0b7-269">Afzonderlijk</span><span class="sxs-lookup"><span data-stu-id="1b0b7-269">Distinct</span></span>                                            |
|  <span data-ttu-id="1b0b7-270">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-270">x &lt; y &lt; z</span></span>  |                                           <span data-ttu-id="1b0b7-271">Kleiner dan</span><span class="sxs-lookup"><span data-stu-id="1b0b7-271">Less than</span></span>                                           |
|  <span data-ttu-id="1b0b7-272">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-272">x &gt; y &gt; z</span></span>  |                                         <span data-ttu-id="1b0b7-273">Groter dan</span><span class="sxs-lookup"><span data-stu-id="1b0b7-273">Greater than</span></span>                                          |
| <span data-ttu-id="1b0b7-274">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-274">x &lt;= y &lt;= z</span></span> |                                     <span data-ttu-id="1b0b7-275">Kleiner dan of gelijk aan</span><span class="sxs-lookup"><span data-stu-id="1b0b7-275">Less than or equal to</span></span>                                     |
| <span data-ttu-id="1b0b7-276">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="1b0b7-276">x &gt;= y &gt;= z</span></span> |                                   <span data-ttu-id="1b0b7-277">Groter dan of gelijk aan</span><span class="sxs-lookup"><span data-stu-id="1b0b7-277">Greater than or equal to</span></span>                                    |
|        <span data-ttu-id="1b0b7-278">(x)</span><span class="sxs-lookup"><span data-stu-id="1b0b7-278">(x)</span></span>        |                           <span data-ttu-id="1b0b7-279">Haakjes overschrijven standaard voorrang.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-279">Parentheses override default precedence.</span></span>                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="1b0b7-280">Waarom worden mijn expressiebeperkingen niet correct gevalideerd?</span><span class="sxs-lookup"><span data-stu-id="1b0b7-280">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="1b0b7-281">U kunt geen gereserveerde sleutelwoorden gebruiken als oplossernamen voor kenmerken, onderdelen of subonderdelen in een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-281">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span><span data-ttu-id="1b0b7-282"> Hierna vindt u een lijst met de gereserveerde woorden die u niet kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="1b0b7-282"> Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="1b0b7-283">Plafond</span><span class="sxs-lookup"><span data-stu-id="1b0b7-283">Ceiling</span></span>
-   <span data-ttu-id="1b0b7-284">Element</span><span class="sxs-lookup"><span data-stu-id="1b0b7-284">Element</span></span>
-   <span data-ttu-id="1b0b7-285">Gelijk</span><span class="sxs-lookup"><span data-stu-id="1b0b7-285">Equal</span></span>
-   <span data-ttu-id="1b0b7-286">Etage</span><span class="sxs-lookup"><span data-stu-id="1b0b7-286">Floor</span></span>
-   <span data-ttu-id="1b0b7-287">Als</span><span class="sxs-lookup"><span data-stu-id="1b0b7-287">If</span></span>
-   <span data-ttu-id="1b0b7-288">Kleiner</span><span class="sxs-lookup"><span data-stu-id="1b0b7-288">Less</span></span>
-   <span data-ttu-id="1b0b7-289">Groter</span><span class="sxs-lookup"><span data-stu-id="1b0b7-289">Greater</span></span>
-   <span data-ttu-id="1b0b7-290">Heeft</span><span class="sxs-lookup"><span data-stu-id="1b0b7-290">Implies</span></span>
-   <span data-ttu-id="1b0b7-291">Logboek</span><span class="sxs-lookup"><span data-stu-id="1b0b7-291">Log</span></span>
-   <span data-ttu-id="1b0b7-292">Max.</span><span class="sxs-lookup"><span data-stu-id="1b0b7-292">Max</span></span>
-   <span data-ttu-id="1b0b7-293">Min</span><span class="sxs-lookup"><span data-stu-id="1b0b7-293">Min</span></span>
-   <span data-ttu-id="1b0b7-294">Min</span><span class="sxs-lookup"><span data-stu-id="1b0b7-294">Minus</span></span>
-   <span data-ttu-id="1b0b7-295">Plus</span><span class="sxs-lookup"><span data-stu-id="1b0b7-295">Plus</span></span>
-   <span data-ttu-id="1b0b7-296">Vermogen</span><span class="sxs-lookup"><span data-stu-id="1b0b7-296">Power</span></span>
-   <span data-ttu-id="1b0b7-297">Tijden</span><span class="sxs-lookup"><span data-stu-id="1b0b7-297">Times</span></span>
-   <span data-ttu-id="1b0b7-298">Tijd</span><span class="sxs-lookup"><span data-stu-id="1b0b7-298">Slot</span></span>
-   <span data-ttu-id="1b0b7-299">Model</span><span class="sxs-lookup"><span data-stu-id="1b0b7-299">Model</span></span>
-   <span data-ttu-id="1b0b7-300">Beslissing</span><span class="sxs-lookup"><span data-stu-id="1b0b7-300">Decision</span></span>
-   <span data-ttu-id="1b0b7-301">Doelstelling</span><span class="sxs-lookup"><span data-stu-id="1b0b7-301">Goal</span></span>


<a name="additional-resources"></a><span data-ttu-id="1b0b7-302">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1b0b7-302">Additional resources</span></span>
--------

[<span data-ttu-id="1b0b7-303">Maak een expressiebeperking</span><span class="sxs-lookup"><span data-stu-id="1b0b7-303">Create an expression constraint</span></span>](tasks/add-expression-constraint-product-configuration-model.md)

[<span data-ttu-id="1b0b7-304">Een berekening toevoegen aan een productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="1b0b7-304">Add a calculation to a product configuration model</span></span>](tasks/add-calculation-product-configuration-model.md)



