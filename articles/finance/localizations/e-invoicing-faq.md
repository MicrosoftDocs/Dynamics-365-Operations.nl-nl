---
title: Veelgestelde vragen over Elektronische facturering
description: Dit onderwerp bevat informatie over veelgestelde vragen over Elektronische facturering.
author: gionoder
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 1ba1a6c5542c10306d4b7494d33e7ff04504fa95
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893773"
---
# <a name="electronic-invoicing-faq"></a>Veelgestelde vragen over Elektronische facturering

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat antwoorden op veelgestelde vragen over Elektronische facturering. Elektronische facturering vergroot de mogelijkheden voor elektronische facturering die bestaan in Dynamics 365 Finance, Dynamics 365 Supply Chain Management en Dynamics 365 Project Operations. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Wat is belangrijk over elektronische facturering en waarom doet het ertoe voor mijn organisatie?

Operationele complexiteit en risico's blijven toenemen terwijl organisaties wereldwijd groeien en een grote voetafdruk achterlaten in regio's. Het wordt voor bedrijven steeds moeilijker om compliant te blijven en zich aan te passen aan voortdurend veranderende regelgeving en dit is in het bijzonder van belang als het om factureren gaat. Facturering is traditioneel een duur en foutgevoelig proces omdat bedrijven afhankelijk zijn van papieren documenten en intensieve handmatige processen.  

Organisaties stappen langzaam maar zeker af van papieren facturen om de kosten te verlagen en het hele proces te versnellen. Overheden stappen meer en meer over op elektronische facturering als hoofdcomponent van belastingdigitalisatie. Door van organisaties te eisen dat ze real-time belastinggegevens digitaal indienen bij de belastingdienst, kunnen overheden belastingontduiking en -manipulatie minimaliseren en fraude beperken. 

De wereld stapt over op documentverwerking zonder papier en zonder elektronische facturering te implementeren, kunnen klanten het risico lopen te maken te krijgen met conformiteitsproblemen, onnodige kosten en achter te blijven op concurrenten. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Bevatten Finance, Supply Chain Management en Project Operations niet al functionaliteit voor elektronische facturering? Welke waarde biedt dit mij als klant? 

Met de functie voor elektronische facturering worden de bestaande mogelijkheden voor elektronische facturering in Finance, Supply Chain Management en Project Operations uitgebreid. De functionaliteit vereenvoudigt ook de naleving van de nieuwste standaarden voor elektronische facturering en biedt samenhangende opties voor verschillende regio's in de verwerking en uitwisseling van elektronische facturen. De functie voor elektronische facturering ontgrendelt een aantal voordelen, waaronder: 

   - Snellere en eenvoudigere toepassing van vereisten die specifiek per land/regio gelden.
   - Standaardisatie van implementaties van e-factureringsoplossingen. 
   - Verbeterde traceerbaarheid van verwerking van e-facturen.  
   - Eenvoudiger te onderhouden om te voldoen aan veranderende wettelijke vereisten en lokale zakelijke praktijken. 
   - Vereenvoudigde oplossingsverpakkingen.
   - Mogelijkheden voor schalen voor een groot volume aan ingediende documenten, resulterend in een snellere doorlooptijd.
   - De mogelijkheid om uw oplossingen met andere bedrijven te delen.

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Ondersteunt Elektronische facturering de on-premises installaties van Finance, Supply Chain Management en Project Operations? 

Het huidige platform staat het gebruik van de on-premises versie niet toe en er zijn geen plannen om dit in de toekomst te ondersteunen.

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>Werkt de interface voor elektronische facturering met de functie voor leveranciersimportautomatisering?

Nee. Er bestaan wel plannen hiervoor, maar geen geplande tijdlijn. Indien gepland, worden de datums aangekondigd in de [releaseplannen](/dynamics365/release-plans/).

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Hoe verwerkt Elektronische facturering bestandsbijlagen in de elektronische factuur? Is een SharePoint-server nodig bij het insluiten van PDF-bestanden in het XML-bestand?

De bestanden die aan de elektronische factuur zijn gekoppeld, worden verwerkt als ingesloten binaire gegevens in een XML-element. U hebt geen SharePoint-server nodig om PDF-bestanden in te sluiten, maar de bijlage moet wel worden opgeslagen in het documentbeheersysteem van Finance, Supply Chain Management en Project Operations.

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>Is Elektronische facturering beschikbaar volgens de regelgeving van mijn land/regio?

Elektronische facturering is een microserviceplatform dat globaal beschikbaar wordt.

Microsoft is van plan de indelingen en integraties van elektronische facturen te publiceren voor de landen die functioneel zijn gelokaliseerd door Microsoft. Zie [Beschikbaarheid van functies voor elektronische facturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) voor meer informatie.

Als de indeling voor elektronische facturering niet beschikbaar is voor uw land/regio, streeft het platform er wel naar dit scenario in de toekomst te ondersteunen. U kunt nog steeds profiteren van de configuratiemogelijkheden die Elektronische facturering te bieden heeft en de indeling voor elektronische facturering zelf configureren, maar u kunt ook met een partner/ISV werken om deze voor uw organisatie te configureren.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Is Dynamics 365 for Regulatory Services een nieuwe module, zoals Human Resources of project Operations, die is gekoppeld aan Finance of Supply Chain Management? Zijn hieraan extra kosten verbonden?

Dynamics 365 for Regulatory Services (RCS) is een cloudservice voor de configuratie van globalisatieresources. RCS is gratis voor alle licentiehouders van Finance, Supply Chain Management en Project Operations.

Voor aanmelding bij RCS gaat u naar <https://marketing.configure.global.dynamics.com/>.

Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie.

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>Moet ik me aanmelden om Elektronische facturering te krijgen of kan ik dit gewoon inschakelen in Functiebeheer?

Als u een licentie hebt voor Finance, Supply Chain Management en Project Operations, raadpleegt u [Aan de slag met servicebeheer via de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md) om u aan te melden voor Elektronische facturering.

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Werkt Elektronische facturering met virtuele machines van Tier 1? Wat is de minimaal vereiste omgeving?

Voor de integratie met Elektronische facturering is ten minste een virtuele Tier 2-machine nodig als host voor Finance of Supply Chain Management. Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie over omgevingsplanning.

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>Biedt Elektronische facturering een testmodus voor het testen van factuurverzendingen?

Dit kan worden bereikt door middel van configuratie. Als u de indiening van facturen wilt testen, kunt u vanuit een UAT-omgeving (User Acceptance Test) verbinding maken met Finance of Supply Chain Management en de testfacturen indienen. Elektronische facturering ondersteunt de configuratie van digitale testcertificaten en voor e-facturen waarvoor digitale goedkeuring vereist is, kan een URL worden ingesteld op basis van testwebservices die door de belastingdienst zijn gepubliceerd.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Bestaat er documentatie over de kant-en-klare landspecifieke functies voor elektronische facturering?

Ja. Zie [Beschikbaarheid van functies voor elektronische facturering](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features) voor informatie over de beschikbaarheid van functies voor elektronische facturering en de indelingen die deze ondersteunen.

> [!NOTE] 
> Als u het antwoord dat u zoekt niet hebt gevonden, stuurt u uw vraag per e-mail naar het productontwikkelingsteam op <D365EInvoicePreview@microsoft.com>. Wij nemen contact met u op of verbeteren de dekking van dit document met veelgestelde vragen.