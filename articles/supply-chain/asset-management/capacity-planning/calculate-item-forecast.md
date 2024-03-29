---
title: Artikelprognose berekenen
description: In dit artikel wordt uitgelegd hoe u een artikelprognose berekent in Activabeheer.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25e9b00533fb183b27c1bbe616cf6f414b44b5e7
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016096"
---
# <a name="calculate-item-forecast"></a>Artikelprognose berekenen

[!include [banner](../../includes/banner.md)]

 

Net zoals u de capaciteitsbelasting kunt berekenen, zoals in de vorige sectie is beschreven, kunt u ook artikelprognoses berekenen voor:

- onderhoudsschemaregels  
- werkorders die nog niet zijn gepland  
- geplande werkorders

Dit is handig als u een overzicht wilt weergeven van het verwachte artikelverbruik (reserveonderdelen en andere artikelen die nodig zijn voor het voltooien van werkorders) gedurende een bepaalde periode. De berekening van een artikelprognose kan worden uitgevoerd voor alle activa of geselecteerde activa. U kunt ook een berekening uitvoeren voor een activiteit voor uitvaltijd voor onderhoud activiteit (**Alle activiteiten voor uitvaltijd voor onderhoud** of **Actieve activiteiten voor uitvaltijd voor onderhoud**) of een werkordergroep (**Alle werkordergroepen** of **Actieve werkordergroepen**).

1. Klik op **Activabeheer** > **Query's** > **Artikelprognose** of **Activabeheer** > **Werkordergroepen** > **Alle werkordergroepen** / **Actieve werkordergroepen** > selecteer de werkordergroep in de lijst > de knop **Artikelprognose** of **Activabeheer** > **Activiteiten voor uitvaltijd voor onderhoud** > **Alle activiteiten voor uitvaltijd voor onderhoud** / **Actieve activiteiten voor uitvaltijd voor onderhoud** > selecteer de activiteit voor uitvaltijd voor onderhoud in de lijst > de knop **Artikelprognose**.

2. Selecteer in het dialoogvenster **Artikelprognose berekenen** een periode voor de berekening in de velden **Begindatum/-tijd** en **Einddatum/-tijd**.

3. Selecteer Ja voor de wisselknop **Onderhoudsschema opnemen** als u onderhoudsschemaregels wilt opnemen in de prognoseberekening.

4. Selecteer Ja voor de wisselknop **Werkorder opnemen** als u werkordertaken wilt opnemen in de prognoseberekening.

5. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de prognoseregels moeten zijn met betrekking tot functionele locaties. 

      Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle onderhoudsschemaregels en werkorders voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. 
  
      Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle onderhoudsschemaregels en alle werkorders weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

6. Klik op **OK** om de berekening te starten.

7. Klik in de groepen **Groeperen op...** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven. In de onderstaande schermopname worden de geselecteerde knoppen **Groeperen op** in blauwe kleur gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

8. Klik op de knop **Dimensies weergeven** als u de product-, opslag- of traceringsdimensies wilt weergeven die betrekking hebben op de artikelen. Schakel de relevante selectievakjes in en klik op **OK**.

![Figuur 1.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]