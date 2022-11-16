---
title: Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.22 (november 2021)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.22.
author: kamaybac
ms.date: 08/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: b95f131a45c11748cfd4c66c47e5a51c765ed486
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740405"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10022-november-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.22 (november 2021)

[!include [banner](../includes/banner.md)]

In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in versie 10.0.22 van Microsoft Dynamics 365 Supply Chain Management. Deze versie heeft een buildnummer van 10.0.995 en is als volgt beschikbaar:

- **Preview-versie:** september 2021
- **Algemene beschikbaarheid van versie (zelfupdate):** oktober 2021
- **Algemene beschikbaarheid van versie (automatische update):** november 2021

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. De kolom *Functie* bevat koppelingen naar het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) waar u de officiële vrijgavedatums voor elke functie kunt zien. De kolom *Meer informatie* bevat meer details en/of koppelingen naar gerelateerde documentatie. Zie de kolom *Ingeschakeld per* om te bepalen hoe u een functie kunt inschakelen. Zie [Overzicht Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)voor meer informatie over het gebruik van Functiebeheer. Mogelijk wordt dit artikel gewijzigd om functies op te nemen die in de build zijn gemaakt nadat dit artikel oorspronkelijk werd gepubliceerd.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door |
|---|---|---|---|
| Planning | [Optimalisatieondersteuning voor capaciteitstoewijzing van bronnen plannen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-capability-based-resource-allocation) | [Plannen met resourceselectie op basis van mogelijkheden](../master-planning/planning-optimization/capability-based-scheduling.md) | Functiebeheer: *Onbeperkte capaciteitsplanning voor Planningsoptimalisatie* |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven). Als u een van deze functies wilt gebruiken, moet u deze expliciet inschakelen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Gedistribueerde hybride topologie | *(Functiebeheer is niet vereist.)* | <p>Deze versie biedt een uitbreiding op de uitgaande ladingsplanningsmogelijkheden van de warehouse management-werkbelasting voor cloud- en edge-schaaleenheden.</p><p>Zie [Workloads voor magazijnbeheer voor cloud- en edgeschaaleenheden](../cloud-edge/cloud-edge-workload-warehousing.md) voor meer informatie.</p> |
| Beheer voor technische wijzigingen | Varianten genereren voor technische producten | <p>Met deze functie kunt u verschillende varianten voor een engineeringproduct genereren op basis van de kleur, grootte, stijl of configuratiedimenssie.</p><p>Zie 'Varianten voor [engineeringproducten genereren'](../engineering-change-management/engineering-variants.md) voor meer informatie.</p> |
| Voorraad- en magazijnbeheer | Integratie van voorraadzichtbaarheid met verschuiving van reservering | <p>Deze functie kan alleen worden ingeschakeld nadat de functie *Service voor voorraadzichtbaarheid* is ingeschakeld. Deze functie biedt functionaliteit om reserveringen te compenseren die zijn gemaakt op voorraadzichtbaarheid.</p><p>Zie [Voorraadzichtbaarheid reserveringen](../inventory/inventory-visibility-reservations.md) voor meer informatie.</p> |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-artikelen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Deze artikelen hoeven niet te zijn gerelateerd aan de nieuwe functies die voor deze versie zijn toegevoegd, zoals in de vorige sectie is vermeld. Deze kunnen u echter helpen meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte artikelen |
|---|---|
| Beheer voor technische wijzigingen | [In het overzicht van engineeringwijzigingsbeheer](../engineering-change-management/product-engineering-overview.md) worden nu alle verwante, optionele functies vermeld die beschikbaar zijn in functiebeheer |
| Hoofdplanning | [Instelling van Vraagprognose](../master-planning/demand-forecasting-setup.md) |
| Hoofdplanning | [Nettovereisten en informatie over tracering van de behoefte](../master-planning/planning-optimization/net-requirements.md) |
| Magazijnbeheer | [Vrijgave naar magazijn ](../warehousing/release-to-warehouse-process.md) biedt een gedetailleerd overzicht van het proces voor volledige vrijgave naar magazijn |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiën en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.22 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.22 van apps voor financiën en bedrijfsactiviteiten (november 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.22, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=615299).

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

