---
title: Explosie van een stuklijstversie
description: In dit artikel wordt een hoofdplanningsscenario uitgelegd dat betrekking heeft op de explosie van een stuklijstversie.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ef8a04ce4ab2180f39a6d2bcdab976eb146d610
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741225"
---
# <a name="explosion-of-a-bom-version"></a>Explosie van een stuklijstversie

[!include [banner](../includes/banner.md)]

In dit artikel wordt een hoofdplanningsscenario uitgelegd dat betrekking heeft op de explosie van een stuklijstversie.

Een vraagexplosie van een stuklijstversie maakt een vraag voor elk stuklijstregelartikel op een bepaalde locatie en mogelijk in een bepaald magazijn. In een locatiespecifieke stuklijst kan een specifiek magazijn worden gedefinieerd voor elke stuklijstregel. Bovendien bepalen de dimensie-instellingen van het artikel voor elke stuklijstregel of het magazijn al dan niet nodig is. De resulterende vraag voor elk stuklijstregelartikel wordt dan het beginpunt voor extra vraagexplosies. Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:

-   De locatiedimensie is verplicht en moet bij de vraagtransactie worden opgegeven.
-   De sitedimensie is consistent. De site voor een vraag op een lager niveau is hetzelfde als de site bij de eerste vraagtransactie.

In de volgende afbeelding ziet u het proces voor de vraagexplosie van de hoofdplanning. ![Vraagexplosie met stuklijstversie.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Aanvullende bronnen

- [De stuklijstversie bepalen](master-plan-bom-version-determined.md)
- [Overzicht van de hoofdplanning en functionaliteit voor meerdere locaties](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]