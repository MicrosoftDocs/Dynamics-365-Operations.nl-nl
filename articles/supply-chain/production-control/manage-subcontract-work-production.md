---
title: Uitbesteed werk in productie beheren
description: 'In dit onderwerp wordt uitgelegd hoe uitbestede bewerkingen worden beheerd in Dynamics 365 Supply Chain Management. Met andere woorden: hierin wordt uitgelegd hoe de productiebewerkingen die zijn toegewezen aan een resource, worden beheerd door een leverancier.'
author: cvocph
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup, ProdBOMVendorListPagePreviewPane, ProdBOMVendor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11728694565b10bf0336671f6c1b5f43cbcadf78
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825814"
---
# <a name="manage-subcontracting-work-in-production"></a>Uitbesteed werk in productie beheren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe uitbestede bewerkingen worden beheerd in Dynamics 365 Supply Chain Management. Met andere woorden: hierin wordt uitgelegd hoe de productiebewerkingen die zijn toegewezen aan een resource, worden beheerd door een leverancier.

In [productieprocessen](production-process-overview.md) kunnen werkzaamheden worden uitgevoerd door resources die eigendom zijn van leveranciers of die door leveranciers worden beheerd. Leveranciersresources worden meestal gebruikt voor het nivelleren van periodiek excessieve vraag die de beschikbare capaciteit van de eigen resources van een bedrijf overschrijdt. De leverancier kan mogelijk ook specifieke [resourcemogelijkheden](resource-capabilities.md) of resources tegen een lagere prijs aanbieden.  

Afhankelijk van de leveranciersresources die in een productieproces worden gebruikt, heeft een [route](routes-operations.md) vaak extra logistieke vereisten, omdat het materiaal en de halffabricaten eerst moeten worden vervoerd naar de locatie van de leverancier. Het resultaat van de uitbestede bewerking moet vervolgens worden vervoerd naar de locatie die is toegewezen aan de volgende bewerking of naar een magazijn voor eindproducten.  

Wanneer uitbestede bewerkingen of activiteiten worden gebruikt, zijn deze van invloed op alle stadia van de bewerkingen, vanaf de definitie van de bewerkingen die vereist zijn in de productie, kostprijsberekening, prognoses, planning en inplanning, tot het beheer van logistiek voor materialen, halffabrikaten en eindproducten. Ten slotte hebben deze resources hun eigen processen voor boekhouding en kostenbeheer.  

Voor interne resources is gewoonlijk een vast kostentarief toegewezen voor een periode. Daarentegen worden de kosten van uitbestede resources gebaseerd op de inkoopprijs van de gerelateerde service. De service wordt gedefinieerd als een ander product en wordt gebruikt om de aanschaf- en inkoopprocessen aan te sturen voor een bepaalde uitbestede bewerking.  

Er is momenteel geen expliciet concept van halffabrikaten in Supply Chain Management. In geval van een productieorder waarvoor meer dan één bewerking is vereist om grondstoffen te transformeren in het eindproduct, wordt het eindproduct alleen in de laatste bewerking teruggeboekt naar de voorraad. De halffabricaten die door de eerdere bewerkingen worden geproduceerd, worden meegenomen in het onderhanden werk (OHW), maar ze worden niet geboekt of bijgehouden in de voorraad. Hoewel u routes en stuklijsten in meerdere kleinere eenheden kunt opsplitsen, verhoogt deze methode het aantal producten, stuklijsten en routes die moeten worden beheerd.  

Er zijn twee methoden voor het modelleren van uitbestede werkzaamheden voor productiebewerkingen. Deze methoden verschillen in de wijze waarop het uitbestedingsproces kan worden gemodelleerd, de manier waarop halffabrikaten worden vertegenwoordigd in het proces en de manier waarop kostenbeheer wordt beheerd.

-   Uitbesteding van routebewerkingen in productieorders of batchorders
    -   Het serviceproduct moet een product in voorraad zijn en moet deel uitmaken van de stuklijst.
    -   Deze methode ondersteunt FIFO (First In, First Out) of een standaardkostprijs.
    -   Halffabrikaten worden vertegenwoordigd door het serviceproduct in het proces.
    -   Kostenbeheer wijst de kosten die zijn gekoppeld aan uitbestede werkzaamheden toe aan de materiaalkosten.
-   Uitbesteding van productiestroomactiviteiten in een lean-productiestroom
    -   De service is een niet-voorradig serviceproduct en maakt geen deel uit van de stuklijst.
    -   Deze methode gebruikt inkoopovereenkomsten als serviceovereenkomsten.
    -   Deze methode gebruikt kostprijsberekening via terugwaarts afboeken.
    -   In deze methode is samengevoegde en asynchrone aanschaffing mogelijk. (Materiaalstroom is onafhankelijk van het aanschaffingsproces.)
    -   Kostenbeheer wijst uitbesteed werk in een eigen kostenanalyseblok toe.

