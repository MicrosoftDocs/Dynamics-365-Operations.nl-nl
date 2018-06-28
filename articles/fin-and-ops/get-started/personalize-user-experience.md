---
title: De gebruikerservaring aanpassen
description: In dit onderwerp wordt uitgelegd hoe u Microsoft Dynamics 365 for Finance and Operations kunt aanpassen.
author: TLeforMicrosoft
manager: AnnBe
ms.date: 05/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 862bbf4d1d9b0dc2b6dc418ee766ed4dedef49fe
ms.openlocfilehash: 8ad5bd607f08d4e0b266d86a96a0b7f3e352c4cd
ms.contentlocale: nl-nl
ms.lasthandoff: 05/24/2018

---

# <a name="personalize-the-user-experience"></a>De gebruikerservaring aanpassen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u Microsoft Dynamics 365 for Finance and Operations kunt aanpassen.

Er bestaan drie basisklassen met aanpassingen in Finance and Operations. 
- Aanpassingen aangebracht op een instellingspagina. Voorbeelden zijn kleurenthema en tijdzone.
- Aanpassingen die verband houden met paginagebruik, worden *impliciete* aanpassingen genoemd. Finance and Operations houdt bijvoorbeeld de breedte van rasterkolommen bij als u deze aanpast, en de status van uitgevouwen of samengevouwen sneltabbladen. 
- Aanpassingen die een gebruiker aanbrengt om de weergave van een pagina te wijzigen door te wijzigen hoe een element op die pagina wordt weergegeven of werkt, vaak door een interactieve aanpassingsmodus. Deze aanpassingen worden *expliciete* aanpassingen genoemd De gebruiker kan bijvoorbeeld elementen op de pagina toevoegen, verbergen of opnieuw ordenen.

Alle aanpassingen die een gebruiker aanbrengt in Finance and Operations, zijn alleen voor die gebruiker, ongeacht het type aanpassing of het bedrijf waarmee de gebruiker op dat moment communiceert. De wijzigingen die een gebruiker op een pagina aanbrengt, beïnvloeden andere gebruikers in het systeem niet.

## <a name="system-wide-options-for-the-current-user"></a>Opties in het hele systeem voor de huidige gebruiker
De pagina **Gebruikersopties** bevat enkele algemene instellingen voor de huidige gebruiker. Als u de pagina **Gebruikersopties** wilt openen, selecteert u het menu **Instellingen** (het tandwielsymbool) op de navigatiebalk en selecteert u **Gebruikersopties**. De pagina **Gebruikersopties** bevat vier tabbladen met verschillende gebruikersinstellingen:

- **Zichtbaar:** selecteer een kleurenthema en de standaardgrootte van elementen op pagina's.
- **Voorkeuren**: selecteer standaardwaarden die elke keer dat u Finance and Operations opent, worden gebruikt. Deze waarden zijn het bedrijf, de eerste pagina en de standaardmodus voor weergeven/bewerken. (De modus voor weergeven/bewerken bepaalt of een pagina is vergrendeld voor weergave of geopend voor bewerking steeds als u deze opent.) Dit tabblad bevat ook opties voor de taal, de tijdzone en de datum, tijd en getalnotatie. Ten slotte bevat dit tabblad verschillende voorkeuren die variëren van versie tot versie.
- **Rekening:**: pas uw gebruikersnaam en andere rekeningopties aan.
- **Werkstroom**: werkstroomgerelateerde opties selecteren.

## <a name="implicit-personalizations"></a>Impliciete aanpassingen
Impliciete aanpassingen zijn aanpassingen die u eenvoudig aanbrengt door met bepaalde besturingselementen te werken die hun huidige zichtbare status onthouden.

