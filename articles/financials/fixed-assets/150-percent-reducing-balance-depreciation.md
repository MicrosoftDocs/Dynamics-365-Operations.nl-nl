---
title: Degressieve afschrijving van 150 procent
description: Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 150 procent.
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
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff4b40663f0da6bcc01b00f3f44cd8d8b43b56a1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "331616"
---
# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="6182f-103">Degressieve afschrijving van 150 procent</span><span class="sxs-lookup"><span data-stu-id="6182f-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6182f-104">Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 150 procent.</span><span class="sxs-lookup"><span data-stu-id="6182f-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="6182f-105">Wanneer u een profiel voor de afschrijving van vaste activa instelt en **150% degressief** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, worden de vaste activa waaraan dit afschrijvingsprofiel is toegewezen, afgeschreven met hetzelfde percentage in elke afschrijvingsperiode.</span><span class="sxs-lookup"><span data-stu-id="6182f-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="6182f-106">Dit percentage wordt berekend aan de hand van de levensduur van het activum.</span><span class="sxs-lookup"><span data-stu-id="6182f-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="6182f-107">Als een activum een levensduur van bijvoorbeeld vijf jaar heeft, wordt het percentage berekend als 30 procent (150% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="6182f-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="6182f-108">Voor een 150% degressieve afschrijving moet u ook opties selecteren in het veld **Afschrijvingsjaar** en het veld **Periodefrequentie** op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="6182f-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="6182f-109">De opties die beschikbaar zijn in het veld **Periodefrequentie** variëren, afhankelijk van de waarde die in het veld **Afschrijvingsjaar** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="6182f-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="6182f-110">Selectie van afschrijvingsjaar</span><span class="sxs-lookup"><span data-stu-id="6182f-110">Selection of depreciation year</span></span>
<span data-ttu-id="6182f-111">U kunt **Kalender** of **Fiscaal** selecteren in het veld **Afschrijvingsjaar** op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="6182f-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="6182f-112">De standaardwaarde is **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="6182f-112">The default value is **Calendar**.</span></span> <span data-ttu-id="6182f-113">Uw keuze bepaalt welke opties beschikbaar zijn in het veld **Periodefrequentie**.</span><span class="sxs-lookup"><span data-stu-id="6182f-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="6182f-114">Dit veld bepaalt voor het gehele jaar de boekingdatums en bedragen voor de toerekening van de afschrijving.</span><span class="sxs-lookup"><span data-stu-id="6182f-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="6182f-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="6182f-115">Calendar</span></span>

<span data-ttu-id="6182f-116">U kunt de standaardwaarde **Kalender** in het veld **Afschrijvingsjaar** behouden.</span><span class="sxs-lookup"><span data-stu-id="6182f-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="6182f-117">Met de optie **Kalender** wordt de afschrijvingsbasis op 1 januari van elk jaar bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="6182f-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="6182f-118">Doorgaans is de afschrijvingsbasis de nettoboekwaarde min de restwaarde.</span><span class="sxs-lookup"><span data-stu-id="6182f-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="6182f-119">In de voorbeelden verderop in dit onderwerp is de afschrijvingsbasis de teller in de eerste expressie in de berekeningenkolom.</span><span class="sxs-lookup"><span data-stu-id="6182f-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="6182f-120">Als u **Kalender** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:</span><span class="sxs-lookup"><span data-stu-id="6182f-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="6182f-121">**Jaarlijks**: op 31 december wordt een bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="6182f-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="6182f-122">**Maandelijks**: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="6182f-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="6182f-123">**Driemaandelijks**: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="6182f-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="6182f-124">**Zesmaandelijks**: aan het einde van elk half jaar (30 juni en 31 december) wordt er een halfjaarlijks bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="6182f-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="6182f-125">Met **Dagelijks** wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.</span><span class="sxs-lookup"><span data-stu-id="6182f-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="6182f-126">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="6182f-126">Fiscal</span></span>

