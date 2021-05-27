---
title: Salarisdetails voor posities
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarisdetails voor posities in Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019317"
---
# <a name="payroll-position"></a>Salarispositie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarisdetails voor posities in Dynamics 365 Human Resources.

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Jaarlijkse normale uren**<br>annualregularhours<br>*Decimaal* | Alleen-lezen<br>Vereist | Jaarlijkse normale uren die voor de positie zijn gedefinieerd.  |
| **Entiteit-id Salarisdetails voor posities**<br>payrollpositiondetailsentityid<br>*GUID* | Vereist<br>Door systeem gegenereerd. | Een door het systeem gegenereerde GUID-waarde als unieke id van de positie.  |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Vereist<br>Door systeem gegenereerd |  |
| **Waarde positiefunctie-id**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_PayrollPositionJobEntity van de mshr_payrollpositionjobentity |Id van de taak die aan de geselecteerde positie is gekoppeld.|
| **Waarde vaste compensatieplan-id**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_FixedCompPlan_id van mshr_payrollfixedcompensationplanentity  | Id van het vaste compensatieplan dat aan de positie is gekoppeld. |
| **Betalingscyclus-id**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De salariscyclus die voor de positie is gedefinieerd. |
| **Betaald door rechtspersoon**<br>paidbylegalentity<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De rechtspersoon die is gedefinieerd in de positie die verantwoordelijk is voor de uitgifte van de betaling. |
| **Positie-id**<br>mshr_positionid<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De id van de positie. |
| **Geldig tot**<br>validto<br>*Verschil datum en tijd* | Alleen-lezen<br>Vereist |De datum waarop de positiedetails geldig worden.  |
| **Geldig vanaf**<br>validfrom<br>*Verschil datum en tijd* | Alleen-lezen<br>Vereist |De datum tot wanneer de positiedetails geldig zijn.  |

**Query**

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Respons**

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
