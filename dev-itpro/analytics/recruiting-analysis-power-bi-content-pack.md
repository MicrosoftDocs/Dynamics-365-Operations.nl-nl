---
title: Power BI-inhoud Werving
description: In dit onderwerp wordt de Power BI-inhoud Werving besproken. U vindt hier een uitleg hoe u toegang krijgt tot de rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 49cfd0f1ed645f1980b21b6d4f453cb7a8957a1a
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="recruiting-power-bi-content"></a>Power BI-inhoud Werving

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt de Microsoft Power BI-inhoud **Werving** besproken. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
Als u werkt met de update voor juli 2017 van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, vindt u de Power BI-inhoud **Werving** in het werkgebied **Wervingsbeheer**. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Rapporten en visuals in het werkgebied Wervingsbeheer
Het werkgebied **Wervingsbeheer** bevat een tabblad **Analyses**. Dit tabblad bevat de ingesloten Power BI-inhoud voor werving. De inhoud bestaat uit een overzichtstabblad en extra tabbladen die gegevens bevatten. In de onderstaande tabel vindt u een overzicht van de rapporten op elk tabblad.

| Rapport               | Inhoud |
|----------------------|----------|
| Overzicht van Werving | Samenvatting van andere rapporten |
| Sollicitanten-analyse   | Totaal aantal sollicitatnen, sollicitanten op functie, bronnen van sollicitanten, verhouding vrouwelijke-mannelijke sollicitanten en sollicitanten op locatie |
| Status sollicitant     | Sollicitanten op type en status en status van sollicitant |
| Wervingsanalyse  | Nettopercentage in dienst genomen, gemiddeld aantal dagen tot indienstneming, percentage slechte werknemers en wervingskosten, aantal wervingsprojecten, verhouding aangenomen tot gesolliciteerd en sollicitanten versus vacatures op wervingsproject |

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over het filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

In de volgende tabel vindt u de entiteiten waarop de Power BI-inhoud **Werving** is gebaseerd.

| Entiteit               | Inhoud                                                         | Relaties met andere entiteiten |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Sollicitant            | Sollicitanten, in dienst genomen sollicitanten, netto indienstnemingsverhouding en kosten          | Naam sollicitant, bedrijf, kalender-offset, datum, geografische locatie, demografische gegevens, functie, media, wervingsproject |
| Naam sollicitant       | Voornaam, achternaam en volledige naam van sollicitant                   | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Kalender-offset      | Kalenderverschuivingen om rapporten in te delen                                | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Bedrijf              | Bedrijven waarop rapporten moeten worden gefilterd                                   | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Datum                 | Dagen, weken, maanden en jaren                                   | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Demografische gegevens         | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat         | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Sollicitant in dienst genomen   | Sollicitant, prestaties, begindatum en type sollicitant           | Bedrijf, kalender-offset, datum, geografische locatie, naam sollicitant, dienstverband, prestaties, functie, media, wervingsproject |
| Aanstelling           | Begindatum, einddatum en overgangsdatum                        | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Geografische locatie  | Plaats, provincie, postcode en staat of provincie                 | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Functie                  | Functie, type en titel                                        | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Media                | Bron van sollicitanten                                             | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Prestaties          | Classificatie, beschrijving en classificatiemodel                            | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Wervingsproject  | Projectomschrijving, projectstatus en vacatures                | Sollicitant, sollicitant in dienst genomen, afgewezen sollicitant |
| Afgewezen sollicitant | Afgewezen sollicitanten, reden, prestaties en datum waarop het dienstverband is beëindigd | Bedrijf, kalender-offset, datum, geografische locatie, prestaties, demografische gegevens, dienstverband, media, wervingsproject, naam sollicitant |

Deze entiteiten zijn gebruikt om berekende metingen te maken. Deze berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in de inhoud worden gebruikt. Als u extra berekeningen in uw rapporten en het dashboard wilt opnemen, kunt u het bestand Recruiting.pbix downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS) en dit aanpassen. Dit bestand is het standaardgegevensmodel, dat is gebruikt om de inhoud te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

