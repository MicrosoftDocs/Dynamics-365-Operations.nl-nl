---
title: Grootboektoewijzingsregels
description: Dit artikel bevat informatie over grootboektoewijzingsregels. Het beschrijft de verschillende onderdelen van deze toewijzingsregels en toewijzingsmethoden die hiervoor kunnen worden gebruikt.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: kfend
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0691c65e6a499f713952070811cefaa7a213af7b
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787548"
---
# <a name="ledger-allocation-rules"></a>Grootboektoewijzingsregels

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over grootboektoewijzingsregels. Het beschrijft de verschillende onderdelen van deze toewijzingsregels en toewijzingsmethoden die hiervoor kunnen worden gebruikt.

Grootboektoewijzingsregels worden gebruikt om toewijzingsjournalen en journaalregels automatisch te berekenen en te genereren voor de toewijzing van grootboeksaldi of vaste bedragen. Toewijzingsmethoden kunnen variabel of vast zijn. De toewijzing wordt gebaseerd op de waarde van de transactievaluta. Boekingen voor winst/verlies van vreemde valuta worden bijvoorbeeld geboekt om de bedragen aan te passen in de valuta voor boekhouding en rapportage. Deze vermeldingen zijn niet onderworpen aan toewijzingsregels omdat de transactievalutawaarde 0,00 is. De volgende toewijzingsmethoden kunnen voor grootboektoewijzingsregels worden gebruikt:

-   **Basis** - Deze variabele methode wordt gebruikt wanneer de toewijzing afhankelijk is van het werkelijke grootboeksaldo, gebaseerd op filtercriteria. Reclameonkosten bijvoorbeeld kunnen worden toegewezen op basis van de verkoop van elke afdeling in verhouding tot de totale afdelingsverkoop.
-   **Vast percentage** en **Vast gewicht** - Voor deze methoden wordt het toewijzingspercentage of -gewicht direct gedefinieerd voor de regel. Reclameonkosten bijvoorbeeld kunnen worden toegewezen zodat Afdeling A 70 procent van de reclameonkosten ontvangt en Afdeling B 30 procent.
-   **Evenredig** - Deze methode verdeelt het bedrag evenredig over elk gedefinieerd doel. Stel dat er doelen zijn gedefinieerd voor Afdeling A en Afdeling B, dan kunnen de reclameonkosten zo worden toegewezen dat zowel Afdeling A als Afdeling B 50 procent van de reclameonkosten ontvangen.

Als Basis als toewijzingsmethode voor een toewijzingsregel wordt gebruikt, moet u ook afzonderlijke basisregels voor grootboektoewijzing definiëren. Gebruikers kunnen met het proces "Toewijzingsaanvraag verwerken" de grootboektoewijzingsregel verwerken en de resulterende toewijzingsjournaalregels bekijken voordat ze de berekende toewijzingen boeken of verwijderen.

## <a name="components-of-ledger-allocation-rules"></a>Onderdelen van grootboektoewijzingsregels
Elke toewijzingsregel bestaat uit vier onderdelen: algemeen, bron, doel en tegenrekening. Een extra onderdeel, de basisregels voor grootboektoewijzing, is vereist als Basis als toewijzingsmethode wordt gebruikt. Al deze onderdelen bevatten essentiële informatie die nodig is om toewijzingen te verwerken.

-   **Algemeen** – In dit onderdeel geeft de gebruiker onder andere opties op voor de toewijzingsmethode, intercompany-regelinstellingen en of de regel actief is.
-   **Bron** - In dit onderdeel geeft de gebruiker de brongegevens voor de toewijzing op. Toewijzing kan zijn gebaseerd op grootboeksaldi (**Gegevensbron** = **Grootboek**) of vaste bedragen (**Gegevensbron** = **Vaste waarde**). Wanneer **Gegevensbron** is ingesteld op **Grootboek**, moeten bronfiltercriteria zijn gedefinieerd voor de grootboektoewijzingsregel (bijvoorbeeld voor de reclameonkosten).
-   **Doel** – Via dit onderdeel bepaalt u hoe het resultaat van de toewijzingsberekening moet worden verdeeld en verantwoord. Er kan bijvoorbeeld één doelregel voor elke afdeling zijn.
-   **Tegenrekenen** - Deze component bepaalt hoe hoofdrekeningen en dimensies moeten worden bepaald voor de tegenrekeningsitems die de doelitems in overeenstemming brengen. Door de gebruiker gedefinieerde opties worden meestal gebruikt in plaats van rekeningen en dimensies die zijn gebaseerd op de bron. Wanneer **Gegevensbron** is ingesteld op **Vaste waarde**, kan **Bron** niet als optie worden gebruikt.
-   **Basisregels voor grootboektoewijzing** - Deze regels gebruiken hun eigen bronfiltercriteria om te bepalen welke grootboeksaldi voor toewijzing (bijvoorbeeld de opbrengsten per afdeling) moeten worden gebruikt. Elke toewijzingsbasisregel kan met meerdere toewijzingsregels worden gebruikt.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
