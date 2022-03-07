---
title: De gebruikerservaring aanpassen
description: In dit onderwerp wordt uitgelegd hoe u de app kunt aanpassen.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 764444442aedcbf0934f1c636d7440bc0d277043
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944528"
---
# <a name="personalize-the-user-experience"></a>De gebruikerservaring aanpassen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de app personaliseert en worden de volgende onderwerpen behandeld: 

- **Opties voor het hele systeem** : deze personalisatieopties worden gemaakt op een instellingspagina en zijn beschikbaar voor alle gebruikers. Voorbeelden zijn kleurenthema en tijdzone. 
- **Beperkte toegang voor persoonlijke instellingen**: op dit toegangsniveau worden gebruikersacties die zijn gekoppeld aan het standaardpaginagebruik automatisch opgeslagen door de app en teruggezet de volgende keer dat u de pagina bezoekt. Zo slaat de app bijvoorbeeld de breedte van rasterkolommen op als u deze aanpast, en de status van uitgevouwen of samengevouwen sneltabbladen. 
- **Volledige toegang tot persoonlijke instellingen**: op dit toegangsniveau hebben gebruikers toegang tot alle mogelijkheden van personalisatie in de app. Ze hebben met name toegang tot de werkbalk **Persoonlijke instellingen**. 
- **Persoonlijke instellingen delen**: gebruikers die toegang hebben tot volledige persoonlijke instellingen, kunnen hun paginapersonalisatie exporteren en delen met andere gebruikers.
- **Beheer van persoonlijke instellingen**: bevoegde gebruikers hebben toegang tot de beheerpagina **Persoonlijke instellingen** om alle persoonlijke instellingen op organisatieniveau te beheren. 

## <a name="system-wide-options-for-the-current-user"></a>Opties in het hele systeem voor de huidige gebruiker

De pagina **Gebruikersopties** bevat enkele algemene instellingen voor de huidige gebruiker. Deze opties zijn beschikbaar voor alle gebruikers, zelfs gebruikers die geen toegang hebben gekregen tot aanpassing. Als u de pagina **Gebruikersopties** wilt openen, selecteert u de knop **Instellingen** op de navigatiebalk en selecteert u **Gebruikersopties**. De pagina **Gebruikersopties** bevat vier tabbladen met verschillende gebruikersinstellingen:

- **Zichtbaar:** selecteer een kleurenthema en de standaardgrootte van elementen op pagina's.
- **Voorkeuren**: selecteer standaardwaarden die elke keer dat u het systeem opent, worden gebruikt. Deze waarden omvatten het standaardbedrijf, de eerste pagina en de standaardmodus voor weergeven/bewerken. (De modus voor weergeven/bewerken bepaalt of een pagina is vergrendeld voor weergave of geopend voor bewerking steeds als u deze opent.) Dit tabblad bevat ook opties voor de taal, de tijdzone en datum, tijd en getalnotaties. Ten slotte bevat dit tabblad verschillende voorkeuren die variëren van versie tot versie.
- **Account**: bekijk of wijzig uw gebruikersnaam en andere accountopties.
- **Werkstroom**: werkstroomgerelateerde opties selecteren.

Naast het wijzigen van de gebruikersinstellingen kunt u uw gebruiksgegevens en persoonlijke instellingen bekijken en verwijderen vanaf de pagina **Gebruikersopties**. Als u uw gebruiksgegevens wilt weergeven, selecteert u **Gebruiksgegevens** in het actievenster. Op het tabblad **Aanpassing** kunt u de persoonlijke wijzigingen die u hebt aangebracht in de pagina's in het systeem weergeven en beheren. Op dit tabblad kunt u ook de functietoelichtingen opnieuw instellen (dat wil zeggen: de pop-upvensters met informatie over nieuwe systeemfuncties). Vervolgens krijgt u opnieuw meldingen bij eerder uitgebrachte functies.

> [!NOTE]
> Als de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld, kunt u uw persoonlijke instellingen weergeven en beheren door **Aanpassing** te selecteren in het actievenster op de **pagina Gebruikersopties**.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Beperkte toegang tot persoonlijke instellingen (voorheen impliciete gepersonaliseerde items)

Op het niveau **Beperkte toegang voor persoonlijke instellingen** worden gebruikersacties die zijn gekoppeld aan het standaardpaginagebruik automatisch opgeslagen door de app en teruggezet de volgende keer dat u de pagina bezoekt. Er is geen expliciete opslagactie vereist. 

Hier volgt een lijst met de acties die onder het normale gebruik van de pagina vallen en die vallen onder beperkte toegang tot persoonlijke instellingen: 

