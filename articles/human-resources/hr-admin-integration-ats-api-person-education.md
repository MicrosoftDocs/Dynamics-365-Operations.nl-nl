---
title: Opleiding van persoon
description: In dit onderwerp wordt de entiteit Opleiding van persoon voor Dynamics 365 Human Resources beschreven.
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
ms.openlocfilehash: c04a9c973e5a93b716889bdc0bb5f59ff5bbdd7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053750"
---
# <a name="person-education"></a>Opleiding van persoon

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt de entiteit Opleiding van persoon voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmpersoneducationentity

## <a name="description"></a>Beschrijving

Deze entiteit bevat de opleidingshistorie van de persoon die de kandidaat is. De opleiding is gekoppeld aan de persoonsrecord, zodat de opleiding kan worden gekoppeld aan alle andere rollen die voor de persoon zijn gemaakt, naast de kandidaatrecord (werknemer, contractant, enzovoort).

## <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Entiteits-id Opleiding van de persoon**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Alleen-lezen<br>Vereist | Door het systeem gegenereerde unieke id voor de entiteitsrecord van de opleiding van de persoon. |
| **Partijnummer**<br>mshr_partynumber<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | De unieke id van de partijrecord (persoon) voor de kandidaat. |
| **Waarde persoonlijke id**<br>_mshr_fk_person_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity | De door het systeem gegenereerde unieke id voor de persoonlijke record van de kandidaat. |
| **Creditbasis**<br>mshr_creditbasis<br>*mshr_hcmeducationcreditbasis optieset* | Lezen/schrijven<br>Optioneel | De creditbasis van het diploma van de opleiding. |
| **Voltooide credits**<br>mshr_creditscompleted<br>*Decimaal* | Lezen/schrijven<br>Optioneel | Het aantal voltooide credits voor de opleiding. |
| **Behaalde credits**<br>mshr_creditsearned<br>*Decimaal* | Lezen/schrijven<br>Optioneel | Het aantal credits dat voor de opleiding is behaald voor een opleiding die wordt gevolgd. |
| **Benodigde credits**<br>mshr_creditsneeded<br>*Decimaal* | Lezen/schrijven<br>Optioneel | Het aantal credits dat is vereist voor een opleiding die wordt gevolgd. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Een omschrijving van het diploma van de kandidaat. |
| **Opleidingsniveau-id**<br>mshr_educationlevelid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De id van het opleidingsniveau. | 
| **Waarde opleidingsniveau-id**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmeducationdegreeentityid van mshr_hcmeducationdegreeentity entiteit | Door het systeem gegenereerde unieke id voor de record van het diploma van de opleiding. Deze id geeft de diploma's en opleidingsniveaus die voor de organisatie zijn gedefinieerd. |
| **Opleidingsvakgebied-id**<br>mshr_educationdisciplineid<br>*Tekenreeks* | Lezen/schrijven<br>Vereist<br>Refererende sleutel: opleidingsvakgebied | De id van het vakgebied van de opleiding. |
| **Waarde opleidingsvakgebied-id**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmeducationdisciplineentityid van mshr_hcmeducationdisciplineentity | De door het systeem gegenereerde unieke id van het opleidingsvakgebied van de opleidingsrecord. |
| **Minor**<br>mshr_secondaryemphasis<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De minor binnen het behaalde diploma. |
| **Opleidingsinstelling-id**<br>mshr_educationinstitutionid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De id van de opleidingsinstelling waar de opleiding is gevolgd. |
| **Waarde opleidingsinstelling-id**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmeducationinstitutionentityid van mshr_hcmeducationinstitutionentity | Unieke door het systeem gegenereerde id van de opleidingsinstelling. |
| **Begindatum**<br>mshr_startdate<br>*Datum/tijd* | Lezen/schrijven<br>Optioneel | De begindatum van de opleiding voor het behaalde diploma. |
| **Einddatum**<br>mshr_enddate<br>*Datum/tijd* | Lezen/schrijven<br>Vereist | De datum waarop referentie is uitgegeven. |
| **Duur**<br>mshr_duration<br>*Decimaal* | Lezen/schrijven<br>Optioneel | De duur van de tijd van de opleidingsrecord. |
| **Duureenheid**<br>mshr_durationunit<br>*mshr_periodunit optieset* | Lezen/schrijven<br>Optioneel | De tijdseenheid die aan de duur van de opleidingsrecord is gekoppeld. |
| **Gemiddeld eindcijfer**<br>mshr_gradepointaverage<br>*Decimaal* | Lezen/schrijven<br>Optioneel | Het behaalde gemiddelde eindcijfer voor het diploma. |
| **Puntenschaal**<br>mshr_gradescale<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De schaal die wordt gebruikt voor het gemiddelde eindcijfer. |
| **Opmerkingen**<br>mshr_notes<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Notities die worden gebruikt door de werver of de aanstellend manager. |
| **Primair veld**<br>mshr_primaryfield<br>*Tekenreeks* | Alleen-lezen<br>Vereist | Veld dat wordt gebruikt als nog een primaire id van de entiteitsrecord. Combinatie van partijnummer, opleidingsvakgebied-id, opleidingsinstelling-id en opleidingsniveau-id. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor Kandidaten voor aanstelling](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]