---
title: De uitvoeringsinterface voor de werkvloer configureren
description: In dit artikel wordt beschreven hoe u een of meer configuraties maakt voor de uitvoeringsinterface van de werkvloer. Wanneer u de uitvoeringsinterface van de werkvloer opent, worden automatisch een geselecteerde configuratie en een taakfilter geladen die specifiek zijn voor de browser en het apparaat. In de configuratie stelt u de beleidsregels in die toegepast moeten worden op een specifiek gebruik.
author: johanhoffmann
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7196306b34a72e4c53113dd644f666346f170ed7
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708719"
---
# <a name="configure-the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de werkvloer configureren

[!include [banner](../includes/banner.md)]

Medewerkers op de werkvloer gebruiken de uitvoeringsinterface van de werkvloer om hun dagelijkse werkzaamheden te registreren, bijvoorbeeld wanneer taken worden gestart, feedback over taken wordt geregistreerd, indirecte activiteiten worden geregistreerd en verzuim wordt gerapporteerd. Deze registraties vormen de basis voor het bijhouden van de voortgang en de kosten van productieorders, en voor het berekenen van de basis voor het salaris van de werknemers.

Wanneer u de uitvoeringsinterface van de werkvloer opent, worden automatisch een geselecteerde configuratie en een taakfilter geladen die specifiek zijn voor de browser en het apparaat. In de configuratie stelt u de beleidsregels in die toegepast moeten worden op een specifiek gebruik. Hieronder vindt u een aantal gebruiksvoorbeelden:

- Op een apparaat in de bedrijfshal klokken werknemers in wanneer ze binnenkomen op kantoor en ze klokken uit wanneer ze weer naar huis gaan.
- Op een apparaat op de werkvloer registreren machinewerkers wanneer ze taken starten en voltooien. Ze registreren ook pauzes en indirecte activiteiten.

In dit artikel worden de verschillende opties beschreven voor het configureren van een uitvoeringsinterface voor de werkvloer voor elk apparaat dat op uw locatie wordt gebruikt.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>De uitvoeringsinterface voor de werkvloer en de bijbehorende optionele functies inschakelen

De uitvoeringsinterface voor de werkvloer zelf, plus een aantal optionele instellingen die in dit artikel worden beschreven, moeten voor uw systeem zijn ingeschakeld voordat u ze kunt gebruiken. Gebruik de pagina [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om een of meer van de functies die in de volgende subsecties worden beschreven, in te schakelen.

### <a name="the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de werkvloer

Dit is de primaire functie die in dit artikel wordt beschreven en is een vereiste voor alle andere functies die in deze sectie worden genoemd. Vanaf Supply Chain Management 10.0.25 is dit verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Uitvoering werkvloer* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="generate-license-plates"></a>Nummerplaten genereren

Deze functies maken de functionaliteit voor nummerplaten beschikbaar voor de uitvoeringsinterface voor de werkvloer. Als u ze wilt gebruiken, schakelt u de volgende functies in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in (in deze volgorde):

1. *Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten*<br>(Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht.)
1. *Het automatisch genereren van nummerplaatnummers inschakelen bij het gereedmelden in het apparaat voor taakkaarten*<br>(Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht.)

### <a name="print-labels"></a>Etiketten afdrukken

Deze functies maken de functionaliteit voor het afdrukken van labels beschikbaar voor de uitvoeringsinterface voor de werkvloer. Als u ze wilt gebruiken, schakelt u de volgende functies in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) in (in deze volgorde):

1. *Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten*<br>(Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht.)
1. *Label afdrukken vanaf apparaat voor taakkaart*<br>(Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht.)

### <a name="allow-locking-the-touch-screen"></a>Vergrendeling van het aanraakscherm toestaan

Met deze functie kunnen werknemers het touchscreen vergrendelen, zodat ze deze kunnen opschonen.

Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Functie voor vergrendelen van taakkaartapparaat en taakkaartterminal zodat ze kunnen worden schoongemaakt* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Functionaliteit van activabeheer voor de uitvoeringsinterface voor de werkvloer

