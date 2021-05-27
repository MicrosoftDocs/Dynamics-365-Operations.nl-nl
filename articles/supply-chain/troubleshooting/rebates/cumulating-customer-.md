---
title: De cumulatie van klantkortingen mislukt wanneer artikelkortingsgroepen worden gebruikt
description: Wanneer u klantkortingsovereenkomsten gebruikt in combinatie met artikelkortingsgroepen, worden kortingen berekend, maar mislukt de cumulatie.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026395"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>De cumulatie van klantkortingen mislukt wanneer artikelkortingsgroepen worden gebruikt

KB-nummer: 4611372

## <a name="symptoms"></a>Symptomen

Wanneer u klantkortingsovereenkomsten (van het type *bedrag*) gebruikt in combinatie met artikelkortingsgroepen, worden kortingen berekend, maar mislukt de cumulatie.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp. Artikelengroepen groeperen alleen artikelen met dezelfde drempelvoorwaarde. De kortingsvoorwaarde (drempel) wordt ingesteld op het bedrag voor elk artikel, niet op het gecumuleerde bedrag voor een artikel in de artikelgroep.
