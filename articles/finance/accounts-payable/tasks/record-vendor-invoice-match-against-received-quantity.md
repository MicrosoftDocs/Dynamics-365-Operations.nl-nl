---
title: Leverancierfactuur vastleggen en met ontvangen hoeveelheid matchen
description: Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a3f1463821a43af0d8d5f15225944b080414e4c
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109913"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Leverancierfactuur vastleggen en met ontvangen hoeveelheid matchen

[!include [banner](../../includes/banner.md)]

Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling. Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd. 

Op de pagina **Parameters van module Leveranciers** moet u ervoor zorgen dat de optie **Factuurvereffeningsvalidatie inschakelen** is geselecteerd, het veld **Factuur met verschillen boeken** is ingesteld op **Goedkeuring vereisen** en het veld **Regelovereenstemmingsbeleid** is ingesteld op **Drieweg-afstemming**.

Bij deze procedure wordt het demobedrijf USMF gebruikt. De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren.


## <a name="create-a-purchase-order"></a>Inkooporder maken
1. Ga naar Alle inkooporders.
2. Klik op **Nieuw**.
3. Klik in het veld **Leverancier** op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Typ een waarde in het veld **Leveranciersrekening**.
5. Klik op **OK**.
6. Klik op **Regel toevoegen**.
7. Typ een waarde in het veld **Artikelnummer**.
8. Klik in het actievenster op **Inkoop**.
9. Klik op **Bevestigen**.

## <a name="post-a-product-receipt"></a>Een productontvangstbon boeken
1. Klik in het actievenster op **Ontvangen**.
2. Klik op **Productontvangstbon**.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld **Productontvangstbon**.
5. Klik op **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Een leveranciersfactuur registreren en vereffenen met productontvangstbon
1. Klik in het actievenster op **Factuur**.
2. Klik op **Factuur**.
3. Typ een waarde in het veld **Nummer**.
4. Klik op **Standaard vanaf: Bestelde hoeveelheid** om het dialoogvenster voor beëindigen te openen.
5. Selecteer een optie in het veld **Standaardhoeveelheid voor regels**.
6. Klik tot slot op **OK**.
7. Klik op **Ja**.
8. Klik op **Productontvangstbonnen vereffenen**.
9. Klik tot slot op **OK**.
10. Klik in het actievenster op **Controleren**.
11. Klik op **Vereffeningsgegevens**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
