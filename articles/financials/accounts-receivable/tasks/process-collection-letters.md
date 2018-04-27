--- 
title: Aanmaningen verwerken
description: Deze procedure laat zien hoe u aanmaningen maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Aanmaningen verwerken

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u aanmaningen maakt, afdrukt en boekt. Bij deze taak wordt het demobedrijf USMF gebruikt.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Een aanmaningsreeks instellen op het boekingsprofiel
1. Ga naar Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant.
2. Klik op Bewerken.
    * Selecteer een aanmaningsreeks in de vervolgkeuzelijst. Als u geen aanmaningen wilt genereren voor transacties met dit boekingsprofiel, laat u het veld leeg.  
    * Met het tabblad Tabelbeperking kunt u de methode wijzigen waarmee aanmaningen worden verwerkt. Als dit veld is ingesteld op Ja, worden aanmaningen gemaakt voor dit boekingsprofiel.  
3. Sluit de pagina.

## <a name="create-collection-letters"></a>Aanmaningen maken
1. Ga naar Crediteren en aanmaningen > Aanmaning > Aanmaningen maken.
    * U moet de transactietypen selecteren waarvoor u aanmaningen wilt verzamelen. Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.  
2. Selecteer een optie in het veld Aanmaning.
3. Voer de datum van de aanmaning in.
    * Er zijn twee boekingsprofielopties: Rekening: gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor elke rentenota.   Selecteren - Gebruik het boekingsprofiel dat u selecteert in het veld Boekingsprofiel.  
    * Selecteer een boekingsprofiel als u 'Boekingsprofiel gebruiken van' hebt gewijzigd in 'Selecteren'.  
4. Breid de sectie Op te nemen records uit.
5. Klik op Filter.
6. Voer in het veld Criteria een klant-id in. U kunt bijvoorbeeld 'US-001' invoeren.
7. Klik op OK.
8. Klik op OK.

## <a name="print-collection-letters"></a>Aanmaningen afdrukken
1. Ga naar Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken.
2. Selecteer 'Gemaakt' in het veld Status.
3. Selecteer 'Niet afgedrukt' in het veld Afgedrukt.
4. Klik op Afdrukken.
5. Klik op Notitie bij aanmaning.
6. Breid de sectie Op te nemen records uit.
7. De afsluitdatum voor boekingen opgeven
8. Klik op OK om de aanmaning af te drukken.

## <a name="post-the-collection-letter"></a>De aanmaning boeken
1. Klik op Boeken.
2. Voer de boekingsdatum voor de aanmaning in
3. Breid de sectie Op te nemen records uit.
4. Klik op OK.
5. Selecteer 'Geboekt' in het veld Status.
6. Selecteer een optie in het veld Afgedrukt.


