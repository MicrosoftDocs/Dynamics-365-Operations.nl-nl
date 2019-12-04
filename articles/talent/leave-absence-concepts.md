---
title: De concepten verlof en verzuim
description: In dit onderwerp worden de concepten verlof en verzuim beschreven en wordt aangegeven hoe verlofsaldi worden bepaald.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3dbf5807a213e425b24d5a4809df694393faeb9b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832763"
---
# <a name="leave-and-absence-concepts"></a>De concepten verlof en verzuim

[!include [banner](includes/banner.md)]

Op basis van de hier beschreven concepten en termen kunt u bepalen hoe aan een werknemer verlof wordt toegekend en hoe de tijdsaldi van die werknemer worden berekend. Zie [Beheer van verlof en verzuim](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview) voor meer informatie over verlof- en verzuimbeheer.

## <a name="leave-plan-details"></a>Verlofplandetails

### <a name="start-date"></a>Begindatum

De begindatum is de datum waarop de daadwerkelijke toerekeningsverwerking begint. De begindatum dient ook als de overgangsdatum die wordt gebruikt om transportbedragen te berekenen.

## <a name="accruals"></a>Transitorische posten

Transitorische posten bepalen wanneer en hoe vaak verlof wordt toegekend aan een werknemer. Beleidsregels over wanneer transitorische posten moeten worden toegekend en beleidsregels over betaling naar rato worden bij het instellen van het verlof- en verzuimplan gedefinieerd in de sectie **Transitorische posten**.

### <a name="accrual-frequency"></a>Toerekenfrequentie

De toerekenfrequentie bepaalt hoe vaak verlof wordt toegerekend of toegekend. De volgende opties zijn beschikbaar:

- Dagelijks
- Wekelijks
- Om de twee weken
- Halfmaandelijks
- Maandelijks
- Driemaandelijks
- Halfjaarlijks
- Jaarlijks
- Geen

### <a name="accrual-period-basis"></a>Basis toerekenperiode

De basis voor de toerekenperiode bepaalt welke datum wordt gebruikt om toerekenperioden te berekenen. De volgende opties zijn beschikbaar:

- **Begindatum plan**
- **Werknemerspecifieke datum**: als deze optie is geselecteerd, bepaalt de waarde de bron van de eerste datumwaarde die wordt gebruikt om toerekenperioden te berekenen. De volgende opties zijn beschikbaar:

    - Aangepast
    - Jubileumdatum
    - Oorspronkelijke datum indiensttreding
    - Anciënniteitsdatum
    - Aangepaste begindatum van medewerker
    - Begindatum van medewerker

### <a name="accrual-award-date"></a>Toewijzingsdatum toerekening

De toewijzingsdatum voor de toerekening bepaalt wanneer verlof wordt toegekend aan een werknemer. De volgende opties zijn beschikbaar:

- **Einddatum toerekeningsperiode**: aan de werknemer wordt verlof toegekend op de laatste dag van de toekenningsperiode.

    Als u het juiste bedrag wilt toerekenen, moet het toerekeningsproces de gehele periode omvatten. De toerekeningsperiode is bijvoorbeeld van 1 januari 2018 tot en met 31 januari 2018. In dat geval moet de toerekening voor 1 februari 2018 worden uitgevoerd als januari hierin moet worden opgenomen.

- **Begindatum toerekeningsperiode**: aan de werknemer wordt verlof toegekend op de eerste dag van de toekenningsperiode.

### <a name="accrual-policy-on-enrollment"></a>Toerekeningsbeleid bij inschrijving

Met het toerekeningsbeleid bij inschrijving wordt gedefinieerd hoe de toerekening wordt berekend wanneer een werknemer tijdens een toerekeningsperiode wordt ingeschreven. De volgende opties zijn beschikbaar:

- **Evenredig**: het datumbereik tussen de inschrijvingsdatum en de begindatum wordt gebruikt om het verschil in dagen te bepalen. Dat verschil wordt toegepast wanneer toerekeningen worden verwerkt.
- **Volledige toerekening**: het volledige toerekeningsbedrag, gebaseerd op het niveau, wordt toegekend tijdens de eerste toerekeningsverwerking.
- **Geen toerekening**: geen toerekening tot de volgende toerekeningsperiode.

### <a name="accrual-policy-on-unenrollment"></a>Toerekeningsbeleid bij uitschrijving

Met het toerekeningsbeleid bij uitschrijving wordt gedefinieerd hoe de toerekening wordt berekend wanneer een werknemer tijdens een toerekeningsperiode wordt uitgeschreven. De volgende opties zijn beschikbaar:

