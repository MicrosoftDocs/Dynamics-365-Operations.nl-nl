---
title: Werkervaring van persoon
description: In dit artikel wordt de entiteit Werkervaring van persoon voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: d306213e4c647ecd4be98598cba92376aba0d5bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856420"
---
# <a name="person-professional-experience"></a>Werkervaring van persoon


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Werkervaring van persoon voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>Beschrijving

Deze entiteit beschrijft werkervaring of arbeidsverleden van een kandidaat.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Werkervaring van persoon**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Alleen-lezen<br>Vereist | Door het systeem gegenereerde unieke id voor de entiteitsrecord. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Unieke id van de partijrecord (persoon) voor de kandidaat. |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | Door het systeem gegenereerde unieke id voor de entiteitsrecord van de persoon. |
| **Positie werkgever**<br>mshr_employerposition<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De functie die de kandidaat bekleedt bij een dienstverband. |
| **Naam van werkgever**<br>mshr_employername<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De naam van de werkgever. |
| **Locatie werkgever**<br>mshr_employerlocation<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De locatie van de werkgever. Maximale lengte: 60. Er is geen specifieke indeling gedefinieerd of vereist. |
| **Telefoonnummer**<br>mshr_phone<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het telefoonnummer van de werkgever. |
| **URL**<br>mshr_url<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De URL van de website van de werkgever. |
| **Begindatum**<br>mshr_startdate<br>*Datum/tijd* | Lezen/schrijven<br>Vereist | De begindatum van het dienstverband van de kandidaat. |
| **Einddatum**<br>mshr_enddate<br>*Datum/tijd* | Lezen/schrijven<br>Optioneel | De einddatum van het dienstverband van de kandidaat of null als de kandidaat hier nog in dienst is. |
| **Contact met werkgever toestaan**<br>mshr_allowcontactemployer<br>*mshr_hrmblankyesno optieset* | Lezen/schrijven<br>Optioneel | Geeft aan of de kandidaat contact mag opnemen met de vorige werkgever. |
| **Opmerkingen**<br>mshr_note<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Notities die worden gebruikt door de werver of de aanstellend manager. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Veld dat wordt gebruikt als een primaire id van de entiteitsrecord. Combinatie van partijnummer, begindatum, werkgeverpositie en werkgevernaam. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
