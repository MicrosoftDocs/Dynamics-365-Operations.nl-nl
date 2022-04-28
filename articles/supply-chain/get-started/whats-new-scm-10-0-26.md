---
title: Preview van Dynamics 365 Supply Chain Management 10.0.26 (mei 2022)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.26.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 996988b1a4d59ae9ad7b4031e492824c0a6abc95
ms.sourcegitcommit: d475dea4cf13eae2f0ce517542c5173bb9d52c1c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547868"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10026-may-2022"></a>Preview van Dynamics 365 Supply Chain Management 10.0.26 (mei 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management, previewversie 10.0.26. Deze versie heeft een buildnummer van 10.0.1192 en is als volgt beschikbaar:

- **Preview van versie:** maart 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** april 2022
- **Algemene beschikbaarheid van versie (automatische update):** mei 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit onderwerp gewijzigd om functies op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door   |
|---|---|---|---|
| Voorraad en logistiek | [Query voor Voorraadzichtbaarheid om geavanceerde magazijnbeheerartikelen te ondersteunen](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Ondersteuning voor Inventory Visibility voor WHS-artikelen](../inventory/inventory-visibility-whs-support.md) | Functiebeheer:<br>*Magazijnartikelen inschakelen voor Voorraadzichtbaarheid* |
| Voorraad en logistiek | [Available to promise voor de invoegvoeging Voorraadzichtbaarheid](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Planningen van wijzigingen in voorhanden hoeveelheid en available to promise in Voorraadzichtbaarheid](../inventory/inventory-visibility-available-to-promise.md) | Ingeschakeld door serviceconfiguratie |
| Productie | [Catch weight-artikelen voor de uitvoeringsinterface voor de werkvloer](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Hoe medewerkers de uitvoeringsinterface voor de werkvloer gebruiken](../production-control/production-floor-execution-use.md) | Functiebeheer:<br>*(Preview) Rapport over catch weight-artikelen uit de uitvoeringsinterface van de productievloer* |
| Productie | Het tabblad Mijn taken in de uitvoeringsinterface voor de werkvloer <!-- KFM: Add link to release plan when available --> | [Hoe medewerkers de uitvoeringsinterface voor de werkvloer gebruiken](../production-control/production-floor-execution-use.md) | Functiebeheer:<br>*Het tabblad Mijn taken in de uitvoeringsinterface voor de werkvloer* |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven).

