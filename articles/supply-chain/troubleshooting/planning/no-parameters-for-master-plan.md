---
title: Parameters voor het hoofdplan bestaan niet
description: Wanneer u een geplande order probeert te fiatteren, ontvangt u een foutbericht dat er geen parameters voor het hoofdplan bestaan.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294049"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>Parameters voor het hoofdplan bestaan niet

Foutcode: SYS25368

## <a name="symptoms"></a>Symptomen

Wanneer u een geplande order probeert te fiatteren, wordt het volgende foutbericht weergegeven:

> Parameters voor hoofdplan %1 bestaan niet.

## <a name="cause"></a>Oorzaak

Vanwege configuratieproblemen kan het systeem de instellingen voor het opgegeven plan niet vinden.

## <a name="resolution"></a>Oplossing

- Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen** en zorg ervoor dat er een plan met de opgegeven naam bestaat.
