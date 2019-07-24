---
title: Hoofdplanning instellen
description: Dit onderwerp beschrijft diverse belangrijke strategieën en parameters die worden gebruikt voor het instellen van de hoofdplanning.
author: t-benebo
manager: AnnBe
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 5dcfee8d48c274e16b07b051f8f36fd27432720c
ms.sourcegitcommit: 98894aa32150e95fb7e87f98703b266b03493362
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2019
ms.locfileid: "1718565"
---
# <a name="set-up-master-planning"></a>Hoofdplanning instellen


[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft diverse belangrijke strategieën en parameters die worden gebruikt voor het instellen van de hoofdplanning. Het bevat een overzicht van de typen plannen die worden gebruikt door de hoofdplanning en geeft aan welke planstrategie u moet gebruiken, afhankelijk van de vereisten van uw bedrijf. Verder worden de belangrijkste parameters beschreven die van invloed zijn op het plan en wordt uitgelegd hoe deze parameters invloed hebben op de voorgestelde geplande orders.

## <a name="types-of-master-plans"></a>Typen hoofdplannen

Hoofdplanning heeft twee typen plannen: statisch en dynamisch. Elk type is ontworpen voor een ander gebruik. Voor de beste prestaties raden we u aan het juiste plan voor uw scenario te gebruiken.

### <a name="static-plan"></a>Statisch plan

Het statische plan blijft ongewijzigd, ongeacht eventuele wijzigingen in vraag en aanbod, tot de volgende keer dat de hoofdplanning wordt uitgevoerd.

Het statische plan wordt gebruikt om de voorgestelde orders goed te keuren en te fiatteren. Het is een werkplan waar medewerkers zoals inkopers of productieplanners hun besluitvorming op kunnen baseren en dat ze kunnen gebruiken voor het uitvoeren van hun dagelijkse werkzaamheden.

Het statische plan ondersteunt ook opnieuw genereren. Een volledig nieuw, geoptimaliseerd plan wordt berekend telkens wanneer de hoofdplanning wordt uitgevoerd en bestaande orders die niet zijn goedgekeurd, worden verwijderd.

### <a name="dynamic-plan"></a>Dynamisch plan

Het dynamische plan begint meestal als een kopie van het statische plan, maar kan elke keer dat de hoofdgegevens worden gewijzigd, worden bijgewerkt. Bijvoorbeeld, als de gegevens worden gewijzigd, wordt een nieuwe verkooporder gemaakt.

Het dynamische plan wordt gebruikt voor ad-hoc planning. Het stelt het bedrijf in staat wijzigende ordernetwerk- en artikelbeschikbaarheid te controleren zonder het statische plan te verstoren dat andere personen gebruiken voor hun werkprocessen. Het wordt vooral gebruikt voor CTP (capable to promise). Het dynamische plan is het standaardplan wanneer nettobehoeften worden geopend vanuit orderpagina's (zoals de pagina's verkooporder, inkooporder of productieorder).

Het dynamische plan gebruikt nettowijziging. Daarom kan het een snellere uitvoering van het programma garanderen.

## <a name="strategies-for-using-master-plans"></a>Strategieën voor het gebruik van hoofdplannen

U kunt één plan of twee plannen in de hoofd planning gebruiken. De strategie die u gebruikt, is afhankelijk van uw zakelijke vereisten.

### <a name="one-plan-strategy"></a>Eén‑plansstrategie

Voor de één‑plansstrategie gebruikt u hetzelfde hoofdplan voor het statische plan en het dynamische plan. Deze strategie wordt gebruikt voor make‑to‑stockscenario's waarbij u normaal gesproken geen plan hoeft te simuleren dat aan een order voldoet.

