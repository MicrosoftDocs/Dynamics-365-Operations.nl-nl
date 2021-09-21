---
title: Onvoldoende werk gevonden voor cluster na configureren van profiel
description: Als u een clusterprofiel configureert, ontvangt u mogelijk een foutbericht dat er niet voldoende werk kan worden gevonden. Bewerk het profiel en stel de posities Activeren in op Nee.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475978"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Er is onvoldoende werk gevonden voor cluster bij het gebruik van door het systeem gestuurde clusterverzameling

## <a name="symptoms"></a>Symptomen

Wanneer u het proces *Door systeem gestuurde clusterverzameling* gebruikt en een clusterprofiel configureert waarbij bijvoorbeeld tien posities kunnen worden verzameld, werkt het proces zoals gepland wanneer er voldoende werk is om te worden verzameld tot tien posities. Als er echter slechts acht posities kunnen worden verzameld, wordt het volgende foutbericht weergegeven:

> Er is onvoldoende werk gevonden voor cluster.

## <a name="resolution"></a>Oplossing

U kunt dit probleem oplossen door het clusterprofiel te bewerken en de optie **Posities activeren** in te stellen op *Nee*.
