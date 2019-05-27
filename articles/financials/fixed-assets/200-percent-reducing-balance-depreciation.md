---
title: Degressieve afschrijving van 200 procent
description: Dit artikel geeft een overzicht van de afschrijvingsmethode Degressieve afschrijving van 200 procent.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec51f9e12e31e81c56fab9e82d0fc18d45beb5e6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569308"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="9d914-103">Degressieve afschrijving van 200 procent</span><span class="sxs-lookup"><span data-stu-id="9d914-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d914-104">Dit artikel geeft een overzicht van de afschrijvingsmethode Degressieve afschrijving van 200 procent.</span><span class="sxs-lookup"><span data-stu-id="9d914-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="9d914-105">Wanneer u een profiel voor de afschrijving van vaste activa instelt en **200% degressief** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, worden de vaste activa waaraan dit afschrijvingsprofiel is toegewezen, afgeschreven met hetzelfde percentage in elke afschrijvingsperiode.</span><span class="sxs-lookup"><span data-stu-id="9d914-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="9d914-106">Het percentage wordt berekend aan de hand van de levensduur van het activum.</span><span class="sxs-lookup"><span data-stu-id="9d914-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="9d914-107">Als een activum een levensduur van bijvoorbeeld vijf jaar heeft, wordt het percentage berekend als 40 procent (200% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="9d914-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="9d914-108">Deze methode wordt ook 'double declining balance' genoemd.</span><span class="sxs-lookup"><span data-stu-id="9d914-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="9d914-109">Voor een 200% degressieve afschrijving moet u ook opties selecteren in het veld **Afschrijvingsjaar** en het veld **Periodefrequentie** op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="9d914-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="9d914-110">De opties die beschikbaar zijn in het veld **Periodefrequentie** variëren, afhankelijk van de waarde die u selecteert in het veld **Afschrijvingsjaar**.</span><span class="sxs-lookup"><span data-stu-id="9d914-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="9d914-111">Een afschrijvingsjaar selecteren</span><span class="sxs-lookup"><span data-stu-id="9d914-111">Select a depreciation year</span></span>
<span data-ttu-id="9d914-112">U kunt **Kalender** of **Fiscaal** selecteren in het veld **Afschrijvingsjaar** op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="9d914-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="9d914-113">De standaardwaarde is **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="9d914-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="9d914-114">Uw keuze bepaalt welke opties beschikbaar zijn in het veld **Periodefrequentie**.</span><span class="sxs-lookup"><span data-stu-id="9d914-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="9d914-115">Dit veld bepaalt voor het gehele jaar de boekingdatums en bedragen voor de toerekening van de afschrijving.</span><span class="sxs-lookup"><span data-stu-id="9d914-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="9d914-116">Kalender</span><span class="sxs-lookup"><span data-stu-id="9d914-116">Calendar</span></span>

<span data-ttu-id="9d914-117">U kunt de standaardwaarde **Kalender** in het veld **Afschrijvingsjaar** behouden.</span><span class="sxs-lookup"><span data-stu-id="9d914-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="9d914-118">Met de optie **Kalender** wordt de afschrijvingsbasis op 1 januari van elk jaar bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="9d914-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="9d914-119">Doorgaans is de afschrijving de nettoboekwaarde min de restwaarde.</span><span class="sxs-lookup"><span data-stu-id="9d914-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="9d914-120">In de voorbeelden verderop in dit onderwerp is de afschrijvingsbasis de teller in de eerste expressie in de berekeningenkolom.</span><span class="sxs-lookup"><span data-stu-id="9d914-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="9d914-121">Als u **Kalender** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:</span><span class="sxs-lookup"><span data-stu-id="9d914-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="9d914-122">**Jaarlijks**: op 31 december wordt een bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="9d914-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="9d914-123">**Maandelijks**: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="9d914-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="9d914-124">**Driemaandelijks**: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="9d914-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="9d914-125">**Zesmaandelijks**: aan het einde van elk half jaar (30 juni en 31 december) wordt er een halfjaarlijks bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="9d914-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="9d914-126">Met **Dagelijks** wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.</span><span class="sxs-lookup"><span data-stu-id="9d914-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="9d914-127">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="9d914-127">Fiscal</span></span>

<span data-ttu-id="9d914-128">Als u **Boekjaar** selecteert in het veld **Afschrijvingsjaar**, wordt de 200% degressieve afschrijving van de levensduur berekend op basis van het boekjaar voor de fiscale kalender die is opgegeven voor het boek of op basis van de pagina **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="9d914-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="9d914-129">Fiscale kalenders kunt u instellen op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="9d914-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="9d914-130">Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend.</span><span class="sxs-lookup"><span data-stu-id="9d914-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="9d914-131">Een boekjaar kan langer of korter dan 12 maanden zijn.</span><span class="sxs-lookup"><span data-stu-id="9d914-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="9d914-132">De afschrijving wordt voor elke periode aangepast.</span><span class="sxs-lookup"><span data-stu-id="9d914-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="9d914-133">De lengte van het volgende boekjaar wordt bepaald door de perioden die zijn ingesteld op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="9d914-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="9d914-134">Als **Fiscaal** als afschrijvingsjaar wordt geselecteerd, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:</span><span class="sxs-lookup"><span data-stu-id="9d914-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="9d914-135">**Jaarlijks** boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar als één bedrag op de laatste dag van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="9d914-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="9d914-136">**Boekperiode**: boekt het totale bedrag van de afschrijving dat is berekend voor het boekjaar op de laatste dag van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="9d914-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="9d914-137">Dit bedrag wordt toegerekend in de boekperioden die zijn gedefinieerd op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="9d914-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="9d914-138">Voorbeeld van een 200% degressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="9d914-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="9d914-139">Bijboekingskosten</span><span class="sxs-lookup"><span data-stu-id="9d914-139">Acquisition cost</span></span>               | <span data-ttu-id="9d914-140">11.000</span><span class="sxs-lookup"><span data-stu-id="9d914-140">11,000</span></span> |
| <span data-ttu-id="9d914-141">Restwaarde</span><span class="sxs-lookup"><span data-stu-id="9d914-141">Salvage value</span></span>                  | <span data-ttu-id="9d914-142">1.000</span><span class="sxs-lookup"><span data-stu-id="9d914-142">1, 000</span></span> |
| <span data-ttu-id="9d914-143">Afschrijvingsbasis</span><span class="sxs-lookup"><span data-stu-id="9d914-143">Depreciation base</span></span>              | <span data-ttu-id="9d914-144">10.000</span><span class="sxs-lookup"><span data-stu-id="9d914-144">10,000</span></span> |
| <span data-ttu-id="9d914-145">Levensduur in jaren</span><span class="sxs-lookup"><span data-stu-id="9d914-145">Service life years</span></span>             | <span data-ttu-id="9d914-146">5</span><span class="sxs-lookup"><span data-stu-id="9d914-146">5</span></span>      |
| <span data-ttu-id="9d914-147">Jaarlijks afschrijvingspercentage</span><span class="sxs-lookup"><span data-stu-id="9d914-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="9d914-148">40%</span><span class="sxs-lookup"><span data-stu-id="9d914-148">40%</span></span>    |

<span data-ttu-id="9d914-149">Bij de methode 200% degressieve afschrijvingsmethode, wordt 200 procent door het aantal jaren levensduur gedeeld.</span><span class="sxs-lookup"><span data-stu-id="9d914-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="9d914-150">Dat percentage wordt vermenigvuldigd met de nettoboekwaarde van de activa om het afschrijvingsbedrag voor het jaar te kunnen bepalen.</span><span class="sxs-lookup"><span data-stu-id="9d914-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="9d914-151">Periode</span><span class="sxs-lookup"><span data-stu-id="9d914-151">Period</span></span> | <span data-ttu-id="9d914-152">Berekening van het jaarlijkse afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="9d914-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="9d914-153">Boekwaarde</span><span class="sxs-lookup"><span data-stu-id="9d914-153">Book value</span></span>             | <span data-ttu-id="9d914-154">Nettoboekwaarde aan het einde van het jaar</span><span class="sxs-lookup"><span data-stu-id="9d914-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="9d914-155">Jaar 1</span><span class="sxs-lookup"><span data-stu-id="9d914-155">Year 1</span></span> | <span data-ttu-id="9d914-156">(11.000 – 1.000) × 40% = 4.000</span><span class="sxs-lookup"><span data-stu-id="9d914-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="9d914-157">11.000 – 4.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="9d914-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="9d914-158">11.000 – 1.000 – 4.000 = 6.000</span><span class="sxs-lookup"><span data-stu-id="9d914-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="9d914-159">Jaar 2</span><span class="sxs-lookup"><span data-stu-id="9d914-159">Year 2</span></span> | <span data-ttu-id="9d914-160">6.000 × 40% = 2.400</span><span class="sxs-lookup"><span data-stu-id="9d914-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="9d914-161">7.000 – 2.400 = 4.600</span><span class="sxs-lookup"><span data-stu-id="9d914-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="9d914-162">6.000 – 2.400 = 3.600</span><span class="sxs-lookup"><span data-stu-id="9d914-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="9d914-163">Jaar 3</span><span class="sxs-lookup"><span data-stu-id="9d914-163">Year 3</span></span> | <span data-ttu-id="9d914-164">3.600 × 40% = 1.440</span><span class="sxs-lookup"><span data-stu-id="9d914-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="9d914-165">4.600 – 1.440 = 3.160</span><span class="sxs-lookup"><span data-stu-id="9d914-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="9d914-166">3.600 – 1.440 = 2.160</span><span class="sxs-lookup"><span data-stu-id="9d914-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="9d914-167">Wanneer het bedrag dat wordt berekend met de methode voor 200% degressieve afschrijving lager is dan het bedrag dat wordt berekend door de lineaire methode te gebruiken, vindt er doorgaans een conversie naar de lineaire methode plaats voor de resterende levensduur.</span><span class="sxs-lookup"><span data-stu-id="9d914-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



