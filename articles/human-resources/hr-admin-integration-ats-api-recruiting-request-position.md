---
title: Positie van wervingsaanvraag
description: In dit onderwerp wordt de entiteit Positie van wervingsaanvraag voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 76c96b722c2be76d9aff999633ffd30a576a1614bdc5e4cc4a24fb17d92fe22a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758731"
---
# <a name="recruiting-request-position"></a>Positie van wervingsaanvraag

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Positie van wervingsaanvraag voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>Beschrijving

Beschrijft de positie of posities om op te vullen voor een wervingsaanvraag. Een positie toevoegen aan de wervingsaanvraag is optioneel. De eigenschappen van de positie zijn alleen-lezen, omdat de positie-eigenschappen niet anders mogen zijn in de wervingsaanvraag dan in de hoofdrecord van de positie. Als de eigenschappen moeten worden gewijzigd, moet dit op de hoofdrecord van de positie worden uitgevoerd voordat u de positie toevoegt aan de wervingsaanvraag.

### <a name="json-representation"></a>JSON-weergave
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Positie van wervingsaanvraag**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Alleen-lezen<br>Vereist |    Door het systeem gegenereerde unieke id van de wervingsaanvraagrecord. |
| **Wervingsaanvraag-id**<br>mshr_recruitingrequestid<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist | De door de gebruiker leesbare unieke id van de wervingsaanvraag. |
| **Waarde wervingsaanvraag-id**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmrecruitingrequestentityid van mshr_hcmrecruitingrequestentity entiteit | Door het systeem gegenereerde unieke id van de wervingsaanvraag waaraan de positie is toegewezen. |
| **Positie-id**<br>mshr_positionid<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist | De door de gebruiker leesbare unieke id van de positie. |
| **Waarde positie-id**<br>_mshr_fk_position_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmpositionv2entityid van de entiteit mshr_2entity | Door het systeem gegenereerde id van de positie. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De omschrijving van de positie. |
| **Positietype-id**<br>mshr_positiontypeid<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | De door de gebruiker leesbare unieke id van het positietype voor deze positie. |
| **Waarde positietype-id**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmpositiontypeentityid van de entiteit mshr_hcmpositiontypeentity | Een door het systeem gegenereerde unieke id van het positietype voor deze positie. |
| **Status**<br>mshr_status<br>*Positiestatus van wervingsaanvraag* optieset | Lezen/schrijven<br>Vereist | Status van de positie voor de wervingsaanvraag. |
| **Afdelingsnummer**<br>mshr_departmentnumber<br>*Tekenreeks* | Alleen-lezen<br>Optioneel<br> | Het afdelingsnummer van de positie. |
| **Waarde afdelings-id**<br>_mshr_fk_department_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_omdepartmententityid van de entiteit mshr_omdepartmententity | Door het systeem gegenereerde unieke id van de afdeling van de positie. |
| **Positie-id manager**<br>mshr_reportstopositionid<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De door de gebruiker leesbare id van de positie waaraan de wervingspositie rapporteert in de organisatiehiërarchie. |
| **Waarde positie-id manager**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmpositionv2entityid van de entiteit mshr_2entity | De door het systeem gegenereerde id van de positie waaraan de wervingspositie rapporteert. |
| **Personeelsnummer manager**<br>mshr_reportstopersonnelnumber<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De werknemer-id van de werknemer aan wie de in dienst genomen kandidaat zal rapporteren. |
| **Waarde werknemer-id manager**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmworkerbaseentityid van de entiteit mshr_hcmworkerbaseentity | Door het systeem gegenereerde id van de werknemer aan wie de aangestelde kandidaat zal rapporteren. |
| **Financiële dimensie**<br>mshr_financialdimension<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | De financiële dimensie (bijvoorbeeld de kostenplaats) die aan de positie is toegewezen. De financiële dimensie wordt toegewezen voor elke positie per rechtspersoon. Kostenplaatsen die in dimensies zijn gedefinieerd, zijn toegankelijk via de entiteit mshr_dimattributeomcostcenterentity. |
| **Id gegevensgebied**<br>mshr_dataareaid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Specificeert de rechtspersoon (bedrijf) voor de positie voor de wervingsaanvraag. |
| **Waarde van id gegevensgebied**<br>_mshr_dataareaid_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: cdm_companyid van cdm_company entiteit | Door het systeem gegenereerde GUID-waarde die de rechtspersoon (bedrijf) identificeert voor de wervingsaanvraagpositie. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Samenvoeging van de waarde en positie-id van de wervingsaanvraag als een andere methode om een record een unieke id te geven. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]