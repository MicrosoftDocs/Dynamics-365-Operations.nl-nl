---
title: Door het annuleren van het restant van de levering wordt de status van de inkooporder gewijzigd in Bevestigd
description: Als een restant van een levering wordt geannuleerd op een inkooporder waarvoor wijzigingsbeheer is ingeschakeld, krijgt de inkooporder de status Bevestigd
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476024"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Door het annuleren van het restant van de levering wordt de status van de inkooporder gewijzigd in Bevestigd

## <a name="symptoms"></a>Symptomen

Als een inkooporder is onderworpen aan wijzigingsbeheer en de enige wijziging die wordt aangevraagd, de annulering van een leveringsrestant op een of meer van de regels is, krijgt de inkooporder weer direct de status *Bevestigd* bevestigd wanneer deze wordt goedgekeurd en wordt er geen journaal gemaakt.

## <a name="resolution"></a>Oplossing

Annulering van een restant van de levering heeft geen invloed op de inhoud van het bevestigingsjournaal. Deze functionaliteit moet worden gebruikt wanneer de regel gedeeltelijk is ontvangen en de resterende kwaliteit in de processtap moet worden geannuleerd nadat de inkooporder met de leverancier is bevestigd.

Als dit op de bevestiging van de inkoopordermoet worden weergegeven, moet de hoeveelheid op de inkooporderregel zo worden gecorrigeerd dat de bevestiging is vereist. Als er niets op de regel is ontvangen, kan de hoeveelheid worden verwijderd. In dit geval is herbevestiging vereist.
