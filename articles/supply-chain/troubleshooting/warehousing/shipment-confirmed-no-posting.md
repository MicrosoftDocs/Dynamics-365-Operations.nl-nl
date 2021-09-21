---
title: Zending voor lading werd bevestigd, maar er zijn geen regels geboekt
description: De zendingsbevestiging heeft geen invloed op de boeking. Hiermee wordt alleen de zendings- en ladingstatus bijgewerkt. De boeking moet plaatsvinden in een afzonderlijk proces.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e754f1461672c1e9f2d8dd1a7ceffc81f3809120
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476047"
---
# <a name="shipment-for-load-has-been-confirmed-but-no-lines-are-posted"></a>Zending voor lading is bevestigd, maar er zijn geen regels geboekt

## <a name="symptoms"></a>Symptomen

Wanneer u met uitgaande magazijnbewerkingen werkt, wordt mogelijk het volgende bericht weergegeven:

> De zending voor lading 1% is bevestigd.

Er vond echter geen verdere boeking plaats.

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. De zendingsbevestiging heeft geen invloed op de boeking. Hiermee wordt alleen de zendings- en ladingstatus bijgewerkt. De boeking moet plaatsvinden in een afzonderlijk proces.
