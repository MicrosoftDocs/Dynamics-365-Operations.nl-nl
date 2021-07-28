---
title: Voorspellingen voor klantbetalingen gebruiken (preview)
description: In dit onderwerp worden de vereisten en algemene stappen doorlopen die nodig zijn om een proefversie van de Financiële inzichten te gebruiken.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 873a11f3151344de63ee0b01b586ccbffe0df51b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355617"
---
# <a name="use-customer-payment-predictions-preview"></a>Voorspellingen voor klantbetalingen gebruiken (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u de Voorspellingen voor klantbetalingen kunt gebruiken. Voordat u deze functie gebruikt, moet u ervoor zorgen dat u de juiste installatiestappen hebt uitgevoerd. Zie [Voorspellingen voor klantbetalingen inschakelen](enable-cust-paymnt-prediction.md) voor meer informatie.

U kunt voorspellingen voor klantbetalingen weergeven in het werkgebied **Klantcreditering en -aanmaning beheren** en op twee nieuwe lijstpagina's: **Betalingsvoorspellingen per transactie** en **Betalingsvoorspelling per klant**.

### <a name="manage-customer-credit-and-collections-workspace"></a>Werkgebied Klantcreditering en -aanmaning beheren

Het werkgebied **Klantcreditering en -aanmaning beheren** bevat twee nieuwe tegels: **Betalingsvoorspelling per transactie** en **Klanten met voorspelde hoge late saldi**.

- De tegel **Betalingsvoorspelling per transactie** geeft het aantal openstaande klanttransacties weer die een betalingswaarschijnlijkheid hebben die kleiner is dan 50 procent in de bucket **Op tijd**. U kunt deze tegel selecteren om de lijstpagina **Betalingsvoorspellingen per transactie** te openen.
- De tegel **Klanten met voorspelde hoge late saldi** geeft het aantal klanten waarvoor meer dan de helft (50 procent) van het totaalsaldo wordt voorspeld om te laat en/of zeer laat betaald te worden. U kunt deze tegel selecteren om de lijstpagina **Betalingsvoorspelling per klant** te openen.

