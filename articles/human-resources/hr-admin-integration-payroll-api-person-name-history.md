---
title: Historie van naam van persoon
description: Dit artikel bevat details en een voorbeeldquery voor de entiteit Naamsgeschiedenis van persoon in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e34b0d7bebd1c4037347161087ff3a4485a58878
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875766"
---
# <a name="person-name-history"></a>Historie van naam van persoon


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Naamsgeschiedenis van persoon in Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Omschrijving

Deze entiteit geeft informatie over de naamsgeschiedenis voor een bepaalde persoon.

> [!IMPORTANT] 
> De velden **Voornaam**, **TweedeNaam**, **Achternaam**, **NaamGeldigVanaf** en **NaamGeldigTot** zijn niet langer beschikbaar voor de entiteit Salarisadministratie van werknemer. Ze zijn verwijderd om ervoor te zorgen dat alleen een gegevensbron met één ingangsdatum deze entiteit ondersteunt.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Omschrijving |
| --- | --- | --- |
| **Voornaam**</br>mshr_firstname</br>*Tekenreeks* | Alleen-lezen | De voornaam. |
| **Voorvoegsel van achternaam**</br>mshr_lastnameprefix</br>*Tekenreeks*) | Alleen-lezen | Het voorvoegsel van de achternaam |
| **Achternaam**</br>mshr_lastname</br>*Tekenreeks*) | Alleen-lezen | De achternaam. |
| **Tweede voornaam**</br>mshr_middlename</br>*Tekenreeks*) | Alleen-lezen | De tweede voornaam. |
| **Geldig tot**</br>mshr_validto</br>*Tekenreeks*) | Alleen-lezen | De datum tot wanneer de naam geldig is. |
| **Partijnummer**</br>mshr_partynumber</br>*Tekenreeks* | Alleen-lezen | Een door de gebruiker leesbare unieke id voor de persoon. |
| **Primair veld**</br>mshr_primaryfield</br>*Tekenreeks* | Alleen-lezen | De unieke id van de record. |
| **Entiteits-id van de naamsgeschioedenis van de persoon**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde unieke GUID-waarde (Globally Unique Identifier) om de record uniek te identificeren. |

## <a name="relations"></a>Relaties

| Eigenschapwaarde | Gerelateerde entiteit | Navigatie-eigenschap | Type verzameling |
| --- | --- | --- | --- |
| Niet van toepassing | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Niet van toepassing | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Voorbeeldquery voor werknemer in salarisadministratie

**Aanvraag**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Respons**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
