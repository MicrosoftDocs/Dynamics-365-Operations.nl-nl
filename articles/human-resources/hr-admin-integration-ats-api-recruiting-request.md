---
title: Wervingsaanvraag
description: In dit onderwerp wordt de entiteit Wervingsaanvraag voor Dynamics 365 Human Resources beschreven.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 572ee0755e331d19b41442e3614effb92db95a92
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125420"
---
# <a name="recruiting-request"></a>Wervingsaanvraag

In dit onderwerp wordt de entiteit Wervingsaanvraag voor Dynamics 365 Human Resources beschreven.

Fysieke naam: mshr_hcmrecruitingrequestentity

### <a name="description"></a>Beschrijving

Beschrijft een aanvraag om personeel voor een functie te werven.

### <a name="json-representation"></a>JSON-weergave

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Eigenschappen

| Eigenschap<br>**Fysieke naam**<br>**_Type_** | Gebruiken | Beschrijving |
| --- | --- | --- |
| **Wervingsaanvraag-id**<br>mshr_recruitingrequestid<br>*Tekenreeks* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Een door de gebruiker leesbare unieke id voor de aanvraag die in de HR-toepassing wordt weergegeven. Nummerreeks. |
| **Entiteits-id Wervingsaanvraag**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Alleen-lezen<br>Vereist<br>Door systeem gegenereerd | Een door het systeem gegenereerde GUID-waarde als unieke id van de wervingsaanvraag. |
| **Id gegevensgebied**<br>mshr_dataareaid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel<br> | Specificeert de rechtspersoon (bedrijf) voor de wervingsaanvraag. |
| **Waarde van id gegevensgebied**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Alleen-lezen<br>Optioneel<br>Refererende sleutel: cdm_companyid van cdm_company entiteit | Door het systeem gegenereerde GUID-waarde die de rechtspersoon (bedrijf) identificeert voor de wervingsaanvraag. |
| **Personeelsnummer van aanstellend manager**<br>mshr_hiringmanagerpersonnelnumber<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het personeelsnummer van de aanstellend manager die aan deze wervingsaanvraag is gekoppeld. |
| **ID-waarde aanstellend manager**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmworkerbaseentityid van de entiteit mshr_hcmworkerbaseentity | Door het systeem gegenereerde GUID-waarde om de manager te identificeren die aan de wervingsaanvraag is gekoppeld. |
| **Nummer van wervende partij**<br>mshr_recruiterpartynumber<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het persoonsnummer (partij) van de werver die voor de aanvraag is geselecteerd. |
| **Id-waarde werver**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_dirpersonentityid van mshr_dirpersonentity entiteit | Door het systeem gegenereerde GUID-waarde om de werver te identificeren die aan de wervingsaanvraag is gekoppeld. |
| **Status**<br>mshr_status<br>*Status van wervingsaanvraag* optieset | Lezen/schrijven<br>Vereist<br> | Geeft de status aan van de wervingsaanvraag. |
| **Beschrijving**<br>mshr_description<br>*Tekenreeks* | Lezen/schrijven<br>Vereist | Omschrijft de aanvraag. |
| **Locatie-id van wervingsaanvraag**<br>mshr_recruitingrequestlocationid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | De door de gebruiker leesbare unieke id van de functielocatie die aan deze aanvraag is gekoppeld. |
| **Waarde wervingslocatie-id**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmrecruitingrequestlocationentityid van de entiteit mshr_hcmrecruitingrequestlocationentity | Door het systeem gegenereerde GUID-waarde om de locatie van de wervingsaanvraag te identificeren die voor de aanvraag is geselecteerd. |
| **Opmerkingen**<br>mshr_comments<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Opmerkingen over de aanvraag voor gebruik door aanstellend managers en wervers. |
| **Taak-ID**<br>mshr_jobid<br>*Tekenreeks* | Eenmaal schrijven<br>Vereist |   De door de gebruiker leesbare unieke id van de functie die wordt gedeeld door alle posities die aan deze aanvraag zijn gekoppeld. |
| **Waarde functie-ID**<br>_mshr_fk_job_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmjobentityid van de entiteit mshr_hcmjobentity | De door het systeem gegenereerde unieke id van de functie die wordt gedeeld door alle posities die aan de wervingsaanvraag zijn gekoppeld. |
| **Titel-id**<br>mshr_titleid<br>*Tekenreeks* | Alleen-lezen<br>Vereist | De door de gebruiker leesbare unieke id van de functietitel die aan deze aanvraag is gekoppeld. |
| **Waarde titel-id**<br>_mshr_fk_title_id_value<br>*GUID* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_hcmtitleid van de entiteit mshr_hcmtitleentity | De door het systeem gegenereerde unieke id voor de titel van de functie die is geselecteerd voor de wervingsaanvraag. |
| **Taakfunctie-id**<br>mshr_jobfunctionid<br>*Tekenreeks* | Alleen-lezen<br>Vereist<br>Refererende sleutel: mshr_jobfunctionid van de entiteit mshr_hcmjobfunctionentity | De door de gebruiker leesbare unieke id van de taakfunctie die aan deze aanvraag is gekoppeld. |
| **Standaard voltijdsequivalent**<br>mshr_defaultfulltimeequivalency<br>*Dubbel* | Alleen-lezen<br>Vereist | De voltijdsequivalente waarde voor de taak, waarbij 1,0 een fulltime werknemer vertegenwoordigt. |
| **Wettelijke taakcategorie**<br>mshr_regulatoryjobcategory<br>*Wettelijke taakcategorie* optieset | Alleen-lezen<br>Optioneel | De EEO-taakcategorie van de taakfunctie die voor de taak is geselecteerd. Geldige waarden in de optieset HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory). |
| **Taaktype-id**<br>mshr_jobtypeid<br>*Tekenreeks* | Alleen-lezen<br>Optioneel | Het type taak dat aan de geselecteerde positie is gekoppeld. De taaktypen zijn door de gebruiker gedefinieerde waarden die beschikbaar zijn in de entiteit mshr_hcmjobtypeentity. |
| **Waarde taaktype-id**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmjobtypeentityid van de entiteit mshr_hcmjobtypenentity | De door het systeem gegenereerde unieke id van het taaktype dat is gekoppeld aan de taak voor de wervingsaanvraag. |
| **Vrijstellingsstatus**<br>mshr_exemptstatus<br>*Taakvrijstellingsstatus* optieset | Alleen-lezen<br>Optioneel | De FLSA-vrijstellingsstatus op basis van het taaktype. |
| **Geschatte begindatum**<br>mshr_estimatedstartdate<br>*Datum* | Lezen/schrijven<br>Vereist | De geschatte datum waarop een kandidaat met werken zou beginnen. |
| **Externe omschrijving**<br>mshr_externaldescription<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Een omschrijving van de taak of positie van de kandidaat. | Lage compensatiedrempel<br>mshr_compensationlowthreshold<br>*Dubbel* | Lezen/schrijven<br>Optioneel | Ondergrens voor het compensatieniveau. |
| **Compensatiecontrolepunt**<br>mshr_compensationcontrolpoint<br>*Dubbel* | Lezen/schrijven<br>Optioneel | Controlepunt voor het compensatieniveau. |
| **Hoge compensatiedrempel**<br>mshr_compensationhighthreshold<br>*Dubbel* | Lezen/schrijven<br>Optioneel | Bovengrens voor het compensatieniveau. |
| **Compensatieniveau**<br>mshr_compensationlevelid<br>*Tekenreeks* | Lezen/schrijven<br>Optioneel | Het compensatieniveau van de taak. Een taak kan meerdere compensatieniveaus hebben. Met dit kenmerk wordt het geselecteerde taakcompensatieniveau voor deze aanvraag aangegeven. |
| **Taakcompensatie-id**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Alleen-lezen<br>Optioneel<br>Refererende sleutel: mshr_hcmjobcompensationentityid van de entiteit mshr_hcmjobcompensationentity | Door het systeem gegenereerde unieke id voor het compensatieniveau dat is gekoppeld aan de taak van de wervingsaanvraag. |

## <a name="see-also"></a>Zie ook

[Integratie-API voor sollicitantenvolgsysteem - Inleiding](hr-admin-integration-ats-api-introduction.md)<br>
[Voorbeeldquery voor wervingsaanvraag](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]