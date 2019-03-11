---
title: Btw-vereffeningsperioden instellen
description: Btw-vereffeningsperioden bevatten info over de periode-intervallen waarvoor btw moet worden aangegeven en betaald.
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "326188"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Btw-vereffeningsperioden instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Btw-vereffeningsperioden bevatten info over de periode-intervallen waarvoor btw moet worden aangegeven en betaald. Een vereffeningsproces kan voor een vereffeningsperiode voor een bepaald datuminterval worden uitgevoerd. Alle btw-codes die aan de vereffeningsperiode zijn gekoppeld worden vereffend. Afhankelijk van de instellingen van de gerelateerde belastingdienst, wordt de belastingschuld geboekt of naar een leverancier of een grootboekrekening.



Bij deze taak wordt het demobedrijf USMF gebruikt.



1. Ga naar Belasting Tax > Indirecte belastingen > Btw > Btw-vereffeningsperioden.
2. Klik op Nieuw.
3. Typ in het veld Vereffeningsperiode een waarde.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer in het veld Btw-dienst de btw-dienst die de rapporten en betalingen ontvangt die worden gemaakt voor de vereffeningsperiode.
6. Zoek en selecteer het gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld Betalingstermijn op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De gerelateerde btw-dienst kan als leverancier worden ingesteld en de btw-vereffening maakt een open leveranciersfactuur. De betalingstermijnen bepalen de vervaldatum voor de open leveranciersfactuur.  
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Selecteer een type voor de vereffeningsperiode-intervallen.
12. Voer het aantal periode-intervaleenheden per periode in. Bijvoorbeeld, een kwartaal heeft 3 maanden.
13. Schakel het selectievakje Batchverwerking gebruiken voor btw-vereffening in of uit.
    * Het vereffeningsproces voor de vereffeningsperiode kan als batchtaak in de achtergrond worden verwerkt. Dit wordt aanbevolen voor een groot aantal btw-transacties binnen een periode-interval.  
14. Schakel het selectievakje Genereren van tegengerekende btw-transacties voorkomen in of uit.
    * Standaard genereert het systeem tegengerekende btw-transacties tijdens het vereffeningsproces, wat kan leiden tot prestatieprobleem als er een groot aantal btw-transacties binnen een periode-interval is. Schakel dit selectievakje in om genereren van tegengerekende btw-transacties te voorkomen.
15. Vouw het tabblad Periode-intervallen uit.
16. Klik op Toevoegen.
17. Markeer in de lijst de geselecteerde rij.
18. Voer een datum in het veld Begindatum in.
19. Voer een datum in het veld Einddatum in.
20. Klik op Nieuw periode-interval.
    * Als het eerste periode-interval is ingevoerd, kunnen nieuwe perioden automatisch worden gemaakt. U kunt later nieuwe periode-intervallen toevoegen.  
21. Sluit de pagina.

