---
title: Power BI-inhoud Werknemerontwikkeling
description: In dit onderwerp wordt de Power BI-inhoud Werknemerontwikkeling besproken. U vindt hier een uitleg hoe u toegang krijgt tot de rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 91f7071cc759686dd90b5893adaf58d1521e9185
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="employee-development-power-bi-content"></a>Power BI-inhoud Werknemerontwikkeling

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt de Microsoft Power BI-inhoud **Werknemerontwikkeling** besproken. U vindt hier een uitleg hoe u toegang krijgt tot de rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen

Als u werkt met Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), vindt u het inhoudpakket **Werknemerontwikkeling** in de bibliotheek met gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u het inhoudpakket downloadt en aan uw gegevens koppelt het onderwerp [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud
De rapporten die zijn opgenomen in de Power BI-inhoud **Werknemerontwikkeling** bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                        | Inhoud |
|-------------------------------|----------|
| Overzicht werknemerontwikkeling | Overzicht van andere rapporten |
| Vaardigheidsanalyse werknemer       | Vaardigheidstypen en werknemersvaardigheden op type |
| Vaardigheidsniveau-analyse werknemer | Vaardigheidsniveaus van werknemers per afdeling, werknemers per vaardigheidsniveau en vaardigheidstype en laagste en hoogste niveaus per vaardigheid |
| Vaardigheidsprofiel                 | Vaardigheidsprofiel voor de geselecteerde werknemer |
| Vaardigheidsanalyse                | Vaardigheden per type en classificatie |
| Prestatiebeoordelingsanalyse   | Werknemers op basis van laagste en hoogste beoordeling per functie, werknemersbeoordelingen per afdeling, werknemers per beoordeling en positietype en hoogste en laagste beoordelingen per positie  |
| Werknemersprestatieanalyse | Werknemersbeoordelingen voor geselecteerde beoordeling door manager |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over het filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
| Entiteit                   | Inhoud                                                                                                   | Relaties met andere entiteiten |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalender-offset          | Kalenderverschuivingen om rapporten in te delen                                                                          | Toewijzing eerdere positie, Trend positie, Trend werknemer, Ontslagen werknemer 
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
| Functie                      | Functie, type en titel                                                                                      | Huidige werknemer, Huidige positie, Trend werknemer, Voorkeursvaardigheid functie, Toewijzing eerdere positie, Trend positie, Ontslagen werknemer |
| Voorkeursvaardigheid functie      | Belang, beoordeling, vaardigheid en vaardigheidsniveau                                                                 | Functie |
| Vaardigheidsanalyse werknemer  | Gecertificeerd, niveau, niveaudatum en vaardigheid                                                                    | Werknemernaam, Vaardigheid |  
| Prestaties              | Classificatie, beschrijving en classificatiemodel                                                                      | Huidige werknemer, Huidige positie, Trend werknemer, Voorkeursvaardigheid functie, Toewijzing eerdere positie, Trend positie, Ontslagen werknemer |
|  Vaardigheid                   | Vaardigheid, vaardigheidstype en classificatie                                                                              | Vaardigheidsanalyse werknemer, Voorkeursvaardigheid functie |                                                                                                                        

Deze entiteiten zijn gebruikt om berekende eenheden in het gegevensmodel te maken. Deze berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in de Power BI-inhoud worden gebruikt. Als u extra berekeningen in uw rapporten en het dashboard wilt opnemen, kunt u het .pbix-bestand downloaden vanuit LCS en dit aanpassen. Dit bestand is het standaardgegevensmodel, dat is gebruikt om de Power BI-inhoud te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

