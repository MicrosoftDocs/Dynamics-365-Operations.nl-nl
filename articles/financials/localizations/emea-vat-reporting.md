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
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: afcc2ea8c0ca3a5877b44fd758aec9d2caf92d92
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="d55d2-103">Btw-aangifte voor Europa</span><span class="sxs-lookup"><span data-stu-id="d55d2-103">VAT reporting for Europe</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d55d2-104">Dit onderwerp bevat algemene informatie over het instellen en genereren van het btw-overzicht (belasting toegevoegde waarde) voor een aantal Europese landen.</span><span class="sxs-lookup"><span data-stu-id="d55d2-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="d55d2-105">Dit onderwerp biedt een algemene aanpak voor het instellen en genereren van de btw-aangifte.</span><span class="sxs-lookup"><span data-stu-id="d55d2-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="d55d2-106">Deze benadering geldt voor alle gebruikers in rechtspersonen in de volgende landen:</span><span class="sxs-lookup"><span data-stu-id="d55d2-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="d55d2-107">Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="d55d2-107">Austria</span></span>
-   <span data-ttu-id="d55d2-108">België</span><span class="sxs-lookup"><span data-stu-id="d55d2-108">Belgium</span></span>
-   <span data-ttu-id="d55d2-109">Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="d55d2-109">Czech Republic</span></span>
-   <span data-ttu-id="d55d2-110">Estland</span><span class="sxs-lookup"><span data-stu-id="d55d2-110">Estonia</span></span>
-   <span data-ttu-id="d55d2-111">Finland</span><span class="sxs-lookup"><span data-stu-id="d55d2-111">Finland</span></span>
-   <span data-ttu-id="d55d2-112">Duitsland</span><span class="sxs-lookup"><span data-stu-id="d55d2-112">Germany</span></span>
-   <span data-ttu-id="d55d2-113">Letland</span><span class="sxs-lookup"><span data-stu-id="d55d2-113">Latvia</span></span>
-   <span data-ttu-id="d55d2-114">Litouwen</span><span class="sxs-lookup"><span data-stu-id="d55d2-114">Lithuania</span></span>
-   <span data-ttu-id="d55d2-115">Nederland</span><span class="sxs-lookup"><span data-stu-id="d55d2-115">Netherlands</span></span>
-   <span data-ttu-id="d55d2-116">Zweden</span><span class="sxs-lookup"><span data-stu-id="d55d2-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="d55d2-117">Overzicht btw-overzichten</span><span class="sxs-lookup"><span data-stu-id="d55d2-117">VAT statement overview</span></span>
<span data-ttu-id="d55d2-118">Het btw-overzicht is gebaseerd op bedragen van belastingtransacties.</span><span class="sxs-lookup"><span data-stu-id="d55d2-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="d55d2-119">Het proces voor het genereren van een btw-aangifte is onderdeel van het btw-betalingsproces dat is geïmplementeerd via de functie Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="d55d2-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="d55d2-120">Met deze functie wordt de btw berekend die verschuldigd is voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="d55d2-121">De berekening van de vereffening omvat de geboekte btw voor de geselecteerde vereffeningsperiode voor de belastingtransacties.</span><span class="sxs-lookup"><span data-stu-id="d55d2-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="d55d2-122">Het proces voor het berekenen van gegevens voor een btw-overzicht is gebaseerd op de relatie tussen btw-codes en btw-aangiftecodes, waarbij btw-aangiftecodes overeenkomen met de btw-overzichtvakken (of labels in XML).</span><span class="sxs-lookup"><span data-stu-id="d55d2-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="d55d2-123">Voor elke btw-code moeten er btw-aangiftecodes worden ingesteld voor elk type transactie, zoals belastbare verkoop, belastbare inkopen, belastbare import.</span><span class="sxs-lookup"><span data-stu-id="d55d2-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="d55d2-124">Dit transactietype wordt beschreven in het gedeelte Btw-codes voor btw-aangifte verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="d55d2-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="d55d2-125">Voor elke btw-aangiftecode moet een specifieke rapportindeling worden bepaald.</span><span class="sxs-lookup"><span data-stu-id="d55d2-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="d55d2-126">Btw-codes worden tegelijkertijd gekoppeld aan een specifieke btw-dienst via btw-vereffeningsperioden.</span><span class="sxs-lookup"><span data-stu-id="d55d2-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="d55d2-127">Voor elke btw-dienst moet een rapportindeling worden bepaald.</span><span class="sxs-lookup"><span data-stu-id="d55d2-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="d55d2-128">Dus alleen btw-aangiftecodes met dezelfde rapportindeling als die is ingesteld voor een btw-dienst in btw-vereffeningsperioden voor btw-code, kunnen worden geselecteerd in de rapportinstelling van de btw-code.</span><span class="sxs-lookup"><span data-stu-id="d55d2-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="d55d2-129">Een btw-transactie die is gegenereerd bij het boeken van een order of een journaal, bevat een btw-code, btw-bron, btw-richting en transactiebedragen (belastingbasisbedrag en belastingbedrag in valuta voor boekhouding, btw-valuta en transactievaluta).</span><span class="sxs-lookup"><span data-stu-id="d55d2-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="d55d2-130">Op basis van de combinatie van belastingtransactiekenmerken bestaan transactiebedragen uit totaalbedragen voor btw-aangiftecodes die zijn opgegeven voor btw-codes.</span><span class="sxs-lookup"><span data-stu-id="d55d2-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="d55d2-131">In de volgende afbeelding wordt de gegevensrelatie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d55d2-131">The following illustration shows the data relationship.</span></span>

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="d55d2-133">Instelling btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="d55d2-133">VAT statement setup</span></span>
<span data-ttu-id="d55d2-134">Als u een btw-overzicht wilt genereren, moet u het volgende instellen.</span><span class="sxs-lookup"><span data-stu-id="d55d2-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="d55d2-135">Btw-diensten voor btw-rapportage</span><span class="sxs-lookup"><span data-stu-id="d55d2-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="d55d2-136">Voordat u btw-aangiftecodes kunt instellen, moet u de juiste rapportindeling voor de btw-dienst selecteren.</span><span class="sxs-lookup"><span data-stu-id="d55d2-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="d55d2-137">Selecteer op de pagina **Btw-diensten** in de sectie **Algemeen** een **Rapportindeling**.</span><span class="sxs-lookup"><span data-stu-id="d55d2-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="d55d2-138">Deze indeling wordt gebruikt bij het instellen van btw-aangiftecodes.</span><span class="sxs-lookup"><span data-stu-id="d55d2-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="d55d2-139">Btw-aangiftecodes</span><span class="sxs-lookup"><span data-stu-id="d55d2-139">Sales tax reporting codes</span></span>

