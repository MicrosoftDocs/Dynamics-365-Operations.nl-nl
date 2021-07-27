---
title: Onderhoudsstatus
description: In dit onderwerp wordt uitgelegd hoe u de onderhoudsstatus berekent in Activabeheer.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1b0c8b6a81fd863d66ca01689262f0ec08a94d76
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354971"
---
# <a name="maintenance-status"></a>Onderhoudsstatus

[!include [banner](../../includes/banner.md)]

 

In Activabeheer kunt u een berekening uitvoeren om een overzicht weer te geven voor een specifieke periode van nieuwe, actieve en voltooide onderhoudsverzoeken, werkorders en activiteiten voor uitvaltijd voor onderhoud. U kunt ook het aantal voltooide evaluaties van voorwaarden voor dezelfde periode weergeven. Gebruik deze berekening om een overzicht te krijgen van de werkbelasting voor inkomende en voltooide onderhoudsverzoeken en werkorders.

## <a name="make-a-maintenance-status-calculation"></a>Een berekening van de onderhoudsstatus uitvoeren

1. Klik op **Activabeheer** > **Query's** > **Onderhoudsstatus**.

2. Selecteer in het dialoogvenster **Status berekenen** in de velden **Begindatum** en **Einddatum** het periodebereik waarvoor u de berekening wilt uitvoeren.

3. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor onderhoud moeten zijn met betrekking tot functionele locaties. 

  Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle onderhoudsregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kan de status op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. 
  
  Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle regels voor onderhoud weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

4. Klik op **OK** om de berekening te starten.

5. Klik op de knoppen **Groeperen op** om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen **Groeperen op** worden gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

6. Klik op de knop **Bijwerken** om de berekening telkens bij te werken wanneer u wijzigingen aanbrengt door knoppen **Groeperen op** te activeren of te deactiveren of door een berekening voor een nieuwe periode uit te voeren.

7. Klik op **Status** als u een nieuwe berekening van de onderhoudsstatus wilt uitvoeren.

>[!NOTE]
>De weergegeven resultaten in **Onderhoudsstatus** omvatten alleen onderhoudsverzoeken en werkorders met een werkelijke begindatum en -tijd. De einddatum en -tijd kunnen leeg zijn.

## <a name="example-1"></a>Voorbeeld 1

In de volgende afbeelding zijn de knoppen **Jaar** en **Maand** geactiveerd. Als deze opties voor **Groeperen op** zijn geselecteerd, krijgt u een algemeen overzicht op maandelijkse basis van de werkbelasting en doorvoer met betrekking tot onderhoudsverzoeken en werkorders. 

![Voorbeeld van maandelijkse werkbelasting.](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Voorbeeld 2

In de volgende afbeelding is informatie over functionele locaties toegevoegd. Nu is het mogelijk om de werkbelasting en doorvoer te vergelijken tussen verschillende functionele locaties, die geografische locaties, fabrieken of werkgebieden kunnen voorstellen. 

![Voorbeeld van maandelijkse werkbelasting met functionele locaties.](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]