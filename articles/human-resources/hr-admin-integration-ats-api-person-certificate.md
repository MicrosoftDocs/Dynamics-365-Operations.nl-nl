---
title: Certificaat van persoon
description: In dit artikel wordt de entiteit Certificaat van persoon voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 12/15/2022
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
ms.openlocfilehash: 1f9d5a8c83d9714a4d10dec16e66ab87b794b074
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887312"
---
# <a name="person-certificate"></a>Certificaat van persoon


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Certificaat van persoon voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmpersoncertificateentity

## <a name="description"></a>Beschrijving

Deze entiteit beschrijft de professionele certificaten van een kandidaat.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Description |
| --- | --- | --- |
| **Certificaattype-id**<br>mshr_certificatetypeid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist |  De id van het certificaattype dat is gedefinieerd in Human Resources. |
| **Begindatum**<br>mshr_startdate<br>*Datum/tijd* | Lezen/schrijven<br>Vereist | De datum waarop het certificaat is uitgegeven. |
| **Einddatum**<br>mshr_enddate<br>*Datum/tijd* | Lezen/schrijven<br>Optioneel | De datum waarop het certificaat afloopt. |
| **Opmerkingen**<br>mshr_notes<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Notities die worden gebruikt door aanstellende managers en wervers. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De partij-id (persoon) van de kandidaat. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist |  Het veld dat moet worden gebruikt als id van de entiteitsrecord. Combinatie van partijnummer, certificaattype-id en begindatum. |
| **Waarde certificaattype-id**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmcertificatetypeentityid van mshr_hcmcertificatetypeentity | Door het systeem gegenereerde unieke id voor het certificaattype in de gekoppelde entiteit. |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon). |
| **Entiteits-id Certificaat van persoon**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Alleen-lezen<br>Vereist | Door het systeem gegenereerde unieke id voor de entiteitsrecord van het certificaat van de persoon. |




## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
