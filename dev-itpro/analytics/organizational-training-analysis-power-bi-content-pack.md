---
title: Power BI-inhoud voor organisatietraining
description: In dit onderwerp wordt Power BI-inhoud voor organisatietraining in Finance and Operations beschreven. U vindt hier uitleg hoe u toegang krijgt tot het inhoudpakket, samen met een beschrijving van het gegevensmodel en de entiteiten waarmee het inhoudpakket is samengesteld.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 26499bf5423bc3711d110bd7e548eda238162b7a
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="organizational-training-power-bi-content"></a>Power BI-inhoud voor organisatietraining

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt Power BI-inhoud voor organisatietraining in Finance and Operations beschreven. U vindt hier uitleg hoe u toegang krijgt tot het inhoudpakket, samen met een beschrijving van het gegevensmodel en de entiteiten waarmee het inhoudpakket is samengesteld.

<a name="accessing-the-content-pack"></a>Toegang tot het inhoudpakket
--------------------------

U vindt het inhoudpakket Organisatietraining in de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u het inhoudpakket downloadt en koppelt aan uw Microsoft Dynamics 365 for Finance and Operations-gegevens [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporten die zijn opgenomen in het inhoudpakket
Nadat u het inhoudpakket aan uw Finance and Operations-gegevens hebt gekoppeld, geven de rapporten de gegevens van uw organisatie weer. Als u Microsoft Power BI nog niet eerder hebt gebruikt, raadpleegt u de pagina [Guided Learning for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). De rapporten die zijn opgenomen in het inhoudpakket, bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport          | Inhoud                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Analyse van de cursus | Registratie op locatie, cursusdeelnemers op status en registratielijst |
| Cursustypen    | Cursustypen per vaardigheid                                                       |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over het filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Gegevens in Finance and Operations worden gebruikt voor het vullen van de rapporten in het inhoudpakket Organisatietraining. De volgende tabel bevat de entiteiten waarop het inhoudpakket is gebaseerd.

| Entiteit                    | Inhoud                                                         | Relaties met andere entiteiten                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Kalenderverschuivingen om rapporten in te delen                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | Bedrijven waarop rapporten moeten worden gefilterd                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | Cursus, omschrijving, naam docent, locatie, lokaal en status | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Agenda, cursus en begin- en eindtijden                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | Naam, status, functie en datum van aanmelding                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Vaardigheden, vaardigheidstype en niveau                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | Dagen, weken, maanden en jaren                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | Begindatum, einddatum en overgangsdatum                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | Functie, type en titel                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | Positie, titel en voltijds equivalent (VTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | Voornaam, achternaam en volledige naam                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Titel en anciënniteitsdatum                                         | Training\_CourseAttendees                                                                                                                                                                          |

Deze entiteiten zijn gebruikt om berekende eenheden in het gegevensmodel te maken. Deze berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in het inhoudpakket worden gebruikt. Als u extra berekeningen in uw rapporten en het dashboard wilt opnemen, kunt u het bestand Training.pbix downloaden vanuit LCS en dit aanpassen. Dit bestand is het standaardgegevensmodel, dat is gebruikt om het inhoudpakket te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

## <a name="additional-resources"></a>Aanvullende bronnen
Hieronder staan enkele nuttige koppelingen die zijn gerelateerd aan entiteiten en het samenstellen van Power BI-content:

-   [Gegevensentiteiten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatorische inhoudpakketten maken](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gegevens modelleren met Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI-tegels toevoegen aan werkruimten](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





