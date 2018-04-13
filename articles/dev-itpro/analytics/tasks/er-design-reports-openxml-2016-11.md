--- 
title: Een configuratie ontwerpen voor het genereren van rapporten in OpenXML-indeling voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een sjabloon bevat voor het genereren van elektronische documenten in OPENXML-indeling.
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Een configuratie ontwerpen voor het genereren van rapporten in OpenXML-indeling voor elektronische aangifte (ER)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een sjabloon bevat voor het genereren van elektronische documenten in OPENXML-indeling. Deze configuratie wordt voor de verwerking van leveranciersbetalingen gebruikt.



In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in GBSI-bedrijven worden uitgevoerd.



Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien. U moet ook het Microsoft Excel-bestand [Sjabloon van betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266) downloaden en opslaan. 

## <a name="upload-the-payments-data-model-configuration"></a>De gegevensmodelconfiguratie Betalingen uploaden
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Markeer in de lijst de geselecteerde rij.
    * Selecteer de configuratieprovider voor het voorbeeldbedrijf Litware,Inc. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.  
3. Klik op Instellingen als actief.
4. Klik op Opslagplaatsen.
    * Selecteer een opslagplaats voor het type Bronnen voor bedrijfsactiviteiten, indien beschikbaar. Als deze beschikbaar is, slaat u de volgende stappen in verband met het maken van een nieuwe opslagplaats over.  
5. Klik op Toevoegen om het dialoogvenster te openen.
6. Voer Bronnen voor bedrijfsactiviteiten in het veld Opslagplaatstype van configuratie in.
7. Klik op Opslagplaats maken.
8. Klik op OK.
9. Klik op Openen.
10. Selecteer Betalingsmodel in de structuur.
11. Klik op Importeren.
    * Importeer dit gegevensmodel. Het wordt als een gegevensbron in een nieuwe indelingsconfiguratie gebruikt. Sla deze stap over als deze configuratie al is geïmporteerd.  
12. Klik op Ja.
13. Sluit de pagina.
14. Sluit de pagina.

## <a name="create-a-new-format-configuration"></a>Een nieuwe indelingsconfiguratie maken
1. Klik op Rapportconfiguraties.
2. Selecteer Betalingsmodel in de structuur.
3. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
4. Voer in het veld Nieuw veld "Indeling gebaseerd op gegevensmodel PaymentModel" in.
    * Maak een indeling die op het gegevensmodel PaymentModel is gebaseerd.  
5. Typ Voorbeeldwerkbladrapport in het veld Naam.
    * Voorbeeldwerkbladrapport  
6. Typ Voorbeeldwerkbladrapport voor leveranciersbetalingen in het veld Omschrijving.
    * Voorbeeldwerkbladrapport voor betalingen van leveranciers.  
7. Typ of selecteer een waarde in het veld Definitie gegevensmodel.
    * Selecteer de definitie 'CustomerCreditTransferInitiation'.  
8. Klik op Configuratie maken.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Een nieuw document in OPENXML-werkbladindeling ontwerpen
1. Selecteer Betalingsmodel\Voorbeeldwerkbladrapport in de structuur.
2. Klik op Ontwerper.
3. Klik in het actievenster op Importeren.
4. Klik op Importeren uit Excel.
5. Klik op Bijlagen.
    * Voeg het bestaande Excel-document als een sjabloon toe.  
6. Klik op Nieuw.
7. Klik op Bestand.
    * Wijs naar het bestaande Excel-bestand.  
8. Sluit de pagina.
9. Typ of selecteer een waarde in het veld Sjabloon.
    * Selecteer het gekoppelde Excel-bestand dat als sjabloon moet worden gebruikt.  
10. Klik op OK.
    * ER-indelingscomponenten zijn gemaakt in de ontwerpende indeling op basis van de structuur van het verwijzende MS Excel-document (benoemde bereiken).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Een nieuwe gegevensbron maken om totalen per valutacode te berekenen
1. Klik op het tabblad Toewijzing.
2. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
3. Selecteer in de structuur Functies\Groeperen op.
4. Typ PaymentByCurrency in het veld Naam.
    * PaymentByCurrency  
5. Klik op Groeperen op bewerken
6. Vouw in de structuur "model" uit.
7. Selecteer "model\Payments" in de structuur.
8. Klik op Veld toevoegen aan.
9. Klik op Wat groeperen.
10. Vouw "model\Payments" uit in de structuur.
11. Selecteer 'model\Payments\Currency' in de structuur.
12. Klik op Veld toevoegen aan.
13. Klik op Gegroepeerde velden.
14. Selecteer 'model\Payments\Instructed Amount(InstructedAmount)' in de structuur.
15. Klik op Veld toevoegen aan.
16. Klik op Aggregatievelden.
17. Selecteer een optie in het veld Methode.
    * Selecteer de aggregatiefunctie SUM.  
18. Typ 'TotalInstructuredAmount' in het veld Naam.
    * TotalInstructuredAmount  
19. Klik op Opslaan.
20. Sluit de pagina.
21. Klik op OK.

