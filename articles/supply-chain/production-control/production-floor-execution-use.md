---
title: Hoe medewerkers de interface voor de uitvoering van de productievloer gebruiken
description: In dit artikel wordt beschreven hoe de uitvoeringsinterface van de werkvloer moet worden gebruikt vanuit het perspectief van een werknemer.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0d857ef31e0fed2a0d7550197209fac9251d8812
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069781"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Hoe werknemers de uitvoeringsinterface voor de werkvloer gebruiken

[!include [banner](../includes/banner.md)]

De uitvoeringsinterface van de werkvloer is geoptimaliseerd voor aanraakinteractie. Het ontwerp biedt een visueel contrast dat voldoet aan de toegankelijkheidsvereisten voor werkvloeromgevingen. Het biedt dezelfde functionele mogelijkheden als het taakkaartapparaat. Het biedt echter ook de mogelijkheid om meerdere taken tegelijk te starten vanuit een takenlijst. (Deze mogelijkheid wordt ook wel *bundeling van taken* genoemd.) Bovendien kunnen werknemers via een takenlijst een guide openen die is gemaakt in Microsoft Dynamics 365 Guide. Op deze manier kunnen zij visuele instructies krijgen voor een HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Als werknemer aanmelden bij de uitvoeringsinterface van de werkvloer

Voordat werknemers het apparaat kunnen gaan gebruiken, moet een supervisor of technisch personeel het apparaat voorbereiden en de juiste pagina openen in Dynamics 365 Supply Chain Management. Zie [Een apparaat instellen voor het uitvoeren van de uitvoeringsinterface van de werkvloer](production-floor-execution-setup.md) voor meer informatie over het instellen van het apparaat.

Nadat het apparaat is voorbereid, wordt de aanmeldingspagina erop weergegeven. Deze pagina bevat informatie over de status van taken voor de lokale werkcel. Deze informatie wordt periodiek bijgewerkt. Op de pagina gebruiken werknemers hun badge-id's voor aanmelding. Hoewel werknemers geen gebruikersaccount hoeven te hebben voor Supply Chain Management, moeten ze een account voor *werknemer met tijdregistratie* hebben die ze kunnen gebruiken wanneer ze zich aanmelden.

![Aanmeldingspagina van de uitvoeringsinterface voor de werkvloer.](media/pfei-sign-in-page.png "Aanmeldingspagina van de uitvoeringsinterface voor de werkvloer")

In de overige secties van dit artikel wordt beschreven hoe werknemers met de interface werken.

## <a name="all-jobs-tab"></a>Tabblad Alle taken

Op het tabblad **Alle taken** vindt u een takenlijst waarin alle productietaken worden weergegeven met de status *Niet gestart*, *Gestopt* of *Gestart*. (Deze tabbladnaam is aanpasbaar en kan anders zijn voor uw systeem.)

![Tabblad Alle taken.](media/pfei-all-jobs-tab.png "Tabblad Alle taken")

De takenlijst heeft de volgende kolommen. De nummers komen overeen met de nummers in de vorige afbeelding.

1. **Selectiekolom**: in de linkerkolom worden vinkjes gebruikt om taken aan te duiden die door de werknemer zijn geselecteerd. Werknemers kunnen meerdere taken tegelijk selecteren in de lijst. Als u alle taken in de lijst wilt selecteren, selecteert u het vinkje in de kolomkop. Als één taak is geselecteerd, worden details over die taak weergegeven in het onderste gedeelte van de pagina.
1. **Taakstatuskolom**: in deze kolom worden symbolen gebruikt om de status van elke taak aan te geven. Taken zonder symbool in deze kolom hebben de status *Niet gestart*. Een groen driehoekje geeft taken aan die de status *Gestart* hebben. Twee gele verticale lijnen geven taken met de status *Gestopt* aan.
1. **Kolom met hoge prioriteit**: in deze kolom worden uitroeptekens gebruikt om taken met een hoge prioriteit aan te duiden.
1. **Order**: in deze kolom wordt het productieordernummer voor een taak weergegeven.
1. **Omschrijving**: in deze kolom wordt een omschrijving gegeven van de bewerking waarvan een taak deel uitmaakt.
1. **Aangevraagd**: in deze kolom wordt de hoeveelheid weergegeven die voor een taak is gepland om te produceren.
1. **Gestart**: deze kolom bevat de hoeveelheid die al is gestart voor een taak.
1. **Voltooid**: deze kolom bevat de hoeveelheid die al is voltooid voor een taak.
1. **Buiten gebruik gesteld**: deze kolom bevat de hoeveelheid die al buiten gebruik is gesteld voor een taak.
1. **Resterend**: in deze kolom wordt de hoeveelheid weergegeven die nog moet worden voltooid voor een taak.

