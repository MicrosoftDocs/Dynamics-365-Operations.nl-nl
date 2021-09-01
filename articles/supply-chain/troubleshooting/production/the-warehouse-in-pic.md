---
title: Het magazijn in het orderverzamellijstjournaal is niet bijgewerkt op een stuklijstregel.
description: Het magazijn in het orderverzamellijstjournaal is niet bijgewerkt op een stuklijstregel.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 970930bbdd30b57a8374de7810bb3ece8cb19a7010b5ef19d90bfc39d09f172b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740546"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Het magazijn in het orderverzamellijstjournaal is niet bijgewerkt op een stuklijstregel

KB-nummer: 4614848

## <a name="symptoms"></a>Symptomen

Het magazijn in het orderverzamellijstjournaal is niet bijgewerkt op een stuklijstregel.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp. Als er een orderverzamellijstjournaalregel is gemaakt die een verwijzing (via de partij-id) naar een productielijstregel heeft, wordt het magazijn op de stuklijstregel voor de productie niet bijgewerkt als de magazijndimensie op de orderverzamellijstjournaalregel voor de productie later wordt gewijzigd.
