---
title: Salarisdetails voor posities
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarisdetails voor posities in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2bbb234d2f51391ea65e3d6153d6cee250f3c6dc
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069802"
---
# <a name="payroll-position"></a>Salarispositie


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Salarisposities in Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_payrollpositionentity.

### <a name="description"></a>Beschrijving

Deze entiteit voorziet in positiegerelateerde informatie over een gegeven werknemer.

Fysieke naam: mshr_payrollpositionentity.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Omschrijving |
| --- | --- | --- |
| **Positie-id**</br>mshr_positionid</br>*Tekenreeks* | Alleen-lezen | De id van de positie. |
| **Betalingscyclus-id**</br>mshr_paycycleid</br>*Tekenreeks* | Alleen-lezen | De betalingscyclus die voor de positie is gedefinieerd. |
| **Jaarlijkse normale uren**</br>annualregularhours</br>*Decimaal* | Alleen-lezen | De jaarlijkse normale uren die voor de positie zijn gedefinieerd. |
| **Betaald door rechtspersoon**</br>paidbylegalentity</br>*Tekenreeks* | Alleen-lezen | De rechtspersoon die is gedefinieerd voor de positie en die verantwoordelijk is voor de uitgifte van de betaling. |
| **Geldig tot**</br>validto</br>*Verschil datum en tijd* | Alleen-lezen | De datum tot wanneer de positiedetails geldig zijn. |
| **Geldig vanaf**</br>validfrom</br>*Verschil datum en tijd* | Alleen-lezen | De datum vanaf wanneer de positiedetails geldig zijn. |
| **Primair veld**</br>mshr_primaryfield</br>*Tekenreeks* | Door systeem gegenereerd | Het primaire veld. |
| **Entiteit-id Salarisdetails voor posities**</br>payrollpositiondetailsentityid</br>*GUID* | Vereist</br>Door systeem gegenereerd. | Een door het systeem gegenereerde unieke GUID-waarde (Globally Unique Identifier) om de positie uniek te identificeren. |

## <a name="relations"></a>Relaties

| Eigenschapwaarde | Gerelateerde entiteit | Navigatie-eigenschap | Type verzameling |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Niet van toepassing |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Niet van toepassing |

## <a name="example-query"></a>Voorbeeldquery

**Aanvraag**

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

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
