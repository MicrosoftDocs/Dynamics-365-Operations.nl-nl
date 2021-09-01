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
ms.openlocfilehash: cf307964a07c2b69eb5e4ef2cf9dc094482736d0970e333e84f674c9be6331c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740522"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a>Er wordt slechts één label afgedrukt voor meerdere werkkopteksten op één ontvangstbewijs

KB-nummer: 4614667

## <a name="symptoms"></a>Symptomen

Er worden meerdere werkkopteksten gemaakt voor dezelfde doelnummerplaat als onderdeel van één ontvangstgebeurtenis voor de magazijn-app. Wanneer het product binnen is, wordt echter slechts één nummerplaatlabel afgedrukt.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp.

In het huidige ontwerp wordt altijd één nummerplaatlabel gegenereerd, ongeacht het aantal bestaande combinaties van werkkoptekst en werkregel. Het gegenereerde label bevat de informatie voor slechts één combinatie.

Als u dit probleem wilt oplossen, moet u ervoor zorgen dat het maken van werkkopteksten altijd is toegewezen aan slechts één doelnummerplaat.
