---
title: Vaardigheid wervingsaanvraag
description: In dit onderwerp wordt de entiteit Vaardigheid wervingsaanvraag voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 52dc7a839249ad8d55bb1f52cc5efe15cdf18e13
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059203"
---
# <a name="recruiting-request-skill"></a>Vaardigheid wervingsaanvraag

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Vaardigheid wervingsaanvraag voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>Beschrijving

Beschrijft vaardigheidsvereisten voor een wervingsaanvraag.

### <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Vaardigheid wervingsaanvraag**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Alleen-lezen<br>Vereist | Unieke, door het systeem gegenereerde id voor de record **Vaardigheid wervingsaanvraag**. |
| **Wervingsaanvraag-id**<br>mshr_recruitingrequestid<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist | De door de gebruiker leesbare unieke id van de gekoppelde wervingsaanvraag. |
| **Waarde wervingsaanvraag-id**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br> Refererende sleutel: mshr_hcmrecruitingrequestentityid van mshr_hcmrecruitingrequestentity entiteit | De door het systeem gegenereerde unieke id van de gekoppelde wervingsaanvraag. |
| **Vaardigheids-id**<br>mshr_skillid<br>*Tekenreeks*<br> | Eenmaal schrijven<br>Vereist | De door de gebruiker leesbare unieke id van de vereiste vaardigheid. |
| **Waarde vaardigheids-id**<br>_mshr_fk_skill_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmskillentityid van mshr_hcmskillentity entiteit | Unieke door het systeem gegenereerde id van de vereiste vaardigheid. |
| **Beoordelingsniveau-id**<br>mshr_ratinglevelid<br>*Tekenreeks* | Eenmaal schrijven<br>Optioneel | De vereiste waarde voor het vaardigheidsniveau dat voor de functie is geselecteerd, op basis van het beoordelingsmodel dat aan de vaardigheid is toegewezen. |
| **Waarde beoordelingsniveau-id**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmratinglevelentityid van mshr_hcmratinglevelentity entiteit | Door het systeem gegenereerde unieke id voor het niveau. |
| **Omschrijving vaardigheid**<br>mshr_skilldescription<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De omschrijving van de vaardigheid. |
| **Omschrijving beoordelingsniveau**<br>mshr_ratingleveldescription<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | De omschrijving van de geselecteerde vaardigheidsniveau. |
| **Id gegevensgebied**<br>mshr_dataareaid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Geeft de rechtspersoon (bedrijf) op. |
| **Waarde van id gegevensgebied**<br>_mshr_dataareaid_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: cdm_companyid van cdm_company entiteit | Door het systeem gegenereerde GUID-waarde die de rechtspersoon (het bedrijf) identificeert. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Samenvoeging van de waarde en vaardigheids-id van de wervingsaanvraag als een andere methode om een record een unieke id te geven. |
| **Beoordelingsmodel-id**<br>mshr_ratingmodelid<br>*Tekenreeks* | Lezen-schrijven<br>Vereist | Het beoordelingsmodel dat wordt gebruikt om de vaardigheid te beoordelen. |
| **Waarde beoordelingsmodel-id**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmratingmodelentityid van mshr_hcmratingmodelentity entiteit | Door het systeem gegenereerde unieke id van het beoordelingsmodel dat wordt gebruikt om de vaardigheid te beoordelen. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]