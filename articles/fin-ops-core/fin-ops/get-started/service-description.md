---
title: Beschrijving van service voor Finance and Operations-toepassingen
description: In dit onderwerp vindt u de serviceomschrijving voor Finance and Operations-toepassingen.
author: tomhig
ms.date: 01/05/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: 85f82a863f0bde4c0414760fa2477651242538f2
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952361"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Beschrijving van service voor Finance and Operations-toepassingen

[!include[banner](../includes/banner.md)]

Finance and Operations-toepassingen zijn ERP-software (Enterprise Resource Planning) als serviceaanbiedingen (Ers) die zijn gebaseerd op en voor [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/). De service biedt organisaties een ERP-functionaliteit die ondersteuning biedt voor hun unieke behoeften en die ze helpt bij het aanpassen aan het veranderen van bedrijfsomgevingen zonder dat zij de Finance and Operations-infrastructuur moeten beheren. Finance and Operations-toepassingen kunnen een of meer van de volgende oplossingsgebieden bevatten:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Samen met [business intelligence](/power-bi/fundamentals/power-bi-service-overview)-, [infrastructuur](https://azure.microsoft.com/global-infrastructure/)-, [compute](/azure/service-fabric/service-fabric-overview)- en [databaseservices](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/) stelt u organisaties in staat om bedrijfstakspecifieke en operationele bedrijfsprocessen uit te voeren. Klanten worden ondersteund door hun implementatiepartner en bepalen de configuratie van de bedrijfstoepassingslogica die het beste bij de unieke bedrijfsprocessen past. Functionaliteit en bedrijfsprocessen kunnen worden aangevuld met een of meer van de volgende oplossingen:

- Ingebouwde [personalisatie-ervaring](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md)-hulpmiddelen
- [Visual Studio](https://visualstudio.microsoft.com)–gebaseerde [Finance and Operations software development kit (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) en [Azure DevOps build automation](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Oplossingen voor onafhankelijke softwareleveranciers (ISV) van [AppSource](https://appsource.microsoft.com/partners)

Klanten kiezen op basis van behoeften hun oplossingsbenadering. Zij werken samen met hun implementatiepartner om hun oplossing te definiëren, te ontwikkelen en te testen met behulp van de hulpprogramma's en best practices die worden geleverd in [Microsoft Dynamics Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs.md). Er zijn vier veelvoorkomende scenario's:

- Standaard Finance and Operations toepassingen met 'out of the box' configuratie (geen uitbreidingen)
- Finance and Operations-toepasingsconfiguratie met een of meer ISV-oplossingen
- Finance and Operations-toepassingsconfiguratie met een of meer klantspecifieke uitbreidingen
- Finance and Operations-toepassingsconfiguratie met een combinatie van klantspecifieke uitbreidingen en één of meer ISV-oplossingen

U kunt organisaties laten meegroeien met hun bedrijfsgroei door eenvoudig gebruikers en bedrijfsprocessen toe te voegen via een eenvoudig, transparant abonnementsmodel. Zie [Dynamics 365-licentiehandleiding](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365) voor meer informatie.

## <a name="operating-model"></a>Gebruiksmodel

Het gebruiksmodel van toepassingen definieert specifieke rollen en verantwoordelijkheden voor de klant, implementatiepartner en Microsoft tijdens de Finance and Operations-levenscyclus van de service. Zie [cloudbewerkingen en service in de cloud](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md) voor meer informatie.

### <a name="customer-activities"></a>Klantenactiviteiten

Klanten werken samen met hun partner en [Microsoft FastTrack](/dynamics365/fasttrack/) op basis van het [Dynamics 365 Implementation Guide](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide), the [Success by Design](/dynamics365/fasttrack/success-by-design-overview)-framework en maken gebruik van de tools en best practice-sjablonen die in [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) worden geleverd om de oplossing te implementeren. Veelvoorkomende activiteiten zijn:

- Identiteit en beveiligingsbeheer van gebruikers
- Bedrijfsprocessen definiëren, ontwikkelen en bedienen
- Uitbreidingen definiëren, ontwikkelen, testen en bedienen
- Implementaties buiten productie bewaken en beheren
- Toepassingsupdates beheren en uitbreidingen valideren
- ISV-oplossingen en integratie van derde partijen beheren

### <a name="microsoft-responsibilities"></a>Verantwoordelijkheden van Microsoft

Microsoft beheert de service door klant- en productieomgevingen te implementeren, te controleren en af Finance and Operations te werken in het Microsoft SaaS-abonnement. Dit beheer omvat het toewijzen van de vereiste systeeminfrastructuur om de service uit te voeren en proactief te communiceren met klanten over de gezondheid van de service. Verantwoordelijkheden zijn onder meer:

**Infrastructuurbeheer**
- Beveiliging en isolatie
- Besturingssystemen en virtualisatie
- Servers, opslag en networking
- Ondersteuning datacentrum, netwerken, koelen

**Platformbeheer voor toepassing**
- 24/7 toepassingscontrole en meldingen
- Diagnoses, platformupdates, patchs, service-updates
- Toepassingsrouting, taakverdeling, sitereplicatie
- Voorzieningen en beheer van het milieu
- Databasebeheer, hoge beschikbaarheid (HA)/disaster recovery (DR), schalen, bewerkingen
- Implementatie, opschalen en neerschalen

## <a name="system-configuration"></a>Systeemconfiguratie

Finance and Operations-toepassingen schalen op basis van het transactievolume en de gebruikersbelasting. Door elke klantuitvoering wordt een unieke oplossing geproduceerd die uit de volgende elementen bestaat:

- **Gegevenscompositie**: een unieke set parameters die de gedragscontrole bepalen, de indeling van de organisatie, de structuur van hoofdgegevens (zoals financiële en voorraaddimensies) en de gedetailleerdheid van transactievolgbaarheid.
- **Uitbreiding en configuratie** – Uitbreidingsmechanismen die code-uitbreidingen, ISV-oplossingen en unieke configuraties gebruiken met workflows, integraties en rapportconfiguraties.
- **Gebruikspatronen** - een unieke combinatie van online- en batchgebruik, samen met de mogelijkheid om te integreren met upstream en downstream systemen voor centrale gegevensstroom en de mogelijkheid om onderscheid te maken op basis van de informatieweergaven die klanten in hun bedrijfsprocessen gebruiken.

Microsoft configureert klantproductieomgevingen die zijn aangepast aan de transactievolumes en gelijktijdigheid van gebruikers. Microsoft is verantwoordelijk voor de volgende taken:

- De resources van productieomgevingen correct toewijzen op basis van de profileringsgegevens van de klant in de [LCS-abonnementsschatter](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- De servicebeschikbaarheid van productieomgevingen continu controleren en diagnosticeren
- Problemen met systeemprestaties analyseren en oplossen met Finance and Operations-toepassingen

Om ervoor te zorgen dat een implementatie is geconfigureerd voor hoge prestaties, moeten klanten de volgende taken uitvoeren:

- Geef nauwkeurige gebruiksinformatie over de Finance and Operations-implementatie in de [LCS-abonnementschatter](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Uitbreidingen bouwen en testen op prestaties en schaalbaarheid.
- De gegevensconfiguraties op de juiste manier testen op de prestaties.
- Schaalbaarheid controleren door [prestatietests](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) uit te voeren voordat u live gaat.

## <a name="onboarding-and-implementation"></a>Onboarding en implementatie

De volgende tabel toont typische onboarding- en implementatiegebeurtenissen.

| Aanvragen | Verwachte Microsoft-actie | Verwachte actie van klant-/implementatiepartner |
|---|---|---|
| Aankoop van eerste aanbieding | Er wordt een LCS-project gemaakt na de aankoop van de aanbieding, op basis van een gebeurtenis die door de klant is geactiveerd. | Doorloop het Enterprise Agreement (EA) of Cloud Solution Provider (CSP) [commercieel proces](before-you-buy.md). De partner maakt, indien van toepassing, een tenant voor de klant. |
| Aankoop van invoegtoepassing | Verleen de klant toegang tot de invoegtoepassing die tijdens de implementatie is geselecteerd. | Niet van toepassing |
| Implementatieplanning en -analyse | Relevante hulpmiddelen in LCS leveren, zoals [Business Process Modeler (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) en [interoperabiliteit met Azure DevOps](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Voer projectplanning uit, stel Azure DevOps in, voltooi de systeemintroductie en stel beheerdersaccounts in. |

Zie [Onboarding van een implementatieproject](../imp-lifecycle/onboard.md) voor meer informatie.

## <a name="globalization"></a>Globalisatie

Finance and Operations-toepassingen worden vanuit verschillende Azure-regio's over de hele wereld gebruikt. Finance and Operations-toepassingen bieden functionaliteit ter ondersteuning van verschillende landen/regio's en moedertalen. Zie [Localisatie en wettelijke functies](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features) voor meer informatie.

### <a name="countryregion-specific-considerations"></a>Land-/regiospecifieke overwegingen

- Klanten in de gereguleerde sector of commerciële organisaties die zaken doen met entiteiten in Frankrijk die lokale gegevensresidentie vereisen, moeten [Finance and Operations in Frankrijk](../../dev-itpro/deployment/france-local-deployment.md) nalezen.
- Klanten die activiteiten in China hebben moeten [Azure China Playbook](/azure/china/) en [Finance and Operations via 21Vianet in China](../../dev-itpro/deployment/china-local-deployment.md) raadplegen.
- Klanten die bewerkingen hebben in Rusland, moeten de [Russische localisatiewetgeving van persoonlijke gegevens](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia) controleren.

### <a name="general-data-protection-regulation-gdpr"></a>Algemene verordening gegevensbescherming (AVG)

Voor Finance and Operations-toepassingen fungeert Microsoft als gegevensverwerker. Als gegevensverwerker biedt Finance and Operations processen en functies die klanten helpen te voldoen aan de AVG-verplichtingen als gegevensbeheerder. Zie [AVG](../../dev-itpro/gdpr/gdpr-guide.md) voor meer informatie.

## <a name="environment-and-data-management"></a>Omevings - en gegevensbeheer

In deze sectie worden enkele gang van zaken beschreven voor de omgevings- en gegevensbeheergebeurtenissen die in de service plaatsvinden.

### <a name="environment-and-data-management-events-for-production-instances"></a>Omgevings- en gegevensbeheergebeurtenissen voor productie-exemplaren

LCS biedt [self-service tools](../../dev-itpro/deployment/infrastructure-stack.md) en [gegevensverplaatsingsbewerkingen](../../dev-itpro/database/dbmovement-operations.md) die gebruikt worden voor het uitvoeren van omgevings- en gegevensbeheertaken. Hieronder volgen een aantal voorbeelden:

**Gebeurtenis:** [een productie-exemplaar aanvragen](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- Voltooi de [Go-live controlelijst](../imp-lifecycle/prepare-go-live.md) en verzend deze naar het [Microsoft FastTrack](/dynamics365/fasttrack/)-team.
- Voltooi de [LCS-abonnementsschatter](../../dev-itpro/lifecycle-services/subscription-estimator.md) voordat u een productie-exemplaar aanvraagt.
- Voltooi alle implementatietaken die zijn opgegeven in de [LCS-methodologie](../../dev-itpro/lifecycle-services/create-methodology.md).

**Gebeurtenis:** [een sandbox database kopiëren naar een productie-exemplaar](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Uitgevoerd voor een nieuwe go-live of een werkelijke go-live cutover.

**Gebeurtenis:** [Onderhoudsmodus](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Schakel de onderhoudsmodus in in LCS.
2. Het vereiste onderhoud voltooien.
3. Schakel de onderhoudsmodus uit in LCS.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Omgevings- en gegevensbeheergebeurtenissen voor niet-productie-exemplaren

LCS biedt [self-service tools](../../dev-itpro/deployment/infrastructure-stack.md) en [gegevensverplaatsingsbewerkingen](../../dev-itpro/database/dbmovement-operations.md) die gebruikt worden voor het uitvoeren van omgevings- en gegevensbeheertaken. Hieronder volgen een aantal voorbeelden:

**Gebeurtenis:** [een nieuw sandbox exemplaar implementeren](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Zorg ervoor dat alle vereiste exemplaren zijn [gepland](../imp-lifecycle/environment-planning.md) en dat de toepasselijke invoegaanbiedingen zijn aangeschaft.
- Het implementatieproces in LCS uitvoeren.
- Voltooi alle taken die zijn gespecificeerd in de LCS-checklists.
    
>[!NOTE]
>Een sandbox ontwikkelomgeving is een virtuele machine (VM) die wordt [geïmplementeerd in het Azure-abonnement van de klant](../../dev-itpro/dev-tools/access-instances.md) en door de klant wordt beheerd.

**Gebeurtenis:** [een gouden configuratiedatabase kopiëren van sandbox naar productie](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Uitgevoerd voor een nieuwe go-live of een werkelijke go-live cutover.

**Gebeurtenis:** [een back-up van een productiepunt in een niet-productie-instantie terugzetten](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Voer de optie [Database vernieuwen](../../dev-itpro/database/database-refresh.md) uit in LCS.
- Post-copy: verwijder of verdoezel gevoelige gegevens via scripts, pas omgevingsspecifieke applicatieconfiguraties aan (zoals integratie-eindpunten) en activeer of voeg gebruikers toe. Houd er rekening mee dat deze wijzigingen worden aangebracht door een [gegevenspakket](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package)  toe te passen.

**Gebeurtenis:** [punt-in-tijd herstellen niet-productie-exemplaardatabase](../../dev-itpro/database/database-point-in-time-restore.md)

- Accepteer dat het proces niet ongedaan kan worden gemaakt.
- Voer de punt-in-tijd-herstelbewerking uit in LCS.

**Gebeurtenis:** een Database van Tier 2-database kopiëren naar een ontwikkelingsdatabase voor het oplossen van problemen en [foutopsporing](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Voer de database-exportbewerking in LCS uitvoer in de Tier 2-omgeving.
- De database in de ontwikkelomgeving importeren en bijwerken.

## <a name="data-backup-and-retention"></a>Back-up van gegevens en inhouding

Databases voor Finance and Operations-omgevingen in het SaaS-abonnement worden beveiligd door automatische back-ups. Voor productieomgevingen worden automatische back-ups 28 dagen bewaard, tenzij Microsoft een rollback doet. Voor een sandbox-omgeving (Tier 2+) blijven deze zeven dagen behouden. De productieomgeving kan worden terugdraaien als een fout optreedt tijdens een geplande onderhoudsupdate.

Zie [Automatische back-ups - Azure SQL Database & SQL Managed Instance](/azure/azure-sql/database/automated-backups-overview?tabs=single-database) voor meer informatie over automatische back-ups.

## <a name="service-activity-responsibilities"></a>Verantwoordelijkheden voor serviceactiviteiten

De volgende tabel beschrijft een aantal gebruikelijke scenario's en activiteiten voor de service. De informatie geeft ook aan of Microsoft, de klant of zowel Microsoft als de klant veelheid voor de activiteiten heeft.

| Activiteit | Verantwoordelijkheden van Microsoft | Verantwoordelijkheid van de klant |
|---|---|---|
| **Inrichten initiële tenants** | | |
| Bepaal de geprojecteerde belasting in LCS met behulp van het hulpprogramma Abonnementsschatter en vraag om de inrichting van specifieke omgevingen. | | X |
| Richt in voor alle productie-exemplaren en niet-productie-exemplaren. | X | |
| Valideer voor alle productie-exemplaren en niet-productie-exemplaren. | | X |
| **Service-updates** | |
| Pas service-updates toe op toegewezen niet-productie- en productie-exemplaren. | X | |
| Pas handmatig service-updates van LCS toe op sandbox-exemplaren. Download, ontwikkel en test de update en geef het code-updatepakket terug aan LCS. | | X |
| Vraag uitbreidingsupdates aan en plan ze voor toepassing op het productie-exemplaar. | | X |
| Maak een code en back-up van gegevens voor het productie-exemplaar voordat eventuele updates worden toegepast. | X | |
| Bij een fout, kunt u het productie-exemplaar terugdraaien naar de code en back-up van de gegevens. | X | |
| **Gegevensbeheer (back-up maken, herstellen en bijwerken)** | | |
| Een back-up maken van de database. | X | |
| Bepalen van een hoge beschikbaarheid en een herstelplan voor noodgevallen. | X | |
| De prestaties van de database met productie-instantie controleren. | X | |
| Stem de productie-exemplaardatabase af op prestaties. | X | |
| Voer op een bepaalde tijd een vernieuwing van de database van een productie-exemplaar naar een niet-productie-exemplaar uit. | | X |
| **De infrastructuur bijwerken** | | |
| Plan regelmatige infrastructuurupdates. | X | |
| **Op- en afschalen (gebruikers, opslag en exemplaren)** | | |
| Extra gebruikers en invoegtoepassingen voor niet-productie aanschaffen. | | X |
| Werk gebruikswijzigingen bij in de LCS abonnementsschatter-tool. | | X |
| Belangrijke prestatieproblemen rapporteren die van invloed zijn op het gebruik van de service. | | X |
| De resources die vereist zijn voor de toepasselijke service proactief beheren. | X | |
| Incidenten onderzoeken en oplossen. | X | |
| **Beveiliging (gebruikerstoegang)** | | |
| Geef gebruikers toegang tot de service. | | X |
| Geef LCS-projecttoegang voor het beheer en de bewerking van exemplaren die via LCS zijn geïmplementeerd. | | X |
| **productie-exemplaren controleren** | | |
| Controleer productie-exemplaren 24/7. | X | |
| De klant proactief op de hoogte brengen van incidenten met het productie-exemplaar. | X | |
| **Niet-productie-exemplaren beheren en controleren** | | |
| Niet-productie-exemplaren beheren met LCS. | | X |
| Niet-productie-exemplaren controleren. | | X |

## <a name="service-update-strategy"></a>Strategie van service-update

In overeenstemming met het [softwarelevenscyclusbeleid](../../dev-itpro/migration-upgrade/versions-update-policy.md), volgen Finance and Operations -apps fhet Microsoft [Modern levenscyclusbeleid](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), dat producten dekt die continu worden onderhouden en ondersteund. 

Microsoft brengt in de volgende maanden elk jaar acht service-updates uit voor Finance and Operations-apps:

- Januari
- Februari
- April
- Mei
- Juli
- Augustus
- Oktober
- November

>[!NOTE]
>April en oktober zijn belangrijke releasewaves voor functies. Klanten kunnen een afzonderlijke service-update onderbreken voor maximaal drie opeenvolgende updatecycli.

Raadpleeg de volgende onderwerpen voor meer informatie:

- [Overzicht van One Version-service-updates](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Service-updates configureren via LCS](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Service-updates onderbreken via LCS](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Berichten ontvangen over service-updates via LCS](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Testprogramma's voor regressie om service-updates te valideren](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365 roadmap en releasewaves](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Beveiliging en beheerderstoegang

De beheertoegang tot Finance and Operations-productieomgeving wordt streng geregeld en bijgehouden. Klantgegevens worden verwerkt in overeenstemming met de voorwaarden van [Microsoft Online Services](https://www.microsoft.com/licensing/terms/productoffering). 

### <a name="customer-administrative-access"></a>Beheerdertoegang voor klanten

De tenantbeheerder van de klant heeft toegang tot productie-exemplaren of niet-productie-exemplaren, zoals beschreven in de volgende tabel:

| Omgevingstype | Doel | Niveau van klanttoegang |
|---|---|---|
| **Niet-productie**<br>Sandbox van niveau 1 | Een niet-productieomgeving die door klanten wordt geïmplementeerd voor ontwikkelings-, demonstratie- of trainingsdoeleinden. | Een sandbox van niveau 1 (ook wel een cloud-hostomgeving genoemd) is een door de klant beheerde VM die wordt geïmplementeerd in het Azure-abonnement van de klant vanuit LCS. Omdat het een VM is in het Abonnement op Azure van de klant, heeft de klant volledige beheertoegang tot de omgeving via Extern bureaublad. |
| **Niet-productie**<br>Tier 2 (of hoger) sandbox | Een niet-productieomgeving die door klanten wordt geïmplementeerd voor acceptatietests voor gebruikers, integratietests, training, fasering of andere scenario's vóór de productie. | Tier 2 en hogere sandboxes worden geïmplementeerd in het Finance and Operations-SaaS-abonnement. Toegang tot Azure SQL-databases die aan de niet-productieomgeving zijn gekoppeld, wordt verleend via [just-in-time toegang](../../dev-itpro/database/database-just-in-time-jit-access.md). Toegang tot extern bureaublad is niet beschikbaar. |
| **Productie** | Een productieomgeving wordt geïmplementeerd wanneer het project gereed is [voor eerste go-live](/imp-lifecycle/environment-planning.md#production-system-readiness). | Productieomgevingen worden geïmplementeerd in het SaaS-abonnement. Alle toegang is via de browser, service-eindpunten of LCS. |

### <a name="microsoft-administrative-access"></a>Microsoft-beheerderstoegang

De volgende tabel toont de verschillende toegangsniveaus voor verschillende Microsoft-beheerders:

| Beheerder | Klantgegevens |
|---|---|
| Operationeel responsteam<br>(Alleen beperkt tot sleutelpersoneel) | Toegang wordt verleend via een supportticket. De toegang wordt gecontroleerd en beperkt tot de duur van de ondersteuningsactiviteit. |
| Microsoft klantondersteuning (Customer Support Services, CSS) | Geen directe toegang. Klant kan schermdeling gebruiken om te werken met ondersteuningspersoneel voor foutopsporing van problemen. |
| Engineering | Geen directe toegang. Het operationeel responsteam kan schermdeling gebruiken om te werken met engineering voor foutopsporing voor problemen. |
| Overige in Microsoft | Geen toegang. |

## <a name="monitoring"></a>Controle

Microsoft heeft geïnvesteerd in een uitgebreide toolset om de productie-exemplaren van klanten te monitoren en diagnosticeren. Microsoft controleert de productieomgevingen van klanten 24 uur per dag, zeven dagen per week. Zie [Productieondersteuning en -controle](../imp-lifecycle/production-support-monitoring.md) voor meer informatie.

| Verantwoordelijkheden van Microsoft | Verantwoordelijkheden van klant |
|---|---|
| <ul><li>De beschikbaarheid van de service controleren.</li><li>Voortdurend bewaken en waarschuwen via gezondheidsstatistieken en waakhonden voor kritieke componenten zoals Application Object Server (AOS), Batch, Data Import/Export Framework (DIXF), Commerce en Management Reporter.</li><li>Controleren op prestatieverbetering die wordt veroorzaakt door infrastructuurservices (zoals Azure Active Directory \[Azure AD\] en Azure SQL).</li><li>Als Microsoft vaststelt dat een enkel proces of batchtaak afwijkingen veroorzaakt, wordt dat proces of die taak beëindigd na communicatie met de klant.</li></ul> | <ul><li>Wijzigingen in toepassingsconfiguraties en extensies controleren die kunnen leiden tot functionele problemen en prestatieproblemen.</li><li>Toepassingsfouten moeten worden gecontroleerd door gebruik te maken van de controleprogramma's. Gebruik deze functies om een diagnose te maken van door de gebruiker gerapporteerde prestatieafwijkingen.</li><li>Microsoft informeren als er wordt verwacht dat er belasting op het systeem wordt geladen boven het verwachte piekgebruik.</li><li>Als de toepasselijke service niet beschikbaar is in het productie-exemplaar, kan de klant LCS gebruiken om een [productie-uitval](../../dev-itpro/lifecycle-services/report-production-outage.md) te rapporteren.</li></ul> |

Door online ondersteuningsverzoeken in te dienen, via LCS, stellen klanten Microsoft in staat om snelle en diepgaande technische expertise op de meest effectieve en efficiënte manier te leveren. Hoewel er een telefoonoptie beschikbaar is, moet u deze alleen gebruiken als de online optie niet beschikbaar is. Zie [Ondersteuning via telefoon](/power-platform/admin/support-overview.md?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&bc=/dynamics365/breadcrumb/toc.json#is-there-a-phone-number-i-can-call-to-contact-support) voor meer informatie.

## <a name="incident-management"></a>Incidenten beheren

Microsoft reageert op en repareert incidenten op basis van ernstniveaus. De ernstniveaus van incidenten van Microsoft kunnen worden gewijzigd tijdens de eerste beoordeling van het incident en naarmate er meer informatie over de impact en reikwijdte beschikbaar komt. Als het incident wordt beperkt, blijft de ernst van het incident ongewijzigd.

Zie deze [ernsttabel](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request) voor meer informatie over ernstsniveaus.

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Bedrijfscontinuïteit door hoge beschikbaarheid en noodherstel 

Microsoft biedt bedrijfscontinuïteit en noodherstel voor productie-instanties van Finance and Operations-apps in het geval van storingen in de hele Azure-regio. Zie [Bedrijfscontiteit en herstel](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md) voor meer informatie.

- **Hoge beschikbaarheid**: De HA-functionaliteit biedt manieren om uitvaltijd te voorkomen die wordt veroorzaakt door het mislukken van één knooppunt in een Azure-systeem. De cloudarchitectuur van elke service maakt gebruik van Azure-beschikbaarheidssets voor de rekenlaag om single-point-of-failure-gebeurtenissen te voorkomen. HA voor databases wordt geleverd via [Azure SQL HA-functies](/azure/azure-sql/database/high-availability-sla).
- **Noodherstel** – [Azure-functies voor noodherstel](/azure/best-practices-availability-paired-regions) beschermen elke service tegen storingen die een heel Azure-datacenter in grote lijnen treffen. Dit zijn enkele van deze functies:

    - Azure SQL active-geo-replicatie voor de primaire database (bedrijfsdatabase).
    - Geo-redundante kopieën van Azure Blob Storage (die documentbijlagen bevat) in andere Azure-regio's.
    - Secundaire regio voor de Azure SQL- en Azure Blob Storage-replicaties.

De primaire gegevensarchieven zijn ondersteund voor replicatie. Daarom gebruiken onderdelen voor elke service, zoals Management Reporter en entiteitsopslag, transformatiegegevens uit de primaire database. Deze gegevens moeten worden gegenereerd nadat de herstelsite is ingesteld en de service is gestart. Klantcode-artefacten en herstelde gegevensarchieven worden gebruikt om de site opnieuw te implementeren. Met de nieuweployment kunnen de status van de berekende knooppunten samen met deze en andere onderdelen worden gebruikt om de herstelde gegevensopslagpunten te gebruiken om de secundaire site in te stellen. Als noodherstel wordt gebruikt om het productie-exemplaar van de klant te herstellen, voldoen Microsoft en de klant aan hun [verantwoordelijkheden bij](service-description.md#incident-management) incidentbeheer.

De plannen en procedures voor noodherstel van Microsoft worden regelmatig onderzocht door middel van System and Organization Controls (SOC)-audits. Deze compliance-audits getuigen van het technische en procedurele proces van Microsoft's DR, inclusief Dynamics 365 Finance and Operations-toepassingen. [SoC-conformiteitscontrolerapporten](/compliance/regulatory/offering-soc-2) en alle andere conformiteitsrapporten zijn beschikbaar op het [nalevingsaanbod van het Microsoft Trust Center](/compliance/regulatory/offering-home).

| Verantwoordelijkheden van Microsoft | Verantwoordelijkheden van klant |
|---|---|
| Microsoft biedt een secundaire omgeving in het aan Azure gekoppelde exemplaar wanneer het primaire productie-exemplaar wordt geïmplementeerd. Zie [Bedrijfscontinuïteit en herstel na noodgeval (BCDR of Business Continuity and Disaster Recovery): gekoppelde Azure-regio's](/azure/best-practices-availability-paired-regions) voor meer informatie. | None |
| Microsoft schakelt de geografische opslag van SQL SQL en Azure cloud in wanneer het primaire productie-exemplaar wordt geïmplementeerd. | None |
| Microsoft schakelt automatische back-up van de SQL-databases in Azure in. | None |
| <p>Bij een storing bepaalt Microsoft of een failover moet worden uitgevoerd voor de klant en of er gegevens verloren gaan. Klanten kunnen een gegevensverlies van maximaal 15 minuten ervaren, afhankelijk van de aard en timing van de uitval. | In het geval van gegevensverlies, moet de klant mogelijk een schriftelijke ondertekening aanleveren om de failover te activeren. |
| Wanneer een failover optreedt, werkt de toepasselijke service in beperkte modus. Updateonderhoud kan niet worden geactiveerd in de failovermodus. | De klant kan geen pakketimplementaties of andere regelmatige onderhoudsaanvragen aanvragen in de failovermodus. |
| Wanneer het datacenter operationeel wordt, valt Microsoft terug op het productie-exemplaar in de primaire Azure-regio. Normale bewerkingen worden hervat. | De klant moet mogelijk tekenen voor failback naar het productie-exemplaar in de primaire Azure-regio. |

## <a name="finance-and-operations-support-offerings"></a>Finance and Operations-ondersteuningsaanbiedingen

Technische ondersteuning is beschikbaar in markten waar Finance and Operations-services worden aangeboden. [Ondersteuningservaringen](../../dev-itpro/lifecycle-services/lcs-support.md) worden geleverd in LCS of Finance and Operations-apps. Hieronder volgen een aantal voorbeelden:

- [Problemen zoeken](../../dev-itpro/lifecycle-services/issue-search-lcs.md) in LCS
- [Geïntegreerde technische ondersteuning](../../dev-itpro/lifecycle-services/support-experience.md) in Finance and Operations-toepassingen
- [Cloudondersteuning](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) in LCS

Microsoft biedt Finance and Operations-klanten drie ondersteuningsplannen: Premier, Professional Direct en de ondersteuning die is opgenomen in het abonnement. Het ondersteuningsniveau per plan verschilt. De volgende tabel toont een vergelijking van de drie plannen.

| Ondersteuningsfunctie | Premier | Professional Direct | Abonnement |
|---|---|---|---|
| Onbeperkte indiening van onderbreking/reparatie-incidenten | Ja | Ja | Ja |
| 24/7 toegang via LCS | Ja | Ja | Ja |
| Responstijd incident | Minder dan één uur | Minder dan één uur | Volgende werkdag |
| Adviesuren | Pools worden per overeenkomst verworven. | Nee | Nee |
| Specifieke accountmanager voor ondersteuning | Ja | Nee | Nee |
| Specifieke ondersteuningstechnicus | Onder een afzonderlijke overeenkomst | Nee | Nee |

Zie [Overzicht van ondersteuning](/power-platform/admin/support-overview) voor meer informatie.

### <a name="process-to-engage-support"></a>Proces om ondersteuning te krijgen

Bij incidenten waarbij zijn Finance and Operations-toepassingen betrokken zijn, dienen klanten via LCS ondersteuningstickets in bij Microsoft. CSS verwerkt de incidenten op basis van het ondersteuningsplan van de klant en de ernst van het incident zoals aangegeven door CSS.

### <a name="service-level-agreement"></a>Servicelevelovereenkomst

Microsoft heeft een beschikbaarheidspercentage van 99,9 procent per maand van de service toegezegd. Als Microsoft het serviceniveau voor de toepasselijke service niet behoudt zoals wordt beschreven in de serviceovereenkomst (SLA), kan de klant in aanmerking komen voor een krediet voor een deel van de maandelijkse servicekosten voor die service. Zie de sectie "Claims" van de serviceservice voor informatie over het starten van een [servicekrediet](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Belangrijke resources

- **[Vertrouwenscentrum](https://www.microsoft.com/trust-center)** – Krijg informatie over waar uw Finance and Operations-gegevens zijn opgeslagen, plus aanvullende informatie over privacy-, compliance- en beveiligingsprocedures.
- **[Licentievoorwaarden en -documentatie](https://www.microsoftvolumelicensing.com/)** – Krijg snel toegang tot licentievoorwaarden, -voorwaarden en aanvullende informatie die relevant is voor het gebruik van producten en services die zijn gelicentieerd via Microsoft-volumelicentieprogramma's.
- **[Licentievoorwaarden](https://www.microsoft.com/licensing/product-licensing/)**- De resources op deze pagina definiëren de algemene voorwaarden voor de software en onlineserviceproducten die u aanschaft via commerciële licentieprogramma's van Microsoft.
- **[Microsoft-levenscyclusbeleid](/lifecycle/)** – deze pagina biedt consistente en voorspelbaare richtlijnen voor de beschikbaarheid van ondersteuning gedurende de levensduur van een product.
- **[Licentiehandleiding](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – gebruik deze handleiding om meer te weten te komen over de licentie voor Dynamics 365.
- **[Klantenondersteuning](https://dynamics.microsoft.com/support/)** – Krijg toonaangevende ondersteuning voor uw Dynamics 365-apps.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** - Beheer de levenscyclus van uw toepasing en ga naar voorspelbare, herhaalbare, hoogwaardige implementaties.
- **[Implementatiehandleiding van Dynamics 365](https://aka.ms/D365ImplementationGuideFlip)** - De implementatiehandleiding van Dynamics 365 documenteert beproefde Success by Design-principes en biedt richtlijnen voor architectuur, bouw, test en implementatie van Dynamics 365-oplossingen.

## <a name="definitions"></a>Definities

### <a name="azure-region"></a>[Azure-regio](/azure/availability-zones/az-overview#regions)

Een geografische regio waar een of meer Azure-datacenters bestaan. Voorbeelden zijn de VS en europa.

### <a name="business-process-modeler-bpm"></a>[Modelleertool bedrijfsprocessen (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md)

Een tool in LCS die helpt bij het voltooien van een fit-gap-analyse voor een bepaalde implementatie door gebruik te maken van bedrijfsprocesdefinities van het American Productivity & Quality Center (APQC) die worden ondersteund in Finance and Operations-toepassingen.

### <a name="cloud-solution-provider"></a>Cloudoplossingsprovider

Een partner die deel uitmaakt van het Microsoft Cloud Solution Provider (CSP)-programma en die klanten cloudservices met toegevoegde waarde, ondersteuning, één factuur en klantenbeheer op schaal biedt ondersteuning, één factuur en klantbeheer.

### <a name="customer"></a>Klant

Een bedrijfsentiteit die Finance and Operations-toepassingen gebruikt en door een tenant wordt vertegenwoordigd in Office 365.

### <a name="development-environment"></a>Ontwikkelingsomgeving

Een niet-productieomgeving die wordt gebruikt om uitbreidingen te ontwikkelen. Klanten implementeren deze omgeving in hun eigen Azure-abonnement vanuit LCS. Deze omgeving kan ook worden gebruikt voor demonstratie, training of andere testtaken. Ditwordt ook een [Sandbox van niveau 1](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher) genoemd.

### <a name="downtime"></a>Uitvaltijd

Elke periode waarin gebruikers zich niet kunnen aanmelden of toegang hebben tot hun actieve tenant vanwege een storing in het niet-verlopen platform of de service-infrastructuur, zoals Microsoft bepaalt op basis van geautomatiseerde statusbewaking en systeemlogboeken. Downtime omvat niet geplande downtime, het niet beschikbaar zijn van service-add-onfuncties, de onmogelijkheid om toegang te krijgen tot de service vanwege uw wijzigingen aan de service, of perioden waarin de capaciteit van de schaaleenheid wordt overschreden.

### <a name="implementation-partner"></a>Implementatiepartner

De partner die de klant selecteert om de Finance and Operations-oplossingen aan te passen, te configureren, te implementeren en te beheren.

### <a name="incident"></a>Incident

Een probleem dat klanten tegenkomen terwijl ze de Finance and Operations-service gebruiken en waarvoor ze een ticket indienen via LCS.

### <a name="microsoft-customer-support-services-css"></a>Microsoft Customer Support Services (CSS)

Het Microsoft-globale ondersteuningsteam dat zich richt op het leveren van kwaliteitsservice voor Finance and Operations-toepassingen.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

De administratieve portal voor levenscyclusbeheer van Finance and Operations-apps, van proef tot implementatie, tot postproductiebeheer en ondersteuning. Zie voor meer informatie [Lifecycle Services-resources](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Niet-productie-exemplaar

Elk van de volgende exemplaren van een service die de klant gebruikt om extensies te valideren en andere ontwikkelingstaken uit te voeren:

- **Sandbox van niveau 1** – Ontwikkelaar-exemplaar (door een klant gehost)
- **Sandbox Tier 2** – Exemplaar voor standaard acceptatietests
- **Sandbox Tiers 3–5** – Bijkomende sandboxes

Voor meer info over Tiers 2 tot 5, zie [De juiste Tier-2 of hogere omgeving selecteren](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Productie-exemplaar

Een Finance and Operations-omgeving waarin de klant de dagelijkse live transacties en bedrijfsprocessen beheert.

### <a name="sandbox-environment"></a>Sandbox-omgeving

Een niet-productieomgeving die door de klant wordt gebruikt voor demonstratie, training, acceptatie van gebruikers, validatie van uitbreidingen en andere testtaken.

### <a name="service"></a>Service

Alle kernservices die zijn opgenomen in Finance and Operations-toepassingen.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Serviceovereenkomst (SLA) voor onlineservices van Microsoft

De SLA is van toepassing op de onlineservices van Microsoft. Zie voor meer informatie [SLA's](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Serviceupdate

Microsoft onderhoudt Finance and Operations-omgevingen op consistente basis via service-updates. Klanten stellen hun eigen kalender voor service-updates in op basis van hun zakelijke behoeften. Meer informatie over dit onderwerp vindt u in [Veelgestelde vragen over updates van service met één versie](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Het raamwerk dat een implementatie systematisch door een reeks evaluaties in belangrijke fasen begeleidt om te zorgen voor een optimale architectuur, beveiliging, prestaties en gebruikerservaring voor een Dynamics 365-oplossing.

### <a name="user"></a>Gebruiker

Eén enkele persoon die Finance and Operations-omgevingen gebruikt en die is gekoppeld aan de tenant van een klant.
