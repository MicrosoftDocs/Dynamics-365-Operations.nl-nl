---
title: Dataverse-tabellen
description: Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838577"
---
# <a name="dataverse-tables"></a>Dataverse-tabellen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources maakt gebruik van Dataverse om uitbreidings- en integratiescenario's in te schakelen.

> [!NOTE]
> Human Resources-entiteiten komen overeen met Dataverse-tabellen. Voor meer informatie over Dataverse (voorheen Common Data Service) en bijgewerkte terminologie, zie [Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

De volgende Dataverse-entiteiten zijn beschikbaar op basis van Human Resource-entiteiten.

Zie [Problemen zoeken in Lifecycle Services (LCS)](/dev-itpro/lifecycle-services/issue-search-lcs) voor meer informatie over de bekende problemen.

## <a name="benefit-tables"></a>Tabellen voor vergoedingen

| Name | Tabel | Bekende problemen  | Status |
| --- | --- |    --------|----------  |
| Frequentie van vergoedingenberekening | cdm_benefitcalculationfrequency |     |     |
| Salarisperiode vergoedingsberekeningsfrequentie | cdm_benefitcalculationfrequencypayperiod |     |     |
| Berekeningstarief vergoeding | cdm_benefitcalculationrate |    |     |
| Details berekeningstarief vergoeding | cdm_benefitcalculationratedetail |753225 | Opgelost  |
| Vergoedingsoptie | cdm_benefitoption |    |     |
| Vergoedingsplan | cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden) |    |     |
| Vergoedingstype | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>Tabellen voor bedrijfsprocestaken

| Name | Tabel |Bekende problemen  | Status |
| --- | --- |   --------|----------   |
| Kalender voor bedrijfsprocessen | cdm_businessprocesscalendar | 751867 | Opgelost |
| Groepstoewijzing van bedrijfsproces | cdm_businessprocessgroupassignment | 751869  751863 | Actief|
| Bibliotheektaakgroep voor bedrijfsproces | cdm_businessprocesslibrarytaskgroup |751866 | Dicht |
| Bedrijfsprocesfase | cdm_businessprocessstage |      |     |
| Koptekst van controlelijstsjabloon | cdm_businessprocesstemplateheader |     |     |
| Taak voor controlelijstsjabloon | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>Tabellen voor compensatie

| Name | Tabel |Bekende problemen  | Status |
| --- | --- | ----------      | -------    |
| Vast compensatieplan | cdm_compensationfixedplan |754453 | Dicht |
| Compensatieraster | cdm_compensationgrid |             |     |
| Compensatieniveau | cdm_compensationlevel |           |     |
| Compensatiebetalingsfrequentie | cdm_compensationpayfrequency |                  |     |
| Instelling van compensatiereferentiepunten | cdm_compensationreferencepointsetup |               |     |
| Regel voor instellen van compensatiereferentiepunten | cdm_compensationreferencepointsetupline |             |     |
| Compensatieregio | cdm_compensationregion |                   |     |
| Compensatiestructuur | cdm_compensationstructure |    754456        | Dicht    |
| Plan voor variabele compensatie | cdm_compensationvariableplan |               |     |
| Niveau van plan voor variabele compensatie | cdm_compensationvariableplanlevel |                |     |
| Type plan voor variabele compensatie | cdm_compensationvariableplantype |               |     |
| Gebeurtenis voor vaste compensatie | cdm_fixedcompensationevent |               |     |
| Vestigingsregel | cdm_vestingrule |              |     |
| Vaste compensatie van medewerker | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>Tabellen voor de organisatie

