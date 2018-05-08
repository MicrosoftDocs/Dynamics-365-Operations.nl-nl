--- 
title: Elektronische documenten genereren voor betalingen met een indelingsconfiguratie voor elektronische aangifte (taakbegeleiding) (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken om elektronische documenten te genereren voor de verwerking van betalingen.
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>Elektronische documenten genereren voor betalingen met een indelingsconfiguratie voor elektronische aangifte (taakbegeleiding) (ER)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken om elektronische documenten te genereren voor de verwerking van betalingen. Deze stappen kunnen in het voorbeeldbedrijf GBSI worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratie maken met de indeling van een betalingsdocument" voltooien.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>De configuratie van de elektronische betalingsmethode wijzigen
1. Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.
2. Selecteer indien nodig de sectie Bestandsindeling om deze uit te vouwen.
3. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Betalingsmethode met de waarde 'Elektronisch'.
4. Klik op Bewerken.
5. Stel het veld Algemene elektronische rapportage in op Ja.
    * Selecteer Ja als u het algemene patroon voor elektronische rapportage wilt gebruiken voor het genereren van betalingsbestanden.  
6. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer de indelingsconfiguratie BACS (UK fictief).
8. Klik op Opslaan.
9. Sluit de pagina.

## <a name="test-the-format-of-generated-payment-files"></a>De indeling van gegenereerde betalingsbestanden testen
1. Ga naar Leveranciers > Betalingen > Betalingsjournaal.
2. Klik op Nieuw.
3. Markeer in de lijst de geselecteerde rij.
4. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer VendPay.  
6. Klik op Opslaan.
7. Klik op Regels.
8. Typ 'DEMF' in het veld Bedrijf.
    * DEMF  
9. Geef in het veld Rekening de waarde 'DE-01001' op.
    * DE - 01001  
10. Typ 'Betaling' in het veld Omschrijving.
    * Betaling  
11. Voer een nummer in het veld Debet in.
    * 1000  
12. Klik op het tabblad Betaling.
13. Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.
14. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de waarde Elektronisch.  
15. Klik in de lijst op de koppeling in de geselecteerde rij.
16. Klik op Opslaan.
17. Klik op Betalingen genereren.
18. Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.
19. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de waarde Elektronisch.  
20. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer de waarde Elektronisch.  
21. Typ een waarde in het veld Bestandsnaam.
    * Typ bijvoorbeeld 'betalingen'.  
22. Klik in het veld Bankrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
23. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer de waarde GBSI OPER.  
24. Klik op OK.
25. Klik op OK.
    * Analyseer het gemaakte betalingsbestand in XML-indeling. Vergelijken het met de ontworpen documentindeling en de gedefinieerde kenmerken van de betalingstransactie.  


