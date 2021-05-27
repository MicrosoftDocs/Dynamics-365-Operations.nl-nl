---
title: Adres medewerker salarisadministratie
description: Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Adres medewerker salarisadministratie in Dynamics 365 Human Resources.
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020700"
---
# <a name="payroll-worker-address"></a>Adres medewerker salarisadministratie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dit onderwerp bevat details en een voorbeeldquery voor de entiteit Adres medewerker salarisadministratie in Dynamics 365 Human Resources.

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Plaats**<br>mshr_city<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De plaats voor het adres   |
| **Personeelsnummer**<br>mshr_personnelnumber<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Het unieke personeelsnummer van de werknemer.  |
| **Land/regio**<br>mshr_countryregionid<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Het land of de regio voor het adres.  |
| **Geldig vanaf**<br>mshr_postaladdressvalidfrom<br>*Verschil datum en tijd* | Alleen-lezen <br>Vereist | De datum vanaf wanneer het adres geldig is. |
| **Gewerkt op adres**<br>mshr_isworkedinaddressbr>*Int32* | Alleen-lezen<br>Vereist | Geeft aan of dit het adres is waar de werknemer werkt. |
| **Land/regio**<br>mshr_county<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De land of de regio voor het adres  |
| **Id medewerker salarisadministratie**<br>mshr_payrollworkeraddressentityid<br>*GUID* | Vereist<br>Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van het adres.  |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist |  |
| **Adres**<br>mshr_street<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De straatnaam voor het adres |
| **Geldig tot**<br>mshr_postaladdressvalidto<br>*Verschil datum en tijd* | Alleen-lezen <br>Vereist | De datum tot wanneer het adres geldig is.  |
| **Locatie-ID**<br>mshr_locationidbr>*Tekenreeks* | Alleen-lezen <br>Vereist | Het id voor het adres.  |
| **Postcode**<br>mshr_zipcode<br>*Tekenreeks* | Alleen-lezen <br>Vereist |Het identificatienummer dat voor de werknemer is gedefinieerd.  |
| **Gewoond op adres**<br>mshr_islivedinaddressbr>*Tekenreeks* | Alleen-lezen<br>Vereist | Geeft aan of dit het adres is waar de werknemer woont. |
| **Staat/provincie**<br>mshr_state<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De staat/provincie voor het adres  |

## <a name="example-query"></a>Voorbeeldquery

**Aanvragen**

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
