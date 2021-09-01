---
title: Werknemer in salarisadministratie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Werknemer in salarisadministratie in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 20e74e97f98d0bc0fd454d54cbf969d4f1b46c7c98b2949b0ed8cfe671312dd2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768186"
---
# <a name="payroll-employee"></a>Werknemer in salarisadministratie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Werknemer in salarisadministratie voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_payrollemployeeentity.

### <a name="description"></a>Beschrijving

Deze entiteit geeft informatie over de werknemer. U moet de [parameters voor salarisintegratie instellen](hr-admin-integration-payroll-api-parameters.md) voordat u deze entiteit kunt gebruiken.

>[!IMPORTANT] 
>De velden **Voornaam**, **TweedeNaam**, **Achternaam**, **NaamGeldigVanaf** en **NaamGeldigTot** zijn niet langer beschikbaar voor deze entiteit. Hierdoor wordt gewaarborgd dat er slechts één ingangsdatum voor de gegevensbron is die een back-up maakt van deze entiteit.
>Deze velden zijn beschikbaar in de **DirPersonNameHistoricalEntity**, die is vrijgegeven in Platform update 43. Er bestaat een OData-relatie van **PayrollEmployeeEntity** naar **DirPersonNameHistoricalEntity** in het veld **Persoon**. 

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Personeelsnummer**<br>mshr_personnelnumber<br>*Tekenreeks* | Alleen-lezen | Het unieke personeelsnummer van de werknemer. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Door systeem gegenereerd |  |
| **Rechtspersoon-ID**<br>mshr_legalentityID<br>*Tekenreeks* | Alleen-lezen | Geeft de rechtspersoon (bedrijf) op. |
| **Geslacht**<br>mshr_gender<br>[mshr_hcmpersongender optieset](hr-admin-integration-payroll-api-gender.md) | Alleen-lezen | Gender van de werknemer. |
| **Entiteit-id werknemer in salarisadministratie**<br>mshr_payrollemployeeentityid<br>*GUID* | Vereist<br>Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van de werknemer. |
| **Begindatum dienstverband**<br>mshr_employmentstartdate<br>*Verschil datum en tijd* | Alleen-lezen | De begindatum van het dienstverband van de werknemer. |
| **Identificatietype-id**<br>mshr_identificationtypeid<br>*Tekenreeks* |Alleen-lezen | Het identificatietype dat voor de werknemer is gedefinieerd. |
| **Einddatum dienstverband**<br>mshr_employmentenddate<br>*Verschil datum en tijd* | Alleen-lezen |De einddatum van het dienstverband van de werknemer.  |
| **Id gegevensgebied**<br>mshr_dataareaid_id<br>*GUID* | Alleen-lezen <br>Door systeem gegenereerd | Door het systeem gegenereerde GUID-waarde die de rechtspersoon (het bedrijf) identificeert. |
| **Geldig tot**<br>mshr_namevalidto<br>*Verschil datum en tijd* |  Alleen-lezen | De datum tot wanneer de gegevens van de werknemer geldig zijn. |
| **Geboortedatum**<br>mshr_birthdate<br>*Verschil datum en tijd* | Alleen-lezen | De geboortedatum van de werknemer. |
| **Identificatienummer tot**<br>mshr_identificationnumber<br>*Tekenreeks* | Alleen-lezen |Het identificatienummer dat voor de werknemer is gedefinieerd.  |

## <a name="example-query-for-payroll-employee"></a>Voorbeeldquery voor werknemer in salarisadministratie

**Aanvragen**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
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
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
    "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
    "_mshr_dataareaid_id_value": null
}
```
## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
