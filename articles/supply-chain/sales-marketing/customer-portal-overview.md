---
title: Overzicht van klantportal voor Dynamics 365 Supply Chain Management
description: In dit onderwerp wordt de klantportal geïntroduceerd en wordt uitgelegd wie de portal moet gebruiken en hoe deze werkt.
author: dasani-madipalli
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 86d9a40d991e915d3529e0c330f7559d8e7ce9ea
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529573"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Overzicht van klantportal voor Dynamics 365 Supply Chain Management

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="what-is-the-customer-portal"></a>Wat is de klantportal?

Moderne toeleveringssystemen zijn gebaseerd op integratie. Hiervoor moeten de voorraad-, klantvraag- en verkoopafdelingen worden geïntegreerd in plaats van dat ze in afzonderlijke silo's worden geplaatst. De klantportal helpt organisaties die Microsoft Dynamics 365 Supply Chain Management gebruiken om deze integratie uit te breiden en hun klanten effectiever op de hoogte te houden.

De klantportal is een sjabloon voor [Power Apps-portals](https://docs.microsoft.com/powerapps/maker/portals/overview) waarmee bedrijven een extern gerichte Business-to-Business (B2B)-website kunnen maken voor scenario's die betrekking hebben op de verwerking van verkooporders. De sjabloon maakt gebruik van [twee keer wegschrijven](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management en Power Apps-portals om externe ondernemingsklanten in staat te stellen gegevens te bekijken en te maken vanuit de Dynamics 365-omgeving van het bedrijf.

De klantportalsjabloon bevat alle aanpassingsfuncties die door de portalfunctie voor Power Apps wordt geleverd. De sjabloon kan eenvoudig worden gewijzigd om het merk van het bedrijf aan te geven, verbeterde functionaliteit toe te voegen en de gebruikerservaring te wijzigen. U kunt alle functies van de sjabloon uit het vak desgewenst wijzigen.

> [!IMPORTANT]
> De sjabloon zal niet volledig functioneel zijn. De service biedt een voorziening voor klanten die een externe website willen maken, zodat ondernemingsklanten kunnen werken met gegevens uit Supply Chain Management.

> [!NOTE]
> De documentatie van de klantportal is gericht op beheerders, aanpassers en systeemintegrators die de klantportal instellen voor een Supply Chain Management-installatie. De termen _klant_ en _gebruiker_ worden gebruikt om personen te beschrijven die klanten zijn van de organisatie die Supply Chain Management uitvoert en die de eindportal zelf zullen gebruiken.

## <a name="video"></a>Video

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

De video [overzicht van de klantportalsjabloon in Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) (zie hierboven) is opgenomen in de [Finance and Operations-afspeellijst](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.

## <a name="who-should-use-it"></a>Wie moet het gebruiken?

De klantportal is ontworpen voor bedrijven die Supply Chain Management uitvoeren en de volgende kenmerken hebben:

- Ze willen een extern gerichte website maken die informatie over de orderverwerking (zoals de orderstatus of accountgegevens) direct vanuit hun Supply Chain Management-systeem aan hun bedrijfsklanten doorgeeft.
- Ze stappen over van Dynamics AX 2012 naar Supply Chain Management en gebruikten eerder de [AX 2012 zelfservice portal voor leveranciers](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

De volgende typen organisaties zijn **niet** geschikt voor de implementatie van de klantportal:

- Bedrijven die een website willen maken voor niet-ondernemingsklanten. Deze bedrijven moeten overwegen om een [Dynamics 365 Commerce e-commerce-website](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site) te maken.
- Bedrijven die al een bestaande Power Apps-portalwebsite gebruiken voor een vergelijkbaar doel. Deze bedrijven ontvangen geen extra voordelen van de klantportal. De klantportal wordt geleverd als een sjabloon die fungeert als leidraad en als uitgangspunt voor klanten die Twee keer wegschrijven, Supply Chain Management en Power Apps-portals willen laten samenwerken. Als u hiervoor al een website hebt ingesteld, is het mogelijk dat u niet veel meerwaarde krijgt van het gebruik van de klantportalsjabloon om die website opnieuw in te richten.

## <a name="how-does-it-work"></a>Hoe functioneert dit?

De klantportal wordt geleverd als Power Apps-portalsjabloon. Deze hangt af van Power Apps-portals en twee keer wegschrijven.

[Power Apps-portals](https://docs.microsoft.com/powerapps/maker/portals/overview) is een functie waarmee gebruikers een extern gerichte website kunnen maken waarbij mensen van buiten de organisatie zich kunnen aanmelden. Er is weinig tot geen codering nodig om portals te maken. De klantportal is een van de vele [Dynamics 365-portalsjablonen](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) die Microsoft beschikbaar stelt.

[Twee keer wegschrijven](https://docs.microsoft.com/powerapps/maker/portals/overview) is een kant-en-klaar infrastructuurproduct dat vrijwel realtime-interactie biedt tussen modelgestuurde apps in Dynamics 365 en Finance and Operations-apps. Twee keer wegschrijven biedt bidirectionele integratie tussen Finance and Operations-apps en Common Data Service. Daarom geeft dit een geïntegreerde gebruikerservaring over de apps heen. De klantportal is afhankelijk van entiteiten die met twee keer wegschrijven worden gesynchroniseerd. Voordat gegevens van Supply Chain Management kunnen worden afgelezen in de klantportal, moet twee keer wegschrijven zijn ingeschakeld voor alle relevante entiteiten.

![Afhankelijkheden van klantportal](media/customer-portal-elements.png "Afhankelijkheden van klantportal")

De klantportal fungeert als uitgangspunt voor organisaties die Power Apps-portals willen gebruiken om een extern gerichte website te maken die gegevens uit hun Supply Chain Management-installatie gebruikt. Het helpt organisaties om twee keer wegschrijven, Supply Chain Management en Power Apps-portals te koppelen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]