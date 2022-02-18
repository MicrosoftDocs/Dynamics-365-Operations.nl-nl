---
title: Adres medewerker salarisadministratie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Adres medewerker salarisadministratie in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 70e42cbf657a28327699d927731edd36de7c4a64
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069752"
---
# <a name="payroll-worker-address"></a>Adres medewerker salarisadministratie


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Adres medewerker salarisadministratie voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_payrollworkeraddressentity.

### <a name="description"></a>Beschrijving

Deze entiteit voorziet in de salarisplaats en de salariswerklocatie voor een bepaalde werknemer.

## <a name="properties"></a>Eigenschappen

| Eigenschap</br>**Fysieke naam**</br>**_Type_** | Gebruiken | Omschrijving |
| --- | --- | --- |
| **Personeelsnummer**</br>mshr_personnelnumber</br>*Tekenreeks* | Alleen-lezen | Het unieke personeelsnummer van de werknemer. |
| **Locatie-ID**</br>mshr_locationidbr>*Tekenreeks* | Alleen-lezen | Het id voor het adres. |
| **Gewoond op adres**</br>mshr_islivedinaddressbr </br> *[Optieset mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Alleen-lezen | Een waarde die aangeeft of het adres het adres is waar de werknemer woont. |
| **Gewerkt op adres** </br> mshr_isworkedinaddressbr </br>*[Optieset mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Alleen-lezen | Een waarde die aangeeft of het adres het adres is waar de werknemer werkt. |
| **Land/regio**</br>mshr_countryregionid</br>*Tekenreeks* | Alleen-lezen</br>Vereist | Het land of de regio die voor het adres is gedefinieerd. |
| **Postcode**</br>mshr_zipcode<br>*Tekenreeks* | Alleen-lezen | Het identificatienummer dat voor de werknemer is gedefinieerd. |
| **Straat**</br>mshr_street</br>*Tekenreeks* | Alleen-lezen | De straatnaam die voor het adres is gedefinieerd. |
| **Plaats**</br>mshr_city</br>*Tekenreeks* | Alleen-lezen | De plaats die voor het adres is gedefinieerd. |
| **Staat/provincie**</br>mshr_state</br>*Tekenreeks* | Alleen-lezen | De staat of de provincie die voor het adres is gedefinieerd. |
| **District**</br>mshr_county</br>*Tekenreeks* | Alleen-lezen | De graafschap die voor het adres is gedefinieerd. |
| **Geldig vanaf**</br>mshr_postaladdressvalidfrom</br>*Verschil datum en tijd* | Alleen-lezen | De datum vanaf wanneer het adres geldig is. |
| **Geldig tot**</br>mshr_postaladdressvalidto</br>*Verschil datum en tijd* | Alleen-lezen | De datum tot wanneer het adres geldig is. |
| **Primair veld**</br>mshr_primaryfield</br>*Tekenreeks* | Alleen-lezen | Het primaire veld. |
| **Id medewerker salarisadministratie**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Door systeem gegenereerd | Een door het systeem gegenereerde unieke GUID-waarde (Globally Unique Identifier) om het adres uniek te identificeren. |

## <a name="relations"></a>Relaties

| Eigenschapwaarde | Gerelateerde entiteit | Navigatie-eigenschap | Type verzameling |
| --- | --- | --- | --- |
| _mshr_fk_werknemer_id_waarde | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

## <a name="example-query"></a>Voorbeeldquery

**Aanvraag**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Respons**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
