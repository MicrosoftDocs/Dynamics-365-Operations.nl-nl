---
title: Salarisadministratie - plan voor vaste compensatie
description: Dit artikel bevat details en een voorbeeldquery voor de entiteit Vast compensatieplan in salarisadministratie in Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: 83fa8aeb38cc44191242cf029022939cefb22cb8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909841"
---
# <a name="payroll-fixed-compensation-plan"></a>Salarisadministratie - plan voor vaste compensatie


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Vast compensatieplan in salarisadministratie voor Dynamics 365 Human Resources beschreven.

### <a name="description"></a>Beschrijving

Deze entiteit voorziet in het vaste compensatieplan dat is toegewezen voor een bepaalde functie van een werknemer.

Fysieke naam: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Plan-id**</br>mshr_planid</br>*Tekenreeks* | Alleen-lezen | Geeft het compensatieplan aan  |
| **Personeelsnummer**</br>mshr_personnelnumber</br>*Tekenreeks* | Alleen-lezen | Het unieke personeelsnummer van de werknemer. |
| **Loontarief**</br>mshr_payrate</br>*Decimaal* | Alleen-lezen | Salaristarief dat is gedefinieerd in de vastecompensatieregeling. |
| **Positie-id**</br>mshr_positionid</br>*Tekenreeks* | Alleen-lezen | De positie-id die is gekoppeld aan de werknemer en de inschrijving voor het vaste compensatieplan. |
| **Geldig vanaf**</br>mshr_validfrom</br>*Verschil datum en tijd* |  Alleen-lezen | De datum vanaf wanneer de vaste compensatie voor de werknemer geldig is.  |
| **Geldig tot**</br>mshr_validto</br>*Verschil datum en tijd* | Alleen-lezen | De datum tot wanneer de vaste compensatie voor de werknemer geldig is. |
| **Betalingsfrequentie**</br>mshr_payfrequency</br>*Tekenreeks* | Alleen-lezen | De id van de [compensatiebetalingsfrequentie](hr-admin-integration-payroll-api-compensation-pay-frequency.md) voor het opgegeven betalingstarief. |
| **Valuta**</br>mshr_currency</br>*Tekenreeks* | Alleen-lezen | De voor het vaste compensatieplan gedefinieerde valuta. |
| **Entiteit Vast compensatieplan in salarisadministratie**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van het compensatieplan. |

## <a name="relations"></a>Relaties

|Eigenschapwaarde | Gerelateerde entiteit | Navigatie-eigenschap | Type verzameling |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_waarde | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Voorbeeldquery

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Respons**

```json
{
    "mshr_planid": "GradeC",
    "mshr_personnelnumber": "000041",
    "mshr_payrate": 75200,
    "mshr_positionid": "000276",
    "mshr_validfrom": "2011-04-05T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_payfrequency": "Annual",
    "mshr_currency": "USD",
    "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": null
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
