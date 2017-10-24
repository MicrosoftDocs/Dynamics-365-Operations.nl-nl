--- 
title: Een plan met beperkingen genereren
description: Deze procedure laat zien hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt.
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a>Een plan met beperkingen genereren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een plan maakt dat zowel met materiaal- als capaciteitsbeperkingen rekening houdt. Het plan garandeert dat de productie niet start voordat de materialen beschikbaar zijn en dat resources niet worden overboekt. 

Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de productieplanner.


## <a name="set-up-a-constrained-plan"></a>Een plan met beperkingen instellen
1. Klik op Hoofdplanning.
2. Klik op Hoofdplannen.
3. Zoek en selecteer de gewenste record in de lijst.
    * Voorbeeld: StaticPlan  
4. Selecteer Ja in het veld Eindige capaciteit.
5. Voer 30 in het veld Tijdlimiet beperkte capaciteit in.
6. Vouw de sectie Time fences in dagen uit.
7. Selecteer Ja in het veld Capaciteit.
8. Voer in het veld Time fence capaciteitsplanning (dagen) een nummer in.
    * Voorbeeld: 60  
9. Selecteer Ja in het veld Berekende vertragingen.
10. Voer in het veld Time fence vertragingen berekenen (dagen) een nummer in.
    * Voorbeeld: 60  
11. Vouw de sectie Berekende vertragingen uit.
12. Selecteer Ja in het veld De berekende vertraging optellen bij de behoeftedatum.
13. Selecteer Ja in het veld De berekende vertraging optellen bij de behoeftedatum.
14. Selecteer Ja in het veld De berekende vertraging optellen bij de behoeftedatum.
15. Sluit de pagina.

## <a name="create-a-constrained-plan"></a>Plan met beperkingen maken
1. Klik op Uitvoeren.
2. Typ of selecteer een waarde in het veld Hoofdplan.
    * Selecteer het plan waarvoor u beperkingen hebt ingesteld.  
3. Klik op OK.
    * Dit kan enige tijd duren.  
4. Klik op Geplande orders.


