---
title: Routes en bewerkingen
description: In dit onderwerp vindt u informatie over routes en bewerkingen. Een route definieert het proces voor het produceren van een product of de productvariant. Hierin wordt elke stap (bewerking) in het productieproces beschreven, plus de volgorde waarin deze stappen moeten worden uitgevoerd. Voor elke stap definieert de route ook de vereiste bronnen voor bedrijfsactiviteiten, de vereiste insteltijd en uitvoeringstijd en hoe de kosten moet worden berekend.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 017985645e0f77e7f269fce2932c0ec0f6eaaa1c
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="routes-and-operations"></a>Routes en bewerkingen

[!include[banner](../includes/banner.md)]


In dit onderwerp vindt u informatie over routes en bewerkingen. Een route definieert het proces voor het produceren van een product of de productvariant. Hierin wordt elke stap (bewerking) in het productieproces beschreven, plus de volgorde waarin deze stappen moeten worden uitgevoerd. Voor elke stap definieert de route ook de vereiste bronnen voor bedrijfsactiviteiten, de vereiste insteltijd en uitvoeringstijd en hoe de kosten moet worden berekend.

<a name="overview"></a>Overzicht
--------

Met een route wordt de volgorde van bewerkingen beschreven die nodig is om een product of de productvariant te produceren. Voor elke bewerking definieert de route ook de bronnen voor bedrijfsactiviteiten die vereist zijn, de tijd die nodig is om de bewerking in te stellen en uit te voeren en hoe de kosten moet worden berekend. U kunt met één en dezelfde route meerdere producten produceren of kunt u een unieke route definiëren voor elk product of productvariant. U kunt zelfs meerdere routes voor hetzelfde product hebben. In dit geval kunnen verschillende routes worden gebruikt, afhankelijk van factoren zoals de hoeveelheid die moet worden geproduceerd. De definitie van een route in Microsoft Dynamics 365 for Finance and Operations bestaat uit vier afzonderlijke elementen die samen het productieproces beschrijven:

-   **Route:** Een route definieert de structuur van het productieproces. Met andere woorden, de route definieert de volgorde van bewerkingen.
-   **Bewerking:** Een bewerking identificeert een benoemde stap in een route, zoals **Montage**. Dezelfde bewerking kan voorkomen in meerdere routes en verschillende bewerkingsnummers hebben.
-   **Bewerkingsrelatie:** Een bewerkingsrelatie definieert de operationele eigenschappen van een bewerking, zoals de insteltijd en uitvoeringstijd, kostencategorieën, verbruiksparameters en resourcevereisten. Dankzij de bewerkingsrelatie kunnen de operationele eigenschappen van een bewerking variëren, afhankelijk van route waarin de bewerking wordt gebruikt of de producten die worden geproduceerd.
-   **Routeversie:** Een routeversie bepaalt de route die wordt gebruikt voor het produceren van een product of de productvariant. Routeversies maken het mogelijk om routes opnieuw te gebruiken voor verschillende producten of in de loop van de tijd te wijzigen. Ze maken het ook mogelijk om verschillende routes te gebruiken om één en hetzelfde product te produceren. In dit geval is de gebruikte route afhankelijk van factoren zoals de locatie of de hoeveelheid die moet worden geproduceerd.

## <a name="routes"></a>Routes
Met een route wordt de volgorde van bewerkingen beschreven die gebruikt wordt om een product of de productvariant te produceren. Aan elke bewerking wordt een bewerkingsnummer toegewezen en een volgende bewerking. De volgorde van bewerkingen vormt een routenetwerk, dat kan worden voorgesteld door een gericht diagram met een of meer beginpunten en een enkel eindpunt. In Finance and Operations wordt onderscheid gemaakt tussen routes op basis van het type structuur. De twee typen routes zijn eenvoudige routes en routenetwerken. In de parameters van Productiebeheer kunt u opgeven of alleen eenvoudige routes kunnen worden gebruikt of dat de meer complexe routenetwerken kunnen worden gebruikt.

### <a name="simple-routes"></a>Eenvoudige routes

Een eenvoudige route is sequentieel en heeft slechts één beginpunt.  

