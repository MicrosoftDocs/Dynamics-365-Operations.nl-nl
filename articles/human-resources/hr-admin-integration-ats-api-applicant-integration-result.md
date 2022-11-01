---
title: Integratieresultaat van sollicitant
description: In dit artikel wordt de resulterende optieset voor de integratie Sollicitant voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 09/12/2022
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
ms.openlocfilehash: 86f3f75e538268644cea4f927f04c07aae115f00
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702223"
---
# <a name="applicant-integration-result"></a>Integratieresultaat van sollicitant


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de resulterende optieset voor de integratie Sollicitant voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmapplicantintegrationresult

Deze opsomming geeft de status van een kandidaatrecord.

| Waarde | Etiket | Beschrijving |
| --- | --- | --- |
| 200000000 | Niet verwerkt | Kandidaat komt nog in aanmerking. |
| 200000001 | Aangenomen | De kandidaat is aangenomen. |
| 200000002 | Niet in dienst genomen | De beslissing is genomen om de kandidaat niet in dienst te nemen. |
| 200000003 | Genegeerd | De kandidaat werd afgewezen. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
