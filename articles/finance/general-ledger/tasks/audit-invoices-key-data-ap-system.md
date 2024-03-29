---
title: Facturen en hoofdgegevens controleren in Leveranciers
description: In dit artikel leert u hoe u facturen en hoofdgegevens controleert in Leveranciers.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4525534f906322c7fe4c232f0f6da5b308829087
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775210"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Facturen en hoofdgegevens controleren in leveranciers

[!include [banner](../../includes/banner.md)]

Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling. Controleer voordat u begint of de configuratiesleutel Factuurvereffening is geselecteerd. 

Op de pagina **Parameters van module Leveranciers** moet u ervoor zorgen dat de optie **Factuurvereffeningsvalidatie inschakelen** is geselecteerd, het veld **Factuur met verschillen boeken** is ingesteld op **Goedkeuring vereisen** en het veld **Regelovereenstemmingsbeleid** is ingesteld op **Drieweg-afstemming**.

Bij deze procedure wordt het demobedrijf USMF gebruikt. De leveranciersmanager of Accounting Manager-rol kan deze stappen uitvoeren.


## <a name="create-a-purchase-order"></a>Inkooporder maken
1. Ga naar **Alle inkooporders**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Leveranciersrekening**.
4. Klik tot slot op **OK**.
5. Klik op **Regel toevoegen**.
6. Typ een waarde in het veld **Artikelnummer**.
7. Klik in het actievenster op **Inkoop**.
8. Klik op **Bevestigen**.

## <a name="post-a-product-receipt"></a>Een productontvangstbon boeken
1. Klik in het actievenster op **Ontvangen**.
2. Klik op **Productontvangstbon**.
3. Typ een waarde in het veld **Productontvangstbon**.
4. Klik tot slot op **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Een leveranciersfactuur registreren en vereffenen met productontvangstbon
1. Klik in het actievenster op **Factuur > Factuur**.
2. Typ een waarde in het veld **Nummer**.
3. Klik op **Standaard vanaf: Bestelde hoeveelheid** om het dialoogvenster voor beëindigen te openen.
4. Selecteer een optie in het veld **Standaardhoeveelheid voor regels**.
5. Klik tot slot op **OK**.
6. Klik op **Ja**.
7. Klik op **Productontvangstbonnen vereffenen**.
8. Klik tot slot op **OK**.
9. Klik in het actievenster op **Controleren**.
10. Klik op **Vereffeningsgegevens**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
