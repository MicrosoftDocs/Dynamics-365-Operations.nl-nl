---
title: Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)
description: In dit artikel worden de functies beschreven die in Dynamics 365 Supply Chain Management 10.0.21 nieuw of gewijzigd zijn.
author: kamaybac
ms.date: 10/28/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: a78b4c37bfca9fedbd46cd8a16b47bd4444fbfee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849527"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10021-october-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.21 (oktober 2021)

[!include [banner](../includes/banner.md)]

In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in versie 10.0.21 van Microsoft Dynamics 365 Supply Chain Management. Deze versie heeft een buildnummer van 10.0.960 en is als volgt beschikbaar:

- **Preview van versie:** augustus 2021
- **Algemene beschikbaarheid van versie (zelfupdate):** september 2021
- **Algemene beschikbaarheid van versie (automatische update):** oktober 2021

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. De kolom *Functie* bevat koppelingen naar het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) waar u de officiële vrijgavedatums voor elke functie kunt zien. De kolom *Meer informatie* bevat meer details en/of koppelingen naar gerelateerde documentatie.

De meeste functies moeten worden ingeschakeld via [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voordat u ze kunt gebruiken.

| Functiegebied | Functie | Meer informatie |
|---|---|---|
| Voorraad en logistiek | [Invoegtoepassing voor Algemene voorraadboekhouding voor Dynamics 365 Supply Chain Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/global-inventory-accounting-add-in-dynamics-365-supply-chain-management) | [Startpagina Algemene voorraadboekhouding](../global-inventory-accounting/global-inventory-accounting-home.md) |
| Voorraad en logistiek | [Voorhanden correcties boeken met codes die zijn gekoppeld aan tegenrekeningen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/post-on-hand-adjustments-using-configurable-reason-codes-connected-offset-accounts) | [Redencodes voor voorraadtelling](../warehousing/reason-codes-for-counting-journals.md) |
| Voorraad en logistiek | [Verkoopofferte verwees naar gegevensexportbeleid](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy) | Kies of wijzigingen in gegevens waarnaar wordt verwezen door offertes ertoe leiden dat die offertes (of regels) worden opgenomen in de volgende incrementele export. Uw incrementele exporten worden sneller uitgevoerd als u ervoor kiest om dergelijke offertes of regels niet op te nemen.<br><br>Met deze functie voegt u een instelling toe met de naam **Gegevens waarnaar door verkoopoffertes wordt verwezen, overslaan tijdens bijhouden van wijzigingen** aan de pagina **Parameters van module Klanten**. |
| Voorraad en logistiek | [Verzegelde biedingen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sealed-bidding) | [Verzegelde biedingen voor offerteaanvragen](../procurement/sealed-bidding.md) |
| Voorraad en logistiek | [Softe reservering voor de invoegtoepassing van de voorraadzichtbaarheid](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/soft-reservation-inventory-visibility-add-in) | [Reserveringen voor voorraadzichtbaarheid](../inventory/inventory-visibility-reservations.md) |
| Voorraad en logistiek | [Verbeteringen van aftrek en catch weight voor Kortingsbeheer](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/deduction-catch-weight-enhancements-rebate-management) | [Inhoudingen beheren met de inhoudingsworkbench](../rebate-management/deduction-workbench.md )<br><br>[Kortingen verwerken, controleren en posten](../rebate-management/process-review-post.md)<br><br>[Deals voor kortingsbeheer](../rebate-management/rebate-management-deals.md) |
| Voorraad en logistiek | [Stapinstructies van magazijnapp](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-app-step-instructions) | [Staptitels en instructies aanpassen voor de mobiele app Warehouse Management](../warehousing/mobile-app-titles-instructions.md) |
| Voorraad en logistiek | [Werkopsplitsing- en traceringsupdates voor Francoprijzen](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/work-breaks-tracking-updates-landed-cost) | [Bijhouden van updates voor wegzetten](../landed-cost/update-tracking-putaway.md )<br><br>[Goederen in transit verwerken](../landed-cost/in-transit-processing.md) |
| Hoofdplanning | [Negatieve dagen voor Planningsoptimalisatie](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/negative-days-support-planning-optimization) | [Vertragingstolerantie (negatieve dagen)](../master-planning/planning-optimization/delay-tolerance.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven). Als u een van deze functies wilt gebruiken, moet u deze expliciet inschakelen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functie&nbsp;naam&nbsp;in Functie&nbsp;beheer | Meer informatie |
|---|---|---|
| Kostenbeheer | Voortgangsdetails van voorraadsluiting | Deze preview-functie biedt een gedetailleerde weergave van de voortgang van voorraadafsluiting. |
| Inkoopbeheer | Oververbruik van algemene budgetreserveringen voorkomen als er meerdere opdrachten tot inkoop in een workflow zijn | Met deze preview-functie wordt de foutcontrole verbeterd wanneer gebruikers inkoopopdrachten indienen en goedkeuren die het resterende saldo van een algemene budgetreserveringsregel overschrijden. Dit helpt om een te hoog verbruik van algemene budgetreserveringen te voorkomen wanneer er meerdere inkoopopdrachten in de werkstroom zijn. |
| Productiebeheer | Volledige serie-, batch- en nummerplaatnummers tonen in de uitvoeringsinterface van de productievloer | Deze functie biedt een betere ervaring met het weergeven van lijsten met serie-, batch- en nummerplaatnummers in de uitvoeringsinterface van de werkvloer. De weergave verandert van een kaartweergave met een beperkt aantal tekens in een lijstweergave die voldoende ruimte biedt om de volledige waarden weer te geven. De lijst biedt ook de mogelijkheid om naar specifieke nummers te zoeken. |
| Verkoopbeheer en marketing | Het aantal verkooporders beperken dat kan worden geselecteerd voor boeking | Met deze functie kunt u het maximum aantal verkooporders vastleggen, dat tijdens het boeken van bevestigingen, orderverzamellijsten, pakbonnen en facturen op de pagina met verkooporderlijsten geselecteerd kan worden. Deze wordt automatisch ingeschakeld. Met deze functie kunt u een instelling met de naam **Max. aantal verkooporders voor het boeken** toevoegen aan de pagina **Parameters van module Klanten**. De nieuwe instelling heeft standaard een waarde van *100*. Deze functie zorgt ervoor dat de prestaties van de pagina met verkooporderlijsten worden verbeterd wanneer er een bepaald aantal verkooporders geselecteerd wordt. Dit heeft geen invloed op het aantal verkooporders dat door een periodieke taak kan worden verwerkt. |
| Magazijnbeheer | Opslagwerk loskoppelen van ASN's | Deze functie is vereist voor het verzenden en ontvangen van advance shipping notices (ASN's) wanneer u een werkbelasting van magazijnbeheer uitvoert op een schaaleenheid (als onderdeel van een gedistribueerde hybride topologie). Er wordt een nieuwe databasetabel toegevoegd die speciaal is bedoeld voor het opslaan van informatie over wegzetwerk. Eerder is deze informatie opgeslagen in tabellen die ook worden gebruikt voor de ASN's. |
| Magazijnbeheer | Ruimte met gemengde eenheden | Items kunnen op locaties met gemengde eenheden (zoals dozen en kisten) worden weggezet. Voor elke sjabloonregel voor vakken kunt u met deze functie kiezen of met de regel artikelen op locaties met gemengde eenheden of met één eenheid moeten worden geplaatst. |
| Magazijnbeheer | Snellere API gebruiken voor het sluiten/heropenen van containers op inpakstation | Wanneer deze preview-functie is ingeschakeld, worden voorraadtransacties met betrekking tot containers gemaakt met behulp van een nieuw proces waarmee de prestaties van het sluiten of opnieuw openen van containers worden verbeterd tijdens de verwerking op handmatige inpakstations. |

