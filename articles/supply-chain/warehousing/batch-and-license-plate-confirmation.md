---
title: Bevestiging van batch en nummerplaat
description: In dit onderwerp wordt beschreven hoe u bevestiging van batch en nummerplaat instelt en toepast vanaf een mobiel apparaat.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6454335989fe03a7332b6fb956667850896ffaf4
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="batch-and-license-plate-confirmation"></a>Bevestiging van batch en nummerplaat

[!include[banner](../includes/banner.md)]

Met batchbevestiging kunt u bevestigen dat de juiste batch van het mobiele apparaat wordt verzameld. Tijdens de eerste verzameling van werk voor alleen batch erboven-items waarbij batch erboven aangeeft dat de rangorde van de batch hoger is dan de locatie in de zoekhiërarchie, moet u controleren of de verzamelde batch overeenkomt met de batch op de werkregel. 

Met bevestiging van nummerplaat kunt u bevestigen dat de juiste nummerplaat van het mobiele apparaat wordt verzameld. Bij het verzamelen van werk vanaf een faseringslocatie moet u controleren of de nummerplaat die wordt verzameld, overeenkomt met de nummerplaat die aan het werk is gekoppeld. Als het werk wordt gestart door een nummerplaat te scannen, wordt deze bevestigingsstap overgeslagen.

## <a name="where-it-applies"></a>Waar van toepassing
Bevestiging is van toepassing in de volgende scenario's:

- Batchbevestiging is van toepassing op de eerste verzamelingen van werk voor batch erboven-items.
- Nummerplaatbevestiging is van toepassing op verzamelingen van faseringslocaties.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Bevestiging van batch en nummerplaat instellen
U kunt de batch- en nummerplaatbevestiging configureren via de menuopties van mobiele apparaten.  
1.  Voer de menuopties voor het mobiele apparaat onder de werkbevestigingsinstellingen in.  
2.  Selecteer de optie voor batch- of nummerplaatbevestiging. Beide opties zijn beschikbaar voor verzamelingen van het werktype waarvoor geen automatische bevestiging is ingeschakeld.  

