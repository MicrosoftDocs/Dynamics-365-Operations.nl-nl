--- 
title: Btw-vereffeningsperioden instellen
description: Btw-vereffeningsperioden bevatten info over de periode-intervallen waarvoor btw moet worden aangegeven en betaald.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: ab7d3a00a327f42a9f70c954d9b64a360a7f9163
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

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
14. Vouw het tabblad Periode-intervallen uit.
15. Klik op Toevoegen.
16. Markeer in de lijst de geselecteerde rij.
17. Voer een datum in het veld Begindatum in.
18. Voer een datum in het veld Einddatum in.
19. Klik op Nieuw periode-interval.
    * Als het eerste periode-interval is ingevoerd, kunnen nieuwe perioden automatisch worden gemaakt. U kunt later nieuwe periode-intervallen toevoegen.  
20. Sluit de pagina.


