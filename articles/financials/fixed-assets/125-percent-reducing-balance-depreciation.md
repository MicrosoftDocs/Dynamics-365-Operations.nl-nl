---
title: Degressieve afschrijving van 125 procent
description: Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 125 procent.
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7af5413376a98c3b2b7ded46c757c9156a3fadf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555691"
---
# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="b6635-103">Degressieve afschrijving van 125 procent</span><span class="sxs-lookup"><span data-stu-id="b6635-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6635-104">Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 125 procent.</span><span class="sxs-lookup"><span data-stu-id="b6635-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="b6635-105">Wanneer u een profiel voor de afschrijving van vaste activa instelt en **125% degressieve afschrijving** in het veld **Methode** op de pagina **Afrschrijvingsprofielen**, worden vaste activa die zijn toegewezen aan het afschrijvingsprofiel met hetzelfde percentage afgeschreven in elke afschrijvingsperiode.</span><span class="sxs-lookup"><span data-stu-id="b6635-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="b6635-106">Dit percentage wordt berekend aan de hand van de levensduur van het activum.</span><span class="sxs-lookup"><span data-stu-id="b6635-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="b6635-107">Als een activum een levensduur van bijvoorbeeld vijf jaar heeft, wordt het percentage berekend als 25 procent (125% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="b6635-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="b6635-108">Voor een degressieve afschrijving van 125% moet u ook opties selecteren in het veld **Afschrijvingsjaar** en het veld **Periodefrequentie** op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="b6635-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="b6635-109">De opties die beschikbaar zijn in het veld **Periodefrequentie** variëren, afhankelijk van de waarde die in het veld **Afschrijvingsjaar** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b6635-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="b6635-110">Een afschrijvingsjaar selecteren</span><span class="sxs-lookup"><span data-stu-id="b6635-110">Select a depreciation year</span></span>
<span data-ttu-id="b6635-111">U kunt **Kalender** of **Fiscaal** selecteren in het veld **Afschrijvingsjaar** op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="b6635-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="b6635-112">De standaardwaarde is **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="b6635-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="b6635-113">Uw keuze bepaalt welke opties beschikbaar zijn in het veld **Periodefrequentie**.</span><span class="sxs-lookup"><span data-stu-id="b6635-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="b6635-114">Dit veld bepaalt voor het gehele jaar de boekingdatums en bedragen voor de toerekening van de afschrijving.</span><span class="sxs-lookup"><span data-stu-id="b6635-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="b6635-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="b6635-115">Calendar</span></span>

<span data-ttu-id="b6635-116">U kunt de standaardwaarde **Kalender** in het veld **Afschrijvingsjaar** behouden.</span><span class="sxs-lookup"><span data-stu-id="b6635-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="b6635-117">Met de optie **Kalender** wordt de afschrijvingsbasis op 1 januari van elk jaar bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b6635-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="b6635-118">Doorgaans is de afschrijvingsbasis de nettoboekwaarde min de restwaarde.</span><span class="sxs-lookup"><span data-stu-id="b6635-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="b6635-119">In de voorbeelden verderop in dit onderwerp is de afschrijvingsbasis de teller in de eerste expressie in de berekeningenkolom.</span><span class="sxs-lookup"><span data-stu-id="b6635-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="b6635-120">Als u **Kalender** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:</span><span class="sxs-lookup"><span data-stu-id="b6635-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="b6635-121">**Jaarlijks**: op 31 december wordt een bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b6635-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="b6635-122">**Maandelijks**: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b6635-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="b6635-123">**Driemaandelijks**: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b6635-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="b6635-124">**Zesmaandelijks**: aan het einde van elk half jaar (30 juni en 31 december) wordt er een halfjaarlijks bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b6635-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="b6635-125">Met **Dagelijks** wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.</span><span class="sxs-lookup"><span data-stu-id="b6635-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="b6635-126">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="b6635-126">Fiscal</span></span>

