---
title: Kandidaten voor aanstelling
description: In dit onderwerp wordt de entiteit Kandidaten voor aanstelling voor Dynamics 365 Human Resources beschreven.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f0ddf7bd403c926b231f9e010280083d1638b3ad
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795040"
---
# <a name="candidate-to-hire"></a>Kandidaten voor aanstelling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Kandidaten voor aanstelling voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmcandidatetohireentity

## <a name="description"></a>Beschrijving

Deze entiteit levert kandidaatdetails die worden gebruikt om een werknemer te maken in Dynamics 365 Human Resources. Deze wordt gebruikt om alle kandidaatrecords te lezen en interne en externe kandidaatrecords te maken, waardoor u persoonlijke gegevens voor de nieuwe kandidaat kunt maken.

Wanneer u een externe kandidaatrecord maakt die een nieuwe persoonrecord in het systeem wordt, moet u geen partijnummer (persoon) definiëren dat u een nieuwe kandidaatrecord wilt plaatsen. De nieuwe entiteitsrecord van de persoon wordt gemaakt met de nieuwe kandidaatrecord.

Wanneer u een interne kandidaatrecord maakt (een kandidaat voor de functie die reeds een werknemersrecord bij het bedrijf heeft), definieer dan het partijnummer (persoon) van de reeds bestaande persoon voor de eigenschap mshr_partynumber op de kandidaatrecord in plaats van persoonlijke informatie te definiëren (zoals naam, gender of geboortedatum) die gebruikt zou worden om een nieuwe persoonrecord te maken.

