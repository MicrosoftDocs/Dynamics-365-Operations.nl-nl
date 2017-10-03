--- 
title: Rente verwerken
description: Deze procedure laat zien hoe u rentenota's maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8a53c4deb146d336fdd8ca88a081e6a5af71465a
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="process-interest"></a>Rente verwerken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u rentenota's maakt, afdrukt en boekt. Bij deze taak wordt het demobedrijf USMF gebruikt.


## <a name="set-up-interest-on-the-posting-profile"></a>Rente instellen in het boekingsprofiel
1. Ga naar Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant.
2. Klik op Bewerken.
    * Selecteer een rentecode in de vervolgkeuzelijst. Als u geen rente wilt berekenen voor transacties met dit boekingsprofiel, laat u het veld leeg.  
    * Met het tabblad Tabelbeperking kunt u de methode wijzigen waarop rente wordt verwerkt. Als dit veld is ingesteld op Ja, wordt rente berekend voor dit boekingsprofiel.  

## <a name="calculate-interest"></a>Rente berekenen
1. Ga naar Crediteringen en aanmaningen > Rente > Rentenota's maken.
    * U moet de transactietypen selecteren waarvoor u rente wilt berekenen. Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.  
    * Als u Rente selecteert, wordt rente op rente berekend. U kunt de wetten die de berekening van rente op rente bepalen controleren voordat u deze transacties opneemt.  
    * Er wordt rente berekend vanaf deze datum tot aan de "Einddatum". Als u geen specifieke "Begindatum" opgeeft, worden alle niet-geboekte rentenota's geannuleerd en wordt de rente opnieuw berekend vanaf de transactiedatum.  
2. Voer de datum van de rentenota in.
    * Er zijn drie boekingsprofielopties: Rekening - gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor iedere rentenota.   Selecteren - Gebruik het boekingsprofiel dat u selecteert in het veld Boekingsprofiel.   Transactie - Gebruik het afzonderlijke boekingsprofiel van transacties waarbij rente wordt berekend voor elke rentenota. Transacties waaraan geen boekingsprofiel is toegewezen maken gebruik van het boekingsprofiel dat is opgegeven in het gebied Grootboek en btw van het formulier Parameters van module Klanten.  
    * Selecteer hier een boekingsprofiel als u "Boekingsprofiel gebruiken van" hebt gewijzigd in "Selecteren".  
3. Vouw de sectie Op te nemen records uit of samen.
4. Klik op Filter.
5. Voer in het veld Criteria een klant-id in. U kunt bijvoorbeeld 'US-001' invoeren.
6. Klik op OK.
7. Klik op OK.

## <a name="print-interest-notes"></a>Rentenota's afdrukken
1. Ga naar Crediteringen en aanmaningen > Rente > Rentenota's controleren en verwerken.
2. Selecteer 'Gemaakt' in het veld Status.
3. Selecteer 'Niet afgedrukt' in het veld Afgedrukt.
4. Klik op Afdrukken.
5. Vouw de sectie Op te nemen records uit of samen.
6. Klik op OK.
7. Sluit de pagina.

## <a name="post-the-interest-note"></a>De rentenota boeken
1. Selecteer een rentenota die gereed is om te worden geboekt (status is Gemaakt).
2. Klik op Boeken.
3. Voer de boekingsdatum voor de rentenota in.
    * Schakel Ja in om een grootboektransactie te maken voor elke rentenota.     Als u Ja niet inschakelt, wordt de rente op alle rentenota's aan de klant opgeteld en in één transactie naar het grootboek geboekt.  
4. Vouw de sectie Op te nemen records uit of samen.
5. Klik op OK.
6. Selecteer 'Geboekt' in het veld Status.


