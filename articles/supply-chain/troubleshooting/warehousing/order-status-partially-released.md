---
title: Orderstatus blijft Gedeeltelijk vrijgegeven nadat deze is gefactureerd
description: In sommige gevallen blijft de status van een verkooporder Gedeeltelijk vrijgegeven, zelfs nadat de verkooporder is gefactureerd. Op deze pagina wordt uitgelegd waarom en wordt een mogelijke oplossing gegeven.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476022"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>De orderstatus blijft Gedeeltelijk vrijgegeven, zelfs nadat de verkooporder is gefactureerd

## <a name="symptoms"></a>Symptomen

Een verkooporder is een leveringsorder, maar een of meer artikelen op de order hebben een andere leveringsmethode. Nadat de order is gefactureerd, heeft deze nog steeds de vrijgavestatus *Gedeeltelijk vrijgegeven*.

Een verkooporder heeft bijvoorbeeld twee artikelen: een voor levering en een voor ophalen. De levering en het ophalen zijn voltooid. Daarom zijn beide regels gefactureerd. De vrijgavestatus wordt echter nog steeds weergegeven als *Gedeeltelijk vrijgegeven*. Dit is misleidend.

## <a name="workaround"></a>Tijdelijke oplossing

De vrijgavestatus is alleen van toepassing op orderregels met artikelen waarvoor magazijnbeheer is ingeschakeld. Daarom blijft de vrijgavestatus *Gedeeltelijk vrijgegeven* in dit scenario. Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. Een uitbreiding kan worden toegevoegd als onderdeel van de pakbon en het factureringsproces om de vrijgavestatus bij te werken.
