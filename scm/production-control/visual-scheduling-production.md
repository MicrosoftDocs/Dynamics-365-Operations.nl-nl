---
title: Een gantt-diagram voor het plannen van taken
description: Het Gantt-diagram is ontworpen om productieplanners meer mogelijkheden te bieden om het productieplan te beheren en te optimaliseren. Het Gantt-diagram maakt de stroom van bewerkingen transparant en maakt het eenvoudig om het productieschema aan te passen waarbij rekening wordt gehouden met materiaal- of resourcetekorten. Dit helpt planningen optimaal gebruik te maken van beschikbare resources, onderhanden werk te minimaliseren en doorvoertijden voor productieorders te optimaliseren.
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: johanhoffmann
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 55631c4d588c699b9e47f73190d5b01d6da3b9ec
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="gantt-chart-for-job-scheduling"></a>Een gantt-diagram voor het plannen van taken

[!include[banner](../includes/banner.md)]


Het Gantt-diagram is ontworpen om productieplanners meer mogelijkheden te bieden om het productieplan te beheren en te optimaliseren. Het Gantt-diagram maakt de stroom van bewerkingen transparant en maakt het eenvoudig om het productieschema aan te passen waarbij rekening wordt gehouden met materiaal- of resourcetekorten. Dit helpt planningen optimaal gebruik te maken van beschikbare resources, onderhanden werk te minimaliseren en doorvoertijden voor productieorders te optimaliseren.

Het Gantt-diagram is ontworpen om productieplanners meer mogelijkheden te bieden om het productieplan te beheren en te optimaliseren. Het Gantt-diagram maakt de stroom van bewerkingen transparant en maakt het eenvoudig om het productieschema aan te passen waarbij rekening wordt gehouden met materiaal- of resourcetekorten. Dit helpt planningen optimaal gebruik te maken van beschikbare resources, onderhanden werk te minimaliseren en doorvoertijden voor productieorders te optimaliseren.

Een Gantt-diagram is een visuele weergave van geplande activiteiten binnen een gedefinieerde periode. De activiteiten worden gepland voor resources waarvoor capaciteit is gedefinieerd door een capaciteitskalender. De volgende typen activiteiten kunnen worden weergegeven in het Gantt-diagram.

-   Taken van productieorders die in taken zijn gepland.
-   Taken uit geplande productieorders.
-   In taken geplande projectactiviteiten van het type Uurprognose.

Het Gantt-diagram kan worden geopend in twee verschillende weergaven **Order** en **Bron**[.](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true)In de weergave **Order** worden activiteiten gegroepeerd onder productieorders. Dit kan bijvoorbeeld handig zijn als u een overzicht wilt bijhouden van alle taken die behoren tot dezelfde orders. In de weergave **Bron** zijn alle taken gegroepeerd onder de afzonderlijke resources. Deze weergave kan nuttig zijn bij het optimaliseren van het plan op het resourceniveau, bijvoorbeeld een machine of een groep machines. De Gantt-diagrammen in de afbeeldingen hieronder geven de weergaven **Order** en **Bron** weer met de volgende belangrijke elementen:

1.  Activiteit in Gantt-diagram
2.  Pictogram Materiaaltekort
3.  Pictogram Materiaalbeschikbaarheid
4.  Pictogram Leveringsdatum van order
5.  Capaciteitsbalk

## <a name="order-view"></a>Orderweergave

