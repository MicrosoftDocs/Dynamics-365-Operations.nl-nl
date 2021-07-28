---
title: Explosie van een stuklijstversie
description: In dit artikel wordt een hoofdplanningsscenario uitgelegd dat betrekking heeft op de explosie van een stuklijstversie.
author: roxanadiaconu
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c4f1306faa2c0ae02fee48449839db4ff0907ff
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348387"
---
# <a name="explosion-of-a-bom-version"></a>Explosie van een stuklijstversie

[!include [banner](../includes/banner.md)]

In dit artikel wordt een hoofdplanningsscenario uitgelegd dat betrekking heeft op de explosie van een stuklijstversie.

Een vraagexplosie van een stuklijstversie maakt een vraag voor elk stuklijstregelartikel op een bepaalde locatie en mogelijk in een bepaald magazijn. In een locatiespecifieke stuklijst kan een specifiek magazijn worden gedefinieerd voor elke stuklijstregel. Bovendien bepalen de dimensie-instellingen van het artikel voor elke stuklijstregel of het magazijn al dan niet nodig is. De resulterende vraag voor elk stuklijstregelartikel wordt dan het beginpunt voor extra vraagexplosies. Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:

-   De locatiedimensie is verplicht en moet bij de vraagtransactie worden opgegeven.
-   De sitedimensie is consistent. De site voor een vraag op een lager niveau is hetzelfde als de site bij de eerste vraagtransactie.

In de volgende afbeelding ziet u het proces voor de vraagexplosie van de hoofdplanning. ![Vraagexplosie met stuklijstversie.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Aanvullende bronnen

[De stuklijstversie bepalen](master-plan-bom-version-determined.md)

[Overzicht van de hoofdplanning en functionaliteit voor meerdere locaties](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]