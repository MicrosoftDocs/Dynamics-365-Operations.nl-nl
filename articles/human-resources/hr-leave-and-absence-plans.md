---
title: Een verlof- en verzuimplan maken
description: Maak verlofplannen in Dynamics 365 Human Resources voor verschillende verloftypen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ed7a47068c451cd3ffaa26ee709599373858721b
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087295"
---
# <a name="create-a-leave-and-absence-plan"></a>Een verlof- en verzuimplan maken

Definieer verlof- en verzuimplannen in Dynamics 365 Human Resources voor elk verloftype dat u aanbiedt. Toerekening voor verlof- en verzuimplannen kan plaatsvinden met verschillende frequenties, zoals jaarlijks, maandelijks of halfmaandelijks. U kunt ook een plan definiëren als beloning, met één toerekening op een bepaalde datum. Zo kunt u bijvoorbeeld een plan maken waarmee jaarlijks wisselende feestdagen worden toegekend.

Met gelaagde verlofplannen kunnen werknemers vergoedingen ontvangen op basis van hoe lang zij deel uitmaken van een organisatie. In gelaagde plannen wordt automatische inschrijving voor extra verlofuren ingeschakeld.

U kunt de maximale transport opgeven die u kunt meenemen of minimumsaldi om ervoor te zorgen dat werknemers alleen de verlofuren gebruiken die zij hebben opgebouwd.

Met een gelaagd plan kunt u bijvoorbeeld een vergoeding van 80 uur betaald verlof (PTO) toekennen aan nieuwe werknemers. Vervolgens kunt u 120 uur toekennen aan werknemers met een dienstverband van 60 maanden.

U kunt ook verlof toekennen op basis van positie, zoals speciale verlofuren voor leidinggevenden.

## <a name="create-a-leave-plan"></a>Een verlofplan maken

1. Selecteer op de pagina **Verlof en verzuim** de optie **Nieuw plan maken**.

2. Voer onder **Details** de **naam**, de **begindatum**, de **beschrijving** en het **verloftype** voor uw plan in.

3. Definieer toerekeningen op het tabblad **Toerekeningen**. Toerekeningen bepalen wanneer en hoe vaak een werknemer verloftijd ontvangt. In deze stap definieert u het beleid voor wanneer toerekeningen moeten worden toegekend en het beleid met betrekking tot het naar rato toekennen van verlof.

   1. Selecteer een waarde in de vervolgkeuzelijst **Toerekenfrequentie**:

      - Dagelijks
      - Wekelijks
      - Tweewekelijks
      - Halfmaandelijks
      - Maandelijks
      - Driemaandelijks
      - Halfjaarlijks
      - Jaarlijks
      - Geen

   2. Selecteer een optie in de vervolgkeuzelijst **Basis toerekenperiode** om de begindatum te bepalen die wordt gebruikt voor het berekenen van toerekenperioden:

      | Basis toerekenperiode | Beschrijving |
      | --- | --- |
      | **Begindatum plan** | De begindatum van de toerekenperiode is de datum waarop het plan beschikbaar is. |
      | **Werknemerspecifieke datum** | De begindatum van de toerekenperiode is afhankelijk van een werknemersgebeurtenis:</br><ul><li>Aangepast (u moet voor elke afzonderlijke inschrijving een toerekendatum opgeven)</li><li>Jubileumdatum</li><li>Oorspronkelijke datum indiensttreding</li><li>Anciënniteitsdatum</li><li>Aangepaste begindatum van medewerker</li><li>Begindatum van medewerker</li></ul> |

   3. Selecteer een optie in de vervolgkeuzelijst **Toewijzingsdatum toerekening**:

      - **Einddatum toerekeningsperiode**: aan de werknemer wordt verlof toegekend op de laatste dag van de toekenningsperiode. Als u het juiste bedrag wilt toerekenen, moet het toerekeningsproces de gehele periode omvatten. Als de toerekenperiode bijvoorbeeld 1 januari 2020 tot en met 31 januari 2020 is, moet u de toerekening voor 1 februari 2020 uitvoeren om januari mee te nemen.

      - **Begindatum toerekeningsperiode**: aan de werknemer wordt verlof toegekend op de eerste dag van de toekenningsperiode.

   4. Selecteer een optie in de vervolgkeuzelijst **Toerekeningsbeleid bij inschrijving**. Met deze waarde wordt gedefinieerd hoe de toerekening wordt berekend wanneer een werknemer zich in het midden van een toerekenperiode inschrijft.

      - **Evenredig**: het datumbereik tussen de inschrijvingsdatum en de begindatum wordt gebruikt om het verschil in dagen te bepalen. Dat verschil wordt toegepast wanneer toerekeningen worden verwerkt.

      - **Volledige toerekening**: het volledige toerekeningsbedrag, gebaseerd op het niveau, wordt toegekend tijdens de eerste toerekeningsverwerking.

      - **Geen toerekening**: geen toerekening tot de volgende toerekeningsperiode.

   5. Selecteer een optie in de vervolgkeuzelijst **Toerekeningsbeleid bij uitschrijving**. Met deze waarde wordt gedefinieerd hoe de toerekening wordt berekend wanneer een werknemer zich in het midden van een toerekenperiode uitschrijft.

      - **Evenredig**: het datumbereik tussen de inschrijvingsdatum en de begindatum wordt gebruikt om het verschil in dagen te bepalen. Dat verschil wordt toegepast wanneer toerekeningen worden verwerkt.

      - **Volledige toerekening**: het volledige toerekeningsbedrag, gebaseerd op het niveau, wordt toegekend tijdens de eerste toerekeningsverwerking.

      - **Geen toerekening**: geen toerekening tot de volgende toerekeningsperiode.

