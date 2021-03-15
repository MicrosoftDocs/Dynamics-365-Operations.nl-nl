---
title: Leverancierfactuur vastleggen en met ontvangen hoeveelheid matchen
description: Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be1e818e8a97684248c9c0b9d43c39e631f855f5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979258"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Leverancierfactuur vastleggen en met ontvangen hoeveelheid matchen

[!include [banner](../../includes/banner.md)]

Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling. Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd. 

In de pagina van parameters voor leveranciers, moet u ervoor zorgen dat de optie Factuurvereffeningsvalidatie inschakelen is geselecteerd, het veld Factuur met verschillen boeken is ingesteld en het veld Regelovereenstemmingsbeleid is ingesteld op Drieweg-afstemming.

Bij deze procedure wordt het demobedrijf USMF gebruikt. De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren.


## <a name="create-a-purchase-order"></a>Inkooporder maken
1. Ga naar Alle inkooporders.
2. Klik op Nieuw.
3. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Typ een waarde in het veld Leveranciersrekening.
5. Klik op OK.
6. Klik op Regel toevoegen.
7. Typ een waarde in het veld Artikelnummer.
8. Klik in het actievenster op Inkoop.
9. Klik op Bevestigen.

## <a name="post-a-product-receipt"></a>Een productontvangstbon boeken
1. Klik in het actievenster op Ontvangen.
2. Klik op Productontvangstbon.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld Productontvangstbon.
5. Klik op OK.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Een leveranciersfactuur registreren en vereffenen met productontvangstbon
1. Klik in het actievenster op Factuur.
2. Klik op Factuur.
3. Typ een waarde in het veld Nummer.
4. Klik op Standaard vanaf: Bestelde hoeveelheid om het dialoogvenster voor beëindigen te openen.
5. Selecteer een optie in het veld Standaardhoeveelheid voor regels.
6. Klik op OK.
7. Klik op Ja.
8. Klik op Productontvangstbonnen vereffenen.
9. Klik op OK.
10. Klik in het actievenster op Controleren.
11. Klik op Vereffeningsgegevens.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]