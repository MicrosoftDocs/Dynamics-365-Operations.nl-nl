---
title: Structuren voor werkspecificatie
description: "Een structuur voor werkspecificatie (WBS) is een omschrijving van de werkzaamheden die voor een project worden uitgevoerd. Dit is een hiërarchie van taken die het projectteam inzicht geeft in de samenstelling van de werkzaamheden, de grootte, kosten en de duur van elke component of taak."
author: KimANelson
manager: AnnBe
ms.date: 06/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8bc3d23fac6112622e722e57b61fdb686f5a98ed
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="work-breakdown-structures"></a>Structuren voor werkspecificatie

[!INCLUDE [banner](../includes/banner.md)]

Een structuur voor werkspecificatie (WBS) is een omschrijving van de werkzaamheden die voor een project worden uitgevoerd. Dit is een hiërarchie van taken die het projectteam inzicht geeft in de samenstelling van de werkzaamheden, de grootte, kosten en de duur van elke component of taak. Een WBS heeft drie belangrijke doeleinden:

-   Een analyse of de samenstelling van het werk in taken.
-   Plannen van de projectwerkzaamheden.
-   Schatting maken van de kosten van elke taak.

De mate van detail in een WBS is afhankelijk van het niveau van nauwkeurigheid dat is vereist in ramingen en het niveau van tracering dat is vereist voor die ramingen. Projecten met een zeer lage tolerantie voor vertragingen in planning of overschrijding van kosten vereisen gewoonlijk een gedetailleerdere WBS en dat de werkvoortgang en kosten nauwgezet worden bijgehouden met betrekking tot de werkspecificatiestructuur. Dit type project is normaal in de bouw- en engineeringsector. 

Daarentegen zijn de projecten in bedrijfstakken zoals media en reclame, software en IT-infrastructuur van één type , en de productiviteit is gekoppeld aan de ervaring en competentie van de persoon die de taak uitvoert. Deze bedrijfstakken gebruiken daarom een WBS om een schatting te krijgen van de grootte van een project, en niet om in detail de voortgang van het project bij te houden. 

Het samenstellen van een WBS is een intensief proces dat doorgaans over een lange periode wordt uitgevoerd, en dat samenwerking en informatie van een grote verscheidenheid aan mensen vereist. Dit onderwerp beschrijft hoe u WBS-verbeteringen in Microsoft Dynamics 365 for Finance and Operations kunt gebruiken om aan uw vereisten te voldoen voor ramingen en tracering.

## <a name="prerequisites-for-creating-a-wbs"></a>Vereisten voor het maken van een WBS
Om een WBS te maken moet u een werkplanning kunnen maken en de kosten van het werk schatten.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Vereisten voor het maken van een werkplanning

Om alle planningsmogelijkheden van de WBS-functies volledig te benutten, voert u de volgende instellingen uit:

1.  Stel een standaardkalender en een projectkalender in:
    1.  Klik op **Projectbeheer en boekhouding** &gt; **Instellingen** &gt; **Projectbeheer- en boekhoudingsparameters** &gt; **Planning**. Geef een standaardwerkkalender op in het veld **Standaardwerkkalender**. Dit wordt de standaardwerkkalender voor elk nieuw project dat wordt gemaakt.
    2.  U kunt de standaardkalender wijzigen voor een bepaald project. Klik op de detailpagina van het project, klik vervolgens op het sneltabblad **Projectteam en planning** en werk het veld **Planningskalender** bij door een andere kalender te selecteren.

2.  Stel standaardwerkdagen en -werkuren in. De kalender die instelt als werkkalender voor uw project wordt in WBS gebruikt om de volgende informatie te bepalen:

-   Werkdagen en vakanties
-   Het aantal werkuren in een dag

Om de werkdagen en de werkuren voor een kalender in te stellen of een nieuwe kalender te maken klikt u op **Organisatiebeheer** &gt; **Algemeen** &gt; **Kalenders**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Vereisten voor het schatten van de kosten van werkzaamheden

Om de volledige kostenramingsmogelijkheden van WBS te benutten, moet u de kosten en verkoopprijzen voor werknemers, arbeidscategorieën, onkosten, kosten en artikelen instellen.

