---
title: INTERVAT-belastingaangifte
description: Dit onderwerp biedt land-/regiospecifieke informatie over het instellen en maken van de INTERVAT-belastingaangifte voor rechtspersonen in alleen België.
author: anasyash
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxIntervat
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 273023
ms.search.region: Belgium
ms.author: v-oloski
ms.dyn365.ops.version: AX 7.0.1
ms.search.validFrom: 2016-05-31
ms.openlocfilehash: ac59959451bf4267d1347db29d3326605c9121e6
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621338"
---
# <a name="intervat-tax-declaration"></a><span data-ttu-id="e434a-103">INTERVAT-belastingaangifte</span><span class="sxs-lookup"><span data-stu-id="e434a-103">INTERVAT tax declaration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e434a-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="e434a-104">Overview</span></span>

<span data-ttu-id="e434a-105">Dit onderwerp biedt land-/regiospecifieke informatie over het instellen en maken van de INTERVAT-belastingaangifte voor rechtspersonen in België.</span><span class="sxs-lookup"><span data-stu-id="e434a-105">This topic provides country/region-specific information about how to set up and create the INTERVAT tax declaration for legal entities in Belgium.</span></span>

<span data-ttu-id="e434a-106">U kunt de INTERVAT-btw-aangifte als een XML-bestand maken.</span><span class="sxs-lookup"><span data-stu-id="e434a-106">You can create the INTERVAT tax declaration as an XML file.</span></span> <span data-ttu-id="e434a-107">U kunt ook een voorbeeld weergeven van de bedragen van de btw-aangifte in een afdrukbare indeling.</span><span class="sxs-lookup"><span data-stu-id="e434a-107">You can also preview the amounts of the value-added tax (VAT) declaration in a printable format.</span></span>

<span data-ttu-id="e434a-108">De INTERVAT-aangifte die u maakt, omvat btw-transacties uit de huidige periode.</span><span class="sxs-lookup"><span data-stu-id="e434a-108">The INTERVAT declaration that you create includes tax transactions from the current period.</span></span> <span data-ttu-id="e434a-109">Het kan ook correcties van de vorige periode bevatten als een transactie is geboekt in de vorige periode nadat deze periode werd afgesloten.</span><span class="sxs-lookup"><span data-stu-id="e434a-109">It can also include corrections from the previous period, if a transaction was posted in the previous period after that period was closed.</span></span>

<span data-ttu-id="e434a-110">U kunt aanvullende informatie voor de aangifte invoeren en de gegevens handmatig corrigeren op de pagina **Aanvullende btw-rapportvakken**.</span><span class="sxs-lookup"><span data-stu-id="e434a-110">You can enter additional information for the declaration and manually correct data on the **Additional sales tax report boxes** page.</span></span> <span data-ttu-id="e434a-111">Handmatige correctie kan nodig zijn als u bijvoorbeeld het bedrag van de aangiftecode in de INTERVAT-aangifte niet kunt afdrukken omdat het bedrag negatief is.</span><span class="sxs-lookup"><span data-stu-id="e434a-111">Manual correction might be required if, for example, you can't print the amount of the reporting code in the INTERVAT declaration because the amount is negative.</span></span> <span data-ttu-id="e434a-112">Negatieve bedragen moeten worden afgetrokken van de volgende btw-aangifte en deze taak moet handmatig worden voltooid met behulp van correcties.</span><span class="sxs-lookup"><span data-stu-id="e434a-112">Negative amounts must be deducted from the next VAT declaration, and this task must be completed manually by using corrections.</span></span> <span data-ttu-id="e434a-113">Voordat u het gecorrigeerde bedrag kunt aangeven, moet u aangeven welke btw-aangiftecodes kunnen worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="e434a-113">Before you can indicate the corrected amount, you must indicate which sales tax reporting codes allow for corrections.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e434a-114">Vereisten</span><span class="sxs-lookup"><span data-stu-id="e434a-114">Prerequisites</span></span>
<span data-ttu-id="e434a-115">De volgende vereisten moeten worden ingesteld voordat u begint te werken met de INTERVAT-belastingaangifte:</span><span class="sxs-lookup"><span data-stu-id="e434a-115">The following prerequisites must be set up before you begin to work with the INTERVAT tax declaration:</span></span>

-   <span data-ttu-id="e434a-116">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="e434a-116">Legal entity</span></span>
-   <span data-ttu-id="e434a-117">Registratienummer</span><span class="sxs-lookup"><span data-stu-id="e434a-117">Registration number</span></span>
-   <span data-ttu-id="e434a-118">Gegevens contactpersoon</span><span class="sxs-lookup"><span data-stu-id="e434a-118">Contact information</span></span>
-   <span data-ttu-id="e434a-119">Nummerreeksen</span><span class="sxs-lookup"><span data-stu-id="e434a-119">Number sequences</span></span>
-   <span data-ttu-id="e434a-120">Boekingsjournaal</span><span class="sxs-lookup"><span data-stu-id="e434a-120">Posting journal</span></span>
-   <span data-ttu-id="e434a-121">Btw-dienst</span><span class="sxs-lookup"><span data-stu-id="e434a-121">Sales tax authorities</span></span>
-   <span data-ttu-id="e434a-122">Btw-aangiftecodes</span><span class="sxs-lookup"><span data-stu-id="e434a-122">Sales tax reporting codes</span></span>
-   <span data-ttu-id="e434a-123">Btw-codes</span><span class="sxs-lookup"><span data-stu-id="e434a-123">Sales tax codes</span></span>
-   <span data-ttu-id="e434a-124">Btw-nummer</span><span class="sxs-lookup"><span data-stu-id="e434a-124">Tax exempt number</span></span>

### <a name="legal-entity"></a><span data-ttu-id="e434a-125">Rechtspersoon</span><span class="sxs-lookup"><span data-stu-id="e434a-125">Legal entity</span></span>

1.  <span data-ttu-id="e434a-126">Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen** en selecteer uw rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="e434a-126">Go to **Organization administration** \> **Organizations** \> **Legal entities**, and select your legal entity.</span></span>
2.  <span data-ttu-id="e434a-127">Maak een adres op het sneltabblad **Adressen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-127">On the **Addresses** FastTab, create an address.</span></span>
3.  <span data-ttu-id="e434a-128">Selecteer in het veld **Land/regio** de waarde **België**.</span><span class="sxs-lookup"><span data-stu-id="e434a-128">In the **Country/region** field, select **Belgium**.</span></span>
4.  <span data-ttu-id="e434a-129">Vul andere adrescomponenten in en markeer het adres als **primair**.</span><span class="sxs-lookup"><span data-stu-id="e434a-129">Fill in other address components, and mark the address as **Primary**.</span></span>
5.  <span data-ttu-id="e434a-130">In het Sneltabblad **Belastingregistratie**, in het veld **BTW-registratienummer**, specificeer het BTW-registratienummer van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="e434a-130">On the **Tax registration** FastTab, in the **Tax registration number** field, specify the tax registration number for your company.</span></span>

### <a name="registration-number"></a><span data-ttu-id="e434a-131">Registratienummer</span><span class="sxs-lookup"><span data-stu-id="e434a-131">Registration number</span></span>