## <a name="subcontracting-of-route-operations"></a>Uitbesteding van routebewerkingen
Als u uitbesteding van routebewerkingen wilt gebruiken voor productie- of batchorders, moet het serviceproduct dat wordt gebruikt voor de aanschaf van de service worden gedefinieerd als een product van het type **Service**. Bovendien moet het serviceproduct een artikelmodelgroep hebben waarvoor de optie **Product in voorraad** onder **Voorraadbeleid** is ingesteld op **Ja**. Deze optie bepaalt of een product wordt verwerkt als voorraad op een productontvangstbon (**Product in voorraad** = **Ja**), of dat het product wordt opgevoerd op een rekening voor winst en verlies (**Product in voorraad** = **Nee**). Hoewel dit gedrag tegenstrijdig lijkt, is het gebaseerd op het feit dat alleen producten waarop dit beleid van toepassing is, voorraadtransacties maken die kunnen worden gebruikt in kostenbeheer om geplande kosten te berekenen en de werkelijke kosten te bepalen wanneer een productieorder wordt beëindigd.  

De service moet aan de stuklijst worden toegevoegd om te worden meegenomen in de planning en kostenberekening. De stuklijstregel moet het type **Leverancier** hebben en moet worden toegewezen aan de routebewerking waaraan de service is toegewezen. Deze routebewerking moet beschikken over een kostprijsresource en resourcevereiste die verwijzen naar een resource van het type **Leverancier** waarmee de bewerking en de gerelateerde service worden gerelateerd aan de bijbehorende leveranciersrekening.  

Wanneer deze configuratie wordt gebruikt, wordt er een inkooporder gemaakt voor het gerelateerde serviceproduct, op basis van een schatting van een productieorder. De inkooporder van de service wordt gebruikt als een anker voor de uitbestede bewerkingen. Het uitbestede werk kan worden beheerd via de lijstpagina **Uitbesteed werk** in productiebeheer. Het uitbestede werk wordt gebruikt voor het verzenden van grondstoffen en uiteindelijk een halffabricaat naar de leverancier ter voorbereiding van de bewerking. Het wordt ook gebruikt voor ontvangst van het resulterende product van de uitbestede bewerking in de artikelontvangst, waar het serviceproduct wordt gebruikt ter identificatie van de aankomst van het halffabricaat. Wanneer de inkooporderregel wordt ontvangen, wordt de productiebewerking bijgewerkt als voltooid.  

Een productieorder kan vele bewerkingen hebben en elke bewerking kan worden toegewezen aan een andere leverancier. Een end-to-end productieorder kan daarom meerdere inkooporders activeren.

## <a name="subcontracting-of-production-flow-activities"></a>Uitbesteding van productiestroomactiviteiten
In de [lean manufacturing](lean-manufacturing-overview.md)-oplossing wordt het uitbestede werk gemodelleerd als een service die is gerelateerd aan een activiteit van een [productiestroom](tasks/create-production-flow-version.md) (Taakbegeleider-onderwerp). Daarom kan naar dit soort uitbesteding ook worden verwezen als [uitbesteding op basis van een activiteit.](activity-based-subcontracting.md) Er is een speciaal soort kostengroeptype met de naam **Rechtstreekse uitbesteding** geïntroduceerd en de uitbestedingsservices maken geen deel uit van de stuklijst van de eindproducten. Wanneer u lean manufacturing gebruikt, worden alle activiteiten gedefinieerd door kanbans die kunnen worden gekoppeld aan een of meer productiestroomactiviteiten. Tot nu toe lijkt die uitleg op de uitleg van productieorders. Maar terwijl productieorders altijd met een eindproduct eindigen, kunt u kanbans maken om een halffabricaat te leveren. U hoeft geen nieuw product en stuklijstniveau te introduceren.  

Omdat kanbanregels zeer dynamisch kunnen zijn, kunt u verschillende varianten van levering modelleren voor hetzelfde product in een productiestroom. Wanneer u lean-uitbesteding gebruikt, worden de materiaalstroom en de financiële stroom strikt gescheiden. De hele materiaalstroom wordt vertegenwoordigd door kanbanactiviteiten. De inkooporders voor de serviceproducten en de boekingen van de ontvangst van deze services kunnen worden geautomatiseerd op basis van de status van kanbantaken in de productiestroom. Kanbantaken kunnen worden gestart en voltooid voordat de inkooporders worden gemaakt. Per periode en service kunnen de uitbestedingsdocumenten (inkooporder en inkoopontvangst van de service) worden samengevoegd. Daarom kan het aantal inkoopdocumenten en regels klein worden gehouden, zelfs in bewerkingen die heel vaak worden herhaald, waarbij leveranciers uitbestede services in een stroom voor één stuk leveren.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Uitbesteding in een productiestroom modelleren

In een [lean-productiestroom](lean-manufacturing-modeling-lean-organization.md) kan een procesactiviteit worden gedefinieerd als uitbesteed wanneer deze wordt toegewezen aan een werkcel (resourcegroep) die een resource voor één leverancier heeft. Als een werkcel wordt uitbesteed, moeten de gerelateerde procesactiviteiten worden gekoppeld aan een actieve inkoopovereenkomstregel die het serviceartikel en de prijs van de service bevat. De serviceovereenkomst van de activiteit definieert ook de berekeningsverhouding tussen de producthoeveelheid van de kanbantaak en de resulterende servicehoeveelheid. U kunt aangeven of de servicehoeveelheid wordt berekend op basis van het aantal taken, de juiste producthoeveelheid die in de taken wordt aangegeven of de totale producthoeveelheid (deze totale hoeveelheid omvat buiten gebruik gestelde producten).  