- **Evenredig**: het datumbereik tussen de inschrijvingsdatum en de begindatum wordt gebruikt om het verschil in dagen te bepalen. Dat verschil wordt toegepast wanneer toerekeningen worden verwerkt.
- **Volledige toerekening**: het volledige toerekeningsbedrag, gebaseerd op het niveau, wordt toegekend tijdens de eerste toerekeningsverwerking.
- **Geen toerekening**: geen toerekening tot de volgende toerekeningsperiode.

## <a name="accrual-schedule"></a>Toerekeningsschema

Het toerekeningsschema bepaalt hoe een werknemer verlof verzamelt en welke bedragen deze werknemer verzamelt en transporteert. Er kunnen niveaus worden gemaakt, zodat verlof wordt toegekend op basis van verschillende niveaus.

### <a name="months-of-service"></a>Servicemaanden

Met de waarde bij **Servicemaanden** wordt het minimum aantal maanden bepaald dat werknemers moeten werken om recht op toerekeningen te hebben. Als er geen minimum vereist is voor werknemers, stelt u de waarde in op **0**.

### <a name="hours-worked"></a>Gewerkte uren

Met de waarde bij **Gewerkte uren** wordt het minimum aantal uren bepaald dat werknemers per toerekeningsperiode moeten werken om recht op toerekeningen te hebben. Als er geen minimum vereist is voor werknemers, stelt u de waarde in op **0**.

### <a name="accrual-amount"></a>Toerekeningsbedrag

Het toerekeningsbedrag is het aantal uren of dagen dat werknemers per periode verzamelen. De periode is gebaseerd op de toerekeningsfrequentie.

### <a name="minimum-balance"></a>Minimumsaldo

Een negatieve waarde kan worden gebruikt voor het minimumsaldo als werknemers meer verlof kunnen aanvragen dan er beschikbaar is.

### <a name="maximum-carry-forward"></a>Maximaal transport

Met het toerekeningsproces worden verlofsaldi aangepast die het maximale transportsaldo op de verjaardag van de begindatum overschrijden.

### <a name="grant-amount"></a>Toewijzingshoeveelheid

De toewijzingshoeveelheid heeft betrekking op het oorspronkelijke aantal uren of dagen dat werknemers krijgen wanneer ze zich inschrijven voor het verlofplan. Deze hoeveelheid wordt niet voor elke toerekeningperiode verzameld.

## <a name="enrollments-and-balances"></a>Inschrijvingen en saldi

### <a name="enrollment-date"></a>Inschrijvingsdatum

De inschrijvingsdatum bepaalt wanneer een werknemer kan beginnen met het verzamelen van verlof. Als een werknemer bijvoorbeeld op 15 juni 2018 wordt ingeschreven voor een vakantieplan, kan zij geen verlof verzamelen vóór 15 juni 2018.

### <a name="current-balance"></a>Huidig saldo

Het huidige saldo is de hoeveelheid verloftijd die beschikbaar is voor verlofaanvragen. In deze hoeveelheid zijn toerekeningen, goedgekeurde aanvragen en correcties tot en met de huidige datum verwerkt.

### <a name="current-balance-examples"></a>Voorbeelden van huidig saldo

#### <a name="annual-plan"></a>Jaarlijks plan

**Planinstellingen**

| Begindatum plan | Inschrijvingsdatum | Toerekenfrequentie | Basis toerekenperiode | Toewijzingsdatum toerekening    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Jaarlijks            | Begindatum plan      | Einde van toerekeningsperiode |

Toerekeningen worden verwerkt op 1 januari 2019 (1-1-2019), zodat die gehele periode is opgenomen.

**Resultaten**

