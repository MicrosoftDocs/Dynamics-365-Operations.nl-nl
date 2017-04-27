---
title: Power BI-inhoud voor rapporten voor werknemercompetenties en -ontwikkeling
description: In dit onderwerp wordt Power BI-inhoud Werknemercompetenties en -ontwikkeling van Dynamics 365 for Operations beschreven. In dit onderwerp wordt uitgelegd hoe u toegang kunt krijgen tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Power BI-inhoud voor rapporten voor werknemercompetenties en -ontwikkeling

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt Power BI-inhoud Werknemercompetenties en -ontwikkeling van Dynamics 365 for Operations beschreven. In dit onderwerp wordt uitgelegd hoe u toegang kunt krijgen tot rapporten in het inhoudpakket en wordt informatie gegeven over het gegevensmodel en de gegevensentiteiten waarmee het inhoudpakket is samengesteld.

<a name="accessing-the-content-pack"></a>Toegang tot het inhoudpakket
--------------------------

U vindt het inhoudpakket Werknemercompetenties en -ontwikkeling in de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u het inhoudpakket downloadt en koppelt aan uw Microsoft Dynamics 365 for Operations-gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporten die zijn opgenomen in het inhoudpakket
Nadat u het inhoudpakket aan uw Dynamics 365 for Operations-gegevens hebt gekoppeld, geven de rapporten de gegevens van uw organisatie weer. Als u Microsoft Power BI nog niet eerder hebt gebruikt, raadpleegt u de pagina [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporten die zijn opgenomen in het inhoudpakket, bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                            | Inhoud                                               |
|-----------------------------------|--------------------------------------------------------|
| Analyse competentie en ontwikkeling | Vaardigheidstypen teamleden en vaardigheden per type van teamleden |
| Vaardigheidsprofiel                     | Vaardigheidsprofiel voor de geselecteerde werknemer                |
| Vaardigheidsanalyse                    | Vaardigheden per type en classificatie                              |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over het filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Gegevens in Dynamics 365 for Operations worden gebruikt om de rapporten te vullen in het inhoudpakket Werknemercompetenties en -ontwikkeling. De volgende tabel bevat de entiteiten waarop het inhoudpakket is gebaseerd.

| Entiteit                            | Inhoud                                                                                                   | Relaties met andere entiteiten                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Kalenderverschuivingen om rapporten in te delen                                                                          |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Company                | Bedrijven waarop rapporten moeten worden gefilterd                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Compensation           | Loontarief en betalingsfrequentie in de loop van de tijd                                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_CurrentCompensation    | Loontarief en betalingsfrequentie vanaf de huidige datum                                                              | Workforce\_Company Workforce\_CurrentCompensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Posities vanaf de huidige datum, voltijdse equivalenten (VTE), openstaande posities en openstaande-tot-ingevulde posities | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                      |
| Workforce\_CurrentWorker          | Werknemers vanaf de huidige datum, leeftijd en personeelsbezetting                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_PersonSkill Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position                     |
| Workforce\_Date                   | Dagen, weken, maanden en jaren                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Demographics           | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat                                                   |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Employment             | Begindatum, einddatum en overgangsdatum                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_GeographicLocation     | Plaats, provincie, postcode en staat of provincie                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Job                    | Functie, type en titel                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_JobPreferredSkill      | Belang, beoordeling, vaardigheid en vaardigheidsniveau                                                                 | Workforce\_Skill Workforce\_Job                                                                                                                                                                                                                                                                         |
| Workforce\_PastPositionAssignment | Reden van toewijzing, begindatum, einddatum en taak                                                           | Workforce\_ClaendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_Performance            | Classificatie, beschrijving en classificatiemodel                                                                      |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PersonSkill            | Niveau, niveaudatum en vaardigheid                                                                               | Workforce\_Skill                                                                                                                                                                                                                                                                                        |
| Workforce\_PersonSkillAnalysis    | Gecertificeerd, niveau, niveaudatum en vaardigheid                                                                    | Workforce\_WorkerName Workforce\_Skill                                                                                                                                                                                                                                                                  |
| Workforce\_Position               | Afdeling, VTE, positie, positietype en titel                                                        |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PositionTrend          | Posities in de loop van de tijd, VTE en taak                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_ReportsToWorkerName    | Voornaam, achternaam en volledige naam                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Skill                  | Vaardigheid, vaardigheidstype en classificatie                                                                              |                                                                                                                                                                                                                                                                                                         |
| Workforce\_TerminatedWorker       | Ontslagen werknemers, beëindigingsdatum dienstverband, titel, positie en taak                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position |
| Workforce\_WorkerName             | Voornaam, achternaam en volledige naam                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_WorkerTitle            | Titel en anciënniteitsdatum                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Werknemers in de loop van de tijd, personeelsbezetting, bedrijf en positie                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job                     |

Deze entiteiten zijn gebruikt om berekende eenheden in het gegevensmodel te maken. Deze berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in het inhoudpakket worden gebruikt. Als u extra berekeningen in uw rapporten en dashboard wilt opnemen, kunt u het bestand CompetenciesandDevelopment.pbix downloaden vanuit LCS en dit aanpassen. Dit bestand is het standaardgegevensmodel, dat is gebruikt om het inhoudpakket te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





