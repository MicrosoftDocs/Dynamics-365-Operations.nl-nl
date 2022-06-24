---
title: Bevestiging van batch en nummerplaat
description: In dit artikel wordt beschreven hoe u bevestiging van batch en nummerplaat instelt en toepast vanaf een mobiel apparaat.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef0d528d23c1ee9424e35e29d39121d42ba548e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903719"
---
# <a name="batch-and-license-plate-confirmation"></a>Bevestiging van batch en nummerplaat

[!include [banner](../includes/banner.md)]

Met batchbevestiging kunt u bevestigen dat de juiste batch van het mobiele apparaat wordt verzameld. Tijdens de eerste verzameling van werk voor alleen *Batch-boven\[locatie\]*-artikelen waarbij batch erboven aangeeft dat de rangorde van de batch hoger is dan de locatie in de zoekhiërarchie, moet u controleren of de verzamelde batch overeenkomt met de batch op de werkregel.

Met bevestiging van nummerplaat kunt u bevestigen dat de juiste nummerplaat van het mobiele apparaat wordt verzameld. Bij het verzamelen van werk vanaf een faseringslocatie moet u controleren of de nummerplaat die wordt verzameld, overeenkomt met de nummerplaat die aan het werk is gekoppeld. Als het werk wordt gestart door een nummerplaat te scannen, wordt deze bevestigingsstap overgeslagen.

## <a name="where-it-applies"></a>Waar van toepassing

Bevestiging is van toepassing in de volgende scenario's:

- Batchbevestiging is van toepassing op de eerste verzamelingen van werk voor batch erboven-items.
- Nummerplaatbevestiging is van toepassing op verzamelingen van faseringslocaties.

> [!IMPORTANT]
> Aanvulling wordt niet ondersteund voor bevestiging van de nummerplaat. Bij de uitvoering van aanvullingswerkzaamheden wordt er geen bevestigingsstap voor de nummerplaat gemaakt.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Bevestiging van batch en nummerplaat instellen

U kunt de batch- en nummerplaatbevestiging configureren via de menuopties van mobiele apparaten.

1. Voer de menuopties voor het mobiele apparaat onder de werkbevestigingsinstellingen in.  
1. Selecteer de optie voor batch- of nummerplaatbevestiging. Beide opties zijn beschikbaar voor verzamelingen van het werktype waarvoor geen automatische bevestiging is ingeschakeld.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
