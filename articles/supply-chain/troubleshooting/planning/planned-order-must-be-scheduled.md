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
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777738"
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