<span data-ttu-id="d55d2-140">Btw-aangiftecodes zijn vakcodes in het btw-overzicht of labelnamen in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="d55d2-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="d55d2-141">Deze codes worden gebruikt voor het samenvoegen en voorbereiden van bedragen voor het rapport.</span><span class="sxs-lookup"><span data-stu-id="d55d2-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="d55d2-142">De namen van de resultaatbedragen worden gebruikt bij het configureren van de ER-indeling (elektronische rapportage) van het btw-overzicht.</span><span class="sxs-lookup"><span data-stu-id="d55d2-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="d55d2-143">U kunt btw-aangiftecodes maken en onderhouden op de pagina **Btw-aangiftecodes**.</span><span class="sxs-lookup"><span data-stu-id="d55d2-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="d55d2-144">U moet aan elke code een rapportindeling toewijzen.</span><span class="sxs-lookup"><span data-stu-id="d55d2-144">You must assign each code a report layout.</span></span> <span data-ttu-id="d55d2-145">Nadat u de btw-aangiftecodes hebt gemaakt, kunt u de codes kiezen in de sectie **Rapport instellen** op de pagina **Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="d55d2-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="d55d2-146">Btw-codes voor btw-aangifte</span><span class="sxs-lookup"><span data-stu-id="d55d2-146">Sales tax codes for VAT reporting</span></span>

