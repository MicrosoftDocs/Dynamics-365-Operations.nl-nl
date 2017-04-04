---
title: Routes en bewerkingen
description: Dit onderwerp biedt informatie over routes en bewerkingen. Een route bepaalt het proces voor het produceren van een product of de productvariant. Hierin wordt elke stap (bewerking) in het productieproces en de volgorde waarin deze stappen moeten worden uitgevoerd. Voor elke stap bepaalt de route ook vereist de bronnen voor bedrijfsactiviteiten, de vereiste insteltijd en uitvoeringstijd, en hoe de kosten moet worden berekend.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Routes en bewerkingen

Dit onderwerp biedt informatie over routes en bewerkingen. Een route bepaalt het proces voor het produceren van een product of de productvariant. Hierin wordt elke stap (bewerking) in het productieproces en de volgorde waarin deze stappen moeten worden uitgevoerd. Voor elke stap bepaalt de route ook vereist de bronnen voor bedrijfsactiviteiten, de vereiste insteltijd en uitvoeringstijd, en hoe de kosten moet worden berekend.

<a name="overview"></a>Overzicht
--------

Een route geeft de volgorde van bewerkingen die nodig is om te kunnen produceren van een product of de productvariant. De route bepaalt ook de bronnen voor bedrijfsactiviteiten die vereist zijn, de tijd die nodig is om te kunnen instellen en uitvoeren van de bewerking en hoe de kosten moet worden berekend voor elke bewerking. U kunt dezelfde route meerdere producten produceren of kunt u een unieke route voor elk product of de productvariant definiëren. U kunt zelfs meerdere routes voor hetzelfde product hebben. In dit geval wordt is de route die wordt gebruikt afhankelijk van factoren zoals de hoeveelheid die moet worden geproduceerd. De definitie van een route in Microsoft Dynamics 365 voor bedrijfsactiviteiten bestaat uit vier afzonderlijke elementen die samen het productieproces wordt beschreven:

-   **Route** : een route bepaalt de structuur van het productieproces. Met andere woorden, definieert deze de volgorde van bewerkingen.
-   **Bewerking** : een bewerking identificeert een benoemde stap in een route, zoals **Assembly**. Dezelfde bewerking kan optreden in meerdere routes en verschillende bewerkingsnummers kan hebben.
-   **Bewerkingsrelatie** : een bewerkingsrelatie de operationele eigenschappen van een bewerking, zoals de insteltijd en uitvoeringstijd, kostencategorieën, verbruik parameters en bronbehoeften definieert. De bewerkingsrelatie kan de operationele eigenschappen van een bewerking waarmee de verschillen, afhankelijk van de route die de bewerking wordt gebruikt in of de producten die zijn ontstaan.
-   **Routeversie** : een routeversie bepaalt de route die wordt gebruikt voor het produceren van een product of de productvariant. Routeversies schakelen routes worden in de hele producten gebruikt of gewijzigd na verloop van tijd. Daarmee kunt ook andere wegen moet worden gebruikt voor de productie van hetzelfde product. In dit geval wordt de route die wordt gebruikt, is afhankelijk van factoren zoals de locatie of de hoeveelheid die moet worden geproduceerd.

## <a name="routes"></a>Routes
Een route geeft de volgorde van bewerkingen die wordt gebruikt voor het produceren van een product of de productvariant. Elke bewerking is toegewezen een bewerkingsnummer en de werking van een opvolgende taak. De volgorde van bewerkingen vormt een routenetwerk, die kan worden voorgesteld door een gestuurde diagram met een of meer beginpunt en een enkele eindpunt. In Dynamics 365 voor bedrijfsactiviteiten, routes onderscheiden op basis van het type structuur. De twee soorten routes zijn eenvoudige routes en routeversies netwerken. In de parameters van productiebeheer, kunt u opgeven of alleen eenvoudige routes kunnen worden gebruikt of of de meer complexe routenetwerken kunnen worden gebruikt.

### <a name="simple-routes"></a>Eenvoudige routes

Een eenvoudige route sequentieel is en er is slechts één beginpunt voor de route.  

