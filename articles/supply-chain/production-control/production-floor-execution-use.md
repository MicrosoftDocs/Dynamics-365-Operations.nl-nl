---
title: Hoe werknemers de uitvoeringsinterface voor de werkvloer gebruiken
description: In dit onderwerp wordt beschreven hoe de uitvoeringsinterface van de werkvloer moet worden gebruikt vanuit het perspectief van een werknemer.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 40c6794fdf25da44a75aba4a502a89966c0ec4d0
ms.sourcegitcommit: f27f5d07c040bdca1bcd616f5d3f2320d3b3337e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2020
ms.locfileid: "4425753"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Hoe werknemers de uitvoeringsinterface voor de werkvloer gebruiken

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

De uitvoeringsinterface van de werkvloer is geoptimaliseerd voor aanraakinteractie. Het ontwerp biedt een visueel contrast dat voldoet aan de toegankelijkheidsvereisten voor werkvloeromgevingen. Het biedt dezelfde functionele mogelijkheden als het taakkaartapparaat. Het biedt echter ook de mogelijkheid om meerdere taken tegelijk te starten vanuit een takenlijst. (Deze mogelijkheid wordt ook wel *bundeling van taken* genoemd.) Bovendien kunnen werknemers via een takenlijst een guide openen die is gemaakt in Microsoft Dynamics 365 Guide. Op deze manier kunnen zij visuele instructies krijgen voor een HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Als werknemer aanmelden bij de uitvoeringsinterface van de werkvloer

Voordat werknemers het apparaat kunnen gaan gebruiken, moet een supervisor of technisch personeel het apparaat voorbereiden en de juiste pagina openen in Dynamics 365 Supply Chain Management. Zie [Een apparaat instellen voor het uitvoeren van de uitvoeringsinterface van de werkvloer](production-floor-execution-setup.md) voor meer informatie over het instellen van het apparaat.

Nadat het apparaat is voorbereid, wordt de aanmeldingspagina erop weergegeven. Deze pagina bevat informatie over de status van taken voor de lokale werkcel. Deze informatie wordt periodiek bijgewerkt. Op de pagina gebruiken werknemers hun badge-id's voor aanmelding. Hoewel werknemers geen gebruikersaccount hoeven te hebben voor Supply Chain Management, moeten ze een account voor *werknemer met tijdregistratie* hebben die ze kunnen gebruiken wanneer ze zich aanmelden.

![Aanmeldingspagina van de uitvoeringsinterface voor de werkvloer](media/pfei-sign-in-page.png "Aanmeldingspagina van de uitvoeringsinterface voor de werkvloer")

In de overige secties van dit onderwerp wordt beschreven hoe werknemers met de interface werken.

## <a name="all-jobs-tab"></a>Tabblad Alle taken

Op het tabblad **Alle taken** vindt u een takenlijst waarin alle productietaken worden weergegeven met de status *Niet gestart*, *Gestopt* of *Gestart*.

![Tabblad Alle taken](media/pfei-all-jobs-tab.png "Tabblad Alle taken")

De takenlijst heeft de volgende kolommen. (De nummers komen overeen met de nummers in de vorige afbeelding.)

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

![Tabblad Actieve taken](media/pfei-active-jobs-tab.png "Tabblad Actieve taken")

De takenlijst op het tabblad **Actieve taken** heeft de volgende kolommen:

- **Selectiekolom**: in de linkerkolom worden vinkjes gebruikt om taken aan te duiden die door de werknemer zijn geselecteerd. Werknemers kunnen meerdere taken tegelijk selecteren in de lijst. Als u alle taken in de lijst wilt selecteren, selecteert u het vinkje in de kolomkop. Als één taak is geselecteerd, worden details over die taak weergegeven in het onderste gedeelte van de pagina.
- **Order**: in deze kolom wordt het productieordernummer voor een taak weergegeven.
- **Omschrijving**: in deze kolom wordt een omschrijving gegeven van de bewerking waarvan een taak deel uitmaakt.
- **Aangevraagd**: in deze kolom wordt de hoeveelheid weergegeven die voor een taak is gepland om te produceren.
- **Gestart**: deze kolom bevat de hoeveelheid die al is gestart voor een taak.
- **Voltooid**: deze kolom bevat de hoeveelheid die al is voltooid voor een taak.
- **Buiten gebruik gesteld**: deze kolom bevat de hoeveelheid die al buiten gebruik is gesteld voor een taak.
- **Resterend**: in deze kolom wordt de hoeveelheid weergegeven die nog moet worden voltooid voor een taak.

## <a name="starting-and-completing-production-jobs"></a>Productietaken starten en voltooien

Werknemers starten een productietaak door een taak te selecteren op het tabblad **Alle taken** en vervolgens **Taak starten** te selecteren om het dialoogvenster **Taak starten** te openen.

![Dialoogvenster Taak starten](media/pfei-start-job-dialog.png "Dialoogvenster Taak starten")

