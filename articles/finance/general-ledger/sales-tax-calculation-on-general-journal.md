---
title: Btw-berekening voor algemene journaalregels
description: In dit onderwerp wordt uitgelegd hoe btw wordt berekend voor verschillende typen rekeningen (leverancier, klant, grootboek en project) op algemene journaalregels.
author: EricWang
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e4d367fe6cb729c9c5658a9bbbac04e53fdf9644
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815327"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="e7b4b-103">Btw-berekening voor algemene journaalregels</span><span class="sxs-lookup"><span data-stu-id="e7b4b-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7b4b-104">In dit onderwerp wordt uitgelegd hoe btw wordt berekend voor verschillende typen rekeningen (leverancier, klant, grootboek en project) op algemene journaalregels.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="e7b4b-105">Het proces kan in drie stappen worden onderverdeeld:</span><span class="sxs-lookup"><span data-stu-id="e7b4b-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="e7b4b-106">De btw-richting bepalen.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="e7b4b-107">Het btw-bedrag bepalen dat wordt opgeslagen in de tijdelijke btw-tabel.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="e7b4b-108">Het btw-bedrag en de rekening op het boekstuk bepalen.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="e7b4b-109">De btw-richting bepalen</span><span class="sxs-lookup"><span data-stu-id="e7b4b-109">Determine the sales tax direction</span></span>

<span data-ttu-id="e7b4b-110">De manier waarop de richting van de btw wordt bepaald, is afhankelijk van het type rekening in het boekstuk.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="e7b4b-111">De btw-richting wordt bepaald door de combinatie van rekeningtype en btw-code.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="e7b4b-112">In de volgende gedeelten vindt u meer informatie over de mogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="e7b4b-113">Het rekeningtype is Project.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-113">Account type is Project</span></span>

<span data-ttu-id="e7b4b-114">Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Project** is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="e7b4b-115">In de volgende afbeelding ziet u de regel.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-115">The following illustration shows the rule.</span></span> <span data-ttu-id="e7b4b-116">De volgende punten tonen de mogelijke belastingrichtingen voor projectrekeningen.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="e7b4b-117">• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="e7b4b-118">• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="e7b4b-119">• Als de btw-code intracommunautaire btw is, is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="e7b4b-120">• Als de btw-code verlegd is, is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="e7b4b-121">Anders is de btw-richting Te Ontvangen Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="e7b4b-122">In het volgende diagram wordt de regel grafisch weergeven.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-122">The following diagram illustrates the rule graphically.</span></span>

