---
title: Veelgestelde vragen over Elektronische facturering
description: Dit onderwerp bevat informatie over veelgestelde vragen over Elektronische facturering.
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0b3bd48cbc1ce5f236f51b79b8235d6b7c3890c0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022343"
---
# <a name="electronic-invoicing-faq"></a>Veelgestelde vragen over Elektronische facturering

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat antwoorden op veelgestelde vragen over de service Elektronische facturering. Elektronische facturering vergroot de mogelijkheden voor elektronische facturering die bestaan in Dynamics 365 Finance, Dynamics 365 Supply Chain Management en Dynamics 365 Project Operations. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Wat is belangrijk over elektronische facturering en waarom doet het ertoe voor mijn organisatie?

Operationele complexiteit en risico's blijven toenemen terwijl organisaties wereldwijd groeien en een grote voetafdruk achterlaten in regio's. Het wordt voor bedrijven steeds moeilijker om compliant te blijven en zich aan te passen aan voortdurend veranderende regelgeving en dit is in het bijzonder van belang als het om factureren gaat. Facturering is traditioneel een duur en foutgevoelig proces omdat bedrijven afhankelijk zijn van papieren documenten en intensieve handmatige processen.  

Organisaties stappen langzaam maar zeker af van papieren facturen om de kosten te verlagen en het hele proces te versnellen. Overheden stappen meer en meer over op elektronische facturering als hoofdcomponent van belastingdigitalisatie. Door van organisaties te eisen dat ze real-time belastinggegevens digitaal indienen bij de belastingdienst, kunnen overheden belastingontduiking en -manipulatie minimaliseren en fraude beperken. 

De wereld stapt over op documentverwerking zonder papier en zonder elektronische facturering te implementeren, kunnen klanten het risico lopen te maken te krijgen met conformiteitsproblemen, onnodige kosten en achter te blijven op concurrenten. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Bevatten Finance, Supply Chain Management en Project Operations niet al functionaliteit voor elektronische facturering? Welke waarde biedt dit mij als klant? 

Met de functie Elektronische facturering worden de bestaande mogelijkheden voor elektronische facturering in Finance, Supply Chain Management en Project Operations uitgebreid. De functionaliteit vereenvoudigt ook de naleving van de nieuwste standaarden voor elektronische facturering en biedt samenhangende opties voor verschillende regio's in de verwerking en uitwisseling van elektronische facturen. De functie voor elektronische facturering ontgrendelt een aantal voordelen, waaronder: 

   - Snellere en eenvoudigere toepassing van vereisten die specifiek per land/regio gelden.
   - Standaardisatie van implementaties van e-factureringsoplossingen. 
   - Verbeterde traceerbaarheid van verwerking van e-facturen.  
   - Eenvoudiger te onderhouden om te voldoen aan veranderende wettelijke vereisten en lokale zakelijke praktijken. 
   - Vereenvoudigde oplossingsverpakkingen.
   - Mogelijkheden voor schalen voor een groot volume aan ingediende documenten, resulterend in een snellere doorlooptijd.
   - De mogelijkheid om uw oplossingen met andere bedrijven te delen.

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Ondersteunt de service Elektronische facturering de on-premises installaties van Finance, Supply Chain Management en Project Operations? 

Het huidige platform staat het gebruik van de on-premises versie niet toe en er zijn geen plannen om dit in de toekomst te ondersteunen.

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>Werkt de interface voor de service Elektronische facturering met de functie voor leveranciersimportautomatisering?