[![Orderweergave](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Bronweergave
[![Bronweergave](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Activiteiten
De activiteiten worden weergegeven als balken en worden ingedeeld in een tijdschaalraster met een geplande begin- en eindtijd, waardoor de lengte van de balken evenredig is aan de tijd die nodig is om de activiteit te voltooien. De activiteiten worden weergegeven op basis van een tijdschaal. U kunt de tijdschaal aanpassen in het menu, waar u een begindatum, einddatum en tijdseenheid selecteert, bijvoorbeeld uren of dagen. U kunt door het aanpassen van de tijdschaal de focus stellen op een tijdsinterval waarin u activiteiten wilt beheren. 

Als u een beter overzicht wilt, zijn er verschillende opties voor het instellen van de kleur van de activiteiten. U kunt een individuele kleur voor activiteiten configureren, de themakleur gebruiken die de algemene themakleur voor de toepassing is, of instellen dat de kleur wordt geregeld door de kleurcode voor productieorders. 

Het tijdsinterval voor activiteiten heeft een achtergrondkleur. Perioden met een witte achtergrond geven een tijdsinterval aan met gedefinieerde capaciteit voor de resource voor de activiteit, terwijl perioden met een grijze achtergrond tijdsintervallen aanduiden waarvoor geen capaciteit is gedefinieerd. 

Aan de linkerkant van het diagram er is extra informatie over de activiteit, bijvoorbeeld de resource waarop de activiteit is gepland en het productieordernummer. De verbinding tussen de taken die behoren tot dezelfde order wordt aangegeven met een pijl. 

U kunt meer informatie vinden over een activiteit in het dialoogvenster van de activiteit. U opent het dialoogvenster door te dubbelklikken op de activiteit of het menu **Informatie** te selecteren. In het dialoogvenster kunt u de geplande begin- en einddatum zien en tijdinformatie over de geplande materialen die de activiteit gaat verbruiken. 

De activiteiten kunnen worden gegroepeerd in groepeerniveaus. De groepeerniveaus zijn hiërarchisch en kunnen worden gebruikt voor het maken van een logische groepering van activiteiten. Als u bijvoorbeeld een indeling hebt waarin fabricageactiviteiten worden gegroepeerd op Vestiging, Productie-eenheden, Brongroepen en Resources, kunt u met de groeperingsniveaus de activiteiten groeperen in overeenstemming met die indeling. De groepeerniveaus kunnen worden uitgevouwen en samengevouwen op het afzonderlijke groepeerniveau of voor alle niveaus in het diagram door middel van de menuknoppen **Alles uitvouwen** en **Alles samenvouwen**. U kunt ook de groepeerniveaus configureren om te worden uitgevouwen of samengevouwen wanneer het diagram wordt geopend.

### <a name="material-availability"></a>Materiaalbeschikbaarheid

Het Gantt-diagram kunt u instellen om de planner te voorzien van gedetailleerde informatie over de materiaalstatus van de afzonderlijke activiteiten. Dit kan bijvoorbeeld handig zijn als materiaal vertraagd is en dit het productieplan beïnvloedt. In dit geval worden materiaalproblemen gemarkeerd in het Gantt-diagram, om de planner het helpen begrijpen wat de gevolgen zijn en de benodigde aanpassingen door te voeren. 

Een taak wordt weergegeven met een materiaaltekortpictogram als de geplande startdatum van de taak later is dan de beschikbaarheidsdatum van materialen die de taak verbruikt. De materiaalbeschikbaarheid wordt berekend op basis van de behoeftetraceringsinformatie in het dynamische hoofdplan. Het materiaaltekortpictogram verschijnt bijvoorbeeld bij een taak die materiaal verbruikt dat wordt getraceerd voor een inkooporder met een ontvangstdatum die later is dan de geplande begindatum van de taak.

### <a name="indicator-of-material-availability-date"></a>Indicator van de materiaalbeschikbaarheidsdatum

Wanneer u het diagram instelt om taken met materiaaltekorten weer te geven, kunt u ook een pictogram voor de materiaalbeschikbaarheidsdatum voor de taak laten weergeven. Het pictogram wordt alleen weergegeven als de datum van materiaalbeschikbaarheid binnen het gedefinieerde tijdsinterval van het diagram ligt. Als de datum van de materiaalbeschikbaarheid buiten het gedefinieerde tijdsinterval valt, kunt u meer gedetailleerde materiaalbeschikbaarheidsgegevens ophalen uit de materialenlijst in het taakdialoogvenster. In de lijst vindt u ook een pictogram dat materialen aanduidt die te laat worden ontvangen voor de taak. U kunt een taak opnieuw plannen met de materiaalbeschikbaarheidsdatum als begindatum.

### <a name="indicator-of-order-delivery-date"></a>Indicator van de leveringsdatum van de order

Dit pictogram geeft de leveringsdatum voor een productieorder aan. Het pictogram is alleen zichtbaar in de Orderweergave.

### <a name="capacity-bar"></a>Capaciteitsbalk

U kunt het diagram ook configureren voor weergave van een resourcecapaciteitsbalk. Deze balk geeft een overzicht van de resourcecapaciteit voor een activiteit in het gedefinieerde tijdsinterval van het diagram. De capaciteitsbalk wordt niet weergegeven voor perioden waarin de resource niet is geboekt. In perioden waarin volledige capaciteit van de resource is geboekt, wordt de capaciteitsbalk weergegeven als een ononderbroken balk. In perioden waarin de resource overboekt is, wordt de balk dikker en met een rode kleur weergegeven. Als bijvoorbeeld twee taken elkaar overlappen, geeft de capaciteitsbalk een overboeking aan in het tijdsinterval waarin de overlapping valt. De capaciteitsbalk wordt dynamisch bijgewerkt wanneer u een taak plant. U activeert de capaciteitsbalk in het menu **Capaciteitsbalk weergeven**. De balk kan alleen worden weergegeven in de **Bronweergave**. Als u een gedetailleerdere weergave van de capaciteitsbelasting van een resource wilt zien, gebruikt u het diagram **Capaciteitsbelasting**, dat kan worden geopend vanuit het menu of het contextmenu voor een geselecteerde activiteit.

## <a name="job-scheduling-in-the-gantt-chart"></a>Taken inplannen in het Gantt-diagram
Het Gantt-diagram biedt verschillende opties voor het doorvoeren van aanpassingen aan het productieplan. In het Gantt-diagram kunt u activiteiten opnieuw plannen als een interactie met slepen en neerzetten, of vanuit een planningsmenu. In het planningsproces kunt u rekening houden met resourcecapaciteit, resourcemogelijkheden en materiaalbeperkingen.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Een taak plannen als een interactie met slepen en neerzetten

U kunt een taak opnieuw plannen binnen het gedefinieerde tijdsinterval als een slepen-en-neerzetten-interactie. U kunt de taak alleen opnieuw plannen op dezelfde resource en u kunt slechts één taak tegelijk plannen.

### <a name="schedule-a-job-from-the-menu"></a>Een taak plannen vanuit het menu

In het menu **Taken plannen** kunt u een of meer geselecteerde taken in het diagram plannen op basis van een planningsrichting en een planningsdatum/-tijd. Er zijn drie verschillende planningsrichtingen.

-   Verder vanaf planningsdatum
-   Terug vanaf planningsdatum
-   Verder vanaf de beschikbaarheidsdatum van materiaal

Het is niet mogelijk om een taak te plannen buiten het gedefinieerde tijdsinterval van het Gantt-diagram. Als u dit doet, blijft de taak ongepland en u ontvangt het foutbericht "Kan taak niet plannen binnen de geladen periode."

### <a name="schedule-previous-jobs"></a>Eerdere taken plannen

In een netwerk van activiteiten, zoals taken die deel uitmaken van dezelfde productieorder, kunt u met de functie **Eerdere taken plannen** de taken plannen die worden uitgevoerd vóór een geselecteerde taak in het netwerk. In het volgende voorbeeld is de gemarkeerde activiteit de geselecteerde taak.

<table>
<tr>
<td>
Vóór
</td>
<td rowspan=2>
<img src='./media/schprevjob3.png'/>
</td>
</tr>
<tr>
<td>
Na
</td>
</tr>
</table>

### <a name="schedule-next-jobs"></a>Volgende taken plannen

U kunt met de functie **Volgende taken plannen** taken plannen die worden uitgevoerd na een geselecteerde taak in een netwerk van activiteiten. In het volgende voorbeeld is de gemarkeerde activiteit de geselecteerde taak.

<table>
<tr>
<td>
Vóór
</td>
<td rowspan=2>
<img src='./media/schnxtjob.png'/>
</td>
</tr>
<tr>
<td>
Na
</td>
</tr>
</table>

### <a name="schedule-around-job"></a>Plannen rond taak

U kunt met de functie **Plannen rond taak** een taak vóór en een taak na de geselecteerde taak plannen in een netwerk van activiteiten. In het volgende voorbeeld is de gemarkeerde activiteit de geselecteerde taak.

<table>
<tr>
<td>
Vóór
</td>
<td rowspan=2>
<img src='./media/scharoundjob1.png'/>
</td>
</tr>
<tr>
<td>
Na
</td>
</tr>
</table>

### <a name="arrange-jobs"></a>Taken rangschikken

Met de functie **Schikken** kunt u geselecteerde activiteiten schikken voor dezelfde resource. Deze activiteiten kunnen zich in hetzelfde netwerk van activiteiten bevinden, maar kunnen ook deel uitmaken van verschillende netwerken. Als u de functie Schikken gebruikt, wordt tijd tussen de geselecteerde activiteiten geschrapt. Met deze functie kunt u het gebruik van de capaciteit van de resources optimaliseren.

<table>
<tr>
<td>
Vóór
</td>
<td rowspan=2>
<img src='./media/arrangejobs1.png'/>
</td>
</tr>
<tr>
<td>
Na
</td>
</tr>
</table>

### <a name="reassign-activities-from-one-resource-to-another"></a>Activiteiten opnieuw toewijzen aan een andere resource

U kunt een taak verwijderen bij een resource en hem toewijzen aan een andere resource. Dit kan nuttig zijn in situaties waarin een machine is defect of overboekt is en u een andere beschikbare resource moet vinden die de taak kan uitvoeren.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Een activiteit opnieuw toewijzen als een slepen-en-neerzetten-interactie

In de weergave **Resource** kunt u een activiteit toewijzen aan een andere resource in het Gantt-diagram, als een slepen-en-neerzetten-interactie. U doet dit door de rij te selecteren waarin de activiteit is gepland. Als de rij is geselecteerd, kunt u de rij verslepen naar de resource in het diagram die is gegroepeerd onder een andere resourcegroepeerniveau.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Een activiteit opnieuw toewijzen in het menu Taken plannen

U kunt een taak opnieuw toewijzen in het dialoogvenster **Taken plannen** dat u kunt openen vanuit het menu **Taken plannen**. In dit menu kunt u alleen een taak opnieuw toewijzen aan een resource die al is geladen in het Gantt-diagram. Als u slechts één taak selecteert, wordt de vervolgkeuzelijst voor de resource gesorteerd op toepasselijke resources. Als u meerdere taken selecteert, is geen informatie over toepasselijke resources beschikbaar in de lijst met resources.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Extra resources in het Gantt-diagram laden
In de weergave **Bron** hebt u een optie om extra resources te laden in het Gantt-diagram. Dit kan nuttig zijn als u wilt zoeken naar een alternatieve resource voor een taak die is gepland op een machine die overboekt of defect is. Op de pagina **Extra resources laden** ziet u een lijst met resources die beschikbaar zijn vanaf de datum waarop de lijst wordt geopend. Resources die geschikt zijn voor een geselecteerde taak in het Gantt-diagram, worden als eerste vermeld. Als u meerdere taken hebt geselecteerd voordat u de lijst opent, wordt geen indicatie voor toepasselijke resources weergegeven. Op de pagina **Extra resources laden** kunt u een of meer resources selecteren die in het Gantt-diagram worden geladen wanneer u uw selectie bevestigt. Als geen taken zijn gepland voor de geselecteerde resource in de tijdsperiode van het Gantt-diagram, wordt de resource geplaatst onder een resourcegroepeerniveau onderaan de lijst met activiteiten in het Gantt-diagram.

### <a name="access-the-gantt-chart"></a>Het Gantt-diagram openen

U kunt het Gantt-diagram openen vanaf de volgende pagina's.

| **Pagina**                                                                                     | **Beschrijving**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Productieorderlijst en details**                                                         | Op de pagina **Productieorderlijst en details** kunt u het Gantt-diagram openen vanuit een of meer geselecteerde orders. Als u het diagram opent vanuit het menu-item **Gantt-diagram**, worden alle taken geladen die zijn gekoppeld aan de geselecteerde productieorders, maar ook taken uit andere productieorders die voor dezelfde resources zijn gepland. Als u het diagram opent vanuit het menu-item **Gantt-diagram - snelle weergave**, worden alleen taken geladen die zijn gekoppeld aan de geselecteerde productieorders. In deze weergave is het niet mogelijk om taken te plannen. |
| **Resource**                                                                                 | Op de pagina **Resource** kunt u het Gantt-diagram openen vanuit het menu-item **Gantt-diagram**. Wanneer dit is geselecteerd, worden alle taken die zijn gepland voor de resource in een geselecteerd tijdsinterval in het diagram geladen.                                                                                                                                                                                                                                                                                                   |
| **Resourcegroep**                                                                           | Op de pagina **Resourcegroep** kunt u het Gantt-diagram openen vanuit het menu-item **Gantt-diagram**. Wanneer dit is geselecteerd, worden alle taken die zijn gepland voor de resources in de resourcegroep weergegeven in een geselecteerd tijdsinterval.                                                                                                                                                                                                                                                                                    |
| **Gantt-diagrammen**                                                                             | Op de pagina **Gantt-diagrammen** kunt u Gantt-diagrammen configureren op resources en resourcegroepen. Als u bijvoorbeeld productieactiviteiten voor bepaalde reeksen resources of resourcegroepen wilt aansturen, kunt u afzonderlijke configuraties daarvan maken op de pagina **Gantt-diagrammen**. U kunt vervolgens het Gantt-diagram openen vanuit elke configuratie.                                                                                                                                                    |
| **Uurprognoses** (project)                                                                 | Projectactiviteiten van het type **Uurprognose** kunnen in taken worden gepland voor resources. Op de pagina **Uurprognose** in het menu **Planning** kunt u het Gantt-diagram voor een order openen, om in taken geplande projectactiviteiten van het type Uurprognose te bekijken.                                                                                                                                                                                                                                                             |
| **Te voltooien taak** (lijst in het werkgebied **Productiebeheer**)                      | De lijst **Te voltooien taken** in het werkgebied Productiebeheer toont taken uit productie- en batchorders die worden uitgevoerd met de geselecteerde resources voor het werkgebied. Met het menu-item **Gantt-diagram** kunt u het Gantt-diagram openen, waarmee alle taken die zijn geselecteerd in de lijst worden geladen in het diagram.                                                                                                                                                                                |
| **Vrij te geven productieorders** (geopend vanuit het werkgebied **Productiebeheer**) | De pagina Vrij te geven productieorders wordt geopend vanuit het werkgebied **Productiebeheer**. Deze pagina geeft geplande productie- en batchorders weer die wachten om te worden vrijgegeven. Op deze pagina kunt u het Gantt-diagram voor geselecteerde productieorders openen.                                                                                                                                                                                                                                                        |




