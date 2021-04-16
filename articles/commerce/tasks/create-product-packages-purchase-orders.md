---
title: " Productpakketten voor inkooporders maken"
description: Deze procedure doorloopt het maken van een productpakket en het gebruik ervan in een inkooporder.
author: josaw1
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c84c829ca1344d70dee294da35b659299d6fa37
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802714"
---
# <a name="create-product-packages-for-purchase-orders"></a> Productpakketten voor inkooporders maken

[!include [banner](../includes/banner.md)]

Deze procedure doorloopt het maken van een productpakket en het gebruik ervan in een inkooporder. De inkooporder wordt gebruikt om een order te maken voor een vooraf gedefinieerde set producten. Deze procedure gebruikt het demobedrijf USRT.


## <a name="create-a-product-package"></a>Een productpakket maken
1. Ga naar Retail en Commerce > Voorraadbeheer > Aanvulling > Productpakketten.
2. Klik op Nieuw.
3. Typ een waarde in het veld Pakketnummer.
4. Typ een waarde in het veld Omschrijving.
5. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik op Toevoegen.
8. Typ '0160' in het veld Artikelnummer.
9. Klik in het veld Grootte op de vervolgkeuzeknop om de zoekopdracht te openen.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Voer in het veld Hoeveelheid een getal in.
12. Klik op Toevoegen.
13. Typ '0160' in het veld Artikelnummer.
14. Klik in het veld Variantnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
15. Klik in de lijst op de koppeling in de geselecteerde rij.
16. Voer in het veld Hoeveelheid een getal in.
17. Klik op Toevoegen.
18. Typ '0175' in het veld Artikelnummer.
19. Voer in het veld Hoeveelheid een getal in.
20. Klik op Opslaan.
21. Sluit de pagina.

## <a name="add-package-to-purchase-order"></a>Pakket toevoegen aan inkooporder
1. Ga naar Leveranciers > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer in de lijst dezelfde leverancier voor wie het productpakket eerder is gemaakt, als er een leverancier was geselecteerd.
5. Schakel de uitbreiding van de sectie Algemeen om.
6. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Klik op OK.
11. Schakel de uitbreiding van de sectie Regeldetails om.
12. Klik op het tabblad Productpakketten.
13. Klik op Inkooporderregel.
14. Klik op Regels maken op basis van verpakking.
15. Zoek en selecteer in de lijst het productpakket dat in de vorige stap is gemaakt.
16. Voer een getal in het veld Hoeveelheid in.
17. Klik op Maken.
18. Klik op Opslaan.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]