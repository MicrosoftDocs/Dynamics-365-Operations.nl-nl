---
title: Verlofsaldo
description: Dit artikel bevat details en een voorbeeldquery voor de entiteit Verlofsaldo in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4792c316b8b7af3e86b097029eb281af4a10d113
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899696"
---
# <a name="leave-balance"></a>Verlofsaldo


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Verlofsaldo voor Dynamics 365 Human Resources beschreven.

### <a name="description"></a>Description

Deze entiteit voorziet in het verlofsaldo per verloftype voor een bepaalde werknemer.

Fysieke naam: mshr_essleavebalanceentities.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Personeelsnummer**</br>mshr_personnelnumber</br>*Tekenreeks* | Alleen-lezen | Het unieke personeelsnummer van de werknemer. |
| **Huidig saldo**</br>mshr_balanceavailable</br>*Decimaal* | Alleen-lezen | Het huidige saldo van de werknemer. |
| **Type**</br>mshr_balanceavailable</br>*Tekenreeks* | Alleen-lezen | De id van het verloftype. |
| **Toerekeningstarief**</br>mshr_accrualratedescription</br> | Alleen-lezen | Het toerekeningstarief. |
| **Laatste transporthoeveelheid**</br>mshr_lastcarryforwardamount</br>*Decimaal* | Alleen-lezen | Het bedrag voor Laatste transport. |
| **Dit jaar opgenomen**</br>mshr_takenthisyear</br>*Decimaal* | Alleen-lezen | De hoeveelheid verlof die dit jaar is opgenomen. |
| **Totaal voor dit jaar**</br>mshr_totalthisyear</br>*Decimaal* | Alleen-lezen | Het totaalbedrag voor dit jaar. |
| **Id gegevensgebied**</br>mshr_dataareaid_id</br>*Tekenreeks* | Alleen-lezen | Geeft de rechtspersoon (bedrijf) op. |
| **Primair veld**</br>mshr_primaryfield</br>*GUID* | Alleen-lezen</br>Door systeem gegenereerd | |
| **Id verloftype**</br>_mshr_fk_leavetype_id_value</br>*GUID* | Alleen-lezen</br>Refererende sleutel: mshr_essleavetypeentityid van entiteit mshr_essleavetypeentity  | Id verloftype |
| **Entiteit Verlofsaldo**</br>mshr_essleavebalanceentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van het saldo. |

## <a name="example-query"></a>Voorbeeldquery

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Respons**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
