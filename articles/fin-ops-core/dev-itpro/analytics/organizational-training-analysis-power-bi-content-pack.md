---
title: Power BI-inhoud Organisatietraining
description: In dit artikel wordt Power BI-inhoud voor organisatietraining in Finance and Operations beschreven.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ba332fc0c241969cbe0c25e7985101a2bbe12be4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892416"
---
# <a name="organizational-training-power-bi-content"></a>Power BI-inhoud Organisatietraining

[!include [banner](../includes/banner.md)]

In dit artikel wordt Power BI-inhoud voor organisatietraining in Finance and Operations beschreven.

## <a name="reports-that-are-included-in-the-content-pack"></a>Rapporten die zijn opgenomen in het inhoudpakket
Nadat u het inhoudpakket aan uw gegevens hebt gekoppeld, geven de rapporten de gegevens van uw organisatie weer. Als u Microsoft Power BI nog niet eerder hebt gebruikt, raadpleegt u de pagina [Guided Learning for Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). De rapporten die zijn opgenomen in het inhoudpakket, bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport          | Inhoud                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Analyse van de cursus | Registratie op locatie, cursusdeelnemers op status en registratielijst |
| Cursustypen    | Cursustypen per vaardigheid                                                       |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
Toepassingsgegevens worden gebruikt voor het vullen van de rapporten in het inhoudpakket Organisatietraining. De volgende tabel bevat de entiteiten waarop het inhoudpakket is gebaseerd.

| Entiteit                    | Inhoud                                                         | Relaties met andere entiteiten |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Training\_CalendarOffset  | Kalenderverschuivingen om rapporten in te delen                                | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Company         | Bedrijven waarop rapporten moeten worden gefilterd                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Course          | Cursus, omschrijving, naam docent, locatie, lokaal en status | Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill |
| Training\_CourseAgenda    | Agenda, cursus en begin- en eindtijden                          | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Course |
| Training\_CourseAttendees | Naam, status, functie en datum van aanmelding                         | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position |
| Training\_CourseSkill     | Vaardigheden, vaardigheidstype en niveau                                     | Training\_Course |
| Training\_Date            | Dagen, weken, maanden en jaren                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Demographics    | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat         | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Employment      | Begindatum, einddatum en overgangsdatum                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Job             | Functie, type en titel                                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Position        | Positie, titel en voltijds equivalent (VTE)                  | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_WorkerName      | Voornaam, achternaam en volledige naam                             | Training\_CourseAttendees |
| Training\_WorkerTitle     | Titel en anciënniteitsdatum                                         | Training\_CourseAttendees |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]