---
title: Voorraad markeren
description: Dit artikel biedt informatie over de opties die beschikbaar zijn voor voorraadmarkering in gefiatteerde orders.
author: t-benebo
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: c86db6a670d7d0f7bfe74b7466b9bce766e4a08d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740571"
---
# <a name="inventory-marking"></a>Voorraad markeren

[!include [banner](../../includes/banner.md)]

Dit artikel biedt informatie over de opties die beschikbaar zijn voor voorraadmarkering in gefiatteerde orders.

*Markering* wordt gebruikt om vraag en aanbod te koppelen. Het lijkt op *tracering van de behoefte* waarmee wordt aangegeven hoe de hoofdplanning de vraag verwacht te dekken. Vanuit het oogpunt van planning is het belangrijkste verschil dat markering permanenter is dan tracering van de behoefte.

Markering is geïntroduceerd ter ondersteuning van speciale kostprijsberekeningsscenario's voor first in, first out (FIFO) en last in, first out (LIFO). Deze wordt nu echter ook gebruikt voor sommige niet-kostprijsberekeningsscenario's. Markering tussen vraag en aanbod is optioneel en bijna permanent. Markering kan handmatig worden verwijderd door een gebruiker of worden verwijderd door een explosie van verkooporderregels uit te voeren, waarbij de optie **Markering verwijderen** is geselecteerd.

Tracering van de behoefte wordt geregeld door de hoofdplanning tijdens dekking om de vraag te koppelen aan het vereiste aanbod. Tracering van de behoefte kan worden bijgewerkt voor elke planningsuitvoering om het aanbod te optimaliseren dat nodig is om de vraag te dekken. Wanneer hoofdplanning informatie over de tracering van de behoefte bijwerkt, wordt er rekening gehouden met bestaande markering.

Tracering van de behoefte begint met het opnemen van relevante markering, reserveringen voor voorhanden voorraad en reserveringen voor in bestelling in de volgende volgorde:

1. Markering tussen vraag en aanbod
1. Reserveringen voorhanden voorraad
1. Reserveringen voor in bestelling

Wanneer u een geplande order fiatteert, bevat het dialoogvenster **Fiattering** een veld **Markering bijwerken** dat u gebruikt om opties voor markering in te stellen voor de orders die tijdens het fiatteren worden gemaakt. Selecteer een van de volgende waarden:

- *Nee* – Er wordt geen voorraadmarkering toegepast.
- *Standaard* – De voorraadmarkering wordt bijgewerkt volgens de tracering van de behoefte. Een behoefteorder (vraag) wordt aan de hand van een vervullingsorder (aanbod) gemarkeerd. Als een bepaalde hoeveelheid op de vervullingsorder blijft staan, wordt deze niet gemarkeerd en wordt de verwijzingsinformatie leeg gelaten. Als bijvoorbeeld een verkooporder voor 100 EA wordt vastgelegd voor een inkooporder voor 150 EA, wordt verwijzingsinformatie alleen aan de verkooporder toegewezen.
- *Uitgebreid* – Zowel de behoefteorder (vraag) als de vervullingsorder (aanbod) worden gemarkeerd, ongeacht of er hoeveelheid op de vervullingsorder overblijft. Als bijvoorbeeld een verkooporder voor 100 EA wordt vastgelegd voor een inkooporder voor 150 EA, wordt verwijzingsinformatie aan de verkooporder en de inkooporder toegewezen.
- *Standaard met één niveau*: er wordt markering op één niveau gebruikt. Markering op één niveau markeert alleen het hoofdartikel en niet de stuklijstonderdelen. Zo kunt u na de goedkeuring componenttoewijzing voor productieorders flexibel houden. Markering op één niveau stelt het systeem in staat om te optimaliseren voor vraagwijzigingen op het laatste moment. In de *standaardmarkering op één niveau* worden behoefteorders gemarkeerd tegen hun afhandelingsorders, maar afhandelingsorders worden niet gemarkeerd als er een hoeveelheid resteert.
- *Eén niveau uitgebreid*: er wordt markering op één niveau gebruikt. In de *markering op één niveau uitgebreid* worden behoefteorders gemarkeerd tegen hun afhandelingsorders en worden afhandelingsorders altijd gemarkeerd, of er nu wel of niet een hoeveelheid resteert.

Ga naar **Hoofdplanning \> Instellingen \> Parameters voor hoofdplanning** om de standaardmarkeringsoptie voor het systeem in te stellen. Stel vervolgens op het tabblad **Standaard bijwerken** het markeringsveld **bijwerken in** op uw voorkeursoptie.

> [!NOTE]
> De opties *Standaard één niveau* en *Eén niveau uitgebreid* zijn alleen beschikbaar als de functie *Aanbodautomatisering voor maken naar order* op uw systeem is ingeschakeld. Raadpleeg [Aanbodautomatisering voor maken naar order](../make-to-order-supply-automation.md) voor meer informatie over deze functie en het inschakelen ervan.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
