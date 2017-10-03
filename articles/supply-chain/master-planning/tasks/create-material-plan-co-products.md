--- 
title: Een materiaalplan voor co-producten maken
description: De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4eb36b0de53f40f882950628d55d6ac08ac5fdde
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Een materiaalplan voor co-producten maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.


## <a name="create-requirement-for-a-co-product"></a>Vereiste voor een co-product maken
1. Ga naar Standaarddashboard.
2. Klik op Verkooporderverwerking en -onderzoek.
3. Klik op Nieuw.
4. Klik op Verkooporder.
5. Typ een waarde in het veld Klantrekening.
    * Voorbeeld: US-001  
6. Klik op OK.
7. Typ een waarde in het veld Artikelnummer.
    * Voorbeeld: P6003  
8. Voer in het veld Hoeveelheid een getal in.
    * Voorbeeld: 50000  
9. Klik op Opslaan.

## <a name="create-a-material-plan-for-co-products"></a>Een materiaalplan voor co-producten maken
1. Klik op Hoofdplanning.
2. Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Voorbeeld: Hoofdplan  
4. Klik op Uitvoeren.
5. Vouw de sectie Op te nemen records uit of samen.
6. Klik op Filter.
7. Selecteer in de lijst de rij voor het veld Artikelnummer.
8. Typ een waarde in het veld Criteria.
    * Voorbeeld: P6003  
9. Klik op OK.
10. Klik op OK.
11. Klik op Geplande orders.
12. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".
    * Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.  
13. Markeer in de lijst de geselecteerde rij.
    * Selecteer een van de rijen die door het filter worden geretourneerd.  
14. Klik in de lijst op de koppeling in de geselecteerde rij.
15. Vouw de sectie Tracering van behoefte uit of samen.
16. Klik in de lijst op de koppeling in de geselecteerde rij.
    * De geplande order is getraceerd naar de verkooporder van het co-product.  
17. Sluit de pagina.


