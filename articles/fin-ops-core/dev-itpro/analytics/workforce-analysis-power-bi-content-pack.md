---
title: Power BI-inhoud Metrische gegevens personeel
description: In dit artikel wordt de Power BI-inhoud Metrische gegevens personeel beschreven.
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
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.form: HcmWorkforceWorkspace
ms.openlocfilehash: 9d5c156eda3559394cb2723f0492b0ab575d815d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289811"
---
# <a name="workforce-metrics-power-bi-content"></a>Power BI-inhoud Metrische gegevens personeel

[!include [banner](../includes/banner.md)]

In dit artikel wordt de Microsoft Power BI-inhoud **Metrische gegevens personeel** beschreven. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud
De Power BI-inhoud **Metrische gegevens personeel** wordt weergegeven in het werkgebied **Personeelsbeheer** als u een van deze producten gebruikt:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
De volgende tabel bevat de metrische gegevens die in elk rapport worden weergegeven.

| Rapport                                           | Metrische gegevens |
|--------------------------------------------------|---------|
| Metrische gegevens personeel                                   | Overzicht van andere rapporten |
| Personeelsbezettingsanalyse per bedrijf, afdeling, locatie | Personeelsbezetting per bedrijf, personeelsbezetting per afdeling, personeelsbezetting per locatie en totale personeelsbezetting |
| Personeelsbezettingsanalyse per functie, schaal, manager            | Personeelsbezetting per functie, personeelsbezetting per schaal, personeelsbezetting per manager en totale personeelsbezetting |
| Trendanalyse personeelsbezetting                         | Personeelsbezetting van dit jaar versus vorig jaar per bedrijf en huidige personeelsbezetting voor de afgelopen 12 maanden |
| FTE-analyse                                     | Totale FTE (Fulltime Equivalent), totale toegewezen FTE, FTE per afdeling, FTE voor de afgelopen 12 maanden en FTE per functie |
| Demografische gegevens personeel                           | Personeelsbezetting op leeftijd en geslacht, personeelsbezetting op etnische afkomst, personeelsbezetting op veteraanstatus, personeelsbezetting op burgerlijke staat, het aantal fulltime studenten, gemiddelde diensttijd, gemiddelde leeftijd, verhouding van vrouwelijke en mannelijke werknemers en talen die door werknemers worden gesproken |
| Positieanalyse                                | Openstaande posities per afdeling, openstaande-tot-ingevulde posities, actieve-tot-inactieve posities en posities per afdeling |
| Verloopanalyse                               | Verloop van dit jaar versus vorig jaar, verloop, werknemers die weggaan op basis van leeftijd en geslacht, gemiddelde diensttijd van mensen die weggaan, werknemers die deze maand weggaan en werknemers die weggaan op basis van reden |
| Mensen per afdeling                             | Werknemers met een personeelsnummer per afdeling, positie en begin- en einddatum van toewijzing |
| Analyse dienstjaren                               | Gemiddeld diensttijd, gemiddeld aantal dienstjaren per bedrijf en anciënniteitslijst |
| Jubilea van werknemers                           | Jubilea in deze maand, jubilea in de volgende maand, werknemers op basis van aantal dienstjaren, en jubilea en aantal dienstjaren per afdeling |
| Verjaardagen van werknemers                               | Verjaardagen in deze maand, verjaardagen in de volgende maand, verjaardagen van werknemers en verjaardagen per maand en afdeling |
| Projecten voor massaal aanstellen                               | Totaal aantal projecten voor massaal aanstellen, projecten voor massaal aanstellen op basis van status, projecten voor massaal aanstellen per afdeling en eigenaar, projecten voor massaal aanstellen per functie en projecten voor massaal aanstellen |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Let erop dat u de Power BI-inhoud **Metrische gegevens personeel** downloadt die van toepassing is voor de versie van Microsoft Dynamics 365 die u gebruikt.

> [!NOTE]
> De .pbix-bestanden die beschikbaar zijn in Lifecycle Services, zijn alleen van toepassing op apps voor financiën en bedrijfsactiviteiten.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
De volgende tabel bevat de entiteiten waarop de inhoud is gebaseerd.

| Entiteit                   | Inhoud                                                                            | Relaties met andere entiteiten |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Kalender-offset          | Kalenderverschuivingen om rapporten in te delen                                                   | Toewijzing eerdere positie, Trend positie, Trend werknemer, Ontslagen werknemer |
| Bedrijf                  | Bedrijven waarop rapporten moeten worden gefilterd                                                      | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Huidige positie         | Posities vanaf de huidige datum, FTE, openstaande posities en openstaande-tot-ingevulde posities | Functie, Positie |
| Huidige werknemer         | Werknemers vanaf de huidige datum, leeftijd en personeelsbezetting                                  | Bedrijf, Geografische locatie, Werknemersnaam, Rapporteert aan, Werknemertitel, Demografische gegevens, Functie, Aanstelling, Positie |
| Datum                     | Dagen, weken, maanden en jaren                                                      | Toewijzing eerdere positie, Trend positie, Ontslagen werknemer, Trend werknemer |
| Demografische gegevens             | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat                            | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Aanstelling               | Begindatum, einddatum en overgangsdatum                                           | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Geografische locatie      | Plaats, provincie, postcode en staat of provincie                                    | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Functie                      | Functie, type en titel                                                           | Huidige positie, Huidige werknemer |
| Toewijzing eerdere positie | Reden van toewijzing, begindatum, einddatum en taak                                    | Kalender-offset, Datum, Functie, Positie |
| Positie                 | Afdeling, VTE, positie, positietype en titel                                 | Huidige positie, Huidige werknemer |
| Trend positie           | Posities in de loop van de tijd, VTE en taak                                                   | Kalender-offset, Datum, Functie, Positie |
| Rapporteert aan               | Voornaam, achternaam en volledige naam                                                | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Ontslagen werknemer      | Ontslagen werknemers, beëindigingsdatum dienstverband, titel, positie en taak                      | Bedrijf, Geografische locatie, Werknemersnaam, Rapporteert aan, Kalender-offset, Datum, Werknemertitel, Demografische gegevens, Aanstelling, Functie, Positie |
| Naam van werknemer            | Voornaam, achternaam en volledige naam                                                | Huidige medewerker, Ontslagen werknemer, Trend werknemer |
| Werknemertitel           | Titel en anciënniteitsdatum                                                            | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Trend werknemer           | Werknemers in de loop van de tijd, personeelsbezetting, bedrijf en positie                                 | Bedrijf, Geografische locatie, Werknemersnaam, Rapporteert aan, Kalender-offset, Datum, Werknemertitel, Demografische gegevens, Aanstelling, Functie |
| Project voor massaal aanstellen        | Aantal projecten voor massaal aanstellen, projecteigenaar en projectstatus                     | Bedrijf, Regel voor massaal aanstellen. |
| Regel voor massaal aanstellen           | Afdeling, type dienstverband en positie                                           | Datum, Functie, Project voor massaal aanstellen |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
