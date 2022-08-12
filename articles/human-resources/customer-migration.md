---
title: Veelgestelde vragen over Human Resources-klantmigratie
description: In dit artikel worden veelgestelde vragen beantwoord over de migratie van Microsoft Dynamics 365 Human Resources naar de samengevoegde infrastructuur voor financiën en bedrijfsactiviteiten.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a6f883da07bd1d3a6b0379f1582dc8556e166ff
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151078"
---
# <a name="human-resources-customer-migration"></a>Human Resources-klantmigratie

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Hoe kunnen klanten van Dynamics 365 Human Resources overstappen naar de infrastructuur voor financiën en bedrijfsactiviteiten?

Twee categorieën van klanten van Microsoft Dynamics 365 Human Resources worden beïnvloed en moeten wijzigingen aanbrengen om ervoor te zorgen dat ze gebruik maken van de meest recente infrastructuur voor financiën en bedrijfsactiviteiten:

- Klanten die Dynamics 365 Human Resources gebruiken en geen andere apps voor bedrijfsactiviteiten van Dynamics 365 hebben
- Klanten die gebruikmaken van zowel Dynamics 365 Human Resources als Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce of Dynamics 365 Project Operations

Ongeacht de categorie waartoe klanten behoren, moeten ze gegevens verplaatsen naar een nieuwe omgeving in de infrastructuur voor financiën en bedrijfsactiviteiten en moeten ze controleren of de samenvoeging met succes is voltooid.

In de toekomst zal de Dynamics 365 Human Resources-app een eigen omgeving voor financiën en bedrijfsactiviteiten hebben die los staat van andere apps voor bedrijfsactiviteiten. Op deze manier kunnen klanten gebruik maken van opties voor uitbreidbaarheid zonder dat hun huidige gegevens moeten worden samengevoegd. Microsoft biedt hulpmiddelen en een sandbox-omgeving waarin klanten de gegevensmigratie kunnen testen en valideren voordat ze naar een productieomgeving overstappen. De hulpmiddelen maken een bijna geautomatiseerd proces mogelijk en zijn beschikbaar tussen augustus en november 2022.

Klanten die andere apps in de infrastructuur voor financiën en bedrijfsactiviteiten gebruiken, hebben de mogelijkheid om hun Human Resources-gegevens samen te voegen met een bestaande omgeving. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Wanneer vindt voor klanten de overstap naar de infrastructuur voor financiën en bedrijfsactiviteiten plaats?

De overgang voor elk bedrijf is afhankelijk van de huidige configuratie van dat bedrijf en de gereedheid om naar de infrastructuur voor financiën en bedrijfsactiviteiten over te stappen. Klanten worden aangeraden samen met hun Microsoft-partner het beste pad vooruit te bepalen.

- Organisaties die de module **Human Resources** gebruiken in Dynamics 365 Finance kunnen nieuwe mogelijkheden van Dynamics 365 Human Resources inschakelen als onderdeel van het normale One Version-updateproces. Volgens planning zullen vanaf januari 2022 nieuwe functies algemeen beschikbaar komen.
- Organisaties die gebruik maken van Dynamics 365 Human Resources, hebben toegang tot hulpmiddelen die ze kunnen gebruiken om de infrastructuursamenvoeging te voltooien. Microsoft werkt samen met klanten aan de overgang om enige onderbreking in de service te voorkomen. Klanten hebben 12 tot 18 maanden de tijd om de overgang te maken, te beginnen vanaf het moment waarop de migratiehulpmiddelen beschikbaar komen.
- Organisaties die gebruikmaken van zowel Dynamics 365 Human Resources als de module **Human Resources**, kunnen hun eigen Human Resources-infrastructuur verplaatsen naar de infrastructuur voor financiën en bedrijfsactiviteiten. Een andere optie is de samenvoeghulpmiddelen te gebruiken om de omgevingen in één omgeving samen te brengen. Er is geen vereiste of tijdsbestek voor het samenvoegen van de twee omgevingen.