-   Om de kosten en de verkoopprijs van arbeid, onkosten en kostencategorieën in te stellen, klikt u op **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Prijzen**.
-   Om de kosten en verkoopprijs van artikelen in testellen, gebruikt u de pagina **Handelsovereenkomsten** voor elk artikel op de lijstpagina **Vrijgegeven producten** in Productgegevensbeheer.

## <a name="creating-a-wbs"></a>Een WBS maken
Voor het maken van een WBS zijn drie activiteiten nodig:

1.  **Werk-ontleding** - Het werk opsplitsen in handelbare brokken of taken.
2.  **Werkschema** - Schatting van de tijd die nodig is om een taak te voltooien, taakafhankelijkheden instellen en de begin- en einddatums voor taken selecteren.
3.  **Kostenraming** - Ramingskosten voor elke taak.

In de volgende secties wordt besproken hoe de WBS-mogelijkheden bij elk van deze activiteiten van pas kunnen komen.

### <a name="work-decomposition"></a>Werkontleding

Het maken van een specificatie of ontleding van het werk is doorgaans de eerste stap tijdens het maken van een WBS. De WBS-functionaliteit ondersteunt de volgende basisconcepten voor werkspecificatie of -ontleding. 

**Projecthoofdtaak** De projecthoofdtaak is de hoogste overzichtstaak voor een project. Alle andere projecttaken worden daaronder gemaakt. De naam van de hoofdtaak wordt altijd ingesteld op de projectnaam. De inzet, datums en duur van het hoofdknooppunt omvatten de waarden voor de taken onder de hoofdtaak. U kunt de eigenschappen van het hoofdknooppunt wijzigen of verwijderen.

**Overzichts- of containertaken** Een overzichtstaak is een taak die deeltaken heeft of integrale taken onder zich heeft. Een overzichtstaak heeft zelf geen werkinspanning of kosten. In plaats daarvan zijn de werkinspanning en kosten van een overzichtstaak de som van de werkinspanning en kosten van de integrale taken. De vroegste begindatum van de integrale taken wordt gebruikt als begindatum van de overzichtstaak, en de einddatum van de integrale taken wordt gebruikt als einddatum. U kunt de naam van een overzichtstaak wijzigen, maar u kunt de planningseigenschappen voor inspanning, datums en duur niet wijzigen. Als u een overzichtstaak verwijdert, verwijdert u ook alle integrale taken. 

**Bladknooppunttaken** Een bladknooppunttaak vertegenwoordigt het meest gedetailleerde werkpakket in het project. Een bladknooppunt heeft een geraamde inspanning, gepland aantal resources, geplande begindatum en einddatum en duur. 

U kunt de volgende hiërarchiebewerkingen uitvoeren om het maken van een werkhiërarchie het -ontleding voor een project in te schakelen. 

**Nieuwe taak** Elke nieuwe taak die u maakt wordt automatisch toegevoegd onder het hoofdknooppunt, en een WBS-nummer wordt automatisch toegewezen aan de taak. Het WBS-nummer vertegenwoordigt het niveau van de taak in de hiërarchie. Voor taken in het eerste niveau onder de taak van de projecthoofdmap, wordt een nummeringsplan van 1, 2, 3, enz. gebruikt. Voor taken onder het eerste niveau wordt een nummeringsplan van 1.1, 1.2, 1.3, enz. gebruikt. Voor elk niveau dat onder een vorig niveau wordt toegevoegd, wordt een nieuwe gestippelde reeks nummers toegevoegd. 

Momenteel kunt u de WBS-nummering niet aanpassen. 

**Inspringingtaak** Wanneer u een taak inspringt, wordt deze een onderliggend item van de taak die eraan voorafgaat. Het WBS-nummer van de onderliggende nieuwe taak wordt automatisch opnieuw berekend op basis van het WBS-nummer van het bijbehorende nieuwe bovenliggende item. De bovenliggende taak is nu een overzicht of containertaak en wordt daarom een samenvoeging van de integrale taken. 

