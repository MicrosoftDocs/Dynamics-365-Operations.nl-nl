---
title: Bundelartikel wordt niet ondersteund in een intercompany-proces
description: Het bundelartikel is niet beschikbaar voor aankoop. De verkooporder koopt alleen de onderdelen van het bundelartikel, niet het bundelartikel zelf.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476014"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Een bundelartikel wordt niet ondersteund in een intercompany-proces

## <a name="symptoms"></a>Symptomen

Het bundelartikel is niet beschikbaar voor de inkooporder, want als u de verkooporderregels voor het bundelartikel bekijkt, ziet u dat de hoeveelheid *0* (nul) is en de status *Geannuleerd*.

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. In de verkooporder worden alleen de onderdelen van het bundelartikel gekocht. In de verkooporder wordt niet het bundelartikel zelf gekocht. Als u een bundel moet aanschaffen, overweeg dan of u deze als een bundelartikel moet markeren, omdat deze functionaliteit eigenlijk is bedoeld voor opbrengsttoerekeningsscenario's. Meer informatie over bundelartikelen vindt u in [Bundels](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
