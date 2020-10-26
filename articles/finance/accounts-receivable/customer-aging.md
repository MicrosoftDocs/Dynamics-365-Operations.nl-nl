---
title: Naar ouderdom gerangschikt rapport voor klanten
description: In het naar ouderdom gerangschikt rapport voor klanten worden de saldi weergegeven die door klanten verschuldigd zijn, gesorteerd op datuminterval of ouderdomsperiode.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 062e8972c879d770cc4106c2811cd4c16fff0446
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974856"
---
# <a name="customer-aging-report"></a><span data-ttu-id="fc973-103">Naar ouderdom gerangschikt rapport voor klanten</span><span class="sxs-lookup"><span data-stu-id="fc973-103">Customer aging report</span></span> 

<span data-ttu-id="fc973-104">In het **naar ouderdom gerangschikt** rapport voor klanten worden de saldi weergegeven die door klanten verschuldigd zijn, gesorteerd op datuminterval of ouderdomsperiode.</span><span class="sxs-lookup"><span data-stu-id="fc973-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="fc973-105">Wanneer u dit rapport genereert, worden de volgende standaardparameters weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fc973-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="fc973-106">U kunt deze parameters gebruiken om de gegevens te filteren die in het rapport worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fc973-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="fc973-107">Zie [Verzamelingen instellen](set-up-collections.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="fc973-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc973-108">Veld</span><span class="sxs-lookup"><span data-stu-id="fc973-108">Field</span></span></p></th>
<th><p><span data-ttu-id="fc973-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="fc973-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc973-110"><strong>Factureringsclassificatie</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-111">Selecteer een of meer factureringsclassificaties die u in het rapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="fc973-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="fc973-112">**Opmerking**: dit besturingselement is alleen beschikbaar als de configuratiesleutel <STRONG>Openbare sector</STRONG> is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fc973-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc973-113"><strong>Transacties opnemen zonder een factureringsclassificatie</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-114">Als dit selectievakje is ingeschakeld, worden alle transacties waaraan geen factureringsclassificatie is toegewezen, weergegeven in het rapport.</span><span class="sxs-lookup"><span data-stu-id="fc973-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="fc973-115">**Opmerking**: dit besturingselement is alleen beschikbaar als de configuratiesleutel <STRONG>Openbare sector</STRONG> is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fc973-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc973-116"><strong>Ouderdom vanaf</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-117">Voer de datum in die wordt gebruikt in de huidige ouderdomsperiode.</span><span class="sxs-lookup"><span data-stu-id="fc973-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc973-118"><strong>Saldo per</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-119">Voer de datum in waarvoor de klantsaldi moeten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fc973-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="fc973-120">Deze datum staat ook bekend als de afsluitdatum voor transacties.</span><span class="sxs-lookup"><span data-stu-id="fc973-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc973-121"><strong>Begindatum</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-122">Voer een datum in die binnen het eerste periode-interval of de ouderdomsperiode valt die in het rapport moet worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="fc973-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc973-123"><strong>Criteria</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-124">Selecteer het type datum waarop u het rapport wilt baseren.</span><span class="sxs-lookup"><span data-stu-id="fc973-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="fc973-125"><strong>Transactiedatum</strong>: de boekingsdatum van de transacties.</span><span class="sxs-lookup"><span data-stu-id="fc973-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="fc973-126">Dit kan bijvoorbeeld een factuurdatum zijn die de basis vormt voor de berekening van de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="fc973-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="fc973-127"><strong>Vervaldatum</strong>: de vervaldatum van de transacties die is gebaseerd op de betalingsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="fc973-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="fc973-128"><strong>Documentdatum</strong>: een datum van het door de gebruiker gedefinieerde document, die wordt gebruikt als basis voor het berekenen van de vervaldatum.</span><span class="sxs-lookup"><span data-stu-id="fc973-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc973-129"><strong>Definitie van ouderdomsperiode</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-130">Selecteer een ouderdomsperiodedefinitie.</span><span class="sxs-lookup"><span data-stu-id="fc973-130">Select an aging period definition.</span></span> <span data-ttu-id="fc973-131">Het veld <strong>Interval</strong> wordt niet gebruikt als u een ouderdomsperiodedefinitie selecteert.</span><span class="sxs-lookup"><span data-stu-id="fc973-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="fc973-132">Ouderdomsperiodedefinities met meer dan zes ouderdomsperioden kunnen niet worden gebruikt in het afgedrukte rapport.</span><span class="sxs-lookup"><span data-stu-id="fc973-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="fc973-133">**Opmerking**: u kunt ouderdomsperioden instellen op de pagina <STRONG>Ouderdomsperiodedefinities</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="fc973-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc973-134"><strong>Omschrijving van ouderdomsperiode afdrukken</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-135">Selecteer <strong>Ja</strong> om omschrijvingen van ouderdomsperioden boven aan elke ouderdomsperiodekolom in het rapport op te nemen.</span><span class="sxs-lookup"><span data-stu-id="fc973-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="fc973-136">Selecteer <strong>Nee</strong> om het rapport zonder kolomkoppen af te drukken.</span><span class="sxs-lookup"><span data-stu-id="fc973-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc973-137"><strong>Interval</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-138">Definieer de gewenste periode door het aantal dag- of maandeenheden in elke periode in te voeren.</span><span class="sxs-lookup"><span data-stu-id="fc973-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="fc973-139">On bijvoorbeeld de naar ouderdom gerangschikte informatie per week te bekijken, voert u een 7 in dit veld in en selecteert u <strong>Dag</strong> in het veld <strong>Dag/maand</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc973-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="fc973-140">**Opmerking:** de informatie die u in dit veld invoert, wordt alleen gebruikt als u geen ouderdomsperiodedefinitie hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fc973-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="fc973-141">Anders wordt de afdrukrichting gedefinieerd in de ouderdomsperiodedefinitie.</span><span class="sxs-lookup"><span data-stu-id="fc973-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc973-142"><strong>Dag/mnd.</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-143">Selecteer de eenheid, <strong>Dag</strong> of <strong>Maand</strong>, waarmee de periode wordt gedefinieerd in het veld <strong>Interval</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc973-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc973-144"><strong>Afdrukrichting</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-145">Geef aan of saldi moeten worden berekend en het naar ouderdom gerangschikte rapport moet worden afgedrukt voor perioden in het verleden of in de toekomst.</span><span class="sxs-lookup"><span data-stu-id="fc973-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="fc973-146">De datums zijn relatief ten opzichte van de datum die in het veld <strong>Saldo vanaf</strong> is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fc973-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="fc973-147">Selecteer <strong>Achterwaarts</strong> om informatie voor perioden in het verleden weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fc973-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="fc973-148">Selecteer <strong>Voorwaarts</strong> om informatie voor perioden in de toekomst weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fc973-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>