> [!NOTE] 
> Wanneer u taken inspringt onder een taak die een bladknooppunt vóór de inspringbewerking was, verliest de nieuwe overzichtstaak de eigen datums, inzet en het aantal resources. Deze gebruikt nu een overzicht van de waarden van de nieuwe integrale taken. 

**Inspringing taak** Wanneer u een taak inspringt, is deze niet langer een integrale van de bovenliggende taak. Het WBS-nummer van deze taak wordt automatisch opnieuw berekend om het nieuwe niveau van de taak in de hiërarchie te reflecteren. De inzet, kosten en datums van de vorige bovenliggende taak van de taak worden opnieuw berekend om deze taak uit te sluiten. 

**Omhoog en Omlaag** Wanneer u op **Omhoog** en **Omlaag** klikt, wijzigt u de positie van een taak in de hiërarchie van de bovenliggende taak. De positie van een taak heeft geen invloed op de inzet, kosten, datums of duur van de taak. Het WBS-nummer van de taak wordt echter automatisch opnieuw berekend om de nieuwe positie van de taak te reflecteren.

### <a name="schedule-estimation"></a>Planningsraming

Planningsraming is meestal de tweede stap bij het maken van een WBS. U kunt het best de planningsraming uitvoeren nadat u de taken hebt gemaakt. De pagina **Structuur voor werkspecificatie** in Finance and Operations heeft twee gedeelten. Het bovenste deelvenster is bedoeld voor planningsraming, en het onderste deelvenster bevat een tabblad **Geraamde kosten en inkomsten** dat u kunt gebruiken voor kostenraming. 
**Taakafhankelijkheden** In een WBS kunt u een voorafgaande relatie maken tussen taken. Wanneer u voorafgaande taken aan een taak toewijst, kan die taak pas starten nadat alle voorafgaande taken zijn voltooid. De geplande begindatum van de taak wordt automatisch ingesteld op de laatste datum van alle voorafgaande taken. 

**Taakplanning Microsoft Dynamics 365 for Finance and Operations** De volgende factoren bepalen het plannen van bladknooppunttaken:

-   Voorgangers
-   Inzet
-   Het aantal resources
-   Begin- en einddatums

De begindatum van een bladknooppunttaak zonder voorafgaande taken wordt automatisch ingesteld op de planningsbegindatum van het project. De duur van een bladknooppunttaak wordt altijd berekend als het aantal werkdagen tussen de begin- en einddatum. 

*<strong><em>Planningsregels</em></strong>* Wanneer automatische planningshulp is ingeschakeld, gelden de volgende regels voor taakplanning voor bladknooppunttaken:

-   De begin- en einddatum van een taak moeten werkdagen zijn volgens de planningskalender van het project.
-   De begindatum van een taak met voorafgaande taken wordt automatisch ingesteld op de laatste einddatum van alle voorafgaande taken.
-   De inzet voor een taak wordt automatisch als volgt berekend:

Aantal personen × duur × aantal uren in een standaard werkdag op de projectkalender. 

In sommige gevallen kunt u van deze regels afwijken. U kunt automatische planning uitschakelen om te voorkomen dat Finance and Operations automatisch eigenschappen van bladknooppunttaken instelt of corrigeert. Wanneer u de gegevens voor een taak invoert die een schending van planningsregels veroorzaakt, wordt een planningsfoutpictogram weergegeven voor de taak. Als u niet wilt dat planningsfouten worden weergegeven, klikt u op **Planningsfouten worden weergegeven** om de functie uit te schakelen. 

> [!NOTE] 
> De waarden voor een overzicht of containertaak worden nog steeds berekend als de som van waarden van de integrale taken, ongeacht of automatische planningshulp is in- of uitgeschakeld. 

**Planningsfouten oplossen** Wanneer automatische planningshulp is ingeschakeld, komen planningsfouten meestal niet voor. Als u automatische planningshulp echter uitschakelt en later weer inschakelt, kunnen er planningsfoutpictogrammen in de WBS worden weergegeven. 