| Name | Tabel |Bekende problemen  | Status |
| --- | --- | ----------      | -------    |
| Afdeling | cdm_department |  752194    | Dicht    |
| Dienstverband | cdm_employment | 762414  |  Dicht  |
| Bedrijf | cdm_company |  |     |
| Taak | cdm_job |  |     |
| Functiepositie | cdm_jobfunction |        |     |
| Taakpositie | cdm_jobposition | 752214      | Dicht    |
| Positietype | cdm_positiontype |            |     |
| Medewerkertoewijzing voor positie | cdm_positionworkerassignmentmap | 752224    |  Dicht   |
| Dimensie van taakpositie | cdm_jobpositiondimension|       |     |
| Functietype | cdm_jobtype |      |     |
| Taal | cdm_language |        |     |
| Titel | cdm_title |       |     |

> [!NOTE]
> Financiële dimensies voor **Positietype**, **Medewerkertoewijzing voor positie** en **Dienstverband** bieden integratie in één richting naar Dataverse. Updates van financiële dimensies kunnen momenteel niet van Dataverse naar Human Resources worden gesynchroniseerd. 

## <a name="leave-and-absence-tables"></a>Tabellen voor verlof en verzuim

| Name | Tabel | Bekende problemen  | Status |
| --- | --- |   ----------      | -------    |
| Verlofbanktransactie | cdm_leavebanktransaction |  752252    |    Opgelost |
| Verlofinschrijving | cdm_leaveenrollment |  752934    |Dicht     |
| Verlofplan | cdm_leaveplan |   752232   |   Dicht  |
| Verlofaanvraag | cdm_leaverequest | 753207     | Dicht    |
| Gegevens van verlofaanvraag | cdm_leaverequestdetail | 753207     |   Dicht  |
| Verloftype | cdm_leavetype |      |     |
| Redencode voor verloftype | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>De integratie van twee keer wegschrijven met behulp van Dataverse-tabellen voor verlof en verzuim is alleen beschikbaar wanneer de functie **Meerdere verloftypen configureren voor één verlofplan** is ingeschakeld in Microsoft Dynamics 365 Finance via **Functiebeheer**. 

## <a name="payroll-tables"></a>Tabellen voor salarisadministratie

| Name | Tabel |Bekende problemen  | Status |
| --- | --- |  ----------      | -------    |
| Betalingscyclus | cdm_paycycle |    |     |
| Salarisperiode | cdm_payperiod |          |     |
| Salarisinkomstencode | cdm_payrollearningcode |   754458        |   Dicht  |
| Bankrekeningvoorschot | cdm_bankaccountdisbursement |    751904     |   Dicht  |
| Belastingregio | cdm_taxregion |          |     |

## <a name="worker-tables"></a>Tabellen voor werknemers

| Name | Tabel |Bekende problemen  | Status |
| --- | --- |----------      | -------    |
| Werknemer | cdm_worker |    751906    |    Dicht |
| Medewerkeradres | cdm_workeraddress |   754465     |Dicht     |
| Persoonsgegevens van medewerker | cdm_workerpersonaldetail |   751906     |   Dicht  |
| Persoonlijk identificatienummer medewerker | cdm_workerpersonidentificationnumber |  766704      |   Dicht  |
| Persoonlijk identificatietype medewerker | cdm_workerpersonidentificationtype |        |     |
| Werkkalender | cdm_workcalendar |        |     |
| Werkkalenderdag | cdm_workcalendarday |        |     |
| Feestdag werkkalender |cdm_workcalendarholiday |        |     |
| Feestdagregel van werkkalender | cdm_workcalendarholidayline |        |     |
| Tijdsinterval werkkalender | cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden) |        |     |
| Bankrekening van medewerker | cdm_workerbankaccount |        |     |

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

![Medewerker.](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Functie en functiepositie

![Functie en functiepositie.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Voordelen

![Voordelen.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Compensatie

![Compensatie.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Verlof

![Verlof.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Werkkalender

![Werkkalender.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Zie ook

[Een technologie voor gegevensintegratie kiezen](hr-admin-integration-choose-technology.md)<br>
[Integratie met Dataverse configureren](hr-admin-integration-common-data-service.md)<br>
[Virtuele Dataverse-entiteiten configureren](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Veelgestelde vragen over virtuele tabellen voor Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminologiewijzigingen](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
