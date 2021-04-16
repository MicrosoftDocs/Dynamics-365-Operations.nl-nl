---
title: Power BI-inhoud - leren
description: In dit onderwerp wordt de Power BI-inhoud - leren beschreven.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 668308b0a5cfe2fe242a218250c4f714d6f2c279
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744258"
---
# <a name="learning-power-bi-content"></a>Power BI-inhoud - leren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de Microsoft Power BI-inhoud **Leren** beschreven.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud

De rapporten die zijn opgenomen in de Power BI-inhoud **Leren** bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                | Inhoud |
|-----------------------|----------|
| Overzicht van Leren     | Overzicht van andere rapporten |
| Analyse van de cursus       | Registratie op locatie, deelnemer per status, cursussen per type per bedrijf en cursusdeelname op taak |
| Registratie-analyse | Registratielijst |
| Cursustypen          | Cursustypen per vaardigheid |
| Docentanalyse   | Verhouding van cursussen tot docenten, aantal docenten, cursussen op docent, cursussen per docent en cursusagenda op docent |
| Aangeboden cursussen       | Lijst met cursussen |
| Ontwerp cursussen        | Agenda van de cursus |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

De volgende gegevens worden gebruikt om de rapporten in de Power BI-inhoud **Leren** in te vullen. Deze tabel bevat de entiteiten waarop de inhoud is gebaseerd.

| Entiteit           | Inhoud                                                         | Relaties met andere entiteiten |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalender-offset  | Kalenderverschuivingen om rapporten in te delen                                | Cursusagenda, cursusdeelnemers |
| Bedrijf          | Bedrijven waarop rapporten moeten worden gefilterd                                   | Cursusagenda, cursusdeelnemers |
| Cursus           | Cursus, omschrijving, naam docent, locatie, lokaal en status | Cursusagenda, cursusdeelnemers, cursusvaardigheden |
| Cursusagenda    | Agenda, cursus en begin- en eindtijden                          | Bedrijf, kalender-offset, datum, cursus |
| Cursusdeelnemers | Naam, status, functie en datum van aanmelding                         | Bedrijf, kalender-offset, datum, cursus, demografische gegevens, werkgelegenheid, cursus, naam van werknemer, werknemertitel, functie, positie |
| Cursusvaardigheden     | Vaardigheden, vaardigheidstype en niveau                                     | Cursus |
| Datum             | Dagen, weken, maanden en jaren                                   | Cursusagenda, cursusdeelnemers |
| Demografische gegevens     | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat         | Cursusagenda, cursusdeelnemers |
| Aanstelling       | Begindatum, einddatum en overgangsdatum                        | Cursusagenda, cursusdeelnemers |
| Functie              | Functie, type en titel                                        | Cursusagenda, cursusdeelnemers |
| Positie         | Positie, titel en voltijds equivalent (VTE)                  | Cursusagenda, cursusdeelnemers |
| Naam van werknemer    | Voornaam, achternaam en volledige naam                             | Cursusdeelnemers |
| Werknemertitel   | Titel en anciënniteitsdatum                                         | Cursusdeelnemers |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]