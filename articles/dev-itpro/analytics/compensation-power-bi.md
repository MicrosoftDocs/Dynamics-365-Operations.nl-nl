---
title: Power BI-inhoud Compensatie
description: In dit onderwerp wordt de Power BI-inhoud voor Compensatie besproken. U vindt hier een uitleg hoe u toegang krijgt tot de rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
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
ms.openlocfilehash: daf7232f13b5a2d4262a46f302bfd9e7efd60ead
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="compensation-power-bi-content"></a>Power BI-inhoud Compensatie

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt de Microsoft Power BI-inhoud voor **Compensatie** besproken. U vindt hier een uitleg hoe u toegang krijgt tot de rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud verkrijgen
De Power BI-inhoud **Compensatie** wordt weergegeven in het werkgebied **Compensatiebeheer** als u een van de volgende producten gebruikt:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017)
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud
De rapporten die zijn opgenomen in de Power BI-inhoud **Compensatie** bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                     | Inhoud |
|----------------------------|----------|
| Overzicht compensatie      | Overzicht van andere rapporten |
| Compensatieanalyse      | Werknemers met als instelling Uurtarief of Salaris op basis van bedrijf, totaal aantal werknemers per compensatieplan, mannelijke en vrouwelijke werknemers per compensatieplan en werknemerscompensatie per afdeling |
| Positiesalarisanalyse      | Hoogste en laagste betaling per uur en salaris, posities met het hoogste en laagste salaris en fulltime en parttime posities |
| Compensatieplananalyse | Werknemersinschrijving op basis van geselecteerde vergoeding |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over het filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>De Power BI-inhoud uitbreiden
Als u werkt met versie 1611 van Microsoft Dynamics 365 for Operations of Finance and Operations, Enterprise edition (juli 2017), kunt u de Power BI-inhoud **Compensatie** vinden in de bibliotheek met gedeelde activa in LCS. Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](power-bi-content-microsoft-partners.md). Als u een demo wilt zien over hoe u de Power BI-inhoud implementeert, bekijkt u de Office Mix [Power BI-inhoud van Microsoft en uw partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

Let erop dat u de Power BI-inhoud **Compensatie** downloadt, die geldt voor de versie van Microsoft Dynamics 365 die u gebruikt.

>[!NOTE]
>De .pbix-bestanden die beschikbaar zijn in Lifecycle Services, zijn alleen van toepassing op Finance and Operations.

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
De volgende gegevens worden gebruikt om de rapporten in de Power BI-inhoud **Compensatie** in te vullen. Deze tabel bevat de entiteiten waarop de inhoud is gebaseerd.

| Entiteit                   | Inhoud                                                                                                   | Relaties met andere entiteiten |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalender-offset          | Kalenderverschuivingen om rapporten in te delen                                                                          | Toewijzing eerdere positie, Trend positie, Trend werknemer, Ontslagen werknemer |
| Bedrijf                  | Bedrijven waarop rapporten moeten worden gefilterd                                                                             | Huidige compensatie, Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Compensatie             | Loontarief en betalingsfrequentie in de loop van de tijd                                                                           | Huidige compensatie, Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Huidige compensatie     | Loontarief en betalingsfrequentie vanaf de huidige datum                                                              | Bedrijf, Compensatie, Demografische gegevens, Functie, Positie |
| Huidige positie         | Posities vanaf de huidige datum, voltijdse equivalenten (VTE), openstaande posities en openstaande-tot-ingevulde posities | Functie, Positie |
| Huidige werknemer         | Werknemers vanaf de huidige datum, leeftijd en personeelsbezetting                                                         | Bedrijf, Compensatie, Geografische locatie, Werknemersnaam, Rapporteert aan, Werknemertitel, Demografische gegevens, Functie, Aanstelling, Positie, Vergoedingen |
| Datum                     | Dagen, weken, maanden en jaren                                                                             | Toewijzing eerdere positie, Trend positie, Ontslagen werknemer, Trend werknemer |
| Demografische gegevens             | Geboortedatum, geslacht, etnische afkomst en burgerlijke staat                                                   | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Aanstelling               | Begindatum, einddatum en overgangsdatum                                                                  | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Geografische locatie      | Plaats, provincie, postcode en staat of provincie                                                           | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Functie                      | Functie, type en titel                                                                                  | Huidige positie, Huidige werknemer |
| Toewijzing eerdere positie | Reden van toewijzing, begindatum, einddatum en taak                                                           | Kalender-offset, Datum, Functie, Positie |
| Positie                 | Afdeling, VTE, positie, positietype en titel                                                        | Huidige positie, Huidige werknemer |
| Trend positie           | Posities in de loop van de tijd, VTE en taak                                                                          | Kalender-offset, Datum, Functie, Positie |
| Rapporteert aan               | Voornaam, achternaam en volledige naam                                                                       | Huidige medewerker, Ontslagen werknemer, Trend werknemer |
| Ontslagen werknemer      | Ontslagen werknemers, Ontslagdatum, Titel, Positie en Functie                                             | Bedrijf, Compensatie, Geografische locatie, Werknemersnaam, Rapporteert aan, Kalender-offset, Datum, Werknemertitel, Demografische gegevens, Aanstelling, Functie, Positie, Vergoedingen |
| Vergoedingen                 | Ingangsdatum, vergoedingsoptie, vergoedingsplan en vergoedingstype                                             | Huidige naam, Ontslagen werknemer, Trend werknemer |
| Naam van werknemer            | Voornaam, achternaam en volledige naam                                                                       | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Werknemertitel           | Titel en anciënniteitsdatum                                                                                   | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Trend werknemer           | Werknemers in de loop van de tijd, personeelsbezetting, bedrijf en positie                                                        | Bedrijf, Compensatie, Geografische locatie, Werknemersnaam, Rapporteert aan, Kalender-offset, Datum, Werknemertitel, Demografische gegevens, Aanstelling, Functie, Vergoedingen |

Deze entiteiten zijn gebruikt om berekende eenheden in het gegevensmodel te maken. Deze berekende eenheden worden vervolgens gebruikt om de Key Performance Indicators (KPI's) en rapporten te berekenen, die in de inhoud worden gebruikt. Als u extra berekeningen in uw rapporten en het dashboard wilt opnemen, kunt u het .pbix-bestand downloaden vanuit LCS en dit aanpassen. Dit bestand is het standaardgegevensmodel, dat is gebruikt om de inhoud te maken. Wanneer u klaar bent met aanbrengen van wijzigingen, kunt u een organisatorisch inhoudpakket en dashboard maken met de informatie die u hebt toegevoegd.

