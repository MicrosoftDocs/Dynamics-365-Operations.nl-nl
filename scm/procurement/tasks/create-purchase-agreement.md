--- 
title: Een inkoopovereenkomst maken
description: Deze procedure begeleidt u door het maken van een inkoopovereenkomst.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 22a252d98da5415f50a1d6ffb28f57aae19b5d14
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-agreement"></a>Een inkoopovereenkomst maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure begeleidt u door het maken van een inkoopovereenkomst. Dit wordt gewoonlijk gedaan door een inkoopmanager. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens. U moet de classificaties van inkoopovereenkomsten hebben ingesteld voordat u begint. Nadat u een overeenkomst hebt gemaakt, kunt u deze gebruiken wanneer u een inkooporder maakt. De voorwaarden van de inkoopovereenkomst worden dan gekopieerd naar de koptekst en naar regels in de order die door de overeenkomst worden beïnvloed.


## <a name="create-a-new-purchase-agreement"></a>Een nieuwe inkoopovereenkomst maken
1. Ga naar Inkoop en sourcing > Inkoopovereenkomsten > Inkoopovereenkomsten.
2. Klik op Nieuw.
3. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik in het veld Classificatie van inkoopovereenkomst op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer de gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Vouw de sectie Algemeen uit.
10. Voer een datum in het veld Vervaldatum in.
    * Deze vervaldatum wordt de standaardwaarde voor alle toezeggingsregels zijn en bepaalt hoe lang elke specifieke toezegging geldig is.  
11. Typ in het veld Documenttitel een naam voor uw inkoopovereenkomst.
    * Laat het veld Standaardtoezegging ingesteld op Toezegging producthoeveelheid (of wijzig het als het hier niet op is ingesteld).  
    * De waarde van de standaardtoezegging bepaalt uw opties op de overeenkomstregels. Als u een nieuw toezeggingstype nodig hebt wanneer u de overeenkomstregels maakt, moet u de standaardtoezegging in de koptekst wijzigen.  Er zijn 4 typen toezeggingen: Toezegging producthoeveelheid - voor een bepaalde hoeveelheid van een product; Toezegging productwaarde - voor een specifiek valutabedrag van een product; Waardetoezegging productcategorie - voor een specifiek valutabedrag in een aanschaffingscategorie waar het bedrag voor een catalogusartikel of een niet-catalogus artikel kan zijn; Waardetoezegging - voor een specifiek valutabedrag dat kan worden afgehandeld door elk product of elke aanschaffingscategorie.  
12. Klik op OK.

## <a name="add-a-commitment"></a>Een toezegging toevoegen
1. Klik op Regel toevoegen.
2. Markeer in de lijst de geselecteerde rij.
3. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer het product waarvoor u een toezegging wilt toevoegen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Voer in het veld Hoeveelheid een getal in.
    * Dit is de totale hoeveelheid die u bent overeengekomen te kopen van uw leverancier.  
7. Voer in het veld Eenheidsprijs een getal in.
8. Vouw de sectie Regeldetails uit.
9. Stel de optie Max is afgedwongen in op Ja.
    * De optie Max is afgedwongen beperkt het gebruik van de toezegging. U kunt slechts maximaal de hoeveelheid kopen die is opgegeven in het veld Hoeveelheid voor de regel.  
10. Vouw de sectie Regeldetails uit.

## <a name="add-header-conditions"></a>Koptekstvoorwaarden toevoegen
1. Klik in het actievenster op Opties.
2. Klik op Weergave wijzigen.
3. Klik op Weergave kopteksten.
4. Vouw de sectie Voorwaarden uit.
5. Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De betalingsvoorwaarden van de leverancierrekening worden hier standaard weergegeven.       
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld Leveringsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Klik in het veld Levering op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="confirm-and-activate-the-agreement"></a>De verkoopovereenkomst bevestigen en activeren
1. Klik in het actievenster op Inkoopovereenkomst.
2. Klik op Bevestiging.
    * Stel de optie Overeenkomst als effectief markeren in op Ja.  
3. Klik op OK.
4. Klik in het actievenster op Inkoopovereenkomst.
5. Klik op Bevestigingen van inkoopovereenkomst.
    * Met de optie Voorbeeld/afdrukken kunt u een document voor de inkoopovereenkomst genereren dat u vervolgens kunt afdrukken of naar de leverancier kunt verzenden. Als u de overeenkomst later wilt bijwerken en opnieuw wilt bevestigen, worden hier beide versies weergegeven.  
6. Sluit de pagina.

