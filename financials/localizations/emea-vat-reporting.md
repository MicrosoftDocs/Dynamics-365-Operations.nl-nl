---
title: Btw-aangifte voor Europa
description: Dit onderwerp bevat algemene informatie over het instellen en genereren van het btw-overzicht (belasting toegevoegde waarde) voor een aantal Europese landen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c0be253e80636d659027f69cbac58062cb28269e
ms.contentlocale: nl-nl
ms.lasthandoff: 07/21/2017

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="bd451-103">Btw-aangifte voor Europa</span><span class="sxs-lookup"><span data-stu-id="bd451-103">VAT reporting for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bd451-104">Dit onderwerp bevat algemene informatie over het instellen en genereren van het btw-overzicht (belasting toegevoegde waarde) voor een aantal Europese landen.</span><span class="sxs-lookup"><span data-stu-id="bd451-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="bd451-105">Dit onderwerp biedt een algemene aanpak voor het instellen en genereren van de btw-aangifte.</span><span class="sxs-lookup"><span data-stu-id="bd451-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="bd451-106">Deze benadering geldt voor alle gebruikers in rechtspersonen in de volgende landen:</span><span class="sxs-lookup"><span data-stu-id="bd451-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="bd451-107">Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="bd451-107">Austria</span></span>
-   <span data-ttu-id="bd451-108">België</span><span class="sxs-lookup"><span data-stu-id="bd451-108">Belgium</span></span>
-   <span data-ttu-id="bd451-109">Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="bd451-109">Czech Republic</span></span>
-   <span data-ttu-id="bd451-110">Estland</span><span class="sxs-lookup"><span data-stu-id="bd451-110">Estonia</span></span>
-   <span data-ttu-id="bd451-111">Finland</span><span class="sxs-lookup"><span data-stu-id="bd451-111">Finland</span></span>
-   <span data-ttu-id="bd451-112">Duitsland</span><span class="sxs-lookup"><span data-stu-id="bd451-112">Germany</span></span>
-   <span data-ttu-id="bd451-113">Letland</span><span class="sxs-lookup"><span data-stu-id="bd451-113">Latvia</span></span>
-   <span data-ttu-id="bd451-114">Litouwen</span><span class="sxs-lookup"><span data-stu-id="bd451-114">Lithuania</span></span>
-   <span data-ttu-id="bd451-115">Nederland</span><span class="sxs-lookup"><span data-stu-id="bd451-115">Netherlands</span></span>
-   <span data-ttu-id="bd451-116">Zweden</span><span class="sxs-lookup"><span data-stu-id="bd451-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="bd451-117">Overzicht btw-overzichten</span><span class="sxs-lookup"><span data-stu-id="bd451-117">VAT statement overview</span></span>
<span data-ttu-id="bd451-118">Het btw-overzicht is gebaseerd op bedragen van belastingtransacties.</span><span class="sxs-lookup"><span data-stu-id="bd451-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="bd451-119">Het proces voor het genereren van een btw-aangifte is onderdeel van het btw-betalingsproces dat is geïmplementeerd via de functie Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="bd451-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="bd451-120">Met deze functie wordt de btw berekend die verschuldigd is voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="bd451-121">De berekening van de vereffening omvat de geboekte btw voor de geselecteerde vereffeningsperiode voor de belastingtransacties.</span><span class="sxs-lookup"><span data-stu-id="bd451-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="bd451-122">Het proces voor het berekenen van gegevens voor een btw-overzicht is gebaseerd op de relatie tussen btw-codes en btw-aangiftecodes, waarbij btw-aangiftecodes overeenkomen met de btw-overzichtvakken (of labels in XML).</span><span class="sxs-lookup"><span data-stu-id="bd451-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="bd451-123">Voor elke btw-code moeten er btw-aangiftecodes worden ingesteld voor elk type transactie, zoals belastbare verkoop, belastbare inkopen, belastbare import.</span><span class="sxs-lookup"><span data-stu-id="bd451-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="bd451-124">Dit transactietype wordt beschreven in het gedeelte Btw-codes voor btw-aangifte verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="bd451-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="bd451-125">Voor elke btw-aangiftecode moet een specifieke rapportindeling worden bepaald.</span><span class="sxs-lookup"><span data-stu-id="bd451-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="bd451-126">Btw-codes worden tegelijkertijd gekoppeld aan een specifieke btw-dienst via btw-vereffeningsperioden.</span><span class="sxs-lookup"><span data-stu-id="bd451-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="bd451-127">Voor elke btw-dienst moet een rapportindeling worden bepaald.</span><span class="sxs-lookup"><span data-stu-id="bd451-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="bd451-128">Dus alleen btw-aangiftecodes met dezelfde rapportindeling als die is ingesteld voor een btw-dienst in btw-vereffeningsperioden voor btw-code, kunnen worden geselecteerd in de rapportinstelling van de btw-code.</span><span class="sxs-lookup"><span data-stu-id="bd451-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="bd451-129">Een btw-transactie die is gegenereerd bij het boeken van een order of een journaal, bevat een btw-code, btw-bron, btw-richting en transactiebedragen (belastingbasisbedrag en belastingbedrag in valuta voor boekhouding, btw-valuta en transactievaluta).</span><span class="sxs-lookup"><span data-stu-id="bd451-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="bd451-130">Op basis van de combinatie van belastingtransactiekenmerken bestaan transactiebedragen uit totaalbedragen voor btw-aangiftecodes die zijn opgegeven voor btw-codes.</span><span class="sxs-lookup"><span data-stu-id="bd451-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="bd451-131">In de volgende afbeelding wordt de gegevensrelatie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bd451-131">The following illustration shows the data relationship.</span></span>

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="bd451-133">Instelling btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="bd451-133">VAT statement setup</span></span>
<span data-ttu-id="bd451-134">Als u een btw-overzicht wilt genereren, moet u het volgende instellen.</span><span class="sxs-lookup"><span data-stu-id="bd451-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="bd451-135">Btw-diensten voor btw-rapportage</span><span class="sxs-lookup"><span data-stu-id="bd451-135">Sales tax authorities for VAT reporting</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-authorities). -->
<span data-ttu-id="bd451-136">Voordat u btw-aangiftecodes kunt instellen, moet u de juiste rapportindeling voor de btw-dienst selecteren.</span><span class="sxs-lookup"><span data-stu-id="bd451-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="bd451-137">Selecteer op de pagina **Btw-diensten** in de sectie **Algemeen** een **Rapportindeling**.</span><span class="sxs-lookup"><span data-stu-id="bd451-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="bd451-138">Deze indeling wordt gebruikt bij het instellen van btw-aangiftecodes.</span><span class="sxs-lookup"><span data-stu-id="bd451-138">This layout will be used when you set up sales tax reporting codes.</span></span>

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="bd451-139">Btw-aangiftecodes</span><span class="sxs-lookup"><span data-stu-id="bd451-139">Sales tax reporting codes</span></span>

