---
title: Factuurgegevens invoeren in leveranciers met behulp van een goedkeuringsjournaal
description: In dit onderwerp wordt getoond hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ce66a4b92f26bcec0849accad3878aef2b2f658
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109651"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Factuurgegevens invoeren in leveranciers met behulp van een goedkeuringsjournaal

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt getoond hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.

## <a name="create-and-post-and-invoice"></a>Een factuur maken en boeken
1. Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Facturenregister**.
2. Selecteer **Nieuw**.
3. Selecteer de naam van het facturenregister dat u wilt gebruiken.
4. Selecteer **Regels** om het register te openen en onkostenregels in te voeren.
5. Selecteer een leverancier. Typ of selecteer bijvoorbeeld `US-104`.
6. Typ een waarde in het veld **Factuur**.
7. Typ een waarde in het veld **Beschrijving**.
8. Voer in het veld **Krediet** een numerieke waarde in.
9. Selecteer in het veld **Goedgekeurd door** een fiatteur in het vervolgkeuzemenu.
10. Selecteer **Boeken**.

## <a name="approve-an-invoice"></a>Een factuur goedkeuren
1. Ga in het navigatiedeelvenster naar **Modules > Leveranciers > Facturen > Goedkeuring van facturen**.
2. Selecteer **Nieuw**.
3. Selecteer de naam van het factuurgoedkeuringsjournaal dat u wilt gebruiken.
4. Selecteer **Regels** om een pagina weer te geven waarin u de facturen kunt selecteren die u wilt goedkeuren.
5. Selecteer **Boekstukken zoeken** om alle facturen weer te geven die klaar staan voor goedkeuring.
6. Markeer de factuur die u hebt gemaakt en klik op **Selecteren**. De boekstukken die u boven hebt geselecteerd worden naar deze lijst verplaatst nadat u ze selecteert.  
7. Selecteer **OK**.
8. Klik op het veld **Rekeningnummer** om een onkostenrekening aan de factuur toe te voegen.
9. Geef een rekeningnummer op en ga met Tab uit het veld. Voer bijvoorbeeld `600120` in.
10. Selecteer **Boeken**.
11. Klik op **Boekstuk** om de gegevens weer te geven die zijn geboekt. De rekening Facturen in afwachting van goedkeuring wordt tegengeboekt en vervangen door de werkelijke onkostenrekening.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
