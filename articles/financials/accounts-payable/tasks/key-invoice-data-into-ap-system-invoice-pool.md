--- 
title: Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep
description: Deze taakhandleiding laat zien hoe u het facturenregister kunt gebruiken om facturen te maken.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakhandleiding laat zien hoe u het facturenregister kunt gebruiken om facturen te maken.  Gebruik vervolgens de facturenpool om de factuur af te stemmen op een inkooporder en de onkosten te finaliseren op de pagina voor leveranciersfacturen.


## <a name="create-a-purchase-order"></a>Inkooporder maken
1. Ga naar Leveranciers > Inkooporders > Inkooporders.
2. Klik op Nieuw om een inkooporder te maken.
3. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer de leverancier in de lijst. Bijvoorbeeld leverancier 1001.
5. Klik op OK.
6. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek het artikelnummer voor services in de lijst. Selecteer bijvoorbeeld S0001.
8. Klik op het artikelnummer en selecteer dit.
    * Het nettobedrag is 75,00.  Dat is het bedrag dat we verwachten op de factuur.  
9. Klik in het actievenster op Inkoop.
10. Klik op Bevestigen.

## <a name="create-and-post-and-invoice"></a>Een factuur maken en boeken
1. Ga naar Leveranciers > Facturen > Facturenregister.
2. Klik op Nieuw.
3. Open de zoekopdracht om de naam te selecteren van het facturenregister dat u wilt gebruiken.
4. Selecteer de naam van het facturenregister dat u wilt gebruiken.
5. Klik op Regels om het register te openen en onkostenregels in te voeren.
6. Selecteer een leverancier in de zoekopdracht. Klik bijvoorbeeld op leverancier 1001.
7. Voer in het veld Factuur het factuurnummer in.
8. Typ een waarde in het veld Omschrijving.
9. Voer een nummer in het veld Credit in.
10. Klik in het veld Inkooporder op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Selecteer de inkooporder die u eerder hebt gemaakt.
12. Klik in het veld Goedgekeurd door op de vervolgkeuzeknop om de zoekopdracht te openen.
13. Markeer een fiatteur en klik op Selecteren om die fiatteur te selecteren.
14. Klik op Boeken.
15. Het formulier sluiten.
16. Het formulier sluiten.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Open een factuur vanuit de pool en vereffen deze met een inkooporder om het factureringsproces te voltooien
1. Ga naar Leveranciers > Facturen > Facturenpool.
2. Klik op Inkooporder om een leveranciersfactuur te maken op basis van de factuur in de pool.
3. Selecteer de factuur die u wilt bekijken.
4. Klik op Vereffeningsstatus bijwerken om de vereffening te voltooien.
5. Klik in het actievenster op Opties.
6. Klik op Weergave wijzigen.
7. Klik op Rasterweergave.
8. Klik op Boeken.
9. Het formulier sluiten.
10. Ga naar Leveranciers > Leveranciers > Leveranciers.
11. Selecteer de leverancier die op de inkooporder staat vermeld. Selecteer bijvoorbeeld leverancier 1001.
12. Klik in de lijst op de koppeling in de geselecteerde rij.
13. Klik in het actievenster op Leverancier.
14. Klik op Transacties.
15. Selecteer de factuur die u hebt gemaakt.
    * De toerekening van het facturenregister is omgekeerd en geboekt naar de juiste onkostenrekening.  


