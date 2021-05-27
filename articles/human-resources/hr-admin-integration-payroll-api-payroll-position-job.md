---
title: Salarispositiefunctie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Salarispositiefunctie in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 9444a36f5ddf92bd41008c83ec77ab7ff5191fa3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019341"
---
# <a name="payroll-position-job"></a>Salarispositiefunctie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Relatie van salarispositiefunctie in Dynamics 365 Human Resources.

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

