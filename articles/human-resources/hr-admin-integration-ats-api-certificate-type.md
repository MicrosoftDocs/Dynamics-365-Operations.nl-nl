---
title: Type certificaat
description: In dit onderwerp wordt de entiteit Type certificaat voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: cc8f49be9af3f95ba182e1e0f1b288334a959ec40315b319a73feff3dbb3fdc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771558"
---
# <a name="certificate-type"></a>Type certificaat

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Type certificaat voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmcertificatetypeentity

## <a name="description"></a>Beschrijving

Deze entiteit definieert de lijst met typen professionele certificaten die in Human Resources zijn ingesteld. De entiteit is niet specifiek voor een rechtspersoon (bedrijf).

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Type certificaat**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Alleen-lezen<br>Vereist 
Door systeem gegenereerd | Unieke primaire id voor het certificaattype. |
| **Type certificaat**<br>mshr_certificatetype<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Unieke door de gebruiker leesbare id voor het certificaattype. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Omschrijving van het certificaattype. |
| **Verlenging vereisen**<br>mshr_requirerenewal<br>*mshr_noyes optieset* | Lezen/schrijven<br>Optioneel | Geeft aan of verlenging is vereist voor het certificaat. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]