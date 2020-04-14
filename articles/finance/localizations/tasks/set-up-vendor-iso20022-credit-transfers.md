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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4809a352f87cc3d88429461a06dfe36189ed5f31
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138964"
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

