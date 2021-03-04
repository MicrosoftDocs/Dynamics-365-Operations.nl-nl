---
title: Rente verwerken
description: Deze procedure laat zien hoe u rentenota's maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441984"
---
# <a name="process-interest"></a>Rente verwerken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u rentenota's maakt, afdrukt en boekt. Bij deze taak wordt het demobedrijf USMF gebruikt.


## <a name="set-up-interest-on-the-posting-profile"></a>Rente instellen in het boekingsprofiel
1. Ga in het **navigatievenster** naar **Modules > Crediteringen en aanmaningen > Instellen > Boekingsprofielen van klant**.
2. Klik op **Bewerken**.
3. Selecteer op het sneltabblad **Instellingen** in het veld **Rentecode** een rentecode in de vervolgkeuzelijst. Als u geen rente wilt berekenen voor transacties met dit boekingsprofiel, laat u het veld leeg. Via het sneltabblad **Tabelbeperking** kunt u de methode wijzigen waarop rente wordt verwerkt. Als dit veld is ingesteld op Ja, wordt rente berekend voor dit boekingsprofiel.  

## <a name="calculate-interest"></a>Rente berekenen
1. Ga in het **navigatievenster** naar **Modules > Crediteringen en aanmaningen > Rente > Rentenota's maken**.
2. U moet de transactietypen selecteren waarvoor u rente wilt berekenen. Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.  
3. Als u **Rente** instelt op Ja, wordt rente op rente berekend. U kunt de wetten die de berekening van rente op rente bepalen controleren voordat u deze transacties opneemt.  
4. Voer in het veld **Begindatum** een begindatum voor de berekening van rente in. Als u geen specifieke **begindatum** opgeeft, worden alle niet-geboekte rentenota's geannuleerd en wordt de rente opnieuw berekend vanaf de transactiedatum.
5. Voer in het veld **Einddatum** een einddatum voor de berekening van rente in.
6. Selecteer een optie in het veld **Boekingsprofiel gebruiken van**. Er zijn drie boekingsprofielopties:
    - Rekening – Gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor iedere rentenota. 
    - Selecteren - Gebruik het boekingsprofiel dat u selecteert in het veld Boekingsprofiel.
    - Transactie - Gebruik het afzonderlijke boekingsprofiel van transacties waarbij rente wordt berekend voor elke rentenota. Transacties waaraan geen boekingsprofiel is toegewezen maken gebruik van het boekingsprofiel dat is opgegeven in het gebied Grootboek en btw van het formulier Parameters van module Klanten.  
7. Vouw het sneltabblad **Op te nemen records** uit.
8. Klik op **Filter**.
9. Voer in het veld **Criteria** een klant-id in. U kunt bijvoorbeeld 'US-001' invoeren.
6. Klik op **OK**.
7. Klik op **OK**.

## <a name="print-interest-notes"></a>Rentenota's afdrukken
1. Ga in het **navigatievenster** naar **Modules > Crediteringen en aanmaningen > Rente > Rentenota's controleren en verwerken**.
2. Selecteer Gemaakt in het veld **Status**.
3. Selecteer Niet afgedrukt in het veld **Afgedrukt**.
4. Klik op **Afdrukken**.
5. Vouw het sneltabblad **Op te nemen records** uit.
6. Klik op **OK**.
7. Sluit de pagina.

## <a name="post-the-interest-note"></a>De rentenota boeken
1. Selecteer een rentenota die gereed is om te worden geboekt (status is Gemaakt).
2. Klik op **Boeken**.
3. Voer de boekingsdatum voor de rentenota in. Schakel Ja in om een grootboektransactie te maken voor elke rentenota. Als u Ja niet inschakelt, wordt de rente op alle rentenota's aan de klant opgeteld en in één transactie naar het grootboek geboekt.  
4. Vouw het sneltabblad **Op te nemen records** uit.
5. Klik op **OK**.
6. Selecteer Geboekt in het veld **Status**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]