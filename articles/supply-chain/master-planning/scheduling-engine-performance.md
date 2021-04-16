---
title: Prestaties van planningsengine verbeteren
description: Dit onderwerp biedt informatie over de planningsengine en over hoe u de prestaties kunt verbeteren.
author: ChristianRytt
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1378ae652ea70cba941316f4667052dcb05f717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812902"
---
# <a name="improve-scheduling-engine-performance"></a>Prestaties van planningsengine verbeteren

[!include [banner](../includes/banner.md)]

De planningsengine voor resources wordt gebruikt bij het plannen van routes voor geplande en vrijgegeven productieorders. De engine werd oorspronkelijk uitgebracht als onderdeel van Dynamics AX 2012 en heeft sinds de release verschillende verbeteringen ondergaan.

Het [probleem van taakplanning op de werkvloer](https://en.wikipedia.org/wiki/Job_shop_scheduling) is een uitzonderlijk ingewikkelde gecombineerde kwestie waarbij de oplossingstijd exponentieel toeneemt met het aantal beslissingsvariabelen. Vaak hebben klanten productieroutes en gerelateerde gegevens ingesteld op een manier die leidt tot een planningsprobleem dat niet binnen redelijke tijd kan worden opgelost, zelfs op de meest moderne hardware. Dit onderwerp helpt u bij het begrijpen van de planningsengine en biedt inzicht in hoe een bepaalde instelling invloed op de prestaties kan hebben.

Wanneer u de prestaties van de planning wilt verbeteren, is het raadzaam de complexiteit te reduceren van het probleem dat door de engine moet worden opgelost. Enkele van de belangrijkste factoren die van invloed kunnen zijn op de prestaties zijn:

- Routes met veel bewerkingen
- Routes met parallelle bewerkingen
- Bewerkingen met een hoeveelheid resources van meer dan één
- Bewerkingen met veel van toepassing zijnde resources
- Gebruik van harde koppelingen
- Gebruik van eindige capaciteit
- Het aantal verschillende kalenders dat wordt gebruikt
- Het aantal werktijdvakken per dag in de kalender
- Totale duur van de route
- Gelijktijdige uitvoering van meerdere planningsengines

## <a name="overview-of-basic-scheduling-flow"></a>Overzicht van de basisplanningsstroom

Om inzicht te krijgen in de prestaties van een bepaalde instelling, is het belangrijk dat u begrijpt hoe het proces verloopt, zowel binnen de engine als in de omringende X++-code.

Het basisproces voor het plannen van een order bestaat uit drie hoofdstappen:

- **Gegevens laden**: hier worden de X++-gegevensmodellen omgezet in het interne gegevensmodel van de engine in de vorm van taken en beperkingen.
- **Planning**: dit is de hoofdbron voor de planning waarbij het opgegeven model en de beperkingen worden verwerkt en een resultaat wordt gegenereerd. Tijdens dit proces zal de engine waar nodig de werktijdinformatie en bestaande capaciteitsreserveringen opvragen van X++.
- **Gegevens opslaan**: de engine resulteert in de vorm van reserveringstijdvakken voor taakcapaciteit en wordt verwerkt door X++-code om capaciteitsreserveringen op te slaan en de begin- en eindtijd van de taken/bewerking/order bij te werken.

## <a name="load-data-into-the-engine"></a>Gegevens in de engine laden

De planningsengine heeft een meer abstract gegevensmodel dan de Supply Chain Management-database omdat deze is gemaakt als een algemene engine die verschillende gegevensbronnen kan verwerken. De concepten van route, secundaire bewerkingen en uitvoeringstijd moeten worden 'vertaald' naar het algemene taak- en beperkingsmodel dat door de engine wordt gehanteerd. De logica voor het opbouwen van het model bevat een aanzienlijke hoeveelheid bedrijfslogica en is afhankelijk van de brongegevens. De verantwoordelijke X++-klasse is `WrkCtrScheduler` en deze heeft afgeleide klassen voor geplande productieorders, vrijgegeven productieorders en projectprognoses.

Een voorbeeld hiervan is een route die wordt weergegeven in de volgende tabel en afbeelding, die relatief eenvoudig lijkt.

| Bew. Nr. | Prioriteit | Insteltijd | Uitvoeringstijd | Wachttijd na | Hoeveelheid resources | Volgende |
| --- | --- | --- | --- | --- | --- | --- |
| 10 | Primair | 1.00 | 2.00 | | 1 | 20 |
| 10 | Secundair&nbsp;1 | | | | 1 | 20 |
| 20 | Primair | | 3.00 | 1.00 | 3 | 0 |

![Voorbeeld van routediagram](media/scheduling-engine-route.png "Voorbeeld van routediagram")

Wanneer u dit verzendt naar de engine, wordt het opgesplitst in acht taken, zoals wordt weergegeven in de volgende afbeelding (selecteer de afbeelding om deze te vergroten).

[![Taken van planningsengine](media/scheduling-engine-jobs.png "Taken van planningsengine")](media/scheduling-engine-jobs-large.png)

De standaardkoppeling tussen twee taken is `FinishStart`, wat inhoudt dat de eindtijd van de ene taak vóór de begintijd van een andere taak moet liggen. Aangezien de instellingen moeten worden uitgevoerd door dezelfde resource die het proces later uitvoert, zijn er `OnSameResource`-beperkingen. Tussen de taken voor primaire en secundaire bewerking voor 10 zijn er `StartStart`- en `FinishFinish`-koppelingen, wat betekent dat de taken zowel op hetzelfde moment moeten beginnen als eindigen en dat er `NotOnSameResource`-beperkingen zijn, waardoor niet dezelfde resource voor primaire en secundaire bewerking wordt gebruikt.

Voor bewerking 20, waarbij de hoeveelheid resources is ingesteld op 3, is de procestaak opgesplitst in drie afzonderlijke taken waarbij alle taken op exact dezelfde tijd moeten worden uitgevoerd.
In dit geval is de routegroep zo ingesteld dat er geen capaciteit voor de wachtrij wordt gereserveerd, waardoor er slechts één taak is voor de wachtrij.

De planningsengine begrijpt alleen de concepten van taken en heeft geen idee van bewerkingen. Dit betekent dat de bewerkingen bij het uitvoeren van bewerkingstaken ook worden opgesplitst in taken, hoewel deze niet worden vastgelegd in de database.

Voor elke taak wordt ook gedefinieerd wat de vereiste taakcapaciteit is (het aantal seconden dat is vereist). Afhankelijk van de manier waarop de resourcevereisten zijn gedefinieerd, kunnen we voor elke taak ook een lijst verzenden met alle mogelijke resources waarvoor de taak kan worden uitgevoerd en wat de capaciteitsbehoefte voor die specifieke resource is. Hoewel de lijst met toepasselijke resources tijdens het maken van het model wordt verzonden, moet de engine nog steeds zorgen dat de resourcetoewijzing werkelijk geldig is voor de gehele taakduur.

## <a name="scheduling-engine-internals"></a>Interne werking van planningsengine

### <a name="scheduling-engine-interface"></a>Interface van planningsengine

Om een idee te krijgen van de interne werking van de engine, kunt u het beste de functionaliteit bekijken die extern wordt weergegeven. In X++ is `WrkCtrSchedulerEngineInterface` de hoofdinterface. Deze bevat de methoden die in de volgende subsecties worden beschreven.

#### <a name="general-engine"></a>Algemene engine

| **methode** | **Doel** |
| --- | --- |
| `run` | Alle geladen taken worden gepland en de foutcode wordt weergegeven. |
| `getJobSchedulingSequenceResult` | Haalt het planningsresultaat op en de eerste fouttaak voor de reeks die wordt geïdentificeerd door een specifieke taak. |
| `validateJobCapacityReservations` | Valideert de capaciteitsreserveringen voor alle taken die door de engine zijn opgeslagen. |
| `setReservationsTimeStamp` | Verzendt een tijdstempel naar de engine die is ingesteld voor alle nieuwe capaciteitsreserveringen voor de geplande taken in de cache van de engine. |
| `addPropertyToGroupAggregation` | Voegt een eigenschapsvoorvoegsel toe aan de set eigenschappen die wordt gebruikt wanneer de capaciteit wordt samengevoegd. |
| `addResource` | Voegt een resource toe aan de resourcegroep van de planningsengine. |
| `addResourceGroup` | Voegt een resourcegroep toe aan de resourcegroeppool van de planningsengine. |
| `addResourceGroupMembership` | Voegt een resource als lid toe aan een resourcegroep. |
| `addOptimizationGoal` | Voegt een doel voor planningsoptimalisatie toe (duur of prioriteit). |

#### <a name="individual-jobs"></a>Afzonderlijke taken

| **methode** | **Doel** |
| --- | --- |
| `addJobInfo` | Voegt een record met taakgegevens toe die de engine informeert over een taak die moet worden gepland. |
| `addConstraintJobEndsAt` | Voegt een beperking toe dat een taak op een bepaalde datum en tijd moet worden beëindigd. |
| `addConstraintJobStartsAt` | Voegt een beperking toe dat een taak op een bepaalde datum en tijd moet worden gestart. |
| `addConstraintMaxJobDays` | Definieert de beperking dat een taak een opgegeven maximumaantal dagen kan beslaan. |
| `addConstraintResourceRequirement` | Voegt de beperking toe dat de taak moet worden gepland voor een specifieke resource. |
| `addJobBindPriority` | Voegt een taakbindingsprioriteit toe voor een (taak, beperkingsniveau)-paar. Een hogere prioriteit betekent dat de taakvariabelen eerder zijn gebonden. De taak wordt verwerkt vóór taken met een lagere prioriteit in dezelfde volgorde. |
| `addJobCapacity` | Voegt informatie over capaciteitsbelasting toe voor een taak (zoals de vereiste uitvoeringstijd voor een taak) die onafhankelijk is van de resource waarop de taak wordt uitgevoerd. |
| `addJobResourceCapacity` | Voegt een resource toe aan de reeks resources waarmee de taak wordt uitgevoerd en geeft de vereiste capaciteit aan wanneer deze wordt uitgevoerd op die resource. |
| `addJobGoal` | Voegt informatie over taakdoelen toe voor een specifiek beperkingsniveau (vroegste eindtijd of laatste begintijd). |
| `addJobResourcePriority` | Voegt de prioriteit toe die moet worden gebruikt wanneer een taak voor een resource wordt gepland. |
| `addJobResourceRuntime` | Geeft een taaktijd op die afhankelijk is van de resource waarop het project wordt gepland. |
| `addJobRuntime` | Geeft een taaktijd op die onafhankelijk is van de resource waarop het project wordt gepland. |
| `scheduleJobOnResourceGroup` | Markeert een taak voor de planning op het niveau van de resourcegroep. |
| `setJobResourcePreemptionAllowed` | Stelt in of voorrang nemen is toegestaan voor een taak in een resource (als de engine de taak kan plannen in niet-aaneengesloten capaciteitstijdvakken). |
| `setRequiredNumberOfResources` | Stel het aantal resources in dat nodig is om een taak te plannen (alleen voor de planning van bewerkingen). |

#### <a name="constraints-between-jobs"></a>Beperkingen tussen taken

| **methode** | **Doel** |
| --- | --- |
| `addJobLink` | Voegt een koppeling (zoals einde\>begin) tussen twee taken toe. |
| `addConstraintEndsDelayed` | Definieert de beperking dat een taak niet kan worden beëindigd voordat een andere taak eindigt en enige vertragingstijd. |
| `addConstraintJobListWorkingTimeIntersect` | Voegt een beperking toe dat de capaciteitstijdvakken die zijn gereserveerd voor de taken zich in de kruisende werktijden moeten bevinden voor de twee resources die door de taken worden gebruikt. |
| `addConstraintJobOverlap` | Voegt een beperking toe waarmee wordt gedefinieerd hoe taken worden geordend wanneer een bepaalde hoeveelheid van een artikel kan worden verplaatst tussen twee resources terwijl de eerste resource nog steeds niet is verwerkt, zodat de tweede resource de verwerking kan starten. |
| `addConstraintNotOnSameResource` | Voegt een beperking toe dat twee taken niet mogen worden gepland voor dezelfde resource. |
| `addConstraintOnSameResource` | Voegt een beperking toe dat twee taken moeten worden gepland met dezelfde resource. |
| `addJobSameReservations` | Voegt een beperking toe dat een taak moet eindigen met capaciteitsreserveringen voor dezelfde tijdvakken als de primaire taak. |
| `setPrimaryParallelJob` | Voegt informatie toe over welke taak de primaire taak is in een set parallelle taken. |

### <a name="solver"></a>Oplossing

De engine zelf is in feite een gespecialiseerde beperkingsoplosser waaraan aangepaste heuristiek is toegevoegd. De oplosser is gebaseerd op twee hoofdelementen: variabelen en beperkingen.

#### <a name="variable"></a>Variabele

Een variabele vertegenwoordigt een domein van mogelijke waarden. Planningsengine heeft twee typen variabelen:

- **DateTime-variabele**: heeft een domein van alle datums en tijden en het domein kan worden beperkt door de onder- en bovengrens voor de tijd van de variabele dichter bij elkaar te plaatsen.
- **Resource-variabele**: heeft een domein van toepasselijke resources en het domein kan worden beperkt door resources uit de lijst te verwijderen.

#### <a name="constraint"></a>Beperking

Een beperking werkt op variabelen door de bijbehorende domeinen te beperken, maar is ook afhankelijk van variabelen die worden geactiveerd wanneer de variabelen worden gewijzigd. Het proces van het 'doorgeven van beperkingen' vindt plaats wanneer een beperking de hoofdfunctie uitvoert en rapporteert aan de hoofdlogica als deze is geslaagd.

Een variabele wordt als gebonden beschouwd wanneer deze verder niet kan worden beperkt, wat voor de DateTime-variabele inhoudt dat de boven- en ondergrens hetzelfde is en voor de Resource-variabele dat deze slechts één toepasselijke resource heeft. Wanneer alle variabelen zijn gekoppeld, wordt er een oplossing gevonden.

### <a name="constraint-levels"></a>Beperkingsniveaus

Wanneer de planning wordt uitgevoerd als onderdeel van de dekkingsfase van de materiaalbehoefteplanning, worden de orders teruggepland vanaf de behoeftedatum. Als het echter niet mogelijk is om een planning te vinden die vandaag of later wordt gestart en eindigt voor de behoeftedatum, wordt de planningsrichting gewijzigd in vooruit vanaf vandaag.

Deze hoofdbedrijfsregel wordt verwerkt door de beperkingen in niveaus te ordenen. Als er geen oplossing wordt gevonden bij het gebruik van de beperkingen op het hoogste niveau, worden de beperkingen op dat niveau verwijderd en wordt het lagere niveau geprobeerd. In de praktijk betekent dit dat voor achterwaarts plannen het model een niveau 1 bevat met taakdoelen van laatste begintijd en een beperking voor maximale eindtijd (de behoeftedatum) en een niveau 0 met taakdoelen van vroegste eindtijd en een beperking van vandaag voor minimale begintijd.

### <a name="algorithm"></a>Algoritme

De belangrijkste stappen van het algoritme van de engine zijn:

1. Zoek reeksen (ketens van taak) die afzonderlijk kunnen worden opgelost.
1. Probeer een eerste oplossing te vinden voor de reeks voor het hoogste beperkingsniveau.
    1. Sorteer de taken in de volgorde op basis van doel en prioriteiten van de taak, zodat een starttaak kan worden gevonden.
    1. Herhaal de taken in deze volgorde:
        1. Zoek alle beperkingen die moeten worden doorgegeven en voer de doorgifte uit.
        1. Als alle variabelen voor de taak zijn gebonden, is er een oplossing voor die taak gevonden.
        1. Als een van de variabelen niet kan worden gebonden zonder de beperkingen te schenden, kunt u de binding van de variabele terugdraaien, een andere waarde proberen in het domein (voor resource-variabele) en de doorgifte van beperkingen opnieuw uitvoeren.
1. Als er geen oplossing is gevonden, worden alle beperkingen op het huidige beperkingsniveau verwijderd, wordt het niveau lager (als er lagere niveaus beschikbaar zijn) en wordt er met de nieuwe beperking geprobeerd een oplossing te zoeken.
1. Als er een bruikbare oplossing is gevonden, wordt de optimaliseringsfase gestart. Hierbij wordt geprobeerd een betere oplossing te vinden totdat de time-out voor optimalisatie is bereikt of alle resourcecombinaties zijn uitgeput.

De beperkingsoplossing is niet bekend met de specifieke planningsalgoritmen. De 'magie' vindt plaats bij de definitie en combinatie van de verschillende beperkingen.

### <a name="determining-working-times"></a>Werktijden bepalen

Een groot deel van de (interne) beperkingen in de engine bepaalt de werktijd en capaciteit van een resource. De taak is in wezen het laten doorlopen van de werktijden voor een resource vanaf een bepaald punt in een bepaalde richting en het zoeken van een interval waarin de vereiste capaciteit (tijd) voor de taken kan passen.

Hiervoor moet de engine de werktijden van een resource kennen. In tegenstelling tot de gegevens van het hoofdmodel ziijn de werktijden *lazy loaded*, wat betekent dat ze naar behoefte in de engine worden geladen. De reden hiervoor is dat een kalender in Supply Chain Management vaak werktijden voor een zeer lange tijd bevat en dat er meestal veel kalenders zijn, zodat de hoeveelheid gegevens te groot zou zijn om vooraf te worden geladen.

Kalendergegevens worden door de engine in segmenten aangevraagd door de X++-klassemethode `WrkCtrSchedulingInteropDataProvider.getWorkingTimes` aan te roepen. De aanvraag is voor een specifieke kalender-id binnen een bepaald tijdsinterval. Afhankelijk van de status van de servercache in Supply Chain Management, kan elk van deze aanvragen een aantal databaseaanroepen opleveren, wat veel tijd in beslag neemt (vergeleken met de zuivere rekentijd). Als de kalender zeer complexe werktijddefinities bevat met veel werktijdintervallen per dag, duurt het laden nog langer.

Wanneer de werktijdgegevens in de planningsengine worden geladen, worden deze in de interne cache voor de specifieke kalender bewaard, wat betekent dat als er andere taken of resources in dezelfde kalender worden gebruikt, de volgende zoekopdrachten snel vanuit het geheugen kunnen worden uitgevoerd. Een veelvoorkomende oorzaak van slechte prestaties is het feit dat er voor elke resource een afzonderlijke kalender-id wordt gebruikt, omdat er vervolgens gegevens moeten worden aangevraagd voor elke kalender, zelfs als de inhoud van de kalenders hetzelfde kan zijn.

### <a name="finite-capacity"></a>Eindige capaciteit

Wanneer u eindige capaciteit gebruikt, worden de werktijdvakken uit de kalender gesplitst en verminderd op basis van de bestaande capaciteitsreserveringen. Deze reserveringen worden ook met dezelfde `WrkCtrSchedulingInteropDataProvider`-klasse opgehaald als de kalenders, maar gebruiken in plaats daarvan de `getCapacityReservations`-methode. Bij het plannen tijdens de hoofdplanning wordt rekening gehouden met de reserveringen voor het specifieke hoofdplan en als deze zijn ingeschakeld op de pagina **Parameters hoofdplanning**, worden de reserveringen van gefiatteerde productieorders eveneens opgenomen. Bij het plannen van een productieorder is het ook een optie om reserveringen van bestaande geplande orders op te nemen, hoewel dit niet zo gebruikelijk is als de andere methode.

Door het gebruik van eindige capaciteit zal de planning om een aantal redenen langer duren:

- Het ophalen van de capaciteitsgegevens uit de database is een trage bewerking en het opslaan in de cache van capaciteitsgegevens op de server is meestal niet zo goed als voor werktijden omdat deze niet worden gedeeld door resources zoals kalenders.
- Het aantal werktijdvakken dat moet worden doorlopen neemt toe vanwege opssplitsingen en tijdvakken voor een langere periode moeten doorgaans worden onderzocht voordat een oplossing kan worden gevonden.
- Nadat de planning is voltooid, moet er een controle op conflicterende reserveringen worden uitgevoerd (zie de sectie 'Gelijktijdige uitvoering van meerdere planningsengines' voor meer informatie).

### <a name="examining-the-resource-combinations"></a>De resourcecombinaties onderzoeken

Als de takenreeks alleen de standaard `FinishStart`-koppelingen bevat, zodat deze een eenvoudige keten zonder vertakkingen vormt, kunt u een optimaal resultaat (gezien vanuit de enkele order, niet over orders heen) bereiken met behulp van de beste oplossing voor de eerste taak en vervolgens naar de beste oplossing voor de volgende taak gaan. De beste oplossing voor een taak betekent het zoeken van de resource die de begin- en einddatum kan halen van de taak die het dichtst bij het taakdoel ligt (bij voorwaarts plannen betekent dit dat de einddatum van de taak zo vroeg mogelijk ligt) terwijl de beperkingen nog steeds worden gerespecteerd.

Wanneer er parallelle taken zijn, kan het zoeken naar een oplossing betrekking hebben op het onderzoeken van verschillende combinaties van resources. Het aantal mogelijke resourcecombinaties is het product van het aantal toepasselijke resources voor de verbonden parallelle taken. Met name wanneer een order terug wordt gepland vanaf een behoeftedatum, kan het een tijdje duren om te realiseren dat er geen oplossing voor het probleem is, waardoor de parallelle taken vóór de datum van vandaag zullen worden uitgevoerd, aangezien alle combinaties moeten worden gecontroleerd, omdat er mogelijk bepaalde resources zijn met een hogere efficiëntie of een andere kalender die een resultaat kan opleveren. Dit betekent dat als er geen time-outlimiet is ingesteld, de uitvoering lange tijd doorgaat voordat de richting in voorwaarts wordt gewijzigd.

Deze combinatorische logica betekent ook dat het toevoegen van meer toepasselijke resources tot een tragere uitvoering van de engine kan leiden. Als er prestatieproblemen optreden wanneer er parallelle bewerkingen en een oneindige capaciteit worden gepland, kan deze gedeeltelijk worden bepaald door de routeontwerper een beslissing te laten nemen over welke resource moet worden gebruikt en vervolgens de resource rechtstreeks aan de bewerking toe te wijzen (omdat de engine in de meeste gevallen altijd dezelfde resource ophaalt en het eindresultaat dus hetzelfde blijft).

### <a name="hard-links"></a>Harde koppelingen

Als u het koppelingstype tussen twee taken instelt op hard, zorgt u ervoor dat er geen tijdshiaat bestaat tussen het einde van de ene taak en het begin van de volgende. Dit kan erg handig zijn in scenario's als wanneer metaal wordt verhit in de ene taak en vervolgens verwerkt in de volgende taak, waarbij het niet wenselijk is om het metaal tussendoor te laten afkoelen.

Met standaard zachte koppelingen en voorwaartse planningen kan, als de route een eenvoudige keten zonder vertakkingen is, een oplossing worden bereikt door een oplossing te vinden voor de eerste taak die aan zijn eigen beperkingen voldoet en vervolgens door de keten wordt verplaatst waarbij de eindtijd van de vorige taak wordt doorgegeven aan de volgende taak. Als de huidige taak geen capaciteit kan vinden, wordt de begintijd voor deze taak verder verplaatst zonder dat er een leemte bestaat tussen de taken. Met harde koppelingen (met name met betrekking tot eindige capaciteit) voor hetzelfde scenario, betekent het feit dat een taak de capaciteit verderop in de keten niet kan vinden, dat alle eerder geplande taken één voor één moeten worden 'meegesleept' en dus een aantal keren opnieuw worden gepland. Met name in scenario's met een hoge belasting voor meerdere resources kunnen de harde koppelingen een kettingreactie veroorzaken waarbij de taken elkaar beïnvloeden en er een aantal iteraties moet worden uitgevoerd voordat het resultaat zich stabiliseert in een haalbaar schema.

## <a name="running-scheduling-engines-in-parallel"></a>Gelijktijdige uitvoering van planningsengines

Bij het uitvoeren van een planning als onderdeel van een hoofdplanning waarin helpers worden gebruikt, kan elk van de helper-threads voor de hoofdplanning ook activiteiten voor de planning van productieorders ophalen. Dit houdt in dat meerdere planningsengines tegelijkertijd kunnen worden uitgevoerd. Hoewel multithreading in het algemeen een zeer belangrijk prestatievoordeel is, zijn er ook enkele functionele nadelen wat betreft planning.

In MRP worden alle productieorders voor een bepaald stuklijstniveau gepland in de behoeftedatumreeks, wat betekent dat de orders met de vroegste behoeftedatum eerst moeten worden gepland waardoor de beschikbare resourcecapaciteit zo hoog mogelijk wordt. Wanneer meerdere engines gebruikmaken van de lijst met ongeplande orders, is de reeks echter niet lanager gegarandeerd, aangezien de ene engine mogelijk sneller gereed is dan een andere.

Bovendien kan een race condition optreden bij het plannen met behulp van eindige capaciteit en wanneer meerdere engine-exemplaren proberen om orders te plannen die mogelijk gebruikmaken van dezelfde resources in hetzelfde tijdsinterval. Het aantal van dergelijke race condities wordt vastgelegd in het veld **Planningsconflicten** op de geschiedenispagina van de hoofdplanning. De logica voor het oplossen van conflicten is als volgt:

- Plan een order (zonder vergrendeling) en haal capaciteitsreserveringen op.
- Neem de vergrendeling.
- Controleer of er nieuwere capaciteitsreserveringen bestaan voor de geplande resources in het tijdsbestek.
  - Als dat niet zo is, schrijft u de capaciteit en heft u de vergrendeling op.
  - Zo ja, dan heft u de vergrendeling op en plant u de order opnieuw vanaf het begin.

Bij het plannen van meerdere engine-exemplaren is het resultaat dus niet volledig deterministisch, omdat het afhankelijk is van de exacte timing van elk van de threads.

## <a name="operation-scheduling-performance"></a>Prestaties van bewerkingsplanning

Hoewel de bewerkingsplanning ook wel eens capaciteitsplanning wordt genoemd, gezien uit het oogpunt van de engine, kan het moeilijker zijn om een oplossing te vinden als er beperkte capaciteit wordt gebruikt, aangezien er meer gegevens nodig zijn om de haalbaarheid te bepalen.

De capaciteit van een resourcegroep is afhankelijk van welke en hoeveel resources lid zijn van de resourcegroep. Een resourcegroep op zichzelf heeft geen capaciteit. Alleen als resources lid zijn van de groep hebben zij capaciteit. Omdat het lidmaatschap van de resourcegroep kan variëren per periode, moet de capaciteit per dag worden geëvalueerd.

Bij de bewerkingsplanning wordt de kalender van de resourcegroep gebruikt om de begin- en eindtijd voor elke bewerking te bepalen. Dit houdt in dat in de kalender van de resourcegroep een limiet wordt ingesteld voor de hoeveelheid tijd waarvoor bewerkingsplanning voor één bewerking op één dag in één resourcegroep kan worden uitgevoerd. In tegenstelling tot bij de kalender voor de specifieke resources worden de efficiëntiegegevens van de kalender genegeerd voor de resourcegroep, aangezien hiervoor simpelweg openingstijden en geen werkelijke capaciteit worden aangegeven.

Als de werktijd voor een resourcegroep op een bepaalde datum bijvoorbeeld van 8:00 tot 16:00 bedraagt, kan een bewerking de resourcegroep niet verder belasten dan past in 8 uur, ongeacht de hoeveelheid capaciteit van de resourcegroep op die dag. De beschikbare capaciteit kan de belasting echter verder beperken.

De belasting van de taakplanning voor alle resources die zijn opgenomen in de resourcegroep op een bepaalde dag wordt meegenomen bij het berekenen van de beschikbare capaciteit voor de resourcegroep op dezelfde dag. Voor elke datum is de berekening:

*Beschikbare capaciteit resourcegroep = capaciteit voor resources in de groep op basis van hun kalender &ndash; voor de taak geplande belasting voor de resources in de groep &ndash; voor bewerkingen geplande belasting voor de resources in de groep &ndash; voor bewerkingen geplande belasting voor de resourcegroep*

Op het tabblad **Resourcevereisten** van de routebewerking kunt u de resourcebehoeften opgeven met behulp van een specifieke resource (in welk geval de bewerking wordt gepland met behulp van die resource), voor een resourcegroep, voor een resourcetype of voor een of meer capaciteiten, kwalificaties, cursussen of certificaten. Wanneer u al deze opties gebruikt, kunt u het routeontwerp op een flexibele manier plannen, maar de planning voor de engine wordt hierdoor ook bemoeilijkt, omdat de capaciteit moet worden berekend per 'eigenschap' (de abstracte naam die in de-engine wordt gebruikt voor capaciteit, vaardigheden enzovoort).

De capaciteit van de resourcegroep voor een capaciteit is de som van de capaciteit voor alle resources in de resourcegroep die de desbetreffende mogelijkheid heeft. Als een resource in de groep een mogelijkheid heeft, wordt deze in overweging genomen, ongeacht het vereiste niveau van de capaciteit.

Bij de bewerkingsplanning wordt de beschikbare capaciteit voor een bepaalde capaciteit voor een resourcegroep verlaagd wanneer deze wordt geladen met een bewerking waarvoor de desbetreffende functie vereist is. Als voor de bewerking meer dan één mogelijkheid is vereist, wordt de capaciteit voor alle vereiste capaciteiten verlaagd.

Voor elke datum is de vereiste berekening:

*Beschikbare capaciteit voor een mogelijkheid = capaciteit voor de mogelijkheid &ndash; voor taak geplande belasting voor de resources met de specifieke mogelijkheid die is opgenomen in de resourcegroep &ndash; voor bewerkingen geplande belasting voor de resources met de specifieke mogelijkheid die is opgenomen in de resourcegroep &ndash; voor bewerkingen geplande belasting voor de resourcegroep zelf die de specifieke capaciteit vereist*

Dit houdt in dat als er wordt geladen voor een specifieke resource, de belasting wordt meegenomen bij de berekening van de beschikbare capaciteit van de resourcegroep per mogelijkheid, omdat de belasting van een specifieke resource de bijdrage van de resourcegroep verlaagt voor een mogelijkheid, ongeacht of de belasting voor de specifieke resource voor die specifieke mogelijkheid geldt. Als er wordt geladen op het niveau van de resourcegroep, wordt deze alleen in de berekening van de beschikbare capaciteit van de resourcegroep per mogelijkheid beschouwd als de werklast afkomstig is van een bewerking waarvoor de specifieke mogelijkheid vereist is.

De bovenstaande logica is ingewikkeld, aangezien deze voor elk type 'eigenschap' hetzelfde is, zodat er voor het gebruik van bewerkingsplanning met beperkte capaciteit een aanzienlijke hoeveelheid gegevens moet worden geladen.

## <a name="viewing-scheduling-engine-input-and-output"></a>Invoer en uitvoer van planningsengine weergeven

Als u specifieke informatie over de invoer en uitvoer van het planningsproces wilt weergeven, schakelt u logboekregistratie in door naar **Organisatiebeheer \> Instellen \> Planning \> Traceringscockpit plannen** te gaan.

Selecteer op deze pagina de optie **Logboekregistratie inschakelen** in het actievenster. Voer vervolgens de planning voor de productieorder uit. Keert, wanneer u klaar bent, terug naar de pagina **Traceringscockpit plannen** en selecteer **Logboekregistratie uitschakelen** in het actievenster. Vernieuw de pagina. Er wordt nu een een nieuwe regel weergegeven in het raster. Selecteer de nieuwe regel en selecteer **Downloaden** in het actievenster. Hierdoor krijgt u een gecomprimeerde ZIP-map met de volgende bestanden:

- **Log. txt**: dit is het logboekbestand waarin de stappen worden beschreven die de engine doorloopt. Het is zeer uitgebreid en kan een beetje overweldigend zijn, maar wanneer dit wordt gebruikt als onderdeel van het experimenteren met de route-instelling om prestatieproblemen op te lossen, is het eerste wat er moet worden gezocht, het verschil in de tijd tussen de eerste en de laatste regel, omdat u hierdoor precies kunt bepalen hoe lang de planner heeft gewerkt.
- **XmlModel.xml**: dit bevat het model dat is ingebouwd in X++ en waarop de engine actief is. De `JobId` die wordt gebruikt in het bestand komt overeen met de `RecId`-brontabel met de taken (`ReqRouteJob` of `ProdRouteJob`). Waar u standaard naar kunt kijken in dit bestand is of de datums die zijn opgegeven in `ConstraintJobStartsAt` en `ConstraintJobEndsAt` zoals verwacht zijn, dat de `JobGoal`-eigenschap juist is ingesteld en dat de taken aan elkaar zijn gerelateerd via de `JobLink`-beperkingen.
- **XmlSlots.xml**: dit bevat alle werktijden en capaciteitsreserveringen die de engine heeft aangevraagd. De werktijden en reserveringen van de kalender worden alleen aangevraagd door de engine voor de tijdsperioden waarin deze de taken (en een extra buffer) probeert te plaatsen, dus als het bestand tijden ver in de toekomst bevat, kan dit een indicatie zijn van een probleem met de instelling. In de `ResourceProperty`-knooppunten wordt voor elke resource aangegeven aan welke resourcegroep en -capaciteiten ze zijn gekoppeld gedurende welke perioden.
- **Result.xml**: dit bevat het resultaat van de planningsuitvoering.

De traceringsfunctionaliteit kan aanzienlijke prestatieoverhead toevoegen, dus gebruik deze functie alleen op een gecontroleerde manier voor het onderzoeken van de planning van specifieke orders. Als deze tijdens een hoofdplanning wordt ingeschakeld, wordt snel de maximale grootte bereikt en wordt gestopt.

## <a name="troubleshooting-performance"></a>Problemen met prestaties oplossen

Zoals kan worden geïnterpreteerd uit alle voorgaande secties, zijn er enkele valkuilen die betrekking hebben op de instelling en het gebruik van de planningsengine. Deze kunnen leiden tot prestatieproblemen. U kunt de volgende checklijst gebruiken om dergelijke problemen op te lossen. Het is belangrijk om alle punten te bekijken, zoals het vaakst een combinatie is van meerdere factoren die leiden tot problemen.

### <a name="performing-scheduling-as-part-of-mrp-when-it-is-not-needed"></a>Een planning uitvoeren als onderdeel van MRP wanneer dit niet nodig is

Hoewel routes worden gebruikt voor de productiecontrole, zoals kostprijsberekening en rapportage, is het wellicht niet nodig om deze te overwegen tijdens MRP. In sommige gevallen is het opgeven van een standaard doorlooptijd van de productie voor het artikel voldoende voor de planning. Als u de routeplanning wilt uitschakelen, stelt u de time fence voor capaciteit in op nul. Als de planning moet worden uitgevoerd, moet de time fence van de capaciteit nauwkeurig worden ingesteld omdat het mogelijk niet nodig is om routes te overwegen voor de volledige omvang van de time fence voor behoefteplanning van de MRP.

Als de order niet is gepland tijdens MRP, moet deze in plaats daarvan worden ingepland wanneer de geplande order wordt gefiatteerd. Dit houdt in dat het proces langer duurt, dus afhankelijk van het aantal voorgestelde geplande orders dat gefiatteerd wordt gaat de prestatiewinst tijdens MRP mogelijk verloren bij het fiatteren.

### <a name="route-with-unnecessary-operations"></a>Route met onnodige bewerkingen

Bij het ontwerpen van de route bestaat de neiging om de echte wereld precies te modelleren met alle stappen die de productie doorloopt. Hoewel dit in sommige gevallen handig kan zijn, is het niet goed voor de prestaties als het model dat de engine nodig heeft om te werken, groter is (zowel wat betreft taken als beperkingen) en er meer SQL-instructies worden uitgevoerd voor het invoegen en bijwerken van de taken en capaciteitsreserveringen. Bovendien is er een downstream-effect dat de voortgang van de taken uiteindelijk moet rapporteren, wat kan worden verminderd met automatische boekingen. Als de gegevens niet worden gebruikt, zorgt dit voor onnodige belasting.

We raden u aan alleen bewerkingen te maken die strikt nodig zijn voor de planning (dit zijn doorgaans de bottleneck resources) en/of kostprijsberekening. U kunt een groot aantal kleinere afzonderlijke bewerkingen ook groeperen in één grotere bewerking die een groter deel van het proces vertegenwoordigt.

### <a name="many-applicable-resources-for-an-operation"></a>Veel van toepassing zijnde resources voor een bewerking

Het aantal toepasselijke resources voor een bewerking wordt bepaald door de resourcevereisten die zijn ingesteld op de bewerkingsrelatie. De behoefte kan gelden voor een specifieke (individuele) resource of zijn gebaseerd op het lidmaatschap van de resource van een resourcegroep of mogelijkheid.

Als er geen planning wordt uitgevoerd met behulp van eindige capaciteit en alle toepasselijke resources dezelfde kalender en efficiëntie hebben, wordt er door de planningsengine altijd dezelfde resource verzameld voor een bewerking, maar pas nadat alle toepasselijke resources zijn uitgeprobeerd om te controleren of er een 'betere' is dan de andere resources. In dat geval kan de belasting van de planning eenvoudig worden verminderd door altijd een specifieke resource aan de bewerking toe te wijzen op de route-ontwerptijd.

### <a name="route-with-parallel-operations"></a>Route met parallelle bewerkingen

Hoewel parallelle bewerkingen (primair/secundair) een krachtig hulpmiddel zijn om scenario's te maken zoals wanneer een machine en een operator beide nodig zijn om een bepaalde taak uit te voeren, is dit ook de bron van een groot aantal prestatieproblemen. Als een behoefte aan een bepaalde afzonderlijke resource is toegewezen aan de primaire en secundaire bewerking, is dit doorgaans geen probleem. Als er echter veel mogelijke resources zijn voor elk van de bewerkingen, voegt deze een aanzienlijke berekeningscomplexiteit toe aan de planning.

Een alternatief voor het gebruik van parallelle bewerkingen is om de paren als 'virtuele' resources (die het team weergeven dat altijd samen voor de bewerking komt) te modelleren of om een van de bewerkingen alleen te modelleren als deze geen bottleneck vormt.

### <a name="route-with-quantity-of-resources-higher-than-1"></a>Route met hoeveelheid resources van meer dan 1

Als de hoeveelheid resources die nodig zijn voor een hogere bewerking wordt ingesteld op meer dan één, resulteert deze in effectief dezelfde manier als bij het gebruik van primaire/secundaire bewerkingen, omdat er meerdere parallelle taken naar de engine worden verzonden. Voor dit geval is er echter geen optie voor het gebruik van specifieke resourcetoewijzingen, omdat voor een hoeveelheid die groter is dan één resource, meer dan één resource van toepassing is voor de bewerking.

### <a name="excessive-use-of-finite-capacity"></a>Buitensporig gebruik van eindige capaciteit

Het gebruik van eindige capaciteit vereist dat de engine de capaciteitsgegevens uit een database laadt en een berekeningsoverhead kan hebben omdat het moeilijker is om een oplossing te vinden vooral in omgevingen waarin de resources worden geboekt met de maximale capaciteit. Daarom is het belangrijk om nauwkeurig te beoordelen of een bron echt een eindige capaciteit nodig heeft of dat deze daadwerkelijk kan worden geboekt. Omdat er mogelijk verschil is tussen resources met een beperkte capaciteit en belangrijk dat deze niet overboekt zijn, kunt u het beste de bottleneck-optie voor een resource gebruiken in combinatie met een aparte waarde voor het plan in 'Time fence capaciteit voor bottleneck resources'. Met het bottleneck-concept kan de time fence van de algemene eindige capaciteit worden verlaagd.

### <a name="setting-hard-links"></a>Harde koppelingen instellen

Het standaardkoppelingstype van de route is *zacht*, wat betekent dat een tijdshiaat is toegestaan tussen de eindtijd van de ene bewerking en het begin van de volgende. Dit kan een vervelend effect hebben dat, als materialen of capaciteit niet erg lang beschikbaar zijn voor een van de bewerkingen, de productie mogelijk een behoorlijke tijd inactief kan zijn, waardoor de hoeveelheid onderhanden werk toeneemt. Dit gebeurt niet met harde koppelingen, omdat het einde en begin perfect moeten zijn afgestemd. Als u echter harde koppelingen instelt, is het planningsprobleem lastiger omdat de kruisingen voor werktijden en capaciteit moeten worden berekend voor de twee resources van de bewerkingen. Als er ook parallelle bewerkingen zijn, wordt er een aanzienlijke tijd toegevoegd. Als de resources van de twee bewerkingen verschillende kalenders hebben die helemaal niet overlappen, is het probleem onoplosbaar.

Het is raadzaam om harde koppelingen alleen te gebruiken wanneer dat strikt noodzakelijk is en zorgvuldig te bedenken of het nodig is voor elke bewerking van de route.

Om het werk in uitvoering te verminderen zonder harde koppelingen toe te passen, is het een truc om de order tweemaal te plannen met een wijziging in de tegenovergestelde richting voor de tweede fase. Als de eerste planning terugwaarts is uitgevoerd vanaf de leveringsdatum, moet de tweede voorwaarts worden uitgevoerd vanaf de geplande begindatum. Hierdoor worden de taken zo veel mogelijk gecomprimeerd, zodat het onderhanden werk wordt geminimaliseerd.

### <a name="separate-calendar-for-each-resource"></a>Afzonderlijke kalender voor elke resource

Een van de belangrijkste gegevensbronnen voor de planningsengine zijn kalendergegevens. Het laden hiervan vanuit de database kan duur zijn. Omdat kalenders worden gegenereerd op basis van sjablonen, zou het verleidelijk zijn om een kalender te genereren voor elke resource en vervolgens de informatie in deze kalender aan te passen wanneer de resource downtime en andere problemen heeft. Hierdoor wordt de mogelijkheid van de engine om kalendergegevens in de cache op te slaan echter ernstig beperkt, omdat het daarom nodig is om voor elke bron nieuwe gegevens aan te vragen. Dit kan tot ernstige prestatieproblemen leiden. In plaats daarvan kunt u het beste de kalenders zo veel mogelijk opnieuw gebruiken tussen de resources en vervolgens downtimewijzigingen regelen door een andere kalender-id voor een periode toe te wijzen.

### <a name="high-number-of-working-time-slots-per-calendar-day"></a>Groot aantal werktijdvakken per kalenderdag

Omdat de engine werkt door tijdvakken één voor één te onderzoeken op capaciteit, is het handig om het aantal tijdvakken per kalenderdag te beperken. U kunt dit bijvoorbeeld doen door rekening te houden met het feit of het volgens de planning belangrijk is dat werknemers elk uur een pauze van 5 minuten nemen.

### <a name="large-or-none-scheduling-timeouts"></a>Grote (of geen) planningstime-outs

U kunt de prestaties van de planningsengine optimaliseren met behulp van parameters op de pagina **Planningsparameters**. De instellingen **Planningstime-out ingeschakeld** en **Planningsoptimalisatie ingeschakeld** moeten altijd zijn ingesteld op **Ja**. Als de waarde is ingesteld op **Nee**, kan de planning mogelijk oneindig worden uitgevoerd als er een niet-bruikbare route met veel opties is gemaakt.

De waarde voor **Maximale planningstijd per reeks** bepaalt hoeveel seconden kunnen worden besteed aan het zoeken naar een oplossing voor één reeks (in de meeste gevallen komt een reeks overeen met een enkele order). De waarde die u hier kunt gebruiken, is afhankelijk van de complexiteit van de route en de instellingen, zoals een eindige capaciteit, maar ongeveer 30 seconden is een goed uitgangspunt.

De waarde voor **Time-out optimalisatiepogingen** bepaalt hoeveel seconden maximaal kunnen worden gebruikt om een betere oplossing te vinden dan de versie die oorspronkelijk is gevonden. Dit heeft alleen invloed op routes die parallelle bewerkingen gebruiken, aangezien deze moeten worden gebruikt om verschillende combinaties te testen.

> [!NOTE]
> De waarden die voor de time-outs zijn ingesteld, worden toegepast voor het plannen van vrijgegeven productieorders en van geplande orders als onderdeel van MRP. Hierdoor kan het instellen van zeer hoge waarden leiden tot een aanzienlijke toename van de uitvoeringstijd van MRP wanneer deze wordt uitgevoerd voor een plan met veel geplande productieorders.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]