## <a name="active-jobs-tab"></a>Tabblad Actieve taken

Op de tabbladen **Actieve taken** wordt een lijst weergegeven met alle taken die de aangemelde werknemer al heeft gestart. (Deze tabbladnaam is aanpasbaar en kan anders zijn voor uw systeem.)

![Tabblad Actieve taken.](media/pfei-active-jobs-tab.png "Tabblad Actieve taken")

De lijst met actieve taken heeft de volgende kolommen:

- **Selectiekolom**: in de linkerkolom worden vinkjes gebruikt om taken aan te duiden die door de werknemer zijn geselecteerd. Werknemers kunnen meerdere taken tegelijk selecteren in de lijst. Als u alle taken in de lijst wilt selecteren, selecteert u het vinkje in de kolomkop. Als één taak is geselecteerd, worden details over die taak weergegeven in het onderste gedeelte van de pagina.
- **Order**: in deze kolom wordt het productieordernummer voor een taak weergegeven.
- **Omschrijving**: in deze kolom wordt een omschrijving gegeven van de bewerking waarvan een taak deel uitmaakt.
- **Aangevraagd**: in deze kolom wordt de hoeveelheid weergegeven die voor een taak is gepland om te produceren.
- **Gestart**: deze kolom bevat de hoeveelheid die al is gestart voor een taak.
- **Voltooid**: deze kolom bevat de hoeveelheid die al is voltooid voor een taak.
- **Buiten gebruik gesteld**: deze kolom bevat de hoeveelheid die al buiten gebruik is gesteld voor een taak.
- **Resterend**: in deze kolom wordt de hoeveelheid weergegeven die nog moet worden voltooid voor een taak.

## <a name="my-jobs-tab"></a>Tabblad Mijn taken

Op het tabblad **Mijn taken** kunnen werknemers eenvoudig alle niet-gestarte en onvoltooide taken bekijken die specifiek aan hen zijn toegewezen. Dit is handig in bedrijven waarin taken soms of altijd aan bepaalde werknemers (Human Resources) worden toegewezen in plaats van aan andere typen resources (zoals machines).

Het planningssysteem wijst elke productie taakautomatisch toe aan een specifieke resourcerecord en elke resourcerecord heeft een type (zoals machine of persoon). Wanneer u een werknemer in dienst stelt als productiewerker, kunt u het werknemersaccount koppelen aan een unieke registratie voor Human Resources.

Het tabblad **Mijn taken** bevat alle niet-gestarte en onvoltooide taken die zijn toegewezen aan de human resource-record van de aangemelde werknemer, als een werknemer is aangemeld. Taken die zijn toegewezen aan een machine of een ander type resource worden nooit vermeld, zelfs als de aangemelde werknemer aan deze taken is begonnen.

Als u alle taken wilt weergeven die zijn gestart door de aangemelde werknemer, ongeacht het type resource dat aan elke taak is toegewezen, gebruikt u het tabblad **Actieve taken**. Gebruik het tabblad **Alle taken** als u alle onvoltooide taken wilt weergeven die overeenkomen met de configuratie van het lokale taakfilter, ongeacht de werknemer of de beginstatus.

![Tabblad Mijn taken.](media/pfei-my-jobs-tab.png "Tabblad Mijn taken")

## <a name="my-machine-tab"></a>Tabblad Mijn machine

Op het tabblad **Mijn machine** kunnen werknemers een activum selecteren dat is gekoppeld aan een machineresource in de filterset op het tabblad **Alle taken**. De werknemer kan vervolgens de status en gesteldheid van het geselecteerde activum weergeven door waarden te lezen voor maximaal vier geselecteerde tellers en lijsten met recente onderhoudsverzoeken en geregistreerde uitvaltijden. De werknemer kan ook onderhoud voor het geselecteerde activum aanvragen en uitvaltijd van de machine registreren en bewerken. (Deze tabbladnaam is aanpasbaar en kan anders zijn voor uw systeem.)

![Het tabblad Mijn machine.](media/pfei-my-machine-tab.png "Het tabblad Mijn machine")

Het tabblad **Mijn machine** heeft de volgende kolommen. De nummers komen overeen met de nummers in de vorige afbeelding.

1. **Machineactiva**: selecteer het machineactivum dat u wilt volgen. Typ een naam die u wilt selecteren in een lijst met overeenkomende activa of selecteer het vergrootglaspictogram dat u wilt selecteren in een lijst met alle activa die zijn gekoppeld aan de resources in het filter van de takenlijst.

    > [!NOTE]
    > Gebruikers van Supply Chain Management kunnen zo nodig een resource aan elk activum toewijzen via de pagina **Alle activa** (op het tabblad **Vaste activa** met de vervolgkeuzelijst **Resource**). Zie [Een activum maken](../asset-management/objects/create-an-object.md) voor meer informatie.

