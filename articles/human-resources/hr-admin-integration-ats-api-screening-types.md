---
title: Screeningtypen
description: In dit artikel wordt de entiteit Screeningtypen voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 95f4a3dce6851c7080ac665f5922e3b5877fa9f3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880533"
---
# <a name="screening-types"></a>Screeningtypen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Screeningtypen voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmscreeningtypeentity

## <a name="description"></a>Beschrijving

Deze entiteit beschrijft de screeningtypen die door het bedrijf zijn ingesteld voor lopende screeningprocessen en screeningprocessen voorafgaand aan een dienstverband voor werknemers.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Screeningtype**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Unieke primaire id voor de screeningtyperecord. |
| **Screeningtype-id**<br>mshr_screeningtypeid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Door de gebruiker gedefinieerde unieke primaire id voor het screeningtype. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De omschrijving van het screeningtype. |
| **Frequentie-eenheid**<br>mshr_frequencyunit<br>*mshr_hcmfrequencyunit optieset* | Lezen/schrijven<br>Vereist | Beschrijft de frequentie waarmee de screening moet worden uitgevoerd voor de toegewezen persoon. |
| **Genereren op basis van**<br>mshr_generatefrom<br>*mshr_hcmfrequencygeneratefrom optieset* | Lezen-schrijven<br>Vereist | Als de frequentiewaarde een andere waarde is dan 'Eenmalig', bepaalt de waarde GenerateFrom de datum waarop de volgende screeninggebeurtenis wordt berekend. |
| **Frequentie-interval**<br>mshr_frequencyinterval<br>*Geheel getal* | Lezen-schrijven<br>Vereist | Als de waarde Frequentie een andere waarde is dan 'Eenmalig', moet u een interval definiëren voor de tijdseenheden tussen elke screeninggebeurtenis. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
