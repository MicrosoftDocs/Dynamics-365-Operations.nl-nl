---
title: Afschrijvingsmethoden en conventies
description: Dit artikel geeft een overzicht van de afschrijvingsconventies en afschrijvingsmethoden die door Microsoft Dynamics 365 Finance worden ondersteund.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3370db28f551b5ce4a9b49342cb0c0b2f3945c0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769495"
---
# <a name="depreciation-methods-and-conventions"></a>Afschrijvingsmethoden en conventies

[!include [banner](../includes/banner.md)]

Dit artikel geeft een overzicht van de ondersteunde afschrijvingsconventies en afschrijvingsmethoden.

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





<a name="additional-resources"></a>Aanvullende resources
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



