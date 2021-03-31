---
title: Kredietbrief importeren
description: Deze procedure begeleidt u door het proces voor het importeren van een kredietbrief.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac0b1aacbf0e5dbe69a8125dc0a1373de0957d4e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225388"
---
# <a name="import-letter-of-credit"></a>Kredietbrief importeren

[!include [banner](../../includes/banner.md)]

Deze procedure begeleidt u door het proces voor het importeren van een kredietbrief. Het volgende moet worden ingesteld voordat u deze procedure uitvoert: bankfaciliteiten, boekingsprofielen, een bankfaciliteitsovereenkomst en de details van de leverancier.

Bij deze procedure wordt het demobedrijf USMF gebruikt.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Een verkooporder met kredietbrief maken
1. Ga naar Leveranciers > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Leveranciersrekening.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Vouw de sectie Algemeen uit.
7. Typ of selecteer een waarde in het veld Locatie.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Typ of selecteer een waarde in het veld Magazijn.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Voer in het veld Boekingsdatum een datum in.
12. Typ een datum in het veld Leveringsdatum.
    * Opmerking: het veld 'Type bankdocument' moet worden geselecteerd met de waarde 'Kredietbrief'.  
13. Klik op OK.
14. Typ of selecteer een waarde in het veld Artikelnummer.
15. Zoek en selecteer de gewenste record in de lijst.
16. Klik in de lijst op de koppeling in de geselecteerde rij.
17. Vouw de sectie Regeldetails uit.
18. Klik op het tabblad Levering.
19. Typ een datum in het veld Leveringsdatum.
20. Typ een datum in het veld Bevestigde leveringsdatum.
21. Voer in het veld Eenheidsprijs een getal in.
    * Definieer de details van de kredietbrief.  
22. Klik in het actievenster op Beheren.
23. Klik op Kredietbrief/importincasso.
24. Typ in het veld Aanvraagdatum de datum en een tijd.
    * Controleer of het veld 'Bankrekening' de standaard actieve bankrekening heeft waarop de aanvraagdatum is gebaseerd.  
25. Typ een waarde in het veld Bankdocumentnummer.
26. Typ in het veld Ontvangstdatum de datum en een tijd.
27. Vouw de sectie Bankdocument uit.
28. Voer in het veld Vervaldatum een datum en tijd in.
29. Vouw de sectie Bankgegevens uit.
30. Typ of selecteer een waarde in het veld Adviserende bank.
31. Klik in de lijst op de koppeling in de geselecteerde rij.
32. Klik op Opslaan.
33. Klik op Inkooporderverzendingen ophalen.
34. Sluit de pagina.
35. Klik in het actievenster op Inkoop.
36. Klik op Bevestigen.
37. Klik in het actievenster op Beheren.
38. Klik op Kredietbrief/importincasso.
39. Klik op Verwerken.
40. Klik op Bevestigen.
    * Controleer of het Faciliteitssaldo het inkooporderbedrag verlaagt.  In dit voorbeeld: Inkoopbedrag = 500,00,  Faciliteitslimiet = 10.000,00,  dus faciliteitsaldo = 9500,00.  
41. Sluit de pagina.
42. Voer in het veld Eenheidsprijs een getal in.
43. Klik op Opslaan.
44. Klik in het actievenster op Inkoop.
45. Klik op Bevestigen.
    * Wijzig de kredietbrief, vanwege de wijziging in de Eenheidsprijs.  
46. Klik in het actievenster op Beheren.
47. Klik op Kredietbrief/importincasso.
    * Wijzig de kredietbrief, vanwege de wijziging in de Inkoopeenheidsprijs.  
48. Klik op Verwerken.
49. Klik op Aanpassen.
50. Klik op Verwijderen.
51. Klik op Ja.
52. Klik op Inkooporderverzendingen ophalen.
53. Klik op Verwerken.
54. Klik op Bevestigen.
    * Controleer of het Faciliteitssaldo het inkooporderbedrag verlaagt.  In dit voorbeeld: bewerkt Inkoopbedrag = 600,00,  Faciliteitslimiet = 10.000,00,  dus faciliteitsaldo = 9400,00.  
