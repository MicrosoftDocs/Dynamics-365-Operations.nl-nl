---
title: Boekingsprofielen van klant
description: Met klantprofielen wordt de boeking van klanttransacties naar het grootboek beheerd.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ccd663a769aa98afb800f6fcd6217f39bb513597
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="e65ec-103">Boekingsprofielen van klant</span><span class="sxs-lookup"><span data-stu-id="e65ec-103">Customer posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e65ec-104">Met klantprofielen wordt de boeking van klanttransacties naar het grootboek beheerd.</span><span class="sxs-lookup"><span data-stu-id="e65ec-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="e65ec-105">Boekingsprofielen van klant</span><span class="sxs-lookup"><span data-stu-id="e65ec-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="e65ec-106">Met boekingsprofielen van klanten kunt u grootboekrekeningen en documentinstellingen aan alle klanten, een groep klanten of één klant toewijzen.</span><span class="sxs-lookup"><span data-stu-id="e65ec-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="e65ec-107">Deze instellingen worden gebruikt als u verkooporders, vrije-tekstfacturen, contante betalingen, aanmaningen en rentenota's maakt.</span><span class="sxs-lookup"><span data-stu-id="e65ec-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="e65ec-108">Voor sommige transacties kunt u een boekingsprofiel selecteren dat afwijkt van en voorrang heeft op de boekingsprofielen die zijn ingesteld voor transacties op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="e65ec-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="e65ec-109">Het standaardboekingsprofiel wordt gedefinieerd op het sneltabblad Grootboek en btw op de pagina Parameters van module Klanten.</span><span class="sxs-lookup"><span data-stu-id="e65ec-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="e65ec-110">Het standaardboekingsprofiel wordt vervolgens automatisch opgenomen in de koptekst van nieuwe documenten waarin u het vervolgens in een ander boekingsprofiel kunt wijzigen, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="e65ec-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="e65ec-111">Op de pagina Boekdefinities voor transacties kunt u boekingsdefinities ook aan transactieboekingstypen koppelen.</span><span class="sxs-lookup"><span data-stu-id="e65ec-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="e65ec-112">Boekingsdefinities regelen de boeking van klanttransacties naar het grootboek in plaats van boekingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="e65ec-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="e65ec-113">Een boekingsprofiel maken</span><span class="sxs-lookup"><span data-stu-id="e65ec-113">Creating a posting profile</span></span>
<span data-ttu-id="e65ec-114">De grootboekrekeningen opgeven die bij het boeken van transacties met het geselecteerde boekingsprofiel worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e65ec-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="e65ec-115">Een rekeningcode en, voor zover mogelijk, een rekening of groep voor het geselecteerde boekingsprofiel selecteren.</span><span class="sxs-lookup"><span data-stu-id="e65ec-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="e65ec-116">In het boekingsproces wordt het meest passende boekingsprofiel voor elke transactie gevonden door te zoeken naar de meest specifieke combinatie van rekeningcode, rekeningnummer of groepsnummer met de volgende prioriteit:</span><span class="sxs-lookup"><span data-stu-id="e65ec-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="e65ec-117">De veldwaarde **Rekeningcode**</span><span class="sxs-lookup"><span data-stu-id="e65ec-117">**Account code** field value</span></span> | <span data-ttu-id="e65ec-118">De veldwaarde **Rekening/groepsnummer**</span><span class="sxs-lookup"><span data-stu-id="e65ec-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="e65ec-119">Zoekprioriteit</span><span class="sxs-lookup"><span data-stu-id="e65ec-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="e65ec-120">**Tabel**</span><span class="sxs-lookup"><span data-stu-id="e65ec-120">**Table**</span></span>                    | <span data-ttu-id="e65ec-121">Specifieke klantenrekening</span><span class="sxs-lookup"><span data-stu-id="e65ec-121">Specific customer account</span></span>                       | <span data-ttu-id="e65ec-122">1</span><span class="sxs-lookup"><span data-stu-id="e65ec-122">1</span></span>               |
| <span data-ttu-id="e65ec-123">**Groep**</span><span class="sxs-lookup"><span data-stu-id="e65ec-123">**Group**</span></span>                    | <span data-ttu-id="e65ec-124">Klantengroep die is toegewezen aan de klant</span><span class="sxs-lookup"><span data-stu-id="e65ec-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="e65ec-125">2</span><span class="sxs-lookup"><span data-stu-id="e65ec-125">2</span></span>               |
| <span data-ttu-id="e65ec-126">**Alle**</span><span class="sxs-lookup"><span data-stu-id="e65ec-126">**All**</span></span>                      | <span data-ttu-id="e65ec-127">Leeg</span><span class="sxs-lookup"><span data-stu-id="e65ec-127">Blank</span></span>                                           | <span data-ttu-id="e65ec-128">3</span><span class="sxs-lookup"><span data-stu-id="e65ec-128">3</span></span>               |

