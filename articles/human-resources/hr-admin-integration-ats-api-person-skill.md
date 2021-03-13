---
title: Vaardigheid van persoon
description: In dit onderwerp wordt de entiteit Vaardigheid van persoon voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: b6bcbbd1203f4e9e80f6c5264cf4d5ea7d0970fc
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126093"
---
# <a name="person-skill"></a>Vaardigheid van persoon

In dit onderwerp wordt de entiteit Vaardigheid van persoon voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmpersonskillentity

## <a name="description"></a>Beschrijving

Deze entiteit beschrijft de vaardigheden van een kandidaat.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Vaardigheid van de persoon**<br>mshr_hcmpersonskillentityid<br>*GUID* | Alleen-lezen<br>Vereist | Door het systeem gegenereerde unieke id voor de entiteitsrecord. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist |   De id van de gekoppelde partijrecord (persoon). |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon). |
| **Certificerende partij**<br>mshr_certifier<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het personeelsnummer van de werknemer die deze vaardigheid heeft gecertificeerd. |
| **Waarde id van certificerende partij**<br>_mshr_fk_certifier_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmworkerentityid van mshr_hcmworkerentity | Door het systeem gegenereerde unieke id van de werknemerrecord voor de werknemer die de vaardigheid heeft gecertificeerd. |
| **Vaardigheids-id**<br>mshr_skillid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De id van de vaardigheid die is gedefinieerd in Human Resources. |
| **Waarde vaardigheids-id**<br>_mshr_fk_skill_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmskillentityid van mshr_hcmskillentity | De door het systeem gegenereerde id van de geselecteerde vaardigheid. |
| **Jaren ervaring**<br>mshr_yearsofexperience<br>*Decimaal* | Lezen/schrijven<br>Optioneel | De jaren ervaring die de kandidaat heeft met deze vaardigheid. |
| **Beoordelings-id**<br>mshr_ratingid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Het schaaltype van de beoordeling. Voor deze entiteit is de waarde **Vaardigheden**. |
| **Niveautype**<br>mshr_leveltype<br>*mshr_hrmskillleveltype optieset* | Lezen/schrijven<br>Vereist | Een type categorisatie voor het niveau dat aan de vaardigheid is toegewezen. |
| **Niveau-id**<br>mshr_levelid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De id van het beoordelingsniveau dat de kandidaat voor deze kwalificatie heeft. |
| **Waarde beoordelingsniveau-id**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmratinglevelentityid van mshr_hcmratinglevelentity | De door het systeem gegenereerde id van het beoordelingsniveau. |
| **Niveaudatum**<br>mshr_leveldate<br>*Datum/tijd* | Lezen/schrijven<br>Vereist | De datum waarop de kandidaat in de vaardigheid is beoordeeld. |
| **Beoordelingsniveau examinator**<br>mshr_ratinglevelexaminer<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het personeelsnummer van de werknemer die de kandidaat heeft beoordeeld. |
| **Waarde beoordelingsniveau-id examinator**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmworkerentityid van mshr_hcmworkerentity | De door het systeem gegenereerde id van de werknemer die het vaardigheidsniveau van de kandidaat heeft onderzocht. |
| **Geverifieerd**<br>mshr_verified<br>*mshr_noyes optieset* | Lezen/schrijven<br>Vereist | Geeft aan of het beoordeelde vaardigheidsniveau is geverifieerd. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Het veld dat moet worden gebruikt als id van de entiteitsrecord. Combinatie van partijnummer, niveautype, vaardigheids-id en niveaudatum. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