**Planningsfouten op taak oplossen** Wanneer u dubbelklikt op het planningsfoutpictogram voor een bepaalde taak, worden in het dialoogvenster alle planningsfouten voor die taak weergegeven. U kunt kiezen welke planningsfouten u voor de taak wilt oplossen. 

**Alle planningsfouten oplossen** Als u wilt dat Finance and Operations alle fouten in de WBS oplost, dan klikt u in het actievenster **Alle afwijkingen in planning corrigeren**. 

> [!NOTE] 
> Deze functie kan aanzienlijke wijzigingen aan de WBS veroorzaken. De fouten worden gecorrigeerd in de volgende volgorde:

1.  De geraamde inspanning voor alle taken wordt gewijzigd zodat dit gelijk is aan de capaciteit die op de projectkalender is gedefinieerd.
2.  De begindatum van elke taak wordt gewijzigd zodat de taak start nadat alle voorafgaande taken zijn voltooid.
3.  De begindatum van elke taak wordt gewijzigd om tussenruimten in de begindatums van voorafgaande taken te verwijderen.

### <a name="cost-estimation"></a>Kostenraming

Zoals eerder in dit document is vermeld, voert u de kostenraming voor elke bladknooppunttaak in via het tabblad **Geschatte kosten en opbrengsten** in het onderste deelvenster van de pagina **Structuur voor werkspecificatie**. 

> [!NOTE] 
> U kunt de kostenraming voor een overzichts- of containertaak niet wijzigen. De kostenraming voor een overzichtstaak is gelijk aan de som van de kostenraming van de bladknooppunttaken. De geschatte totale kosten voor elke taak worden berekend als de som van geschatte kostbedragen voor de volgende transactietypen:

-   Arbeid
-   Artikel of materiaal
-   Uitgaven

Een transactietype **Kosten** wordt gebruikt om op kosten gebaseerde opbrengst te schatten. Dit transactietype heeft geen kostencomponent en wordt daarom niet meegenomen wanneer kosten worden geraamd. 

Een transactietype **A conto** wordt gebruikt voor het registreren van de aangegane verkoopwaarde in een projecttype met een vaste waarde. Dit transactietype wordt ook niet meegenomen wanneer kosten worden geraamd. 

Wanneer u kosten voor arbeid raamt, moet u het materiaal en onkosten voor elke taak toewijzen aan een projectcategorie voor de kostenraming. 

**Arbeidskosten ramen** Voor elke bladknooppunttaak wijst u een werkinspanning in uren en een standaardcategorie toe. Wanneer u dus een planning instelt voor een taak, wordt de arbeidskostenraming voor die taak automatisch toegevoegd in de standaardcategorie voor arbeid. Deze kostenraming wordt weergegeven op het tabblad **Geraamde kosten en inkomsten** in het raster **Regeldetails** voor die taak. Als u meer arbeidskostenramingen nodig hebt, kunt u deze toevoegen op dit tabblad. Als u het aantal uren op de arbeidskostenraming verhoogt of verlaagt, wordt de planning voor de taak automatisch opnieuw berekend. 

**Onkosten en materiaalkosten ramen** Op het tabblad **Geraamde kosten en inkomsten** kunt u desgewenst ook onkosten en materiaalkosten voor een taak ramen. 

De kostprijs en verkoopprijs voor elke arbeids- of onkostenramingsregel zijn gebaseerd op de instellingen die zijn gedefinieerd voor elke categorie in de prijstabellen in **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Prijzen**. Voor artikelen worden de kosten en verkoopprijs automatisch toegevoegd uit de artikel- of handelsovereenkomsten op de lijstpagina **Vrijgegeven producten** in Productgegevensbeheer.

## <a name="tracking-progress-on-the-wbs"></a>Voortgang in de WBS bijhouden
Bepaalde bedrijfstakken volgen de voortgang van een project met een WBS op een heel laag niveau, terwijl anderen de voortgang op een hoger niveau van de WBS volgen. In deze sectie wordt beschreven hoe u WBS kunt gebruiken voor uw projectvereisten. 

Finance and Operations heeft drie weergaven voor de WBS van een project: Planningsweergave, Weergave inzettracering en Weergave kostentracering.

