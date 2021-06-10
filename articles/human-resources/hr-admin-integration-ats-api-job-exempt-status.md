---
title: Vrijstellingsstatus taak
description: In dit onderwerp wordt de optieset voor Vrijstellingsstatus taak voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053846"
---
# <a name="job-exempt-status"></a>Vrijstellingsstatus taak

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de optieset voor Vrijstellingsstatus taak voor Dynamics 365 Human Resources beschreven.

Fysieke naam: cdm_jobexemptstatus

Deze opsomming specificeert de optieset voor de waarden voor FLSA-vrijstellingsstatussen voor taken. Dit wordt opgegeven in de bestaande optieset voor cdm_jobexemptstatus.

| Waarde | Etiket | Beschrijving |
| --- | --- | --- |
| 200000000 | Vrijstelling | De taak heeft een vrijstellingsstatus op basis van de FLSA-richtlijnen. |
| 200000001 | Geen vrijstelling | De taak heeft de status Geen vrijstelling op basis van de FLSA-richtlijnen. |
| 200000002 | Niet van toepassing | De richtlijnen voor de FLSA-status zijn niet van toepassing op de taak. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]