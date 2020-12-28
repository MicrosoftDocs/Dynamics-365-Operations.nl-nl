---
title: Materiaalverbruik berekenen
description: Dit artikel bevat informatie over verschillende opties met betrekking tot de berekening van materiaalverbruik.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f58365278200344169b93658e9c92dea2bc4f18f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425510"
---
# <a name="calculate-material-consumption"></a><span data-ttu-id="0da96-103">Materiaalverbruik berekenen</span><span class="sxs-lookup"><span data-stu-id="0da96-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0da96-104">Dit artikel bevat informatie over verschillende opties met betrekking tot de berekening van materiaalverbruik.</span><span class="sxs-lookup"><span data-stu-id="0da96-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="0da96-105">De volgende opties die aan de berekening van het materiaalverbruik zijn gerelateerd zijn beschikbaar op de tabbladen **Instellen** en **Stapverbruik** op het sneltabbblad **Regeldetails** van de pagina **Stuklijst**.</span><span class="sxs-lookup"><span data-stu-id="0da96-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="0da96-106">Variabel en constant verbruik</span><span class="sxs-lookup"><span data-stu-id="0da96-106">Variable and constant consumption</span></span>
<span data-ttu-id="0da96-107">In het veld **Verbruik** kunt u aangeven of verbruik moet worden berekend als een constante of een variabele hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="0da96-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="0da96-108">Selecteer **Constante** als een vaste hoeveelheid of een vast volume nodig is voor de productie, ongeacht de hoeveelheid die wordt geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="0da96-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="0da96-109">Selecteer, **Variabel**, oftewel de standaardinstelling, als de vereiste hoeveelheid materiaal in de eindproducten proportioneel is aan het aantal geproduceerde eindproducten.</span><span class="sxs-lookup"><span data-stu-id="0da96-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="0da96-110">Verbruik berekenen op basis van een formule</span><span class="sxs-lookup"><span data-stu-id="0da96-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="0da96-111">In het veld **Formule** kunt u verschillende formules instellen voor het berekenen van materiaalverbruik.</span><span class="sxs-lookup"><span data-stu-id="0da96-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="0da96-112">Als u de standaardwaarde gebruikt, **Standaard**, wordt het verbruik niet berekend op basis van een formule.</span><span class="sxs-lookup"><span data-stu-id="0da96-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="0da96-113">De volgende formules werken samen met de velden **Hoogte**, **Breedte**, **Diepte**, **Dichtheid** en **Constant**:</span><span class="sxs-lookup"><span data-stu-id="0da96-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="0da96-114">Hoogte \* constante</span><span class="sxs-lookup"><span data-stu-id="0da96-114">Height \* Constant</span></span>
-   <span data-ttu-id="0da96-115">Hoogte \* breedte \* constante</span><span class="sxs-lookup"><span data-stu-id="0da96-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="0da96-116">Hoogte \* breedte \* diepte \* constante</span><span class="sxs-lookup"><span data-stu-id="0da96-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="0da96-117">(Hoogte \* breedte \* diepte/dichtheid) \* constante</span><span class="sxs-lookup"><span data-stu-id="0da96-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="0da96-118">Veelvouden afronden</span><span class="sxs-lookup"><span data-stu-id="0da96-118">Rounding up and multiples</span></span>
<span data-ttu-id="0da96-119">Samen kunt u met de velden **Naar boven afronden** en **Veelvouden** de waarde voor het materiaalverbruik naar boven afronden.</span><span class="sxs-lookup"><span data-stu-id="0da96-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="0da96-120">Zo kunt u bijvoorbeeld de waarde naar boven afronden op basis van de materiaalverwerkingseenheid waarin de grondstof voor productie wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="0da96-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="0da96-121">De volgende opties zijn beschikbaar in het veld **Naar boven afronden**: **Hoeveelheid**, **Afmeting** en **Verbruik**.</span><span class="sxs-lookup"><span data-stu-id="0da96-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="0da96-122">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0da96-122">Quantity</span></span>

<span data-ttu-id="0da96-123">Als u **Hoeveelheid** selecteert als mechanisme voor naar boven afronden, moet de hoeveelheid een veelvoud zijn van de opgegeven hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="0da96-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="0da96-124">Als er bijvoorbeeld gehele getallen vereist zijn, selecteert u **1** in het veld **Veelvouden**.</span><span class="sxs-lookup"><span data-stu-id="0da96-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="0da96-125">Getallen worden vervolgens naar boven afgerond tot een hoeveelheid die deelbaar is door 1.</span><span class="sxs-lookup"><span data-stu-id="0da96-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="0da96-126">Meting</span><span class="sxs-lookup"><span data-stu-id="0da96-126">Measurement</span></span>

