---
title: Filters op een plan toepassen
description: In dit onderwerp wordt uitgelegd hoe u filters gebruikt voor een plan wanneer de functionaliteit Planningsoptimalisatie wordt gebruikt.
author: ChristianRytt
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c2fbaa6945cf46b7ef09232e6004f09b487ea7c822e72225dc00d3d28ecb008e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780193"
---
# <a name="apply-filters-to-a-plan"></a>Filters op een plan toepassen

[!include [banner](../../includes/banner.md)]

Wanneer de functionaliteit Planningsoptimalisatie wordt gebruikt, kunt u een filter toepassen op een plan. Het **planfilter** wordt altijd toegepast tijdens de uitvoering van een hoofdplanning. Een **planfilter** is handig als u een plan wilt beperken tot een bepaalde groep artikelen en als u ervoor wilt zorgen dat er geen andere artikelen worden opgenomen als onderdeel van de resulterende hoofdplanning.

Als er een **planfilter** wordt toegepast en er tijdens de uitvoering van een hoofdplanning ook een runtimefilter wordt toegepast, wordt alleen het snijpunt van de twee filters opgenomen in de planningsuitvoering.

Het **planfilter** kan worden geopend vanuit **Hoofdplannen** wanneer Planningsoptimalisatie wordt gebruikt.

## <a name="example-scenario"></a>Voorbeeldscenario

Er is een planfilter ingesteld met de artikelen A, B en C. Vervolgens vinden voor hetzelfde plan hoofdplanningsuitvoeringen plaats, maar worden er verschillende runtimefilters toegepast:

- **Runtimefilter dat artikel D bevat:** er zijn geen artikelen gepland omdat er geen snijpunt tussen het planfilter en runtimefilter bestaat.
- **Runtimefilter dat artikel A en D bevat:** alleen artikel A wordt opgenomen in de planningsuitvoering omdat artikel D geen deel uitmaakt van het planfilter.
- **Runtimefilter dat artikel B bevat:** alleen artikel B wordt opgenomen in de planningsuitvoering en de eerdere planningsuitvoer voor artikel A wordt behouden.
- **Runtimefilter dat alle artikelen bevat (leeg filter):** artikelen A, B en C worden opgenomen in de planningsuitvoering en de eerdere planningsuitvoer voor artikelen A en B wordt overschreven.

> [!NOTE]
> Stel geen planfilter in voor het plan dat als **Huidig dynamisch hoofdplan** is geselecteerd op de pagina **Parameters hoofdplanning**. Anders wordt de functionaliteit voor dynamische hoofdplannen beperkt tot de gefilterde artikelen. Als de nettobehoeften bijvoorbeeld worden bijgewerkt voor een artikel dat geen deel uitmaakt van het planfilter, wordt er geen resultaat gegenereerd.

## <a name="related-resources"></a>Gerelateerde bronnen

[Overzicht van Planningsoptimalisatie](planning-optimization-overview.md)

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Een planningstaak annuleren](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]