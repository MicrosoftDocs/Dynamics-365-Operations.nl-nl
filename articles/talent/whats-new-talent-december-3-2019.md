---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (3 december 2019)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528688"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (3 december 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit artikel worden de functies beschreven die in Dynamics 365 Talent nieuw of gewijzigd zijn.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2646. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Werkgebied Functiebeheer

Het werkgebied **Functiebeheer** bevat een lijst met functies die in elke versie worden geleverd. Nieuwe functies zijn standaard uitgeschakeld. U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven. Zie [Overzicht Functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)voor meer informatie over Functiebeheer.

Alle nieuwe functies behouden gedurende minimaal 30 dagen en doorgaans 30-60 dagen de previewstatus. De belangrijkste functies zijn over het algemeen beschikbaar in oktober en april van elk jaar na de previewperiode. Zodra u nieuwe functies in het werkgebied **Functiebeheer** ziet, kunt u deze inschakelen. Sommige functies zijn mogelijk standaard ingeschakeld.
 
Soms is een integrale functie standaard ingeschakeld en kan deze niet worden uitgeschakeld (bijvoorbeeld het werkgebied **Functiebeheer**).
 
Als een functie algemeen beschikbaar is, kan deze worden in- of uitgeschakeld in productieomgevingen. Het werkgebied **Functiebeheer** geeft aan wanneer een preview-functie verplicht wordt. Deze datum is gewoonlijk 1 oktober of 1 april, in overeenstemming met de halfjaarlijkse releaseplannen. U kunt verplichte functies niet uitschakelen. Tot de functie verplicht wordt, kunt u deze in alle omgevingen in- of uitschakelen.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Automatische planning van opschonen van batchtaakhistorie toevoegen (332528)

Met deze wijziging wordt **Batchtaakhistorie** elke avond uitgevoerd en worden items ouder dan 30 dagen verwijderd.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent reageert niet in medewerkersacties wanneer de lengte van het identificatienummer niet overeenkomt met het identificatietype (390971)

In deze versie wordt het probleem gecorrigeerd dat opduikt wanneer de lengte van het identificatienummer niet overeenkomt met de definitie in het identificatietype. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Vaste compensatie werkt niveau niet bij in geval van wijzigingen in positiedetails (348085)

In de versie van deze week bepaalt **Begindatum compensatie** de taak die is gekoppeld aan de positie op dat moment bij het maken van een nieuwe record voor vaste compensatie voor een werknemer.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>In de lijsten Medewerkers, Werknemers en Contractanten wordt nu Beide weergegeven bij Type medewerker als het alleen Medewerker of Contractant moet zijn (384473)

Deze wijziging resulteert in een nauwkeurige weergave van het type medewerker dat wordt ingevoerd (contractant of werknemer).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>E-mailmeldingen voor aanstellingsacties bevatten geen naamgegevens vanwege beveiligingsbeleid (383402)

Deze wijziging corrigeert de informatie die wordt weergegeven in de velden voor voor- en achternaam binnen de tijdelijke aanduidingen voor de werkstroom wanneer geavanceerde beveiliging is ingeschakeld.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>In het systeem is het mogelijk om twee volledige verlofdagen voor dezelfde dag op te nemen (379284)

Door deze wijziging kunt u niet twee verlofaanvragen voor dezelfde dag uitgeven. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Lijst met adreswijzigingen moet worden gesorteerd op ingangsdatum (352798)

Door deze wijziging wordt de lijst met adreswijzigingen nu gesorteerd op **ingangsdatum**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Verlofaanvragen moeten via Common Data Service kunnen worden verwijderd uit Talent (376999)

Door deze wijziging kunnen concept- en geannuleerde verlofaanvragen worden verwijderd vanuit Common Data Service en vervolgens uit Talent.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Het verwijderen van inkomstencodes is toegestaan wanneer dezelfde inkomstencode is toegewezen aan een werknemer (371792)

In deze versie moet u eerst de inkomstencode van de werknemer verwijderen voordat u deze uit het systeem verwijdert.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Werkstroom voor verlof en verzuim met twee goedkeuringsfasen kan niet worden voltooid (391116)

Door deze wijziging doorloopt de werkstroom voor verlof en verzuim alle stappen wanneer er meer dan één goedkeuringsfase voor de aanvraag is geconfigureerd.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Uitgiftedatum wordt niet gesynchroniseerd met Common Data Service indien bijgewerkt of ingevoerd in Talent (397361)