55. Sluit de pagina.

## <a name="post-packing-slip"></a>Pakbon boeken
1. Klik in het actievenster op Ontvangen.
2. Klik op Productontvangstbon.
3. Typ een waarde in het veld PurchParmTable_Num.
    * Selecteer het Verzendnummer dat samen met de verwijzing naar de kredietbrief werd gemaakt.  
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Typ een datum in het veld Datum productontvangstbon.
6. Klik op OK.
7. Sluit de pagina.
8. Sluit de pagina.

## <a name="verify-import-letter-of-credit-status"></a>De status van de Importkredietbrief controleren
1. Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief importeren en incasso importeren.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Controleer de status van de Importkredietbrief.     
4. Sluit de pagina.
5. Sluit de pagina.

## <a name="post-purchase-invoice"></a>Inkoopfactuur boeken
1. Ga naar Leveranciers > Inkooporders > Alle inkooporders.
    * Selecteer de inkooporder die samen met de kredietbrief werd gemaakt.  
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het actievenster op Factuur.
5. Klik op Factuur.
6. Typ een waarde in het veld Nummer.
7. Typ of selecteer een waarde in het veld Verzendnummer.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Voer een datum in het veld Factuurdatum in.
10. Klik op Vereffeningsstatus bijwerken.
11. Klik op Boeken.
12. Sluit de pagina.
13. Sluit de pagina.

## <a name="verify-import-letter-of-credit-status"></a>De status van de Importkredietbrief controleren
1. Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief importeren en incasso importeren.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Controleer de status van de kredietbrief2.  
    * Valideren: verzending status = details van gefactureerde bankfaciliteit  
4. Klik op Weergeven.
5. Klik op Aanvraag afdrukken.
6. Klik op OK.
    * Controleer of de kredietbriefaanvraag wordt afgedrukt.  
7. Sluit de pagina.
8. Sluit de pagina.
9. Sluit de pagina.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Het betalingsjournaal van leveranciers boeken voor de gemaakte inkoopfactuur met kredietbrief
1. Ga naar Leveranciers > Betalingen > Betalingsjournaal.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Naam.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik op Regels.
6. Voer een datum in het veld Datum in.
7. Geef in het veld Rekening de gewenste waarden op.
8. Klik op Transacties vereffenen.
9. Vouw de sectie Totalen uit.
10. Selecteer een optie in het veld Weergeven.
    * Controleer of de velden Bankdocumentnummer en Verzendnummer zijn bijgewerkt.  
11. Schakel het selectievakje Markeren in.
12. Klik op OK.
13. Klik op het tabblad Betaling.
    * Controleer of de velden Bankdocumentnummer en Verzendnummer zijn bijgewerkt.  
14. Klik op Boeken.
15. Sluit de pagina.
16. Sluit de pagina.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>De status van de importkredietbrief controleren na betaling van factuur
1. Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief importeren en incasso importeren.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Controleer de status van de Importkredietbrief.   
4. Sluit de pagina.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>De bankfaciliteitslimiet en het verbruikrapport controleren
1. Ga naar Contanten en bankbeheer > Query's en rapporten > Kredietbrieven of borgstellingen > Bankfaciliteiten en gebruik (rapport).
2. Breid de sectie Op te nemen records uit.
3. Klik op Filter.
    * Definieer het veld Criteria met vereiste de bankrekening.  
4. Typ of selecteer een waarde in het veld Criteria.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op OK.
7. Klik op OK.
    * Controleer het rapport waarin de transacties worden vermeld.  
    * Controleer of het rapport de transacties met bankdocumentnummer, faciliteitslimiet, verbruikt bedrag en het saldobedrag van de faciliteit vermeldt.  
8. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]