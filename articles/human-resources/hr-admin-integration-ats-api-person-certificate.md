---
title: Certificaat van persoon
description: In dit onderwerp wordt de entiteit Certificaat van persoon voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 300bf294bb4b2fadd4c5d3e68e74674a69dd48f2
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067824"
---
# <a name="person-certificate"></a>Certificaat van persoon


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Certificaat van persoon voor Dynamics 365 Human Resources beschreven.

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

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Certificaat van persoon**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Alleen-lezen<br>Vereist | Door het systeem gegenereerde unieke id voor de entiteitsrecord van het certificaat van de persoon. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De partij-id (persoon) van de kandidaat. |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon). |
| **Certificaattype-id**<br>mshr_certificatetypeid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist |  De id van het certificaattype dat is gedefinieerd in Human Resources. |
| **Waarde certificaattype-id**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmcertificatetypeentityid van mshr_hcmcertificatetypeentity | Door het systeem gegenereerde unieke id voor het certificaattype in de gekoppelde entiteit. |
| **Begindatum**<br>mshr_startdate<br>*Datum/tijd* | Lezen/schrijven<br>Vereist | De datum waarop het certificaat is uitgegeven. |
| **Einddatum**<br>mshr_enddate<br>*Datum/tijd* | Lezen/schrijven<br>Optioneel | De datum waarop het certificaat afloopt. |
| **Opmerkingen**<br>mshr_notes<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Notities die worden gebruikt door aanstellende managers en wervers. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist |  Het veld dat moet worden gebruikt als id van de entiteitsrecord. Combinatie van partijnummer, certificaattype-id en begindatum. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
