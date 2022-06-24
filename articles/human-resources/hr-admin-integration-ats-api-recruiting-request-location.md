---
title: Locatie van wervingsaanvraag
description: In dit artikel wordt de entiteit Locatie wervingsaanvraag voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: d31af9ab62db310b89fbc7a2d7099621b59a356d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893811"
---
# <a name="recruiting-request-location"></a>Locatie van wervingsaanvraag


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Locatie wervingsaanvraag voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>Beschrijving

De lijst met locaties die zijn gedefinieerd als locaties waar geworven werknemers na aanstelling zullen werken. Dit zijn locaties die door rechtspersonen zijn gemaakt.

### <a name="json-representation"></a>JSON-weergave

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Locatie-ID**<br>mshr_locationid<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist | De door het systeem gegenereerde, door de gebruiker leesbare id voor de wervingslocatie. |
| **Locatie van wervingsaanvraag**<br>mshr_recruitingrequestlocationid<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist | Door de gebruiker gedefinieerde unieke id voor de wervingslocatie. |
| **Entiteits-id Locatie van wervingsaanvraag**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Alleen-lezen<br>Vereist | Unieke door het systeem gegenereerde id voor de record Locatie wervingsaanvraag. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Beschrijving van de locatie. |
| **Land-/regio-id**<br>mshr_countryregionid<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | Specificeert het land of de regio waar de kandidaat staatsburger is. |
| **Waarde voor land-/regio-id**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_logisticaddresscountryregionentityid van mshr_logisticsaddresscountryregionentity | Door het systeem gegenereerde unieke id van het land of de regio van het adres. |
| **ZipCode**<br>mshr_zipcode<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | Postcode. |
| **Adres**<br>mshr_street<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | Straatnaam. |
| **Plaats**<br>mshr_city<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | Plaats. |
| **Staat/provincie**<br>mshr_state<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | Staat of provincie. |
| **Land/regio**<br>mshr_county<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | Land. |
| **Telefoon**<br>mshr_telephone<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Telefoonnummer voor de locatie. |
| **E-mailadres**<br>mshr_email<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | E-mailadres. |
| **Internetadres**<br>mshr_internetaddress<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De URL voor de locatiewebsite. |
| **Id gegevensgebied**<br>mshr_dataareaid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Geeft de rechtspersoon (bedrijf) op. |
| **Waarde van id gegevensgebied**<br>_mshr_dataareaid_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: cdm_companyid van cdm_company entiteit | Door het systeem gegenereerde GUID-waarde die de rechtspersoon (het bedrijf) identificeert. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
