---
title: Preview van Dynamics 365 Supply Chain Management 10.0.28 (augustus 2022)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.28.
author: kamaybac
ms.date: 05/27/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 306ff9be80c7a7a947b9132e3c9b4b9ec799b265
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813071"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10028-august-2022"></a>Preview van Dynamics 365 Supply Chain Management 10.0.28 (augustus 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management, previewversie 10.0.28. Deze versie heeft het buildnummer 10.0.1264 en is beschikbaar volgens de onderstaande planning:

- **Preview van versie:** mei 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** juli 2022
- **Algemene beschikbaarheid van versie (automatische update):** juli 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit onderwerp gewijzigd om functies op te nemen die zijn toegevoegd na de oorspronkelijke publicatie van dit onderwerp.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door   |
|---|---|---|---|
| Voorraad en logistiek | [Entiteiten voor integratie van francoprijzen voor externe expediteurs](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/landed-cost-integration-third-party-freight-forwarders) | [Overzicht van entiteiten voor francoprijzen](../landed-cost/landed-cost-entities-overview.md) | Standaard ingeschakeld |
| Planning | [Planningsoptimalisatie-ondersteuning voor houdbaarheid](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-shelf-life) | Binnenkort beschikbaar <!-- KFM: Vendor is preparing this. Expected May 20. --> | Standaard ingeschakeld |

<!-- KFM: Confirm status of this feature:
| Planning | [Demand Driven Material Requirements Planning (DDMRP)](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/demand-driven-material-requirements-planning-ddmrp) | Coming soon | Feature management:<br>*(Preview) DDMRP for Planning Optimization* | -->

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven).

Als u een van deze functies wilt in- of uitschakelen, moet u dat doen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Voorraad- en magazijnbeheer | Intercompany voorhanden voorraad inschakelen om alleen niet-nul voorhanden hoeveelheid weer te geven | Met deze functie kunt u kiezen of artikelen met een voorhanden hoeveelheid van nul in de lijst met intercompany voorhanden voorraad moeten worden opgenomen. U kunt deze optie beheren met de instelling **Artikelen met nul voorhanden hoeveelheid niet weergeven in de lijst met intercompany voorhanden voorraad** waarmee deze functie wordt toegevoegd aan de pagina **Voorraad- en magazijnbeheerparameters**. |
| Voorraad- en magazijnbeheer | (India) Voor transferprijsregels, negeer locatie wanneer "Van magazijncode" is ingesteld op "Alle" | <p>Deze functie is alleen van toepassing op lokalisaties in India. Het maakt het proces van het instellen van transferprijzen voor artikelen in voorraadtransfers intuïtiever.</p><p>U stelt transferprijzen in door elk artikel met transferprijsregels te configureren. Een manier om deze configuratie uit te voeren, is een regel op te nemen waarin het veld **Van magazijncode** is ingesteld op *Alle*. Met deze instelling wordt aangegeven dat de door de regel gedefinieerde transferprijs van toepassing is ongeacht het magazijn waaruit het artikel wordt opgehaald. Als deze functie is ingeschakeld, wordt de instelling **Locatie** genegeerd door de transferprijsregels in gevallen waarin het veld **Van magazijncode** is ingesteld op *Alle*. Dat betekent dat de regel van toepassing is ongeacht de locatie die op de transferorder wordt opgegeven. Dit gedrag is waarschijnlijk naar verwachting, omdat de locatie zich onder magazijn in de opslagdimensiehiërarchie bevindt.</p><p>Zonder deze functie worden regels van dit type alleen toegepast wanneer de locatie in de transferorder exact overeenkomt met de locatie die voor de regel is ingesteld. (Als een lege locatie is ingesteld voor de regel, wordt de regel alleen toegepast op transferorders die ook een lege waarde voor de locatie hebben.)</p> |
| Voorraad- en magazijnbeheer | Opschonen van gegevens in rapport met voorhanden voorraad | Deze functie biedt een manier om de gegevens op te schonen waarmee *Opslag voor rapporten voorhanden voorraad*-rapporten worden gemaakt. |
| Productiebeheer | Projectactiviteiten toewijzen voor serviceovereenkomst en serviceorderregels | Met deze functie wordt een veld met de naam **Projectactiviteit** toegevoegd aan serviceovereenkomst- en serviceorderregels, zodat u een projectactiviteit voor de regels kunt instellen. Deze functie helpt blokkeringsfouten te voorkomen wanneer u servicebeheerprojectjournalen boekt waarvoor een projectactiviteit moet worden ingesteld.  |
| Magazijnbeheer | Handmatige orderverzamelactiviteit van transferregels voor beheerder of soortgelijke vertrouwde gebruikers | Met deze functie kunnen beheerders handmatig voorraadtransacties verzamelen die zijn gerelateerd aan transferregels. Deze regels omvatten regels die reeds zijn vrijgegeven aan het magazijn. Beheerders mogen deze orderverzameling alleen uitvoeren in uitzonderlijke situaties, bijvoorbeeld wanneer het systeem beschadigd is. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-onderwerpen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Deze onderwerpen hoeven niet te zijn gerelateerd aan de nieuwe functies die voor deze versie zijn toegevoegd, zoals in de vorige secties is vermeld. Deze kunnen u echter helpen meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte onderwerpen |
|---|---|
| Kostenbeheer | [Vaste ontvangstprijs](../cost-management/fixed-receipt-price.md) |
| Kostenbeheer | [Veelgestelde vragen over kostprijsberekening van de voorraad](../cost-management/inventory-costing-faq.md) |
| Kostenbeheer | [Boekhoudprincipe voor boeken op toeslagrekening](../cost-management/post-to-charge-account-accounting-principle.md) |
| Voorraadbeheer | [Voorraadtransactiedetails](../inventory/inventory-transactions-details.md) |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.28 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.28 van apps voor financiële en bedrijfsactiviteiten (juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-28.md).<!-- KFM Confirm link -->

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.28, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

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
