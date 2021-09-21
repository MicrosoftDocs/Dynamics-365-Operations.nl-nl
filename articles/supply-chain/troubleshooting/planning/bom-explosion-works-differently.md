---
title: Stuklijstexplosie zal zich anders gedragen voor gefiatteerde en geraamde productieorders
description: Een explosie van stuklijsten werkt anders voor gefiatteerde productieorders en voor geraamde productieorders voor handmatig aangemaakt werk
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476009"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>Stuklijstexplosie zal zich anders gedragen voor gefiatteerde en geraamde productieorders

## <a name="symptoms"></a>Symptomen

Wanneer een productieorder wordt gefiatteerd, worden de artikelen niet geëxplodeerd wanneer u de stuklijst explodeert. Wanneer u echter handmatig een werkorder maakt en vervolgens de productieorder raamt, worden de artikelen geëxplodeerd.

### <a name="resolution"></a>Oplossing

De explosie die plaatsvindt wanneer de productieorder wordt gefiatteerd, verwijst naar de geplande order, maar er wordt in dat geval niet aangegeven dat de geplande order momenteel is gefiatteerd. Als de productieorder echter is geraamd, wordt de explosie geactiveerd vanuit de vrijgegeven productieorder waarvoor geen geplande order bestaat.