Nee. Er bestaan wel plannen hiervoor, maar geen geplande tijdlijn. Indien gepland, worden de datums aangekondigd in de [releaseplannen](/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Hoe verwerkt de service Elektronische facturering bestandsbijlagen in de elektronische factuur? Is een SharePoint-server nodig bij het insluiten van PDF-bestanden in het XML-bestand?

De bestanden die aan de elektronische factuur zijn gekoppeld, worden verwerkt als ingesloten binaire gegevens in een XML-element. U hebt geen SharePoint-server nodig om PDF-bestanden in te sluiten, maar de bijlage moet wel worden opgeslagen in het documentbeheersysteem van Finance, Supply Chain Management en Project Operations.

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>Is de service Elektronische facturering beschikbaar volgens de regelgeving van mijn land/regio?

De service Elektronische facturering is een microserviceplatform dat globaal beschikbaar wordt.

Microsoft is van plan de indelingen en integraties van elektronische facturen te publiceren voor de landen die functioneel zijn gelokaliseerd door Microsoft. Zie [Beschikbaarheid van functies voor elektronische facturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) voor meer informatie.

Als de indeling voor elektronische facturering niet beschikbaar is voor uw land/regio, streeft het platform er wel naar dit scenario in de toekomst te ondersteunen. U kunt nog steeds profiteren van de configuratiemogelijkheden die Elektronische facturering te bieden heeft en de indeling voor elektronische facturering zelf configureren, maar u kunt ook met een partner/ISV werken om deze voor uw organisatie te configureren.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Is Dynamics 365 for Regulatory Services een nieuwe module, zoals Human Resources of project Operations, die is gekoppeld aan Finance of Supply Chain Management? Zijn hieraan extra kosten verbonden?

Dynamics 365 for Regulatory Services (RCS) is een cloudservice voor de configuratie van globalisatieresources. RCS is gratis voor alle licentiehouders van Finance, Supply Chain Management en Project Operations.

Voor aanmelding bij RCS gaat u naar <https://marketing.configure.global.dynamics.com/>.

Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie.

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>Moet ik me aanmelden om de service Elektronische facturering te krijgen of kan ik dit gewoon inschakelen in Functiebeheer?

Als u een licentie hebt voor Finance, Supply Chain Management en Project Operations, raadpleegt u [Aan de slag met servicebeheer via de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md) om u aan te melden voor Elektronische facturering.

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Werkt de service Elektronische facturering met virtuele machines van Tier 1? Wat is de minimaal vereiste omgeving?

Voor de integratie met de service Elektronische facturering is ten minste een virtuele Tier 2-machine nodig als host voor Finance of Supply Chain Management. Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie over omgevingsplanning.

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>Biedt de service Elektronische facturering een testmodus voor het testen van factuurverzendingen?

Dit kan worden bereikt door middel van configuratie. Als u de indiening van facturen wilt testen, kunt u vanuit een UAT-omgeving (User Acceptance Test) verbinding maken met Finance of Supply Chain Management en de testfacturen indienen. Elektronische facturering ondersteunt de configuratie van digitale testcertificaten en voor e-facturen waarvoor digitale goedkeuring vereist is, kan een URL worden ingesteld op basis van testwebservices die door de belastingdienst zijn gepubliceerd.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Bestaat er documentatie over de kant-en-klare landspecifieke functies voor de service Elektronische facturering?

Ja. Zie [Beschikbaarheid van functies voor Elektronische facturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) voor informatie over de beschikbaarheid van functies voor elektronische facturering en de indelingen die deze ondersteunen.

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>Kan een rechtspersoon in Finance of Supply Chain Management die voor een bepaald land is geconfigureerd met de service Elektronische facturering functies voor elektronische facturering gebruiken vanuit verschillende landen/regio's?

Ja. De functies voor elektronische facturering kunnen worden gebruikt om onafhankelijk van het land van de rechtspersoon indieningen van bedrijfsdocumenten te verwerken, als het volgende geldt:

   - Het bedrijfsdocument dat wordt gegenereerd gebruikt de juiste documentmodeltoewijzing.
   - Er is een overeenkomst tussen het bedrijfsdocument en de regels voor toepasbaarheid die in de functie Elektronische facturering zijn geconfigureerd.

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>Maakt de service Elektronische facturering gebruik van dezelfde configuratie- en ontwerpervaring als die van de module Elektronische rapportage in Finance en Supply Chain Management? 

Ja. Dezelfde ontwerpprogramma's die worden gebruikt in de module Elektronische rapportage (ER) in Finance en Supply Chain Management worden gebruikt voor het maken en configureren van configuraties voor gegevensmodeltoewijzing en bestandsindelingen. Deze ontwerpprogramma's worden ook gebruikt in Regulatory Configuration Services (RCS) voor het maken en configureren van configuraties voor gegevensmodeltoewijzing en bestandsindelingen die worden gebruikt in de configuratie van de e-factureringsfuncties.

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>Kunnen de toepasbaarheidsregels worden uitgebreid en geconfigureerd zodat ze niet zijn gekoppeld aan een specifieke parameter, zoals een rechtspersoon?

Ja. De toepasbaarheidsregels kunnen volledig worden geconfigureerd. U kunt clausules toevoegen of verwijderen, logische bewerkingen maken en clausules groeperen en uit groepen halen. Meer informatie over dit onderwerp vindt u in [Toepasbaarheidsregels](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules).

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>Ondersteunt de service Elektronische facturering het toevoegen van andere ER-indelingsconfiguraties om andere typen documenten te genereren? Biedt het ondersteuning voor het elektronisch verzenden van documenten naar klanten, bijvoorbeeld een afleveringsbewijs?

U kunt andere configuraties voor ER-indelingen gebruiken om de gewenste uitvoerbestanden te produceren. De configuratie van de ER-indeling moet echter worden afgeleid van dezelfde ER-factuurmodeltoewijzing die in Finance of Supply Chain Management is geconfigureerd om bedrijfsdocumenten te genereren. Standaard biedt Elektronische facturering geen ondersteuning voor het rechtstreeks naar de klant verzenden van een uitvoerbestand als een EDI-transactie.

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>Ondersteunt de service Elektronische facturering het uitwisselen van elektronische facturen met klanten? Biedt het ondersteuning voor het configureren van verschillende factuurindelingen voor dezelfde factuur?

Er wordt gewerkt aan de mogelijkheid om elektronische leveranciersfacturen te ontvangen en te importeren, maar het automatisch verzenden van de elektronische facturen naar klanten wordt momenteel niet ondersteund.

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>Biedt de service Elektronische facturering ondersteuning voor het uitwisselen van EDI-berichten met andere bedrijven?

De focus van de service Elektronische facturering ligt op het uitwisselen van typen elektronische facturen op basis van door wettelijke vereisten. Er wordt gewerkt aan de mogelijkheid om elektronische leveranciersfacturen te ontvangen en te importeren, maar het verzenden van de elektronische facturen naar klanten wordt momenteel niet standaard ondersteund, behalve in gevallen waarin het verzenden van de elektronische factuur naar de klant een wettelijke vereiste is.

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>Ondersteunt de service Elektronische facturering het importeren of samenvoegen van aanpassingen die in de ER-indelingsconfiguraties zijn aangebracht vanuit de verouderde functie Elektronische facturering ?

U kunt configuraties voor ER-indelingen opnieuw gebruiken in de service Elektronische facturering. De configuratie van de ER-indeling moet echter worden afgeleid van dezelfde ER-factuurmodeltoewijzing waarvoor de functie Elektronische facturering was ontworpen en die in Finance of Supply Chain Management is geconfigureerd om de bedrijfsdocumenten te genereren.

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>Ondersteunt de service Elektronische facturering de uitgifte van elektronische facturen vanuit zelfgemaakt tabellen? Zo ja, hoe kan ik de ER-gegevensmodelconfiguraties maken voor deze nieuwe tabellen en entiteiten?

Ja. U moet de factuurmodeltoewijzing echter aanpassen en de benodigde verwijzingen naar de zelfgemaakte tabellen toevoegen, of een nieuwe factuurmodeltoewijzing maken, afhankelijk van de complexiteit.

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>Ondersteunt de service Elektronische facturering verschillende eindpunten voor webservices?

De service Elektronische facturering ondersteunt verschillende eindpunten voor webservices. U kunt configureerbare integratie met REST-webservices gebruiken, of diverse landspecifieke webserviceintegraties met parameters. U kunt verschillende eindpunten configureren voor dezelfde webservices en API's, met verschillende versies van configuraties. Zie [Lijst met parameters per actie](e-invoicing-setup.md#list-of-parameters-by-action) voor meer informatie.

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>Is elektronische facturering geïntegreerd met de API's van de verschillende factuurverwerkers uit de Scandinavische landen of moeten dat per geval worden verwerkt?

Microsoft werkt continu aan uitbreiding van de functionaliteit om standaardintegraties te bieden met behulp van de elektronische factureringsfuncties. Meer informatie over de indelingen en integraties die worden ondersteund, vindt u in [Beschikbaarheid van elektronische factureringsfuncties](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Als u het antwoord dat u zoekt niet hebt gevonden, stuurt u uw vraag per e-mail naar het productontwikkelingsteam op <D365EInvoicePreview@microsoft.com>. Wij nemen contact met u op of verbeteren de dekking van dit document met veelgestelde vragen.
