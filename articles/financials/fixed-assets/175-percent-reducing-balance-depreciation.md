---
title: Degressieve afschrijving van 175 procent
description: Dit onderwerp biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 175 procent.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a61e743898e3e65c0012a7aeb9837e55e9143d01
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="b02da-103">Degressieve afschrijving van 175 procent</span><span class="sxs-lookup"><span data-stu-id="b02da-103">175 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b02da-104">Dit onderwerp biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving van 175 procent.</span><span class="sxs-lookup"><span data-stu-id="b02da-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="b02da-105">Wanneer u een profiel voor de afschrijving van vaste activa instelt en **175% degressief** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, worden de vaste activa waaraan dit afschrijvingsprofiel is toegewezen, afgeschreven met hetzelfde percentage in elke afschrijvingsperiode.</span><span class="sxs-lookup"><span data-stu-id="b02da-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="b02da-106">Voor een 175% degressieve afschrijving moet u ook opties selecteren in het veld **Afschrijvingsjaar** en het veld **Periodefrequentie** op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="b02da-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="b02da-107">De opties die beschikbaar zijn in het veld **Periodefrequentie** variëren, afhankelijk van de waarde die in het veld **Afschrijvingsjaar** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b02da-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="b02da-108">Een afschrijvingsjaar selecteren</span><span class="sxs-lookup"><span data-stu-id="b02da-108">Select a depreciation year</span></span>
<span data-ttu-id="b02da-109">U kunt **Kalender** of **Fiscaal** selecteren in het veld **Afschrijvingsjaar** op de pagina **Afschrijvingsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="b02da-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="b02da-110">De standaardwaarde is **Kalender**.</span><span class="sxs-lookup"><span data-stu-id="b02da-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="b02da-111">Uw keuze bepaalt welke opties beschikbaar zijn in het veld **Periodefrequentie**.</span><span class="sxs-lookup"><span data-stu-id="b02da-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="b02da-112">Dit veld bepaalt voor het gehele jaar de boekingdatums en bedragen voor de toerekening van de afschrijving.</span><span class="sxs-lookup"><span data-stu-id="b02da-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="b02da-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="b02da-113">Calendar</span></span>

<span data-ttu-id="b02da-114">U kunt de standaardwaarde **Kalender** in het veld **Afschrijvingsjaar** behouden.</span><span class="sxs-lookup"><span data-stu-id="b02da-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="b02da-115">Met de optie **Kalender** wordt de afschrijvingsbasis op 1 januari van elk jaar bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b02da-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="b02da-116">Doorgaans is de afschrijvingsbasis de nettoboekwaarde min de restwaarde.</span><span class="sxs-lookup"><span data-stu-id="b02da-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="b02da-117">In de voorbeelden verderop in dit onderwerp is de afschrijvingsbasis de teller in de eerste expressie in de berekeningenkolom.</span><span class="sxs-lookup"><span data-stu-id="b02da-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="b02da-118">Als u **Kalender** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:</span><span class="sxs-lookup"><span data-stu-id="b02da-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="b02da-119">**Jaarlijks**: op 31 december wordt een bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b02da-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="b02da-120">**Maandelijks**: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b02da-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="b02da-121">**Driemaandelijks**: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b02da-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="b02da-122">**Zesmaandelijks**: aan het einde van elk half jaar (30 juni en 31 december) wordt er een halfjaarlijks bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b02da-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="b02da-123">Met **Dagelijks** wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.</span><span class="sxs-lookup"><span data-stu-id="b02da-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="b02da-124">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="b02da-124">Fiscal</span></span>

