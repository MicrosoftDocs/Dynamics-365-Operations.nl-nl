--- 
title: Overboekingsactiviteiten maken voor lean manufacturing
description: Maak een overboekingsactiviteit voor lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 010ac08fa96ead49b6ecbbe083e59fb96427e29e
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Overboekingsactiviteiten maken voor lean manufacturing

[!include [task guide banner](../../includes/task-guide-banner.md)]

Maak een overboekingsactiviteit voor lean manufacturing. 

Vereisten: 

1. Een productiestroom en versie die niet actief zijn, moeten worden gemaakt.

2. Het bronmagazijn en het doelmagazijn moeten worden gemaakt. De aanvullende of bijgevulde werkcel moet eventueel worden gemaakt.


## <a name="find-the-production-flow-version"></a>De productiestroomversie vinden
1. Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.
2. Zoek en selecteer de gewenste record in de lijst.
    * De productiestroom moet een versie in conceptstatus hebben.  
3. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="create-a-new-activity"></a>Een nieuwe activiteit maken
1. Klik op Activiteiten.
    * Zorg ervoor dat de geselecteerde productiestroom een versie in concept heeft en selecteer deze versie.  
2. Klik op Nieuwe planactiviteit maken.
3. Klik op Volgende.
4. Typ een waarde in het veld Naam.
5. Selecteer 'Overboeking' in het veld Type activiteit.
6. Voer in het veld Verwerkingshoeveelheid een getal in.
7. Klik op Volgende.

## <a name="select-the-work-cells"></a>De werkcellen selecteren
1. Klik in het veld Aanvullen op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer een werkcel om de uitvoerlocatie van de werkcel te gebruiken als de beginlocatie in een overboekingsactiviteit. Hetzelfde kan met de bijgevulde werkcel worden uitgevoerd, wat de doellocatie van de overboekingsactiviteit instelt.  
2. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="define-the-inventory-updates"></a>De updates van de voorraad definiëren
1. Selecteer een optie in het veld Producttype.
    * Een overboeking wijzigt het type van het product niet. U kunt eindproducten of halffabricaten overboeken (overboeking tussen twee activiteiten van een productiestroom en misschien een kanbanstroom).     Wanneer u klaar bent met het overboeken van producten, kunt u selecteren of orderverzameling of ontvangst resulteert in een voorraadtransactie.  

## <a name="define-the-transfer-locations"></a>De overboekingslocaties definiëren
1. Klik op Volgende.
2. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer het gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Selecteer 'Expediteur' in het veld Bevracht door.
    * Opties omvatten: Expediteur - de organisatie die het magazijn van verzending beheert, Ontvanger - de organisatie die het ontvangende magazijn beheert, Vervoerder - een externe leverancier. Als de operationele organisatie een leverancier is, is voor de overboekingsactiviteit een uitbestedingsovereenkomst vereist.  
8. Klik op Volgende.

## <a name="define-the-activity-times"></a>De activiteitstijden dfiniëren
1. Zoek en selecteer de gewenste record in de lijst.
    * De definitie van Runtime is vereist. Uitvoeringstijd wordt gebruikt om kosten en de doorvoertijden van de kanbantaken te berekenen. Runtimes worden niet gebruikt om capaciteitsbelasting en verbruik te berekenen. Deze wordt berekend door cyclusduur, afgeleid uit de taak van de productiestroomversie.  
2. Voer in het veld Tijd een nummer in.
3. Typ een waarde in het veld Eenheid.
4. Selecteer de tijdseenheid.
5. Voer in het veld Per hoeveelheid een getal in.
6. Zoek en selecteer de gewenste record in de lijst.
    * Wachttijden zijn optioneel.  
7. Voer in het veld Tijd een nummer in.
8. Typ een waarde in het veld Eenheid.
9. Selecteer de tijdseenheid.
10. Voer in het veld Per hoeveelheid een getal in.
11. Klik op Volgende.
12. Klik op Voltooien.
13. Sluit de pagina.


