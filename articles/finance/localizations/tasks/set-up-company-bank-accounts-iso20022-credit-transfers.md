---
title: Bankrekeningen voor ISO20022-kredietoverdrachten voor een bank instellen
description: In deze procedure ziet u hoe u de bedrijfsspecifieke bankrekeninggegevens instelt die vereist zijn voor het genereren van SEPA-betalingsbestanden.
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
ms.openlocfilehash: a3b3b5ce9d7e24b2b7d3f76e4d770968df897b546df507ba9e3bde5aeac91715
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780765"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Bankrekeningen voor ISO20022-kredietoverdrachten voor een bank instellen

[!include [banner](../../includes/banner.md)]

In deze procedure ziet u hoe u de bedrijfsspecifieke bankrekeninggegevens instelt die vereist zijn voor het genereren van SEPA-betalingsbestanden. U configureert informatie die nodig is om de indeling voor de ISO20022-kredietoverdracht te genereren. Maar afhankelijk van de indeling kan ook andere informatie nodig zijn, zoals de bedrijfs-ID of de sorteercode. 

Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.

Dit is de tweede van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties. Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="set-up-iban-and-swift-code"></a>IBAN en SWIFT-code instellen
1. Ga naar Contanten en bankbeheer > Bankrekeningen.
2. Gebruik het snelfilter om op het veld Bankrekening te filteren met de waarde 'DEMF OPER'.
3. Klik op DEMF OPER om bankrekeninggegevens te openen.
4. Klik op Bewerken.
5. Vouw de sectie Aanvullende identificatie uit.
6. Typ 'DE89370400440532013000' in het veld IBAN.
7. Typ 'DEUTDEFF' in het veld SWIFT-code.
    * Merk op dat SWIFT/BIC niet voor veel betalingsindelingen is vereist. Het wordt echter wel aanbevolen om het te registreren voor een bankrekening.  
8. Klik op Opslaan.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Bankrekening instellen voor de rechtspersoon
1. Ga naar Organisatiebeheer > Organisaties > Rechtspersonen.
2. Klik op Bewerken.
3. Vouw de sectie Bankrekeninggegevens uit.
4. Typ of selecteer een waarde in het veld Bankrekening.
5. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]