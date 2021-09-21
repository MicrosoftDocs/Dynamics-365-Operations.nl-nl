---
title: Een leverancierskorting wordt niet gecumuleerd op basis van facturen
description: Een leverancierskorting wordt niet gecumuleerd op basis van facturen
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476055"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Een leverancierskorting wordt niet gecumuleerd op basis van facturen

## <a name="symptoms"></a>Symptomen

Als facturen die zijn geboekt verschillende vervaldatums hebben, worden deze facturen niet weergegeven in leverancierskortingen die daaruit worden gegenereerd.

## <a name="resolution"></a>Oplossing

De vervaldatum wordt niet meegenomen wanneer de leverancierskorting wordt berekend. U zou het systeem zo kunnen aanpassen dat de vervaldatum en de relatie met de factuur duidelijker zijn ten opzichte van de feitelijke leverancierskorting.
