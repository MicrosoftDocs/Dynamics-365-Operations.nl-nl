--- 
title: Gepostdateerde cheques instellen
description: In dit onderwerp wordt uitgelegd hoe u kunt opgeven of journaalposten voor gepostdateerde cheques moeten worden geboekt en welke boekingsjournalen moeten worden gebruikt om transacties en leveranciersbetalingen te wissen.
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: be0bf9e091b198f054745b29fa24318cee0b69ab
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-postdated-checks"></a>Gepostdateerde cheques instellen

[!include[task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd hoe u kunt opgeven of journaalposten voor gepostdateerde cheques moeten worden geboekt en welke boekingsjournalen moeten worden gebruikt om transacties en leveranciersbetalingen te wissen. U kunt tijdelijke rekeningen opgeven voor uitgegeven cheques, ontvangen cheques en bronbelasting. Gepostdateerde cheques zijn cheques die worden uitgegeven om betalingen op een datum in de toekomst uit te voeren en te ontvangen. U kunt opgeven of de cheque vóór de vervaldatum in uw boekhoudingsstukken moet worden weerspiegeld.



De rol van deze procedure is penningmeester. Bij deze procedure wordt het demobedrijf USMF gebruikt.


## <a name="set-up-postdated-checks"></a>Gepostdateerde cheques instellen
1. Ga naar Contanten en bankbeheer > Instellingen > Parameters voor kas- en bankbeheer.
2. Klik op het tabblad Gepostdateerde cheques.
3. Schakel het selectievakje Gepostdateerde cheques inschakelen in of uit.
4. Schakel het selectievakje Journaalboekingen voor gepostdateerde cheques uitvoeren in of uit.
5. Geef in het veld Aflossingsrekening voor uitgegeven cheques de gewenste waarden op.
6. Geef in het veld Aflossingsrekening voor ontvangen cheques de gewenste waarden op.
7. Typ een waarde in het veld Algemeen journaal voor aflossingstransacties.
8. Typ een waarde in het veld Gepostdateerde cheques overboeken naar dit leveranciersbetalingsjournaal.
9. Geef de gewenste waarden op in het veld Aflossingsrekening bronbelasting.
10. Klik op Opslaan.
11. Sluit de pagina.
12. Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.
13. Klik op Nieuw.
14. Typ een waarde in het veld Betalingsmethode.
15. Selecteer de optie Boeking van aflossing gepostdateerde cheque om aan te geven dat het bedrag van de cheque naar een tijdelijke rekening wordt geboekt.
16. Selecteer Bank in het veld Bankrekening.
    * De tegenrekening van de betalingsmethode zal een bank zijn.  
17. Geef in het veld Betalingsrekening de gewenste waarden op.
    * Selecteer de bankrekening die wordt gebruikt om het factuurbedrag af te trekken.  
18. Sluit de pagina.
19. Ga naar Klanten > Betalingsinstelling > Betalingsmethoden
20. Klik op Nieuw.
21. Typ een waarde in het veld Betalingsmethode.
22. Selecteer de optie Boeking van aflossing gepostdateerde cheque om aan te geven dat het bedrag van de cheque naar een tijdelijke rekening wordt geboekt.
23. Selecteer Bank in het veld Bankrekening.
    * De tegenrekening van de betalingsmethode zal een bank zijn.  
24. Geef in het veld Betalingsrekening de gewenste waarden op.
    * Selecteer de bankrekening die wordt gebruikt om het factuurbedrag af te trekken.  
25. Sluit de pagina.