<span data-ttu-id="fc973-149">**Opmerking:** de informatie die u in dit veld invoert, wordt alleen gebruikt als u geen ouderdomsperiodedefinitie hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="fc973-149">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc973-150"><strong>Gegevens</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-151">Selecteer deze optie om transacties weer te geven die zijn opgenomen in de saldi die in het rapport worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fc973-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc973-152"><strong>Bedragen in transactievaluta opnemen</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-153">Selecteer deze optie om bedragen in de transactievaluta op te nemen naast bedragen in de valuta voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="fc973-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="fc973-154">Als dit selectievakje niet is ingeschakeld, worden de bedragen in het rapport alleen in de valuta voor boekhouding weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fc973-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc973-155"><strong>Negatief saldo</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-156">Selecteer deze optie om klantrekeningen met negatieve saldi op te nemen.</span><span class="sxs-lookup"><span data-stu-id="fc973-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc973-157"><strong>Rekeningen met nulsaldo uitsluiten</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-158">Selecteer deze optie om klantrekeningen met een nulsaldo uit te sluiten.</span><span class="sxs-lookup"><span data-stu-id="fc973-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc973-159"><strong>Betalingspositionering</strong></span><span class="sxs-lookup"><span data-stu-id="fc973-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="fc973-160">Selecteer deze optie om betalingen weer te geven die niet zijn vereffend.</span><span class="sxs-lookup"><span data-stu-id="fc973-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="fc973-161">Deze worden in de eerste kolom van het rapport weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fc973-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

