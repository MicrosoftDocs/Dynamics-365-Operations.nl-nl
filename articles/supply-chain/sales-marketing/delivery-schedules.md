---
title: Afleveringsschema's
description: Afleveringsschema's maken het bijhouden van de orderregelhoeveelheid mogelijk wanneer u meerdere leveringen voor één verkooporder, verkoopofferte of inkooporder gebruikt.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193777"
---
# <a name="delivery-schedules"></a>Afleveringsschema's

[!include [banner](../includes/banner.md)]

Afleveringsschema's maken het bijhouden van de orderregelhoeveelheid mogelijk wanneer u meerdere leveringen voor één verkooporder, verkoopofferte of inkooporder gebruikt.

Gebruik een afleveringsschema als de totale hoeveelheid op een order- of offerteregel in meerdere zendingen moet worden geleverd. Afzonderlijke zendingen worden vertegenwoordigd door leveringsregels. Twee of meer leveringsregels vormen samen één afleveringsschema. De leveringsregels kunnen verschillende leveringsdatums, hoeveelheden, leveringsmethoden en opslagdimensies, zoals locatie en magazijn, bevatten.  

**Voorbeeld van een afleveringsschema**

| Artikel                              | Waarde                                    |
|-----------------------------------|------------------------------------------|
| Totale order (oorspronkelijke orderregel) | 600 stoelen                               |
| Gevraagde afleveringsschema       | 100 stoelen per maand                     |
| Gevraagd tijdsbestek voor levering | 6 maanden, op de eerste dag van elke maand |

In dit scenario vraagt de klant een levering van 600 stoelen in batches van 100 stoelen over zes maanden. Om de leveringsvereisten bij te houden maakt u een afleveringsschema. In de pagina voor het afleveringsschema maakt u zes aparte leveringsregels. Elke leveringsregel bevat 100 stoelen en geeft de leveringsdatum voor die 100 stoelen aan. In dit geval wordt gedurende zes opeenvolgende maanden elke regel naar een tegenrekening geboekt op de eerste van de maand.  

Als u een afleveringsschema maakt, wordt het type van de oorspronkelijke orderregel automatisch gewijzigd in **Orderregel met meerdere leveringen**. Een regel van dit type wordt genoemd commerciële regel en wordt gemarkeerd door een pictogram. De leveringsregel wordt gemarkeerd door een ander pictogram. Als u een hoeveelheid op een leveringsregel wijzigt, wordt de commerciële regel bijgewerkt met de totale hoeveelheid van het afleveringsschema. Als er op een handelsovereenkomst een totale korting voor de order is gedefinieerd, zorgt het afleveringsschema ervoor dat uw order in aanmerking komt voor de totale orderkorting, zelfs wanneer de order is opgesplitst in aparte leveringen.  

Orders die een afleveringsschema hebben worden verwerkt voor de leveringsregels. De verwerking omvat het boeken van productontvangstbonnen, pakbonnen, en de facturering.  

Documentafdrukken van orders en offertes die een afleveringsschema hebben geven alleen de leveringsregels weer. Ze geven niet de oorspronkelijke commerciële regels weer. **Opmerking:** Bovendien worden alleen de leveringsregels weergegeven als u deze acties uitvoert:

-   Plaatsen
-   Pagina's kopiëren
-   In lijstpagina's en rapporten bladeren

Wanneer u verkoopoffertes bevestigt, geven de resulterende verkooporders het hele afleveringsschema weer, zelfs de orderregels meerdere leveringen hebben. Bovendien wordt het hele afleveringsschema weergegeven in alle hoofdpagina´s, zoals verkooporders, verkoopoffertes en inkooporders.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]