### <a name="planning-view"></a>Planningsweergave

De planningsweergave toont de geplande of basislijnraming van de planning en de kostengegevens. Hoewel er geen functies voor het volgen van de versie en basislijn voor een project-WBS zijn, zijn de waarden in deze weergave bedoeld om de basislijnversie weer te geven. De sectie Planningsraming en Kostenraming in dit onderwerp beschrijven deze weergave en hoe deze wordt gebruikt om een WBS te maken.

### <a name="effort-tracking-view"></a>Weergave inzettracering

De Weergave inzettracering houdt de voortgang bij voor taken in de WBS. Deze vergelijkt de cumulatieve werkelijke inspanningsuren voor een taak met de geplande inspanningsuren. De volgende formules bieden de waarden in de Weergave inzettracering:

-   Voortgangspercentage = Werkelijke inspanning tot heden ÷ Gepland inspanning voor de taak
-   Resterende inspanning (ofwel Kostenraming tot voltooid, \[ETC\]) = Geplande inspanning – Werkelijke inspanning tot heden
-   Raming bij voltooid (EAC) = Resterende inspanning + Werkelijke inspanning tot heden
-   Verwachte inspanningsafwijking = Geplande inspanning - EAC

De Weergave inzettracering geeft een projectie weer van de inspanningsafwijking voor de taak, afhankelijk van of EAC meer of minder is dan de geplande inspanning:

-   Als het EAC meer is dan de geplande inspanning, wordt geschat dat de taak meer tijd kost dan gepland was en achterloopt op het schema.
-   Als het EAC minder is dan de geplande inspanning, wordt geschat dat de taak minder tijd kost dan gepland was en voorloopt op het schema.

**Re-projectie van inspanning door de projectmanager** Soms moet de projectmanager of een andere persoon die de voortgang van een project bijhoudt, de oorspronkelijke ramingen voor een taak herzien. De taak kan om diverse redenen sneller of langzamer gaan dan oorspronkelijk was gepland. De omvang kan bijvoorbeeld zijn verlaagd of werknemers hebben minder ervaring dan oorspronkelijk gepland. Projecties zijn het inzicht in ramingen van de projectmanager op basis van de huidige status van een project. In het algemeen moet u niet de basislijnnummers wijzigen, omdat een projectbasislijn een goed-gepubliceerd document vormt voor de planning en kostenraming van het project waarmee alle belanghebbenden van het project akkoord zijn gegaan. 

Er zijn twee manieren waarop projectmanagers de inspanning voor taken kunnen wijzigen:

-   De resterende inspanning wijzigen die automatisch is ingesteld om de werkelijke resterende inspanning voor de taak bij te werken.
-   Het voortgangspercentage wijzigen dat automatisch is ingesteld om de werkelijke voortgang voor de taak bij te werken.

Beide benaderingen leiden tot een herberekening van de ETC, EAC en het voortgangspercentage, en de verwachte inspanningsafwijking voor de taak. De EAC, ETC en het voortgangspercentage voor overzichtstaken worden opnieuw berekend, en de verwachte inspanningsafwijking wordt bijgewerkt. 

**Gewijzigde inspanning op overzichtstaken** U kunt de inspanning op overzichts- of containertaken wijzigen. Ongeacht of u deze waarden wijzigt door de resterende inspanning of het voortgangspercentage op de overzichtstaken te gebruiken, worden de berekeningen automatisch in de volgende volgorde weergegeven:

1.  De EAC, ETC en voortgangspercentage voor de taak worden berekend.
2.  De nieuwe EAC wordt gedistribueerd naar de onderliggende taken in dezelfde verhouding als het oorspronkelijke EAC-bedrag.
3.  De nieuwe EAC op elke bladknooppunttaak wordt berekend.
4.  Het resterende inspannings- en voortgangspercentage worden opnieuw berekend voor alle betrokken onderliggende taken op basis van de nieuwe EAC-waarde. De inspanningsafwijking van de taken wordt ook opnieuw berekend.
5.  De EAC van de overzichtstaken wordt opnieuw berekend vanuit de bladknooppunten.

