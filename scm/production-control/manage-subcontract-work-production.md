---
title: Uitbesteding onderhanden productie beheren
description: 'Dit onderwerp wordt uitgelegd hoe uitbestede bewerkingen worden beheerd in Microsoft Dynamics 365 voor bewerkingen. Met andere woorden: hierin wordt uitgelegd hoe de productiebewerkingen die zijn toegewezen aan een bron worden beheerd door een leverancier.'
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 79430358bebd93fd96f1169d22737d3537dbfc08
ms.lasthandoff: 03/31/2017


---

# <a name="manage-subcontracting-work-in-production"></a>Uitbesteding onderhanden productie beheren

Dit onderwerp wordt uitgelegd hoe uitbestede bewerkingen worden beheerd in Microsoft Dynamics 365 voor bewerkingen. Met andere woorden: hierin wordt uitgelegd hoe de productiebewerkingen die zijn toegewezen aan een bron worden beheerd door een leverancier.

In [productieprocessen](production-process-overview.md), kan gebruik worden gemaakt door resources die eigendom zijn of die door leveranciers wordt beheerd. Leveranciersresources worden meestal gebruikt voor het niveau periodieke overtollige vraag die de beschikbare capaciteit van een bedrijf wordt overschreden eigen bronnen. De leverancier ook mogelijk om aan te bieden specifieke [Bronmogelijkheden](resource-capabilities.md)of resources tegen een lagere prijs.  

Afhankelijk van de leverancier-bronnen die worden gebruikt in een productieproces een [route](routes-operations.md) heeft vaak extra logistieke vereisten, omdat de materiaal- en half afgewerkte producten moeten eerst worden vervoerd naar de locatie van de leverancier. Het resultaat van de uitbestede bewerking moet vervolgens worden vervoerd naar de locatie die is toegewezen aan de volgende bewerking of aan een magazijn afgewerkte goederen.  

Wanneer u uitbesteding bewerkingen of activiteiten worden gebruikt, ze van invloed zijn op alle stadia van de bewerkingen van de definitie van de bewerkingen die vereist zijn voor productie, kostprijsberekeningsversie, prognoses, planningen en planning, het beheer van logistiek voor materialen, halffabrikaten en eindproducten. Ten slotte moeten deze bronnen hun eigen processen voor accounting en kostenbeheer.  

Voor interne bronnen is gewoonlijk een vaste kostentarief toegewezen voor een periode. Daarentegen is de kosten van uitbestede resources gebaseerd op de aankoopprijs van de gerelateerde prestaties. De service is gedefinieerd als een ander product en aan de aanschaffingscategorieën rijden en processen voor een bepaalde uitbestede bewerking opdracht wordt gebruikt.  

Er is momenteel geen expliciete concept van halffabrikaten in Microsoft Dynamics 365 voor bewerkingen. Voor een productieorder waarvoor meer dan één bewerking vereist voor het transformeren van grondstoffen in het eindproduct, het eindproduct wordt teruggestuurd naar de voorraad geboekt alleen in de laatste bewerking. De halfvoltooide producten die de eerdere bewerkingen produceren worden verantwoord in het onderhanden werk (OHW), maar ze niet zijn geboekt of bijgehouden in de voorraad. Hoewel u routes en stuklijsten (BOMs) in meerdere kleinere eenheden splitsen kunt, verhoogt deze methode het aantal producten, stuklijsten en routes die moeten worden beheerd.  

Er zijn twee methoden voor de modelvariabelen werk voor de productiebewerkingen uitbesteding. Deze methoden verschillen in de manier waarop dat de uitbesteding proces kan worden gemodelleerd, de manier waarop halffabrikaten worden weergegeven in het proces en de manier waarop kostenbeheer wordt beheerd.

-   Uitbesteding van routebewerkingen in productieorders of batchorders
    -   Het serviceproduct moet een product in voorraad, en deze moet deel uitmaken van de stuklijst.
    -   Deze methode ondersteunt first in, first out (FIFO) of een standaardkostprijs.
    -   Halffabrikaten worden vertegenwoordigd door het serviceproduct in het proces.
    -   Kostenbeheer worden de kosten die gekoppeld aan de materiaalkosten uitbestede werk zijn toegewezen.
-   Uitbesteding van productiestroomactiviteiten in een lean productiestroom
    -   De service is een niet-voorradige serviceproduct en deze geen deel uitmaakt van de stuklijst.
    -   Deze methode wordt de inkoopovereenkomsten als serviceovereenkomsten.
    -   Deze methode wordt de kostprijsberekening via terugwaarts afboeken.
    -   Deze methode kan gecombineerd en asynchrone aanschaffingscategorieën. (Materiaalstroom onafhankelijk is van het inkoopproces.)
    -   Kostenbeheer wijst uitbesteed werk in een eigen kosten onderverdeling blok.