Controleer de [Releaseplannen](/dynamics365/release-plans/) regelmatig voor bijgewerkte informatie.

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Hebben klanten nog aangepaste integraties tussen Dynamics 365 Human Resources en de Human Resources-module nodig?

- Klanten die zowel een omgeving met Dynamics 365 Human Resources als een omgeving met een infrastructuur voor financiën en bedrijfsactiviteiten hebben die momenteel worden geïntegreerd, moeten de twee omgevingen blijven integreren na de samenvoeging.
- Klanten die ervoor kiezen hun Dynamics 365 Human Resources-omgeving gescheiden te houden van hun bestaande omgeving met de app voor financiën en bedrijfsactiviteiten, moeten de omgevingen blijven integreren om de gegevens beschikbaar te maken in beide omgevingen.
- Klanten kunnen de Data Integrator blijven gebruiken om gegevens tussen de twee omgevingen te kopiëren. Klanten die gegevens na de migratie in één omgeving samenvoegen, hoeven de gegevens niet meer te integreren omdat alle gegevens zich in één database bevinden.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Worden ISV-oplossingen van klanten automatisch gemigreerd?

De migratie-ervaring voor elke ISV-oplossing (Independent Software Vendor) is afhankelijk van de integratiemethode van de oplossing. Microsoft werkt nauw samen met ISV's om te zorgen voor een probleemloze overgang naar de nieuwe infrastructuur voor financiën en bedrijfsactiviteiten. Veel ISV-oplossingen worden gebaseerd op Dataverse met behulp van de mogelijkheden van Microsoft Power Platform. Deze oplossingen hangen af van de Dataverse-integratie tussen de Dynamics 365 Human Resources-omgeving en de Dataverse-omgeving. De Dataverse-integratie wordt afgeschaft als onderdeel van de samenvoeging van de infrastructuur. In de infrastructuur voor financiën en bedrijfsactiviteiten zijn nieuwe toewijzingen voor twee keer wegschrijven gepland ter vervanging van de functionaliteit van de Dataverse-integratie.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Hoe is een en ander van invloed op Gegevensintegrator waarmee gegevens tussen Dynamics 365 Human Resources en andere Dynamics 365-toepassingen worden verplaatst?

Nadat klanten naar de infrastructuur voor financiën en bedrijfsactiviteiten zijn overgestapt, moeten ze gegevens tussen de twee omgevingen blijven integreren. Klanten kunnen de Gegevensintegrator blijven gebruiken om deze taken voor gegevensmigratie uit te voeren. Klanten die van plan zijn hun Dynamics 365 Human Resources-omgeving gescheiden te houden van hun bestaande omgeving met de apps voor financiën en bedrijfsactiviteiten, moeten de gegevens tussen de twee omgevingen blijven integreren. Voor klanten die de twee omgevingen samenvoegen in één omgeving, is integratie tussen de twee omgevingen niet langer vereist.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Hoe worden gegevens tussen Dynamics 365 Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten en Dataverse na de migratie verplaatst?

De huidige Dataverse-integratie tussen Dynamics 365 Human Resources en Dataverse wordt afgeschaft als onderdeel van de infrastructuur voor financiën en bedrijfsactiviteiten. Er zijn plannen voor het introduceren van toewijzingen voor twee keer wegschrijven om de entiteiten voor financiën en bedrijfsactiviteiten aan de Dataverse-tabellen toe te wijzen. Klanten moeten bepalen welke toewijzingen voor twee keer wegschrijven vereist zijn voor de implementatie. U wordt aangeraden virtuele tabellen te gebruiken voor integraties en ISV-oplossingen, tenzij er een specifieke zakelijke behoefte bestaat om de gegevens in Dataverse te dupliceren om bedrijfslogica uit te voeren.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Hoe is de migratie van invloed op Dataverse-uitbreidingen voor Dynamics 365 Human Resources?