<span data-ttu-id="e65ec-129">Als u wilt dat alle klanttransacties hetzelfde boekingsprofiel hebben, stelt u slechts één boekingsprofiel in met de optie Alle in het veld Rekeningcode.</span><span class="sxs-lookup"><span data-stu-id="e65ec-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="e65ec-130">Geef de volgende waarden op om uw boekingsprofiel in te stellen:</span><span class="sxs-lookup"><span data-stu-id="e65ec-130">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e65ec-131">Veld</span><span class="sxs-lookup"><span data-stu-id="e65ec-131">Field</span></span></th>
<th><span data-ttu-id="e65ec-132">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e65ec-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e65ec-133"><strong>Boekingsprofiel</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="e65ec-134">Een code invoeren voor het boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="e65ec-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="e65ec-135">U kunt bijvoorbeeld twee boekingsprofielen maken om één rekening te krijgen voor klantsaldi in de nationale valuta en een andere rekening voor klantsaldi in een vreemde valuta.</span><span class="sxs-lookup"><span data-stu-id="e65ec-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="e65ec-136">U zou dan de ene rekening Nationaal kunnen noemen en de andere Internationaal.</span><span class="sxs-lookup"><span data-stu-id="e65ec-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e65ec-137"><strong>Omschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="e65ec-138">Een omschrijving van het boekingsprofiel invoeren.</span><span class="sxs-lookup"><span data-stu-id="e65ec-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="e65ec-139">Dit wordt alleen gebruikt om het boekingsprofiel beter te identificeren wanneer u het op deze pagina weergeeft.</span><span class="sxs-lookup"><span data-stu-id="e65ec-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e65ec-140"><strong>Rekeningcode</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="e65ec-141">Opgeven of het boekingsprofiel van toepassing is op één klant, een groep klanten of op alle klanten:</span><span class="sxs-lookup"><span data-stu-id="e65ec-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="e65ec-142"><strong>Tabel</strong>: het boekingsprofiel is van toepassing op een enkele klant.</span><span class="sxs-lookup"><span data-stu-id="e65ec-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="e65ec-143">Selecteer de klantrekening in het veld Rekening/groepsnummer.</span><span class="sxs-lookup"><span data-stu-id="e65ec-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="e65ec-144"><strong>Groep</strong>: het boekingsprofiel is van toepassing op een klantgroep.</span><span class="sxs-lookup"><span data-stu-id="e65ec-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="e65ec-145">Selecteer de klantgroep in het veld Rekening/groepsnummer.</span><span class="sxs-lookup"><span data-stu-id="e65ec-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="e65ec-146"><strong>Alle</strong>: het boekingsprofiel is van toepassing op alle klanten.</span><span class="sxs-lookup"><span data-stu-id="e65ec-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="e65ec-147">Laat het veld Rekening/groepsnummer leeg.</span><span class="sxs-lookup"><span data-stu-id="e65ec-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e65ec-148"><strong>Rekening/groepsnummer</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="e65ec-149">Als Tabel is geselecteerd in het veld Rekeningcode, selecteert u het rekeningnummer van de klant die aan het boekingsprofiel is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e65ec-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="e65ec-150">Selecteer de klantengroep als Groep is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e65ec-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="e65ec-151">Als Alle is geselecteerd, laat u dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="e65ec-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e65ec-152"><strong>Totaalrekening</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="e65ec-153">De grootboekrekening selecteren die wordt gebruikt als de klantoverzichtsrekening voor klanten die aan het boekingsprofiel zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="e65ec-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e65ec-154"><strong>Rekening vereffenen</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="e65ec-155">De liquiditeitsgrootboekrekening selecteren die wordt gebruikt voor cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="e65ec-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="e65ec-156">Dit veld wordt alleen weergegeven als cashflowprognoses zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="e65ec-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e65ec-157"><strong>Btw-vooruitbetalingen</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="e65ec-158">De rekening selecteren voor btw op ontvangen vooruitbetalingen.</span><span class="sxs-lookup"><span data-stu-id="e65ec-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e65ec-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Opmerking</span><span class="sxs-lookup"><span data-stu-id="e65ec-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="e65ec-160"><strong>Opmerking</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e65ec-161">Gebruik de pagina Parameters van module Klanten om het boekingsprofiel op te geven dat u wilt gebruiken wanneer een betaling is gemarkeerd als een vooruitbetaling.</span><span class="sxs-lookup"><span data-stu-id="e65ec-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e65ec-162"><strong>Aansprakelijkheden voor discontorekening</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="e65ec-163">De grootboekrekening voor verplichtingen voor disconto selecteren.</span><span class="sxs-lookup"><span data-stu-id="e65ec-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e65ec-164"><strong>Aanmaningsreeks</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="e65ec-165">De identificatie selecteren van de aanmaningsreeks die wordt gebruikt voor klanten waaraan het boekingsprofiel is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e65ec-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e65ec-166"><strong>Rentecode</strong></span><span class="sxs-lookup"><span data-stu-id="e65ec-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="e65ec-167">De rentecode selecteren die u wilt gebruiken voor de berekening van rente voor klanten aan wie het boekingsprofiel is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="e65ec-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="e65ec-168">**Tabelbeperkingen**</span><span class="sxs-lookup"><span data-stu-id="e65ec-168">**Table restrictions**</span></span>

