---
title: Veelgestelde vragen over infrastructuursamenvoeging voor Dynamics 365 Human Resources
description: In dit artikel worden veelgestelde vragen beantwoord over het samenvoegen van de infrastructuur voor Microsoft Dynamics 365 Human Resources en apps voor financiële en bedrijfsactiviteiten.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8c005f677624336b4194bebea6d69667182128b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880475"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Veelgestelde vragen over infrastructuursamenvoeging voor Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit artikel worden veelgestelde vragen beantwoord over het samenvoegen van de infrastructuur voor Microsoft Dynamics 365 Human Resources en apps voor financiële en bedrijfsactiviteiten.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Wat is de infrastructuursamenvoeging voor Dynamics 365 Human Resources?

Dynamics 365 Human Resources is een zelfstandige toepassing die een andere infrastructuur gebruikt dan andere apps voor financiën en bedrijfsactiviteiten, zoals Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce en Dynamics 365 Project Operations. Door de infrastructuursamenvoeging krijgt Dynamics 365 Human Resources dezelfde infrastructuur als andere apps voor financiële en bedrijfsactiviteiten.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Toegevoegde waarde en voordelen van de infrastructuursamenvoeging

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Mijn organisatie gebruikt Dynamics 365 Human Resources om de eigen HR-bewerkingen te beheren. Welke voordelen zullen deze wijzigingen ons bieden?

- Door deze wijzigingen wordt een einde gemaakt aan de verwarring door meerdere sets HR-capaciteiten in Dynamics 365.
- Ze bieden zowel uitbreidbaarheid voor Microsoft Power Platform als een manier om bedrijfslogica en functieopties uit te breiden.
- Deze zorgen voor consistentie tussen Dynamics 365 Human Resources en andere apps voor financiële en bedrijfsactiviteiten in termen van AlM (Application Lifecycle Management), Microsoft Dynamics Lifecycle Services (LCS), geografische beschikbaarheid, uitbreidbaarheid en meer.
- Met deze services kunt u profiteren van gedeelde services en hulpprogramma's en de kosten helpen verlagen.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Mijn organisatie gebruikt de Human Resources-module in Dynamics 365 Finance, Supply Chain Management, Commerce of Project Operations. Welke voordelen zullen deze wijzigingen ons bieden?

De capaciteiten en investeringen die zijn gedaan in Dynamics 365 Human Resources komen nu beschikbaar voor klanten die gebruikmaken van de HR-module in Dynamics 365 Finance. Tot een aantal van deze capaciteiten behoren verlof- en verzuimbeheer, vergoedingenbeheer en taakbeheer.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Raak ik alle functies of capaciteiten kwijt die ik momenteel gebruik?

