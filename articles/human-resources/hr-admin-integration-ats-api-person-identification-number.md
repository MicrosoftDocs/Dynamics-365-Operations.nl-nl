---
title: Persoonlijk identificatienummer
description: In dit artikel wordt de entiteit Persoonlijk identificatienummer beschreven voor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2d3641ffede29b7fda904ffb6cd70cb33d7800d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858267"
---
# <a name="person-identification-number"></a>Persoonlijk identificatienummer


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Persoonlijk identificatienummer beschreven voor Dynamics 365 Human Resources.

Fysieke naam: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>Beschrijving

Deze entiteit beschrijft de identificatienummers voor de kandidaat. Hiermee kan de API-consument identificatienummers, zoals burgerservicenummers of paspoortnummers, in het kandidatendossier schrijven. Identificatienummers verschijnen in het werknemersdossier, maar niet in de kandidaat-record. Een integrerende toepassing kan de waarden schrijven naar de Human Resources-database, maar de getallen zijn pas zichtbaar in Human Resources als de werknemersrecord van de kandidaat is gemaakt.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id persoonlijk identificatienummer**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Unieke primaire id voor het persoonlijk identificatienummerrecord. |
| **Invoertype**<br>mshr_entrytype<br>*Tekenreeks* | Lezen-schrijven<br>Optioneel | Vrije waarde om te verwijzen naar het type vermelding voor het identificatienummer. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen-schrijven<br>Optioneel | De omschrijving van het identificatienummer. |
| **Vervaldatum**<br>mshr_expirationdate<br>*Datum/tijd* | Lezen-schrijven<br>Optioneel | De datum waarop het identificatienummer of bijbehorende document vervalt. |
| **Is primair**<br>mshr_isprimary<br>*mshr_noyes optieset* | Lezen-schrijven<br>Optioneel | Definieert of het identificatienummer de primaire record voor de persoon voor dit identificatietype is. |
| **Identificatienummer**<br>mshr_identificationnumber<br>*Tekenreeks* | Lezen-schrijven<br>Vereist | Het identificatienummer. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen-schrijven<br>Vereist | De id van de partij (persoon) die eigenaar is van het identificatienummer. |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity entiteit | De unieke id van de partij (persoon). |
| **Identificatietype-id**<br>mshr_identificationtypeid<br>*Tekenreeks* | Lezen-schrijven<br>Vereist | Het type identificatienummer. |
| **Waarde identificatietype-id**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmidentificationtypeentityid van mshr_hcmidentificationtypeentity entiteit | Unieke id van het identificatietype die door het systeem is gegenereerd. |
| **Uitgifte-instantie-id**<br>mshr_issuingagencyid<br>*Tekenreeks* | Lezen-schrijven<br>Optioneel | De instantie of organisatie die het identificatienummer uitgeeft. |
| **Waarde uitgifte-instantie-id**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmissuingagencyentityid van mshr_hcmissuingagencyentity entiteit | Unieke, door het systeem gegenereerde id van de instantie die het identificatienummer uitgeeft. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Het veld dat moet worden gebruikt als id van de entiteitsrecord. Combinatie van partijnummer, id van het identificatietype en identificatienummer. |
| **Uitgiftedatum**<br>mshr_issuedate<br>*Datum* | Lezen-schrijven<br>Optioneel | De datum waarop het identificatienummer is uitgegeven. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
