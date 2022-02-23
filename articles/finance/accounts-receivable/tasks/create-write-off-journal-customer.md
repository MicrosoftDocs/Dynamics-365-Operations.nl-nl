---
title: Een afschrijvingsjournaal voor een klant maken
description: Deze taakhandleiding toont u hoe u de parameters voor afschrijvingen instelt en vervolgens transacties van afschrijft van de pagina Incasso's, de pagina Openstaande klantfacturen en de pagina Klant.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: dd97f91f1ba53b56150b556fffdfed10a0c8911a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442071"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Een afschrijvingsjournaal voor een klant maken

[!include [banner](../../includes/banner.md)]

Deze taakhandleiding toont u hoe u de parameters voor afschrijvingen instelt en vervolgens transacties van afschrijft van de pagina Incasso's, de pagina Openstaande klantfacturen en de pagina Klant. Bij deze taak wordt het demobedrijf USMF gebruikt.


## <a name="set-up-the-write-off-parameters"></a>De afschrijvingsparameters instellen
1. Ga naar **navigatievenster > Modules > Crediteringen en aanmaningen > Instellingen > Parameters van module Klanten**.
2. Klik op het tabblad **Incasso's**.
3. Vouw de sectie **Afschrijven** uit of samen.
    - Het **afschrijvingsjournaal** is het algemene journaal dat de afschrijvingstransacties bevat die u maakt.  
    - U kunt een redencode koppelen aan elke afschrijving. U kunt deze standaardinstelling bij de afschrijving overschrijven.  
    - Stel **Btw apart** in op Ja als u de btw van de oorspronkelijke transactie wilt scheiden in de afschrijving.  
4. Sluit de pagina.
5. Ga naar **Crediteringen en aanmaningen > Instellingen > Boekingsprofielen van klant**. De afschrijvingsrekening wordt gebruikt als onkostenrekening of reservecorrectie in het algemene journaal.
6. Sluit de pagina.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Een klantsaldo afschrijven van de pagina met ouderdomssaldi
1. Ga naar **Crediteringen en aanmaningen > Incasso's > Vervallen saldi**.
2. Markeer de rij voor de klant die u wilt afschrijven. Markeer bijvoorbeeld de regel die Birch Company bevat.
3. Klik in het **actievenster** op **Incasso**.
4. Klik op **Afschrijven**.
5. Klik op **OK**.
6. Sluit de pagina.
7. Ga naar **Navigatievenster > Modules > Grootboek > Journaalboekingen > Algemene journalen**.
8. Selecteer het journaalbatchnummer voor het journaal dat uw afschrijving bevat. Er wordt één regel gemaakt om het klantsaldo om te keren. Er worden een of meer regels gemaakt om de afschrijving naar de afschrijvingsrekening te boeken.  
9. Sluit de pagina.
10. Sluit de pagina.

## <a name="write-off-transactions-from-the-collections-form"></a>Schrijf transacties af vanuit het formulier Incasso's.
1. Ga naar **Crediteringen en aanmaningen > Incasso's > Vervallen saldi**.
2. Selecteer de naam van de klant die de transacties heeft die u wilt afschrijven. Selecteer bijvoorbeeld Cave Wholesales (US-004).
3. Markeer de rij voor de eerste transactie.
4. Markeer de rij voor de tweede transactie.
5. Klik op **Afschrijven**.
6. Typ Oninbare vorderingen in het veld **Opmerking reden**.
7. Klik op **OK**.
8. Sluit de pagina.
9. Sluit de pagina.
10. Ga naar **Grootboek > Journaalboekingen > Algemene journalen**.
11. Selecteer het journaalbatchnummer voor het journaal dat uw afschrijving bevat. Er wordt één regel gemaakt om het klantsaldo om te keren. Er worden een of meer regels gemaakt om de afschrijving naar de afschrijvingsrekening te boeken.  
12. Sluit de pagina.
13. Sluit de pagina.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Een factuur afschrijven vanaf de pagina Openstaande klantfacturen
1. Ga in het navigatievenster naar **Modules > Klanten > Facturen > Openstaande klantfacturen**.
2. Markeer de regel voor een factuur. Markeer bijvoorbeeld de regel voor CIV-000667.
3. Klik in het **actievenster** op **Factuur**.
4. Klik op **Afschrijven**.
5. Klik op **OK**.
6. Sluit de pagina.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Een klantsaldo afschrijven van de klantpagina
1. Ga naar **Klanten > Klanten > Alle klanten**.
2. Een klantrekening selecteren. Selecteer bijvoorbeeld US-001 (Contoso Retail San Diego).
3. Klik in het **actievenster** op **Incasso**.
4. Klik op **Afschrijven**.
5. Klik op **OK**.
6. Sluit de pagina.

