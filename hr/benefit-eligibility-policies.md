---
title: Beleid voor geschiktheid vergoedingen
description: Dit artikel biedt informatie over het beleid voor geschiktheid voor vergoedingen, waarmee u kunt bepalen wie voor specifieke vergoedingen in aanmerking komt.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
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
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8c158ac5badd22054db86d269b58d223274176d2
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="benefit-eligibility-policies"></a>Beleid voor geschiktheid vergoedingen

[!include[banner](includes/banner.md)]


Dit onderwerp bevat informatie over het beleid voor geschiktheid voor vergoedingen, waarmee u kunt bepalen wie voor specifieke vergoedingen in aanmerking komt.

Als u vergoedingen maakt, bepaalt u welke vergoedingen beschikbaar zijn voor welke werknemers. In de volgende tabel worden voorbeelden weergegeven van vergoedingen die u voor specifieke werknemers beschikbaar kunt maken.

| Vergoeding          | Voor wie de vergoeding beschikbaar is |
|------------------|---------------------------------|
| Ziektekostenverzekering | Alle werknemers                   |
| Mobiele telefoon     | Verkooppersoneel, leidinggevenden         |
| Parkeervergunningen   | Stafleden                      |

De volgende onderdelen worden gebruikt om geschiktheidsbeleid te maken:

-   Beleidsregeltypen
-   Beleid voor geschiktheid vergoedingen

Met typen bedrijfsregels worden de queryparameters bepaald die worden gebruikt wanneer u specifieke bedrijfsregels ontwikkelt. Nadat u typen beleidsregels hebt gemaakt, kunt u geschiktheidsbeleidsregels voor vergoedingen maken. Met de beleidsregels kunt u een verzameling regels maken die op een of meer rechtspersonen van toepassing zijn. Binnen elk beleid kunt u alle eerder gemaakte geschiktheidsbeleidsregels voor vergoedingen weergeven. 

U definieert het bereik van de regel binnen het beleid. Als u bijvoorbeeld een type geschiktheidsbeleidsregel voor vergoedingen maakt met de naam **Leidinggevende**, kunt u opgeven wat de regel binnen dat beleid is. In dit voorbeeld kan de regel aangeven dat elke functietitel die het woord "leidinggevende" bevat in de regel moet worden opgenomen. Nadat u de parameters van de regel of regels hebt gedefinieerd die in het beleid zijn opgenomen, kunt u een specifieke regel aan de vergoeding toewijzen.

<a name="see-also"></a>Zie ook
--------

[Een vergoedingsprogramma definiëren en beheren](manage-benefit-program.md)




