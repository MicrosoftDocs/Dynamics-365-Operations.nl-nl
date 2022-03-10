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
ms.openlocfilehash: d845179077fc2e04dfb3bd05eaa70b0a2a016121
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067096"
---
# <a name="recruiting-request-status"></a>Status wervingsaanvraag


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
