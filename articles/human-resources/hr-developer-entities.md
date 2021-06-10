---
title: Dataverse-tabellen
description: Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054351"
---
# <a name="dataverse-tables"></a>Dataverse-tabellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.

> [!NOTE]
> Human Resources-entiteiten komen overeen met Dataverse-tabellen. Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

De volgende Dataverse-entiteiten zijn beschikbaar op basis van Human Resource-entiteiten.

## <a name="benefit-tables"></a>Tabellen voor vergoedingen

| Naam | Tabel |
| --- | --- |
| Frequentie van vergoedingenberekening | cdm_benefitcalculationfrequency |
| Salarisperiode vergoedingsberekeningsfrequentie | cdm_benefitcalculationfrequencypayperiod |
| Berekeningstarief vergoeding | cdm_benefitcalculationrate |
| Details berekeningstarief vergoeding | cdm_benefitcalculationratedetail |
| Vergoedingsoptie | cdm_benefitoption |
| Vergoedingsplan | cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden) |
| Vergoedingstype | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Tabellen voor bedrijfsprocestaken

| Naam | Tabel |
| --- | --- |
| Kalender voor bedrijfsprocessen | cdm_businessprocesscalendar |
| Groepstoewijzing van bedrijfsproces | cdm_businessprocessgroupassignment |
| Bibliotheektaakgroep voor bedrijfsproces | cdm_businessprocesslibrarytaskgroup |
| Bedrijfsprocesfase | cdm_businessprocessstage |
| Koptekst van controlelijstsjabloon | cdm_businessprocesstemplateheader |
| Taak voor controlelijstsjabloon | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Tabellen voor compensatie

| Naam | Tabel |
| --- | --- |
| Vast compensatieplan | cdm_compensationfixedplan |
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
| Vaste compensatie van medewerker | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Tabellen voor de organisatie

| Naam | Tabel |
| --- | --- |
| Departement | cdm_department |
| Dienstverband | cdm_employment |
| Bedrijf | cdm_company |
| Taak | cdm_job |
| Functiepositie | cdm_jobfunction |
| Taakpositie | cdm_jobposition |
| Positietype | cdm_positiontype |
| Medewerkertoewijzing voor positie | cdm_positionworkerassignmentmap |
| Dimensie van taakpositie | cdm_jobpositiondimension|
| Functietype | cdm_jobtype |
| Taal | cdm_language |
| Titel | cdm_title |

> [!NOTE]
> Financiële dimensies voor **Positietype**, **Medewerkertoewijzing voor positie** en **Dienstverband** bieden integratie in één richting naar Dataverse. Updates van financiële dimensies kunnen momenteel niet van Dataverse naar Human Resources worden gesynchroniseerd. 

## <a name="leave-and-absence-tables"></a>Tabellen voor verlof en verzuim

| Naam | Tabel |
| --- | --- |
| Verlofbanktransactie | cdm_leavebanktransaction |
| Verlofinschrijving | cdm_leaveenrollment |
| Verlofplan | cdm_leaveplan |
| Verlofaanvraag | cdm_leaverequest |
| Gegevens van verlofaanvraag | cdm_leaverequestdetail |
| Verloftype | cdm_leavetype |
| Redencode voor verloftype | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Tabellen voor salarisadministratie

| Naam | Tabel |
| --- | --- |
| Betalingscyclus | cdm_paycycle |
| Salarisperiode | cdm_payperiod |
| Salarisinkomstencode | cdm_payrollearningcode |
| Bankrekeningvoorschot | cdm_bankaccountdisbursement |
| Belastingregio | cdm_taxregion |

## <a name="worker-tables"></a>Tabellen voor werknemers

| Naam | Tabel |
| --- | --- |
| Werknemer | cdm_worker |
| Medewerkeradres | cdm_workeraddress |
| Persoonsgegevens van medewerker | cdm_workerpersonaldetail |
| Persoonlijk identificatienummer medewerker | cdm_workerpersonidentificationnumber |
| Persoonlijk identificatietype medewerker | cdm_workerpersonidentificationtype |
| Werkkalender | cdm_workcalendar |
| Werkkalenderdag | cdm_workcalendarday |
| Feestdag werkkalender |cdm_workcalendarholiday |
| Feestdagregel van werkkalender | cdm_workcalendarholidayline |
| Tijdsinterval werkkalender | cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden) |
| Bankrekening van medewerker | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>Tabellen voor werknemerinstellingen

| Naam | Tabel |
| --- | --- |
| Veteraanstatus | cdm_veteranstatus |
| Etnische afkomst | cdm_ethnicorigin |
| Redencode | cdm_reasoncode |
| Uitgevende instantie voor persoonsidentificatie | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Tabellen voor competenties

| Naam | Tabel |
| --- | --- |
| Vaardigheidstype | cdm_skilltype |

## <a name="table-relationship-models"></a>Tabelrelatiemodellen

### <a name="worker"></a>Werknemer

![Werknemer](./media/HCMCommon-worker-entity-diagram.png)

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

[Een technologie voor gegevensintegratie kiezen](hr-admin-integration-choose-technology.md)<br>
[Integratie met Dataverse configureren](hr-admin-integration-common-data-service.md)<br>
[Virtuele Dataverse-entiteiten configureren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Veelgestelde vragen over virtuele tabellen voor Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologiewijzigingen](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]