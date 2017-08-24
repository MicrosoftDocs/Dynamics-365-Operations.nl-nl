--- 
title: Een hoofdplanningsuitvoering controleren
description: De productieplanner wil zien of er een hoofdplanning wordt uitgevoerd.
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8eb19ac9ded4dc2a091ff733f2f43cb6cafa1b43
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="monitor-a-master-planning-run"></a>Een hoofdplanningsuitvoering controleren

[!include[task guide banner](../../includes/task-guide-banner.md)]

De productieplanner wil zien of er een hoofdplanning wordt uitgevoerd. Gebruik het demobedrijf USMF om deze procedure te voltooien.


## <a name="run-master-planning"></a>Hoofdplanning uitvoeren
1. Klik op Hoofdplanning.
    * U vindt dit in het standaarddashboard.  
2. Typ of selecteer een waarde in het veld Plan.
    * Voorbeeld: StaticPlan  
3. Klik op Uitvoeren.
4. Selecteer Ja in het veld Verwerkingstijd traceren.
    * Als het veld al is geselecteerd, slaat u deze stap over.  
5. Voer een getal in het veld Aantal threads in.
6. Breid de sectie Op te nemen records uit.
7. Klik op Filter.
8. Markeer in de lijst de geselecteerde rij.
    * Markeer de rij waarin Veld = Artikelnummer.  
9. Typ of selecteer een waarde in het veld Criteria.
    * Voorbeeld: T0001  
10. Klik op OK.
11. Klik op OK.

## <a name="monitor-the-master-planning-run"></a>De hoofdplanningsuitvoering controleren
1. Klik op Historie.
2. Klik op Query's.
3. Klik op Duur procestaak.
4. Zoek en selecteer de gewenste record in de lijst.
    * Voor elk artikel kunt u een overzicht krijgen van de tijd die de voltooiing van elke planningsstap in beslag nam.  


