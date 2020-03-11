---
title: Entiteiten in Common Data Service
description: Microsoft Dynamics 365 Human Resources maakt gebruik van Common Data Service om uitbreidings- en integratiescenario's in te schakelen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087341"
---
# <a name="common-data-service-entities"></a>Entiteiten in Common Data Service

Microsoft Dynamics 365 Human Resources maakt gebruik van Common Data Service om uitbreidings- en integratiescenario's in te schakelen.

Zie [Wat is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro) voor meer informatie over Common Data Service.

De volgende Human Resources-entiteiten zijn beschikbaar in Common Data Service.

## <a name="benefit-entities"></a>Vergoedingsentiteiten

| Naam | Entiteit |
| --- | --- |
| Frequentie van vergoedingenberekening | cdm_benefitcalculationfrequency |
| Salarisperiode vergoedingsberekeningsfrequentie | cdm_benefitcalculationfrequencypayperiod |
| Berekeningstarief vergoeding | cdm_benefitcalculationrate |
| Details berekeningstarief vergoeding | cdm_benefitcalculationratedetail |
| Vergoedingsoptie | cdm_benefitoption |
| Vergoedingsplan | cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden) |
| Vergoedingstype | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Entiteiten voor bedrijfsprocestaken

| Naam | Entiteit |
| --- | --- |
| Kalender voor bedrijfsprocessen | cdm_businessprocesscalendar |
| Groepstoewijzing van bedrijfsproces | cdm_businessprocessgroupassignment |
| Bibliotheektaakgroep voor bedrijfsproces | cdm_businessprocesslibrarytaskgroup |
| Bedrijfsprocesfase | cdm_businessprocessstage |
| Koptekst van controlelijstsjabloon | cdm_businessprocesstemplateheader |
| Taak voor controlelijstsjabloon | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Entiteiten voor compensatie

| Naam | Entiteit |
| --- | --- |
| Vastecompensatieplan | cdm_compensationfixedplan |
| Compensatieraster | cdm_compensationgrid |
| Compensatieniveau | cdm_compensationlevel |
| Compensatiebetalingsfrequentie | cdm_compensationpayfrequency |
| Instelling van compensatiereferentiepunten | cdm_compensationreferencepointsetup |
| Regel voor instellen van compensatiereferentiepunten | cdm_compensationreferencepointsetupline |
| Compensatieregio | cdm_compensationregion |
| Compensatiestructuur | cdm_compensationstructure |
| Plan voor variabele compensatie | cdm_compensationvariableplan |
| Niveau van plan voor variabele compensatie | cdm_compensationvariableplanlevel |
| Type plan voor variabele compensatie | cdm_compensationvariableplantype |
| Gebeurtenis voor vaste compensatie | cdm_fixedcompensationevent |
| Vestigingsregel | cdm_vestingrule |
| Vaste compensatie medewerker | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Organisatie-entiteiten

| Naam | Entiteit |
| --- | --- |
| Departement | cdm_department |
| Dienstverband | cdm_employment |
| Bedrijf | cdm_company |
| Taak | cdm_job |
| Functiepositie | cdm_jobfunction |
| Taakpositie | cdm_jobposition |
| Positietype | cdm_positiontype |
| Medewerkertoewijzing voor positie | cdm_positionworkerassignmentmap |
| Functietype | cdm_jobtype |
| Taal | cdm_language |

## <a name="leave-and-absence-entities"></a>Entiteiten voor verlof en verzuim

| Naam | Entiteit |
| --- | --- |
| Bank verlaten-transactie | cdm_leavebanktransaction |
| Verlofinschrijving | cdm_leaveenrollment |
| Verlofplan | cdm_leaveplan |
| Verlofaanvraag | cdm_leaverequest |
| Gegevens van verlofaanvraag | cdm_leaverequestdetail |
| Verloftype | cdm_leavetype |
| Redencode voor verloftype | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Entiteiten salarisadministratie

| Naam | Entiteit |
| --- | --- |
| Betalingscyclus | cdm_paycycle |
| Salarisperiode | cdm_payperiod |
| Inkomstencode salaris | cdm_payrollearningcode |
| Bankrekeningvoorschot | cdm_bankaccountdisbursement |
| Belastingregio | cdm_taxregion |

## <a name="worker-entities"></a>Entiteiten medewerker

| Naam | Entiteit |
| --- | --- |
| Medewerker | cdm_worker |
| Adres medewerker | cdm_workeraddress |
| Persoonsgegevens van medewerker | cdm_workerpersonaldetail |
| Persoonlijk identificatienummer medewerker | cdm_workerpersonidentificationnumber |
| Persoonlijk identificatietype medewerker | cdm_workerpersonidentificationtype |
| Werkkalender | cdm_workcalendar |
| Werkkalenderdag | cdm_workcalendarday |
| Feestdag werkkalender |cdm_workcalendarholiday |
| Feestdagregel van werkkalender | cdm_workcalendarholidayline |
| Tijdsinterval werkkalender | cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden) |
| Bankrekening medewerker | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>Entiteiten voor de instelling van medewerkers

| Naam | Entiteit |
| --- | --- |
| Veteraanstatus | cdm_veteranstatus |
| Etnische afkomst | cdm_ethnicorigin |
| Redencode | cdm_reasoncode |
| Instelling die persoonsidentificatie uitgeeft | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Competentie-entiteiten

| Naam | Entiteit |
| --- | --- |
| Vaardigheidstype | cdm_skilltype |

## <a name="entity-relationship-models"></a>Entiteitsrelatiemodellen

### <a name="worker"></a>Medewerker

![Medewerker](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Functie en functiepositie

![Functie en functiepositie](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Vergoedingen

![Vergoedingen](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Compensatie

![Compensatie](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Verlaten

![Verlaten](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Werkkalender

![Werkkalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Zie ook

[Een technologie voor gegevensintegratie kiezen](hr-admin-integration-choose-technology.md)</br>
[Integratie met Common Data Service configureren](hr-admin-integration-common-data-service.md)