## <a name="subcontracting-of-route-operations"></a>Uitbesteding van routebewerkingen
Als u wilt gebruiken van routebewerkingen voor productie of batchorders uitbesteding, de serviceproduct dat wordt gebruikt voor de levering van de service moet worden gedefinieerd als een product van de **Service** type. Bovendien moet er een artikelmodelgroep waarvoor het **product in voorraad** optie onder **voorraad beleid** ingesteld op **Ja**. Deze optie bepaalt of een product wordt verwerkt als voorraad op productontvangstbon (**product in voorraad** = **Ja**), of of het product als last opgenomen op een rekening voor winst en verlies (**product in voorraad** = **Nee**). Hoewel dit gedrag tegenstrijdige lijken mogelijk, is op basis van het feit dat alleen producten waarop dit beleid voorraadtransacties die kunnen worden gebruikt in kostenbeheer berekenen geplande kosten en de werkelijke kosten bepalen maakt wanneer een productieorder is beëindigd.  

Om te worden opgenomen in de berekening van planning en kosten, moet de service worden toegevoegd aan de stuklijst. De stuklijstregel moet van het **leverancier** type, en moeten worden toegewezen aan de routebewerking dat de service is toegewezen aan. Deze routebewerking moet beschikken over een middel voor kostprijsberekening en resourcevereiste die verwijzen naar een bron van de **leverancier** type waarmee de bewerking en de gerelateerde prestaties aan de bijbehorende leveranciersrekening.  

Wanneer deze configuratie wordt gebruikt, wordt een inkooporder gemaakt voor het gekoppelde product, op basis van een schatting van een productieorder. De inkooporder van de service wordt gebruikt als een anker voor de uitbestede bewerkingen. Uitbesteed werk kan worden beheerd via de **uitbesteed werk** lijstpagina in productiebeheer. Uitbesteed werk wordt gebruikt voor het verzenden van grondstoffen en, uiteindelijk een half afgewerkte product aan de leverancier ter voorbereiding van de bewerking. Deze ook worden ontvangen van het resulterende product van de uitbestede bewerking in de artikelontvangst, waar het serviceproduct wordt gebruikt ter identificatie van de aankomst van het half afgewerkte product. Wanneer de inkooporderregel wordt ontvangen, wordt de productiebewerking wordt bijgewerkt als voltooid.  

Een productieorder kan veel bewerkingen, en elke bewerking kan worden toegewezen aan een andere leverancier. Een end-to-end productieorder kan daarom meerdere inkooporders activeren.

