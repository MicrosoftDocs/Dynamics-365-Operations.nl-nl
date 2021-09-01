---
title: Het batchnummer wordt gewist wanneer een nieuwe partij-id is geselecteerd
description: Wanneer u een orderverzamellijstjournaalregel bekijkt, wordt de waarde in het veld Batchnummer gewist als u een nieuwe waarde selecteert in het veld Partij-id.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738814"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Het batchnummer wordt gewist wanneer een nieuwe partij-id is geselecteerd

KB-nummer: 4613107

## <a name="symptoms"></a>Symptomen

Wanneer u een orderverzamellijstjournaalregel bekijkt, wordt de waarde in het veld **Batchnummer** gewist als u een nieuwe waarde selecteert in het veld **Partij-id**.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp. Als u de partij-ID wijzigt, wijzigt u de artikelcontext. Daarom wordt het batchnummer opnieuw ingesteld.

Als u het batchnummer aan een partij-id wilt koppelen, moet u eerst de partij-id instellen.