- **Rasterkolommen:** u kunt de breedte van een kolom in een raster aanpassen door de formaatbalk links of rechts van de kolomkop te selecteren en deze naar links of rechts te schuiven totdat de kolom de gewenste breedte heeft. Finance and Operations slaat de breedte op die u instelt voor een kolom. De kolom krijgt vervolgens die grootte steeds wanneer u de pagina opent die dat raster bevat.
- **Sneltabbladen**: sommige pagina's bevatten uitvouwbare secties genaamd *sneltabbladen*. Finance and Operations bevat gegevens over de sneltabbladen die u hebt uitgevouwen en samengevouwen. Vervolgens worden elke keer dat u terugkeert naar de pagina dezelfde sneltabbladen uitgevouwen of samengevouwen, gebaseerd op uw laatste interactie met de pagina. In sommige gevallen kunt u de systeemprestaties helpen verbeteren door een sneltabblad samen te vouwen, omdat Finance and Operations de gegevens voor dat sneltabblad pas op hoeft te halen als het tabblad is uitgevouwen. Zoals later in dit onderwerp uitgelegd kunt u ook de volgorde wijzigen van de sneltabbladen op een pagina.
- **Feitenvakken**: sommige pagina's hebben een onderdeel dat een *feitenvak* wordt genoemd. Dit deelvenster bevat alleen-lezen gegevens met betrekking tot het huidige onderwerp van de pagina. Elke sectie in het feitenvakvenster wordt een *feitenvak* genoemd. U kunt het hele feitenvakvenster verbergen of weergeven en u kunt ook afzonderlijke feitenvakken uitvouwen of samenvouwen. Finance and Operations slaat uw voorkeuren op. Vervolgens worden elke keer dat u terugkeert naar de pagina, de status van het feitenvak en de afzonderlijke feitenvakken weergegeven op basis van uw laatste interactie met de pagina. In sommige gevallen kunt u de systeemprestaties helpen verbeteren door een feitenvak samen te vouwen, omdat Finance and Operations de gegevens voor dat feitenvak pas op hoeft te halen als het feitenvak is uitgevouwen.
- **Actievensters**: een *actievenster* wordt weergegeven boven aan de meeste pagina's. Het actievenster bevat knoppen voor een groot aantal van de acties die u op de huidige pagina uitvoeren kunt. Deze knoppen zijn vaak geordend op tabbladen. U kunt het gehele actievenster open vastzetten of u kunt het standaard samengevouwen laten. Vervolgens herstelt Finance and Operations de volgende keer dat u de pagina opent, de vastgezette staat van het actievenster. Als het actievenster is open is vastgezet, toont Finance and Operations ook het tabblad met acties die u het laatst hebt gebruikt.
- **Snelfilters**: een *snelfilter* wordt boven aan veel rasters weergegeven. Met het snelfilter kunt u het raster filteren op basis van een kolom die u selecteert. Finance and Operations slaat de kolom op waarop u hebt gefilterd. De volgende keer dat u de pagina opent die het raster bevat, wordt het raster op dezelfde kolom gefilterd. U kunt het raster vervolgens echter op een andere kolom filteren.
- **Kolomkopfilters**: wanneer u een raster filtert met behulp van *kolomkopfilters*, kunt u de filteroperator indien nodig wijzigen om de gegevens te vinden die u zoekt. U kunt de operator bijvoorbeeld wijzigen van **begint met** in **is exact**. Telkens wanneer u een koptekstfilter gebruikt en de filteroperator wijzigt, slaat Finance and Operations de wijziging op. Vervolgens wordt de filteroperator hersteld wanneer u de volgende keer op die kolom filtert.
- **Navigatievenster**: u kunt het *navigatievenster* openen door de knop **Menu** te selecteren, in het linkervenster van een pagina. (De knop **Menu** wordt soms ook wel de *hamburger*, het *hamburgermenu*, of de *hamburgerknop* genoemd.) U kunt het navigatievenster open vastzetten of u kunt het standaard samengevouwen houden. Nadat u het navigatievenster open hebt vastgezet, houdt Finance and Operations het open totdat u het samenvouwt.

