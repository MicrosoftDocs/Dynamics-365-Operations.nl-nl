---
title: Afschrijvingsmethoden en conventies
description: Dit artikel bevat een overzicht van de afschrijvingsconventies en afschrijvingsmethoden die door Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition worden ondersteund.
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 8b0361edb0f2dc7484fb9046ce4793fe9397e3d1
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---

# <a name="depreciation-methods-and-conventions"></a>Afschrijvingsmethoden en conventies

[!include[banner](../includes/banner.md)]


Dit artikel bevat een overzicht van de afschrijvingsconventies en afschrijvingsmethoden die door Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition worden ondersteund.

U kunt verscheidene afschrijvingsmethoden en -conventies selecteren. Het doel van de methoden is het toewijzen van de afschrijfbare waarde van het vaste activum in boekperioden. De afschrijfbare waarde van het vaste activum is de verwervingsprijs, verminderd met een eventuele restwaarde. 

Als u afschrijvingsconventies gebruikt en de uitvoeringsdatum van de laatste afschrijving voor een activum wijzigt, waardoor dan enkele afschrijvingen worden overgeslagen, kan de afschrijving voor het afgelopen jaar hoger of lager zijn dan verwacht. De afschrijving wordt aangepast met het aantal afschrijvingsperioden dat werd beïnvloed door de aanpassing van de uitvoeringsdatum van de laatste afschrijving.

Als u bijvoorbeeld de afschrijvingsconventie Half jaar voor drie jaar gebruikt, vindt de afschrijving doorgaans in 3 1/2 jaar plaats. Als u de uitvoeringsdatum van de laatste afschrijving wijzigt tijdens die 3 1/2 jaar, wordt het aantal perioden dat wordt beïnvloed vergroot door het laatste jaar van de afschrijving. Als u de datum drie maanden verschuift, heeft het laatste jaar negen maanden afschrijving, terwijl er normaal gesproken zes maanden afschrijving zou zijn.

U kunt uit de volgende afschrijvingsconventies kiezen.


-   Half jaar
-   Hele maand
-   Midden kwartaal
-   Midden maand (1ste van de maand)
-   Midden maand (15e van de maand)
-   Half jaar (begin van het jaar)
-   Halfjaar (volgend jaar)

U kunt uit de volgende afschrijvingsmethoden kiezen.
-   Levensduur lineaire
-   Degressief
-   Handmatig
-   Factor
-   Verbruik
-   Resterende levensduur lineaire
-   200% degressief
-   175% degressief
-   150% degressief
-   125% degressief

 



<a name="see-also"></a>Zie ook
--------

[Afschrijving vaste activa](fixed-asset-depreciation.md)

[Lineaire afschrijving van levensduur](Straight-line-service-life-depreciation.md)

[Degressieve afschrijving](reduce-balance-depreciation.md)

[Handmatige afschrijving](manual-depreciation.md)

[Factorafschrijving](factor-depreciation.md)

[Afschrijving naar rato van verbruik](consumption-depreciation.md)

[Lineaire afschrijving restlevensduur](straight-line-life-remaining-depreciation.md)

[Degressieve afschrijving van 125 procent](125-percent-reducing-balance-depreciation.md)

[Degressieve afschrijving van 150 procent](150-percent-reducing-balance-depreciation.md)

[Degressieve afschrijving van 175 procent](175-percent-reducing-balance-depreciation.md)

[Degressieve afschrijving van 200 procent](200-percent-reducing-balance-depreciation.md)




