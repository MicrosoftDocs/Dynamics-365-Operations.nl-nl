--- 
title: Facturen en hoofdgegevens controleren in leveranciers
description: Wanneer u een factuur ontvangt van een leverancier voor goederen of services op een inkooporder, hanteert het bedrijf misschien een beleid waarbij de goederen of services moeten zijn ontvangen voordat de factuur kan worden goedgekeurd voor betaling.
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5cd9448c95b7ec0c4a82aca3d21d961259dfb109
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Facturen en hoofdgegevens controleren in leveranciers

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


