---
title: Explosie van een stuklijstversie
description: In dit artikel wordt een hoofdplanningsscenario uitgelegd dat betrekking heeft op de explosie van een stuklijstversie.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f852c8d100c91d055e58c4594106aedf6fe5afb
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="explosion-of-a-bom-version"></a>Explosie van een stuklijstversie

[!INCLUDE [banner](../includes/banner.md)]

In dit artikel wordt een hoofdplanningsscenario uitgelegd dat betrekking heeft op de explosie van een stuklijstversie.

Een vraagexplosie van een stuklijstversie maakt een vraag voor elk stuklijstregelartikel op een bepaalde locatie en mogelijk in een bepaald magazijn. In een locatiespecifieke stuklijst kan een specifiek magazijn worden gedefinieerd voor elke stuklijstregel. Bovendien bepalen de dimensie-instellingen van het artikel voor elke stuklijstregel of het magazijn al dan niet nodig is. De resulterende vraag voor elk stuklijstregelartikel wordt dan het beginpunt voor extra vraagexplosies. Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:

-   De locatiedimensie is verplicht en moet bij de vraagtransactie worden opgegeven.
-   De sitedimensie is consistent. De site voor een vraag op een lager niveau is hetzelfde als de site bij de eerste vraagtransactie.

In de volgende afbeelding ziet u het proces voor de vraagexplosie van de hoofdplanning. ![Vraagexplosie met stuklijstversie](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a>Zie ook
--------

[Hoofdplanning - hoe de stuklijstversie wordt bepaald](master-plan-bom-version-determined.md)

[Hoofdplanning en de functionaliteit voor meerdere locaties](master-plan-multisite-functionality.md)