<span data-ttu-id="bd451-140">Btw-aangiftecodes zijn vakcodes in het btw-overzicht of labelnamen in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="bd451-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="bd451-141">Deze codes worden gebruikt voor het samenvoegen en voorbereiden van bedragen voor het rapport.</span><span class="sxs-lookup"><span data-stu-id="bd451-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="bd451-142">De namen van de resultaatbedragen worden gebruikt bij het configureren van de ER-indeling (elektronische rapportage) van het btw-overzicht.</span><span class="sxs-lookup"><span data-stu-id="bd451-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="bd451-143">U kunt btw-aangiftecodes maken en onderhouden op de pagina **Btw-aangiftecodes**.</span><span class="sxs-lookup"><span data-stu-id="bd451-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="bd451-144">U moet aan elke code een rapportindeling toewijzen.</span><span class="sxs-lookup"><span data-stu-id="bd451-144">You must assign each code a report layout.</span></span> <span data-ttu-id="bd451-145">Nadat u de btw-aangiftecodes hebt gemaakt, kunt u de codes kiezen in de sectie **Rapport instellen** op de pagina **Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="bd451-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-reporting-codes).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="bd451-146">Btw-codes voor btw-aangifte</span><span class="sxs-lookup"><span data-stu-id="bd451-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-codes).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the **Sales tax codes** page. The following table describes the transaction types in the report setup for sales tax codes. The calculation includes transactions for all types of sources except sales tax.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bd451-147"><strong>Transactietype</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-147"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="bd451-148"><strong>Omschrijving van transacties en bedragen die moeten worden geteld voor het transactietype</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-148"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-149"><strong>Belastbare verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-149"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="bd451-150">Som van <strong>Belastingbasisbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-150">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-151">Transactiedatum bevindt zich in de geselecteerde periode/</span><span class="sxs-lookup"><span data-stu-id="bd451-151">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="bd451-152">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-152">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="bd451-153">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-153">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-154"><strong>Verkoop zonder btw</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-154"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="bd451-155">Som van <strong>Belastingbasisbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-155">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-156">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-156">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-157">De verkoop is export (<strong>Belastingrichting</strong> is <strong>Verkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-157">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="bd451-158">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-158">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-159"><strong>Te betalen btw</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-159"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="bd451-160">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-160">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-161">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-161">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-162">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-162">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="bd451-163">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-163">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-164"><strong>Creditnota belastbare verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-164"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="bd451-165">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-165">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-166">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-166">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-167">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-167">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="bd451-168">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-168">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-169"><strong>Creditnota vrijgestelde verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-169"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="bd451-170">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-170">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-171">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-171">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-172">De verkoop is export (<strong>Belastingrichting</strong> is <strong>Verkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-172">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="bd451-173">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-173">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-174"><strong>Btw op creditnota verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-174"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="bd451-175">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-175">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-176">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-176">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-177">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-177">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="bd451-178">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-178">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-179"><strong>Belastbare inkopen</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-179"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="bd451-180">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-180">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-181">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-181">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-182">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-182">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="bd451-183">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-183">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-184"><strong>Inkoop zonder btw</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-184"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="bd451-185">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-185">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-186">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-186">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-187">De inkoop is import (<strong>Belastingrichting</strong> is <strong>Inkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-187">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="bd451-188">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-188">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-189"><strong>Te ontvangen btw</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-189"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="bd451-190">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-190">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-191">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-191">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-192">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-192">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="bd451-193">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-193">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-194"><strong>Creditnota belastbare inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-194"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="bd451-195">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-195">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-196">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-196">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-197">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-197">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="bd451-198">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-198">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-199"><strong>Creditnota vrijgestelde inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-199"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="bd451-200">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-200">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-201">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-201">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-202">De inkoop is import (<strong>Belastingrichting</strong> is <strong>Inkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-202">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="bd451-203">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-203">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-204"><strong>Btw op creditnota inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-204"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="bd451-205">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-205">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-206">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-206">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-207">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="bd451-207">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="bd451-208">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-208">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-209"><strong>Belastbare import</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-209"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="bd451-210">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-210">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-211">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-211">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-212"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-212"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="bd451-213">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-213">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-214"><strong>Belastbare import tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-214"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="bd451-215">Omgekeerde som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-215">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-216">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-216">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-217"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd451-217"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="bd451-218">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-218">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-219"><strong>Creditnota belastbare import</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-219"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="bd451-220">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-220">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-221">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-221">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="bd451-222">e</span><span class="sxs-lookup"><span data-stu-id="bd451-222">e</span></span><li><span data-ttu-id="bd451-223"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd451-223"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="bd451-224">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-224">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-225"><strong>Creditnota belastbare import tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-225"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="bd451-226">Omgekeerde som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-226">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-227">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-227">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-228">Belastingrichting is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd451-228">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="bd451-229">d</span><span class="sxs-lookup"><span data-stu-id="bd451-229">d</span></span><li><span data-ttu-id="bd451-230">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-230">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bd451-231"><strong>Gebruiksbelasting</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-231"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="bd451-232">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-232">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-233">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-233">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-234"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd451-234"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="bd451-235">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-235">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bd451-236"><strong>Gebruiksbelasting tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="bd451-236"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="bd451-237">Omgekeerde som van <strong>Belastingbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="bd451-237">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="bd451-238">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="bd451-238">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="bd451-239"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd451-239"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="bd451-240">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="bd451-240">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bd451-241">Voor de bovenstaande tabel wordt ervan uitgegaan dat aan de volgende criteria wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="bd451-241">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="bd451-242">Het belastingbasisbedrag is een transactiebedrag van het veld **Oorsprong in valuta voor boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="bd451-242">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="bd451-243">Het belastingbedrag is een transitiebedrag van het veld **Werkelijke btw-bedrag in valuta voor boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="bd451-243">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="bd451-244">Het ER-model configureren en indelen voor het rapport</span><span class="sxs-lookup"><span data-stu-id="bd451-244">Configure the ER model and format for the report</span></span>

