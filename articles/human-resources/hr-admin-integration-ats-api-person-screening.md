---
title: Persoonscreening
description: In dit artikel wordt de entiteit Persoonscreening voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 12/05/2022
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
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831885"
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
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Description |
| --- | --- | --- |
| **Opmerkingen**<br>mshr_note<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Notities die worden gebruikt door aanstellende managers en wervers. |
| **Vereist door**<br>mshr_requiredby<br>*Datum/tijd* | Lezen/schrijven<br>Optioneel | De datum waarop de screening moet zijn voltooid. |
| **Status**<br>mshr_status<br>*mshr_hcmcompletionstatus option set*|Lezen/schrijven<br>Vereist | De status van de kandidaat voor de screening. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Het partijnummer (persoon) dat aan de kandidaat is gekoppeld. |
| **Screeningtype-id**<br>mshr_screeningtypeid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist<br>Refererende sleutel: Screeningtype | De id van het screeningtype dat is gedefinieerd in Human Resources. |
| **Waarde screeningtype-id**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmscreeningtypeentityid van mshr_hcmscreeningtypeentity | Door het systeem gegenereerde id voor de record van het screeningtype in de gekoppelde entiteit. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* |  Alleen-lezen<br>Vereist | Het veld dat moet worden gebruikt als id van de entiteitsrecord. |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon). |
| **Entiteits-id Persoonscreening**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd| Unieke primaire id voor de persoonscreeningrecord. |
| **Datum van voltooiing**<br>mshr_completeddate<br>*Datum/tijd* | Lezen/schrijven<br>Optioneel | De datum waarop de screening is voltooid. |


## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