[![Eenvoudige routes](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Als u in de parameters van productiebeheer alleen eenvoudige routes hebt ingeschakeld, genereert Finance and Operations automatisch de bewerkingsnummers (10, 20, 30, enzovoort) wanneer u de route definieert.

### <a name="route-networks"></a>Routenetwerken

Als u de meer complexe routenetwerken in de parameters van productiebeheer inschakelt, kunt u routes definiëren met meerdere beginpunten en bewerkingen, die parallel kunnen worden uitgevoerd.  

[![Routenetwerk](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Opmerkingen:**

-   Elke bewerking mag slechts één opvolgende bewerking hebben en de hele route moet eindigen met één bewerking.
-   Er is geen garantie dat meerdere bewerkingen met dezelfde opvolgende bewerking (in het bovenstaande voorbeeld bijvoorbeeld bewerkingen 30 en 40) werkelijk gelijktijdig worden uitgevoerd. De beschikbaarheid en capaciteit van resources leveren mogelijk beperkingen op voor de wijze waarop bewerkingen worden gepland.
-   U kunt 0 (nul) niet gebruiken als het bewerkingsnummer. Dit nummer is gereserveerd en wordt gebruikt om op te geven dat de laatste bewerking in de route geen opvolgende bewerking heeft.

### <a name="parallel-operations"></a>Parallelle bewerkingen

Soms is een combinatie van meerdere bronnen voor bedrijfsactiviteiten met verschillende kenmerken vereist om een bewerking uit te voeren. Voor een montagebewerking kan bijvoorbeeld een machine en een stuk gereedschap vereist zijn, plus één medewerker voor elke twee machines om toezicht te houden op de bewerking. Dit voorbeeld kan worden gemodelleerd met behulp van parallelle bewerkingen, waarbij één bewerking is aangewezen als de primaire bewerking en de andere secundair zijn.  

[![Route met primaire en secundaire bewerkingen](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Doorgaans vertegenwoordigt de primaire bewerking de bottleneck resource en bepaalt de uitvoeringstijd voor de secundaire bewerkingen. Tijdens planning waarbij eindige capaciteit meespeelt, moeten echter de bronnen die zijn gepland voor zowel de primaire bewerking als de secundaire bewerkingen tegelijk beschikbaar zijn en vrije capaciteit hebben.  

Zowel de primaire bewerking als de secundaire bewerkingen moeten hetzelfde bewerkingsnummer hebben (nummer 30 in de vorige afbeelding).  

In het voorgaande voorbeeld is de resourcevereiste voor de primaire bewerking (30) de machine, terwijl de resourcevereiste voor de secundaire bewerkingen (30' en 30'') het gereedschap en de werknemer zijn. Een belasting van 50 procent zorgt ervoor dat de geplande medewerker toezicht kan houden op twee machines tegelijkertijd.

### <a name="approval-of-routes"></a>Goedkeuring van routes

Voordat een route in de planning of het productieproces kan worden gebruikt, moet deze worden goedgekeurd. Goedkeuring geeft aan dat het ontwerp van de route is afgerond. Eén en hetzelfde vrijgegeven product of productvariant kan meerdere goedgekeurde routes hebben. Doorgaans vindt goedkeuring van een route plaats wanneer de eerste relevante routeversie wordt goedgekeurd. In sommige bedrijfsscenario's zijn goedkeuring van de route en van de routeversie echter afzonderlijke activiteiten waarbij verschillende eigenaars betrokken kunnen zijn.  

Elke route kan afzonderlijk worden goedgekeurd of afgekeurd. Houd er rekening mee dat wanneer de goedkeuring van een route wordt ingetrokken, dit ook gebeurt voor alle gerelateerde routeversies. In de parameters van productiebeheer kunt u opgeven of de goedkeuring van routes kan vervallen en of de goedgekeurde routes kunnen worden gewijzigd.  

Als u een logboek moet bijhouden waarin wordt geregistreerd wie de routes goedkeurt, kunt u elektronische handtekeningen vereisen voor routegoedkeuring. Gebruikers moeten dan hun identiteit bevestigen door middel van een [elektronische handtekening](/dynamics365/unified-operations/fin-and-ops/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Operations
Een bewerking is een stap in het productieproces. In Finance and Operations heeft elke bewerking een ID en een eenvoudige beschrijving. In de volgende tabellen staan gangbare voorbeelden van bewerkingen in een machinewerkplaats.

| Bewerking  | Omschrijving        |
|------------|--------------------|
| PijpSnijden    | Pijp snijden       |
| TIGlassen    | TIG lassen        |
| JigMont    | Jig monteren       |
| Inspectie | Kwaliteitsinspectie |

De operationele eigenschappen van een bewerking, zoals de insteltijd en uitvoeringstijd, resourcevereisten, kostprijsberekeningsgegevens en verbruiksberekening, worden opgegeven in de bewerkingsrelatie. Zie het volgende onderdeel voor meer informatie over bewerkingsrelaties.

## <a name="operation-relations"></a>Bewerkingsrelaties
De volgende operationele eigenschappen van een bewerking worden op de bewerkingsrelatie onderhouden:

-   Kostencategorieën
-   Verbruiksparameters
-   Verwerkingstijden
-   Verwerkte hoeveelheden
-   Resourcevereisten
-   Notities en instructies

U kunt meerdere bewerkingsrelaties voor dezelfde bewerking definiëren. Elke bewerkingsrelatie is echter specifiek voor een bewerking. Hierin worden eigenschappen opgeslagen die specifiek zijn voor een route, een vrijgegeven product of een reeks vrijgegeven producten die zijn gerelateerd aan een artikelengroep. Daarom kan dezelfde bewerking worden gebruikt in meerdere routes die verschillende operationele eigenschappen hebben. Daarnaast kunt u uw hoofdgegevens gemakkelijker beheren als u standaardbewerkingen met dezelfde operationele eigenschappen gebruikt, ongeacht de gebruikte route en het te produceren product. Het bereik van de bewerkingsrelatie wordt gedefinieerd door de eigenschappen **Artikelcode**, **Artikelrelatie**, **Routecode** en **Routerelatie**, zoals in de volgende tabel wordt weergegeven.

| Artikelcode | Artikelrelatie         | Routecode | Routerelatie   | Bereik van de bewerkingsrelatie                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabel     | &lt;Artikel-id&gt;       | route      | &lt;Route-id&gt; | De operationele eigenschappen van een bewerking wanneer deze wordt gebruikt in de route waar **Routenummer**=&lt;route-ID&gt; voor de productie van het vrijgegeven product waar **Artikelnummer**=&lt;artikel-ID&gt;.                                                                                                                        |
| Tabel     | &lt;Artikel-id&gt;       | Alles        |                  | De standaard operationele eigenschappen van een bewerking wanneer deze wordt gebruikt voor productie van het vrijgegeven product waar **Artikelnummer**=&lt;artikel-ID&gt;. Met andere woorden, deze operationele eigenschappen zijn van toepassing als er geen routespecifieke bewerkingsrelatie bestaat voor het vrijgegeven product.                                     |
| Groep     | &lt;Artikelengroep-ID&gt; | route      | &lt;Route-id&gt; | De operationele eigenschappen van een bewerking wanneer deze wordt gebruikt in de route waar **Routenummer**=&lt;route-ID&gt; voor de productie van vrijgegeven producten die gekoppeld zijn aan artikelengroep &lt;artikelengroep-ID&gt;, tenzij er een routespecifieke bewerkingsrelatie voor het vrijgegeven product bestaat.                         |
| Groep     | &lt;Artikelengroep-ID&gt; | Alles        |                  | De standaard operationele eigenschappen van een bewerking wanneer deze wordt gebruikt voor de productie van vrijgegeven producten die gekoppeld zijn aan artikelengroep &lt;artikelengroep-ID&gt;, tenzij een meer specifieke bewerkingsrelatie bestaat.                                                                                                  |
| Alles       |                       | route      | &lt;Route-id&gt; | De standaard operationele eigenschappen van de bewerking als deze wordt gebruikt in de route waar **Routenummer**=&lt;route-ID&gt;. Met andere woorden, deze operationele eigenschappen zijn van toepassing als er geen bewerkingsrelatie voor deze route bestaat die specifiek is voor ofwel het vrijgegeven product ofwel diens gekoppelde artikelengroep. |
| Alles       |                       | Alles        |                  | De standaard operationele eigenschappen van een bewerking. Deze operationele eigenschappen zijn van toepassing wanneer een specifiekere bewerkingsrelatie niet bestaat.                                                                                                                                                                |

U kunt ook opgeven dat een bewerkingsrelatie specifiek is voor een locatie. Op deze manier kunnen de operationele eigenschappen van een bewerking variëren, afhankelijk van de vestiging (dat wil zeggen, de locatie) waar de bewerking wordt uitgevoerd. U kunt voor geconfigureerde producten ook verschillende operationele eigenschappen opgeven voor elke productconfiguratie.  

Bewerkingsrelaties geven u meer flexibiliteit bij het definiëren van uw routes. Bovendien reduceert de mogelijkheid om standaardeigenschappen te definiëren de hoeveelheid hoofdgegevens die u moet beheren. Deze flexibiliteit betekent echter ook dat u moet rekening houden met de context waarin u een bewerkingsrelatie wijzigt.  

**Opmerking:** Omdat de operationele eigenschappen worden opgeslagen in de bewerkingsrelaties per bewerking per route, hebben alle exemplaren van dezelfde bewerking (bijvoorbeeld Montage) dezelfde insteltijd, uitvoeringstijd, resourcevereisten e.d. Als twee exemplaren van een bewerking in dezelfde route moeten plaatsvinden maar verschillende uitvoeringstijden hebben, moet u twee verschillende bewerkingen maken, bijvoorbeeld Montage1 en Montage2.

### <a name="modifying-product-specific-routes"></a>Productspecifieke routes wijzigen

Bij het openen van de pagina **Route** vanuit de pagina **Vrijgegeven productdetails** worden de routeversies weergegeven die gekoppeld zijn aan het geselecteerde vrijgegeven product. In deze context geeft Finance and Operations voor elke bewerking de operationele eigenschappen weer uit de bewerkingsrelatie die het meest overeenkomt met de routeversie. Merk op dat de lijst met bewerkingen de eigenschappen **Artikelcode** en **Routecode** van de bewerkingsrelatie bevat. Zo kunt u bepalen welke bewerkingsrelatie wordt weergegeven.  

Op de pagina **Route** kunt u de operationele eigenschappen van de bewerking wijzigen, zoals de uitvoeringstijd of de kostencategorieën. Uw wijzigingen worden opgeslagen in de bewerkingsrelatie die specifiek is voor de route en het vrijgegeven product waarnaar wordt verwezen in de huidige routeversie. Als de bewerkingsrelatie die wordt weergegeven niet specifiek is voor de route en het vrijgegeven product, maakt het systeem een kopie van de bewerkingsrelatie voordat uw wijzigingen worden opgeslagen. Deze kopie *is* specifiek voor de route en het vrijgegeven product. Zo hebben uw wijzigingen geen invloed op andere routes of vrijgegeven producten. Om te controleren welke bewerkingsrelatie wordt gewijzigd op de pagina **Route**, bekijkt u de velden **Artikelcode** en **Routecode**.  

U kunt ook handmatig een bewerking maken die specifiek is voor een route en een vrijgegeven product met behulp van de functie **Relatie kopiëren en bewerken**.  

**Opmerking:** Als u een nieuwe bewerking toevoegt aan een route op de pagina **Route**, wordt alleen een bewerkingsrelatie gemaakt voor het huidige vrijgegeven product. Dus als de route ook gebruikt wordt voor de productie van andere vrijgegeven producten, bestaat er geen toepasselijke bewerkingsrelatie voor de desbetreffende vrijgegeven producten en kan de route niet meer worden gebruikt voor de desbetreffende vrijgegeven producten.

### <a name="maintaining-operation-relations-per-route"></a>Bewerkingsrelaties per route onderhouden

Bij het openen van de pagina **Routedetails** van de lijstpagina **Routes**, wordt een lijst met alle bewerkingsrelaties getoond die van toepassing zijn op de geselecteerde route. Zo kunt u eenvoudig controleren welke operationele eigenschappen worden gebruikt voor welke producten. U kunt zowel de standaardwaarden van eigenschappen als de productspecifieke eigenschapswaarden wijzigen.  

Als u een nieuwe bewerkingsrelatie toevoegen op de pagina **Routedetails**, wordt het veld **Routecode** automatisch ingesteld op **Route** en het veld **Routerelatie** wordt ingesteld op het routenummer van de huidige route.

### <a name="maintaining-operation-relations-per-operation"></a>Bewerkingsrelaties per bewerking onderhouden

Vanaf de pagina **Bewerkingen** kunt u de pagina **Bewerkingsrelaties** openen. Op deze pagina kunt u alle bewerkingsrelaties voor een bepaalde bewerking wijzigen. U kunt zelfs bewerkingsrelaties wijzigen die standaardwaarden bevatten.  

Als uw bedrijf gebruikmaakt van standaardbewerkingen en de operationele parameters hetzelfde zijn voor alle producten en processen, biedt de pagina **Bewerkingsrelaties** een handige manier voor het beheren van de operationele standaardeigenschappen van deze bewerkingen.

### <a name="applying-operation-relations"></a>Bewerkingsrelaties toepassen

In sommige gevallen moet Finance and Operations de operationele eigenschappen zoeken voor een bewerking. Wanneer bijvoorbeeld een inkooporder wordt gemaakt, moeten de operationele eigenschappen van elke bewerking worden gekopieerd van de bewerkingsrelaties naar de productieroute. In dergelijke situaties zoekt Finance and Operations de relevante bewerkingsrelaties vanaf de meest specifieke combinatie tot en met de minst specifieke combinatie.  

Wanneer Finance and Operations de meest relevante bewerkingsrelatie zoekt voor een vrijgegeven product, krijgt een bewerkingsrelatie die overeenkomt met de artikel-ID van het vrijgegeven product de voorkeur boven een bewerkingsrelatie die overeenkomt met de artikelengroep-ID. Op zijn beurt krijgt een bewerkingsrelatie die overeenkomt met de artikelengroep-ID de voorkeur boven de standaardbewerkingsrelatie. De zoekopdracht wordt in de volgende volgorde uitgevoerd:

1.  **Artikelcode**=**Tabel** en **Artikelrelatie**=&lt;artikel-ID&gt;
2.  **Artikelcode**=**Groep** en **Artikelrelatie**=&lt;artikelengroep-ID&gt;
3.  **Artikelcode**=**Alle**
4.  **Routecode**=**Route** en **Routerelatie**=&lt;route-ID&gt;
5.  **Routecode**=**Alle**
6.  **Configuratie**=&lt;configuratie-ID&gt;
7.  **Configuratie**=
8.  **Locatie**=&lt;locatie-ID&gt;
9.  **Locatie**=

Een bewerking kan daarom het beste slechts één keer voor elke route worden gebruikt. Als de bewerking meerdere keren in dezelfde route voorkomt, hebben alle exemplaren van die bewerking dezelfde bewerkingsrelatie. U kunt dan niet verschillende eigenschappen (bijvoorbeeld uitvoeringstijden) instellen voor elk exemplaar.

## <a name="route-versions"></a>Routeversies
Routeversies worden gebruikt om variaties mogelijk te maken in de productie van producten of om meer controle te hebben over het productieproces. Ze definiëren welke route moet worden gebruikt wanneer een bepaald vrijgegeven product of vrijgegeven productvariant wordt geproduceerd. Om te bepalen welke route wordt gebruikt voor een vrijgegeven product kunt u de volgende beperkingen gebruiken:

-   Productdimensies (grootte, kleur, stijl of configuratie)
-   Productiehoeveelheid
-   Productielocatie
-   Productiedatum

Wanneer u het product op een bepaalde locatie produceert, in een specifieke hoeveelheid of in een bepaalde periode, kunt u een specifieke routeversie aanwijzen als de standaardversie van de route. Bedenk wel dat slechts één actieve route is toegestaan voor een bepaald vrijgegeven product en een bepaalde reeks beperkingen.  

U kunt in de parameters van productiebeheer vereisen dat altijd de geldigheidsperiode van een routeversie moet worden opgegeven.

### <a name="approval-of-route-versions"></a>Goedkeuring van routeversies

Voordat een routeversie in de planning of het productieproces kan worden gebruikt, moet deze worden goedgekeurd. Wanneer u een routeversie goedkeurt, kunt u ook de gerelateerde route goedkeuren. Houd er rekening mee dat een routeversie alleen kan worden goedgekeurd als de gerelateerde route al is goedgekeurd.

### <a name="activating-the-default-route-version"></a>De standaardrouteversie activeren

Wanneer u een routeversie activeert, wijst u deze aan als de standaardversie van de route die de hoofdplanning gebruikt, of die wordt gebruikt om productieorders te maken. U kunt slechts één actieve routeversie hebben voor een bepaalde set beperkingen (bijvoorbeeld periode, locatie of hoeveelheid). U krijgt een foutbericht als de versie die u probeert te activeren, conflicteert met een versie die al actief is. U moet de conflicterende versie eerst deactiveren of de versiebeperkingen (meestal de periode) van de routeversie wijzigen om een dubbelzinnige activering te voorkomen.

### <a name="electronic-signatures"></a>Elektronische handtekeningen

Als u een logboek moet bijhouden waarin wordt geregistreerd wie de routeversies goedkeurt en activeert, kunt u elektronische handtekeningen voor deze taken vereisen. Gebruikers die routeversies goedkeuren en activeren, moeten dan hun identiteit bevestigen door middel van een [elektronische handtekening](/dynamics365/unified-operations/fin-and-ops/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Productwijziging door middel van casebeheer

De productwijzigingscase voor goedkeuring en activering van nieuwe of gewijzigde routes en routeversies biedt een gemakkelijke manier om een overzicht van de routeversiebeperkingen te bekijken. U kunt ook in één bewerking alle routes goedkeuren en activeren die zijn gerelateerd aan een specifieke wijziging en de resultaten in de productwijzigingscase vastleggen.

## <a name="maintaining-routes"></a>Routes onderhouden
Afhankelijk van uw bedrijfsbehoeften kunt u mogelijk het werk reduceren dat het beheer van uw procesdefinities vereist.

### <a name="making-routes-independent-of-resources"></a>Routes onafhankelijk van resources maken

In veel systemen moet de bron voor bedrijfsactiviteiten of resourcegroep die een bewerking moet uitvoeren, in de route worden opgegeven. In Finance and Operations kunt u echter een aantal vereisten definiëren waaraan een bron voor bedrijfsactiviteiten voldoen moet om in aanmerking te komen voor de bewerking. Daarom hoeft de specifieke bron voor bedrijfsactiviteiten of resourcegroep die u wilt gebruiken niet te worden bepaald totdat de bewerking wordt gepland. Deze functionaliteit is vooral nuttig als u veel werknemers of machines hebt die dezelfde bewerking kunnen uitvoeren.  

Stel dat u opgeeft dat een bewerking een bron voor bedrijfsactiviteiten vereist van het type **Machine** met een **Stempel**-vermogen van 20 ton. De planningsengine zet deze vereisten om naar een specifieke bron voor bedrijfsactiviteiten of resourcegroep wanneer de bewerking wordt gepland. Omdat u alleen deze vereisten kunt opgeven in plaats van de bewerking aan een specifieke machine te koppelen, hebt u veel grotere flexibiliteit. Bovendien is onderhoud eenvoudiger wanneer resources worden verplaatst of nieuwe resources worden toegevoegd.  

Zie voor meer informatie over de verschillende soorten resourcevereisten en hoe u deze gebruikt de onderwerpen Resourcevereisten voor bewerkingen en [Bronmogelijkheden](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Routes delen tussen locaties

Als u hetzelfde product op meer dan één productielocatie produceert en als de stappen voor het produceren van het product hetzelfde zijn op alle sites, kunt u vaak een gedeelde route opstellen die wordt gebruikt op alle productielocaties. Als u een gedeelde route wilt maken, geeft u geen locatie op in de route. U moet echter nog steeds een routeversie maken die de gedeelde route koppelt aan het product op elke site.  

U moet er ook voor zorgen dat de resourcevereisten voor elke bewerking in de route niet om specifieke bronnen voor bedrijfsactiviteiten of resourcegroepen vragen, maar in plaats daarvan worden uitgedrukt in termen van de kenmerken van de vereiste bronnen. De planningsengine kan vervolgens de juiste bronnen voor bedrijfsactiviteiten toewijzen van de site waarop de productie wordt gepland. Als er bijvoorbeeld kleine verschillen in de uitvoeringstijd bestaan, of als de insteltijd voor een bepaalde bewerking locatiespecifiek is, kunt u deze informatie opgeven door een extra bewerkingsrelatie voor die site toe te voegen.  

Om volledig te profiteren van de voordelen van gedeelde routes, moet u ook het verbruik van resources op de bijbehorende stuklijst (BOM) gebruiken. Wanneer u de vlag voor resourceverbruik instelt op de stuklijstregel, worden het magazijn en locatie waarvan de grondstoffen moeten worden verbruikt, afgeleid van de bron voor bedrijfsactiviteiten waarvoor de bewerking wordt gepland. Daarom hoeft u het magazijn en locatie pas te bepalen wanneer de productie wordt gepland. Op deze manier kunt u zowel de stuklijst als ook de route onafhankelijk maken van de fysieke locatie waar het product wordt geproduceerd.

### <a name="standard-operation-relations"></a>Standaardbewerkingsrelaties

Als uw bedrijf gebruik maakt van gestandaardiseerde bewerkingen in de gehele productie als er weinig of geen variatie bestaat in de insteltijd, uitvoeringstijd, verbruiksberekening, kostenberekening e.d., kan het handig zijn om standaardbewerkingsrelaties voor alle bewerkingen te maken. Maak in dit geval geen bewerkingsrelaties die specifiek zijn voor een route of vrijgegeven product.  

Als u ook resourcevereisten uitdrukt in termen van vaardigheden en capaciteiten en uw routes locatieonafhankelijk maakt, kan dat bijdragen aan een reductie in het doorlopende onderhoud van uw bedrijfsprocessen.  

Wanneer u deze methode gebruikt, wordt de pagina **Bewerkingsrelaties** uw primaire bestemming voor het onderhoud van uitvoeringstijden en andere eigenschappen.

### <a name="resource-specific-process-times"></a>Resourcespecifieke verwerkingstijden

Als u geen bron voor bedrijfsactiviteiten of resourcegroep opgeeft als onderdeel van de resourcevereisten voor een bewerking, kunnen de toepasselijke resources werken met verschillende snelheden. De tijd die nodig is voor het verwerken van een bewerking kan daardoor variëren. Om dit probleem op te lossen, kunt u met het veld **Formule** in de bewerkingsrelatie opgeven hoe de verwerkingstijd wordt berekend. De volgende opties zijn beschikbaar:

-   **Standaard:** De standaardoptie. De berekening gebruikt alleen de velden uit de bewerkingsrelatie en vermenigvuldigt de opgegeven uitvoeringstijd met de orderhoeveelheid.
-   **Capaciteit:** De berekening omvat het veld **Capaciteit** uit de bron voor bedrijfsactiviteiten. De tijd is daarmee afhankelijk van de resource. De waarde die is opgegeven voor de bron voor bedrijfsactiviteiten is de capaciteit per uur. Deze waarde wordt vermenigvuldigd met de orderhoeveelheid en de waarde in het veld **Factor** uit de bewerkingsrelatie.
-   **Batch:** Een batchcapaciteit wordt berekend met behulp van gegevens uit de bewerkingsrelatie. Het aantal batches en daarmee de verwerkingstijd kan vervolgens worden berekend op basis van de orderhoeveelheid.
-   **Resourcebatch:** Deze optie is eigenlijk hetzelfde als de optie **Batch**. De berekening omvat hierin echter het veld **Batchcapaciteit** uit de bron voor bedrijfsactiviteiten. De tijd is daarmee afhankelijk van de resource.


<a name="see-also"></a>Zie ook
--------

[Stuklijsten en formules](bill-of-material-bom.md)

[Kostencategorieën die in productieroutering worden gebruikt](../cost-management/cost-categories-used-production-routings.md)

[Bronmogelijkheden](resource-capabilities.md)

[Overzicht van elektronische handtekeningen](/dynamics365/unified-operations/fin-and-ops/organization-administration/electronic-signature-overview)




