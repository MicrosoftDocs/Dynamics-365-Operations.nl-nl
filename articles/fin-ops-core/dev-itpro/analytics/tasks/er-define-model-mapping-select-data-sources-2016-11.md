---
title: ER-modeltoewijzingen definiëren en gegevensbronnen hiervoor selecteren
description: In dit onderwerp wordt uitgelegd hoe een systeembeheerder of ontwikkelaar voor elektronische rapportage gegevensbronnen kan selecteren voor een ER-gegevensmodel (elektronische rapportage).
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69fb025b273aca6a0cf7733732f2849686eaa470ded6804a10b793cff9837562
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717540"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a>ER-modeltoewijzingen definiëren en gegevensbronnen hiervoor selecteren

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage gegevensbronnen kan selecteren voor een ER-gegevensmodel (elektronische rapportage). De gegevensbronnen worden verbonden met afzonderlijke onderdelen van het geselecteerde gegevensmodel tijdens ontwerptijd en vullen zakelijke gegevens in dat gegevensmodel in tijdens de uitvoering. In dit voorbeeld selecteert u gegevensbronnen voor een bestaand gegevensmodel dat voor het voorbeeldbedrijf, Litware, Inc. is gemaakt. Als u deze stappen wilt uitvoeren, moet u de stappen in de procedure "Een nieuw gegevensmodel maken" eerst uitvoeren.


## <a name="open-the-electronic-reporting-configurations-tree"></a>De structuur met ER-configuraties openen
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Rapportconfiguraties.

## <a name="insert-a-new-model-mapping"></a>Een nieuwe modeltoewijzing invoegen
1. Selecteer "Payments (simplified model)" in de structuur.
2. Klik op Ontwerper.
3. Klik op Model toewijzen aan gegevensbron.
4. Klik op Nieuw.
    * Hiermee wordt een nieuwe record gemaakt waarmee het gegevensmodel wordt toegewezen aan gegevensbronnen. In dit voorbeeld wijst u het gegevensmodel toe aan gegevensbronnen voor het gewenste betalingstype: kredietoverdracht.     Het is mogelijk om meer dan één toewijzing te ontwerpen voor een bepaald gegevensmodel. Zo kunt u bijvoorbeeld een toewijzing maken voor de verschillende typen betalingen, zoals voor automatische afschrijving of voor kredietoverdrachten. In dit voorbeeld maakt u een toewijzing voor kredietoverdrachten.  
5. Typ "CT-toewijzing" in het veld Naam.
    * CT-toewijzing  
6. Typ "Betalingsmodel voor CT-toewijzing" in het veld Beschrijving.
    * Betalingsmodel voor CT-toewijzing  
7. Typ in het veld Definitie: 'CustomerCreditTransferInitiation'.
    * CustomerCreditTransferInitiation  
8. ResolveChanges de definitie.
9. Klik op Opslaan.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Vereiste gegevensbronnen voor de huidige modeltoewijzing definiëren
1. Klik op Ontwerper.
2. Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.
3. Klik op Basis toevoegen.
    * Voer deze gegevensbron in om toegang te krijgen tot betalingstransacties.  
4. Typ "Transacties" in het veld Naam.
    * Transacties  
5. Typ "Transacties" in het veld Label.
    * Transacties  
6. Typ "Grootboekjournaalregels" in het veld Help.
    * Grootboekjournaalregels  
7. Selecteer Ja in het veld Vragen om query.
    * Selecteer Ja.  
8. Typ "LedgerJournalTrans" in het veld Tabel.
    * LedgerJournalTrans  
9. Klik op OK.
    * Selecteer de tabel LedgerJournalTrans als gegevensbron voor het huidige gegevensmodel.  
10. Selecteer "Functions\Calculated field" in de structuur.
11. Klik op Toevoegen.
    * Klik op Toevoegen om een nieuw berekend veld toe te voegen.  
12. Typ "$EndToEndID" in het veld Naam.
    * $EndToEndID  
13. Klik op Formule bewerken.
14. Selecteer "String\CONCATENATE" in de structuur.
15. Klik op Functie toevoegen.
16. Vouw "Transactions" uit in de structuur.
17. Selecteer "Transactions\Voucher" in de structuur.
18. Klik op Gegevensbron toevoegen.
19. Typ in het veld Formule: 'CONCATENATE(Transactions.Voucher, "-", '. (Let op de spatie tussen komma en enkel aanhalingsteken.)
    * Typ [ , "-", ] aan het einde van de formule.  