1. **Instellingen**: selecteer het tandwielpictogram om een dialoogvenster te openen waarin u kunt kiezen welke tellers voor het geselecteerde machineactivum moeten worden weergegeven. Waarden voor deze tellers worden boven aan het tabblad **Activabeheer** weergegeven. In het menu **Instellingen** (in de volgende schermopname) kunt u maximaal vier tellers inschakelen. Voor elke teller die u wilt inschakelen, gebruikt u het zoekveld boven aan de tegel om een teller te selecteren. Het zoekveld bevat alle tellers die zijn gekoppeld aan het activum dat boven aan de pagina **Activabeheer** is geselecteerd. Stel elke teller in om de **samengevoegde** waarde of de laatste **werkelijke** waarde voor de teller te controleren. Als u bijvoorbeeld een teller in stelt die bijhoudt hoeveel uur de machine al draait, moet u de teller instellen op **Samengevoegd**. Als u een teller instelt om de meest recente bijgewerkte temperatuur of druk te meten, moet u deze instellen op **Werkelijk**. Selecteer **OK** om de instellingen op te slaan en het dialoogvenster te sluiten.

    ![De instellingen van het tabblad Mijn machine.](media/pfei-my-machine-tab-settings.png "De instellingen van het tabblad Mijn machine")

1. **Onderhoud aanvragen**: selecteer deze knop om een dialoogvenster te openen waarin u een onderhoudsaanvraag kunt maken. U kunt een omschrijving en een notitie maken. De aanvraag wordt onder de aandacht gebracht van een Supply Chain Management-gebruiker, die de onderhoudsaanvraag vervolgens kan converteren naar een onderhoudswerkorder.
1. **Uitvaltijd registreren**: selecteer deze knop om een dialoogvenster te openen waarin u de uitvaltijd van machines kunt registreren. U kunt een redencode selecteren en een datum/tijd voor de uitvaltijd invoeren. De registratie van uitvaltijd van machines wordt gebruikt om de efficiëntie van de machineactiva te berekenen.
1. **Weergeven of bewerken**: selecteer deze knop om een dialoogvenster te openen waarin u bestaande uitvaltijdrecords kunt bewerken of weergeven.

## <a name="starting-and-completing-production-jobs"></a>Productietaken starten en voltooien

Werknemers starten een productietaak door een taak te selecteren op het tabblad **Alle taken** en vervolgens **Taak starten** te selecteren om het dialoogvenster **Taak starten** te openen.

![Dialoogvenster Taak starten.](media/pfei-start-job-dialog.png "Dialoogvenster Taak starten")

Werknemers gebruiken het dialoogvenster **Taak starten** om de productiehoeveelheid te bevestigen en vervolgens de taak te starten. Werknemers kunnen de hoeveelheid aanpassen door het veld **Hoeveelheid** te selecteren en vervolgens het numerieke toetsenbord te gebruiken dat wordt weergegeven. Werknemers selecteren vervolgens **Starten** om aan de taak te gaan werken. Het dialoogvenster **Taak starten** wordt gesloten en de taak wordt toegevoegd aan het tabblad **Actieve taken**.

Werknemers kunnen een taak met een willekeurige status starten. Wanneer een werknemer een taak start die de status *Niet gestart* heeft , wordt in het veld **Hoeveelheid** in het dialoogvenster **Taak starten** in eerste instantie de volledige hoeveelheid weergegeven. Wanneer een werknemer een taak start die de status *Gestart* of *Gestopt* heeft , wordt in het veld **Hoeveelheid** in eerste instantie de resterende hoeveelheid weergegeven.

## <a name="reporting-good-quantities"></a>Goede hoeveelheden rapporteren

Wanneer werknemers een taak voltooien of gedeeltelijk voltooien, kunnen ze goede hoeveelheden rapporteren die zijn geproduceerd door een taak te selecteren op het tabblad **Actieve taken** en vervolgens **Voortgang rapporteren** te selecteren. Vervolgens voert de werknemer in het dialoogvenster **Voortgang rapporteren** de goede hoeveelheid in met het numerieke toetsenbord. De hoeveelheid is standaard leeg. Nadat een hoeveelheid is ingevoerd, kan de werknemer de status van de taak bijwerken naar *In uitvoering*, *Gestopt* of *Voltooid*.

![Dialoogvenster Voortgang rapporteren.](media/pfei-report-progress-dialog.png "Dialoogvenster Voortgang rapporteren")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Goede hoeveelheden rapporteren voor batchorders met co- en bijproducten

Werknemers kunnen de uitvoeringsinterface voor de werkvloer gebruiken om de voortgang van batchorders te rapporteren. Deze rapportage omvat rapportage over co- en bijproducten.

