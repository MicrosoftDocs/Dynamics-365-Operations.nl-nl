---
title: Contactpersoon partij
description: In dit onderwerp wordt de entiteit Contactpersoon partij voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fca72cb73ef46a4eeee27d43e22254373a425a36
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067171"
---
# <a name="party-contact"></a>Contactpersoon partij


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Contactpersoon partij voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_dirpartycontactentities

## <a name="description"></a>Beschrijving

Deze entiteit beschrijft de contactgegevens van de kandidaat, waaronder telefoon-, e-mail- en social media-accounts.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Contactpersoon partij**<br>mshr_dirpartycontactentityid<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Door het systeem gegenereerde unieke id voor de entiteitsrecord. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De id van de gekoppelde partijrecord (persoon). |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | De door het systeem gegenereerde unieke id voor de entiteitsrecord van de partij (persoon). |
| **Locatie-ID**<br>mshr_locationid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De locatie-id van de adresrecord. Stel dit in de entiteit mshr_logisticspostaladdresslocationcdsentity in. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De omschrijving van de contactgegevens. |
| **Type**<br>mshr_type<br>*mshr_logisticselectronicaddressmethodtype optieset* | Lezen/schrijven<br>Vereist | Het detailtype van het contact. |
| **Land-/regiocode**<br>mshr_countryregioncode<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het land of de regio van het adres. |
| **Locator**<br>mshr_locator<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De gegevens van de contactpersoon. Als het type bijvoorbeeld **E-mailadres** is, bevat dit veld het e-mailadres van de kandidaat. |
| **Locatorextensie**<br>mshr_locatorextension<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De locatorextensie. Als het type bijvoorbeeld **Telefoon** is, bevat deze eigenschap het toestelnummer. |
| **Is mobiel**<br>mshr_ismobile<br>*mshr_noyes optieset* | Lezen/schrijven<br>Vereist | Geeft aan of het primaire telefoonnummer een mobiel nummer is. |
| **Is chatbericht**<br>mshr_isinstantmessage<br>*mshr_noyes optieset* | Lezen/schrijven<br>Vereist | Geeft aan of de telefoon is ingeschakeld voor chatberichten. |
| **Is primair**<br>mshr_isprimary<br>*mshr_noyes optieset* | Lezen/schrijven<br>Vereist | Bepaalt de primaire contactpersoon van het contacttype. Er mag slechts één primaire record per contacttype zijn. |
| **Is privé**<br>mshr_isprivate<br>*mshr_noyes optieset* | Lezen/schrijven<br>Vereist | Geeft aan of dit adres een privéadres voor de persoon is. |
| **Doel**<br>mshr_purpose<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel/de rol van de contactgegevens. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Veld dat wordt gebruikt als een primaire id van de entiteitsrecord. Combinatie van partijnummer, type, omschrijving en locator. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