[![Eenvoudige route](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Als u alleen eenvoudige routes in de parameters van productiebeheer hebt ingeschakeld, genereert Dynamics 365 for Operations automatisch de bewerkingsnummers (10, 20, 30, enzovoort) wanneer u de route definiëren.

### <a name="route-networks"></a>Routenetwerken

Als u de meer complexe routenetwerken in de parameters van productiebeheer inschakelt, kunt u routes met meerdere begin punten en bewerkingen die tegelijkertijd kunnen worden uitgevoerd.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Opmerkingen:**

-   Elke bewerking kan slechts één opvolgende bewerking en de hele route moet eindigen in één bewerking.
-   Er is geen garantie die meerdere bewerkingen met dezelfde opvolgende bewerking (bijvoorbeeld bewerkingen 30 en 40 in het voorgaande voorbeeld) werkelijk gelijktijdig worden uitgevoerd. De beschikbaarheid en capaciteit van resources mogelijk beperkingen op de manier waarop bewerkingen gepland geplaatst.
-   U kunt 0 (nul) als het bewerkingsnummer gebruiken. Dit nummer is gereserveerd en wordt gebruikt om op te geven dat de laatste bewerking in de route geen bewerking opvolgende is.

### <a name="parallel-operations"></a>Parallelle bewerkingen

Soms is een combinatie van meerdere bronnen voor bedrijfsactiviteiten die verschillende kenmerken hebben vereist om een bewerking uitvoeren. Assemblage kan bijvoorbeeld een machine, een hulpmiddel en één werknemer voor elke twee andere machines voor de besteding van de bewerking nodig. In dit voorbeeld kan worden gemodelleerd met behulp van parallelle bewerkingen, waarbij één bewerking is aangewezen als de primaire bewerking en de andere secundair.  

[![Route met primaire en secundaire bewerkingen](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Doorgaans worden de primaire bewerking vertegenwoordigt de knelpuntbron en bepaalt de bewerkingstijd voor secundaire bewerkingen. Echter tijdens de planning heeft betrekking op het eindige capaciteit, de resources die zijn gepland voor zowel de primaire bewerking als de secundaire bewerkingen moeten beschikbaar en vrije capaciteit tegelijk hebben.  

Zowel de primaire bewerking en de secundaire bewerkingen moeten hetzelfde bewerkingsnummer (30 in de vorige afbeelding) hebben.  

In het voorgaande voorbeeld is de Resourcevereiste voor de primaire bewerking (30) de machine, terwijl de resourcebehoeften voor de secundaire bewerkingen (30' en 30'') het hulpprogramma en de werknemer zijn. Een belasting van 50 procent zorgt ervoor dat de geplande werknemer twee machines tegelijkertijd kunt besteding.

### <a name="approval-of-routes"></a>Goedkeuring van routes

Een route moet worden goedgekeurd voordat deze kan worden gebruikt tijdens het plannen of productie. Goedkeuring geeft aan dat het ontwerp van de route is voltooid. Dezelfde vrijgegeven product of variant vrijgegeven product kan meerdere routes die zijn goedgekeurd. Goedkeuring van een route vindt meestal plaats wanneer de eerste relevante routeversie is goedgekeurd. In sommige zakelijke zijn scenario's, de goedkeuring van de route en de routeversie afzonderlijke activiteiten waarbij verschillende eigenaars.  

Elke route kan worden goedgekeurd of niet-goedgekeurde afzonderlijk. Bedenk wel dat, als een route afgekeurd wordt, alle gerelateerde routeversies ook niet-goedgekeurde zijn. In de parameters van productiebeheer, kunt u opgeven of routes niet-goedgekeurde worden kunnen en of de goedgekeurde routes kunnen worden gewijzigd.  

Als u een logboek die records die elke route goedkeurt bijhouden moet, kunt u elektronische handtekeningen vereisen voor routegoedkeuring. Gebruikers moeten hun identiteit bevestigen met behulp van een [elektronische handtekening](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Bewerkingen
Een bewerking is een stap in het productieproces. In Dynamics 365 voor bewerkingen, wordt elke bewerking heeft een ID en een eenvoudige omschrijving. De volgende tabellen staan gangbare voorbeelden van bewerkingen van een machine shop.

| Bewerking  | Omschrijving        |
|------------|--------------------|
| PipeCut    | Pijplijnclient snijden       |
| TIGweld    | TIG lassen        |
| JigAssy    | Jig-assembly       |
| Inspectie | Kwaliteitsinspectie |

De operationele eigenschappen van de bewerking, zoals de insteltijd en uitvoeringstijd resourcebehoeften, informatie over kostprijsberekening en verbruik berekenen worden opgegeven voor de bewerkingsrelatie. (Zie de volgende sectie voor meer informatie over bewerkingsrelaties.)

## <a name="operation-relations"></a>Bewerkingsrelaties
De volgende operationele eigenschappen van een bewerking worden op de bewerkingsrelatie beheerd:

-   Kostencategorieën
-   Parameters voor verbruik
-   Verwerkingstijden
-   Verwerking van hoeveelheden
-   Resourcevereisten
-   Notities en instructies

U kunt meerdere bewerkingsrelaties voor dezelfde bewerking definiëren. Echter elke bewerkingsrelatie is specifiek voor één bewerking en eigenschappen die specifiek zijn voor een route, een vrijgegeven product of een reeks vrijgegeven producten die zijn gerelateerd aan een groep voor artikelen worden opgeslagen. Daarom kan dezelfde bewerking worden gebruikt in meerdere routes die andere operationele eigenschappen hebben. Bovendien kunt u uw belangrijkste gegevens gemakkelijker beheren als u standaard bewerkingen met dezelfde operationele eigenschappen, ongeacht de route die wordt gebruikt als het product dat wordt geproduceerd. De scope van de bewerkingsrelatie wordt gedefinieerd door de **artikelcode**, **artikelrelatie**, **code routeren** en **relatie routeren** eigenschappen, zoals in de volgende tabel wordt weergegeven.

| Artikelcode | Artikelrelatie         | Routecode | Routerelatie   | Bereik van de bewerkingsrelatie                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabel     | &lt;Artikel-id&gt;       | route      | &lt;Route-id&gt; | De operationele eigenschappen van een bewerking wanneer het wordt gebruikt in de route waar **routenummer**=&lt;route-ID&gt; voor de productie van het vrijgegeven product waar **artikelnummer**=&lt;artikel-ID&gt;.                                                                                                                        |
| Tabel     | &lt;Artikel-id&gt;       | Alles        |                  | De standaard operationele eigenschappen van een bewerking wanneer deze wordt gebruikt voor het vrijgegeven product te produceren waar **artikelnummer**=&lt;artikel-ID&gt;. Deze operationele eigenschappen toepassen met andere woorden, als er geen bewerkingsrelatie route specifieke voor het vrijgegeven product.                                     |
| Groep     | &lt;Groeps-ID&gt; | route      | &lt;Route-id&gt; | De operationele eigenschappen van een bewerking wanneer het wordt gebruikt in de route waar **routenummer**=&lt;route-ID&gt; voor de productie van vrijgegeven producten die gekoppeld aan de groep voor artikel zijn &lt;artikel groep-ID&gt;, tenzij er een specifieke route bewerkingsrelatie voor het vrijgegeven product.                         |
| Groep     | &lt;Groeps-ID&gt; | Alles        |                  | De standaard operationele eigenschappen van een bewerking wanneer deze wordt gebruikt voor de productie van vrijgegeven producten die gekoppeld aan de groep voor artikel zijn &lt;artikel groep-ID&gt;, tenzij een specifieke bewerking bestaat.                                                                                                  |
| Alles       |                       | route      | &lt;Route-id&gt; | De standaard operationele eigenschappen van de bewerking als het wordt gebruikt in de route waar **routenummer**=&lt;route-ID&gt;. Deze operationele eigenschappen toepassen met andere woorden, als er geen bewerkingsrelatie voor deze route die specifiek is voor een vrijgegeven product of deze groep voor artikel zijn gekoppeld. |
| Alles       |                       | Alles        |                  | De standaard operationele eigenschappen van een bewerking. Deze operationele eigenschappen van toepassing wanneer een specifiekere bewerkingsrelatie bestaat niet.                                                                                                                                                                |

U kunt ook opgeven dat een bewerkingsrelatie specifiek voor een site is. Op deze manier kunnen de operationele eigenschappen van een bewerking variëren, afhankelijk van de vestiging (dat wil zeggen, de site) waar de bewerking wordt uitgevoerd. U kunt ook verschillende operationele eigenschappen voor elke productconfiguratie voor geconfigureerde producten opgeven.  

Bewerkingsrelaties kunnen u meer flexibiliteit bij het definiëren van de routes. Bovendien vermindert de mogelijkheid te definiëren van eigenschappen voor standaarddatabase het bedrag van de hoofdgegevens die u moet beheren. Deze flexibiliteit ook betekent echter dat u moet rekening houden met de context die u wijzigt een bewerkingsrelatie in.  

**opmerking:** omdat de operationele eigenschappen worden opgeslagen in de bewerkingsrelaties per bewerking per route, alle exemplaren van dezelfde bewerking (bijvoorbeeld Assembly) hebben dezelfde insteltijd, uitvoeringstijd, resourcebehoeften, enzovoort. Als twee exemplaren van een bewerking moeten in dezelfde route plaatsvinden maar verschillende uit de uitvoeringstijden, moet u twee verschillende bewerkingen, zoals Assembly1 en Assembly2.

### <a name="modifying-product-specific-routes"></a>Productspecifieke routes wijzigen

Bij het openen van de **Route** pagina van de **vrijgegeven productdetails** pagina de routeversies weergegeven die gekoppeld aan het geselecteerde vrijgegeven product zijn worden weergegeven. In deze context wordt voor elke bewerking, geeft Dynamics 365 for Operations de operationele eigenschappen van de bewerkingsrelatie beste past bij de routeversie. Zult u zien dat de lijst met bewerkingen bevat de **artikelcode** en **code routeren** eigenschappen van de bewerkingsrelatie. Daarom kunt u bepalen welke bewerkingsrelatie wordt weergegeven.  

Op de **Route** pagina kunt u de operationele eigenschappen van de bewerking, zoals de uitvoeringstijd of de kostencategorieën wijzigen. Uw wijzigingen worden opgeslagen op de bewerkingsrelatie die specifiek is voor de route en vrijgegeven product waarnaar wordt verwezen in de huidige routeversie. Als de bewerkingsrelatie die wordt weergegeven niet specifiek zijn voor de route en het vrijgegeven product voordat uw wijzigingen worden opgeslagen, maakt het systeem een kopie van de bewerkingsrelatie. Dit exemplaar *is* specifiek zijn voor de route en vrijgegeven product. Daarom worden uw wijzigingen hebben geen invloed op andere routes of vrijgegeven producten. Om te controleren welke bewerkingsrelatie wordt gewijzigd op de **Route** pagina, bekijkt u de **artikelcode** en **code routeren** velden.  

U kunt ook handmatig maken met een bewerking die specifiek is voor een route en vrijgegeven product met behulp van de **kopiëren en bewerken van de relatie** functie.  

**opmerking:** als u een nieuwe bewerking aan een route toevoegen aan de **Route** pagina een bewerkingsrelatie is alleen gemaakt voor het huidige vrijgegeven product. Dus als de route ook gebruikt wordt voor de productie van andere vrijgegeven producten, geen bewerkingsrelatie van toepassing bij de desbetreffende vrijgegeven producten zullen bestaan en de route niet meer kan worden gebruikt bij de desbetreffende vrijgegeven producten.

### <a name="maintaining-operation-relations-per-route"></a>Bewerkingsrelaties per route beheren

Bij het openen van de **routegegevens** pagina van de **Routes** (lijstpagina), een lijst met alle bewerkingsrelaties die voor de geselecteerde route gelden wordt weergegeven. Daarom kunt u eenvoudig controleren welke operationele eigenschappen worden gebruikt voor welke producten. U kunt zowel de standaardwaarden van eigenschappen en de productspecifieke eigenschapswaarden wijzigen.  

Als u een nieuwe bewerkingsrelatie toevoegen aan de **routegegevens** pagina, de **code routeren** veld wordt automatisch ingesteld op **Route**, en de **relatie routeren** veld is ingesteld op het routenummer van de huidige route.

### <a name="maintaining-operation-relations-per-operation"></a>Bewerkingsrelaties per bewerking onderhouden

Uit de **bewerkingen** pagina kunt u openen het **bewerkingsrelaties** pagina. Op deze pagina kunt u alle bewerkingsrelaties voor een bepaalde bewerking wijzigen. U kunt zelfs bewerkingsrelaties met standaardwaarden wijzigen.  

Als uw bedrijf gebruikmaakt van standaardbewerkingen en de operationele parameters zijn hetzelfde voor alle producten en processen, de **bewerkingsrelaties** pagina bevat een handige manier voor het beheren van de operationele standaardeigenschappen van deze bewerkingen.

### <a name="applying-operation-relations"></a>Bewerkingsrelaties toepassen

In sommige gevallen moet Dynamics 365 for Operations de operationele eigenschappen zoeken voor een bewerking. Bijvoorbeeld wanneer een inkooporder wordt gemaakt, moeten de operationele eigenschappen van elke bewerking worden gekopieerd uit de bewerkingsrelaties aan de productieroute. In dergelijke situaties zoekt Dynamics 365 for Operations in de relevante bewerkingsrelaties door de meest specifieke combinatie naar de laatste specifieke combinatie.  

Wanneer Dynamics 365 voor bewerkingen zoekopdrachten naar de meest relevante bewerkingsrelatie voor een vrijgegeven product, een bewerkingsrelatie die overeenkomt met de artikel-ID van het vrijgegeven product heeft de voorkeur boven een bewerkingsrelatie dat overeenkomt met de groep voor artikel-id. Op zijn beurt heeft een bewerkingsrelatie die overeenkomt met de groeps-ID de voorkeur boven de standaard bewerkingsrelatie. De zoekopdracht wordt uitgevoerd in de volgende volgorde:

1.  **Artikelcode**=**tabel** en **artikelrelatie**=&lt;artikel-ID&gt;
2.  **Artikelcode**=**groep** en **artikelrelatie**=&lt;artikel groep-ID&gt;
3.  **Artikelcode**=**alle**
4.  **Code routeren**=**Route** en **relatie routeren**=&lt;route-ID&gt;
5.  **Code routeren**=**alle**
6.  **Configuratie**=&lt;configuratie-ID&gt;
7.  **Configuration**=
8.  **Locatie**=&lt;opslagruimte-ID&gt;
9.  **Site**=

Een bewerking moet daarom slechts één keer voor elke route gebruikt. De bewerking plaatsvindt meerdere keren in dezelfde route, alle exemplaren van die bewerking heeft dezelfde bewerkingsrelatie als u niet mogelijk andere eigenschappen (bijvoorbeeld uitvoeringstijden) hebben elk exemplaar.

## <a name="route-versions"></a>Routeversies
Routeversies worden gebruikt voor variaties in de productie van producten of hebben meer controle over het productieproces. Ze bepalen welke route moet worden gebruikt wanneer een bepaalde product vrijgegeven of variant vrijgegeven product wordt geproduceerd. Om te bepalen welke route wordt gebruikt voor een vrijgegeven product kunt u de volgende beperkingen:

-   Productdimensies (grootte, kleur, stijl of configuratie)
-   Productiehoeveelheid
-   Productielocatie
-   Productiedatum

Wanneer u bij het produceren van het product op een bepaalde locatie, in een specifieke hoeveelheid of in een bepaalde periode, kunt u een specifieke routeversie aanwijzen als de standaardversie van de route. Bedenk wel dat slechts één actieve route is toegestaan voor een bepaalde vrijgegeven product en een bepaalde set beperkingen.  

U kunt in de parameters van productiebeheer vereisen dat altijd de geldigheidsperiode van een routeversie worden opgegeven.

### <a name="approval-of-route-versions"></a>Goedkeuring van routeversies

Voordat u een routeversie kan worden gebruikt in de plannings- of productieproces, moet worden goedgekeurd. Wanneer u een routeversie goedkeurt, kunt u ook de gerelateerde route goedkeuren. Let er wel een routeversie kan worden goedgekeurd alleen als de gerelateerde route ook is goedgekeurd.

### <a name="activating-the-default-route-version"></a>De standaard routeversie activeren

Wanneer u een routeversie activeren, toewijzen u deze zoals de standaardversie van de route die de hoofdplanning wordt gebruikt en die worden gebruikt om productieorders te maken. U kunt slechts één actieve routeversie voor een bepaalde set beperkingen (bijvoorbeeld periode, locatie of hoeveelheid) hebben. Als de versie die u probeert te activeren is strijdig met een versie die al actief is, ontvangt u een foutbericht weergegeven. Als u wilt voorkomen dat een niet-eenduidige activering, moet u deze vervolgens de conflicterende versie deactiveren of de beperkingen (doorgaans de periode) op de routeversie te wijzigen.

### <a name="electronic-signatures"></a>Elektronische handtekeningen

Als u een logboek die records die u goedkeurt en elke routeversie activeert bijhouden moet, kunt u elektronische handtekeningen vereisen voor deze taken. Gebruikers die het goedkeuren en activeren van routeversies moeten hun identiteit bevestigen met behulp van een [elektronische handtekening](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Wijziging van het product dat gebruik van aanvraagbeheer

Het product wijzigen voor de goedkeuring en activering van nieuwe of gewijzigde routes en routeversies hebt u een eenvoudige manier om een overzicht van de route versie beperkingen. U kunt ook goedkeuren en activeren van alle routes die zijn gerelateerd aan een specifieke wijziging in één bewerking en de resultaten in het geval van de wijziging product vastleggen.

## <a name="maintaining-routes"></a>Routes onderhouden
Afhankelijk van uw zakelijke behoeften, kunt u mogelijk minder moeite die vereist is om te beheren van uw definities.

### <a name="making-routes-independent-of-resources"></a>Routes maken niet afhankelijk van de resources

In veel systemen moet de bron voor bedrijfsactiviteiten of resourcegroep die een bewerking moet worden uitgevoerd in de route worden opgegeven. In Dynamics 365 voor bewerkingen, kunt u echter een aantal vereisten waaraan een bron voor bedrijfsactiviteiten voldoen moet om te worden toegepast voor de bewerking definiëren. Daarom de specifieke resource voor bedrijfsactiviteiten of resourcegroep die moet worden gebruikt, hoeft te worden bepaald totdat de bewerking wordt gepland. Deze functionaliteit is vooral nuttig als er veel werknemers of machines die dezelfde bewerking kunnen uitvoeren.  

Stel, u opgeven dat een bewerking een bron voor bedrijfsactiviteiten van vereist de **Machine** type met een **Stamping** de mogelijkheid van 20 ton. De planningsengine zal lost deze vereisten aan een specifieke resource voor bedrijfsactiviteiten of resourcegroep wanneer de bewerking wordt gepland. Omdat u alleen deze vereisten in plaats van de bewerking koppelen aan een specifieke machine opgeven kunt, hebt u veel grotere flexibiliteit. Bovendien is onderhoud eenvoudiger wanneer resources worden verplaatst of nieuwe resources worden toegevoegd.  

Zie voor meer informatie over de verschillende soorten resourcevereisten en het gebruik van deze bewerkingen resourcevereisten en [Bronmogelijkheden](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Routes delen tussen locaties

Als u hetzelfde product op meer dan één productielocatie produceren en als de stappen voor het produceren van het product zijn dat hetzelfde op alle sites, kunt u vaak een gedeelde route die wordt gebruikt voor alle productielocaties te ontwerpen. Als u wilt maken van een gedeelde route, geeft u een locatie op de route zelf. U moet echter nog steeds een routeversie die de gedeelde route worden gekoppeld aan het product bij elke site maken.  

U moet tevens voor zorgen dat de resourcebehoeften voor elke bewerking in de route niet voor specifieke bewerkingen resources of resourcegroepen oproepen, maar in plaats daarvan worden uitgedrukt in termen van de kenmerken van de vereiste bronnen. De planningsengine zijn vervolgens kan de bronnen voor bedrijfsactiviteiten betreffende toewijzen uit de locatie die de productie wordt gepland op. Als er kleine verschillen in de uitvoeringstijd, of als de insteltijd voor een bepaalde bewerking locatiespecifieke is, kunt u deze informatie opgeven door een extra bewerkingsrelatie voor die site toe te voegen.  

U volledig profiteren van de voordelen van gedeelde routes, moet u ook verbruik van bronnen op de bijbehorende stuklijst (BOM) gebruiken. Wanneer u de vlag voor resourceverbruik instelt op de stuklijstregel, wordt het magazijn en locatie grondstoffen moeten worden verbruikt van afgeleid van de bron voor bedrijfsactiviteiten die de bewerking wordt gepland op. Daarom het magazijn en locatie, hoeft te worden bepaald tot de productie is gepland. Op deze manier kunt u zowel de stuklijst en de route niet afhankelijk van de fysieke locatie waar het product wordt geproduceerd.

### <a name="standard-operation-relations"></a>Standaard bewerkingsrelaties

Als uw bedrijf gebruikmaakt van gestandaardiseerde bewerkingen in de gehele productie als er weinig of geen variatie in de insteltijd, uitvoeringstijd, verbruiksberekening, de berekening van kosten en enzovoort, kan het handig in bewerkingsrelaties voor alle bewerkingen worden gemaakt. Maak geen in dit geval bewerkingsrelaties die specifiek zijn voor een route of vrijgegeven product.  

Als u ook express bronbehoeften in de vorm van vaardigheden en capaciteiten en breng uw routes site-onafhankelijke, kunt u het voortdurende onderhoud van uw bedrijfsprocessen tot een minimum te beperken.  

Wanneer u deze methode gebruikt de **bewerkingsrelaties** pagina, wordt uw primaire bestemming voor het onderhouden van uitvoeringstijden en andere eigenschappen.

### <a name="resource-specific-process-times"></a>Resource-specifieke verwerkingstijden

Als u een bron voor bedrijfsactiviteiten of resourcegroep als onderdeel van de resourcebehoeften voor een bewerking opgeeft, kunnen de toepasselijke resources werken met verschillende snelheden. De tijd die nodig is voor het verwerken van een bewerking kan dus variëren. Dit probleem wilt oplossen, kunt u de **formule** op de bewerkingsrelatie om op te geven hoe de verwerkingstijd wordt berekend. De volgende opties zijn beschikbaar:

-   **Standaard** : (standaard optie) de berekening wordt alleen de velden uit de bewerkingsrelatie en wordt de opgegeven uitvoeringstijd vermenigvuldigd met de orderhoeveelheid.
-   **Capaciteit** : de berekening omvat de **capaciteit** veld uit de bron voor bedrijfsactiviteiten. De tijd is daarom afhankelijk van de resource. De waarde die is opgegeven op de bron voor bedrijfsactiviteiten is de capaciteit per uur. Deze waarde wordt vermenigvuldigd met de orderhoeveelheid en de **Factor** waarde van de bewerkingsrelatie.
-   **Batch** : een batchcapaciteit wordt berekend met behulp van gegevens uit de bewerkingsrelatie. Het aantal batches en daarom de verwerkingstijd kan vervolgens worden berekend op basis van de orderhoeveelheid.
-   **Resourcebatch** : deze optie is eigenlijk hetzelfde als de **Batch** optie. Echter, de berekening omvat de **capaciteit Batch** veld uit de bron voor bedrijfsactiviteiten. De tijd is daarom afhankelijk van de resource.


<a name="see-also"></a>Zie ook
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


