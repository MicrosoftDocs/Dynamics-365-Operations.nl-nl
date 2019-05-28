---
title: Bankrekeningen voor ISO20022-automatische overschrijvingen voor een bank instellen
description: Deze taak voert u door het instellen van de bedrijfsspeifieke bankrekeninggegevens die zijn vereist voor het genereren van klantenbetalingsbestanden.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 290d0eeb383dc3808935809e21b1bf6c99a8550a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552389"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Bankrekeningen voor ISO20022-automatische overschrijvingen voor een bank instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taak voert u door het instellen van de bedrijfsspeifieke bankrekeninggegevens die zijn vereist voor het genereren van klantenbetalingsbestanden. Deze procedure gebruikt als voorbeeld de indeling voor automatische incasso van ISO20022. Andere indelingen kunnen extra configuratie-informatie vereisen, zoals de bedrijfs-ID of de sorteercode.



Deze taak is gemaakt met het demobedrijf DEMF.



Dit is de tweede van vijf taken die het proces voor klantenbetalingen toelichten door middel van elektronische rapportageconfiguraties.


## <a name="set-up-the-iban-and-swift-codes"></a>De IBAN en SWIFT-code instellen
1. Ga naar Contanten en bankbeheer > Bankrekeningen.
2. Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'DEMF OPER'.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Bijvoorbeeld: klik op 'DEMF OPER' om de bankrekeninggegevens te openen.  
4. Klik op Bewerken.
5. Vouw de sectie Aanvullende identificatie uit of samen.
6. Typ een waarde in het veld IBAN.
    * Voer bijvoorbeeld 'DE89370400440532013000' in.  
7. Typ een waarde in het veld SWIFT-code.
    * Voer bijvoorbeeld 'DEUTDEFF' in.    Merk op dat SWIFT/BIC niet voor veel betalingsindelingen is vereist. Het wordt echter wel aanbevolen om het te registreren voor een bankrekening.  
8. Klik op Opslaan.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Een bankrekening instellen voor de rechtspersoon
1. Ga naar Organisatiebeheer > Organisaties > Rechtspersonen.
2. Klik op Bewerken.
3. Vouw de sectie Bankrekeninggegevens uit of samen.
4. Klik in het veld Bankrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Selecteer bijvoorbeeld de bankrekening "DEMF OPER".  
6. Klik op Opslaan.

