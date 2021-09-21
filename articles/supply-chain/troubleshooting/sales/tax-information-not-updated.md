---
title: De belastinggegevens worden niet bijgewerkt als de locatie in de verkooporder wordt gewijzigd
description: Als de locatie, het magazijn of het afleveradres wordt gewijzigd in de koptekst van een verkooporder, wordt de belastinginformatie voor de aanvraag niet automatisch bijgewerkt voor de regels. U moet dit handmatig doen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77a73a787ff8a174c575f3b4f75694ded45d5712
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476016"
---
# <a name="tax-information-isnt-updated-if-location-on-a-sales-order-header-is-changed"></a>De belastinggegevens worden niet bijgewerkt als de locatie in de verkooporderkoptekst wordt gewijzigd

## <a name="symptoms"></a>Symptomen

Als de locatie, het magazijn of het afleveradres wordt gewijzigd in de koptekst van een verkooporder, wordt de belastinginformatie voor de aanvraag niet automatisch bijgewerkt voor de regels.

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. Het probleem doet zich voor omdat het afleveradres, de locatie en het magazijn niet automatisch op regelniveau worden gewijzigd. U moet ze handmatig bijwerken.
