---
title: Artikelprognose berekenen
description: In dit onderwerp wordt uitgelegd hoe u een artikelprognose berekent in Activabeheer.
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
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886765"
---
# <a name="calculate-item-forecast"></a>Artikelprognose berekenen

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Net zoals u de capaciteitsbelasting kunt berekenen, zoals in de vorige sectie is beschreven, kunt u ook artikelprognoses berekenen voor

- Onderhoudsschemaregels  
- Werkorders die nog niet zijn gepland  
- Geplande werkorders

Dit is handig als u een overzicht wilt weergeven van het verwachte artikelverbruik (reserveonderdelen en andere artikelen die nodig zijn voor het voltooien van werkorders) gedurende een bepaalde periode. De berekening van een artikelprognose kan worden uitgevoerd voor alle activa of geselecteerde activa. U kunt ook een berekening uitvoeren voor een activiteit voor uitvaltijd voor onderhoud activiteit (**Alle activiteiten voor uitvaltijd voor onderhoud** of **Actieve activiteiten voor uitvaltijd voor onderhoud**) of een werkordergroep (**Alle werkordergroepen** of **Actieve werkordergroepen**).

1. Klik op **Activabeheer** > **Query's** > **Artikelprognose** of **Activabeheer** > **Algemeen** > **Werkordergroepen** > **Alle werkordergroepen** / **Actieve werkordergroepen** > selecteer de werkordergroep in de lijst > de knop **Artikelprognose** of **Activabeheer** > **Algemeen** > **Activiteiten voor uitvaltijd voor onderhoud** > **Alle activiteiten voor uitvaltijd voor onderhoud** / **Actieve activiteiten voor uitvaltijd voor onderhoud** > selecteer de activiteit voor uitvaltijd voor onderhoud in de lijst > de knop **Artikelprognose**.

2. Selecteer in het dialoogvenster **Artikelprognose berekenen** een periode voor de berekening in de velden **Begindatum/-tijd** en **Einddatum/-tijd**.

3. Selecteer Ja voor de wisselknop **Onderhoudsschema opnemen** als u onderhoudsschemaregels wilt opnemen in de prognoseberekening.

4. Selecteer Ja voor de wisselknop **Werkorder opnemen** als u werkordertaken wilt opnemen in de prognoseberekening.

5. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de prognoseregels moeten zijn met betrekking tot functionele locaties. Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle onderhoudsschemaregels en werkorders voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle onderhoudsschemaregels en alle werkorders weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

6. Klik op **OK** om de berekening te starten.

7. Klik in de actievenstergroepen **Groeperen op** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen in de actieschermgroep zijn in een blauwe kleur gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

8. Klik op de knop **Dimensies weergeven** als u de product-, opslag- of traceringsdimensies wilt weergeven die betrekking hebben op de artikelen. Schakel de relevante selectievakjes in en klik op **OK**.

De volgende afbeelding toont een schermafbeelding van de interface.

![Figuur 1](media/02-capacity-planning.png)