Sommige fabrikanten, met name die in procesindustrieën, gebruiken batchorders om hun productieprocessen te beheren. Batchorders worden gemaakt op basis van formules. U kunt deze formules zo definiëren dat deze co- en bijproducten als uitvoer hebben. Wanneer feedback over deze batchorders wordt gerapporteerd, moet de hoeveelheid uitvoer worden geregistreerd voor het formule-artikel en voor de co- en bijproducten.

Wanneer een werknemer een taak voor een batchorder voltooit of gedeeltelijk voltooit, kan deze goede of uitvalhoeveelheden rapporteren voor elk product dat is gedefinieerd als uitvoer voor de order. Producten die zijn gedefinieerd als uitvoer voor een batchorder, kunnen van het type *Formule*, *Coproduct* of *Bijproduct* zijn.

Als een werknemer goede hoeveelheden voor de producten wil rapporteren, selecteert deze een taak op het tabblad **Actieve taken** en selecteert deze vervolgens **Voortgang rapporteren**.

Vervolgens kan de werknemer in het dialoogvenster **Voortgang rapporteren** producten selecteren die zijn gedefinieerd als uitvoer voor de batchorder waarover wordt gerapporteerd. De werknemer kan een of meer producten in de lijst selecteren en vervolgens **Voortgang rapporteren** selecteren. Voor elk product is de hoeveelheid standaard leeg en de werknemer kan de hoeveelheid invoeren op het numerieke toetsenbord. De werknemer kan de knoppen **Vorige** en **Volgende** gebruiken om tussen de geselecteerde producten te schakelen. Nadat een hoeveelheid is ingevoerd voor elk product, kan de werknemer de status van de taak bijwerken naar *In uitvoering*, *Gestopt* of *Voltooid*.

![Rapporteren over co- en bijproducten.](media/report-co-by-products.png "Rapporteren over co- en bijproducten")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Rapporteren over batchorders voor planningsartikelen

Wanneer een werknemer een taak voltooit voor een batchorder voor een planningsartikel, rapporteren ze alleen hoeveelheden voor co- en bijproducten, omdat planningsartikelen geen artikel van het type *Formule* bevatten.

### <a name="reporting-co-product-variation"></a>Rapporteren over co-productvariaties

Als een batchorder is gemaakt op basis van een formuleversie waarbij de optie **Co-productvariaties** is ingesteld op *Ja*, kan de werknemer rapporteren over co-producten die geen deel uitmaken van de definitie voor de batchorders. Deze functionaliteit wordt gebruikt in scenario's waarin tijdens het productieproces onverwachte productuitvoer kan plaatsvinden.

In dit geval kan de werknemer het co-product en de hoeveelheid opgeven waarover deze wil rapporteren door **Co-productvariaties** te selecteren in het dialoogvenster voor voortgangsrapportage. De werknemer kan vervolgens kiezen uit alle vrijgegeven producten die als co-producten zijn gedefinieerd.

### <a name="reporting-catch-weight-items"></a>Catch weight-artikelen rapporteren

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Werknemers kunnen de uitvoeringsinterface voor de werkvloer gebruiken om de voortgang van batchorders die zijn gemaakt voor catch weight-artikelen te rapporteren. Batchorders worden gemaakt op basis van formules die u kunt definiëren zodat ze catch weight-artikelen als formule-artikelen, co- en bijproducten als uitvoer hebben. U kunt ook formuleregels definiëren voor ingrediënten die zijn gedefinieerd voor catch weight. Catch weight-artikelen gebruiken twee maateenheden om de voorraad te volgen: de hoeveelheid catch weight en de voorraadhoeveelheid. In de voedselindustrie kan verplakt vlees bijvoorbeeld worden gedefinieerd als catch weight-artikel, waarbij de catch weight-hoeveelheid wordt gebruikt om het aantal dozen bij te houden en de voorraadhoeveelheid wordt gebruikt om het gewicht van de dozen bij te houden.

## <a name="reporting-scrap"></a>Uitval rapporteren

Wanneer werknemers een taak voltooien of gedeeltelijk voltooien, kunnen ze uitval rapporteren door een taak te selecteren op het tabblad **Actieve taken** en vervolgens **Uitval rapporteren** te selecteren. Vervolgens voert de werknemer in het dialoogvenster **Uitval rapporteren** de uitvalhoeveelheid in met het numerieke toetsenbord. De werknemer selecteert ook een reden (*Geen*, *Machine*, *Operator* of *Materiaal*).

![Dialoogvenster Uitval rapporteren.](media/pfei-report-scrap-dialog.png "Dialoogvenster Uitval rapporteren")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Materiaalverbruik aanpassen en materiaalreserveringen maken

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Medewerkers kunnen materiaalverbruik voor elke productietaak aanpassen. Deze functionaliteit wordt gebruikt in gevallen waarin de werkelijke hoeveelheid materialen die door een productietaak is verbruikt, meer of minder was dan de geplande hoeveelheid. Daarom moet u deze aanpassen om de voorraadniveaus actueel te houden.

