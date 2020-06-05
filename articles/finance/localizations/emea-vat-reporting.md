---
title: Btw-aangifte voor Europa
description: Dit onderwerp bevat algemene informatie over het instellen en genereren van het btw-overzicht (belasting toegevoegde waarde) voor een aantal Europese landen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2a9b5bafb70883d9daf35a7d5a9107d7aee23469
ms.sourcegitcommit: 98ef9178b28cd548f08f8c32255636e6e09b25f2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/22/2020
ms.locfileid: "3395981"
---
# <a name="vat-reporting-for-europe"></a><span data-ttu-id="40f6e-103">Btw-aangifte voor Europa</span><span class="sxs-lookup"><span data-stu-id="40f6e-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40f6e-104">Dit onderwerp bevat algemene informatie over het instellen en genereren van het btw-overzicht (belasting toegevoegde waarde) voor een aantal Europese landen.</span><span class="sxs-lookup"><span data-stu-id="40f6e-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="40f6e-105">Dit onderwerp biedt een algemene aanpak voor het instellen en genereren van de btw-aangifte.</span><span class="sxs-lookup"><span data-stu-id="40f6e-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="40f6e-106">Deze benadering geldt voor alle gebruikers in rechtspersonen in de volgende landen:</span><span class="sxs-lookup"><span data-stu-id="40f6e-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="40f6e-107">Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="40f6e-107">Austria</span></span>
-   <span data-ttu-id="40f6e-108">België</span><span class="sxs-lookup"><span data-stu-id="40f6e-108">Belgium</span></span>
-   <span data-ttu-id="40f6e-109">Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="40f6e-109">Czech Republic</span></span>
-   <span data-ttu-id="40f6e-110">Estland</span><span class="sxs-lookup"><span data-stu-id="40f6e-110">Estonia</span></span>
-   <span data-ttu-id="40f6e-111">Finland</span><span class="sxs-lookup"><span data-stu-id="40f6e-111">Finland</span></span>
-   <span data-ttu-id="40f6e-112">Duitsland</span><span class="sxs-lookup"><span data-stu-id="40f6e-112">Germany</span></span>
-   <span data-ttu-id="40f6e-113">Letland</span><span class="sxs-lookup"><span data-stu-id="40f6e-113">Latvia</span></span>
-   <span data-ttu-id="40f6e-114">Litouwen</span><span class="sxs-lookup"><span data-stu-id="40f6e-114">Lithuania</span></span>
-   <span data-ttu-id="40f6e-115">Nederland</span><span class="sxs-lookup"><span data-stu-id="40f6e-115">Netherlands</span></span>
-   <span data-ttu-id="40f6e-116">Zweden</span><span class="sxs-lookup"><span data-stu-id="40f6e-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="40f6e-117">Overzicht btw-overzichten</span><span class="sxs-lookup"><span data-stu-id="40f6e-117">VAT statement overview</span></span>
<span data-ttu-id="40f6e-118">Het btw-overzicht is gebaseerd op bedragen van belastingtransacties.</span><span class="sxs-lookup"><span data-stu-id="40f6e-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="40f6e-119">Het proces voor het genereren van een btw-aangifte is onderdeel van het btw-betalingsproces dat is geïmplementeerd via de functie Btw vereffenen en boeken.</span><span class="sxs-lookup"><span data-stu-id="40f6e-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="40f6e-120">Met deze functie wordt de btw berekend die verschuldigd is voor een bepaalde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="40f6e-121">De berekening van de vereffening omvat de geboekte btw voor de geselecteerde vereffeningsperiode voor de belastingtransacties.</span><span class="sxs-lookup"><span data-stu-id="40f6e-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="40f6e-122">Het proces voor het berekenen van gegevens voor een btw-overzicht is gebaseerd op de relatie tussen btw-codes en btw-aangiftecodes, waarbij btw-aangiftecodes overeenkomen met de btw-overzichtvakken (of labels in XML).</span><span class="sxs-lookup"><span data-stu-id="40f6e-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="40f6e-123">Voor elke btw-code moeten er btw-aangiftecodes worden ingesteld voor elk type transactie, zoals belastbare verkoop, belastbare inkopen, belastbare import.</span><span class="sxs-lookup"><span data-stu-id="40f6e-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="40f6e-124">Dit transactietype wordt beschreven in het gedeelte Btw-codes voor btw-aangifte verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="40f6e-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="40f6e-125">Voor elke btw-aangiftecode moet een specifieke rapportindeling worden bepaald.</span><span class="sxs-lookup"><span data-stu-id="40f6e-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="40f6e-126">Btw-codes worden tegelijkertijd gekoppeld aan een specifieke btw-dienst via btw-vereffeningsperioden.</span><span class="sxs-lookup"><span data-stu-id="40f6e-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="40f6e-127">Voor elke btw-dienst moet een rapportindeling worden bepaald.</span><span class="sxs-lookup"><span data-stu-id="40f6e-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="40f6e-128">Dus alleen btw-aangiftecodes met dezelfde rapportindeling als die is ingesteld voor een btw-dienst in btw-vereffeningsperioden voor btw-code, kunnen worden geselecteerd in de rapportinstelling van de btw-code.</span><span class="sxs-lookup"><span data-stu-id="40f6e-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="40f6e-129">Een btw-transactie die is gegenereerd bij het boeken van een order of een journaal, bevat een btw-code, btw-bron, btw-richting en transactiebedragen (belastingbasisbedrag en belastingbedrag in valuta voor boekhouding, btw-valuta en transactievaluta).</span><span class="sxs-lookup"><span data-stu-id="40f6e-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="40f6e-130">Op basis van de combinatie van belastingtransactiekenmerken bestaan transactiebedragen uit totaalbedragen voor btw-aangiftecodes die zijn opgegeven voor btw-codes.</span><span class="sxs-lookup"><span data-stu-id="40f6e-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="40f6e-131">In de volgende afbeelding wordt de gegevensrelatie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="40f6e-131">The following illustration shows the data relationship.</span></span>

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="40f6e-133">Instelling btw-overzicht</span><span class="sxs-lookup"><span data-stu-id="40f6e-133">VAT statement setup</span></span>
<span data-ttu-id="40f6e-134">Als u een btw-overzicht wilt genereren, moet u het volgende instellen.</span><span class="sxs-lookup"><span data-stu-id="40f6e-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="40f6e-135">Btw-diensten voor btw-rapportage</span><span class="sxs-lookup"><span data-stu-id="40f6e-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="40f6e-136">Voordat u btw-aangiftecodes kunt instellen, moet u de juiste rapportindeling voor de btw-dienst selecteren.</span><span class="sxs-lookup"><span data-stu-id="40f6e-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="40f6e-137">Selecteer op de pagina **Btw-diensten** in de sectie **Algemeen** een **Rapportindeling**.</span><span class="sxs-lookup"><span data-stu-id="40f6e-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="40f6e-138">Deze indeling wordt gebruikt bij het instellen van btw-aangiftecodes.</span><span class="sxs-lookup"><span data-stu-id="40f6e-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="40f6e-139">Btw-aangiftecodes</span><span class="sxs-lookup"><span data-stu-id="40f6e-139">Sales tax reporting codes</span></span>

