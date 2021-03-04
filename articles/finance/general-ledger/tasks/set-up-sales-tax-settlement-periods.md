---
title: Btw-vereffeningsperioden instellen
description: In dit onderwerp wordt uitgelegd hoe u vereffeningsperioden voor btw instelt in Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5068c121e921c1586dc6ae003c0021bf41d2254
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441968"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Btw-vereffeningsperioden instellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u vereffeningsperioden voor btw instelt. Btw-vereffeningsperioden bevatten info over de periode-intervallen waarvoor btw moet worden aangegeven en betaald. Een vereffeningsproces kan voor een vereffeningsperiode voor een bepaald datuminterval worden uitgevoerd. Alle btw-codes die aan de vereffeningsperiode zijn gekoppeld worden vereffend. Afhankelijk van de instellingen van de gerelateerde belastingdienst, wordt de belastingschuld geboekt of naar een leverancier of een grootboekrekening.

Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga in het navigatievenster naar **Modules > Belasting > Indirecte belastingen > Btw > Btw-vereffeningsperioden**.
2. Selecteer **Nieuw**.
3. Typ in het veld **Vereffeningsperiode** een waarde.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer in het veld **Belastingdienst** de btw-dienst die de rapporten en betalingen ontvangt die worden gemaakt voor de vereffeningsperiode.
6. Zoek en selecteer de gewenste record in de lijst.
7. Selecteer in het veld **Betalingscondities** de gewenste record in het vervolgkeuzemenu. De gerelateerde btw-dienst kan als leverancier worden ingesteld en de btw-vereffening maakt een open leveranciersfactuur. De betalingstermijnen bepalen de vervaldatum voor de open leveranciersfactuur.  
8. Selecteer een type voor de vereffeningsperiode-intervallen.
9. Voer het aantal periode-intervaleenheden per periode in. Bijvoorbeeld, een kwartaal heeft 3 maanden.
10. Schakel het selectievakje **Batchverwerking gebruiken voor btw-vereffening** in of uit. Het vereffeningsproces voor de vereffeningsperiode kan als batchtaak in de achtergrond worden verwerkt. Dit wordt aanbevolen voor een groot aantal btw-transacties binnen een periode-interval.  
    > [!NOTE]
    > Momenteel wordt dit niet ondersteund in Spanje, Japan en Nederland.
11. Schakel het selectievakje **Genereren van tegengerekende btw-transacties voorkomen** in of uit. Standaard genereert het systeem tegengerekende btw-transacties tijdens het vereffeningsproces, wat kan leiden tot prestatieprobleem als er een groot aantal btw-transacties binnen een periode-interval is. Schakel dit selectievakje in om genereren van tegengerekende btw-transacties te voorkomen.
12. Vouw het tabblad **Periode-intervallen** uit.
13. Selecteer **Toevoegen**.
14. Voer een datum in in het veld **Begindatum** op de nieuwe rij.
15. Voer een datum in het veld **Einddatum** in.
16. Selecteer **Nieuw periode-interval**. Als het eerste periode-interval is ingevoerd, kunnen nieuwe perioden automatisch worden gemaakt. U kunt later nieuwe periode-intervallen toevoegen.  
17. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]