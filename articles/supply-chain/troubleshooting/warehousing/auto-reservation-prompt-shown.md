---
title: Prompt voor automatische reservering wordt weergegeven met beschikbare voorraad
description: Wanneer u een artikel gebruikt in een magazijn waar magazijnprocessen niet zijn ingeschakeld, wordt de prompt voor automatische reservering weergegeven. Geef alle dimensies op boven Locatie.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476049"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Prompt voor automatische reservering voor batchnummer wordt weergegeven, zelfs bij beschikbare voorraad

## <a name="symptoms"></a>Symptomen

Wanneer u een artikel met een *batch-boven*-reserveringshiërarchie gebruikt in een magazijn dat magazijnprocessen niet heeft ingeschakeld en automatische reservering is ingeschakeld, wordt de automatische reserveringsprompt voor een batchnummer weergegeven, zelfs als er slechts één batch beschikbaar is voor verzamelen.

Wanneer u echter hetzelfde artikel gebruikt in een magazijn waar magazijnprocessen zijn ingeschakeld, wordt de automatische reserveringsprompt niet weergegeven.

## <a name="resolution"></a>Oplossing

Als een reserveringshiërarchie wordt gedefinieerd als *batch-boven* of *serienummer-boven*, moet de dimensie waarnaar wordt verwezen (**Batchnummer** of **Serienummer**) altijd worden opgegeven op aanvraagorders. Magazijnprocessen kunnen de informatie mogelijk voltooien als een enkel batch- of serienummer beschikbaar is. Omdat het magazijn echter niet is ingeschakeld voor magazijnprocessen, moet de gebruiker altijd alle dimensies boven **Locatie** opgeven.
