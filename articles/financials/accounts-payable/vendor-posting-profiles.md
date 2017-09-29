---
title: Boekingsprofielen van leverancier
description: Met boekingsprofielen van leveranciers worden boekingen van leverancierstransacties naar het grootboek beheerd.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 540ad7be384e34054454cdc34c4945ed505b7963
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="a7dac-103">Boekingsprofielen van leverancier</span><span class="sxs-lookup"><span data-stu-id="a7dac-103">Vendor posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a7dac-104">Met boekingsprofielen van leveranciers worden boekingen van leverancierstransacties naar het grootboek beheerd.</span><span class="sxs-lookup"><span data-stu-id="a7dac-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="a7dac-105">Boekingsprofielen van leverancier</span><span class="sxs-lookup"><span data-stu-id="a7dac-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="a7dac-106">Met boekingsprofielen van leveranciers kunt u grootboekrekeningen en documentinstellingen aan alle leveranciers, een groep leveranciers of één leverancier toewijzen.</span><span class="sxs-lookup"><span data-stu-id="a7dac-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="a7dac-107">Deze instellingen worden gebruikt wanneer u inkooporders, leveranciersfacturen en contante betalingen maakt.</span><span class="sxs-lookup"><span data-stu-id="a7dac-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="a7dac-108">Voor sommige transacties kunt u een boekingsprofiel selecteren dat afwijkt van en voorrang heeft op de boekingsprofielen die zijn ingesteld voor transacties op deze pagina.</span><span class="sxs-lookup"><span data-stu-id="a7dac-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="a7dac-109">Het standaardboekingsprofiel wordt gedefinieerd op het sneltabblad Grootboek en btw op de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="a7dac-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="a7dac-110">Het standaardboekingsprofiel wordt vervolgens automatisch opgenomen in de koptekst van nieuwe documenten waarin u het vervolgens in een ander boekingsprofiel kunt wijzigen, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="a7dac-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="a7dac-111">Op de pagina Boekdefinities voor transacties kunt u boekingsdefinities ook aan transactieboekingstypen koppelen.</span><span class="sxs-lookup"><span data-stu-id="a7dac-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="a7dac-112">Boekingsdefinities regelen de boeking van leverancierstransacties naar het grootboek in plaats van boekingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="a7dac-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="a7dac-113">Een boekingsprofiel maken</span><span class="sxs-lookup"><span data-stu-id="a7dac-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="a7dac-114">**Instellingen**</span><span class="sxs-lookup"><span data-stu-id="a7dac-114">**Setup**</span></span>

<span data-ttu-id="a7dac-115">De grootboekrekeningen opgeven die bij het boeken van transacties met het geselecteerde boekingsprofiel worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a7dac-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="a7dac-116">Een rekeningcode en, voor zover mogelijk, een rekening of groep voor het geselecteerde boekingsprofiel selecteren.</span><span class="sxs-lookup"><span data-stu-id="a7dac-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="a7dac-117">In het boekingsproces wordt het meest passende boekingsprofiel voor elke transactie gevonden door te zoeken naar de meest specifieke combinatie van rekeningcode, rekeningnummer of groepsnummer met de volgende prioriteit:</span><span class="sxs-lookup"><span data-stu-id="a7dac-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="a7dac-118">De veldwaarde **Rekeningcode**</span><span class="sxs-lookup"><span data-stu-id="a7dac-118">**Account code** field value</span></span> | <span data-ttu-id="a7dac-119">De veldwaarde **Rekening/groepsnummer**</span><span class="sxs-lookup"><span data-stu-id="a7dac-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="a7dac-120">Zoekprioriteit</span><span class="sxs-lookup"><span data-stu-id="a7dac-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="a7dac-121">**Tabel**</span><span class="sxs-lookup"><span data-stu-id="a7dac-121">**Table**</span></span>                    | <span data-ttu-id="a7dac-122">Specifieke leveranciersrekening</span><span class="sxs-lookup"><span data-stu-id="a7dac-122">Specific vendor account</span></span>                     | <span data-ttu-id="a7dac-123">1</span><span class="sxs-lookup"><span data-stu-id="a7dac-123">1</span></span>               |
| <span data-ttu-id="a7dac-124">**Groep**</span><span class="sxs-lookup"><span data-stu-id="a7dac-124">**Group**</span></span>                    | <span data-ttu-id="a7dac-125">leveranciersgroep die aan de leverancier is toegewezen</span><span class="sxs-lookup"><span data-stu-id="a7dac-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="a7dac-126">2</span><span class="sxs-lookup"><span data-stu-id="a7dac-126">2</span></span>               |
| <span data-ttu-id="a7dac-127">**Alle**</span><span class="sxs-lookup"><span data-stu-id="a7dac-127">**All**</span></span>                      | <span data-ttu-id="a7dac-128">Leeg</span><span class="sxs-lookup"><span data-stu-id="a7dac-128">Blank</span></span>                                       | <span data-ttu-id="a7dac-129">3</span><span class="sxs-lookup"><span data-stu-id="a7dac-129">3</span></span>               |

