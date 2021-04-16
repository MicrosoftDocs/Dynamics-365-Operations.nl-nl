---
title: Berekeningen van productconfiguratiemodel
description: In dit onderwerp wordt beschreven hoe u berekeningen maakt voor kenmerken in een productconfiguratiemodel
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829613"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="268d6-103">Berekeningen van productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="268d6-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="268d6-104">In dit onderwerp wordt beschreven hoe u berekeningen maakt voor kenmerken in een productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="268d6-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="268d6-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="268d6-105">Prerequisites</span></span>

<span data-ttu-id="268d6-106">Berekeningen worden gebruikt in een productconfiguratiemodel om de configuratiewaarden voor een product te berekenen.</span><span class="sxs-lookup"><span data-stu-id="268d6-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="268d6-107">Voordat u begint met het instellen van berekeningen, moet het bijbehorende productconfiguratiemodel bestaan.</span><span class="sxs-lookup"><span data-stu-id="268d6-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="268d6-108">Zie [Een productconfiguratiemodel instellen](set-up-maintain-product-configuration-model.md) voor een overzicht van het installatieproces voor configuratiemodellen en de bijbehorende taken.</span><span class="sxs-lookup"><span data-stu-id="268d6-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="268d6-109">Een berekening maken</span><span class="sxs-lookup"><span data-stu-id="268d6-109">Create a calculation</span></span>

<span data-ttu-id="268d6-110">Een berekening bestaat uit een expressie en een doelkenmerk.</span><span class="sxs-lookup"><span data-stu-id="268d6-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="268d6-111">Zie [Veelgestelde vragen over berekeningen voor productonfiguratiemodellen](calculate-product-configuration-models.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="268d6-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="268d6-112">Volg deze stappen om een berekening voor een bestaand productmodel te maken.</span><span class="sxs-lookup"><span data-stu-id="268d6-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="268d6-113">Ga naar **Productgegevensbeheer \> Algemeen \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="268d6-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="268d6-114">Open een productconfiguratiemodel en selecteer vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="268d6-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="268d6-115">Selecteer op het sneltabblad **Berekeningen** de optie **Toevoegen** om een berekening toe te voegen en stel vervolgens de onderstaande velden in:</span><span class="sxs-lookup"><span data-stu-id="268d6-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="268d6-116">**Naam**: voer een naam in voor de berekening.</span><span class="sxs-lookup"><span data-stu-id="268d6-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="268d6-117">**Beschrijving**: voer een beschrijving van de berekening in.</span><span class="sxs-lookup"><span data-stu-id="268d6-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="268d6-118">**Doelkenmerk**: selecteer het kenmerk waarvoor u de berekening maakt.</span><span class="sxs-lookup"><span data-stu-id="268d6-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="268d6-119">Selecteer **Expressie bewerken**.</span><span class="sxs-lookup"><span data-stu-id="268d6-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="268d6-120">Voeg in het dialoogvenster **Een berekening invoeren** de vereiste kenmerken, operatoren en waarden toe aan de expressie.</span><span class="sxs-lookup"><span data-stu-id="268d6-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="268d6-121">Zie [Expressiebeperkingen en tabelbeperkingen in productconfiguratiemodellen](expression-constraints-table-constraints-product-configuration-models.md) voor meer informatie over hoe u kunt werken met deze elementen.</span><span class="sxs-lookup"><span data-stu-id="268d6-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="268d6-122">Wanneer uw expressie gereed is, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="268d6-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="268d6-123">Voorbeelden van berekening</span><span class="sxs-lookup"><span data-stu-id="268d6-123">Calculation examples</span></span>

<span data-ttu-id="268d6-124">In deze sectie vindt u enkele voorbeelden die laten zien hoe berekeningen werken.</span><span class="sxs-lookup"><span data-stu-id="268d6-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="268d6-125">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="268d6-125">Example 1</span></span>

<span data-ttu-id="268d6-126">Het doelkenmerk s Booleaans en de berekening gebruikt de volgende voorwaardelijke expressie:</span><span class="sxs-lookup"><span data-stu-id="268d6-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="268d6-127">Deze expressie retourneert een waarde van *True* naar het doelkenmerk als `decimalAttribute2` groter is dan of gelijk is aan `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="268d6-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="268d6-128">Anders wordt de waarde *False* geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="268d6-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="268d6-129">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="268d6-129">Example 2</span></span>

<span data-ttu-id="268d6-130">In dit voorbeeld wordt het tekstkenmerk `textFixedList` gebruikt als doelkenmerk.</span><span class="sxs-lookup"><span data-stu-id="268d6-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="268d6-131">Dit kenmerk bevat de volgende vaste lijst.</span><span class="sxs-lookup"><span data-stu-id="268d6-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="268d6-132">Waarde</span><span class="sxs-lookup"><span data-stu-id="268d6-132">Value</span></span> | <span data-ttu-id="268d6-133">Oplossingswaarde</span><span class="sxs-lookup"><span data-stu-id="268d6-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="268d6-134">V</span><span class="sxs-lookup"><span data-stu-id="268d6-134">A</span></span> | <span data-ttu-id="268d6-135">1a</span><span class="sxs-lookup"><span data-stu-id="268d6-135">1a</span></span> |
| <span data-ttu-id="268d6-136">B</span><span class="sxs-lookup"><span data-stu-id="268d6-136">B</span></span> | <span data-ttu-id="268d6-137">2b</span><span class="sxs-lookup"><span data-stu-id="268d6-137">2b</span></span> |
| <span data-ttu-id="268d6-138">C</span><span class="sxs-lookup"><span data-stu-id="268d6-138">C</span></span> | <span data-ttu-id="268d6-139">2c</span><span class="sxs-lookup"><span data-stu-id="268d6-139">2c</span></span> |

