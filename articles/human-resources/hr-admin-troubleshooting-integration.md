---
title: Veelgestelde vragen over integratie met Finance
description: In dit artikel wordt uitgelegd welke gegevens in een integratie van Human Resources en Finance worden gesynchroniseerd.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2ac28a1bd09cf68c711295116fb007bdfab2070
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053390"
---
# <a name="integration-with-finance-faq"></a>Veelgestelde vragen over integratie met Finance

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp wordt antwoord gegeven op veelgestelde vragen over welke gegevens worden gesynchroniseerd wanneer Dynamics 365 Human Resources wordt geïntegreerd met Dynamics 365 Finance.

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Kan ik de Dynamics 365 Talent-toepassingsgebruiker bewerken in Power Apps?

Nr. Als u de Human Resources-toepassingsgebruiker bewerkt, kan de integratie tussen Human Resources en Dataverse mislukken. In de volgende tabel worden de standaardinstellingen voor de Talent-toepassingsgebruiker getoond.

| Volledige naam | Sollicitatie-ID | Azure AD Object-id | Sollicitatie-ID URI |
| --- | --- | --- | --- |
| Dynamics365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Standaardinstellingen voor Talent-toepassingsgebruiker](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Worden alle gegevens gesynchroniseerd of alleen sommige gegevensentiteiten?

Er wordt een subset van de gegevens gesynchroniseerd. Zie [Integratie met Dynamics 365 Finance](hr-admin-integration-finance.md) voor een overzicht van alle entiteiten.

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>Waarom zie ik geen gegevens die zijn gesynchroniseerd met Dataverse?

Synchronisatie met Dataverse is standaard uitgeschakeld in nieuwe omgevingen die de opgegeven demogegevens niet bevatten. Standaard is deze ingeschakeld in nieuwe omgevingen die demogegevens bevatten, en gegevenssynchronisatie begint wanneer de omgeving wordt ingericht. Wanneer uw omgeving klaar is om gegevens te synchroniseren, kunt u de integratie inschakelen. Meer informatie vindt u in [Dataverse-integratie configureren](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Kan ik een nieuwe toewijzing maken zonder de sjablonen te gebruiken?

Sjablonen vormen het beginpunt. U kunt uw eigen sjabloon maken, maar een sjabloon is altijd vereist bij het maken van een integratieproject. Zie voor meer informatie over Gegevensintegrator (DI), sjablonen en projecten [Gegevens integreren in Microsoft Dataverse](/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Kan ik financiële dimensies toewijzen voor overdracht tussen Human Resources en Finance?

Dataverse bevat momenteel geen financiële dimensies en daardoor maken ze geen deel uit van de standaardsjabloon. Deze entiteit is gepland, maar momenteel is nog niet bekend wanneer deze beschikbaar is.

Voor gegevens die zich bevinden in Finance, maar niet in Human Resources, koppelt u de twee systemen met behulp van **Koppelingen configureren** in Human Resources.

![Financiële dimensies toewijzen](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Soms veranderen werknemers bij het importeren in inactieve werknemers in Finance. Waarom niet?

U kunt deze fout krijgen als werknemers geen detailrecord voor een actief dienstverband hebben in Human Resources. U lost dit op door naar **Personeelsbeheer \> Werknemers \> Historie dienstverband \> Datumbeheer** te gaan en te controleren of er een detailrecord voor actief dienstverband is.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Als ik besluit alleen een subset van velden toe te wijzen, wordt dan met wijzigingen die worden aangebracht in niet-toegewezen velden, een synchronisatie geactiveerd?

Gegevenssynchronisatie volgt de uitvoeringsplanning. Met de integratie wordt een record opgehaald als een veld in de record verandert, ongeacht of het veld deel uitmaakt van de integratietoewijzing.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Hoe kan ik alleen wijzigingen van actieve werknemers en niet van ontslagen werknemers verzenden?

U kunt met behulp van 'Geavanceerde query' brongegevens filteren en wijzigen voordat deze worden doorgegeven aan de bestemming.

![Geavanceerde query voor actieve medewerkers](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Kan ik opgeven welke velden moeten worden verzonden naar Finance voor een bepaalde entiteit?

Velden kunnen worden toegevoegd aan of verwijderd uit de integratietaak. Niet alle gegevensvelden die aanwezig zijn in de tabel Dataverse, worden ingevuld vanuit Human Resources.
Aanvullende gegevens kunnen worden ingevuld via Power Apps.

![Velden toevoegen aan en verwijderen uit een integratietaak](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Ik heb integratie als een batchtaak ingesteld, maar Human Resources heeft de verbinding met het doelsysteem verloren. Hoe kan ik dezelfde reeks wijzigingen naar het doelsysteem verzenden?

Er is geen speciale instelling vereist voor het afhandelen van uitzonderingen. Met de Gegevensintegrator worden fouten in de bron en de bestemming automatisch geïdentificeerd en gerapporteerd en handmatige nieuwe pogingen zijn toegestaan. Echter handmatige gegevenscorrectie is niet toegestaan. Als gegevens moeten worden bijgewerkt, moet dat in de bron of de bestemming plaatsvinden.

## <a name="can-i-set-up-bi-directional-integration"></a>Kan ik integratie in twee richtingen instellen?

Nee, de integratie verloopt momenteel slechts in één richting (van Human Resources naar Finance and Operations). Er is echter een standaardsjabloon beschikbaar voor het verzenden van gegevens van Human Resources naar Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Kan ik recordverwijdering toestaan als onderdeel van mijn integratie?

Nee, met Gegevensintegrator worden verwijderde records niet vastgelegd voor gegevensoverdracht. Gegevens kunnen momenteel alleen worden gemaakt en bijgewerkt (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Kan ik de foutieve uitvoering opnieuw uitvoeren? Als dat zo is, wordt dan een volledig bestand gestuurd of alleen de wijzigingen?

De eerste uitvoering van Gegevensintegrator is altijd een volledige uitvoering. Latere uitvoeringen zijn gebaseerd op bijhouden van wijzigingen. Wanneer een foutuitvoering wordt uitgevoerd, worden de records in het bereik opgehaald en worden de meest recente wijzigingen vanuit Dataverse verzonden.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Wanneer ik het project opsla, wordt het foutbericht: 'Project heeft toewijzingsfouten' weergegeven. Wat moet ik doen?

Controleer de instellingen van uw integratiesleutels, breng de nodige wijzigingen aan in de instellingen en vernieuw de entiteiten in het project.

Als de standaardsjabloon wordt gebruikt, worden de integratiesleutels automatisch geïmporteerd. Dit probleem kan optreden wanneer er nieuwe taken worden toegevoegd aan de bestaande sjabloon.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Als ik N aantal rechtspersonen heb waar werknemers dienstverbanden hebben, moet ik dan voor ieder van hen een toewijzing maken?

Ja, voor elke rechtspersoon in Finance hebt u een afzonderlijk integratieproject in de gegevensintegratie nodig.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Ik moet gegevens overbrengen die geen deel uitmaken van de standaardsjabloon die door Microsoft is geleverd. Kan ik dit doen?

Ja, velden kunnen worden toegevoegd aan of verwijderd uit de bestaande sjabloon. De sjabloon kan worden gewijzigd om extra gegevens op te nemen van andere Dataverse-tabellen. De entiteit moet zich in Dataverse bevinden om in de sjabloon te kunnen worden opgenomen. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Ik heb nieuwe Finance- en Human Resources-omgevingen gemaakt en ik krijg het volgende foutbericht: 'De gegevenswaarde schendt de integriteitsbeperkingen'. Waarom niet?

Redenen voor deze fout kunnen zijn:

- De gegevensoverdracht heeft geresulteerd in het extraheren van dubbele records bij de bron (Dataverse).

- De gegevensoverdracht heeft null-waarden voor velden die vereist zijn in Finance and Operations. Controleer of de gegevens zich in Dataverse bevinden en voldoen aan de vereisten van Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Als er uitvoeringsfouten zijn en de werknemer-ID niet is gesynchroniseerd, hoe vind ik de historietaak met de mislukte werknemerrecord dan?

Gegevensintegrator maakt meerdere projecten in Finance. De relatie tussen de Gegevensintegrator-taak en het Finance-project is een-op-een.

Zoek de tijd op van de uitvoeringsgeschiedenis van Gegevensintegrator en zoek naar het index -1 project in Finance. Als het taaknummer 9 in Gegevensintegrator is, is de index in Finance 8.

1. Leg de taakindex in Gegevensintegrator vast (in dit voorbeeld is dit '9').

    ![Taakindex in Gegevensintegrator vastleggen](media/CaptureTaskIndex.png)

2. Houd de uitvoeringstijd van het project bij.

    ![Uitvoeringstijd van project bijhouden](media/CaptureTimeOfExecution.png)

3. Geef index - 1 op in Finance. In dit voorbeeld komt het project met achtervoegsel '8' en uitvoeringstijd van index '0' overeen met de uitvoeringstijd in stap 2.

    ![Index identificeren](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>Na integratie van Human Resources en Finance worden mijn Human Resources-gegevens niet in Finance weergegeven. Wat moet ik doen?

De integratie met Finance is een proces dat uit twee stappen bestaat. Controleer eerst of de Human Resources-gegevens zijn bijgewerkt en beschikbaar zijn in Dataverse. Dit is een bijna realtime-synchronisatie en kan in Power Apps worden geverifieerd door te kijken naar de gegevens in de gegevenstabellen.

![Gegevens in Dataverse](media/DataInCDS.png)

Als de gegevens niet zoals verwacht in Dataverse worden weergegeven, controleert u of de entiteit in de integratie wordt ondersteund. Als u aanvullende gegevens in Dataverse wilt opnemen, is een wijziging aan Microsoft-zijde vereist.

Als de entiteit wordt ondersteund en de gegevens beschikbaar zijn in Dataverse, controleert u of de toewijzing in Gegevensintegrator juist is. Als de integratortoewijzing er goed uitziet, controleert u of de taken voor gegevensbeheer zonder problemen zijn uitgevoerd. Er kunnen fouten optreden tijdens de uitvoering van de batchtaken. Zie [Gegevensbeheer](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json) voor meer informatie over Gegevensbeheer.

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>De adressen van mijn werknemers zijn onjuist nadat ik deze in Finance heb geïmporteerd. Wat moet ik doen?

De nummerreeks voor **Locatie-id** gebruikt hetzelfde patroon in zowel Human Resources als Finance. De nummerreeks moet voor beide uniek zijn zodat er geen adresconflicten ontstaan bij het integreren van gegevens van Dataverse met Finance and Operations.

Controleer tijdens de implementatie van Human Resources of de nummerreeksen niet hetzelfde zijn in Human Resources en Finance. Controleer of alle nummerreeksen niet identiek zijn in gevallen waar gegevens in beide systemen kunnen worden beheerd.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Bij het maken van mijn verbindingenset zie ik de verbinding niet in de vervolgkeuzelijst Verbinding. Wat moet ik doen?

Zorg ervoor dat wanneer u uw verbindingen maakt, u Dynamics 365 Finance en Dataverse kiest.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Tijdens het synchroniseren van dienstverbanden krijg ik de fouten 'CompanyInfo_FK bestaat niet' of 'De waarde '12/31/2154 23:59:59 pm' in het veld Einddatum dienstverband' is niet gevonden in de gerelateerde tabel 'Dienstverband'. Wat moet ik doen?

Zorg ervoor dat u toewijst aan de juiste rechtspersonen. Synchronisatie van rechtspersonen maakt geen deel uit van de standaardsjabloon. Dus elke rechtspersoon die aanwezig is in Human Resources en Dataverse, zal naar verwachting ook aanwezig zijn in Finance.
Zorg er ook voor dat u de juiste rechtspersonen voor de bijbehorende verbindingenset selecteert.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Nadat ik mijn project heb ingesteld, is de veldtoewijzing voor Finance leeg. Wat moet ik doen?

Vernieuw de gegevensentiteiten in Finance door naar **Gegevensbeheer \> Raamwerkparameters \> Entiteitsinstellingen \> Entiteitslijst vernieuwen** te gaan. Dit duurt enkele minuten. Vervolgens moet u deze toewijzingen zien. Dit probleem treedt op wanneer nieuwe projecten worden gemaakt.

![Veldtoewijzing ontbreekt](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Aanvullende bronnen

- Gegevensintegrator (DI): 

  - [Gegevens integreren in Microsoft Dataverse](/powerapps/administrator/data-integrator)

  - [Foutbeheer en probleemoplossing van Gegevensintegrator](/powerapps/administrator/data-integrator-error-management)

  - [Reageren op DSR-aanvragen voor door het systeem gegenereerde logboeken in Power Apps, Microsoft Power Automate en Dataverse](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Gegevensbeheer:

  - [Gegevensbeheer](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]