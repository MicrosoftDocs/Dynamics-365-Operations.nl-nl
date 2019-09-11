---
title: Aanmaningen verwerken
description: In dit onderwerp leest u hoe u aanmaningen maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867650"
---
# <a name="process-collection-letters"></a>Aanmaningen verwerken

[!include [banner](../../includes/banner.md)]

In dit onderwerp leest u hoe u aanmaningen maakt, afdrukt en boekt. Bij deze taak wordt het demobedrijf USMF gebruikt.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Een aanmaningsreeks instellen op het boekingsprofiel
1. Ga naar **Navigatievenster > Modules > Crediteringen en aanmaningen > Instellen > Boekingsprofielen van klant**.
2. Klik op **Bewerken**.
3. Selecteer een aanmaningsreeks in de vervolgkeuzelijst. Als u geen aanmaningen wilt genereren voor transacties met dit boekingsprofiel, laat u het veld leeg.  
4. Vouw het tabblad **Tabelbeperkingen** uit om de methode te wijzigen waarmee aanmaningen worden verwerkt. Als dit veld is ingesteld op **Ja**, worden aanmaningen gemaakt voor dit boekingsprofiel.  

## <a name="create-collection-letters"></a>Aanmaningen maken
1. Ga naar **Navigatievenster > Modules > Crediteren en aanmaningen > Aanmaning > Aanmaningen maken**.
2. Selecteer de transactietypen waarvoor u aanmaningen wilt verzamelen. Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.  
3. Selecteer een optie in het veld **Aanmaning**.
4. Voer in het veld **Aanmaningsdatum** de datum van de aanmaning in.
5. Selecteer een boekingsprofiel als u **Boekingsprofiel gebruiken van** hebt gewijzigd in **Selecteren**. Er zijn twee boekingsprofielopties:   

   - **Rekening** – Gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor iedere rentenota.   
   - **Selecteren** - Gebruik het boekingsprofiel dat u selecteert in het veld **Boekingsprofiel**.  

6. Vouw de sectie **Op te nemen records** uit.
7. Selecteer **Filter**.
8. Voer in het veld **Criteria** een klant-id in. U kunt bijvoorbeeld 'US-001' invoeren.
9. Selecteer **OK**.
10. Selecteer **OK**.

## <a name="print-collection-letters"></a>Aanmaningen afdrukken
1. Ga naar **Navigatievenster > Modules > Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken**.
2. Selecteer **Gemaakt** in het veld **Status**.
3. Selecteer **Niet afgedrukt** in het veld **Afgedrukt**.
4. Selecteer **Afdrukken**.
5. Selecteer **Notitie bij aanmaning**.
6. Voer in de sectie **Parameters** de afsluitdatum voor boekingen in.
7. Vouw de sectie **Op te nemen records** uit en voer de details van de notitie van de aanmaning in.
8. Selecteer **OK** om de aanmaning af te drukken.
9. Boek de aanmaning.

    1. Selecteer **Boeken**.
    1. Voer de boekingsdatum voor de aanmaning in
    1. Vouw de sectie **Op te nemen records** uit.
    1. Selecteer **OK**.
    1. Selecteer **Geboekt** in het veld **Status**.
    1. Selecteer een optie in het veld **Afgedrukt**.

## <a name="control-collection-letters-at-the-customer-level"></a>Aanmaningen op klantniveau beheren
U kunt ook aanmaningen op het klantenniveau instellen zodat de aanmaningscode voor elke transactie wordt bijgehouden, maar de verwerking van de aanmaning wordt gebaseerd op één aanmaningsniveau dat wordt opgeslagen voor de klant. Deze ene aanmaning bevat alle achterstallige transacties voor de klant. Omdat de respijtdagen nu op het klantenniveau worden bijgehouden, wordt de volgende aanmaning pas verzonden als het aantal respijtdagen voor de volgende aanmaning in de reeks is verstreken, hoewel transacties achterstallig worden als de laatste aanmaning is verzonden. Met deze optie beperkt u het aantal aanmaningen dat u per klant verzendt. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>De klant configureren om aanmaningen op klantniveau te beheren
1.  Ga naar **Navigatievenster > Modules > Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten** en selecteer het tabblad **Aanmaningen**. 
2.  Wijzig de waarde van **Aanmaning maken per** in **Klant**. 
3.  Ga naar **Navigatievenster > Modules > Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken**. Voor de klant wordt slechts één aanmaning met alle achterstallige transacties gegenereerd.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode
Als u betalingen en creditnota's opneemt in de transacties die worden opgenomen in de aanmaningen, hebt u mogelijk betalingen of creditnota's die een aanmaning activeren. U kunt bepalen hoe betalingen en creditnota's de aanmaningscode de aanmaningscode bepalen door de waarde van de parameter **Betalingen en creditnota's negeren bij het berekenen van aanmaningscode** te wijzigen. 

Ga als volgt te werk om betalingen en creditnota's te negeren bij het berekenen van de aanmaningscode.

1. Ga naar **Navigatievenster > Modules > Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten** en klik op het tabblad **Aanmaningen**. 
2. Wijzig de waarde van **Betalingen en creditnota's negeren bij het berekenen van aanmaningscode** in **Ja**.
