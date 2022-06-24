---
title: Persoonscreening
description: In dit artikel wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: e9b2bbda8f8191f592462f4fbd1902e7274cf7f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907635"
---
# <a name="person-screening"></a>Persoonscreening


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
