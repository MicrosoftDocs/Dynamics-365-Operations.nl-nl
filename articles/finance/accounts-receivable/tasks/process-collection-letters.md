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
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: a189bbdd360d07b2b5198fa357380fd9a89ac167
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992959"
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
Als aanmaningen worden ingesteld op het transactieniveau, kunnen er meerdere brieven worden gegenereerd voor een klant, gebaseerd op hoelang geleden een transactie heeft plaatsgevonden. Als transacties in verschillende letterreeksen voorkomen, worden afzonderlijke aanmaningen gegenereerd voor elke groep met achterstallige transacties voor de klant. Daarom kan een afzonderlijke klant bijvoorbeeld een aanmaning ontvangen voor transacties die 60 dagen achterstallig zijn en een andere aanmaning voor transacties die 90 dagen achterstallig zijn. 

Elke aanmaning wordt ook gekoppeld aan een aanmaningscode. De aanmaningscode is gekoppeld aan afzonderlijke transacties en wordt gebruikt om te bepalen wanneer de volgende aanmaning moet worden gegenereerd voor elke transactie. Als een transactie bijvoorbeeld meer dan 30 dagen achterstallig is, wordt met de aanmaningscode bepaald dat de volgende aanmaning wordt verzonden wanneer de transactie na 60 dagen nog niet is betaald. 

Aanmaningen kunnen ook worden ingesteld op klantniveau. In dit geval wordt de aanmaningscode voor elke transactie bijgehouden, maar de verwerking van de aanmaning wordt gebaseerd op één aanmaningsniveau dat wordt opgeslagen voor de klant. Deze ene aanmaning bevat alle achterstallige transacties voor de klant. Omdat de respijtdagen nu op het klantniveau worden bijgehouden, wordt de volgende aanmaning pas verzonden als het aantal respijtdagen voor de volgende aanmaning in de reeks is verstreken, hoewel transacties achterstallig worden als de laatste aanmaning is verzonden. Met deze optie beperkt u het aantal aanmaningen dat u per klant moet verzenden.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>De klant configureren om aanmaningen op klantniveau te beheren
1.  Ga naar **Navigatievenster > Modules > Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten** en selecteer het tabblad **Aanmaningen**. 
2.  Wijzig de waarde van **Aanmaning maken per** in **Klant**. 
3.  Ga naar **Navigatievenster > Modules > Crediteren en aanmaningen > Aanmaning > Aanmaningen controleren en verwerken**. Voor de klant wordt slechts één aanmaning met alle achterstallige transacties gegenereerd.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Betalingen en creditnota's negeren bij het berekenen van de aanmaningscode
Als u betalingen en creditnota's opneemt in de transacties die worden opgenomen in de aanmaningen, hebt u mogelijk betalingen of creditnota's die een aanmaning activeren. U kunt bepalen hoe betalingen en creditnota's de aanmaningscode de aanmaningscode bepalen door de waarde van de parameter **Betalingen en creditnota's negeren bij het berekenen van aanmaningscode** te wijzigen. 

Ga als volgt te werk om betalingen en creditnota's te negeren bij het berekenen van de aanmaningscode.

1. Ga naar **Navigatievenster > Modules > Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten** en klik op het tabblad **Aanmaningen**. 
2. Wijzig de waarde van **Betalingen en creditnota's negeren bij het berekenen van aanmaningscode** in **Ja**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]