Met deze functie voegt u een Activabeheer-tabblad toe aan de interface voor het uitvoeren van productielijnen. Werknemers kunnen dit tabblad gebruiken om een activum te selecteren dat is verbonden met een machineresource die zich in het geselecteerde filter van de takenlijst bevindt. Voor de geselecteerde machineactiva kan de werknemer de status en de staat van het activum uit tellerwaarden weergeven voor maximaal vier geselecteerde tellers.

Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.29 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Functionaliteit van activabeheer voor de uitvoeringsinterface voor de werkvloer* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="job-search"></a>Taak zoeken

Met deze functie kunt u een zoekveld aan de takenlijst toevoegen. Werknemers kunnen een specifieke taak vinden door de taak-ID in te voeren of alle taken voor een specifieke order zoeken door de order-ID in te voeren. Werknemers kunnen de ID invoeren met behulp van een toetsenblok of door een streepjescode te scannen.

Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.29 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Taak zoeken voor de uitvoeringsinterface voor de werkvloer* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="report-on-co-products-and-by-products"></a>Rapport over co- en bijproducten

Met deze functie kunnen werknemers de uitvoeringsinterface voor de werkvloer gebruiken om de voortgang van batchorders te rapporteren. Deze rapportage omvat rapportage over co- en bijproducten.

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Rapport over co- en bijproducten uit de uitvoeringsinterface op de productievloer* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="display-full-serial-batch-and-license-plate-numbers"></a>De weergave van volledige serienummers, batchnummers en nummerplaatnummers

Deze functie biedt een betere ervaring met het weergeven van lijsten met serie-, batch- en nummerplaatnummers in de uitvoeringsinterface van de werkvloer. De weergave verandert van een kaartweergave met een beperkt aantal tekens in een lijstweergave die voldoende ruimte biedt om de volledige waarden weer te geven. De lijst biedt ook de mogelijkheid om naar specifieke nummers te zoeken.

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Volledige serie-, batch- en nummerplaatnummers tonen in de uitvoeringsinterface van de productievloer* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).


Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Volledige serie-, batch- en nummerplaatnummers tonen in de uitvoeringsinterface van de productievloer* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="register-material-consumption"></a>Materiaalverbruik registreren

Met deze functie kunnen werknemers de uitvoeringsinterface voor de werkvloer gebruiken om materiaalverbruik, batchnummers en serienummers te registreren. Sommige fabrikanten, met name fabrikanten in de procesindustrieën, moeten de hoeveelheid verbruikt materiaal voor elke batch of productieorder expliciet registreren. Werknemers kunnen bijvoorbeeld een schaal gebruiken om te wegen hoeveel materiaal tijdens het werk wordt verbruikt. Voor volledige materiaaltraceerbaarheid moeten deze organisaties ook registreren welke batchnummers zijn verbruikt bij de productie van elk product.

Er zijn twee versies van deze functie. Eén functie ondersteunt alleen artikelen die *niet zijn* ingeschakeld om magazijnbeheerprocessen (WMS) te gebruiken. De andere ondersteunt artikelen die *zijn ingeschakeld* om WMS te gebruiken. Als u deze functionaliteit wilt gebruiken, moet u een of meer van de volgende functies in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in deze volgorde) inschakelen, afhankelijk van het feit of er artikelen zijn ingeschakeld voor WMS:

- *Materiaalverbruik registreren in de uitvoeringsinterface van de werkvloer (niet-WMS)*
- *Materiaalverbruik registreren in de uitvoeringsinterface van de productievloer (WMS ingeschakeld)*

> [!IMPORTANT]
> U kunt alleen de functie niet-WMS gebruiken. Als u echter WMS gebruikt, moet u beide functies inschakelen.

### <a name="report-on-catch-weight-items"></a>Rapport over catch weight-artikelen

Werknemers kunnen de uitvoeringsinterface voor de werkvloer gebruiken om de voortgang van batchorders met catch weight-artikelen te rapporteren. Batchorders worden gemaakt op basis van formules die u kunt definiëren zodat ze catch weight-artikelen als formule-artikelen, co- en bijproducten als uitvoer hebben. U kunt ook formuleregels definiëren voor ingrediënten die zijn gedefinieerd voor catch weight. Catch weight-artikelen gebruiken twee maateenheden om de voorraad te volgen: de hoeveelheid catch weight en de voorraadhoeveelheid. In de voedselindustrie kan verplakt vlees bijvoorbeeld worden gedefinieerd als catch weight-artikel, waarbij de catch weight-hoeveelheid wordt gebruikt om het aantal dozen bij te houden en de voorraadhoeveelheid wordt gebruikt om het gewicht van de dozen bij te houden.

