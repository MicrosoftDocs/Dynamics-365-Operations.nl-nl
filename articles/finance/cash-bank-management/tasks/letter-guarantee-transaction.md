---
title: Borgstellingstransactie
description: Deze procedure begeleidt u door het proces van de borgstelling.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 786aecf69bae3d07ac80a55b4dc835dd8129bd59
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803959"
---
# <a name="letter-of-guarantee-transaction"></a>Borgstellingstransactie

[!include [banner](../../includes/banner.md)]

Deze procedure begeleidt u door het proces van de borgstelling.



De volgende taken moeten zijn voltooid voordat u deze procedure start.

- Stel bankfaciliteiten en boekingsprofielen in voor een borgstelling.

- Een bankfaciliteitsovereenkomst maken voor een borgstelling.



Bij deze procedure wordt het demobedrijf USMF gebruikt.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Verkooporder met borgstelling maken
1. Ga naar **Klanten > Orders > Alle verkooporders**.
2. Klik op **Nieuw**.
3. Typ of selecteer een waarde in het veld **Klantrekening**.
4. Vouw de sectie **Algemeen** uit.
5. Typ of selecteer een waarde in het veld **Locatie**.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Typ of selecteer een waarde In het veld **Magazijn**.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Selecteer **Borgstelling** in het veld **Type bankdocument**.
10. Klik op **OK**.
11. Typ of selecteer een waarde in het veld **Artikelnummer**.
12. Voer een nummer in het veld **Eenheidsprijs** in.
13. Vouw de sectie **Regeldetails** uit.
14. Klik op het tabblad **Levering**.

>[!Note] 
>Selecteer **Controle van leveringsdatum** = **Geen**  

15. Typ een datum in het veld **Gewenste verzenddatum**.
16. Typ een datum in het veld **Bevestigde verzenddatum**.

## <a name="process-letter-of-guarantee_request"></a>Borgstellingsaanvraag verwerken
1. Klik in het actievenster op **Beheren**.
2. Klik op **Borgstelling**.
3. Klik in het actievenster op **Borgstelling**.
4. Klik op **Aanvraag** om het dialoogvenster te openen.
5. Typ of selecteer een waarde in het veld **Type**.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Typ een getal in het veld **Waarde**.
8. Voer in het veld **Vervaldatum** een datum en tijd in.
9. Klik op **OK**.
10. Sluit de pagina.

## <a name="process-letter-of-guarantee_submit-to-bank"></a>Borgstelling Indienen bij bank verwerken
1. Ga naar **Contanten en bankbeheer > Borgstellingen > Borgstellingen**.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik op **Indienen bij bank** om het dialoogvenster te openen.
4. Typ of selecteer een waarde in het veld **Bankrekening**.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op **OK**.

## <a name="process-letter-of-guarantee_receive-from-bank"></a>Borgstelling Ontvangen van bank verwerken
1. Klik op **Ontvangen van bank** om het dialoogvenster te openen.
2. Typ een waarde in het veld **Banknummer**.
    * Controleer de waarden in de berekende velden **Marge** en **Onkosten**.  
3. Klik op **OK**.
4. Vouw de sectie **Acties** uit.
    * Controleer de record 'Ontvangen van bank'.  
5. Klik om de koppeling in het veld **Journaalbatchnummer** te volgen.
6. Klik op **Regels**.
    * Controleer de boeking van journaalposten.  
7. Sluit de pagina.

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a>Borgstelling Geven aan begunstigde verwerken
1. Ga naar **Klanten > Orders > Alle verkooporders**.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
3. Klik in het actievenster op **Beheren**.
4. Klik op **Borgstelling**.
5. Klik in het actievenster op **Borgstelling**.
6. Klik op **Geven aan begunstigde** om het dialoogvenster te openen.
7. Klik op **OK**.
8. Ga naar **Contanten en bankbeheer > Borgstellingen > Borgstellingen**.
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik op **Geven aan begunstigde** om het dialoogvenster te openen.
11. Klik op **OK**.
12. Vouw de sectie **Acties** uit.
    * Valideer de record 'Geven aan begunstigde'.  

## <a name="process-letter-of-guarantee_increase-value"></a>Borgstelling Waarde verhogen verwerken
1. Ga naar **Klanten > Orders > Alle verkooporders**.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
3. Klik in het actievenster op **Beheren**.
4. Klik op **Borgstelling**.
5. Klik in het actievenster op **Borgstelling**.
6. Klik op **Waarde verhogen** om het dialoogvenster te openen.
7. Typ een getal in het veld **Toe te voegen waarde**.
8. Klik op **OK**.
9. Ga naar **Contanten en bankbeheer > Borgstellingen > Borgstellingen**.
10. Zoek en selecteer de gewenste record in de lijst.
11. Klik op **Waarde verhogen** om het dialoogvenster te openen.
12. Klik op **OK**.
13. Vouw de sectie **Acties** uit.
    * Controleer de record 'Waarde verhogen'.  
14. Zoek en selecteer de gewenste record in de lijst.
15. Klik om de koppeling in het veld **Journaalbatchnummer** te volgen.
16. Klik op **Regels**.
    * Controleer de geboekt journaalposten.  

## <a name="process-letter-of-guarantee_liquidate"></a>Borgstelling Liquideren verwerken
1. Ga naar **Klanten > Orders > Alle verkooporders**.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
3. Klik in het actievenster op **Beheren**.
4. Klik op **Borgstelling**.
5. Klik in het actievenster op **Borgstelling**.
6. Klik op **Liquideren** om het dialoogvenster te openen.
7. Klik op **OK**.
8. Ga naar **Contanten en bankbeheer > Borgstellingen > Borgstellingen**.
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik op **Liquideren** om het dialoogvenster te openen.
11. Klik op **OK**.
12. Vouw de sectie **Acties** uit.
    * Controleer de record 'Liquideren'.  
13. Zoek en selecteer de gewenste record in de lijst.
14. Klik om de koppeling in het veld **Journaalbatchnummer** te volgen.
15. Klik op **Regels**.
    * Controleer de geboekt journaalposten.  
16. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
