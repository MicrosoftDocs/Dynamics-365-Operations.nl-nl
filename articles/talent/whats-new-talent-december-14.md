---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (14 december 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
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
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 9887d22a513e820c35c51b6c702e2d9d34ab1214
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529751"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-december-14-2018"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (14 december 2018)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Build 8.1.2085**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.

## <a name="changes"></a>Wijzigingen

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>Ondersteuning voor de US - ACA (Affordable Care Act) voor de 1095-B- en 1095-C-formulieren voor het fiscale jaar 2018

Elk jaar moeten ALE's (Applicable Large Employers; toepasselijke grote werkgevers) alle fulltime werknemers voorzien van een 1095-C-formulier. Als de werkgever interne verzekering aanbiedt, moeten werknemers het 1095-C-formulier (voor ALE's) en een 1095-B-formulier (voor kleine werkgevers) verstrekken aan alle werknemers (fulltime of parttime) die vallen onder een van de aangeboden verzekeringen. Deze functie voorziet in afdrukbare 1095-C- en 1095-B-formulieren.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>Tijdens het importeren wordt het veld SubmittedByPersonId in HcmPerfJournalEntity genegeerd

Bij het importeren/exporteren van journaalposten voor prestaties wordt het veld **Ingediend door** genegeerd. Met deze wijziging weerspiegelt de waarde voor **geïmporteerd/geëxporteerd** de waarde in de tabel tijdens het exporteren. Bij het importeren wordt het systeem bijgewerkt met de waarde die is opgegeven in het importbestand.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Op het tabblad Analyses in het werkgebied Verlof en verzuim wordt de fout OpenConnectionError weergegeven voor niet-systeembeheerdersrollen

Met deze update worden er geen fouten meer weergegeven wanneer u het tabblad **Analyses** in het werkgebied **Verlof en verzuim** opent.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Bovenliggende knooppunt kan niet vanuit tegel worden opgehaald bij inzoomen op positiehiërarchie voor werknemersselfservice

Er is een wijziging aangebracht om de fout Het ophalen van het bovenliggende knooppunt is mislukt te corrigeren wanneer de positiehiërarchie is aangepast om in een bestaande werkruimte weer te geven en een positie is geselecteerd in de hiërarchie.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Moet systeembeheerder zijn om het tabblad Salaris op de pagina Positie weer te geven

Een wijziging is aangebracht zodat de juiste beveiligingselementen worden opgenomen in de bestaande bevoegdheid Details salarismedewerker en -positie onderhouden. Met deze wijziging heeft de salarisadministrateur standaard toegang tot de salarisvelden op de pagina Positie.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Fout bij het indienen van prestatiebeoordeling bij manager en de tijdelijke aanduiding %Reviews.PerfPeriod% wordt gebruikt in de indieningsinstructies

Een wijziging is aangebracht om de fout Nullreferentie te corrigeren bij gebruik van de tijdelijke aanduiding %Reviews.PerfPeriod% in de indieningsinstructies.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Power BI-rapport Personeel bevat een fout wanneer de anciënniteitsdatum van de werknemer een schrikkeldag is

Met deze wijziging worden schrikkeldagen nu ondersteund in Power BI.

### <a name="integration-between-core-hr-and-attract"></a>Integratie tussen Core HR en Attract

Een wijziging is doorgevoerd om de integratie tussen Core HR en Attract met betrekking tot aan te stellen kandidaten bij te werken. Om aan te stellen kandidaten zichtbaar te maken in het werkgebied **Personeelsbeheer**, worden de volgende Common Data Service-entiteiten gebruikt:

Sollicitatie
- Reden van status moet worden ingesteld op Aanbieding geaccepteerd
-   Biedt kandidaat en vacature

Kandidaat
-   Biedt informatie over kandidaat

Vacature
-   Biedt vacature-id en deelnemers voor vacature

Deelnemers voor vacature
-   Biedt aanstellend manager

Wanneer een kandidaat wordt toegevoegd aan Personeelsbeheer, kan de kandidaat nu ook worden afgewezen met behulp van een nieuwe optie die beschikbaar is op de kandidaatkaart.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Verlof en verzuim: toekomstig verlof en prognoses van verlofsaldi

