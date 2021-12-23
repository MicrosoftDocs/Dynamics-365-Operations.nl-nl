---
title: Preview van Dynamics 365 Supply Chain Management 10.0.23 (januari 2022)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.23.
author: kamaybac
ms.date: 10/15/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: fd6483c86b34d355e3727a95794b7876dc54ec32
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891788"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10023-january-2022"></a>Preview van Dynamics 365 Supply Chain Management 10.0.23 (januari 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in de preview van Microsoft Dynamics 365 Supply Chain Management versie 10.0.23. Deze versie heeft een buildnummer van 10.0.1037 en is als volgt beschikbaar:

- **Preview van versie:** oktober 2021
- **Algemene beschikbaarheid van versie (zelfupdate):** december 2021
- **Algemene beschikbaarheid van versie (automatische update):** januari 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. De kolom *Functie* bevat koppelingen naar het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) waar u de officiële vrijgavedatums voor elke functie kunt zien. De kolom *Meer informatie* bevat meer details en/of koppelingen naar gerelateerde documentatie. Zie de kolom *Ingeschakeld per* om te bepalen hoe u een functie kunt inschakelen. Zie [Overzicht Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)voor meer informatie over het gebruik van Functiebeheer. Mogelijk wordt dit onderwerp gewijzigd om functies op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door   |
|---|---|---|---|
| Algemeen adresboek | Een standaardstaat/-provincie definiëren voor een land/regio in adresinstellingen | U kunt nu een standaardstaat/-provincie definiëren voor een land/regio in de adresinstellingen voor het globale adresboek. Wanneer een standaardstaat/-provincie is ingesteld, wordt dit de standaardwaarde die is ingevoerd in de velden voor de staat/provincie wanneer u een nieuwe staat- of plaatsrecord voor een land/regio maakt. Zie ook [Adresinstellingen](../../fin-ops-core/fin-ops/organization-administration/global-address-book-address-setup.md?toc=/dynamics365/supply-chain/toc.json) | Standaard ingeschakeld. |
| Voorraad en logistiek | [Taken onderbreken in de mobiele app Warehouse Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/park-tasks-warehouse-management-mobile-app) | [Omleidingen configureren voor stappen in menu-items van mobiele apparaten](../warehousing/warehouse-app-detours.md) | Functiebeheer (*Omleidingen van app Warehouse Management*) |
| Voorraad en logistiek | [Gepropageerde velden van magazijnapp](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Gepropageerde velden configureren voor stappen in het mobiele apparaat](../warehousing/warehouse-app-promoted-fields.md)| Functiebeheer (*Gepropageerde velden van magazijnapp*) |
| Productie | [Integratie met productie-uitvoeringssystemen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-systems-integration) | [Integratie met productie-uitvoeringssystemen van derden](../production-control/mes-integration.md) | Functiebeheer: (*Integratie met productie-uitvoeringssysteem*) |
| Productie | [Rapport over co- en bijproducten uit de uitvoeringsinterface op de productievloer](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | [Hoe medewerkers de uitvoeringsinterface voor de werkvloer gebruiken](../production-control/production-floor-execution-use.md) | Functiebeheer (*Rapport over co- en bijproducten uit de uitvoeringsinterface op de productievloer*) |
| Planning | [Planningsoptimalisatie-ondersteuning voor op prioriteit gebaseerde planning](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-priority-based-planning) | [Op prioriteit gebaseerde planning](../master-planning/planning-optimization/priority-based-planning.md) | Functiebeheer: (*Prioriteitsgestuurde MRP-ondersteuning voor Planningsoptimalisatie*) |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die nieuw zijn voor deze versie. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven).

