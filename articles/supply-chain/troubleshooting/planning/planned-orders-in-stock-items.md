---
title: Geplande orders worden gegenereerd voor in voorraad met productieorders
description: Er worden geplande orders gegenereerd, hoewel er al artikelen in voorraad of productieorders voor zijn.
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
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476061"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Geplande orders worden gegenereerd voor in voorraad met productieorders

## <a name="symptoms"></a>Symptomen

Er worden geplande orders gegenereerd, hoewel er al artikelen in voorraad of productieorders voor zijn.

## <a name="resolution"></a>Oplossing

U kunt dit probleem mogelijk oplossen door de waarde van de **Positieve dagen** te verhogen voor de relevante groepen op de pagina **Behoefteplanningsgroep**. Door deze wijziging wordt door het systeem bepaald of de voorhanden voorraad voor de vraag kan worden gebruikt. Er wordt dan geen nieuwe geplande order gegenereerd voor de artikelen die in voorraad zijn.
