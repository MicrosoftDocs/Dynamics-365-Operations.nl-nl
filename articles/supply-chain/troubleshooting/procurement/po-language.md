---
title: Inkooporders reflecteren niet de taalinstellingen van de rechtspersoon
description: De productnaam op een inkooporder wordt weergegeven in de systeemtaal in plaats van de taal die is ingesteld voor de rechtspersoon waarvoor de inkooporder is gemaakt.
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
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476001"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Inkooporders reflecteren niet de taalinstellingen van de rechtspersoon


## <a name="symptoms"></a>Symptomen

De productnaam op een inkooporder wordt weergegeven in de systeemtaal in plaats van de taal die is ingesteld voor de rechtspersoon waarvoor de inkooporder is gemaakt.

## <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Stel de systeemtaal in op *en-US* (Amerikaans-Engels).
1. Zorg ervoor dat er een product is waarin de talen *en_US* en *de* (Duits) worden onderhouden voor vertalingen van de productnaam.
1. De taal van een rechtspersoon wijzigen in *de*.
1. Maak in de rechtspersoon waarvoor de taal *de* is ingesteld een inkooporder die het product bevat.
1. U ziet dat de productnaam nog steeds wordt weergegeven in Amerikaans Engels (de systeemtaal).

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. Op inkooporders wordt het product altijd weergegeven in de systeemtaal. De taal van de inkooporder wordt gebruikt bij het maken van een bevestigingsjournaal.
