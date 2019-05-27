---
title: Boekhoudingsverdelingen en journaalposten in de subadministratie voor facturen met vrije tekst
description: Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de omzet, btw of heffingen zal worden verwerkt op een factuur met vrije tekst. Elk bedrag dat moet worden verwerkt wanneer de factuur met vrije tekst in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d1546e8537110daec5d6655f68d3328a58ca1cb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571183"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="1a460-104">Boekhoudingsverdelingen en journaalposten in de subadministratie voor facturen met vrije tekst</span><span class="sxs-lookup"><span data-stu-id="1a460-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a460-105">Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de omzet, btw of heffingen zal worden verwerkt op een factuur met vrije tekst.</span><span class="sxs-lookup"><span data-stu-id="1a460-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="1a460-106">Elk bedrag dat moet worden verwerkt wanneer de factuur met vrije tekst in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen.</span><span class="sxs-lookup"><span data-stu-id="1a460-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="1a460-107">Boekhoudingsverdelingen</span><span class="sxs-lookup"><span data-stu-id="1a460-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="1a460-108">U kunt de volgende knoppen in de pagina Vrije-tekstfactuur gebruiken voor het weergeven en mogelijk wijzigen van de boekhoudingsverdelingen voor elk bedrag op de factuur met vrije tekst.</span><span class="sxs-lookup"><span data-stu-id="1a460-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="1a460-109">**Bedragen verdelen**: De boekhoudingsverdelingen weergeven en wijzigen voor een afzonderlijke regel en alle onderliggende regels, zoals belastingen of heffingen.</span><span class="sxs-lookup"><span data-stu-id="1a460-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="1a460-110">U kunt de boekhoudingsverdeling voor de onderliggende regel rechtstreeks weergeven en wijzigen op de pagina Btw-transacties of de pagina Transacties met toeslagen transacties.</span><span class="sxs-lookup"><span data-stu-id="1a460-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="1a460-111">Bedragen in de koptekst van facturen met vrije tekst wijzigen, zoals heffingen of valuta-afrondingsbedragen.</span><span class="sxs-lookup"><span data-stu-id="1a460-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="1a460-112">Bedragen op regels van facturen met vrije tekst wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1a460-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="1a460-113">**Verdelingen weergeven**: Voor alle regels op het document de boekhoudingsverdelingen weergeven.</span><span class="sxs-lookup"><span data-stu-id="1a460-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="1a460-114">Vanuit deze weergave kunt u de boekhoudingsverdelingen niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1a460-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="1a460-115">Bedragen in de koptekst en op de regel weergeven.</span><span class="sxs-lookup"><span data-stu-id="1a460-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="1a460-116">Bedragen verdelen</span><span class="sxs-lookup"><span data-stu-id="1a460-116">Distributing amounts</span></span>
<span data-ttu-id="1a460-117">Wanneer u een factuur met vrije tekst invoert, wordt elk bedrag als volgt verdeeld.</span><span class="sxs-lookup"><span data-stu-id="1a460-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1a460-118">Type monetair bedrag</span><span class="sxs-lookup"><span data-stu-id="1a460-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="1a460-119">Van waaruit de hoofdrekening wordt weergegeven</span><span class="sxs-lookup"><span data-stu-id="1a460-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="1a460-120">Volgorde van prioriteit die bepaalt welke standaard financiële dimensie wordt weergegeven</span><span class="sxs-lookup"><span data-stu-id="1a460-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a460-121">Factuurregel van vrije tekst-factuur</span><span class="sxs-lookup"><span data-stu-id="1a460-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="1a460-122">De grootboekrekening op de factuurregel van de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="1a460-123">Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</span><span class="sxs-lookup"><span data-stu-id="1a460-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="1a460-124">Indien de hoofdrekening geen toewijzingsrekening is, gebruikt u de standaardsjabloon voor financiële dimensie op de factuurregel voor de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1a460-125">De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1a460-126">De standaard financiële dimensiewaarden gebruiken van de grootboekrekening in de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="1a460-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a460-127">Factuurregel voor vrije tekst-factuur voor een vaste activa-nummer en waardemodelcombinatie</span><span class="sxs-lookup"><span data-stu-id="1a460-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1a460-128"><strong>Opmerking </strong></span><span class="sxs-lookup"><span data-stu-id="1a460-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a460-129">De hoofdrekening op de factuurregel voor de vrije tekst-factuur is de verwerkingsrekening voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="1a460-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="1a460-130">De grootboekrekening op de factuurregel van de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="1a460-131">De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1a460-132">De standaard financiële dimensiewaarden gebruiken van de grootboekrekening in de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="1a460-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a460-133">Kortingsbedrag voor de vrije tekst-factuur</span><span class="sxs-lookup"><span data-stu-id="1a460-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="1a460-134">Het veld Hoofdrekening voor klantkortingen op de pagina Contantkortingen.</span><span class="sxs-lookup"><span data-stu-id="1a460-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="1a460-135">Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</span><span class="sxs-lookup"><span data-stu-id="1a460-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="1a460-136">Indien de hoofdrekening geen toewijzingsrekening is, gebruikt u de standaardsjabloon voor financiële dimensie op de factuurregel voor de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1a460-137">De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1a460-138">De standaard financiële dimensiewaarden gebruiken van de grootboekrekening in de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="1a460-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a460-139">Btw-bedrag voor de vrije tekst-factuur</span><span class="sxs-lookup"><span data-stu-id="1a460-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="1a460-140">Het veld Te betalen btw op de pagina Grootboekboekingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="1a460-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="1a460-141">De financiële dimensies gebruiken die zijn gedefinieerd op het regelbedrag van de vrije tekst-factuur of de verdelingen voor het heffingsregelbedrag.</span><span class="sxs-lookup"><span data-stu-id="1a460-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="1a460-142">De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1a460-143">De standaard financiële dimensiewaarden gebruiken van de grootboekrekening in de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="1a460-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1a460-144">Heffingsregelbedrag op vrije tekst-factuur</span><span class="sxs-lookup"><span data-stu-id="1a460-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="1a460-145">Het veld Creditrekening in de pagina Toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="1a460-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="1a460-146">Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</span><span class="sxs-lookup"><span data-stu-id="1a460-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="1a460-147">Indien de hoofdrekening geen toewijzingsrekening is, gebruikt u de standaardsjabloon voor financiële dimensie op de factuurregel voor de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1a460-148">De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</span><span class="sxs-lookup"><span data-stu-id="1a460-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="1a460-149">De standaard financiële dimensiewaarden gebruiken van de grootboekrekening in de pagina Rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="1a460-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="1a460-150">Belastingen verdelen</span><span class="sxs-lookup"><span data-stu-id="1a460-150">Distributing taxes</span></span>
<span data-ttu-id="1a460-151">Boekhoudingsverdelingen voor belastingen kunnen pas worden gemaakt nadat belastingen zijn berekend.</span><span class="sxs-lookup"><span data-stu-id="1a460-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="1a460-152">Voor het berekenen van de btw moet u een van de volgende taken uitvoeren in het formulier Vrije-tekstfactuur:</span><span class="sxs-lookup"><span data-stu-id="1a460-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="1a460-153">De btw weergeven.</span><span class="sxs-lookup"><span data-stu-id="1a460-153">View the sales tax.</span></span>
-   <span data-ttu-id="1a460-154">Het factuurtotaal weergeven.</span><span class="sxs-lookup"><span data-stu-id="1a460-154">View the invoice total.</span></span>
-   <span data-ttu-id="1a460-155">De cashflow weergeven.</span><span class="sxs-lookup"><span data-stu-id="1a460-155">View the cash flow.</span></span>
-   <span data-ttu-id="1a460-156">Boekhoudingsverdelingen voor de totale vrije tekst-factuur weergeven.</span><span class="sxs-lookup"><span data-stu-id="1a460-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="1a460-157">De subadministratie bekijken.</span><span class="sxs-lookup"><span data-stu-id="1a460-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="1a460-158">Subadministratie voor vrije tekst-facturen</span><span class="sxs-lookup"><span data-stu-id="1a460-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="1a460-159">Voordat u een vrije tekst-factuur boekt, kunt u het volledige boekhoudingsjournaal van de factuur bekijken, inclusief debet- en creditbedragen, om te controleren of de factuur naar de juiste rekeningen wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="1a460-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="1a460-160">Deze weergave van het volledige boekhoudingsjournaal heet een subadministratie.</span><span class="sxs-lookup"><span data-stu-id="1a460-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="1a460-161">Indien het journaal in de subadministratie onjuist is wanneer u een afdrukvoorbeeld bekijkt voordat u de vrije tekst-factuur boekt, kunt u het journaal in de subadministratie niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1a460-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="1a460-162">In plaats daarvan moet u de boekhoudingsverdelingen of het boekingsprofiel wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1a460-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="1a460-163">De boekhoudingsverdelingen worden gebruikt om één kant van de boekhoudingspost, de debit- of de creditzijde, te definiëren.</span><span class="sxs-lookup"><span data-stu-id="1a460-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="1a460-164">De compenserende journaalregel in de subadministratie wordt gemaakt van de boekingsprofielen, zoals van de klantrekening of de belasting.</span><span class="sxs-lookup"><span data-stu-id="1a460-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>



