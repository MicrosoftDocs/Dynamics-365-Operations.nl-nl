---
title: Verlofaanvraag
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Verlofaanvraag in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0f14c143a59553786fe85284c128cec80905810b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067674"
---
# <a name="leave-request"></a>Verlofaanvraag


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Verlofaanvraag voor Dynamics 365 Human Resources beschreven.

### <a name="description"></a>Beschrijving

Deze entiteit voorziet in informatie over een verlofaanvraag.

Fysieke naam: mshr_essleaverequestentity.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Aanvraag-id**</br>mshr_requestid</br>*Tekenreeks* | Alleen-lezen | De aanvraag-id. |
| **Id verloftype**</br>mshr_leavetypeid</br>*Tekenreeks* | Alleen-lezen | De id van het verloftype. |
| **Datum**</br>mshr_leavedate</br>*Verschil datum en tijd* | Alleen-lezen | De datum van de verlofaanvraag. |
| **Bedrag**</br>mshr_amount</br>*Decimaal* | Alleen-lezen | Het bedrag van de verlofaanvraag. |
| **Type halve dag**</br>mshr_halfdaydefinition</br>*Optieset mshr_LeaveHalfDayDefinition* | Alleen-lezen | Het type verlof van een halve dag. |
| **Opmerking**</br>mshr_comment</br>*Tekenreeks* | Alleen-lezen | Opmerking over de aanvraag. |
| **Status**</br>mshr_status</br>*Optieset mshr_status* | Alleen-lezen | De status van de aanvraag. |
| **Datum**</br>mshr_requestdate</br>*Verschil datum en tijd* | Alleen-lezen | De datum van de aanvraag. |
| **Personeelsnummer**</br>mshr_personnelnumber</br>*Tekenreeks* | Alleen-lezen | Het unieke personeelsnummer van de werknemer. |
| **Redencode-id**</br>mshr_reasoncodeid</br>*Tekenreeks* | Alleen-lezen | De redencode-id. |
| **Id gegevensgebied**</br>mshr_dataareaid</br>*Tekenreeks* | Alleen-lezen | Geeft de rechtspersoon (bedrijf) op. |
| **Primair veld**</br>mshr_primaryfield</br>*GUID* | Alleen-lezen</br>Door systeem gegenereerd | |
| **Entiteit Verloftype**</br>mshr_essleaverequestentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van de verlofaanvraag. |

## <a name="example-query"></a>Voorbeeldquery

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Respons**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
