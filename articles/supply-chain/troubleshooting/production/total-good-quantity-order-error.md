---
title: Fout in totale goede hoeveelheid bij het beëindigen van een order
description: Wanneer u probeert een productieorder te beëindigen en dit te melden als Gereed, wordt mogelijk een fout in de goede hoeveelheid weergegeven. Deze pagina licht toe waarom en hoe u het probleem kunt oplossen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476002"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Fout in totale goede hoeveelheid bij het beëindigen van een productieorder

## <a name="symptoms"></a>Symptomen

Wanneer u een gereedmeldingsjournaal voor een productieorder probeert te boeken, wordt het volgende foutbericht weergegeven:

> Totale goede hoeveelheid die voor de productie is gereedgemeld, is %1. Feedback voor de laatste bewerking is 0,00 in totaal.

## <a name="cause"></a>Oorzaak

Dit probleem doet zich voor als de hoeveelheden die in de laatste bewerkingen zijn geboekt, onjuist waren. Als de productie bijvoorbeeld wordt gestart, maar de hoeveelheid die moet worden gestart niet is toegewezen, wordt het routekaartjournaal zonder regels geboekt. Om de situatie te bevestigen, opent u de productieorder en selecteert u vervolgens in het actievenster op het tabblad **Weergave** de optie **Routekaart**.

## <a name="resolution"></a>Oplossing

U kunt dit probleem oplossen door aanvullende journalen te boeken voor de bewerkingen waarvoor de journalen niet juist geboekt zijn. Start de productieorder opnieuw en geef op dat u de aanvullende journalen wilt boeken. Met deze actie wordt de productieorder niet gestart, maar worden de journalen geboekt. De routekaart moet vervolgens de hoeveelheden weergeven die zijn geboekt en u moet de productieorders kunnen beëindigen.
