---
title: De gebruikerservaring aanpassen
description: In dit onderwerp wordt uitgelegd hoe u de app kunt aanpassen.
author: jasongre
manager: AnnBe
ms.date: 10/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 124609041163bbcaf1b86a6964fa3f56fcd8f755
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658755"
---
# <a name="personalize-the-user-experience"></a>De gebruikerservaring aanpassen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u de app kunt aanpassen.

Er zijn drie basisklassen van persoonlijke instellingen.

- Aanpassingen die zijn aangebracht op een instellingspagina. Voorbeelden zijn kleurenthema en tijdzone.
- Aanpassingen die samenhangen met het gebruik van de pagina. Deze aanpassingen worden *impliciete* aanpassingen genoemd Zo houdt het systeem bijvoorbeeld de breedte van rasterkolommen bij als u deze aanpast, en de status van uitgevouwen of samengevouwen sneltabbladen.
- Aanpassingen die een gebruiker aanbrengt om de weergave van een pagina te wijzigen door te wijzigen hoe een element op die pagina wordt weergegeven of werkt, vaak door een interactieve aanpassingsmodus. Deze aanpassingen worden *expliciete* aanpassingen genoemd De gebruiker kan bijvoorbeeld elementen op de pagina toevoegen, verbergen of opnieuw ordenen.

Alle aanpassingen die een gebruiker aanbrengt, zijn alleen voor die gebruiker, ongeacht het type aanpassing of het bedrijf waarmee de gebruiker op dat moment communiceert. De wijzigingen die een gebruiker op een pagina aanbrengt, beïnvloeden andere gebruikers in het systeem niet.

## <a name="system-wide-options-for-the-current-user"></a>Opties in het hele systeem voor de huidige gebruiker

De pagina **Gebruikersopties** bevat enkele algemene instellingen voor de huidige gebruiker. Als u de pagina **Gebruikersopties** wilt openen, selecteert u de knop **Instellingen** (het tandwielsymbool) op de navigatiebalk en selecteert u **Gebruikersopties**. De pagina **Gebruikersopties** bevat vier tabbladen met verschillende gebruikersinstellingen:

- **Zichtbaar:** selecteer een kleurenthema en de standaardgrootte van elementen op pagina's.
- **Voorkeuren**: selecteer standaardwaarden die elke keer dat u het systeem opent, worden gebruikt. Deze waarden zijn het bedrijf, de eerste pagina en de standaardmodus voor weergeven/bewerken. (De modus voor weergeven/bewerken bepaalt of een pagina is vergrendeld voor weergave of geopend voor bewerking steeds als u deze opent.) Dit tabblad bevat ook opties voor de taal, de tijdzone en datum, tijd en getalnotaties. Ten slotte bevat dit tabblad verschillende voorkeuren die variëren van versie tot versie.
- **Rekening:**: pas uw gebruikersnaam en andere rekeningopties aan.
- **Werkstroom**: werkstroomgerelateerde opties selecteren.

Naast het wijzigen van de gebruikersinstellingen kunt u uw gebruiksgegevens en persoonlijke instellingen bekijken en verwijderen door te klikken op de pagina **Gebruiksgegevens**. Selecteer **Gebruiksgegevens** in het actievenster.

Wanneer u de app gebruikt, worden veel van uw selecties opgeslagen, zodat het systeem voor u de volgende keer gemakkelijker te gebruiken is. Op het tabblad **Aanpassing** kunt u de persoonlijke wijzigingen die u hebt aangebracht in de pagina's in het systeem weergeven en beheren. Op dit tabblad kunt u ook de functietoelichtingen opnieuw instellen (dat wil zeggen: de pop-upvensters met informatie over nieuwe systeemfuncties). Vervolgens krijgt u opnieuw meldingen bij eerder uitgebrachte functies.

> [!NOTE]
> Als de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld, kunt u uw persoonlijke instellingen weergeven en beheren door **Aanpassing** te selecteren in het actievenster op de **pagina Gebruikersopties**.

## <a name="implicit-personalizations"></a>Impliciete aanpassingen

