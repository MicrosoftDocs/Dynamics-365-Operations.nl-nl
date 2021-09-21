---
title: Artikel RM kan niet worden gereserveerd wanneer een productieorder wordt vrijgegeven
description: Wanneer u een productieorder vrijgeeft, wordt mogelijk de fout 'Artikel RM kan niet volledig worden gereserveerd' weergegeven. Zorg ervoor dat de volledige hoeveelheid beschikbaar is of reserveer artikelen handmatig.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476039"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Artikel RM kan niet volledig worden gereserveerd wanneer een productieorder wordt vrijgegeven

## <a name="symptoms"></a>Symptomen

Als niet alle stuklijstregelartikelen fysiek beschikbaar zijn wanneer een productieorder naar een magazijn wordt vrijgegeven en het beleid **Vrijgave naar magazijn** is ingesteld op *Volledige reservering vereisen*, wordt het volgende foutbericht weergegeven:

> Artikel RM kan niet volledig worden gereserveerd. Controleer of de volledige hoeveelheid beschikbaar is of reserveer de artikelen handmatig als het veld Reservering op de stuklijstregel is ingesteld op Handmatig of Begonnen. Kon de order niet vrijgeven aan magazijn omdat sommige materialen niet konden worden gereserveerd.

## <a name="resolution"></a>Oplossing

Dit gedrag is inherent aan het ontwerp en is zoals verwacht. U kunt het probleem oplossen door de richtlijnen in het foutbericht te volgen: 'Zorg ervoor dat de volledige hoeveelheid beschikbaar is of reserveer de artikelen handmatig als het veld Reservering op de stuklijstregel is ingesteld op Handmatig of Gestart.'
