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
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026396"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a>Het magazijn in het orderverzamellijstjournaal is niet bijgewerkt op een stuklijstregel

KB-nummer: 4614848

## <a name="symptoms"></a>Symptomen

Het magazijn in het orderverzamellijstjournaal is niet bijgewerkt op een stuklijstregel.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp. Als er een orderverzamellijstjournaalregel is gemaakt die een verwijzing (via de partij-id) naar een productielijstregel heeft, wordt het magazijn op de stuklijstregel voor de productie niet bijgewerkt als de magazijndimensie op de orderverzamellijstjournaalregel voor de productie later wordt gewijzigd.