![Mogelijke belastingrichtingen voor projectrekeningen](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="e7b4b-124">Het rekeningtype is Leverancier</span><span class="sxs-lookup"><span data-stu-id="e7b4b-124">Account type is Vendor</span></span>

<span data-ttu-id="e7b4b-125">Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Leverancier** is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="e7b4b-126">De volgende punten tonen de mogelijke belastingrichtingen voor leveranciersrekeningen.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="e7b4b-127">• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="e7b4b-128">• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="e7b4b-129">• Als de btw-code intracommunautaire btw is, is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="e7b4b-130">• Als de btw-code verlegd is, is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="e7b4b-131">Anders is de btw-richting Te Ontvangen Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="e7b4b-132">In het volgende diagram wordt de regel grafisch weergeven.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-132">The following diagram illustrates the rule graphically.</span></span>

![Mogelijke belastingrichtingen voor leveranciersrekeningen](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="e7b4b-134">Het rekeningtype is Klant</span><span class="sxs-lookup"><span data-stu-id="e7b4b-134">Account type is Customer</span></span>

<span data-ttu-id="e7b4b-135">Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Klant** is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="e7b4b-136">De volgende punten tonen de mogelijke belastingrichtingen voor klantentrekeningen.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="e7b4b-137">• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="e7b4b-138">• Als de btw-code intracommunautaire btw is, is de btw-richting Te Ontvangen Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="e7b4b-139">• Als de btw-code verlegd is, is de btw-richting Te Ontvangen Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="e7b4b-140">Anders is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="e7b4b-141">In het volgende diagram wordt de regel grafisch weergeven.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-141">The following diagram illustrates the rule graphically.</span></span>

![Mogelijke belastingrichtingen voor klantenrekeningen](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="e7b4b-143">Het rekeningtype is Grootboek</span><span class="sxs-lookup"><span data-stu-id="e7b4b-143">Account type is Ledger</span></span>

<span data-ttu-id="e7b4b-144">In de volgende afbeelding ziet u de regel die van toepassing is, wanneer een boekstuk alleen journaalregels heeft waarvoor het rekeningtype **Grootboek** is.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="e7b4b-145">De volgende punten tonen de mogelijke belastingrichtingen voor grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="e7b4b-146">• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="e7b4b-147">• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="e7b4b-148">Als het bedrag van het journaal debet (positief) is, is de btw-richting Te Ontvangen Btw. Als het bedrag van het journaal credit is (negatief), is de btw-richting Verschuldigde Btw.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="e7b4b-149">In het volgende diagram wordt de regel grafisch weergeven.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-149">The following diagram illustrates the rule graphically.</span></span>

![Mogelijke belastingrichtingen voor grootboekrekeningen](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="e7b4b-151">De btw-richting negeren</span><span class="sxs-lookup"><span data-stu-id="e7b4b-151">Override the sales tax direction</span></span>

<span data-ttu-id="e7b4b-152">U kunt de btw-richting negeren wanneer het boekstuk alleen regels bevat waarvoor het rekeningtype **Grootboek is**.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="e7b4b-153">Ga naar **Grootboek \> Rekeningschema \> Rekeningen \> Hoofdrekeningen** en selecteer het sneltabblad **Rechtspersoon overschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="e7b4b-154">Het btw-bedrag bepalen</span><span class="sxs-lookup"><span data-stu-id="e7b4b-154">Determine the sales tax amount</span></span>

<span data-ttu-id="e7b4b-155">In deze sectie wordt beschreven hoe het teken voor het btw-bedrag wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Pagina Btw-transacties](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="e7b4b-157">In de volgende tabel wordt de algemene regel weergegeven voor het bepalen van het teken van btw-bedragen in de tijdelijke btw-tabel.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="e7b4b-158">Bedrag journaalregel:</span><span class="sxs-lookup"><span data-stu-id="e7b4b-158">Journal line amount</span></span> | <span data-ttu-id="e7b4b-159">Btw-richting</span><span class="sxs-lookup"><span data-stu-id="e7b4b-159">Sales tax direction</span></span>  | <span data-ttu-id="e7b4b-160">Teken btw-bedrag</span><span class="sxs-lookup"><span data-stu-id="e7b4b-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="e7b4b-161">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-161">Positive</span></span>            | <span data-ttu-id="e7b4b-162">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-162">Sales Tax Receivable</span></span> | <span data-ttu-id="e7b4b-163">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-163">Positive</span></span>              |
| <span data-ttu-id="e7b4b-164">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-164">Positive</span></span>            | <span data-ttu-id="e7b4b-165">Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-165">Sales Tax Payable</span></span>    | <span data-ttu-id="e7b4b-166">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-166">Negative</span></span>              |
| <span data-ttu-id="e7b4b-167">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-167">Negative</span></span>            | <span data-ttu-id="e7b4b-168">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-168">Sales Tax Receivable</span></span> | <span data-ttu-id="e7b4b-169">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-169">Negative</span></span>              |
| <span data-ttu-id="e7b4b-170">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-170">Negative</span></span>            | <span data-ttu-id="e7b4b-171">Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-171">Sales Tax Payable</span></span>    | <span data-ttu-id="e7b4b-172">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-172">Positive</span></span>              |

<span data-ttu-id="e7b4b-173">Er is een speciale regel voor boekstukken die alleen **Project-** of **Grootboek** regels hebben, wanneer een btw-groep of artikel-btw-groep wordt geselecteerd op de **Grootboek** regel.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="e7b4b-174">Deze regel wordt bepaald door onafhankelijke btw-berekeningsfunctie in te schakelen voor algemene journalen.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="e7b4b-175">Wanneer deze functie is uitgeschakeld, gebruikt het btw-bedrag van de **Grootboek** regel de debet/credit-richting van de **Project** regel.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="e7b4b-176">Wanneer de functie is ingeschakeld, gebruikt het btw-bedrag van de **Grootboek** regel zijn eigen debet/credit-richting.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="e7b4b-177">In de volgende tabellen wordt de regel voor elk scenario weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="e7b4b-178">**Regel wanneer de functie is ingeschakeld.**</span><span class="sxs-lookup"><span data-stu-id="e7b4b-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="e7b4b-179">Journaalregel bedrag van project</span><span class="sxs-lookup"><span data-stu-id="e7b4b-179">Journal line amount of project</span></span> | <span data-ttu-id="e7b4b-180">Btw-richting</span><span class="sxs-lookup"><span data-stu-id="e7b4b-180">Sales tax direction</span></span>  | <span data-ttu-id="e7b4b-181">Teken btw-bedrag</span><span class="sxs-lookup"><span data-stu-id="e7b4b-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="e7b4b-182">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-182">Positive</span></span>                       | <span data-ttu-id="e7b4b-183">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-183">Sales Tax Receivable</span></span> | <span data-ttu-id="e7b4b-184">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-184">Positive</span></span>              |
| <span data-ttu-id="e7b4b-185">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-185">Negative</span></span>                       | <span data-ttu-id="e7b4b-186">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-186">Sales Tax Receivable</span></span> | <span data-ttu-id="e7b4b-187">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-187">Negative</span></span>              |

<span data-ttu-id="e7b4b-188">**Regel wanneer de functie is uitgeschakeld**</span><span class="sxs-lookup"><span data-stu-id="e7b4b-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="e7b4b-189">Journaalregel bedrag van grootboek</span><span class="sxs-lookup"><span data-stu-id="e7b4b-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="e7b4b-190">Btw-richting</span><span class="sxs-lookup"><span data-stu-id="e7b4b-190">Sales tax direction</span></span>  | <span data-ttu-id="e7b4b-191">Teken btw-bedrag</span><span class="sxs-lookup"><span data-stu-id="e7b4b-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="e7b4b-192">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-192">Positive</span></span>                       | <span data-ttu-id="e7b4b-193">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-193">Sales Tax Receivable</span></span> | <span data-ttu-id="e7b4b-194">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-194">Positive</span></span>              |
| <span data-ttu-id="e7b4b-195">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-195">Negative</span></span>                       | <span data-ttu-id="e7b4b-196">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-196">Sales Tax Receivable</span></span> | <span data-ttu-id="e7b4b-197">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="e7b4b-198">Het btw-bedrag en de rekening op het boekstuk bepalen</span><span class="sxs-lookup"><span data-stu-id="e7b4b-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="e7b4b-199">Wanneer u btw boekt, wordt de hoofdrekening opgehaald uit het groepsprofiel voor de grootboek-boekingen.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="e7b4b-200">Wanneer de btw terug te ontvangen is, gebruikt het systeem de rekening voor Te Ontvangen Btw die in het profiel is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="e7b4b-201">Wanneer de btw verschuldigd is, gebruikt het systeem de rekening voor Verschuldigde Btw die in het profiel is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="e7b4b-202">De volgende tabel laat de generieke regel zien.</span><span class="sxs-lookup"><span data-stu-id="e7b4b-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="e7b4b-203">Btw-richting</span><span class="sxs-lookup"><span data-stu-id="e7b4b-203">Sales tax direction</span></span>  | <span data-ttu-id="e7b4b-204">Teken btw-bedrag</span><span class="sxs-lookup"><span data-stu-id="e7b4b-204">Sales tax amount sign</span></span> | <span data-ttu-id="e7b4b-205">Btw-rekening</span><span class="sxs-lookup"><span data-stu-id="e7b4b-205">Sales tax account</span></span>      | <span data-ttu-id="e7b4b-206">Bedrag op boekstuk</span><span class="sxs-lookup"><span data-stu-id="e7b4b-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="e7b4b-207">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-207">Sales Tax Receivable</span></span> | <span data-ttu-id="e7b4b-208">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-208">Positive</span></span>              | <span data-ttu-id="e7b4b-209">Rekening voor Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-209">Tax Receivable Account</span></span> | <span data-ttu-id="e7b4b-210">Positief (Debet)</span><span class="sxs-lookup"><span data-stu-id="e7b4b-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="e7b4b-211">Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-211">Sales Tax Receivable</span></span> | <span data-ttu-id="e7b4b-212">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-212">Negative</span></span>              | <span data-ttu-id="e7b4b-213">Rekening voor Te Ontvangen Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-213">Tax Receivable Account</span></span> | <span data-ttu-id="e7b4b-214">Negatief (Credit)</span><span class="sxs-lookup"><span data-stu-id="e7b4b-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="e7b4b-215">Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-215">Sales Tax Payable</span></span>    | <span data-ttu-id="e7b4b-216">Positief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-216">Positive</span></span>              | <span data-ttu-id="e7b4b-217">Rekening voor Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-217">Tax Payable Account</span></span>    | <span data-ttu-id="e7b4b-218">Negatief (Credit)</span><span class="sxs-lookup"><span data-stu-id="e7b4b-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="e7b4b-219">Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-219">Sales Tax Payable</span></span>    | <span data-ttu-id="e7b4b-220">Negatief</span><span class="sxs-lookup"><span data-stu-id="e7b4b-220">Negative</span></span>              | <span data-ttu-id="e7b4b-221">Rekening voor Verschuldigde Btw</span><span class="sxs-lookup"><span data-stu-id="e7b4b-221">Tax Payable Account</span></span>    | <span data-ttu-id="e7b4b-222">Positief (Debet)</span><span class="sxs-lookup"><span data-stu-id="e7b4b-222">Positive (Debit)</span></span>  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]