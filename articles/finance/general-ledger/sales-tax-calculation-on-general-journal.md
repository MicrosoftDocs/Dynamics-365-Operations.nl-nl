---
title: Btw-berekening voor algemene journaalregels
description: In dit onderwerp wordt uitgelegd hoe btw wordt berekend voor verschillende typen rekeningen (leverancier, klant, grootboek en project) op algemene journaalregels.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
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
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dd1df355d39065d6959915cc916987d3c58b15a6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570189"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="12162-103">Btw-berekening voor algemene journaalregels</span><span class="sxs-lookup"><span data-stu-id="12162-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="12162-104">In dit onderwerp wordt uitgelegd hoe btw wordt berekend voor verschillende typen rekeningen (leverancier, klant, grootboek en project) op algemene journaalregels.</span><span class="sxs-lookup"><span data-stu-id="12162-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="12162-105">Het proces kan in drie stappen worden onderverdeeld:</span><span class="sxs-lookup"><span data-stu-id="12162-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="12162-106">De btw-richting bepalen.</span><span class="sxs-lookup"><span data-stu-id="12162-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="12162-107">Het btw-bedrag bepalen dat wordt opgeslagen in de tijdelijke btw-tabel.</span><span class="sxs-lookup"><span data-stu-id="12162-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="12162-108">Het btw-bedrag en de rekening op het boekstuk bepalen.</span><span class="sxs-lookup"><span data-stu-id="12162-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="12162-109">De btw-richting bepalen</span><span class="sxs-lookup"><span data-stu-id="12162-109">Determine the sales tax direction</span></span>

<span data-ttu-id="12162-110">De manier waarop de richting van de btw wordt bepaald, is afhankelijk van het type rekening in het boekstuk.</span><span class="sxs-lookup"><span data-stu-id="12162-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="12162-111">De btw-richting wordt bepaald door de combinatie van rekeningtype en btw-code.</span><span class="sxs-lookup"><span data-stu-id="12162-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="12162-112">In de volgende gedeelten vindt u meer informatie over de mogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="12162-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="12162-113">Het rekeningtype is Project.</span><span class="sxs-lookup"><span data-stu-id="12162-113">Account type is Project</span></span>

<span data-ttu-id="12162-114">Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Project**is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting.</span><span class="sxs-lookup"><span data-stu-id="12162-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="12162-115">In de volgende afbeelding ziet u de regel.</span><span class="sxs-lookup"><span data-stu-id="12162-115">The following illustration shows the rule.</span></span> <span data-ttu-id="12162-116">De volgende punten tonen de mogelijke belastingrichtingen voor projectrekeningen.</span><span class="sxs-lookup"><span data-stu-id="12162-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="12162-117">• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.</span><span class="sxs-lookup"><span data-stu-id="12162-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="12162-118">• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.</span><span class="sxs-lookup"><span data-stu-id="12162-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="12162-119">• Als de btw-code intracommunautaire btw is, is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="12162-120">• Als de btw-code verlegd is, is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="12162-121">Anders is de btw-richting Te Ontvangen Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="12162-122">In het volgende diagram wordt de regel grafisch weergeven.</span><span class="sxs-lookup"><span data-stu-id="12162-122">The following diagram illustrates the rule graphically.</span></span>

