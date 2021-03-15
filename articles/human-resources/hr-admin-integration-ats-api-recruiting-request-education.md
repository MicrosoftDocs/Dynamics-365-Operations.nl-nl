---
title: Opleiding wervingsaanvraag
description: In dit onderwerp wordt de entiteit Opleiding wervingsaanvraag voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 1767edfe67f9c3af4ac67eb5403d63a7f54dcac8
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126069"
---
# <a name="recruiting-request-education"></a>Opleiding wervingsaanvraag

In dit onderwerp wordt de entiteit Opleiding wervingsaanvraag voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>Beschrijving

Beschrijft opleidingsvereisten voor een wervingsaanvraag.

### <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Opleiding wervingsaanvraag**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Alleen-lezen<br>Vereist | Unieke door het systeem gegenereerde id voor de record Opleiding wervingsaanvraag. |
| **Wervingsaanvraag-id**<br>mshr_recruitingrequestid<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist | De door de gebruiker leesbare unieke id van de gerelateerde wervingsaanvraag. |
| **Waarde wervingsaanvraag-id**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmrecruitingrequestentityid van mshr_hcmrecruitingrequestentity | De door het systeem gegenereerde unieke id van de gerelateerde wervingsaanvraag. |
| **Opleidingsniveau-id**<br>mshr_educationlevelid<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist | Het vereiste opleidingsniveau. |
| **Waarde opleidingsniveau-id**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmeducationlevelentityid van mshr_hcmeducationlevelentity | Unieke door het systeem gegenereerde id van het vereiste opleidingsniveau. |
| **Omschrijving opleidingsniveau**<br>mshr_educationleveldescription<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De omschrijving van het vereiste niveau voor de vaardigheid. |
| **Opleidingsvakgebied-id**<br>mshr_educationdisciplinedescription<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist | Het vakgebied van de opleiding. |
| **Waarde opleidingsvakgebied-id**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmeducationdisciplineentityid van mshr_hcmeducationdisciplineentity | Unieke door het systeem gegenereerde id van het vakgebied van de opleiding. |
| **Omschrijving vakgebied van opleiding**<br>mshr_educationdisciplinedescription<br>Tekenreeks | Alleen-lezen<br>Vereist | De omschrijving van het vakgebied van de opleiding. |
| **Id gegevensgebied**<br>mshr_dataareaid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Geeft de rechtspersoon (bedrijf) op.|
| **Waarde van id gegevensgebied**<br>_mshr_dataareaid_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: cdm_companyid van cdm_company entiteit | Door het systeem gegenereerde GUID-waarde die de rechtspersoon (het bedrijf) identificeert. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Samenvoeging van de waarde, de opleidingsniveau-id en de opleidingsvakgebied-id van de wervingsaanvraag als een andere methode om een record een unieke id te geven. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]