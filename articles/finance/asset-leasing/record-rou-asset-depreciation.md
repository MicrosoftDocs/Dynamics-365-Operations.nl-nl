---
title: Afschrijving van activum met gebruiksrecht vastleggen (preview)
description: In dit artikel wordt uitgelegd hoe u de journaalboeking kunt maken voor de afschrijving die is vereist voor leases die worden herkend op de balans van een organisatie.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseAssetSchedule
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 93e521cf409af4c01d625f27bdd7a7564e471bd9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903271"
---
# <a name="record-right-of-use-asset-depreciation-preview"></a>Afschrijving van activum met gebruiksrecht vastleggen (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Voor leases die worden herkend op de balans van een organisatie, wordt het activum met gebruiksrecht maandelijks afgeschreven. In dit artikel wordt uitgelegd hoe u de journaalboeking voor de afschrijving maakt. De afschrijving wordt afgeschreven van de onkostengrootboekrekening en bijgeschreven opde samengevoegde afschrijvingsgrootboekrekening, op basis van de instellingen van uw boekingsprofiel en het leasetype. Deze boekingen kunnen voor elke lease worden gemaakt, of ze kunnen worden gemaakt voor meerdere leases met behulp van de batchjournaalfunctie.

## <a name="asset-depreciation-schedule"></a>Afschrijvingsschema van activa

