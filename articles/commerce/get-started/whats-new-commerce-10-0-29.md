---
title: Nieuwe en gewijzigde functies in Dynamics 365 Commerce 10.0.29 (oktober 2022)
description: In dit artikel worden de functies beschreven die in Microsoft Dynamics 365 Commerce 10.0.29 nieuw of gewijzigd zijn.
author: josaw1
ms.date: 09/29/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0629228516d688abf4dcd4280d1ad676f8f35331
ms.sourcegitcommit: ce4e56d798281258479432ad821287a1cc8e26bf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2022
ms.locfileid: "9601566"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10029-october-2022"></a>Wat is nieuw of gewijzigd in Dynamics 365 Commerce 10.0.29 (oktober 2022)

[!include [banner](../includes/banner.md)]


In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Microsoft Dynamics 365 Commerce versie 10.0.29. Deze versie heeft het buildnummer 10.0.1326 en is beschikbaar volgens de onderstaande planning:

- **Preview van versie:** augustus 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** september 2022
- **Algemene beschikbaarheid van versie (automatische update):** oktober 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit artikel gewijzigd om functies op te nemen die zijn toegevoegd na de oorspronkelijke publicatie van dit artikel.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door   |
|---------|------------------|----------------|--------------| 
| B2B | [Ondersteuning inschakelen voor verkoopovereenkomst via verschillende kanalen](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | Met deze functionaliteit kunnen B2B-verkooporganisaties (business-to-business) verkoopovereenkomsten gebruiken in Commerce headquarters om op contracten gebaseerde prijzen vast te stellen voor hun kopers. Wanneer een B2B-koper op de e-commercewebsite shopt, worden de op een contract gebaseerde prijzen die voor de betreffende B2B-koper zijn ingesteld automatisch toegepast voor het hele proces van productselectie, aankoop en betaling. | Functiebeheer<p>*Ondersteuning voor verkoopovereenkomst tussen verschillende handelskanalen* |
| Customer Service | [Klantenservice inschakelen met Dynamics 365 Omnichannel for Customer Service](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | Een eersteklas klantenservicebeleving is voor consumenten van groot belang om te zorgen voor een persoonlijke en soepele winkelervaring. Momenteel bestaan er meerdere commerce touchpoints, zoals fysieke winkels, online kanalen en sociale kanalen. Consumenten verwachten voor al deze touchpoints een persoonlijke ondersteuningservaring. Met deze functionaliteit kunt u het aantal winkelwagenconversies naar verkopen verhogen, meer persoonlijke betrokkenheid met klanten realiseren en klantenservice verbeteren door de integratie met Dynamics 365 Omnichannel for Customer Service. | Ingeschakeld door beheerder/makers |
| E-commerce | Ondersteuning voor productvergelijking in e-commerce | Maak het mogelijk dat shoppende bezoekers hun producten in een groot aantal categorieën kunnen vergelijken zodat ze de juiste aankoopbeslissing kunnen maken. Deze functionaliteit is zowel voor B2C- (business-to-consumer) en B2B-sites beschikbaar. | Site builder | 
| Geschenkbonnen | Ondersteuning voor cadeaukaarttabellen voor retail voor het delen van gegevens tussen verschillende bedrijven | Dynamics headquarters ondersteunt de mogelijkheid voor het inschakelen van gegevens delen tussen verschillende bedrijven voor specifieke tabellen in de architectuur van Dynamics. In deze functionaliteit voegt Dynamics 365 Commerce ondersteuning toe voor het delen van gegevens tussen verschillende bedrijven voor cadeaukaarttabellen voor retail. Daardoor kunnen de gegevens van een cadeaukaart bij het ene bedrijf nu gedupliceerd worden naar een ander bedrijf in de omgeving. Wijziging die in de cadeaukaarttabel van het oorspronkelijke bedrijf worden gemaakt, worden gedeeld met de cadeaukaarttabel van het gedupliceerde bedrijf. | Ontwikkelaars |
| Globalisatie | [Lokalisatiefuncties voor Commerce inschakelen voor nieuwe Commerce SDK](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-commerce-localization-features-new-commerce-sdk) | De nieuwe functie biedt de mogelijkheid om Commerce-lokalisatiefuncties in te schakelen vanuit Commerce Headquarters met behulp van de functie management framework of parameters. Voorbeelden voor fiscale integratie zijn nu opgenomen in de nieuwe Commerce SDK en ondersteunen onafhankelijke verpakking. Met deze functie kunt u ook de functionaliteit van de Store Commerce-app van klanten in Global Commerce gebruiken.<p><p>Deze release bevat Commerce-lokalisatiefuncties en voorbeelden voor belastingintegratie voor [Oostenrijk](../localizations/emea-aut-fi-sample.md), [de Tsjechische Republiek](../localizations/emea-cze-fi-sample.md), [Frankrijk](../localizations/emea-fra-cash-registers.md), [Duitsland](../localizations/emea-deu-fi-sample.md), [Italië](../localizations/emea-ita-fpi-sample.md), [Noorwegen](../localizations/emea-nor-cash-registers.md) en [Polen](../localizations/emea-pol-fpi-sample.md). | Ingeschakeld door beheerder/makers |
| Offline | [Compressie van offlinedatabase voor POS](../dev-itpro/implementation-considerations-offline.md#important-offline-features) | Deze nieuwe functie reduceert offline databasegrootten door geautomatiseerde indexcompressie buiten de [openingstijden](../dev-itpro/store-hours.md) van het kanaal in te schakelen. | Functiebeheer<p>*Compressie van offlinedatabase voor POS* |
| Prestaties | RTS-afhankelijkheid voor ″klant bewerken″-scenario′s verwijderen | Hoge beschikbaarheid en high performance zijn standaard verwachtingen voor verkooppunt- (POS) en e-commercekanalen. Om aan deze verwachtingen te voldoen hoeven Dynamics 365 Commerce-kanalen niet langer te vertrouwen op realtime communicatie met Commerce headquarters wanneer klantinformatie is bewerkt. De mogelijkheid om klantinformatie asynchroon te bewerken voor asynchrone en niet-asynchrone klanten kan helpen om realtime oproepen naar Commerce headquarters te verminderen. | Ingeschakeld door beheerder/makers |

## <a name="feature-state-changes-in-this-release"></a>Wijzigingen in status van functie in deze versie

In de volgende tabel worden functies weergegeven die verplicht zijn geworden of standaard zijn ingeschakeld in versie 10.0.29. Al deze functies worden automatisch voor uw systeem ingeschakeld zodra u een update uitvoert naar versie 10.0.29. Verplichte functies kunnen niet worden uitgeschakeld, maar functies die standaard zijn ingeschakeld, kunnen wel worden uitgeschakeld door gebruik te maken van [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

De tabel bevat ook functies die eerder in openbare preview waren, maar zijn gewijzigd om algemeen beschikbaar te worden in versie 10.0.29. Deze wijziging geeft aan dat de functies nu worden aanbevolen voor gebruik in productieomgevingen. Deze functies zijn standaard uitgeschakeld, tenzij anders wordt aangegeven. Daarom moet u [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om ze in te schakelen als u ze wilt gebruiken.

| Functie | Titel | Nieuwe functiestatus |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brazilië) Commerce-functionaliteit die specifiek is voor Brazilië | Standaard ingeschakeld |
| RetailAdvancedGTETaxAdjustmentFeature | (India) GST die wordt berekend voor detailhandelstransacties in Retail POS op detailhandelsoverzichten toepassen | Standaard ingeschakeld |
| RetailChronologicalInvoicePostingFeature_IT | (Italië) Toestaan dat detailhandelfacturen niet in chronologische volgorde worden geboekt | Standaard ingeschakeld |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Mexico) Kortingscorrectie in Retail CFDI Global | Standaard ingeschakeld |
| RetailFiscalIntegrationConfigurationEnhancementFeature | Overschrijvingen technische profielen fiscale integratie | Standaard ingeschakeld |
| RetailFiscalIntegrationConnectorLocationFeature | Directe fiscale integratie vanuit POS-kassa's | Standaard ingeschakeld |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | Back-up lokale opslag voor fiscale integratie | Standaard ingeschakeld |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | Uitgestelde registratie van documenten | Standaard ingeschakeld |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | Fiscale registratiestatus van POS-kassa's | Standaard ingeschakeld |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (India) GST berekenen op basis van factuuradres voor e-commerceorders | Standaard ingeschakeld |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Polen) Standaardstatus van verkoopdocument voor detailhandelsfacturen | Standaard ingeschakeld |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Mexico) Afronding wordt herberekend voor belastingbasisbedragen in internationale CFDI-functies voor Retail. | Standaard ingeschakeld |
| RetailSupplementaryInvoiceFeature | Aanvullende facturen inschakelen voor contante transacties die zijn voltooid in winkels | Standaard ingeschakeld |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Voorraadbuffers en voorraadniveaus inschakelen    |  Standaard ingeschakeld|
|RetailInboundOutboundInventoryValidationFeature|   Validatie inschakelen in de inkomende en uitgaande voorraadbewerking van het verkooppunt (POS)   |   Standaard ingeschakeld   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Uitgebreide berekeningslogica voor voorraad op kanaalzijde van e-Commerce |   Standaard ingeschakeld   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Voorraadcorrecties in verkooppunt   |  Standaard ingeschakeld  |
| RetailMultiplePickupDeliveryModeFeature |  Ondersteuning voor meerdere leveringsmethoden voor afhalen     |   Verplicht    |
|  RetailProductAvailabilityOptimizationFeature |   Berekening van geoptimaliseerde productbeschikbaarheid  |  Verplicht |
|   RetailPricingDataManagerV2Feature   |   Prestaties verbeteren voor Commerce-prijsengine |   Verplicht |
|  RetailPricingPreventUnintendedRecalculationFeature   | Onbedoelde prijsberekening voor commerce-orders voorkomen    |  Verplicht  |
| RetailTeamsIntegration    |   Integratie met Microsoft Teams inschakelen| Verplicht   |  
| ConsumerEFDSyncProcessFeature_BR | (Brazilië) NFC-e synchrone verwerking | Standaard ingeschakeld |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | Ondersteuning voor interne en externe connectors in het raamwerk voor fiscale integratie | Verplicht |
| RetailTaxRegistrationIdEnableFeature_BR | (Brazilië) Klanten in Retail POS zoeken op basis van belastingregistratienummers | Verplicht |
| RetailTaxRegistrationIdEnableFeature_IN | (India) Klanten in Retail POS zoeken op basis van belastingregistratienummers | Verplicht |
| RetailTaxRegistrationIdEnableFeature_IT | (Italië) Beheer van klantgegevens in Retail POS | Verplicht |
| RetailTaxRegistrationIdEnableFeature_PL | (Polen) Beheer van klantgegevens in Retail POS | Verplicht |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (Detailhandel GST voor India) Creditnota's met verwijzingen naar oorspronkelijke facturen bijwerken | Verplicht |
| RetailUserDefinedCertificateProfileFeature | Door gebruiker gedefinieerde certificaatprofielen voor winkels | Verplicht |
  

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Commerce 10.0.29 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.29 van apps voor financiële en bedrijfsactiviteiten (oktober 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). 

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van versie 10.0.29, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2022

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk de [Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2022](/dynamics365-release-plan/2022wave2/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-features"></a>Verwijderde en afgeschafte functies

In het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) worden functies beschreven die zijn verwijderd of afgeschaft voor Commerce.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Commerce](removed-deprecated-features-commerce.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