Door deze wijziging wordt een probleem gecorrigeerd waarbij de uitgiftedatum voor records van het type **Persoonsidentificatie** niet worden gesynchroniseerd met Common Data Service vanuit Talent.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Er wordt een fout over een hiërarchische kringverwijzing uitgegeven bij het toewijzen van een manager aan een positie (386659)

Deze wijziging corrigeert een uniek scenario waarbij een kringverwijzingsfout wordt weergegeven bij het toewijzen van een nieuwe manager aan een positie.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service-entiteiten die nu aangepaste velden ondersteunen

De volgende Common Data Service-entiteiten ondersteunen nu aangepaste velden:

| Naam | Entiteit |
| --- | --- |
| Bankrekeningvoorschot | cdm_bankaccountdisbursement |
| Frequentie van vergoedingenberekening | cdm_benefitcalculationfrequency |
| Salarisperiode vergoedingsberekeningsfrequentie | cdm_benefitcalculationfrequencypayperiod |
| Berekeningstarief vergoeding | cdm_benefitcalculationrate |
| Details berekeningstarief vergoeding | cdm_benefitcalculationratedetail |
| Vergoedingsoptie | cdm_benefitoption |
| Vergoedingsplan | cdm_benefitplan (niet ingeschakeld voor ondersteuning van aangepaste velden) |
| Vergoedingstype | cdm_benefittype |
| Kalender voor bedrijfsprocessen | cdm_businessprocesscalendar |
| Groepstoewijzing van bedrijfsproces | cdm_businessprocessgroupassignment |
| Bibliotheektaakgroep voor bedrijfsproces | cdm_businessprocesslibrarytaskgroup |
| Bedrijfsprocesfase | cdm_businessprocessstage |
| Koptekst van controlelijstsjabloon | cdm_businessprocesstemplateheader |
| Taak voor controlelijstsjabloon | cdm_businessprocesstemplatetask |
| Bedrijf | cdm_company |
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
| Departement | cdm_department |
| Dienstverband | cdm_employment |
| Etnische afkomst | cdm_ethnicorigin |
| Gebeurtenis voor vaste compensatie | cdm_fixedcompensationevent |
| Taak | cdm_job |
| Functiepositie | cdm_jobfunction |
| Functiepositie | cdm_jobposition |
| Functietype | cdm_jobtype |
| Taal | cdm_language |
| Bank verlaten-transactie | cdm_leavebanktransaction |
| Verlofinschrijving | cdm_leaveenrollment |
| Verlofplan | cdm_leaveplan |
| Verlofaanvraag | cdm_leaverequest |
| Gegevens van verlofaanvraag | cdm_leaverequestdetail |
| Verloftype | cdm_leavetype |
| Redencode voor verloftype | cdm_leavetypereasoncode |
| Betalingscyclus | cdm_paycycle |
| Salarisperiode | cdm_payperiod |
| Inkomstencode salaris | cdm_payrollearningcode |
| Instelling die persoonsidentificatie uitgeeft | cdm_personidentificationissuingagency |
| Positietype | cdm_positiontype |
| Medewerkertoewijzing voor positie | cdm_positionworkerassignmentmap |
| Redencode | cdm_reasoncode |
| Vaardigheidstype | cdm_skilltype |
| Belastingregio | cdm_taxregion |
| Vestigingsregel | cdm_vestingrule |
| Veteraanstatus | cdm_veteranstatus |
| Werkkalender | cdm_workcalendar |
| Werkkalenderdag | cdm_workcalendarday |
| Feestdag werkkalender |cdm_workcalendarholiday |
| Feestdagregel van werkkalender | cdm_workcalendarholidayline |
| Tijdsinterval werkkalender | cdm_workcalendartimeinterval (niet ingeschakeld voor ondersteuning van aangepaste velden) |
| Medewerker | cdm_worker |
| Adres medewerker | cdm_workeraddress |
| Bankrekening medewerker | cdm_workerbankaccount |
| Vaste compensatie medewerker | cdm_workerfixedcompensation |
| Persoonsgegevens van medewerker | cdm_workerpersonaldetail |
| Persoonlijk identificatienummer medewerker | cdm_workerpersonidentificationnumber |
| Persoonlijk identificatietype medewerker | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Preview

Preview-functies zijn alleen beschikbaar in **Sandbox**-omgevingen.

### <a name="print-performance-reviews"></a>Prestatiebeoordelingen afdrukken

Zie [Beoordelingen van afdrukprestaties](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in het Dynamics 365: releasewave 2-plan van 2019.
