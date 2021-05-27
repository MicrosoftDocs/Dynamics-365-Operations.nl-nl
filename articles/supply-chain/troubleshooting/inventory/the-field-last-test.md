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
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026416"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Het veld Datum laatst getest wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt

KB-nummer: 4612803

## <a name="symptoms"></a>Symptomen

Het veld **Datum laatst getest** wordt niet bijgewerkt wanneer er meerdere kwaliteitsorders worden gemaakt.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp. De datum van de laatste test is niet gerelateerd aan kwaliteitsorders. Dit is de datum waarop de eindproducten voor het eerst zijn ingekocht of gefabriceerd. Met deze datum wordt de adviesdatum voor de houdbaarheid berekend.
