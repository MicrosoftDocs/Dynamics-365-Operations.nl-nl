--- 
title: Een mandaat voor automatische afschrijving maken voor een klant
description: Deze taakhandleiding laat zien hoe een mandaat voor automatische afschrijving wordt gemaakt en hoe het op een factuur wordt gebruikt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Een mandaat voor automatische afschrijving maken voor een klant

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakhandleiding laat zien hoe een mandaat voor automatische afschrijving wordt gemaakt en hoe het op een factuur wordt gebruikt.


## <a name="create-a-bank-account"></a>Een bankrekening maken
1. Ga naar Klanten > Klanten > Alle klanten.
2. Selecteer bijvoorbeeld US-001
3. Klik in het actievenster op Klant.
4. Klik op Bankrekeningen.
5. Klik op Nieuw.
6. Typ een waarde in het veld Bankrekening.
7. Typ een waarde in het veld Naam.
8. Typ een waarde in het veld IBAN.
9. Typ een waarde in het veld Valuta.
10. Klik op Opslaan.
11. Sluit de pagina.
12. Ga naar Contanten en bankbeheer > Bankrekeningen > Bankrekeningen.
13. Zoek en selecteer de gewenste record in de lijst.
14. Klik in de lijst op de koppeling in de geselecteerde rij.
15. Klik op Bewerken.
16. Vouw de sectie Aanvullende identificatie uit.
17. Typ een waarde in het veld ID automatische afschrijving.
18. Typ een waarde in het veld IBAN.
19. Sluit de pagina.
20. Sluit de pagina.

## <a name="define-the-electronic-payment-method"></a>De elektronische betalingsmethode definiëren
1. Ga naar Klanten > Betalingsinstelling > Betalingsmethoden.
2. Klik op Nieuw.
3. Typ een waarde in het veld Betalingsmethode.
4. Typ een waarde in het veld Omschrijving.
5. Het betalingstype bij een betalingsmethode voor het mandaat voor automatische afschrijving moet Elektronische betaling zijn.
6. Selecteer Ja in het veld Mandaat vereisen.
7. Sluit de pagina.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Voeg een mandaat voor automatische afschrijving toe aan een klant.
1. Ga naar Klanten > Klanten > Alle klanten.
2. Selecteer bijvoorbeeld US-001
3. Klik op Bewerken.
4. Vouw de sectie van Standaardwaarden betaling uit.
5. Typ of selecteer een waarde in het veld Betalingsmethode.
6. Vouw de sectie van Standaardwaarden betaling uit.
7. Vouw de sectie Mandaten voor automatische afschrijving uit.
8. Klik op Toevoegen.
9. Typ of selecteer een waarde in het veld Bankrekening.
10. Typ of selecteer een waarde in het veld Bankrekening van crediteur.
11. Voer het aantal betalingen in dat u voor dit mandaat verwacht te verwerken.
12. Klik op OK.
13. Klik op Afdrukken.
14. Klik op Mandaatrapport.
15. Sluit de pagina.
16. Klik op Bewerken.
17. Voer een datum in het veld Handtekening in.
18. Klik op Ja.
19. Voer de locatie in waar het mandaat is ondertekend.
20. Klik op OK.
21. Sluit de pagina.

## <a name="create-a-free-text-invoice-with-mandate"></a>Een vrije-tekstfactuur met mandaat maken
1. Ga naar Klanten > Facturen > Alle vrije-tekstfacturen.
2. Klik op Nieuw.
3. Selecteer de klant aan wie u het mandaat hebt toegevoegd.
4. Typ of selecteer een waarde in het veld Mandaat-id voor automatische afschrijving.