Als u een van deze functies wilt in- of uitschakelen, moet u dat doen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Inkoopbeheer | Geregistreerde hoeveelheden van producten in voorraad en restanten van niet-voorraadproducten voor ontvangstbewijzen en leveranciersfacturen boeken | Deze functie wijzigt de manier waarop hoeveelheden van producten die niet op voorraad zijn (zoals services), worden geboekt bij de verwerking van leveranciersfacturen en inkomende zendingen voor inkooporders. De functie stemt het gedrag van de hoeveelheidsoptie *Geregistreerde hoeveelheid en services* voor het boeken van ontvangsten en leveranciersfacturen af op de optie *Geregistreerde hoeveelheid en niet-voorraadproducten*, die al is opgegeven bij het boeken van hoeveelheden voor verkooppakbonnen.<br><br>Wanneer u een productontvangstbon of leveranciersfactuur boekt met de hoeveelheidsoptie *Geregistreerde hoeveelheid en services*, boekt het systeem de geregistreerde hoeveelheid in voorraadproducten en boekt het de resterende hoeveelheid als niet-voorraadproducten (inclusief zowel services als niet-services). Zonder deze functie boekt het systeem de geregistreerde hoeveelheid voorraadproducten (inclusief services die zijn geconfigureerd als voorraadartikelen) maar wordt altijd de volledige bestelde hoeveelheid niet-voorraadproducten geboekt (en negeert niet-voorraadproducten van het type *Service*). |
| Inkoopbeheer | Traceringsdimensies synchroniseren op intercompany-verkoop- en inkooporderregels | Met deze functie kunt u bepalen of de traceringsdimensies voor serie- en batchnummers worden gesynchroniseerd tussen intercompany-verkooporderregels en -inkooporderregels. Er worden nieuwe instellingen toegevoegd aan zowel het **inkooporderbeleid** als het tabblad **Verkooporderbeleid** van de pagina **Intercompany-instelling** voor klanten en leveranciers. Ook worden de namen van enkele verwante, dichtbijliggende instellingen voor de duidelijkheid bijgewerkt.<br><br>Als u geavanceerd magazijnbeheer (WMS) gebruikt, moet u er rekening mee houden dat alleen batch- en serienummers worden gesynchroniseerd wanneer deze dimensies zich boven de locatie in de reserveringshiërarchie van de doelbestemming bevinden. |
| Productgegevensbeheer | Waarden van productkenmerk opschonen | Met deze functie wordt een periodieke taak toegevoegd met de naam **Productkenmerkwaarden opschonen**, waarmee waarderecords worden opgeschoond van productkenmerken die niet meer aan een product zijn gekoppeld via een productcategorie. |
| Voorraad- en magazijnbeheer | (Rusland) Afwijkingen voorkomen bij het uitgeven van GTD's voor inkooporders die artikelen bevatten die zijn ingeschakeld voor WMS | Deze functie is alleen beschikbaar voor Russische lokalisatie. Hiermee worden discrepanties voorkomen die optreden bij het uitgeven van Russische GTD's (douaneaangiftenummers) voor inkooporders voor import die artikelen bevatten die zijn ingeschakeld voor geavanceerde magazijnen (WMS). Door het GTD-uitgifteproces worden sommige voorraaddimensiewaarden in de gerelateerde voorraadtransacties gewijzigd voor facturen in het aangepaste journaal, wat resulteert in verschillen tussen de werkrecords voor de inkooporder en de voorraadtransacties voor de inkoop. Wanneer deze functie is ingeschakeld, genereert het GTD-uitgifteproces correctiewerk waardoor dergelijke verschillen worden verwijderd. |
| Magazijnbeheer | Verbeterde parser voor GS1-streepjescodes | Deze functie voegt een verbeterde parser toe voor GS1-symboolgegevens. De nieuwe parser implementeert het GS1 General Specification-algoritme voor het parseren van GS1-symbolen en zorgt voor een betere gegevensvalidatie. Zie [GS1-streepjescodes scannen](../warehousing/gs1-barcodes.md) voor meer informatie. |
| Magazijnbeheer | Nieuwe workbenchpagina's voor ladingplanning | Hiermee worden twee nieuwe workbenchpagina's voor ladingplanning toegevoegd: **Workbench voor binnenkomende ladingplanning** en **Workbench voor uitgaande ladingplanning**. |
| Magazijnbeheer | Magazijnbeheertoepassing - lege GTD | Deze functie is alleen beschikbaar voor Russische lokalisatie. Met deze functie kunnen werknemers die de mobiele app Warehouse Management gebruiken, de Russische GTD's (douaneaangiftenummers) zo nodig leeg laten. Als de GTD-traceringsdimensie zo is ingesteld dat lege waarden zijn toegestaan, accepteert het systeem lege waarden voor GTD voor voorraadbewerkingen als voorhanden voorraad beschikbaar is. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-onderwerpen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Deze onderwerpen hoeven niet te zijn gerelateerd aan de nieuwe functies die voor deze versie zijn toegevoegd, zoals in de vorige secties is vermeld. Deze kunnen u echter helpen meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte onderwerpen |
|---|---|
| Kostenbeheer | Aan elk van de volgende onderwerpen zijn bijgewerkte voorbeelden en diagrammen toegevoegd:<ul><li>[FIFO met fysieke waarde en markering](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO met fysieke waarde en markering](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO-datum met fysieke waarde en markering](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Lopend gemiddelde kostprijs](../cost-management/running-average-cost-price.md)</li><li>[Gewogen gemiddelde met fysieke waarde en markering](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |
| Inkoopbeheer | [Verschillen in gegevens op inkooporderregels](../troubleshooting/procurement/purchase-order-line-data-issues.md) |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.26 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.26 van apps voor financiële en bedrijfsactiviteiten (mei 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.26, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

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
