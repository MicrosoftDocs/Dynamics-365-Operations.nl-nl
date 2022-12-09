---
title: Mogelijkheden in Store Commerce-app
description: In dit artikel wordt de functionaliteit beschreven die beschikbaar is in de Store Commerce-app voor Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788507"
---
# <a name="store-commerce-app-capabilities"></a>Mogelijkheden in Store Commerce-app

[!include [banner](includes/banner.md)]

De Store Commerce-app is de moderne POS-ervaring (Point of Sale) voor Microsoft Dynamics 365 Commerce. Hiermee kunnen bedrijven transacties in de winkel verwerken en back-officebewerkingen beheren, zoals de verwerking van voorraad en orders. Met de app kunnen bedrijven ook klantrelaties met loyaliteit en clienteling beheren. 

Gebaseerd op Commerce Scale Unit (CSU) biedt de Store Commerce-app een volledige oplossing voor meerdere kanalen. Een klant kan bijvoorbeeld online een product kopen en het ophalen in een winkel in de buurt, aldus doorgaand met winkelen via verschillende kanalen zonder gegevens te verliezen. 

Dit artikel biedt een overzicht van de mogelijkheden van de Store Commerce-app.

## <a name="platform"></a>Platform

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Meerdere kanalen | Dynamics 365 Commerce biedt een allesomvattende oplossing voor meerdere kanalen die een universele ervaring biedt voor de backoffice, in de winkel, in het callcenter en bij digitale activiteiten. | [Overzicht](index.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Headless commerce | De Commerce Scale Unit fungeert als host voor de engine voor headless commerce. De headless commerce-engine fungeert als het centrale punt voor alle commerciële bedrijfslogica en stuurt een volledige oplossing voor meerdere kanalen aan. | <p>[Architectuuroverzicht](commerce-architecture.md)</p><p>[Headless architectuur](dev-itpro/retail-server-architecture.md)</p> | [Techspraak](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce Headquarters | Commerce Headquarters biedt back-officecapaciteiten waarmee producten, werknemers, bedrijfsprocessen, prijzen en andere functies kunnen worden geconfigureerd die voor het bedrijf vereist zijn. | [Architectuuroverzicht](commerce-architecture.md) | |
| POS (Point of Sale) | De Store Commerce-app is de POS-ervaring voor Dynamics 365 Commerce. Deze service biedt geavanceerde en uitgebreide POS-mogelijkheden waarmee verkoopmedewerkers, kassamedewerkers en managers kunnen voorzien in een betere klantenservice. Bovendien biedt het een aantal implementatieopties voor detailhandelaren, betere prestaties en een verbeterd levenscyclusbeheer voor toepassingen (Application Lifecycle Management). | [Store Commerce-app](dev-itpro/store-commerce.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Video](https://youtu.be/7B332XH_zfs)</p><p>[Migratie van MPOS naar Store Commerce](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Cloudimplementatie | Er kunnen meerdere exemplaren van Commerce Scale Units worden geïmplementeerd voor belastingdistributie en geografische nabijheid. | [Cloudimplementatie](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| On-premises implementatie | Met behulp van een implementatie van lokale bedrijfsgegevens krijgen Commerce-klanten meer controle- en beheermogelijkheden voor hun Dynamics 365-omgevingen. | [On-premises implementatie](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Apparaatbeheer

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Meerdere formulierfactoren | De Store Commerce-app wordt ondersteund op verschillende apparaatformulierfactoren, zoals pc's, tablets en mobiele apparaten. Met de responsieve gebruikersinterface kan de indeling automatisch worden aangepast en aan de schermgrootte worden aangepast. | [Visuele configuraties](pos-screen-layouts.md) |  |
| Platformonafhankelijk | De Store Commerce-app wordt ondersteund op web-, Windows-, iOS- en Android-platforms. | [Platforms](dev-itpro/hybridapp.md) | |
| Branding | In de schermontwerper kunt u schermindelingen aanpassen aan de behoeften van uw bedrijf. Daarnaast kunnen thema's, indelingen, kleuren en afbeeldingen worden gemaakt op basis van werknemersrollen en kunnen ze vervolgens worden gedeeld door gebruikers voor merkconsistentie en gebruiksgemak. | [Visuele configuraties](pos-screen-layouts.md) | [Video](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topologie | Er worden verschillende topologieën voor de winkel ondersteund op basis van de netwerkbeschikbaarheid. | <p>[Topologie](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Infographic](dev-itpro/retail-in-store-topology.md)</p> | |
| Beheer van meerdere apparaten | Meerdere apparaten in winkels kunnen eenvoudig vanuit Commerce Headquarters worden beheerd. | [Activering](set-up-activation-accounts-validate-devices-hq.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Personeelsbeheer

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Aanmelden | Elke winkelmedewerker kan specifieke aanmeldingsgegevens hebben. Aanmelding is onder andere mogelijk op basis van gebruikersnaam, streepjescode, magneetstriplezer, biometrie en Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Uitgebreide aanmelding](extended-logon.md)</p> | |
| Machtigingen | Er worden verschillende machtigingsniveaus ondersteund voor werknemers, zoals de machtiging om orders te maken en de machtiging om orders te bewerken. | [Machtigingen](tasks/create-pos-permission-groups.md) | |
| Tijd- en aanwezigheidsbeheer | Aanwezigheid kan worden beheerd met de functie Tijdklok. Aanwezigheidsgegevens kunnen in salarisadministratie worden verwerkt met de Dynamics 365 Human Resources-app. | [Tijdbeheer](retail-time-attendance.md) | |
| Verkoopprovisie | Verkopen kunnen per verkoper worden gevolgd voor het berekenen van provisie of andere beloningen. | [Provisie](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Merchandising

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Assortimentsbeheer | Merchandisingmanagers kunnen producten zo indelen dat ze via een specifiek kanaal en gedurende een bepaalde periode te koop zijn. | [Assortimenten](assortments.md) | |
| Catalogi | Merchandisingmanagers kunnen catalogi beheren om de producten te identificeren die u wilt aanbieden met catalogusspecifieke prijzen. | [Catalogi](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Product- en categoriebeheer | In Commerce Headquarters kunnen merchandisingmanagers producten maken met varianten, kenmerken, een maateenheid, enzovoort. U kunt ook een categoriehiërarchie opgeven om producten te ordenen. | [Artikel](retail-hierarchies.md) | |
| Bundels | Merchandisingmanagers kunnen producten zo groeperen dat ze worden verkocht als bundel of kit. | [Kits](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Infocodes | Gebruik informatiecodes om de kassier te vragen om informatie in te voeren tijdens verschillende acties op de POS, zoals artikelverkopen, artikelretouren of klantselecties. | [Infocodes](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Gekoppelde artikelen | Gebruik gekoppelde artikelen voor het upsellen van producten wanneer een artikel aan de transactie wordt toegevoegd. | [Gekoppelde artikelen](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Garanties | Uitgebreide garanties kunnen samen met producten worden verkocht. | [Garantie](extended-warranty.md) | |
| Labels afdrukken | Er kunnen labels worden gegenereerd die productinformatie bevatten, zoals het batchnummer, het serienummer en de vervaldatum. | [Labels afdrukken](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Ondersteunde verkoop

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Bladeren in producten | Zoek naar producten per categorie. | [Producthiërarchie](retail-hierarchies.md) | |
| Artikel zoeken | Zoek naar producten op naam en verfijn zoekopdrachten met behulp van productkenmerken, zoals het merk, de prijs en het materiaal. Deze mogelijkheid wordt aangestuurd door Azure Cognitive Search. | [Zoekopdrachten via cloud](cloud-powered-search-overview.md) | |
| De pagina Productgegevens | Pagina's met uitgebreide productgegevens kunnen afbeeldingen, een omschrijving, productkenmerken en aanbevolen producten bevatten. Aanbevelingen worden aangestuurd door de aanbevelingenservice. | | |
| Productvergelijking | Vergelijk meerdere producten en help klanten er een te kiezen en deze aan een transactie toe te voegen. | | |
| Eindeloze gang | Zoek eenvoudig voorraad in andere winkels en maak orders. | [Zoeken in voorraad](pos-inventory-lookup-operation.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Aanbevelingen | Profiteer van mogelijkheden voor cross- en upselling met de Recommendations-service. Deze service maakt gebruik van gepatenteerde technologie om aanbevelingen te doen op basis van inkooptrends en kenmerken, zoals net binnen, vergelijkbaar uiterlijk en meest verkocht. Deze aanbevelingen zijn beschikbaar op productdetailpagina's, de pagina **Klantgegevens** en de pagina **Transacties**. | [Aanbevelingen](product-recommendations.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Klantrelatie

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Klantbeheer | Maak, bewerk en beheer bankrekeningen van klanten. Klantrekeningen kunnen in de asynchrone modus worden beheerd om realtime verwerking te voorkomen. | [Beheer](customer-mgmt-stores.md) | |
| Klantkenmerken | Met het framework voor klantkenmerken kunnen extra klantgerelateerde gegevens worden vastgelegd op basis van zakelijke vereisten. | [Kenmerken](dev-itpro/customer-attributes.md) | |
| Pagina met klantgegevens | Een pagina met uitgebreide klantgegevens biedt inzicht in de interacties van de klant via alle kanalen. Deze interacties omvatten inkopen, wenslijsten en loyaliteitspunten. | | |
| Zoekopdrachten voor klanten via cloud | Zoek klanten op naam, telefoonnummer, e-mailadres, loyaliteitskaart, adres, enzovoort. | [Zoekopdrachten via cloud](pos-search-improvements.md#customer-search) | |
| Loyaliteit en beloningen | Klanten kunnen deelnemen aan loyaliteitsprogramma's en loyaliteitspunten via meerdere kanalen inwisselen. | [Loyaliteit](set-up-customer-loyalty-program.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| Clienteling | Beheer belangrijke klanten met behulp van een klantenboek en houd activiteiten en notities voor het klantprofiel bij. Dankzij de integratie van Dynamics 365 Customer Insights kunnen winkelmedewerkers hints krijgen over de volgende beste actie voor elke klant. | [Clienteling](clienteling-overview.md#activities-and-notes) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>Prijzen en kortingen

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Handelsovereenkomsten | Prijsmanagers kunnen handelsovereenkomsten gebruiken om speciale prijzen te definiëren op basis van langetermijnovereenkomsten voor specifieke klanten. | [Prijscalculatie](price-management.md)| [Video](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Verkoopovereenkomsten | Prijsmanagers kunnen verkoopovereenkomsten gebruiken voor het definiëren van prijzen op basis van contracten in B2B-commercescenario's (Business-to-Business). | [Prijscalculatie](price-management.md) | |
| Prijscorrecties | Prijsmanagers kunnen de functies voor prijscorrectie gebruiken voor het maken, bijhouden en beheren van prijsverlagingen voor hun producten. | [Prijscorrecties](price-adjustments-discounts.md) | |
| Kortingen | Prijsmanagers kunnen verschillende typen korting instellen om allerlei promoties uit te voeren. Deze kortingen omvatten eenvoudige kortingen, hoeveelheidskortingen, drempelkortingen, combinatiekortingen, kortingen op basis van betalingsmethode en verzendkortingen. | [Kortingen](retail-discounts-overview.md) | |
| Coupons | Prijsmanagers kunnen couponcodes of streepjescodes instellen, deze koppelen aan kortingen en ze onder klanten verdelen. Verkoopmedewerkers kunnen coupons toevoegen aan verkooptransacties of deze verwijderen. | [Coupons](coupons.md) | |
| Prijsgroepen | Prijsmanagers kunnen de functie voor prijsgroepen gebruiken om contextprijzen te definiëren op basis van kanalen, catalogi, aansluitingen of loyaliteitsprogramma's. | [Prijscalculatie](price-management.md) | |
| Beschikbare promoties | Verkoopmedewerkers kunnen eenvoudig beschikbare promoties zoeken voor producten in de winkel, producten die aan een transactie zijn toegevoegd, enzovoort. | [Prijsfuncties](pos-pricing-functions.md) | |
| Prijscontroles | Verkoopmedewerkers kunnen snel actieve verkoopprijzen van producten in de winkel controleren. | [Prijsfuncties](pos-pricing-functions.md) | |
| Prijsoverschrijvingen | Verkoopmedewerkers die over de vereiste machtigingen beschikken, kunnen de door het systeem geconfigureerde of berekende prijzen overschrijven. | [Prijsfuncties](pos-pricing-functions.md) | |
| Handmatige kortingen | Verkoopmedewerkers die over de vereiste machtigingen beschikken, kunnen handmatige kortingen toepassen op verkooptransacties of -regels. | [Prijsfuncties](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektronische betalingen

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Credit en debet | De Store Commerce-app ondersteunt belangrijke creditcard- en betaalpassbetalingen via de Adyen-betalingsgateway en het afhandelen van de order via PayPal. De Betalingen-SDK ondersteunt externe gatewayverbindingen die worden ondersteund door ISV-integraties (Independent Software Vendor). | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[PayPal](paypal.md)</p><p>[Betalingen](payment-methods.md)</p> | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Ondersteuning voor digitale wallet | De Store Commerce-app ondersteunt betalingswijzen via de digitale wallet die geen BIN-bereik (Bank Identification Number) gebruiken, zoals traditionele creditcards en betaalpassen. Betalingswijzen kunnen worden toegepast op digitale walletbetalingen, zoals Adyen. | [Wallet](wallets.md) | |
| Ondersteuning voor geschenkbonnen | Dynamics 365-geschenkbon met bankidentificatienummer, oplossingen voor opgeslagen waarden (SVS) en Givex-geschenkbonnen. Geschenkbonnen kunnen in een order worden gekocht en ingewisseld. | [Geschenkbonnen](dev-itpro/gift-card.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Fraud Protection | Met Dynamics 365 Fraud Protection kunt u frauduleuze activiteiten voorkomen en plaatsen identificeren waar fraude onopgemerkt kan blijven. | [Fraud Protection](dev-itpro/dfp.md) | [Video](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Belastingen en toeslagen

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Belastingen | De Store Commerce-app ondersteunt veel typen indirecte belastingen zoals btw, belasting toegevoegde waarde (btw), belasting voor goederen en services (GST), kosten op basis van eenheden en bronbelasting. | [Belastingen](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Toeslagen | Toeslagen kunnen worden geconfigureerd op regelniveau, koptekstniveau, als automatische toeslagen, per kanaal, enzovoort. | [Toeslagen](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Orderafhandeling en -afhandeling

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Order maken | Er kan een order worden gemaakt voor verzending of ophalen in een winkel in de buurt. Er kunnen tijdvakken voor ophalen worden ingesteld. | [Overzicht](customer-orders-overview.md) | |
| Orderwijziging | Een order kan worden gewijzigd, geretourneerd, geannuleerd, enzovoort. | <p>[Annuleren](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Retouren](pos-returns.md)</p> | |
| Orders zoeken | Zoek en filter orders met behulp van orderspecifieke informatie. | [Zoeken](enhancedorderrecall.md) | |
| Orderkenmerken | Met het framework voor orderkenmerken kunnen extra ordergerelateerde gegevens worden vastgelegd op basis van zakelijke vereisten. | [Kenmerken](dev-itpro/order-attributes.md) | |
| Rechtstreekse levering | Artikelen kunnen worden gemarkeerd voor rechtstreekse levering door een leverancier aan een klantadres. Rechtstreekse levering wordt ook wel drop shipping genoemd. | [Rechtstreekse levering](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Offerte | Winkelmedewerkers kunnen offertes voor klanten maken en een speciale prijs, handmatige kortingen en een geldigheidsdatum voor de offerte opgeven. | [Offerte](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Afhandeling | Winkels kunnen orders picken, verpakken en verzenden. U kunt een pakbon toevoegen aan de pakketten die klaar zijn voor verzending. | [Afhandeling](order-fulfillment-overview.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[Video](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| Gedistribueerd orderbeheer | De Store Commerce-app ondersteunt de optimalisering voor intelligente orderafhandeling, waarbij bedrijfsstrategieën kunnen worden geconfigureerd op basis van de aard van het bedrijf, het type klant, de oorsprong van een order en de leveringsmethode voor een order. | [DOM](dom.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>Voorraadbeheer

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Klantlevering | Stroomlijn de distributie van beschikbare voorraad vanuit een distributiecentrum naar meerdere winkels of magazijnen. | [Klantlevering](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Cross-docken | Stroomlijn de distributie van voorraad op binnenkomende inkooporders naar meerdere winkels of magazijnen. | [Cross-docken](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Binnenkomende voorraad | Ontvang voorraad van een leverancier via een inkooporder of vanuit een ander magazijn via een transferorder. Maak een aanvraag voor binnenkomende inkoop- of transferorders. | [Inkomend](pos-inbound-inventory-operation.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Uitgaande voorraad | Verzend voorraad naar een ander magazijn via een transferorder en maak een aanvraag voor een uitgaande transferorder. | [Uitgaand](pos-outbound-inventory-operation.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Zoeken in voorraad | Controleer voorhanden voorraad op producten in verschillende winkels en magazijnen, en controleer de ATP-voorraad (available to promise) op toekomstige datums. | [Zoeken in voorraad](pos-inventory-lookup-operation.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Voorraadcorrectie | Pas de voorraad in of uit het magazijn van een winkel aan de specifieke behoeften van het bedrijf aan zonder verkoop, ontvangst of hertelling. | [Voorraadcorrectie](work-with-store-inventory.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Voorraadtellingen | Tel de fysieke voorraad en pas de systeemboekhoudvoorraad hieraan aan. | [Tellen](work-with-store-inventory.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| Voorraadmutatie | Verplaats voorraad tussen locaties in een winkel. | [Mutatie](work-with-store-inventory.md) | <p>[Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>Financiële items

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Kasbeheer | De Store Commerce-app ondersteunt het beheer van contant geld en andere opgegeven betalingsmethoden in de winkel. Bovendien kan de afstemming van ploegendiensten in de winkel worden ingeschakeld voor geavanceerde functies voor het beheer van contant geld. | [Contant](cash-mgmt.md) | |
| Financiële overzichten en afstemming | Transacties met contant geld en transactionele transacties voor een winkel worden in Commerce Headquarters geregistreerd via de boekingsprocessen. | [Overzichten](retail-statements.md) | |
| Inkomsten- en uitgaventransacties | Verwerk kleingeldtransacties in de winkel en registreer inkomsten die niet op de traditionele manier binnenkomen, zoals gevonden geld, het deel van de opbrengst van een koffiecorner in uw lobby en schoonmaakdiensten. | [Overzichten](retail-statements.md) | |
| Factuurbetalingen | Leg betalingen op basis van facturen vast. | [Factuur](payinvoice.md) | |

## <a name="employee-productivity"></a>Productiviteit van werknemers

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Taakbeheer | Maak taaklijsten en taken, en wijs deze toe aan winkels en werknemers. Houd de status van taken in winkels bij. Naadloze integratie met Microsoft Teams wordt geboden. | <p>[Taakbeheer](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Video](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Hardware en randapparatuur

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Randapparaten aansluiten | Sluit randapparaten, zoals printers, kassaladen, scanners en betalingapparaten, aan op een POS-terminal. | [Randapparaten](retail-peripherals-overview.md) ||
| Randapparatuur delen | Kassabonprinters , kassaladen en betalingsapparaten kunnen tussen een groot aantal terminals worden gedeeld door deze aan een gedeeld hardwarestation te koppelen. | <p>[Hardwarestation](retail-peripherals-overview.md) ||
| POS en randapparatuursimulator | De randapparatuursimulator ondersteunt het testen van scenario's waarin gewoonlijk fysieke POS-randapparaten vereist zijn. Daarnaast bevat deze een POS-simulator die u kunt gebruiken om de compatibiliteit te testen van fysieke randapparatuur zonder dat u de POS-client hoeft te implementeren. | [Simulator](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Ontvangstbewijzen

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Ontvangstbewijzen afdrukken | Ontvangstbewijzen van verschillende typen, zoals verkoopontvangstbonnen, creditcardontvangstbonnen, geschenkbonnen en facturen, kunnen standaard of na bevestiging van de kassamedewerker bij het uitchecken worden afgedrukt. Ze kunnen ook opnieuw worden afgedrukt vanuit het journaal. | [Afdrukken](receipt-templates-printing.md) | |
| Ontvangstbewijzen per e-mail | Ontvangstbewijzen kunnen vanuit het POS worden gemaild nadat het uitchecken is voltooid. | [E-mailadres](email-receipts.md) | |
| Ontvangstbewijzen ontwerpen | Ontvangstbewijzen voor winkels kunnen worden aangepast, zodat ze gegevens en indelingen tonen die passen bij de detailhandelaar en het transactietype. Ontvangstbewijzen kunnen ook worden uitgebreid, zodat ze aangepaste gegevens bevatten die de detailhandelaar nodig heeft. | [Ontwerp](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Offline ondersteuning

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Naadloos offline | Met naadloos offline kunt u doorgaan met transacties, zelfs als internetconnectiviteit beperkt of niet beschikbaar is. Met gegevensuitsluiting kunt u de gegevensgrootte van de offline databases beperken en de prestaties optimaliseren. | [Offline](pos-operations.md) | |
| Op prestaties gebaseerde schakelingen | Schakel over op offline wanneer prestatievermindering wordt gedetecteerd. | [Offline](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI) |
| Offline dashboard | Het dashboard **Offline status** geeft de offline status, fouten en details van de gegevens voor elk apparaat weer. Daarom kunt u de status van een groot aantal apparaten eenvoudig beheren. | [Offline](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Uitbreidbaarheid

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Commerce Headquarters | U kunt oplossingen voor Commerce Headquarters aanpassen door bedrijfsprocessen toe te voegen of te wijzigen. Commerce Headquarters ondersteunt het gebruik van metagegevens en een codegestuurd uitbreidingsmodel om aangepaste functionaliteit toe te voegen. Deze kan eenvoudig in externe oplossingen worden geïntegreerd. | [Overzicht](dev-itpro/extend-customer-cdx-package.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Headless commerce | Het framework voor uitbreidbare API's via meerdere kanalen kan worden gebruikt om bedrijfslogica aan te passen en toe te voegen. API's met aanvraaghandlers en extensiepatronen vóór en na activering. | [CSU](dev-itpro/retail-server-customer-consumer-api.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Commerce-SDK | De Commerce-SDK bevat de code, codevoorbeelden, sjablonen en hulpmiddelen die nodig zijn om de Dynamics 365 Commerce-functionaliteit uit te breiden of aan te passen. De SDK wordt in verschillende opslagplaatsen (repo's) in GitHub opgeslagen, afhankelijk van de extensieonderdelen. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Verkooppunt | De Store Commerce-app kan onafhankelijk worden uitgebreid met de POS-extensiefunctie van de Commerce-SDK. Het framework ondersteunt de aanpassing van de gebruikerservaring (UX), workflows en bedrijfslogica. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [Techspraak](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Aangifte

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Verkooprapporten | Verkooprapporten met betrekking tot personeel, kassa, betalingstype, retouren, product en dergelijke zijn beschikbaar voor winkelmanagers. Managers kunnen deze rapporten weergeven en gebruiken om provisie toe te wijzen en producttrends te identificeren. | | |

## <a name="diagnostics"></a>Diagnose

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Operationele inzichten | In de winkel beheerde betrouwbaarheids- en prestatiegegevens over de status van de service zijn beschikbaar in het Application Insights-abonnement van de klant. Er zijn geavanceerde waarschuwings- en controlemogelijkheden beschikbaar. | | |
| Statuscontrole | De beschikbaarheid van randapparatuur die met een POS is verbonden, kan worden gecontroleerd door de statuscontrole uit te voeren. Individuele randproblemen kunnen vervolgens worden opgelost en geverifieerd. | [Statuscontrole](pos-healthcheck.md) | [Video](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globalisatie

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Ondersteuning voor meerdere markten | Marktspecifieke functies, zoals fiscale integratie, GST, geavanceerde facturering en vooruitbetalingen, worden standaard ondersteund. Deze functie beslaat verschillende markten in Europa, Noord- en Zuid-Amerika, Rusland, Azië, Saudi-Arabië, enzovoort. | [Globalisatie](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Conformiteit

| Mogelijkheid | Description | Documentatie | Aanvullende inhoud |
|---|---|---|---|
| Microsoft-standaarden | De Store Commerce-app voldoet aan Microsoft-standaarden voor beveiliging, privacy, toegankelijkheid, de AVG, de gegevensgrens van de EU, enzovoort. | | |

