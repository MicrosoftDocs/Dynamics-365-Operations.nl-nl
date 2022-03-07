---
title: Systeembeheerders kunnen orderwachtstanden niet wissen, omdat ze niet geautoriseerd zijn
description: Systeembeheerders kunnen orderwachtstanden niet wissen, omdat ze niet geautoriseerd zijn.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026422"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Systeembeheerders kunnen orderwachtstanden niet wissen, omdat ze niet geautoriseerd zijn

KB-nummer: 4614642

## <a name="symptoms"></a>Symptomen

Systeembeheerders kunnen verkooporderwachtstanden niet wissen, tenzij zij de specifieke rol hebben die in de orderwachtstandcode is toegewezen.

## <a name="resolution"></a>Oplossing

De toegang tot bepaalde bewerkingen, zoals het leegmaken van verkooporderwachtstanden, wordt aangestuurd door het instellen van een bedrijfsbeleid. Systeembeheerders kunnen normaal gesproken geen bewerkingen van dit type uitvoeren. 

Hoe meer mensen een bepaalde taak kunnen uitvoeren, wordt bepaald door het beleid van het bedrijf. Alleen bepaalde personen in een organisatie zijn goedgekeurd om die taak uit te voeren. Voorbeelden zijn goedkeuringen die het resultaat zijn van werkstroomgoedkeuringen en specifieke taken die het resultaat zijn van een werkstroomconfiguratie.

Hoewel er geen werkstroom is gekoppeld aan orderwachtstanden, is het principe vergelijkbaar. Met een relevante rol wordt de specifieke groep mensen in een organisatie aangeduid die over het recht beschikt om orderwachtstanden te wissen. Dit recht hoeft niet aan alle beheerders te worden toegekend, omdat die benadering in strijd is met het gedefinieerde bedrijfsbeleid.