Medewerkers kunnen ook reserveringen maken voor de batch- en serienummers van materialen. Deze functionaliteit wordt gebruikt in gevallen waarin een medewerker handmatig moet opgeven welke materiaalbatch- of serienummers zijn verbruikt om te voldoen aan de vereisten voor materiaaltraceerbaarheid.

Medewerkers kunnen de hoeveelheid opgeven die moet worden aangepast door **Materiaal aanpassen** te selecteren. Deze knop is beschikbaar op de volgende plaatsen:

- In het dialoogvenster **Uitval rapporteren**
- In het dialoogvenster **Voortgang rapporteren**.
- Op de werkbalk aan de rechterkant

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Materiaalverbruik aanpassen vanuit de dialoogvensters Uitval rapporteren en Voortgang rapporteren

Nadat een medewerker de hoeveelheid die moet worden gerapporteerd in het dialoogvenster **Voortgang rapporteren** of **Uitval rapporteren** heeft ingevoerd, is de knop **Materiaal aanpassen** beschikbaar. Als de gebruiker deze knop selecteert, verschijnt het dialoogvenster **Materiaal aanpassen**. In dit dialoogvenster worden de artikelen weergegeven die gepland staan voor verbruik wanneer de goede of uitgevallen hoeveelheid voor de taak wordt gerapporteerd.

De lijst in het dialoogvenster toont de volgende informatie:

- **Productnummer**: het productmodel en de productvariant.
- **Productnaam** – De naam van het product.
- **Voorstel**: de geschatte hoeveelheid materiaal die wordt verbruikt wanneer voortgang of uitval wordt gerapporteerd voor de opgegeven hoeveelheid voor de taak.
- **Verbruik**: de werkelijke hoeveelheid materiaal die wordt verbruikt wanneer voortgang of uitval wordt gerapporteerd voor de opgegeven hoeveelheid voor de taak.
- **Gereserveerd**: de hoeveelheid materiaal die fysiek in de voorraad is gereserveerd.
- **Eenheid**: de eenheid van de stuklijst.

Aan de rechterkant van het dialoogvenster wordt de volgende informatie weergegeven:

- **Productnummer**: het productmodel en de productvariant.
- **Geraamd**: de geraamde hoeveelheid om te verbruiken.
- **Gestart**: de hoeveelheid die is gestart voor de productietaak.
- **Resterende hoeveelheid**: van de geraamde hoeveelheid is dit de hoeveelheid die resteert om te verbruiken.
- **Vrijgegeven hoeveelheid**: de hoeveelheid die is verbruikt.

De volgende acties kunnen worden uitgevoerd:

- Medewerkers kunnen de hoeveelheid opgeven die moet worden aangepast voor een materiaal door **Verbruik aanpassen** te selecteren. Nadat de hoeveelheid is bevestigd, wordt de hoeveelheid in de kolom **Verbruik** bijgewerkt met de aangepaste hoeveelheid.
- Wanneer de medewerker **Materiaal aanpassen** selecteert, wordt een orderverzamellijstjournaal voor de productie gemaakt. Dit journaal bevat dezelfde artikelen en hoeveelheden als de lijst **Materiaal aanpassen**.
- Als de medewerker een hoeveelheid aanpast in het dialoogvenster **Materiaal aanpassen**, wordt het veld **Voorstel** op de bijbehorende journaalregel bijgewerkt met dezelfde hoeveelheid. Als de medewerker **Annuleren** selecteert in het dialoogvenster **Materiaal aanpassen**, wordt de orderverzamellijst verwijderd.
- Als de medewerker **OK** selecteert, wordt de orderverzamellijst niet verwijderd. Deze lijst wordt geboekt wanneer de taak wordt gerapporteerd in het dialoogvenster **Uitval rapporteren** of **Voortgang rapporteren**.
- Als de medewerker **Annuleren** selecteert in het dialoogvenster **Voortgang rapporteren** of **Uitval rapporteren**, wordt de orderverzamellijst verwijderd.

### <a name="adjust-material-from-the-primary-or-secondary-toolbar"></a>Materiaal aanpassen via de primaire of secundaire werkbalk