| Toerekeningsbedrag | Minimumsaldo | Maximaal transport | Aanvraagbedrag | Huidig saldo (op 1-1-2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Huidig saldo (160) = Toerekeningsbedrag (200) – Aanvraagbedrag (40)

#### <a name="semimonthly-plan"></a>Halfmaandelijks plan

**Planinstellingen**

| Begindatum plan | Inschrijvingsdatum | Toerekenfrequentie | Basis toerekenperiode | Toewijzingsdatum toerekening    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halfmaandelijks       | Begindatum plan      | Einde van toerekeningsperiode |

Toerekeningen worden verwerkt op 1 mei 2018 (1-5-2018), zodat die gehele periode is opgenomen.

**Resultaten**

| Toerekeningsbedrag | Minimumsaldo | Maximaal transport | Aanvraagbedrag | Huidig saldo (op 1-1-2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Huidig saldo (22) = Toerekeningsbedrag (5 × 6) – Aanvraagbedrag (8)

#### <a name="monthly-plan"></a>Maandelijks plan

**Planinstellingen**

| Begindatum plan | Inschrijvingsdatum | Toerekenfrequentie | Basis toerekenperiode | Toewijzingsdatum toerekening    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halfmaandelijks       | Begindatum plan      | Einde van toerekeningsperiode |

Toerekeningen worden verwerkt op 1 mei 2018 (1-5-2018), zodat die gehele periode is opgenomen.

**Resultaten**

| Toerekeningsbedrag | Minimumsaldo | Maximaal transport | Aanvraagbedrag | Huidig saldo (op 1-1-2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Huidig saldo (7) = Toerekeningsbedrag (5 × 3) – Aanvraagbedrag (8)

### <a name="forecasted-balance"></a>Voorspeld saldo

Het *voorspelde saldo* is de hoeveelheid verlof die beschikbaar is op een toekomstige datum. Toerekeningen en getransporteerde correcties worden geraamd tot die datum.

De volgende formule wordt hierbij gebruikt:

Voorspeld saldo voor maandag = Huidig saldo – Aanvragen + Toerekeningen – Getransporteerde correctie

### <a name="forecasted-balance-examples"></a>Voorbeelden van voorspeld saldo

#### <a name="annual-plan"></a>Jaarlijks plan

**Planinstellingen**

| Begindatum plan | Inschrijvingsdatum | Toerekenfrequentie | Basis toerekenperiode | Toewijzingsdatum toerekening    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Jaarlijks            | Begindatum plan      | Einde van toerekeningsperiode |

Toerekeningen worden verwerkt op 15 februari 2019 (15-2-2019), zodat die gehele periode is opgenomen.

**Resultaten**

| Toerekeningsbedrag | Minimumsaldo | Maximaal transport | Huidig saldo | Voorspeld saldo (op 15-2-2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Voorspeld saldo (40) = Toerekeningsbedrag (20) + Huidig saldo (40) – Getransporteerde correctie (20)

#### <a name="semimonthly-plan"></a>Halfmaandelijks plan

**Planinstellingen**

| Begindatum plan | Inschrijvingsdatum | Toerekenfrequentie | Basis toerekenperiode | Toewijzingsdatum toerekening    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halfmaandelijks       | Begindatum plan      | Einde van toerekeningsperiode |

Toerekeningen worden verwerkt op 15 februari 2019 (15-2-2019), zodat die gehele periode is opgenomen.

**Resultaten**

| Toerekeningsbedrag | Minimumsaldo | Maximaal transport | Huidig saldo | Voorspeld saldo (op 15-2-2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Voorspeld saldo (35) = Toerekeningsbedrag (5 × 3) + Huidig saldo (40) – Getransporteerde correctie (20)

#### <a name="monthly-plan"></a>Maandelijks plan

**Planinstellingen**

| Begindatum plan | Inschrijvingsdatum | Toerekenfrequentie | Basis toerekenperiode | Toewijzingsdatum toerekening    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Halfmaandelijks       | Begindatum plan      | Einde van toerekeningsperiode |

Toerekeningen worden verwerkt op 15 februari 2019 (15-2-2019), zodat die gehele periode is opgenomen.

**Resultaten**

| Toerekeningsbedrag | Minimumsaldo | Maximaal transport | Huidig saldo | Voorspeld saldo (op 15-2-2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Voorspeld saldo (30) = Toerekeningsbedrag (10 × 1) + Huidig saldo (40) – Getransporteerde correctie (20)

### <a name="proration-balance-examples"></a>Voorbeelden van evenredig saldo

#### <a name="prorated-monthly-plan"></a>Maandelijks plan Evenredig

**Planinstellingen**

| Begindatum plan | Toerekenfrequentie | Basis toerekenperiode |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Maandelijks           | Begindatum plan      |

**Resultaten**

| Werknemer            | Servicemaanden | Inschrijvingsdatum | Begindatum | Toerekeningsbedrag | Toerekening verwerken | Balans |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2.53    |

#### <a name="full-accrual-monthly-plan"></a>Maandelijks plan Volledige toerekening

**Planinstellingen**

| Begindatum plan | Toerekenfrequentie | Basis toerekenperiode |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Maandelijks           | Begindatum plan      |

**Resultaten**

| Werknemer            | Servicemaanden | Inschrijvingsdatum | Begindatum | Toerekeningsbedrag | Toerekening verwerken | Balans |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Maandelijks plan Geen toerekening

**Planinstellingen**

| Begindatum plan | Toerekenfrequentie | Basis toerekenperiode |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Maandelijks           | Begindatum plan      |

**Resultaten**

| Werknemer            | Servicemaanden | Inschrijvingsdatum | Begindatum | Toerekeningsbedrag | Toerekening verwerken | Balans |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2.00    |
