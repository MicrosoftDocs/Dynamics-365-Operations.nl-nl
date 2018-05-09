---
title: Degressieve afschrijving
description: Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving.
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 94bd18697c5074deb17980d4354dc0e690233f6f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="reduce-balance-depreciation"></a><span data-ttu-id="dccc3-103">Degressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="dccc3-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dccc3-104">Dit artikel biedt een overzicht van de afschrijvingsmethode Degressieve afschrijving.</span><span class="sxs-lookup"><span data-stu-id="dccc3-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="dccc3-105">Wanneer u een profiel voor de afschrijving van vaste activa instelt en Degressieve afschrijving selecteert in het veld Methode op de pagina Afschrijvingsprofielen, worden de activa waaraan dit afschrijvingsprofiel is toegewezen, afgeschreven met hetzelfde percentage in elke afschrijvingsperiode.</span><span class="sxs-lookup"><span data-stu-id="dccc3-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="dccc3-106">Om degressieve afschrijving in te stellen, moet u ook waarden selecteren in velden op het sneltabblad Algemeen van de pagina Afschrijvingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="dccc3-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="dccc3-107">Selecteer eerst een jaar in het veld Afschrijvingsjaar.</span><span class="sxs-lookup"><span data-stu-id="dccc3-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="dccc3-108">In het veld Periodefrequentie worden verschillende opties weergegeven, afhankelijk van wat in het andere veld is geselecteerd (zie verderop).</span><span class="sxs-lookup"><span data-stu-id="dccc3-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="dccc3-109">U dient ook een waarde in te voeren bij het veld Percentage voor het afschrijvingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="dccc3-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="dccc3-110">Als u de optie Volledige afschrijving selecteert, wordt de resterende afschrijvingsbasis gekozen in de laatste afschrijvingsperiode en is het mogelijk een grote hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="dccc3-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="dccc3-111">Bepaalde landen/regio's gebruiken geen overschakeling naar een lineaire methode.</span><span class="sxs-lookup"><span data-stu-id="dccc3-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="dccc3-112">Wanneer het bedrag van de alternatieve afschrijvingsmethode groter dan of gelijk aan is het bedrag van het primaire afschrijvingsprofiel, wordt overgeschakeld en wordt het bedrag van de alternatieve methode gebruikt als afschrijvingsbedrag.</span><span class="sxs-lookup"><span data-stu-id="dccc3-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="dccc3-113">Aangezien een activum nooit volledig zal worden afgeschreven op basis van een berekening van het percentage, dient u de optie Volledige afschrijving te selecteren om een activum volledig af te schrijven.</span><span class="sxs-lookup"><span data-stu-id="dccc3-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="dccc3-114">Een afschrijvingsjaar selecteren</span><span class="sxs-lookup"><span data-stu-id="dccc3-114">Select a depreciation year</span></span>
<span data-ttu-id="dccc3-115">U kunt Kalender of Fiscaal selecteren in het veld Afschrijvingsjaar op de pagina Afschrijvingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="dccc3-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="dccc3-116">De selectie bepaalt welke opties beschikbaar zijn in het veld Periodefrequentie.</span><span class="sxs-lookup"><span data-stu-id="dccc3-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="dccc3-117">De standaardoptie is Kalender.</span><span class="sxs-lookup"><span data-stu-id="dccc3-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="dccc3-118">Kalender</span><span class="sxs-lookup"><span data-stu-id="dccc3-118">Calendar</span></span>

<span data-ttu-id="dccc3-119">Met de optie Kalender wordt de afschrijvingsbasis (doorgaans de nettoboekwaarde min de restwaarde) bijgewerkt op 1 januari van elk jaar.</span><span class="sxs-lookup"><span data-stu-id="dccc3-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="dccc3-120">In het onderstaande voorbeeld van degressieve saldoafschrijving verder in dit onderwerp, is de afschrijvingsbasis de teller in de eerste uitdrukking in de kolom met berekeningen.</span><span class="sxs-lookup"><span data-stu-id="dccc3-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="dccc3-121">Als u Kalender selecteert, zijn de volgende opties beschikbaar in het veld Periodefrequentie. Dit veld bepaalt voor het gehele kalenderjaar de boekdatums en bedragen voor de toerekening van de afschrijving:</span><span class="sxs-lookup"><span data-stu-id="dccc3-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="dccc3-122">Jaarlijks boekt op 31 december.</span><span class="sxs-lookup"><span data-stu-id="dccc3-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="dccc3-123">Maandelijks: aan het einde van elke kalendermaand wordt een maandbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="dccc3-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="dccc3-124">Driemaandelijks: aan het einde van elk kwartaal (31 maart, 30 juni, 30 september en 31 december) wordt een kwartaalbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="dccc3-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="dccc3-125">Met Zesmaandelijks wordt aan het einde van elk half jaar (30 juni en 31 december) een halfjaarlijks bedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="dccc3-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="dccc3-126">Met Dagelijks wordt het afschrijvingsbedrag voor de dagelijkse afschrijvingsmethode geboekt met één transactie voor elke dag.</span><span class="sxs-lookup"><span data-stu-id="dccc3-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="dccc3-127">Als u bijvoorbeeld Jaarlijks selecteert, wordt de jaarlijkse afschrijving wordt slechts één keer geboekt. Dit is telkens op 31 december.</span><span class="sxs-lookup"><span data-stu-id="dccc3-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="dccc3-128">Als u Maandelijks selecteert, wordt de maandelijkse afschrijving elke maand als 1/12de van het jaarlijkse afschrijvingsbedrag geboekt.</span><span class="sxs-lookup"><span data-stu-id="dccc3-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="dccc3-129">Fiscaal</span><span class="sxs-lookup"><span data-stu-id="dccc3-129">Fiscal</span></span>

