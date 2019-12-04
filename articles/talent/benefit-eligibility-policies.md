---
title: Beleid voor geschiktheid vergoedingen
description: Dit artikel biedt informatie over het beleid voor geschiktheid voor vergoedingen, waarmee u kunt bepalen wie voor specifieke vergoedingen in aanmerking komt.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: b44287bf22f0b6c4e33a29b4b86aaae934505a43
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814688"
---
# <a name="benefit-eligibility-policies"></a>Beleid voor geschiktheid vergoedingen

[!include [banner](includes/banner.md)]

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

U definieert het bereik van de regel binnen het beleid. Als u bijvoorbeeld een type geschiktheidsbeleidsregel voor vergoedingen maakt met de naam **Leidinggevende**, kunt u opgeven wat de regel binnen dat beleid is. In dit voorbeeld kan de regel aangeven dat elke functietitel die het woord 'leidinggevende' bevat in de regel moet worden opgenomen. Nadat u de parameters van de regel of regels hebt gedefinieerd die in het beleid zijn opgenomen, kunt u een specifieke regel aan de vergoeding toewijzen.

<a name="additional-resources"></a>Aanvullende resources
--------

[Een vergoedingenprogramma definiëren en beheren](manage-benefit-program.md)



