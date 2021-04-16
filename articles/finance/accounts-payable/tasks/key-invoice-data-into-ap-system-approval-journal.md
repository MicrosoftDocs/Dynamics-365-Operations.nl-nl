---
title: Factuurgegevens invoeren in leveranciers met behulp van een goedkeuringsjournaal
description: In dit onderwerp wordt getoond hoe u het facturenregister gebruikt om facturen te maken en vervolgens het goedkeuringsjournaal gebruikt om de kostenrekeningen bij te werken.
author: abruer
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d01c04fcf707109cd7bc6f056846506914e96dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838880"
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