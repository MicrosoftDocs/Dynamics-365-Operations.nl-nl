---
title: Persoonscreening
description: In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125372"
---
# <a name="person-screening"></a>Persoonscreening

In dit onderwerp wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.

Fsyieke naam: mshr_hcmpersonscreeningentity

## <a name="description"></a>Beschrijving

Deze entiteit beschrijft de screenings waarvoor een kandidaat is geslaagd of moet slagen voor een aanstelling.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Persoonscreening**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Unieke primaire id voor de persoonscreeningrecord. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Het partijnummer (persoon) dat aan de kandidaat is gekoppeld. |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon). |
| **Screeningtype-id**<br>mshr_screeningtypeid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist<br>Refererende sleutel: Screeningtype | De id van het screeningtype dat is gedefinieerd in Human Resources. |
| **Waarde screeningtype-id**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmscreeningtypeentityid van mshr_hcmscreeningtypeentity | Door het systeem gegenereerde id voor de record van het screeningtype in de gekoppelde entiteit. |
| **Vereist door**<br>mshr_requiredby<br>*Datum/tijd* | Lezen/schrijven<br>Optioneel | De datum waarop de screening moet zijn voltooid. |
| **Status**<br>mshr_status<br>*mshr_hcmcompletionstatus option set*<br>Lezen/schrijven<br>Vereist | De status van de kandidaat voor de screening. |
| **Datum van voltooiing**<br>mshr_completeddate<br>*Datum/tijd* | Lezen/schrijven<br>Optioneel | De datum waarop de screening is voltooid. |
| **Opmerkingen**<br>mshr_note<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Notities die worden gebruikt door aanstellende managers en wervers. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