<span data-ttu-id="a7dac-130">Als u wilt dat alle leverancierstransacties hetzelfde boekingsprofiel hebben, stelt u slechts één boekingsprofiel in met de optie Alle in het veld Rekeningcode.</span><span class="sxs-lookup"><span data-stu-id="a7dac-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="a7dac-131">Geef de volgende waarden op om uw boekingsprofiel in te stellen:</span><span class="sxs-lookup"><span data-stu-id="a7dac-131">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7dac-132">Veld</span><span class="sxs-lookup"><span data-stu-id="a7dac-132">Field</span></span></th>
<th><span data-ttu-id="a7dac-133">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a7dac-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7dac-134"><strong>Boekingsprofiel</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="a7dac-135">Een code invoeren voor het boekingsprofiel.</span><span class="sxs-lookup"><span data-stu-id="a7dac-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="a7dac-136">U kunt bijvoorbeeld twee boekingsprofielen maken om een rekening voor leverancierssaldi in de nationale valuta te verkrijgen en een andere voor leveranciersaldi in een vreemde valuta.</span><span class="sxs-lookup"><span data-stu-id="a7dac-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="a7dac-137">U zou dan de ene rekening Nationaal kunnen noemen en de andere Internationaal.</span><span class="sxs-lookup"><span data-stu-id="a7dac-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7dac-138"><strong>Omschrijving</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="a7dac-139">Een omschrijving van het boekingsprofiel invoeren.</span><span class="sxs-lookup"><span data-stu-id="a7dac-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7dac-140"><strong>Rekeningcode</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="a7dac-141">Opgeven of het boekingsprofiel van toepassing is op een specifieke leverancier, een groep leveranciers of alle leveranciers:</span><span class="sxs-lookup"><span data-stu-id="a7dac-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="a7dac-142"><strong>Tabel</strong>: het boekingsprofiel is van toepassing op een enkele leverancier.</span><span class="sxs-lookup"><span data-stu-id="a7dac-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="a7dac-143">Selecteer de leverancier in het veld Rekening/groepsnummer.</span><span class="sxs-lookup"><span data-stu-id="a7dac-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="a7dac-144"><strong>Groep</strong>: het boekingsprofiel is van toepassing op een leveranciersgroep.</span><span class="sxs-lookup"><span data-stu-id="a7dac-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="a7dac-145">Selecteer de leveranciersgroep in het veld Rekening/groepsnummer.</span><span class="sxs-lookup"><span data-stu-id="a7dac-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="a7dac-146"><strong>Alle</strong>: het boekingsprofiel is van toepassing op alle leveranciers.</span><span class="sxs-lookup"><span data-stu-id="a7dac-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="a7dac-147">Laat het veld Rekening/groepsnummer leeg.</span><span class="sxs-lookup"><span data-stu-id="a7dac-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7dac-148"><strong>Rekening/groepsnummer</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="a7dac-149">Als Tabel is geselecteerd in het veld Rekeningcode, selecteert u het rekeningnummer van de leverancier die aan het boekingsprofiel is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="a7dac-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="a7dac-150">Als Groep is geselecteerd, selecteert u een leveranciersgroep.</span><span class="sxs-lookup"><span data-stu-id="a7dac-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="a7dac-151">Als Alle is geselecteerd, laat u dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="a7dac-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7dac-152"><strong>Totaalrekening</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="a7dac-153">Selecteer de grootboekrekening die gebruikt wordt als overzichtsrekening voor de leveranciers waarnaar het boekingsprofiel verwijst.</span><span class="sxs-lookup"><span data-stu-id="a7dac-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a7dac-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Opmerking</span><span class="sxs-lookup"><span data-stu-id="a7dac-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="a7dac-155"><strong>Opmerking</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7dac-156">Als de schakeloptie Boekdefinities gebruiken is geselecteerd op de pagina Grootboekparameters, wordt de transactieboekingsdefinitie voor leveranciersfacturen gebruikt in plaats van de overzichtsrekening.</span><span class="sxs-lookup"><span data-stu-id="a7dac-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7dac-157"><strong>Rekening vereffenen</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="a7dac-158">De liquiditeitsgrootboekrekening selecteren die wordt gebruikt voor cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="a7dac-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="a7dac-159">Deze velden zijn alleen beschikbaar als cashflowprognoses zijn ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="a7dac-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7dac-160"><strong>Btw-vooruitbetalingen</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="a7dac-161">Selecteer de rekening voor btw-betalingen die vooruit ontvangen zijn.</span><span class="sxs-lookup"><span data-stu-id="a7dac-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a7dac-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Opmerking</span><span class="sxs-lookup"><span data-stu-id="a7dac-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="a7dac-163"><strong>Opmerking</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7dac-164">Het boekingsprofiel dat wordt gebruikt wanneer de betaling is gemarkeerd als een vooruitbetaling is geselecteerd in het veld Boekingsprofiel met journaalboekstuk van vooruitbetaling in het gedeelte Grootboek en btw van de pagina Parameters van module Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="a7dac-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7dac-165"><strong>Ontvangst</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="a7dac-166">Selecteer de grootboekrekening waarnaar informatie over niet-goedgekeurde leveranciersfacturen geboekt wordt.</span><span class="sxs-lookup"><span data-stu-id="a7dac-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="a7dac-167">De informatie wordt ingevoerd in het facturenregisterjournaal.</span><span class="sxs-lookup"><span data-stu-id="a7dac-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="a7dac-168">Een gebruiker voert bijvoorbeeld heel beperkte gegevens in over leveranciersfacturen als ze in het facturenregister worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="a7dac-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="a7dac-169">Als het facturenregister wordt geboekt, worden de transacties geboekt naar de rekening die hier en in het veld Tegenrekening is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="a7dac-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="a7dac-170">Als de facturen worden goedgekeurd, wordt de schuld overgeboekt van de ontvangstrekening naar de totaalrekening voor de leverancier.</span><span class="sxs-lookup"><span data-stu-id="a7dac-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7dac-171"><strong>Tegenrekening</strong></span><span class="sxs-lookup"><span data-stu-id="a7dac-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="a7dac-172">Selecteer de grootboekrekening die gebruikt wordt voor het tegenboeken van niet-goedgekeurde leveranciersfacturen die bijgewerkt worden met het facturenregister.</span><span class="sxs-lookup"><span data-stu-id="a7dac-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="a7dac-173">De tegenrekening fungeert als tegenrekening voor transacties die geboekt worden op binnenkomstrekeningen.</span><span class="sxs-lookup"><span data-stu-id="a7dac-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="a7dac-174">Daarom bevat de rekening leveranciersaankopen die nog niet zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="a7dac-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a><span data-ttu-id="a7dac-175">**Tabelbeperkingen**</span><span class="sxs-lookup"><span data-stu-id="a7dac-175">**Table restrictions**</span></span>

