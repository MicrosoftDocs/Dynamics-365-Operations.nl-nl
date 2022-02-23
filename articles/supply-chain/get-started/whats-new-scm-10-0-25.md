---
title: Preview van Dynamics 365 Supply Chain Management 10.0.25 (april 2022)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.25.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 0ce9bc4685542cf691d862c0fec76f3f7b40c6b6
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087315"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Preview van Dynamics 365 Supply Chain Management 10.0.25 (april 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in de preview van Microsoft Dynamics 365 Supply Chain Management versie 10.0.25. Deze versie heeft een buildnummer van 10.0.1149 en is als volgt beschikbaar:

- **Preview van versie:** februari 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** maart 2022
- **Algemene beschikbaarheid van versie (automatische update):** april 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit onderwerp gewijzigd om functies op te nemen die in de build zijn gemaakt nadat dit onderwerp oorspronkelijk werd gepubliceerd.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door   |
|---|---|---|---|
| Voorraad en logistiek | Verbeteringen gevaarlijke materialen | Deze verbeteringen zijn gebaseerd op bestaande functionaliteit voor gevaarlijke materialen om bedrijven te helpen bij het voldoen aan lokale regelgeving bij het transport van gevaarlijke materialen in verschillende regio's. <!-- KFM: Update to 2022w1 link when published -->| Functiebeheer:<br>*Verbeteringen gevaarlijke materialen* |
| Voorraad en logistiek | Inpakwerk voor inpakstations | Met deze functie worden de flexibiliteit en functionaliteit van uw verpakkings- en verzendbewerkingen verbeterd. Magazijnmedewerkers kunnen nu tijdens het verpakkingsproces afzonderlijke pakketten inpakken en verzenden die zijn gerelateerd aan dezelfde zending en lading. Orderregels die deel uitmaken van dezelfde zending hoeven niet samen te worden verzonden als sommige artikelen meteen klaar zijn voor verzending. Eén order kan in meerdere pakketten op verschillende verzendtijden worden verpakt en verzonden, waardoor de wachttijden worden verkort en de flexibiliteit wordt verbeterd.<!-- KFM: Update to 2022w1 link when published --> | Functiebeheer:<br>*Inpakwerk voor inpakstations* |
| Voorraad en logistiek | [Streepjescodes scannen in het magazijn met behulp van GS1-indelingsstandaarden](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) <!-- KFM: Update to 2022w1 link when published --> | [GS1-streepjescodes en QR-codes](../warehousing/gs1-barcodes.md) | Functiebeheer:<br>*GS1-streepjescode scannen* |
| Productie | [Materiaalverbruik en reserveringen in de uitvoeringsinterface van de productievloer](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Hoe medewerkers de uitvoeringsinterface voor de werkvloer gebruiken](../production-control/production-floor-execution-use.md) | Functiebeheer:<br>*(Preview) Materiaalverbruik registreren in de uitvoeringsinterface van de productievloer (WMS ingeschakeld)* |
| Productie | [Materiaalverbruik voor schaaleenheden registreren](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Werkbelasting voor productie-uitvoering voor cloud- en randschaaleenheden](../cloud-edge/cloud-edge-workload-manufacturing.md) | Functiebeheer:<br>*Materiaalverbruik op de mobiele app op een schaaleenheid registreren* |
| Planning | [Suggesties voor Planningsoptimalisatie om bestaande voorraad te optimaliseren](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Actieberichten](../master-planning/action-messages.md) | Standaard ingeschakeld |
| Planning | Geplande orders vereenvoudigd | [Geplande orders vereenvoudigd](../master-planning/planning-optimization/planned-orders-simplified.md ) | Functiebeheer:<br>*Geplande orders vereenvoudigd* |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven).