1. Selecteer een lease op de pagina **Leaseoverzicht**. Selecteer vervolgens **Boeken \> Afschrijvingsschema activa** om de pagina **Afschrijvingsschema activa** te openen.

    Het journaalpost voor afschrijvingskosten van het RoU-activum is gebaseerd op het bedrag in de kolom **Afschrijvingskosten**. Zie het gedeelte [Afschrijvingskosten voor RoU-activum berekenen voor financiële leases](#calculation-of-rou-asset-amortization-expense-for-finance-leases) verderop in dit artikel voor een voorbeeld van de richtlijnen voor de naleving van de boekhoudstandaard.
    
2. Selecteer de afschrijvingperiode en selecteer **Journaal maken**. U ontvangt een bericht met de mededeling dat het journaal dat wordt gebruikt voor het vastleggen van de afschrijving is gemaakt.
3. Selecteer **Journalen \> Activaleasejournalen** om de pagina **Activaleasejournaal** te openen, waar u de gemaakte journaalpost voor afschrijvingskosten kunt bekijken.

   Bepaalde financiële velden worden door het systeem vergrendeld, zodat eventuele afwijkingen tussen de transacties en de planningen worden voorkomen. Sommige velden die vergrendeld zijn, zijn: **Rekening**, **Bedragen**, **Financiële dimensies**, **Valuta** en **Transactietype**. Bovendien kunt u geen journaalinvoerregels aan een activa-leasejournaalinvoer toevoegen of daaruit verwijderen, omdat dit tot discrepanties tussen de planningen en de transacties kan leiden.

4. Selecteer de journaalboeking en selecteer vervolgens **Boeken** om de afschrijvingspost vast te leggen in het grootboek.

## <a name="calculation-of-rou-asset-amortization-expense-for-operating-leases"></a>Berekenen van afschrijvingskosten voor RoU-activa voor operationele leases

De afschrijvingskosten van een operationele lease worden berekend als het verschil tussen de maandelijkse lineaire leaseonkosten en de maandelijkse rentelasten op de leaseverplichtingen, in overeenstemming met Accounting Standards Codification Topic 842 (ASC 842), de standaard in algemeen geaccepteerde boekhoudprincipes in de Verenigde Staten (US GAAP). De lineaire leaseonkosten worden berekend als de som van alle leasebetalingen gedeeld door de leasetermijn in maanden. (De som van leasebetalingen omvat alle vooruitbetalingen, de initiële directe kosten, de ontmantelingskosten en de leasebonussen.) In de volgende tabel ziet u een voorbeeld van de afschrijvingskosten voor een operationele lease.

### <a name="example-of-rou-asset-amortization-expense-for-operating-leases"></a>Voorbeeld van afschrijvingskosten voor RoU-activa voor operationele leases

| Veld                                          | Waarde       |
|------------------------------------------------|-------------|
| Betalingsbedrag                                 | 1.000       |
| Betalingsfrequentie                              | Maandelijks     |
| Leasetermijn (maanden)                            | 24          |
| Totaal leasebetalingen                           | 24,000      |
| Verhoogd leningtarief                     | 5%          |
| Type annuïteit                                   | Te betalen annuïteit |
| Samenstellingsinterval                           | Maandelijks     |
| Contante waarde van toekomstige minimale leasebetalingen | 22,888.87   |

Zoals eerder vermeld worden de lineaire leaseonkosten berekend als de som van alle leasebetalingen gedeeld door de leasetermijn. De maandelijkse rentelasten worden automatisch door het systeem berekend op het afschrijvingsschema voor verplichtingen. De rentelasten worden berekend met behulp van de methode van effectieve rente. De lineaire leaseonkosten worden door het systeem gebruikt om de rentelasten voor elke maand af te trekken. De waarde wordt gebruikt om het RoU-activum te verminderen.

| Maand | Lineaire leaseonkosten | Rente-uitgaven                        | Berekening van de afschrijvingskosten voor RoU-activa |
|-------|--------------------------|-----------------------------------------|-----------------------------------------------|
| 1     | (24.000 ÷ 24) = 1.000,00 | (22.888,87 – 1.000) × (5% ÷ 12) = 91,20 | 1.000 – 91,20 = 908,80                        |
| 2     | (24.000 ÷ 24) = 1.000,00 | (21.980,08 – 1.000) × (5% ÷ 12) = 87,42 | 1.000 – 87,42 = 912,58                        |
| 3     | (24.000 ÷ 24) = 1.000,00 | (21.067,49 – 1.000) × (5% ÷ 12) = 83,62 | 1.000 – 83,62 = 916,39                        |

> [!NOTE]
> Volgens ASC 842 wordt de afschrijving van het RoU-activum voor een operationele lease geclassificeerd als leaseonkosten op het inkomensoverzicht. Voor zichtbaarheid beschrijft de activalease de boeking als de afschrijving van het RoU-activum. De debetpost moet echter worden toegewezen aan een onkostenrekening voor operationele leases en de creditpost moet rechtstreeks worden toegewezen aan het RoU-activum voor de operationele lease. In de leaseparameters kunt u echter opgeven dat creditposten moeten worden gemaakt op een rekening voor de samengevoegde afschrijving voor RoU-activa.

Als de lease is geclassificeerd als een operationele lease, wordt de maandelijkse afschrijving na waardevermindering berekend met behulp van lineaire afschrijving.

## <a name="calculation-of-rou-asset-amortization-expense-for-finance-leases"></a>Berekenen van afschrijvingskosten voor RoU-activa voor financiële leases

Voor leases met een financiële classificatie wordt de afschrijving van RoU-activa op lineaire basis berekend. Daarom zijn de afschrijvingskosten voor elke maand gelijk.

In overeenstemming met de International Financial Reporting Standard 16 (IFRS 16) en ASC 842 wordt het activum afgeschreven over de leasetermijn of de economische levensduur van het activum, afhankelijk van wat minder is. Als de parameter **Overdracht van eigendom** is ingeschakeld voor de lease, wordt de lease bovendien automatisch afgeschreven over de economische levensduur van het activum.

### <a name="example-of-rou-asset-amortization-expense-for-finance-leases"></a>Voorbeeld van afschrijvingskosten voor RoU-activa voor financiële leases

| Veld                                | Waarde                                   |
|--------------------------------------|-----------------------------------------|
| Balans van activum met gebruiksrecht beginnen | 22,889.87                               |
| Leasetermijn (maanden)                  | 24                                      |
| Economische levensduur activum (maanden)           | 36                                      |
| Maand                                | Afschrijvingskosten van activum met gebruiksrecht |
| 1                                    | 22.889,87 ÷ 24 = 953,74                 |
| 2                                    | 22.889,87 ÷ 24 = 953,74                 |
| 3                                    | 22.889,87 ÷ 24 = 953,74                 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
