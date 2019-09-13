---
title: Onderhoudsstatus
description: In dit onderwerp wordt uitgelegd hoe u de onderhoudsstatus berekent in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918344"
---
# <a name="maintenance-status"></a>Onderhoudsstatus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In Activabeheer kunt u een berekening uitvoeren om een overzicht weer te geven van nieuwe, actieve en voltooide onderhoudsverzoeken, werkorders en activiteiten voor uitvaltijd voor onderhoud voor een specifieke periode. U kunt ook het aantal voltooide evaluaties van voorwaarden voor dezelfde periode weergeven. Gebruik deze berekening om een overzicht te krijgen van de werkbelasting met betrekking tot inkomende en voltooide onderhoudsverzoeken en werkorders.

## <a name="make-a-maintenance-status-calculation"></a>Een berekening van de onderhoudsstatus uitvoeren

1. Klik op **Activabeheer** > **Query's** > **Onderhoudsstatus**.

2. Selecteer in het dialoogvenster **Status berekenen** in de velden **Begindatum** en **Einddatum** de periode waarvoor u de berekening wilt uitvoeren.

3. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor onderhoud moeten zijn met betrekking tot functionele locaties. Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle onderhoudsregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kan de status op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle regels voor onderhoud weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

4. Klik op **OK** om de berekening te starten.

5. Klik in de actievenstergroepen **Groeperen op** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen in het actievenster zijn gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

6. Klik op de knop **Bijwerken** om de berekening telkens bij te werken wanneer u wijzigingen aanbrengt door knoppen **Groeperen op** te activeren of te deactiveren of door een berekening voor een nieuwe periode uit te voeren.

7. Klik op **Status** als u een nieuwe berekening van de onderhoudsstatus wilt uitvoeren.

>[!NOTE]
>De weergegeven resultaten in **Onderhoudsstatus** omvatten alleen onderhoudsverzoeken en werkorders met een werkelijke begindatum en -tijd. De einddatum en -tijd kunnen leeg zijn.

*Voorbeeld 1:*

In de volgende afbeelding zijn de knoppen **Jaar** en **Maand** geactiveerd. Hier krijgt u een algemeen overzicht op maandelijkse basis van de werkbelasting en doorvoer met betrekking tot onderhoudsverzoeken en werkorders. 

![Figuur 1](media/13-controlling-and-reporting.png)

*Voorbeeld 2:*

In de volgende afbeelding is informatie over functionele locaties toegevoegd. Nu is het mogelijk om de werkbelasting en doorvoer te vergelijken tussen verschillende functionele locaties, die geografische locaties, fabrieken of werkgebieden kunnen voorstellen. 

![Figuur 2](media/14-controlling-and-reporting.png)