<span data-ttu-id="bd451-245">U kunt elektronische rapportage (ER) gebruiken om overzichten en aangifte te configureren en om gegevens te exporteren in verschillende elektronische indelingen zonder de X ++-code te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="bd451-245">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="bd451-246">Voor aanvullende informatie:</span><span class="sxs-lookup"><span data-stu-id="bd451-246">For additional information:</span></span>

-   [<span data-ttu-id="bd451-247">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="bd451-247">Electronic reporting overview</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting)
-   [<span data-ttu-id="bd451-248">Elektronische rapportageconfiguraties downloaden van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="bd451-248">Download Electronic reporting configurations from Lifecycle Services</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [<span data-ttu-id="bd451-249">Lokalisatievereisten: een GER-configuratie maken</span><span class="sxs-lookup"><span data-stu-id="bd451-249">Localization requirements – Create a GER configuration</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="bd451-250">Landspecifieke resources voor btw-overzichten</span><span class="sxs-lookup"><span data-stu-id="bd451-250">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="bd451-251">Het btw-overzicht voor elk land moet voldoen aan de vereisten van de wetgeving van het land.</span><span class="sxs-lookup"><span data-stu-id="bd451-251">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="bd451-252">Er zijn vooraf gedefinieerde algemene modellen en indelingen van btw-overzichten voor de landen die in de volgende tabel staan.</span><span class="sxs-lookup"><span data-stu-id="bd451-252">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="bd451-253">Land/regio</span><span class="sxs-lookup"><span data-stu-id="bd451-253">Country</span></span>        | <span data-ttu-id="bd451-254">Aanvullende gegevens</span><span class="sxs-lookup"><span data-stu-id="bd451-254">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="bd451-255">Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="bd451-255">Austria</span></span>        |  [<span data-ttu-id="bd451-256">Details btw-overzicht voor Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="bd451-256">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="bd451-257">België</span><span class="sxs-lookup"><span data-stu-id="bd451-257">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="bd451-258">Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="bd451-258">Czech Republic</span></span> |  [<span data-ttu-id="bd451-259">Details btw-overzicht voor de Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="bd451-259">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="bd451-260">Estland</span><span class="sxs-lookup"><span data-stu-id="bd451-260">Estonia</span></span>        |  [<span data-ttu-id="bd451-261">Details btw-overzicht voor Estland</span><span class="sxs-lookup"><span data-stu-id="bd451-261">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="bd451-262">Finland</span><span class="sxs-lookup"><span data-stu-id="bd451-262">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="bd451-263">Duitsland</span><span class="sxs-lookup"><span data-stu-id="bd451-263">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="bd451-264">Italië</span><span class="sxs-lookup"><span data-stu-id="bd451-264">Italy</span></span>          | [<span data-ttu-id="bd451-265">Details btw-overzicht voor Italië</span><span class="sxs-lookup"><span data-stu-id="bd451-265">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="bd451-266">Letland</span><span class="sxs-lookup"><span data-stu-id="bd451-266">Latvia</span></span>         | [<span data-ttu-id="bd451-267">Details btw-overzicht voor Letland</span><span class="sxs-lookup"><span data-stu-id="bd451-267">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="bd451-268">Litouwen</span><span class="sxs-lookup"><span data-stu-id="bd451-268">Lithuania</span></span>      | [<span data-ttu-id="bd451-269">Details btw-overzicht voor Litouwen</span><span class="sxs-lookup"><span data-stu-id="bd451-269">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="bd451-270">Nederland</span><span class="sxs-lookup"><span data-stu-id="bd451-270">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="bd451-271">Zweden</span><span class="sxs-lookup"><span data-stu-id="bd451-271">Sweden</span></span>         |                                                                                 |






