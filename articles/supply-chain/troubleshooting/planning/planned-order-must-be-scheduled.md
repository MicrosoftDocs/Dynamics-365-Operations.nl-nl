---
title: Geplande productieorder moet worden gepland voordat deze kan worden gefiatteerd
description: Wanneer u een geplande order probeert te gefiatteerd, ontvangt u een foutbericht dat de order moet worden gepland voordat deze kan worden gefiatteerd.
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294051"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Geplande productieorder moet worden gepland voordat deze kan worden gefiatteerd

Foutcode: SYS309802

## <a name="symptoms"></a>Symptomen

Wanneer u een geplande order probeert te fiatteren, wordt het volgende foutbericht weergegeven:

> De geplande productieorder moet worden gepland voordat deze kan worden gefiatteerd.

## <a name="cause"></a>Oorzaak

De geplande begindatum en einddatum mogen niet leeg zijn.

## <a name="resolution"></a>Oplossing

Als u de begin- en einddatum voor de geplande order wilt opgeven, gaat u als volgt te werk.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Geplande orders**.
1. Open de betreffende geplande order.
1. Geef in het sneltabblad **Algemeen** in de sectie **Gepland** datums op in de velden **Begindatum** en **Einddatum**.
