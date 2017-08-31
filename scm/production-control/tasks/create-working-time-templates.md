--- 
title: Werktijdsjablonen maken
description: "Werktijdsjablonen de definiëren de werkuren door een week en worden gebruikt om werktijden voor een periode te genereren."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ff1978f127a014e75619a4bbbb9b6ff3a3ad7c7a
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-working-time-templates"></a>Werktijdsjablonen maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Werktijdsjablonen de definiëren de werkuren door een week en worden gebruikt om werktijden voor een periode te genereren. Deze procedure toont hoe u een werktijdsjabloon bepaalt met behulp van eigenschappen van werktijdplanningen om werktijdsintervallen te categoriseren. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.

1. Ga naar Alle werkruimten > Levenscyclusbeheer bron.
2. Klik op Werktijdsjablonen.

## <a name="create-working-time-template"></a>Werktijdsjabloon maken
1. Klik op Nieuw.
2. Typ een waarde in het veld Werktijdsjabloon.
3. Typ een waarde in het veld Naam.
4. Vouw de sectie Maandag uit.
5. Klik op Toevoegen.
6. Voer in het veld Van een tijd in.
    * Geef de tijd op waarop het werk 's ochtends begint.  
7. Voer in het veld Tot een tijd in.
    * Geef de tijd op waarop medewerkers lunchpauze hebben.  
8. Klik op Toevoegen.
9. Voer in het veld Van een tijd in.
    * Geef de tijd op waarop het werk na de lunch hervat.  
10. Voer in het veld Tot een tijd in.
    * Geef het einde van de werkdag op.  

## <a name="replicate-working-times-to-all-week-days"></a>Werktijden repliceren naar alle weekdagen
1. Klik op Dag kopiëren.
    * Kopieer de definities van werktijden van maandag naar dinsdag.  
2. Klik op OK.
3. Klik op Dag kopiëren.
    * Kopieer de definities van werktijden van maandag naar woensdag.  
4. Selecteer een optie in het veld Tot weekdag.
5. Klik op OK.
6. Klik op Dag kopiëren.
    * Kopieer de definities van werktijden van maandag naar donderdag.  
7. Selecteer een optie in het veld Tot weekdag.
8. Klik op OK.
9. Klik op Dag kopiëren.
    * Kopieer de definities van werktijden van maandag naar vrijdag.  
10. Selecteer een optie in het veld Tot weekdag.
11. Klik op OK.

## <a name="define-time-slots-for-special-operations"></a>Tijdsleuven voor specifieke acties definiëren
1. Vouw de sectie Vrijdag uit.
2. Zoek en selecteer de gewenste record in de lijst.
3. Typ of selecteer een waarde in het veld Eigenschap.
4. Zoek en selecteer de gewenste record in de lijst.
5. Typ of selecteer een waarde in het veld Eigenschap.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Weekenddagen markeren als Gesloten voor ophalen
1. Vouw de sectie Zaterdag uit.
2. Selecteer Ja in het veld Gesloten voor ophalen.
3. Vouw de sectie Zondag uit.
4. Selecteer Ja in het veld Gesloten voor ophalen.


