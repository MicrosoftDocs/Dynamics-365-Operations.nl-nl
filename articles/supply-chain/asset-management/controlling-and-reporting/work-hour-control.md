---
title: Controle van werkuren
description: In dit artikel wordt de controle van werkuren in Activabeheer uitgelegd.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f5f5dbb23c4d6c86bee7612c4ade65ef4b1cee8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869744"
---
# <a name="work-hour-control"></a>Controle van werkuren

[!include [banner](../../includes/banner.md)]

 

In Activabeheer kunt u uren berekenen om een overzicht te krijgen van de werkelijke uren ten opzichte van budgeturen voor activa, functionele locaties of werkorders. Werkelijke uren worden gebaseerd op geboekte transacties.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Controle van werkuren voor activa, functionele locaties en werkorders

De berekeningen voor activa, functionele locaties en werkorders zijn bijna identiek. Het enige verschil is dat u voor activa en functionele locaties ook subactiva en sublocaties kunt opnemen in de berekening. De datum is de transactiedatum waarop de registratie is vastgelegd.

1. Klik op **Activabeheer** > **Query's** > **Activa** > **Uurcontrole activa**, **Uurcontrole voor functionele locatie** of **Activabeheer** > **Query's** > **Werkorders** > **Uurcontrole voor werkorder**.

2. Het betreffende dialoogvenster **Uurcontrole** wordt geopend.

3. Selecteer in het dialoogvenster **Uurcontrole activa** / **Uurcontrole voor functionele locatie** / **Uurcontrole voor werkorder** een periode die moet worden berekend in de velden **Begindatum** en **Einddatum**.

4. Selecteer zo nodig een **financiële-dimensieset** die in de berekening moet worden opgenomen.

5. Selecteer Ja voor de wisselknop **Nul overslaan** als u geen resultaten wilt weergeven met nul uren.

6. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor uurcontrole zijn met betrekking tot functionele locaties. 

    Als u bijvoorbeeld het getal 1 invoegt in het veld en u een hiërarchie met meerdere niveaus voor functionele locaties hebt, worden alle uurcontroleregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel worden opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. 
    
    Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle uurcontroleregels weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

7. Selecteer Ja voor de wisselknop **Subactiva opnemen** om kosten gerelateerd aan subactiva als afzonderlijke regels weer te geven.

8. Als u de zoekopdracht wilt beperken, kunt u specifieke activa/functionele locaties/werkorders selecteren op het sneltabblad **Op te nemen records**.

9. Klik op **OK** om de berekening te starten.

10. Klik op de pagina **Uurcontrole activa** op de knoppen **Groeperen op** om het vereiste detailniveau van de berekening weer te geven. De geselecteerde knoppen **Groeperen op** worden gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

## <a name="example"></a>Voorbeeld

In onderstaande schermafbeelding ziet u een voorbeeld van een berekening van een **Uurcontrole activa**.

- In het veld **Oorspronkelijk budget** worden budgeturen uit de werkorderprognose weergegeven. 
- In het veld **Werkelijke uren** worden geboekte uren voor werkorders weergegeven. 
- In het veld **Toegezegde uren** wordt het totale aantal uren weergegeven dat uw bedrijf heeft toegezegd met betrekking tot werkorders.

![Voorbeeld van een berekening van uurcontrole activa.](media/04-controlling-and-reporting.png)

U kunt uren ook berekenen door meerdere activa te selecteren in **Alle activa** of **Actieve activa**. Vervolgens klikt u op de knop **Uurcontrole** op het sneltabblad **Algemeen**. De geselecteerde activa worden automatisch ingevoegd in het veld **Activum** op het sneltabblad **Op te nemen records**. Klik op **OK** in het dialoogvenster **Uurcontrole activa** om de berekening voor de geselecteerde activa weer te geven. Dezelfde procedure kan worden uitgevoerd voor functionele locaties in **Alle functionele locaties** of **Actieve functionele locaties** en voor werkorders in **Alle werkorders** of **Actieve werkorders**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]