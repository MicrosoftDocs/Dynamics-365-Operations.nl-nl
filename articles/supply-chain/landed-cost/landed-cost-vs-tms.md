---
title: Francoprijzen versus Transportbeheer
description: Microsoft Dynamics 365 Supply Chain Management biedt twee verschillende modules om met transport, Transportbeheer (TMS) en Francoprijzen te werken. In dit onderwerp wordt de functionaliteit samengevat die de twee modules gemeen hebben en komen de verschillen tussen de twee aan de orde.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ba745048d1d9f28300f03ed0bc98142d80aa5a26
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569812"
---
# <a name="landed-cost-vs-transportation-management"></a>Francoprijzen versus Transportbeheer

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management biedt twee verschillende modules om met transport, **Transportbeheer** (TMS) en **Francoprijzen** te werken. In dit onderwerp wordt de functionaliteit samengevat die de twee modules gemeen hebben en komen de verschillen tussen de twee aan de orde. U kunt deze informatie gebruiken om te bepalen welke module het beste bij uw bedrijf past. U vindt wellicht dat bepaalde zakelijke werkwijzen beter werken met TMS, terwijl andere het beste werken met Francoprijzen. U kunt er vervolgens voor kiezen om, afhankelijk van uw bedrijfsbehoeften, maar één module te gebruiken of om de twee modules te combineren.

In dit onderwerp wordt geen uitgebreid overzicht gegeven van alle functies van de beide modules. In plaats daarvan wordt de beschikbare functionaliteit benadrukt voor het transport van goederen van een leverancier naar het magazijn van uw bedrijf waar ze kunnen worden verbruikt.

## <a name="terminology-reference-data-and-reporting-differences"></a>Terminologie, referentiegegevens en rapportageverschillen

### <a name="terminology-comparison"></a>Vergelijking van terminologie

In TMS en Francoprijzen worden verschillende termen gebruikt voor vergelijkbare concepten. In de volgende tabel wordt een overzicht gegeven van deze termen en hun gebruik in de twee modules.

| Term in TMS | Term in Francoprijzen | Opmerkingen |
|----------|------------------|-------|
| **Inlezen**<p>Een *lading* is een verzameling zendingen die gelijktijdig worden getransporteerd in dezelfde transporteenheid (zoals een truck of een schip). Bij ladingen kan het om inkomende of uitgaande ladingen gaan.</p> | **Reis**<p>Meestal is een *reis* één vaartuig dat één *traject* aflegt. Een reis kan meerdere *containers* bevatten en kan ook inkomende orders van verschillende rechtspersonen van uw organisatie bevatten. Reizen kunnen alleen inkomend zijn.</p> | In TMS wordt de term *reisnummer* gebruikt dat verwijst naar een informatieveld waarin u een id kunt invoeren. Er is echter geen functionaliteit aan het TMS-veld gekoppeld en het is niet gerelateerd aan het concept *reis* in Francoprijzen. |
| **Route**<p>Een *route* is het fysieke pad van een transport van herkomst naar bestemming.</p> | **Traject**<p>Een *traject* is het fysieke pad van een transport van vertrek naar bestemming. Elke reis moet aan een traject worden toegewezen.</p> | |
| **Routesegmenten**<p>Een route kan meerdere *routesegmenten* hebben. Deze segmenten staan voor één stap van het traject. Een route kan meerdere vervoerders of services bevatten, die elk als een routesegment worden beschouwd.</p> | **Etappes**<p>Elk traject kan meerdere *etappes* hebben die elk één stap van het traject vertegenwoordigen. Een etappe kan deel uitmaken van transport, verwerking van heffingen of een andere activiteit.</p> | |
| **Containers**<p>Een *container* kan elk type pakket of verpakking zijn dat door TMS wordt gebruikt.</p> | **containers**<p>Een *container* is een letterlijke fysieke container zoals van containerschepen.</p> | |
| **Basisproductcodes**<p>In TMS (en op andere plaatsen in Supply Chain Management) geven *basisproductcodes* typen basisproducten aan. Deze kunnen van invloed zijn op tarieven, de verwerking van gevaarlijke stoffen enzovoort.</p> | **Basisproductcodes**<p>In Francoprijzen worden *basisproductcodes* vastgesteld op het niveau van de rechtspersoon. Deze worden meestal voor rapportagedoeleinden gebruikt.</p> | Bij Francoprijzen kunnen ook de basisproductcodes worden gebruikt die voor TMS en op andere plaatsen in Supply Chain Management worden gebruikt. De basisproductcodes van Francoprijzen worden echter alleen gebruikt voor Francoprijzen. |

