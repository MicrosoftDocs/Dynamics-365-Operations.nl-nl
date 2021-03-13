---
title: Screeningtypen
description: In dit onderwerp wordt de entiteit Screeningtypen voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126165"
---
# <a name="screening-types"></a>Screeningtypen

In dit onderwerp wordt de entiteit Screeningtypen voor Dynamics 365 Human Resources beschreven.

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