Als u een van deze functies wilt in- of uitschakelen, moet u dit doen in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), waar deze worden weergegeven met de namen die worden weergegeven in de kolom *Functienaam in functiebeheer* van de volgende tabel.

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Activabeheer | Tegenrekeningen voor onkosten in werkorderjournaden | Met deze functie kunt u een tegenrekening opgeven voor alle onkosten die worden vermeld in een werkorderjournaal. U kunt doorgaans een leveranciersrekening aan elke onkosten koppelen, maar andere rekeningtypen worden ook ondersteund. Er worden twee nieuwe kolommen (**Tegenrekeningtype** en **Tegenrekening**) toegevoegd aan het sneltabblad **Onkosten** op de pagina **Werkorderjournaal**.|
| Kostenbeheer | Gerelateerde boekstukken maken voor herwaarderingen van standaardkostenafrondingen | <p>Wanneer er een financiële voorraadboeking (zoals een verkooporderfactuur of voorraadtransactie) wordt gemaakt, maakt het systeem door deze functie een afzonderlijk boekstuk voor alle gerelateerde herwaarderingen van standaardkosten voor afronding van de kostprijs en koppelt dit aan het boekstuk van de financiële boeking als een gerelateerd boekstuk.</p><p>Zonder deze functie registreert het systeem herwaarderingen van standaardkostenafronding op dezelfde boekstukboeking. Dat gedrag kan soms tot gegevens met tegenstrijdige datums leiden, omdat bij de herwaarderingen de sessie- of systeemdatum wordt gebruikt, terwijl financiële boekingen de boekingsdatum gebruiken.</p> |
| Voorraad- en magazijnbeheer | \[Rusland\] Stornotransacties voor financiële voorraad boeken volgens de correctiemarkering in het financiële boekstuk voor verkooporders | Deze functie is van invloed op de functionaliteit voor correcties van creditnota's voor Rusland. Hiermee wordt het boeken van voorraadtransacties voor verkoopfacturen in overeenstemming met de correctieoptie in het grootboek mogelijk. Wanneer deze functie is ingeschakeld, zijn er geen verschillen meer tussen de vlag **Correctie** op het financiële boekstuk van de voorraadtransactie en de vlag **Storno** op voorraadtransacties. |
| Voorraad- en magazijnbeheer | (Rusland) Berekening van omzetrapport van voorraadsaldo in batch uitvoeren | Deze functie verschaft voor Russische lokalisaties van Supply Chain Management de mogelijkheid het rapport *Omzet van voorraadsaldi* in batch uit te voeren, dit op te slaan en de rapporten die eerder zijn gegenereerd, weer te geven. |
| Voorraad- en magazijnbeheer | (Rusland) Vertalingen naar lokale taal gebruiken in land- of regiospecifieke primaire formulieren in Voorraadbeheer | Deze functie maakt voor Russische lokalisaties van Supply Chain Management gebruik van Russische vertalingen mogelijk voor product-/artikelnamen en maateenheden in de volgende specifiek Russische voorraadafdrukken:Tellijst (INV-3),Tellijst (INV-5),Tellijst (INV-6). |
| Hoofdplanning | Vraagprognose voor service Azure Machine Learning service | Met deze functie kan Azure Machine Learning Service vraagprognoses genereren op basis van historische gegevens. Zie voor meer informatie [Instelling van Vraagprognose](../master-planning/demand-forecasting-setup.md). |
| Inkoopbeheer | Inkooporderhistorie voor update opschonen | Met deze functie kunt u tijdelijke historische records opschonen die zijn gerelateerd aan updates van inkooporders. Hiermee wordt een nieuwe knop met de naam **Inkooporderhistorie voor update opschonen** aan het actievenster toegevoegd op de pagina **Alle inkooporders**. Deze functie is standaard ingeschakeld. |
| Productiebeheer | (Preview) Automatisch verzamelen van materialen waarvoor magazijn is ingeschakeld voor automatisch geboekte orderverzamellijsten | Met deze functie kunt u voorraaddimensies automatisch verzamelen en oplossen voor automatisch geboekte en terugwaarts afgeboekte orderverzamellijstjournalen. |
| Productiebeheer | Vervaldatum van grondstoffen valideren tegen geplande verbruiksdatum | Door deze functie wordt de validatie van batchverloopdatums gewijzigd bij het reserveren van een batch grondstoffen die tijdens de productie moet worden gebruikt. Wanneer deze functie is ingeschakeld, wordt de vervaldatum van de batch gevalideerd tegen de geplande verbruiksdatum (de grondstofdatum), zoals is vastgesteld op de productiestuklijstregel of batchorderformuleregel. Als deze functie is uitgeschakeld, wordt de batchvervaldatum gevalideerd tegen de geplande leveringsdatum van de productie- of batchorder (zoals eerder). |
| Verkoopbeheer en marketing | Verkoophistorie voor update opschonen op basis van ouderdom | Met deze functie kunt u de maximale ouderdom instellen van records die u wilt behouden wanneer de periodieke taak **Opschoning van verkoophistorie voor update** wordt uitgevoerd. Oudere records worden verwijderd. Dit is handig wanneer u de taak zo in stelt dat deze periodiek wordt uitgevoerd, omdat de ouderdom altijd wordt berekend in relatie tot de datum waarop de taak wordt uitgevoerd. Zonder deze functie kunt u alleen een specifieke datum instellen voor de oudste records die u kunt bewaren. |
| Verkoopbeheer en marketing | Prestaties van rapport 'Top 100 van klanten' verbeteren | Deze functie verbetert de prestaties van het rapport **Top 100**-klanten door altijd het rapport uit te voeren voor alle klanten (wat het bedoelde gebruik is) in plaats van aangepaste query's toe te staan. Wanneer deze functie is ingeschakeld, worden alle **Op te nemen records**-instellingen uitgeschakeld in het rapportdialoogvenster **Top 100**. |
| Magazijnbeheer | Ondersteuning van de eenheidseenheid voor het vrijgeven naar magazijn van uitgaande orders | Wanneer deze functie is ingeschakeld, kunnen uitgaande orders vanaf de hub direct worden vrijgegeven naar de schaaleenheid, waar de orders zullen worden uitgevoerd. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-onderwerpen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Deze onderwerpen hoeven niet te zijn gerelateerd aan de nieuwe functies die voor deze versie zijn toegevoegd, zoals in de vorige sectie is vermeld. Deze kunnen u echter helpen meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte onderwerpen |
|---|---|
| Beheer voor technische wijzigingen | [Technische kenmerken en zoekopdracht voor technische kenmerken](../engineering-change-management/engineering-attributes-and-search.md) beschrijft nu hoe overname van technische kenmerken werkt. |
| Hoofdplanning | [Hoofdplanning met vraagprognoses](../master-planning/planning-optimization/demand-forecast.md) en [Reductiesleutels van prognose](../master-planning/reduction-keys.md) bieden nu meer informatie over het werken met reductiesleutels. |
| Hoofdplanning | [Afhandeling van veiligheidsvoorraad voor artikelen](../master-planning/safety-stock-replenishment.md) biedt nu meer informatie over het gebruik van minimum-/maximumsleutels. |
| Hoofdplanning | [Voorraadprognoses](../master-planning/inventory-forecast.md) bevat nu meer informatie over het toewijzen van prognoses. |
| Hoofdplanning | [Voorraadplanning](../master-planning/supply-schedule.md) |
| Magazijnbeheer | [Algemene parameters voor mobiele apparaten](../warehousing/mobile-device-parameters.md) |
| Magazijnbeheer | [Verankering](../warehousing/anchoring.md) |
| Verkoopbeheer en marketing | Intercompany-handel wordt nu uitgebreid beschreven, te beginnen bij [Het instellen van intercompany-handel](../sales-marketing/intercompany-trade-set-up.md) en de gerelateerde onderwerpen. |
| Voorraadbeheer | De documentatie voor Voorraadzichtbaarheid is uitgebreid en bijgewerkt, te beginnen met [het overzicht van de invoegtoepassing Voorraadzichtbaarheid](../inventory/inventory-visibility.md) en de gerelateerde onderwerpen. |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platform updates voor Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.23 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.23 van Finance and Operations-apps (november 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-23.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.23, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=627874&dbType=3&qc=9b7e01944eb8b43f9c3aac4be26811c27be205847d6d2a240424f34f7e722910).

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2021

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk de [Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2021](/dynamics365-release-plan/2021wave2/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Verwijderde en afgeschafte functies voor Supply Chain Management

In het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
