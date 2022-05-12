---
title: Scenario's voor afstemmingsdatums
description: In dit onderwerp vindt u voorbeelden die laten zien hoe afstemmingsdatums werken bij facturering van abonnementen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e80797e8dd532bb4b2ef78422b459487430d83d6
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629432"
---
# <a name="alignment-date-scenarios"></a>Scenario's voor afstemmingsdatums

In dit onderwerp vindt u voorbeelden die laten zien hoe afstemmingsdatums werken bij facturering van abonnementen.

Voor deze voorbeelden heeft een factureringsdetail voor een factureringsschema de afstemmingsdatum 31 oktober 2019. Het eerste factureringsdetail voor de regel eindigt op 31 oktober 2019 en wordt overeenkomstig omgeslagen. De regel wordt automatisch vernieuwd met 11 november als begindatum voor verlenging.

> [!NOTE]
> Het jaar is relevant omdat de afstemmingsdatum hierdoor meer of minder dan een jaar kan zijn. Voor deze voorbeelden is de methode voor betaling naar rato ingesteld op **Maandelijks** op de pagina **Terugkerende contractfactureringsparameters** Als deze parameter is ingesteld op **Dagelijks**, zullen sommige gedeeltelijke bedragen afwijken.

## <a name="scenario-1-no-alignment"></a>Scenario 1: geen afstemming

Het factureringsschema wordt opgezet met de volgende gegevens:

- **Begindatum:** 1 mei 2019
- **Einddatum:** 31 december 2024
- **Bedrag:** $1000

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 1-5-2019 | 30-4-2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-5-2020 | 30-4-2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-5-2021 | 30-4-2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-5-2022 | 30-4-2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-5-2023 | 30-4-2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-5-2024 | 31-12-2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>Scenario 2: verkorte afstemming

Het factureringsschema wordt opgezet met de volgende gegevens:

- **Begindatum:** 1 mei 2019
- **Einddatum:** 31 december 2024
- **Bedrag:** $1000
- **Afstemmingsdatum:** 31 december 2019

Het eerste verlengingsbedrag is voor minder dan één jaar.

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 1-5-2019 | 31-12-2019 | | | 1.00 | | 1.00 | 666.67 |
| 1-1-2020 | 31-12-2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2021 | 31-12-2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2022 | 31-12-2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2023 | 31-12-2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2024 | 31-12-2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>Scenario 3: verlengde afstemming

Het factureringsschema wordt opgezet met de volgende gegevens:

- **Begindatum:** 1 mei 2019
- **Einddatum:** 31 december 2024
- **Bedrag:** $1000
- **Afstemmingsdatum:** 31 december 2020

Het eerste verlengingsbedrag is voor meer dan één jaar.

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 1-5-2019 | 31-12-2020 | | | 1.00 | | 1.00 | 1,666.67 |
| 1-1-2021 | 31-12-2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2022 | 31-12-2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2023 | 31-12-2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2024 | 31-12-2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>Scenario 4: afstemming met een andere eindmaand

Het factureringsschema wordt opgezet met de volgende gegevens:

- **Begindatum:** 1 mei 2019
- **Einddatum:** 31 oktober 2024
- **Bedrag:** $1000
- **Afstemmingsdatum:** 31 december 2019

> [!NOTE]
> Dit scenario komt niet vaak voor.

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 1-5-2019 | 31-12-2019 | | | 1.00 | | 1.00 | 666.67 |
| 1-1-2020 | 31-12-2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2021 | 31-12-2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2022 | 31-12-2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2023 | 31-12-2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1-1-2024 | 31-10-2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>Scenario 5: een gedeeltelijk jaar

Het factureringsschema wordt opgezet met de volgende gegevens:

- **Begindatum:** 1 mei 2019
- **Einddatum:** 31 december 2019
- **Bedrag:** $1000
- **Afstemmingsdatum:** 31 december 2019

In dit scenario is de afstemmingsdatum niet nodig. Dit scenario wordt vaak gebruikt voor automatische verlengingen.

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 1-5-2019 | 31-12-2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>Scenario 6: berekende datums

Het ondersteuning en verlenging wordt opgezet met de volgende gegevens:

- **Begindatum overschrijven:** Nee
- **Begindatums voor ondersteuning en verlenging:** begin van volgende maand
- **Boekingsdatum van factuur:** 22 juni 2019
- **Afstemmingsdatum:** 31 december 2020

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 1-7-2019 | 31-7-2019 | | | 1.00 | | 1.00 | 297.60 |
| 1-8-2019 | 31-12-2020 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>Scenario 7: berekende datums en boekingen in de toekomst

Het ondersteuning en verlenging wordt opgezet met de volgende gegevens:

- **Begindatum overschrijven:** Nee
- **Begindatums voor ondersteuning en verlenging:** begin van volgende maand
- **Boekingsdatum van factuur:** 22 juni 2019
- **Afstemmingsdatum:** 31 december 2020

Voor dit scenario wordt de afstemmingsdatum gewijzigd in 31 december 2021.

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 22-6-2019 | 22-6-2019 | | | 1.00 | | 1.00 | 0,00 |
| 1-8-2019 | 31-12-2020 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Scenario 8: handmatige datums en meerdere jaren

Het ondersteuning en verlenging wordt opgezet met de volgende gegevens:

- **Begindatum overschrijven:** Ja
- **Begindatum verlenging:** 1 juli 2020
- **Einddatum verlenging:** 31 december 2024
- **Afstemmingsdatum:** 31 december 2021

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 22-6-2019 | 22-6-2019 | | | 1.00 | | 1.00 | 0,00 |
| 1-7-2020 | 31-12-2021 | | | 1.00 | | 1.00 | 375.00 |
| 1-1-2022 | 31-12-2022 | | | 1.00 | | 1.00 | 250,00 |
| 1-1-2023 | 31-12-2023 | | | 1.00 | | 1.00 | 250,00 |
| 1-1-2024 | 31-12-2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Scenario 9: handmatige datums, meerdere jaren en een andere eindmaand

Het ondersteuning en verlenging wordt opgezet met de volgende gegevens:

- **Begindatum overschrijven:** Ja
- **Begindatum verlenging:** 1 juli 2020
- **Einddatum verlenging:** 31 oktober 2024
- **Afstemmingsdatum:** 31 december 2021

| Begindatum facturering | Einddatum facturering | Vorige meting | Huidige meting | Ingevoerde hoeveelheid | Vrije hoeveelheid | Factureerbare hoeveelheid | Eenheidsprijs |
|---|---|---|---|---|---|---|---|
| 22-6-2019 | 22-6-2019 | | | 1.00 | | 1.00 | 0,00 |
| 1-7-2020 | 31-12-2021 | | | 1.00 | | 1.00 | 375.00 |
| 1-1-2022 | 31-12-2022 | | | 1.00 | | 1.00 | 250,00 |
| 1-1-2023 | 31-12-2023 | | | 1.00 | | 1.00 | 250,00 |
| 1-1-2024 | 31-10-2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Scenario 10: afstemming zonder betaling naar rato

Het ondersteuning en verlenging wordt opgezet met de volgende gegevens:

- **Begindatum overschrijven:** Nee
- **Boekingsdatum van factuur:** 22 juni 2019
- **Afstemmingsdatum:** 31 december 2019

De begindatum voor verlenging en de afstemmingsdatums zijn aangepast, zodat beide begindatums na de boekingsdatum liggen.

- **Begindatum verlenging:** 1 januari 2020
- **Einddatum verlenging:** 31 december 2020
