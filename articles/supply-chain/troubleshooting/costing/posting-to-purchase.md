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
ms.openlocfilehash: 304609e065389d4f56913ae3f2f7fc562de2eadc9f0885ddbe2c8f4747081c66
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722170"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>Inkoopontvangst met een nulbedrag wordt geboekt voor een productontvangstbon met nulwaarde

KB-nummer: 4612588

## <a name="symptoms"></a>Symptomen

Wanneer een productontvangstbon met een nulwaarde wordt geboekt, wordt een boeking naar inkooptoerekening gemaakt waarbij het bedrag 0 (nul) is.

## <a name="resolution"></a>Oplossing

Voor boekingen in het grootboek van het type *Inkoop, toerekening*, wordt het veld `IsTransferredIndetail` standaard ingesteld op *Samenvatting* in subgrootboektransacties. Er wordt dus een bijbehorende boekstukinvoer gemaakt, zelfs als het bedrag 0 (nul) is.

Om dit boekingstype over te slaan wanneer het bedrag 0 (nul) is, moet u de methode `subledgerJournalizer.markDoNotTransferEntries` uitbreiden zodat deze `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount` omvat, zoals in het volgende voorbeeld wordt weergegeven.

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
