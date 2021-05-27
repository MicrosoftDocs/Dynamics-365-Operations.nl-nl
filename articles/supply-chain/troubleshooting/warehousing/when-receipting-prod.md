---
title: Er wordt slechts één label afgedrukt voor meerdere werkkopteksten op één ontvangstbewijs
description: Er wordt slechts één label afgedrukt voor meerdere werkkopteksten op één ontvangstbewijs.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026404"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Er wordt slechts één label afgedrukt voor meerdere werkkopteksten op één ontvangstbewijs

KB-nummer: 4614667

## <a name="symptoms"></a>Symptomen

Er worden meerdere werkkopteksten gemaakt voor dezelfde doelnummerplaat als onderdeel van één ontvangstgebeurtenis voor de magazijn-app. Wanneer het product binnen is, wordt echter slechts één nummerplaatlabel afgedrukt.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp.

In het huidige ontwerp wordt altijd één nummerplaatlabel gegenereerd, ongeacht het aantal bestaande combinaties van werkkoptekst en werkregel. Het gegenereerde label bevat de informatie voor slechts één combinatie.

Als u dit probleem wilt oplossen, moet u ervoor zorgen dat het maken van werkkopteksten altijd is toegewezen aan slechts één doelnummerplaat.
