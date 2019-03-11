---
title: Integratie van Dynamics 365 for Talent met Dynamics 365 for Finance and Operations - veelgestelde vragen
description: In dit onderwerp wordt uitgelegd welke gegevens in een integratie van Talent en Finance and Operations worden gesynchroniseerd.
author: negudava
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aea025bc4898d6399e82030cf1f52b21949e014f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303925"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>Integratie van Dynamics 365 for Talent met Dynamics 365 for Finance and Operations - veelgestelde vragen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt antwoord gegeven op veelgestelde vragen over welke gegevens worden gesynchroniseerd wanneer Dynamics 365 for Talent wordt geïntegreerd met Dynamics 365 for Finance and Operations.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Worden alle gegevens gesynchroniseerd of alleen sommige gegevensentiteiten?

Met Core Human Resources (HRM) wordt een subset van de gegevens gesynchroniseerd. Zie voor een overzicht van alle entiteiten [Integratie van Dynamics 365 for Talent met Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).

Voor Attract en Onboard zijn alle gegevens systeemeigen voor Common Data Service´s (CDS) voor Apps.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Kan ik een nieuwe toewijzing maken zonder de sjablonen te gebruiken?

Sjablonen vormen het beginpunt. U kunt uw eigen sjabloon maken, maar een sjabloon is altijd vereist bij het maken van een integratieproject. Zie voor meer informatie over Gegevensintegrator (DI), sjablonen en projecten [Gegevens integreren in Common Data Service voor Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Kan ik financiële dimensies toewijzen voor overdracht tussen Talent en Finance and Operations?

CDS voor Apps bevat momenteel geen financiële dimensies en daardoor maken ze geen deel uit van de standaardsjabloon. Deze entiteit is gepland, maar momenteel is nog niet bekend wanneer deze beschikbaar is.

Voor gegevens die zich bevinden in Finance and Operations maar niet in Talent, koppelt u de twee systemen met behulp van **Koppelingen configureren** in Talent. Zie voor meer informatie over het configureren van koppelingen tussen Talent en Finance and Operations [Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (31 oktober 2018)](whats-new-talent-october-31.md).

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>Soms veranderen werknemers bij het importeren in inactieve werknemers in Finance and Operations. Waarom niet?

U kunt deze fout krijgen als werknemers geen detailrecord voor een actief dienstverband hebben in Talent. U lost dit op door naar **Personeelsbeheer \> Werknemers \> Historie dienstverband \> Datumbeheer** te gaan en te controleren of er een detailrecord voor actief dienstverband is.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Als ik besluit alleen een subset van velden toe te wijzen, wordt dan met wijzigingen die worden aangebracht in niet-toegewezen velden, een synchronisatie geactiveerd?

Gegevenssynchronisatie volgt de uitvoeringsplanning. Met de integratie wordt een record opgehaald als een veld in de record verandert, ongeacht of het veld deel uitmaakt van de integratietoewijzing.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Hoe kan ik alleen wijzigingen van actieve werknemers en niet van ontslagen werknemers verzenden?

U kunt met behulp van 'Geavanceerde query' brongegevens filteren en wijzigen voordat deze worden doorgegeven aan de bestemming.

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>Kan ik opgeven welke velden moeten worden verzonden naar Finance and Operations voor een bepaalde entiteit?

Velden kunnen worden toegevoegd aan of verwijderd uit de integratietaak. Niet alle gegevensvelden die aanwezig zijn in de entiteit CDS voor Apps (CDS 2.0) worden ingevuld vanuit Core HR.
Aanvullende gegevens kunnen worden ingevuld via PowerApps.

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Ik heb integratie als een batchtaak ingesteld, maar Talent heeft de verbinding met het doelsysteem verloren. Hoe kan ik dezelfde reeks wijzigingen naar het doelsysteem verzenden?

Er is geen speciale instelling vereist voor het afhandelen van uitzonderingen. Met de Gegevensintegrator worden fouten in de bron en de bestemming automatisch geïdentificeerd en gerapporteerd en handmatige nieuwe pogingen zijn toegestaan. Echter handmatige gegevenscorrectie is niet toegestaan. Als gegevens moeten worden bijgewerkt, moet dat in de bron of de bestemming plaatsvinden.

## <a name="can-i-set-up-bi-directional-integration"></a>Kan ik integratie in twee richtingen instellen?

Nee, integratie verloopt momenteel in één richting (Talent naar Finance and Operations). Er is echter een standaardsjabloon beschikbaar voor het verzenden van gegevens van Talent naar Finance and Operations.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Kan ik recordverwijdering toestaan als onderdeel van mijn integratie?

Nee, met Gegevensintegrator worden verwijderde records niet vastgelegd voor gegevensoverdracht. Gegevens kunnen momenteel alleen worden gemaakt en bijgewerkt (UPSERT).

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Kan ik de foutieve uitvoering opnieuw uitvoeren? Als dat zo is, wordt dan een volledig bestand gestuurd of alleen de wijzigingen?

De eerste uitvoering van Gegevensintegrator is altijd een volledige uitvoering. Latere uitvoeringen zijn gebaseerd op bijhouden van wijzigingen. Wanneer een foutuitvoering wordt uitgevoerd, worden de records in het bereik opgehaald en worden de meest recente wijzigingen vanuit CDS verzonden.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Wanneer ik het project opsla, wordt het foutbericht: 'Project heeft toewijzingsfouten' weergegeven. Wat moet ik doen?

Controleer de instellingen van uw integratiesleutels, breng de nodige wijzigingen aan in de instellingen en vernieuw de entiteiten in het project.

Als de standaardsjabloon wordt gebruikt, worden de integratiesleutels automatisch geïmporteerd. Dit probleem kan optreden wanneer er nieuwe taken worden toegevoegd aan de bestaande sjabloon.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Als ik N aantal rechtspersonen heb waar werknemers dienstverbanden hebben, moet ik dan voor ieder van hen een toewijzing maken?

Ja, voor elke rechtspersoon in Finance and Operations hebt u een afzonderlijk integratieproject in de gegevensintegratie nodig.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Ik moet gegevens overbrengen die geen deel uitmaken van de standaardsjabloon die door Microsoft is geleverd. Kan ik dit doen?

Ja, velden kunnen worden toegevoegd aan of verwijderd uit de bestaande sjabloon. De sjabloon kan worden gewijzigd om extra gegevens op te nemen van andere CDS voor Apps-entiteiten. De entiteit moet zich in CDS voor Apps bevinden om in de sjabloon te kunnen worden opgenomen. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Ik heb nieuwe Finance and Operations- en Talent-omgevingen gemaakt en ik krijg het foutbericht dat de gegevenswaarde integriteitsbeperkingen schendt. Waarom niet?

Redenen voor deze fout kunnen zijn:

- De gegevensoverdracht heeft geresulteerd in het extraheren van dubbele records bij de bron (CDS).

- De gegevensoverdracht heeft null-waarden voor velden die vereist zijn in Finance and Operations. Controleer of de gegevens zich in CDS bevinden en voldoen aan de vereisten van Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Als er uitvoeringsfouten zijn en de werknemer-ID niet is gesynchroniseerd, hoe vind ik de historietaak met de mislukte werknemerrecord dan?

Gegevensintegrator maakt meerdere projecten in Finance and Operations. De relatie tussen de Gegevensintegrator-taak en het Finance and Operations-project is een-op-een.

Zoek de tijd op van de uitvoeringshistorie van Gegevensintegrator en zoek naar index -1 project in Finance and Operations. Als het taaknummer 9 in Gegevensintegrator is, is de index in Finance and Operations 8.

1. Leg de taakindex in Gegevensintegrator vast (in dit voorbeeld is dit '9').

![Taakindex in Gegevensintegrator vastleggen](media/CaptureTaskIndex.png)

2. Houd de uitvoeringstijd van het project bij.

![Uitvoeringstijd van project bijhouden](media/CaptureTimeOfExecution.png)

3. Identificeer index - 1 in Finance and Operations. In dit voorbeeld komt het project met achtervoegsel '8' en uitvoeringstijd van index '0' overeen met de uitvoeringstijd in stap 2.

![Index identificeren](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Nadat ik Talent en Finance and Operations heb geïntegreerd, zie ik mijn Talent-gegevens in Finance and Operations niet. Wat moet ik doen?

De integratie met Finance and Operations is een proces dat uit twee stappen bestaat. Controleer eerst of de Talent-gegevens zijn bijgewerkt en beschikbaar zijn in CDS. Dit is een bijna realtime-synchronisatie en kan in PowerApps worden geverifieerd door te kijken naar de gegevens in de gegevensentiteiten.

![Gegevens in CDS](media/DataInCDS.png)

Als de gegevens niet zoals verwacht in CDS worden weergegeven, controleert u of de entiteit in de integratie wordt ondersteund. Als u aanvullende gegevens in CDS wilt opnemen, is een wijziging aan Microsoft-zijde vereist.

Als de entiteit wordt ondersteund en de gegevens beschikbaar zijn in CDS, controleert u of de toewijzing in Gegevensintegrator juist is. Als de integratortoewijzing er goed uitziet, controleert u of de taken voor gegevensbeheer zonder problemen zijn uitgevoerd. Er kunnen fouten optreden tijdens de uitvoering van de batchtaken. Zie [Gegevensbeheer](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json) voor meer informatie over Gegevensbeheer.

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>De adressen van mijn werknemers zijn onjuist nadat ik deze in Finance and Operations heb geïmporteerd. Wat moet ik doen?

De nummerreeks voor **Locatie-ID** gebruikt hetzelfde patroon in zowel Talent als Finance and Operations. De nummerreeks moet voor beide uniek zijn zodat er geen adresconflicten ontstaan bij het integreren van gegevens van CDS met Finance and Operations.

Controleer tijdens de implementatie van Talent of de nummerreeksen niet hetzelfde zijn in Talent en Finance and Operations. Controleer of alle nummerreeksen niet identiek zijn in gevallen waar gegevens in beide systemen kunnen worden beheerd.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Bij het maken van mijn verbindingenset zie ik de verbinding niet in de vervolgkeuzelijst Verbinding. Wat moet ik doen?

Zorg ervoor dat wanneer u uw verbindingen maakt, u Dynamics 365 for Finance and Operations (momenteel in het voorbeeld) en Common Data Service kiest.

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Tijdens het synchroniseren van dienstverbanden krijg ik de fouten 'CompanyInfo_FK bestaat niet' of 'De waarde '12/31/2154 23:59:59 pm' in het veld Einddatum dienstverband' is niet gevonden in de gerelateerde tabel 'Dienstverband'. Wat moet ik doen?

Zorg ervoor dat u toewijst aan de juiste rechtspersonen. Synchronisatie van rechtspersonen maakt geen deel uit van de standaardsjabloon. Dus elke rechtspersoon die aanwezig is in Talent en CDS, zal naar verwachting ook aanwezig zijn in Finance and Operations.
Zorg er ook voor dat u de juiste rechtspersonen voor de bijbehorende verbindingenset selecteert.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>Nadat ik mijn project heb ingesteld, is de veldtoewijzing voor Finance and Operations leeg. Wat moet ik doen?

Vernieuw de gegevensentiteiten in Finance and Operations door naar **Gegevensbeheer \> Raamwerkparameters \> Entiteitsinstellingen \> Entiteitslijst vernieuwen** te gaan. Dit duurt enkele minuten. Vervolgens moet u deze toewijzingen zien. Dit probleem treedt op wanneer nieuwe projecten worden gemaakt.

![Veldtoewijzing ontbreekt](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Aanvullende bronnen

- Gegevensintegrator (DI): 

  - [Gegevens integreren in Common Data Service voor Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [Foutbeheer en probleemoplossing van Gegevensintegrator](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [Reageren op DSR-aanvragen voor door het systeem gegenereerde logboeken in PowerApps, Microsoft Flow en Common Data Service voor Apps](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Gegevensbeheer:

  - [Gegevensbeheer](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
