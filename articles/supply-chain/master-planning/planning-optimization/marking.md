---
title: Voorraadmarkering met Planningsoptimalisatie
description: Dit onderwerp biedt informatie over de opties die beschikbaar zijn voor voorraadmarkering in gefiatteerde orders wanneer u Planningsoptimalisatie gebruikt.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99a52c03e519384955d68d7101a7b73b7e9a7af6
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672179"
---
# <a name="inventory-marking-with-planning-optimization"></a>Voorraadmarkering met Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

Dit onderwerp biedt informatie over de opties die beschikbaar zijn voor voorraadmarkering in gefiatteerde orders wanneer u Planningsoptimalisatie gebruikt.

*Markering* wordt gebruikt om vraag en aanbod te koppelen. Het lijkt op *tracering van de behoefte* waarmee wordt aangegeven hoe de hoofdplanning de vraag verwacht te dekken. Vanuit het oogpunt van planning is het belangrijkste verschil dat markering permanenter is dan tracering van de behoefte.

Markering is geïntroduceerd ter ondersteuning van speciale kostprijsberekeningsscenario's voor first in, first out (FIFO) en last in, first out (LIFO). Deze wordt nu echter ook gebruikt voor sommige niet-kostprijsberekeningsscenario's. Markering tussen vraag en aanbod is optioneel en bijna permanent. Markering kan handmatig worden verwijderd door een gebruiker of worden verwijderd door een explosie van verkooporderregels uit te voeren, waarbij de optie **Markering verwijderen** is geselecteerd.

Tracering van de behoefte wordt geregeld door de hoofdplanning tijdens dekking om de vraag te koppelen aan het vereiste aanbod. Tracering van de behoefte kan worden bijgewerkt voor elke planningsuitvoering om het aanbod te optimaliseren dat nodig is om de vraag te dekken. Wanneer hoofdplanning informatie over de tracering van de behoefte bijwerkt, wordt er rekening gehouden met bestaande markering.

Tracering van de behoefte begint met het opnemen van relevante markering, reserveringen voor voorhanden voorraad en reserveringen voor in bestelling in de volgende volgorde:

1. Markering tussen vraag en aanbod
1. Reserveringen voorhanden voorraad
1. Reserveringen voor in bestelling

Wanneer u een geplande order fiatteert, bevat het dialoogvenster **Fiattering** een veld **Markering bijwerken** dat u gebruikt om opties voor markering in te stellen voor de orders die tijdens het fiatteren worden gemaakt. Selecteer een van de volgende waarden:

- **Nee** – Er wordt geen voorraadmarkering toegepast.
- **Standaard** – De voorraadmarkering wordt bijgewerkt volgens de tracering van de behoefte. Een behoefteorder (vraag) wordt aan de hand van een vervullingsorder (aanbod) gemarkeerd. Als een bepaalde hoeveelheid op de vervullingsorder blijft staan, wordt deze niet gemarkeerd en wordt de verwijzingsinformatie leeg gelaten. Als bijvoorbeeld een verkooporder voor 100 EA wordt vastgelegd voor een inkooporder voor 150 EA, wordt verwijzingsinformatie alleen aan de verkooporder toegewezen.
- **Uitgebreid** – Zowel de behoefteorder (vraag) als de vervullingsorder (aanbod) worden gemarkeerd, ongeacht of er hoeveelheid op de vervullingsorder overblijft. Als bijvoorbeeld een verkooporder voor 100 EA wordt vastgelegd voor een inkooporder voor 150 EA, wordt verwijzingsinformatie aan de verkooporder en de inkooporder toegewezen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]