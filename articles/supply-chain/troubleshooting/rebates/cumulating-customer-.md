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
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760365"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>De cumulatie van klantkortingen mislukt wanneer artikelkortingsgroepen worden gebruikt

KB-nummer: 4611372

## <a name="symptoms"></a>Symptomen

Wanneer u klantkortingsovereenkomsten (van het type *bedrag*) gebruikt in combinatie met artikelkortingsgroepen, worden kortingen berekend, maar mislukt de cumulatie.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp. Artikelengroepen groeperen alleen artikelen met dezelfde drempelvoorwaarde. De kortingsvoorwaarde (drempel) wordt ingesteld op het bedrag voor elk artikel, niet op het gecumuleerde bedrag voor een artikel in de artikelgroep.