- **Rasterkolombreedten:** u kunt de breedte van een kolom in een raster aanpassen door de formaatbalk links of rechts van de kolomkop te selecteren en deze naar links of rechts te schuiven totdat de kolom de gewenste breedte heeft. De app slaat de breedte op die u instelt voor een kolom. De kolom krijgt die grootte steeds wanneer u de volgende keer die pagina opent.
- **Rastervoettekst- en kolomtotalen**: *(alleen beschikbaar als het nieuwe rasterbesturingselement is ingeschakeld)* U bepaalt of er een totaal moet worden weergegeven onder aan een numerieke kolom in een raster en of de rastervoettekst zichtbaar is. De app slaat deze gegevens op en past ze toe wanneer u de pagina de volgende keer opent. Zie [Rastermogelijkheden](grid-capabilities.md) voor meer informatie. 
- **Sneltabbladen**: sommige pagina's bevatten uitvouwbare secties genaamd *sneltabbladen*. De app bevat gegevens over de sneltabbladen die u hebt uitgevouwen of samengevouwen. Vervolgens worden de volgende keer dat u de pagina opent, dezelfde sneltabbladen uitgevouwen of samengevouwen, gebaseerd op uw laatste interactie met de pagina. In sommige gevallen kunt u de systeemprestaties helpen verbeteren door een sneltabblad samen te vouwen, omdat de app de gegevens voor sneltabbladen pas op hoeft te halen als ze worden uitgevouwen. Zoals later in dit onderwerp wordt uitgelegd kunt u ook de volgorde wijzigen van de sneltabbladen op een pagina.
- **Feitenblokken**: sommige pagina's hebben een deelvenster **Verwante informatie** waarin alleen-lezen informatie wordt weergegeven over het huidige onderwerp van de pagina. Elke sectie in het deelvenster **Verwante informatie** wordt een *feitenblok* genoemd. U kunt het deelvenster **Verwante informatie** uitvouwen of samenvouwen en u kunt ook afzonderlijke feitenblokken uitvouwen of samenvouwen. De app slaat deze voorkeuren op. Wanneer u de volgende keer de pagina opent, zijn het deelvenster **Verwante informatie** en de afzonderlijke feitenblokken uitgevouwen of samengevouwen op basis van uw laatste interactie met de pagina. In sommige gevallen kunt u de systeemprestaties helpen verbeteren door het deelvenster **Verwante informatie** samen te vouwen, omdat de app de gegevens voor feitenblokken pas op hoeft te halen als ze worden uitgevouwen.
- **Actievensters**: een *actievenster* wordt weergegeven boven aan de meeste pagina's. Het actievenster bevat knoppen voor een groot aantal van de acties die u op de huidige pagina uitvoeren kunt. Deze knoppen zijn vaak geordend op tabbladen. U kunt het gehele actievenster open *vastzetten* of u kunt het standaard samengevouwen laten. De volgende keer dat u de pagina opent, is het actievenster geopend of samengevouwen, gebaseerd op uw laatste interactie met de pagina. Als u het actievenster open hebt vastgemaakt, wordt het laatst gebruikte tabblad weergegeven.
- **Snelfilters**: een *snelfilter* wordt boven aan veel rasters weergegeven. Met het snelfilter kunt u het raster filteren op basis van één kolom die u selecteert. De app slaat de kolom op waarop u hebt gefilterd. De volgende keer dat u die pagina opent, wordt het raster standaard op dezelfde kolom gefilterd. U kunt vervolgens echter toch een andere kolom selecteren om het raster op te filteren.
- **Kolomkopfilters**: wanneer u een raster filtert met behulp van *kolomkopfilters*, kunt u de filteroperator indien nodig wijzigen om de gegevens te vinden die u zoekt. U kunt de operator bijvoorbeeld wijzigen van **begint met** in **is exact**. Telkens wanneer u een koptekstfilter gebruikt en de filteroperator wijzigt, slaat de app de wijziging op. Vervolgens wordt de filteroperator hersteld wanneer u de volgende keer op die kolom filtert.
- **Navigatievenster**: u kunt het *navigatievenster* openen door de knop **Het navigatiedeelvenster uitvouwen** te selecteren, linksboven op elke pagina. (Deze knop wordt ook wel de _**Menu** knop_, de *hamburger*, het *hamburgermenu* of de *hamburgerknop* genoemd.) U kunt het navigatievenster open vastzetten of u kunt het standaard samengevouwen houden. Nadat u het navigatievenster open hebt vastgezet, houdt de app het open totdat u het samenvouwt.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Volledige toegang tot persoonlijke instellingen (voorheen expliciete gepersonaliseerde items)

Op het niveau **Volledige toegang tot persoonlijke instellingen** hebben gebruikers toegang tot alle personalisatiemogelijkheden van de app. Aangezien verschillende mensen en bedrijven verschillende behoeften hebben bij de interactie met de app, met name op het gebied van gebruikte velden, biedt personalisatie tools waarmee gebruikers en organisaties de manier kunnen aanpassen waarop informatie wordt geordend en er binnen de app mee wordt gewerkt. Deze mogelijkheden zijn essentieel voor het bieden van vereenvoudigde, geoptimaliseerde ervaringen in de app die op u en uw organisatie zijn afgestemd. 

Als de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld, is er een expliciete opslag nodig om deze wijzigingen in de gebruikerservaring voor een specifieke weergave te behouden. Wanneer de functie **Opgeslagen weergaven** is uitgeschakeld, worden deze wijzigingen automatisch opgeslagen.

De volgende secties hebben betrekking op de mate van personalisatiefuncties die voor gebruikers beschikbaar zijn op het niveau **volledige toegang tot persoonlijke instellingen**. Dit zijn enkele van deze mogelijkheden:

