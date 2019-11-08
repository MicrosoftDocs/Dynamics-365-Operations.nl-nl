---
title: Btw-berekeningsmethoden in het veld Oorsprong
description: Dit artikel beschrijft de opties in het veld Oorsprong op de btw-codespagina en hoe de btw op basis van de geselecteerde optie voor een btw-code wordt berekend.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37bb02dfc9cfcb3e2c1dcda446be3945563d6594
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570575"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="b48d1-103">Btw-berekeningsmethoden in het veld Oorsprong</span><span class="sxs-lookup"><span data-stu-id="b48d1-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b48d1-104">Dit artikel beschrijft de opties in het veld Oorsprong op de btw-codespagina en hoe de btw op basis van de geselecteerde optie voor een btw-code wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="b48d1-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="b48d1-105">Voor elke btw-code die u in de pagina Btw-codes maakt, selecteert u welke berekeningsmethode moet worden toegepast op het btw-basisbedrag in het veld Oorsprong.</span><span class="sxs-lookup"><span data-stu-id="b48d1-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="b48d1-106">Percentage van nettobedrag</span><span class="sxs-lookup"><span data-stu-id="b48d1-106">Percentage of net amount</span></span>
<span data-ttu-id="b48d1-107">Het berekeningsmethode Percentage van nettobedrag is de standaardwaarde in het veld Oorsprong.</span><span class="sxs-lookup"><span data-stu-id="b48d1-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="b48d1-108">De btw wordt berekend als een percentage van het aankoop- of verkoopbedrag, exclusief eventuele andere btw.</span><span class="sxs-lookup"><span data-stu-id="b48d1-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="b48d1-109">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="b48d1-109">Example</span></span>

<span data-ttu-id="b48d1-110">Het btw-tarief is 25%.</span><span class="sxs-lookup"><span data-stu-id="b48d1-110">The tax rate is 25%.</span></span> <span data-ttu-id="b48d1-111">De factuurregel bevat een hoeveelheid van 10 artikelen voor € 1,00 per stuk en de klant heeft recht op een regelkorting van 10%.</span><span class="sxs-lookup"><span data-stu-id="b48d1-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="b48d1-112">Nettobedrag: (10 x 1,00) -10% = 9,00 Btw: 9,00 x 25% = 2,25 Totaalbedrag: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="b48d1-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="b48d1-113"> Percentage van brutobedrag</span><span class="sxs-lookup"><span data-stu-id="b48d1-113">Percentage of gross amount</span></span>
<span data-ttu-id="b48d1-114">Als u de methode Percentage van brutobedrag selecteert, wordt de btw berekend als een percentage van het brutoverkoopbedrag.</span><span class="sxs-lookup"><span data-stu-id="b48d1-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="b48d1-115">Het brutobedrag is het regelnettobedrag plus alle belastingen en bijzondere kosten voor de regel behalve de ene belasting met Oorsprong = Percentage van brutobedrag.</span><span class="sxs-lookup"><span data-stu-id="b48d1-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="b48d1-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="b48d1-116">Example</span></span>

