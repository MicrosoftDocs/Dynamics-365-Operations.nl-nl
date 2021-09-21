---
title: Update van gereedmelding mislukt met een ontbrekende hoeveelheidsfout
description: Als u een productieorder wilt gereedmelden tijdens het rapporteren van de fouthoeveelheid, maar niet de tijd of de materiaalhoeveelheid, mislukt het rapport als voltooide update.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7785549c47063727f2749749940c1a96a351e70f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475983"
---
# <a name="report-as-finished-update-fails-with-a-missing-quantity-error"></a>Update van gereedmelding mislukt met een ontbrekende hoeveelheidsfout

## <a name="symptoms"></a>Symptomen

U probeert een productieorder gereed te melden terwijl u de fouthoeveelheid rapporteert, maar niet terwijl u de tijd of de materiaalhoeveelheid rapporteert. De update van de gereedmelding mislukt wanneer u probeert de productieorder te beëindigen en u krijgt het volgende foutbericht:

> Gereedgemelde hoeveelheid ontbreekt.

## <a name="resolution"></a>Oplossing

Als u de fouthoeveelheid van een productieorder niet rapporteert, moet u ook de goede hoeveelheid rapporteren.