Naast de wijzigingen om werknemers in staat te stellen verlof te voorspellen en toekomstige verlofaanvragen aan te vragen zonder dat dit invloed heeft op hun huidige verlofsaldi, wordt ook de wijze aangepast waarop verlofsaldi worden weergegeven. 

Het beschikbare saldo dat momenteel wordt weergegeven, is de hoeveelheid verlof die beschikbaar is voor aanvragen, met inbegrip van toerekeningen tot en met vandaag en alle goedgekeurde aanvragen tot en met het einde van de tijd. 

Wanneer de functie voor voorspellen wordt vrijgegeven, wordt het huidige verlofsaldo weergegeven, inclusief toerekeningen en verzoeken tot en met vandaag. Werknemers en managers zien deze bijgewerkte saldi in de selfservice-functionaliteit voor werknemer en manager op de kaart **Verlof** en in het venster **Verlofsaldi**. Voor HR-managers worden deze bijgewerkte saldi weergegeven in het werkgebied **Mensen** en in het venster **Toegewezen verlofplannen** van de werknemer.

## <a name="known-issue"></a>Bekend probleem

### <a name="mapping-errors-in-the-integration-with-finance"></a>Toewijzingsfouten in de integratie met Finance

De volgende problemen kunnen optreden in de huidige sjabloon voor het integreren van Talent met Dynamics 365 Finance. Binnenkort wordt een nieuwe sjabloon gepubliceerd om toe te passen op alle nieuwe integratieprojecten die zijn gemaakt. Voor bestaande integratieprojecten kunnen de taaktoewijzingen worden bijgewerkt. Raadpleeg de volgende tabel voor bijgewerkte toewijzingen. 

>[!NOTE]
> Met de taak voor het toewijzen van taken aan bovenliggende posities worden geen gegevens geïntegreerd. Dit probleem wordt momenteel onderzocht. Er is geen oplossing in de huidige toewijzing. 

Voor de taak Afdelingen naar Operationele eenheid moeten de volgende toewijzingen worden bijgewerkt.

| Bestaand bronveld          | Nieuw bronveld |
| -------------------------------|------------------|
| cdm_description (omschrijving)  | cdm_name (naam)  |

Daarnaast moet een aanvullende toewijzing worden toegevoegd. Selecteer het laatste veld **Geen** om de volgende toewijzing toe te voegen.

| Bronveld                   | Doelveld    |
| -------------------------------|----------------------|
| cdm_description (omschrijving)  | NAMEALIAS (NAMEALIAS)|

De bijgewerkte toewijzingen moeten op de volgende afbeelding lijken.

![Taak Afdelingen naar Operationele eenheden](./media/DepartmentMapping.png)


Voor de taak Taken naar Taakdetails moeten de volgende toewijzingen worden bijgewerkt.

| Bestaand bronveld          | Nieuw bronveld                   |
| -------------------------------|------------------------------------|
| cdm_name (naam)                | cdm_description (omschrijving)      |
| cdm_name (omschrijving)         | cdm_jobdescription (taakomschrijving)|


De bijgewerkte toewijzingen moeten op de onderstaande afbeelding lijken.

![Taak Taken naar Taakdetails](./media/JobMapping.png)

Voor de taak Medewerkers naar Werk moeten de volgende toewijzingen worden bijgewerkt.

| Bestaand bronveld                 | Nieuw bronveld                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-mailadres 1)   | cdm_primaryemailaddress (primair e-mailadres) |
| cdm_telephone1 (telefoon 1)          | cdm_primarytelephone (primaire telefoon)       |

De transformatie van het veld Geslacht moet ook worden bijgewerkt. Selecteer het toewijzingtype **fn** (functie) voor Geslacht en werk de volgende waardetoewijzingen bij.

| Waarde Common Data Service                   | Waarde Finance and Operations                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Mannelijk                                             |
| 75440001                    | Vrouwelijk                                           |
| 75440002                    | None                                             | 
| 75440003                    | NonSpecific                                      |

De bijgewerkte toewijzingen moeten op de volgende afbeeldingen lijken.

![Taak Werknemers naar Werknemer.](./media/WorkerMapping.png)

![Transformatie van veld Geslacht](./media/WorkerTransform.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]