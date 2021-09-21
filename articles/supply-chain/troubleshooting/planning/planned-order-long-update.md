---
title: Het bijwerken van geplande orders duurt erg lang
description: Wanneer u de vereist hoeveelheid en/of leveringsdatum van een geplande order bijwerkt, duurt het doorgaans minimaal 30 seconden per order om de update op te slaan.
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476025"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Het bijwerken van geplande orders duurt erg lang

## <a name="symptoms"></a>Symptomen

Wanneer u de behoeftehoeveelheid en/of leveringsdatum op een geplande order bijwerkt, duurt het doorgaans minimaal 30 seconden per order om de update op te slaan.

## <a name="resolution"></a>Oplossing

Dit is een bekend probleem met de ingebouwde hoofdplanningsengine. Dit wordt veroorzaakt door de onderliggende automatische explosie via de stuklijststructuur tijdens bewerkingen. Dit probleem wordt verholpen in planningsoptimalisatie, waarbij een planner de relevante orders kan bijwerken en goedkeuren en zo nodig een planningsuitvoering kan activeren om geplande orders voor de onderliggende stuklijststructuur bij te werken.

Eén manier om de prestaties te verbeteren met de ingebouwde hoofdplanningsengine bestaat uit de volgende stappen:

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Een plan selecteren.
1. Vouw het sneltabblad **Time fence in dagen** uit.
1. Stel **Explosie** in op *Ja* en stel het veld onder deze instelling in op 0 (nul).

> [!NOTE]
> Hierdoor wordt de periode voor explosies die voor dit hoofdplan worden uitgevoerd tot één dag beperkt.
