---
title: Bankrekeningen voor ISO20022-automatische overschrijvingen voor een bank instellen
description: Deze taak voert u door het instellen van de bedrijfsspeifieke bankrekeninggegevens die zijn vereist voor het genereren van klantenbetalingsbestanden.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0f8ac369bb6b9a7a0f21c23aaddab2601ae3f8f37e2427cbb10b5509a7a2f23
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768712"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Bankrekeningen voor ISO20022-automatische overschrijvingen voor een bank instellen

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]