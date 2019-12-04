---
title: Filters op een plan toepassen
description: In dit onderwerp wordt uitgelegd hoe u filters gebruikt voor een plan wanneer de functionaliteit Planningsoptimalisatie wordt gebruikt.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ff9c9f875368fcc4dd62b9c188d489e20a5c7960
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773935"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="apply-filters-to-a-plan"></a>Filters op een plan toepassen

Wanneer de functionaliteit Planningsoptimalisatie wordt gebruikt, kunt u een filter toepassen op een plan. Het planfilter wordt altijd toegepast tijdens de uitvoering van een hoofdplanning. Een planfilter is handig als u een plan wilt beperken tot een bepaalde groep artikelen en als u ervoor wilt zorgen dat er geen andere artikelen worden opgenomen als onderdeel van de resulterende hoofdplanning.

Als er een planfilter wordt toegepast en er tijdens de uitvoering van een hoofdplanning ook een runtimefilter wordt toegepast, wordt alleen het snijpunt van de twee filters opgenomen in de planningsuitvoering.

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
