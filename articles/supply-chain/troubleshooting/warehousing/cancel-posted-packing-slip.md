---
title: Kan pakbon niet annuleren nadat deze is geboekt vanuit een order
description: Wanneer orderverzamelings- en verzendprocessen zijn ingeschakeld voor WMS, kunt u een pakbon niet annuleren nadat deze is geboekt vanuit een verkooporder. Deze pagina biedt een workaround.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476065"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Kan een pakbon niet annuleren nadat deze is geboekt vanuit een verkooporder

## <a name="symptoms"></a>Symptomen

Wanneer orderverzamelings- en verzendprocessen zijn ingeschakeld voor geavanceerd magazijnbeheer (WMS), kunt u een pakbon niet annuleren nadat deze is geboekt vanuit een verkooporder.

## <a name="resolution"></a>Oplossing

Als u geboekte pakbonnen wilt corrigeren voor artikelen die zijn ingeschakeld voor WMS, moet u de boeking uitvoeren vanuit de lading, niet vanuit de order. Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is.  

In het algemeen kan een verkooporder die is verzameld en verzonden via magazijnbeheerprocessen met de pakbon worden bijgewerkt vanuit de lading of zending en het verkooporderdocument zelf. Als u de verkooporder echter met de pakbon bijwerkt vanuit het verkooporderdocument, kan de pakbon nog steeds niet worden teruggeboekt vanuit de lading of verkooporder. Daarom wordt u aangeraden de pakbonboeking uit de lading te gebruiken. In dit geval wordt de terugboeking ingeschakeld die moet worden uitgevoerd vanuit de lading.
