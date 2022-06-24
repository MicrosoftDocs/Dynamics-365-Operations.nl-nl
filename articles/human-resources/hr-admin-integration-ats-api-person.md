---
title: Persoon
description: In dit artikel wordt de entiteit Persoon voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: 49d9b5e1a1297c9528bfa82d0e8307bad3b2d1cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864107"
---
# <a name="person"></a>Persoon


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit artikel wordt de entiteit Persoon voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_dirpersonentity

### <a name="description"></a>Beschrijving

Deze entiteit levert de persoonlijke gegevens van de persoon die de kandidaat is.

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Persoon**<br>mshr_dirpersonentityid<br>*GUID* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Een door het systeem gegenereerde unieke id voor de entiteitsrecord. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Een door de gebruiker leesbare unieke id voor de persoon.  |
| **Naam**<br>mshr_name<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De veldwaarde is een samenvoeging van Voornaam, Tweede voornaam, Voorvoegsel bij achternaam en Achternaam in de volgorde die is gedefinieerd in het veld **Naamreeks weergeven als**. |
| **Naamalias**<br>mshr_namealias<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Een naamalias dat mogelijk voor de persoon wordt opgegeven. |
| **Bekend als**<br>mshr_knownas<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Een naam die kan worden gebruikt voor de persoon als deze meestal bekend staat met een andere naam. |
| **Taal-id**<br>mshr_languageid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De taal-id van de primaire taal van de persoon, zoals deze is gedefinieerd in de ISO 639-1-indeling. |
| **Adresboeken**<br>mshr_addressbooks<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Adresboek waaraan de persoon kan worden toegewezen. Adresboeken die voor de organisatie zijn ingesteld, worden vermeld in de entiteit mshr_diraddressbooksentity. |
| **Jubileumdag**<br>mshr_anniversaryday<br>*Int* | Lezen/schrijven<br>Optioneel | De dag van de jubileumdatum van de persoon. |
| **Jubileummaand**<br>mshr_anniversarymonth<br>*mshr_monthsofyear optieset* | Lezen/schrijven<br>Optioneel | De maand van de jubileumdatum van de persoon. |
| **Jubileumjaar**<br>mshr_anniversaryyear<br>*Int* | Lezen/schrijven<br>Optioneel | Het jaar van de jubileumdatum van de persoon. |
| **Geboortedag**<br>mshr_birthday<br>*Int* | Lezen/schrijven<br>Optioneel | De dag van de geboortedatum van de persoon. |
| **Geboortemaand**<br>mshr_birthmonth<br>*mshr_monthsofyear optieset* | Lezen/schrijven<br>Optioneel | De maand van de geboortedatum van de persoon. |
| **Geboortejaar**<br>mshr_birthyear<br>*Int* | Lezen/schrijven<br>Optioneel | Het jaar van de geboortedatum van de persoon. |
| **Namen van kinderen**<br>mshr_childrennames<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Tekenreeks voor de namen van de kinderen van de persoon. Er is geen vereist scheidingsteken. |
| **Geslacht**<br>mshr_gender<br>*mshr_hcmpersongender optieset* | Lezen/schrijven<br>Optioneel | Het gender van de persoon. |
| **Hobby's**<br>mshr_hobbies<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De hobby's van de persoon. |
| **Initialen**<br>mshr_initials<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De initialen van de naam van de persoon. |
| **Burgerlijke staat**<br>mshr_maritalstatus<br>*mshr_hcmpersonmaritalstatus optieset* | Lezen/schrijven<br>Optioneel | De burgerlijke staat van de persoon. |
| **Fonetische voornaam**<br>mshr_phoneticfirstname<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De fonetische uitspraak van de voornaam van de persoon. |
| **Fonetische achternaam**<br>mshr_phoneticlastname<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De fonetische uitspraak van de achternaam van de persoon. |
| **Fonetische tweede voornaam**<br>mshr_phoneticmiddlename<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De fonetische uitspraak van de achternaam van de persoon. |
| **Persoonlijk achtervoegsel**<br>mshr_personalsuffix<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het persoonlijke achtervoegsel van de persoon. Geldige waarden in de entiteit mshr_dirnameaffixentity waarbij mshr_type Achtervoegsel is (200000001). |
| **Aanspreektitel**<br>mshr_personaltitle<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Een persoonlijke titel voor de persoon. Geldige waarden in de entiteit mshr_dirnameaffixentity waarbij mshr_type Titel is (200000000).
| **Professioneel achtervoegsel**<br>mshr_professionalsuffix<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Een professioneel achtervoegsel. |
| **Professionele titel**<br>mshr_professionaltitle<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Een professionele titel. |
| **Volledig primair adres**<br>mshr_fullprimaryaddress<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het volledige primaire adres van de persoon, een samenvoeging van de primaire adresvelden. |
| **Adres - Plaats**<br>mshr_addresscity<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De plaats van het primaire adres van de persoon. Stel deze in de entiteit mshr_logisticsaddresscityentity in. |
| **Adres Land Regio**<br>mshr_addresscountryregionid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het land/de regio van het primaire adres van de persoon. Geldige waarden in de entiteit mshr_logisticsaddresscountryregionentity. |
| **ISO-code Adres Land Regio**<br>mshr_addresscountryregionisocode<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De ISO-code van het land/de regio van het primaire adres van de persoon. |
| **Adres Provincie**<br>mshr_addresscounty<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De provincie van het primaire adres van de persoon. Stel deze in de entiteit mshr_logisticsaddresscountyentity in. |
| **Adres districtnaam**<br>mshr_addressdistrictname<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het district van het primaire adres van de persoon. Stel deze in de entiteit mshr_logisticsaddressdistrictentity in. |
| **Adres breedtegraad**<br>mshr_addresslatitude<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De breedtegraad van het primaire adres van de persoon. |
| **Adres locatie-id**<br>mshr_addresslocationid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De unieke id voor de locatie van het primaire adres van de persoon. Geldige waarden in de entiteit mshr_logisticspostaladdresslocationcdsentity. |
| **Adres locatierollen**<br>mshr_addresslocationroles<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De locatierol van het primaire adres van de persoon. Stel deze in de entiteit mshr_logisticslocationrolecdsentity in. |
| **Adres lengtegraad**<br>mshr_addresslongitude<br>*Tekenreeks* |  Lezen/schrijven<br>Optioneel | De lengtegraad van het primaire adres van de persoon. |
| **Adres staat**<br>mshr_addressstate<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De staat van het primaire adres van de persoon. Stel deze in de entiteit nmshr_logisticsaddressstateentity in. |
| **Adres straatnaam**<br>mshr_addressstreet<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De straatnaam van het primaire adres van de persoon. |
| **Adres geldig vanaf**<br>mshr_addressvalidfrom<br>*Datum* | Lezen/schrijven<br>Optioneel | De datum waarop het primaire adres van de persoon ingaat. |
| **Adres geldig tot**<br>mshr_addressvalidto<br>*Datum* | Lezen/schrijven<br>Optioneel | De datum waarop het primaire adres van de persoon niet meer geldig is. |
| **Adres postcode**<br>mshr_addresszipcode<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De postcode van het primaire adres van de persoon. Stel deze in de entiteit mshr_logisticsaddresspostalcodeentity in. |
| **Adres is privé**<br>mshr_addressisprivate<br>*mshr_noyes optieset* | Lezen/schrijven<br>Optioneel | Bepaalt of het primaire adres van de persoon wordt gedeeld met anderen in de organisatie. |
| **Adresomschrijving**<br>mshr_addressdescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De omschrijving van het primaire adres van de persoon. |
| **Primair e-mailadres van contactpersoon**<br>mshr_primarycontactemail<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | He primaire e-mailadres van de persoon. |
| **Omschrijving primair e-mailadres van contactpersoon**<br>mshr_primarycontactemaildescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Een omschrijving die wordt opgegeven voor het primaire e-mailadres. |
| **Primair e-mailadres van contactpersoon is IM**<br>mshr_primarycontactemailisim<br>*mshr_noyes optieset* | Lezen/schrijven<br>Optioneel | Bepaalt of het primaire e-mailadres beschikbaar is voor chatberichten. |
| **Doel van primair e-mailadres van contactpersoon**<br>mshr_primarycontactemailpurpose<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel voor het primaire e-mailadres. Stel deze in de entiteit mshr_logisticslocationroleentity in. |
| **Primaire fax van contactpersoon**<br>mshr_primarycontactfax<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Primair faxnummer. |
| **Omschrijving primaire fax van contactpersoon**<br>mshr_primarycontactfaxdescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Omschrijving die wordt opgegeven voor het primaire faxnummer. |
| **Toestelnummer primaire fax van contactpersoon**<br>mshr_primarycontactfaxextension<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het toestelnummer van het primaire faxnummer. |
| **Doel van primair fax van contactpersoon**<br>mshr_primarycontactfaxpurpose<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel voor het primaire faxnummer. Stel deze in de entiteit mshr_logisticslocationroleentity in.
| **Primair telefoonnummer van contactpersoon**<br>mshr_primarycontactphone<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Eerste telefoonnummer. |
| **Omschrijving primair telefoonnummer van contactpersoon**<br>mshr_primarycontactphonedescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Omschrijving die wordt opgegeven voor het primaire telefoonnummer. |
| **Toestelnummer primaire telefoon van contactpersoon**<br>mshr_primarycontactphoneextension<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het toestelnummer van het primaire telefoonnummer. |
| **Primair telefoonnummer van contactpersoon is mobiel**<br>mshr_primarycontactphoneismobile<br>*mshr_noyes optieset* | Lezen/schrijven<br>Optioneel | Bepaalt of het primaire telefoonnummer een mobiele telefoon is. |
| **Doel van primair telefoonnummer van contactpersoon**<br>mshr_primarycontactphonepurpose<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel voor het primaire telefoonnummer. Stel deze in de entiteit mshr_logisticslocationroleentity in. |
| **Primair telexnummer van contactpersoon**<br>mshr_primarycontacttelex<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Primair telexnummer. |
| **Omschrijving primair telexnummer van contactpersoon**<br>mshr_primarycontacttelexdescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Omschrijving die wordt opgegeven voor het primaire telexnummer van de persoon. |
| **Doel van primaire telex van contactpersoon**<br>mshr_primarycontacttelexpurpose<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel voor het primaire telexnummer van de persoon. Stel deze in de entiteit mshr_logisticslocationroleentity in. |
| **Primaire URL voor contactpersoon**<br>mshr_primarycontacturl<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De primaire URL. |
| **Omschrijving primaire URL van contactpersoon**<br>mshr_primarycontacturldescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De omschrijving die wordt opgegeven voor de primaire URL van de persoon. |
| **Doel van primaire URL van contactpersoon**<br>mshr_primarycontacturldescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel voor de primaire URL van de persoon. Stel deze in de entiteit mshr_logisticslocationroleentity in. |
| **Primaire Facebook van contactpersoon**<br>mshr_primarycontactfacebook<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Primair Facebook-account. Geïdentificeerd met Gebruikers-id. |
| **Omschrijving primaire Facebook van contactpersoon**<br>mshr_primarycontactfacebookdescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De omschrijving die wordt opgegeven voor het primaire Facebook-account van de persoon. |
| **Primair Facebook-account van contactpersoon is privé**<br>mshr_primarycontactfacebookisprivate<br>*mshr_noyes optieset* | Lezen/schrijven<br>Optioneel | Bepaalt of het primaire Facebook-account zichtbaar is voor andere gebruikers. |
| **Doel van primair Facebook-account van contactpersoon**<br>mshr_primarycontactfacebookpurpose<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel voor het primaire Facebook-account van de persoon. Stel deze in de entiteit mshr_logisticslocationroleentity in. |
| **Primair LinkedIn-account van contactpersoon**<br>mshr_primarycontactlinkedin<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Primair LinkedIn-count. Geïdentificeerd met gebruikersnaam. |
| **Omschrijving primair LinkedIn-account van contactpersoon**<br>mshr_primarycontactlinkedindescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De omschrijving die wordt opgegeven voor het primaire LinkedIn-account van de persoon. |
| **Primair LinkedIn-account van contactpersoon is privé**<br>mshr_primarycontactlinkedinisprivate<br>*mshr_noyes optieset* | Lezen/schrijven<br>Optioneel | Bepaalt of de gegevens van het primaire LinkedIn-account van de persoon worden gedeeld met andere gebruikers. |
| **Doel van primair LinkedIn-account van contactpersoon**<br>mshr_primarycontactlinkedinpurpose<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel voor het primaire LinkedIn-account van de persoon. Stel deze in de entiteit mshr_logisticslocationroleentity in. |
| **Primaire Twitter van contactpersoon**<br>mshr_primarycontacttwitter<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het primaire Twitter-account van de persoon. Geïdentificeerd met @gebruikersnaam. |
| **Omschrijving primair Twitter-account van contactpersoon**<br>mshr_primarycontacttwitterdescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De omschrijving die wordt opgegeven voor het primaire Twitter-account van de persoon. |
| **Primair Twitter-account van contactpersoon is privé**<br>mshr_primarycontacttwitterisprivate<br>*mshr_noyes optieset* | Lezen/schrijven<br>Optioneel | Bepaalt of de gegevens van het primaire Twitter-account van de persoon worden gedeeld met andere gebruikers. |
| **Doel van primair Twitter-account van contactpersoon**<br>mshr_primarycontacttwitterpurpose<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het doel voor het primaire Twitter-account van de persoon. Stel deze in de entiteit mshr_logisticslocationroleentity in. |
| **Type partij**<br>mshr_partytype<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het partijtype van de persoon. Is altijd **Persoon** voor kandidaten. |
| **Naamreeks weergeven als**<br>mshr_namesequencedisplayas<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De reeks waarin de naameigenschappen van de persoon worden samenvoegd met de eigenschapwaarde Naam (mshr_name). |
| **Voornaam**<br>mshr_firstname<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De voornaam van de persoon. |
| **Tweede naam**<br>mshr_middlename<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De tweede voornaam van de persoon. |
| **Voorvoegsel van achternaam**<br>mshr_lastnameprefix<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het voorvoegsel van de achternaam van de persoon. |
| **Achternaam**<br>mshr_lastname<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De achternaam van de persoon. |
| **Elektronische locatie-id**<br>mshr_electroniclocationid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De id van de elektronische locatie van de persoon. |
| **Tijdzone van adres**<br>mshr_addresstimezone<br>*Int* | Lezen/schrijven<br>Optioneel | De tijdzone van het primaire adres van de persoon. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
