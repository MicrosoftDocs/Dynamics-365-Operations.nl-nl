---
title: Geplande inkooporder wordt gemaakt wanneer er binnen negatieve dagen een inkoop bestaat
description: Als de behoefteplanningscode Min/max is, wordt via Planningsoptimalisatie een geplande inkooporder gemaakt wanneer er binnen negatieve dagen een inkoop bestaat.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026411"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Geplande inkooporder wordt gemaakt wanneer er binnen negatieve dagen een inkoop bestaat

KB-nummer: 4614298

## <a name="symptoms"></a>Symptomen

Als de behoefteplanningscode *Min/max* is, wordt via Planningsoptimalisatie een geplande inkooporder gemaakt wanneer er binnen negatieve dagen een inkoop bestaat.

## <a name="resolution"></a>Oplossing

Bij planningsoptimalisatie worden negatieve dagen niet ondersteund. Het zorgt er echter altijd voor dat geplande orders niet worden gepland binnen de doorlooptijd ten opzichte van de huidige datum. De doorlooptijd van inkoop is bijvoorbeeld 10 dagen en de verwachting is dat een inkooporder acht dagen later dan vandaag binnenkomt. In dit geval wordt de inkooporder gebruikt als vraagaanbod van vijf dagen vanaf vandaag.

Het wordt daarom aangeraden de doorlooptijden aan te passen voor alle (of bijna alle) scenario's.
