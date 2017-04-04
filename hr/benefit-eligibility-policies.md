---
title: Beleid voor geschiktheid vergoedingen
description: Dit artikel biedt informatie over het beleid voor geschiktheid voor vergoedingen, waarmee u kunt bepalen wie voor specifieke vergoedingen in aanmerking komt.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 543e43df2ec70e6f6e884019bb1c65bf3661ff35
ms.openlocfilehash: 3f9ab358ecbe7a992341610184002dbd97a31a4d
ms.lasthandoff: 03/31/2017


---

# <a name="benefit-eligibility-policies"></a>Beleid voor geschiktheid vergoedingen

In dit onderwerp geeft informatie over de vergoeding in aanmerking komen beleid, welke hulp u definiëren die in aanmerking voor specifieke voordelen komt.

Als u vergoedingen maakt, bepaalt u welke vergoedingen beschikbaar zijn voor welke werknemers. In de volgende tabel worden voorbeelden weergegeven van vergoedingen die u voor specifieke werknemers beschikbaar kunt maken.

| Vergoeding          | Voor wie de vergoeding beschikbaar is |
|------------------|---------------------------------|
| Ziektekostenverzekering | Alle werknemers                   |
| Mobiele telefoon     | Verkooppersoneel, leidinggevenden         |
| Parkeervergunningen   | Stafleden                      |

De volgende onderdelen in worden gebruikt om in aanmerking komen beleidsregels te maken:

-   Beleidsregeltypen
-   Beleid voor geschiktheid vergoedingen

Met typen bedrijfsregels worden de queryparameters bepaald die worden gebruikt wanneer u specifieke bedrijfsregels ontwikkelt. Nadat u typen beleidsregels hebt gemaakt, kunt u geschiktheidsbeleidsregels voor vergoedingen maken. Met de beleidsregels kunt u een verzameling regels maken die op een of meer rechtspersonen van toepassing zijn. Binnen elk beleid kunt u alle eerder gemaakte geschiktheidsbeleidsregels voor vergoedingen weergeven. 

U definieert het bereik van de regel binnen het beleid. Als u bijvoorbeeld een type geschiktheidsbeleidsregel voor vergoedingen maakt met de naam **Leidinggevende**, kunt u opgeven wat de regel binnen dat beleid is. In dit voorbeeld kan de regel aangeven dat elke functietitel die het woord "leidinggevende" bevat in de regel moet worden opgenomen. Nadat u de parameters van de regel of regels hebt gedefinieerd die in het beleid zijn opgenomen, kunt u een specifieke regel aan de vergoeding toewijzen.

<a name="see-also"></a>Zie ook
--------

[Een vergoedingsprogramma definiëren en beheren](manage-benefit-program.md)


