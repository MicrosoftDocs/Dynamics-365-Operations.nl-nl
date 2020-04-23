---
title: Analyse voor passende Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u uw huidige instellingen en gegevens kunt controleren op basis van de mogelijkheden van de functionaliteit Optimalisatieplanning.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208749"
---
# <a name="planning-optimization-fit-analysis"></a>Analyse voor passende Planningsoptimalisatie

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Als u wilt zien hoe compatibel uw huidige instellingen en gegevens zijn met de functie Planningsoptimalisatie, gaat u naar **Hoofdplanning** \> **Instellingen** \> **Analyse voor passende Planningsoptimalisatie** en selecteert u **Analyse uitvoeren**. Als in de analyse inconsistenties worden gevonden, worden deze op dezelfde pagina weergegeven. (Het kan enkele minuten duren voordat de analyse is uitgevoerd.)

> [!NOTE]
> Als er inconsistenties worden gevonden, kunt u Planningsoptimalisatie nog steeds gebruiken. De resultaten van de aanpassingsanalyse geven alleen de plaatsen aan waar de planningsservice de huidige instellingen niet kan inwilligen. Met andere woorden, de plaatsen worden weergegeven waar bepaalde processen mogelijk worden genegeerd of niet worden ondersteund.

## <a name="analysis-results-example-1"></a>Resultaten van analyse: voorbeeld 1

- **Functie:** productie
- **Probleem:** artikelen met stuklijstniveau hoger dan nul: 56
- **Uitleg:** de aanpassingsanalyse heeft 56 artikelen gevonden met een ingestelde stuklijst voor productie. Omdat de huidige versie van Planningsoptimalisatie productie niet ondersteunt, worden in Planningsoptimalisatie geplande inkooporders gegenereerd in plaats van geplande productieorders. Er wordt ook een waarschuwing weergegeven waarin de betreffende artikelen worden vermeld.

### <a name="analysis-results-example-2"></a>Resultaten van analyse: voorbeeld 2

- **Functie:** acties
- **Probleem:** behoefteplanningsgroepen waarvoor actieberekening is ingeschakeld: 6
- **Uitleg:** de aanpassingsanalyse heeft zes behoefteplanningsgroepen gevonden waarvoor actieberekeningen zijn ingeschakeld. Omdat de huidige versie van Planningsoptimalisatie acties niet ondersteunt, worden er geen acties gegenereerd tijdens de hoofdplanning.

## <a name="related-resources"></a>Gerelateerde bronnen

[Overzicht van Planningsoptimalisatie](planning-optimization-overview.md)

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Filters op een plan toepassen](plan-filters.md)

[Een planningstaak annuleren](cancel-planning-job.md)