![Mogelijke belastingrichtingen voor projectrekeningen](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="12162-124">Het rekeningtype is Leverancier</span><span class="sxs-lookup"><span data-stu-id="12162-124">Account type is Vendor</span></span>

<span data-ttu-id="12162-125">Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Leverancier**is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting.</span><span class="sxs-lookup"><span data-stu-id="12162-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="12162-126">De volgende punten tonen de mogelijke belastingrichtingen voor leveranciersrekeningen.</span><span class="sxs-lookup"><span data-stu-id="12162-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="12162-127">• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.</span><span class="sxs-lookup"><span data-stu-id="12162-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="12162-128">• Als de btw-code intracommunautaire btw is, is de btw-richting Te Ontvangen Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="12162-129">• Als de btw-code verlegd is, is de btw-richting Te Ontvangen Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="12162-130">Anders is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="12162-131">In het volgende diagram wordt de regel grafisch weergeven.</span><span class="sxs-lookup"><span data-stu-id="12162-131">The following diagram illustrates the rule graphically.</span></span>

![Mogelijke belastingrichtingen voor leveranciersrekeningen](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="12162-133">Het rekeningtype is Klant</span><span class="sxs-lookup"><span data-stu-id="12162-133">Account type is Customer</span></span>

<span data-ttu-id="12162-134">Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Klant**is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting.</span><span class="sxs-lookup"><span data-stu-id="12162-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="12162-135">De volgende punten tonen de mogelijke belastingrichtingen voor klantentrekeningen.</span><span class="sxs-lookup"><span data-stu-id="12162-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="12162-136">• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.</span><span class="sxs-lookup"><span data-stu-id="12162-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="12162-137">• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.</span><span class="sxs-lookup"><span data-stu-id="12162-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="12162-138">• Als de btw-code intracommunautaire btw is, is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="12162-139">• Als de btw-code verlegd is, is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="12162-140">Anders is de btw-richting Te Ontvangen Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="12162-141">In het volgende diagram wordt de regel grafisch weergeven.</span><span class="sxs-lookup"><span data-stu-id="12162-141">The following diagram illustrates the rule graphically.</span></span>

![Mogelijke belastingrichtingen voor klantenrekeningen](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="12162-143">Het rekeningtype is Grootboek</span><span class="sxs-lookup"><span data-stu-id="12162-143">Account type is Ledger</span></span>

<span data-ttu-id="12162-144">In de volgende afbeelding ziet u de regel die van toepassing is, wanneer een boekstuk alleen journaalregels heeft waarvoor het rekeningtype **Grootboek** is.</span><span class="sxs-lookup"><span data-stu-id="12162-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="12162-145">De volgende punten tonen de mogelijke belastingrichtingen voor grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="12162-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="12162-146">• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.</span><span class="sxs-lookup"><span data-stu-id="12162-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="12162-147">• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.</span><span class="sxs-lookup"><span data-stu-id="12162-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="12162-148">Als het bedrag van het journaal debet (positief) is, is de btw-richting Te Ontvangen Btw. Als het bedrag van het journaal credit is (negatief), is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="12162-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="12162-149">In het volgende diagram wordt de regel grafisch weergeven.</span><span class="sxs-lookup"><span data-stu-id="12162-149">The following diagram illustrates the rule graphically.</span></span>

![Mogelijke belastingrichtingen voor grootboekrekeningen](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="12162-151">De btw-richting negeren</span><span class="sxs-lookup"><span data-stu-id="12162-151">Override the sales tax direction</span></span>

<span data-ttu-id="12162-152">U kunt de btw-richting negeren wanneer het boekstuk alleen regels bevat waarvoor het rekeningtype **Grootboek is**.</span><span class="sxs-lookup"><span data-stu-id="12162-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="12162-153">Ga naar **Grootboek \> Rekeningschema \> Rekeningen \> Hoofdrekeningen** en selecteer het sneltabblad **Rechtspersoon overschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="12162-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="12162-154">Het btw-bedrag bepalen</span><span class="sxs-lookup"><span data-stu-id="12162-154">Determine the sales tax amount</span></span>

<span data-ttu-id="12162-155">In deze sectie wordt beschreven hoe het teken voor het btw-bedrag wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="12162-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Pagina Btw-transacties](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="12162-157">In de volgende tabel wordt de algemene regel weergegeven voor het bepalen van het teken van btw-bedragen in de tijdelijke btw-tabel.</span><span class="sxs-lookup"><span data-stu-id="12162-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="12162-158">Bedrag journaalregel:</span><span class="sxs-lookup"><span data-stu-id="12162-158">Journal line amount</span></span> | <span data-ttu-id="12162-159">Btw-richting</span><span class="sxs-lookup"><span data-stu-id="12162-159">Sales tax direction</span></span>  | <span data-ttu-id="12162-160">Teken btw-bedrag</span><span class="sxs-lookup"><span data-stu-id="12162-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="12162-161">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-161">Positive</span></span>            | <span data-ttu-id="12162-162">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-162">Sales Tax Receivable</span></span> | <span data-ttu-id="12162-163">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-163">Positive</span></span>              |
| <span data-ttu-id="12162-164">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-164">Positive</span></span>            | <span data-ttu-id="12162-165">Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="12162-165">Sales Tax Payable</span></span>    | <span data-ttu-id="12162-166">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-166">Negative</span></span>              |
| <span data-ttu-id="12162-167">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-167">Negative</span></span>            | <span data-ttu-id="12162-168">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-168">Sales Tax Receivable</span></span> | <span data-ttu-id="12162-169">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-169">Negative</span></span>              |
| <span data-ttu-id="12162-170">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-170">Negative</span></span>            | <span data-ttu-id="12162-171">Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="12162-171">Sales Tax Payable</span></span>    | <span data-ttu-id="12162-172">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-172">Positive</span></span>              |

<span data-ttu-id="12162-173">Er is een speciale regel voor boekstukken die alleen **Project-** of **Grootboek**regels hebben, wanneer een btw-groep of artikel-btw-groep wordt geselecteerd op de **Grootboek**regel.</span><span class="sxs-lookup"><span data-stu-id="12162-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="12162-174">Deze regel wordt bepaald door onafhankelijke btw-berekeningsfunctie in te schakelen voor algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="12162-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="12162-175">Wanneer deze functie is uitgeschakeld, gebruikt het btw-bedrag van de **Grootboek**regel de debet/credit-richting van de **Project**regel.</span><span class="sxs-lookup"><span data-stu-id="12162-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="12162-176">Wanneer de functie is ingeschakeld, gebruikt het btw-bedrag van de **Grootboek**regel zijn eigen debet/credit-richting.</span><span class="sxs-lookup"><span data-stu-id="12162-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="12162-177">In de volgende tabellen wordt de regel voor elk scenario weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="12162-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="12162-178">**Regel wanneer de functie is ingeschakeld.**</span><span class="sxs-lookup"><span data-stu-id="12162-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="12162-179">Journaalregel bedrag van project</span><span class="sxs-lookup"><span data-stu-id="12162-179">Journal line amount of project</span></span> | <span data-ttu-id="12162-180">Btw-richting</span><span class="sxs-lookup"><span data-stu-id="12162-180">Sales tax direction</span></span>  | <span data-ttu-id="12162-181">Teken btw-bedrag</span><span class="sxs-lookup"><span data-stu-id="12162-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="12162-182">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-182">Positive</span></span>                       | <span data-ttu-id="12162-183">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-183">Sales Tax Receivable</span></span> | <span data-ttu-id="12162-184">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-184">Positive</span></span>              |
| <span data-ttu-id="12162-185">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-185">Negative</span></span>                       | <span data-ttu-id="12162-186">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-186">Sales Tax Receivable</span></span> | <span data-ttu-id="12162-187">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-187">Negative</span></span>              |

<span data-ttu-id="12162-188">**Regel wanneer de functie is uitgeschakeld**</span><span class="sxs-lookup"><span data-stu-id="12162-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="12162-189">Journaalregel bedrag van grootboek</span><span class="sxs-lookup"><span data-stu-id="12162-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="12162-190">Btw-richting</span><span class="sxs-lookup"><span data-stu-id="12162-190">Sales tax direction</span></span>  | <span data-ttu-id="12162-191">Teken btw-bedrag</span><span class="sxs-lookup"><span data-stu-id="12162-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="12162-192">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-192">Positive</span></span>                       | <span data-ttu-id="12162-193">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-193">Sales Tax Receivable</span></span> | <span data-ttu-id="12162-194">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-194">Positive</span></span>              |
| <span data-ttu-id="12162-195">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-195">Negative</span></span>                       | <span data-ttu-id="12162-196">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-196">Sales Tax Receivable</span></span> | <span data-ttu-id="12162-197">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="12162-198">Het btw-bedrag en de rekening op het boekstuk bepalen</span><span class="sxs-lookup"><span data-stu-id="12162-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="12162-199">Wanneer u btw boekt, wordt de hoofdrekening opgehaald uit het groepsprofiel voor de grootboek-boekingen.</span><span class="sxs-lookup"><span data-stu-id="12162-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="12162-200">Wanneer de btw terug te ontvangen is, gebruikt het systeem de rekening voor Te Ontvangen Btw die in het profiel is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="12162-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="12162-201">Wanneer de btw verschuldigd is, gebruikt het systeem de rekening voor Verschuldigde Btw die in het profiel is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="12162-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="12162-202">De volgende tabel laat de generieke regel zien.</span><span class="sxs-lookup"><span data-stu-id="12162-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="12162-203">Btw-richting</span><span class="sxs-lookup"><span data-stu-id="12162-203">Sales tax direction</span></span>  | <span data-ttu-id="12162-204">Teken btw-bedrag</span><span class="sxs-lookup"><span data-stu-id="12162-204">Sales tax amount sign</span></span> | <span data-ttu-id="12162-205">Btw-rekening</span><span class="sxs-lookup"><span data-stu-id="12162-205">Sales tax account</span></span>      | <span data-ttu-id="12162-206">Bedrag op boekstuk</span><span class="sxs-lookup"><span data-stu-id="12162-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="12162-207">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-207">Sales Tax Receivable</span></span> | <span data-ttu-id="12162-208">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-208">Positive</span></span>              | <span data-ttu-id="12162-209">Rekening voor Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-209">Tax Receivable Account</span></span> | <span data-ttu-id="12162-210">Positief (Debet)</span><span class="sxs-lookup"><span data-stu-id="12162-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="12162-211">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-211">Sales Tax Receivable</span></span> | <span data-ttu-id="12162-212">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-212">Negative</span></span>              | <span data-ttu-id="12162-213">Rekening voor Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="12162-213">Tax Receivable Account</span></span> | <span data-ttu-id="12162-214">Negatief (Credit)</span><span class="sxs-lookup"><span data-stu-id="12162-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="12162-215">Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="12162-215">Sales Tax Payable</span></span>    | <span data-ttu-id="12162-216">Positief</span><span class="sxs-lookup"><span data-stu-id="12162-216">Positive</span></span>              | <span data-ttu-id="12162-217">Rekening voor Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="12162-217">Tax Payable Account</span></span>    | <span data-ttu-id="12162-218">Negatief (Credit)</span><span class="sxs-lookup"><span data-stu-id="12162-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="12162-219">Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="12162-219">Sales Tax Payable</span></span>    | <span data-ttu-id="12162-220">Negatief</span><span class="sxs-lookup"><span data-stu-id="12162-220">Negative</span></span>              | <span data-ttu-id="12162-221">Rekening voor Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="12162-221">Tax Payable Account</span></span>    | <span data-ttu-id="12162-222">Positief (Debet)</span><span class="sxs-lookup"><span data-stu-id="12162-222">Positive (Debit)</span></span>  |
