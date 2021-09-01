---
title: Preview van Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Supply Chain Management 10.0.21.
author: kamaybac
ms.date: 08/02/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 517411512760374f1d1fd3b8ea3615563c47202c2e847569d00cb17a94657630
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012032"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10021-october-2021"></a>Preview van Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in de preview van Microsoft Dynamics 365 Supply Chain Management versie 10.0.21. Deze versie heeft een buildnummer van 10.0.960 en is als volgt beschikbaar:

- **Preview van versie:** augustus 2021
- **Algemene beschikbaarheid van versie (zelfupdate):** september 2021
- **Algemene beschikbaarheid van versie (automatische update):** oktober 2021

## <a name="known-deployment-issue"></a>Bekend implementatieprobleem
Bij de implementatie van release 10.0.21 op IaaS, ontvangt u mogelijk de volgende waarschuwing:

**Waarschuwingscode:** 95017

**Waarschuwingsbericht:** Uitvoering van script voor [SetupDiagnostics] VM is mislukt

De implementatie werkt ondanks de waarschuwing, maar de volgende bekende problemen kunnen zich voordoen in Lifecycle Services (LCS):

-   Op de pagina **Omgevingsbewaking** wordt de koppeling **Gedetailleerde versiegegevens weergeven** niet weergegeven, zodat u de specifieke versies van de modules die in uw omgeving zijn geïnstalleerd, niet kunt zien. Zonder deze gegevens kunnen volgende hotfixes mislukken, omdat bij het proces dat hotfixes gebruikt, deze gegevens worden gebruikt om te controleren of aan de vereisten van de moduleversie is voldaan. De impact moet minimaal zijn, omdat het niet mogelijk is om de PEAP/Preview-build in productie te gebruiken of hotfixes toe te passen.
-   Op de tabbladen **Prestatiemetingen** en **Indexanalyse** op de pagina **Omgevingsbewaking** onder SQL Insights worden geen gegevens weergegeven. Alle andere functies van **Omgevingsbewaking** werken zoals bedoeld.
-   De pagina **Volledige systeemdiagnose** is niet toegankelijk. De gekoppelde gegevens over de status van de nachtelijke collectoruitvoeringen en problemen die zijn gedetecteerd door de bijbehorende regels, worden ook niet weergeven.

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. De kolom *Functie* bevat koppelingen naar het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) waar u de officiële vrijgavedatums voor elke functie kunt zien. De kolom *Meer informatie* bevat meer details en/of koppelingen naar gerelateerde documentatie.

