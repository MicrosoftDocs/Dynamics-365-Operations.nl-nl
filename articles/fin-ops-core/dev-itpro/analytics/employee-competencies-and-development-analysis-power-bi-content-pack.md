---
title: Power BI-inhoud Competenties en ontwikkeling van werknemer
description: In dit artikel wordt de Power BI-inhoud voor Competenties en ontwikkeling van werknemer besproken.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.openlocfilehash: 1ddc117c83e551374bc8da6872429e3bb9eeee58
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280953"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI-inhoud Competenties en ontwikkeling van werknemer

[!include [banner](../includes/banner.md)]

In dit artikel wordt de Power BI-inhoud voor Competenties en ontwikkeling van werknemer besproken. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporten die zijn opgenomen in het inhoudpakket
Nadat u het inhoudpakket aan uw gegevens hebt gekoppeld, geven de rapporten de gegevens van uw organisatie weer. Als u Microsoft Power BI nog niet eerder hebt gebruikt, raadpleegt u de pagina [Guided Learning for Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). De rapporten die zijn opgenomen in het inhoudpakket, bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                            | Inhoud                                               |
|-----------------------------------|--------------------------------------------------------|
| Analyse competentie en ontwikkeling | Vaardigheidstypen teamleden en vaardigheden per type van teamleden |
| Vaardigheidsprofiel                     | Vaardigheidsprofiel voor de geselecteerde werknemer                |
| Vaardigheidsanalyse                    | Vaardigheden per type en classificatie                              |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Toepassingsgegevens worden gebruikt om de rapporten te vullen in het inhoudpakket Competenties en ontwikkeling van werknemer. De volgende tabel bevat de entiteiten waarop het inhoudpakket is gebaseerd.

| Entiteit                            | Inhoud                                                                                                   | Relaties met andere entiteiten |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalenderverschuivingen om rapporten in te delen                                                                          | |
| Workforce\_Company                | Bedrijven waarop rapporten moeten worden gefilterd                                                                             | |
| Workforce\_Compensation           | Loontarief en betalingsfrequentie in de loop van de tijd                                                                           | |
| Workforce\_CurrentCompensation    | Loontarief en betalingsfrequentie vanaf de huidige datum                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Posities vanaf de huidige datum, voltijdse equivalenten (VTE), openstaande posities en openstaande-tot-ingevulde posities | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Werknemers vanaf de huidige datum, leeftijd en personeelsbezetting                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Workforce\_Date                   | Dagen, weken, maanden en jaren                                                                             | |
| Workforce\_Demographics           | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat                                                   | |
| Workforce\_Employment             | Begindatum, einddatum en overgangsdatum                                                                  | |
| Workforce\_GeographicLocation     | Plaats, provincie, postcode en staat of provincie                                                           | |
| Workforce\_Job                    | Functie, type en titel                                                                                  | |
| Workforce\_JobPreferredSkill      | Belang, beoordeling, vaardigheid en vaardigheidsniveau                                                                 | Workforce\_Skill, Workforce\_Job |
| Workforce\_PastPositionAssignment | Reden van toewijzing, begindatum, einddatum en taak                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Classificatie, beschrijving en classificatiemodel                                                                      | |
| Workforce\_PersonSkill            | Niveau, niveaudatum en vaardigheid                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | Gecertificeerd, niveau, niveaudatum en vaardigheid                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | Afdeling, VTE, positie, positietype en titel                                                        | |
| Workforce\_PositionTrend          | Posities in de loop van de tijd, VTE en taak                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Voornaam, achternaam en volledige naam                                                                       | |
| Workforce\_Skill                  | Vaardigheid, vaardigheidstype en classificatie                                                                              | |
| Workforce\_TerminatedWorker       | Ontslagen werknemers, beëindigingsdatum dienstverband, titel, positie en taak                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Workforce\_WorkerName             | Voornaam, achternaam en volledige naam                                                                       | |
| Workforce\_WorkerTitle            | Titel en anciënniteitsdatum                                                                                   | |
| Workorce\_WorkerTrend             | Werknemers in de loop van de tijd, personeelsbezetting, bedrijf en positie                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