Impliciete aanpassingen zijn aanpassingen die u eenvoudig aanbrengt door met bepaalde besturingselementen te werken die hun huidige zichtbare status opslaan.

- **Rasterkolommen:** u kunt de breedte van een kolom in een raster aanpassen door de formaatbalk links of rechts van de kolomkop te selecteren en deze naar links of rechts te schuiven totdat de kolom de gewenste breedte heeft. De app slaat de breedte op die u instelt voor een kolom. De kolom krijgt die grootte steeds wanneer u de volgende keer de pagina met dat raster opent.
- **Sneltabbladen**: sommige pagina's bevatten uitvouwbare secties genaamd *sneltabbladen*. De app bevat gegevens over de sneltabbladen die u hebt uitgevouwen en samengevouwen. Vervolgens worden elke keer dat u de pagina opent, dezelfde sneltabbladen uitgevouwen of samengevouwen, gebaseerd op uw laatste interactie met de pagina. In sommige gevallen kunt u de systeemprestaties helpen verbeteren door een sneltabblad samen te vouwen, omdat de app de gegevens voor sneltabbladen pas op hoeft te halen als ze worden uitgevouwen. Zoals later in dit onderwerp wordt uitgelegd kunt u ook de volgorde wijzigen van de sneltabbladen op een pagina.
- **Feitenvakken**: sommige pagina's hebben een deelvenster **Verwante informatie** waarin alleen-lezen informatie wordt weergegeven over het huidige onderwerp van de pagina. Elke sectie in het deelvenster **Verwante informatie** wordt een *feitenvak* genoemd. U kunt het deelvenster **Verwante informatie** uitvouwen of samenvouwen en u kunt ook afzonderlijke feitenvakken uitvouwen of samenvouwen. De app slaat deze voorkeuren op. Wanneer u de volgende keer de pagina opent, zijn het deelvenster **Verwante informatie** en de afzonderlijke feitenvakken uitgevouwen of samengevouwen op basis van uw laatste interactie met de pagina. In sommige gevallen kunt u de systeemprestaties helpen verbeteren door een feitenvak samen te vouwen, omdat de app de gegevens voor feitenvakken pas op hoeft te halen als ze worden uitgevouwen.
- **Actievensters**: een *actievenster* wordt weergegeven boven aan de meeste pagina's. Het actievenster bevat knoppen voor een groot aantal van de acties die u op de huidige pagina uitvoeren kunt. Deze knoppen zijn vaak geordend op tabbladen. U kunt het gehele actievenster open vastzetten of u kunt het standaard samengevouwen laten. Vervolgens worden elke keer dat u de pagina opent, is het actievenster geopend of samengevouwen, gebaseerd op uw laatste interactie met de pagina. Als u het actievenster open hebt vastgemaakt, wordt het laatst gebruikte tabblad weergegeven.
- **Snelfilters**: een *snelfilter* wordt boven aan veel rasters weergegeven. Met het snelfilter kunt u het raster filteren op basis van een kolom die u selecteert. De app slaat de kolom op waarop u hebt gefilterd. De volgende keer dat u de pagina opent die het raster bevat, wordt het raster op dezelfde kolom gefilterd. U kunt vervolgens echter een andere kolom selecteren om het raster op te filteren.
- **Kolomkopfilters**: wanneer u een raster filtert met behulp van *kolomkopfilters*, kunt u de filteroperator indien nodig wijzigen om de gegevens te vinden die u zoekt. U kunt de operator bijvoorbeeld wijzigen van **begint met** in **is exact**. Telkens wanneer u een koptekstfilter gebruikt en de filteroperator wijzigt, slaat de app de wijziging op. Vervolgens wordt de filteroperator hersteld wanneer u de volgende keer op die kolom filtert.
- **Navigatievenster**: u kunt het *navigatievenster* openen door de knop **Het navigatiedeelvenster uitvouwen** te selecteren, linksboven op elke pagina. (Deze knop wordt ook wel de _**Menu**knop_, de *hamburger*, het *hamburgermenu* of de *hamburgerknop* genoemd.) U kunt het navigatievenster open vastzetten of u kunt het standaard samengevouwen houden. Nadat u het navigatievenster open hebt vastgezet, houdt de app het open totdat u het samenvouwt.

