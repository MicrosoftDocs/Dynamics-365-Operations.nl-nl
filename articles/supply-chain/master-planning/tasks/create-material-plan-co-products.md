---
title: Een materiaalplan voor coproducten maken
description: De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: deae0d7e0295aa02f5ad512f67e9e3d2148c2e33
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578291"
---
# <a name="create-a-material-plan-for-co-products"></a>Een materiaalplan voor coproducten maken

[!include [banner](../../includes/banner.md)]

De productieplanner plant de materiaalbehoeften voor artikelen die co-producten van de formule zijn. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USP2.

## <a name="create-requirement-for-a-co-product"></a>Vereiste voor een co-product maken

1. Ga naar **Verkoop en marketing \> Werkgebieden \> Verkooporderverwerking en -onderzoek**.
1. Selecteer **Nieuw**.
1. Selecteer **Verkooporders**.
1. Typ een waarde in het veld **Klantrekening**.
    * Voorbeeld: US-001  
1. Selecteer **OK**.
1. Typ een waarde in het veld **Artikelnummer**.
    * Voorbeeld: P6003  
1. Voer een getal in het veld **Hoeveelheid** in.
    * Voorbeeld: 50000  
1. Selecteer **Opslaan**.

## <a name="create-a-material-plan-for-co-products"></a>Een materiaalplan voor co-producten maken

1. Sluit de pagina.
1. Sluit de pagina.
1. Selecteer **Hoofdplanning**.
1. Selecteer in het veld **Plan** de vervolgkeuzeknop om de zoekopdracht te openen.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
    * Voorbeeld: Hoofdplan  
1. Selecteer **Uitvoeren**.
1. Vouw de sectie **Op te nemen records** uit of samen.
1. Selecteer **Filter**.
1. Selecteer in de lijst de rij voor **Veld** = *Artikelnummer*.
1. Typ een waarde in het veld **Criteria**.
    * Voorbeeld: P6003  
1. Selecteer **OK**.
1. Selecteer **OK**.
1. Selecteer **Geplande orders**.
1. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld **Artikelnummer** op de waarde 'P6000'.
    * Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.  
1. Markeer in de lijst de geselecteerde rij.
    * Selecteer een van de rijen die door het filter worden geretourneerd.  
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
1. Vouw de sectie **Tracering van behoefte** uit.
1. Selecteer in de lijst de koppeling in de geselecteerde rij.
    * De geplande order is getraceerd naar de verkooporder van het co-product.  
1. Sluit de pagina.

## <a name="create-a-second-requirement-for-a-co-product"></a>Een tweede vereiste voor een co-product maken

1. Ga naar **Verkoop en marketing \> Werkgebieden \> Verkooporderverwerking en -onderzoek**.
1. Selecteer **Nieuw**.
1. Selecteer **Verkooporders**.
1. Typ een waarde in het veld **Klantrekening**.
    * Voorbeeld: US-001  
1. Selecteer **OK**.
1. Typ een waarde in het veld **Artikelnummer**.
    * Voorbeeld: P6003  
1. Voer een getal in het veld **Hoeveelheid** in.
    * Voorbeeld: 50000  
1. Selecteer **Opslaan**.

## <a name="create-a-second-material-plan-for-co-products"></a>Een tweede materiaalplan voor co-producten maken

1. Selecteer in het veld **Plan** de vervolgkeuzeknop om de zoekopdracht te openen.
2. Selecteer in de lijst de koppeling in de geselecteerde rij.
    * Voorbeeld: Hoofdplan  
3. Selecteer **Uitvoeren**.
4. Vouw de sectie **Op te nemen records** uit of samen.
5. Selecteer **Filter**.
6. Selecteer in de lijst de rij voor **Veld** = *Artikelnummer*.
7. Typ een waarde in het veld *Criteria*.
    * Voorbeeld: P6003  
8. Selecteer **OK**.
9. Selecteer **OK**.
10. Selecteer **Geplande orders**.
11. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het Veld **Artikelnummer** op de waarde 'P6000'.
    * Filter op het formuleartikel dat een co-product van het artikel bevat waarvoor u een verkooporder hebt gemaakt.  
12. Markeer in de lijst de geselecteerde rij.
    * Selecteer een van de rijen die door het filter worden geretourneerd.  
13. Selecteer in de lijst de koppeling in de geselecteerde rij.
14. Vouw de sectie **Tracering van behoefte** uit of samen.
15. Selecteer in de lijst de koppeling in de geselecteerde rij.
    * De geplande order is getraceerd naar de verkooporder van het co-product.  
16. Sluit de pagina.
17. Selecteer **Hoofdplanning**.
18. Ga naar **Hoofdplanning \> Instellen \> Parameters hoofdplanning**.
19. Selecteer *Nee* in het veld **Alle planningsprocessen uitschakelen**.
20. Sluit de pagina.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]