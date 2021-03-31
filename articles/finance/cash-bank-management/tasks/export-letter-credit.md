---
title: Kredietbrief exporteren
description: Deze procedure begeleidt u door het proces van de exportkredietbrief.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 127f38e7db0a8c0703fd95274f45ff4ca49c131e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225436"
---
# <a name="export-letter-of-credit"></a>Kredietbrief exporteren

[!include [banner](../../includes/banner.md)]

Deze procedure begeleidt u door het proces van de exportkredietbrief.

Een kredietbrief is een overeenkomst die dor een bank wordt uitgegeven, waarin de bank akkoord gaat om namens de koper de betaling te garanderen als aan de voorwaarden van de overeenkomst tussen de koper en verkoper is voldaan.



Voer de procedure 'Bankfaciliteiten en boekingsprofielen instellen' en de procedure 'Kredietbrief_Een bankfaciliteitsovereenkomst maken' uit vóór deze procedure. Het USMF-demobedrijf moet zijn geselecteerd om deze procedure goed uit te voeren.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Verkooporder voor exportkredietbrief maken
1. Ga naar Klanten > Orders > Alle verkooporders.
2. Klik op Nieuw.
3. Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Vouw de sectie Algemeen uit of samen.
7. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer de site waar het uit te geven artikel is opgeslagen.  
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer het magazijn waar het uit te geven artikel is opgeslagen.  
10. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Opmerking: het veld Type bankdocument moet worden geselecteerd met de waarde 'Kredietbrief'.  
11. Selecteer 'Kredietbrief' in het vel Type bankdocument.
12. Vouw de sectie Levering uit of samen.
    * Selecteer Controle van leveringsdatum = Geen.  
13. Typ een datum in het veld Gevraagde ontvangstdatum.
14. Klik op OK.
15. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Selecteer het vereiste artikel dat moet worden uitgegeven/verkocht.  
16. Zoek en selecteer de gewenste record in de lijst.
17. Klik in de lijst op de koppeling in de geselecteerde rij.
18. Voer een nummer in het veld Eenheidsprijs in.
19. Vouw de sectie Regeldetails uit of samen.
20. Klik op het tabblad Levering.
21. Typ een datum in het veld Gewenste verzenddatum.
22. Typ een datum in het veld Bevestigde verzenddatum.
23. Klik in het actievenster op Beheren.
24. Klik op Kredietbrief.
25. Typ een waarde in het veld Bankdocumentnummer.
26. Voer in het veld Vervaldatum een datum en tijd in.
27. Vouw de sectie Bankgegevens uit of samen.
28. Klik in het veld Uitgevende bank op de vervolgkeuzeknop om de zoekopdracht te openen.
29. Klik in de lijst op de koppeling in de geselecteerde rij.
30. Klik in het veld Adviserende bank op de vervolgkeuzeknop om de zoekopdracht te openen.
31. Zoek en selecteer het gewenste record in de lijst.
32. Klik in de lijst op de koppeling in de geselecteerde rij.
33. Klik op Verkooporderverzendingen ophalen.
34. Klik op Bankdocument uitgeven.
35. Sluit de pagina.

## <a name="post-packing-slip"></a>Pakbon boeken
1. Klik in het actievenster op Verzamelen en inpakken.
2. Klik op Pakbon boeken.
3. Vouw de sectie Parameters uit of samen.
4. Selecteer in het veld Hoeveelheid de optie Alle.
5. Vouw de sectie Instellingen uit of samen.
6. Typ een datum in het veld Pakbondatum.
7. Selecteer het Verzendnummer.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik op OK.
10. Klik op OK.

## <a name="post-sales-invoice"></a>Verkoopfactuur boeken
1. Klik in het actievenster op Factuur.
2. Klik op Factuur.
3. Vouw de sectie Overzicht uit of samen.
4. Selecteer het Verzendnummer.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Vouw de sectie Instellingen uit of samen.
7. Voer een datum in het veld Factuurdatum in.
8. Klik op OK.
9. Klik op OK.

## <a name="shipment-document-submitted-status"></a>Status ingediend verzendingsdocument
1. Klik in het actievenster op Beheren.
2. Klik op Kredietbrief.
3. Vouw de sectie Regels uit of samen.
    * Opmerking: het veld 'Document ingediend' moet op 'Ja' worden ingesteld.  

## <a name="verify-export-letter-of-credit"></a>Exportkredietbrief controleren
1. Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief exporteren en incasso importeren.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Controleer of de Exportkredietbrief als verzendstatus 'Gefactureerd' heeft.  

## <a name="customer-payment"></a>Betaling van klant
1. Ga naar Klanten > Betalingen > Betalingsjournaal.
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op Regels.
7. Voer een datum in het veld Datum in.
8. Geef in het veld Rekening de gewenste waarden op.
9. Klik op Vereffening.
10. Schakel het selectievakje in de koptekst van Totalen in.
    * Opmerking: stel het veld Weergeven in op 'Kredietbrief'.  
11. Zoek en selecteer de gewenste record in de lijst.
12. Schakel het selectievakje Markeren in of uit.
13. Klik op OK.
14. Klik op het tabblad Betaling.
    * Details van bankdocumentnummer en verzendummer controleren  
15. Klik op Boeken.

## <a name="verify-export-letter-of-credit-after-payment"></a>Exportkredietbrief controleren na betaling
1. Ga naar Contanten en bankbeheer > Kredietbrieven > Kredietbrief exporteren en incasso importeren.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Controleer Verzendstatus = Betaling ontvangen en saldobedrag = 0,00.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]