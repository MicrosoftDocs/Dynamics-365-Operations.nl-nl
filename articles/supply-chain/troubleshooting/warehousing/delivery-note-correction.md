---
title: Correctie van afleveringsbewijs kan niet worden verwerkt
description: Als u een afleveringsbewijs probeert te corrigeren nadat het is geboekt, wordt er een foutbericht weergegeven. Op deze pagina wordt uitgelegd hoe u geboekte pakbonnen corrigeert voor artikelen die zijn ingeschakeld voor WMS.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476038"
---
# <a name="delivery-note-correction-cant-be-processed"></a>Correctie van afleveringsbewijs kan niet worden verwerkt

## <a name="symptoms"></a>Symptomen

Nadat u een afleveringsbewijs hebt geboekt, kunt u het niet meer annuleren, omdat de knop **Annuleren** niet beschikbaar is. U kunt het afleveringsbewijs ook niet corrigeren. Als u dit probeert, wordt mogelijk het volgende foutbericht weergegeven:

> De correctie van het afleveringsbewijs kan niet worden verwerkt. Het afleveringsbewijs bevat alleen artikelen die onder magazijnbeheerprocessen vallen, aangezien deze niet worden ondersteund door correctie van afleveringsbewijzen.

## <a name="resolution"></a>Oplossing

Als u geboekte pakbonnen wilt corrigeren voor artikelen die zijn ingeschakeld voor geavanceerd magazijnbeheer (WMS), moet u de boeking uitvoeren vanuit de lading, niet rechtstreeks vanuit de order.