[![Werkgebied Klantcreditering en -aanmaning beheren.](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)

### <a name="payment-predictions-per-transaction-list-page"></a>Lijstpagina Betalingsvoorspellingen per transactie

Op de lijstpagina **Betalingsvoorspellingen per transactie** kunt u de betalingswaarschijnlijkheid voor openstaande transacties zien in de buckets **Op tijd**, **Te laat** en **Zeer laat**. Voor elke transactie in het raster wordt in de kolom **Waarschijnlijkheid Op tijd** de waarschijnlijkheid weergegeven dat de factuur op of vóór de vervaldatum wordt betaald. Als de waarschijnlijkheid van betaling op tijd kleiner is dan 50 procent, wordt er een rode cirkel weergegeven naast het percentage in de kolom **Waarschijnlijkheid Op tijd** om het risico van late betaling aan te geven.

[![Pagina Betalingsvoorspelling per transactie.](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)

Het venster **Gerelateerde informatie** aan de rechterkant van de pagina bevat meer details over de voorspellingen:

- Voor de transactie die is geselecteerd in het raster, wordt in het sneltabblad **Betalingsvoorspelling** de details weergegeven van de betalingsvoorspellingen in de buckets **Op tijd**, **Te laat** en **Zeer laat**. In het gedeelte **Belangrijkste factoren** worden de belangrijkste factoren weergegeven die invloed hebben op de voorspellingen. De belangrijkste factoren zijn kenmerken van de geselecteerde transactie en/of de klant voor die transactie.
- Het sneltabblad **Klantinzichten** bevat de huidige statistieken voor factuur, betaling en incasso voor de klant voor de geselecteerde transactie.
- Op het sneltabblad **Klanthistorie** wordt de betalingshistorie van de klant weergegeven in de buckets **Op tijd**, **Te laat** en **Zeer laat**.

De gegevens in het gedeelte **Belangrijkste factoren** en op de sneltabbladen **Klantinzichten** en **Klanthistorie** helpen u de betalingsvoorspellingen te begrijpen. Dit kan helpen uw vertrouwen in de effectiviteit van de voorspellingen te vergroten.

[![Grafische indicatoren voor betalingsvoorspellingenin het venster Gerelateerde informatie.](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)

### <a name="payment-prediction-per-customer-list-page"></a>Lijstpagina Betalingsvoorspelling per klant

Op de lijstpagina **Betalingsvoorspelling per klant** wordt het totale openstaande saldo weergegeven en het bedrag dat wordt voorspeld om te worden betaald in de buckets **Op tijd**, **Te laat** en **Zeer laat**.

[![Pagina Betalingsvoorspellingen per klant.](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)

Het betalingsbedrag in elke bucket wordt berekend als de som van het gewogen gemiddelde van het transactiesaldo. Dit bedrag wordt berekend op basis van de betalingskansen in elke bucket.

Een klant heeft bijvoorbeeld drie openstaande transacties met de volgende betalingskansen in elke bucket.

| Transactie | Bedrag | Waarschijnlijkheid betaling Op tijd | Waarschijnlijkheid betaling Te laat | Waarschijnlijkheid betaling Zeer laat |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| T1          | 100    | 10 procent                  | 50 procent               | 40 procent                    |
| T2          | 1.000  | 50 procent                  | 30 procent               | 20 procent                    |
| T3          | 10,000 | 1 procent                   | 4 procent                | 95 procent                    |

In dit geval worden betalingen voor elke bucket op de volgende manier voorspeld.

| Buckets   | Transactie T1      | Transactie T2         | Transactie T3            | Totaal |
|-----------|---------------------|------------------------|---------------------------|-------|
| Op tijd   | 100 × 10 ÷ 100 = 10 | 1.000 × 50 ÷ 100 = 500 | 10.000 × 1 ÷ 100 = 100    | 610   |
| Te laat      | 100 × 50 ÷ 100 = 50 | 1.000 × 30 ÷ 100 = 300 | 10.000 × 4 ÷ 100 = 400    | 750   |
| Erg laat | 100 × 40 ÷ 100 = 40 | 1.000 × 20 ÷ 100 = 200 | 10.000 × 95 ÷ 100 = 9.500 | 9,740 |

Het gedeelte **Gerelateerde informatie** aan de rechterkant van de pagina bevat meer details over de voorspellingen:

- Voor de transactie die is geselecteerd in het raster, wordt in het sneltabblad **Betalingsvoorspellingen** de details weergegeven van de betalingsvoorspellingen in de buckets **Op tijd**, **Te laat** en **Zeer laat**. In het gedeelte **Belangrijkste factoren** worden de belangrijkste factoren weergegeven die invloed hebben gehad op de betalingen. De belangrijkste factoren zijn kenmerken van de geselecteerde transactie en/of de klant voor die transactie.
- Het sneltabblad **Klantinzichten** bevat de huidige statistieken voor factuur, betaling en incasso voor de klant voor de geselecteerde transactie.
- Op het sneltabblad **Klanthistorie** wordt de betalingshistorie van de klant weergegeven in de buckets **Op tijd**, **Te laat** en **Zeer laat**.

De gegevens in het gedeelte **Belangrijkste factoren** en op de sneltabbladen **Klantinzichten** en **Klanthistorie** helpen u de betalingsvoorspellingen te begrijpen. Dit kan helpen uw vertrouwen in de effectiviteit van de voorspellingen te vergroten.

## <a name="improving-the-accuracy-of-payment-predictions"></a>De nauwkeurigheid van betalingsvoorspellingen verbeteren

U kunt de nauwkeurigheid van betalingsvoorspellingen bekijken door naar **Crediteringen en aanmaningen \> Instellingen \> Financiële inzichten \> Parameters voor financiële inzichten** te gaan. Op het tabblad **Inzichten in klantbetalingen** geeft het gedeelte **Voorspellingsmodel** de nauwkeurigheid van het prognosemodel als een percentage weer.

[![Nauwkeurigheid van betalingsvoorspellingen.](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)

Als u niet tevreden bent met de nauwkeurigheid, selecteert u de koppeling **Modelnauwkeurigheid verbeteren** om de extensie van AI Builder te openen. In de extensie AI Builder kunt u velden selecteren of de selectie van velden annuleren totdat u de velden hebt geselecteerd waarvan u denkt dat ze het belangrijkst zijn voor het nauwkeurig voorspellen van betalingskansen. Wanneer u klaar bent, kunt u het voorspellingsmodel eenvoudig opnieuw trainen en uw wijzigingen publiceren. Het nieuwe getrainde voorspellingsmodel wordt automatisch opgehaald voor voorspellingen in Dynamics 365 Finance.

[![Extensie AI Builder.](./media/ai-builder.png)](./media/ai-builder.png)

## <a name="release-details"></a>Releasegegevens

De openbare preview van Finance Insights is beschikbaar voor proefimplementaties in de Verenigde Staten van Amerika, Europa en het Verenigd Koninkrijk. Microsoft voegt incrementeel ondersteuning toe voor meer regio's.

Functies van de openbare preview kunnen en zouden alleen moeten worden ingeschakeld in Tier-2 sandbox-omgevingen. Setup-modellen en AI-modellen die in een sandbox-omgeving zijn gemaakt, kunnen niet naar een productieomgeving worden gemigreerd. Zie voor meer informatie [Aanvullende gebruiksrechtovereenkomst voor Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
