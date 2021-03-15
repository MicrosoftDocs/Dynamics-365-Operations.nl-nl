---
title: Type certificaat
description: In dit onderwerp wordt de entiteit Type certificaat voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125708"
---
# <a name="certificate-type"></a>Type certificaat

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