Als u een van deze functies wilt in- of uitschakelen, moet u dat doen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Voorraad- en magazijnbeheer | (Polen) Toestaan dat meerdere SAD-facturen aan één inkooporderregel in één SAD worden gekoppeld | Met deze functie kunt u inkooporderregels splitsen en deze koppelen aan één beheerdocument (SAD/Single Administrative Document) wanneer die inkooporderregels voor verschillende facturen zijn geboekt (bijvoorbeeld voor verschillende zendingen). |
| Inkoopbeheer | Meerdere opdrachten tot inkoop samenvoegen in één inkooporder op boekingsdatum | Met deze functie kunnen meerdere opdrachten tot inkoop worden geconsolideerd in één inkooporder als de verschillende opdrachten tot inkoop verschillende boekingsdatums hebben. Aanschafbeleidsregels voor het maken van inkooporders en consolidatie van vraag kunnen worden ingesteld om de beslissing voor het groeperen van regels voor opdrachten tot inkoop per boekingsdatum op inkooporderniveau te automatiseren. Consolidatie van inkooporders per boekingsdatum wordt niet ondersteund als budgetbeheer is ingeschakeld, omdat de boekingsdatum wordt gebruikt voor budgetreserveringen en vorderingen. Daarom moet deze tijdens de overgang van opdracht tot inkoop naar inkooporder worden behouden. |
| Inkoopbeheer | Knop Distributie van opdracht tot inkoop opnieuw instellen uitschakelen | Met deze functie wordt de knop **Opnieuw instellen** op de pagina **Boekhoudingsverdeling** uitgeschakeld voor regels van opdrachten tot inkoop die worden beoordeeld. |
| Inkoopbeheer | Oude standaard veldinstellingen voor reactie op offerteaanvraag weergeven | Met deze functie worden de oude, eerder uit de gebruikersinterface verwijderde standaardinstellingen voor antwoordvelden van offerteaanvragen opnieuw geïntroduceerd. Deze instellingen bieden geen standaardfunctionaliteit, maar dit kunt u aanpassen. Schakel deze functie in als uw organisatie al functionaliteit heeft toegevoegd voor de standaardinstellingen van antwoordvelden voor offerteaanvragen, of dit van plan is. Als deze functie is ingeschakeld, kunt u de instellingen openen door naar de pagina **Parameters inkoop en sourcing** te gaan, het tabblad **Offerteaanvraag** te openen en **Standaard antwoordvelden voor offerteaanvragen** te selecteren. |
| Inkoopbeheer | Financiële dimensies van de leverancier samenvoegen met financiële dimensies van actieve dimensiekoppeling op de inkooporder | Met deze functie kunt u financiële dimensies van leveranciers samenvoegen met financiële dimensies van actieve dimensiekoppelingen na goedkeuring van opdrachten tot inkoop als u een koppeling instelt tussen een financiële dimensie en de locatievoorraaddimensie. Aanschafbeleidsregels voor het maken van inkooporders en consolidatie van vraag kunnen zo worden ingesteld dat de beslissing voor het samenvoegen van financiële dimensies van leveranciers met een financiële dimensie voor actieve dimensiekoppeling op koptekstniveau van inkooporders wordt aangestuurd. |
| Productiebeheer | (Rusland) Standaardlocatie-instellingen voor productieformule/stuklijst en automatisch GTD-reservering/verbruik in productie inschakelen | Met de functie worden extra opties voor productie uit geïmporteerde grondstoffen ingeschakeld (alleen lokalisatie voor Rusland):<ul><li>De optie voor het instellen van de automatische standaardlocatie voor productieformules en stuklijsten voor zowel resourcegroepen als magazijnen.</li><li>Automatische reservering van grondstoffen door de dimensie *GTD-nummer* bij magazijnen die door WMS zijn geactiveerd volgens het algoritme voor niet-WMS-reserveringen. Dit is van toepassing wanneer er een werkbeleid voor *Orderverzameling van grondstoffen* bestaat waarbij **Werkaanmaakmethode** is ingesteld op *Nooit* en de instelling van het magazijn, de locatie en het artikelnummer overeenkomt met de voorraadtransacties van de productieorder (batch).</li><li>Automatisch verbruik van grondstoffen per *GTD-nummer*-dimensie bij het boeken van de orderverzamellijst op basis van de eerder beschreven verkregen reservering.</li></ul> |
| Magazijnbeheer | Verwachte ontvangsten van kwaliteitsorders uitschakelen die een voorbeeld van geblokkeerde voorraad bieden | Hiermee voorkomt u dat er verwachte ontvangsttransacties worden gemaakt voor kwaliteitsorders die een voorbeeld bieden van voorraad met een blokkeringsstatus. Omdat de geblokkeerde voorraad niet beschikbaar is, worden de verwachte ontvangsten met deze functie verwijderd. Hiermee wordt ervoor gezorgd dat voorraad niet opgescheept zit met meerdere blokkeringsstatussen, wat kan leiden tot problemen met gegevensintegriteit. |
| Magazijnbeheer | (Preview) Ondersteuning van schaaleenheden voor binnenkomende en uitgaande magazijnorders | Deze functie zorgt ervoor dat uitgaande magazijnorders tijdens het proces van vrijgave aan magazijn worden gemaakt en dat inkomende magazijnorders worden gemaakt wanneer transferorders worden geboekt als verzonden. Vervolgens wordt elke inkomende of uitgaande magazijnorder gesynchroniseerd met de schaaleenheid die verantwoordelijk is voor de verzending of ontvangst van de order. Houd er rekening mee dat wanneer u deze functie hebt ingeschakeld, een upgrade moet worden uitgevoerd op de workloads voor magazijnuitvoering. Zie [Workloads voor magazijnbeheer voor cloud- en edgeschaaleenheden](../cloud-edge/cloud-edge-workload-warehousing.md) voor meer informatie.<br><br>Voor deze functie is de functie *Wegzetwerk loskoppelen van ASN's* nodig en met deze functie is het mogelijk om transferorders te ontvangen met behulp van het proces voor het ontvangen van nummerplaten in de mobiele app Warehouse Management. |

