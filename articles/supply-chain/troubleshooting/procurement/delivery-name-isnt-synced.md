---
title: Nadat het afleveradres in een inkooporder is gewijzigd, wordt de leveringsnaam niet gesynchroniseerd
description: Nadat het afleveradres in de kop van een inkooporder is gewijzigd, wordt de leveringsnaam niet gesynchroniseerd
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
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475980"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Nadat het afleveradres in een inkooporder is gewijzigd, wordt de leveringsnaam niet gesynchroniseerd

## <a name="symptoms"></a>Symptomen

Het adres in de koptekst van een inkooporder wordt bijgewerkt naar een adres dat geen afleveradres is. Hoewel het adres op de inkooporder wordt bijgewerkt, wordt de leveringsnaam niet bijgewerkt op basis van het bijgewerkte adres.

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. Het geselecteerde adres moet worden geclassificeerd als afleveradres. Anders wordt de leveringsnaam niet bijgewerkt op basis van het geselecteerde adres.
