---
title: Automatische vereffening en prioriteitstelling
description: Dit onderwerp beschrijft hoe transacties worden vereffend als u Automatische vereffening op de pagina Parameters van module Klanten selecteert. Het legt ook uit hoe de automatische vereffening in combinatie met de betalingsprioriteit kan worden gebruikt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 043f403c22ae3334e28dedda3b65136499822d9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993084"
---
# <a name="automatic-settlement-and-prioritization"></a>Automatische vereffening en prioriteitstelling

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft hoe transacties worden vereffend als u Automatische vereffening op de pagina Parameters van module Klanten selecteert. Het legt ook uit hoe de automatische vereffening in combinatie met de betalingsprioriteit kan worden gebruikt.

U hebt twee opties wanneer u betalingen met facturen en andere transacties vereffent. U kunt de te vereffenen transacties handmatig selecteren of u kunt de transacties in het systeem automatisch laten selecteren door de functie Automatische vereffeningen te gebruiken. U kunt ook aanpassen hoe automatische vereffeningen worden verwerkt door de optie **Prioriteit van vereffening** te gebruiken. Al deze opties maken deel uit van de vereffeningparameters die zijn gedefinieerd op de pagina **Parameters van module Klanten**. De manier waarop transacties automatisch worden vereffend kan verschillen, afhankelijk van de methode die u voor automatische vereffening gebruikt. De volgende methoden zijn beschikbaar:

-   Door gebruiker gedefinieerde prioriteit van vereffening
-   Standaard automatische vereffening

De volgende secties beschrijven hoe transacties worden vereffend voor elke methode.

## <a name="example-transactions"></a>Voorbeelden van transacties
De voorbeelden van vereffeningen verderop in dit artikel zijn gebaseerd op de volgende transacties. Alle transacties zijn voor klant 2050.

| Transactie   | Datum        | Bedrag | Voorwaarden voor contantkorting | Datum voor contantkorting | Opmerkingen                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Factuur 1     | 15 augustus   | 100,00 | 2%14, netto 30        | 29 augustus          |                                                                                                                                                                                               |
| Factuur 2     | 1 september | 250,00 | 2%14, netto 30        | 15 september       |                                                                                                                                                                                               |
| Factuur 3     | 15 oktober  | 500,00 | 2% 14/Net 30        | 29 oktober         |                                                                                                                                                                                               |
| Rentenota | 15 oktober  | 7,00   |                     |                    | Deze rentenota is voor factuur 1 en factuur 2. Het bedrag wordt berekend als rente van 2 procent op bedragen van meer dan 30 dagen na de vervaldatum. Bijvoorbeeld: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Door gebruiker gedefinieerde prioriteit van vereffening
Als u **Prioriteit gebruiken voor automatische vereffeningen** instelt op **Ja** op de pagina **Parameters van module Klanten**, wordt de vereffeningsprioriteit die u op de pagina **Vereffeningsprioriteit** definieert gebruikt wanneer transacties worden geselecteerd voor automatische vereffening. Voor dit voorbeeld wordt de volgende vereffeningsprioriteit gedefinieerd:

1.  Transactietype
    -   Betalingskosten
    -   Aanmaningen
    -   Rentenota's
    -   Facturen

2.  Transactiedatum, oplopend
3.  Boekstuk

Als u op 25 oktober een betaling voor 700,00 boekt, wordt de betaling in deze volgorde vereffend met de transacties.

| Boekstuk       | Datum       | Factuur | Bedrag in transactievaluta | Bedrag om te vereffenen | Saldo | Valuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Rentenota | 10/15/2015 |         | 7,00                           | 7,00             | 0,00    | USD      |
| Factuur 1     | 8/15/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Factuur 2     | 9/1/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Factuur 3     | 10/15/2015 |         | 500,00                         | 343,00           | 157,00  | USD      |

## <a name="default-automatic-settlement"></a>Standaard automatische vereffening
Als er geen vereffeningsprioriteit voor de gebruiker gedefinieerd is, worden transacties automatisch voor vereffening geselecteerd op basis van de vervaldatum. De transacties die vereffend worden moeten dezelfde valuta hebben als de transactie waarmee deze vereffend worden. Als u op 25 oktober een betaling voor 700,00 boekt, worden de volgende transacties voor vereffening geselecteerd.

| Boekstuk       | Datum       | Factuur | Bedrag in transactievaluta | Bedrag om te vereffenen | Saldo | Valuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Factuur 1     | 8/15/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Factuur 2     | 9/1/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Factuur 3     | 10/15/2015 |         | 500.00                         | 350.00           | 150.00  | EUR      |
| Rentenota | 10/15/2015 |         | 7.00                           | 0,00             | 7.00    | EUR      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]