<span data-ttu-id="6182f-127">Als u **Boekjaar** selecteert in het veld **Afschrijvingsjaar**, wordt de 150% degressieve afschrijving van de levensduur berekend op basis van het boekjaar voor de fiscale kalender die is opgegeven voor het boek of op basis van de pagina **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="6182f-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="6182f-128">Fiscale kalenders kunt u instellen op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="6182f-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="6182f-129">Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend.</span><span class="sxs-lookup"><span data-stu-id="6182f-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="6182f-130">Een boekjaar kan langer of korter dan 12 maanden zijn.</span><span class="sxs-lookup"><span data-stu-id="6182f-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="6182f-131">De afschrijving wordt voor elke periode aangepast.</span><span class="sxs-lookup"><span data-stu-id="6182f-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="6182f-132">De lengte van het volgende boekjaar wordt bepaald door de perioden die zijn ingesteld op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="6182f-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="6182f-133">Als u **Fiscaal** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:</span><span class="sxs-lookup"><span data-stu-id="6182f-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="6182f-134">**Jaarlijks**: boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar op de laatste dag van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="6182f-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="6182f-135">**Boekperiode**: boekt het totale bedrag van de afschrijving dat is berekend voor het boekjaar op de laatste dag van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="6182f-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="6182f-136">Dit bedrag wordt toegerekend in de boekperioden die zijn gedefinieerd op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="6182f-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="6182f-137">Voorbeeld van een 150% degressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="6182f-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="6182f-138">Bijboekingskosten</span><span class="sxs-lookup"><span data-stu-id="6182f-138">Acquisition cost</span></span>               | <span data-ttu-id="6182f-139">11.000</span><span class="sxs-lookup"><span data-stu-id="6182f-139">11,000</span></span> |
| <span data-ttu-id="6182f-140">Restwaarde</span><span class="sxs-lookup"><span data-stu-id="6182f-140">Salvage value</span></span>                  | <span data-ttu-id="6182f-141">1.000</span><span class="sxs-lookup"><span data-stu-id="6182f-141">1,000</span></span>  |
| <span data-ttu-id="6182f-142">Afschrijvingsbasis</span><span class="sxs-lookup"><span data-stu-id="6182f-142">Depreciation base</span></span>              | <span data-ttu-id="6182f-143">10.000</span><span class="sxs-lookup"><span data-stu-id="6182f-143">10,000</span></span> |
| <span data-ttu-id="6182f-144">Levensduur in jaren</span><span class="sxs-lookup"><span data-stu-id="6182f-144">Service life years</span></span>             | <span data-ttu-id="6182f-145">5</span><span class="sxs-lookup"><span data-stu-id="6182f-145">5</span></span>      |
| <span data-ttu-id="6182f-146">Jaarlijks afschrijvingspercentage</span><span class="sxs-lookup"><span data-stu-id="6182f-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="6182f-147">30%</span><span class="sxs-lookup"><span data-stu-id="6182f-147">30%</span></span>    |

<span data-ttu-id="6182f-148">Bij de methode 150% degressieve afschrijvingsmethode, wordt 150 procent door het aantal jaren levensduur gedeeld.</span><span class="sxs-lookup"><span data-stu-id="6182f-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="6182f-149">Dat percentage wordt vermenigvuldigd met de nettoboekwaarde van de activa om het afschrijvingsbedrag voor het jaar te kunnen bepalen.</span><span class="sxs-lookup"><span data-stu-id="6182f-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="6182f-150">Periode</span><span class="sxs-lookup"><span data-stu-id="6182f-150">Period</span></span> | <span data-ttu-id="6182f-151">Berekening van het jaarlijkse afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="6182f-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="6182f-152">Boekwaarde</span><span class="sxs-lookup"><span data-stu-id="6182f-152">Book value</span></span>             | <span data-ttu-id="6182f-153">Nettoboekwaarde aan het einde van het jaar</span><span class="sxs-lookup"><span data-stu-id="6182f-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="6182f-154">Jaar 1</span><span class="sxs-lookup"><span data-stu-id="6182f-154">Year 1</span></span> | <span data-ttu-id="6182f-155">(11.000 – 1.000) × 30% = 3.000</span><span class="sxs-lookup"><span data-stu-id="6182f-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="6182f-156">11.000 – 3.000 = 8.000</span><span class="sxs-lookup"><span data-stu-id="6182f-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="6182f-157">11.000 – 1.000 – 3.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="6182f-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="6182f-158">Jaar 2</span><span class="sxs-lookup"><span data-stu-id="6182f-158">Year 2</span></span> | <span data-ttu-id="6182f-159">7.000 × 30% = 2.100</span><span class="sxs-lookup"><span data-stu-id="6182f-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="6182f-160">8000 – 2100 = 5900</span><span class="sxs-lookup"><span data-stu-id="6182f-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="6182f-161">7000 – 2100 = 4900</span><span class="sxs-lookup"><span data-stu-id="6182f-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="6182f-162">Jaar 3</span><span class="sxs-lookup"><span data-stu-id="6182f-162">Year 3</span></span> | <span data-ttu-id="6182f-163">4.900 × 30% = 1.470</span><span class="sxs-lookup"><span data-stu-id="6182f-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="6182f-164">5.900 – 1.470 = 4.430</span><span class="sxs-lookup"><span data-stu-id="6182f-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="6182f-165">4.900 – 1.470 = 3.430</span><span class="sxs-lookup"><span data-stu-id="6182f-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="6182f-166">Wanneer het bedrag dat wordt berekend met de methode voor 150% degressieve afschrijving lager is dan het bedrag dat wordt berekend door de lineaire methode te gebruiken, vindt er doorgaans een conversie naar de lineaire methode plaats voor de resterende levensduur.</span><span class="sxs-lookup"><span data-stu-id="6182f-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