<span data-ttu-id="a7dac-176">Voor transacties met het geselecteerde boekingsprofiel geeft u op of transacties automatisch worden vereffend, rente wordt berekend en aanmaningen worden uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="a7dac-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="a7dac-177">U kunt ook de rekening selecteren die wordt gebruikt wanneer transacties met het geselecteerde boekingsprofiel worden afgesloten.</span><span class="sxs-lookup"><span data-stu-id="a7dac-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="a7dac-178">Geef de volgende waarden op om uw boekingsprofiel in te stellen:</span><span class="sxs-lookup"><span data-stu-id="a7dac-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="a7dac-179">Veld</span><span class="sxs-lookup"><span data-stu-id="a7dac-179">Field</span></span>          | <span data-ttu-id="a7dac-180">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a7dac-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7dac-181">**Vereffening**</span><span class="sxs-lookup"><span data-stu-id="a7dac-181">**Settlement**</span></span> | <span data-ttu-id="a7dac-182">Selecteer deze optie om automatische vereffening in te schakelen van transacties die dit boekingsprofiel hebben.</span><span class="sxs-lookup"><span data-stu-id="a7dac-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="a7dac-183">Als deze optie niet is geselecteerd, moet u transacties handmatig vereffenen via de pagina Openstaande transacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="a7dac-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="a7dac-184">**Annuleren**</span><span class="sxs-lookup"><span data-stu-id="a7dac-184">**Cancel**</span></span>     | <span data-ttu-id="a7dac-185">Selecteer deze optie als u transacties met dit boekingsprofiel wilt kunnen annuleren.</span><span class="sxs-lookup"><span data-stu-id="a7dac-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="a7dac-186">**Sluiten**</span><span class="sxs-lookup"><span data-stu-id="a7dac-186">**Close**</span></span>      | <span data-ttu-id="a7dac-187">Selecteer een boekingsprofiel om naar over te gaan als transacties met dit boekingsprofiel gesloten zijn.</span><span class="sxs-lookup"><span data-stu-id="a7dac-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="a7dac-188">Een transactie wordt als afgesloten beschouwd als deze volledig is vereffend.</span><span class="sxs-lookup"><span data-stu-id="a7dac-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






