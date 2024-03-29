---
title: Handmatig vracht afstemmen
description: Deze procedure laat zien hoe u vracht handmatig afstemt.
author: Weijiesa
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily, TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8afec41cdb10185077d39a665d0153df1c9bdb9f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672733"
---
# <a name="reconcile-freight-manually"></a>Handmatig vracht afstemmen

[!include [banner](../../includes/banner.md)]]

Deze procedure laat zien hoe u vracht handmatig afstemt. Dit wordt gewoonlijk gedaan door een transportcoördinator. U kunt deze procedure gebruiken in het demobedrijf USMF.


## <a name="select-a-load-to-reconcile"></a>Selecteer belasting om af te stemmen
1. Ga naar Transportbeheer > Planning > Workbench van ladingplanning.
2. Schakel het selectievakje Verzonden en ontvangen verbergen uit. 
3. Selecteer in de lijst de lading met id 00006.

## <a name="create-a-carrier-invoice"></a>Een leverancierfactuur maken
Als u handmatig vracht afstemt en vervoerdersfacturen niet automatisch ontvangt, kunt u een factuur maken op basis van de vrachtfactuur.  
1. Klik op Verwante informatie.
2. Klik op Details vrachtfactuur weergeven.
3. Klik op Vrachtfactuur genereren.
4. Typ een waarde in het veld Factuur.
5. Klik op OK.

## <a name="reconcile-the-invoice"></a>De factuur afstemmen
Wanneer u een vervoerderfactuur en een vrachtfactuur afstemt, wordt dat regel voor regel gedaan.  
1. Klik op Vrachtfacturen en facturen vereffenen.
2. Vouw de sectie Factuurdetails uit.
3. Vouw de sectie Niet-afgestemde details vrachtfactuur uit.
4. Markeer in de lijst de geselecteerde rij.
5. Klik op Afstemmen.
6. Vouw de sectie Afgestemde details vrachtfactuur uit.

## <a name="submit-the-invoice-for-approval"></a>De factuur verzenden voor goedkeuring
1. Klik op Aanbieden ter goedkeuring.
2. Sluit de pagina.
3. Schakel het selectievakje Goedgekeurd verbergen uit. 
4. Klik op Leveranciersfactuurjournalen.
5. Klik om de koppeling in het veld Verwijzing naar journaalnummer te volgen.
6. Klik op Regels.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]