<span data-ttu-id="b02da-125">Als u **Boekjaar** selecteert in het veld **Afschrijvingsjaar**, wordt de 175% degressieve afschrijving van de levensduur berekend op basis van het boekjaar voor de fiscale kalender die is opgegeven voor het boek of op basis van de pagina **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="b02da-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="b02da-126">Fiscale kalenders kunt u instellen op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="b02da-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="b02da-127">Zie voor meer informatie [Fiscale kalenders, boekjaren en boekperioden](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="b02da-127">For more information, see [Fiscal calendars, fiscal years, and periods](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="b02da-128">Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend.</span><span class="sxs-lookup"><span data-stu-id="b02da-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="b02da-129">Een boekjaar kan langer of korter dan 12 maanden zijn.</span><span class="sxs-lookup"><span data-stu-id="b02da-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="b02da-130">De afschrijving wordt automatisch voor elke periode aangepast, en de lengte van het volgend boekjaar wordt gehaald uit de instellingen van perioden op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="b02da-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="b02da-131">Als u **Fiscaal** als het afschrijvingsjaar selecteert, zijn de volgende opties beschikbaar in het veld **Periodefrequentie**:</span><span class="sxs-lookup"><span data-stu-id="b02da-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="b02da-132">**Jaarlijks**: boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar op de laatste dag van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="b02da-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="b02da-133">**Boekperiode**: berekent het totale bedrag van de afschrijving voor het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="b02da-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="b02da-134">Dit bedrag wordt toegerekend in de boekperioden die zijn gedefinieerd op de pagina **Fiscale kalenders**.</span><span class="sxs-lookup"><span data-stu-id="b02da-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="b02da-135">Voorbeeld van een 175% degressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="b02da-135">Example of 175% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="b02da-136">Bijboekingskosten</span><span class="sxs-lookup"><span data-stu-id="b02da-136">Acquisition cost</span></span>               | <span data-ttu-id="b02da-137">11.000</span><span class="sxs-lookup"><span data-stu-id="b02da-137">11,000</span></span> |
| <span data-ttu-id="b02da-138">Restwaarde</span><span class="sxs-lookup"><span data-stu-id="b02da-138">Salvage value</span></span>                  | <span data-ttu-id="b02da-139">1.000</span><span class="sxs-lookup"><span data-stu-id="b02da-139">1,000</span></span>  |
| <span data-ttu-id="b02da-140">Afschrijvingsbasis</span><span class="sxs-lookup"><span data-stu-id="b02da-140">Depreciation base</span></span>              | <span data-ttu-id="b02da-141">10.000</span><span class="sxs-lookup"><span data-stu-id="b02da-141">10,000</span></span> |
| <span data-ttu-id="b02da-142">Levensduur in jaren</span><span class="sxs-lookup"><span data-stu-id="b02da-142">Service life years</span></span>             | <span data-ttu-id="b02da-143">5</span><span class="sxs-lookup"><span data-stu-id="b02da-143">5</span></span>      |
| <span data-ttu-id="b02da-144">Jaarlijks afschrijvingspercentage</span><span class="sxs-lookup"><span data-stu-id="b02da-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="b02da-145">35%</span><span class="sxs-lookup"><span data-stu-id="b02da-145">35%</span></span>    |

<span data-ttu-id="b02da-146">Bij de methode 175% degressieve afschrijvingsmethode wordt 175 procent door het aantal jaren levensduur gedeeld.</span><span class="sxs-lookup"><span data-stu-id="b02da-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="b02da-147">Dat percentage wordt vermenigvuldigd met de nettoboekwaarde van de activa om het afschrijvingsbedrag voor het jaar te kunnen bepalen.</span><span class="sxs-lookup"><span data-stu-id="b02da-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="b02da-148">Periode</span><span class="sxs-lookup"><span data-stu-id="b02da-148">Period</span></span> | <span data-ttu-id="b02da-149">Berekening van het jaarlijkse afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="b02da-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="b02da-150">Boekwaarde</span><span class="sxs-lookup"><span data-stu-id="b02da-150">Book value</span></span>                  | <span data-ttu-id="b02da-151">Nettoboekwaarde aan het einde van het jaar</span><span class="sxs-lookup"><span data-stu-id="b02da-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="b02da-152">Jaar 1</span><span class="sxs-lookup"><span data-stu-id="b02da-152">Year 1</span></span> | <span data-ttu-id="b02da-153">(11.000 – 1000) × 35% = 3500</span><span class="sxs-lookup"><span data-stu-id="b02da-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="b02da-154">11.000 – 3500 = 7500</span><span class="sxs-lookup"><span data-stu-id="b02da-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="b02da-155">11.000 – 1000 – 3500 = 6500</span><span class="sxs-lookup"><span data-stu-id="b02da-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="b02da-156">Jaar 2</span><span class="sxs-lookup"><span data-stu-id="b02da-156">Year 2</span></span> | <span data-ttu-id="b02da-157">6500 × 35% = 2275</span><span class="sxs-lookup"><span data-stu-id="b02da-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="b02da-158">7500 – 2275 = 5225</span><span class="sxs-lookup"><span data-stu-id="b02da-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="b02da-159">6500 – 2275 = 4225</span><span class="sxs-lookup"><span data-stu-id="b02da-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="b02da-160">Jaar 3</span><span class="sxs-lookup"><span data-stu-id="b02da-160">Year 3</span></span> | <span data-ttu-id="b02da-161">4225 × 35% = 1478,75</span><span class="sxs-lookup"><span data-stu-id="b02da-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="b02da-162">5225 – 1478,75 = 3746,25</span><span class="sxs-lookup"><span data-stu-id="b02da-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="b02da-163">4225 – 1478,75 = 2746,25</span><span class="sxs-lookup"><span data-stu-id="b02da-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="b02da-164">Wanneer het bedrag dat wordt berekend met de methode voor 175% degressieve afschrijving lager is dan het bedrag dat wordt berekend door de lineaire methode te gebruiken, vindt er doorgaans een conversie naar de lineaire methode plaats voor de resterende levensduur.</span><span class="sxs-lookup"><span data-stu-id="b02da-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




