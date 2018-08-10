--- 
title: Brandstofindex van een vervoerder instellen
description: Deze handleiding geeft aan hoe een regio voor de brandstofindex, een brandstofindex en een index van de vervoerder kan worden gemaakt.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 81f3244ff42cf13cd93ac10656c47f8a9204ef99
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-carrier-fuel-index"></a>Brandstofindex van een vervoerder instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze handleiding geeft aan hoe een regio voor de brandstofindex, een brandstofindex en een index van de vervoerder kan worden gemaakt. De regio van de brandstofindex bepaalt in welke regio de brandstofindex moet worden toegepast en de brandstofindex geeft een brandstofprijs op voor een bepaalde periode. U kunt de wijziging in brandstofprijzen in de loop van de tijd weerspiegelen door meerdere brandstofindexen aan een vervoerder te koppelen.  Deze taken worden gewoonlijk uitgevoerd door een transportcoördinator. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens.


## <a name="create-a-fuel-index-region"></a>Een brandstofindexregio maken
1. Ga naar Transportbeheer > Instellingen > Brandstofindexen > Brandstofindexregio's.
    * Eerst moet u de verschillende regio's maken waar u verschillende brandstoftoeslagen hanteert en berekent.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Regio.
4. Typ een waarde in het veld Naam.
5. Klik op Opslaan.

## <a name="create-a-fuel-index"></a>Maak een brandstofindex
1. Ga naar Transportbeheer > Instellingen > Brandstofindexen > Brandstofindexen.
    * Voor de regio's die u hebt ingesteld moet u de huidige prijzen voor de brandstof invoeren.  
2. Klik op Nieuw.
3. Klik in het veld Regio op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Typ een getal in het veld Prijs per gallon.
6. Typ een datum en tijd in het veld Ingangsdatum en -tijd.
7. Klik op Opslaan.

## <a name="create-a-carrier-fuel-index"></a>Een brandstofindex voor de vervoerder maken
1. Ga naar Transportbeheer > Instellingen > Brandstofindexen > Brandstofindexen van vervoerder.
2. Klik op Nieuw.
3. Typ een waarde in het veld Brandstofindex vervoerder.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Nieuw.
6. Typ een datum en tijd in het veld Ingangsdatum en -tijd.
7. Typ een getal in het veld PPL van.
    * In dit voorbeeld kunt u het veld PPL van instellen op 1,95.  
8. Typ een getal in het veld PPL tot.
    * In dit voorbeeld kunt u het veld PPL tot instellen op 2.  
9. Voer een getal in het veld Percentage in.
    * In dit voorbeeld kunt u het percentage instellen op 3.  
10. Klik in het veld Valuta op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Zoek en selecteer de gewenste record in de lijst.
12. Klik in de lijst op de koppeling in de geselecteerde rij.
13. Klik op Opslaan.