- Opties in snelmenu
- De werkbalk **Persoonlijke instellingen**
- Tegels, lijsten en koppelingen naar werkruimten toevoegen
- Een overzicht toevoegen aan een werkgebied of dashboard
- Het dashboard aanpassen

### <a name="shortcut-menu-options"></a>Opties in snelmenu

Snelmenu's bevatten een manier om de interface van een pagina te wijzigen zodat deze beter voldoet aan uw behoeften of de vereisten van uw organisatie. (Een snelmenu wordt ook wel een *rechtsklikmenu* of *contextmenu* genoemd.)

Sommige van de meest gangbare en belangrijke wijzigingen die in een pagina kunnen worden aangebracht, zijn rechtstreeks als opties in een snelmenu beschikbaar. U kunt bijvoorbeeld met de rechtermuisknop op een kolomkop klikken en **Kolommen invoegen** of **Deze kolom verbergen** selecteren als u kolommen in een raster wilt toevoegen of verbergen.

Bovendien zijn de meest algemene typen aanpassing beschikbaar door met de rechtermuisknop op een element te klikken en vervolgens **Aanpassen** te selecteren. (Houd er rekening mee dat niet alle elementen op uw pagina kunnen worden aangepast.) Wanneer u deze methode van aanpassing selecteert, ziet u het *eigenschappenvenster* van het element.

![Eigenschappen van een element aanpassen](./media/cli-element-property-window.png)

U kunt het eigenschappenvenster gebruiken om een element op de volgende manieren aan te passen:

- Het label van het element wijzigen.
- Het element verbergen zodat het niet wordt weergegeven op de pagina. De gegevens in het veld worden niet verwijderd of gewijzigd. De informatie wordt alleen niet meer weergegeven op de pagina.
- De informatie in de samenvattingssectie van het sneltabblad opnemen (als het element zich op een sneltabblad bevindt).
- Sla het veld over zodat het nooit de focus krijgt wanneer u door de pagina navigeert.
- Voorkom dat gegevens in het veld (voor elke record) worden bewerkt.
- Wijs een veld aan dat vereist is voor de gegevensinvoer. Als er in dit veld geen waarde is ingevoerd, wordt dit weergegeven met een rode rand en een sterretje om deze status aan te geven. Deze optie is alleen beschikbaar vanaf versie 10.0.11 als de functies [Opgeslagen weergaven](saved-views.md) en **Velden aanwijzen die vereist zijn voor persoonlijke instellingen** zijn ingeschakeld.

Het eigenschappenvenster kan andere mogelijkheden voor aanpassing hebben, afhankelijk van het element. Met het eigenschappenvenster van een tegel kunt u de tegel bijvoorbeeld promoveren tot dashboard en met het eigenschappenvenster van elementen op het standaarddashboard kunt u mogelijk een nieuw werkgebied maken.

### <a name="personalization-toolbar"></a>Aanpassingswerkbalk

Als u meerdere wijzigingen in een pagina wilt aanbrengen of wijzigingen wilt doorvoeren die niet beschikbaar zijn via andere mechanismen (zoals de volgorde van elementen wijzigen), kunt u de werkbalk **Aanpassing** gebruiken. Voer een van de volgende stappen uit om de werkbalk **Aanpassing** te openen:

- Selecteer **Ctrl+Shift+p** vanuit een element op de pagina.
- Selecteer **Deze pagina aanpassen** in het eigenschappenvenster van een element.
- Selecteer **Deze pagina aanpassen** in de groep **Aanpassen** op het tabblad **Opties** van het actievenster van een pagina.
- Selecteer de knop **Instellingen** (het tandwielsymbool) op de navigatiebalk en selecteer **Aanpassen.**