De knop **Materiaal aanpassen** kan worden geconfigureerd zodat deze op de primaire of secundaire werkbalk wordt getoond. (Zie voor meer informatie [De interface voor de uitvoering van de productievloer ontwerpen](production-floor-execution-tabs.md).) Een medewerker kan **Materiaal aanpassen** selecteren voor een productietaak die in uitvoering is. In dit geval wordt het dialoogvenster **Materiaal aanpassen** weergegeven, waarin de medewerker de gewenste wijzigingen kan aanbrengen. Wanneer het dialoogvenster wordt geopend, wordt een orderverzamellijst voor productie met regels voor de aangepaste hoeveelheden gemaakt voor de productieorder. Als de medewerker **Nu boeken** selecteert, wordt de correctie bevestigd en wordt de orderverzamellijst geboekt. Als de medewerker **Annuleren** selecteert, wordt de orderverzamellijst verwijderd en wordt geen correctie aangebracht.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Materiaalverbruik voor artikelen met een catch weight aanpassen

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Werknemers kunnen het materiaalverbruik voor artikelen met een catch weight aanpassen. Deze functionaliteit wordt gebruikt in gevallen waarin de werkelijke hoeveelheid van een catch weight-materiaal dat door een productietaak is verbruikt, meer of minder was dan de geplande hoeveelheid. Daarom moet u deze aanpassen om de voorraadniveaus actueel te houden. Wanneer een werknemer het verbruik van een catch weight-artikel per product aanpast, kunnen ze zowel de catch weight-hoeveelheid als de voorraadhoeveelheid aanpassen. Als een productietaak bijvoorbeeld is gepland voor het verbruik van vijf dozen met een geraamd gewicht van 2 kilogram per doos, kan de werknemer zowel het aantal dozen dat moet worden verbruikt als het gewicht van de dozen aanpassen. Het systeem valideert of het opgegeven gewicht van de dozen binnen de gedefinieerde minimum- en maximumdrempel valt die voor het vrijgegeven product is gedefinieerd.

### <a name="reserve-materials"></a>Materialen reserveren

In het dialoogvenster **Materiaal aanpassen** kan een medewerker materiaalreserveringen maken en aanpassen door **Materiaal reserveren** te selecteren. In het dialoogvenster **Materiaal reserveren** dat verschijnt, wordt de fysiek beschikbare voorraad voor het artikel weergegeven voor elke opslag- en traceringsdimensie.

Als het materiaal is ingeschakeld voor magazijnbeheerprocessen (WMS), bevat de lijst alleen de fysiek beschikbare voorraad voor de productie-invoerlocatie voor het materiaal. De productie-invoerlocatie wordt gedefinieerd voor de resource waar de productietaak is gepland. Als het artikelnummer een batch- of serienummer is, wordt de volledige lijst met fysiek beschikbare batch- en serienummers weergegeven. Als u een te reserveren hoeveelheid wilt opgeven, kan de medewerker **Materiaal reserveren** selecteren . Als u een bestaande reservering wilt verwijderen, kan de medewerker **Reservering verwijderen** selecteren .

