---
title: Werkstroom voor onkostenbeheer
description: In dit onderwerp wordt uitgelegd hoe u het workflowsysteem in Microsoft Dynamics 365 Finance kunt gebruiken om een beoordelingsproces voor onkostenrapporten in Onkostenbeheer in te stellen.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153966"
---
# <a name="expense-management-workflow"></a>Werkstroom voor onkostenbeheer

[!include [banner](../includes/banner.md)]

U kunt het werkstroomsysteem gebruiken voor het instellen van een beoordelingsproces voor onkostenrapporten in Onkostenbeheer. U kunt een workflow instellen die de volgende criteria gebruikt om te bepalen wie onkostenrapporten goedkeurt:

- De rapporteringshiërarchie van werknemers en vooraf gedefinieerde goedkeuringslimieten
- Goedkeuring op meerdere niveaus die ondersteuning biedt voor tussentijdse fiatteurs en een definitieve fiatteur
- Financiële dimensies en de projectverantwoordelijkheid
- Toewijzing aan specifieke gebruikers of gebruikersgroepen

Workflowgoedkeuringen kunnen worden gemaakt voor onkostenrapporten, reisopdrachten, vooruitbetalingen in contanten en terugvordering van de belasting toegevoegde waarde (btw).

**Voorbeeld**

Het volgende proces is een voorbeeld van een onkostenbeheerwerkstroom voor een onkostennota.

1. Een werknemer maakt een onkostenrapport en slaat het op.
2. De werknemer dient het onkostenrapport in ter goedkeuring. De fiatteur wordt geïdentificeerd op basis van de regels die zijn gedefinieerd wanneer de werkstroom werd ingesteld.
3. De fiatteur ontvangt een bericht wanneer de onkostennota klaar is om te worden goedgekeurd. De fiatteur bekijkt de onkostennota en controleert of aan de volgende voorwaarden wordt voldaan:

    - De onkosten zijn niet in strijd met onkostenbeleidsregels. Als onkosten in strijd zijn met een beleidsregel, controleert de fiatteur of de onkostennota een geldige zakelijke reden bevat.
    - Er zijn elektronische ontvangstbewijzen gekoppeld aan de onkostennota.

4. De fiatteur keurt de onkostennota goed.
5. De onkostennota wordt aan de coördinator van Leveranciers toegewezen om te worden geboekt.
6. Een van de volgende stappen treedt op, afhankelijk van of automatische boeking is geconfigureerd:

    - Als automatische boeking is geconfigureerd, wordt de onkostennota verwerkt voor betaling en wordt de status van de onkostennota bijgewerkt.
    - Als automatische boeking niet is geconfigureerd, controleert de coördinator van Leveranciers of alle oorspronkelijke ontvangsten zijn ingediend en alle ontvangsten zijn uitgelijnd met de onkosten in de onkostennota. Alle ingevoerde btw-codes op de onkostennota moeten ook worden geverifieerd als correct.

Nadat deze vereisten zijn gecontroleerd, wordt de onkostennota geboekt.

Nadat de onkostennota is geboekt, wordt betaling voor de onkostennota toegestaan en wordt de werknemer vergoed.
