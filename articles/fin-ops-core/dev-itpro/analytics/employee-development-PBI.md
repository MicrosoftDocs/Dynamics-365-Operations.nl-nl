---
title: Werknemersontwikkeling Power BI-inhoud
description: In dit onderwerp wordt de Werknemersontwikkeling Power BI-inhoud besproken.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ebebe9c5877f23e635ec0cd1993727014047f310
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005797"
---
# <a name="employee-development-power-bi-content"></a>Werknemersontwikkeling Power BI-inhoud

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de **Werknemersontwikkeling** Microsoft Power BI-inhoud.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud
De rapporten die zijn opgenomen in de **Werknemersontwikkeling** Power BI-inhoud bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                        | Inhoud |
|-------------------------------|----------|
| Overzicht werknemerontwikkeling | Overzicht van andere rapporten |
| Vaardigheidsanalyse werknemer       | Vaardigheidstypen en werknemersvaardigheden op type |
| Vaardigheidsniveau-analyse werknemer | Vaardigheidsniveaus van werknemers per afdeling, werknemers per vaardigheidsniveau en vaardigheidstype en laagste en hoogste niveaus per vaardigheid |
| Vaardigheidsprofiel                 | Vaardigheidsprofiel voor de geselecteerde werknemer |
| Vaardigheidsanalyse                | Vaardigheden per type en classificatie |
| Prestatiebeoordelingsanalyse   | Werknemers op basis van laagste en hoogste beoordeling per functie, werknemersbeoordelingen per afdeling, werknemers per beoordeling en positietype en hoogste en laagste beoordelingen per positie |
| Werknemersprestatieanalyse | Werknemersbeoordelingen voor geselecteerde beoordeling door manager |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

| Entiteit                   | Inhoud                                                                                                   | Relaties met andere entiteiten |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalender-offset          | Kalenderverschuivingen om rapporten in te delen                                                                          | Toewijzing eerdere positie, Trend positie, Trend werknemer, Ontslagen werknemer |
| Bedrijf                  | Bedrijven waarop rapporten moeten worden gefilterd                                                                             | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Huidige positie         | Posities vanaf de huidige datum, voltijdse equivalenten (VTE), openstaande posities en openstaande-tot-ingevulde posities | Functie, Positie |
| Huidige werknemer         | Werknemers vanaf de huidige datum, leeftijd en personeelsbezetting                                                         | Bedrijf, Geografische locatie, Werknemersnaam, Rapporteert aan, Werknemertitel, Demografische gegevens, Functie, Aanstelling, Positie |
| Datum                     | Dagen, weken, maanden en jaren                                                                             | Toewijzing eerdere positie, Trend positie, Ontslagen werknemer, Trend werknemer |
| Demografische gegevens             | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat                                                   | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Aanstelling               | Begindatum, einddatum en overgangsdatum                                                                  | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Geografische locatie      | Plaats, provincie, postcode en staat of provincie                                                           | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Functie                      | Functie, type en titel                                                                                  | Huidige positie, Huidige werknemer |
| Toewijzing eerdere positie | Reden van toewijzing, begindatum, einddatum en taak                                                           | Kalender-offset, Datum, Functie, Positie |
| Positie                 | Afdeling, VTE, positie, positietype en titel                                                        | Huidige positie, Huidige werknemer |
| Trend positie           | Posities in de loop van de tijd, VTE en taak                                                                          | Kalender-offset, Datum, Functie, Positie |
| Rapporteert aan               | Voornaam, achternaam en volledige naam                                                                       | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Ontslagen werknemer      | Ontslagen werknemers, beëindigingsdatum dienstverband, titel, positie en taak                                             | Bedrijf, Geografische locatie, Werknemersnaam, Rapporteert aan, Kalender-offset, Datum, Werknemertitel, Demografische gegevens, Aanstelling, Functie, Positie |
| Naam van werknemer            | Voornaam, achternaam en volledige naam                                                                       | Huidige medewerker, Ontslagen werknemer, Trend werknemer |
| Werknemertitel           | Titel en anciënniteitsdatum                                                                                   | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Trend werknemer           | Werknemers in de loop van de tijd, personeelsbezetting, bedrijf en positie                                                        | Bedrijf, Geografische locatie, Werknemersnaam, Rapporteert aan, Kalender-offset, Datum, Werknemertitel, Demografische gegevens, Aanstelling, Functie |
| Functie                      | Functie, type en titel                                                                                  | Huidige werknemer, Huidige positie, Trend werknemer, Voorkeursvaardigheid functie, Toewijzing eerdere positie, Trend positie, Ontslagen werknemer |
| Voorkeursvaardigheid functie      | Belang, beoordeling, vaardigheid en vaardigheidsniveau                                                                 | Functie |
| Vaardigheidsanalyse werknemer  | Gecertificeerd, niveau, niveaudatum en vaardigheid                                                                    | Werknemernaam, Vaardigheid |
| Prestaties              | Classificatie, beschrijving en classificatiemodel                                                                      | Huidige werknemer, Huidige positie, Trend werknemer, Voorkeursvaardigheid functie, Toewijzing eerdere positie, Trend positie, Ontslagen werknemer |
| Vaardigheid                    | Vaardigheid, vaardigheidstype en classificatie                                                                              | Vaardigheidsanalyse werknemer, Voorkeursvaardigheid functie |