De één‑plansstrategie wordt meestal gebruikt in de detailhandel en de distributiesector, of waar verkoopleveringsdatums worden bevestigd op basis van service level agreements (SLA's) of levertijden. Voor het plan kan controle van de leveringsdatum worden gebruikt zonder CTP.

Als u een simulatie moet doen, kan het plan opnieuw worden uitgevoerd voor de artikelen waarvoor de simulatie is vereist. De geplande orders die ordersimulaties genereren, worden meestal gefiatteerd.

### <a name="two-plan-strategy"></a>Twee‑plansstrategie

Voor de twee‑plansstrategie gebruikt u een statisch plan en een ander dynamisch plan. De twee‑plansstrategie wordt meestal gebruikt voor configure-to‑order- en make‑to‑orderscenario's waarvoor u verkoopordersimulaties moet uitvoeren en exacte leveringsdatums voor verkooporders moet berekenen, maar de berekeningen geen invloed mogen hebben op de dagelijkse werkzaamheden. Deze simulaties worden altijd uitgevoerd in het dynamische plan. De twee‑plansstrategie is bijvoorbeeld handig in de automobielindustrie en OEM-industrieën (Original Equipment Manufacturer).

Voor de twee‑planstrategie kan controle van de leveringsdatum CTP worden gebruikt. Wanneer CTP wordt gebruikt, wordt automatisch de uitvoering in het dynamische plan geactiveerd.

### <a name="setting-up-the-plans"></a>De plannen instellen

U kunt plannen maken op de pagina **Hoofdplannen** (**Hoofdplanning \> Instellingen \> Plannen \> Hoofdplannen**).

U kunt opgeven welke plannen voor het statische plan en het dynamische plan worden gebruikt door de velden **Huidige statisch hoofdplan** en **Huidig dynamisch hoofdplan** op de pagina **Parameters hoofdplanning** (**Hoofdplanning \> Instellingen \> Parameters hoofdplanning**). Als u een één‑plansstrategie wilt gebruiken, selecteert u hetzelfde plan in de velden **Huidige statische hoofdplan** en **Huidige dynamische hoofdplan**.

## <a name="types-of-planning-methods"></a>Typen planningsmethoden

Er kunnen drie berekeningsmethoden worden gebruikt om de hoofdplanning uit te voeren: opnieuw genereren en nettowijziging. Elke methode levert een ander plan op wanneer het wordt uitgevoerd.

U kunt de planningsmethode opgeven in het dialoogvenster **Hoofdplanning uitvoeren**. Als u dit dialoogvenster wilt openen, gaat u naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Hoofdplanning** of selecteert u **Uitvoeren** in het werkgebied **Hoofdplanning**.

### <a name="regeneration"></a>Opnieuw genereren

Met de planningsmethode Opnieuw genereren worden bestaande geplande orders verwijderd, tenzij deze worden gefiatteerd. Er worden nieuwe geplande orders gegenereerd op basis van alle behoeften. Opnieuw genereren is de enige planningsmethode die beschikbaar is voor statische plannen.

- Er wordt rekening gehouden met wijzigingen in het aanbod. Deze wijzigingen omvatten wijzigingen in de prognose.
- Deze methode respecteert de **Periode** behoefteplanningscode.
- Deze methode ondersteunt de functionaliteit voor productvervanging (PI).

### <a name="net-change"></a>Nettowijziging

De planningsmethode nettowijziging genereert geplande orders om de vereisten te dekken die zijn gecreëerd of gewijzigd sinds de laatste uitvoering van de hoofdplanning. Wijzigingen in het aanbod worden niet meegenomen wanneer deze methode wordt uitgevoerd. Het systeem neemt geen nieuwe voorraden in beschouwing en eerder gemaakte geplande orders worden niet verwijderd als ze niet meer nodig zijn. De planningsmethode nettowijziging wordt sneller uitgevoerd dan de methode van opnieuw genereren. Het is alleen beschikbaar voor dynamische plannen.

- Actiedatums en toekomstige datums worden echter bijgewerkt voor alle behoeften.
- Deze methode respecteert de **Periode** behoefteplanningscode niet.
- Deze methode voldoet niet aan de prognose, zelfs als deze is geselecteerd in het plan.
- Deze methode ondersteunt de functionaliteit voor productvervanging (PI) niet.

### <a name="net-change-minimized"></a>Minimale nettowijziging

De geminimaliseerde planningsmethode nettowijziging genereert geplande orders om alleen de vereisten te dekken die zijn gecreëerd of gewijzigd sinds de laatste uitvoering van de hoofdplanning. In tegenstelling tot de nettotoewijzingsmethode worden actiedatums en toekomstige datums alleen bijgewerkt voor nieuwe of gewijzigde behoeften. Deze planningsmethode is alleen beschikbaar voor dynamische plannen.

## <a name="types-of-scheduling-methods"></a>Typen planningsmethoden

Voor elk plan moet u op het sneltabblad **Algemeen** van de pagina **Hoofdplannen** (**Hoofdplanning \> Instellingen \> Plannen \> Hoofdplannen**) de planningsmethode selecteren die voor productieorders wordt gebruikt. U kunt de productie op het niveau van de bewerking en het taakniveau plannen.

### <a name="operations-scheduling"></a>Bewerkingsplanning

U kunt het plannen van bewerkingen gebruiken om een algemene schatting te geven voor de duur van het productieproces. Bij het plannen van bewerkingen worden de bewerkingen voor de productieroute niet in taken opgesplitst. Zie [Bewerkingsplanning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) voor meer informatie over bewerkingsplanning.

### <a name="job-scheduling"></a>Taakplanning

Taakplanning is een meer gedetailleerde planningsmethode, waarbij elke bewerking wordt verdeeld in de afzonderlijke taken. De taakplanning bevat informatie over de capaciteit. Deze wordt meestal gebruikt voor het plannen van afzonderlijke taken op de werkvloer voor een onmiddellijke of een korte periode. Zie [Taakplanning](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling) voor meer informatie over taakplanning.

## <a name="time-fences-in-days"></a>Time fences in dagen

Voor elk plan kunt u selecteren hoe ver in de toekomst de verschillende vereisten en andere overwegingen moeten worden berekend op basis van de hoofdplanning. De periode wordt een *time fence*genoemd. Voor de beste prestaties in de hoofdplanning raden wij aan de verschillende time fences aan te passen om aan uw zakelijke vereisten te voldoen. Voor elk plan kunt u de time fences vinden op het sneltabblad **Time fences in dagen** op de pagina **Hoofdplannen** (**Hoofdplanning \> Instellingen \> Plannen \> Hoofdplannen**).

> [!NOTE]
> De time fences geven aan hoe ver in de toekomst de verschillende vereisten en andere overwegingen worden berekend door de hoofdplanning. De time fences die zijn geselecteerd op deze pagina, overschrijven de time fences die zijn gedefinieerd in de behoefteplanningsgroep. Dit betekent dat een time fence-optie wordt ingesteld op Ja en dat het definiëren van de dagen de time fence die is gedefinieerd in de behoefteplanningsgroep zal overschrijven. Bij het instellen op Nee wordt de time fence gedefinieerd in de behoefteplanningsgroep. Als u een optie niet wilt of hoeft te gebruiken (u wilt bijvoorbeeld geen actieberichten gebruiken), stelt u deze in op **Ja**en stelt u de time fence in op **0** (nul) dagen.

### <a name="coverage"></a>Behoefteplanning

De time fence voor behoefteplanning vertegenwoordigt de planningsperiode of in hoeverre de vraag moet worden opgenomen. Met andere woorden, het geeft uw planningshorizon aan.

Door de optie **Behoefteplanning** in te stellen op **Ja** kunt u de time fence voor behoefteplanning overschrijven die voor het artikel is gedefinieerd tijdens de hoofdplanning. In dit geval geeft u hier het aantal dagen op waarvoor behoeften moeten worden gepland in de hoofdplanning. De timefence voor behoeften wordt vooruit vanaf de huidige datum berekend. Behoeften voorafgaand aan de huidige datum worden altijd verwerkt.

> [!NOTE]
> Voor de beste prestaties in de hoofdplanning raden wij aan de time fence voor behoefteplanning aan te passen aan uw planningshorizon.

### <a name="freeze"></a>Vergrendeling

De blokkering van de time fence vertegenwoordigt de periode waarin bestaande geplande orders niet worden gewijzigd wanneer een nieuwe hoofdplanning wordt uitgevoerd. De geplande orders worden geblokkeerd en er worden geen nieuwe plannen gesuggereerd.

Door de optie **Blokkeren** in te stellen op **Ja** kunt u de time fence die voor het artikel is gedefinieerd blokkeren tijdens de hoofdplanning. In dit geval geeft u hier het aantal dagen op dat planningsactiviteiten geblokkeerd moeten worden. Bedenk dat tijdens deze periode geen nieuwe geplande orders worden gemaakt en bestaande geplande orders niet kunnen worden gewijzigd.

### <a name="firming"></a>Fiattering

De time fence voor fiattering geeft de tijdsperiode aan waarin geplande orders automatisch worden omgezet in productie- en inkooporders. Dit proces wordt ook het *automatisch fiatteren van geplande orders* genoemd.

Door de optie **Fiatteren** in te stellen op **Ja** kunt u de time fence voor fiattering die voor het artikel is gedefinieerd blokkeren tijdens de hoofdplanning. In dit geval geeft u op gedurende hoeveel dagen de geplande inkooporders en geplande productieorders automatisch moeten worden gefiatteerd. De timefence voor fiattering wordt vooruit vanaf de hoofdplanningsdatum berekend. Een geplande inkooporder kan alleen automatisch worden gefiatteerd als het artikel is gekoppeld aan een leverancier.

### <a name="forecast-plan"></a>Prognoseplan

De time fence voor prognoseplannen geeft aan hoe ver in de toekomst de hoofdplanning geplande orders maakt voor artikelen met een geraamde vraag.

Door de optie **Prognoseplan** in te stellen op **Ja** kunt u de time fence voor het prognoseplan die voor het artikel is gedefinieerd tijdens de hoofdplanning overschrijven. In dit geval geeft u hier op gedurende hoeveel dagen de verkoopprognose van het prognoseplan moet worden opgenomen in de hoofdplanning.

### <a name="capacity"></a>Capaciteit

De time fence voor capaciteit geeft aan hoe ver in de toekomst de maximale capaciteit van de resources wordt beschouwd bij het plannen van orders. Met andere woorden, het plan plant de productieorders met behulp van de productieroute voor de artikelen en beschouwt de resources van de productieroute en de maximum capaciteit van elke resource.

Door de optie **Capaciteit** in te stellen op **Ja** kunt u de time fence voor capaciteit overschrijven die voor het artikel is gedefinieerd tijdens de hoofdplanning. In dit geval voert u het aantal dagen in dat de capaciteit moet worden gepland voor geplande productieorders. Voor de hoofdplanning wordt de actieve productieroute voor het artikel gebruikt en wordt terug in de tijd gepland vanaf de behoeftendatum. Als de behoeftendatum voor een geplande productieorder buiten de timefence voor de capaciteit valt, wordt de levertijd bepaald op basis van de levertijd van het artikel. De timefence voor capaciteit wordt vooruit vanaf de huidige datum berekend.

### <a name="action-message"></a>Actiebericht

In actieberichten worden wijzigingen voorgesteld die kunnen worden aangebracht in de bestaande leveringsorder om het leveringsplan te optimaliseren. Het is bijvoorbeeld mogelijk dat u orders vooruit moet boeken of moet uitstellen of dat u de orderhoeveelheden moet verhogen of verlagen.

Door de optie **Actiebericht** in te stellen op **Ja** kunt u de time fence voor het actiebericht die voor het artikel is gedefinieerd tijdens de hoofdplanning overschrijven. In dit geval geeft u hier op gedurende hoeveel dagen de hoofdplanning actieberichten voor behoeften moet genereren. De timefence voor actieberichten wordt vooruit vanaf de huidige datum berekend.

Zie [Actieberichten](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/action-messages) voor meer informatie over actieberichten.

> [!NOTE]
> De berekening van actieberichten veroorzaakt een langere uitvoeringstijd voor de hoofdplanning. Als actieberichten niet regelmatig worden geanalyseerd en toegepast (dagelijks, wekelijks, enzovoort), kunt u overwegen de berekening uit te schakelen tijdens de uitvoering van de hoofdplanning. Als u de berekening wilt uitschakelen, stelt u op de pagina **Hoofdplannen** de time fence **Actiebericht** op **0** (nul) voor het hoofdplan dat u uitvoert. Controleer ook of de instelling **Actiebericht** is uitgeschakeld voor alle behoefteplanningsgroepen.

### <a name="calculated-delays"></a>Berekende vertragingen

U kunt opgeven hoe ver in de toekomst mogelijke vertragingen in geplande orders worden gedetecteerd en gerapporteerd. Op deze manier kunt u mogelijke (vertraagde) leveringsdatums plannen.

Als een geplande order niet kan worden uitgevoerd voor de gevraagde datum, wordt deze gepland voor de vroegste datum voor de uitvoering van een transactie, op basis van doorlooptijden en beschikbaarheid van materiaal en capaciteit.

### <a name="approved-requisitions-time-fence"></a>Time fence goedgekeurde bestelaanvragen

U kunt de hoofdplanning instellen om geplande orders voor de bestelaanvraag te maken. Stel de optie **Aanvragen opnemen** in op **Ja** op het sneltabblad **Algemeen** van de pagina **Hoofdplannen**. Wanneer het doel van een goedgekeurde bestelaanvraag aanvulling is, wordt in de hoofdplanning automatisch een bijbehorende geplande order gemaakt om deze uit te voeren. De aanvullingsmethode wordt bepaald door het leveringsbeleid dat is ingesteld voor de artikelen in uw organisatie. Nadat de aanvraag tot aanvulling is gemaakt en goedgekeurd, is geen extra actie vereist van de gebruiker.

Door de optie **Time fence goedgekeurde bestelaanvragen** in te stellen op **Ja** op het sneltabblad **Time fences in dagen**, kunt u de geselecteerde time fence voor goedgekeurde bestelaanvragen overschrijven die voor het artikel is gedefinieerd tijdens de hoofdplanning. Voer in dit geval het aantal dagen in het verleden in dat de vraag uit goedgekeurde bestelaanvragen met de doelstelling aanvulling, moet worden opgenomen in de hoofdplanning. U kunt bijvoorbeeld specificeren dat alleen de openstaande, achterstallige vraag van goedgekeurde bestelaanvragen die zijn gemaakt in de afgelopen 10 dagen moet worden opgenomen en ingepland.

### <a name="sequencing"></a>Sequentiëren

Met sequentiëren kunnen geplande orders worden gerangschikt op basis van sequentiekenmerken die aan het eindproduct zijn gekoppeld. Dit wordt vaak gebruikt om productieorders voor te bereiden op verpakking. Het kan bijvoorbeeld worden gebruikt om dozen in een bepaalde volgorde in te pakken op basis van kleur en grootte.

Als u de optie **Sequentiëren** instelt op **Ja**, kunt u opgeven hoe ver in de toekomst de bewerkingen of taken moeten worden geordend. Bedenk dat hoe groter de time fence, hoe langer het duurt om de hoofdplanning uit te voeren.

### <a name="calculated-delays"></a>Berekende vertragingen

Vertragingsopties helpen garanderen dat de orders bruikbare geplande datums hebben. De volgende opties zijn beschikbaar op het sneltabblad **Berekende vertraging** van de pagina **Hoofdplannen**:

- **Zorg ervoor dat de geplande orders niet zijn gemaakt vóór de uitvoeringsdatum van de hoofdplanning**: stel deze optie in op **Ja** om te garanderen dat orders niet in het verleden kunnen worden gepland.
- **De berekende vertraging optellen bij de behoeftedatum** (onder **Geplande inkooporders**): Stel deze optie in op **Ja** om de berekende vertraging toe te voegen aan de behoeften.
- **De berekende vertraging optellen bij de behoeftedatum** (onder **Geplande productieorders**): Stel deze optie in op **Ja** om de berekende vertraging toe te voegen aan de behoeften.
- **De berekende vertraging optellen bij de behoeftedatum** (onder **Geplande transfer**): Stel deze optie in op **Ja** om de berekende vertraging toe te voegen aan de behoeften.
- **De berekende vertraging optellen bij de behoeftedatum** (onder **Geplande kanban**): Stel deze optie in op **Ja** om de berekende vertraging toe te voegen aan de behoeften.

Wanneer u de opties **De berekende vertraging optellen bij de behoefte datum** instelt op **Ja** om de vertragingen aan de behoeften toe te voegen, beschouwt het systeem de capaciteit van de resources en maakt het haalbaar geplande orders. De herberekening van de geplande orderdatums verhoogt de uitvoeringstijd voor de hoofdplanning. Stel de opties in op **Nee** als u de vertragingen niet hoeft te gebruiken.

## <a name="positive-and-negative-days"></a>Positieve en negatieve dagen

Positieve en negatieve dagen bepalen hoe de hoofdplanning geplande orders en acties voorstelt. Er worden positieve en negatieve dagen ingesteld voor de behoefteplanningsgroep van het artikel. U kunt de verschillende behoefteplanningsgroepen definiëren en de bijbehorende parameters instellen op de pagina **Behoefteplanningsgroepen** (**Hoofdplanning \> Instellingen \> Behoefteplanning \> Behoefteplanningsgroepen**).

### <a name="positive-days"></a>Positieve dagen

Positieve dagen geven aan hoe ver in de toekomst de hoofdplanning de huidige voorraad of ontvangsten in beschouwt als voldoende om aan een toekomstige vraag te voldoen. Als de positieve dagen bijvoorbeeld zijn ingesteld op **100**, kan de huidige voorraad worden gebruikt om te voldoen aan de vraag in de komende 100 dagen. Als er een order is op 150 dagen vanaf de huidige datum, wordt door de hoofdplanning een geplande order gemaakt om aan die vraag te voldoen, zelfs als de voorhanden voorraad voor het artikel kan voldoen aan de order. Voor artikelen met een korte doorlooptijd wilt u mogelijk de voorhanden voorraad niet gebruiken voor een order die ver in de toekomst ligt. In het geval van snelle doorlooptijd is de huidige voorhanden voorraad snel verdwenen en kunnen er in de toekomst meer orders worden geplaatst om op tijd te voldoen aan een toekomstige vraag. Dit kan mogelijk worden veroorzaakt door de korte doorloop tijd van het artikel.

De positieve dagen hebben ook invloed op de actieberichten. Het systeem kan bijvoorbeeld aanbevelen een geplande inkooporder te vergroten zodat deze een vraag bevat die binnen het aantal positieve dagen in de toekomst valt. Als de positieve dagen zijn ingesteld op **100** en als er vraag is voor een artikel binnen 30 dagen vanaf de huidige datum, wordt er door het systeem een geplande order gemaakt om aan die vraag te voldoen. Als er binnen 90 dagen na de huidige datum vraag naar hetzelfde artikel is, wordt u aangeraden de hoeveelheid van de order voor 30 dagen vanaf de huidige datum te verhogen, zodat de order de vraag ook binnen 90 dagen omvat. Als er echter een vraag naar het artikel is voor over 150 dagen vanaf de huidige datum, zal het systeem niet aanraden om de hoeveelheid van de order die al is gepland te verhogen. In plaats daarvan wordt er een nieuwe geplande order gemaakt.

In de regel worden de positieve dagen ingesteld op een getal tussen de langste doorlooptijd van de artikelen en de time fence van de behoefteplanning. Het is raadzaam artikelen die regelmatig worden aangeschaft of geproduceerd toe te wijzen aan een behoefteplanningsgroep waarin de positieve dagen gelijk zijn aan de doorlooptijd van het artikel.

### <a name="negative-days"></a>Negatieve dagen

Negatieve dagen geven aan tot wanneer artikelontvangst wordt toegestaan. Ze geven het aantal dagen aan dat u bereid bent om te wachten voordat u nieuwe aanvulling bestelt wanneer u negatieve voorraad of niet voldoende voorraad hebt. Negatieve dagen beantwoorden de vraag: Moeten we een nieuwe inkooporder voor het artikel maken of moeten we een bestaande inkoop gebruiken, zelfs als we weten dat het artikel te laat zal zijn?

Stel dat u een verkooporder hebt voor een artikel voor 15 dagen vanaf de huidige datum. U hebt ook een inkooporder voor hetzelfde artikel. Deze inkooporder zal worden ontvangen binnen 20 dagen na de huidige datum. Wilt u dat er een inkooporder voor die verkooporder wordt gemaakt of wilt u de bestaande order gebruiken, ook als u de verkooporder niet op tijd kunt uitvoeren? Als de negatieve dagen zijn ingesteld op minder dan **5** om aan te geven dat het artikel maximaal vijf dagen mag zijn vertraagd, wordt er een nieuwe geplande inkooporder gemaakt om aan de verkooporder te voldoen. Als de negatieve dagen op hoger dan **5** zijn ingesteld, wordt de bestaande order voor het artikel gebruikt.

De negatieve dagen beïnvloeden ook de prestaties van de hoofdplanning. Als de negatieve dagen op een hoog aantal zijn ingesteld, worden er veel actieberichten gegenereerd.

We raden u aan om de negatieve dagen in te stellen op een waarde die kleiner is dan de doorlooptijd van het artikel.

### <a name="dynamic-negative-days"></a>Dynamische negatieve dagen

Dynamische negatieve dagen beschouwen de doorlooptijd van het artikel en de negatieve dagen die u hebt opgegeven. Er wordt een nieuwe geplande inkooporder gemaakt op basis van de time fence voor negatieve dagen die met behulp van de volgende formule wordt berekend:

Doorlooptijd + negatieve dagen + datum van vandaag – datum nodig

Het systeem gebruikt alleen de geplande orders die binnen deze time fence vallen en er wordt een nieuwe geplande order daarbuiten gemaakt. Het voordeel van dynamische negatieve dagen is dat het de individuele productdoorlooptijd omvat, om bestaande orders opnieuw te gebruiken en te voorkomen dat nieuwe geplande orders worden gemaakt die eindigen op een latere dag, vanwege vertragingen die worden veroorzaakt door de doorlooptijd. 

Zie [Negatieve dagen en dynamische negatieve dagen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/more-about-dynamic-negative-days) voor meer informatie.