<span data-ttu-id="0da96-127">Doorgaans selecteert u **Afmeting** als mechanisme voor naar boven afronden wanneer de grondstof specifieke dimensies heeft.</span><span class="sxs-lookup"><span data-stu-id="0da96-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="0da96-128">Stel dat een metalen buis van 2 meter lengte is vereist voor een eindproduct en de metalen buis wordt opgeslagen in lengten van 4,5 meter.</span><span class="sxs-lookup"><span data-stu-id="0da96-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="0da96-129">In dit geval kan het mechanisme voor naar boven afronden **Afmeting** worden gebruikt om te berekenen hoeveel metalen buizen nodig zijn om een bepaald aantal stuks van het eindproduct te vervaardigen.</span><span class="sxs-lookup"><span data-stu-id="0da96-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="0da96-130">In dit voorbeeld is het veld **Formule** ingesteld op **Hoogte \* constante**.</span><span class="sxs-lookup"><span data-stu-id="0da96-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="0da96-131">Het veld **Hoogte** is ingesteld op **2** om de lengte aan te geven van de buis die vereist is voor het eindproduct.</span><span class="sxs-lookup"><span data-stu-id="0da96-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="0da96-132">Het veld **Veelvoud** wordt ingesteld op **4,5** om aan te geven dat de buis in lengten van 4,5 meter wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="0da96-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="0da96-133">Hier volgt de berekening:</span><span class="sxs-lookup"><span data-stu-id="0da96-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="0da96-134">Aantal veelvouden dat is vereist voor 10 stuks van het eindproduct: 10 ÷ 2 = 5 stuks</span><span class="sxs-lookup"><span data-stu-id="0da96-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="0da96-135">Totaal verbruik: 4,5 x 5 = 22,5 meter metalen buis</span><span class="sxs-lookup"><span data-stu-id="0da96-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="0da96-136">Er wordt aangenomen dat 0,5 meter buis als afval overblijft voor elke vijf stuks buizen die worden verbruikt.</span><span class="sxs-lookup"><span data-stu-id="0da96-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="0da96-137">Verbruik</span><span class="sxs-lookup"><span data-stu-id="0da96-137">Consumption</span></span>

<span data-ttu-id="0da96-138">Doorgaans selecteert u **Verbruik** als mechanisme voor naar boven afronden wanneer grondstoffen moeten worden verzameld in gehele hoeveelheden van een specifieke materiaalverwerkingseenheid van het product.</span><span class="sxs-lookup"><span data-stu-id="0da96-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="0da96-139">Zo worden bijvoorbeeld 2 liter verf gebruikt om één eindproduct te maken, en de verf wordt verzameld in blikken van 25 liter.</span><span class="sxs-lookup"><span data-stu-id="0da96-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="0da96-140">In dit geval kan het mechanisme voor afronding naar boven **Verbruik** worden gebruikt om het verbruik af te ronden op gehele getallen voor blikken van 25 liter.</span><span class="sxs-lookup"><span data-stu-id="0da96-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="0da96-141">Hier volgt de berekening voor de hoeveelheid verf die is vereist als 180 stuks van het eindproduct moeten worden vervaardigd:</span><span class="sxs-lookup"><span data-stu-id="0da96-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="0da96-142">Vereiste verf, exclusief uitval: 180 x 2 = 360 liter</span><span class="sxs-lookup"><span data-stu-id="0da96-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="0da96-143">Aantal blikken: 360 ÷ 25 = 14,4, hetgeen wordt afgerond tot 15</span><span class="sxs-lookup"><span data-stu-id="0da96-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="0da96-144">Vereiste verf, inclusief uitval: 15 x 25 = 375 liter</span><span class="sxs-lookup"><span data-stu-id="0da96-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="0da96-145">Stapverbruik</span><span class="sxs-lookup"><span data-stu-id="0da96-145">Step consumption</span></span>
<span data-ttu-id="0da96-146">Stapverbruik wordt gebruikt voor het berekenen van het constante verbruik in hoeveelheidsintervallen.</span><span class="sxs-lookup"><span data-stu-id="0da96-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="0da96-147">Als u **Stapverbruik** selecteert in het veld **Formule** op het tabblad **Instellingen**, kunt u informatie over de stappen toevoegen op het tabblad **Stapverbruik**. De vaste verbruikte hoeveelheid kan worden ingesteld in intervallen van de geproduceerde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="0da96-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="0da96-148">Stapverbruik wordt bijvoorbeeld,ingesteld op de wijze die in de volgende tabel wordt aangegeven.</span><span class="sxs-lookup"><span data-stu-id="0da96-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="0da96-149">Van serie</span><span class="sxs-lookup"><span data-stu-id="0da96-149">From series</span></span> | <span data-ttu-id="0da96-150">Hoeveelheid</span><span class="sxs-lookup"><span data-stu-id="0da96-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="0da96-151">0,00</span><span class="sxs-lookup"><span data-stu-id="0da96-151">0.00</span></span>        | <span data-ttu-id="0da96-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="0da96-152">10.0000</span></span>  |
| <span data-ttu-id="0da96-153">100,00</span><span class="sxs-lookup"><span data-stu-id="0da96-153">100.00</span></span>      | <span data-ttu-id="0da96-154">20,0000</span><span class="sxs-lookup"><span data-stu-id="0da96-154">20.0000</span></span>  |
| <span data-ttu-id="0da96-155">200,00</span><span class="sxs-lookup"><span data-stu-id="0da96-155">200.00</span></span>      | <span data-ttu-id="0da96-156">40,0000</span><span class="sxs-lookup"><span data-stu-id="0da96-156">40.0000</span></span>  |

<span data-ttu-id="0da96-157">De hoeveelheid van de stuklijst (BOM) is 1 en productiehoeveelheid is 110.</span><span class="sxs-lookup"><span data-stu-id="0da96-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="0da96-158">De formule voor het verbruik is Van reeks (hoeveelheid) = Verbruik.</span><span class="sxs-lookup"><span data-stu-id="0da96-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="0da96-159">Omdat de productiehoeveelheid 110 is, valt deze binnen de "Van 100 reeks".</span><span class="sxs-lookup"><span data-stu-id="0da96-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="0da96-160">Daarom is de hoeveelheid 20.</span><span class="sxs-lookup"><span data-stu-id="0da96-160">Therefore, the quantity is 20.</span></span>