4. Definieer het toerekeningsschema op het tabblad **Toerekeningsschema**. Het toerekeningsschema bepaalt:

   - Hoe een werknemer verlof opbouwt
   - Hoeveel tijd de werknemer opbouwt
   - Hoeveel tijd wordt getransporteerd

   U kunt niveaus maken om verlof toe te kennen op basis van verschillende niveaus.

   Als u werknemers hebt die per uur worden betaald, kunt u verlof toekennen op basis van gewerkte uren in plaats van de diensttijd bij uw organisatie. De gewerkte uren worden doorgaans opgeslagen in een tijd- en aanwezigheidssysteem. U kunt normale en overuren importeren die zijn gewerkt vanuit het tijd- en aanwezigheidssysteem en deze gebruiken als basis voor de toekenning aan een werknemer.

   1. Selecteer een optie in de vervolgkeuzelijst **Toerekeningstype**:

      - **Servicemaanden** : baseer het toerekeningsschema op de servicemaanden.

      - **Gewerkte uren**: baseer het toerekeningsschema op gewerkte uren. Zie [Verlof toerekenen op basis van gewerkte uren](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked) voor meer informatie over toerekeningen voor gewerkte uren.

      Zie [Verlof toerekenen op basis van gewerkte uren](hr-leave-and-absence-plans.md?enrollments-and-balances) voor meer informatie over toerekeningssaldi.

    2. Geef waarden op in de tabel voor het toerekeningsschema:

      - **Servicemaanden**: het minimum aantal maanden dat werknemers moeten werken om recht op toerekeningen te hebben. Als u geen minimum nodig hebt, stelt u de waarde in op 0.

      - **Gewerkte uren**: het minimum aantal uren dat werknemers per toerekeningsperiode moeten werken om recht op toerekeningen te hebben. Als u geen minimum nodig hebt, stelt u de waarde in op 0.

      - **Toerekeningsbedrag**: het aantal uren of dagen dat werknemers per periode opbouwen. De periode is gebaseerd op de toerekeningsfrequentie.

      - **Minimumsaldo**: u kunt een negatieve waarde gebruiken voor het minimumsaldo als werknemers meer verlof kunnen aanvragen dan er beschikbaar is.

      - **Maximaal transport**: het toerekeningsproces past verlofsaldi aan die het maximale transportsaldo op de verjaardag van de begindatum overschrijden.

      - **Toewijzingshoeveelheid**: het oorspronkelijke aantal uren of dagen dat werknemers krijgen wanneer ze zich inschrijven voor het verlofplan. Deze hoeveelheid wordt niet voor elke toerekeningperiode verzameld.

5. Selecteer **Opslaan**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Verlof toerekenen op basis van gewerkte uren

Als u werknemers hebt die per uur worden betaald, kunt u verlof toekennen op basis van gewerkte uren in plaats van de diensttijd bij uw organisatie. De gegevens over gewerkte uren worden doorgaans opgeslagen in een tijd- en aanwezigheidssysteem. U kunt normale en overuren importeren die zijn gewerkt vanuit uw tijd- en aanwezigheidssysteem en deze gebruiken als basis voor de toekenning aan een werknemer.

Wanneer u de optie voor gewerkte uren selecteert als toerekeningstype, kunt u twee typen uren gebruiken voor de toerekening: normale uren en overuren. Voor de toerekeningsverwerking voor plannen voor gewerkte uren worden de toerekeningsfrequentie en de basis van de toerekeningsperiode gebruikt om de toe te rekenen uren te bepalen.

### <a name="annual-accrual-frequency"></a>Jaarlijkse toerekeningsfrequentie

| Toekenningsdatum toerekening    | Niveau gewerkte uren    | Toerekeningsbedrag        | Datums gewerkte uren   | Werkelijk gewerkte uren| Toekenning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1-1-2018-31-12-2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1-1-2018-31-12-2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Maandelijkse toerekeningsfrequentie

| Toekenningsdatum toerekening    | Niveau gewerkte uren    | Toerekeningsbedrag        | Datums gewerkte uren   | Werkelijk gewerkte uren| Toekenning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8-1-2018-31-8-2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8-1-2018-31-8-2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Halfmaandelijkse toerekeningsfrequentie

| Toekenningsdatum toerekening    | Niveau gewerkte uren    | Toerekeningsbedrag        | Datums gewerkte uren   | Werkelijk gewerkte uren| Toekenning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 8-16-2018-31-8-2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 8-16-2018-31-8-2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Wekelijkse toerekeningsfrequentie

