---
title: Positiestatus voor wervingsaanvragen
description: In dit onderwerp wordt de optieset voor Positiestatus voor wervingsaanvragen voor Dynamics 365 Human Resources beschreven.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126045"
---
# <a name="recruiting-request-position-status"></a>Positiestatus voor wervingsaanvragen

In dit onderwerp wordt de optieset voor Positiestatus voor wervingsaanvragen voor Dynamics 365 Human Resources beschreven.

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