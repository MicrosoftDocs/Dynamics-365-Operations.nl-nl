---
title: Een materiaalplan voor coproducten maken
description: De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a87935f8f30d909f1a6a62ed7be00c83476a36a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214365"
---
# <a name="create-a-material-plan-for-co-products"></a>Een materiaalplan voor coproducten maken

[!include [banner](../../includes/banner.md)]

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
1. Sluit de pagina.
2. Sluit de pagina.
3. Klik op Hoofdplanning.
4. Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Voorbeeld: Hoofdplan  
6. Klik op Uitvoeren.
7. Vouw de sectie Op te nemen records uit of samen.
8. Klik op Filter.
9. Selecteer in de lijst de rij voor het veld Artikelnummer.
10. Typ een waarde in het veld Criteria.
    * Voorbeeld: P6003  
11. Klik op OK.
12. Klik op OK.
13. Klik op Geplande orders.
14. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".
    * Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.  
15. Markeer in de lijst de geselecteerde rij.
    * Selecteer een van de rijen die door het filter worden geretourneerd.  
16. Klik in de lijst op de koppeling in de geselecteerde rij.
17. Vouw de sectie Tracering van behoefte uit of samen.
18. Klik in de lijst op de koppeling in de geselecteerde rij.
    * De geplande order is getraceerd naar de verkooporder van het co-product.  
19. Sluit de pagina.

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
1. Klik in het veld Plan op de vervolgkeuzeknop om de zoekopdracht te openen.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Voorbeeld: Hoofdplan  
3. Klik op Uitvoeren.
4. Vouw de sectie Op te nemen records uit of samen.
5. Klik op Filter.
6. Selecteer in de lijst de rij voor het veld Artikelnummer.
7. Typ een waarde in het veld Criteria.
    * Voorbeeld: P6003  
8. Klik op OK.
9. Klik op OK.
10. Klik op Geplande orders.
11. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld Artikelnummer met een waarde van "P6000".
    * Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.  
12. Markeer in de lijst de geselecteerde rij.
    * Selecteer een van de rijen die door het filter worden geretourneerd.  
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Vouw de sectie Tracering van behoefte uit of samen.
15. Klik in de lijst op de koppeling in de geselecteerde rij.
    * De geplande order is getraceerd naar de verkooporder van het co-product.  
16. Sluit de pagina.
17. Klik op Hoofdplanning.
18. Ga naar Hoofdplanning > Instellen > Hoofdplanning > Parameters hoofdplanning.
19. Selecteer Nee in het veld Alle planningsprocessen uitschakelen.
20. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]