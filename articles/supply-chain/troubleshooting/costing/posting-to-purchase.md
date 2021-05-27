---
title: Inkoopontvangst met een nulbedrag wordt geboekt voor een productontvangstbon met nulwaarde
description: Wanneer een productontvangstbon met een nulwaarde wordt geboekt, wordt een boeking naar inkooptoerekening gemaakt waarbij het bedrag 0 (nul) is.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f8d9d857590dc788d16b01edf77600d8fd8c8444
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026421"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a><span data-ttu-id="ab2e8-103">Inkoopontvangst met een nulbedrag wordt geboekt voor een productontvangstbon met nulwaarde</span><span class="sxs-lookup"><span data-stu-id="ab2e8-103">Purchase accrual that has a zero amount is posted for a zero-value product receipt</span></span>

<span data-ttu-id="ab2e8-104">KB-nummer: 4612588</span><span class="sxs-lookup"><span data-stu-id="ab2e8-104">KB number: 4612588</span></span>

## <a name="symptoms"></a><span data-ttu-id="ab2e8-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="ab2e8-105">Symptoms</span></span>

<span data-ttu-id="ab2e8-106">Wanneer een productontvangstbon met een nulwaarde wordt geboekt, wordt een boeking naar inkooptoerekening gemaakt waarbij het bedrag 0 (nul) is.</span><span class="sxs-lookup"><span data-stu-id="ab2e8-106">When a product receipt that has zero value is posted, the system creates a posting to purchase accrual where the amount is 0 (zero).</span></span>

## <a name="resolution"></a><span data-ttu-id="ab2e8-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="ab2e8-107">Resolution</span></span>

<span data-ttu-id="ab2e8-108">Voor boekingen in het grootboek van het type *Inkoop, toerekening*, wordt het veld `IsTransferredIndetail` standaard ingesteld op *Samenvatting* in subgrootboektransacties.</span><span class="sxs-lookup"><span data-stu-id="ab2e8-108">By default, for ledger postings of the *Purchase, accrual* type, the `IsTransferredIndetail` field is always set to *Summary* in subledger transactions.</span></span> <span data-ttu-id="ab2e8-109">Er wordt dus een bijbehorende boekstukinvoer gemaakt, zelfs als het bedrag 0 (nul) is.</span><span class="sxs-lookup"><span data-stu-id="ab2e8-109">Therefore, the system creates a related voucher entry even if the amount is 0 (zero).</span></span>

<span data-ttu-id="ab2e8-110">Om dit boekingstype over te slaan wanneer het bedrag 0 (nul) is, moet u de methode `subledgerJournalizer.markDoNotTransferEntries` uitbreiden zodat deze `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` omvat, zoals in het volgende voorbeeld wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ab2e8-110">To skip this posting type when the amount is 0 (zero), extend the `subledgerJournalizer.markDoNotTransferEntries` method so that it includes `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`, as shown in the following example.</span></span>

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