<span data-ttu-id="b48d1-117">De belastingdienst heeft een artikel met speciale heffingen belast.</span><span class="sxs-lookup"><span data-stu-id="b48d1-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="b48d1-118">De heffingsbedragen worden toegevoegd aan het nettobedrag voordat de btw wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="b48d1-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="b48d1-119">Uitgaande van de volgende btw-codes:</span><span class="sxs-lookup"><span data-stu-id="b48d1-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="b48d1-120">HEFFING 1 = 10%, met de berekeningsmethode Percentage van nettobedrag</span><span class="sxs-lookup"><span data-stu-id="b48d1-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="b48d1-121">HEFFING 2 = 20%, met de berekeningsmethode Percentage van nettobedrag</span><span class="sxs-lookup"><span data-stu-id="b48d1-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="b48d1-122">BTW = 25%, met de berekeningsmethode Percentage van brutobedrag</span><span class="sxs-lookup"><span data-stu-id="b48d1-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="b48d1-123">Is het nettobedrag 10,00, dan HEFFING 1 = 1,00 (10,00 x 10%) en HEFFING 2 = 2,00 (10,00 x 20%).</span><span class="sxs-lookup"><span data-stu-id="b48d1-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="b48d1-124">De bedragen zijn als volgt: Brutobedrag: nettobedrag + HEFFING 1 bedrag + HEFFING 2 bedrag (10,00 + 1,00 + 2,00) = 13,00 BTW = 13,00 x 25% = 3,25 Totaal HEFFINGEN en BTW: 1,00 + 2,00 + 3,25 = 6,25 Totaalbedrag: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="b48d1-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="b48d1-125">**Opmerking**</span><span class="sxs-lookup"><span data-stu-id="b48d1-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b48d1-126">Slechts één btw-code met Oorsprong = Percentage van brutobedrag kan voor een transactie worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b48d1-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="b48d1-127">Als meerdere dergelijke btw-codes voor een transactie worden gedefinieerd wordt een fout weergegeven dat de btw niet kan worden berekend.</span><span class="sxs-lookup"><span data-stu-id="b48d1-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="b48d1-128">Btw-percentage</span><span class="sxs-lookup"><span data-stu-id="b48d1-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="b48d1-129">Als u Btw-percentage selecteert in het veld Oorsprong, wordt de btw berekend als het percentage van de btw dat is geselecteerd in het veld Btw op btw.</span><span class="sxs-lookup"><span data-stu-id="b48d1-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="b48d1-130">De btw die in het veld Btw op btw is geselecteerd, wordt eerst berekend.</span><span class="sxs-lookup"><span data-stu-id="b48d1-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="b48d1-131">De tweede btw wordt berekend op basis van het eerste btw-bedrag.</span><span class="sxs-lookup"><span data-stu-id="b48d1-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="b48d1-132">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="b48d1-132">Example</span></span>

<span data-ttu-id="b48d1-133">Uitgaande van de volgende btw-codes:</span><span class="sxs-lookup"><span data-stu-id="b48d1-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="b48d1-134">HEFFING 1 = 10%, met de methode Percentage van nettobedrag</span><span class="sxs-lookup"><span data-stu-id="b48d1-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="b48d1-135">HEFFING 2 = 20%, waarbij de methode Btw-percentage is gebruikt, met Heffing 1 in het veld Btw op btw</span><span class="sxs-lookup"><span data-stu-id="b48d1-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="b48d1-136">BTW = 25%, met de methode Percentage van brutobedrag</span><span class="sxs-lookup"><span data-stu-id="b48d1-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="b48d1-137">Nettobedrag: 10,00 HEFFING 1: 10,00 x 10% = 1,00 HEFFING 2: 1,00 x 20% = 0,20 Brutobedrag: 10,00 + 1,00 + 0,20 = 11,20 BTW: 11,20 x 25% = 2,80 Totaal HEFFINGEN en BTW: 1,00 + 0,20 + 2,80 = 4,00 Totaalbedrag: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="b48d1-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="b48d1-138">**Opmerking**</span><span class="sxs-lookup"><span data-stu-id="b48d1-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b48d1-139">Belasting op meerdere niveaus in belastingberekeningen is niet mogelijk.</span><span class="sxs-lookup"><span data-stu-id="b48d1-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="b48d1-140">Een belasting kan niet worden berekend op basis van een belasting die al op basis van een andere belasting wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="b48d1-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="b48d1-141">Er kunnen meerdere één-niveau-belastingen op btw-codes worden berekend voor een transactie.</span><span class="sxs-lookup"><span data-stu-id="b48d1-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="b48d1-142"> Bedrag per eenheid</span><span class="sxs-lookup"><span data-stu-id="b48d1-142">Amount per unit</span></span>
<span data-ttu-id="b48d1-143">Wanneer u Bedrag per eenheid in het veld Oorsprong selecteert, wordt de btw als vast bedrag per eenheid berekend, vermenigvuldigd met de hoeveelheid die op de documentregel wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="b48d1-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="b48d1-144">De eenheid moet worden geselecteerd in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="b48d1-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="b48d1-145">Het bedrag per eenheid wordt opgegeven in de pagina Waarden btw-code.</span><span class="sxs-lookup"><span data-stu-id="b48d1-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="b48d1-146">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="b48d1-146">Example</span></span>

