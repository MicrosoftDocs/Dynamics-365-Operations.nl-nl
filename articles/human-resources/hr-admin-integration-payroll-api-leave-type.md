---
title: Verloftype
description: Dit artikel bevat details en een voorbeeldquery voor de entiteit Verloftype in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893781"
---
# <a name="leave-type"></a>Verloftype


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Verloftype voor Dynamics 365 Human Resources beschreven.

### <a name="description"></a>Description

Deze entiteit voorziet in informatie over een gegeven verloftype.

Fysieke naam: mshr_essleavetypeentity.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Id verloftype**</br>mshr_leavetypeid</br>*Tekenreeks* | Alleen-lezen | De id van het verloftype. |
| **Beschrijving**</br>mshr_description</br>*Tekenreeks* | Alleen-lezen | Een beschrijving van het verloftype. |
| **Categorie**</br>mshr_category</br>*Optieset mshr_LeaveTypeCategory* | Alleen-lezen | De categorie van het verloftype. |
| **Redencode vereist**</br>mshr_isreasoncoderequired</br>*Optieset mshr_NoYes* | Alleen-lezen | Definieert of er een redencode is vereist voor het verloftype. |
| **Verlofeenheid**</br>mshr_leaveamountunit</br>*Optieset mshr_LeaveAmountUnit* | Alleen-lezen | De eenheid van dit verloftype. |
| **Halve dag inschakelen**</br>mshr_enablehalfdaydefinition</br>*Optieset mshr_NoYes* | Definieert of halve dag is ingeschakeld voor het verloftype. |
| **Id gegevensgebied**</br>mshr_dataareaid_id</br>*Tekenreeks* | Alleen-lezen | Geeft de rechtspersoon (bedrijf) op. |
| **Entiteit Verloftype**</br>mshr_essleavetypeentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van het verloftype. |

## <a name="example-query"></a>Voorbeeldquery

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Respons**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