## <a name="explicit-personalizations"></a>Expliciete aanpassingen
Verschillende mensen en bedrijven beschikken over een ander perspectief op de gegevens die voor hen het belangrijkst zijn of op de gegevens die ze niet nodig hebben voor de manier waarop ze hun bedrijf runnen. In Finance and Operations kunt u de manier aanpassen waarop uw informatie wordt geordend en ermee wordt gewerkt. U kunt ook opgeven dat bepaalde informatie moet worden verborgen. Deze mogelijkheden zijn belangrijk voor een persoonlijke en productieve ervaring en het zijn voorbeelden van expliciete aanpassingen. Expliciete aanpassingen zijn aanpassingen die u expliciet aanbrengt met de bedoeling de weergave of werking van een element of pagina te wijzigen.

### <a name="shortcut-menu-options"></a>Opties in snelmenu
Snelmenu's bevatten een aantal manieren om een pagina expliciet te wijzigen om deze aan te passen aan uw behoeften of de vereisten van uw bedrijf. (Een snelmenu wordt ook wel een *rechtsklikmenu* of *contextmenu* genoemd.)

Sommige van de meest gangbare en belangrijke wijzigingen die in een pagina kunnen worden aangebracht, zijn rechtstreeks als opties in een snelmenu beschikbaar. Als u bijvoorbeeld kolommen in een raster wilt toevoegen of verbergen, klikt u met de rechtermuisknop op een rasterkolomkop en selecteert u **Kolommen toevoegen** of **Kolommen verbergen**.

Bovendien zijn de meest algemene typen expliciete aanpassing beschikbaar door met de rechtermuisknop op een element te klikken en vervolgens **Aanpassen** te selecteren. (Houd er rekening mee dat niet alle elementen op uw pagina kunnen worden aangepast.) Wanneer u deze methode van aanpassing selecteert, ziet u het eigenschappenvenster van het element.