<span data-ttu-id="b48d1-147">Btw-code is ingesteld als: USD 1,20 per eenheid = doos Op een verkoopfactuurregel worden 25 dozen van een artikel verkocht Btw wordt berekend als 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="b48d1-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="b48d1-148">**Opmerking**</span><span class="sxs-lookup"><span data-stu-id="b48d1-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b48d1-149">Als de transactie in een andere eenheid wordt ingevoerd dan de eenheid die is opgegeven voor de btw-code, wordt deze automatisch omgezet op basis van de eenheidsomrekeningen die in de pagina Eenheidsomrekeningen zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="b48d1-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="b48d1-150"> Bedrag per eenheid, extra optie</span><span class="sxs-lookup"><span data-stu-id="b48d1-150">Amount per unit, additional option</span></span>

<span data-ttu-id="b48d1-151">Op het tabblad Berekening kunt u selecteren of een als bedrag per eenheid berekende btw wordt berekend vóór andere btw-codes en opgeteld bij het nettobedrag voordat andere btw-codes met Oorsprong = Percentage van nettobedrag worden berekend.</span><span class="sxs-lookup"><span data-stu-id="b48d1-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="b48d1-152">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="b48d1-152">Examples</span></span>

<span data-ttu-id="b48d1-153">Stel we berekenen 2 btw-codes voor een transactie:</span><span class="sxs-lookup"><span data-stu-id="b48d1-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="b48d1-154">HEFFING: Oorsprong = Bedrag per eenheid en een btw, de waarde is ingesteld op 5,00 per eenheid = stks</span><span class="sxs-lookup"><span data-stu-id="b48d1-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="b48d1-155">BTW: Oorsprong = als getoond in de onderstaande voorbeelden, de waarde is ingesteld op 25%</span><span class="sxs-lookup"><span data-stu-id="b48d1-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="b48d1-156">We verkopen 1 stuks van een artikel met een eenheidsprijs van 10,00</span><span class="sxs-lookup"><span data-stu-id="b48d1-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="b48d1-157">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="b48d1-157">Example 1</span></span>

<span data-ttu-id="b48d1-158">BTW: Oorsprong = methode Percentage van brutobedrag De optie Berekenen vóór btw heeft geen invloed, omdat BTW wordt berekend als een percentage van het brutobedrag.</span><span class="sxs-lookup"><span data-stu-id="b48d1-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="b48d1-159">HEFFING: 1 x 5,00 = 5,00 Brutobedrag: 10,00 + 5,00 = 15,00 BTW: 15,00 x 25% = 3,75 Totaal btw: 5,00 + 3,75 = 8,75 Totaal bedrag: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="b48d1-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="b48d1-160">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="b48d1-160">Example 2</span></span>

<span data-ttu-id="b48d1-161">BTW: Oorsprong = Percentage van nettobedrag De optie Berekenen vóór btw is niet geselecteerd voor de HEFFING-berekening.</span><span class="sxs-lookup"><span data-stu-id="b48d1-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="b48d1-162">Nettobedrag: 10,00 HEFFING: 1 x 5,00 = 5,00 BTW: 10,00 x 25% = 2,50 Totale btw: 5,00 + 2,50 = 7,50 Totaal bedrag: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="b48d1-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="b48d1-163">Voorbeeld 3</span><span class="sxs-lookup"><span data-stu-id="b48d1-163">Example 3</span></span>