### <a name="some-reference-data-isnt-shared"></a>Sommige verwijzingsgegevens worden niet gedeeld

In TMS en Francoprijzen worden geen verwijzingsgegevens gedeeld voor entiteiten zoals kosteninstellingen, trajecten en etappes. Als u beide modules gebruikt, moet u verwijzingsgegevens die niet worden gedeeld, opnieuw maken.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>In intercompany-rapporten wordt niet met goederen in transit gewerkt

In de volgende rapporten wordt niet samengewerkt met de functie goederen in transit die Francoprijzen biedt:

- [Rapport van totalen voor intercompany-goederen in transit](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Rapport van totalen voor intercompany-goederen in transit](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

In deze rapporten wordt ervan uitgenomen dat goederen worden overgebracht zodra u een verkooppakbon uitgeeft en dat ze bij ontvangst in de voorraad worden opgenomen. Goederen in transit worden echter niet op deze manier verwerkt. Als u de goederen in transit en intercompany-functies tezamen gebruikt, zijn de resultaten voor beide rapporten daarom onjuist.

## <a name="using-the-two-modules-together"></a>De twee modules samen gebruiken

U kunt TMS gebruiken voor zowel inkomende als uitgaande bewerkingen. Hoewel Francoprijzen voor inkomende bewerkingen grotendeels dezelfde basisfunctionaliteit biedt als TMS, bevat Francoprijzen een paar extra functies. U kunt daarom overwegen om TMS gebruiken voor uitgaande bewerkingen en Francoprijzen voor inkomende bewerkingen.

Over het algemeen raden we niet aan om beide modules samen te gebruiken voor inkomende bewerkingen. U moet de module gebruiken die het beste aan uw vereisten voldoet. Als u de twee modules wel samen gebruikt, moet u geen brondocumenten tussen de twee modules delen. Gebruik bijvoorbeeld niet dezelfde inkooporder voor zowel een lading in TMS als voor een traject in Francoprijzen. U moet er vooral voor zorgen dat u het systeem niet zo instelt dat er automatisch inkomende ladingen worden gemaakt. Als artikelen van inkooporders in een traject worden opgenomen, kunnen ze niet worden verwerkt als onderdeel van een lading.

## <a name="goods-in-transit"></a>Goederen in transit

Een van de primaire functies van Francoprijzen is de mogelijkheid om goederen in transit te verwerken. Met verwerking van goederen in transit kunt u de financiële verantwoordelijkheid nemen van verzonden artikelen voordat deze fysiek worden ontvangen in het doelmagazijn. Verwerking van goederen in transit is vaak vereist voor internationale handel.

### <a name="tms-goods-in-transit-features"></a>TMS-functies voor goederen in transit

TMS ondersteunt momenteel niet de verwerking van goederen in transit.

### <a name="landed-cost-goods-in-transit-features"></a>Functies in Francoprijzen voor goederen in transit

Het verwerken goederen in transit is een primaire functie van Francoprijzen en biedt de volgende functionaliteit:

- **Magazijnen voor goederen in transit**: Aan elk magazijn in Supply Chain Management kan een magazijn voor goederen in transit worden gekoppeld. Goederen worden overgebracht naar transitmagazijnen nadat de oorspronkelijke inkooporder is gefactureerd. Artikelen die fysiek in het magazijn zijn gereserveerd, zijn pas beschikbaar voor verbruik wanneer ze in hun fysieke magazijn zijn ontvangen. U kunt daarom het financiële eigendom van goederen overnemen door de inkooporder te factureren.
- **Grootboekrekening voor goederen in transit**: Bij Francoprijzen wordt een specifieke grootboekrekening voor boekingen toegevoegd aan het boekingsprofiel van de inkooporder om goederen in transit te verwerken. Deze grootboekrekening voor goederen in transit fungeert als rekening van het type 'goederen die zijn gefactureerd maar niet zijn ontvangen'. Wanneer de oorspronkelijke inkooporder wordt gefactureerd en de order voor de goederen in transit wordt gemaakt, worden de kosten van de directe inkooporder geboekt op de grootboekrekening voor goederen in transit totdat de goederen op de uiteindelijke fysieke locatie zijn ontvangen.
- **Updates voor traceringsbeheer**: Orders voor goederen in transit ondersteunen de functie voor traceringsbeheer in Francoprijzen. Met traceringsbeheer kunt u de verwachte datum van de ontvangst van goederen bijwerken terwijl ze in transit zijn. Met traceringsbeheer worden vervolgens het traject en de gekoppelde inkooporderregels bijgewerkt. De verwachte leveringsdatum is vervolgens beschikbaar voor hoofdplanning en logistiek.
- **Activeren van transacties voor meer- en minderleveringen**: Als er een afwijking optreedt tussen de verwachte goederen op een reisregel en de werkelijke goederen die in het magazijn worden ontvangen, wordt dit met Francoprijzen opgelost door transacties voor meer- en minderleveringen te maken. U kunt deze transacties vervolgens beheren op basis van de manier waarop u ze wilt verwerken: via een inkooporder of via een mutatiejournaal. De transacties voor meer- en minderleveringen bieden een koppeling waarmee u weer teruggaat naar de oorspronkelijke inkooporder en het nieuwe mutatiejournaal of de nieuwe inkooporder voor het verschil.
- **Orders voor goederen in transit**: Met Francoprijzen wordt een nieuw brondocument geïntroduceerd met de naam *order voor goederen in transit*. Met een order voor goederen in transit kunt u de oorspronkelijke inkooporder factureren om financieel eigenaar te worden van de artikelen. Wanneer de inkooporder wordt gefactureerd, wordt het nieuwe brondocument gemaakt voor elke inkooporderregel met een combinatie van voorraaddimensies. Goederen worden vervolgens fysiek verplaatst naar een transitmagazijn, waar ze fysiek zijn gereserveerd voor de order voor goederen in transit en niet kunnen worden verbruikt tenzij er orders voor goederen in transit worden ontvangen.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Diverse toeslagen en verzendkosten

Een van de belangrijkste aspecten van verzending en verzendingsbeheer voor goederen is de herkenning van de overheadkosten die aan zendingen zijn gekoppeld. Deze overheadkosten zijn niet de directe voorraadkosten die aan een inkooporder en een zending of traject zijn gekoppeld. Dit zijn extra kosten die worden geïntroduceerd door de aard van de verplaatsing van de goederen van de leverancier naar uw organisatie. Deze kosten kunnen vrachtkosten zijn die zijn gekoppeld aan de verzending van goederen van de ene fysieke locatie naar de andere, of de invoerkosten van goederen van een buitenlandse leverancier.

Met Francoprijzen worden deze kosten verwerkt door een nieuw type kostenstructuur te maken dat *automatische kosten* wordt genoemd. TMS verwerkt deze kosten door de functionaliteit voor diverse toeslagen te gebruiken.

### <a name="tms-charge-and-cost-features"></a>Toeslagen- en kostenfuncties van TMS

In TMS worden diverse toeslagen gebruikt om extra kosten te beheren voor belastingen die zijn toegewezen aan de gerelateerde brondocumentregels. Deze diverse toeslagen kunnen worden ingesteld op het niveau van de inkooporderregel of de header van de inkooporder.

In TMS kunnen diverse toeslagen worden verdeeld of gedeeld door het gewicht, het volume of de hoeveelheid van de voorraad. Toeslagen kunnen worden gedeeld door vracht- of bijkomende toeslagen. Er is verdere ontwikkeling vereist als u extra verdelingsmethoden in TMS wilt gebruiken.

### <a name="landed-cost-charge-and-cost-features"></a>Toeslag van francoprijzen en kostenfuncties

Francoprijzen biedt een set kostenfuncties waarmee extra kosten worden verwerkt die aan de verzending van goederen zijn gekoppeld. Deze kosten worden ook wel automatische kosten genoemd en worden toegepast op het moment van de eerste facturering van de verzending aan de hand van het geschatte kostenbedrag. Elk kostentype wordt beheerd in de bijbehorende boeking. Nadat de werkelijke facturen voor overheadkosten zijn geboekt, worden de geschatte kosten automatisch bijgewerkt met de werkelijke kosten.

Bovendien kunnen de overheadkosten die aan de verzending van goederen zijn gekoppeld, worden gefactureerd tijdens de reis van de haven van herkomst of op elk moment nadat de goederen zijn ontvangen. Deze mogelijkheid biedt meer flexibiliteit voor het verbruik van goederen.

In de volgende lijst komen een paar concepten voor de toeslag- en kostenfuncties in Francoprijzen aan de order:

- **Kostengebied**: kosten en toeslagen kunnen aan verschillende niveaus, of *kostengebieden* worden gekoppeld. De kosten kunnen worden toegepast op het niveau van het traject en worden opgesplitst voor elk artikel in het traject. Verder kunnen kosten worden toegepast op het niveau van de container, inkooporder, artikel of overboekingsorder. Elke kostenpost kan in de diverse gebieden afzonderlijk worden beheerd en wordt opgesplitst in kosten per artikel.
- **Verdelingsmethode**: Er zijn verschillende verdelingsmethoden beschikbaar in Francoprijzen. Toeslagen op kosten kunnen worden verdeeld per hoeveelheid, bedrag in dollars, waarde, gewicht, volume, afmeting of een door de gebruiker gedefinieerde volumemaat.
- **Vereffenings-/verschillenbeheer**: toeslagen op kosten worden ingesteld als hun eigen kostencodetype in Francoprijzen. Met elk kostencodetype kunt u een vereffeningsrekening definiëren voor geschatte kosten, en ook rekeningen voor toerekeningen en inkoopprijsverschillen voor afwijkingen in geschatte kosten versus werkelijke kosten. Wanneer de geschatte kosten in eerste instantie worden geboekt, wordt er een creditnota naar de vereffeningsrekening geboekt. Nadat de werkelijke facturen zijn geboekt, worden de werkelijke kosten op toeslagen geboekt en worden de geschatte kosten gedebiteerd van de vereffeningsrekening.

## <a name="matching-freight-bills-and-invoices"></a>Vrachtfacturen en facturen vereffenen

### <a name="tms-bill-and-invoice-matching-features"></a>Functies voor het vereffenen van wissels en facturen in TMS

In TMS kunnen vrachtfacturen met geschatte kosten en facturen met de werkelijke kosten van de vracht vereffenen. Facturen kunnen elektronisch of op papier worden ontvangen. Het vereffenen van verschillen tussen de geschatte kosten en de werkelijke kosten is niet van invloed op de voorraadwaardering.

Zie [Vracht afstemmen in transportbeheer](../transportation/reconcile-freight-transportation-management.md) voor meer informatie.

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Functies voor het vereffenen van wissels en facturen in Francoprijzen

In Francoprijzen kunnen vrachtfacturen worden vereffend met de geschatte kosten en kunnen de werkelijke kosten worden gefactureerd aan de geschatte kosten. Op het moment van factureren worden de vrachtkosten in een factuurjournaal vermeld en worden de geschatte kosten uit de vereffeningsrekening gehaald. Daarnaast worden de werkelijke kosten geboekt tegen de kosten van de verkochte goederen voor het artikel, samen met de verschillen tussen de geschatte toeslagen en de werkelijke toeslagen. Dit gedrag zorgt voor flexibiliteit in het factureringsproces.

## <a name="tracking"></a>Tracering

Een belangrijke functie van zowel TMS als Francoprijzen is de mogelijkheid om goederen te volgen en te bepalen waar ze zich in het traject bevinden van het punt van vertrek tot het uiteindelijke doelmagazijn. Met tracering kunt u volgen en bijwerken waar de goederen zich bevinden en wanneer voor verbruik ze worden verwacht in het magazijn. Naast de status van goederen tijdens hun traject, biedt Francoprijzen verwachte en werkelijke datums voor elke stap van het traject.

### <a name="tms-tracking-features"></a>Traceringsfuncties van TMS

TMS biedt een beperkt aantal functies voor het traceren van inkomende ladingen. Met deze functies worden datums weergegeven en integratie mogelijk gemaakt om de exacte positie te vinden (bijvoorbeeld op de pagina **Transportstatus**).

Voor elk routesegment kunt u geschatte schema's en aankomsttijden invoeren.

### <a name="landed-cost-tracking-features"></a>Traceringsfuncties voor Francoprijzen

Francoprijzen kunnen traceringsbeheer bieden voor elke reis, van de haven van herkomst tot aan de eindbestemming. Met traceringsbeheer wordt de status van de reis bepaalt. De status geeft aan of de reis per schip onderweg is, bij de douane is of via lokale levering op weg is naar het definitieve magazijn. De status kan worden ingesteld op het niveau van de inkooporderregel, de container en de header van de reis. U hebt daarom meer gedetailleerde controle.

Bovendien is aan elke stap van een traject een bevestigde, verwachte datum gekoppeld die is gebaseerd op opgegeven doorlooptijden. De bevestigde en verwachte leveringsdatums worden toegevoegd aan de inkooporderregel en aan orders voor goederen en kunnen worden gebruikt voor hoofdplanning en logistiek. Behalve de verwachte datums kunnen ook de werkelijke datums worden bijgewerkt. De volgende stappen in een traject worden nu dienovereenkomstig bijgewerkt.

## <a name="multi-leg-journeys"></a>Trajecten met meerdere etappes

Het concept van een traject geeft aan waar de goederen zich in het proces bevinden en bepaalt de status van de goederen terwijl ze in transit zijn. Goederen kunnen verschillende etappes van een traject doorlopen en u kunt diverse kosten aan een specifieke etappe koppelen. Voorbeelden hiervan zijn vrachtkosten voor vervoer per vaartuig en lokale transportkosten bij het transport van goederen van de haven naar de bestemming.

### <a name="tms-multi-leg-journey-features"></a>TMS-functies voor trajecten met meerdere etappes

In TMS kunnen routes in routesegmenten worden opgesplitst om trajecten met meerdere etappes aan te geven. Met TMS kunnen spottarieven en bijkomende toeslagen aan afzonderlijke routesegmenten worden toegewezen.

Zie [Vrachttransportroutes met meerdere tussenstops plannen](../transportation/plan-freight-transportation-routes-multiple-stops.md) voor meer informatie.

### <a name="landed-cost-multi-leg-journey-features"></a>Functies in Francoprijzen voor trajecten met meerdere etappes

Francoprijzen biedt een raamwerk voor het verplaatsen van goederen van het punt van vertrek naar de bestemming via een reeks etappes. Dit zijn de tussenstops of stappen in een traject. De etappes worden gecombineerd om trajectsjablonen te maken waarin is gedefinieerd hoe goederen worden verplaats van de leverancier naar uw organisatie.

In elke etappe van een traject kunt u de status van elke inkooporderregel en de bijbehorende doorlooptijden verder definiëren. De gecombineerde doorlooptijd voor alle etappes wordt gebruikt om de geschatte leveringsdatum aan te geven. Voor de toepassing van trajecten met meerdere etappes is echter verwerking van goederen in transit vereist. Het traject van goederen van een reis wordt beheerd in een tabel die specifiek is voor Francoprijzen.

## <a name="receiving-by-container"></a>Ontvangen per container

Het kan belangrijk zijn om te beheren hoe goederen worden opgesplitst en opgeslagen op een vaartuig. Op een vaartuig kunnen goederen worden opgeslagen in één container of in meerdere containers. Wanneer goederen worden ontvangen, worden deze in containers ontvangen. Het kan zijn dat verschillende containers op een reis worden ontvangen op verschillende tijden of op verschillende datums.

Zowel TMS als Francoprijzen bieden functionaliteit voor het beheren van de ontvangst van goederen in een container. TMS gebruikt het concept van ladingen om de goederen, inkooporders en overboekingsorders te beheren die aan een container zijn gekoppeld. TMS ondersteunt de ontvangst op basis van een verpakking die wordt ontvangen via een advance shipping notice (ASN). Francoprijzen gebruikt het concept van containers om inkooporders te verwerken en overheadkosten te beheren die aan een container op een schip zijn gekoppeld.

### <a name="tms-receiving-by-container-features"></a>TMS-functies voor het ontvangen per container

TMS ondersteunt inkomende ASN's, alle ontvangstvarianten via de mobiele app Magazijnbeheer en alle ontvangstmethoden via de Supply Chain Management-client.

### <a name="landed-cost-receiving-by-container-features"></a>Functies in Francoprijzen voor het ontvangen per container

Ter ondersteuning van het ontvangen per container worden met Francoprijzen containerrecords gemaakt en inkooporders gekoppeld met een specifieke container met behulp van de bijbehorende container-id. Overheadkosten kunnen vervolgens op die container worden toegepast en worden opgesplitst, zodat ze aan de relevante inkooporders worden gekoppeld.

Containers in Francoprijzen kunnen worden ontvangen via een nieuw type ontvangst, dat ook wel *ontvangst van goederen in transit* wordt genoemd, of via ontvangst via mobiele apparaten. Wanneer er ontvangstjournalen worden gebruikt, kunnen de hoeveelheden worden geïnitialiseerd vanuit de order voor goederen in transit of de oorspronkelijke inkooporderregels in de container. Francoprijzen biedt twee werktypen voor de ontvangst via de mobiele app Magazijnbeheer.

Francoprijzen verstrekt geen ASN voor de elektronische ontvangst van goederen. Daarnaast worden stromen van de mobiele app Magazijnbeheer waarmee de ontvangst van ladingen, nummerplaten en gemengde nummerplaten worden verwerkt, niet ondersteund.

## <a name="rate-shopping-by-vendor"></a>Tarieven zoeken per leverancier

Met Tarieven zoeken kan een bedrijf een expeditiebedrijf selecteren op basis van de laagste prijs, snelste route of een combinatie van beide.

### <a name="tms-rate-shopping-features"></a>TMS-functies voor tarieven zoeken

Met TMS kunt u leveranciers- en routeoplossingen voor inkomende en uitgaande orders identificeren. Bijvoorbeeld, kunt u de snelste route of het minste dure tarief voor een zending identificeren.

TMS biedt alle mogelijkheden voor tarieven zoeken en optimalisatie van vracht via de workbench voor de tariefroute, flexibele opties voor het beoordelen van tarieven, een API voor een beoordelingsengine voor integratie met externe partijen en ondersteuning voor volumetrisch gewicht.

Zie [Engines voor transportbeheer](../transportation/transportation-management-engines.md) voor meer informatie.

### <a name="landed-cost-rate-shopping-features"></a>Functies in Francoprijzen voor tarieven zoeken

Francoprijzen biedt slechts beperkte ondersteuning voor tarieven zoeken per leverancier. Hoewel u waarden voor expediteurs kunt invoeren, worden deze waarden in Francoprijzen niet met waarden van meerdere leveranciers vergeleken.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Inchecken/uitchecken van chauffeur met afspraakplanning

De functies voor het in- en uitchecken van de chauffeur zorgen ervoor dat het systeem ontvangsten kan controleren en congestie bij het laaddok kan voorkomen.

### <a name="tms-driver-check-incheck-out-features"></a>TMS-functies voor in- en uitchecken van chauffeur

Met TMS kunt u *afspraken* maken.. Een afspraak vertegenwoordigt gebeurtenissen die plaatsvinden bij een dok voor het ontvangen van een inkooporder, het verzenden van een inkooporder of de verwerking van een binnenkomend of uitgaande ladingen op een specifieke tijd. Afspraken zorgen ervoor dat doks beschikbaar zijn voor het laden en lossen van goederen en zorgen ervoor dat er niet meerdere vervoerders tegelijkertijd op een locatie aankomen.

Het systeem kan chauffeurs toegestaan om in te checken bij een specifieke dokdeur.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Functies in Francoprijzen voor in- en uitchecken van chauffeur

In Francoprijzen kunnen ramingen worden opgeslagen voor de datum en tijd waarop een container wordt geleverd.

## <a name="transfer-orders-and-additional-costs"></a>overboekingsorders en extra kosten

Vaak moeten bedrijven goederen kunnen overbrengen tussen magazijnen. Wanneer dit type overdracht plaatsvindt, worden er kosten aan gekoppeld die u wilt herkennen. In Francoprijzen kunnen overboekingsorders worden toegevoegd aan een reis of vaartuig om de verplaatsing van goederen te volgen van het ene magazijn naar het andere, de levertijd en de verwachte leveringsdatum te schatten en overheadkosten aan de overdracht van goederen toe te voegen.

### <a name="tms-transfer-order-cost-features"></a>Functies in Francoprijzen voor kosten van overboekingsorders

In TMS kunt u vrachtkosten maken die zijn gekoppeld aan overdrachten. Hoewel deze toeslagen kunnen worden bekeken vanuit de overboekingsorder, worden de francoprijzen niet toegevoegd aan de artikelkosten. Vrachtafstemming wordt ondersteund door een vrachtfactuur te maken die is gebaseerd op deze toeslagen. Deze vrachtfactuur wordt vervolgens vereffend met een vrachtfactuur van een leverancier.

### <a name="landed-cost-transfer-order-cost-features"></a>Functies in Francoprijzen voor kosten van overboekingsorders

Met Francoprijzen kunt u overboekingsorders toevoegen aan een vaartuig of reis. Op deze manier kunt u verzendkosten aan de reis toevoegen als voorraadvereffening op het moment dat de overboekingsorder wordt ontvangen. De overheadkosten kunnen worden gefactureerd voor de werkelijke kosten en worden bijgehouden voor een reis om de kosten van verkochte goederen bij te werken. Hoewel voor overboekingsorders in de standaardrelease geen goederen in transit worden gebruikt, kunnen ze wel aan transporten worden toegevoegd. De francoprijzen worden opgeteld bij de totale kosten van elk artikel.