---
title: Overzicht van invoegtoepassing voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven wat Voorraadzichtbaarheid is en worden de functies ervan beschreven.
author: yufeihuang
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dfc1bc0d457d0b0b2632aa2e2e5ba6a3c2f3fae7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575166"
---
# <a name="inventory-visibility-add-in-overview"></a>Overzicht van invoegtoepassing voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]

De invoegtoepassing voor de Voorraadzichtbaarheid (ook wel *Voorraadzichtbaarheid* genoemd) is een onafhankelijke en zeer schaalbare microservice waarmee real-time tracking van voorhanden voorraad wordt ingeschakeld om een globale weergave van de voorraadzichtbaarheid te genereren. Hierdoor biedt het een algemeen overzicht van de voorraad.

Externe systemen krijgen toegang tot de service via RESTful-API's. Op die manier kunnen ze ofwel zoeken aan de hand van informatie over bepaalde dimensiesets, of kunnen ze in verschillende aangepaste gegevensbronnen wijzigingen aanbrengen in uw voorraad.

Als een microservice die gebaseerd is op Microsoft Dataverse, biedt Voorraadzichtbaarheid de mogelijkheid om uit te breiden. U kunt Power Apps gebruiken om toepassingen te maken. U kunt Power BI ook aanpassen om aangepaste functionaliteit te bieden, die aan uw bedrijfsvereisten voldoet.

U kunt Voorraadzichtbaarheid in systemen van meerdere externe partijen integreren door configuratieopties in te stellen voor gestandaardiseerde voorraaddimensies en transactietypen in te stellen. Voorraadzichtbaarheid ondersteunt ook aangepaste uitbreidbaarheid door middel van configureerbare berekende hoeveelheden.

## <a name="inventory-visibility-integration-with-dynamics-365-supply-chain-management"></a>Integratie van Voorraadzichtbaarheid instellen met Dynamics 365 Supply Chain Management

De geïntegreerde oplossing haalt voorraadgegevens op uit Dynamics 365 Supply Chain Management en houdt de voorraadwijzigingen continu bij. Zie [Voorraadzichtbaarheid installeren en instellen](inventory-visibility-setup.md) en [Voorraadzichtbaarheid configureren](inventory-visibility-configuration.md) voor meer informatie.

## <a name="get-a-global-view-of-inventory"></a>Een algemeen overzicht van de voorraad weergeven

Met de geïntegreerde oplossing kunt u uw eigen gegevensbronnen definiëren en voorraadgegevens centraliseren. Zie [Voorraadzichtbaarheid configureren](inventory-visibility-configuration.md) voor meer informatie.

Uw voorraad kan op twee manieren worden bekeken:

- Een query indienen via de high-performance API. Met deze API kunnen near-real-time voorraadgegevens rechtstreeks vanuit een gecachte record worden opgehaald. U kunt contracten en voorbeelden vinden in [Openbare API's van voorraadzichtbaarheid](inventory-visibility-api.md).
- De onbewerkte lijst met voorraden weergeven. Deze lijst wordt periodiek gesynchroniseerd vanuit een gecachte record en wordt weergegeven in Dataverse. Zie [Voorraadzichtbaarheid-app](inventory-visibility-power-platform.md) voor meer informatie.

## <a name="soft-reservations"></a>Softe reserveringen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Softe reservering is van toepassing wanneer een bedrijf een bepaalde hoeveelheid producten moet reserveren om de afhandeling van verkooporders bijvoorbeeld te kunnen ondersteunen, zodat er niet te veel wordt verkocht. Op het moment dat er een verkooporder wordt aangemaakt en bevestigd in Supply Chain Management of in andere orderbeheersystemen, wordt er een aanvraag naar Voorraadzichtbaarheid verzonden om de hoeveelheid te reserveren. Met Voorraadzichtbaarheid kunt u producten met dimensiegegevens en specifieke voorraadtransactietypen reserveren. (Zie [Voorraadzichtbaarheid-app](inventory-visibility-power-platform.md) voor meer informatie.) Nadat de hoeveelheid met succes gereserveerd is, krijgt u een reserverings-ID. U kunt deze reserverings-ID gebruiken om een koppeling te maken naar de oorspronkelijke order in Supply Chain Management of in andere orderbeheersystemen.

Deze functie is zodanig ontworpen dat de totale hoeveelheid bij een reservering in Voorraadzichtbaarheid niet wordt gewijzigd. In plaats daarvan wordt alleen de gereserveerde hoeveelheid uitgelicht. (Daarom wordt dit een *softe reservering* genoemd.) De op deze wijze gereserveerde hoeveelheid kan worden tegengereserveerd wanneer de producten in Supply Chain Management of in een systeem van een externe partij worden verbruikt door de API opnieuw op te roepen om een hoeveelheidvermindering in te stellen en de totale hoeveelheid in Voorraadzichtbaarheid bij te werken. Zie [Voorraadzichtbaarheid reserveringen](inventory-visibility-reservations.md) voor meer informatie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
