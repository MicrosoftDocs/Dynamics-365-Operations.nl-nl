---
title: ER Ontwerp domeinspecifiek gegevensmodel
description: In dit onderwerp wordt beschreven hoe u een nieuwe ER-configuratie (Electronic Reporting) maakt die een gegevensmodel voor elektronische betalingsdocumenten bevat.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 351c5a6624f7ee912c507a9f74324f4c8f61166b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755029"
---
# <a name="er-design-domain-specific-data-model"></a>ER Ontwerp domeinspecifiek gegevensmodel

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken die een gegevensmodel voor elektronische betalingsdocumenten bevat. Dit gegevensmodel wordt later gebruikt als gegevensbron, wanneer u de indeling van de betalingsdocumenten maakt.

In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld. Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.

    Selecteer de configuratieprovider voor voorbeeldbedrijf, 'Litware, inc.' Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" uitvoeren.  
    
2. Klik op Rapportconfiguraties.

    U maakt een configuratie die een gegevensmodel voor elektronische betalingdocumenten bevat. Dit gegevensmodel wordt later gebruikt als gegevensbron wanneer u de indeling gebruikt voor de betalingdocumenten.  

## <a name="create-a-new-data-model-configuration"></a>Een nieuwe gegevensmodelconfiguratie maken
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
2. Typ "Payments (simplified model)" in het veld Naam.
3. Typ "Configuratie van betalingsmodel" in het veld Omschrijving.

    De actieve configuratieprovider wordt hier automatisch ingevoerd. Deze provider kan deze configuratie onderhouden. Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.  

4. Klik op de knop 'Configuratie maken' om de taak van het maken van een configuratie te voltooien

## <a name="create-a-data-model"></a>Een gegevensmodel maken
U maakt een nieuw gegevensmodel voor de geselecteerde configuratie. Deze configuratieversie heeft de status Concept.  
1. Klik op Ontwerper.

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a>De structuur van een partij die deelneemt aan een betalingsproces definiëren
1. Klik op Nieuw om het verwijderdialoogvenster te openen.
2. Typ in het veld Naam de tekst "Partij".
3. Klik op Toevoegen.
4. Klik op Nieuw om het verwijderdialoogvenster te openen.
5. Typ "Name" in het veld Naam.
6. Selecteer "String" in het veld Artikeltype.
7. Klik op Toevoegen.
8. Typ in het veld Zoeken de tekst "Partij".
9. Klik op Vorige zoeken.

## <a name="define-the-bank-structure-for-this-model"></a>De bankstructuur voor dit model definiëren
1. Klik op Nieuw om het verwijderdialoogvenster te openen.
2. Typ "Agent" in het veld Naam.
3. Selecteer "Record" in het veld Artikeltype.
4. Klik op Toevoegen.
5. Typ in het veld Omschrijving: "Financiële instelling (bijvoorbeeld een bank) waar de partij (debiteur/crediteur) een rekening heeft".

    Financiële instelling (bijvoorbeeld een bank) waar de partij (debiteur/credieteur) een rekening heeft.  

6. Klik op Nieuw om het verwijderdialoogvenster te openen.
7. Typ "Name" in het veld Naam. 
8. Selecteer "String" in het veld Artikeltype.
9. Klik op Toevoegen.
10. Klik op Nieuw om het verwijderdialoogvenster te openen.
11. Typ "SWIFT" in het veld Naam.
12. Klik op Toevoegen.
13. Typ in het veld Beschrijving de tekst "De ID-code van de bank". 
14. Klik op Nieuw om het verwijderdialoogvenster te openen.
15. Typ "RoutingNumber" in het veld Naam.
16. Klik op Toevoegen.
17. Typ in het veld Beschrijving de tekst "Routenummer".
18. Klik op Vorige zoeken.

## <a name="define-the-bank-account-structure-for-this-model"></a>De bankrekeningstructuur voor dit model definiëren
1. Klik op Nieuw om het verwijderdialoogvenster te openen.
2. Typ "Account" in het veld Naam. 
3. Selecteer "Record" in het veld Artikeltype.
4. Klik op Toevoegen.
5. Typ in het veld Beschrijving: "De ID van een rekening van een partij bij een financiële instelling (bijvoorbeeld een bank)".

    De ID van een rekening van een partij bij een financiële instelling (bijvoorbeeld een bank).  

