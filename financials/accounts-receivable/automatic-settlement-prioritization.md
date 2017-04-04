---
title: Automatische vereffening en prioriteiten
description: Dit artikel beschrijft hoe transacties worden vereffend als u Automatische vereffening op de pagina Parameters van module Klanten selecteert. Het legt ook uit hoe de automatische vereffening in combinatie met de betalingsprioriteit kan worden gebruikt.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a751973b49febd6925267d00fb1d2c72114f86b0
ms.lasthandoff: 03/31/2017


---

# <a name="automatic-settlement-and-prioritization"></a>Automatische vereffening en prioriteiten

Dit artikel beschrijft hoe transacties worden vereffend als u Automatische vereffening op de pagina Parameters van module Klanten selecteert. Het legt ook uit hoe de automatische vereffening in combinatie met de betalingsprioriteit kan worden gebruikt.

U hebt twee opties wanneer u betalingen met facturen en andere transacties vereffent. U kunt de te vereffenen transacties handmatig selecteren of Microsoft Dynamics 365 voor bewerkingen kunnen de transacties automatisch selecteren met de functie Automatische vereffening. U kunt ook aanpassen hoe automatische vereffeningen worden verwerkt door de optie **Prioriteit van vereffening** te gebruiken. Al deze opties maken deel uit van de vereffening parameters die zijn gedefinieerd op de **parameters van module klanten** pagina. De manier waarop transacties automatisch worden vereffend kan verschillen, afhankelijk van de methode die u voor automatische vereffening gebruikt. De volgende methoden zijn beschikbaar:

-   Door gebruiker gedefinieerde prioriteit van vereffening
-   Standaard automatische vereffening

De volgende secties beschrijven hoe transacties worden vereffend voor elke methode.

## <a name="example-transactions"></a>Voorbeelden van transacties
De voorbeelden van vereffeningen verderop in dit artikel zijn gebaseerd op de volgende transacties. Alle transacties zijn voor klant 2050.

| Transactie   | Datum        | Bedrag | Voorwaarden voor contantkorting | Datum voor contantkorting | Commentaar                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Factuur 1     | 15 augustus   | 100,00 | 2%14, Net 30        | 29 augustus          |                                                                                                                                                                                               |
| Factuur 2     | 1 september | 250,00 | 2%14, Net 30        | 15 september       |                                                                                                                                                                                               |
| Factuur 3     | 15 oktober  | 500,00 | 2% 14/Net 30        | 29 oktober         |                                                                                                                                                                                               |
| Rentenota | 15 oktober  | 7,00   |                     |                    | Deze rentenota is voor factuur 1 en 2. Het bedrag als 2 procent rente wordt berekend op bedragen die meer dan 30 dagen na de vervaldatum. Bijvoorbeeld: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="userdefined-settlement-priority"></a>Door de gebruiker gedefinieerde vereffeningsprioriteit
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
| Factuur 3     | 10/15/2015 |         | 500,00                         | 350,00           | 150,00  | USD      |
| Rentenota | 10/15/2015 |         | 7,00                           | 0,00             | 0,00    | USD      |