[![Eigenschappen van een element aanpassen](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg)

U kunt het eigenschappenvenster gebruiken om een element op de volgende manieren aan te passen:

- Het label van het element wijzigen.
- Het element verbergen zodat het niet wordt weergegeven op de pagina. De gegevens in het veld worden niet verwijderd of gewijzigd. De informatie wordt alleen niet meer weergegeven op de pagina.
- De informatie in de samenvattingssectie van het sneltabblad opnemen (als het element zich op een sneltabblad bevindt).
- Het veld overslaan wanneer u op Tab drukt om de velden op de pagina te doorlopen.
- Voorkomen dat gegevens in het veld (voor elke record) worden bewerkt.

Het eigenschappenvenster kan andere mogelijkheden voor aanpassing hebben, afhankelijk van het element. Met het eigenschappenvenster van een tegel kunt u de tegel bijvoorbeeld promoveren tot dashboard en met het eigenschappenvenster van een dashboard kunt u mogelijk een nieuwe werkruimte maken op dat dashboard.

### <a name="the-personalization-toolbar"></a>De werkbalk Aanpassing
Als u elementen wilt verplaatsen of verbergen of verschillende wijzigingen wilt aanbrengen op een pagina, kunt u de werkbalk **Aanpassing** gebruiken. Als u de werkbalk **Aanpassing** wilt openen, selecteert u **Dit formulier aanpassen** in het eigenschappenvenster van een element. U kunt ook **Dit formulier aanpassen** selecteren in de groep **Aanpassen** op het tabblad **Opties** van het actievenster van elke pagina.

[![Aanpassingswerkbalk](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

Terwijl de werkbalk **Aanpassing** open is, is de pagina niet-interactief. U kunt daarom geen gegevens invoeren of secties uit- of samenvouwen. U kunt alleen de elementen van de pagina wijzigen.

De volgende hulpmiddelen zijn beschikbaar op de werkbalk **Aanpassing**:

- Gebruik het hulpmiddel **Selecteren** om de eigenschappen van een element te wijzigen. Selecteer het hulpmiddel **Selecteren** en selecteer het element om de eigenschappen ervan te wijzigen. Wanneer u een element selecteert, wordt het eigenschappenvenster van het element geopend en kunt u eventuele eigenschappen van dat element wijzigen. U kunt het proces herhalen voor andere elementen die op een pagina kunnen worden aangepast. Vanwege de manier waarop bepaalde elementen worden gebruikt, staat Finance and Operations niet toe dat u bepaalde eigenschappen ervan wijzigt. Dus wanneer u een element selecteert, ziet u mogelijk enkele eigenschappen die niet kunnen worden gewijzigd. U kunt bijvoorbeeld geen veld verbergen dat vereist is.
- Gebruik het hulpmiddel **Verplaatsen** om een element te verplaatsen naar een andere locatie binnen de huidige groep elementen. (U kunt een element niet buiten de bovenliggende groep verplaatsen.) Selecteer het hulpmiddel **Verplaatsen** en selecteer vervolgens het element dat u wilt verplaatsen. Wanneer u een element selecteert, scant Finance and Operations de pagina om te bepalen waar het element naartoe kan worden verplaatst. Vervolgens wordt een reeks 'neerzetzones' gemaakt. Terwijl u het element binnen de huidige groep versleept, wordt elke 'neerzetzone' weergegeven als een gekleurde vette lijn naast het gebied waar het element kan worden neergezet.
- Gebruik het hulpmiddel **Verbergen** om een element op de pagina te verbergen. Selecteer het hulpmiddel **Verbergen** en selecteer vervolgens het element dat u wilt verbergen. Wanneer u het hulpmiddel **Verbergen** selecteert, worden alle elementen die momenteel verborgen zijn, zichtbaar gemaakt en in een grijze container weergegeven. U kunt deze vervolgens zichtbaar maken. Als u het hulpmiddel **Selecteren** selecteert, ziet u hoe de pagina eruitziet als de geselecteerde elementen worden verborgen.
- Gebruik het hulpmiddel **Overzicht** als u wilt dat een element in de samenvattingssectie van het sneltabblad wordt weergegeven. Het hulpmiddel Overzicht heeft alleen betrekking op velden in een sneltabbladsectie. Wanneer u het hulpmiddel **Overzicht** selecteert, worden alle velden die zijn geselecteerd als overzichtsvelden, weergegeven in een grijze container. U kunt interactief velden toevoegen aan het sneltabbladoverzicht en velden uit het sneltabbladoverzicht verwijderen door de velden te selecteren.
- Gebruik het hulpmiddel **Overslaan** om een element te verwijderen uit de volgorde van de toetsenbordtoets Tab van de pagina. Wanneer u het hulpmiddel **Overslaan** selecteert, worden alle elementen die momenteel overgeslagen worden, weergegeven in een grijze container. U kunt ze vervolgens weer deel laten uitmaken van de tabvolgorde.
- Gebruik het hulpmiddel **Bewerken** wanneer u een element als bewerkbaar of niet bewerkbaar wilt markeren. Wanneer u het hulpmiddel **Bewerken** selecteert, worden alle elementen die momenteel niet-bewerkbaar zijn, weergegeven in een grijze container. U kunt deze vervolgens weer bewerkbaar maken. Merk op dat sommige velden verplicht zijn en niet niet-bewerkbaar kunnen worden gemaakt. Een hangslot wordt weergegeven naast deze velden.
- Gebruik de knop **Invoegen** om een lijst te zien met elementen die kunnen worden ingevoegd op een pagina.

    - Selecteer het hulpmiddel **Veld** onder **Invoegen** om een veld toe te voegen aan uw pagina. Als u werkt met het hulpmiddel **Veld**, kunt u alleen velden toevoegen die deel uitmaken van de paginadefinitie maar die momenteel niet worden weergegeven op de pagina. Zie voor informatie over het maken van nieuwe velden die geen deel uitmaken van de huidige paginadefinitie [Aangepaste velden](user-defined-fields.md). Nadat u het hulpmiddel **Veld** hebt geselecteerd, moet u eerst de groep of het gebied selecteren waar u een veld wilt toevoegen. Er wordt een dialoogvenster weergegeven met de lijst met velden die gerelateerd zijn aan de geselecteerde groep of het geselecteerde gebied. Selecteer in het dialoogvenster een of meer velden om toe te voegen en selecteer vervolgens **Invoegen**. Als u een veld wilt verwijderen dat u eerder hebt toegevoegd, herhaalt u de procedure, maar wist u de selectie van het veld in het dialoogvenster.
    - Selecteer het hulpmiddel **PowerApp** onder **Invoegen** om een app in te sluiten die met Microsoft PowerApps op de pagina is gemaakt. Zie voor gedetailleerde informatie over het insluiten van een PowerApps-app in een pagina [Ingesloten PowerApps](embed-power-apps.md).

- Selecteer de knop **Beheren** om een lijst met beheeropties te bekijken met betrekking tot alle aanpassingen voor de huidige pagina.

    - Selecteer **Wissen** om de pagina weer op de standaard, geïnstalleerde toestand in te stellen. Alle aanpassingen op de huidige pagina worden gewist. Er is geen actie ongedaan maken. Gebruik deze optie daarom alleen als u zeker weet dat u de pagina opnieuw wilt instellen.
    - Selecteer **Importeren** om een aanpassing uit een aanpassingsbestand te laden die u of iemand anders eerder voor de pagina heeft gemaakt. Alle huidige aanpassingen voor de pagina worden vervangen door de aanpassingen uit het geselecteerde bestand.
    - Selecteer **Exporteren** om uw aanpassingen voor de pagina op te slaan in een bestand. U kunt uw aanpassingen delen met andere gebruikers. Deze gebruikers hoeven alleen het bestand te importeren dat uw aanpassingen voor de pagina bevat.

- Selecteer de knop **Sluiten** om de werkbalk **Aanpassing** te sluiten en de pagina terug te brengen naar de vorige interactieve status.

Wanneer de werkbalk **Aanpassing** wordt gebruikt, zijn opslagbewerkingen impliciet. Uw aanpassingen gaan in zodra u ze maakt en u hoeft geen knop **Opslaan** te selecteren. In sommige gevallen ziet u wanneer u een hulpmiddel selecteert een hangslotpictogram naast een element. Dit symbool geeft aan dat u de eigenschappen van het element die zijn gerelateerd aan het geselecteerde hulpmiddel, niet kunt wijzigen omdat wijzigingen in deze eigenschappen voorkomen dat de pagina correct werkt.

### <a name="adding-a-tile-list-or-link-to-a-workspace"></a>Een tegel, lijst of koppeling toevoegen aan een werkruimte
Voor sommige pagina's met lijsten is een extra aanpassingsfunctie beschikbaar. Met de knop **Toevoegen aan werkruimte** in de groep **Aanpassen** op het tabblad **Opties** van het actievenster kunt u de informatie in de huidige lijst in een bepaalde werkruimte weergeven. U kunt een gefilterde en gesorteerde weergave van de informatie in de werkruimte weergeven of u kunt de standaardweergave weergeven. U kunt ook opgeven of de informatie wordt weergegeven in de werkruimte als een lijst, als een overzichttegel die het aantal artikelen in de lijst kan weergeven, of als een koppeling.

[![Toevoegen aan werkgebied](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Als u een lijst aan een werkruimte wilt toevoegen, sorteert of filtert u de lijst op de pagina eerst, zodat deze de informatie bevat zoals u deze wilt weergeven in de werkruimte. Selecteer vervolgens **Toevoegen aan werkruimte**. Selecteer een werkruimte en selecteer in het veld **Presentatie** de optie **Lijst**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u de kolommen kunt selecteren die moeten worden weergegeven in de lijst in de werkruimte. Ook kunt u het label opgeven dat wordt gebruikt voor de lijst in de werkruimte.
- Als u een tegel aan een werkruimte wilt toevoegen, filtert u eerst de lijst op de pagina om de gegevens weer te geven waarvan u een overzicht wilt of waartoe u snel toegang wilt. Selecteer vervolgens **Toevoegen aan werkruimte**. Selecteer een werkruimte en selecteer in het veld **Presentatie** de optie **Tegel**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u het label kunt opgeven dat wordt gebruikt voor de tegel in de werkruimte. U kunt ook opgeven of de tegel een telling moet weergeven. Nadat de tegel is toegevoegd aan de werkruimte, kunt u deze selecteren om de huidige pagina te openen vanuit de werkruimte en de gefilterde lijst weer te geven die is gekoppeld aan de tegel.
- Als u een koppeling aan een werkruimte wilt toevoegen, filtert u de lijst op de pagina eerst zodat hier de gegevens worden weergegeven waarin u geïnteresseerd bent. Selecteer vervolgens **Toevoegen aan werkruimte**. Selecteer een werkruimte en selecteer in het veld **Presentatie** de optie **Koppeling**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u het label kunt opgeven dat wordt gebruikt voor de koppeling. U kunt desgewenst ook een label opgeven voor een nieuwe sectie die deze koppeling zal bevatten.

Nadat uw lijst, tegel of koppeling is toegevoegd aan een werkruimte, kunt u die werkruimte openen en de elementen erin op de gewenste manier ordenen.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Een overzicht toevoegen aan een werkruimte of dashboard
Sommige werkruimten bevatten tellingstegels (tegels met getallen erop) en u wilt deze mogelijk ook in uw dashboard laten weergeven. Klik in een werkgebied met de rechtermuisknop op een tellingstegel en selecteer **Aanpassen**. Selecteer in het eigenschappenvenster van de tegel **Vastmaken op dashboard**. De volgende keer dat u het geselecteerde dashboard opent (en vernieuwt) wordt de telling weergegeven onder de navigatietegel van die werkruimte. U kunt selecteren dat de telling rechtstreeks naar de gegevens gaat die erdoor worden voorgesteld.

### <a name="personalizing-your-dashboard"></a>Het dashboard aanpassen
Het dashboard is vaak de eerste pagina die bij het openen Finance and Operations wordt weergegeven. U kunt het dashboard aanpassen, zodat het alleen de werkruimtetegels weergeeft die u wilt zien. U kunt de tegels ook opnieuw schikken zodat ze in de volgorde worden weergegeven waarin u ze wilt zien, de naam van uw werkruimtenavigatietegels wijzigen of een nieuwe werkruimtetegel toevoegen.

Als u het dashboard wilt aanpassen, klikt u met de rechtermuisknop op een tegel en selecteert u **Aanpassen** om het eigenschappenvenster van de tegel te openen.

- Als u de geselecteerde tegel wilt verbergen of hernoemen, kunt u die wijziging rechtstreeks in het eigenschappenvenster aanbrengen.
- Als u de werkruimtetegels opnieuw wilt ordenen, selecteert u **Dit formulier aanpassen** om de werkbalk **Aanpassing** te openen. U kunt vervolgens het hulpmiddel **Verplaatsen** gebruiken om de tegels te ordenen.
- Voor meer informatie over het maken van een nieuwe werkruimtetegel in het eigenschappenvenster selecteert u **Een werkruimte toevoegen**. Een nieuwe werkruimtetegel wordt onder aan het dashboard gemaakt. U kunt deze werkruimtetegel desgewenst hernoemen. U kunt ook lijsten, tegels en koppelingen toevoegen aan de werkruimte, zoals beschreven in de sectie [Lijsten, tegels of koppelingen toevoegen aan werkruimten](personalize-user-experience.md#adding-a-tile-list-or-link-to-a-workspace) van dit onderwerp.

## <a name="administration-of-personalization"></a>Beheer van aanpassing
Nadat u een pagina hebt aangepast, kunt u uw aanpassingen delen met andere gebruikers door de aangepaste pagina te exporteren. U kunt vervolgens andere gebruikers vragen de aangepaste pagina te openen en het aanpassingsbestand te importeren dat u hebt gemaakt. U kunt ook uw aanpassingen geven aan een gebruiker die beheerdersrechten heeft. Die gebruiker kan het aanpassingsbestand vervolgens toepassen op veel gebruikers tegelijk.

Gebruiker met beheerdersbevoegdheden kunnen ook aanpassingen voor andere gebruikers beheren op de pagina **Aanpassing**. Deze pagina heeft vier tabbladen:

- **Toepassen**: u kunt een aanpassing voor een of meer gebruikers importeren of selecteren. Als u een aanpassing wilt toepassen op een of meer gebruikers, selecteert u eerst een rol en gebruikers die deze rol hebben. Vervolgens selecteert u een bestaande aanpassing om toe te passen op geselecteerde gebruikers of importeert u een aanpassingsbestand. De aanpassing wordt gevalideerd en toegepast op alle geselecteerde gebruikers. Dit wordt van kracht bij de volgende keer dat ze de geselecteerde pagina openen.
- **Wissen**: u kunt alle aanpassingen voor een pagina of werkgebied voor een of meer gebruikers wissen. Selecteer eerst een pagina of werkruimte voor een overzicht van de gebruikers die deze hebben aangepast. Kies vervolgens de gebruikers waarvoor de aanpassingen voor die pagina moeten worden gewist en selecteer **Wissen**. Alle aanpassingen die de geselecteerde gebruikers hebben toegepast op de geselecteerde pagina of het geselecteerde werkgebied, worden verwijderd. Deze actie kan niet ongedaan worden gemaakt. Als de pagina of het werkgebied echter een opgeslagen aanpassing heeft, kan die aanpassing opnieuw worden geïmporteerd.
- **Beheren per gebruiker**: selecteer een gebruiker voor een overzicht van pagina's die deze persoon heeft aangepast. Vervolgens kunt u opgeven of de gebruiker voor bepaalde pagina's of voor het hele systeem aanpassingen kan doorvoeren. U kunt ook een aanpassing importeren, exporteren of wissen voor de geselecteerde gebruiker.
- **Systeem**: u kunt tijdelijk alle aanpassingen voor alle gebruikers in het systeem uitschakelen. In dit geval worden de aanpassingen verwijderd. Alle pagina's krijgen voor alle gebruikers weer de standaardstatus. Als u aanpassingen later opnieuw inschakelt, worden alle aanpassingen opnieuw toegepast. U kunt alle aanpassingen voor alle gebruikers in het systeem ook permanent verwijderen. Er is geen enkele manier om aanpassingen terug te halen die zijn verwijderd. Voordat u deze taak uitvoert, moet u er daarom voor zorgen dat u aanpassingen hebt geëxporteerd die u later mogelijk wilt.

## <a name="personalization-of-inventory-dimensions"></a>Aanpassing van voorraaddimensies

Wanneer u de instellingen van de voorraaddimensies op een pagina wilt aanpassen, kunt u de instellingen toepassen die zijn gemaakt met de optie **Dimensie weergeven**. U gebruikt aanpassing bijvoorbeeld om een kolom te verbergen voor de voorraaddimensie Batchnummer, maar de kolom wordt de volgende keer dat de pagina wordt geopend, weergegeven. Deze werking treedt op omdat de **Weergave van dimensies**-instellingen bepalen welke voorraaddimensiekolommen worden weergegeven.

De **Weergave van dimensies**-instellingen zijn van toepassing op alle pagina's en hebben voorrang op aangepaste instellingen van voorraaddimensievelden op afzonderlijke pagina's.

Als u daarom in het vorige voorbeeld niet wilt dat de kolom voor de voorraaddimensie Batchnummer wordt weergegeven, moet u die dimensie uitschakelen als onderdeel van de optie **Weergave van dimensies** voor de tabel. Deze wijziging zal uiteindelijk niet alleen op een bepaalde pagina gelden, maar voor alle pagina's.