20. Selecteer "String\TEXT" in de structuur.
21. Klik op Functie toevoegen.
22. Selecteer "Transactions\Record-ID(RecId)" in de structuur.
23. Klik op Gegevensbron toevoegen.
24. Typ in het veld Formule: 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.
    * Typ [))] aan het einde van de formule.  
25. Klik op Opslaan.
    * Controleer of er geen fouten zijn gevonden voor de gemaakte formule. Zie het tabblad FOUTEN onder het bedieningselement voor de formule-editor.  
26. Sluit de pagina.
27. Klik op OK.
    * Voeg het berekende veld toe aan deze gegevensbron.  
28. Klik op Toevoegen.
    * Klik op Toevoegen om een nieuw berekend veld toe te voegen.  
29. Typ "$Amount" in het veld Naam.
    * $Amount  
30. Klik op Formule bewerken.
31. Vouw "Transactions" uit in de structuur.
32. Selecteer "Transactions\Debit(AmountCurDebit)" in de structuur.
33. Klik op Gegevensbron toevoegen.
34. Typ in het veld Formule: 'Transactions.AmountCurDebit - '. (Let op de spatie tussen minus-teken en enkel aanhalingsteken.)
    * Typ [ - ] aan het einde van de formule.  
35. Selecteer "Transactions\Credit(AmountCurCredit)" in de structuur.
36. Klik op Gegevensbron toevoegen.
37. Klik op Opslaan.
38. Sluit de pagina.
39. Klik op OK.
    * Hiermee wordt het berekende veld $Amount toegevoegd aan de geselecteerde gegevensbron voor het huidige gegevensmodel.  
40. Selecteer 'Transactions\$Amount' in de structuur.
41. Vouw "Transactions" uit in de structuur.
42. Zoek in de structuur 'Transactions\$Amount' en vouw dit uit of samen.
43. Vouw in de structuur 'Transactions' uit of samen.
44. Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.
45. Klik op Basis toevoegen.
    * Voer deze gegevensbron in om toegang te krijgen tot de bankrekeninggegevens van het bedrijf.  
46. Typ "BankAccount" in het veld Naam.
    * BankAccount  
47. Typ "Bankrekening" in het veld Label.
    * Bankrekening  
48. Typ "Bankrekening" in het veld Help.
    * Bankrekening  
49. Selecteer Ja in het veld Vragen om query.
    * Selecteer Ja.  
50. Typ "BankAccountTable" in het veld Tabel.
    * BankAccountTable  
51. Klik op OK.
    * Selecteer de tabel BankAccountTable als gegevensbron voor het huidige gegevensmodel.  
52. Klik op Basis toevoegen.
    * Voer deze gegevensbron in om toegang te krijgen tot de vereisten van het bedrijf.  
53. Typ "Bedrijf" in het veld Naam.
    * Bedrijf  
54. Typ een waarde in het veld Label.
    * Bedrijfsgegevens  
55. Typ "Bedrijfsinformatie" in het veld Help.
    * Bedrijfsgegevens  
56. Selecteer Ja in het veld Vragen om query.
    * Selecteer Ja.  
57. Typ "CompanyInfo" in het veld Tabel.
    * CompanyInfo  
58. Klik op OK.
    * Selecteer de tabel CompanyInfo als gegevensbron voor het huidige gegevensmodel.  
59. Selecteer "Functions\Calculated field" in de structuur.
60. Klik op Basis toevoegen.
    * Voeg een berekend veld in als nieuwe gegevensbron.  
61. Typ "ProcessingDateTime" in het veld Naam.
    * ProcessingDateTime  
62. Typ Verwerkingsdatum en -tijd in het veld Label.
    * Verwerkingsdatum en -tijd  
63. Klik op Formule bewerken.
64. Selecteer in de structuur 'Date/time\SESSIONNOW'.
65. Klik op Functie toevoegen.
66. Klik op Opslaan.
67. Sluit de pagina.
68. Klik op OK.
    * Voeg het berekende veld ProcessingDateTime toe als gegevensbron voor het huidige gegevensmodel.  
69. Klik op Opslaan.
70. Sluit de pagina.
71. Sluit de pagina.
72. Sluit de pagina.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]