Klanten moeten een migratie naar een sandbox-omgeving maken voordat ze hun productieomgeving migreren. Wanneer klanten hun sandbox-omgeving migreren, moeten ze een kopie van hun Dataverse-omgeving maken om verbinding te maken met de nieuwe gemigreerde omgeving voor financiën en bedrijfsactiviteiten. Wij raden aan dat een klant zowel de gegevens als de oplossingen voor de omgeving kopieert, zodat deze overeenkomen met de huidige productieomgeving van de klant.

Wanneer klanten klaar zijn om hun Dynamics 365 Human Resources-productieomgeving te migreren, migreert Microsoft automatisch de database en Azure Blob Storage. De gemigreerde database en opslag verwijzen de nieuwe omgeving in de infrastructuur voor financiën en bedrijfsactiviteiten naar dezelfde Dataverse-productieomgeving. Voordat de gegevens verder naar Dataverse kunnen worden gekopieerd, moeten klanten alle toewijzingen voor twee keer wegschrijven inschakelen die vereist zijn voor hun integraties, uitbreidingen en ISV-oplossingen die zijn gebaseerd op Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Werken Microsoft Power Platform-onderdelen die zijn gebouwd voor Dynamics 365 Human Resources automatisch nadat de infrastructuurmigratie is voltooid?

Apps die worden gemaakt in Power Apps, stromen die worden gemaakt in Power Automate en andere Microsoft Power Platform-aanpassingen zijn als Dataverse-uitbreidingen. Tijdens de migratie van productieomgevingen van klanten heeft dit geen invloed op Dataverse-omgevingen, zoals uitbreidingen. Apps, stromen en andere aanpassingen van Power Microsoft platform moeten blijven werken zonder dat er nog meer configuratie nodig is.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Wat gebeurt er met virtuele Dataverse-tabelentiteiten voor Dynamics 365 Human Resources tijdens de migratie?

Wanneer klanten hun Dynamics 365 Human Resources-omgeving migreren naar de infrastructuur voor financiën en bedrijfsactiviteiten, blijft de omgeving verbonden met de Dataverse-omgeving die momenteel is verbonden met Dynamics 365 Human Resources. De virtuele Dataverse-tabellen die in de omgeving zijn gegenereerd, blijven werken zonder dat er nog meer configuratie nodig is. De virtuele tabellen moeten mogelijk opnieuw worden gegenereerd in de Dataverse-omgeving die is verbonden met een bestaande omgeving voor financiën en bedrijfsactiviteiten van een klant.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Hoe werkt een integratie waarin de API voor ATS (Applicant Tracking System), API voor salarisadministratie, virtuele Dataverse-tabellen voor Dynamics 365 Human Resources of andere entiteiten in de web-API van Dataverse worden gebruikt nadat de samenvoeging van de infrastructuur is voltooid?

Wanneer klanten hun Dynamics 365 Human Resources-omgeving migreren naar de infrastructuur voor financiën en bedrijfsactiviteiten, blijft de omgeving verbonden met de Dataverse-omgeving die momenteel is verbonden met Dynamics 365 Human Resources. Alle integraties die zijn ontwikkeld met de web-API Dataverse, blijven werken nadat de migratie is voltooid.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Onze organisatie heeft aangepaste beveiliging geconfigureerd in Dynamics 365 Human Resources. Wordt deze nog steeds toegepast nadat de infrastructuurmigratie is voltooid?

Ja, aangepaste beveiligingsconfiguraties worden opgenomen in de gegevensmigratie.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Worden workflows in Dynamics 365 Human Resources automatisch gemigreerd?

Ja, workflowconfiguraties, workflowhistorie en huidige workflows in het proces worden gemigreerd naar de samengevoegde infrastructuur.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Worden opgeslagen weergaven in Dynamics 365 Human Resources automatisch gemigreerd?

Ja, opgeslagen weergaven worden naar de samengevoegde infrastructuur gemigreerd.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Zijn functies die zijn ingeschakeld in Dynamics 365 Human Resources automatisch beschikbaar nadat de infrastructuursamenvoeging is voltooid?