Zie voor meer informatie over het instellen van de productie-invoerlocatie het volgende blogbericht: [De productie-invoerlocatie instellen](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> Reserveringen die een medewerker maakt in het dialoogvenster **Materiaal reserveren** blijven behouden wanneer de medewerker **Annuleren** selecteert in het dialoogvenster **Voortgang rapporteren** of **Uitval rapporteren**.
>
> Het is niet mogelijk reserveringen voor artikelen met een catch weight aan te passen.

## <a name="completing-a-job-and-starting-a-new-job"></a>Een taak voltooien en een nieuwe taak starten

Meestal voltooien werknemers een taak door een of meer huidige taken te selecteren op het tabblad **Actieve taken** en vervolgens **Voortgang rapporteren** te selecteren. Vervolgens voeren ze de hoeveelheid in die is geproduceerd (de goede hoeveelheid) en stellen ze de status in op *Voltooid*. Als er meer dan één taak is geselecteerd, gebruikt een werknemer de knoppen **Vorige** en **Volgende** om tussen de taken te schakelen. Om een nieuwe taak te starten, selecteren werknemers deze op het tabblad **Alle taken** en selecteren ze vervolgens **Taak starten**.

Een werknemer kan ook een nieuwe taak starten terwijl de vorige taak nog is geopend. De werknemer selecteert nogmaals de nieuwe taak op het tabblad **Alle taken** en selecteert vervolgens **Taak starten**. In dit geval worden werknemers in het dialoogvenster **Taak starten** echter geïnformeerd dat ze momenteel werken aan een taak en dat ze de taak dus moeten stoppen of voltooien voordat ze de nieuwe taak starten.

## <a name="working-on-multiple-jobs-in-parallel"></a>Gelijktijdig aan meerdere taken werken

Eén werknemer kan tegelijkertijd aan meerdere taken werken (parallel). In dit geval wordt de verzameling taken waaraan de werknemer werkt, een *taakbundel* genoemd. De werknemer kan nieuwe taken aan de bundel toevoegen of een of meer taken in de bundel voltooien. De volgende twee scenario's laten zien hoe een werknemer parallel aan taken kan werken.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Scenario 1: een werknemer die geen actieve taken heeft, wil twee taken starten en er gelijktijdig aan werken

De werknemer selecteert de twee taken op het tabblad **Alle taken** en selecteert vervolgens **Taak starten**. In het dialoogvenster **Taak starten** worden beide geselecteerde taken weergegeven en kan de werknemer de hoeveelheid aanpassen om met elke taak te beginnen. De werknemer bevestigt vervolgens het dialoogvenster en kan beide taken starten.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Scenario 2: een werknemer die twee actieve taken heeft die in uitvoering zijn, wil een derde taak starten en er gelijktijdig met de andere twee taken aan werken.

De werknemer selecteert de derde taak op het tabblad **Alle taken** en selecteert vervolgens **Bundelen**. In het dialoogvenster **Bundelen** kan de werknemer de hoeveelheid aanpassen om te starten. De werknemer bevestigt vervolgens het dialoogvenster door **Bundelen** te selecteren.

## <a name="working-on-indirect-activities"></a>Werken aan indirecte activiteiten

Indirecte activiteiten zijn activiteiten die niet direct zijn gerelateerd aan een productieorder. Indirecte activiteiten kunnen flexibel worden gedefinieerd, zoals wordt beschreven in [Indirecte activiteiten instellen voor tijd en aanwezigheid](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Bijvoorbeeld: Shannon, een werkvloermedewerker bij Contoso, wil deelnemen aan een bedrijfsvergadering en vergaderingen worden beschouwd als een indirecte activiteit. Een van de volgende twee scenario's is van toepassing:

- **Shannon werkt aan een of meer actieve taken.** Shannon selecteert **Activiteit**, identificeert de activiteit (vergadering) en bevestigt haar selectie. Er wordt een bericht weergegeven met de melding dat ze taken heeft die in uitvoering zijn. In het bericht kan Shannon ervoor kiezen om de taken waarmee ze bezig is, te voltooien of te stoppen voordat ze naar de vergadering gaat.
- **Shannon heeft geen actieve taken.** Shannon selecteert **Activiteit**, identificeert de activiteit (vergadering) en ze bevestigt haar selectie. Ze is nu geregistreerd als aanwezig bij de vergadering.

In beide scenario's gaat Shannon nadat ze de selectie heeft bevestigd, naar de aanmeldingspagina of naar een pagina die wacht tot ze bevestigt dat ze van haar indirecte activiteit is teruggekeerd. De pagina die wordt weergegeven, is afhankelijk van de configuratie van de uitvoeringsinterface van de werkvloer. (Zie [Uitvoeringsinterface van de werkvloer configureren](production-floor-execution-configure.md) voor meer informatie.)

## <a name="registering-breaks"></a>Pauzes registreren

Werknemers kunnen pauzes registreren. Pauzes kunnen flexibel worden gedefinieerd, zoals wordt beschreven in [Salaris op basis van registraties](pay-based-on-registrations.md).

Een werknemer registreert een pauze door **Pauze** te selecteren en vervolgens de kaart te selecteren waarmee het type pauze (bijvoorbeeld lunch) wordt vertegenwoordigd. Nadat de werknemer de selectie heeft bevestigd, wordt op het apparaat de aanmeldingspagina weergegeven of een pagina die wacht op bevestiging van de werknemer dat hij/zij van de pauze is teruggekeerd. De pagina die wordt weergegeven, is afhankelijk van de configuratie van de uitvoeringsinterface van de werkvloer. (Zie [Uitvoeringsinterface van de werkvloer configureren](production-floor-execution-configure.md) voor meer informatie.)

## <a name="view-the-my-day-dialog"></a>Het dialoogvenster Mijn dag weergeven

Het dialoogvenster **Mijn dag** biedt werknemers een overzicht van hun registraties en saldi. Het dialoogvenster bestaat uit de volgende drie secties:

- In de hoofdsectie staan de registraties die de huidige werknemer op een geselecteerde datum heeft gedaan. Het wordt geopend met registraties voor de huidige dag en bevat een datumkiezer waarmee de werknemer andere dagen kan weergeven.
- In de sectie **Laatst berekend dagelijks saldo** worden de huidige saldi van de werknemer getoond voor betaalde tijd, betaalde overuren, verzuim en betaald verzuim. Deze waarden zijn gebaseerd op de registraties die zijn berekend tijdens het goedkeuringsproces.
- De sectie **Saldi** geeft een overzicht van de saldi binnen een gedefinieerde periode voor geselecteerde categorieën registraties (zoals verlof, standaardtijd en overuren). Deze saldi zijn gebaseerd op de manier waarop statistische saldi zijn geconfigureer in de module **Tijd en aanwezigheid**. Meer informatie over het configureren van deze opties vindt u in [Verlofsaldi tonen in de uitvoeringsinterface voor de werkvloer](production-floor-execution-payroll-stats.md).

Beheerders kunnen deze functie toevoegen aan de interface door de knop **Mijn dag** op een werkbalk te plaatsen voor elk relevant tabblad, zoals beschreven in [De uitvoeringsinterface voor de werkvloer ontwerpen](production-floor-execution-tabs.md).

## <a name="working-in-teams"></a>Werken in teams

Wanneer meerdere werknemers aan dezelfde productietaak zijn toegewezen, kunnen ze een team vormen. Het team kan één werknemer aanwijzen als leider. De overige werknemers worden automatisch assistenten van die leider. Voor het team dat hierdoor ontstaat, moet alleen de leider de taakstatus registreren. Tijdregistraties gelden voor alle teamleden.

### <a name="prerequisites"></a>Vereisten

Als u teams wilt gebruiken, moet een beheerder de actie **Assistent** inschakelen voor de primaire werkbalk op het tabblad **Alle taken** van de uitvoeringsinterface voor de werkvloer. Zie [Uitvoeringsinterface voor de productievloer ontwerpen](production-floor-execution-tabs.md) voor instructies.

### <a name="form-a-new-team-that-has-a-pilot-and-an-assistant"></a>Een nieuw team vormen met een leider en een assistent

Een werknemer kan zich registreren als assistent door **Assistent** te selecteren op het tabblad **Alle taken**. Als dan het dialoogvenster **Selecteer een werknemer om te assisteren** wordt geopend, kan de werknemer een leider selecteren in een lijst met werknemers die actief aan een taak werken. Nadat de werknemer de selectie heeft bevestigd, wordt hij of zij assistent van de geselecteerde werknemer en wordt deze de leider van het nieuwe team.

### <a name="assign-a-new-pilot-to-an-existing-team"></a>Een nieuwe leider toewijzen aan een bestaand team

Als een team een nieuwe leider wil selecteren, moet de huidige leider een andere werknemer in het team voordragen als de nieuwe leider. Om een nieuwe leider te nomineren, selecteert de huidige leider de waarde **Assistent** op het tabblad **Alle taken**. Als dan het dialoogvenster **Leider wijzigen** wordt geopend, kan de leider een nieuwe leider selecteren in een lijst met werknemers die al lid zijn van het team. Nadat de huidige leider de selectie heeft bevestigd, wordt hij of zij helemaal uit het team verwijderd. De voormalige leider kan zich daarna wel weer bij het team aanmelden, als dat nodig is.

### <a name="assistant-clocks-out"></a>Assistent klokt uit

Als een werknemer die werkt als assistent uitklokt, verlaat hij of zij het team. Als de opties **Vaste teams** en **Herstarten bij inklokken** zijn ingesteld op *Ja*, wordt een werknemer die uitklokt automatisch weer aan het team toegevoegd wanneer hij of zij weer inklokt. U vindt deze opties op het tabblad **Algemeen** op de pagina **Parameters voor tijd en aanwezigheid**.

## <a name="opening-instructions"></a>Instructies voor openen

Werknemers kunnen een document openen dat aan een taak is gekoppeld door **Instructies** te selecteren. De knop **Instructies** is alleen beschikbaar als een document aan de taak in de hoofdgegevens is gekoppeld. Een document dat bijvoorbeeld is gekoppeld aan een product op de pagina **Vrijgegeven producten** in Supply Chain Management, kan door werknemers in de uitvoeringsinterface van de werkvloer worden geopend.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Mixed Reality-guides voor HoloLens openen

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) kan werknemers hulp bieden met praktijktraining waarin Mixed Reality wordt gebruikt. U kunt gestandaardiseerde processen definiëren waarin stapsgewijze instructies werknemers begeleiden bij het werken met de gereedschappen en onderdelen die ze nodig hebben en die hen laten zien hoe ze deze gereedschappen moeten gebruiken in werksituaties. Hier is een overzicht van het proces.

1. Elke keer dat een werknemer een takenlijst opent in de uitvoeringsinterface voor de werkvloer, worden in de interface alle relevante guides voor de weergegeven taken gezocht.
1. De werknemer selecteert **Guides** om de lijst met guides weer te geven.
1. De werknemer selecteert een relevante guide in de lijst.
1. In de uitvoeringsinterface van de werkvloer wordt een QR-code voor de geselecteerde guide weergegeven.
1. De werknemer zet een HoloLens op en kijkt naar de QR-code om de guide te starten.
1. De werknemer neemt de guide door om de taak te leren.

Zie [Mixed Reality-guides verschaffen aan werknemers in productie](instruction-guides-in-production-overview.md) voor meer informatie over het maken, toewijzen en gebruiken van guides voor HoloLens.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