Er zal functionele pariteit zijn tussen Dynamics 365 Human Resources en de HR-module in apps voor financiële en bedrijfsactiviteiten. Dynamics 365 Human Resources krijgt voorrang bij overeenkomstige functies. Zie [Overzicht van functiebeheer](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.

### <a name="will-the-experience-change-for-my-users"></a>Zal de ervaring voor mijn gebruikers veranderen?

De nieuwe HR-capaciteiten worden beheerd via Functiebeheer. Klanten bepalen of ze ze willen behouden. In sommige gevallen veranderen de mogelijkheden. In die gevallen wordt documentatie geleverd.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Wat is de invloed van deze wijziging op mij als ik een bestaande klant ben en zowel de HR-module in de Finance and Operations-infrastructuur als Dynamics 365 Human Resources gebruik via aangepaste integraties?

Aangepaste integraties tussen Dynamics 365 Human Resources en de HR-module in Dynamics 365 Finance zijn niet langer vereist. Alle HR-gegevens bevinden zich in dezelfde database als andere apps voor financiële en bedrijfsactiviteiten.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Migratie van Dynamics 365 Human Resources naar apps voor financiële en bedrijfsactiviteiten

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Mijn organisatie gebruikt Dynamics 365 Human Resources om HR-bewerkingen te beheren. Waarvoor moeten we plannen om naar de nieuwe ervaring te migreren?

Als uw organisatie gebruikmaakt van Dynamics 365 Human Resources, maar geen andere apps voor financiële en bedrijfsactiviteiten gebruikt, wordt uw Human Resources-omgeving naar de nieuwe infrastructuur gemigreerd. Eeen groot deel van dit migratieproces wordt geautomatiseerd. Er komen processen voor het migreren van de database en het synchroniseren hiervan met de nieuwe infrastructuur.

Daarnaast komt er tooling beschikbaar, zodat u het migratieproces kunt testen en uw gegevens en ervaring kunt valideren voordat u uw productieomgeving migreert.

Als uw organisatie zowel Dynamics 365 Human Resources als andere apps voor financiële en bedrijfsactiviteiten gebruikt, moet u meer tijd inplannen voor validatie om ervoor te zorgen dat uw gegevens correct naar de nieuwe omgeving worden gemigreerd. Bij de migratie naar de nieuwe infrastructuur worden de gegevens van uw Human Resources-omgeving samengevoegd met uw client voor financiële en bedrijfsactiviteiten. In het geval van tegenstrijdige gegevens is gebruikersinvoer nodig om te bepalen hoe het conflict moet worden opgelost. Gebruikers en beheerders moeten de gegevenstoewijzingen beheren bij conflicten en de migratie in een andere omgeving testen vóór de migratie van productieomgevingen.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Mijn organisatie gebruikt de Human Resources-module in Dynamics 365 Finance, Supply Chain Management, Commerce of Project Operations. Waarvoor moeten we plannen om naar de nieuwe ervaring te migreren?

Voor organisaties die de HR-module gebruiken in apps voor financiële en bedrijfsactiviteiten wordt de nieuwe functiefunctionaliteit van Dynamics 365 Human Resources toegepast op uw omgeving via het standaard One Version-updateproces. U kunt de nieuwe functionaliteit in uw omgeving verwachten wanneer deze in elke update beschikbaar komt. U kunt Functiebeheer gebruiken om nieuwe functies in te stellen, maar u moet het valideren van deze functies wel inplannen. Volg de processen die u hebt ingericht voor het valideren van andere updates van uw omgeving. Zie [Overzicht van One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md) voor meer informatie over het toepassen van updates op apps voor financiële en bedrijfsactiviteiten.

### <a name="when-will-my-organization-be-migrated"></a>Wanneer wordt mijn organisatie gemigreerd?

De migratie voor elke organisatie is afhankelijk van de huidige configuratie en gereedheid om naar de nieuwe infrastructuur te migreren. Deze datums kunnen worden gewijzigd.

- Organisaties die momenteel de HR-module in apps voor financiële en bedrijfsactiviteiten gebruiken, ontvangen de HR-functionaliteit voor Dynamics 365 Human Resources als onderdeel van het normale One Version-updateproces. Volgens planning zullen vanaf januari 2022 nieuwe functies algemeen beschikbaar komen.
- Organisaties die alleen met Dynamics 365 Human Resources werken, hebben toegang tot migratieprogramma's, zodat ze vanaf midden 2022 kunnen beginnen met testen en het uitvoeren van de migratie. De datum waarop de migratie naar de nieuwe infrastructuur moet zijn voltooid, is nog niet vastgesteld. Het is echter ten minste één jaar na de datum waarop migratieprogramma's beschikbaar komt.
- Organisaties die momenteel zowel met Dynamics 365 Human Resources als met andere apps voor financiële en bedrijfsactiviteiten werken, hebben toegang tot migratieprogramma's, zodat ze vanaf eind 2022 kunnen beginnen met testen en het uitvoeren van de migratie. De datum waarop de migratie naar de nieuwe infrastructuur moet zijn voltooid, is nog niet vastgesteld. Het is echter ten minste één jaar na de datum waarop migratieprogramma's beschikbaar komt.

Zie [Nieuwe of gewijzigde functies in Human Resources](./hr-admin-whats-new.md) voor meer informatie over de nieuwe functies voor Dynamics 365 Human Resources.

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Mijn organisatie is nog niet live gegaan met Dynamics 365 Human Resources. Moeten we live gaan met de Human Resources-module in apps voor financiële en bedrijfsactiviteiten of met de Dynamics 365 Human Resources-app in de verouderde infrastructuur?

Belangrijke items om rekening mee te houden, zijn de benodigde HR-functionaliteit en het moment waarop die functionaliteit beschikbaar zal zijn op de nieuwe infrastructuur. Als de organisatie de basisfunctionaliteit voor personeelsbeheer nodig heeft, dan is die momenteel beschikbaar in de HR-module van de apps voor financiële en bedrijfsactiviteiten in de nieuwe infrastructuur. Functiepariteit tussen de HR-module van apps voor financiële en bedrijfsactiviteiten en de Dynamics 365 Human Resources-app is naar verwachting beschikbaar met release 10.0.25, die gepland staat voor algemene beschikbaarheid in maart 2022. Integratiefuncties zoals de integratie tussen de Teams-app en Dataverse-entiteit zijn beschikbaar in latere versies.

Als de HR-functionaliteit van de organisatie beschikbaar moet zijn in de nieuwe infrastructuur binnen de periode waarin de organisatie live gaat, is het mogelijk eenvoudiger om live te gaan in de Human Resources-module in de apps voor financiële en bedrijfsactiviteiten. Dit resulteert in een eenvoudiger migratie omdat het een standaardtoepassingsupgrade naar de Dynamics 365 Human Resources-toepassing is en de klant de nieuwe infrastructuur al in gebruik heeft. Als de organisatie besluit live te gaan op de Dynamics 365 Human Resources-toepassing op de verouderde infrastructuur, is een migratie van de omgeving nodig om naar de nieuwe infrastructuur over te stappen. Dit kan worden voorkomen door live te gaan op de nieuwe infrastructuur.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Ik gebruik nieuwe mogelijkheden die alleen beschikbaar zijn in Dynamics 365 Human Resources (zoals **Verlof en verzuim** en **Vergoedingenbeheer**). Zijn deze mogelijkheden nu ook beschikbaar in de module Human Resources in de Finance and Operations-infrastructuur?

Ja, alle modules van Dynamics 365 Human Resources werken net als in apps voor financiële en bedrijfsactiviteiten, met een functiepariteit van 100 procent. Als onderdeel van de algehele migratiestrategie voor klanten die momenteel deze mogelijkheden in HR gebruiken, worden klantgegevens gemigreerd zodat deze blijven werken binnen de Finance and Operations-infrastructuur.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Ik gebruik de nieuwe Dynamics 365 Human Resources-mogelijkheden voor vergoedingenbeheer. Ik heb aangepaste integraties met de HR-module opgebouwd in de Finance and Operations-infrastructuur, zodat ik gebruik kan maken van de salarismogelijkheden door gebruik te maken van vergoedingengegevens. Zijn deze aangepaste integraties in de toekomst vereist?

Als onderdeel van de infrastructuursamenvoeging worden HR-gegevens naar dezelfde database overgebracht als andere apps voor financiële en bedrijfsactiviteiten. Integratie tussen modules in apps voor financiële en bedrijfsactiviteiten is niet langer vereist.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Mijn organisatie gebruikt een of meer ISV-oplossingen met Dynamics 365 Human Resources. Worden onze ISV-oplossingen automatisch gemigreerd?

De migratie-ervaring voor elke ISV-oplossing (Independent Software Vendor) is afhankelijk van de integratiemethode van de oplossing. Microsoft werkt samen met ISV's om een probleemloze overgang naar de nieuwe infrastructuur te waarborgen.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Mijn organisatie maakt gebruik van integratie van LinkedIn Talent Hub met Dynamics 365 Human Resources. Blijft deze integratie werken nadat de infrastructuurwijziging is voltooid?

Nee, de integratie van LinkedIn Talent Hub blijft niet werken na de migratie naar de nieuwe infrastructuur. De service voor LinkedIn Talent Hub-integratie wordt samen met de verouderde Dynamics 365 Human Resources-infrastructuur afgeschaft.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Mijn organisatie gebruikt de Human Resources-app voor Teams. Blijft de app werken nadat de infrastructuurwijziging is voltooid?

Ja, de Human Resources-app voor Teams blijft werken na de migratie naar de nieuwe infrastructuur.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Mijn organisatie heeft aangepaste beveiliging geconfigureerd in Dynamics 365 Human Resources. Wordt onze aangepaste beveiliging nog steeds toegepast nadat de infrastructuurwijziging is voltooid?

Ja, aangepaste beveiligingsconfiguraties worden opgenomen in de gegevensmigratie naar de nieuwe infrastructuur.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>We gebruiken Data Integrator om gegevens te verplaatsen tussen Dynamics 365 Human Resources en apps voor financiële en bedrijfsactiviteiten. Wat zijn de gevolgen voor de gegevens die momenteel worden geïntegreerd?

HR-gegevens die momenteel in Dynamics 365 Human Resources staan, worden gesynchroniseerd met Dataverse. Vervolgens kan Data Integrator worden gebruikt voor synchronisatie in één richting met apps voor financiële en bedrijfsactiviteiten. Na de migratie naar de nieuwe infrastructuur zijn HR-gegevens native voor de apps voor financiële en bedrijfsactiviteiten. Data Integrator is niet langer nodig om de gegevens tussen apps voor financiële en bedrijfsactiviteiten en Human Resources te synchroniseren.

De huidige native Dataverse-gegevenstabellen voor Human Resources blijven de gegevens uit de omgeving in de nieuwe infrastructuur synchroniseren. De entiteiten worden geconverteerd voor ondersteuning van twee keer wegschrijven. Alle andere gegevensintegraties die via Data Integrator voor deze tabellen zijn geconfigureerd voor andere Dynamics 365-apps, blijven werken zoals ze momenteel zijn geconfigureerd.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Er wordt nu gebruikgemaakt van twee keer wegschrijven om HR-gegevens te verplaatsen tussen Dataverse en andere apps voor financiële en bedrijfsactiviteiten. Hoe worden de gegevens die momenteel worden geïntegreerd, beïnvloed door de migratie naar de nieuwe infrastructuur?

HR-gegevens worden native voor de apps voor financiële en bedrijfsactiviteiten in de omgeving in de nieuwe infrastructuur. Twee keer wegschrijven wordt gebruikt om HR-gegevens te verplaatsen tussen de nieuwe omgeving en de Dataverse-omgeving.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Wij hebben aangepaste integraties opgebouwd vanuit Dynamics 365 Human Resources naar een of meer externe systemen. Zullen we nieuwe integraties moeten ontwikkelen nadat de infrastructuurwijziging is voltooid?

Dit is afhankelijk van het integratie-eindpunt. Zie [Integratieoverzicht](../fin-ops-core/dev-itpro/data-entities/integration-overview.md) voor meer informatie over de integratietechnologieën die beschikbaar zijn in apps voor financiële en bedrijfsactiviteiten en hoe u de beste integratietechnologie kunt kiezen.

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>We hebben Dataverse voor Dynamics 365 Human Resources uitgebreid. Worden deze extensies automatisch gemigreerd?

Als de Dynamics 365 Human Resources- en client voor financiële en bedrijfsactiviteitenen die in de omgeving verbonden worden met de nieuwe infrastructuur aan dezelfde Dataverse-omgeving zijn verbonden, blijven de twee apps verbonden met dezelfde Dataverse-omgeving na de migratie. Er is geen migratie vereist voor Dataverse-extensies.

Als echter de Dynamics 365 Human Resources- en client voor financiële en bedrijfsactiviteitenen momenteel verbonden zijn met aparte Dataverse-omgevingen, moeten de twee Dataverse-omgevingen worden gecombineerd zodat zij zijn verbonden met een enkele omgeving in de nieuwe infrastructuur. Voor deze Dataverse-migratie kunnen de Dataverse-tabellen die standaard in de Human Resources-oplossingen zijn opgenomen, worden verbonden opnieuw gesynchroniseerd met de nieuwe Dataverse-omgeving. Eventuele extensies voor de Dataverse-omgeving worden niet automatisch gemigreerd, maar moeten opnieuw worden geïmplementeerd in de nieuwe omgeving. Het is raadzaam om beheerde oplossingen te gebruiken om uw Dataverse-extensies te beheren. Zie [Inleiding tot oplossingen](/powerapps/developer/data-platform/introduction-solutions) voor meer informatie.

### <a name="we-have-utilized-the-custom-field-functionality-within-dynamics-365-human-resources-will-those-custom-fields-migrate-automatically"></a>We hebben de aangepaste veldfunctionaliteit in Dynamics 365 Human Resources gebruikt. Worden deze aangepaste velden automatisch gemigreerd?
Ja, de aangepaste velden die zijn toegevoegd, worden naar de nieuwe infrastructuur gemigreerd.

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>We hebben Microsoft Power Automate-stromen en/of Microsoft Power Apps geconfigureerd om te werken met Dynamics 365 Human Resources. Worden deze Microsoft Power Platform-onderdelen gemigreerd en werken ze automatisch nadat de wijziging in de infrastructuur is voltooid?

Power Apps, Power Automate-stromen en andere Microsoft Power Platform-aanpassingen zijn vergelijkbaar met Dataverse-extensies. Of zij automatisch werken na de migratie naar de nieuwe infrastructuur is afhankelijk van de vraag of de Human Resources-app en de apps voor financiële en bedrijfsactiviteiten vóór de migratie met dezelfde Power Apps-omgeving waren verbonden.

Als de apps momenteel met dezelfde Power Apps-omgeving zijn verbonden, blijven ze verbonden met die Power Apps-omgeving na de migratie naar de nieuwe infrastructuur. In dit geval blijven Power Apps, Power Automate-stromen en andere Microsoft Power Platform-aanpassingen werken zonder extra configuratie. Het is raadzaam om beheerde oplossingen te gebruiken om uw toepassingsextensies in Dataverse te beheren. Zie [Inleiding tot oplossingen](/powerapps/developer/data-platform/introduction-solutions) voor meer informatie.

Als de Human Resources-app en de apps voor financiële en bedrijfsactiviteiten echter met aparte Power Apps-omgevingen zijn verbonden, moeten deze worden gecombineerd als onderdeel van de migratie. Voor deze taak moeten eventuele Power Apps en andere aanpassingen opnieuw worden geïmplementeerd in de nieuwe omgeving.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>We hebben virtuele Dataverse-tabellen ingeschakeld voor Dynamics 365 Human Resources. Wat gebeurt er met deze tabellen tijdens de migratie?

Als de omgeving in de nieuwe infrastructuur na de migratie verbonden blijft met de Dataverse-omgeving die momenteel is verbonden met Dynamics 365 Human Resources, blijven de virtuele Dataverse-tabellen die in die omgeving zijn gegenereerd, werken zonder verdere configuratie.

Als de omgeving in de nieuwe infrastructuur na de migratie echter is verbonden met een andere Dataverse-omgeving, moeten de virtuele tabellen opnieuw worden gemaakt in de nieuwe Dataverse-omgeving.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>We hebben een integratie ontwikkeld met behulp van de ATS-API (Applicant Tracking System), salaris-API, virtuele Dataverse-tabellen voor Dynamics 365 Human Resources of andere entiteiten in de Dataverse-web-API. Blijven deze integraties werken nadat de infrastructuurwijziging is voltooid?

Als de omgeving in de nieuwe infrastructuur na de migratie verbonden blijft met de Dataverse-omgeving die momenteel is verbonden met Dynamics 365 Human Resources, blijven alle integraties die zijn ontwikkeld voor de Dataverse-web-API na de integratie werken zonder verdere configuratie.

Als de omgeving in de nieuwe infrastructuur na de migratie echter verbonden is met een andere Dataverse-omgeving, moeten alle integraties die zijn ontwikkeld voor de Dataverse-web-API opnieuw worden geconfigureerd zodat zij verbinding maken met de nieuwe Dataverse-omgeving.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Zijn er gevolgen voor de Azure-regio wanneer mijn omgeving wordt gemigreerd?

De verwachting is dat uw Human Resources-omgeving normaal gesproken tijdens de migratie in dezelfde Azure-regio blijft. De enige uitzondering treedt op als de Human Resources-omgeving wordt samengevoegd met een client voor financiële en bedrijfsactiviteiten in een andere regio. In dit geval wordt de Human Resources-omgeving gemigreerd naar de Azure-regio van de client voor financiële en bedrijfsactiviteiten.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Mijn organisatie is afhankelijk van werkstromen in Dynamics 365 Human Resources voor een of meer bedrijfsprocessen. Worden de workflows automatisch gemigreerd?

Ja, workflowconfiguraties, workflowhistorie en huidige workflows in het proces worden gemigreerd.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Welke training en resources zijn beschikbaar om te helpen bij het migratieproces?

Er wordt complete documentatie verstrekt om elke stap van het migratieproces gedetailleerd te beschrijven. Er kunnen, afhankelijk van de behoefte, ook aanvullende trainingsbronnen beschikbaar zijn, zoals video's en workshops.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Mijn organisatie heeft opgeslagen weergaven gemaakt in Dynamics 365 Human Resources om de bruikbaarheid van de interface te verbeteren. Worden de opgeslagen weergaven automatisch gemigreerd?

Ja, opgeslagen weergaven worden naar de nieuwe infrastructuur gemigreerd.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>We gebruiken Ceridian met Dynamics 365 Human Resources. Is de Ceridian-integratie beschikbaar nadat de infrastructuurwijziging is voltooid? 

De integratie met Ceridian wordt gemigreerd naar de integratie op basis van de Salaris-API. De op bestanden gebaseerde integratie die momenteel bestaat in Dynamics 365 Human Resources wordt niet naar de Finance and Operations-infrastructuur gemigreerd. Zie [Inleiding tot Salaris-API](./hr-admin-integration-payroll-api-introduction.md) voor meer informatie.

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Wat is de invloed van de migratie op het service-updateproces?

Na de migratie hebben klanten veel meer flexibiliteit met betrekking tot ALM en service-updates. Service-updates worden niet langer automatisch toegepast op Human Resources-omgevingen. In plaats daarvan volgt de service de service-updateprocessen en -functionaliteit van One Version. Daarom komen configuratieopties voor updates beschikbaar via LCS. Zie [Overzicht van One Version](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md) voor meer informatie.

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Welke gevolgen heeft de migratie voor mijn LCS-project voor Dynamics 365 Human Resources?

Bij de migratie naar de nieuwe infrastructuur verplaatst u het beheer van uw Dynamics 365 Human Resources-omgevingen naar een Finance and Operations-implementatieproject in LCS. Als bij de migratie Dynamics 365 Human Resources wordt samengevoegd met een bestaande client voor financiële en bedrijfsactiviteiten, wordt uw Human Resources LCS-project samengevoegd in het LCS-implementatieproject voor de app voor financiële en bedrijfsactiviteiten. Als u op dit moment alleen met Dynamics 365 Human Resources werkt, wordt er een nieuw LCS-implementatieproject gemaakt en wordt uw bestaande Human Resources LCS-project gemigreerd naar het nieuwe project.

Het nieuwe project wordt hetzelfde type project als door apps voor financiële en bedrijfsactiviteiten wordt gebruikt. Het zal over dezelfde functies en functionaliteit voor omgevingsbeheer beschikken. Zie [Lifecycle Services-resources](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md) voor meer informatie=.

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>We hebben onze taakregistraties aan de Business Process Modeler gekoppeld in Human Resources. Hoe wordt de Business Process Modeler gemigreerd en in LCS samengevoegd?

Bedrijfsprocesbibliotheken voor het LCS-project worden gemigreerd naar het nieuwe LCS-project voor Human Resources.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Mijn organisatie maakt momenteel alleen gebruik van Dynamics 365 Human Resources. Welke resources zijn beschikbaar zodat we meer te weten kunnen komen over de ontwikkelingsmogelijkheden nadat de infrastructuurwijziging is voltooid?

Er komen zowel Microsoft Power Platform-uitbreidbaarheidsopties als Finance and Operations-uitbreidbaarheidsopties beschikbaar, die kunnen worden gebruikt voor ontwikkeling. Zie [Startpagina van Ontwikkelen en aanpassen](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md) voor meer informatie.

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>We hebben functies ingeschakeld in Dynamics 365 Human Resources. Worden deze functies automatisch ingeschakeld tijdens de migratie?

Of een functie automatisch wordt ingeschakeld in de nieuwe infrastructuur wordt voor elke functie afzonderlijk bepaald. Deze informatie wordt opgenomen in de functiedocumentatie.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Wat gebeurt er met mijn BYOD-database tijdens de migratie?

Import- en exportconfiguraties voor Bring Your Own Database (BYOD) worden naar de nieuwe infrastructuur gemigreerd.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Wat gebeurt er met mijn Azure Data Lake tijdens de migratie?

Elke export die momenteel is geconfigureerd voor Azure Data Lake Storage in apps voor financiële en bedrijfsactiviteiten behoudt dezelfde configuratie na de migratie.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>We maken momenteel gebruik van Dynamics AX 2012. Worden de upgradeprogramma's die momenteel beschikbaar zijn voor het upgraden van de HR-module in AX 2012 naar Dynamics 365 Human Resources?

Ja. Dynamics 365 Human Resources wordt opgenomen in de samengevoegde codebase en infrastructuur voor apps voor financiële en bedrijfsactiviteiten. Een upgrade van Dynamics AX 2012 naar Dynamics 365 Human Resources maakt gebruik van hetzelfde upgradepad en dezelfde hulpprogramma's als worden gebruikt voor een upgrade naar de meest recente versie van apps voor financiële en bedrijfsactiviteiten.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Wij gebruiken Documentverwerking met Dynamics 365 Human Resources. Wat gebeurt er met de documenten tijdens de migratie?

De documenten blijven in de bestaande documentopslag. Ze worden opnieuw toegewezen aan de omgeving in de nieuwe infrastructuur.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Wat gebeurt er met de batchtaken die we hebben geconfigureerd in Dynamics 365 Human Resources na de migratie?

Toepasselijke batchtaken worden automatisch gemigreerd naar de nieuwe infrastructuur.

## <a name="licensing-impact"></a>Licentie-impact

Deze documentatie vervangt geen enkele wettelijke documentatie die gebruiksrechten omvat.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Mijn organisatie gebruikt Dynamics 365 Human Resources om de eigen HR-bewerkingen te beheren. Veranderen onze licentiekosten?

Klanten die Dynamics 365 Human Resources-licenties hebben aangeschaft worden niet beïnvloed. Er vindt geen migratie van licenties plaats voor deze klant. De extra sandbox-voorraadeenheid (SKU) die specifiek was voor Human Resources, is niet langer van toepassing. In plaats daarvan kunnen klanten ervoor kiezen om een Tier 2-sandbox voor apps voor financiële en bedrijfsactiviteiten te kopen voor een iets lagere prijs. Bestaande klanten die een Human Resources-sandbox hebben gekocht, worden zonder extra kosten naar een Tier 2-sandbox voor apps voor financiële en bedrijfsactiviteiten gemigreerd.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Mijn organisatie gebruikt de Human Resources-module in Dynamics 365 Finance, Supply Chain Management, Commerce of Project Operations. Veranderen mijn licenties of kosten?

Bestaande gebruikers van Dynamics 365-toepassingen en gebruikers van zelfstandige versies van Dynamics 365 Finance, Supply Chain Management, Commerce en Project Operations hebben toegang tot Human Resources als onderdeel van deze licenties tot februari 2025 of totdat de huidige licentieovereenkomst vervalt, indien dat eerder is. U kunt ervoor kiezen eerder naar Human Resources-licenties over te stappen als u hierdoor meer kosten kunt besparen. Vanaf februari 2025 moeten alle bestaande CSP- en EA-klanten HRM-licenties kopen om te kunnen profiteren van de nieuwe mogelijkheden die met de apps voor financiële en bedrijfsactiviteiten worden geboden.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Mijn organisatie is live met Dynamics 365 Finance, Supply Chain Management, Commerce of Project Operations. Worden we verplicht een extra omgeving te kopen voor het ondersteunen van de infrastructuursamenvoeging?

Er zijn geen extra omgevingen vereist voor het ondersteunen van de infrastructuurwijziging.

