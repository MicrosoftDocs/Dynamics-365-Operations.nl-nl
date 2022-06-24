---
title: Variabel compensatieplan in salarisadministratie
description: Dit artikel bevat details en een voorbeeldquery voor de entiteit Variabel compensatieplan in salarisadministratie in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c6190084c3f1ce15d6a4ab8f13843a5da801dd3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868125"
---
# <a name="payroll-variable-compensation-plan"></a>Variabel compensatieplan in salarisadministratie


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Variabel compensatieplan in salarisadministratie voor Dynamics 365 Human Resources beschreven.

### <a name="description"></a>Beschrijving

Deze entiteit voorziet in het variabele compensatieplan dat is toegewezen voor een bepaalde functie van een werknemer.

Fysieke naam: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Personeelsnummer**</br>mshr_personnelnumber</br>*Tekenreeks* | Alleen-lezen | Het unieke personeelsnummer van de werknemer.  |
| **Toekenningsdatum**</br>mshr_awarddate</br>*Verschil datum en tijd* | Alleen-lezen | Datum van de toekenning. |
| **Toekenningstype**</br>mshr_awardtype</br>*[Optieset mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | Alleen-lezen | Het type van de toekenning dat is gedefinieerd voor het variabele compensatieplan. |
| **Valuta**</br>mshr_unitcurrencycode</br>*Tekenreeks* | Alleen-lezen |De valuta die voor het variabele compensatieplan is gedefinieerd.   |
| **Vaste compensatieplan-id**</br>mshr_fixedplanid</br>*Tekenreeks* | Alleen-lezen | Het vaste compensatieplan dat als basis voor het berekenen van de toekenning wordt gebruikt. |
| **Eenheidswaarde**</br>mshr_awardamount</br>*Decimaal* | Alleen-lezen | De waarde van de eenheid |
| **Procestype**</br>mshr_processtype</br>*[Optieset mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | Alleen-lezen | Het procestype. |
| **Type variabele compensatieplan**</br>Tekenreeks</br>*mshr_typeid* | Alleen-lezen | Het type variabel compensatieplan. |
| **Id variabel compensatieplan**</br>Tekenreeks</br>*mshr_planid* | Alleen-lezen | De id van het variabele compensatieplan. |
| **Aantal eenheden**</br>Decimaal</br>*mshr_numberofunits* | Alleen-lezen | Het aantal eenheden van de beloning. |
| **Primair veld**</br>mshr_primaryfield</br>*GUID* | Alleen-lezen</br>Door systeem gegenereerd. | |
| **Entiteit Variabel compensatieplan in salarisadministratie**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van het compensatieplan. |

## <a name="relations"></a>Relaties 

|Eigenschapwaarde | Gerelateerde entiteit | Navigatie-eigenschap | Type verzameling |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Voorbeeldquery

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Respons**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