<span data-ttu-id="b48d1-164">BTW: Oorsprong = Percentage van nettobedrag De optie Berekenen vóór btw is geselecteerd voor de HEFFING-berekening.</span><span class="sxs-lookup"><span data-stu-id="b48d1-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="b48d1-165">Nettobedrag: 10,00 HEFFING: 1 x 5,00 = 5,00 BTW: (10,00 + 5,00) x 25% = 3,75 Totale btw: 5,00 + 3,75 = 8,75 Totaal bedrag: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="b48d1-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="b48d1-166">Voorbeeld 4</span><span class="sxs-lookup"><span data-stu-id="b48d1-166">Example 4</span></span>

<span data-ttu-id="b48d1-167">Het resultaat van voorbeeld 1 en 3 is gelijk, omdat er slechts één heffing wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b48d1-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="b48d1-168">Stel dat u twee HEFFINGEN hebt en dat slechts één is opgenomen in het nettobedrag voor de btw-berekening: HEFFING 1: 5,00, met de methode Bedrag per eenheid, en de optie Berekenen vóór btw is geselecteerd HEFFING 2: 2,50, met de methode Bedrag per eenheid, en de optie Berekenen vóór btw is niet geselecteerd Btw: 25%, met de methode Percentage van nettobedrag Nettobedrag: 10,00 HEFFING 1: 1 x 5,00 = 5,00 HEFFING 2: 1 x 2,50 = 2,50 Nettobedrag onderhevig aan btw: 10,00 + 5,00 = 15,00 BTW: 15,00 x 25% = 3,75 Totale btw, inclusief heffingen: 5,00 + 2,50 + 3,75 = 11,25 Totaal bedrag: 10,00 + 11,25 = 21,25 De 25% BTW wordt berekend voor de som van het nettobedrag (10,00) + HEFFING 1 (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="b48d1-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="b48d1-169">HEFFING 2 wordt aan het btw-bedrag toegevoegd nadat de btw is berekend.</span><span class="sxs-lookup"><span data-stu-id="b48d1-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="b48d1-170"> Berekende percentage van het nettobedrag</span><span class="sxs-lookup"><span data-stu-id="b48d1-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="b48d1-171">Het berekende percentage van het nettobedrag verwerkt de btw-berekening verschillend, afhankelijk van de instelling van de parameter Bedragen inclusief BTW voor het document of journaal.</span><span class="sxs-lookup"><span data-stu-id="b48d1-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="b48d1-172">Voorbeeld 1</span><span class="sxs-lookup"><span data-stu-id="b48d1-172">Example 1</span></span>

<span data-ttu-id="b48d1-173">Document / journaal is ingesteld op Bedragen inclusief BTW = Ja Transactieregelbedrag: 10,00 Btw-tarief: 25% BTW: Transactieregelbedrag x btw-tarief (10,00 x 25%) = 2,50 Basisbedrag belasting (oorsprongbedrag): Transactieregelbedrag - Btw (10,00 - 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="b48d1-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="b48d1-174">Voorbeeld 2</span><span class="sxs-lookup"><span data-stu-id="b48d1-174">Example 2</span></span>

<span data-ttu-id="b48d1-175">Document / journaal is ingesteld op Bedragen inclusief BTW = Nee Transactieregelbedrag: 10,00 Btw-tarief: 25% BTW: (Transactieregelbedrag x btw-tarief) / (100 - btw-tarief) (10,00 x 25%) / (100% - 25%) = 3,33 Basisbedrag belasting (oorsprongbedrag): Transactieregelbedrag = 10,00</span><span class="sxs-lookup"><span data-stu-id="b48d1-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="b48d1-176">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b48d1-176">Additional resources</span></span>
--------

[<span data-ttu-id="b48d1-177">Btw-tarieven bepalen op basis van de velden Marginale basis en Berekeningsmethode</span><span class="sxs-lookup"><span data-stu-id="b48d1-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="b48d1-178">Berekeningsopties Volledige bedrag en Interval voor btw-codes</span><span class="sxs-lookup"><span data-stu-id="b48d1-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)