Als u deze functionaliteit wilt gebruiken, schakelt u in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) de volgende functie in:

- *Rapport over catch weight-artikelen uit de uitvoeringsinterface van de productievloer*

### <a name="the-my-day-dialog"></a>Het dialoogvenster Mijn dag

Het dialoogvenster **Mijn dag** biedt werknemers een overzicht van hun dagelijkse registraties en actuele saldi voor betaalde tijd, betaalde overuren, verzuim en betaald verzuim.

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *De weergave Mijn dag voor de uitvoeringsinterface voor de werkvloer* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="teams"></a>Teams

Wanneer meerdere werknemers aan dezelfde productietaak zijn toegewezen, kunnen ze een team vormen. Het team kan één werknemer aanwijzen als leider. De overige werknemers worden automatisch assistenten van die leider. Voor het team dat hierdoor ontstaat, moet alleen de leider de taakstatus registreren. Tijdregistraties gelden voor alle teamleden.

Als u deze functionaliteit wilt gebruiken, schakelt u in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) de volgende functie in:

- *Productieteams in de uitvoeringsinterface voor de werkvloer*

### <a name="additional-configuration-in-the-production-floor-execution-interface"></a>Aanvullende configuratie in de uitvoeringsinterface voor de werkvloer

Met deze functie kunt u instellingen voor de volgende functionaliteit toevoegen aan de pagina **Uitvoering productievloer configureren**:

- Automatisch het dialoogvenster **Taak beginnen** openen wanneer een zoekopdracht is voltooid.
- Automatisch het dialoogvenster **Voortgang melden** openen wanneer een zoekopdracht is voltooid.
- De resterende hoeveelheid vooraf invullen in het dialoogvenster **Voortgang melden**.
- Aanpassingen voor materiaalverbruik toestaan vanuit de dialoogvensters **Voortgang melden**. Voor deze functionaliteit is ook de functie *Materiaalverbruik registreren op de uitvoeringsinterface van de werkvloer (niet-WMS)* vereist.
- Zoekopdrachten op project-id mogelijk maken.

Informatie over het gebruik van de instellingen vindt u verderop in dit artikel.

Als u deze functionaliteit wilt gebruiken, schakelt u in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) de volgende functie in:

- *Aanvullende configuratie in de uitvoeringsinterface voor de werkvloer*

## <a name="work-with-production-floor-execution-configurations"></a>Werken met uitvoeringsconfiguraties voor de werkvloer

Als u uitvoeringsconfiguraties voor de werkvloer wilt maken en beheren, gaat u naar **Productiebeheer \> Instellen \> Productie-uitvoering \> Uitvoering werkvloer configureren**. Op de pagina **Uitvoering werkvloer configureren** wordt een lijst met bestaande configuraties weergegeven. Op deze pagina kunt u de volgende acties uitvoeren:

- Selecteer een configuratie voor de werkvloer die in de linkerkolom staat om deze weer te geven en te bewerken.
- Selecteer in het actievenster de optie **Nieuw** om een nieuwe configuratie aan de lijst toe te voegen. Voer vervolgens een naam in het veld **Configuratie** in waarmee de nieuwe configuratie wordt geïdentificeerd. De naam die u invoert, moet uniek zijn voor alle configuraties en u kunt deze later niet bewerken. Voer in het veld **Beschrijving** optioneel een beschrijving van de configuratie in.

Configureer vervolgens de verschillende instellingen van de geselecteerde configuratie, zoals beschreven in de volgende subsecties.

### <a name="the-general-fasttab"></a>Het sneltabblad Algemeen

Op het sneltabblad **Algemeen** vindt u de volgende instellingen:

- **Alleen in- en uitklokken**: stel deze optie in op *Ja* om een vereenvoudigde interface te maken die alleen functionaliteit voor in- en uitklokken biedt. Met deze instelling worden de meeste andere opties op deze pagina uitgeschakeld. U moet eerst alle regels verwijderen uit het sneltabblad **Tabselectie** voordat u deze optie kunt inschakelen.
- **Zoeken inschakelen**: stel deze optie in op *Ja* om een zoekveld op te nemen in de takenlijst. Werknemers kunnen een specifieke taak vinden door de taak-id in te voeren, of alle taken voor een specifieke order zoeken door de order-id in te voeren. Werknemers kunnen de id invoeren met behulp van een toetsenblok of door een streepjescode te scannen.
- **Zoeken op project-id inschakelen**: stel deze optie in op *Ja* om werknemers in staat te stellen te zoeken op project-id (naast taak-id en order-id) in het zoekveld van de uitvoeringsinterface voor de werkvloer. U kunt deze optie alleen op *Ja* instellen als de optie **Zoeken inschakelen** ook is ingesteld op *Ja*.
- **Dialoogvenster voor starten automatisch openen**: Als deze optie in ingesteld op *Ja*, wordt het dialoogvenster **Taak beginnen** automatisch geopend wanneer medewerkers een taak zoekt met behulp van de zoekbalk.
- **Dialoogvenster Voortgang melden automatisch openen**: Als deze optie in ingesteld op *Ja*, wordt het dialoogvenster **Voortgang melden** automatisch geopend wanneer medewerkers een taak zoekt met behulp van de zoekbalk.
- **Materiaal aanpassen inschakelen**: Stel deze optie in op *Ja* als u de knop **Materiaal aanpassen** wilt inschakelen in het dialoogvenster **Voortgang melden**. Medewerkers kunnen op deze knop klikken om materiaalverbruik voor de taak aan te passen.
- **Hoeveelheid rapporteren bij uitklokken**: stel deze optie in op *Ja* om werknemers te vragen om bij het uitklokken feedback te rapporteren over taken die in uitvoering zijn. Als deze optie wordt ingesteld op *Nee*, wordt dit niet aan werknemers gevraagd.
- **Werknemer vergrendelen**: wanneer deze optie is ingesteld op *Nee*, worden werknemers onmiddellijk afgemeld nadat ze een registratie hebben gemaakt (zoals een nieuwe taak). De interface keert dan terug naar de aanmeldingspagina. Als deze optie is ingesteld op *Ja*, blijven werknemers aangemeld bij de uitvoeringsinterface voor de werkvloer. Een werknemer kan zich echter handmatig afmelden, zodat een andere werknemer zich kan aanmelden terwijl de uitvoeringsinterface voor de werkvloer actief blijft onder dezelfde systeemgebruikersaccount. Meer informatie over deze typen accounts vindt u in [Toegewezen gebruikers](config-job-card-device.md#assigned-users).
- **De werkelijke registratietijd gebruiken**: stel deze optie in op *Ja* om de tijd in te stellen voor elke nieuwe registratie die gelijk is aan de exacte tijd waarop de registratie is ingediend door de werknemer. Als deze optie is ingesteld op *Nee*, wordt in plaats daarvan de aanmeldingstijd gebruikt. U stelt deze optie meestal in op *Ja* als u de opties **Werknemer vergrendelen** en/of **Eén werknemer** hebt ingesteld op *Ja*, waarbij werknemers vaak aangemeld blijven gedurende langere perioden.
- **Eén werknemer**: stel deze optie in op *Ja* als slechts één werknemer elke uitvoeringsinterface voor de werkvloer gebruikt waarvoor deze configuratie actief is. Als deze optie is ingesteld op *Ja*, wordt de optie **Werknemer vergrendelen** automatisch ingesteld op *Ja*. Bovendien wordt met deze instelling de vereiste (en de mogelijkheid) voor de werknemer om zich aan te melden met behulp van een badge-id (of een andere vergelijkbare id) verwijderd. In plaats daarvan meldt de werknemer zich aan bij Microsoft Dynamics 365 Supply Chain Management met een systeemgebruikersaccount die is gekoppeld aan een *werknemer met tijdregistratie* (uit de tabel *werknemers*) en wordt op hetzelfde moment aangemeld bij de uitvoeringsinterface voor de werkvloer als die werknemer.
- **Vergrendeling van het aanraakscherm toestaan**: stel deze optie in op *Ja* om werknemers in staat te stellen het aanraakscherm van de uitvoeringsinterface voor de werkvloer te vergrendelen zodat ze deze kunnen schoonmaken. Als deze optie is ingesteld op *Ja*, wordt de knop **Scherm vergrendelen voor schoonmaken** toegevoegd aan de aanmeldingspagina. Wanneer een werknemer deze knop selecteert, wordt het aanraakscherm tijdelijk vergrendeld voor onbedoelde invoer. Er wordt ook een aftellingstimer weergegeven. De werknemer kan het apparaat en het scherm vervolgens veilig schoonmaken. Wanneer de timer is afgelopen, wordt het aanraakscherm automatisch ontgrendeld.
- **Duur schermvergrendeling**: wanneer de optie **Vergrendeling van het aanraakscherm toestaan** is ingesteld op *Ja*, gebruikt u deze optie om het aantal seconden op te geven dat het aanraakscherm moet worden vergrendeld voor schoonmaken. De duur moet tussen 5 en 120 seconden liggen.
- **Nummerplaat genereren**: stel deze optie in op *Ja* om voor elke gereedmelding op de uitvoeringsinterface voor de werkvloer een nieuwe nummerplaat te genereren. Het nummerplaatnummer wordt gegenereerd op basis van een nummerreeks die is ingesteld op de pagina **Parameters voor magazijnbeheer**. Als deze optie is ingesteld op *Nee*, moeten werknemers een bestaande nummerplaat opgeven bij het gereedmelden.
- **Label afdrukken**: stel deze optie in op *Ja* om een nummerplaatlabel af te drukken wanneer de werknemer de uitvoeringsinterface voor de werkvloer gebruikt voor de gereedmelding. De configuratie van het label wordt ingesteld in de documentroutering, zoals wordt beschreven in [Labelindelingen voor documentroutering](../warehousing/document-routing-layout-for-license-plates.md).

### <a name="the-tab-selection-fasttab"></a>Het sneltabblad Tabbladselectie

Met de instellingen op het sneltabblad **Tabbladselectie** kunt u kiezen welke tabbladen moeten worden weergegeven in de uitvoeringsinterface voor de werkvloer wanneer de huidige configuratie actief is. U kunt zoveel tabbladen ontwerpen als u nodig hebt en deze vervolgens toevoegen en rangschikken zoals u wilt, door middel van de knoppen op de werkbalk van het sneltabblad. Meer informatie over het ontwerpen van tabbladen en het werken met de instellingen vindt u in [De uitvoeringsinterface voor de werkvloer ontwerpen](production-floor-execution-tabs.md).

### <a name="the-report-progress-fasttab"></a>Het sneltabblad Voortgang melden

Op het sneltabblad **Voortgang melden** vindt u de volgende instellingen:

- **Materiaal aanpassen inschakelen**: Stel deze optie in op *Ja* als u de knop **Materiaal aanpassen** wilt toevoegen aan het dialoogvenster **Voortgang melden**. Medewerkers kunnen op deze knop klikken om materiaalverbruik voor de taak aan te passen.
- **Standaard resterende hoeveelheid**: Stel deze optie in op *Ja* als u de verwachte resterende hoeveelheid voor een productietaak vooraf wilt invullen in het dialoogvenster **Voortgang melden**.

## <a name="clean-up-job-configurations"></a>Taakconfiguraties opschonen

Wanneer de werkvloersupervisor de uitvoeringsinterface van de werkvloer instelt, selecteert hij/zij een configuratie en een taakfilter. Deze selecties worden opgeslagen in een verwijzingstabel in Supply Chain Management en de browser gebruikt een ID die is opgeslagen in een lokale cookie om de juiste rij in die tabel te vinden. In de tabel worden ook de datum en tijd geregistreerd waarop een werknemer bij elk apparaat voor het laatst heeft aangemeld.

Met een batchtaak worden vermeldingen in de verwijzingstabel periodiek opgeschoond voor apparaten die gedurende de laatste 60 dagen geen activiteit hebben geregistreerd. U kunt de vermeldingen ook op elk gewenst moment handmatig opschonen door de volgende stappen uit te voeren.

1. Ga naar **Productiebeheer \> Instellen \> Productie-uitvoering \> Uitvoering werkvloer configureren**.
1. Selecteer in het actievenster de optie **Clientconfiguraties opschonen**.
1. Stel in het dialoogvenster **Clientconfiguratie opschonen** het veld **Aantal dagen** in op het aantal dagen inactiviteit (vóór vandaag) dat u in aanmerking wilt nemen. U verwijdert alle configuraties en aanmeldingsrecords voor apparaten die gedurende die tijd niet actief zijn geweest.
1. Selecteer **OK** om de relevante configuraties op basis van de instelling **Aantal dagen** op te schonen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