[![Aanpassingswerkbalk](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Navigeren op de pagina

Wanneer de werkbalk **Aanpassing** is geopend, is de onderliggende pagina alleen-lezen (met andere woorden u kunt de gegevens niet bewerken), maar is deze nog steeds interactief. U kunt het deelvenster **Verwante informatie** uitvouwen of samenvouwen, tabbladen omwisselen en secties uitvouwen of samenvouwen, zoals u deze acties gewoonlijk op de pagina uitvoert. Als u een samenvouwbare sectie of een tabblad wilt aanpassen (bijvoorbeeld om een sneltabblad te verbergen), activeert u de knop die naast die sectie of dat tabblad verschijnt wanneer deze focus krijgt of wanneer u de muisaanwijzer hierop plaatst.

#### <a name="personalization-tools"></a>Aanpassingsprogramma's

De volgende hulpmiddelen zijn beschikbaar op de werkbalk **Aanpassing**:

- Gebruik het hulpmiddel **Selecteren** om de eigenschappen van een element te wijzigen. Als u dit hulpmiddel wilt gebruiken, selecteert u de knop **Selecteren** op de werkbalk en selecteert u vervolgens het gewenste element. Het eigenschappenvenster van het element wordt geopend en u kunt daar eventuele eigenschappen van dat element wijzigen. U kunt het proces herhalen voor andere elementen die op de pagina kunnen worden aangepast. Sommige aangepaste eigenschappen zijn mogelijk niet in alle scenario's beschikbaar. U kunt bijvoorbeeld geen veld vergrendelen dat vereist is.
- Gebruik het hulpmiddel **Verbergen** om een element op de pagina te verbergen. Als u dit hulpmiddel wilt gebruiken, selecteert u de knop **Verbergen** op de werkbalk en selecteert u vervolgens het element dat u wilt verbergen. Wanneer u het hulpmiddel **Verbergen** gebruikt, worden alle elementen die momenteel verborgen zijn, zichtbaar gemaakt, maar in een grijze container weergegeven. U kunt een element vervolgens zichtbaar maken door het te selecteren. Als u wilt zien hoe de pagina eruitziet wanneer elementen verborgen zijn, schakelt u over op een ander personalisatiehulpmiddel of sluit u de personalisatiewerkbalk.
- Gebruik het hulpmiddel **Velden toevoegen** om velden toe te voegen aan uw pagina. Wanneer u dit hulpmiddel gebruikt, kunt u alleen velden toevoegen die deel uitmaken van de paginadefinitie. Zie voor informatie over het maken van nieuwe velden die geen deel uitmaken van de huidige paginadefinitie [Maken en werken met aangepaste velden](user-defined-fields.md). Nadat u de knop **Velden toevoegen** op de werkbalk hebt geselecteerd, moet u eerst het raster of de sectie selecteren waar u een veld wilt toevoegen. Er wordt een dialoogvenster weergegeven met de lijst met velden die gerelateerd zijn aan het geselecteerde raster of sectie. Selecteer in het dialoogvenster een of meer velden om toe te voegen en selecteer vervolgens **Bijwerken**. Als u een veld wilt verwijderen dat u eerder hebt toegevoegd, herhaalt u de procedure, maar wist u de selectie van het veld in het dialoogvenster.
- Gebruik het hulpmiddel **Verplaatsen** om een element te verplaatsen naar een andere locatie binnen de huidige groep elementen. U kunt een element niet buiten de bovenliggende groep verplaatsen. Als u dit hulpmiddel wilt gebruiken, selecteert u de knop **Verplaatsen** op de werkbalk en selecteert u vervolgens het element dat u wilt verplaatsen. Wanneer u een element selecteert, bepaalt de app de locaties waar het element naartoe kan worden verplaatst. Deze locaties worden *neerzetzones* genoemd. Wanneer u het element binnen de huidige groep versleept, wordt elke neerzetzone weergegeven als een gekleurde vette lijn naast het gebied waar het element kan worden neergezet.
- Gebruik het hulpmiddel **Overslaan** om een element te verwijderen uit de volgorde van de toetsenbordtoets Tab van de pagina. Wanneer u de knop **Overslaan** op de werkbalk selecteert, worden alle elementen die momenteel overgeslagen worden, weergegeven in een grijze container. U kunt velden interactief verwijderen of toevoegen aan de tabvolgorde.
- Gebruik het hulpmiddel **Weergeven in koptekst** als u wilt dat een veld in de samenvattingssectie van het sneltabblad wordt weergegeven. Wanneer u de knop **Weergeven in koptekst** selecteert op de werkbalk, worden alle velden die zijn geselecteerd als overzichtsvelden, weergegeven in een grijze container. U kunt interactief velden toevoegen aan het sneltabbladoverzicht en velden uit het sneltabbladoverzicht verwijderen door de velden te selecteren.
- Gebruik het gereedschap **Vereisen** om een element aan te wijzen dat nodig is voor gegevensinvoer. Wanneer u de knop **Vereisen** op de werkbalk selecteert, worden alle elementen die momenteel zijn aangepast als vereist, weergegeven in een grijze container. U kunt ze vervolgens weer instellen op niet vereist. Deze optie is alleen beschikbaar vanaf versie 10.0.12 als de functie **Velden aanwijzen die vereist zijn voor persoonlijke instellingen** is ingeschakeld.
- Gebruik het hulpmiddel **Vergrendelen** wanneer u een element als bewerkbaar of niet bewerkbaar wilt markeren. Wanneer u de knop **Vergrendelen** op de werkbalk selecteert, worden alle elementen die momenteel niet bewerkbaar zijn, weergegeven in een grijze container. U kunt deze vervolgens weer bewerkbaar maken. Merk op dat sommige velden verplicht zijn en niet niet-bewerkbaar kunnen worden gemaakt. Een hangslot wordt weergegeven naast deze velden.
- Gebruik het hulpmiddel **Een app toevoegen vanuit Power Apps** om een app in te sluiten die met Microsoft Power Apps op de pagina is gemaakt. Zie [Apps insluiten vanuit Power Apps](embed-power-apps.md) voor gedetailleerde informatie over het insluiten van een app op een pagina vanuit Power Apps. Deze optie is alleen beschikbaar als de functie [Opgeslagen weergaven](saved-views.md) is uitgeschakeld.
- Gebruik de **Een app toevoegen** om een app in te sluiten op de pagina. Dit kan een app zijn die is gemaakt in Microsoft Power Apps of een app van derden. Deze optie is alleen beschikbaar als de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld. 
- Gebruik het hulpmiddel **Wissen** om de pagina weer op de standaard, geïnstalleerde toestand in te stellen. Alle aanpassingen op de huidige pagina worden gewist. Deze actie kan niet ongedaan worden gemaakt. Gebruik dit hulpmiddel daarom alleen als u zeker weet dat u de pagina opnieuw wilt instellen. Als de functie **Opgeslagen weergaven** is ingeschakeld, worden met dit hulpmiddel de persoonlijke instellingen voor de huidige weergave gewist.
- Gebruik het hulpmiddel **Importeren** om een aanpassing uit een aanpassingsbestand te laden die u of iemand anders eerder heeft gemaakt. 

    - Wanneer de functie **Opgeslagen weergaven** is uitgeschakeld, kunt u kiezen of u uw bestaande persoonlijke instellingen wilt toevoegen of vervangen door de persoonlijke instellingen die voor de pagina worden geïmporteerd. Deze actie kan niet ongedaan worden gemaakt. Nadat u de persoonlijke instellingen hebt geïmporteerd, moet u de gewenste wijzigingen dus handmatig wissen of ongedaan maken.
    - Als de functie **Opgeslagen weergaven** is ingeschakeld, worden de geïmporteerde gepersonaliseerde items weergegeven op de pagina. Als de weergave al bestaat, kunt u de importoptie overslaan, de huidige weergave met dezelfde naam vervangen of de geïmporteerde weergave een andere naam geven.

- Gebruik het hulpmiddel **Exporteren** om uw aanpassingen voor de pagina op te slaan in een bestand. U kunt vervolgens uw aanpassingen delen met andere gebruikers. Deze gebruikers hoeven alleen het bestand te importeren dat uw aanpassingen voor de pagina bevat. Als de functie **Opgeslagen weergaven** is ingeschakeld, slaat u met dit hulpmiddel uw huidige weergave op in een bestand zodat u deze kunt delen.
- Selecteer de knop **Sluiten** om de werkbalk **Aanpassing** te sluiten en de pagina terug te brengen naar de vorige interactieve status.

Wanneer de werkbalk **Aanpassing** wordt gebruikt, worden uw aanpassingen normaal gesproken van kracht zodra u ze maakt. Als echter de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld, moet u de persoonlijke instellingen van een door u gekozen weergave expliciet opslaan.

In sommige gevallen ziet u wanneer u een hulpmiddel selecteert een hangslotpictogram naast een element. Dit symbool geeft aan dat u de eigenschappen van het element die zijn gerelateerd aan het geselecteerde hulpmiddel, niet kunt wijzigen omdat wijzigingen in deze eigenschappen voorkomen dat de pagina correct werkt.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Tegels, lijsten en koppelingen aan een werkruimte toevoegen

Voor sommige pagina's die lijsten bevatten, is de aanpassingsfunctie **Toevoegen aan werkgebied** beschikbaar in de groep **Aanpassen** op het tabblad **Opties** van het actievenster. Met deze functie kunt u relevante informatie vanuit de huidige lijst in een specifiek werkgebied binnenhalen. De informatie die in het werkgebied wordt weergegeven, kan worden gebaseerd op de gehele lijst of op een gefilterde en gesorteerde versie van de lijst. U kunt ook opgeven of de informatie wordt weergegeven in het werkgebied als een lijst, als een overzichttegel die het aantal artikelen in de lijst kan weergeven, of als een koppeling.

> [!NOTE]
> Als de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld, is de inhoud die u naar een werkgebied verplaatst, rechtstreeks aan een weergave gekoppeld. De query van de weergave wordt gebruikt om gegevens op te halen in de werkruimte. De bijbehorende tegel of koppeling in het werkgebied opent de pagina voor die weergave, zodat de query en de persoonlijke instellingen van de weergave worden toegepast. Als de weergave wordt bijgewerkt, worden de bijbehorende elementen van de werkruimte aangepast aan de nieuwe weergavedefinitie.

[![Toevoegen aan werkgebied](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Als u een lijst aan een werkgebied wilt toevoegen, sorteert of filtert u de lijst op de pagina eerst, zodat deze de informatie bevat zoals u deze wilt weergeven in het werkgebied. (Als de functie **Opgeslagen weergaven** is ingeschakeld, kunt u pas doorgaan nadat u een weergave met deze voorwaarden hebt opgeslagen.) Selecteer vervolgens **Toevoegen aan werkruimte**. Selecteer een werkgebied en selecteer in het veld **Presentatie** de optie **Lijst**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u de kolommen kunt selecteren die moeten worden weergegeven in de lijst in het werkgebied. Ook kunt u het label opgeven dat wordt gebruikt voor de lijst in het werkgebied.
- Als u een tegel aan een werkgebied wilt toevoegen, filtert u eerst de lijst op de pagina om de gegevens weer te geven waarvan u een overzicht wilt of waartoe u snel toegang wilt. (Als de functie **Opgeslagen weergaven** is ingeschakeld, kunt u pas doorgaan nadat u een weergave met deze voorwaarden hebt opgeslagen.) Selecteer vervolgens **Toevoegen aan werkruimte**. Selecteer een werkgebied en selecteer in het veld **Presentatie** de optie **Tegel**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u het label kunt opgeven dat moet worden gebruikt voor de tegel in het werkgebied. U kunt ook opgeven of de tegel een telling moet weergeven. Nadat de tegel is toegevoegd aan het werkgebied, kunt u deze selecteren om de huidige pagina te openen vanuit het werkgebied. Vervolgens kunt u de gefilterde lijst bekijken die aan de tegel is gekoppeld.
- Als u een koppeling aan een werkgebied wilt toevoegen, filtert u de lijst op de pagina eerst zodat hier de gegevens worden weergegeven waarin u geïnteresseerd bent. (Als de functie **Opgeslagen weergaven** is ingeschakeld, kunt u pas doorgaan nadat u een weergave met deze voorwaarden hebt opgeslagen.) Selecteer vervolgens **Toevoegen aan werkruimte**. Selecteer een werkgebied en selecteer in het veld **Presentatie** de optie **Koppeling**. Nadat u **Configureren** hebt geselecteerd, verschijnt een dialoogvenster waarin u het label kunt opgeven dat moet worden gebruikt voor de koppeling. U kunt desgewenst ook een label opgeven voor een nieuwe sectie die deze koppeling bevat.

Nadat een lijst, tegel of koppeling is toegevoegd aan een werkgebied, kunt u dit werkgebied openen en de elementen erin op de gewenste manier ordenen.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Een overzicht toevoegen aan een werkgebied of dashboard

Sommige werkgebieden bevatten tellingstegels (tegels met getallen erop) en u wilt deze mogelijk ook in uw dashboard laten weergeven. Klik in een werkgebied met de rechtermuisknop op een teltegel, selecteer **Aanpassen** en selecteer vervolgens **Vastmaken op dashboard** in het eigenschappenvenster van de tegel. De volgende keer dat u het geselecteerde dashboard opent en vernieuwt, wordt de telling weergegeven onder de navigatietegel van dat werkgebied. U kunt selecteren dat de telling rechtstreeks naar de gegevens gaat die erdoor worden voorgesteld.

### <a name="personalizing-your-dashboard"></a>Het dashboard aanpassen

Het dashboard is vaak de eerste pagina die bij het openen van de app wordt weergegeven. Het kan op dezelfde manier worden aangepast als elke andere pagina in het systeem door gebruik te maken van dezelfde mechanismen die eerder in dit onderwerp zijn beschreven. 

> [!WARNING]
> Wanneer u op dit moment inhoud op het dashboard verbergt, is het van belang dat u rechtstreeks een tegel aanwijst, niet de ruimte eromheen. Als u de groep rond een tegel verbergt, zijn er onverwachte resultaten als er later meer tegels worden toegevoegd of als het systeem naar een andere taal wordt overgeschakeld.

Een unieke aanpassingsmogelijkheid die beschikbaar is op het dashboard, is de mogelijkheid om tegels toe te voegen. 

- Als de functie **Apps op volledige pagina's** is uitgeschakeld, voegt u een nieuwe tegel toe door met de rechtermuisknop op een element in het dashboard te klikken en vervolgens **Een werkgebied toevoegen** te selecteren. Een nieuwe werkgebiedtegel wordt onder aan het dashboard gemaakt. U kunt deze werkgebiedtegel desgewenst hernoemen. U kunt ook lijsten, tegels en koppelingen toevoegen aan het werkgebied, zoals beschreven in de sectie [Tegels, lijsten en koppelingen toevoegen aan een werkgebied](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace) van dit onderwerp.
- Als de functie **Apps op volledige pagina's** is ingeschakeld, voegt u een nieuwe tegel toe door met de rechtermuisknop op een element in het dashboard te klikken en vervolgens **Een app toevoegen** te selecteren. Selecteer in het dialoogvenster of u een tegel wilt toevoegen voor een nieuw werkgebied of een tegel met inhoud uit Power Apps of een website. Voer vervolgens de stappen uit om de geselecteerde optie te configureren. Een nieuwe werkgebiedtegel wordt onder aan het dashboard gemaakt. 

## <a name="sharing-personalizations"></a>Persoonlijke instellingen delen

Nadat u een pagina hebt aangepast, kunt u op verschillende manieren uw aanpassingen delen met andere gebruikers. In de volgende lijst zijn de methoden gerangschikt op volgorde van de meest aanbevolen naar de minst aanbevolen methode.

1. Weergaven naar gebruikers publiceren.
2. Weergaven of aanpassingen naar gebruikers kopiëren.
3. Weergaven of aanpassingen exporteren en importeren.

### <a name="publish-views-to-users"></a>Weergaven naar gebruikers publiceren

Als de functie [Opgeslagen weergaven](saved-views.md) is ingeschakeld en als de pagina weergaven ondersteunt, kunt u de weergave het beste met andere gebruikers delen door de weergave te publiceren naar gebruikers met een of meer beveiligingsrollen. Meer informatie over dit onderwerp vindt u in [Weergaven publiceren](saved-views.md#publishing-views).

### <a name="copy-views-or-personalizations-to-users"></a>Weergaven of aanpassingen naar gebruikers kopiëren

Als de functie [Opgeslagen](saved-views.md) weergaven is uitgeschakeld of als de pagina geen weergaven ondersteunt, is de aanbevolen manier om aanpassingen te delen door deze van de ene gebruiker naar de andere te kopiëren. Deze methode is alleen beschikbaar voor bevoegde gebruikers (bijvoorbeeld systeembeheerders). Beheerders kunnen echter de aanpassing van een bepaalde gebruiker in het systeem opzoeken (inclusief de persoonlijke weergave van de gebruiker als Opgeslagen weergaven is ingeschakeld) en de configuratie naar andere gebruikers kopiëren.

Als Opgeslagen weergaven is ingeschakeld, volgt u deze stappen om de aanpassing te kopiëren.

1. Ga naar **Systeembeheer \> Instellingen \> Persoonlijke instellingen**.
2. U kunt persoonlijke weergaven als volgt kopiëren:

    1. Selecteer **Persoonlijke weergaven**.
    2. Selecteer de gewenste weergaven in de lijst.
    3. Selecteer **Kopiëren naar gebruikers**.
    4. Selecteer de gebruikers naar wie u de weergaven wilt kopiëren.

    Volg deze stappen om aanpassingen te kopiëren van pagina's die geen weergaven ondersteunen:

    1. Selecteer **Gebruikersinstellingen**.
    2. Selecteer de gebruiker met de aanpassing die u wilt delen.
    3. Selecteer **Alle aanpassingen beheren**.
    4. Selecteer de gewenste aanpassingen in de lijst.
    5. Selecteer **Kopiëren naar gebruikers**.
    6. Selecteer de gebruikers naar wie u de aanpassingen wilt kopiëren.

Als Opgeslagen weergaven niet is ingeschakeld, volgt u deze stappen om een aanpassingen te kopiëren.

1. Ga naar **Systeembeheer \> Instellingen \> Persoonlijke instellingen**.
2. Selecteer **Toepassing**.
3. Selecteer de gebruikers naar wie u de aanpassing wilt kopiëren.
4. Selecteer **Bestaande aanpassingen selecteren**.
5. Zoek en selecteer de (enkele) aanpassing waarin u geïnteresseerd bent.
6. Selecteer **OK**.

### <a name="export-and-import-views-or-personalizations"></a>Weergaven of aanpassingen exporteren en importeren

U kunt aanpassingen ook delen via export en import. Individuele gebruikers, of een beheerder die namens hen handelt, kunnen met deze methode hun aanpassingen of weergaven exporteren en vervolgens het geëxporteerde bestand aan andere gebruikers geven om te importeren. Gebruikers kunnen hun geëxporteerde aanpassingen ook geven aan een gebruiker met beheerdersbevoegdheden, waarna die gebruiker de pagina **Persoonlijke instellingen** kan gebruiken om het aanpassingsbestand op een groot aantal gebruikers tegelijk toe te passen.

#### <a name="export"></a>Exporteren

In het algemeen kunt u een van uw eigen weergaven of aanpassingen exporteren door de betreffende pagina te openen, de werkbalk **Persoonlijke instellingen** te openen en vervolgens **Exporteren** te selecteren. Meer informatie over de werkbalk vindt u in de sectie [Aanpassingswerkbalk](#personalization-toolbar) een stukje terug in dit artikel. Als [Opgeslagen weergaven](saved-views.md) is ingeschakeld, kunt u ook gaan naar **Instellingen \> Gebruikersopties \> Persoonlijke instellingen** om een lijst met al uw aanpassingen in het systeem weer te geven. Hier kunt u de weergaven of aanpassingen selecteren die u wilt exporteren en vervolgens **Exporteren** selecteren.

Verder kunnen beheerders de aanpassingen van andere gebruikers exporteren door de volgende stappen uit te voeren.

1. Ga naar **Systeembeheer \> Instellingen \> Persoonlijke instellingen**.
2. Selecteer op het tabblad **Gebruikers** de gewenste gebruiker.
3. Zoek en selecteer de weergave of aanpassing waarin u geïnteresseerd bent.
4. Selecteer **Exporteren**.

#### <a name="import"></a>Importeren

Als u een weergave of aanpassing wilt importeren, opent u gewoon de werkbalk **Persoonlijke instellingen** en selecteert u **Importeren**. Bovendien kunnen beheerders een bestand importeren en dit direct aan een of meer gebruikers geven.

Als Opgeslagen weergaven is ingeschakeld, volgt u deze stappen.

1. Ga naar **Systeembeheer \> Instellingen \> Persoonlijke instellingen**.
2. Selecteer in het actievenster **Weergaven importeren \> Gebruikersweergaven**.
3. Selecteer de importmodus:

    - **Specifieke gebruikers selecteren**: de weergave of de aanpassing geven aan geselecteerde gebruikers.
    - **As-is importeren**: de weergave of personalisatie importeren naar dezelfde gebruiker die deze heeft geëxporteerd.

4. Selecteer **Bladeren** en zoek en selecteer de aanpassing die u wilt importeren.
5. Selecteer **Volgende**.
6. Als u in stap 3 **Specifieke gebruikers selecteren** hebt gekozen, selecteert u de gebruikers naar wie u de personalisatie wilt importeren.
7. Selecteer **Importeren**.
8. Los waar nodig conflicten op.

Als Opgeslagen weergaven niet is ingeschakeld, volgt u deze stappen.

1. Ga naar **Systeembeheer \> Instellingen \> Persoonlijke instellingen**.
2. Selecteer **Toepassing**.
3. Selecteer de gebruikers naar wie u de aanpassing wilt kopiëren.
4. Selecteer **Aanpassingen importeren uit een bestand**.
5. Selecteer **Bladeren** en zoek en selecteer de aanpassing die u wilt importeren.
6. Selecteer **OK**.

## <a name="administration-of-personalizations"></a>Beheer van aanpassingen

De pagina **Persoonlijke instellingen** is de centrale hub voor het beheer van persoonlijke instellingen op een organisatieniveau. De inhoud en mogelijkheden op deze pagina zijn afhankelijk van de vraag of de functie **Opgeslagen weergaven** is ingeschakeld.

Zie de sectie 'Weergaven globaal beheren' in het onderwerp [Opgeslagen weergaven](saved-views.md) voor klanten die de functie **Opgeslagen weergaven** hebben ingeschakeld.

Voor klanten die de functie [Opgeslagen weergaven](saved-views.md) nog niet hebben ingeschakeld, bevat deze pagina vier tabbladen:

- **Toepassen**: u kunt een aanpassing voor een of meer gebruikers importeren of selecteren. Als u een aanpassing wilt toepassen op een of meer gebruikers, selecteert u eerst een rol en gebruikers die deze rol hebben. Vervolgens selecteert u een bestaande aanpassing om toe te passen op geselecteerde gebruikers of importeert u een aanpassingsbestand. De aanpassing wordt gevalideerd en toegepast op alle geselecteerde gebruikers. Dit wordt van kracht bij de volgende keer dat ze de geselecteerde pagina openen.

- **Wissen**: u kunt alle aanpassingen voor een pagina of werkgebied voor een of meer gebruikers wissen. Selecteer eerst een pagina of werkgebied voor een overzicht van de gebruikers die deze hebben aangepast. Kies vervolgens de gebruikers waarvoor de aanpassingen voor die pagina moeten worden gewist en selecteer **Wissen**. Alle aanpassingen die de geselecteerde gebruikers hebben toegepast op de geselecteerde pagina of het geselecteerde werkgebied, worden verwijderd. Deze actie kan niet ongedaan worden gemaakt. Als de pagina of het werkgebied echter een opgeslagen aanpassing heeft, kan die aanpassing opnieuw worden geïmporteerd.

- **Gebruikers**: selecteer een gebruiker voor een lijst met de pagina's die de gebruiker heeft aangepast. Vervolgens kunt u in- of uitschakelen of de gebruiker voor bepaalde pagina's of voor het hele systeem aanpassingen kan doorvoeren. U kunt ook een aanpassing importeren, exporteren of wissen voor de gebruiker. Daarnaast kunt u de functietoelichtingen voor de gebruiker opnieuw instellen. Als de gebruiker pop-upvensters die nieuwe functies introduceren, eerder heeft gesloten, worden deze opnieuw weergegeven wanneer de gebruiker de volgende keer de desbetreffende functie tegenkomt.

- **Systeem**: u kunt tijdelijk aanpassingen voor alle gebruikers in het systeem uitschakelen. In dat geval worden alle aanpassingen voor alle gebruikers verwijderd en worden alle pagina's opnieuw ingesteld op de standaardstatus. Als u aanpassingen later weer wilt inschakelen, worden alle aanpassingen opnieuw toegepast. U kunt alle aanpassingen voor alle gebruikers in het systeem ook permanent verwijderen. Er is geen enkele manier om aanpassingen terug te halen die zijn verwijderd. Voordat u deze taak uitvoert, moet u er daarom voor zorgen dat u aanpassingen hebt geëxporteerd die u later mogelijk wilt.

## <a name="personalizing-inventory-dimensions"></a>Voorraaddimensies aanpassen

Wanneer u de instellingen van de voorraaddimensies op een pagina wilt aanpassen, kunt u de instellingen toepassen die zijn gemaakt met de optie **Dimensie weergeven**. U gebruikt aanpassing bijvoorbeeld om een kolom te verbergen voor de voorraaddimensie Batchnummer, maar de kolom wordt de volgende keer dat de pagina wordt geopend, weergegeven. Deze werking treedt op omdat de **Weergave van dimensies**-instellingen bepalen welke voorraaddimensiekolommen worden weergegeven. De **Weergave van dimensies**-instellingen zijn van toepassing op alle pagina's en hebben voorrang op aangepaste instellingen van voorraaddimensievelden op afzonderlijke pagina's.

Als u in het vorige voorbeeld niet wilt dat de kolom voor de voorraaddimensie Batchnummer wordt weergegeven op een pagina, moet u die dimensie uitschakelen als onderdeel van de optie **Weergave van dimensies** voor die pagina.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