- Voor klanten die de module **Human Resources** gebruiken, worden functies die alleen beschikbaar zijn in Dynamics 365 Human Resources via Functiebeheer beheerd. Meestal zijn deze functies niet standaard ingeschakeld. Alle functies die standaard moeten worden ingeschakeld, worden gedocumenteerd.
- Voor klanten die Dynamics 365 Human Resources gebruiken, zijn functies in de infrastructuur beschikbaar. Functies die niet beschikbaar zijn, worden gedocumenteerd. Elke Functiebeheer-sleutel die in de huidige Dynamics 365 Human Resources-omgeving is ingeschakeld, wordt ingeschakeld in de samengevoegde infrastructuur. Zie [Overzicht van functiebeheer](/fin-ops/get-started/feature-management-overview.md) voor meer informatie.

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Wat gebeurt er met BYOD-databases tijdens de migratie?

Import- en exportconfiguraties voor Bring Your Own Database (BYOD) worden naar de infrastructuur voor financiën en bedrijfsactiviteiten gemigreerd.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Zijn er gevolgen voor de Azure-regio wanneer de klantomgeving wordt gemigreerd?

De Dynamics 365 Human Resources-omgeving blijft voor de migratie in dezelfde Azure-regio. Als een omgeving moet worden verplaatst naar een andere Azure-regio, moeten klanten de standaardstappen volgen om naar een nieuwe regio te migreren nadat de migratie is voltooid.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Wat gebeurt er met Azure Data Lakes tijdens de migratie?

Elke export die momenteel is geconfigureerd voor Azure Data Lake in apps voor financiën en bedrijfsactiviteiten behoudt dezelfde configuratie na de migratie.

> [!NOTE]
> Toewijzingen voor twee keer wegschrijven moeten worden ingeschakeld om gegevens uit de Human Resources-omgeving naar Dataverse te blijven schrijven.

Klanten die Human Resources-gegevens naar de data lake willen exporteren, kunnen deze functie inschakelen nadat de migratie naar de infrastructuur voor financiën en bedrijfsactiviteiten is voltooid. Zie [Data lakes - Azure Architecture Center](/azure/architecture/data-guide/scenarios/data-lake) voor meer informatie.

Klanten kunnen meerdere omgevingen voor financiën en bedrijfsactiviteiten aan dezelfde data lake koppelen. Elke omgeving verwijst echter naar een andere map en container. Klanten die omgevingen later willen samenvoegen, moeten hun aanpak zorgvuldig plannen.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Welke migratie is vereist als een klant momenteel de module Human Resources gebruikt?

Voor klanten die de module **Human Resources** gebruiken, wordt de nieuwe functiefunctionaliteit van Dynamics 365 Human Resources toegepast op hun omgeving via het standaard One Version-updateproces. Klanten kunnen de nieuwe functionaliteit in hun omgeving verwachten wanneer deze in elke update beschikbaar komt. Klanten kunnen Functiebeheer gebruiken om de functies in te schakelen. Klanten moeten validatie van deze nieuwe functies plannen met behulp van de processen die ze al hebben en andere updates van hun omgeving valideren.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Wat gebeurt er met aangepaste integraties met externe systemen?

Klanten moeten hun integraties met de omgeving voor financiën en bedrijfsactiviteiten migreren. Omdat het eindpunt van deze omgeving verschillend is, moeten klanten de integraties mogelijk bijwerken of wijzigen zodat ze naar de nieuwe omgeving verwijzen. Deze taak is voornamelijk een handmatig proces en de benodigde wijzigingen zijn afhankelijk van de architectuur van de integratie. Klanten moeten samenwerken met hun Microsoft-partner om de beste benadering voor het verplaatsen van integraties te bepalen.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Wat gebeurt er met uitbreidingen van Microsoft Power Platform (Dataverse) als klanten een Dynamics 365 Human Resources-omgeving samenvoegen met een bestaande omgeving voor financiën en bedrijfsactiviteiten?