1.  <span data-ttu-id="e434a-132">Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-132">Go to **Organization administration** \> **Organizations** \> **Legal entities**.</span></span>
2.  <span data-ttu-id="e434a-133">Selecteer **Registratie-id's** en klik vervolgens op het tabblad **Registratie-id** op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-133">Select **Registration IDs**, and then, on the **Registration ID** tab, select **Add**.</span></span>
3.  <span data-ttu-id="e434a-134">Selecteer een waarde in het veld **Registratietype**.</span><span class="sxs-lookup"><span data-stu-id="e434a-134">In the **Registration type** field, select a value.</span></span>
4.  <span data-ttu-id="e434a-135">Voer een waarde in het veld **Registratienummer** in</span><span class="sxs-lookup"><span data-stu-id="e434a-135">In the **Registration number** field, enter a value.</span></span>
5.  <span data-ttu-id="e434a-136">Voer op het tabblad **Algemeen** een ingangsdatum in.</span><span class="sxs-lookup"><span data-stu-id="e434a-136">On the **General** tab, enter an effective date.</span></span> <span data-ttu-id="e434a-137">Zie [Registratienummer](emea-registration-ids.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e434a-137">For more information, see [Registration number](emea-registration-ids.md).</span></span>

### <a name="contact-information"></a><span data-ttu-id="e434a-138">Gegevens contactpersoon</span><span class="sxs-lookup"><span data-stu-id="e434a-138">Contact information</span></span>

1.  <span data-ttu-id="e434a-139">Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-139">Go to **Organization administration** \> **Organizations** \> **Legal entities**.</span></span>
2.  <span data-ttu-id="e434a-140">Voeg op het tabblad **Contactgegevens** regels toe voor het telefoonnummer en e-mailadres en stel deze in op **primair**.</span><span class="sxs-lookup"><span data-stu-id="e434a-140">On the **Contact information** tab, add lines for the phone number and email address, and set them to **Primary**.</span></span>

### <a name="number-sequences"></a><span data-ttu-id="e434a-141">Nummerreeksen</span><span class="sxs-lookup"><span data-stu-id="e434a-141">Number sequences</span></span>

1.  <span data-ttu-id="e434a-142">Ga naar **Grootboek** \> **Grootboek instellen** \> **Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="e434a-142">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2.  <span data-ttu-id="e434a-143">Stel op het tabblad **Nummerreeksen** nummerreeksen in voor de referenties **Id van jaarlijkse verkooplijst** en **INTERVAT-id**.</span><span class="sxs-lookup"><span data-stu-id="e434a-143">On the **Number sequences** tab, set up number sequences for the **Annual sales list ID** and **INTERVAT ID** references.</span></span>

### <a name="posting-journal"></a><span data-ttu-id="e434a-144">Boekingsjournaal</span><span class="sxs-lookup"><span data-stu-id="e434a-144">Posting journal</span></span>

1.  <span data-ttu-id="e434a-145">Ga naar **Grootboek** \> **Journaalinstellingen** \> **Boekingsjournalen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-145">Go to **General ledger** \> **Journal setup** \> **Posting journals**.</span></span>
2.  <span data-ttu-id="e434a-146">Selecteer op de pagina **Grootboekinstellingen** **Maken**.</span><span class="sxs-lookup"><span data-stu-id="e434a-146">On the **Journal setup** page, select **Create**.</span></span> <span data-ttu-id="e434a-147">De boekstukreeks wordt automatisch gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e434a-147">The voucher series is automatically created.</span></span>

### <a name="sales-tax-authorities"></a><span data-ttu-id="e434a-148">Btw-dienst</span><span class="sxs-lookup"><span data-stu-id="e434a-148">Sales tax authorities</span></span>

1.  <span data-ttu-id="e434a-149">Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw-dienst**.</span><span class="sxs-lookup"><span data-stu-id="e434a-149">Go to **Tax** \> **Indirect taxes** \> **Sales tax authorities**.</span></span>
2.  <span data-ttu-id="e434a-150">Controleer of het veld **Rapportindeling** moet worden ingesteld op **Indeling van Belgische aangifte**.</span><span class="sxs-lookup"><span data-stu-id="e434a-150">Verify that the **Report layout** field is set to **Belgium report layout**.</span></span>

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="e434a-151">Btw-aangiftecodes</span><span class="sxs-lookup"><span data-stu-id="e434a-151">Sales tax reporting codes</span></span>

-   <span data-ttu-id="e434a-152">Ga naar **Belasting** \> **Instellen** \> **Btw** \> **Btw-aangiftecodes** en maak nieuwe btw-aangiftecodes.</span><span class="sxs-lookup"><span data-stu-id="e434a-152">Go to **Tax** \> **Setup** \> **Sales tax** \> **Sales tax reporting codes**, and create new sales tax reporting codes.</span></span>

<span data-ttu-id="e434a-153">Als het veld **Btw-correctie** is ingeschakeld voor een btw-aangiftecode, is die code beschikbaar voor selectie op de pagina **Aanvullende btw-rapportvakken**.</span><span class="sxs-lookup"><span data-stu-id="e434a-153">If the **Sales tax correction** check box is selected for a sales tax reporting code, that code is available for selection on the **Additional sales tax report boxes** page.</span></span>

<span data-ttu-id="e434a-154">Voorbeelden van btw-aangiftecodes worden gegeven in het gedeelte [Btw-aangiftecodes instellen](#set-up-sales-tax-reporting-codes), verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="e434a-154">Examples of sales tax reporting code are provided in the [Set up sales tax reporting codes](#set-up-sales-tax-reporting-codes) section later in this topic.</span></span>

### <a name="sales-tax-codes"></a><span data-ttu-id="e434a-155">Btw-codes</span><span class="sxs-lookup"><span data-stu-id="e434a-155">Sales tax codes</span></span>

1.  <span data-ttu-id="e434a-156">Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="e434a-156">Go to **Tax** \> **Indirect taxes** \> **Sales tax codes**.</span></span>
2.  <span data-ttu-id="e434a-157">Voeg informatie toe of selecteer deze op de tabbladen **Rapport** en **Rapport – creditnota**.</span><span class="sxs-lookup"><span data-stu-id="e434a-157">Add or select information in the fields on the **Report** and **Report – credit note** tabs.</span></span>
3.  <span data-ttu-id="e434a-158">Selecteer de vereiste waarden in het raster **Btw-aangiftecodes**.</span><span class="sxs-lookup"><span data-stu-id="e434a-158">Select the required values in the **Sales tax reporting codes** grid.</span></span>

### <a name="tax-exempt-number"></a><span data-ttu-id="e434a-159">Btw-nummer</span><span class="sxs-lookup"><span data-stu-id="e434a-159">Tax exempt number</span></span>

1.  <span data-ttu-id="e434a-160">Ga naar **Belasting** \> **Instellen** \> **Btw** \> **Btw-vrijstellingsnummers**.</span><span class="sxs-lookup"><span data-stu-id="e434a-160">Go to **Tax** \> **Setup** \> **Sales tax** \> **Tax exempt numbers**.</span></span>
2.  <span data-ttu-id="e434a-161">Maak voor elk btw-vrijstellingsnummer een record die de volgende informatie bevat:</span><span class="sxs-lookup"><span data-stu-id="e434a-161">For each tax-exempt number, create a record that includes the followinginformation:</span></span>

    -   <span data-ttu-id="e434a-162">Selecteer in het veld **Land/regio** de btw registratie van de andere partij.</span><span class="sxs-lookup"><span data-stu-id="e434a-162">In the **Country/region** field, select the tax registration of the counterparty.</span></span>
    -   <span data-ttu-id="e434a-163">Voer in het veld **Btw-vrijstellingsnummer** het btw-vrijstellingsnummer van de andere partij in.</span><span class="sxs-lookup"><span data-stu-id="e434a-163">In the **Tax exempt number** field, enter the tax-exempt number of the counterparty.</span></span>
    -   <span data-ttu-id="e434a-164">Voer in het veld **Bedrijfsnaam** de naam van de andere partij in.</span><span class="sxs-lookup"><span data-stu-id="e434a-164">In the **Company name** field, enter the name of the counterparty.</span></span>

<span data-ttu-id="e434a-165">Zie [Btw-aangifte voor Europa](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/localizations/emea-vat-reporting.md) voor meer informatie over het opstellen van het btw-overzicht.</span><span class="sxs-lookup"><span data-stu-id="e434a-165">For more information about how to set up the VAT statement, see [VAT reporting for Europe](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/localizations/emea-vat-reporting.md).</span></span>

## <a name="settings"></a><span data-ttu-id="e434a-166">Instellingen</span><span class="sxs-lookup"><span data-stu-id="e434a-166">Settings</span></span>

### <a name="set-up-intervat"></a><span data-ttu-id="e434a-167">INTERVAT instellen</span><span class="sxs-lookup"><span data-stu-id="e434a-167">Set up INTERVAT</span></span>

<span data-ttu-id="e434a-168">Maak regels op de pagina **INTERVAT-instellingen** (**Belasting \> Instellen \> Btw \> INTERVAT-instellingen**).</span><span class="sxs-lookup"><span data-stu-id="e434a-168">Create lines on the **INTERVAT setup** page (**Tax \> Setup \> Sales tax \> INTERVAT setup**).</span></span> <span data-ttu-id="e434a-169">De informatie die u op deze pagina invoert wordt gebruikt wanneer u **Website openen** selecteert op de pagina **INTERVAT-belastingaangifte**.</span><span class="sxs-lookup"><span data-stu-id="e434a-169">The information that you enter on this page is used when you select **Open Web site** on the **INTERVAT tax declaration** page.</span></span> <span data-ttu-id="e434a-170">U moet voor elke taal een element maken.</span><span class="sxs-lookup"><span data-stu-id="e434a-170">You should create an element for each language.</span></span> <span data-ttu-id="e434a-171">Stel de volgende velden in: **Taal**, **Beschrijving** en **URL**.</span><span class="sxs-lookup"><span data-stu-id="e434a-171">Set the following fields: **Language**, **Description**, and **URL**.</span></span>

![Pagina Intervat-instellingen](media/1_Intervat_setup.png)

### <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="e434a-173">Btw-aangiftecodes instellen</span><span class="sxs-lookup"><span data-stu-id="e434a-173">Set up sales tax reporting codes</span></span>

<span data-ttu-id="e434a-174">Zie voor meer informatie over het instellen van btw-aangiftecodes [Btw-aangiftecodes instellen](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/general-ledger/tasks/set-up-sales-tax-reporting-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e434a-174">For information about how to set up sales tax reporting codes, see [Set up sales tax reporting codes](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/general-ledger/tasks/set-up-sales-tax-reporting-codes.md).</span></span>

<span data-ttu-id="e434a-175">Als gebruikers een aangiftecode handmatig kunnen corrigeren, schakelt u het selectievakje **Btw-correcties** in.</span><span class="sxs-lookup"><span data-stu-id="e434a-175">If users are allowed to manually correct a reporting code, select the **Tax corrections** check box.</span></span> <span data-ttu-id="e434a-176">De volgende tabel bevat een voorbeeld van btw-aangiftecodes voor België.</span><span class="sxs-lookup"><span data-stu-id="e434a-176">The following table provides an example of sales tax reporting codes for Belgium.</span></span>

<table width="100%">
<thead>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-177"><strong>Code en corresponderend vakje in de btw-aangifte</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-177"><strong>Code and corresponding box in the VAT declaration</strong></span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-178"><strong>Beschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-178"><strong>Description</strong></span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-179"><strong>Basis/btw</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-179"><strong>Base/tax</strong></span></span></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><span data-ttu-id="e434a-180"><strong>Sectie II. Uitvoer</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-180"><strong>Section II. Outputs</strong></span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-181">100 (vak 00)</span><span class="sxs-lookup"><span data-stu-id="e434a-181">100 (Box 00)</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-182">Verkopen die aan een speciale verordening zijn onderworpen.</span><span class="sxs-lookup"><span data-stu-id="e434a-182">Sales that are subject to a special regulation.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-183">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-183">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-184">01</span><span class="sxs-lookup"><span data-stu-id="e434a-184">01</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-185">Belastbare leveringen en diensten met een btw-tarief van 6 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-185">Taxable supplies and services at a sales tax rate of 6 percent.</span></span></p>
<p><span data-ttu-id="e434a-186">De levering van een product of service met een btw-tarief van 6 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-186">The delivery of a product or service transactions at a sales tax rate of 6 percent.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-187">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-187">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-188">02</span><span class="sxs-lookup"><span data-stu-id="e434a-188">02</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-189">Belastbare leveringen en diensten met een btw-tarief van 12 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-189">Taxable supplies and services at a sales tax rate of 12 percent.</span></span></p>
<p><span data-ttu-id="e434a-190">De levering van een product of service met een btw-tarief van 12 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-190">The delivery of a product or service transactions at a sales tax rate of 12 percent.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-191">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-191">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-192">03</span><span class="sxs-lookup"><span data-stu-id="e434a-192">03</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-193">Belastbare leveringen en diensten met een btw-tarief van 21 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-193">Taxable supplies and services at a sales tax rate of 21 percent.</span></span></p>
<p><span data-ttu-id="e434a-194">De levering van een product of service met een btw-tarief van 21 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-194">The delivery of a product or service transactions at a sales tax rate of 21 percent.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-195">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-195">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-196">44</span><span class="sxs-lookup"><span data-stu-id="e434a-196">44</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-197">Services waarvoor de contractpartner buitenlandse btw verschuldigd is.</span><span class="sxs-lookup"><span data-stu-id="e434a-197">Services that the contractual partner owes foreign VAT for.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-198">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-198">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-199">45</span><span class="sxs-lookup"><span data-stu-id="e434a-199">45</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-200">Omzet waarover de contractpartner btw verschuldigd is.</span><span class="sxs-lookup"><span data-stu-id="e434a-200">Turnover that the contractual partner owes VAT for.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-201">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-201">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-202">46</span><span class="sxs-lookup"><span data-stu-id="e434a-202">46</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-203">Intracommunautaire levering van goederen en soortgelijke transacties (verzendingen).</span><span class="sxs-lookup"><span data-stu-id="e434a-203">Intra-community supply of goods and similar transactions (shipments).</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-204">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-204">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-205">47</span><span class="sxs-lookup"><span data-stu-id="e434a-205">47</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-206">Overige verkoop zonder btw en andere verkoop die in het buitenland wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e434a-206">Other tax-free sales and other sales that are generated abroad.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-207">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-207">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-208">48</span><span class="sxs-lookup"><span data-stu-id="e434a-208">48</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-209">Bedrag van de verzonden creditnota's en negatieve correcties die zijn gerelateerd aan de verkoop uit vakken 44 en 46.</span><span class="sxs-lookup"><span data-stu-id="e434a-209">Amount of the issued credit notes, and negative corrections that are related to sales from boxes 44 and 46.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-210">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-210">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-211">49</span><span class="sxs-lookup"><span data-stu-id="e434a-211">49</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-212">Het bedrag van verzonden kredieten en negatieve correcties die verband houden met vakken van sectie II, "Uitvoer".</span><span class="sxs-lookup"><span data-stu-id="e434a-212">Amount of issued credits, and negative adjustments that are related to other boxes from section II, "Outputs."</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-213">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-213">Base</span></span></p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><span data-ttu-id="e434a-214"><strong>Sectie III. Invoer</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-214"><strong>Section III. Inputs</strong></span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-215">81</span><span class="sxs-lookup"><span data-stu-id="e434a-215">81</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-216">Het bedrag van alle aankopen van goederen, grondstoffen en verbruiksartikelen, plus gerelateerde verwervingskosten.</span><span class="sxs-lookup"><span data-stu-id="e434a-216">Amount of all purchases of goods, raw materials, and consumables, and related acquisition costs.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-217">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-217">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-218">82</span><span class="sxs-lookup"><span data-stu-id="e434a-218">82</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-219">Het bedrag van diverse goederen en services, ongeacht of hierop btw van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="e434a-219">Amount of miscellaneous goods and services, regardless of whether they are subject to VAT.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-220">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-220">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-221">83</span><span class="sxs-lookup"><span data-stu-id="e434a-221">83</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-222">Het bedrag van aankopen van kapitaalgoederen en services, ongeacht of hierop btw van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="e434a-222">Amount of purchases of capital goods, regardless of whether they are subject to VAT.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-223">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-223">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-224">84</span><span class="sxs-lookup"><span data-stu-id="e434a-224">84</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-225">Bedrag van ontvangen kredieten en negatieve correcties die zijn gerelateerd aan verkoop uit vakken 86 en 88.</span><span class="sxs-lookup"><span data-stu-id="e434a-225">Amount of credits received, and negative adjustments that are related to sales from boxes 86 and 88.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-226">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-226">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-227">8684</span><span class="sxs-lookup"><span data-stu-id="e434a-227">8684</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-228">Technische aangiftecode voor het weergeven van creditnotabedragen in vakken 86 en 84.</span><span class="sxs-lookup"><span data-stu-id="e434a-228">Technical reporting code for showing credit note amounts in boxes 86 and 84.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-229">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-229">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-230">8884</span><span class="sxs-lookup"><span data-stu-id="e434a-230">8884</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-231">Technische aangiftecode voor het weergeven van creditnotabedragen in vakken 88 en 84.</span><span class="sxs-lookup"><span data-stu-id="e434a-231">Technical reporting code for showing credit note amounts in boxes 88 and 84.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-232">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-232">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-233">85</span><span class="sxs-lookup"><span data-stu-id="e434a-233">85</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-234">Het bedrag van ontvangen kredieten en negatieve correcties die verband houden met vakken van sectie III, "Invoer".</span><span class="sxs-lookup"><span data-stu-id="e434a-234">Amount of credits received, and negative adjustments that are related to other boxes from section III, "Inputs."</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-235">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-235">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-236">8185</span><span class="sxs-lookup"><span data-stu-id="e434a-236">8185</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-237">Technische aangiftecode voor het weergeven van creditnotabedragen in vakken 81 en 85.</span><span class="sxs-lookup"><span data-stu-id="e434a-237">Technical reporting code for showing credit note amounts in boxes 81 and 85.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-238">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-238">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-239">8285</span><span class="sxs-lookup"><span data-stu-id="e434a-239">8285</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-240">Technische rapporteringscode voor het weergeven van creditnotabedragen in vakken 82 en 85.</span><span class="sxs-lookup"><span data-stu-id="e434a-240">Technical reporting code for showing credit note amounts in boxes 82 and 85.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-241">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-241">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-242">8385</span><span class="sxs-lookup"><span data-stu-id="e434a-242">8385</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-243">Technische rapporteringscode voor het weergeven van creditnotabedragen in vakken 83 en 85.</span><span class="sxs-lookup"><span data-stu-id="e434a-243">Technical reporting code for showing credit note amounts in boxes 83 and 85.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-244">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-244">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-245">8785</span><span class="sxs-lookup"><span data-stu-id="e434a-245">8785</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-246">Technische rapporteringscode voor het weergeven van creditnotabedragen in vakken 87 en 85.</span><span class="sxs-lookup"><span data-stu-id="e434a-246">Technical reporting code for showing credit note amounts in boxes 87 and 85.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-247">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-247">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-248">86</span><span class="sxs-lookup"><span data-stu-id="e434a-248">86</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-249">Intracommunautaire verwervingen en vergelijkbare transacties.</span><span class="sxs-lookup"><span data-stu-id="e434a-249">Intra-community acquisitions and similar transactions.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-250">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-250">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-251">87</span><span class="sxs-lookup"><span data-stu-id="e434a-251">87</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-252">Andere ontvangsten waarover de persoon die zich moet registreren, btw verschuldigd is.</span><span class="sxs-lookup"><span data-stu-id="e434a-252">Other receipts that the person who is liable to register owes VAT for.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-253">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-253">Base</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-254">88</span><span class="sxs-lookup"><span data-stu-id="e434a-254">88</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-255">Intracommunautaire diensten met overdracht van het onderzoek.</span><span class="sxs-lookup"><span data-stu-id="e434a-255">Intra-community services with transfer of the survey.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-256">Basis</span><span class="sxs-lookup"><span data-stu-id="e434a-256">Base</span></span></p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><span data-ttu-id="e434a-257"><strong>Sectie IV. Te betalen belasting</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-257"><strong>Section IV. Taxes payable</strong></span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-258">54</span><span class="sxs-lookup"><span data-stu-id="e434a-258">54</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-259">Btw die moet worden betaald over de omzet die is opgenomen in codes <strong>01</strong>, <strong>02</strong> en <strong>03</strong>.</span><span class="sxs-lookup"><span data-stu-id="e434a-259">VAT that is payable on the turnover that is included in codes <strong>01</strong>, <strong>02</strong>, and <strong>03</strong>.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-260">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-260">Tax</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-261">55</span><span class="sxs-lookup"><span data-stu-id="e434a-261">55</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-262">Btw die moet worden betaald over de omzet die is opgenomen in codes <strong>86</strong> en <strong>88</strong>.</span><span class="sxs-lookup"><span data-stu-id="e434a-262">VAT that is payable on the turnover that is included in codes <strong>86</strong> and <strong>88</strong>.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-263">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-263">Tax</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-264">56</span><span class="sxs-lookup"><span data-stu-id="e434a-264">56</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-265">Btw op verkopen die in vak 87 zijn aangegeven, met uitzondering van invoer met betrekking tot de verplaatsing van het onderzoek.</span><span class="sxs-lookup"><span data-stu-id="e434a-265">VAT on sales that are declared in box 87, excluding imports that involve relocation of the survey.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-266">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-266">Tax</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-267">57</span><span class="sxs-lookup"><span data-stu-id="e434a-267">57</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-268">Btw op de invoer waarbij het onderzoek wordt overgebracht.</span><span class="sxs-lookup"><span data-stu-id="e434a-268">VAT on imports that involve transfer of the survey.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-269">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-269">Tax</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-270">61</span><span class="sxs-lookup"><span data-stu-id="e434a-270">61</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-271">Diverse btw-aanpassingen ten voordele van de staat.</span><span class="sxs-lookup"><span data-stu-id="e434a-271">Various VAT adjustments in favor of the state.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-272">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-272">Tax</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-273">63</span><span class="sxs-lookup"><span data-stu-id="e434a-273">63</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-274">Btw die moet worden aangegeven, zoals weergegeven op de kredieten die zijn ontvangen.</span><span class="sxs-lookup"><span data-stu-id="e434a-274">VAT that must be returned, as shown on the credits that are received.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-275">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-275">Tax</span></span></p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><span data-ttu-id="e434a-276"><strong>Sectie V. Aftrekbare belastingen</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-276"><strong>Section V. Taxes deductible</strong></span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-277">59</span><span class="sxs-lookup"><span data-stu-id="e434a-277">59</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-278">Bedrag van aftrekbare btw.</span><span class="sxs-lookup"><span data-stu-id="e434a-278">Amount of deductible VAT.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-279">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-279">Tax</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-280">62</span><span class="sxs-lookup"><span data-stu-id="e434a-280">62</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-281">Diverse btw-correcties ten voordele van de declarant.</span><span class="sxs-lookup"><span data-stu-id="e434a-281">Various VAT corrections in favor of the declarant.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-282">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-282">Tax</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-283">64</span><span class="sxs-lookup"><span data-stu-id="e434a-283">64</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-284">Btw die moet worden terugbetaald als gevolg van kredieten die zijn toegekend.</span><span class="sxs-lookup"><span data-stu-id="e434a-284">VAT that must be recovered because of credits that are granted.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-285">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-285">Tax</span></span></p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><span data-ttu-id="e434a-286"><strong>Sectie VI. Saldo</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-286"><strong>Section VI. Balance</strong></span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-287">71</span><span class="sxs-lookup"><span data-stu-id="e434a-287">71</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-288">Belasting die moet worden betaald.</span><span class="sxs-lookup"><span data-stu-id="e434a-288">Tax that must be paid.</span></span> <span data-ttu-id="e434a-289">In het INTERVAT-rapport wordt de waarde in dit vak automatisch berekend als de som van de rapporteringscodes <strong>54</strong>, <strong>55</strong>, <strong>56</strong>, <strong>57</strong>, <strong>61</strong> en <strong>63</strong>, minus rapporteringscodes <strong>59</strong>, <strong>62</strong> en <strong>64</strong>.</span><span class="sxs-lookup"><span data-stu-id="e434a-289">On the INTERVAT report, the value in this box is automatically calculated as the sum of reporting codes <strong>54</strong>, <strong>55</strong>, <strong>56</strong>, <strong>57</strong>, <strong>61</strong>, and <strong>63</strong>, minus reporting codes <strong>59</strong>, <strong>62</strong>, and <strong>64</strong>.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-290">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-290">Tax</span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-291">72</span><span class="sxs-lookup"><span data-stu-id="e434a-291">72</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-292">Belasting die moet worden terugbetaald.</span><span class="sxs-lookup"><span data-stu-id="e434a-292">Tax that must be recovered.</span></span> <span data-ttu-id="e434a-293">In het INTERVAT-rapport wordt de waarde in dit vak automatisch berekend als de som van de rapporteringscodes <strong>59</strong>, <strong>62</strong> en <strong>64</strong>, minus rapporteringscodes <strong>54</strong>, <strong>55</strong>, <strong>56</strong>, <strong>57</strong>, <strong>61</strong> en <strong>63</strong>.</span><span class="sxs-lookup"><span data-stu-id="e434a-293">On the INTERVAT report, the value in this box is automatically calculated as the sum of reporting codes <strong>59</strong>, <strong>62</strong>, and <strong>64</strong>, minus reporting codes <strong>54</strong>, <strong>55</strong>, <strong>56</strong>, <strong>57</strong>, <strong>61</strong>, and <strong>63</strong>.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-294">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-294">Tax</span></span></p>
</td>
</tr>
<tr>
<td colspan="3" width="100%">
<p style="text-align: center;"><span data-ttu-id="e434a-295"><strong>Sectie VII. Deposito</strong></span><span class="sxs-lookup"><span data-stu-id="e434a-295"><strong>Section VII. Deposit</strong></span></span></p>
</td>
</tr>
<tr>
<td width="17%">
<p><span data-ttu-id="e434a-296">91</span><span class="sxs-lookup"><span data-stu-id="e434a-296">91</span></span></p>
</td>
<td width="71%">
<p><span data-ttu-id="e434a-297">Btw die verschuldigd is voor de periode van 1 december t/m 20 december.</span><span class="sxs-lookup"><span data-stu-id="e434a-297">VAT that is actually owed for the period from December 1 through December 20.</span></span> <span data-ttu-id="e434a-298">Deze code is van toepassing op de maandelijkse aangifte voor december.</span><span class="sxs-lookup"><span data-stu-id="e434a-298">This code applies to the monthly declaration for December.</span></span></p>
</td>
<td width="10%">
<p><span data-ttu-id="e434a-299">Belasting</span><span class="sxs-lookup"><span data-stu-id="e434a-299">Tax</span></span></p>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e434a-300">U hoeft geen codes **71**, **72** en **91** in te voeren omdat deze automatisch worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e434a-300">You don't have to enter codes **71**, **72**, and **91**, because they will be generated automatically.</span></span>

<span data-ttu-id="e434a-301">Als u een toewijzing van btw-aangiftecodes aan btw-codes wilt instellen, gaat u naar **Btw-codes \> Rapportinstellingen/Rapportinstellingen - Creditnota**.</span><span class="sxs-lookup"><span data-stu-id="e434a-301">To set up an assignment of sales tax reporting codes to sales tax codes, go to **Sales tax codes \> Report setup/Report setup - Credit note**.</span></span> <span data-ttu-id="e434a-302">Houd rekening met de volgende relaties tussen btw-aangiftecodes:</span><span class="sxs-lookup"><span data-stu-id="e434a-302">Consider the following relations between sales tax reporting codes:</span></span>

-   <span data-ttu-id="e434a-303">Als er een bedrag voorkomt in code **01**, **02** of **03**, moet er ook een bedrag voorkomen in code **54**.</span><span class="sxs-lookup"><span data-stu-id="e434a-303">If there is an amount in code **01**, **02**, or **03**, there should also be an amount in code **54**.</span></span>
-   <span data-ttu-id="e434a-304">Als er een bedrag voorkomt in code **54**, moet er ook een bedrag voorkomen in code **01**, **02** of **03**.</span><span class="sxs-lookup"><span data-stu-id="e434a-304">If there is an amount in code **54**, there should also be an amount in code **01**, **02**, or **03**.</span></span>
-   <span data-ttu-id="e434a-305">Als er een bedrag voorkomt in code **86**, moet er ook een bedrag voorkomen in code **55**.</span><span class="sxs-lookup"><span data-stu-id="e434a-305">If there is an amount in code **86**, there should also be an amount in code **55**.</span></span>
-   <span data-ttu-id="e434a-306">Als er een bedrag voorkomt in code **87**, moet er ook een bedrag voorkomen in code **56** of **57**.</span><span class="sxs-lookup"><span data-stu-id="e434a-306">If there is an amount in code **87**, there should also be an amount in code **56** or **57**.</span></span>
-   <span data-ttu-id="e434a-307">Het verschil tussen het bedrag in code **54** en de som van codes **01**, **02** en **03**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet hoger zijn dan 61,97 EUR.</span><span class="sxs-lookup"><span data-stu-id="e434a-307">The difference between the amount in code **54** and the sum of codes **01**, **02**, and **03** multiplied by the corresponding VAT rates can't be more than 61.97 EUR.</span></span>
-   <span data-ttu-id="e434a-308">Het verschil tussen het bedrag in code **55** en de som van codes **84** en **86**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet hoger zijn dan 610,97 EUR.</span><span class="sxs-lookup"><span data-stu-id="e434a-308">The difference between the amount in code **55** and the sum of codes **84** and **86** multiplied by the corresponding VAT rates can't be more than 610.97 EUR.</span></span>
-   <span data-ttu-id="e434a-309">Het verschil tussen het totaal van de bedragen in code **56** en **57** en de som van codes **85** en **87**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet hoger zijn dan 61,97 EUR.</span><span class="sxs-lookup"><span data-stu-id="e434a-309">The difference between the sum of the amounts in codes **56** and **57** and the sum of codes **85** and **87** multiplied by the corresponding VAT rates can't be more than 61.97 EUR.</span></span>
-   <span data-ttu-id="e434a-310">Het bedrag in code **59** moet hoger zijn dan de som van de codes **81**, **82**, **83**, **84** en **85**.</span><span class="sxs-lookup"><span data-stu-id="e434a-310">The amount in code **59** should be more than the sum of codes **81**, **82**, **83**, **84**, and **85**.</span></span>
-   <span data-ttu-id="e434a-311">Het bedrag in code **63** en code **85**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet meer zijn dan 61,97 EUR.</span><span class="sxs-lookup"><span data-stu-id="e434a-311">The amount in code **63** and code **85** multiplied by the corresponding VAT rates can't be more than 61.97 EUR.</span></span>
-   <span data-ttu-id="e434a-312">Het bedrag in code **64** en code **49**, vermenigvuldigd met de overeenkomstige btw-tarieven kan niet meer zijn dan 61,97 EUR.</span><span class="sxs-lookup"><span data-stu-id="e434a-312">The amount in code **64** and code **49** multiplied by the corresponding VAT rates can't be more than 61.97 EUR.</span></span>


### <a name="download-the-format-for-the-report"></a><span data-ttu-id="e434a-313">Download de indeling voor het rapport</span><span class="sxs-lookup"><span data-stu-id="e434a-313">Download the format for the report</span></span>

<span data-ttu-id="e434a-314">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2) kunt u in de bibliotheek met gedeelde activa de meest recente versies downloaden van ER-configuraties (elektronische aangifte) voor de volgende indeling van de btw-aangifte:</span><span class="sxs-lookup"><span data-stu-id="e434a-314">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in the Shared asset library, download the latest versions of the Electronic reporting (ER) configurations for the following VAT declaration format:</span></span>

-   <span data-ttu-id="e434a-315">INTERVAT-indeling (BE)</span><span class="sxs-lookup"><span data-stu-id="e434a-315">INTERVAT format (BE)</span></span>

<span data-ttu-id="e434a-316">Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](https://docs.microsoft.com/dynamics365/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="e434a-316">For more information, see [Download Electronic reporting configurations from Lifecycle Services](https://docs.microsoft.com/dynamics365/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>

## <a name="additional-sales-tax-report-boxes"></a><span data-ttu-id="e434a-317">Aanvullende btw-rapportvakken</span><span class="sxs-lookup"><span data-stu-id="e434a-317">Additional sales tax report boxes</span></span>

1.  <span data-ttu-id="e434a-318">Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Aanvullende btw-rapportvakken**.</span><span class="sxs-lookup"><span data-stu-id="e434a-318">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Additional sales tax report boxes**.</span></span>
2.  <span data-ttu-id="e434a-319">Selecteer **Nieuw** als u regels wilt maken met extra informatie over rapporteringscodes, waaronder handmatige correcties van de INTERVAT-belastingaangifte.</span><span class="sxs-lookup"><span data-stu-id="e434a-319">Select **New** to create lines that have additional information about reporting codes, including manual corrections of the INTERVAT tax declaration.</span></span> <span data-ttu-id="e434a-320">Voordat u een vereffeningsperiode sluit, moet u de regel hiervoor maken door de btw-betaling te boeken of door een INTERVAT-aangifte te maken die is gemarkeerd als **Update**.</span><span class="sxs-lookup"><span data-stu-id="e434a-320">Before you close a settlement period, you should create the line for it, either by posting the sales tax payment or by creating an INTERVAT declaration that is marked as **Update**.</span></span> <span data-ttu-id="e434a-321">In de volgende tabel worden de velden beschreven die u moet instellen voor een nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="e434a-321">The following table describes the fields that you must set for a new line.</span></span>

| <span data-ttu-id="e434a-322">**Veld**</span><span class="sxs-lookup"><span data-stu-id="e434a-322">**Field**</span></span>         | <span data-ttu-id="e434a-323">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e434a-323">**Description**</span></span>                                                                                                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e434a-324">Vereffeningsperiode</span><span class="sxs-lookup"><span data-stu-id="e434a-324">Settlement period</span></span> | <span data-ttu-id="e434a-325">Selecteer de toepasselijke aangifteperiode.</span><span class="sxs-lookup"><span data-stu-id="e434a-325">Select the applicable reporting period.</span></span>                                                                                                                                                   |
| <span data-ttu-id="e434a-326">Begindatum</span><span class="sxs-lookup"><span data-stu-id="e434a-326">From date</span></span>         | <span data-ttu-id="e434a-327">Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="e434a-327">Enter the first day of the sales tax settlement period to calculate sales tax for.</span></span> <span data-ttu-id="e434a-328">Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**.</span><span class="sxs-lookup"><span data-stu-id="e434a-328">This value corresponds to the date in the **From** field on the **Sales tax settlement periods** page.</span></span> |
| <span data-ttu-id="e434a-329">Einddatum</span><span class="sxs-lookup"><span data-stu-id="e434a-329">To date</span></span>           | <span data-ttu-id="e434a-330">Voer de laatste datum van de btw-vereffeningsperiode in.</span><span class="sxs-lookup"><span data-stu-id="e434a-330">Enter the last date of the sales tax settlement period.</span></span>                                                                                                                                   |

3.  <span data-ttu-id="e434a-331">Stel op het sneltabblad **Algemeen** de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="e434a-331">On **General** tab, you can set the following fields:</span></span>

-   <span data-ttu-id="e434a-332">Sectie **Orders**</span><span class="sxs-lookup"><span data-stu-id="e434a-332">**Orders** section</span></span>

| <span data-ttu-id="e434a-333">**Veld**</span><span class="sxs-lookup"><span data-stu-id="e434a-333">**Field**</span></span>                                 | <span data-ttu-id="e434a-334">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e434a-334">**Description**</span></span>                                                                                                                                                                                                                                              |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e434a-335">Vraagt om terugbetaling van teruggevorderde btw</span><span class="sxs-lookup"><span data-stu-id="e434a-335">Requests repayment of sales tax reclaimed</span></span> | <span data-ttu-id="e434a-336">Selecteer deze optie om de terugbetaling van teruggevorderde btw aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="e434a-336">Select this option to request the repayment of any reclaimed sales tax.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="e434a-337">Voorschot</span><span class="sxs-lookup"><span data-stu-id="e434a-337">Disbursement</span></span>                              | <span data-ttu-id="e434a-338">Voer het voorschotbedrag in.</span><span class="sxs-lookup"><span data-stu-id="e434a-338">Enter the amount of disbursement.</span></span> <span data-ttu-id="e434a-339">Een voorschot kan alleen worden uitbetaald voor de maand december (maandelijkse aangifte).</span><span class="sxs-lookup"><span data-stu-id="e434a-339">A disbursement can be paid only for the month of December (monthly declaration).</span></span> <span data-ttu-id="e434a-340">Het voorschot komt overeen met vak 91 in de Belgische btw-aangifte.</span><span class="sxs-lookup"><span data-stu-id="e434a-340">The disbursement corresponds to box 91 in the Belgian VAT declaration.</span></span> <span data-ttu-id="e434a-341">U kunt dit veld alleen instellen als de maand gelijk is aan december (**12**).</span><span class="sxs-lookup"><span data-stu-id="e434a-341">You can set this field only if the month equals December (**12**).</span></span> |
| <span data-ttu-id="e434a-342">Depositoformulier bestellen</span><span class="sxs-lookup"><span data-stu-id="e434a-342">Order deposit form</span></span>                        | <span data-ttu-id="e434a-343">Selecteer deze optie als u depositopagina's voor btw-aangifte wilt bestellen.</span><span class="sxs-lookup"><span data-stu-id="e434a-343">Select this option to order deposit pages for tax reporting purposes.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="e434a-344">Geen jaaroverzichten</span><span class="sxs-lookup"><span data-stu-id="e434a-344">Nil annual listing</span></span>                        | <span data-ttu-id="e434a-345">Selecteer deze optie om aan te geven dat er geen transacties zijn om aan te geven en dat het bedrijf geen verplichting aan de Belgische overheid heeft om de jaaraangifte van het vorige jaar te doen.</span><span class="sxs-lookup"><span data-stu-id="e434a-345">Select this option to indicate that there are no transactions to report, and that the company has no obligation to the Belgian government to declare the annual sales from the previous year.</span></span>                                                                |

-   <span data-ttu-id="e434a-346">Sectie **Omslagpercentages**</span><span class="sxs-lookup"><span data-stu-id="e434a-346">**Pro-rata percentages** section</span></span>

| <span data-ttu-id="e434a-347">**Veld**</span><span class="sxs-lookup"><span data-stu-id="e434a-347">**Field**</span></span>           | <span data-ttu-id="e434a-348">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e434a-348">**Description**</span></span>                                                                                                                                                                                                                 |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e434a-349">Omslagpercentage</span><span class="sxs-lookup"><span data-stu-id="e434a-349">Pro-rata percentage</span></span> | <span data-ttu-id="e434a-350">Voer de waarde in van het pro-rata percentage dat in de **\<AdjustedValue\>**-code in het XML-bestand wordt geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="e434a-350">Enter the value of the pro-rata percentage that will be exported in the **\<AdjustedValue\>** tag in the XML file.</span></span>                                                                                                              |
| <span data-ttu-id="e434a-351">B1, B2, B3, B4, B5</span><span class="sxs-lookup"><span data-stu-id="e434a-351">B1, B2, B3, B4, B5</span></span>  | <span data-ttu-id="e434a-352">Voer bedragen in voor de waarden van B1, B2, B3, B4 en B5, die worden geëxporteerd in de **\<SpecialProRataPercentage\>**-code in het XML-bestand, waarbij **\<SpecialProRataGridNumber\>**=**1**, **2**, **3**, **4**, **5** wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e434a-352">Enter amounts for the values of B1, B2, B3, B4, and B5, which will be exported in the **\<SpecialProRataPercentage\>** tag in the XML file, where **\<SpecialProRataGridNumber\>**=**"1"**, **"2"**, **"3"**, **"4"**, **"5"**.</span></span> |

### <a name="tax-corrections"></a><span data-ttu-id="e434a-353">Belastingcorrecties</span><span class="sxs-lookup"><span data-stu-id="e434a-353">Tax corrections</span></span>

<span data-ttu-id="e434a-354">Voer de volgende stappen uit om handmatige correctiebedragen in te voeren.</span><span class="sxs-lookup"><span data-stu-id="e434a-354">Follow these steps to enter manual correction amounts.</span></span>

1.  <span data-ttu-id="e434a-355">Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Aanvullende btw-rapportvakken**.</span><span class="sxs-lookup"><span data-stu-id="e434a-355">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Additional sales tax report boxes**.</span></span>
2.  <span data-ttu-id="e434a-356">Selecteer **Btw-correcties** \> **Correcties** en stel de volgende velden in.</span><span class="sxs-lookup"><span data-stu-id="e434a-356">Select **Tax corrections** \> **Adjustments** and set the following fields.</span></span>

| <span data-ttu-id="e434a-357">**Veld**</span><span class="sxs-lookup"><span data-stu-id="e434a-357">**Field**</span></span>         | <span data-ttu-id="e434a-358">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e434a-358">**Description**</span></span>                                                                                                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e434a-359">Vereffeningsperiode</span><span class="sxs-lookup"><span data-stu-id="e434a-359">Settlement period</span></span> | <span data-ttu-id="e434a-360">Selecteer de toepasselijke aangifteperiode.</span><span class="sxs-lookup"><span data-stu-id="e434a-360">Select the applicable reporting period.</span></span>                                                                                                                                                   |
| <span data-ttu-id="e434a-361">Begindatum</span><span class="sxs-lookup"><span data-stu-id="e434a-361">From date</span></span>         | <span data-ttu-id="e434a-362">Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="e434a-362">Enter the first day of the sales tax settlement period to calculate sales tax for.</span></span> <span data-ttu-id="e434a-363">Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**.</span><span class="sxs-lookup"><span data-stu-id="e434a-363">This value corresponds to the date in the **From** field on the **Sales tax settlement periods** page.</span></span> |
| <span data-ttu-id="e434a-364">Einddatum</span><span class="sxs-lookup"><span data-stu-id="e434a-364">To date</span></span>           | <span data-ttu-id="e434a-365">Voer de laatste dag van de btw-vereffeningsperiode in.</span><span class="sxs-lookup"><span data-stu-id="e434a-365">Enter the last day of the sales tax settlement period.</span></span>                                                                                                                                    |
| <span data-ttu-id="e434a-366">Aangiftecode</span><span class="sxs-lookup"><span data-stu-id="e434a-366">Reporting code</span></span>    | <span data-ttu-id="e434a-367">Selecteer de aangiftecode.</span><span class="sxs-lookup"><span data-stu-id="e434a-367">Select the reporting code.</span></span> <span data-ttu-id="e434a-368">Alleen de aangiftecodes waarvoor het selectievakje **Btw-correcties** is ingeschakeld, zijn beschikbaar tijdens het invoeren van btw-correcties.</span><span class="sxs-lookup"><span data-stu-id="e434a-368">Only the reporting codes that the **Tax corrections** check box is selected for will be available during tax correction entry.</span></span>                                 |
| <span data-ttu-id="e434a-369">Bedrag</span><span class="sxs-lookup"><span data-stu-id="e434a-369">Amount</span></span>            | <span data-ttu-id="e434a-370">Voer het correctiebedrag in.</span><span class="sxs-lookup"><span data-stu-id="e434a-370">Enter the correction amount.</span></span>                                                                                                                                                              |

> [!NOTE]
> <span data-ttu-id="e434a-371">Bestaande aangiftecodes die worden gebruikt voor creditnota's.</span><span class="sxs-lookup"><span data-stu-id="e434a-371">Composed reporting codes that are used for credit notes.</span></span> <span data-ttu-id="e434a-372">zoals code **8185**, zijn niet beschikbaar voor selectie.</span><span class="sxs-lookup"><span data-stu-id="e434a-372">such as code **8185**, aren't available for selection.</span></span> <span data-ttu-id="e434a-373">Codes **71**, **72** en **91** zijn ook niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="e434a-373">Nor are codes **71**, **72**, and **91**.</span></span> <span data-ttu-id="e434a-374">Codes **71** en **72** worden automatisch berekend wanneer Belgische btw-aangifte wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e434a-374">Codes **71** and **72** are calculated automatically when Belgian sales tax reporting is run.</span></span> <span data-ttu-id="e434a-375">Code **91** wordt op een andere manier ingevoerd (zie omschrijving van het veld **Voorschot** hierboven).</span><span class="sxs-lookup"><span data-stu-id="e434a-375">Code **91** is entered in another way (see description of **Disbursement** field above).</span></span>
>
> <span data-ttu-id="e434a-376">Als een belastingperiode wordt bijgewerkt, worden een boekstuknummer en een datum weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e434a-376">If a tax period is updated, a voucher number and a date will be shown.</span></span> <span data-ttu-id="e434a-377">(Zie voor meer informatie de omschrijving van het selectievakje **Update** in de sectie [Een INTERVAT-btw-aangifte genereren](#generate-an-intervat-tax-declaration), verderop in dit onderwerp.) De periode die een boekstuknummer en een datum heeft, is een afgesloten btw-periode voor België.</span><span class="sxs-lookup"><span data-stu-id="e434a-377">(For more information, see the description of the **Update** check box in the [Generate an INTERVAT tax declaration](#generate-an-intervat-tax-declaration) section later in this topic.) The period that has a voucher number and a date is a closed VAT period for Belgium.</span></span> <span data-ttu-id="e434a-378">Daarom zijn alle waarden op het tabblad **Algemeen** van de pagina **Btw-correcties** alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="e434a-378">Therefore, all values on the **General** tab of the **Tax corrections** page are read-only.</span></span> <span data-ttu-id="e434a-379">Wanneer er nieuwe transacties met belastingen zijn ingevoerd voor de afgesloten btw-periode, wordt de btw doorgestuurd naar de volgende beschikbare openstaande belastingperiode.</span><span class="sxs-lookup"><span data-stu-id="e434a-379">When new transactions that have taxes are entered for the closed VAT period, the taxes will be forwarded to the next available open tax period.</span></span>


## <a name="generate-an-intervat-tax-declaration"></a><span data-ttu-id="e434a-380">Een INTERVAT-btw-aangifte genereren</span><span class="sxs-lookup"><span data-stu-id="e434a-380">Generate an INTERVAT tax declaration</span></span>
1.  <span data-ttu-id="e434a-381">Ga naar **Belasting** \>**Aangiften \> Btw \> INTERVAT-belastingaangifte**.</span><span class="sxs-lookup"><span data-stu-id="e434a-381">Go to **Tax** \>**Declarations \> Sales tax \> INTERVAT tax declaration**.</span></span>
2.  <span data-ttu-id="e434a-382">Selecteer **Nieuwe aangifte** om een INTERVAT-belastingaangifte te genereren.</span><span class="sxs-lookup"><span data-stu-id="e434a-382">Select **New declaration** to generate an INTERVAT tax declaration.</span></span>
3.  <span data-ttu-id="e434a-383">Stel in het dialoogvenster **INTERVAT: Belgische btw-aangifte** de volgende velden in.</span><span class="sxs-lookup"><span data-stu-id="e434a-383">In the **INTERVAT: Belgian sales tax reporting** dialog box, set the following fields.</span></span>

| <span data-ttu-id="e434a-384">**Veld**</span><span class="sxs-lookup"><span data-stu-id="e434a-384">**Field**</span></span>                | <span data-ttu-id="e434a-385">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e434a-385">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e434a-386">Vereffeningsperiode</span><span class="sxs-lookup"><span data-stu-id="e434a-386">Settlement period</span></span>        | <span data-ttu-id="e434a-387">Selecteer de toepasselijke aangifteperiode.</span><span class="sxs-lookup"><span data-stu-id="e434a-387">Select the applicable reporting period.</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="e434a-388">Begindatum</span><span class="sxs-lookup"><span data-stu-id="e434a-388">From date</span></span>                | <span data-ttu-id="e434a-389">Voer de eerste dag van de btw-vereffeningsperiode in waarvoor btw moet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="e434a-389">Enter the first day of the sales tax settlement period to calculate sales tax for.</span></span> <span data-ttu-id="e434a-390">Deze waarde komt overeen met de datum in het veld **Van** op de pagina **Btw-vereffeningsperioden**.</span><span class="sxs-lookup"><span data-stu-id="e434a-390">This value corresponds to the date in the **From** field on the **Sales tax settlement periods** page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="e434a-391">Transactiedatum</span><span class="sxs-lookup"><span data-stu-id="e434a-391">Transaction date</span></span>         | <span data-ttu-id="e434a-392">Voer de datum in waarvoor de btw-aangifte wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="e434a-392">Enter the date when the sales tax report is calculated.</span></span> <span data-ttu-id="e434a-393">De standaardwaarde is de huidige datum.</span><span class="sxs-lookup"><span data-stu-id="e434a-393">The default value is the current date.</span></span> <span data-ttu-id="e434a-394">De btw-betaling wordt berekend voor alle transacties die zijn geboekt tijdens de vereffeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="e434a-394">The sales tax payment is calculated for all transactions that were posted during the settlement period.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="e434a-395">Update</span><span class="sxs-lookup"><span data-stu-id="e434a-395">Update</span></span>                   | <span data-ttu-id="e434a-396">Met een ingeschakeld selectievakje wordt de periode afgesloten en wordt een btw-betaling gemaakt, als deze nog niet is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e434a-396">A selected check box closes the period and creates a sales tax payment, if it wasn't already created.</span></span> <span data-ttu-id="e434a-397">Daarom worden alle btw-transacties die in deze periode zijn ingevoerd na de update, doorgestuurd naar de volgende beschikbare openstaande periode.</span><span class="sxs-lookup"><span data-stu-id="e434a-397">Therefore, all VAT transactions that are entered in this period after the update will be forwarded to the next available open period.</span></span> <span data-ttu-id="e434a-398">Een ingeschakeld selectievakje maakt ook de regel op de pagina **Extra btw-aangifte vakken**, als deze nog niet is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e434a-398">A selected check box also creates the line on the **Additional sales tax report boxes** page, if it wasn't already created.</span></span> <span data-ttu-id="e434a-399">Geen van de waarden op deze nieuwe regel kan worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="e434a-399">None of the values on this new line can be edited.</span></span> |
| <span data-ttu-id="e434a-400">Vervangen btw-aangifte</span><span class="sxs-lookup"><span data-stu-id="e434a-400">Replaced VAT declaration</span></span> | <span data-ttu-id="e434a-401">Voer het identificatienummer in van de te vervangen aangifte.</span><span class="sxs-lookup"><span data-stu-id="e434a-401">Enter the identification number of the declaration to replace.</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e434a-402">Bestand</span><span class="sxs-lookup"><span data-stu-id="e434a-402">File</span></span>                     | <span data-ttu-id="e434a-403">Voer de bestandsnaam in waarnaar de INTERVAT-belastingaangifte zal worden geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="e434a-403">Enter the file name that the INTERVAT tax declaration will be exported to.</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e434a-404">Indelingstoewijzing</span><span class="sxs-lookup"><span data-stu-id="e434a-404">Format mapping</span></span>           | <span data-ttu-id="e434a-405">Selecteer de ER-indeling **INTERVAT-indeling (BE)** die u eerder hebt gedownload.</span><span class="sxs-lookup"><span data-stu-id="e434a-405">Select the **INTERVAT format (BE)** ER format that you downloaded earlier.</span></span>                                                                                                                                                                                                                                                                                                                                                 |

<span data-ttu-id="e434a-406">U kunt de belastingperiode ook afsluiten door een btw-betaling te genereren (**Btw \> Aangiften \> Btw \> Btw vereffenen en boeken**).</span><span class="sxs-lookup"><span data-stu-id="e434a-406">You can also close the tax period by generating a sales tax payment (**Tax \> Declarations \> Sales tax \> Settle and post sales tax**).</span></span>

4.  <span data-ttu-id="e434a-407">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e434a-407">Select **OK**.</span></span> <span data-ttu-id="e434a-408">Het systeem genereert de INTERVAT-belastingaangifteregel en een INTERVAT XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="e434a-408">The system generates the INTERVAT tax declaration line and an INTERVAT XML file.</span></span>
5.  <span data-ttu-id="e434a-409">Bekijk de gegevens in de aangifte.</span><span class="sxs-lookup"><span data-stu-id="e434a-409">Review the information in the declaration.</span></span>

![](media/2_Intervat_tax declaration.png)

6.  <span data-ttu-id="e434a-410">Controleer de volgende velden op het tabblad **Algemeen**: **INTERVAT-id**, **Datum**, **Periode**, **Begindatum**, **Einddatum**, **Periodefrequentie**, **Status** en **Bestandsnaam**.</span><span class="sxs-lookup"><span data-stu-id="e434a-410">On the **General** tab, review the following fields: **INTERVAT ID**, **Date**, **Period**, **Start date**, **End date**, **Period frequency**, **Status**, and **File name**.</span></span>
7.  <span data-ttu-id="e434a-411">Controleer de volgende velden op het tabblad **Frame I: Algemene informatie**.</span><span class="sxs-lookup"><span data-stu-id="e434a-411">On the **Frame I: General information** tab, review the following fields.</span></span> <span data-ttu-id="e434a-412">U kunt deze velden bewerken, zelfs als de periode is afgesloten.</span><span class="sxs-lookup"><span data-stu-id="e434a-412">You can edit these fields, even if the period was closed.</span></span> <span data-ttu-id="e434a-413">De uitzonderingen zijn de velden in de sectie **Omslagpercentages**.</span><span class="sxs-lookup"><span data-stu-id="e434a-413">The exceptions are the fields in the **Pro-rata percentages** section.</span></span> <span data-ttu-id="e434a-414">Deze velden zijn alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="e434a-414">Those fields are read-only.</span></span>

| <span data-ttu-id="e434a-415">**Veld**</span><span class="sxs-lookup"><span data-stu-id="e434a-415">**Field**</span></span>                        | <span data-ttu-id="e434a-416">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e434a-416">**Description**</span></span>                                                                                                                                                                                                                                                                           |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e434a-417">Bedrijfsnaam</span><span class="sxs-lookup"><span data-stu-id="e434a-417">Company name</span></span>                     | <span data-ttu-id="e434a-418">De bedrijfsnaam.</span><span class="sxs-lookup"><span data-stu-id="e434a-418">The company name.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="e434a-419">Btw-nummer</span><span class="sxs-lookup"><span data-stu-id="e434a-419">Sales tax number</span></span>                 | <span data-ttu-id="e434a-420">Het btw-registratienummer dat wordt overgenomen uit de instelling die u hebt gedefinieerd in de sectie [Vereisten](#prerequisites), eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="e434a-420">The tax registration number that is transferred from the setting that you defined in the [Prerequisites](#prerequisites) section earlier in this topic.</span></span>                                                                                                                                   |
| <span data-ttu-id="e434a-421">Ondernemingsnummer</span><span class="sxs-lookup"><span data-stu-id="e434a-421">Enterprise number</span></span>                | <span data-ttu-id="e434a-422">Het ondernemingsnummer dat wordt overgenomen uit de instelling die u hebt gedefinieerd in de sectie [Vereisten](#prerequisites), eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="e434a-422">The enterprise number that is transferred from the setting that you defined in the [Prerequisites](#prerequisites) section.</span></span>                                                                                                                                                               |
| <span data-ttu-id="e434a-423">Telefoon, e-mail</span><span class="sxs-lookup"><span data-stu-id="e434a-423">Telephone, Email</span></span>                 | <span data-ttu-id="e434a-424">Contactgegevens die worden overgenomen uit de instelling die u hebt gedefinieerd in de sectie [Vereisten](#prerequisites), eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="e434a-424">Contact information that is transferred from the setting that you defined in the [Prerequisites](#prerequisites) section.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="e434a-425">Aanvraag van teruggaaf</span><span class="sxs-lookup"><span data-stu-id="e434a-425">Request for reimbursement</span></span>        | <span data-ttu-id="e434a-426">Schakel dit selectievakje in om een terugbetaling van de belasting aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="e434a-426">Select this check box to request a reimbursement of tax.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="e434a-427">Aanvraag van betalingsformulieren</span><span class="sxs-lookup"><span data-stu-id="e434a-427">Request for payment forms</span></span>        | <span data-ttu-id="e434a-428">Schakel dit selectievakje in om betalingspagina's voor de INTERVAT-belastingaangifte aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="e434a-428">Select this check box to request payment pages for the INTERVAT tax declarations.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="e434a-429">Geen jaaroverzichten</span><span class="sxs-lookup"><span data-stu-id="e434a-429">Nil annual listing</span></span>               | <span data-ttu-id="e434a-430">Een aangevinkt selectievakje geeft aan dat deze aangifte een lege aangifte is.</span><span class="sxs-lookup"><span data-stu-id="e434a-430">A selected check box indicates that this declaration is an empty declaration.</span></span> <span data-ttu-id="e434a-431">De waarde wordt overgenomen van de pagina **Aanvullende btw-rapportvakken**, die wordt beschreven in de sectie [Aanvullende btw-rapportvakken](#additional-sales-tax-report-boxes), eerder in dit onderwerp</span><span class="sxs-lookup"><span data-stu-id="e434a-431">The value is transferred from the **Additional sales tax report boxes** page that is described in the [Additional sales tax report boxes](#additional-sales-tax-report-boxes) section earlier in this topic</span></span> |
| <span data-ttu-id="e434a-432">Vervangen btw-aangifte</span><span class="sxs-lookup"><span data-stu-id="e434a-432">Replaced VAT declaration</span></span>         | <span data-ttu-id="e434a-433">Het identificatienummer van de aangifte, om te vervangen wat u hebt gedefinieerd in het dialoogvenster **INTERVAT: Belgisch btw-aangifte**, dat eerder in deze sectie is beschreven.</span><span class="sxs-lookup"><span data-stu-id="e434a-433">The identification number of the declaration, to replace what you defined in the **INTERVAT: Belgian sales tax reporting** dialog box that is described earlier in this section.</span></span>                                                                                                          |
| <span data-ttu-id="e434a-434">Sectie **Omslagpercentages**</span><span class="sxs-lookup"><span data-stu-id="e434a-434">**Pro-rata percentages** section</span></span> | <span data-ttu-id="e434a-435">Controleer de bedragen in de velden **Omslagpercentage**, **B1**, **B2**, **B3**, **B4** en **B5**, die u hebt gedefinieerd op de pagina **Aanvullende btw-rapportvakken** die wordt beschreven in de sectie [Aanvullende btw-rapportvakken](#additional-sales-tax-report-boxes).</span><span class="sxs-lookup"><span data-stu-id="e434a-435">Review the amounts in the **Pro-rata percentage**, **B1**, **B2**, **B3**, **B4**, and **B5** fields that you defined on the **Additional sales tax report boxes** page that is described in the [Additional sales tax report boxes](#additional-sales-tax-report-boxes) section.</span></span>         |

<span data-ttu-id="e434a-436">Op de pagina **INTERVAT-belastingaangifte** kunt u de volgende acties uitvoeren met behulp van de knoppen in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e434a-436">On the **INTERVAT tax declaration** page, you can perform the following actions by using the buttons on the Action Pane.</span></span>

| <span data-ttu-id="e434a-437">**Knop**</span><span class="sxs-lookup"><span data-stu-id="e434a-437">**Button**</span></span>     | <span data-ttu-id="e434a-438">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e434a-438">**Description**</span></span>                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e434a-439">Instellen</span><span class="sxs-lookup"><span data-stu-id="e434a-439">Setup</span></span>          | <span data-ttu-id="e434a-440">De pagina **Aanvullende btw-rapportvakken** openen die wordt beschreven in de sectie [Aanvullende btw-rapportvakken](#additional-sales-tax-report-boxes).</span><span class="sxs-lookup"><span data-stu-id="e434a-440">Open the **Additional sales tax report boxes** page that is described in the [Additional sales tax report boxes](#additional-sales-tax-report-boxes) section.</span></span>                                                                                                     |
| <span data-ttu-id="e434a-441">Bestand opnieuw maken</span><span class="sxs-lookup"><span data-stu-id="e434a-441">Re-create file</span></span> | <span data-ttu-id="e434a-442">Het INTERVAT-bestand opnieuw maken als de periode niet is afgesloten.</span><span class="sxs-lookup"><span data-stu-id="e434a-442">Recreate the INTERVAT file if the period wasn't closed.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="e434a-443">Bestand openen</span><span class="sxs-lookup"><span data-stu-id="e434a-443">Open file</span></span>      | <span data-ttu-id="e434a-444">Het gegenereerde XML-bestand openen.</span><span class="sxs-lookup"><span data-stu-id="e434a-444">Open the generated XML file.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="e434a-445">Website openen</span><span class="sxs-lookup"><span data-stu-id="e434a-445">Open Web site</span></span>  | <span data-ttu-id="e434a-446">De website (URL) openen die u hebt gedefinieerd op de pagina **INTERVAT-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-446">Open the website (URL) that you defined on the **INTERVAT setup** page.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="e434a-447">Status wijzigen</span><span class="sxs-lookup"><span data-stu-id="e434a-447">Change status</span></span>  | <span data-ttu-id="e434a-448">De cursusstatus wijzigen in **Verzonden**.</span><span class="sxs-lookup"><span data-stu-id="e434a-448">Change the status to **Sent**.</span></span> <span data-ttu-id="e434a-449">Wanneer een aangifte wordt gemaakt, heeft deze de status **Gemaakt**.</span><span class="sxs-lookup"><span data-stu-id="e434a-449">When a declaration is created, it has a status of **Created**.</span></span> <span data-ttu-id="e434a-450">Nadat u het gegenereerde bestand dat de INTERVAT-aangifte bevat, op de INTERVAT-site handmatig hebt geïmporteerd, kunt u deze knop gebruiken om de status te wijzigen in **Verzonden**.</span><span class="sxs-lookup"><span data-stu-id="e434a-450">After you manually import the generated file that contains the INTERVAT declaration on the INTERVAT site, you can use this button to change the status to **Sent**.</span></span> |
| <span data-ttu-id="e434a-451">Details</span><span class="sxs-lookup"><span data-stu-id="e434a-451">Details</span></span>        | <span data-ttu-id="e434a-452">De pagina **Intervat-gegevens** openen, waar u de bedragen in de bijbehorende aangiftecodes kunt bekijken.</span><span class="sxs-lookup"><span data-stu-id="e434a-452">Open the **INTERVAT details** page, where you can review the amounts in the corresponding reporting codes.</span></span>                                                                                                                                                        |

## <a name="generate-an-intervat-summary-tax-declaration"></a><span data-ttu-id="e434a-453">Een samenvatting van een INTERVAT-belastingaangifte genereren</span><span class="sxs-lookup"><span data-stu-id="e434a-453">Generate an INTERVAT summary tax declaration</span></span>
<span data-ttu-id="e434a-454">Als u een INTERVAT-belastingaangifte wilt afdrukken voor verschillende belastingperioden, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="e434a-454">To print an INTERVAT tax declaration for several tax periods, follow these steps.</span></span>

1.  <span data-ttu-id="e434a-455">Ga naar **Belasting** \> **Query's en rapporten** \> **Btw-aangiften** \> **INTERVAT-belastingaangifte**.</span><span class="sxs-lookup"><span data-stu-id="e434a-455">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **INTERVAT summary tax declaration**.</span></span>
2.  <span data-ttu-id="e434a-456">Gebruik de filters om criteria op te geven voor het selecteren van gegevens en bekijk vervolgens de informatie in het rapport.</span><span class="sxs-lookup"><span data-stu-id="e434a-456">Use the filters to specify criteria for selecting data, and then review the information on the report.</span></span>

![Gegenereerd rapport voor overzicht INTERVAT-belastingaangiften](media/3_Intervat_summary_tax_declarations.png)

## <a name="example"></a><span data-ttu-id="e434a-458">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="e434a-458">Example</span></span>
<span data-ttu-id="e434a-459">In het volgende voorbeeld ziet u hoe u btw-codes en btw-aangiftecodes kunt instellen, transacties kunt boeken en de INTERVAT-belastingaangifte kunt genereren.</span><span class="sxs-lookup"><span data-stu-id="e434a-459">The following example shows how you can set up sales tax codes and sales tax reporting codes, post transactions, and generate the INTERVAT tax declaration.</span></span>

1.  <span data-ttu-id="e434a-460">Ga naar **Organisatiebeheer \> Organisaties \> Rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-460">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="e434a-461">Voer het op het sneltabblad **Belastingregistratie** in het veld **Btw-registratienummer** **0466.158.640** in.</span><span class="sxs-lookup"><span data-stu-id="e434a-461">On the **Tax registration** FastTab, in the **Tax registration number** field, enter **0466.158.640**.</span></span>
3.  <span data-ttu-id="e434a-462">Selecteer **Registratie-id's** om een regel toe te voegen en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e434a-462">Select **Registration IDs**, add a line, and set the following values:</span></span>

-   <span data-ttu-id="e434a-463">**Registratietype:** ENTNUM</span><span class="sxs-lookup"><span data-stu-id="e434a-463">**Registration type:** ENTNUM</span></span>
-   <span data-ttu-id="e434a-464">**Registratienummer:** BTW BE 0466.158.640</span><span class="sxs-lookup"><span data-stu-id="e434a-464">**Registration number:** BTW BE 0466.158.640</span></span>

4.  <span data-ttu-id="e434a-465">Ga naar **Belasting \> Indirecte belastingen \> Btw \> Btw-codes** en stel de volgende btw-codes in.</span><span class="sxs-lookup"><span data-stu-id="e434a-465">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**, and set up the following sales tax codes.</span></span>

| <span data-ttu-id="e434a-466">**Btw-code**</span><span class="sxs-lookup"><span data-stu-id="e434a-466">**Sales tax code**</span></span> | <span data-ttu-id="e434a-467">**Percentage**</span><span class="sxs-lookup"><span data-stu-id="e434a-467">**Percentage**</span></span> | <span data-ttu-id="e434a-468">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="e434a-468">**Description**</span></span>                                                                      |
|--------------------|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e434a-469">BE21</span><span class="sxs-lookup"><span data-stu-id="e434a-469">BE21</span></span>               | <span data-ttu-id="e434a-470">21</span><span class="sxs-lookup"><span data-stu-id="e434a-470">21</span></span>             | <span data-ttu-id="e434a-471">Binnenlandse verkoop en inkoop met een tarief van 21 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-471">Domestic sales and purchases at a rate of 21 percent.</span></span>                                |
| <span data-ttu-id="e434a-472">BE12</span><span class="sxs-lookup"><span data-stu-id="e434a-472">BE12</span></span>               | <span data-ttu-id="e434a-473">12</span><span class="sxs-lookup"><span data-stu-id="e434a-473">12</span></span>             | <span data-ttu-id="e434a-474">Binnenlandse verkoop en inkoop met een tarief van 12 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-474">Domestic sales and purchases at a rate of 12 percent.</span></span>                                |
| <span data-ttu-id="e434a-475">BE6</span><span class="sxs-lookup"><span data-stu-id="e434a-475">BE6</span></span>                | <span data-ttu-id="e434a-476">6</span><span class="sxs-lookup"><span data-stu-id="e434a-476">6</span></span>              | <span data-ttu-id="e434a-477">Binnenlandse verkoop en inkoop met een tarief van 6 procent.</span><span class="sxs-lookup"><span data-stu-id="e434a-477">Domestic sales and purchases at a rate of 6 percent.</span></span>                                 |
| <span data-ttu-id="e434a-478">BEEU21</span><span class="sxs-lookup"><span data-stu-id="e434a-478">BEEU21</span></span>             | <span data-ttu-id="e434a-479">21</span><span class="sxs-lookup"><span data-stu-id="e434a-479">21</span></span>             | <span data-ttu-id="e434a-480">EU-inkoop met een tarief van 21 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.</span><span class="sxs-lookup"><span data-stu-id="e434a-480">EU purchases at a rate of 21 percent where the **Use tax** option is set to **Yes**.</span></span> |
| <span data-ttu-id="e434a-481">BEEU12</span><span class="sxs-lookup"><span data-stu-id="e434a-481">BEEU12</span></span>             | <span data-ttu-id="e434a-482">12</span><span class="sxs-lookup"><span data-stu-id="e434a-482">12</span></span>             | <span data-ttu-id="e434a-483">EU-inkoop met een tarief van 12 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.</span><span class="sxs-lookup"><span data-stu-id="e434a-483">EU purchases at a rate of 12 percent where the **Use tax** option is set to **Yes**.</span></span> |
| <span data-ttu-id="e434a-484">BEEU6</span><span class="sxs-lookup"><span data-stu-id="e434a-484">BEEU6</span></span>              | <span data-ttu-id="e434a-485">6</span><span class="sxs-lookup"><span data-stu-id="e434a-485">6</span></span>              | <span data-ttu-id="e434a-486">EU-inkoop met een tarief van 6 procent, waarbij de optie **Gebruiksbelasting** is ingesteld **op Ja**.</span><span class="sxs-lookup"><span data-stu-id="e434a-486">EU purchases at a rate of 6 percent where the **Use tax** option is set to **Yes**.</span></span>  |
| <span data-ttu-id="e434a-487">BEEUS</span><span class="sxs-lookup"><span data-stu-id="e434a-487">BEEUS</span></span>              | <span data-ttu-id="e434a-488">21</span><span class="sxs-lookup"><span data-stu-id="e434a-488">21</span></span>             | <span data-ttu-id="e434a-489">EU-verkoop waarvoor de optie **Vrijstelling** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e434a-489">EU sales where the **Exempt** option is set to **Yes**.</span></span>                              |

5.  <span data-ttu-id="e434a-490">Wijs op de pagina **Btw-codes** op het sneltabblad **Rapportinstellingen** aangiftecodes toe aan btw-codes.</span><span class="sxs-lookup"><span data-stu-id="e434a-490">On the **Sales tax codes** page, on the **Report setup** FastTab, assign reporting codes to sales tax codes.</span></span>

<span data-ttu-id="e434a-491">In de volgende tabel wordt aangegeven hoe u de btw-aangiftecodes aan btw-codes kunt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e434a-491">The following table shows how to assign the sales tax reporting codes to sales tax codes.</span></span>

| <span data-ttu-id="e434a-492">**Btw-code**</span><span class="sxs-lookup"><span data-stu-id="e434a-492">**Sales tax code**</span></span> | <span data-ttu-id="e434a-493">**Belastbare verkoop**</span><span class="sxs-lookup"><span data-stu-id="e434a-493">**Taxable sales**</span></span> | <span data-ttu-id="e434a-494">**Verkoop zonder btw**</span><span class="sxs-lookup"><span data-stu-id="e434a-494">**Tax-free sale**</span></span> | <span data-ttu-id="e434a-495">**Te betalen btw**</span><span class="sxs-lookup"><span data-stu-id="e434a-495">**Sales tax payable**</span></span> | <span data-ttu-id="e434a-496">**Belastbare inkopen**</span><span class="sxs-lookup"><span data-stu-id="e434a-496">**Taxable purchases**</span></span> | <span data-ttu-id="e434a-497">**Te ontvangen btw**</span><span class="sxs-lookup"><span data-stu-id="e434a-497">**Sales tax receivable**</span></span> | <span data-ttu-id="e434a-498">**Belastbare import**</span><span class="sxs-lookup"><span data-stu-id="e434a-498">**Taxable import**</span></span> | <span data-ttu-id="e434a-499">**Gebruiksbelasting**</span><span class="sxs-lookup"><span data-stu-id="e434a-499">**Use tax**</span></span> | <span data-ttu-id="e434a-500">**Gebruiksbelasting tegenrekenen**</span><span class="sxs-lookup"><span data-stu-id="e434a-500">**Offset use tax**</span></span> |
|--------------------|-------------------|-------------------|-----------------------|-----------------------|--------------------------|--------------------|-------------|--------------------|
| <span data-ttu-id="e434a-501">BE21</span><span class="sxs-lookup"><span data-stu-id="e434a-501">BE21</span></span>               | <span data-ttu-id="e434a-502">03</span><span class="sxs-lookup"><span data-stu-id="e434a-502">03</span></span>                |                   | <span data-ttu-id="e434a-503">54</span><span class="sxs-lookup"><span data-stu-id="e434a-503">54</span></span>                    |                       |                          |                    |             |                    |
| <span data-ttu-id="e434a-504">BE12</span><span class="sxs-lookup"><span data-stu-id="e434a-504">BE12</span></span>               | <span data-ttu-id="e434a-505">02</span><span class="sxs-lookup"><span data-stu-id="e434a-505">02</span></span>                |                   | <span data-ttu-id="e434a-506">54</span><span class="sxs-lookup"><span data-stu-id="e434a-506">54</span></span>                    |                       |                          |                    |             |                    |
| <span data-ttu-id="e434a-507">BE6</span><span class="sxs-lookup"><span data-stu-id="e434a-507">BE6</span></span>                | <span data-ttu-id="e434a-508">01</span><span class="sxs-lookup"><span data-stu-id="e434a-508">01</span></span>                |                   | <span data-ttu-id="e434a-509">54</span><span class="sxs-lookup"><span data-stu-id="e434a-509">54</span></span>                    |                       |                          |                    |             |                    |
| <span data-ttu-id="e434a-510">BEEU21</span><span class="sxs-lookup"><span data-stu-id="e434a-510">BEEU21</span></span>             |                   |                   |                       |                       | <span data-ttu-id="e434a-511">81</span><span class="sxs-lookup"><span data-stu-id="e434a-511">81</span></span>                       | <span data-ttu-id="e434a-512">86</span><span class="sxs-lookup"><span data-stu-id="e434a-512">86</span></span>                 | <span data-ttu-id="e434a-513">59</span><span class="sxs-lookup"><span data-stu-id="e434a-513">59</span></span>          | <span data-ttu-id="e434a-514">55</span><span class="sxs-lookup"><span data-stu-id="e434a-514">55</span></span>                 |
| <span data-ttu-id="e434a-515">BEEU12</span><span class="sxs-lookup"><span data-stu-id="e434a-515">BEEU12</span></span>             |                   |                   |                       |                       | <span data-ttu-id="e434a-516">81</span><span class="sxs-lookup"><span data-stu-id="e434a-516">81</span></span>                       | <span data-ttu-id="e434a-517">86</span><span class="sxs-lookup"><span data-stu-id="e434a-517">86</span></span>                 | <span data-ttu-id="e434a-518">59</span><span class="sxs-lookup"><span data-stu-id="e434a-518">59</span></span>          | <span data-ttu-id="e434a-519">55</span><span class="sxs-lookup"><span data-stu-id="e434a-519">55</span></span>                 |
| <span data-ttu-id="e434a-520">BEEU6</span><span class="sxs-lookup"><span data-stu-id="e434a-520">BEEU6</span></span>              |                   |                   |                       |                       | <span data-ttu-id="e434a-521">81</span><span class="sxs-lookup"><span data-stu-id="e434a-521">81</span></span>                       | <span data-ttu-id="e434a-522">86</span><span class="sxs-lookup"><span data-stu-id="e434a-522">86</span></span>                 | <span data-ttu-id="e434a-523">59</span><span class="sxs-lookup"><span data-stu-id="e434a-523">59</span></span>          | <span data-ttu-id="e434a-524">55</span><span class="sxs-lookup"><span data-stu-id="e434a-524">55</span></span>                 |
| <span data-ttu-id="e434a-525">BEEUS</span><span class="sxs-lookup"><span data-stu-id="e434a-525">BEEUS</span></span>              |                   | <span data-ttu-id="e434a-526">46</span><span class="sxs-lookup"><span data-stu-id="e434a-526">46</span></span>                |                       |                       |                          |                    |             |                    |

6.  <span data-ttu-id="e434a-527">Wijs op de pagina **Btw-codes** op het sneltabblad **Rapportinstellingen - creditnota** aangiftecodes toe aan btw-codes.</span><span class="sxs-lookup"><span data-stu-id="e434a-527">On the **Sales tax codes** page, on the **Report setup – credit note** FastTab, assign reporting codes to sales tax codes.</span></span>

<span data-ttu-id="e434a-528">In de volgende tabel wordt aangegeven hoe u de btw-aangiftecodes aan btw-codes kunt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e434a-528">The following table shows how to assign the sales tax reporting codes to sales tax codes.</span></span>

| <span data-ttu-id="e434a-529">**Btw-code**</span><span class="sxs-lookup"><span data-stu-id="e434a-529">**Sales tax code**</span></span> | <span data-ttu-id="e434a-530">**Belastbare verkoop CN**</span><span class="sxs-lookup"><span data-stu-id="e434a-530">**Taxable sales CN**</span></span> | <span data-ttu-id="e434a-531">**Verkoop zonder btw CN**</span><span class="sxs-lookup"><span data-stu-id="e434a-531">**Tax-free sale CN**</span></span> | <span data-ttu-id="e434a-532">**Te betalen btw CN**</span><span class="sxs-lookup"><span data-stu-id="e434a-532">**Sales tax payable CN**</span></span> | <span data-ttu-id="e434a-533">**Belastbare inkopen CN**</span><span class="sxs-lookup"><span data-stu-id="e434a-533">**Taxable purchases CN**</span></span> | <span data-ttu-id="e434a-534">**Te ontvangen btw CN**</span><span class="sxs-lookup"><span data-stu-id="e434a-534">**Sales tax receivable CN**</span></span> | <span data-ttu-id="e434a-535">**Belastbare import CN**</span><span class="sxs-lookup"><span data-stu-id="e434a-535">**Taxable import CN**</span></span> | <span data-ttu-id="e434a-536">**Gebruiksbelasting CN**</span><span class="sxs-lookup"><span data-stu-id="e434a-536">**Use tax CN**</span></span> | <span data-ttu-id="e434a-537">**Gebruiksbelasting tegenrekenen CN**</span><span class="sxs-lookup"><span data-stu-id="e434a-537">**Offset use tax CN**</span></span> |
|--------------------|----------------------|----------------------|--------------------------|--------------------------|-----------------------------|-----------------------|----------------|-----------------------|
| <span data-ttu-id="e434a-538">BEEU21</span><span class="sxs-lookup"><span data-stu-id="e434a-538">BEEU21</span></span>             |                      |                      |                          |                          | <span data-ttu-id="e434a-539">8184</span><span class="sxs-lookup"><span data-stu-id="e434a-539">8184</span></span>                        | <span data-ttu-id="e434a-540">86</span><span class="sxs-lookup"><span data-stu-id="e434a-540">86</span></span>                    | <span data-ttu-id="e434a-541">59</span><span class="sxs-lookup"><span data-stu-id="e434a-541">59</span></span>             | <span data-ttu-id="e434a-542">55</span><span class="sxs-lookup"><span data-stu-id="e434a-542">55</span></span>                    |
| <span data-ttu-id="e434a-543">BEEU12</span><span class="sxs-lookup"><span data-stu-id="e434a-543">BEEU12</span></span>             |                      |                      |                          |                          | <span data-ttu-id="e434a-544">8184</span><span class="sxs-lookup"><span data-stu-id="e434a-544">8184</span></span>                        | <span data-ttu-id="e434a-545">86</span><span class="sxs-lookup"><span data-stu-id="e434a-545">86</span></span>                    | <span data-ttu-id="e434a-546">59</span><span class="sxs-lookup"><span data-stu-id="e434a-546">59</span></span>             | <span data-ttu-id="e434a-547">55</span><span class="sxs-lookup"><span data-stu-id="e434a-547">55</span></span>                    |
| <span data-ttu-id="e434a-548">BEEU6</span><span class="sxs-lookup"><span data-stu-id="e434a-548">BEEU6</span></span>              |                      |                      |                          |                          | <span data-ttu-id="e434a-549">8184</span><span class="sxs-lookup"><span data-stu-id="e434a-549">8184</span></span>                        | <span data-ttu-id="e434a-550">86</span><span class="sxs-lookup"><span data-stu-id="e434a-550">86</span></span>                    | <span data-ttu-id="e434a-551">59</span><span class="sxs-lookup"><span data-stu-id="e434a-551">59</span></span>             | <span data-ttu-id="e434a-552">55</span><span class="sxs-lookup"><span data-stu-id="e434a-552">55</span></span>                    |

<span data-ttu-id="e434a-553">In plaats van de codes **55** en **59** kunt u correctiecodes **63** en **64** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e434a-553">Instead of codes **55** and **59**, you can use corrective codes **63** and **64**.</span></span>

> [!NOTE]
> <span data-ttu-id="e434a-554">De voorgaande configuratie is slechts een voorbeeld en is afhankelijk van de structuur van de btw-codes die worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e434a-554">The preceding configuration is just an example and depends on the structure of the sales tax codes that are used.</span></span> <span data-ttu-id="e434a-555">Als u wilt dat waarden worden berekend en overgeboekt naar de btw-aangifte, moet u voor elke btw-code die in het btw-betalingsproces wordt gebruikt, een relevante btw-aangiftecode instellen in een of meer velden op het tabblad **Rapportinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-555">If you want values to be calculated and transferred to the sales tax report, for each tax code that is used in the sales tax payment process, you must set a relevant sales tax reporting code in one or more fields on the **Report setup** tab.</span></span>

7.  <span data-ttu-id="e434a-556">Boek de volgende transacties.</span><span class="sxs-lookup"><span data-stu-id="e434a-556">Post the following transactions.</span></span> <span data-ttu-id="e434a-557">Voor klantfacturen gaat u bijvoorbeeld naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.</span><span class="sxs-lookup"><span data-stu-id="e434a-557">For example, for customer invoices, go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span> <span data-ttu-id="e434a-558">Voor leveranciersfacturen gaat u naar **Leveranciers** \> **Facturen** \> **Facturenjournaal**.</span><span class="sxs-lookup"><span data-stu-id="e434a-558">For vendor invoices, go to **Accounts payable** \> **Invoices** \> **Invoice journal**.</span></span>

| <span data-ttu-id="e434a-559">**Datum**</span><span class="sxs-lookup"><span data-stu-id="e434a-559">**Date**</span></span>         | <span data-ttu-id="e434a-560">**Transactietype**</span><span class="sxs-lookup"><span data-stu-id="e434a-560">**Transaction type**</span></span>  | <span data-ttu-id="e434a-561">**Nettobedrag**</span><span class="sxs-lookup"><span data-stu-id="e434a-561">**Amount net**</span></span> | <span data-ttu-id="e434a-562">**Btw-bedrag**</span><span class="sxs-lookup"><span data-stu-id="e434a-562">**VAT amount**</span></span> | <span data-ttu-id="e434a-563">**Btw-code**</span><span class="sxs-lookup"><span data-stu-id="e434a-563">**Sales tax code**</span></span> | <span data-ttu-id="e434a-564">**Verwachte belastingbasis: aangiftecode**</span><span class="sxs-lookup"><span data-stu-id="e434a-564">**Expected tax base – reporting code**</span></span>                 | <span data-ttu-id="e434a-565">**Verwacht belastingbedrag: aangiftecode**</span><span class="sxs-lookup"><span data-stu-id="e434a-565">**Expected tax amount – reporting code**</span></span> |
|------------------|-----------------------|----------------|----------------|--------------------|--------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="e434a-566">1 februari 2020</span><span class="sxs-lookup"><span data-stu-id="e434a-566">February 1, 2020</span></span> | <span data-ttu-id="e434a-567">Klantfactuur</span><span class="sxs-lookup"><span data-stu-id="e434a-567">Customer invoice</span></span>      | <span data-ttu-id="e434a-568">1,100</span><span class="sxs-lookup"><span data-stu-id="e434a-568">1,100</span></span>          | <span data-ttu-id="e434a-569">132</span><span class="sxs-lookup"><span data-stu-id="e434a-569">132</span></span>            | <span data-ttu-id="e434a-570">BE12</span><span class="sxs-lookup"><span data-stu-id="e434a-570">BE12</span></span>               | <span data-ttu-id="e434a-571">02</span><span class="sxs-lookup"><span data-stu-id="e434a-571">02</span></span>                                                     | <span data-ttu-id="e434a-572">54</span><span class="sxs-lookup"><span data-stu-id="e434a-572">54</span></span>                                       |
| <span data-ttu-id="e434a-573">1 februari 2020</span><span class="sxs-lookup"><span data-stu-id="e434a-573">February 1, 2020</span></span> | <span data-ttu-id="e434a-574">Leveranciersfactuur (EU)</span><span class="sxs-lookup"><span data-stu-id="e434a-574">Vendor invoice (EU)</span></span>   | <span data-ttu-id="e434a-575">1.000</span><span class="sxs-lookup"><span data-stu-id="e434a-575">1,000</span></span>          | <span data-ttu-id="e434a-576">210</span><span class="sxs-lookup"><span data-stu-id="e434a-576">210</span></span>            | <span data-ttu-id="e434a-577">BEEU21</span><span class="sxs-lookup"><span data-stu-id="e434a-577">BEEU21</span></span>             | <span data-ttu-id="e434a-578">86 – Te betalen basis 81 – basisinhouding</span><span class="sxs-lookup"><span data-stu-id="e434a-578">86 – Base payable 81 – Base deduction</span></span>                  | <span data-ttu-id="e434a-579">55 – te betalen belasting 59 – belastingaftrek</span><span class="sxs-lookup"><span data-stu-id="e434a-579">55 – Tax payable 59 – Tax deduction</span></span>      |
| <span data-ttu-id="e434a-580">2 februari 2020</span><span class="sxs-lookup"><span data-stu-id="e434a-580">February 2, 2020</span></span> | <span data-ttu-id="e434a-581">Leveranciersfactuur (EU)</span><span class="sxs-lookup"><span data-stu-id="e434a-581">Vendor invoice (EU)</span></span>   | <span data-ttu-id="e434a-582">\-200</span><span class="sxs-lookup"><span data-stu-id="e434a-582">\-200</span></span>          | <span data-ttu-id="e434a-583">\-42</span><span class="sxs-lookup"><span data-stu-id="e434a-583">\-42</span></span>           | <span data-ttu-id="e434a-584">BEEU21</span><span class="sxs-lookup"><span data-stu-id="e434a-584">BEEU21</span></span>             | <span data-ttu-id="e434a-585">86 – Te betalen basis 81 – basisinhouding 84 – kredietbasis</span><span class="sxs-lookup"><span data-stu-id="e434a-585">86 – Base payable 81 – Base deduction 84 – Credit base</span></span> | <span data-ttu-id="e434a-586">55 – te betalen belasting 59 – belastingaftrek</span><span class="sxs-lookup"><span data-stu-id="e434a-586">55 – Tax payable 59 – Tax deduction</span></span>      |
| <span data-ttu-id="e434a-587">1 februari 2020</span><span class="sxs-lookup"><span data-stu-id="e434a-587">February 1, 2020</span></span> | <span data-ttu-id="e434a-588">Klantfactuur (EU)</span><span class="sxs-lookup"><span data-stu-id="e434a-588">Customer invoice (EU)</span></span> | <span data-ttu-id="e434a-589">100</span><span class="sxs-lookup"><span data-stu-id="e434a-589">100</span></span>            | <span data-ttu-id="e434a-590">0</span><span class="sxs-lookup"><span data-stu-id="e434a-590">0</span></span>              | <span data-ttu-id="e434a-591">BEEUS</span><span class="sxs-lookup"><span data-stu-id="e434a-591">BEEUS</span></span>              | <span data-ttu-id="e434a-592">46</span><span class="sxs-lookup"><span data-stu-id="e434a-592">46</span></span>                                                     | <span data-ttu-id="e434a-593">Niet van toepassing</span><span class="sxs-lookup"><span data-stu-id="e434a-593">Not applicable</span></span>                           |

8.  <span data-ttu-id="e434a-594">Ga naar **Belasting \> Aangiften \> Btw \> Btw rapporteren voor vereffeningsperiode**.</span><span class="sxs-lookup"><span data-stu-id="e434a-594">Go to **Tax \> Declarations \> Sales tax \> Report sales tax for settlement period**.</span></span>
9.  <span data-ttu-id="e434a-595">Selecteer in het dialoogvenster **Btw rapporteren voor vereffeningsperiode** in het veld **Versie van btw-betaling** de optie **Origineel**.</span><span class="sxs-lookup"><span data-stu-id="e434a-595">In the **Report sales tax for settlement period** dialog box, in the **Sales tax payment version** field, select **Original**.</span></span>
10.  <span data-ttu-id="e434a-596">Selecteer **OK** en bekijk de gegevens.</span><span class="sxs-lookup"><span data-stu-id="e434a-596">Select **OK**, and review the data.</span></span>

![Gegenereerde pagina INTERVAT-btw-aangifte](media/4_Intervat_tax_declaration.png)

<span data-ttu-id="e434a-598">U ziet dat het bedrag van de creditnota wordt weergegeven in code **84**.</span><span class="sxs-lookup"><span data-stu-id="e434a-598">Notice that the amount of the credit note is shown in code **84**.</span></span>

11.  <span data-ttu-id="e434a-599">Ga naar **Belasting \> Aangiften \> Btw \> Aanvullende btw-rapportvakken**.</span><span class="sxs-lookup"><span data-stu-id="e434a-599">Go to **Tax \> Declarations \> Sales tax \> Additional sales tax report boxes**.</span></span>
12.  <span data-ttu-id="e434a-600">Selecteer **Nieuw** om een regel voor februari 2020 te maken.</span><span class="sxs-lookup"><span data-stu-id="e434a-600">Select **New** to create a line for February 2020.</span></span>
13.  <span data-ttu-id="e434a-601">Selecteer **Btw-correcties \> Correcties** en maak een regel.</span><span class="sxs-lookup"><span data-stu-id="e434a-601">Select **Tax corrections \> Adjustments**, and create a line.</span></span>

![Pagina Correcties](media/5_Adjustments.png)

14.  <span data-ttu-id="e434a-603">Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **Btw vereffenen en boeken**.</span><span class="sxs-lookup"><span data-stu-id="e434a-603">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
15.  <span data-ttu-id="e434a-604">Selecteer in het dialoogvenster **Btw vereffenen en boeken** in het veld **Versie van btw-betaling** de optie **Origineel**.</span><span class="sxs-lookup"><span data-stu-id="e434a-604">In the **Settle and post sales tax** dialog box, in the **Sales tax payment version** field, select **Original**.</span></span>
16.  <span data-ttu-id="e434a-605">Ga naar **Belasting** \> **Aangiften** \> **Btw** \> **INTERVAT-belastingaangifte**.</span><span class="sxs-lookup"><span data-stu-id="e434a-605">Go to **Tax** \> **Declarations** \> **Sales tax** \> **INTERVAT tax declaration**.</span></span>
17.  <span data-ttu-id="e434a-606">Selecteer **Nieuwe aangifte** en stel de volgende waarden in:</span><span class="sxs-lookup"><span data-stu-id="e434a-606">Select **New declaration**, set the following values:</span></span>

   -   <span data-ttu-id="e434a-607">**Vereffeningsperiode:** MEN</span><span class="sxs-lookup"><span data-stu-id="e434a-607">**Settlement period:** MEN</span></span>
   -   <span data-ttu-id="e434a-608">**Vanaf datum:** 1-2-2020 (1 februari 2020)</span><span class="sxs-lookup"><span data-stu-id="e434a-608">**From date:** 2/1/2020 (February 1, 2020)</span></span>
   -   <span data-ttu-id="e434a-609">**Transactiedatum:** 29-2-2020 (29 februari 2020)</span><span class="sxs-lookup"><span data-stu-id="e434a-609">**Transaction date:** 2/29/2020 (February 29, 2020)</span></span>
   -   <span data-ttu-id="e434a-610">**Update:** Nee</span><span class="sxs-lookup"><span data-stu-id="e434a-610">**Update:** No</span></span>
   -   <span data-ttu-id="e434a-611">**Indelingstoewijzing:** INTERVAT-indeling (BE)</span><span class="sxs-lookup"><span data-stu-id="e434a-611">**Format mapping:** INTERVAT format (BE)</span></span>

![Pagina INTERVAT-belastingaangifte](media/6_Intervat.png)

18.  <span data-ttu-id="e434a-613">Selecteer **OK**, open het bestand en bekijk het rapport.</span><span class="sxs-lookup"><span data-stu-id="e434a-613">Select **OK**, open the file, and review the report.</span></span>

![xml-rapport met INTERVAT-belastingaangifte](media/7_Intervat_XML.png)

19.  <span data-ttu-id="e434a-615">Selecteer **Details** en bekijk de gegevens.</span><span class="sxs-lookup"><span data-stu-id="e434a-615">Select **Details**, and review the data.</span></span>

![Pagina INTERVAT-gegevens](media/8_Intervat_details.png)

<span data-ttu-id="e434a-617">Zoals u ziet, is het bedrag in code **62** gelijk aan **200**.</span><span class="sxs-lookup"><span data-stu-id="e434a-617">Notice that the amount in **62** code equals **200**.</span></span>
    
## <a name="reconciliation-reports-for-belgium"></a><span data-ttu-id="e434a-618">Afstemmingsrapporten voor België</span><span class="sxs-lookup"><span data-stu-id="e434a-618">Reconciliation reports for Belgium</span></span>

<span data-ttu-id="e434a-619">Zie voor informatie over afstemmingsrapporten voor België [Afstemmingsrapporten voor België](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/localizations/emea-bel-reconciliation-reports.md).</span><span class="sxs-lookup"><span data-stu-id="e434a-619">For information about reconciliation reports for Belgium, see [Reconciliation reports for Belgium](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/finance/localizations/emea-bel-reconciliation-reports.md).</span></span>




