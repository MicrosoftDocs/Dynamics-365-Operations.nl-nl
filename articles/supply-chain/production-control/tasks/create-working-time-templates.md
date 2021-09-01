---
title: Werktijdsjablonen maken
description: Werktijdsjablonen de definiëren de werkuren door een week en worden gebruikt om werktijden voor een periode te genereren.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ef913777c8e2aa14af21e28ed56362e31b3d70a1a52e988a90ad94f59b77b70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741256"
---
# <a name="create-working-time-templates"></a>Werktijdsjablonen maken

[!include [banner](../../includes/banner.md)]

Werktijdsjablonen de definiëren de werkuren door een week en worden gebruikt om werktijden voor een periode te genereren. Deze procedure toont hoe u een werktijdsjabloon bepaalt met behulp van eigenschappen van werktijdplanningen om werktijdsintervallen te categoriseren. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.

1. Ga naar **Werkgebieden > Levenscyclusbeheer bron**.
1. Selecteer **Werktijdsjablonen**.

## <a name="create-working-time-template"></a>Werktijdsjabloon maken

1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Werktijdsjabloon**.
1. Typ een waarde in het veld **Naam**.
1. Vouw de sectie **Maandag** uit.
1. Selecteer **Toevoegen**.
1. Voer in het veld **Van** een tijd in.
    * Geef de tijd op waarop het werk 's ochtends begint.  
1. Voer in het veld **Tot** een tijd in.
    * Geef de tijd op waarop medewerkers lunchpauze hebben.  
1. Selecteer **Toevoegen**.
1. Voer in het veld **Van** een tijd in.
    * Geef de tijd op waarop het werk na de lunch hervat.  
1. Voer in het veld **Tot** een tijd in.
    * Geef het einde van de werkdag op.  

## <a name="replicate-working-times-to-all-week-days"></a>Werktijden repliceren naar alle weekdagen

1. Selecteer **Dag kopiëren**.
    * Kopieer de definities van werktijden van maandag naar dinsdag.  
1. Selecteer **OK**.
1. Selecteer **Dag kopiëren**.
    * Kopieer de definities van werktijden van maandag naar woensdag.  
1. Selecteer een optie in het veld **Tot weekdag**.
1. Selecteer **OK**.
1. Selecteer **Dag kopiëren**.
    * Kopieer de definities van werktijden van maandag naar donderdag.  
1. Selecteer een optie in het veld **Tot weekdag**.
1. Selecteer **OK**.
1. Selecteer **Dag kopiëren**.
    * Kopieer de definities van werktijden van maandag naar vrijdag.  
1. Selecteer een optie in het veld **Tot weekdag**.
1. Selecteer **OK**.

## <a name="define-time-slots-for-special-operations"></a>Tijdsleuven voor specifieke acties definiëren

1. Vouw de sectie **Vrijdag** uit.
1. Zoek en selecteer de gewenste record in de lijst.
1. Typ of selecteer een waarde in het veld **Eigenschap**.
1. Zoek en selecteer de gewenste record in de lijst.
1. Typ of selecteer een waarde in het veld **Eigenschap**.

## <a name="mark-weekend-days-as-closed-for-pickup"></a>Weekenddagen markeren als Gesloten voor ophalen

1. Vouw de sectie **Zaterdag** uit.
1. Selecteer *Ja* in het veld **Gesloten voor ophalen**.
1. Vouw de sectie **Zondag** uit.
1. Selecteer *Ja* in het veld **Gesloten voor ophalen**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]