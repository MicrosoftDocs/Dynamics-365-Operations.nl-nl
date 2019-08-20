---
title: Aanmaningen verwerken
description: Deze procedure laat zien hoe u aanmaningen maakt, afdrukt en boekt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
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
ms.openlocfilehash: 8db80b184d565f71f62f99051c7378c4e6e45fb9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834410"
---
# <a name="process-collection-letters"></a>Aanmaningen verwerken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u aanmaningen maakt, afdrukt en boekt. Bij deze taak wordt het demobedrijf USMF gebruikt.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Een aanmaningsreeks instellen op het boekingsprofiel
1. Ga naar **Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant**.
2. Klik op **Bewerken**.
3. Selecteer een aanmaningsreeks in de vervolgkeuzelijst. Als u geen aanmaningen wilt genereren voor transacties met dit boekingsprofiel, laat u het veld leeg.  
4. Vouw het tabblad Tabelbeperkingen uit om de methode te wijzigen waarmee aanmaningen worden verwerkt. Als dit veld is ingesteld op **Ja**, worden aanmaningen gemaakt voor dit boekingsprofiel.  

## <a name="create-collection-letters"></a>Aanmaningen maken
1. Ga naar **Crediteren en aanmaningen > Aanmaning > Aanmaningen maken**.
2. Selecteer de transactietypen waarvoor u aanmaningen wilt verzamelen. Alle openstaande transacties voor deze typen worden meegenomen bij de berekening.  
2. Selecteer een optie in het veld **Aanmaning**.
3. Voer de datum van de aanmaning in.
4. Selecteer een boekingsprofiel als u **Boekingsprofiel gebruiken van** hebt gewijzigd in **Selecteren**. Er zijn twee boekingsprofielopties:   
   - **Rekening** – Gebruik het boekingsprofiel dat aan de klantrekening is toegewezen voor iedere rentenota.   
   - **Selecteren** - Gebruik het boekingsprofiel dat u selecteert in het veld **Boekingsprofiel**.  
5. Vouw de sectie **Op te nemen records** uit.
6. Klik op **Filter**.
7. Voer in het veld **Criteria** een klant-id in. U kunt bijvoorbeeld 'US-001' invoeren.
8. Klik tot slot op **OK**.
9. Klik tot slot op **OK**.

## <a name="print-collection-letters"></a>Aanmaningen afdrukken
1. Ga naar **Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken**.
2. Selecteer **Gemaakt** in het veld **Status**.
3. Selecteer **Niet afgedrukt** in het veld **Afgedrukt**.
4. Klik op **Afdrukken**.
5. Klik op **Notitie bij aanmaning**.
6. Vouw de sectie **Op te nemen records** uit.
7. Geef de afsluitdatum voor boekingen op.
8. Klik op **OK** om de aanmaning af te drukken.
9. Boek de aanmaning.
   1. Klik op **Boeken**.
   2. Voer de boekingsdatum voor de aanmaning in
   3. Vouw de sectie **Op te nemen records** uit.
   4. Klik tot slot op **OK**.
   5. Selecteer **Geboekt** in het veld **Status**.
   6. Selecteer een optie in het veld **Afgedrukt**.

## <a name="control-collection-letters-at-the-customer-level"></a>Aanmaningen op klantniveau beheren
U kunt ook aanmaningen op het klantenniveau instellen zodat de aanmaningscode voor elke transactie wordt bijgehouden, maar de verwerking van de aanmaning wordt gebaseerd op één aanmaningsniveau dat wordt opgeslagen voor de klant. Deze ene aanmaning bevat alle achterstallige transacties voor de klant. Omdat de respijtdagen nu op het klantenniveau worden bijgehouden, wordt de volgende aanmaning pas verzonden als het aantal respijtdagen voor de volgende aanmaning in de reeks is verstreken, hoewel transacties achterstallig worden als de laatste aanmaning is verzonden. Met deze optie beperkt u het aantal aanmaningen dat u per klant verzendt. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>De klant configureren om aanmaningen op klantniveau te beheren
1.  Ga naar **Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten** en klik op het tabblad **Aanmaningen**. 
2.  Wijzig de waarde van **Aanmaning maken per** in **Klant**. 
3.  Ga naar **Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken**. Voor de klant wordt slechts één aanmaning met alle achterstallige transacties gegenereerd.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode
Als u betalingen en creditnota's opneemt in de transacties die worden opgenomen in de aanmaningen, hebt u mogelijk betalingen of creditnota's die een aanmaning activeren. U kunt bepalen hoe betalingen en creditnota's de aanmaningscode de aanmaningscode bepalen door de waarde van de parameter **Betalingen en creditnota's negeren bij het berekenen van aanmaningscode** te wijzigen. 

Ga als volgt te werk om betalingen en creditnota's te negeren bij het berekenen van de aanmaningscode.
1. Ga naar **Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten** en klik op het tabblad **Aanmaningen**. 
2. Wijzig de waarde van **Betalingen en creditnota's negeren bij het berekenen van aanmaningscode** in **Ja**.
