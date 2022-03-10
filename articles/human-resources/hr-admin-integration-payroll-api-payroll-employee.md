---
title: Werknemer salarisadministratie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Werknemer in salarisadministratie in Dynamics 365 Human Resources.
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
ms.openlocfilehash: e853a8a5730d397f253c8ce3a330794594dfd907
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068479"
---
# <a name="payroll-employee"></a>Werknemer in salarisadministratie


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Werknemer in salarisadministratie voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_payrollemployeeentity.

### <a name="description"></a>Beschrijving

Deze entiteit geeft informatie over de werknemer. U moet de [parameters voor salarisintegratie instellen](hr-admin-integration-payroll-api-parameters.md) voordat u deze entiteit kunt gebruiken.

>[!IMPORTANT] 
>De velden **Voornaam**, **TweedeNaam**, **Achternaam**, **NaamGeldigVanaf** en **NaamGeldigTot** zijn niet langer beschikbaar voor deze entiteit. Hierdoor wordt gewaarborgd dat er slechts één ingangsdatum voor de gegevensbron is die een back-up maakt van deze entiteit.
>Deze velden zijn beschikbaar in de **DirPersonNameHistoricalEntity**, die is vrijgegeven in Platform update 43. Er bestaat een OData-relatie van **PayrollEmployeeEntity** naar **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Rechtspersoon-ID**</br>mshr_legalentityid</br>*Tekenreeks* | Alleen-lezen | Geeft de rechtspersoon (bedrijf) op. |
| **Personeelsnummer**</br>mshr_personnelnumber</br>*Tekenreeks* | Alleen-lezen | Het unieke personeelsnummer van de werknemer. |
| **Begindatum dienstverband**</br>mshr_employmentstartdate</br>*Verschil datum en tijd* | Alleen-lezen | De begindatum van het dienstverband van de werknemer. |
| **Einddatum dienstverband**</br>mshr_employmentenddate</br>*Verschil datum en tijd* | Alleen-lezen |De einddatum van het dienstverband van de werknemer.  |
| **Geboortedatum**</br>mshr_birthdate</br>*Verschil datum en tijd* | Alleen-lezen | De geboortedatum van de werknemer. |
| **Geslacht**</br>mshr_gender</br>[mshr_hcmpersongender optieset](hr-admin-integration-payroll-api-gender.md) | Alleen-lezen | Gender van de werknemer. |
| **Aanstellingstype**</br>mshr_employmenttype</br>[optieset mshr_hcmemploymenttype](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Alleen-lezen | Type aanstelling. |
| **Identificatietype-id**</br>mshr_identificationtypeid</br>*Tekenreeks* |Alleen-lezen | Het identificatietype dat voor de werknemer is gedefinieerd. |
| **Identificatienummer tot**</br>mshr_identificationnumber</br>*Tekenreeks* | Alleen-lezen |Het identificatienummer dat voor de werknemer is gedefinieerd. |
| **Gereed voor betaling**</br>mshr_readytopay</br>[mshr_noyes optieset](hr-admin-integration-payroll-api-no-yes.md) | Alleen-lezen | Geeft aan of de werknemer is gemarkeerd als gereed voor betaling. |
| **Entiteit-id werknemer in salarisadministratie**</br>mshr_payrollemployeeentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde unieke GUID-waarde (Globally Unique Identifier) om de werknemer uniek te identificeren. |

## <a name="relations"></a>Relaties

|Eigenschapwaarde | Gerelateerde entiteit | Navigatie-eigenschap | Type verzameling |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_werknemer_id_waarde | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Voorbeeldquery voor werknemer in salarisadministratie

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Respons**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
