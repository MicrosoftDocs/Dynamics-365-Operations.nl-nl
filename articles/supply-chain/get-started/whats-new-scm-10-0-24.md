---
title: Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.24 (februari 2022)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.24.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 94e465616338b0c905ccf6b8244324c18c7a59e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849440"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10024-february-2022"></a>Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.24 (februari 2022)

[!include [banner](../includes/banner.md)]

In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in versie 10.0.24 van Microsoft Dynamics 365 Supply Chain Management. Deze versie heeft een buildnummer van 10.0.1084 en is als volgt beschikbaar:

- **Preview van versie:** december 2021
- **Algemene beschikbaarheid van versie (zelfupdate):** januari 2022
- **Algemene beschikbaarheid van versie (automatische update):** februari 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit artikel gewijzigd om functies op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door   |
|---|---|---|---|
| Gedistribueerde hybride topologie | [Verbeterde werkbelasting voor magazijnuitvoering op schaaleenheden](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden](../cloud-edge/cloud-edge-workload-warehousing.md) | Standaard ingeschakeld. |
| Gedistribueerde hybride topologie | [Productieorder beginnen voor workloads voor magazijnbeheer voor de cloud- en randschaaleenheid](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-manufacturing-execution-workloads-scale-units) | [Werkbelasting voor productie-uitvoering voor cloud- en randschaaleenheden](../cloud-edge/cloud-edge-workload-manufacturing.md) | Functiebeheer (*Productieorder beginnen voor workloads voor magazijnbeheer voor de cloud- en randschaaleenheid*)  |
| Planning | [Ondersteuning van Planningsoptimalisatie voor bestel- en uitgiftemarges](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Veiligheidsmarges](../master-planning/planning-optimization/safety-margins.md) | Standaard ingeschakeld. |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven).

Als u een van deze functies wilt in- of uitschakelen, moet u dat doen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Productiebeheer | Controle voor beschikbaarheid van materiaal op aanvraag voor productieorders | Met deze functie opent u sneller de pagina **Vrij te geven productieorders**, die beschikbaar is vanuit de werkruimte **Productiebeheer**. Zonder deze functie controleert het systeem automatisch of materialen beschikbaar zijn voor alle vermelde productieorders zodra u de pagina opent, wat veel tijd kan kosten als u een groot aantal orders hebt. Wanneer deze functie is ingeschakeld, biedt het systeem in plaats daarvan een werkbalkknop die u kunt gebruiken om de materiaalcontrole alleen te starten voor geselecteerde orders en wanneer dat nodig is. |
| Productiebeheer | (Preview) Materiaalverbruik registreren op de uitvoeringsinterface van de werkvloer (niet-WMS) | Met deze functie kunnen werknemers de uitvoeringsinterface voor de werkvloer gebruiken om materiaalverbruik, batchnummers en serienummers te registreren. Deze functie ondersteunt alleen artikelen die niet zijn ingeschakeld om geavanceerde magazijnprocessen (WMS) te gebruiken. Ondersteuning voor WMS-artikelen is gepland voor een toekomstige versie.<p>Sommige fabrikanten, met name fabrikanten binnen de procesindustrieën, moeten de hoeveelheid verbruikt materiaal voor elke batch of productieorder expliciet registreren. Werknemers kunnen bijvoorbeeld een schaal gebruiken om te wegen hoeveel materiaal tijdens het werk wordt verbruikt. Voor volledige materiaaltraceerbaarheid moeten deze organisaties ook registreren welke batchnummers zijn verbruikt bij de productie van elk product. |
| Productiebeheer | Gereedmelden voor workloads voor magazijnbeheer voor de cloud- en randschaaleenheid | Met deze functie kunnen werknemers de mobiele app Warehouse Management gebruiken om een productie- of batchorder gereed te melden wanneer de app wordt uitgevoerd voor een workload voor magazijnbeheer in een cloud- of randschaaleenheid. Zie [Gereedmelden en wegzetten in een schaaleenheid](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF) voor meer informatie. |
| Magazijnbeheer | Nieuwe workbenchpagina's voor ladingplanning | Hiermee worden twee nieuwe workbenchpagina's voor ladingplanning gemaakt: **Workbench voor binnenkomende ladingplanning** en **Workbench voor uitgaande ladingplanning**. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-artikelen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Deze artikelen hoeven niet te zijn gerelateerd aan de nieuwe functies die voor deze versie zijn toegevoegd, zoals in de vorige sectie is vermeld. Deze kunnen u echter helpen meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte artikelen |
|---|---|
| Kostenbeheer | [Voorraadwaardenrapporten](../cost-management/inventory-value-report-storage.md) |
| Kostenbeheer | [Voorbeelden en logica voorraadwaardenrapporten](../cost-management/inventory-value-report-examples.md) |
| Hoofdplanning | [Datum- en tijdparameters die worden gebruikt door Planningsoptimalisatie](../master-planning/planning-optimization/date-time-used.md) |
| Hoofdplanning | [Instelling van Vraagprognose](../master-planning/demand-forecasting-setup.md) |
| Hoofdplanning | [Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning voor artikelen bij te werken](../master-planning/safety-stock-journal.md) |
| Productiebeheer | [De uitvoeringsinterface voor de productievloer aanpassen](../production-control/production-floor-execution-customize.md) |
| Productiebeheer | [De uitvoeringsinterface voor de werkvloer ontwerpen](../production-control/production-floor-execution-styles.md) |
| Verkoopbeheer en marketing | [Opschonen van verkoophistoriegegevens plannen](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Magazijnbeheer | [Gebruikersaccounts voor mobiele apparaten](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.24 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.24 van apps voor financiële en bedrijfsactiviteiten (februari 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.24, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2021

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk de [Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2021](/dynamics365-release-plan/2021wave2/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Verwijderde en afgeschafte functies voor Supply Chain Management

In het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
