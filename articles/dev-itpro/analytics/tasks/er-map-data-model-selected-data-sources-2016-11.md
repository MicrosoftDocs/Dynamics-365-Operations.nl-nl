---
title: Er Wjis gegevensmodel toe aan geselecteerde gegevensbronnen
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan toewijzen aan geselecteerde Dynamics 365 for Finance and Operations, Enterprise edition-gegevensbronnen.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "331547"
---
# <a name="er-map-data-model-to-selected-data-sources"></a>Er Wjis gegevensmodel toe aan geselecteerde gegevensbronnen

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-gegevensmodel (elektronische rapportage) kan toewijzen aan geselecteerde Dynamics 365 for Finance and Operations, Enterprise edition-gegevensbronnen. Deze modeltoewijzing wordt later gebruikt als gegevensbron in een indelingsconfiguratie die wordt gebruikt om elektronische betalingadocumenten te beheren. In dit voorbeeld wijst u een gegevensmodel voor voorbeeldbedrijf Litware, Inc. aan gegevensbronnen toe. U kunt deze stappen pas uitvoeren nadat u de stappen in de procedure "Gegevensbronnen voor modeltoewijzing selecteren" hebt voltooid.


## <a name="open-er-configurations-tree"></a>ER-configuratiestructuur openen
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Configuraties.

## <a name="select-created-model-mapping"></a>Gemaakte modeltoewijzing selecteren
1. Selecteer "Payments (simplified model)" in de structuur.
    * Zorg ervoor dat de modelconfiguratie "Betalingen (vereenvoudigd model)" vooraf is gemaakt. Ga anders eerst verder met de taakbegeleiding 'Een nieuwe configuratie maken met het gegevensmodel van het geselecteerde domein' voordat u de rest van deze procedure uitvoert.  
2. Klik op Modelontwerper.
3. Klik op Model toewijzen aan gegevensbron.
4. Selecteer de record "CT-toewijzing".
    * CT-toewijzing  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Gemaakte gegevensbronnen aan gegevensmodelelementen binden