## <a name="explicit-personalizations"></a>Expliciete aanpassingen

Verschillende mensen en bedrijven beschikken over een ander perspectief op de gegevens die voor hen het belangrijkst zijn en op de gegevens die ze niet nodig hebben voor de manier waarop ze hun bedrijf runnen. U kunt de manier aanpassen waarop uw informatie wordt geordend en ermee wordt gewerkt. U kunt ook opgeven dat bepaalde informatie moet worden verborgen. Deze mogelijkheden zijn belangrijk voor een persoonlijke en productieve ervaring en het zijn voorbeelden van expliciete aanpassingen. Expliciete aanpassingen zijn aanpassingen die u expliciet aanbrengt omdat u de weergave of werking van een element of pagina wilt wijzigen.

### <a name="shortcut-menu-options"></a>Opties in snelmenu

Snelmenu's bevatten een aantal manieren om een pagina expliciet te wijzigen zodat deze beter voldoet aan uw behoeften of de vereisten van uw bedrijf. (Een snelmenu wordt ook wel een *rechtsklikmenu* of *contextmenu* genoemd.)

Sommige van de meest gangbare en belangrijke wijzigingen die in een pagina kunnen worden aangebracht, zijn rechtstreeks als opties in een snelmenu beschikbaar. In platformupdate 17 kunt u bijvoorbeeld met de rechtermuisknop op een kolomkop klikken en **Kolommen toevoegen** of **Kolommen verbergen** selecteren als u kolommen in een raster wilt toevoegen of verbergen.

Bovendien zijn de meest algemene typen expliciete aanpassing beschikbaar door met de rechtermuisknop op een element te klikken en vervolgens **Aanpassen** te selecteren. (Houd er rekening mee dat niet alle elementen op uw pagina kunnen worden aangepast.) Wanneer u deze methode van aanpassing selecteert, ziet u het eigenschappenvenster van het element.

![Eigenschappen van een element aanpassen](./media/personalization-element-properties.png)

U kunt het eigenschappenvenster gebruiken om een element op de volgende manieren aan te passen:

- Het label van het element wijzigen.
- Het element verbergen zodat het niet wordt weergegeven op de pagina. De gegevens in het veld worden niet verwijderd of gewijzigd. De informatie wordt alleen niet meer weergegeven op de pagina.
- De informatie in de samenvattingssectie van het sneltabblad opnemen (als het element zich op een sneltabblad bevindt).
- Sla het veld over zodat het nooit de focus krijgt wanneer u door de pagina navigeert.
- Voorkom dat gegevens in het veld (voor elke record) worden bewerkt.

Het eigenschappenvenster kan andere mogelijkheden voor aanpassing hebben, afhankelijk van het element. Met het eigenschappenvenster van een tegel kunt u de tegel bijvoorbeeld promoveren tot dashboard en met het eigenschappenvenster van een dashboard kunt u mogelijk een nieuwe werkruimte maken op dat dashboard.

### <a name="the-personalization-toolbar"></a>De werkbalk Aanpassing

Als u meerdere wijzigingen in een pagina wilt aanbrengen of wijzigingen wilt doorvoeren die niet beschikbaar zijn via andere mechanismen (zoals de volgorde van elementen wijzigen), kunt u de werkbalk **Aanpassing** gebruiken. Voer een van de volgende stappen uit om de werkbalk **Aanpassing** te openen:

- Selecteer **Dit formulier aanpassen** in het eigenschappenvenster van een element.
- Selecteer **Deze pagina aanpassen** in de groep **Aanpassen** op het tabblad **Opties** van het actievenster van een pagina.
- Selecteer de knop **Instellingen** (het tandwielsymbool) op de navigatiebalk en selecteer **Aanpassen.**

