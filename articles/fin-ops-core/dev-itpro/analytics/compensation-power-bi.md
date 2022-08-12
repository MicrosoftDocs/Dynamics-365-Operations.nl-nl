---
title: Compensatie Power BI-inhoud
description: In dit artikel wordt Power BI-inhoud voor Compensatie besproken. Er wordt uitgelegd hoe u rapporten kunt openen en u vindt informatie over het gebruikte gegevensmodel.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.search.form: HcmCompensationWorkspace
ms.openlocfilehash: cd51bf429abea5693432643a5ea9441fb9e2e464
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206441"
---
# <a name="compensation-power-bi-content"></a>Compensatie Power BI-inhoud

[!include [banner](../includes/banner.md)]

In dit artikel wordt Microsoft Power BI-inhoud voor **Compensatie** besproken. U vindt hier een uitleg hoe u toegang krijgt tot de rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud
De **Compensatie** Power BI-inhoud wordt weergegeven in het werkgebied **Compensatiebeheer** als u een van de volgende producten gebruikt:

- Apps voor financiën en bedrijfsactiviteiten
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud
De rapporten die zijn opgenomen in **Compensatie** de Power BI-inhoud bevatten diagrammen en tabellen met aanvullende informatie. De onderstaande tabel geeft een overzicht van de rapporten.

| Rapport                     | Inhoud |
|----------------------------|----------|
| Overzicht compensatie      | Overzicht van andere rapporten |
| Compensatieanalyse      | Werknemers met als instelling Uurtarief of Salaris op basis van bedrijf, totaal aantal werknemers per compensatieplan, mannelijke en vrouwelijke werknemers per compensatieplan en werknemerscompensatie per afdeling |
| Positiesalarisanalyse      | Hoogste en laagste betaling per uur en salaris, posities met het hoogste en laagste salaris en fulltime en parttime posities |
| Compensatieplananalyse | Werknemersinschrijving op basis van geselecteerde vergoeding |

U kunt de diagrammen en tegels op deze rapporten filteren en de diagrammen en tegels op het dashboard vastmaken. Zie voor meer informatie over filteren en vastmaken in Power BI [Een dashboard maken en configureren](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen
De volgende gegevens worden gebruikt om de rapporten in de **Compensatie** Power BI-inhoud in te vullen. Deze tabel bevat de entiteiten waarop de inhoud is gebaseerd.

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
| Ontslagen werknemer      | Ontslagen werknemers, Ontslagdatum, Titel, Positie en Functie                                           | Bedrijf, Compensatie, Geografische locatie, Werknemersnaam, Rapporteert aan, Kalender-offset, Datum, Werknemertitel, Demografische gegevens, Aanstelling, Functie, Positie, Vergoedingen |
| Vergoedingen                 | Ingangsdatum, vergoedingsoptie, vergoedingsplan en vergoedingstype                                             | Huidige naam, Ontslagen werknemer, Trend werknemer |
| Naam van werknemer            | Voornaam, achternaam en volledige naam                                                                       | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Werknemertitel           | Titel en anciënniteitsdatum                                                                                   | Huidige werknemer, Ontslagen werknemer, Trend werknemer |
| Trend werknemer           | Werknemers in de loop van de tijd, personeelsbezetting, bedrijf en positie                                                        | Bedrijf, Compensatie, Geografische locatie, Werknemersnaam, Rapporteert aan, Kalender-offset, Datum, Werknemertitel, Demografische gegevens, Aanstelling, Functie, Vergoedingen |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
