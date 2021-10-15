---
title: Historie van naam van persoon
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Naamsgeschiedenis van persoon in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 418047a0643ee29b89763dbe2b030753f405b575
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559636"
---
# <a name="person-name-history"></a>Historie van naam van persoon

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Naamsgeschiedenis van persoon in Dynamics 365 Human Resources beschreven.

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
