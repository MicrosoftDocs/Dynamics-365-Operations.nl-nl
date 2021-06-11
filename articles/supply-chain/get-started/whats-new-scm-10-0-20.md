---
title: Preview van Dynamics 365 Supply Chain Management 10.0.20 (juli 2021)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Supply Chain Management 10.0.20.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: c009625204ef0fdc72c381b5fee11f4d031a6a82
ms.sourcegitcommit: 16376a301a0f121f384d77f9976638f701f8e88e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6123409"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10020-july-2021"></a>Preview van Dynamics 365 Supply Chain Management 10.0.20 (juli 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in de preview van Microsoft Dynamics 365 Supply Chain Management versie 10.0.20. Deze versie heeft een buildnummer van 10.0.886 en is als volgt beschikbaar:

- **Preview van versie:** mei 2021
- **Algemene beschikbaarheid van versie (zelfupdate):** juni 2021
- **Algemene beschikbaarheid van versie (automatische update):** juli 2021

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. De kolom *Functie* bevat koppelingen naar het [releaseplan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) waar u de officiële vrijgavedatums voor elke functie kunt zien. De kolom *Meer informatie* bevat meer details en/of koppelingen naar gerelateerde documentatie.

De meeste functies moeten worden ingeschakeld via [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voordat u ze kunt gebruiken. Sommige van de functies in de lijst zijn nog steeds in preview, terwijl andere mogelijk al algemeen beschikbaar zijn.

| Functiegebied | Functie | Meer informatie |
|---|---|---|
| Voorraad en logistiek | [Verbetering van prestaties verkooporderdetails](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Deze functie zorgt ervoor dat de gebruikersinterface beter reageert bij het openen van verkooporders, met name van orders met een groot aantal regels. |
| Productie | [Procesautomatiseringsstromen aanroepen om kwaliteitsorders te maken](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Procesautomatiseringsstromen aanroepen om kwaliteitsorders te maken](../production-control/process-automation-quality-orders.md ) |
| Productie | [Uitgebreide uitvoeringsinterface voor de werkvloer voor fabricage](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [De uitvoeringsinterface voor de werkvloer configureren](../production-control/production-floor-execution-configure.md) |
| Productgegevensbeheer | [Wijzigingen in formules en de ingrediënten beheren](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Wijzigingen in formules en de ingrediënten beheren](../engineering-change-management/manage-formula-changes.md) |
| Productgegevensbeheer | [Controles op productgereedheid](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Productgereedheid](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven). Als u een van deze functies wilt gebruiken, moet u deze expliciet inschakelen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Functiegebied | Functie&nbsp;naam&nbsp;in Functie&nbsp;beheer | Meer informatie |
|---|---|---|
| Hoofdplanning | Negatieve dagen voor Planningsoptimalisatie | Met deze preview-functie kan bij Planningsoptimalisatie rekening worden houden met vertragingstolerantie op basis van de parameter **Negatieve dagen** die is gedefinieerd in dekkingsgroepen. |
| Hoofdplanning | Parallelle autorisatie van gecorrigeerde vraagprognose | Deze functie maakt parallelle autorisatie van gecorrigeerde vraagprognose via de pagina **Gecorrigeerde vraagprognose** mogelijk. Deze functie is bedoeld om de prestaties te verbeteren wanneer een groot aantal prognoses wordt geautoriseerd. Tijdens het autoriseren kan de gebruiker het **aantal threads** in het autorisatiedialoogvenster opgeven. |
| Hoofdplanning | (Preview) Batchgewijs fiatteren en consolideren voor geplande batchorders voor bulk en verpakking | Met deze functie kunt u batchtaken gebruiken om geplande bulk- en verpakkingsorders te fiatteren en te consolideren. |
| Productiebeheer | Algemene routes kopiëren | Met deze functie wordt de kopieerroutefunctie verbeterd, zodat gebruikers routes kunnen kopiëren die niet artikelspecifiek zijn. Hiermee kan het systeem alle relevante informatie (zoals locatie, routegroep, resourcebehoeften en diverse keren) bijwerken nadat de kopieerroutefunctie is gebruikt om een route te overschrijven die nog niet aan een artikel is toegewezen. |
| Productiebeheer | Gerelateerde bronbehoeften bijwerken wanneer een routebewerking wordt gewijzigd | Met deze functie kan het systeem de gerelateerde bronbehoeften bijwerken nadat een gebruiker de bewerking van een bestaande routestap heeft gewijzigd. |
| Productgegevensbeheer | Voorverwerking van stuklijstrapporten om time-out te voorkomen | Deze functie zorgt ervoor dat het rapport met stuklijsten wordt voorverwerkt. Zo voorkomt u time-outproblemen wanneer er sprake is van een grote gegevensbelasting voor het rapport. |
| Inkoopbeheer | Het opnieuw instellen van inkoopgerelateerde werkstromen inschakelen | Met deze preview-functie kunt u de volgende werkstromen opnieuw instellen op conceptstatus: Inkooporder, Leverancierwijziging en Opdrachten tot inkoop. |
| Transportbeheer | Het maken van een leveranciersfactuurjournaal inschakelen wanneer een vrachtfactuur wordt genegeerd | Wanneer deze functie is ingeschakeld, wordt alleen een bijbehorend leveranciersfactuurjournaal gemaakt om afstemmingsredenen wanneer u de optie voor betalen van leverancier gebruikt. Anders wordt het factuurjournaal altijd gemaakt. |
| Magazijnbeheer | Sjablonen valideren die zijn geselecteerd voor aanvullingstaken | Met deze functie zorgt u ervoor dat gebruikers geldige aanvullingssjablonen selecteren bij het instellen van een aanvullingstaak. Hiermee voorkomt u dat gebruikers een aanvullingstaak maken zonder sjabloon en kunnen sjablonen van het type *Wavevraag*, waarmee geen aanvullingswerk wordt gemaakt en waarvan de verwerking mogelijk lang duurt, niet worden geselecteerd. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-onderwerpen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Ze zijn niet noodzakelijkerwijs gerelateerd aan de nieuwe functies die zijn toegevoegd voor deze versie, zoals wordt beschreven in de vorige sectie, maar ze kunnen u helpen om meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte onderwerpen |
|---|---|
| Beheer voor technische wijzigingen | [Levenscyclusstatussen van producten en transacties](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Voorraadbeheer | [Invoegtoepassing voorraadzichtbaarheid](../inventory/inventory-visibility.md)<br><br>[Overzicht van beheer voor kwaliteit en niet-conformering](../inventory/quality-management-processes.md) (plus alle gerelateerde onderwerpen over kwaliteitsbeheer) |
| Inkoopbeheer | [Leverancierscertificering onderhouden](../../finance/public-sector/manage-vendor-certification.md) |
| Productiebeheer | [De uitvoeringsinterface voor de werkvloer ontwerpen](../production-control/production-floor-execution-styles.md) |
| Magazijnbeheer | [Stappictogrammen en -titels toewijzen voor de mobiele app Warehouse Management](../warehousing/step-icons-titles.md)<br><br>[Uitgestelde verwerking van handmatige voorraadmutaties](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platform updates voor Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.20 bevat platform updates. Zie [Platform updates voor versie 10.0.20 van Finance and Operations- apps (juli 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md) voor meer informatie. <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.20, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8). 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: releasewave 1-plan van 2021

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk [Dynamics 365: releasewave 1-plan van 2021](/dynamics365-release-plan/2021wave1/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Verwijderde en afgeschafte functies voor Supply Chain Management

In het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
