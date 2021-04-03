---
title: Beoordelingsniveau
description: In dit onderwerp wordt de entiteit Beoordelingsniveau voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 2dbdbea7087d8bca8563da10d1bf9a97df24e8b3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464737"
---
# <a name="rating-level"></a>Beoordelingsniveau

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Beoordelingsniveau voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmratinglevelentity

## <a name="description"></a>Beschrijving

Deze entiteit voorziet in de beschikbare beoordelingsniveaus voor vaardigheden. Beoordelingsniveaus gelden voor alle rechtspersonen.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Beoordelingsniveau**<br>mshr_hcmratinglevelentityid<br>*GUID* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | De door het systeem gegenereerde unieke id voor het niveau. |
| **Beoordelingsniveau-id**<br>mshr_ratinglevelid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Door de gebruiker leesbare unieke id voor het niveau. |
| **Beoordelingsmodel-id**<br>mshr_ratingmodelid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Het beoordelingsmodel waarbij het beoordelingsniveau hoort. |
| **Entiteits-id Beoordelingsmodel**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmratingmodelentityid van mshr_hcmratingmodelentity | De door het systeem gegenereerde id voor het beoordelingsmodel waarbij het beoordelingsniveau hoort. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De omschrijving van het beoordelingsniveau. |
| **Factor**<br>mshr_factor<br>*Geheel getal* | Lezen/schrijven<br>Vereist | De factor in voor het beoordelingsniveau. Wanneer u items vergelijkt met een ander aantal beoordelingsniveaus, wordt deze factor gebruikt om de scores te standaardiseren. De waarde moet een geheel getal tussen 0 en 9 zijn. |
| **Opmerking**<br>mshr_note<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Eventuele notities die zijn gekoppeld aan het beoordelingsniveau. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Het veld dat moet worden gebruikt als id van de entiteitsrecord. Combinatie van beoordelingsniveau-id en beoordelingsmodel-id. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]