De meeste functies moeten worden ingeschakeld via [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voordat u ze kunt gebruiken. Sommige van de functies in de lijst zijn nog steeds in preview, terwijl andere mogelijk al algemeen beschikbaar zijn.

| Functiegebied | Functie | Meer informatie |
|---|---|---|
| Voorraad en logistiek | [Invoegtoepassing voor Algemene voorraadboekhouding voor Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Startpagina Algemene voorraadboekhouding](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Voorraad en logistiek | [Voorhanden correcties boeken met codes die zijn gekoppeld aan tegenrekeningen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Redencodes voor voorraadtelling](../warehousing/reason-codes-for-counting-journals.md) |
| Voorraad en logistiek | [Verkoopofferte verwees naar gegevensexportbeleid](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Kies of wijzigingen in gegevens waarnaar wordt verwezen door offertes ertoe leiden dat die offertes (of regels) worden opgenomen in de volgende incrementele export. Uw incrementele exporten worden sneller uitgevoerd als u ervoor kiest om dergelijke offertes of regels niet op te nemen.<br><br>Met deze functie voegt u een instelling toe met de naam **Gegevens waarnaar door verkoopoffertes wordt verwezen, overslaan tijdens bijhouden van wijzigingen** aan de pagina **Parameters van module Klanten**. |
| Voorraad en logistiek | [Streepjescodes scannen in het magazijn met behulp van GS1-indelingsstandaarden](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | *Binnenkort beschikbaar*<!-- KFM: Add doc link when ready. --> |
| Voorraad en logistiek | Verzegelde biedingen <!-- KFM: Add RP link when available --> | *Binnenkort beschikbaar*<!-- KFM: Add doc link when ready. --> |
| Voorraad en logistiek | [Verbeteringen van aftrek en catch weight voor Kortingsbeheer](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Inhoudingen beheren met de inhoudingsworkbench](../rebate-management/deduction-workbench.md )<br><br>[Kortingen verwerken, controleren en posten](../rebate-management/process-review-post.md)<br><br>[Deals voor kortingsbeheer](../rebate-management/rebate-management-deals.md) |
| Voorraad en logistiek | [Stapinstructies van magazijnapp](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | *Binnenkort beschikbaar*<!-- KFM: Add doc link when ready --> |
| Voorraad en logistiek | [Werkopsplitsing- en traceringsupdates voor Francoprijzen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Bijhouden van updates voor wegzetten](../landed-cost/update-tracking-putaway.md )<br><br>[Goederen in transit verwerken](../landed-cost/in-transit-processing.md) |
| Hoofdplanning | [Negatieve dagen voor Planningsoptimalisatie](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Vertragingstolerantie (negatieve dagen)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven). Als u een van deze functies wilt gebruiken, moet u deze expliciet inschakelen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Functiegebied | Functie&nbsp;naam&nbsp;in Functie&nbsp;beheer | Meer informatie |
|---|---|---|
| Kostenbeheer | Voortgangsdetails van voorraadsluiting | Deze preview-functie biedt een gedetailleerde weergave van de voortgang van voorraadafsluiting. |
| Hoofdplanning | (Preview) Prioriteitsgestuurde MRP-ondersteuning voor Planningsoptimalisatie | Met deze preview-functie voor Planningsoptimalisatie is hoofdplanning mogelijk via planningsprioriteit met bestelpunt. De gemarkeerde wijzigingen zijn onder andere: het veld **Planningsprioriteit** op verkooporderregels, inkooporderregels, vraagprognose en geplande orders; een nieuwe optie voor behoefteplanningscodes; het veld **Artikelbehoefteplanning** voor bestelpunt; instellingsformulieren voor hoofdplanning om de instelling van de planningsprioriteit te bepalen; en de berekeningslogica van Planningsoptimalisatie om de planningsprioriteit in te stellen en te respecteren. |
| Inkoopbeheer | Oververbruik van algemene budgetreserveringen voorkomen als er meerdere opdrachten tot inkoop in een workflow zijn | Met deze preview-functie wordt de foutcontrole verbeterd wanneer gebruikers inkoopopdrachten indienen en goedkeuren die het resterende saldo van een algemene budgetreserveringsregel overschrijden. Dit helpt om een te hoog verbruik van algemene budgetreserveringen te voorkomen wanneer er meerdere inkoopopdrachten in de werkstroom zijn. |
| Productiebeheer | Volledige serie-, batch- en nummerplaatnummers tonen in de uitvoeringsinterface van de productievloer | Deze functie biedt een betere ervaring met het weergeven van lijsten met serie-, batch- en nummerplaatnummers in de uitvoeringsinterface van de werkvloer. De weergave verandert van een kaartweergave met een beperkt aantal tekens in een lijstweergave die voldoende ruimte biedt om de volledige waarden weer te geven. De lijst biedt ook de mogelijkheid om naar specifieke nummers te zoeken. |
| Magazijnbeheer | Opslagwerk loskoppelen van ASN's | Deze functie is vereist voor het verzenden en ontvangen van advance shipping notices (ASN's) wanneer u een werkbelasting van magazijnbeheer uitvoert op een schaaleenheid (als onderdeel van een gedistribueerde hybride topologie). Er wordt een nieuwe databasetabel toegevoegd die speciaal is bedoeld voor het opslaan van informatie over wegzetwerk. Eerder is deze informatie opgeslagen in tabellen die ook worden gebruikt voor de ASN's. |
| Magazijnbeheer | Ruimte met gemengde eenheden | Items kunnen op locaties met gemengde eenheden (zoals dozen en kisten) worden weggezet. Voor elke sjabloonregel voor vakken kunt u met deze functie kiezen of met de regel artikelen op locaties met gemengde eenheden of met één eenheid moeten worden geplaatst. |
| Magazijnbeheer | Snellere API gebruiken voor het sluiten/heropenen van containers op inpakstation | Wanneer deze preview-functie is ingeschakeld, worden voorraadtransacties met betrekking tot containers gemaakt met behulp van een nieuw proces waarmee de prestaties van het sluiten of opnieuw openen van containers worden verbeterd tijdens de verwerking op handmatige inpakstations. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-onderwerpen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Ze zijn niet noodzakelijkerwijs gerelateerd aan de nieuwe functies die zijn toegevoegd voor deze versie, zoals wordt beschreven in de vorige sectie, maar ze kunnen u helpen om meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte onderwerpen |
|---|---|
| Hoofdplanning | [Voorraadprognoses](../master-planning/inventory-forecast.md) |
| Hoofdplanning | [Parameters die niet worden gebruikt door Planningsoptimalisatie](../master-planning/planning-optimization/not-used-parameters.md) |
| Hoofdplanning | [Aanvullingsmethoden en gewijzigde hoeveelheden](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Hoofdplanning | [Plannen met onbeperkte capaciteit](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Hoofdplanning | [Planhistorie en planningslogboeken weergeven](../master-planning/planning-optimization/plan-history-logs.md) |
| Magazijnbeheer | [Verpakkingsstrategieën voor containers](../warehousing/container-packing-strategy-overview.md) |
| Magazijnbeheer | [Voorbeeldscenario's voor cyclustelling](../warehousing/cycle-counting-scenarios.md) |
| Magazijnbeheer | [Inkomende ASN's importeren via de V2-gegevensentiteit](../warehousing/import-asn-v2-data-entity.md) |
| Magazijnbeheer | [Oververzamelen voor verkooporders en overboekingsorders](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Magazijnbeheer | [Afdrukken van wavelabels plannen tijdens wave](../warehousing/configure-task-based-wave-label-printing.md) |
| Magazijnbeheer | [Nieuwe of gewijzigde functies in de mobiele app Warehouse Management](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platform updates voor Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.21 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.21 van Finance and Operations-apps (oktober 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.21, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

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
