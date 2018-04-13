---
title: Power BI-inhoud Werving
description: In dit onderwerp wordt de Power BI-inhoud Werving besproken. U vindt hier een uitleg hoe u toegang krijgt tot de rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 0d6bc8584d202810ed14367d36d113d9b109ea7a
ms.contentlocale: nl-nl
ms.lasthandoff: 12/19/2017

---

# <a name="recruiting-power-bi-content"></a>Power BI-inhoud Werving

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp wordt de Microsoft Power BI-inhoud **Werving** besproken. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en bevat informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
De Power BI-inhoud **Werving** wordt weergegeven in het werkgebied **Wervingsbeheer**. 

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