<span data-ttu-id="b6635-127">Als u **Boekjaar** selecteert in het veld **Afschrijvingsjaar**, wordt de 125% degressieve afschrijving van de levensduur berekend op basis van het boekjaar voor de fiscale kalender die is opgegeven voor het boek of op basis van de pagina **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="b6635-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="b6635-128">Fiscale kalenders kunt u instellen op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="b6635-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="b6635-129">Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend.</span><span class="sxs-lookup"><span data-stu-id="b6635-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="b6635-130">Een boekjaar kan langer of korter dan 12 maanden zijn.</span><span class="sxs-lookup"><span data-stu-id="b6635-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="b6635-131">De afschrijving wordt automatisch voor elke periode aangepast, en de lengte van het volgend boekjaar wordt gehaald uit de instellingen van perioden op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="b6635-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="b6635-132">Als u **Fiscaal** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:</span><span class="sxs-lookup"><span data-stu-id="b6635-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="b6635-133">**Jaarlijks** boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar als één bedrag op de laatste dag van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="b6635-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="b6635-134">**Boekperiode**: boekt het totale bedrag van de afschrijving dat is berekend voor het boekjaar op de laatste dag van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="b6635-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="b6635-135">Dit bedrag wordt toegerekend in de boekperioden die zijn gedefinieerd op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="b6635-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="b6635-136">Voorbeeld van een 125% degressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="b6635-136">Example of 125% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="b6635-137">Bijboekingskosten</span><span class="sxs-lookup"><span data-stu-id="b6635-137">Acquisition cost</span></span>               | <span data-ttu-id="b6635-138">11.000</span><span class="sxs-lookup"><span data-stu-id="b6635-138">11,000</span></span> |
| <span data-ttu-id="b6635-139">Restwaarde</span><span class="sxs-lookup"><span data-stu-id="b6635-139">Salvage value</span></span>                  | <span data-ttu-id="b6635-140">1.000</span><span class="sxs-lookup"><span data-stu-id="b6635-140">1,000</span></span>  |
| <span data-ttu-id="b6635-141">Afschrijvingsbasis</span><span class="sxs-lookup"><span data-stu-id="b6635-141">Depreciation base</span></span>              | <span data-ttu-id="b6635-142">10.000</span><span class="sxs-lookup"><span data-stu-id="b6635-142">10,000</span></span> |
| <span data-ttu-id="b6635-143">Levensduur in jaren</span><span class="sxs-lookup"><span data-stu-id="b6635-143">Service life years</span></span>             | <span data-ttu-id="b6635-144">5</span><span class="sxs-lookup"><span data-stu-id="b6635-144">5</span></span>      |
| <span data-ttu-id="b6635-145">Jaarlijks afschrijvingspercentage</span><span class="sxs-lookup"><span data-stu-id="b6635-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="b6635-146">25%</span><span class="sxs-lookup"><span data-stu-id="b6635-146">25%</span></span>    |

<span data-ttu-id="b6635-147">Bij de methode 125% degressieve afschrijvingsmethode, wordt 125 procent door het aantal jaren levensduur gedeeld.</span><span class="sxs-lookup"><span data-stu-id="b6635-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="b6635-148">Dat percentage wordt vermenigvuldigd met de nettoboekwaarde van de activa om het afschrijvingsbedrag voor het jaar te kunnen bepalen.</span><span class="sxs-lookup"><span data-stu-id="b6635-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="b6635-149">Periode</span><span class="sxs-lookup"><span data-stu-id="b6635-149">Period</span></span> | <span data-ttu-id="b6635-150">Berekening van het jaarlijkse afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="b6635-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="b6635-151">Boekwaarde</span><span class="sxs-lookup"><span data-stu-id="b6635-151">Book value</span></span>                    | <span data-ttu-id="b6635-152">Nettoboekwaarde aan het einde van het jaar</span><span class="sxs-lookup"><span data-stu-id="b6635-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="b6635-153">Jaar 1</span><span class="sxs-lookup"><span data-stu-id="b6635-153">Year 1</span></span> | <span data-ttu-id="b6635-154">(11.000 – 1000) × 25% = 2500</span><span class="sxs-lookup"><span data-stu-id="b6635-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="b6635-155">(11.000 – 2500) = 8500</span><span class="sxs-lookup"><span data-stu-id="b6635-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="b6635-156">(11.000 – 1000 – 2500) = 7500</span><span class="sxs-lookup"><span data-stu-id="b6635-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="b6635-157">Jaar 2</span><span class="sxs-lookup"><span data-stu-id="b6635-157">Year 2</span></span> | <span data-ttu-id="b6635-158">7500 × 25% = 1875</span><span class="sxs-lookup"><span data-stu-id="b6635-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="b6635-159">(8500 – 1875) = 6625</span><span class="sxs-lookup"><span data-stu-id="b6635-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="b6635-160">(7500 – 1875) = 5625</span><span class="sxs-lookup"><span data-stu-id="b6635-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="b6635-161">Jaar 3</span><span class="sxs-lookup"><span data-stu-id="b6635-161">Year 3</span></span> | <span data-ttu-id="b6635-162">5625 × 25% = 1406,25</span><span class="sxs-lookup"><span data-stu-id="b6635-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="b6635-163">(6625 – 1406,25) = 5218,75</span><span class="sxs-lookup"><span data-stu-id="b6635-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="b6635-164">(5625 – 1406,25) = 4218,75</span><span class="sxs-lookup"><span data-stu-id="b6635-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="b6635-165">Wanneer het bedrag dat wordt berekend met de methode voor 125% degressieve afschrijving lager is dan het bedrag dat wordt berekend door de lineaire methode te gebruiken, vindt er doorgaans een conversie naar de lineaire methode plaats voor de resterende levensduur.</span><span class="sxs-lookup"><span data-stu-id="b6635-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