<span data-ttu-id="dccc3-130">Als u Fiscaal selecteert in het veld Afschrijvingsjaar wordt de lineaire afschrijvingsmethode gebruikt.</span><span class="sxs-lookup"><span data-stu-id="dccc3-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="dccc3-131">Het wordt berekend op basis van het fiscaal jaar dat is ingesteld op de pagina Fiscale kalenders voor de fiscale kalender die is geselecteerd op de pagina Grootboek.</span><span class="sxs-lookup"><span data-stu-id="dccc3-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="dccc3-132">Voor bijvoorbeeld het boekjaar van 1 juli t/m 30 juni wordt de afschrijving vanaf 1 juli berekend.</span><span class="sxs-lookup"><span data-stu-id="dccc3-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="dccc3-133">Een boekjaar kan langer of korter dan 12 maanden zijn.</span><span class="sxs-lookup"><span data-stu-id="dccc3-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="dccc3-134">De afschrijving wordt voor elke boekperiode aangepast.</span><span class="sxs-lookup"><span data-stu-id="dccc3-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="dccc3-135">De lengte van het volgende boekjaar is gebaseerd op de boekperioden die u instelt wanneer u een nieuw fiscaal jaar maakt op de pagina Fiscale kalenders.</span><span class="sxs-lookup"><span data-stu-id="dccc3-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="dccc3-136">Als u Fiscaal selecteert in het veld Periodefrequentie, dan zijn de volgende opties beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="dccc3-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="dccc3-137">Jaarlijks boekt het totale bedrag van de afschrijving die is berekend voor het boekjaar als één bedrag op de laatste dag van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="dccc3-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="dccc3-138">Boekperiode boekt het totale bedrag van de afschrijving berekend voor het fiscaal jaar, dat wordt toegerekend in de boekperioden die zijn gedefinieerd voor de fiscale kalender die is geselecteerd op de pagina Grootboek of voor de fiscale kalender die is geselecteerd voor het boek voor een vast activum.</span><span class="sxs-lookup"><span data-stu-id="dccc3-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="dccc3-139">Voorbeeld van een degressieve afschrijving</span><span class="sxs-lookup"><span data-stu-id="dccc3-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="dccc3-140">Stel dat de aanschafprijs van het vaste activum 11.000 is, de restwaarde is 1.000 en de afschrijvingspercentagefactor is 30.</span><span class="sxs-lookup"><span data-stu-id="dccc3-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="dccc3-141">Door de methode Degressief te gebruiken, wordt 30 procent van de afschrijvingsbasis (nettoboekwaarde min restwaarde) berekend aan het einde van de vorige afschrijvingsperiode.</span><span class="sxs-lookup"><span data-stu-id="dccc3-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="dccc3-142">De afschrijving voor de eerste drie jaar wordt in de volgende tabel weergegeven.</span><span class="sxs-lookup"><span data-stu-id="dccc3-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="dccc3-143">Periode</span><span class="sxs-lookup"><span data-stu-id="dccc3-143">Period</span></span> | <span data-ttu-id="dccc3-144">Berekening van het jaarlijkse afschrijvingsbedrag</span><span class="sxs-lookup"><span data-stu-id="dccc3-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="dccc3-145">Nettoboekwaarde aan het einde van het jaar</span><span class="sxs-lookup"><span data-stu-id="dccc3-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="dccc3-146">Jaar 1</span><span class="sxs-lookup"><span data-stu-id="dccc3-146">Year 1</span></span> | <span data-ttu-id="dccc3-147">(11.000 - 1000) \* 30% = 3000</span><span class="sxs-lookup"><span data-stu-id="dccc3-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="dccc3-148">(11 000 - 1000) - 3000 = 7000</span><span class="sxs-lookup"><span data-stu-id="dccc3-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="dccc3-149">Jaar 2</span><span class="sxs-lookup"><span data-stu-id="dccc3-149">Year 2</span></span> | <span data-ttu-id="dccc3-150">(7000 - 1000) \* 30% = 1800</span><span class="sxs-lookup"><span data-stu-id="dccc3-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="dccc3-151">(7000 -1800) = 5200</span><span class="sxs-lookup"><span data-stu-id="dccc3-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="dccc3-152">Jaar 3</span><span class="sxs-lookup"><span data-stu-id="dccc3-152">Year 3</span></span> | <span data-ttu-id="dccc3-153">(5200 - 1000) \* 30% = 1260</span><span class="sxs-lookup"><span data-stu-id="dccc3-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="dccc3-154">(5200 - 1260) = 3940</span><span class="sxs-lookup"><span data-stu-id="dccc3-154">(5,200 - 1,260) = 3,940</span></span>               |


-