## <a name="feature-state-changes-in-this-release"></a>Wijzigingen in status van functie in deze versie

In de volgende tabel worden functies weergegeven die verplicht zijn geworden of standaard zijn ingeschakeld vanaf versie 10.0.25. Al deze functies worden automatisch voor uw systeem ingeschakeld zodra u een update uitvoert naar 10.0.25. Verplichte functies kunnen niet worden uitgeschakeld, maar functies die standaard zijn ingeschakeld, kunnen wel worden uitgeschakeld via [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

De tabel bevat ook functies die eerder in openbare preview waren, maar zijn gewijzigd om algemeen beschikbaar te worden in 10.0.25. Dit betekent dat deze functies nu worden aanbevolen voor gebruik in productieomgevingen. Deze functies zijn standaard uitgeschakeld, tenzij anders is aangegeven. U moet [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) dus gebruiken om deze functies in te schakelen als u ze wilt gebruiken.

| Module | Functienaam | Functiestatus |
| --- | --- | --- |
| Activabeheer | Regels toepassen voor het groeperen van werkorders tijdens het uitvoeren van een onderhoudsplan | Algemeen beschikbaar |
| Activabeheer | Verbeteringen voor op teller gebaseerd onderhoud | Algemeen beschikbaar |
| Kostenbeheer | Berekeningsniveau voor kosten | Algemeen beschikbaar |
| Kostenbeheer | Door gebruiker gedefinieerde batchnummerinstellingen inschakelen voor omkeren van voorraadsluiting | Algemeen beschikbaar |
| Kostenbeheer | Voortgangsdetails van voorraadsluiting | Algemeen beschikbaar |
| Kostenbeheer | Opties voor standaardinstellingen voor financiële dimensies voor herwaardering van standaardkosten van voorraad | Algemeen beschikbaar |
| Kostenbeheer | Voorraadwaardenrapport gegevens opschonen | Standaard ingeschakeld |
| Kostenbeheer | Opslag voorraadwaardenrapport | Standaard ingeschakeld |
| Kostenbeheer | Logboek voor voorraadafsluiting in raster weergeven | Standaard ingeschakeld |
| Beheer voor technische wijzigingen | Wijzigingsbeheer voor bestaande producten inschakelen | Standaard ingeschakeld |
| Beheer voor technische wijzigingen | Beheer voor technische wijzigingen | Standaard ingeschakeld |
| Beheer voor technische wijzigingen | Technische meldingen voor productie | Standaard ingeschakeld |
| Beheer voor technische wijzigingen | Verbeterde overname van kenmerken voor Beheer voor technische wijzigingen | Standaard ingeschakeld |
| Beheer voor technische wijzigingen | Wijzigingen in formules en hun ingrediënten beheren | Standaard ingeschakeld |
| Beheer voor technische wijzigingen | Controles op productgereedheid | Standaard ingeschakeld |
| Beheer voor technische wijzigingen | Varianten genereren voor technische producten | Standaard ingeschakeld |
| Voorraad- en magazijnbeheer | Navigatie naar stuklijstversie vanuit stuklijstregels | Verplicht |
| Hoofdplanning | Batchgewijs fiatteren en consolideren voor geplande batchorders voor bulk en verpakking | Algemeen beschikbaar |
| Hoofdplanning | Resourceplanning met onderhoud | Algemeen beschikbaar |
| Hoofdplanning | Wizardfuncties voor het instellen van een hoofdplan inschakelen | Verplicht |
| Hoofdplanning | Selectie prognosemodel in Details vraagprognose | Verplicht |
| Hoofdplanning | Voortgangsvisualisatie hoofdplanning | Verplicht |
| Hoofdplanning | Parallelle fiattering van geplande orders | Verplicht |
| Hoofdplanning | Geplande orders fiatteren met filters | Standaard ingeschakeld |
| Hoofdplanning | Opgeslagen weergaven voor geplande orders | Standaard ingeschakeld |
| Inkoopbeheer | Knop Distributie van opdracht tot inkoop opnieuw instellen uitschakelen | Algemeen beschikbaar |
| Inkoopbeheer | Het opnieuw instellen van inkoopgerelateerde werkstromen inschakelen | Algemeen beschikbaar |
| Inkoopbeheer | Mogelijkheid om geaccepteerde inkooporders van leverancierssamenwerking in batch te bevestigen | Verplicht |
| Inkoopbeheer | Status Afgesloten van inkoopovereenkomst | Verplicht |
| Inkoopbeheer | Regels toevoegen aan IO-facturen die zijn gekoppeld aan een inkoopovereenkomst | Standaard ingeschakeld |
| Inkoopbeheer | Veld Bestelde hoeveelheid toevoegen aan de pagina Productontvangst boeken | Standaard ingeschakeld |
| Inkoopbeheer | Leveranciers toestaan zich aan te melden voor inkoopcategorieën via leverancierssamenwerking | Standaard ingeschakeld |
| Inkoopbeheer | Toeslagen Van- en Tot-bedragen op inkooporders | Standaard ingeschakeld |
| Inkoopbeheer | Toeslagen instellen met vestiging en magazijn | Standaard ingeschakeld |
| Inkoopbeheer | Berekening van inkoopheffing op basis van jaarlijks tarief inschakelen | Standaard ingeschakeld |
| Inkoopbeheer | Verantwoordelijke partij voor inkoopovereenkomst | Standaard ingeschakeld |
| Inkoopbeheer | Opgeslagen weergaven voor inkooporders | Standaard ingeschakeld |
| Productgegevensbeheer | Strikte validatie van standaardorderhoeveelheden | Verplicht |
| Productgegevensbeheer | Voorverwerking van stuklijstrapport om time-out te voorkomen | Standaard ingeschakeld |
| Productgegevensbeheer | Financiële dimensies standaard afzonderlijk bij gebruik van artikelsjablonen | Standaard ingeschakeld |
| Productgegevensbeheer | Productdimensiegroepen inschakelen voor artikelsjablonen | Standaard ingeschakeld |
| Productgegevensbeheer | Productvariantnamen opnieuw genereren op basis van nomenclatuur | Standaard ingeschakeld |
| Productgegevensbeheer | Verbeteringen voor pagina met variantsuggesties | Standaard ingeschakeld |
| Productiebeheer | Verbeterd verzamelen van catch weight-hoeveelheid voor productie | Algemeen beschikbaar |
| Productiebeheer | De nieuwe knop Pauze stoppen is toegevoegd aan de pagina Taakkaartterminal | Verplicht |
| Productiebeheer | Het automatisch genereren van nummerplaatnummers inschakelen bij het gereedmelden in het apparaat voor taakkaarten | Verplicht |
| Productiebeheer | Gedeeltelijke ontvangst van uitbestede artikelen inschakelen en een probleem met de berekening van uitval voor stuklijstregels van het type Leverancier oplossen | Verplicht |
| Productiebeheer | Functie voor vergrendelen van taakkaartapparaat en taakkaartterminal zodat ze kunnen worden schoongemaakt | Verplicht |
| Productiebeheer | Verbeteringen in de dialoogvensters Taken goedkeuren en Taken overboeken | Verplicht |
| Productiebeheer | Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten | Verplicht |
| Productiebeheer | Label afdrukken vanaf apparaat voor taakkaart | Verplicht |
| Productiebeheer | Uitvoering werkvloer | Verplicht |
| Productiebeheer | Functionaliteit van activabeheer voor de uitvoeringsinterface voor de werkvloer | Standaard ingeschakeld |
| Productiebeheer | Taak zoeken voor de uitvoeringsinterface voor de werkvloer | Standaard ingeschakeld |
| Productiebeheer | Standaardproductiereservering overschrijven | Standaard ingeschakeld |
| Productiebeheer | Volledige serie-, batch- en nummerplaatnummers tonen in de uitvoeringsinterface van de productievloer | Standaard ingeschakeld |
| Verkoopbeheer en marketing | Verbetering van prestaties verkooporderdetails | Algemeen beschikbaar |
| Verkoopbeheer en marketing | Verbetering van prestaties verkoopoffertedetails | Algemeen beschikbaar |
| Verkoopbeheer en marketing | Verkooporder verwees naar gegevensexportbeleid | Verplicht |
| Verkoopbeheer en marketing | Verwijderingsbeleid voor verkooporder naar inkooporderregel | Verplicht |
| Verkoopbeheer en marketing | Verkoopofferte verwees naar gegevensexportbeleid | Verplicht |
| Verkoopbeheer en marketing | Optimalisatie van export van gegevensentiteit Contactpersoon | Standaard ingeschakeld |
| Verkoopbeheer en marketing | Zoeken voor de velden Documentinleiding en Documentconclusie van verkoopoffertes inschakelen | Standaard ingeschakeld |
| Verkoopbeheer en marketing | Prestaties van rapport 'Top 100 van klanten' verbeteren | Standaard ingeschakeld |
| Verkoopbeheer en marketing | Geraamd klantsaldo opnieuw berekenen | Standaard ingeschakeld |
| Verkoopbeheer en marketing | Registratie van verkoopretourregel met decimale precisie met en zonder catch weight | Standaard ingeschakeld |
| Verkoopbeheer en marketing | Opgeslagen weergaven voor verkoop en marketing | Standaard ingeschakeld |
| Verkoopbeheer en marketing | Verkooporderbevestiging met één klik | Standaard ingeschakeld |
| Magazijnbeheer | Sjablonen met locatie-instructies voor cross-docken | Algemeen beschikbaar |
| Magazijnbeheer | Verwachte ontvangsten van kwaliteitsorders uitschakelen die een voorbeeld van geblokkeerde voorraad bieden | Algemeen beschikbaar |
| Magazijnbeheer | Ontvangstgeschiedenis nummerplaat | Algemeen beschikbaar |
| Magazijnbeheer | Hoeveelheden afronden naar dichtstbijzijnde verkoopeenheid bij vrijgave aan magazijn | Algemeen beschikbaar |
| Magazijnbeheer | Ondersteuning van schaaleenheden voor werklijsten in magazijnapp | Algemeen beschikbaar |
| Magazijnbeheer | Details van zendingswavelabels | Algemeen beschikbaar |
| Magazijnbeheer | Snellere API gebruiken voor het sluiten/heropenen van containers op inpakstation | Algemeen beschikbaar |
| Magazijnbeheer | Sjablonen valideren die zijn geselecteerd voor aanvullingstaken | Algemeen beschikbaar |
| Magazijnbeheer | Aanvullingssjabloon toestaan om bestaand direct aanvullingswerk te gebruiken (tussen eenheden) | Verplicht |
| Magazijnbeheer | Automatisch toewijzen van de GUID's bij het maken van WHS-gebruikers | Verplicht |
| Magazijnbeheer | Productvarianten en traceringsdimensies vastleggen in de magazijnbeheer-app tijdens het ontvangen van ladingsartikel | Verplicht |
| Magazijnbeheer | De voorraadstatus van artikelen wijzigen die worden beheerd door traceringsdimensies | Verplicht |
| Magazijnbeheer | Werkgroep voor werk wijzigen | Verplicht |
| Magazijnbeheer | Clusterpositie vol | Verplicht |
| Magazijnbeheer | Functie Cluster opslaan | Verplicht |
| Magazijnbeheer | Bevestigen en overboeken | Verplicht |
| Magazijnbeheer | Uitgaande zendingen vanuit batchtaken bevestigen | Verplicht |
| Magazijnbeheer | Bepalen of u een ontvangstoverzichtspagina wilt weergeven op mobiele apparaten | Verplicht |
| Magazijnbeheer | Uitgestelde verwerking van handmatige bewerking voor voorraadmutatie | Verplicht |
| Magazijnbeheer | Niet toestaan dat ladingen worden gemaakt die niet voldoen aan de sjabloonvereisten voor het maken van waveladingen | Verplicht |
| Magazijnbeheer | Verbeterde indelingen voor nummerplaatlabels | Verplicht |
| Magazijnbeheer | Alle acties voor locatie-instructies met meerdere SKU's evalueren | Verplicht |
| Magazijnbeheer | Het veld Totale waarde verbergen op de pagina's Alle ladingen en Ladingdata | Verplicht |
| Magazijnbeheer | Configuratie van nummerplaatlabel maken | Verplicht |
| Magazijnbeheer | Handmatige correctie van ladingsregel voor beheerder of vergelijkbare vertrouwde gebruikers | Verplicht |
| Magazijnbeheer | Positionering van locatie nummerplaat | Verplicht |
| Magazijnbeheer | Locaties voor productdimensie combineren | Verplicht |
| Magazijnbeheer | Het voorraadstatusveld van de voorraadverplaatsing van het mobiele apparaat bewerkbaar maken | Verplicht |
| Magazijnbeheer | Handmatige orderverzamelactiviteit van verkoopregels voor beheerder of soortgelijke vertrouwde gebruikers | Verplicht |
| Magazijnbeheer | Voorkomen dat verzonden nummerplaten van transferorders worden gebruikt in andere magazijnen dan het doelmagazijn | Verplicht |
| Magazijnbeheer | Vragen om niet-eenduidige Loc/LP-namen op te lossen | Verplicht |
| Magazijnbeheer | Kwaliteitscontrole | Verplicht |
| Magazijnbeheer | Gebruikersinstellingen, pictogrammen en stapnamen voor de nieuwe magazijnapp | Verplicht |
| Magazijnbeheer | Extra locatiezone | Standaard ingeschakeld |
| Magazijnbeheer | overboekingsorders maken en verwerken vanuit de magazijnapp | Standaard ingeschakeld |
| Magazijnbeheer | Snelle validatie voor mobiele magazijnapparaten inschakelen | Standaard ingeschakeld |
| Magazijnbeheer | Locatiegebruik artikelconsolidatie | Standaard ingeschakeld |
| Magazijnbeheer | Maximale uitvoeringstijd voor het opschonen van de vermeldingen van voorhanden voorraad voor magazijnbeheer | Standaard ingeschakeld |
| Magazijnbeheer | Visualisatie van uitgaande workload | Standaard ingeschakeld |
| Magazijnbeheer | Gebeurtenissen in magazijnapp verwerken | Standaard ingeschakeld |
| Magazijnbeheer | Opgeslagen weergave voor de workbench voor ladingplanning | Standaard ingeschakeld |
| Magazijnbeheer | Opgeslagen weergave voor de pagina Werkgegevens | Standaard ingeschakeld |
| Magazijnbeheer | Opgeslagen weergave voor de verwerking van waves | Standaard ingeschakeld |
| Magazijnbeheer | Opgeslagen weergaven voor de verwerking van ladingen | Standaard ingeschakeld |
| Magazijnbeheer | Opgeslagen weergaven voor verzendingsverwerking | Standaard ingeschakeld |
| Magazijnbeheer | Details van wavebatchtaken | Standaard ingeschakeld |
| Magazijnbeheer | Meldingen voor uitvoering van wave | Standaard ingeschakeld |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.25 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.25 van apps voor financiële en bedrijfsactiviteiten (april 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.25, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

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