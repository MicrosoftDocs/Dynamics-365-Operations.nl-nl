---
title: Kan de wijziging van de voorraadstatus niet selecteren als werktype
description: U kunt geen werksjabloonregel maken voor de wijziging van de voorraadstatus, omdat het werktype alleen wordt gebruikt door systeemprocessen. Selecteer een ander werktype.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476046"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>Kan de wijziging van de voorraadstatus niet selecteren in de kolom Werktype

## <a name="symptoms"></a>Symptomen

Mogelijk wordt bij het configureren van Microsoft Dynamics 365 Supply Chain Management het volgende foutbericht weergegeven:

> U kunt geen werksjabloonregel maken voor de wijziging van de voorraadstatus, omdat het werktype niet geldig is. Selecteer een ander werktype.

## <a name="resolution"></a>Oplossing

Dit is zo ontworpen. Het werktype *Wijziging van voorraadstatus* wordt alleen door systeemprocessen gebruikt. Deze waarde kan niet worden geconfigureerd. Omdat de lijst met werktypen vast ligt als opsomming, kunnen de extra vermeldingen niet worden gefilterd uit de vervolgkeuzelijst **Werktype**.
