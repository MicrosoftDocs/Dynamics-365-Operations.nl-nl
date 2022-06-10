---
title: Preview van Dynamics 365 Supply Chain Management 10.0.27 (juli 2022)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.27.
author: kamaybac
ms.date: 04/22/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 77c79c88b08844bf7e399a762bb9eb9746ffb71a
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2022
ms.locfileid: "8812939"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10027-july-2022"></a>Preview van Dynamics 365 Supply Chain Management 10.0.27 (juli 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management, previewversie 10.0.27. Deze versie heeft het buildnummer 10.0.1227 en is beschikbaar volgens de onderstaande planning:

- **Preview van versie:** april 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** juni 2022
- **Algemene beschikbaarheid van versie (automatische update):** juli 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit onderwerp gewijzigd om functies op te nemen die zijn toegevoegd na de oorspronkelijke publicatie van dit onderwerp.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door |
|---|---|---|---|
| Voorraad en logistiek | [Voorraadtoewijzing voor de invoegtoepassing Voorraadzichtbaarheid](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-allocation-inventory-visibility-add-in) | [Voorraadtoewijzing voor voorraadzichtbaarheid](../inventory/inventory-visibility-allocation.md) | Standaard ingeschakeld |
| Productie | De weergave Mijn dag voor de uitvoeringsinterface voor de werkvloer | [Hoe medewerkers de interface voor de uitvoering van de productievloer gebruiken](../production-control/production-floor-execution-use.md) en [Verlofsaldi tonen in de uitvoeringsinterface voor de werkvloer](../production-control/production-floor-execution-payroll-stats.md) | Functiebeheer:<br>*De weergave Mijn dag voor de uitvoeringsinterface voor de werkvloer* |
| Planning | [Planningsoptimalisatie-ondersteuning voor uitbesteding](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-subcontracting) | [Uitbesteed werk in productie beheren](../production-control/manage-subcontract-work-production.md) | Standaard ingeschakeld |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven).

