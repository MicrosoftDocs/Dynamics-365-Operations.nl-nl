---
title: Integratieresultaat van sollicitant
description: In dit onderwerp wordt de resulterende optieset voor de integratie Sollicitant voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: dd25eca9cccf46ec4e4bb2a1d948ca98985e73e4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467548"
---
# <a name="applicant-integration-result"></a>Integratieresultaat van sollicitant

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de resulterende optieset voor de integratie Sollicitant voor Dynamics 365 Human Resources beschreven.

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