Klik op **Uitvouwen naar niveau** in de Weergave inzettracering om het niveau in te instellen waarop uw WBS moet worden bijgehouden en beheerd. De WBS wordt automatisch uitgevouwen naar dat niveau in de Weergave inzettracering wanneer u deze opent.

### <a name="cost-tracking-view"></a>Weergave kostentracering

De Weergave kostentracering toont de tracering van kostenverbruik voor een taak. In deze weergave worden de werkelijke kosten voor een taak tot heden vergeleken met de geplande kosten voor de taak. De volgende formules bieden de waarden in de Weergave kostentracering:

-   Percentage verbruikte kosten = Werkelijke kosten tot heden ÷ Geplande kosten voor de taak
-   Kosten voor voltooien (CTC) = Geplande kosten – Werkelijke kosten tot heden
-   Geraamd bij voltooiing (EAC) = CTC + Werkelijke kosten tot heden
-   Verwachte kostenafwijking = Geplande kosten - EAC

De Weergave kostentracering geeft een projectie weer van de kostenafwijking voor de taak, afhankelijk van of EAC meer of minder is dan de geplande kosten:

-   Als het EAC meer is dan de geplande kosten, wordt geschat dat de taak meer geld kost dan gepland was en het budget overschrijdt.
-   Als het EAC minder is dan de geplande kosten, wordt geschat dat de taak minder geld kost dan gepland was en onder het budget blijft.

**Re-projectie van inspanning door de projectmanager** Projectmanagers moeten CTC gebruiken om de oorspronkelijke kostenraming voor een taak te wijzigen. De projectmanager kan de CTC-waarde wijzigen in de kosten die nodig zijn om de taak te voltooien. Als u de CTC-waarde wijzigt, worden de CTC, EAC en het percentage verbruikte kosten, en de geschatte kostenafwijking voor een taak opnieuw berekend. De EAC, ETC en het percentage verbruikte kosten voor overzichtstaken worden ook opnieuw berekend, en de verwachte kostenafwijking wordt bijgewerkt. 

> [!NOTE] 
> Wanneer u inspanning voor een WBS-taak herziet, worden de CTC, EAC, percentage van verbruikte kosten en kostenafwijking allemaal opnieuw berekend in de Weergave kostentracering. Kostenrevisies hebben echter geen invloed op de waarden in de weergave Inzettracering, omdat de kosten per transactietype (arbeid, materiaal of onkosten) of projectcategorie niet worden gecorrigeerd. 

**Projectierevisie voor kosten op overzichtstaken** U kunt kosten op overzichtstaken herzien, en de berekeningen vinden automatisch in de volgende volgorde plaats:

1.  De EAC, CTC en percentage verbruikte kosten voor de taak worden opnieuw berekend.
2.  De nieuwe EAC wordt gedistribueerd naar de onderliggende taken in dezelfde verhouding als de oorspronkelijke EAC voor de taken.
3.  De nieuwe EAC voor elke taak wordt berekend.
4.  Het CTS en percentage verbruikte kosten worden opnieuw berekend voor de beïnvloede onderliggende taken, op basis van de EAC-waarde. De kostenafwijking van de taken wordt ook opnieuw berekend.
5.  De EAC voor alle overzichtstaken wordt opnieuw berekend op basis van deze wijziging.

Klik op **Uitvouwen naar niveau** in de Weergave kostentracering om het niveau in te instellen waarop uw WBS moet worden bijgehouden en beheerd. De WBS wordt automatisch uitgevouwen naar dat niveau in de Weergave kostentracering wanneer u deze opent.

### <a name="earned-value-management"></a>Beheer van verdiende waarde

U kunt de huidige methode voor verdiende waarde (EVM) gebruiken om de voortgang van een project bijhouden. U kunt huidige metriek voor verdiende waarde in het Rollencentrum van de projectmanager weergeven. De component grafiek voor huidige verdiende waarde geeft de tijdgebonden waarden van geplande en werkelijke kosten weer. Verdiende waarde vanaf de huidige datum wordt als een punt weergegeven. De tijdgebonden gegevens voor huidige verdiende waarde is momenteel niet verkrijgbaar. 

