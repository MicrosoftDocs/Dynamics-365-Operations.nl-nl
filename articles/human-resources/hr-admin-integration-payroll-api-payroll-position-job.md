---
title: Salarispositiefunctie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarispositiefunctie in Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 842c459acd8b5e1a8b6074243b3afa18dc6a13c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314232"
---
# <a name="payroll-position-job"></a>Salarispositiefunctie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Salarispositiefunctie voor Dynamics 365 Human Resources beschreven.

### <a name="description"></a>Beschrijving

Deze entiteit geeft de relatie tussen positie en een taak voor een bepaald vast compensatieplan.

Fysieke naam: mshr_payrollpositionjobentity.

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Taak-ID**<br>mshr_jobid<br>*Tekenreeks* | Alleen-lezen<br>Vereist |De id van de functie. |
| **Geldig vanaf**<br>mshr_validto<br>*Verschil datum en tijd* | Alleen-lezen <br>Vereist | Datum waarop de positie- en functierelatie geldig wordt. |
| **Geldig tot**<br>mshr_validto<br>*Verschil datum en tijd* | Alleen-lezen <br>Vereist | Datum tot wanneer de positie- en functierelatie geldig is.  |
| **Positie-id**<br>mshr_positionid<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De id van de positie. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Vereist<br>Door systeem gegenereerd |  |
| **Waarde positiefunctie-id**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_PayrollPositionJobEntity van de mshr_payrollpositionjobentity |Id van de taak die aan de geselecteerde positie is gekoppeld.|
| **Waarde vaste compensatieplan-id**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_FixedCompPlan_id van mshr_payrollfixedcompensationplanentity  | Id van het vaste compensatieplan dat aan de positie is gekoppeld. |
| **Entiteit-id Salarispositiefunctie**<br>mshr_payrollpositionjobentityid<br>*GUID* | Vereist<br>Door systeem gegenereerd. | Een door het systeem gegenereerde GUID-waarde als unieke id van de functie.  |

## <a name="example-query"></a>Voorbeeldquery

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Respons**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
