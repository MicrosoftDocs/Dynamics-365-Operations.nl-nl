---
title: Kostenbeheer activafout
description: In dit artikel wordt kostencontrole voor activafouten in Activabeheer uitgelegd.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 553b89a43b656669b7730b19898f3a5d81a3873a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889659"
---
# <a name="asset-fault-cost-control"></a>Kostenbeheer activafout

[!include [banner](../../includes/banner.md)]

 

In Activabeheer kunt u kosten voor activafoutregistraties berekenen om een overzicht te krijgen van de werkelijke kosten ten opzichte van budgetkosten. Werkelijke kosten worden gebaseerd op geboekte transacties. De datum is de foutdatum waarop het symptoom is vastgelegd.

1. Klik op **Activabeheer** > **Query's** > **Activafout** > **Kostencontrole activafout**.

2. Selecteer in het dialoogvenster **Kostencontrole activafout** een financiële-dimensieset die u wilt opnemen in de berekening, indien nodig.

4. Selecteer Ja voor de wisselknop **Nul overslaan** als u geen resultaten wilt weergeven met nul kosten.

5. U kunt het veld **Niveau** gebruiken om aan te geven hoe gedetailleerd de regels voor kostencontrole moeten zijn met betrekking tot functionele locaties. 

    Als u bijvoorbeeld het getal 1 invoegt in het veld en u een structuur met meerdere niveaus voor functionele locaties hebt, worden alle kostencontroleregels voor een functionele locatie weergegeven op het hoogste niveau. Daarom kunnen de uren op een regel zijn opgeteld op basis van functionele locaties die zich op een lager niveau bevinden. 
    
    Als u het getal 0 in het veld **Niveau** invoegt, wordt er een gedetailleerd resultaat met alle regels voor kostencontrole voor activafouten weergegeven op alle niveaus voor functionele locaties waarop deze betrekking hebben.

6. Als u de zoekopdracht wilt beperken, kunt u specifieke activa, foutdatums en foutoorzaken selecteren op het sneltabblad **Op te nemen records**.

7. Klik op **OK** om de berekening te starten.

8. Klik op de knoppen **Groeperen op** om het vereiste detailniveau van de kostenberekening weer te geven. De geselecteerde knoppen **Groeperen op** worden gemarkeerd. U kunt knoppen activeren of deactiveren door erop te klikken.

## <a name="example"></a>Voorbeeld

In dit voorbeeld wordt een berekening van het kostenbeheer voor activafouten getoond.

- In het veld **Oorspronkelijk budget** worden budgetkosten uit de werkorderprognose weergegeven. 
- In het veld **Werkelijke kosten** worden geboekte kosten voor werkorders weergegeven. 
- In het veld **Toegezegde kosten** wordt het totale aantal kosten weergegeven dat uw bedrijf heeft toegezegd met betrekking tot werkorders.

    ![Figuur 1.](media/05-controlling-and-reporting.png)

Zie het artikel [Foutbeheer](../setup-for-work-orders/fault-management.md) voor informatie over het instellen van fouten.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]