<span data-ttu-id="e65ec-169">Voor transacties met het geselecteerde boekingsprofiel geeft u op of transacties automatisch worden vereffend, rente wordt berekend en aanmaningen worden uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="e65ec-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="e65ec-170">U kunt ook de rekening selecteren die wordt gebruikt wanneer transacties met het geselecteerde boekingsprofiel worden afgesloten.</span><span class="sxs-lookup"><span data-stu-id="e65ec-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="e65ec-171">Geef de volgende waarden op om uw boekingsprofiel in te stellen:</span><span class="sxs-lookup"><span data-stu-id="e65ec-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="e65ec-172">Veld</span><span class="sxs-lookup"><span data-stu-id="e65ec-172">Field</span></span>                 | <span data-ttu-id="e65ec-173">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e65ec-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e65ec-174">**Vereffening**</span><span class="sxs-lookup"><span data-stu-id="e65ec-174">**Settlement**</span></span>        | <span data-ttu-id="e65ec-175">Selecteer deze schakeloptie om de automatische vereffening in te schakelen van transacties die dit boekingsprofiel hebben.</span><span class="sxs-lookup"><span data-stu-id="e65ec-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="e65ec-176">Als deze schakeloptie niet is geselecteerd, moet u transacties handmatig op de pagina Openstaande transacties vereffenen of Klantbetalingen invoeren.</span><span class="sxs-lookup"><span data-stu-id="e65ec-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="e65ec-177">**Interesse**</span><span class="sxs-lookup"><span data-stu-id="e65ec-177">**Interest**</span></span>          | <span data-ttu-id="e65ec-178">Selecteer deze schakeloptie als rente moet worden berekend over openstaande saldi voor klantrekeningen die dit profiel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e65ec-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="e65ec-179">Als deze schakeloptie niet is geselecteerd, wordt voor deze klanten geen rente berekend.</span><span class="sxs-lookup"><span data-stu-id="e65ec-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="e65ec-180">**Aanmaning**</span><span class="sxs-lookup"><span data-stu-id="e65ec-180">**Collection letter**</span></span> | <span data-ttu-id="e65ec-181">Selecteer deze schakeloptie als aanmaningen moeten worden gegenereerd voor klantrekeningen die dit profiel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e65ec-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="e65ec-182">Als deze schakeloptie niet is geselecteerd, worden voor deze klanten geen aanmaningen gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e65ec-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="e65ec-183">**Sluiten**</span><span class="sxs-lookup"><span data-stu-id="e65ec-183">**Close**</span></span>             | <span data-ttu-id="e65ec-184">Selecteer een boekingsprofiel om naar over te gaan als transacties met dit boekingsprofiel gesloten zijn.</span><span class="sxs-lookup"><span data-stu-id="e65ec-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="e65ec-185">Een transactie wordt als afgesloten beschouwd als deze volledig is vereffend.</span><span class="sxs-lookup"><span data-stu-id="e65ec-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="e65ec-186">Zie [Overzicht van klantbetalingen](../cash-bank-management/tasks/customer-payment-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e65ec-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