[![Aanpassingswerkbalk](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigeren op de pagina

Wanneer de werkbalk **Aanpassing** is geopend, is de onderliggende pagina alleen-lezen (met andere woorden u kunt de gegevens niet bewerken), maar is deze nog steeds interactief. U kunt het deelvenster **Verwante informatie** uitvouwen of samenvouwen, tabbladen omwisselen en secties uitvouwen of samenvouwen, zoals u deze acties gewoonlijk op de pagina uitvoert. Als u een samenvouwbare sectie of een tabblad wilt aanpassen (bijvoorbeeld om een sneltabblad te verbergen), activeert u de knop die naast die sectie of dat tabblad verschijnt wanneer deze focus krijgt of wanneer u de muisaanwijzer hierop plaatst.

#### <a name="personalization-tools"></a>Aanpassingsprogramma's

De volgende hulpmiddelen zijn beschikbaar op de werkbalk **Aanpassing**:

- Gebruik het hulpmiddel **Selecteren** om de eigenschappen van een element te wijzigen. Als u dit hulpmiddel wilt gebruiken, selecteert u de knop **Selecteren** op de werkbalk en selecteert u vervolgens het gewenste element. Het eigenschappenvenster van het element wordt geopend en kunt u eventuele eigenschappen van dat element wijzigen. U kunt het proces herhalen voor andere elementen die op de pagina kunnen worden aangepast. Sommige aangepaste eigenschappen zijn mogelijk niet in alle scenario's beschikbaar. U kunt bijvoorbeeld geen veld vergrendelen dat vereist is.
- Gebruik het hulpmiddel **Verbergen** om een element op de pagina te verbergen. Als u dit hulpmiddel wilt gebruiken, selecteert u de knop **Verbergen** op de werkbalk en selecteert u vervolgens het element dat u wilt verbergen. Wanneer u het hulpmiddel **Verbergen** gebruikt, worden alle elementen die momenteel verborgen zijn, zichtbaar gemaakt en in een grijze container weergegeven. U kunt een element vervolgens zichtbaar maken door het te selecteren. Als u wilt zien hoe de pagina eruit ziet wanneer er elementen worden verborgen, schakelt u naar een ander aanpassingshulpmiddel.

    U kunt vereiste velden en secties met verplichte velden verbergen. Zo wordt u een vereenvoudigde ervaring geboden waarbij verplichte velden die standaard worden ingevuld op basis van zakelijke logica, niet worden weergegeven. Verborgen vereiste velden worden tijdelijk zichtbaar als deze leeg zijn wanneer een gebruiker de pagina probeert op te slaan.

- Gebruik het hulpmiddel **Een veld toevoegen** om een veld toe te voegen aan uw pagina. Wanneer u dit hulpmiddel gebruikt, kunt u alleen velden toevoegen die deel uitmaken van de paginadefinitie. Zie voor informatie over het maken van nieuwe velden die geen deel uitmaken van de huidige paginadefinitie [Aangepaste velden](user-defined-fields.md). Nadat u de knop **Een veld toevoegen** op de werkbalk hebt geselecteerd, moet u eerst de groep of het gebied selecteren waar u een veld wilt toevoegen. Er wordt een dialoogvenster weergegeven met de lijst met velden die gerelateerd zijn aan de geselecteerde groep of het geselecteerde gebied. Selecteer in het dialoogvenster een of meer velden om toe te voegen en selecteer vervolgens **Invoegen**. Als u een veld wilt verwijderen dat u eerder hebt toegevoegd, herhaalt u de procedure, maar wist u de selectie van het veld in het dialoogvenster.
- Gebruik het hulpmiddel **Verplaatsen** om een element te verplaatsen naar een andere locatie binnen de huidige groep elementen. U kunt een element niet buiten de bovenliggende groep verplaatsen. Als u dit hulpmiddel wilt gebruiken, selecteert u de knop **Verplaatsen** op de werkbalk en selecteert u vervolgens het element dat u wilt verplaatsen. Wanneer u een element selecteert, bepaalt de app de locaties waar het element naartoe kan worden verplaatst. Deze locaties worden *neerzetzones*genoemd. Wanneer u het element binnen de huidige groep versleept, wordt elke neerzetzone weergegeven als een gekleurde vette lijn naast het gebied waar het element kan worden neergezet.
- Gebruik het hulpmiddel **Overslaan** om een element te verwijderen uit de volgorde van de toetsenbordtoets Tab van de pagina. Wanneer u de knop **Overslaan** op de werkbalk selecteert, worden alle elementen die momenteel overgeslagen worden, weergegeven in een grijze container. U kunt velden interactief verwijderen of toevoegen aan de tabvolgorde.
- Gebruik het hulpmiddel **Weergeven in koptekst** als u wilt dat een veld in de samenvattingssectie van het sneltabblad wordt weergegeven. Wanneer u de knop **Weergeven in koptekst** selecteert op de werkbalk, worden alle velden die zijn geselecteerd als overzichtsvelden, weergegeven in een grijze container. U kunt interactief velden toevoegen aan het sneltabbladoverzicht en velden eruit verwijderen door de velden te selecteren.
- Gebruik het hulpmiddel **Vergrendelen** wanneer u een element als bewerkbaar of niet bewerkbaar wilt markeren. Wanneer u de knop **Vergrendelen** op de werkbalk selecteert, worden alle elementen die momenteel niet bewerkbaar zijn, weergegeven in een grijze container. U kunt deze vervolgens weer bewerkbaar maken. Merk op dat sommige velden verplicht zijn en niet niet-bewerkbaar kunnen worden gemaakt. Een hangslot wordt weergegeven naast deze velden.
- Gebruik de knop **Een PowerApp toevoegen** om een app in te sluiten die met Microsoft PowerApps op de pagina is gemaakt. Zie [PowerApps insluiten](embed-power-apps.md) voor gedetailleerde informatie over het insluiten van een PowerApps-app in een pagina.
- Gebruik het hulpmiddel **Wissen** om de pagina weer op de standaard, geïnstalleerde toestand in te stellen. Alle aanpassingen op de huidige pagina worden gewist. Er is geen actie ongedaan maken. Gebruik dit hulpmiddel daarom alleen als u zeker weet dat u de pagina opnieuw wilt instellen.
- Gebruik het hulpmiddel **Importeren** om een aanpassing uit een aanpassingsbestand te laden die u of iemand anders eerder heeft gemaakt. Wanneer u persoonlijke instellingen voor een pagina importeert, kunt u kiezen of deze moeten worden toegevoegd aan of vervangen door alle bestaande persoonlijke instellingen voor de pagina. Er is geen actie ongedaan maken. Nadat u de persoonlijke instellingen hebt geïmporteerd, moet u de gewenste wijzigingen dus handmatig wissen of ongedaan maken.
- Gebruik het hulpmiddel **Exporteren** om uw aanpassingen voor de pagina op te slaan in een bestand. U kunt vervolgens uw aanpassingen delen met andere gebruikers. Deze gebruikers hoeven alleen het bestand te importeren dat uw aanpassingen voor de pagina bevat.
- Selecteer de knop **Sluiten** om de werkbalk **Aanpassing** te sluiten en de pagina terug te brengen naar de vorige interactieve status.

Wanneer de werkbalk **Aanpassing** wordt gebruikt, worden uw aanpassingen normaal gesproken van kracht zodra u ze maakt. Als echter de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld, moet u de persoonlijke instellingen van een door u gekozen weergave expliciet opslaan.

In sommige gevallen ziet u wanneer u een hulpmiddel selecteert een hangslotpictogram naast een element. Dit symbool geeft aan dat u de eigenschappen van het element die zijn gerelateerd aan het geselecteerde hulpmiddel, niet kunt wijzigen omdat wijzigingen in deze eigenschappen voorkomen dat de pagina correct werkt.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Een tegel, lijst of koppeling toevoegen aan een werkruimte

Voor sommige pagina's die lijsten bevatten, is de aanpassingsfunctie **Toevoegen aan werkgebied** beschikbaar in de groep **Aanpassen** op het tabblad **Opties** van het actievenster. Met deze functie kunt u relevante informatie vanuit de huidige lijst in een specifiek werkgebied binnenhalen. De informatie die in het werkgebied wordt weergegeven, kan worden gebaseerd op de gehele lijst of op een gefilterde en gesorteerde versie van de lijst. U kunt ook opgeven of de informatie wordt weergegeven in de werkruimte als een lijst, als een overzichttegel die het aantal artikelen in de lijst kan weergeven, of als een koppeling.

> [!NOTE]
> Als de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld, is de inhoud die u naar een werkgebied verplaatst, rechtstreeks aan een weergave gekoppeld. De query van de weergave wordt gebruikt om gegevens op te halen in het werkgebied. De bijbehorende tegel of koppeling in het werkgebied opent de pagina voor die weergave, zodat de query en de persoonlijke instellingen van de weergave worden toegepast.

[![Toevoegen aan werkgebied](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Als u een lijst aan een werkruimte wilt toevoegen, sorteert of filtert u de lijst op de pagina eerst, zodat deze de informatie bevat zoals u deze wilt weergeven in de werkruimte. (Als de functie Opgeslagen weergaven is ingeschakeld, kunt u pas doorgaan nadat u een weergave met deze voorwaarden hebt opgeslagen.) Selecteer vervolgens **Toevoegen aan werkgebied**. Selecteer een werkruimte en selecteer in het veld **Presentatie** de optie **Lijst**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u de kolommen kunt selecteren die moeten worden weergegeven in de lijst in de werkruimte. Ook kunt u het label opgeven dat wordt gebruikt voor de lijst in de werkruimte.
- Als u een tegel aan een werkruimte wilt toevoegen, filtert u eerst de lijst op de pagina om de gegevens weer te geven waarvan u een overzicht wilt of waartoe u snel toegang wilt. (Als de functie Opgeslagen weergaven is ingeschakeld, kunt u pas doorgaan nadat u een weergave met deze voorwaarden hebt opgeslagen.) Selecteer vervolgens **Toevoegen aan werkgebied**. Selecteer een werkruimte en selecteer in het veld **Presentatie** de optie **Tegel**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u het label kunt opgeven dat moet worden gebruikt voor de tegel in het werkgebied. U kunt ook opgeven of de tegel een telling moet weergeven. Nadat de tegel is toegevoegd aan het werkgebied, kunt u deze selecteren om de huidige pagina te openen vanuit het werkgebied. Vervolgens kunt u de gefilterde lijst bekijken die aan de tegel is gekoppeld.
- Als u een koppeling aan een werkruimte wilt toevoegen, filtert u de lijst op de pagina eerst zodat hier de gegevens worden weergegeven waarin u geïnteresseerd bent. (Als de functie Opgeslagen weergaven is ingeschakeld, kunt u pas doorgaan nadat u een weergave met deze voorwaarden hebt opgeslagen.) Selecteer vervolgens **Toevoegen aan werkgebied**. Selecteer een werkruimte en selecteer in het veld **Presentatie** de optie **Koppeling**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u het label kunt opgeven dat moet worden gebruikt voor de koppeling. U kunt desgewenst ook een label opgeven voor een nieuwe sectie die deze koppeling bevat.

Nadat een lijst, tegel of koppeling is toegevoegd aan een werkgebied, kunt u dit werkgebied openen en de elementen erin op de gewenste manier ordenen.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Een overzicht toevoegen aan een werkruimte of dashboard

Sommige werkruimten bevatten tellingstegels (tegels met getallen erop) en u wilt deze mogelijk ook in uw dashboard laten weergeven. Klik in een werkgebied met de rechtermuisknop op een teltegel, selecteer **Aanpassen** en selecteer vervolgens **Vastmaken op dashboard** in het eigenschappenvenster van de tegel. De volgende keer dat u het geselecteerde dashboard opent en vernieuwt, wordt de telling weergegeven onder de navigatietegel van die werkruimte. U kunt selecteren dat de telling rechtstreeks naar de gegevens gaat die erdoor worden voorgesteld.

### <a name="personalizing-your-dashboard"></a>Het dashboard aanpassen

Het dashboard is vaak de eerste pagina die bij het openen van de app wordt weergegeven. U kunt het dashboard aanpassen, zodat het alleen de werkruimtetegels weergeeft die u wilt zien. U kunt de tegels ook opnieuw schikken zodat ze in de volgorde worden weergegeven waarin u ze wilt zien, de naam van uw werkruimtenavigatietegels wijzigen of een nieuwe werkruimtetegel toevoegen.

Als u het dashboard wilt aanpassen, klikt u met de rechtermuisknop op een tegel en selecteert u **Aanpassen** om het eigenschappenvenster van de tegel te openen.

- Als u de geselecteerde tegel wilt verbergen of hernoemen, kunt u die wijziging rechtstreeks in het eigenschappenvenster aanbrengen.
- Als u de werkruimtetegels opnieuw wilt ordenen, selecteert u **Dit formulier aanpassen** om de werkbalk **Aanpassing** te openen. U kunt vervolgens het hulpmiddel **Verplaatsen** gebruiken om de tegels anders te ordenen.
- Voor meer informatie over het toevoegen van een nieuwe werkgebiedtegel in het eigenschappenvenster selecteert u **Een werkgebied toevoegen**. Een nieuwe werkruimtetegel wordt onder aan het dashboard gemaakt. U kunt deze werkruimtetegel desgewenst hernoemen. U kunt ook lijsten, tegels en koppelingen toevoegen aan de werkruimte, zoals beschreven in de sectie [Lijsten, tegels of koppelingen toevoegen aan werkruimten](#adding-a-tile-list-or-link-to-a-workspace) van dit onderwerp.

## <a name="administration-of-personalizations"></a>Beheer van aanpassingen

Nadat u een pagina hebt aangepast, kunt u uw aanpassingen delen met andere gebruikers door de aangepaste pagina te exporteren. U kunt vervolgens andere gebruikers vragen de aangepaste pagina te openen en het aanpassingsbestand te importeren dat u hebt gemaakt. U kunt ook uw aanpassingen geven aan een gebruiker die beheerdersrechten heeft. Die gebruiker kan het aanpassingsbestand vervolgens toepassen op veel gebruikers tegelijk.

Gebruiker met beheerdersbevoegdheden kunnen ook aanpassingen voor andere gebruikers beheren op de pagina **Aanpassing**.

Voor klanten die de functie [Opgeslagen weergaven](saved-views.md) niet hebben ingeschakeld, bevat deze pagina vier tabbladen:

- **Toepassen**: u kunt een aanpassing voor een of meer gebruikers importeren of selecteren. Als u een aanpassing wilt toepassen op een of meer gebruikers, selecteert u eerst een rol en gebruikers die deze rol hebben. Vervolgens selecteert u een bestaande aanpassing om toe te passen op geselecteerde gebruikers of importeert u een aanpassingsbestand. De aanpassing wordt gevalideerd en toegepast op alle geselecteerde gebruikers. Dit wordt van kracht bij de volgende keer dat ze de geselecteerde pagina openen.
- **Wissen**: u kunt alle aanpassingen voor een pagina of werkgebied voor een of meer gebruikers wissen. Selecteer eerst een pagina of werkruimte voor een overzicht van de gebruikers die deze hebben aangepast. Kies vervolgens de gebruikers waarvoor de aanpassingen voor die pagina moeten worden gewist en selecteer **Wissen**. Alle aanpassingen die de geselecteerde gebruikers hebben toegepast op de geselecteerde pagina of het geselecteerde werkgebied, worden verwijderd. Deze actie kan niet ongedaan worden gemaakt. Als de pagina of het werkgebied echter een opgeslagen aanpassing heeft, kan die aanpassing opnieuw worden geïmporteerd.
- **Gebruikers**: selecteer een gebruiker voor een lijst met de pagina's die de gebruiker heeft aangepast. Vervolgens kunt u in- of uitschakelen of de gebruiker voor bepaalde pagina's of voor het hele systeem aanpassingen kan doorvoeren. U kunt ook een aanpassing importeren, exporteren of wissen voor de gebruiker. Daarnaast kunt u de functietoelichtingen voor de gebruiker opnieuw instellen. Als de gebruiker pop-upvensters die nieuwe functies introduceren, eerder heeft gesloten, worden deze opnieuw weergegeven wanneer de gebruiker de volgende keer de desbetreffende functie tegenkomt.
- **Systeem**: u kunt tijdelijk aanpassingen voor alle gebruikers in het systeem uitschakelen. In dat geval worden alle aanpassingen voor alle gebruikers verwijderd en worden alle pagina's opnieuw ingesteld op de standaardstatus. Als u aanpassingen later weer wilt inschakelen, worden alle aanpassingen opnieuw toegepast. U kunt alle aanpassingen voor alle gebruikers in het systeem ook permanent verwijderen. Er is geen enkele manier om aanpassingen terug te halen die zijn verwijderd. Voordat u deze taak uitvoert, moet u er daarom voor zorgen dat u aanpassingen hebt geëxporteerd die u later mogelijk wilt.

Voor klanten die de functie [Opgeslagen weergaven](saved-views.md) niet hebben ingeschakeld, bevat de pagina **Aanpassing** vijf tabbladen:

- **Gepubliceerde weergaven**: deze weergaven zijn voor uw organisatie gepubliceerd. Als u de gebruikers wilt wijzigen voor wie deze weergaven zijn bedoeld, kunt u de beveiligingsrollen of rechtspersonen wijzigen die aan elke weergave zijn gekoppeld. U kunt ook een of meer gepubliceerde weergaven exporteren of verwijderen.
- **Niet-gepubliceerde weergaven**: deze weergaven zijn sjabloonweergaven die in uw systeem zijn geïmporteerd maar nog niet zijn gepubliceerd. U kunt deze weergaven publiceren, exporteren of verwijderen.
- **Persoonlijke weergaven**: deze weergaven zijn gemaakt door gebruikers in het systeem. U kunt een persoonlijke weergave voor de organisatie publiceren of een of meer van deze weergaven naar andere gebruikers kopiëren. U kunt deze weergaven ook publiceren, exporteren of verwijderen.
- **Gebruikers**: selecteer een gebruiker voor een lijst met de pagina's die de gebruiker heeft aangepast. Vervolgens kunt u in- of uitschakelen of de gebruiker voor bepaalde pagina's of voor het hele systeem aanpassingen kan doorvoeren. U kunt ook een aanpassing importeren, exporteren of wissen voor de gebruiker. Daarnaast kunt u de functietoelichtingen voor de gebruiker opnieuw instellen. Als de gebruiker pop-upvensters die nieuwe functies introduceren, eerder heeft gesloten, worden deze opnieuw weergegeven wanneer de gebruiker de volgende keer de desbetreffende functie tegenkomt.
- **Systeem**: u kunt tijdelijk aanpassingen voor alle gebruikers in het systeem uitschakelen. In dat geval worden alle aanpassingen voor alle gebruikers verwijderd en worden alle pagina's opnieuw ingesteld op de standaardstatus. Als u aanpassingen later weer wilt inschakelen, worden alle aanpassingen opnieuw toegepast. U kunt alle aanpassingen voor alle gebruikers in het systeem ook permanent verwijderen. Er is geen enkele manier om aanpassingen terug te halen die zijn verwijderd. Voordat u deze taak uitvoert, moet u er daarom voor zorgen dat u aanpassingen hebt geëxporteerd die u later mogelijk wilt.

Gebruikers die toegang hebben tot de pagina **Aanpassing** kunnen ook persoonlijke sjablonen of sjabloonweergaven importeren met de knop **Weergaven importeren** in het actievenster.

## <a name="personalizing-inventory-dimensions"></a>Voorraaddimensies aanpassen

Wanneer u de instellingen van de voorraaddimensies op een pagina wilt aanpassen, kunt u de instellingen toepassen die zijn gemaakt met de optie **Dimensie weergeven**. U gebruikt aanpassing bijvoorbeeld om een kolom te verbergen voor de voorraaddimensie Batchnummer, maar de kolom wordt de volgende keer dat de pagina wordt geopend, weergegeven. Deze werking treedt op omdat de **Weergave van dimensies**-instellingen bepalen welke voorraaddimensiekolommen worden weergegeven. De **Weergave van dimensies**-instellingen zijn van toepassing op alle pagina's en hebben voorrang op aangepaste instellingen van voorraaddimensievelden op afzonderlijke pagina's.

Als u in het vorige voorbeeld niet wilt dat de kolom voor de voorraaddimensie Batchnummer wordt weergegeven op een pagina, moet u die dimensie uitschakelen als onderdeel van de optie **Weergave van dimensies** voor die pagina.
