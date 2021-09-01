---
title: Het veld Datum laatst getest wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt
description: Het veld Datum laatst getest wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742023"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Het veld Datum laatst getest wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt

KB-nummer: 4612803

## <a name="symptoms"></a>Symptomen

Het veld **Datum laatst getest** wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp. De datum van de laatste test is niet gerelateerd aan kwaliteitsorders. Dit is de datum waarop de eindproducten voor het eerst zijn ingekocht of gefabriceerd. Met deze datum wordt de adviesdatum voor de houdbaarheid berekend.
