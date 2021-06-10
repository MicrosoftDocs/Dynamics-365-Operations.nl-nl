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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054687"
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