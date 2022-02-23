---
title: Power BI-inhoud - leren
description: In dit onderwerp wordt de Power BI-inhoud - leren beschreven.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 46b7a442470d1fe78ebc5c9d5a0c6e155c0d9918
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685244"
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
