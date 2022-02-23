---
title: Verlof toerekenen op basis van gewerkte uren
description: In dit onderwerp wordt beschreven hoe verlofplannen kunnen worden geconfigureerd om verlof toe te rekenen op basis van gewerkte uren.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 229ae14b9e2dedcd0ade094a772f16c0524d32a7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460831"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Verlof toerekenen op basis van gewerkte uren

## <a name="overview"></a>Overzicht

Organisaties met medewerkers die per uur worden betaald, kunnen verlof toekennen op basis van gewerkte uren in plaats van de diensttijd bij de organisatie. De gewerkte uren worden doorgaans opgeslagen in een tijd- en aanwezigheidssysteem. 

## <a name="leave-plans"></a>Verlofplannen

In het verlofplan kan het type toerekening worden ingesteld op het aantal servicemaanden of de gewerkte uren. Wanneer de optie voor gewerkte uren is geselecteerd, zijn er twee soorten uren die moeten worden gebruikt voor de toerekening: normale uren en overuren.

Ga als volgt te werk om een verlofplan met gewerkte uren in te stellen:

1. Klik op de pagina **Verlof- en verzuimplannen** op **Nieuw plan maken**.
2. Voer een naam in voor het verlofplan.
3. Selecteer de toerekeningsfrequentie voor het plan.
5. Selecteer de begindatum voor het plan.
6. Kies de basis van de toerekeningsperiode en selecteer de werknemerspecifieke datum, indien van toepassing.
7. Selecteer voor het toerekeningsschema de optie **Gewerkte uren** voor het type toerekening.
8. Selecteer het type uren dat moet worden gebruikt voor de toerekening.
9. Voer het aantal gewerkte uren en het bijbehorende toerekeningsbedrag, het minimumsaldo en het maximaal te transporteren of compensatiebedrag in.

Voor de toerekeningsverwerking voor plannen voor gewerkte uren worden de toerekeningsfrequentie en de basis van de toerekeningsperiode gebruikt om de toe te rekenen uren te bepalen.

## <a name="annual-accrual-frequency"></a>Jaarlijkse toerekeningsfrequentie

| Toekenningsdatum toerekening    | Niveau gewerkte uren    | Toerekeningsbedrag        | Datums gewerkte uren   | Werkelijk gewerkte uren| Toekenning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1-1-2018-31-12-2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1-1-2018-31-12-2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Maandelijkse toerekeningsfrequentie

| Toekenningsdatum toerekening    | Niveau gewerkte uren    | Toerekeningsbedrag        | Datums gewerkte uren   | Werkelijk gewerkte uren| Toekenning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 8-1-2018-31-8-2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 8-1-2018-31-8-2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Halfmaandelijkse toerekeningsfrequentie

| Toekenningsdatum toerekening    | Niveau gewerkte uren    | Toerekeningsbedrag        | Datums gewerkte uren   | Werkelijk gewerkte uren| Toekenning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 8-16-2018-31-8-2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 8-16-2018-31-8-2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Wekelijkse toerekeningsfrequentie

| Toekenningsdatum toerekening    | Niveau gewerkte uren    | Toerekeningsbedrag        | Datums gewerkte uren   | Werkelijk gewerkte uren| Toekenning               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 8-27-2018-31-8-2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 8-27-2018-31-8-2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Aan medewerker toegewezen verlofplannen

In de toegewezen verlofplannen van een werknemer worden de niveaubasis en het type uren weergegeven voor plannen waarvoor de gewerkte uren zijn gedefinieerd als het toerekeningstype. Voor actieve plannen worden de werkelijk gewerkte uren voor de toerekeningsperioden op de huidige datum ook weergegeven ter referentie. 

## <a name="loading-data"></a>Gegevens laden

Werkelijke uren kunnen worden geïmporteerd met behulp van de entiteit Gewerkte verlof- en verzuimuren in Gegevensbeheer. Als u werktijdenkalenders gebruikt, wordt tijdens het importeren gevalideerd of het aantal normale gewerkte uren voor een dag niet hoger is dan het aantal geplande uren voor die dag. Met de import wordt ook gevalideerd of de gewerkte uren voor een bepaalde dag niet meer dan 24 uur bedragen. 

De volgende informatie is nodig voor het importeren van werkelijke uren die moeten worden gebruikt in het proces voor toerekening van verlof:

+ Personeelsnummer 
+ Datum gewerkt
+ Type
+ Uren

Aan één datum kan slechts één van elk type worden gekoppeld.

| PERSONNELNUMBER       | DATEWORKED           | TYPE                  | HOURS                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Normaal               | 8                    |       
| 000337                | 8/7/2018             | Normaal               | 8                    |
| 000337                | 8/7/2018             | Overuren              | 3                    |
| 000337                | 8/8/2018             | Normaal               | 8                    |
| 000337                | 8/7/2018             | Normaal               | 8                    |
| 000337                | 8/9/2018             | Normaal               | 8                    |
