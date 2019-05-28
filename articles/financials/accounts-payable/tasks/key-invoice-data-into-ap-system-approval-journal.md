---
title: Belangrijke factuurgegevens in leverancierssysteem met goedkeuringsjournaal
description: Deze taakbegeleiding toont hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550369"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Belangrijke factuurgegevens in leverancierssysteem met goedkeuringsjournaal

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding toont hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.


## <a name="create-and-post-and-invoice"></a>Een factuur maken en boeken
1. Ga naar Leveranciers > Facturen > Facturenregister.
2. Klik op Nieuw.
3. Selecteer de naam van het facturenregister dat u wilt gebruiken.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik op Regels om het register te openen en onkostenregels in te voeren.
6. Selecteer een leverancier. Typ of selecteer bijvoorbeeld US-104
7. Typ een waarde in het veld Factuur.
8. Typ een waarde in het veld Omschrijving.
9. Voer een nummer in het veld Credit in.
10. Klik in het veld Goedgekeurd door op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Markeer een fiatteur en klik op Selecteren om die fiatteur te selecteren.
12. Klik op Boeken.
13. Sluit de pagina.
14. Sluit de pagina.

## <a name="approve-an-invoice"></a>Een factuur goedkeuren
1. Ga naar Leveranciers > Facturen > Factuurgoedkeuring.
2. Klik op Nieuw.
3. Selecteer de naam van het factuurgoedkeuringsjournaal dat u wilt gebruiken.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik op regels om een pagina weer te geven waarin u de facturen kunt selecteren die u wilt goedkeuren.
6. Selecteer Boekstukken zoeken om alle facturen weer te geven die klaar staan voor goedkeuring.
7. Markeer de factuur die u hebt gemaakt.
8. Klik op Selecteren.
    * De boekstukken die u boven hebt geselecteerd worden naar deze lijst verplaatst nadat u ze selecteert.  
9. Klik op OK.
10. Klik op het rekeningnummerveld om een onkostenrekening aan de factuur toe te voegen.
11. Geef een rekeningnummer op en ga met Tab uit het veld. Voer bijvoorbeeld 600120 in.
12. Klik op Boeken.
13. Klik op Boekstuk om de gegevens weer te geven die zijn geboekt.
    * De rekening Facturen in afwachting van goedkeuring wordt tegengeboekt en vervangen door de werkelijke onkostenrekening.  

