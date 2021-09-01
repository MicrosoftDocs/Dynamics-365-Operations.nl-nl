---
title: Status wervingsaanvraag
description: In dit onderwerp wordt de optieset voor Status wervingsaanvraag voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 91360b07915ba10472768ac32b473e6daf7163fa8aed24e6aabaaa91f0ec7154
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723666"
---
# <a name="recruiting-request-status"></a>Status wervingsaanvraag

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de optieset voor Status wervingsaanvraag voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmrecruitingrequeststatus

Voor deze opsomming wordt de optieset voor de statuswaarden van een wervingsaanvraag ingesteld.

| Waarde | Etiket | Beschrijving |
| --- | --- | --- |
| 200000000 | Concept | De aanvraag is in concept en gereed voor actieve werving. |
| 200000001 | Wordt gecontroleerd | De aanvraag is ingediend en wordt gerouteerd voor goedkeuring per werkstroom. Alleen beschikbaar als werkstroom is ingeschakeld. |
| 200000002 | In behandeling | De werkstroomactie voor de aanvraag is in behandeling. Alleen beschikbaar als werkstroom is ingeschakeld. |
| 200000003 | Geannuleerd | Het verzoek is geannuleerd. Alleen beschikbaar als werkstroom is ingeschakeld. |
| 200000004 | Geweigerd | De aanvraag is afgewezen. Alleen beschikbaar als werkstroom is ingeschakeld. |
| 200000005 | Actief | Elke werkstroom is voltooid en goedgekeurd en de aanvraag is klaar voor actieve werving. |
| 200000006 | Afgesloten | De wervingsaanvraag is gesloten. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]