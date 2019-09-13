---
title: Kosten- en datumcontrole
description: In dit onderwerp worden kosten- en datumcontrole in Activabeheer uitgelegd.
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
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918390"
---
# <a name="cost-and-date-control"></a>Kosten- en datumcontrole

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In Activabeheer kunt u kosten berekenen om een overzicht te krijgen van de werkelijke kosten ten opzichte van budgetkosten voor activa, functionele locaties en werkorders. Werkelijke kosten worden gebaseerd op geboekte transacties. U kunt ook een datumberekening maken als u geplande begin- en einddatums wilt vergelijken met de werkelijke begin- en einddatums van werkorders.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Kostenbeheer voor activa, functionele locaties en werkorders

De berekeningen voor activa, functionele locaties en werkorders zijn bijna identiek. Het enige verschil is dat u voor activa en functionele locaties ook subactiva en sublocaties kunt opnemen in de berekening. De datum is de transactiedatum waarop de registratie is vastgelegd.

1. Klik op **Activabeheer** > **Query's** > **Activa** > **Kostenbeheer activa**, **Kostenbeheer voor functionele locatie** of **Activabeheer** > **Query's** > **Werkorders** > **Kostenbeheer voor werkorder**.

2. Selecteer in het dialoogvenster **Kostenbeheer activa** / **Kostenbeheer voor functionele locatie** / **Kostenbeheer voor werkorder** een periode die moet worden berekend.

3. Selecteer zo nodig een financiële-dimensieset die in de berekening moet worden opgenomen.

4. Selecteer Ja voor de wisselknop **Nul overslaan** als u geen resultaten wilt weergeven met nul kosten.

5. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor kostencontrole moeten zijn met betrekking tot functionele locaties. Als u bijvoorbeeld het getal 1 invoegt in het veld en u een hiërarchie met meerdere niveaus voor functionele locaties hebt, worden alle kostenbeheerregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle kostenbeheerregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

6. Selecteer Ja voor de wisselknop **Openstaande toegezegde kosten weergeven** als u die kolom wilt opnemen in de berekening.

7. Selecteer Ja voor de wisselknop **Subactiva opnemen** om kosten gerelateerd aan subactiva als afzonderlijke regels weer te geven.

8. Als u de zoekopdracht wilt beperken, kunt u specifieke activa/functionele locaties/werkorders selecteren op het sneltabblad **Op te nemen records**.

9. Klik op **OK** om de berekening te starten.

In de volgende afbeelding ziet u een voorbeeld van het dialoogvenster **Kostenbeheer activa**.

![Figuur 1](media/01-controlling-and-reporting.png)

10. Klik in de actievenstergroepen **Groeperen op** op de pagina **Kostenbeheer activa** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen in het actievenster zijn gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

In de volgende afbeelding ziet u een voorbeeld van berekeningsresultaten in **Kostenbeheer activa**.

![Figuur 2](media/02-controlling-and-reporting.png)

U kunt kosten ook berekenen door meerdere activa te selecteren in **Alle activa** of **Actieve activa**. Vervolgens klikt u op de knop **Kostenbeheer** op het tabblad **Algemeen**. In het dialoogvenster **Kostenbeheer activa** worden de geselecteerde activa automatisch ingevoegd in het veld **Activum** op het sneltabblad **Op te nemen records**. Klik op **OK** om een kostenberekening voor de geselecteerde activa weer te geven. Dezelfde procedure kan worden uitgevoerd voor functionele locaties in **Alle functionele locaties** of **Actieve functionele locaties** en voor werkorders in **Alle werkorders** of **Actieve werkorders**.

>[!NOTE]
>In het veld **Oorspronkelijk budget** worden budgetkosten uit de werkorderprognose weergegeven. In het veld **Toegezegde kosten** wordt het totale bedrag weergegeven van de onkosten die de rechtspersoon zelf heeft toegezegd te betalen. Het veld **Openstaande toegezegde kosten** bevat de toezeggingen die moeten worden betaald voor artikelen, uren en services die u hebt besteld of ontvangen, maar nog niet hebt betaald. Wanneer alle verbruiksregistraties zijn geboekt, worden de gerelateerde kosten in het veld **Werkelijke kosten** opgenomen.

## <a name="work-order-date-control"></a>Datumbeheer werkorder

Gebruik deze pagina om een overzicht te krijgen van verwachte begin- en einddatums in vergelijking met de werkelijke begin- en einddatums van werkorders.

1. Klik op **Activabeheer** > **Query's** > **Werkorders** > **Datumbeheer werkorder**.

2. Klik op **Berekenen**.

3. Selecteer een functionele locatie in het veld **Functionele locatie**.

4. Voeg in de velden **Begindatum** en **Einddatum** de periode in waarvoor u de berekening wilt uitvoeren. Alle werkorders met een verwachte begindatum in de periode worden opgenomen.

5. Klik op **OK**.

6. Klik in de actievenstergroepen **Groeperen op** op de relevante knoppen om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen in het actievenster zijn gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

In de volgende afbeelding ziet u een voorbeeld van berekeningsresultaten in **Datumbeheer werkorder**.

![Figuur 3](media/03-controlling-and-reporting.png)

- Het veld **Gemiddelde beginvertraging** geeft het verschil in dagen aan tussen de geplande begindatum voor een werkorder vergeleken met de werkelijke begindatum. Als de werkelijke begindatum bijvoorbeeld twee dagen vóór de geplande begindatum valt, wordt in dit veld de waarde -2 weergegeven.  
- Het veld **Gemiddelde eindvertraging** geeft het verschil in dagen aan tussen de geplande einddatum voor een werkorder vergeleken met de werkelijke einddatum. Als de werkelijke einddatum bijvoorbeeld drie dagen na de geplande einddatum valt, wordt in dit veld de waarde 3 weergegeven.  
- In de velden **Voorvallen** wordt aangegeven hoe vaak afwijkingen plaatsvinden ten aanzien van de geplande en werkelijke begindatum en geplande en werkelijke einddatum van de werkorder.

