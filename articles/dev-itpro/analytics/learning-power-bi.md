---
title: Power BI-inhoud Leren
description: In dit onderwerp wordt de Power BI-inhoud Leren besproken.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0ee0cc2e22609d1a87e7d2b6dcd031606191f879
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="learning-power-bi-content"></a>Power BI-inhoud Leren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de Microsoft Power BI-inhoud **Leren** besproken.

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

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over het filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

De volgende gegevens wordt gebruikt voor het vullen van de rapporten in de Power BI-inhoud **Leren**. Deze tabel bevat de entiteiten waarop de inhoud is gebaseerd.

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