De tijdfase in de huidige grafiek voor verdiende waarde wordt weergegeven per week of maand. Dit onderdeel beschrijft de drie pijlers van EVM: geplande waarde, huidige verdiende waarde en werkelijke kosten. 

**Geplande waarde** De EVM-theorie bepaalt dat de geplande waardegrafiek het tarief toont waarmee het projectteam waarde op het project wil verdienen. 

Finance and Operations gebruikt de verdienregel 0:100 voor het uitzetten van de geplande waarde. Onder deze regel wordt de waarde van de taak geboekt naar de taak vanaf de einddatum. Er wordt geen waarde geboekt tot de taak voor 100 procent is voltooid. 

In Projectbeheer en boekhouding voert u hiervoor de einddatum van de bladknooppunten en de geplande kosten in. Wanneer de grafiek van geplande waarde per week wordt weergegeven, wordt de geplande waarde samengevat per week voor alle bladknooppunttaken voor de duur van het project. 

**Verdiende waarde** De EVM-theorie bepaalt dat de verdiende waardegrafiek het tarief toont waarmee het projectteam in werkelijkheid waarde op het project verdient. 

Finance and Operations gebruikt de verdienregel 0:100 voor het uitzetten van de verdiende waarde. Onder deze regel wordt de waarde van de taak geboekt naar de taak vanaf de einddatum. Er wordt geen waarde geboekt tot de taak voor 100 procent is voltooid. 

Als de huidige verdiende waarde wordt berekend, wordt het voortgangspercentage van elke taak meegenomen. Onder de regel 0:100 worden alleen de taken die tijdens een gedefinieerde periode zijn voltooid meegenomen voor de berekening van huidige verdiende waarde vanaf het einde van de periode. De verdiende waarde op het project wordt berekend voor alle taken die zijn voltooid wanneer de grafiek wordt gemaakt. 

> [!NOTE] 
> Het systeem voor WBS-tracering heeft momenteel niet de gegevensstructuren om historische voortgangspercentages voor elke taak op te slaan. Daarom kan de huidige verdiende waarde alleen worden gerapporteerd vanaf het moment dat de kubus wordt verwerkt. Verwerk de kubus regelmatig om de huidige verdiende-waardegegevens bij te werken die in het Rollencentrum worden weergegeven. 

**Werkelijke kosten** De EVM-theorie bepaalt dat de werkelijke kosten het tarief tonen waarmee geld wordt uitgegeven voor het project. 

Transacties die naar een project worden geboekt, worden gebruikt om de werkelijke-kostenregel in kaart te brengen. De kosten worden samengevat op datum. Deze gegevens worden vervolgens gebruikt om de werkelijke kosten per week of maand in de grafiek voor verdiende waarde weer te geven.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Concepten voor geplande waarde, verdiende waarde en werkelijke kosten gebruiken

**Afwijking van planning** Tijdens de planning maakt u een prognose voor het werk op een tijdlijn. Daarom is de geplande waarde het tempo waarmee projectplanners dachten dat het werk voor het project zou worden uitgevoerd. Nadat een project wordt uitgevoerd, het werk wordt voltooid en verdient het project waarde. Door geplande waarde te vergelijken met verdiende waarde, kunt u bekijken hoe het werk voor het project vordert. Het resultaat van deze vergelijking wordt genoemd planningsafwijking genoemd 

Als de geplande waarde voor een periode hoger is dan de verdiende waarde, is de hoeveelheid werk voor een project minder dan gepland. Daarom loopt het project achter op schema. Omdat geplande waarde en verdiende waarde uitgedrukt in monetaire voorwaarden , wordt de vertragingstijd op het project ook gegeven in een monetaire waarde. 

Als de geplande waarde voor een periode lager is dan de verdiende waarde, is de hoeveelheid werk voor een project meer dan gepland. Daarom loopt het project voor op schema. Aan deze doorlooptijd wordt ook een monetaire waarde gegeven.