<span data-ttu-id="268d6-140">In de volgende schermopname ziet u hoe de instellingen voor dit kenmerk er mogelijk uitzien in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="268d6-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="268d6-141">![Instellingen voor kenmerktypen, bijvoorbeeld 2](media/model-calculations-example2.png "Instellingen voor kenmerktypen, bijvoorbeeld 2")</span><span class="sxs-lookup"><span data-stu-id="268d6-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="268d6-142">Het kenmerk wordt gebruikt in de volgende voorwaardelijke instructie:</span><span class="sxs-lookup"><span data-stu-id="268d6-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="268d6-143">Als `integerAttribute` kleiner is dan 150, retourneert deze instructie de tekstwaarde van de eerste record in de vaste lijst, *A*. Anders retourneert het de tekstwaarde van de derde record in de vaste lijst, *C*.</span><span class="sxs-lookup"><span data-stu-id="268d6-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="268d6-144">De vaste lijst is gelijk aan een op nul gebaseerde opsomming (enum) en de waarden ervan worden geopend met de juiste geheel getalwaarde.</span><span class="sxs-lookup"><span data-stu-id="268d6-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="268d6-145">Daarom wordt de eerste vaste lijstwaarde (*A*) gekoppeld aan *0*, wordt de tweede waarde (*B*) gekoppeld aan *1* en wordt de derde waarde (*C*) gekoppeld aan *2*.</span><span class="sxs-lookup"><span data-stu-id="268d6-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="268d6-146">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="268d6-146">Example 3</span></span>

<span data-ttu-id="268d6-147">In dit voorbeeld wordt het doelkenmerk `textFixedList` uit het vorige voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="268d6-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="268d6-148">Het maakt ook gebruik van een ander tekstkenmerk, `textAttribute`, dat de volgende vaste lijst bevat.</span><span class="sxs-lookup"><span data-stu-id="268d6-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="268d6-149">Waarde</span><span class="sxs-lookup"><span data-stu-id="268d6-149">Value</span></span> | <span data-ttu-id="268d6-150">Oplossingswaarde</span><span class="sxs-lookup"><span data-stu-id="268d6-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="268d6-151">AA</span><span class="sxs-lookup"><span data-stu-id="268d6-151">AA</span></span> | <span data-ttu-id="268d6-152">1aa</span><span class="sxs-lookup"><span data-stu-id="268d6-152">1aa</span></span> |
| <span data-ttu-id="268d6-153">BB</span><span class="sxs-lookup"><span data-stu-id="268d6-153">BB</span></span> | <span data-ttu-id="268d6-154">2bb</span><span class="sxs-lookup"><span data-stu-id="268d6-154">2bb</span></span> |

<span data-ttu-id="268d6-155">In de volgende schermopname ziet u hoe de instellingen voor dit kenmerk er mogelijk uitzien in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="268d6-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="268d6-156">![Instellingen voor kenmerktypen, bijvoorbeeld 3](media/model-calculations-example3.png "Instellingen voor kenmerktypen, bijvoorbeeld 3")</span><span class="sxs-lookup"><span data-stu-id="268d6-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="268d6-157">De waarde voor het kenmerk `textFixedList` wordt berekend met behulp van de volgende voorwaardelijke instructie:</span><span class="sxs-lookup"><span data-stu-id="268d6-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="268d6-158">Als de waarde `textAttribute` een oplosserwaarde heeft die gelijk is aan *1aa*, retourneert deze expressie de tekstwaarde van de eerste record in de vaste lijst voor `textFixedList`, *A*. Anders retourneert het de tekstwaarde van de derde record in de vaste lijst voor `textFixedList`, *C*.</span><span class="sxs-lookup"><span data-stu-id="268d6-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="268d6-159">De voorwaardelijke instructie moet de oplosserwaarde van het kenmerk gebruiken.</span><span class="sxs-lookup"><span data-stu-id="268d6-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="268d6-160">Alleen tekstkenmerken met een vaste lijst kunnen worden gebruikt in berekeningen.</span><span class="sxs-lookup"><span data-stu-id="268d6-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="268d6-161">Zie ook</span><span class="sxs-lookup"><span data-stu-id="268d6-161">See also</span></span>

- [<span data-ttu-id="268d6-162">Berekeningen voor productconfiguratiemodellen: veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="268d6-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="268d6-163">Een expressiebeperking toevoegen aan een productconfiguratiemodel</span><span class="sxs-lookup"><span data-stu-id="268d6-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="268d6-164">Overzicht productconfiguratiemodellen</span><span class="sxs-lookup"><span data-stu-id="268d6-164">Product configuration models overview</span></span>](product-configuration-models.md)