## <a name="json-representation"></a>JSON-weergave

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Kandidaten voor aanstelling**<br>mshr_hcmcandidatetohireentityid<br>Guid | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Een door het systeem gegenereerde unieke id voor de entiteitsrecord. |
| **Kandidaat-id**<br>mshr_candidateid<br>Tekenreeks | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Een unieke id voor de entiteit. |
| **Partijnummer**<br>mshr_partynumber<br>Tekenreeks | Alleen-lezen<br>Vereist | Het partijnummer (persoon) van de persoonrecord van de kandidaat. |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>Guid | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_direpersonentity | De door het systeem gegenereerde unieke id voor de partijrecord (persoon) van de kandidaat. |
| **Type partij**<br>mshr_partytype<br>mshr_dirpartytype optieset | Alleen-lezen<br>Vereist | Het partijtype van de record, zoals gedefinieerd in mshr_dirpartytype optieset. Voor deze entiteit is het type altijd 'Persoon'. |
| **Wervingsaanvraag-id**<br>mshr_recruitingrequestid<br>Tekenreeks | Eenmaal schrijven<br>Optioneel | Verwijzingen naar de wervingsaanvraag die deze kandidaat vervult. |
| **Waarde wervingsaanvraag-id**<br>_mshr_fk_recruitingrequest_id_value<br>Guid | Lezen/schrijven<br>Optioneel<br>Refererende sleutel: mshr_hcmrecruitingrequestentityid van mshr_hcmrecruitingrequestentity | De door het systeem gegenereerde unieke id voor de wervingsaanvraag die de kandidaat vervult. |
| **Positie-id**<br>mshr_positionid<br>Tekenreeks | Lezen/schrijven<br>Optioneel | De id van de positie waarvoor de kandidaat in aanmerking komt. |
| **Waarde positie-id**<br>_mshr_fk_position_if_value<br>Guid | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmpositionv2entityid van de entiteit mshr_2entity | Door het systeem gegenereerde id van de positie waarvoor de kandidaat in aanmerking komt. |
| **Voornaam**<br>mshr_firstname<br>Tekenreeks | Lezen/schrijven<br>Vereist | Voornaam van de kandidaat. |
| **Tweede naam**<br>mshr_middlename<br>Tekenreeks | Lezen/schrijven<br>Optioneel | De tweede voornaam van de kandidaat. |
| **Voorvoegsel van achternaam**<br>mshr_lastnameprefix<br>Tekenreeks | Lezen/schrijven<br>Optioneel | Voorvoegsel van de achternaam van de kandidaat. |
| **Achternaam**<br>mshr_lastname<br>Tekenreeks | Lezen/schrijven<br>Optioneel | Achternaam van de kandidaat. |
| **Geslacht**<br>mshr_gender<br>mshr_hcmpersongender optieset | Lezen/schrijven<br>Optioneel | Het gender van de kandidaat. |
| **Geboortedatum**<br>mshr_birthdate<br>Datetime | Lezen/schrijven<br>Optioneel | De geboortedatum van de kandidaat. |
| **Landcode voor staatsburgerschap**<br>mshr_citizenshipcountrycode<br>Tekenreeks | Lezen/schrijven<br>Optioneel | Specificeert het land waar de kandidaat staatsburger is. Geldige landcodes staan in mshr_logisticaddresscountryregionentity. |
| **Veteranenstatus-id**<br>mshr_veteranstatusid<br>Tekenreeks | Lezen/schrijven<br>Optioneel | Geeft de veteranenstatus van de kandidaat aan. |
| **Waarde veteranenstatus-id**<br>_mshr_fk_veteranstatus_id_value<br>Guid | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmveteranstatusentityid van mshr_hcmveteranstatusentity | Door het systeem gegenereerde unieke id voor de entiteitsrecord van de veteranenstatus van de persoon. |
| **Begindatum militaire dienst**<br>mshr_militaryservicestartdate<br>Datetime | Lezen/schrijven<br>Optioneel | De begindatum van de militaire dienst van de kandidaat. |
| **Einddatum militaire dienst**<br>mshr_militaryserviceenddate<br>Datetime | Lezen/schrijven<br>Optioneel | De einddatum van de militaire dienst van de kandidaat. |
| **Is oorlogsveteraan met handicap**<br>mshr_isdisabledveteran<br>mshr_noyes optieset | Lezen/schrijven<br>Optioneel | Geeft aan of de kandidaat de status gehandicapte veteraan heeft. |
| **Beschikbaarheidsdatum**<br>mshr_availabilitydate<br>Datetime | Lezen/schrijven<br>Optioneel | De vroegste datum waarop de kandidaat beschikbaar zou zijn voor werk. |
| **Is bereid te verhuizen**<br>mshr_iswillingtorelocate<br>mshr_noyes optieset | Lezen/schrijven<br>Optioneel | Geeft aan of de kandidaat bereid is te verhuizen voor de positie. |
| **Opmerkingen**<br>mshr_comments<br>Tekenreeks | Lezen/schrijven<br>Optioneel | Opmerkingen die worden gebruikt door de werver of de aanstellende manager. |
| **Resultaat sollicitatie-integratie**<br>mshr_applcantintegrationresult<br>mshr_applicantintegrationresult optieset | Lezen/schrijven<br>Vereist | De status van de kandidaat in het wervingsproces met betrekking tot de integratie. |
| **Redencode-id Niet aangenomen**<br>mshr_donothirereasoncodeid<br>Tekenreeks | Lezen/schrijven<br>Optioneel | Een optioneel opgegeven redencode wanneer de status (resultaat van sollicitatie-integratie) is ingesteld op 'Niet aangenomen'. |
| **Waarde redencode-id**<br>_mshr_fk_reasoncode_id_value<br>Guid | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmreasoncodeentityid van de entiteit mshr_hcmreasoncodeentity | Door het systeem gegenereerde unieke id voor de redencode **Niet aangenomen**. |
| **Id gegevensgebied**<br>mshr_dataareaid<br>Tekenreeks | Lezen/schrijven<br>Optioneel |  Geeft de rechtspersoon (bedrijf) op. |
| **Waarde van id gegevensgebied**<br>_mshr_dataareaid_id_value<br>Guid | Alleen-lezen<br>Optioneel<br>Refererende sleutel: cdm_companyid van cdm_company entiteit | Door het systeem gegenereerde GUID-waarde die de rechtspersoon (het bedrijf) identificeert. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]