---
title: Een mandaat voor automatische afschrijving maken voor een klant
description: Deze taakhandleiding laat zien hoe een mandaat voor automatische afschrijving wordt gemaakt en hoe het op een factuur wordt gebruikt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177206"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Een mandaat voor automatische afschrijving maken voor een klant

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakhandleiding laat zien hoe een mandaat voor automatische afschrijving wordt gemaakt en hoe het op een factuur wordt gebruikt.


## <a name="create-a-bank-account"></a>Een bankrekening maken
1. Ga in het **navigatiedeelvenster** naar **Modules > Klanten > Klanten > Alle klanten.**
2. Selecteer een record in de lijst. Selecteer bijvoorbeeld US-001
3. Klik in het actievenster op **Klant**.
4. Klik op **Bankrekeningen**.
5. Klik op **Nieuw**.
6. Typ een waarde in het veld **Bankrekening**.
7. Typ een waarde in het veld **Naam**.
8. Typ een waarde in het veld **IBAN**.
9. Typ een waarde in het veld **Valuta**.
10. Klik op **Opslaan**.
11. Sluit de pagina.
12. Ga in het **navigatievenster** naar **Modules > Contanten en bankbeheer > Bankrekeningen > Bankrekeningen**.
13. Zoek en selecteer de gewenste record in de lijst.
14. Klik in de lijst op de koppeling in de geselecteerde rij.
15. Klik op **Bewerken**.
16. Vouw het sneltabblad **Aanvullende identificatie** uit.
17. Typ een waarde in het veld **ID automatische afschrijving**.
18. Typ een waarde in het veld **IBAN**.
19. Sluit de pagina.
20. Sluit de pagina.

## <a name="define-the-electronic-payment-method"></a>De elektronische betalingsmethode definiëren
1. Ga in het **navigatievenster** naar **Modules > Klanten > Instelling van betalingen > Betalingsmethoden**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Betalingsmethode**.
4. Typ een waarde in het veld **Beschrijving**.
5. Typ Elektronische betaling in het veld **Betalingstype**. Het betalingstype bij een betalingsmethode voor het mandaat voor automatische afschrijving moet Elektronische betaling zijn.
6. Selecteer Ja in het veld **Mandaat vereisen**.
7. Sluit de pagina.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Voeg een mandaat voor automatische afschrijving toe aan een klant.
1. Ga in het **navigatiedeelvenster** naar **Modules > Klanten > Klanten > Alle klanten.**
2. Selecteer een record in de lijst. Selecteer bijvoorbeeld US-001
3. Klik op **Bewerken**.
4. Vouw het sneltabblad **Standaardwaarden betaling** uit.
5. Typ of selecteer een waarde in het veld **Betalingsmethode.**
6. Vouw het sneltabblad **Standaardwaarden betaling** uit.
7. Vouw het sneltabblad **Mandaten voor automatische afschrijving** uit.
8. Klik op **Toevoegen**.
9. Typ of selecteer een waarde in het veld **Bankrekening**.
10. Typ of selecteer een waarde in het veld **Bankrekening van crediteur**.
11. Voer in het veld **Betalingsfrequentie** het aantal betalingen in dat u voor dit mandaat verwacht te verwerken.
12. Klik op **OK**.
13. Klik op **Afdrukken**.
14. Klik op **Mandaatrapport**.
15. Sluit de pagina.
16. Klik op **Bewerken**.
17. Voer een datum in het veld **Datum handtekening** in.
18. Klik op **Ja**.
19. Voer de locatie in waar het mandaat is ondertekend.
20. Klik op **OK**.
21. Sluit de pagina.

## <a name="create-a-free-text-invoice-with-mandate"></a>Een vrije-tekstfactuur met mandaat maken
1. Ga in het **navigatievenster** naar **Modules > Klanten > Facturen > Alle vrije-tekstfacturen**.
2. Klik op **Nieuw**.
3. Selecteer de klant aan wie u het mandaat hebt toegevoegd.
4. Typ of selecteer een waarde in het veld **Mandaat-id voor automatische afschrijving**.