Werknemers gebruiken het dialoogvenster **Taak starten** om de productiehoeveelheid te bevestigen en vervolgens de taak te starten. Werknemers kunnen de hoeveelheid aanpassen door het veld **Hoeveelheid** te selecteren en vervolgens het numerieke toetsenbord te gebruiken dat wordt weergegeven. Werknemers selecteren vervolgens **Starten** om aan de taak te gaan werken. Het dialoogvenster **Taak starten** wordt gesloten en de taak wordt toegevoegd aan het tabblad **Actieve taken**.

Werknemers kunnen een taak met een willekeurige status starten. Wanneer een werknemer een taak start die de status *Niet gestart* heeft , wordt in het veld **Hoeveelheid** in het dialoogvenster **Taak starten** in eerste instantie de volledige hoeveelheid weergegeven. Wanneer een werknemer een taak start die de status *Gestart* of *Gestopt* heeft , wordt in het veld **Hoeveelheid** in eerste instantie de resterende hoeveelheid weergegeven.

## <a name="reporting-good-quantities"></a>Goede hoeveelheden rapporteren

Wanneer werknemers een taak voltooien of gedeeltelijk voltooien, kunnen ze goede hoeveelheden rapporteren die zijn geproduceerd door een taak te selecteren op het tabblad **Actieve taken** en vervolgens **Voortgang rapporteren** te selecteren. Vervolgens voert de werknemer in het dialoogvenster **Voortgang rapporteren** de goede hoeveelheid in met het numerieke toetsenbord. De hoeveelheid is standaard leeg. Nadat een hoeveelheid is ingevoerd, kan de werknemer de status van de taak bijwerken naar *In uitvoering*, *Gestopt* of *Voltooid*.

![Dialoogvenster Voortgang rapporteren](media/pfei-report-progress-dialog.png "Dialoogvenster Voortgang rapporteren")

## <a name="reporting-scrap"></a>Uitval rapporteren

Wanneer werknemers een taak voltooien of gedeeltelijk voltooien, kunnen ze uitval rapporteren door een taak te selecteren op het tabblad **Actieve taken** en vervolgens **Uitval rapporteren** te selecteren. Vervolgens voert de werknemer in het dialoogvenster **Uitval rapporteren** de uitvalhoeveelheid in met het numerieke toetsenbord. De werknemer selecteert ook een reden (*Geen*, *Machine*, *Operator* of *Materiaal*).

![Dialoogvenster Uitval rapporteren](media/pfei-report-scrap-dialog.png "Dialoogvenster Uitval rapporteren")

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

Indirecte activiteiten zijn activiteiten die niet direct zijn gerelateerd aan een productieorder. Indirecte activiteiten kunnen flexibel worden gedefinieerd, zoals wordt beschreven in [Indirecte activiteiten instellen voor tijd en aanwezigheid](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Bijvoorbeeld: Shannon, een werkvloermedewerker bij Contoso, wil deelnemen aan een bedrijfsvergadering en vergaderingen worden beschouwd als een indirecte activiteit. Een van de volgende twee scenario's is van toepassing:

- **Shannon werkt aan een of meer actieve taken.** Shannon selecteert **Activiteit**, identificeert de activiteit (vergadering) en bevestigt haar selectie. Er wordt een bericht weergegeven met de melding dat ze taken heeft die in uitvoering zijn. In het bericht kan Shannon ervoor kiezen om de taken waarmee ze bezig is, te voltooien of te stoppen voordat ze naar de vergadering gaat.
- **Shannon heeft geen actieve taken.** Shannon selecteert **Activiteit**, identificeert de activiteit (vergadering) en ze bevestigt haar selectie. Ze is nu geregistreerd als aanwezig bij de vergadering.

In beide scenario's gaat Shannon nadat ze de selectie heeft bevestigd, naar de aanmeldingspagina of naar een pagina die wacht tot ze bevestigt dat ze van haar indirecte activiteit is teruggekeerd. De pagina die wordt weergegeven, is afhankelijk van de configuratie van de uitvoeringsinterface van de werkvloer. (Zie [Uitvoeringsinterface van de werkvloer configureren](production-floor-execution-configure.md) voor meer informatie.)

## <a name="working-on-breaks"></a>Werken in pauzes

Werknemers kunnen pauzes registreren. Pauzes kunnen flexibel worden gedefinieerd, zoals wordt beschreven in [Salaris op basis van registraties](pay-based-on-registrations.md).

Een werknemer registreert een pauze door **Pauze** te selecteren en vervolgens de kaart te selecteren waarmee het type pauze (bijvoorbeeld lunch) wordt vertegenwoordigd. Nadat de werknemer de selectie heeft bevestigd, wordt op het apparaat de aanmeldingspagina weergegeven of een pagina die wacht op bevestiging van de werknemer dat hij/zij van de pauze is teruggekeerd. De pagina die wordt weergegeven, is afhankelijk van de configuratie van de uitvoeringsinterface van de werkvloer. (Zie [Uitvoeringsinterface van de werkvloer configureren](production-floor-execution-configure.md) voor meer informatie.)

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