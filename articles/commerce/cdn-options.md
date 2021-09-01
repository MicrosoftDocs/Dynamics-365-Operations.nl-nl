---
title: Implementatieopties voor netwerk voor contentlevering
description: In dit onderwerp worden de verschillende opties voor de implementatie van het netwerk voor contentlevering (Content Delivery Network - CDN) besproken die kunnen worden gebruikt in Microsoft Dynamics 365 Commerce-omgevingen. Deze opties omvatten oorspronkelijke, door Commerce geleverde exemplaren van Azure Front Door en exemplaren van Azure Front Door die eigendom zijn van klanten.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 73da1fff8f79b4fcde38f9da643b8a3479247959f763976d782279e4e2af7a33
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729909"
---
# <a name="content-delivery-network-implementation-options"></a>Implementatieopties voor netwerk voor contentlevering

[!include [banner](includes/banner.md)]

In dit onderwerp worden de verschillende opties voor de implementatie van het netwerk voor contentlevering (Content Delivery Network - CDN) besproken die kunnen worden gebruikt in Microsoft Dynamics 365 Commerce-omgevingen. Deze opties omvatten oorspronkelijke, door Commerce geleverde exemplaren van Azure Front Door en exemplaren van Azure Front Door die eigendom zijn van klanten.

Commerce-klanten hebben verschillende mogelijkheden wanneer ze overwegen welke CDN-service met hun Commerce-omgeving moet worden gebruikt. Commerce wordt vrijgegeven met basisondersteuning voor Azure Front Door. Dit omvat basishosting en aangepaste domeinvereisten. Voor bedrijven die meer controle en specifiekere beveiligingsvaardigheden willen, zoals een WAF (Web Application Firewall), is de beste optie om een exemplaar van Azure Front Door dat eigendom is van een klant of een externe CDN-service te gebruiken.

De volgende drie implementatieopties voor CDN kunnen in Commerce-omgevingen worden gebruikt:

- Het door Commerce geleverde exemplaar van Azure Front Door
- Een exemplaar van Azure Front Door dat eigendom is van een klant (voor meer controle en extra beveiligingsfuncties)
- Een externe CDN-service

Alle drie de CDN-implementatieopties leveren alleen dynamische HTML-inhoud vanuit aangepaste domeinen. Commerce verwerkt automatisch alle JavaScript-, trapsgewijze opmaakmodellen (CSS), afbeeldingen-, video- en andere statische inhoud via door Microsoft beheerde CDN's. De optie die u kiest, bepaalt de operationele capaciteiten, controlemogelijkheden en aanvullende beveiligingscapaciteiten die beschikbaar zijn.

De volgende afbeelding biedt een overzicht van de Commerce-architectuur.

![Overzicht van de Commerce-architectuur.](media/Commerce_CDN-Option_ComparisonModels.png)

Zie [CDN-ondersteuning toevoegen](add-cdn-support.md) voor meer informatie over het instellen van een exemplaar van Azure Front Door voor uw Commerce-site.

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Het door Commerce geleverde exemplaar van Azure Front Door gebruiken

De volgende tabel bevat de voors en tegens van het gebruik van het door Commerce geleverde exemplaar van Azure Front Door om eindpunten voor content te beheren.

| Voors | Tegens |
|------|------|
| <ul><li>Het exemplaar is opgenomen in de kosten voor Commerce.</li><li>Omdat het exemplaar wordt beheerd door het Commerce-team, is er minder onderhoud vereist en zijn er gedeelde instellingsstappen.</li><li>De door Azure gehoste infrastructuur is schaalbaar, veilig en betrouwbaar.</li><li>Voor het SSL-certificaat (Secure Sockets Layer) is een eenmalige instelling vereist en dit wordt automatisch vernieuwd.</li><li>Het exemplaar wordt door het Commerce-team gecontroleerd op fouten en afwijkingen.</li></ul> | <ul><li>Een WAF wordt niet ondersteund.</li><li>Er zijn geen specifieke aanpassingen of instellingscorrecties.</li><li>Het exemplaar is afhankelijk van het Commerce-team voor updates of wijzigingen.</li><li>Er is een afzonderlijk Azure Front Door-exemplaar vereist voor apex-domeinen en er is extra werk vereist om apex-domeinen te integreren met Azure DNS.</li><li>Er wordt geen telemetrie over responsen per seconden (RPS) of het foutpercentage aan de klant verstrekt.</li></ul> |

De onderstaande afbeelding toont de architectuur van het door Commerce geleverde exemplaar van Azure Front Door.

![Door Commerce geleverd exemplaar van Azure Front Door.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Een exemplaar van de Azure Front Door van een klant gebruiken

De volgende tabel bevat de voors en tegens van het gebruik van een exemplaar van Azure Front Door dat eigendom is van een klant om eindpunten voor content te beheren.

| Voors | Tegens |
|------|------|
| <ul><li>De instelling is veilig en eenvoudig te beheren.</li><li>De door Azure gehoste infrastructuur is schaalbaar, veilig en betrouwbaar.</li><li>Met het exemplaar kunnen WAF-integratie- en gedetailleerde regelbesturingselementen worden gemaakt voor beveiliging van betere kwaliteit die specifiek is afgestemd op uw locatie.</li><li>Met het exemplaar hebt u meer controle over SSL-certificaten (zowel van de klant als door Azure Front Door beheerd) en domeinkoppeling.</li><li>Het exemplaar biedt een apex-domeinoplossing bij rechtstreekse koppeling aan Azure DNS.</li><li>Er worden telemetrie en waarschuwingen geleverd.</li><li>Voor het SSL-certificaat is een eenmalige instelling vereist en dit wordt automatisch vernieuwd.</li></ul> | <ul><li>Het exemplaar wordt zelf beheerd.</li><li>Er moet vooraf kennis worden verworven.</li></ul> |

De volgende afbeelding toont een Commerce-infrastructuur die een exemplaar van Azure Front Door bevat waarvan een klant eigenaar is.

![Commerce-infrastructuur die een exemplaar van Azure Front Door bevat waarvan een klant eigenaar is.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Een externe CDN-service gebruiken

In de volgende tabel worden de voors en tegens aangegeven van het gebruik van een externe CDN-service voor het beheren van eindpunten voor content.

| Voors | Tegens |
|------|------|
| <ul><li>Deze optie is handig als het bestaande domein al op een extern CDN wordt gehost.</li><li>WAF: afhankelijk van externe provider.</li></ul> | <ul><li>Er is een afzonderlijk contract met extra kosten vereist.</li><li>Voor SSL worden mogelijk extra kosten in rekening gebracht.</li><li>Aangezien de service losstaat van de Azure-cloudstructuur, moet extra infrastructuur worden beheerd.</li><li>De service vereist mogelijk grotere tijdsinvesteringen bij het instellen van eindpunten en beveiliging.</li><li>De service wordt zelf beheerd.</li><li>De service wordt zelf bewaakt.</li></ul> |

De volgende illustratie toont een Commerce-infrastructuur die een externe CDN-service omvat.

![Commerce-infrastructuur die een externe CDN-service omvat.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Ondersteuning voor een CDN (netwerk voor contentlevering) toevoegen](add-cdn-support.md)