<span data-ttu-id="40f6e-140">Btw-aangiftecodes zijn vakcodes in het btw-overzicht of labelnamen in XML-indeling.</span><span class="sxs-lookup"><span data-stu-id="40f6e-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="40f6e-141">Deze codes worden gebruikt voor het samenvoegen en voorbereiden van bedragen voor het rapport.</span><span class="sxs-lookup"><span data-stu-id="40f6e-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="40f6e-142">De namen van de resultaatbedragen worden gebruikt bij het configureren van de ER-indeling (elektronische rapportage) van het btw-overzicht.</span><span class="sxs-lookup"><span data-stu-id="40f6e-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="40f6e-143">U kunt btw-aangiftecodes maken en onderhouden op de pagina **Btw-aangiftecodes**.</span><span class="sxs-lookup"><span data-stu-id="40f6e-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="40f6e-144">U moet aan elke code een rapportindeling toewijzen.</span><span class="sxs-lookup"><span data-stu-id="40f6e-144">You must assign each code a report layout.</span></span> <span data-ttu-id="40f6e-145">Nadat u de btw-aangiftecodes hebt gemaakt, kunt u de codes kiezen in de sectie **Rapport instellen** op de pagina **Btw-codes**.</span><span class="sxs-lookup"><span data-stu-id="40f6e-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="40f6e-146">Btw-codes voor btw-aangifte</span><span class="sxs-lookup"><span data-stu-id="40f6e-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> <span data-ttu-id="40f6e-147"> Basisbedragen en belastingbedragen van btw-transacties kunnen worden samengevoegd in aangiftecodes in het btw-overzicht (XML-labels of aangiftevakken).</span><span class="sxs-lookup"><span data-stu-id="40f6e-147">Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes).</span></span> <span data-ttu-id="40f6e-148">U kunt dit instellen door btw-aangiftecodes voor verschillende transactietypen te koppelen voor btw-codes op de pagina <strong>Btw-codes</strong>.</span><span class="sxs-lookup"><span data-stu-id="40f6e-148">You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="40f6e-149">In de volgende tabel worden de transactietypen beschreven in de rapportinstelling voor btw-codes.</span><span class="sxs-lookup"><span data-stu-id="40f6e-149">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="40f6e-150">De berekening omvat de transacties voor alle typen bronnen met uitzondering van btw.</span><span class="sxs-lookup"><span data-stu-id="40f6e-150">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40f6e-151"><strong>Transactietype</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-151"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="40f6e-152"><strong>Omschrijving van transacties en bedragen die moeten worden geteld voor het transactietype</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-152"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-153"><strong>Belastbare verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-153"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="40f6e-154">Som van <strong>Belastingbasisbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-154">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-155">Transactiedatum bevindt zich in de geselecteerde periode/</span><span class="sxs-lookup"><span data-stu-id="40f6e-155">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="40f6e-156">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-156">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-157">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-157">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-158"><strong>Verkoop zonder btw</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-158"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="40f6e-159">Som van <strong>Belastingbasisbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-159">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-160">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-160">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-161">De verkoop is export (<strong>Belastingrichting</strong> is <strong>Verkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-161">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-162">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-162">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-163"><strong>Te betalen btw</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-163"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="40f6e-164">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-164">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-165">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-165">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-166">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-166">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-167">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-167">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-168"><strong>Creditnota belastbare verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-168"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="40f6e-169">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-169">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-170">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-170">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-171">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-171">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-172">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-172">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-173"><strong>Creditnota vrijgestelde verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-173"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="40f6e-174">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-174">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-175">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-175">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-176">De verkoop is export (<strong>Belastingrichting</strong> is <strong>Verkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-176">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-177">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-177">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-178"><strong>Btw op creditnota verkoop</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-178"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="40f6e-179">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-179">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-180">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-180">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-181">De verkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te betalen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-181">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-182">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-182">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-183"><strong>Belastbare inkopen</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-183"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="40f6e-184">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-184">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-185">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-185">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-186">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-186">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-187">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-187">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-188"><strong>Inkoop zonder btw</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-188"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="40f6e-189">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-189">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-190">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-190">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-191">De inkoop is import (<strong>Belastingrichting</strong> is <strong>Inkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-191">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-192">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-192">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-193"><strong>Te ontvangen btw</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-193"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="40f6e-194">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-194">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-195">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-195">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-196">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-196">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-197">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-197">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-198"><strong>Creditnota belastbare inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-198"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="40f6e-199">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-199">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-200">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-200">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-201">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-201">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-202">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-202">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-203"><strong>Creditnota vrijgestelde inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-203"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="40f6e-204">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-204">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-205">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-205">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-206">De inkoop is import (<strong>Belastingrichting</strong> is <strong>Inkoop zonder btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-206">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-207">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-207">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-208"><strong>Btw op creditnota inkoop</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-208"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="40f6e-209">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-209">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-210">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-210">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-211">De inkoop is binnenlands (<strong>Belastingrichting</strong> is <strong>Te ontvangen btw</strong>).</span><span class="sxs-lookup"><span data-stu-id="40f6e-211">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="40f6e-212">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-212">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-213"><strong>Belastbare import</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-213"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="40f6e-214">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-214">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-215">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-215">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-216"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-216"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="40f6e-217">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-217">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-218"><strong>Belastbare import tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-218"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="40f6e-219">Omgekeerde som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-219">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-220">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-220">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-221"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="40f6e-221"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="40f6e-222">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-222">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-223"><strong>Creditnota belastbare import</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-223"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="40f6e-224">Som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-224">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-225">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-225">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="40f6e-226">e</span><span class="sxs-lookup"><span data-stu-id="40f6e-226">e</span></span><li><span data-ttu-id="40f6e-227"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="40f6e-227"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="40f6e-228">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-228">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-229"><strong>Creditnota belastbare import tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-229"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="40f6e-230">Omgekeerde som van <strong>Belastingbasisbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-230">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-231">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-231">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-232">Belastingrichting is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="40f6e-232">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="40f6e-233">d</span><span class="sxs-lookup"><span data-stu-id="40f6e-233">d</span></span><li><span data-ttu-id="40f6e-234">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-234">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40f6e-235"><strong>Gebruiksbelasting</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-235"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="40f6e-236">Som van <strong>Belastingbedragen</strong> van belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-236">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-237">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-237">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-238"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="40f6e-238"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="40f6e-239">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-239">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40f6e-240"><strong>Gebruiksbelasting tegenrekenen</strong></span><span class="sxs-lookup"><span data-stu-id="40f6e-240"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="40f6e-241">Omgekeerde som van <strong>Belastingbedragen</strong> van de belastingtransacties die voldoen aan de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="40f6e-241">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="40f6e-242">Transactiedatum bevindt zich in de geselecteerde periode.</span><span class="sxs-lookup"><span data-stu-id="40f6e-242">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="40f6e-243"><strong>Belastingrichting</strong> is <strong>Gebruiksbelasting</strong>.</span><span class="sxs-lookup"><span data-stu-id="40f6e-243"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="40f6e-244">De transactie <strong>Belastingbasisbedrag</strong> of <strong>Belastingbedrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="40f6e-244">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="40f6e-245">Voor de bovenstaande tabel wordt ervan uitgegaan dat aan de volgende criteria wordt voldaan:</span><span class="sxs-lookup"><span data-stu-id="40f6e-245">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="40f6e-246">Het belastingbasisbedrag is een transactiebedrag van het veld **Oorsprong in valuta voor boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="40f6e-246">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="40f6e-247">Het belastingbedrag is een transitiebedrag van het veld **Werkelijke btw-bedrag in valuta voor boekhouding**.</span><span class="sxs-lookup"><span data-stu-id="40f6e-247">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="40f6e-248">Het ER-model configureren en indelen voor het rapport</span><span class="sxs-lookup"><span data-stu-id="40f6e-248">Configure the ER model and format for the report</span></span>

<span data-ttu-id="40f6e-249">U kunt elektronische rapportage (ER) gebruiken om overzichten en aangifte te configureren en om gegevens te exporteren in verschillende elektronische indelingen zonder de X ++-code te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="40f6e-249">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="40f6e-250">Voor aanvullende informatie:</span><span class="sxs-lookup"><span data-stu-id="40f6e-250">For additional information:</span></span>

-   [<span data-ttu-id="40f6e-251">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="40f6e-251">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="40f6e-252">Elektronische rapportageconfiguraties downloaden van Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="40f6e-252">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="40f6e-253">Lokalisatievereisten: een GER-configuratie maken</span><span class="sxs-lookup"><span data-stu-id="40f6e-253">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="40f6e-254">Landspecifieke resources voor btw-overzichten</span><span class="sxs-lookup"><span data-stu-id="40f6e-254">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="40f6e-255">Het btw-overzicht voor elk land moet voldoen aan de vereisten van de wetgeving van het land.</span><span class="sxs-lookup"><span data-stu-id="40f6e-255">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="40f6e-256">Er zijn vooraf gedefinieerde algemene modellen en indelingen van btw-overzichten voor de landen die in de volgende tabel staan.</span><span class="sxs-lookup"><span data-stu-id="40f6e-256">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="40f6e-257">Land/regio</span><span class="sxs-lookup"><span data-stu-id="40f6e-257">Country</span></span>        | <span data-ttu-id="40f6e-258">Aanvullende gegevens</span><span class="sxs-lookup"><span data-stu-id="40f6e-258">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="40f6e-259">Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="40f6e-259">Austria</span></span>        |  [<span data-ttu-id="40f6e-260">Details btw-overzicht voor Oostenrijk</span><span class="sxs-lookup"><span data-stu-id="40f6e-260">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="40f6e-261">België</span><span class="sxs-lookup"><span data-stu-id="40f6e-261">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="40f6e-262">Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="40f6e-262">Czech Republic</span></span> |  [<span data-ttu-id="40f6e-263">Btw-overzicht voor Tsjechië</span><span class="sxs-lookup"><span data-stu-id="40f6e-263">VAT statement for the Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="40f6e-264">Estland</span><span class="sxs-lookup"><span data-stu-id="40f6e-264">Estonia</span></span>        |  [<span data-ttu-id="40f6e-265">Details btw-overzicht voor Estland</span><span class="sxs-lookup"><span data-stu-id="40f6e-265">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="40f6e-266">Finland</span><span class="sxs-lookup"><span data-stu-id="40f6e-266">Finland</span></span>        | [<span data-ttu-id="40f6e-267">Btw-rapport voor Finland</span><span class="sxs-lookup"><span data-stu-id="40f6e-267">Sales tax report for Finland</span></span>](emea-fin-sales-tax-payment-report-finland.md)          |
| <span data-ttu-id="40f6e-268">Duitsland</span><span class="sxs-lookup"><span data-stu-id="40f6e-268">Germany</span></span>        | [<span data-ttu-id="40f6e-269">Btw-aangifte voor Duitsland</span><span class="sxs-lookup"><span data-stu-id="40f6e-269">VAT declaration for Germany</span></span>](emea-de-vat-declaration.md)                       |
| <span data-ttu-id="40f6e-270">Italië</span><span class="sxs-lookup"><span data-stu-id="40f6e-270">Italy</span></span>          | [<span data-ttu-id="40f6e-271">Details btw-overzichten voor Italië</span><span class="sxs-lookup"><span data-stu-id="40f6e-271">VAT statements details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="40f6e-272">Letland</span><span class="sxs-lookup"><span data-stu-id="40f6e-272">Latvia</span></span>         | [<span data-ttu-id="40f6e-273">Details btw-overzicht voor Letland</span><span class="sxs-lookup"><span data-stu-id="40f6e-273">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="40f6e-274">Litouwen</span><span class="sxs-lookup"><span data-stu-id="40f6e-274">Lithuania</span></span>      | [<span data-ttu-id="40f6e-275">Details btw-overzicht voor Litouwen</span><span class="sxs-lookup"><span data-stu-id="40f6e-275">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="40f6e-276">Nederland</span><span class="sxs-lookup"><span data-stu-id="40f6e-276">Netherlands</span></span>    | [<span data-ttu-id="40f6e-277">Btw-aangifte voor Nederland</span><span class="sxs-lookup"><span data-stu-id="40f6e-277">VAT declaration for the Netherlands</span></span>](emea-nl-vat-declaration.md)           |
| <span data-ttu-id="40f6e-278">Zweden</span><span class="sxs-lookup"><span data-stu-id="40f6e-278">Sweden</span></span>         | [<span data-ttu-id="40f6e-279">Btw-rapport voor Zweden</span><span class="sxs-lookup"><span data-stu-id="40f6e-279">Sales tax report for Sweden</span></span>](emea-swe-sales-tax-payment-report-sweden.md)          |