<span data-ttu-id="d55d2-147">Pagina <!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Btw-codes</strong>.</span><span class="sxs-lookup"><span data-stu-id="d55d2-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="d55d2-148">In de volgende tabel worden de transactietypen beschreven in de rapportinstelling voor btw-codes.</span><span class="sxs-lookup"><span data-stu-id="d55d2-148">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="d55d2-149">De berekening omvat de transacties voor alle typen bronnen met uitzondering van btw.</span><span class="sxs-lookup"><span data-stu-id="d55d2-149">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d55d2-150"><strong>Transactietype</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-150"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="d55d2-151"><strong>Omschrijving van transacties en bedragen die moeten worden geteld voor het transactietype</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-151"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-152"><strong>Belastbare verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-152"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="d55d2-153">Som van <strong>Belastingbasisbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-153">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-154">Transactiedatum bevindt zich in de geselecteerde periode/</span><span class="sxs-lookup"><span data-stu-id="d55d2-154">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="d55d2-155">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-155">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-156">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-156">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-157"><strong>Verkoop zonder btw</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-157"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="d55d2-158">Som van <strong>Belastingbasisbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-158">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-159">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-159">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-160">De verkoop is export (<strong>Belastingrichting</strong> is <strong>Verkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-160">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-161">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-161">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-162"><strong>Te betalen btw</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-162"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="d55d2-163">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-163">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-164">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-164">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-165">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-165">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-166">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-166">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-167"><strong>Creditnota belastbare verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-167"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="d55d2-168">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-168">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-169">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-169">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-170">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-170">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-171">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-171">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-172"><strong>Creditnota vrijgestelde verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-172"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="d55d2-173">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-173">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-174">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-174">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-175">De verkoop is export (<strong>Belastingrichting</strong> is <strong>Verkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-175">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-176">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-176">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-177"><strong>Btw op creditnota verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-177"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="d55d2-178">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-178">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-179">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-179">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-180">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-180">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-181">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-181">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-182"><strong>Belastbare inkopen</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-182"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="d55d2-183">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-183">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-184">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-184">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-185">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-185">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-186">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-186">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-187"><strong>Inkoop zonder btw</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-187"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="d55d2-188">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-188">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-189">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-189">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-190">De inkoop is import (<strong>Belastingrichting</strong> is <strong>Inkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-190">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-191">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-191">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-192"><strong>Te ontvangen btw</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-192"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="d55d2-193">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-193">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-194">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-194">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-195">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-195">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-196">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-196">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-197"><strong>Creditnota belastbare inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-197"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="d55d2-198">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-198">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-199">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-199">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-200">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-200">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-201">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-201">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-202"><strong>Creditnota vrijgestelde inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-202"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="d55d2-203">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-203">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-204">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-204">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-205">De inkoop is import (<strong>Belastingrichting</strong> is <strong>Inkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-205">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-206">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-206">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-207"><strong>Btw op creditnota inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-207"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="d55d2-208">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-208">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-209">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-209">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-210">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="d55d2-210">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="d55d2-211">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-211">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-212"><strong>Belastbare import</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-212"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="d55d2-213">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-213">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-214">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-214">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-215"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-215"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="d55d2-216">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-216">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-217"><strong>Belastbare import tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-217"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="d55d2-218">Omgekeerde som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-218">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-219">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-219">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-220"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="d55d2-220"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="d55d2-221">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-221">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-222"><strong>Creditnota belastbare import</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-222"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="d55d2-223">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-223">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-224">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-224">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="d55d2-225">e</span><span class="sxs-lookup"><span data-stu-id="d55d2-225">e</span></span><li><span data-ttu-id="d55d2-226"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="d55d2-226"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="d55d2-227">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-227">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-228"><strong>Creditnota belastbare import tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-228"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="d55d2-229">Omgekeerde som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-229">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-230">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-230">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-231">Belastingrichting is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="d55d2-231">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="d55d2-232">d</span><span class="sxs-lookup"><span data-stu-id="d55d2-232">d</span></span><li><span data-ttu-id="d55d2-233">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-233">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d55d2-234"><strong>Gebruiksbelasting</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-234"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="d55d2-235">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-235">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-236">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-236">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-237"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="d55d2-237"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="d55d2-238">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-238">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d55d2-239"><strong>Gebruiksbelasting tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="d55d2-239"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="d55d2-240">Omgekeerde som van <strong>Belastingbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d55d2-240">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d55d2-241">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="d55d2-241">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d55d2-242"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="d55d2-242"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="d55d2-243">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d55d2-243">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d55d2-244">Voor de bovenstaande tabel wordt ervan uitgegaan dat aan de volgende criteria wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="d55d2-244">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="d55d2-245">Het belastingbasisbedrag is een transactiebedrag van het veld **Oorsprong in valuta voor boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="d55d2-245">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="d55d2-246">Het belastingbedrag is een transitiebedrag van het veld **Werkelijke btw-bedrag in valuta voor boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="d55d2-246">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="d55d2-247">Het ER-model configureren en indelen voor het rapport</span><span class="sxs-lookup"><span data-stu-id="d55d2-247">Configure the ER model and format for the report</span></span>

<span data-ttu-id="d55d2-248">U kunt elektronische rapportage (ER) gebruiken om overzichten en aangifte te configureren en om gegevens te exporteren in verschillende elektronische indelingen zonder de X ++-code te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d55d2-248">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="d55d2-249">Voor aanvullende informatie:</span><span class="sxs-lookup"><span data-stu-id="d55d2-249">For additional information:</span></span>

-   [<span data-ttu-id="d55d2-250">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="d55d2-250">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="d55d2-251">Elektronische rapportageconfiguraties downloaden van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d55d2-251">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="d55d2-252">Lokalisatievereisten: een GER-configuratie maken</span><span class="sxs-lookup"><span data-stu-id="d55d2-252">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="d55d2-253">Landspecifieke resources voor btw-overzichten</span><span class="sxs-lookup"><span data-stu-id="d55d2-253">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="d55d2-254">Het btw-overzicht voor elk land moet voldoen aan de vereisten van de wetgeving van het land.</span><span class="sxs-lookup"><span data-stu-id="d55d2-254">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="d55d2-255">Er zijn vooraf gedefinieerde algemene modellen en indelingen van btw-overzichten voor de landen die in de volgende tabel staan.</span><span class="sxs-lookup"><span data-stu-id="d55d2-255">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="d55d2-256">Land/regio</span><span class="sxs-lookup"><span data-stu-id="d55d2-256">Country</span></span>        | <span data-ttu-id="d55d2-257">Aanvullende gegevens</span><span class="sxs-lookup"><span data-stu-id="d55d2-257">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d55d2-258">Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="d55d2-258">Austria</span></span>        |  [<span data-ttu-id="d55d2-259">Details btw-overzicht voor Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="d55d2-259">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="d55d2-260">België</span><span class="sxs-lookup"><span data-stu-id="d55d2-260">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="d55d2-261">Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="d55d2-261">Czech Republic</span></span> |  [<span data-ttu-id="d55d2-262">Details btw-overzicht voor de Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="d55d2-262">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="d55d2-263">Estland</span><span class="sxs-lookup"><span data-stu-id="d55d2-263">Estonia</span></span>        |  [<span data-ttu-id="d55d2-264">Details btw-overzicht voor Estland</span><span class="sxs-lookup"><span data-stu-id="d55d2-264">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="d55d2-265">Finland</span><span class="sxs-lookup"><span data-stu-id="d55d2-265">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="d55d2-266">Duitsland</span><span class="sxs-lookup"><span data-stu-id="d55d2-266">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="d55d2-267">Italië</span><span class="sxs-lookup"><span data-stu-id="d55d2-267">Italy</span></span>          | [<span data-ttu-id="d55d2-268">Details btw-overzicht voor Italië</span><span class="sxs-lookup"><span data-stu-id="d55d2-268">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="d55d2-269">Letland</span><span class="sxs-lookup"><span data-stu-id="d55d2-269">Latvia</span></span>         | [<span data-ttu-id="d55d2-270">Details btw-overzicht voor Letland</span><span class="sxs-lookup"><span data-stu-id="d55d2-270">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="d55d2-271">Litouwen</span><span class="sxs-lookup"><span data-stu-id="d55d2-271">Lithuania</span></span>      | [<span data-ttu-id="d55d2-272">Details btw-overzicht voor Litouwen</span><span class="sxs-lookup"><span data-stu-id="d55d2-272">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="d55d2-273">Nederland</span><span class="sxs-lookup"><span data-stu-id="d55d2-273">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="d55d2-274">Zweden</span><span class="sxs-lookup"><span data-stu-id="d55d2-274">Sweden</span></span>         |                                                                                 |