## <a name="map-format-components-to-data-sources"></a>Indelingscomponenten aan gegevensbronnen toewijzen
1. Vouw in de structuur "model" uit.
2. Vouw "model\Payments" uit in de structuur.
3. Vouw 'model\Payments\Initiating Party(InitiatingParty)' in de structuur uit.
4. Selecteer 'model\Payments\Initiating Party(InitiatingParty)\Name' in de structuur.
5. Vouw in de structuur 'Excel\ReportHeader' uit.
6. Selecteer in de structuur 'Excel\ReportHeader\CompanyName'.
7. Klik op Binden.
8. Vouw "model\Payments\Creditor" uit in de structuur.
9. Vouw 'model\Payments\Creditor\Identification' in de structuur uit.
10. Selecteer 'model\Payments\Creditor\Identification\Source ID(SourceID)' in de structuur.
11. Vouw in de structuur 'Excel\PaymLines' uit.
12. Selecteer in de structuur 'Excel\PaymLines\VendAccountName'.
13. Klik op Binden.
14. Selecteer "model\Payments\Creditor\Name" in de structuur.
15. Selecteer in de structuur 'Excel\PaymLines\VendName'.
16. Klik op Binden.
17. Vouw 'model\Payments\Creditor Agent(CreditorAgent)' in de structuur uit.
18. Selecteer 'model\Payments\Creditor Agent(CreditorAgent)\Name' in de structuur.
19. Selecteer in de structuur 'Excel\PaymLines\Bank'.
20. Klik op Binden.
21. Selecteer 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)' in de structuur.
22. Selecteer in de structuur 'Excel\PaymLines\RoutingNumber'.
23. Klik op Binden.
24. Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)" uit.
25. Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)\Identification" uit.
26. Selecteer 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number' in de structuur.
27. Selecteer in de structuur 'Excel\PaymLines\AccountNumber'.
28. Klik op Binden.
29. Selecteer 'model\Payments\Instructed Amount(InstructedAmount)' in de structuur.
30. Selecteer in de structuur 'Excel\PaymLines\Debit'.
31. Klik op Binden.
32. Vouw "model\Payments\Creditor" uit in de structuur.
33. Vouw in de structuur "model\Payments\Creditor Account(CreditorAccount)" uit.
34. Vouw 'model\Payments\Creditor Agent(CreditorAgent)' in de structuur uit.
35. Selecteer 'model\Payments\Currency' in de structuur.
36. Selecteer in de structuur 'Excel\PaymLines\Currency'.
37. Klik op Binden.
38. Vouw 'PaymentByCurrency' in de structuur uit.
39. Vouw 'PaymentByCurrency\grouped' in de structuur uit.
40. Selecteer 'PaymentByCurrency\grouped\Currency' in de structuur.
41. Vouw in de structuur 'Excel\SummaryLines' uit.
42. Selecteer in de structuur 'Excel\SummaryLines\SummaryCurrency'.
43. Klik op Binden.
44. Vouw 'PaymentByCurrency\aggregated' in de structuur uit.
45. Selecteer 'PaymentByCurrency\aggregated\TotalInstructuredAmount' in de structuur.
46. Selecteer in de structuur 'Excel\SummaryLines\SummaryAmount'.
47. Klik op Binden.
48. Selecteer 'PaymentByCurrency' in de structuur.
49. Selecteer in de structuur 'Excel\SummaryLines'.
50. Klik op Binden.
51. Selecteer "model\Payments" in de structuur.
52. Selecteer in de structuur 'Excel\PaymLines'.
53. Klik op Binden.
54. Klik op Opslaan.
55. Sluit de pagina.

## <a name="use-the-created-configuration-for-payments-processing"></a>De gemaakte configuratie gebruiken voor betalingsverwerking
1. Klik op Status wijzigen.
2. Klik op Voltooien.
3. Klik op OK.
4. Sluit de pagina.
5. Sluit de pagina.
6. Ga naar Leveranciers > Betalingsinstelling > Betalingsmethoden.
7. Gebruik het snelfilter om op het veld Betalingsmethode te filteren met de waarde 'Electronisch'.
    * Elektronisch  
8. Klik op Bewerken.
9. Vouw de sectie Bestandsindelingen uit.
10. Selecteer Ja in het veld Algemene elektronische rapportage.
11. Typ of selecteer een waarde in het veld Indelingsconfiguratie exporteren.
    * Selecteer de configuratie ‘Voorbeeldwerkbladrapport’.  
12. Klik op Opslaan.
13. Sluit de pagina.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>De gemaakte configuratie gebruiken voor het testen van de verwerking van betalingsjournalen
1. Ga naar Leveranciers > Betalingen > Betalingsjournaal.
2. Klik op Nieuw.
    * Maak een nieuw betalingsjournaal.  
3. Typ 'VendPay' in het veld Naam.
    * VendPay  
4. Klik op Regels.
5. Geef in het veld Account de waarde 'GB_SI_000001' op.
    * GB_SI_000001  
6. Stel Debet in op '1000'.
7. Klik op Nieuw.
8. Geef in het veld Account de waarde 'GB_SI_000005' op.
    * GB_SI_000005  
9. Stel Debet in op '2000'.
10. Typ EUR in het veld Valuta.
    * EUR  
11. Geef in het veld Tegenrekening de waarde 'GBSI OPER' op.
    * GBSI OPER  
12. Typ Elektronisch in het veld Betalingsmethode.
    * Elektronisch  
13. Klik op Opslaan.
14. Klik op Betalingen genereren.
15. Typ Elektronisch in het veld Betalingsmethode.
    * Elektronisch  
16. Typ in het veld Bestandsnaam 'Betalingen'.
    * Typ bijvoorbeeld Betalingen.  
17. Typ 'GBSI OPER' in het veld Bankrekening.
    * GBSI OPER  
18. Klik op OK.
19. Klik op OK.
    * Controleer het gemaakte werkblad, inclusief details van betalingsregels en totalen voor elke valutacode die in dit betalingsbericht wordt gebruikt.  


