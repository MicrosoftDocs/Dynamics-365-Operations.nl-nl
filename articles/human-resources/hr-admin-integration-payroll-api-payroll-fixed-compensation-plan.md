---
title: Vast compensatieplan in salarisadministratie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Vast compensatieplan in salarisadministratie in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059083"
---
# <a name="payroll-fixed-compensation-plan"></a>Vast compensatieplan in salarisadministratie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Vast compensatieplan in salarisadministratie in Dynamics 365 Human Resources.

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Werknemer-id**<br>mshr_fk_employee_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_Employee_id van de entiteit mshr_payrollemployeeentity  | Werknemer-id |
| **Loontarief**<br>mshr_payrate<br>*Decimaal* | Alleen-lezen<br>Vereist | Salaristarief dat is gedefinieerd in de vastecompensatieregeling. |
| **Plan-id**<br>mshr_planid<br>*Tekenreeks* | Alleen-lezen<br>Vereist |Geeft het compensatieplan aan  |
| **Geldig vanaf**<br>mshr_validfrom<br>*Verschil datum en tijd* |  Alleen-lezen<br>Vereist |De datum vanaf wanneer de vaste compensatie voor de werknemer geldig is.  |
| **Entiteit Vast compensatieplan in salarisadministratie**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Vereist<br>Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van het compensatieplan. |
| **Betalingsfrequentie**<br>mshr_payfrequency<br>*Tekenreeks* | Alleen-lezen<br>Vereist |De frequentie waarmee de werknemer wordt betaald.  |
| **Geldig tot**<br>mshr_validto<br>*Verschil datum en tijd* | Alleen-lezen <br>Vereist | De datum tot wanneer de vaste compensatie voor de werknemer geldig is. |
| **Positie-id**<br>mshr_positionid<br>*Tekenreeks* | Alleen-lezen <br>Vereist | De positie-id die is gekoppeld aan de werknemer en de inschrijving voor het vaste compensatieplan. |
| **Valuta**<br>mshr_currency<br>*Tekenreeks* | Alleen-lezen <br>Vereist |De valuta die voor het vastecompensatieplan is gedefinieerd   |
| **Personeelsnummer**<br>mshr_personnelnumber<br>*Tekenreeks* | Alleen-lezen<br>Vereist |Het unieke personeelsnummer van de werknemer.  |

**Query**

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
