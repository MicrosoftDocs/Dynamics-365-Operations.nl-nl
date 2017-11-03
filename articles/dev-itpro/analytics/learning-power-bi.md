---
title: Power BI-inhoud Leren
description: In dit onderwerp wordt de Power BI-inhoud Leren besproken. U vindt hier een uitleg hoe u toegang krijgt tot de rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0136080b12c6c2bd8e65063e99278f163212178c
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="learning-power-bi-content"></a>Power BI-inhoud Leren

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt de Microsoft Power BI-inhoud **Leren** besproken. U vindt hier uitleg hoe u toegang krijgt tot het inhoudpakket, samen met een beschrijving van het gegevensmodel en de entiteiten waarmee het inhoudpakket is samengesteld.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen

Als u werkt met Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), vindt u de Power BI-inhoud **Leren** in de bibliotheek met gedeelde elementen in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md). Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

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

Deze entiteiten zijn gebruikt om berekende eenheden in het gegevensmodel te maken. Deze berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in de inhoud worden gebruikt. Als u extra berekeningen in uw rapporten en het dashboard wilt opnemen, kunt u het .pbix-bestand downloaden vanuit LCS en dit aanpassen. Dit bestand is het standaardgegevensmodel, dat is gebruikt om de inhoud te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