| Toekenningsdatum toerekening    | Niveau gewerkte uren    | Toerekeningsbedrag        | Datums gewerkte uren   | Werkelijk gewerkte uren| Toekenning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8-27-2018-31-8-2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8-27-2018-31-8-2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Aan medewerker toegewezen verlofplannen

In de toegewezen verlofplannen van een werknemer worden de niveaubasis en het type uren weergegeven voor plannen op basis van gewerkte uren. De werkelijk gewerkte uren voor de toerekeningsperioden op de huidige datum worden ook weergegeven voor actieve plannen.

### <a name="loading-data"></a>Gegevens laden

U kunt werkelijke uren importeren met behulp van de entiteit **Gewerkte verlof- en verzuimuren** in Gegevensbeheer. Als u werktijdenkalenders gebruikt, wordt tijdens het importeren gevalideerd of het aantal normale gewerkte uren voor een dag niet hoger is dan het aantal geplande uren voor die dag. Met de import wordt ook gevalideerd of het aantal gewerkte uren voor een bepaalde dag niet meer dan 24 bedraagt. 

U hebt de volgende informatie nodig voor het importeren van de werkelijke uren die moeten worden gebruikt in het proces voor toerekening van verlof:

- Personeelsnummer 
- Datum gewerkt
- Type
- Uren

Aan één datum kan slechts één van elk type worden gekoppeld.

| Personeelsnummer       | Datum gewerkt           | Type                  | Uren                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Normaal               | 8                    |       
| 000337                | 8/7/2018             | Normaal               | 8                    |
| 000337                | 8/7/2018             | Overuren              | 3                    |
| 000337                | 8/8/2018             | Normaal               | 8                    |
| 000337                | 8/7/2018             | Normaal               | 8                    |
| 000337                | 8/9/2018             | Normaal               | 8                    |

## <a name="enrollments-and-balances"></a>Inschrijvingen en saldi

### <a name="enrollment-date"></a>Inschrijvingsdatum

De inschrijvingsdatum bepaalt wanneer een werknemer kan beginnen met het verzamelen van verlof. Als een werknemer bijvoorbeeld op 15 juni 2018 wordt ingeschreven voor een vakantieplan, kan hij of zij geen verlof opbouwen vóór 15 juni 2018.

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

Toerekeningen worden verwerkt op 1 mei 2018 (5-1-2018), zodat die gehele periode is opgenomen.

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

Toerekeningen worden verwerkt op 1 mei 2018 (5-1-2018), zodat die gehele periode is opgenomen.

**Resultaten**

| Toerekeningsbedrag | Minimumsaldo | Maximaal transport | Aanvraagbedrag | Huidig saldo (op 1-1-2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Huidig saldo (7) = Toerekeningsbedrag (5 × 3) – Aanvraagbedrag (8)

### <a name="forecasted-balance"></a>Saldoprognose

Het *voorspelde saldo* is de hoeveelheid verlof die beschikbaar is op een toekomstige datum. Toerekeningen en getransporteerde correcties worden geraamd tot die datum.

Human Resources maakt gebruik van de volgende formule:

Voorspeld saldo voor maandag = Huidig saldo – Aanvragen + Toerekeningen – Getransporteerde correctie

### <a name="forecasted-balance-examples"></a>Voorbeelden van voorspeld saldo

#### <a name="annual-plan"></a>Jaarlijks plan

**Planinstellingen**

| Begindatum plan | Inschrijvingsdatum | Toerekenfrequentie | Basis toerekenperiode | Toewijzingsdatum toerekening    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Jaarlijks            | Begindatum plan      | Einde van toerekeningsperiode |

Toerekeningen worden verwerkt op 15 februari 2019 (2-15-2019), zodat die gehele periode is opgenomen.

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

Toerekeningen worden verwerkt op 15 februari 2019 (2-15-2019), zodat die gehele periode is opgenomen.

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

Toerekeningen worden verwerkt op 15 februari 2019 (2-15-2019), zodat die gehele periode is opgenomen.

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
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3.00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1.00           | 9/1/2018        | 2.00    |

## <a name="configure-preview-features"></a>Voorbeeldfuncties configureren

Als u de voorbeeldfuncties voor verlof en verzuim hebt ingeschakeld, moet u ook de instellingen hiervoor configureren.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. **Preview-functie: Meerdere verloftypen configureren voor één verlof- en verzuimplan**. Voor elke record in de tabel voor het toerekeningsschema kunt u een verloftype definiëren.

   > [!IMPORTANT]
   > Nadat u deze functie hebt ingeschakeld, kunt u deze niet meer uitschakelen.

2. **Preview-functie: Fulltime-equivalentie gebruiken**. Als u deze preview-functie inschakelt, gebruikt Hurman Resource de fulltime-equivalentie (FTE) die is gedefinieerd voor de positie om de toerekening van een werknemer naar rato uit te voeren. Als het FTE bijvoorbeeld 0,5 is en het toerekeningsbedrag 10, bouwt de werknemer 5 op. U kunt deze functie alleen gebruiken als u meerdere verloftypen inschakelt.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md)
- [Verlof- en verzuimplannen toerekenen](hr-leave-and-absence-accrue.md)