## <a name="subcontracting-of-production-flow-activities"></a>Uitbesteding van productiestroomactiviteiten
De [lean manufacturing](lean-manufacturing-overview.md)oplossing dient als model voor het werk uitbesteding als een service die is gerelateerd aan een activiteit van een [productiestroom](http://ax.help.dynamics.com/en/wiki/create-a-production-flow-version/) (handleiding onderwerp). Daarom kan dit soort uitbesteding wordt ook genoemd [op basis van een activiteit uitbesteding.](activity-based-subcontracting.md) Een speciaal groepstype kosten **directe uitbesteding**, is geïntroduceerd, en de uitbestede services geen deel uitmaken van de stuklijst van de eindproducten. Wanneer u lean manufacturing, worden alle activiteiten worden gedefinieerd door kanbans die kan worden gekoppeld aan een of meerdere productiestroomactiviteiten. Tot nu toe die uitleg lijkt.Net als een uitleg van productieorders. Terwijl productieorders altijd met een eindproduct eindigen moeten, kunt u kanbans levering van een half afgewerkte product maken. U hoeft te introduceren een nieuwe product- en stuklijstniveau.  

Aangezien kanbanregels zeer dynamische, kunt u verschillende varianten van het aanbod voor hetzelfde product op een productiestroom modelleren. Wanneer u lean uitbesteding, de stroom van materiaal en Inkoopbeheer strikt gescheiden. Alle materiaalstroom wordt vertegenwoordigd door de activiteiten van de kanban. De inkooporders voor de serviceproducten en de boekingen van de ontvangst van deze services kunnen worden geautomatiseerd, op basis van de status van kanbantaken in de productiestroom. Kanbantaken kunnen worden gestart en voltooid voordat de inkooporders worden gemaakt. Per periode en de service kunnen de uitbesteding documenten (inkooporder en inkoopontvangst van de service) worden samengevoegd. Daarom kan het aantal regels en inkoopdocumenten klein, zelfs in zeer herhaalde bewerkingen waar leveranciers bieden voor uitbestede services in een stroom één stuk worden bewaard.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Modelvariabelen in een productiestroom uitbesteding

In een [lean productiestroom](lean-manufacturing-modeling-lean-organization.md), een procesactiviteit worden gedefinieerd als wanneer deze wordt toegewezen aan een werkcel (resourcegroep) dat een resource voor één leverancier heeft uitbesteed. Als een werkcel is uitbesteed, moeten de gerelateerde procesactiviteiten worden gekoppeld aan een actieve inkoopovereenkomstregel waarin het serviceartikel en de prijs van de service. De serviceovereenkomst van de activiteit definieert ook de berekening verhouding tussen de producthoeveelheid van de kanbantaak en de resulterende servicehoeveelheid. U kunt selecteren of de servicehoeveelheid wordt berekend op basis van het aantal taken, de goede hoeveelheid die in de taken wordt aangegeven of de totale producthoeveelheid (deze totale hoeveelheid omvat buiten gebruik gestelde producten).  

Overbrengactiviteiten kunnen ook worden gedefinieerd volgens uitbesteed. Deze definitie impliciet treedt op wanneer u de verantwoordelijke partij voor de verzending in de activiteit overboeken. Wanneer u selecteert **verzender** of **ontvanger**, als de bijbehorende bron of doel magazijn een magazijn leverancier beheerd, de activiteit wordt beschouwd als uitbesteed. Wanneer u selecteert **vervoerder**, de activiteit altijd is uitbesteed. Uitbestede procesactiviteiten, zoals een uitbestede overbrengactiviteit moet zijn gekoppeld aan een serviceovereenkomst voordat de productiestroom kan worden geactiveerd.

### <a name="backflush-costing"></a>Kostprijsberekening via terugwaarts afboeken

De kostprijsboekhouding van uitbesteed werk is volledig geïntegreerd in de kostprijsberekening voor de lean manufacturing-oplossing (kostprijsberekening via terugwaarts afboeken). Wanneer de inkooporder wordt ontvangen van de service wordt geboekt of wanneer facturering wordt uitgevoerd, worden de kosten van de service worden toegewezen aan de productiestroom. Voor kostprijsberekening via terugwaarts afboeken, wordt het verschil van uitbestede services berekend door de uitbesteding blok van de standaardkosten van de ontvangen producten ten opzichte van de werkelijke ontvangen en gefactureerd servicehoeveelheden tegenboeken.

## <a name="material-supply-for-subcontracted-operations"></a>Materiaal aanbod voor uitbestede bewerkingen
Halffabrikaten en andere bijbehorende materialen moeten worden overgebracht naar de locatie waar het werk fysiek wordt uitgevoerd. Wanneer u uitbestede bewerkingen en activiteiten, wordt deze overboeking vaak gerelateerd aan extra transport naar een locatie leverancier beheerd. Door het toewijzen van materiaal in de stuklijst naar de uitbestede bewerking, kunt u declareren dat het materiaal moet worden voorbereid op de invoerlocatie van de resourcegroep voor de toegewezen resource. Hoofdplanning of lean aanvulling en voorzieningen van het materiaal naar die locatie.  

Om de voorraad die zich bevindt op de leverancierslocatie van een te modelleren, verdient het beste in de industrie voor het definiëren van een magazijn leverancier beheerd. U kunt een magazijn leverancier beheerd eenvoudig definiëren door een nieuw magazijn maken en toewijzen van de leveranciersrekening. Om dit materiaal moet worden overgeboekt naar de leverancier voordat een bewerking kan worden uitgevoerd, moet u het magazijn beheerd met een leverancier aan het invoermagazijn van de resourcegroep waartoe de resource toewijzen.  

U kunt meerdere strategieën gebruiken voor het bijvullen van materiaal in dit magazijn:

-   Transferorders
-   Journalen overboeken
-   Opnamekanbans
-   Rechtstreekse aankoop op de leverancierslocatie

Half afgewerkte producten vormen een uitzondering op deze regel. Als u wilt overboeken halffabricaten, bent u beperkt tot de volgende opties:

-   Voor productie- en batchorders halffabricaten kunnen alleen worden overgebracht logisch via het orderverzamellijstjournaal uit de **uitbesteed werk** (lijstpagina). Dit journaal kunt maken, een afleveringsbewijs document die kan worden gebruikt om over te brengen half afgewerkte en de grondstof aan de leverancier.
-   Voor uitbestede bewerkingen in productiestromen, wordt de overdracht van halffabrikaten door de ontvangst van kanbans wordt ingetrokken of productie op de leverancierslocatie beschreven. Om een expliciete overbrengactiviteit modelleren, kunt u een productiekanban met een extra overbrengactiviteit beëindigen.

**opmerking:** een productieroute voor een afzonderlijke productieorder kan niet meerdere sites cross. Deze regel geldt ook voor uitbesteed werk. Daarom de magazijnen die staan voor de leverancier beheerd materiaal locaties in dezelfde site als de interne bronnen die worden gebruikt in de route moeten worden gedefinieerd. Hoewel productiestromen kunnen cross-sites, kunnen niet ze halffabricaten van de ene site naar een ander transport dat die bewerking een wijziging van de context van de kosten impliceert.  

De uitvoermagazijn en -locatie van een uitbestede resourcegroep worden doorgaans rechtstreeks toegewezen aan het magazijn en locatie van de volgende stap van de bewerking in de stroom van de route of productie. Deze instelling vermindert het bedrag van de taak melden die plaatsvindt of de nummerreeks extra overdrachtsbewerkingen die moeten worden gemodelleerd.


