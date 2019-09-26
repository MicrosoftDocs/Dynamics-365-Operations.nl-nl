---
title: Capaciteitsbelasting berekenen
description: In dit onderwerp wordt uitgelegd hoe u de capaciteitsbelasting berekent in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: c6d15861492a46ddb1222db2210f8c751ed38cb3
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886788"
---
# <a name="calculate-capacity-load"></a>Capaciteitsbelasting berekenen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In Activabeheer kunt u de capaciteitsbelasting berekenen voor

- onderhoudsschemaregels  
- werkorders die nog niet zijn gepland  
- geplande werkorders

Dit is handig als u een overzicht wilt weergeven van de verwachte capaciteitsbelasting voor een bepaalde periode. De berekening van de capaciteitsbelasting kan worden uitgevoerd voor alle activa of geselecteerde activa. U kunt ook een berekening uitvoeren voor activiteiten voor uitvaltijd of werkordergroepen.

1. Klik op **Activabeheer** > **Query's** > **Capaciteitsbelasting** of **Activabeheer** > **Algemeen** > **Werkordergroepen** > **Alle werkordergroepen** / **Actieve werkordergroepen** > selecteer de werkordergroep in de lijst > de knop **Capaciteitsbelasting** of **Activabeheer** > **Algemeen** > **Activiteiten voor uitvaltijd voor onderhoud** > **Alle activiteiten voor uitvaltijd voor onderhoud** / **Actieve activiteiten voor uitvaltijd voor onderhoud** > selecteer de activiteit voor uitvaltijd voor onderhoud in de lijst > de knop **Capaciteitsbelasting**.

2. Selecteer in het dialoogvenster **Capaciteitsbelasting berekenen** een periode voor de berekening in de velden **Begindatum/-tijd** en **Einddatum/-tijd**.

3. Selecteer Ja voor de wisselknop **Onderhoudsschema opnemen** als u onderhoudsschemaregels wilt opnemen in de berekening.

4. Selecteer Ja voor de wisselknop **Werkorder opnemen** als u werkordertaken wilt opnemen in de berekening.

5. Gebruik het veld **Niveau** om aan te geven hoe gedetailleerd u de capaciteitsbelastingsregels wilt berekenen met betrekking tot functionele locaties. Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle onderhoudsschemaregels en werkorders voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle onderhoudsschemaregels en alle werkorders weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

6. Klik op **OK** om de berekening te starten.

7. Klik in de actievenstergroepen **Groeperen op** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen in de actieschermgroep zijn in een blauwe kleur gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

De volgende afbeelding toont een voorbeeld van de interface.

![Figuur 1](media/01-capacity-planning.png)

>[!NOTE]
>Als u zich alleen wilt richten op capaciteitsplanning voor geplande werkorders, raadpleegt u [Capaciteitsbelasting voor geplande werkorders berekenen](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).