Als klanten een Dynamics 365 Human Resources-omgeving een bestaande omgeving voor financiën en bedrijfsactiviteiten willen samenvoegen in één exemplaar van Dataverse na de migratie, moeten hun Dataverse-omgevingen worden gecombineerd als onderdeel van het samenvoegproces. Voor deze taak moeten alle apps die worden gemaakt met Power Apps en andere aanpassingen opnieuw worden geïmplementeerd in de nieuwe omgeving.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Wat gebeurt er met documenten tijdens de migratie?

Wanneer klanten hun Dynamics 365 Human Resources-omgeving migreren naar de infrastructuur voor financiën en bedrijfsactiviteiten, blijven de documenten in de bestaande documentopslag en worden ze automatisch aan de nieuwe omgeving in de infrastructuur voor financiën en bedrijfsactiviteiten toegewezen.

In een toekomstige release worden nieuwe gegevensentiteiten verschaft. Nadat die wijziging is aangebracht, kunnen klanten die ervoor kiezen hun Dynamics 365 Human Resources-omgeving samen te voegen met een bestaande omgeving voor financiën en bedrijfsactiviteiten, vervolgens documenten exporteren en deze naar de bestaande omgeving verplaatsen.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Wat gebeurt er na de migratie met de batchtaken die zijn geconfigureerd in Dynamics 365 Human Resources?

Batchtaken moeten opnieuw worden geconfigureerd in de omgeving voor financiën en bedrijfsactiviteiten. Klanten moeten elke batchtaak beoordelen en vergelijken met de huidige lijst met batchtaken in de omgeving voor financiën en bedrijfsactiviteiten. Klanten moeten ook de algehele batchplanning analyseren wanneer ze de twee sets batchtaken samenvoegen om te bepalen of wijzigingen moeten worden aangebracht in de batchplanning, prioriteiten of batchgroepen.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Welke gevolgen heeft de migratie voor het LCS-project voor Dynamics 365 Human Resources?

Klanten moeten een nieuw Microsoft Dynamics LCS-project (Lifecycle Service) maken en ze moeten apps voor financiën en bedrijfsactiviteiten selecteren als het product en **Implementatie** als het projecttype. Bovendien is een nieuw veld voor het subprojecttype beschikbaar wanneer een LCS-project wordt gemaakt. Klanten moeten de optie voor Dynamics 365 Human Resources-migratie selecteren om een bestaand Human Resources LCS-project te migreren naar de infrastructuur voor financiën en bedrijfsactiviteiten.

De functies van LCS-projecten voor financiën en bedrijfsactiviteiten verschillen van de functies van Human Resources LCS-projecten.

Nieuwe klanten moeten de volgende taken uitvoeren om live te kunnen gaan:

- Onboarding voor project voltooien.
- De methodologie voltooien.
- Een abonnementsschatting invullen.
- Het proces ter voorbereiding van go-live voltooien.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Hoe wordt de Modelleertool bedrijfsprocessen gemigreerd?

Klanten moeten hun bibliotheek van de Modelleertool bedrijfsprocessen exporteren vanuit het Human Resources LCS-project en deze importeren in het LCS-project voor financiën en bedrijfsactiviteiten. Verder moeten klanten de Help-instellingen in de toepassing bijwerken zodat deze naar het nieuwe LCS-project verwijzen.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Hoe wordt het service-updateproces beïnvloed door de migratie?

Na de migratie hebben klanten veel meer flexibiliteit met betrekking tot ALM (Application Lifecycle Management) en service-updates. Service-updates worden niet langer automatisch toegepast op Human Resources-omgevingen. In plaats daarvan volgt de service de updateprocessen en -functionaliteit van de One Version-service en worden configuratieopties voor updates via LCS ingeschakeld.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Komen klanten in aanmerking voor FastTrack-ondersteuning bij het samenvoegen van de infrastructuur?

Microsoft is nog steeds aan het bepalen welke hulpprogramma's en resources via FastTrack beschikbaar zijn om te helpen bij het samenvoegen.

## <a name="licensing-impact"></a>Licentie-impact

Zie [Veelgestelde vragen over Dynamics 365 Human Resources-infrastructuursamenvoeging](hr-infrastructure-merge-faq.md#licensing-impact) voor meer informatie over de gevolgen voor licenties.