Als u een van deze functies wilt in- of uitschakelen, moet u dat doen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Hoofdplanning | Rekening houden met de doorlooptijd van de voorraad bij het maken van een geplande transferorder | Wanneer een geplande transferorder wordt gemaakt, kan het systeem met deze functie rekening houden met de doorlooptijd van de voorraad die is opgegeven in de standaardorderinstellingen van het artikel wanneer de ontvangstdatum van de geplande transferorder wordt berekend voor de instelling van het besturingselement als levertijd van het type *Geen* of *Verkoop*. Wanneer de transferdoorlooptijd wordt opgegeven, wordt de waarde hiervan gebruikt voor de berekening van de ontvangstdatum en worden transportdagen genegeerd. |
| Inkoopbeheer | Standaardbelastinginformatie voor contract voor tussenpersoon op leveranciersfactuurregels | Deze functie introduceert logica voor het instellen van standaardwaarden voor de velden **Btw** en **Btw van artikel** op leveranciersfactuurregels van het contract van de tussenpersoon. Deze logica wordt alleen toegepast wanneer het toeslagtype op de tussenpersooncontractregel grootboek/grootboek is. De btw-groep van het artikel gebruikt de standaardwaarde uit de inkoopcategorie van de tussenpersoon (als deze is ingesteld) of uit het toeslagtype. De btw-groep neemt de standaardwaarde over uit de leveranciersrekening. |
| Inkoopbeheer | Het aantal inkooporderregels per batchtaak beperken | Met deze functie kunt u de systeemprestaties optimaliseren bij het boeken van bevestigingen en productontvangstbonnen. Er is een nieuwe instelling toegevoegd met de naam **Regels per taak** aan het tabblad **Levering** van de pagina **Parameters voor inkoopbeheer**. Met deze nieuwe instelling kunt u het aantal inkooporderregels beperken dat elke batchtaak verwerkt. Hiermee kunt u voorkomen dat het systeem trager wordt door grote batchtaken. |
| Productgegevensbeheer | Productkenmerkwaarden invullen | Met deze functie wordt een periodieke taak toegevoegd met de naam *Productkenmerkwaarden invullen*. Met deze nieuwe periodieke taak worden ontbrekende productkenmerkwaarderecords gemaakt voor kenmerken die aan producten zijn gekoppeld via een productcategorie. |
| Productiebeheer | Aanvullende configuratie in de uitvoeringsinterface voor de werkvloer | <p>Met deze functie kunt u de volgende opties toevoegen aan de pagina **Uitvoering productievloer configureren**:</p><ul><li>**Dialoogvenster voor starten automatisch openen wanneer het zoeken wordt voltooid:** Als deze optie is ingeschakeld, wordt het dialoogvenster **Taak beginnen** automatisch geopend wanneer medewerkers een taak te zoeken met behulp van de zoekbalk.</li><li>**Dialoogvenster voor rapportvoortgang automatisch openen wanneer het zoeken wordt voltooid:** Als deze optie is ingeschakeld, wordt het dialoogvenster **Voortgang melden** voor de taak automatisch geopend wanneer medewerkers een taak te zoeken met behulp van de zoekbalk.</li><li>**Standaard resterende hoeveelheid in het dialoogvenster Voortgang melden:** als deze optie is ingeschakeld, wordt in het dialoogvenster **Voortgang melden** de resterende hoeveelheid weergegeven die moet worden gemeld voor een productietaak.</li></ul><p>Meer informatie over dit onderwerp vindt u in [Uitvoeringsinterface voor de werkvloer configureren](../production-control/production-floor-execution-configure.md).</p> |
| Productiebeheer | Productieteams in de uitvoeringsinterface voor de werkvloer | <p>Wanneer meerdere werknemers aan dezelfde productie taak zijn toegewezen, kunnen ze nu één werknemer nomineren als leider. De overige werknemers worden automatisch assistenten van die leider. Voor het team dat nu ontstaat moet alleen de leider de taakstatus registreren, terwijl tijdrecords van toepassing zijn op alle teamleden. Deze functie ondersteunt ook een scenario met de naam *Resource assisteren*. In dit scenario kan een werknemer zich registreren als assistent van een andere werknemer, die vervolgens de leider wordt voor de nieuwe gevormde groep.</p><p>Meer informatie over dit onderwerp vindt u in [Hoe medewerkers de uitvoeringsinterface voor de werkvloer gebruiken](../production-control/production-floor-execution-use.md).</p> |
| Productiebeheer | Rapporteren over planningsartikelen in de uitvoeringsinterface voor de werkvloer | Deze functie vereenvoudigt het rapportageproces voor batchorders voor planningsartikelen in de uitvoeringsinterface voor de productievloer. Wanneer er voor een product met het productietype *Planningsartikel* een batchorder wordt gemaakt, is het alleen mogelijk om gereed te melden voor de co-producten en bijproducten voor die batchorder. Batchorders voor planningsartikelen worden doorgaans gebruikt om demontageprocessen te ondersteunen, waarbij een grondstofproduct wordt opgesplitst in diverse verschillende producten. Wanneer een batchorder voor een planningsartikel wordt gereedgemeld, zien medewerkers nu alleen de co-producten en bijproducten in het dialoogvenster **Voortgang melden**. Eerder werd het planningsartikel ook weergegeven, wat voor medewerkers verwarrend kon zijn. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-onderwerpen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Deze onderwerpen hoeven niet te zijn gerelateerd aan de nieuwe functies die voor deze versie zijn toegevoegd, zoals in de vorige secties is vermeld. Deze kunnen u echter helpen meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte onderwerpen |
|---|---|
| Kostenbeheer | [Gewogen gemiddelde datum inclusief fysieke waarde en markering](../cost-management/weighted-average-date.md) |
| Gedistribueerde hybride topologie | [Schaaleenheden in een gedistribueerde hybride topologie uitproberen](../cloud-edge/cloud-edge-try-out.md) |
| Twee keer wegschrijven | [Op verzoek synchroniseren met de Supply Chain Management-prijsengine](../../fin-ops-core/dev-itpro/data-entities/dual-write/pricing-engine.md) |
| Magazijnbeheer | [Vrijgeven naar magazijn](../warehousing/release-to-warehouse-process.md) |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.27 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.27 van apps voor financiële en bedrijfsactiviteiten (juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-27.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.27, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365- en bedrijfsclouds: releasewave 1-plan van 2022

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk de [Dynamics 365- en bedrijfsclouds: releasewave 1-plan van 2022](/dynamics365-release-plan/2022wave1/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Verwijderde en afgeschafte functies voor Supply Chain Management

In het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
