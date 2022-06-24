---
title: Positiestatus voor wervingsaanvragen
description: In dit artikel wordt de optieset voor Positiestatus voor wervingsaanvragen voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846400"
---
# <a name="recruiting-request-position-status"></a>Positiestatus voor wervingsaanvragen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de optieset voor Positiestatus voor wervingsaanvragen voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmrecruitingrequestpositionstatus

Deze opsomming bevat de optieset voor de statuswaarden van elke positie een wervingsaanvraag in de entiteit Positie van wervingsaanvraag.

| Waarde | Etiket | Beschrijving |
| --- | --- | --- |
| 200000000 | Openstaande | De positie in de wervingsaanvraag is open voor werving. Dit geeft niet aan dat er momenteel geen actieve positietoewijzing voor de positie bestaat. Op het moment van werving kan er een werknemer in de positie zijn. Dit geeft alleen aan dat de positie beschikbaar is voor werving in de context van de wervingsaanvraag. |
| 200000001 | Ingevuld | Er is een werknemer geselecteerd voor toewijzing aan de positie. |
| 200000002 | Geannuleerd | De aanvraag om personeel voor deze positie te werven is geannuleerd. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