6. Klik op Nieuw om het verwijderdialoogvenster te openen.
7. Typ "Currency" in het veld Naam. 
8. Selecteer "String" in het veld Artikeltype.
9. Klik op Toevoegen.
10. Typ in het veld Beschrijving de tekst "Valutacode".
11. Klik op Nieuw om het verwijderdialoogvenster te openen.
12. Typ "Number" in het veld Naam. 
13. Klik op Toevoegen.
14. Klik op Nieuw om het verwijderdialoogvenster te openen.
15. Typ "IBAN" in het veld Naam. 
16. Klik op Toevoegen.
17. Typ in het veld Beschrijving de tekst "Internationaal bankrekeningnummer".

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a>De structuur definiëren van het betalingsbericht voor het betalingstype kredietoverdracht
1. Klik op Nieuw om het verwijderdialoogvenster te openen.
2. Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".
3. Typ "CustomerCreditTransferInitiation" in het veld Naam.
4. Klik op Toevoegen.
5. Typ in het veld Zoeken de tekst "CustomerCreditTransferInitiation". 
6. Klik op Vorige zoeken.
7. Klik op Nieuw om het verwijderdialoogvenster te openen.
8. Typ "MessageIdentification" in het veld Naam. 
9. Klik op Toevoegen.
10. Typ in het veld Omschrijving: "De punt-naar-punt-verwijzing, zoals toegewezen door de instruerende partij en verzonden naar de volgende partij in de keten, zodat het bericht ondubbelzinnig kan worden geïdentificeerd".

    De verwijzing van punt naar punt die is toegewezen door de instruerende partij (en verzonden naar de volgende partij) om een bericht te identificeren.  

11. Klik op Nieuw om het verwijderdialoogvenster te openen.
12. Typ "ProcessingDateTime" in het veld Naam.
13. Selecteer "DateTime" in het veld Artikeltype.
14. Klik op Toevoegen.
15. Typ in het veld Beschrijving: "De datum en tijd waarop het betalingsbericht is gemaakt". 
16. Klik op Nieuw om het verwijderdialoogvenster te openen.

    Definieer de betalingstransactiestructuur voor dit model.  

17. Typ "Payments" in het veld Naam.
18. Selecteer "Record list" in het veld Artikeltype.
19. Klik op Toevoegen.
20. Typ "Betalingsregels van het huidige bericht" in het veld Omschrijving.
21. Klik op Nieuw om het verwijderdialoogvenster te openen.
22. Typ "Creditor" in het veld Naam. 
23. Selecteer "Record" in het veld Artikeltype.
24. Klik op Toevoegen.
25. Typ in het veld Beschrijving: "Partij aan wie een geldbedrag verschuldigd is". 
26. Klik op Artikelverwijzing omschakelen.
27. Typ in het veld Zoeken de tekst "Partij".
28. Klik op Volgende zoeken.
29. Klik op OK.
30. Typ in het veld Zoeken de tekst "Betalingen".
31. Klik op Volgende zoeken.
32. Klik op Nieuw om het verwijderdialoogvenster te openen.
33. Typ "Debtor" in het veld Naam. 
34. Klik op Toevoegen.
35. Typ in het veld Beschrijving: "Partij die een geldbedrag verschuldigd is aan de (uiteindelijke) crediteur".
36. Klik op Artikelverwijzing omschakelen.
37. Typ in het veld Zoeken de tekst "Partij".
38. Klik op Volgende zoeken.
39. Klik op OK.
40. Klik op Volgende zoeken.
41. Klik op Nieuw om het verwijderdialoogvenster te openen.
42. Typ "Description" in het veld Naam.
43. Selecteer "String" in het veld Artikeltype.
44. Klik op Toevoegen.
45. Klik op Nieuw om het verwijderdialoogvenster te openen.
46. Typ "Currency" in het veld Naam.
47. Klik op Toevoegen.
48. Typ in het veld Beschrijving de tekst "Valutacode".
49. Klik op Nieuw om het verwijderdialoogvenster te openen.
50. Typ "TransactionDate" in het veld Naam. 
51. Selecteer "Date" in het veld Artikeltype.
52. Klik op Toevoegen.
53. Typ in het veld Beschrijving de tekst "Transactiedatum". 
54. Klik op Nieuw om het verwijderdialoogvenster te openen.
55. Typ "InstructedAmount" in het veld Naam.  
56. Selecteer "Real" in het veld Artikeltype.
57. Klik op Toevoegen.
58. Typ in het veld Beschrijving: "Het geldbedrag dat moet worden verplaatst tussen de debiteur en de crediteur, vóór aftrek van toeslagen". Het bedrag moet worden uitgedrukt in de valuta die door de initiërende partij is aangevraagd." in het veld Omschrijving.

    Het geldbedrag dat moet worden verplaatst tussen de debiteur en de crediteur, vóór aftrek van toeslagen. Het bedrag moet worden uitgedrukt in de valuta die door de initiërende partij is aangevraagd.  

59. Klik op Nieuw om het verwijderdialoogvenster te openen.
60. Typ "End2EndID" in het veld Naam. 
61. Selecteer "String" in het veld Artikeltype.
62. Klik op Toevoegen.
63. Typ in het veld Beschrijving: "De unieke identificatie die is toegewezen door de initiërende partij". Deze identificatie wordt ongewijzigd doorgegeven door de volledige keten heen, van begin tot einde." in het veld Omschrijving. 
64. Typ "PaymentModel" in het veld Naam.

    De naam PaymentModel is afgestemd op vooraf gedefinieerde interfaces van betalingsformulieren.  

65. Klik op Opslaan.
66. Sluit de pagina.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]