1. Klik op Ontwerper.
2. Selecteer 'Processing date & time(ProcessingDateTime)' in de structuur.
3. Selecteer "Processing date(ProcessingDateTime)" in de structuur.
4. Klik op Binden.
5. Selecteer "Payment message identification(MessageIdentification)" in de structuur.
6. Vouw "Transactions" uit in de structuur.
7. Selecteer "Transactions\Journal batch number(JournalNum)" in de structuur.
8. Klik op Binden.
9. Selecteer "Payments" in de structuur.
10. Selecteer "Transactions" in de structuur.
11. Klik op Binden.
12. Vouw "Payments= Transactions" uit in de structuur.
13. Vouw "Payments= Transactions\Creditor" uit in de structuur.
14. Vouw "Payments= Transactions\Creditor\Account" uit in de structuur.
15. Vouw "Payments= Transactions\Creditor\Account\Currency code(Currency)" in de structuur.
16. Vouw "Transactions\vendBankAccountInTransactionCompany()" uit in de structuur.
17. Selecteer "Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)" in de structuur.
18. Klik op Binden.
19. Selecteer "Payments= Transactions\Creditor\Account\IBAN code(IBAN)" in de structuur.
20. Selecteer "Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)" in de structuur.
21. Klik op Binden.
22. Selecteer "Payments= Transactions\Creditor\Account\Number" in de structuur.
23. Selecteer "Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)" in de structuur.
24. Klik op Binden.
25. Vouw "Payments= Transactions\Creditor\Agent" uit in de structuur.
26. Selecteer "Payments= Transactions\Creditor\Agent\Name" in de structuur.
27. Selecteer "Transactions\vendBankAccountInTransactionCompany()\Name" in de structuur.
28. Klik op Binden.
29. Selecteer "Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)" in de structuur.
30. Selecteer "Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)" in de structuur.
31. Klik op Binden.
32. Selecteer "Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)" in de structuur.
33. Selecteer "Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)" in de structuur.
34. Klik op Binden.
35. Selecteer "Payments= Transactions\Creditor\Name" in de structuur.
36. Vouw "Transactions\findVendTable()" uit in de structuur.
37. Selecteer 'Transactions\findVendTable()\name()' in de structuur.
38. Klik op Binden.
39. Selecteer "Payments= Transactions\Currency code(Currency)" in de structuur.
40. Vouw "Transactions\>Relations" uit in de structuur.
41. Vouw "Transactions\>Relations\Currency table(Currency)" uit in de structuur.
42. Selecteer "Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)" in de structuur.
43. Klik op Binden.
44. Vouw "Payments= Transactions\Debtor" uit in de structuur.
45. Vouw "Payments= Transactions\Debtor\Account" uit in de structuur.
46. Selecteer "Payments= Transactions\Debtor\Account\Currency code(Currency)" in de structuur.
47. Selecteer "Bank Account(BankAccount)" in de structuur.
48. Vouw "Bank Account(BankAccount)" uit in de structuur.
49. Selecteer "Bank Account(BankAccount)\Currency(CurrencyCode)" in de structuur.
50. Klik op Binden.
51. Selecteer "Bank Account(BankAccount)\IBAN" in de structuur.
52. Selecteer "Payments= Transactions\Debtor\Account\IBAN code(IBAN)" in de structuur.
53. Klik op Binden.
54. Selecteer "Payments= Transactions\Debtor\Account\Number" in de structuur.
55. Selecteer "Bank Account(BankAccount)\Bank account number(AccountNum)" in de structuur.
56. Klik op Binden.
57. Vouw "Payments= Transactions\Debtor\Agent" uit in de structuur.
58. Selecteer "Payments= Transactions\Debtor\Agent\Name" in de structuur.
59. Selecteer "Bank Account(BankAccount)\Name" in de structuur.
60. Klik op Binden.
61. Selecteer "Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)" in de structuur.
62. Selecteer "Bank Account(BankAccount)\Routing number(RegistrationNum)" in de structuur.
63. Klik op Binden.
64. Selecteer "Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)" in de structuur.
65. Selecteer "Bank Account(BankAccount)\SWIFT code(SWIFTNo)" in de structuur.
66. Klik op Binden.
67. Selecteer "Payments= Transactions\Debtor\Name" in de structuur.
68. Selecteer "Company information(Company)" in de structuur.
69. Vouw "Company information(Company)" uit in de structuur.
70. Selecteer "Company information(Company)\Name" in de structuur.
71. Klik op Binden.
72. Selecteer "Payments= Transactions\Description" in de structuur.
73. Selecteer "Transactions\Description(Txt)" in de structuur.
74. Klik op Binden.
75. Selecteer "Payments= Transactions\End to end identification code(End2EndID)" in de structuur.
76. Selecteer "Transactions\$EndToEndID" in de structuur.
77. Klik op Binden.
78. Selecteer "Payments= Transactions\Instructed amount(InstructedAmount)" in de structuur.
79. Selecteer 'Transactions\$Amount' in de structuur.
80. Klik op Binden.
81. Selecteer "Payments= Transactions\Transaction date(TransactionDate)" in de structuur.
82. Selecteer "Transactions\Date(TransDate)" in de structuur.
83. Klik op Binden.

## <a name="validate-created-mapping"></a>Gemaakte toewijzing valideren
1. Klik op Valideren.
    * De nieuwe toewijzing valideren om te controleren of alle bindingen in orde zijn.  
2. Klik op de pijl om de sectie Foutenlijst uit te vouwen of samen te vouwen.
3. Klik op Opslaan.
4. Sluit de pagina.
5. Sluit de pagina.
6. Sluit de pagina.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>De status van de huidige versie van de modelconfiguratie wijzigen
1. Klik op Status wijzigen.
    * Wijzig de status van de ontworpen modelconfiguratie van Concept in Voltooid, om deze beschikbaar te maken voor het het ontwerp van betalingsindelingen.  
2. Klik op Voltooien.
    * Selecteer Voltooien.  
3. Typ een waarde in het veld Omschrijving.
    * Bijvoorbeeld: 'versie 1'.  
4. Klik op OK.
5. Selecteer de ingevulde versie van de huidige configuratie.
    * Merk op dat de gemaakte configuratie wordt opgeslagen als voltooide versie 1.  