Overbrengactiviteiten kunnen ook worden gedefinieerd als uitbesteed. Deze definitie treedt impliciet op wanneer u de verantwoordelijke partij voor de verzending in de overbrengactiviteit selecteert. Wanneer u **Verzender** of **Ontvanger** selecteert als het bijbehorende bron- of doelmagazijn een door de leverancier beheerd magazijn is, wordt de activiteit beschouwd als uitbesteed. Wanneer u **Vervoerder** selecteert, wordt de activiteit altijd uitbesteed. Net als uitbestede procesactiviteiten moet een uitbestede overbrengactiviteit worden gekoppeld aan een serviceovereenkomst voordat de productiestroom kan worden geactiveerd.

### <a name="backflush-costing"></a>Kostprijsberekening via terugwaarts afboeken

De kostprijsboekhouding van uitbesteed werk is volledig geïntegreerd in de kostprijsberekening van de lean manufacturing-oplossing (kostprijsberekening via terugwaarts afboeken). Wanneer de ontvangstlijst van de inkooporder van de service wordt geboekt of wanneer facturering wordt uitgevoerd, worden de kosten van de service toegewezen aan de productiestroom. In geval van kostprijsberekening via terugwaarts afboeken wordt het verschil van uitbestede services berekend door het uitbestedingsblok van de standaardkosten van de ontvangen producten ten opzichte van de werkelijke ontvangen en gefactureerde servicehoeveelheden tegen te boeken.

## <a name="material-supply-for-subcontracted-operations"></a>Materiaallevering voor uitbestede bewerkingen
Halffabrikaten en andere gerelateerde materialen moeten worden overgebracht naar de locatie waar het werk fysiek wordt uitgevoerd. Wanneer u uitbestede bewerkingen en activiteiten gebruikt, wordt deze overdracht vaak gerelateerd aan extra transport naar een locatie die door de leverancier wordt beheerd. Door materiaal in de stuklijst toe te wijzen aan de uitbestede bewerking, verklaart u dat het materiaal moet worden klaargezet op de invoerlocatie van de resourcegroep voor de toegewezen resource. Hoofdplanning of lean-aanvulling voorziet vervolgens in het materiaal voor die locatie.  

Om de voorraad die zich bevindt op de leverancierslocatie te modelleren, kunt u het beste een door de leverancier beheerd magazijn definiëren. U kunt een door de leverancier beheerd magazijn eenvoudig definiëren door een nieuw magazijn te maken en de leveranciersrekening toe te wijzen. Om vast te leggen dat materiaal moet worden overgebracht naar de leverancier voordat een bewerking kan worden uitgevoerd, moet u het door de leverancier beheerde magazijn toewijzen aan het invoermagazijn van de resourcegroep die de resource bevat.  

U kunt meerdere strategieën gebruiken voor het aanvullen van materiaal in dit magazijn:

-   overboekingsorders
-   Journalen overboeken
-   Opnamekanbans
-   Inkoop naar de leverancierslocatie sturen

Halffabrikaten vormen een uitzondering op deze regel. Als u halffabricaten wilt overbrengen, hebt u slechts de volgende opties:

-   In geval van productie- en batchorders kunnen halffabricaten alleen logischerwijs worden overgebracht via het orderverzamellijstjournaal op de lijstpagina **Uitbesteed werk**. Met dit journaal wordt een afleveringsbewijsdocument gemaakt dat kan worden gebruikt om halffabricaten en grondstoffen naar de leverancier over te brengen.
-   Voor uitbestede bewerkingen in productiestromen wordt de overdracht van halffabrikaten gedocumenteerd door de ontvangst van opnamekanbans of productiekanbans op de leverancierslocatie. Om een expliciete overbrengactiviteit te modelleren, kunt u een productiekanban met een extra overbrengactiviteit beëindigen.

**Opmerking:** een productieroute voor een afzonderlijke productieorder kan niet meerdere locaties omvatten. Deze regel geldt ook voor het uitbestede werk. Daarom moeten de magazijnen die de door de leverancier beheerde materiaallocaties vertegenwoordigen op dezelfde locatie worden gedefinieerd als de interne resources die in de route worden gebruikt. Hoewel productiestromen meerdere locaties kunnen omvatten, kunnen ze geen halffabricaten van de ene locatie naar de ander locatie vervoeren, omdat die bewerking een wijziging van de kostprijscontext inhoudt.  

Het uitvoermagazijn en de uitvoerlocatie van een uitbestede resourcegroep worden doorgaans rechtstreeks toegewezen aan het magazijn en de locatie van de volgende stap van de bewerking in de route of productiestroom. Deze instelling zorgt ervoor dat de hoeveelheid taakrapportage minder wordt of het aantal overdrachtsbewerkingen die moeten worden gemodelleerd.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]