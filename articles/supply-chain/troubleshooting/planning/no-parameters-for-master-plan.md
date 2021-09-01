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
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756770"
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
