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
ms.openlocfilehash: c0b70411e6535b22d698545438dcb0b16935e731
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559578"
---
# <a name="payroll-position-job"></a>Salarispositiefunctie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Salarispositiefunctie voor Dynamics 365 Human Resources beschreven.

### <a name="description"></a>Beschrijving

Deze entiteit geeft de relatie tussen positie en een taak voor een bepaald vast compensatieplan.

Fysieke naam: mshr_payrollpositionjobentity.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Omschrijving |
| --- | --- | --- |
| **Positie-id**</br>mshr_positionid</br>*Tekenreeks* | Alleen-lezen | De id van de positie. |
| **Geldig vanaf**</br>mshr_validto</br>*Verschil datum en tijd* | Alleen-lezen | De datum vanaf wanneer de positie- en functierelatie geldig zijn. |
| **Geldig tot**</br>mshr_validto</br>*Verschil datum en tijd* | Alleen-lezen | De datum tot wanneer de positie- en functierelatie geldig is. |
| **Taak-ID**</br>mshr_jobid</br>*Tekenreeks* | Alleen-lezen | De id van de functie. |
| **Primair veld**</br>mshr_primaryfield</br>*Tekenreeks* | Door systeem gegenereerd | Het primaire veld. |
| **Entiteit-id Salarispositiefunctie**</br>mshr_payrollpositionjobentityid</br>*GUID* | Door systeem gegenereerd. | Een door het systeem gegenereerde unieke GUID-waarde (Globally Unique Identifier) om de taak uniek te identificeren. |

## <a name="relations"></a>Relaties

| Eigenschapwaarde | Gerelateerde entiteit | Navigatie-eigenschap | Type verzameling |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Niet van toepassing |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Voorbeeldquery

**Aanvraag**

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
