---
title: Een afschrijvingsjournaal voor een klant maken
description: Deze taakhandleiding toont u hoe u de parameters voor afschrijvingen instelt en vervolgens transacties van afschrijft van de pagina Incasso's, de pagina Openstaande klantfacturen en de pagina Klant.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 44f36a12195a57e1b4cea524d2e4881f1fa7d0e9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842924"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Een afschrijvingsjournaal voor een klant maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakhandleiding toont u hoe u de parameters voor afschrijvingen instelt en vervolgens transacties van afschrijft van de pagina Incasso's, de pagina Openstaande klantfacturen en de pagina Klant. Bij deze taak wordt het demobedrijf USMF gebruikt.


## <a name="set-up-the-write-off-parameters"></a>De afschrijvingsparameters instellen
1. Ga naar Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten.
2. Klik op het tabblad Incasso's.
3. Vouw de sectie Afschrijven uit of samen.
    * Het afschrijvingsjournaal is het algemene journaal dat de afschrijvingstransacties bevat die u maakt.  
    * U kunt een redencode koppelen aan elke afschrijving. U kunt deze standaardinstelling bij de afschrijving overschrijven.  
    * Stel deze optie in op Ja als u de btw van de oorspronkelijke transactie wilt scheiden in de afschrijving.  
4. Sluit de pagina.
5. Ga naar Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant.
    * De afschrijvingsrekening wordt gebruikt als onkostenrekening of reservecorrectie in het algemene journaal   
6. Sluit de pagina.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Een klantsaldo afschrijven van de pagina met ouderdomssaldi
1. Ga naar Crediteringen en aanmaningen > Incasso's > Vervallen saldi.
2. Markeer de rij voor de klant die u wilt afschrijven. Markeer bijvoorbeeld de regel die Birch Company bevat.
3. Klik in het actievenster op Incasso.
4. Klik op Afschrijven.
5. Klik op OK.
6. Sluit de pagina.
7. Ga naar Grootboek > Journaalboekingen > Algemene journalen.
8. Selecteer het journaalbatchnummer voor het journaal dat uw afschrijving bevat.
    * Er wordt één regel gemaakt om het klantsaldo om te keren. Er worden een of meer regels gemaakt om de afschrijving naar de afschrijvingsrekening te boeken.  
9. Sluit de pagina.
10. Sluit de pagina.

## <a name="write-off-transactions-from-the-collections-form"></a>Schrijf transacties af vanuit het formulier Incasso's.
1. Ga naar Crediteringen en aanmaningen > Incasso's > Vervallen saldi.
2. Selecteer de naam van de klant die de transacties heeft die u wilt afschrijven. Selecteer bijvoorbeeld Cave Wholesales (US-004).
3. Markeer de rij voor de eerste transactie.
4. Markeer de rij voor de tweede transactie.
5. Klik op Afschrijven.
6. Typ "Oninbare vorderingen" in het veld Opmerking reden.
7. Klik op OK.
8. Sluit de pagina.
9. Sluit de pagina.
10. Ga naar Grootboek > Journaalboekingen > Algemene journalen.
11. Selecteer het journaalbatchnummer voor het journaal dat uw afschrijving bevat.
    * Er wordt één regel gemaakt om het klantsaldo om te keren. Er worden een of meer regels gemaakt om de afschrijving naar de afschrijvingsrekening te boeken.  
12. Sluit de pagina.
13. Sluit de pagina.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Een factuur afschrijven vanaf de pagina Openstaande klantfacturen
1. Ga naar Klanten > Facturen > Openstaande klantfacturen.
2. Markeer de regel voor een factuur. Markeer bijvoorbeeld de regel voor CIV-000667.
3. Klik in het actievenster op Factuur.
4. Klik op Afschrijven.
5. Klik op OK.
6. Sluit de pagina.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Een klantsaldo afschrijven van de klantpagina
1. Ga naar Klanten > Klanten > Alle klanten.
2. Een klantrekening selecteren. Selecteer bijvoorbeeld US-001 (Contoso Retail San Diego).
3. Klik in het actievenster op Incasso.
4. Klik op Afschrijven.
5. Klik op OK.
6. Sluit de pagina.