## <a name="features-turned-on-by-default-in-this-release"></a>Functies die standaard zijn ingeschakeld in deze release

De volgende tabel vermeldt de functies die standaard zijn ingeschakeld in 10.0.21. De meeste functies die standaard zijn ingeschakeld, kunnen worden uitgeschakeld in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Functienaam | Inschakeldatum | Functie toegevoegd op | Functiestatus | Module |
| :--- | :--- | :--- | :--- | :--- |
| Opslag voor rapporten voorhanden voorraad | 1-9-2021 | 1-4-2020 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Annulering van transferorder | 1-9-2021 | 13-7-2020 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Voorraadjournaal ontgrendelen | 1-9-2021 | 17-8-2020 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Opgeslagen weergaven voor voorraadbeheer | 1-9-2021 | 30-9-2020 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Navigatie naar stuklijstversie vanuit stuklijstregels | 1-9-2021 | 11-11-2019 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Het gebruik van maateenheid en eenheidshoeveelheid in voorraadjournalen | 1-9-2021 | 11-11-2019 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Lege batchkenmerkwaarden toestaan | 1-9-2021 | 11-11-2019 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Automatische verhoging van regelnummers van de regels van voorraadtransferorders | 1-9-2021 | 11-10-2019 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Goedkeuringswerkstroom voorraadjournaal | 1-9-2021 | 6-1-2020 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Waarschuwingsfunctie voor parameters voorraadkwaliteitsbeheer inschakelen | 1-9-2021 | 7-10-2019 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Transferorder maken op basis van verkoopregel | 1-9-2021 | 31-8-2019 | Standaard ingeschakeld | Voorraad- en magazijnbeheer |
| Selectie prognosemodel in Details vraagprognose | 1-9-2021 | 11-10-2019 | Standaard ingeschakeld | Hoofdplanning |
| Voortgangsvisualisatie hoofdplanning | 1-9-2021 | 7-10-2019 | Standaard ingeschakeld | Hoofdplanning |
| Automatisch fiatteren voor Planningsoptimalisatie | 1-9-2021 | 11-10-2019 | Standaard ingeschakeld | Hoofdplanning |
| Parallelle fiattering van geplande orders | 1-9-2021 | 31-8-2019 | Standaard ingeschakeld | Hoofdplanning |
| Bericht over geslaagde indiening van bod | 1-9-2021 | 15-5-2019 | Standaard ingeschakeld | Inkoopbeheer |
| Verwijzingskoppeling voor offerteaanvraag toegevoegd aan IO | 1-9-2021 | 31-8-2019 | Standaard ingeschakeld | Inkoopbeheer |
| Mogelijkheid om geaccepteerde inkooporders van leverancierssamenwerking in batch te bevestigen | 1-9-2021 | 10-9-2019 | Standaard ingeschakeld | Inkoopbeheer |
| Verbeteringen inkoop-cXML | 1-9-2021 | 11-11-2019 | Standaard ingeschakeld | Inkoopbeheer |
| De koppeling &quot;Gepubliceerde offerteaanvragen openen&quot; weergeven als tegel | 1-9-2021 | 30-9-2020 | Standaard ingeschakeld | Inkoopbeheer |
| Vragen en antwoorden offerteaanvraag | 1-9-2021 | 19-2-2020 | Standaard ingeschakeld | Inkoopbeheer |
| Productinformatie en verzendingsdocumentatie over gevaarlijke materialen | 1-9-2021 | 14-6-2020 | Standaard ingeschakeld | Productgegevensbeheer |
| Strikte validatie van standaardorderhoeveelheden | 1-9-2021 | 24-6-2020 | Standaard ingeschakeld | Productgegevensbeheer |
| Functie voor beheer van land van oorsprong | 1-9-2021 | 13-7-2020 | Standaard ingeschakeld | Productgegevensbeheer |
| Opgeslagen weergaven voor vrijgegeven producten | 1-9-2021 | 30-9-2020 | Standaard ingeschakeld | Productgegevensbeheer |
| Verbeteringen in de dialoogvensters Taken goedkeuren en Taken overboeken | 1-9-2021 | 11-10-2019 | Standaard ingeschakeld | Productiebeheer |
| Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten | 1-9-2021 | 31-8-2019 | Standaard ingeschakeld | Productiebeheer |
| De nieuwe knop Pauze stoppen is toegevoegd aan de pagina Taakkaartterminal | 1-9-2021 | 19-2-2020 | Standaard ingeschakeld | Productiebeheer |
| Schakel gedeeltelijke ontvangst van uitbestede artikelen in en los een probleem op met de berekening van uitval voor stuklijstregels van het type Leverancier. | 1-9-2021 | 11-11-2019 | Standaard ingeschakeld | Productiebeheer |
| Opgeslagen weergaven voor productiebeheer | 1-9-2021 | 17-8-2020 | Standaard ingeschakeld | Productiebeheer |
| Dynamics 365 Guides voor productie | 1-9-2021 | 13-7-2020 | Standaard ingeschakeld | Productiebeheer |
| Uitvoering werkvloer | 1-9-2021 | 30-9-2020 | Standaard ingeschakeld | Productiebeheer |
| Functie voor vergrendelen van taakkaartapparaat en taakkaartterminal zodat ze kunnen worden schoongemaakt | 1-9-2021 | 10-5-2020 | Standaard ingeschakeld | Productiebeheer |
| Toewijzing van toeslagen voor een verkooporder | 1-9-2021 | 30-9-2020 | Standaard ingeschakeld | Verkoopbeheer en marketing |
| Het aantal verkooporders beperken dat kan worden geselecteerd voor boeking | 1-9-2021 | 1-9-2021 | Standaard ingeschakeld | Verkoopbeheer en marketing |
| Verkooporderhistorie voor update opschonen | 1-9-2021 | 1-9-2021 | Standaard ingeschakeld | Verkoopbeheer en marketing |
| De nummerreeks voor cyclustellingswerk wijzigen | 1-9-2021 | 7-10-2019 | Standaard ingeschakeld | Magazijnbeheer |
| Aanvulling op wavevraag op basis van taken | 1-9-2021 | 7-10-2019 | Verplicht | Magazijnbeheer |
| Het veld Totale waarde verbergen op de pagina's &quot;Alle ladingen&quot; en &quot;Ladingdetails&quot; | 1-9-2021 | 7-10-2019 | Standaard ingeschakeld | Magazijnbeheer |
| Wavelabels afdrukken | 1-9-2021 | 19-2-2020 | Verplicht | Magazijnbeheer |
| Voorraadtransacties van inkooporder koppelen aan lading | 1-9-2021 | 6-1-2020 | Verplicht | Magazijnbeheer |
| Verbeterde indelingen voor nummerplaatlabels | 1-9-2021 | 19-2-2020 | Standaard ingeschakeld | Magazijnbeheer |
| Werk blokkeren voor de hele organisatie | 1-9-2021 | 19-2-2020 | Verplicht | Magazijnbeheer |
| Details werkregel | 1-9-2021 | 11-10-2019 | Standaard ingeschakeld | Magazijnbeheer |
| Het voorraadstatusveld van de voorraadverplaatsing van het mobiele apparaat bewerkbaar maken | 1-9-2021 | 16-10-2019 | Standaard ingeschakeld | Magazijnbeheer |
| Uitgaande zendingen vanuit batchtaken bevestigen | 1-9-2021 | 13-7-2020 | Standaard ingeschakeld | Magazijnbeheer |
| Bepalen of u een ontvangstoverzichtspagina wilt weergeven op mobiele apparaten | 1-9-2021 | 1-4-2020 | Standaard ingeschakeld | Magazijnbeheer |
| Vragen om niet-eenduidige &#39;Loc/LP&#39;-namen op te lossen | 1-9-2021 | 1-4-2020 | Standaard ingeschakeld | Magazijnbeheer |
| Productvarianten en traceringsdimensies vastleggen in de magazijnbeheer-app tijdens het ontvangen van ladingsartikel | 1-9-2021 | 10-5-2020 | Standaard ingeschakeld | Magazijnbeheer |
| Sta niet toe dat er ladingen worden gemaakt die niet voldoen aan de sjabloonvereisten voor het maken van wavelading. | 1-9-2021 | 17-8-2020 | Standaard ingeschakeld | Magazijnbeheer |
| Alle acties voor locatie-instructies met meerdere SKU's evalueren | 1-9-2021 | 30-9-2020 | Standaard ingeschakeld | Magazijnbeheer |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-artikelen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Ze zijn niet noodzakelijkerwijs gerelateerd aan de nieuwe functies die zijn toegevoegd voor deze versie, zoals wordt beschreven in de vorige sectie, maar ze kunnen u helpen om meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte artikelen |
|---|---|
| Hoofdplanning | [Voorraadprognoses](../master-planning/inventory-forecast.md) |
| Hoofdplanning | [Parameters die niet worden gebruikt door Planningsoptimalisatie](../master-planning/planning-optimization/not-used-parameters.md) |
| Hoofdplanning | [Aanvullingsmethoden en gewijzigde hoeveelheden](../master-planning/planning-optimization/replenishment-methods-quantity-modification.md) |
| Hoofdplanning | [Plannen met onbeperkte capaciteit](../master-planning/planning-optimization/infinite-capacity-planning.md) |
| Hoofdplanning | [Planhistorie en planningslogboeken weergeven](../master-planning/planning-optimization/plan-history-logs.md) |
| Magazijnbeheer | [Verpakkingsstrategieën voor containers](../warehousing/container-packing-strategy-overview.md) |
| Magazijnbeheer | [Voorbeeldscenario's voor cyclustelling](../warehousing/cycle-counting-scenarios.md) |
| Magazijnbeheer | [Inkomende ASN's importeren via de V3-gegevensentiteit](../warehousing/import-asn-data-entity.md) |
| Magazijnbeheer | [Oververzamelen voor verkooporders en overboekingsorders](../warehousing/over-picking-for-sales-and-transfer-orders.md) |
| Magazijnbeheer | [Afdrukken van wavelabels plannen tijdens wave](../warehousing/configure-task-based-wave-label-printing.md) |
| Magazijnbeheer | [Nieuwe of gewijzigde functies in de mobiele app Warehouse Management](../warehousing/whats-new-wma.md) |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.21 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.21 van apps voor financiële en bedrijfsactiviteiten (oktober 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.21, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=605166&dbType=3&qc=4b9449bf0d947113983bd0697140bf4d8727bfafd5566aa682cb38db343374de).

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