**Kostenafwijking** Omdat de verdiende waarde gebruikmaakt van de kostprijs als multiplicator, geeft de verdiende waarde de kosten weer van het werk dat aan een project wordt verricht. Als een project vordert, biedt het transactielogboek een registratie van geld dat werkelijk wordt uitgegeven aan dat project. Door verdiende waarde te vergelijken met werkelijke kosten kunt u zien welk geldbedrag wordt uitgeven versus de verdiende waarde. Het resultaat van deze vergelijking wordt kostenafwijking genoemd. 

Als de werkelijke kosten die voor een periode worden uitgegeven hoger zijn dan de verdiende waarde, is er meer geld uitgegeven dan is verdiend. Daarom is het project boven het budget. 

Als de werkelijke kosten die voor een periode worden uitgegeven lager zijn dan de verdiende waarde, is er meer geld verdiend dan is uitgegeven. Daarom is het project onder het budget.

## <a name="wbs-templates"></a>WBS-sjablonen
U kunt de WBS-sjablonenfunctie gebruiken om standaardsjablonen voor projecten te maken. Als de projecten die uw bedrijf aanbiedt veel repeterend werk bevatten, kunt u overwegen om een WBS-sjabloon te maken. 

U kunt een WBS-sjabloon vanuit de WBS van een bestaand project maken, zodat de kennis en de beste praktijken die u tijdens de planning van het project verzamelde op vergelijkbare projecten in de toekomst opnieuw kunnen worden gebruikt. Het kan in sommige gevallen geen zin hebben om de hele WBS als sjabloon op te slaan. Daarom kunt u ook sjablonen maken van onderdelen van de WBS voor een project.

### <a name="saving-a-projects-wbs-as-a-template"></a>Het opslaan van de WBS van een project als sjabloon

Nadat u een sjabloon hebt gemaakt, kunt u deze importeren in de WBS van een nieuw project onder het basisknooppunt, of onder elke taak in de WBS van het project.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Een WBS-sjabloon in importeren in de WBS van een project

Wanneer u taken importeert, worden de taken in de sjabloon ingedeeld op basis van de begindatum van de taak waaronder ze zijn geïmporteerd. Tijdens het importeren worden de voorafgaande relaties in de sjabloontaken gebruikt om de begindatums voor de geïmporteerde taken te verwerken. De bestemming standaard werkkalender wordt toegepast om de einddatums van de geïmporteerde taken te berekenen, zodat werkdagen en de standaard werkuren, die in de huidige werkkalender zijn gedefinieerd, worden behouden. 

Kostenbedragen en verkoopprijzen op de ramingsregels worden toegepast om te garanderen dat de prijzen voor het project of projectcontract een geldige datum hebben.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Verschillen tussen de WBS van een project en een WBS-sjabloon

-   De taken in WBS-sjablonen hebben geen begin- en einddatum.

De werk- en niet-werkdagen worden niet ingesteld voor WBS-sjablonen.

-   WBS-sjablonen gebruiken altijd de planningskalender die is ingesteld als standaardwerkkalender voor alle projecten.

De standaardplanningskalender wordt alleen gebruikt om het aantal uren in een standaard werkdag te weten te komen.

-   De voorafgaande relaties worden niet gekopieerd naar een WBS-sjabloon.

Omdat WBS-sjablonen geen datums hebben, is de logica van de begindatum die gebaseerd is op de einddatum van een voorafgaande taak niet vereist.

-   Een arbeidskostenramingsregel wordt automatisch gemaakt wanneer een taak in een WBS-sjabloon wordt gemaakt. De verkoopprijs en het kostenbedrag worden gekopieerd uit de geselecteerde werknemer.

Onkosten en artikelkosten kunnen handmatig worden gemaakt, net zoals op de WBS van een project.

-   Planningsfouten worden weergegeven als er afwijkingen van de volgende formule zijn:

Inspanning = aaantal resources × duur × aantal uren in een standaardwerkdag 

U kunt alle planningsfouten tegelijk corrigeren door te klikken op **Alle planningsfouten oplossen**. 

Als alternatief kunt u afzonderlijk planningsfouten corrigeren door op het waarschuwingspictogram voor elke taak te klikken.




