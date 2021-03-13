---
title: Adres van persoon
description: In dit onderwerp wordt de entiteit Adres van persoon voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 9911362ff8260860864cfe24f0b60f59adb77186
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125877"
---
# <a name="person-address"></a>Adres van persoon

In dit onderwerp wordt de entiteit Adres van persoon voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmpersonaddressentities

## <a name="description"></a>Beschrijving

Deze entiteit bevat de lijst met postadressen voor kandidaatrecords.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Adres van persoon**<br>mshr_hcmpersonaddressentityid<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Door het systeem gegenereerde unieke id voor de entiteitsrecord. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De id van de gekoppelde partijrecord (persoon). |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon). |
| **Locatie-ID**<br>mshr_locationid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De locatie-id van de adresrecord. Stel dit in de entiteit mshr_logisticspostaladdresslocationcdsentity in. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Een omschrijving van het adres van de kandidaat. |
| **Rollen**<br>mshr_roles<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De rollen die voor dit adres zijn toegewezen. Er kunnen meerdere rollen worden toegewezen. De rollen moeten van elkaar worden gescheiden door een puntkomma. Geldige waarden in de entiteit mshr_logisticslocationroleentity. |
| **Adres**<br>mshr_street<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het huisnummer. |
| **Plaats**<br>mshr_city<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De plaats van het adres. Stel deze in de entiteit mshr_logisticsaddresscityentity in. |
| **Staat/provincie**<br>mshr_state<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De provincie van het adres. Stel deze in de entiteit nmshr_logisticsaddressstateentity in. |
| **Land/regio**<br>mshr_county<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De regio van het adres. Stel deze in de entiteit mshr_logisticsaddresscountyentity in. |
| **Postcode**<br>mshr_zipcode<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De postcode van het adres. Stel deze in de entiteit mshr_logisticsaddresspostalcodeentity in. |
| **Land-/regio-id**<br>mshr_countryregionid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het land of de regio van het adres. |
| **Waarde voor land-/regio-id**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_logisticaddresscountryregionentityid van mshr_logisticsaddresscountryregionentity | Door het systeem gegenereerde unieke id van het land of de regio van het adres. |
| **Is primair**<br>mshr_isprimary<br>*mshr_noyes optieset* | Lezen/schrijven<br>Vereist | Identificeert of dit adres het primaire adres is voor de persoon met de gedefinieerde rol. |
| **Is privé**<br>mshr_isprivate<br>*mshr_noyes optieset* | Lezen/schrijven<br>Vereist | Geeft aan of dit adres een privéadres voor de persoon is. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Veld dat wordt gebruikt als een primaire id van de entiteitsrecord. Combinatie van partijnummer en locatie-id. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

