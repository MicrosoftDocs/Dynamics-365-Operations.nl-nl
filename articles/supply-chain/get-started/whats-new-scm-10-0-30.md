---
title: Preview van Dynamics 365 Supply Chain Management 10.0.30 (November 2022)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.30.
author: kamaybac
ms.date: 09/08/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-09-08
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 477b27bf77d2a3ef91a5c2d39f2dfb06d8ad4e59
ms.sourcegitcommit: 562ea02e1f7409f18ee1cc4750a838bff4381e91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9429118"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10030-november-2022"></a>Preview van Dynamics 365 Supply Chain Management 10.0.30 (November 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management, previewversie 10.0.30. Deze versie heeft het buildnummer 10.0.1362 en is beschikbaar volgens de onderstaande planning:

- **Preview-versie:** september 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** oktober 2022
- **Algemene beschikbaarheid van versie (automatische update):** november 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit artikel gewijzigd om functies op te nemen die zijn toegevoegd na de oorspronkelijke publicatie van dit artikel.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door |
|---|---|---|---|
| Productie | [Apparatuur bewaken met Sensor Data Intelligence](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/monitor-equipment-sensor-data-intelligence) | [De startpagina Sensor Data Intelligence](../sensor-data-intelligence/sdi-home-page.md) | Functiebeheer:<br>*(Preview) Sensor Data Intelligence* |
| Magazijnbeheer | Omleidingen van meerdere niveaus voor de mobiele app Warehouse Management <!-- KFM: Add link when RP updates --> | [Omleidingen configureren voor stappen in menu-items van mobiele apparaten](../warehousing/warehouse-app-detours.md) | Functiebeheer:<br>*Omleidingen van meerdere niveaus voor de mobiele app Warehouse Management* |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven).

Als u een van deze functies wilt in- of uitschakelen, moet u dat doen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Productiebeheer | Informatie over voorhanden voorraad op pagina Vrij te geven productieorders | Hiermee wordt een kolom toegevoegd voor de hoeveelheid voorhanden voorraad voor het regelartikel in de sectie Regels van de pagina **Vrij te geven productieorders.**  |
| Transportbeheer | Zendingen toewijzen aan gerelateerde routesegmenten | Met deze functie kan het systeem verzendingsvrachtkosten nauwkeuriger toedelen, ook voor ladingen met meerdere zendingen die naar verschillende segmentbestemmingen op één route worden geleverd. Elke zending wordt toegewezen aan het meest geschikte routesegment op basis van de doeladressen van de zending en het segment. De functie berekent vervolgens de vrachtkosten van elke zending als een verhouding van de totale vrachtkosten van de zending op basis van het relatieve gewicht, het volume, de hoeveelheid en de afgelegde afstand van de zending. Deze functie is alleen van toepassing op zendingen die worden beheerd met de module Transportbeheer (TMS). |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.30 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.30 van Finance and Operations-apps (november 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md). <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van versie 10.0.29, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365- en bedrijfsclouds: releasewave 1-plan van 2022

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk de [Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2022](/dynamics365-release-plan/2022wave2/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Verwijderde en afgeschafte functies voor Supply Chain Management

In het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
