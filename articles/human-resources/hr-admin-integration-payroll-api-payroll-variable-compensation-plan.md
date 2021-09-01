---
title: Variabel compensatieplan in salarisadministratie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Variabel compensatieplan in salarisadministratie in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96a644bf129de6dd3f78098bcb6415d17058d6decbd7d904a99bb6f050d3a9e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730437"
---
# <a name="payroll-variable-compensation-plan"></a>Variabel compensatieplan in salarisadministratie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Variabel compensatieplan in salarisadministratie voor Dynamics 365 Human Resources beschreven.

### <a name="description"></a>Beschrijving

Deze entiteit voorziet in het variabele compensatieplan dat is toegewezen voor een bepaalde functie van een werknemer.

Fysieke naam: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Personeelsnummer**</br>mshr_personnelnumber</br>*Tekenreeks* | Alleen-lezen</br>Vereist |Het unieke personeelsnummer van de werknemer.  |
| **Toekenningsdatum**</br>mshr_awarddate</br>*Verschil datum en tijd* | Alleen-lezen</br>Vereist | Datum van de toekenning. |
| **Toekenningstype**</br>mshr_awardtype</br>*[Optieset mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | Alleen-lezen</br>Vereist | Het type van de toekenning dat is gedefinieerd voor het variabele compensatieplan. |
| **Valuta**</br>mshr_unitcurrencycode</br>*Tekenreeks* | Alleen-lezen </br>Vereist |De valuta die voor het variabele compensatieplan is gedefinieerd.   |
| **Vaste compensatieplan-id**</br>mshr_fixedplanid</br>*Tekenreeks* | Alleen-lezen | Het vaste compensatieplan dat als basis voor het berekenen van de toekenning wordt gebruikt. |
| **Eenheidswaarde**</br>mshr_awardamount</br>*Decimaal* | Alleen-lezen | De waarde van de eenheid |
| **Procestype**</br>mshr_processtype</br>*[Optieset mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | Alleen-lezen | Het procestype. |
| **Type variabele compensatieplan**</br>Tekenreeks</br>*mshr_typeid* | Alleen-lezen | Het type variabel compensatieplan. |
| **Id variabel compensatieplan**</br>Tekenreeks</br>*mshr_planid* | Alleen-lezen | De id van het variabele compensatieplan. |
| **Primair veld**</br>mshr_primaryfield</br>*GUID* | Alleen-lezen</br>Door systeem gegenereerd. | |
| **Werknemer-id**</br>mshr_fk_employee_id_value</br>*GUID* | Alleen-lezen</br>Vereist</br>Refererende sleutel: mshr_Employee_id van de entiteit mshr_payrollemployeeentity  | Werknemer-id. |
| **Entiteit Variabel compensatieplan in salarisadministratie**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Vereist</br>Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van het compensatieplan. |


## <a name="example-query"></a>Voorbeeldquery

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**Respons**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
