---
title: Klanten en bankrekeningen van klanten instellen voor ISO20022-automatische overschrijvingen
description: Deze taak voert u door het instellen van een bankrekening voor een klant en een mandaat voor automatische afschrijving van een klant die zijn vereist voor het genereren van het klantenbetalingsbestand zoals ISO20022 automatische afschrijving.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a8a3eff1f882d0d9b3d4943e352a8f3d1a6ae4
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852593"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Klanten en bankrekeningen van klanten instellen voor ISO20022-automatische overschrijvingen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taak voert u door het instellen van een bankrekening voor een klant en een mandaat voor automatische afschrijving van een klant die zijn vereist voor het genereren van het klantenbetalingsbestand zoals ISO20022 automatische afschrijving. Afhankelijk van de indelingen voor klantenbetalinge die zijn geconfigureerd, kan extra informatie zijn vereist voor een klant of een klantenbankrekening, die niet in deze procedure wordt behandeld. 

Deze taak werd gemaakt met het demobedrijf DEMF met een primair adres van een rechtspersoon in Duitsland.



Dit is de vierde van vijf taken die het proces voor klantenbetalingen toelichten door middel van elektronische rapportageconfiguraties.


## <a name="set-up-a-customer-bank-account"></a>Een bankrekening voor een klant instellen
1. Ga naar Klanten > Klanten > Alle klanten.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Rekening met een waarde van 'DE-010'.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het actievenster op Klant.
5. Klik op Bankrekeningen.
6. Klik op Nieuw.
7. Typ een waarde in het veld Bankrekening.
8. Typ een waarde in het veld Naam.
    * Voer bijvoorbeeld 'EUR bank' in.  
9. Typ of selecteer een waarde in het veld Bankgroepen.
10. Typ een waarde in het veld IBAN.
    * Voer bijvoorbeeld 'DE36200400000628808808' in.  
11. Typ een waarde in het veld SWIFT-code.
    * Voer bijvoorbeeld 'COBADEFFXXX' in.  Merk op dat SWIFT/BIC niet voor veel betalingsindelingen is vereist. Het wordt echter wel aanbevolen om het te registreren voor een bankrekening.  
12. Klik op Opslaan.
13. Sluit de pagina.
14. Klik op Bewerken.
15. Vouw de sectie van Standaardwaarden betaling uit.
16. Typ of selecteer een waarde in het veld Bankrekening.

## <a name="add-a-direct-debit-mandate"></a>Een mandaat voor automatische afschrijving toevoegen
1. Vouw de sectie Mandaten voor automatische afschrijving uit.
2. Klik op Toevoegen.
3. Typ of selecteer een waarde in het veld Bankrekening van crediteur.
    * Selecteer bijvoorbeeld DEMF OPER.  
4. Voer een datum in het veld Handtekening in.
5. Klik op Ja om de datum te bevestigen.
6. Typ of selecteer een waarde in het veld Locatie handtekening.
7. Voer in het veld Verwacht aantal betalingen een getal in.
8. Klik op OK.
9. Klik op Opslaan.

