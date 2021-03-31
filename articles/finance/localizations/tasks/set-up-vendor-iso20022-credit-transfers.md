---
title: Leveranciers en bankrekeningen voor leveranciers voor ISO20022-kredietoverdrachten instellen
description: Deze procedure laat zien hoe u de leverancier- en leverancierspecifieke bankrekeninggegevens kunt instellen voor het genereren van bestanden voor ISO20022-kredietoverdracht of andere vormen van leveranciersbetalingen.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3a16d614efed0aafbf13fc59c17ab568811d82
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222034"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Leveranciers en bankrekeningen voor leveranciers voor ISO20022-kredietoverdrachten instellen

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u de leverancier- en leverancierspecifieke bankrekeninggegevens kunt instellen voor het genereren van bestanden voor ISO20022-kredietoverdracht of andere vormen van leveranciersbetalingen. 

Het demobedrijf dat wordt gebruikt om deze procedure te maken is DEMF.
Dit is de vierde van vijf taken die het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties. Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="set-up-bank-details"></a>Bankgegevens instellen
1. Ga naar Leveranciers > Leveranciers > Alle leveranciers.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Leveranciersrekening met een waarde van 'DE-001'.
3. Klik op DE-001 om de leveranciersgegevens te openen.
4. Klik in het actievenster op Leverancier.
5. Klik op Bankrekeningen.
6. Klik op Bewerken.
    * Als er geen bankrekening beschikbaar is, moet u een nieuwe maken.  
7. Typ 'COBADEFFXXX' in het veld SWIFT-code.
8. Typ 'DE36200400000628808808' in het veld IBAN.
9. Sluit de pagina.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Een betalingswijze voor de leverancier instellen
1. Klik op Bewerken.
2. Vouw de sectie Betaling uit of samen.
3. Klik in het veld Betalingsmethode op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de rij SEPA CT.
5. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]