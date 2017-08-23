--- 
title: Verkoopovereenkomsten afhandelen
description: Deze procedure toont hoe u een verkoopovereenkomst vervult door er verkooporders aan te koppelen.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4e6c597446c16b73846ee84636d2517f09620f36
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="fulfill-sales-agreements"></a>Verkoopovereenkomsten afhandelen

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe u een verkoopovereenkomst vervult door er verkooporders aan te koppelen. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens. Voordat u deze handleiding start, moet u ervoor zorgen u een effectieve verkoopovereenkomst van het type 'Toezegging productwaarde' hebt. Anders kunt u de taakhandleiding met de naam 'Verkoopovereenkomsten maken' uitvoeren.  




## <a name="release-a-sales-order-from-the-agreement"></a>Een verkooporder uit de overeenkomst vrijgeven
1. Ga naar Verkoop en marketing > Verkoopovereenkomsten > Verkoopovereenkomsten.
2. Open in de lijst de overeenkomst waarvoor u de order wilt vrijgeven.
3. Klik in het actievenster op Verkoopovereenkomst.
4. Klik op Vrijgaveorder.
    * Zoals de tekst bovenaan de pagina Vrijgaveorder maken aangeeft, verschillen de details die vereist zijn voor de verkooporderregels, afhankelijk van of de overeenkomst is gebaseerd op hoeveelheid of waarde.  
    * De overeenkomst in deze handleiding is van het type 'Toezegging productwaarde'. Daarom is de sectie Regels van deze pagina leeg. Als de toezegging was gebaseerd op hoeveelheid, zou de regelinformatie vanuit de overeenkomst worden gekopieerd.  
5. Klik op Maken.
    * Het bericht meldt u dat er nu een verkooporder is gemaakt. Omdat de order geen regels bevat, moet u orderregeldetails toevoegen om het vrijgaveproces te voltooien.   
6. Sluit de pagina.
7. Sluit de pagina.
8. Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.
9. Zoek in de lijst en open de order die werd gemaakt als resultaat van de ordervrijgave in de vorige taak.
10. Klik op Regel toevoegen.
11. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
12. Typ of selecteer in het veld Artikelnummer het artikel dat is opgegeven in de gekoppelde verkoopovereenkomst.
13. Voer in het veld Hoeveelheid een getal in.
    * Zorg ervoor dat u een hoeveelheid invoert die het Nettobedrag onder de waarde van de gekoppelde verkoopovereenkomst brengt.  
    * Omdat de verkooporder aan de overeenkomst is gekoppeld, wordt het overeengekomen kortingspercentage op de orderregel toegepast.  
14. Klik op Regel bijwerken.
15. Klik op Gekoppeld.
    * De pagina Bijgevoegde overeenkomst toont de id en voorwaarden van de overeenkomst waarvan de regel worden vrijgegeven.  
16. Sluit de pagina.
17. Klik in het actievenster op Algemeen.
18. Klik op Gekoppelde verkoopovereenkomst.
19. Vouw de sectie Regeldetails uit.
20. Klik op het tabblad Vervulling.
    * Het tabblad Vervulling geeft een overzicht van alle verkooporderregels die aan deze toezegging zijn gekoppeld en hun vervullingsstatus, het bedrag dat of de hoeveelheid die nog niet is vrijgegeven.   
21. Sluit de pagina.
22. Sluit de pagina.
23. Sluit de pagina.

## <a name="apply-sales-agreement-in-the-order-process"></a>Een verkoopovereenkomst toepassen in het orderproces
1. Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.
2. Klik op Nieuw.
3. Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek in de lijst en selecteer de klant die op de verkoopovereenkomst wordt opgegeven.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Vouw de sectie Algemeen uit.
7. Klik in het veld Verkoopovereenkomst-id op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik op Ja.
10. Klik op OK.
11. Markeer in de lijst de geselecteerde rij.
12. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
13. Typ of selecteer in het veld Artikelnummer het artikel dat is opgegeven in de gekoppelde verkoopovereenkomst.
14. Klik in de lijst op de koppeling in de geselecteerde rij.
15. Klik op Opslaan.
16. Klik in het actievenster op Verzamelen en inpakken.
17. Klik op Pakbon boeken.
18. Vouw de sectie Parameters uit.
19. Selecteer Ja in het veld Boeking.
20. Klik op OK.
21. Klik op OK.
22. Klik in het actievenster op Algemeen.
23. Klik op Gekoppelde verkoopovereenkomst.
24. Klik op het tabblad Vervulling.


