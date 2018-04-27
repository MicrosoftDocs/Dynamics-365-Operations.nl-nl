--- 
title: Factuurgegevens invoeren in leveranciers met behulp van een leveranciersfactuur
description: Deze taakbegeleider helpt u een leveranciersfactuur van een inkooporder te maken en de resultaten van het afstemmen van inkooporder, ontvangstbon en factuur (3-weg afstemming) weer te geven.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 48535a283cbdfdc7343a20105b139c527cac85f4
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-a-vendor-invoice"></a>Factuurgegevens invoeren in leveranciers met behulp van een leveranciersfactuur

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleider helpt u een leveranciersfactuur van een inkooporder te maken en de resultaten van het afstemmen van inkooporder, ontvangstbon en factuur (3-weg afstemming) weer te geven.


## <a name="create-a-purchase-order"></a>Inkooporder maken
1. Ga naar Leveranciers > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek een leverancier om te selecteren. Bijvoorbeeld, blader omlaag naar US-104.
5. Selecteer leverancier US-104.
6. Klik op OK.
7. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Selecteer een voorraadartikel. Selecteer voor dit voorbeeld artikelnummer 1000.
9. Vouw de sectie Regeldetails uit of samen.
10. Klik op het tabblad Instellingen.
    * U kunt het afstemmingsbeleid negeren om geen afstemming, tweeweg-afstemming of drieweg-afstemming te gebruiken.  
11. Vouw de sectie Regeldetails uit of samen.
12. Klik in het actievenster op Inkoop.
13. Klik op Bevestigen.

## <a name="receive-the-products"></a>De producten ontvangen
1. Klik in het actievenster op Ontvangen.
2. Klik op Productontvangstbon.
3. Voer in het veld Productontvangstbon het nummer van de productontvangstbon in. Voer bijvoorbeeld PR123 in.
4. Klik op OK om de productontvangstbon te boeken.
5. Sluit de pagina.

## <a name="create-a-vendor-invoice"></a>Een leveranciersfactuur maken
1. Ga naar Leveranciers > Inkooporders > Inkooporders ontvangen maar niet gefactureerd.
2. Selecteer de inkooporder die is gemaakt.
3. Klik in het actievenster op Factuur.
4. Klik op Factuur.
5. Voer in het veld Nummer het factuurnummer in.
6. Typ een waarde in het veld Factuuromschrijving.
7. Voer een datum in het veld Factuurdatum in.
8. Voer 1200 in het veld Eenheidsprijs in.
9. Klik op Regel toevoegen.
10. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Zoek in de lijst het artikelnummer van de installatietoeslag. Bijvoorbeeld S0001
12. Selecteer het artikelnummer van de installatietoeslag.
    * Merk op dat geen afstemming is uitgevoerd sinds u de wijzigingen hebt aangebracht.  
13. Klik op Vereffeningsstatus bijwerken.
14. Klik in het actievenster op Controleren.
15. Klik op Vereffeningsgegevens.
    * De nieuwe regel met services hoeft niet te worden afgestemd zodat de status "Niet uitgevoerd" blijft.  
16. Selecteer de productontvangstbon voor het voorraadartikel dat u hebt ontvangen.
    * De regel met de productontvangstbon is afgestemd maar de hoeveelheid of prijs komt niet overeen, waardoor de afstemming mislukt.  
17. Voer in het veld Eenheidsprijs een getal in.
    * Nu de eenheidsprijs overeenkomt, wordt de status gewijzigd in Geslaagd. Als uw beleid verschillen toestaat of als afstemmen alleen een waarschuwing is, kunt u de factuur toch boeken.  
18. Sluit de pagina.
19. Klik op Boeken.
20. Het formulier sluiten.
    * Merk op dat de inkooporder niet meer wordt weergegeven als ontvangen maar als niet gefactureerd.  


