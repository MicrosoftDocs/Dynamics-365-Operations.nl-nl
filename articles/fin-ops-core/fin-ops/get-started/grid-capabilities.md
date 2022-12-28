---
title: Rastermogelijkheden
description: Dit artikel beschrijft diverse krachtige functies van het rasterbesturingselement. U moet de nieuwe rasterfunctie inschakelen als u toegang tot deze mogelijkheden wilt hebben.
author: jasongre
ms.date: 08/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6d14bba13dbf701a8c27c10ac2d318b071092bc1
ms.sourcegitcommit: 77ffeccffff28fbb6ff576864d7abddd412cdab6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/15/2022
ms.locfileid: "9852368"
---
# <a name="grid-capabilities"></a>Rastermogelijkheden

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Het nieuwe rasterbesturingselement biedt verschillende handige en krachtige functies die u kunt gebruiken om de productiviteit van gebruikers te verbeteren, interessantere weergaven van uw gegevens te maken en inzicht te krijgen in uw gegevens. In dit artikel worden de volgende mogelijkheden besproken: 

- Berekende waarden weergeven 
- Voor het systeem uit typen
- Wiskundige expressies evalueren 
- Tabelgegevens groeperen (afzonderlijk ingeschakeld met de functie **Groeperen in rasters**)
- Kolommen blokkeren (afzonderlijk ingeschakeld via de functie **Kolommen blokkeren in rasters**)
- Kolombreedte automatisch aanpassen
- Uitrekbare kolommen

## <a name="showing-calculated-values"></a>Berekende waarden weergeven
In apps voor financiën en bedrijfsactiviteiten kunnen gebruikers een berekende waarde weergeven voor elke numerieke kolom in een raster. Deze berekende waarden worden weergegeven in een voettekstgedeelte onder in het raster.

[![Berekende waarden weergeven in rasters.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

In versies vóór 10.0.29 is het totaal de enige ondersteunde berekende waarde. Vanaf versie 10.0.29 kunnen gebruikers echter, na het inschakelen van de functie **Voorzieningen voor uitgebreide-rasteraggregaties**, uit de volgende vier berekende waarden kiezen:

- Minimum
- Maximum
- Totaal
- Gemiddeld

Eén kolom kan slechts één type berekende waarde tonen. Elke kolom in het raster kan echter zo worden geconfigureerd dat er een ander type berekende waarde wordt gebruikt.

### <a name="showing-the-grid-footer"></a>De rastervoettekst weergeven
Onder aan elk raster in tabelvorm in apps voor financiën en bedrijfsactiviteiten bevindt zich een voettekstgebied. In de voettekst kunnen waardevolle gegevens worden weergegeven die betrekking hebben op de gegevens die in het raster worden weergegeven. Hiermee volgen enkele voorbeelden van dergelijke informatie:

- Het aantal geselecteerde rijen in de tabel (wanneer u meer dan één record selecteert)
- Berekende waarden onder aan geconfigureerde numerieke kolommen (bijv. totalen)
- Het aantal rijen in de gegevensset 

Deze voettekst is standaard verborgen, maar u kunt deze inschakelen. Als u de voettekst voor een raster wilt weergeven, klikt u op de knop **Rasteropties** in rasterkop en selecteert u de optie **Voettekst weergeven**. Nadat u de voettekst voor een bepaald raster hebt ingeschakeld, wordt deze instelling gebruikt totdat de gebruiker ervoor kiest om de voettekst te verbergen. Als u de voettekst wilt verbergen, selecteert u **Voettekst verbergen** in het menu **Rasteropties**.

### <a name="specifying-columns-with-calculated-values"></a>Kolommen met berekende waarden opgeven
Op dit moment worden berekende waarden niet standaard in kolommen weergegeven. In plaats daarvan wordt het instellen beschouwd als een eenmalige activiteit, vergelijkbaar met het aanpassen van de breedte van kolommen in rasters. Nadat u hebt opgegeven dat u een berekende waarde voor een kolom wilt bekijken, wordt deze instelling de volgende keer dat u de pagina bezoekt, onthouden.

Er zijn twee manieren om een kolom te configureren voor het weergeven van een berekende waarde:

- Selecteer de kolom en houd de muisknop ingedrukt (of klik met de rechtermuiskop)waarvoor u de berekende waarde wilt weergeven. Selecteer, als de functie **Voorzieningen voor uitgebreide rasteraggregaties** is ingeschakeld, **Kolomtotalen weergeven** en selecteer vervolgens de gewenste berekende waarde. Als deze functie niet is ingeschakeld, selecteer dan **Totaal deze kolom**. Door deze actie worden er drie gebeurtenissen uitgevoerd:

    1. De voettekst voor het raster wordt zichtbaar. 
    2. Uw voorkeur voor het weergeven van een berekende waarde voor de kolom wordt opgeslagen. 
    3. De gewenste berekening wordt uitgevoerd voor de kolom en alle andere kolommen die u eerder hebt geconfigureerd voor het weergeven van een berekende waarde. De tijd die nodig is om de berekende waarden weer te geven, is afhankelijk van de grootte van de gegevensset.

- Selecteer, nadat de voettekst zichtbaar is, **Totaal weergeven** (of **Berekende waarde selecteren** als de functie **Voorzieningen voor uitgebreide rasteraggregaties** is ingeschakeld) in het voettekstgebied onderaan de kolom waar u een berekende waarde voor wilt weergeven. Als er geen geconfigureerde kolommen zijn, wordt die knop beschikbaar in de voettekst voor alle numerieke kolommen.

    Nadat ten minste één kolom zo is geconfigureerd dat er een berekende waarde wordt weergeven,is de knop **Totaal weergeven** (of **Berekende waarde selecteren**) alleen beschikbaar voor muisaanwijzers of focus. De actie van het selecteren van de knop slaat de voorkeur op voor het weergeven van een berekende waarde in de kolom, zodat de voorkeur wordt toegepast tijdens toekomstige bezoeken aan de pagina. In de voettekst wordt deze toestand aangegeven via een streepje dat in de kolom wordt weergegeven. (NB: de berekende waarde wordt onmiddellijk weergegeven als de dataset klein genoeg is.)

Als u een fout maakt en u een berekende waarde in een bepaalde kolom niet meer wilt weergeven, selecteert u de waarde in de kolom en houdt u de muisknop ingedrukt (of klikt u met de rechtermuisknop) en selecteert u **Totaal verbergen** (of **Kolomtotalen weergeven \> Geen** als de functie **Voorzieningen uitgebreide rasteraggregaties** is ingeschakeld). U kunt ook **Totaal verbergen** (of **Berekende waarde verbergen**) selecteren in de voettekst van die kolom. Deze voorkeur wordt ook opgeslagen voor toekomstige bezoeken aan de pagina. 

### <a name="calculating-aggregate-values"></a>Geaggregeerde waarden berekenen
Wanneer u naar een pagina gaat waar de voettekst zichtbaar is en in kolommen al berekende waarden zijn weergegeven, worden die waarden mogelijk niet weergegeven in de voettekst. Het gedrag is afhankelijk van de grootte van de gegevensset op de pagina. Als de gegevensset klein genoeg is, worden de berekende waarden automatisch getoond, samen met het aantal rijen in de gegevensset. Als er streepjes in de voettekst staan onder de kolommen die u hebt geconfigureerd, is de gegevensset te groot om het systeem de berekende waarden direct weer te laten geven. In dat geval is expliciete actie vereist om de waarden te berekenen. Als u de waarden wilt berekenen, klikt u op de knop **Berekenen** in de voettekst. U kunt ook een kolom selecteren en de muisknop ingedrukt houden (of klikken met de rechtermuisknop) waarvoor u de totalen wilt weergeven en daarna **Totaal deze kolom** selecteren (of **Kolomtotalen weergeven** en vervolgens de gewenste berekende waarde als de functie **Voorzieningen uitgebreide rasteraggregaties** is ingeschakeld).

Als het voltooien van de berekening te lang duurt, kunt u de bewerking op elk gewenst moment annuleren door **Annuleren** te selecteren. Soms is de gegevensset te groot om geaggtegeerde waarden te berekenen (een limiet die door uw organisatie wordt opgelegd). In dit geval krijgt u de melding dat u uw gegevens beter moet filteren.

> [!NOTE]
> Systeembeheerders kunnen de limiet voor het aantal records dat beschikbaar is voor het berekenen van geaggregeerde waarden wijzigen door de parameter **Maximum aantal lokale records voor elk raster** op de pagina **Prestatieopties voor de client** aan te passen. De standaardwaarde is 25.000 records. Beheerders moeten voorzichtig zijn bij het aanpassen van deze waarde, omdat een te grote waarde teveel geheugen gebruikt op de machine van de gebruiker. Het wordt aanbevolen om deze waarde niet hoger in te stellen dan 50.000 records.

Berekende waarden worden automatisch bijgewerkt wanneer u rijen in de gegevensset bijwerkt, verwijdert of aanmaakt.

## <a name="typing-ahead-of-the-system"></a>Voor het systeem uit typen
In veel zakelijke scenario's is het heel belangrijk om snel gegevens in het systeem in te voeren. Voordat het nieuwe rasterbesturingselement werd geïntroduceerd, konden gebruikers gegevens alleen in de huidige rij wijzigen. Daardoor konden gebruikers, nadat ze wijzigingen in een rij hadden aangebracht, niet naar een andere rij overschakelen of een nieuwe rij aanmaken totdat het systeem de wijzigingen in de huidige rij had gevalideerd en (in geval van het aanmaken van een rij) alle logica had uitgevoerd die is gekoppeld aan het aanmaken van een nieuwe rij. In een poging de tijd die gebruikers moeten wachten op de voltooiing van deze validaties te beperken en om de productiviteit van gebruikers te verbeteren, worden deze acties door het nieuwe raster zodanig aangepast dat ze asynchroon worden uitgevoerd. Gebruikers kunnen dus nieuwe rijen aanmaken of naar andere rijen gaan om wijzigingen aan te brengen terwijl de validatie van de vorige rij en de logica voor het aanmaken van rijen in behandeling zijn. 

[![Voor het systeem uit typen.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Ter ondersteuning van dit nieuwe gedrag is er een nieuwe kolom voor de rijstatus rechts van de rijselectiekolom toegevoegd wanneer het raster in de bewerkingsmodus staat. Deze kolom geeft een van de volgende statussen aan:

- **Leeg**: geen statusafbeelding geeft aan dat de rij door het systeem is opgeslagen.
- **Verwerking in behandeling:** deze status geeft aan dat de wijzigingen in de rij nog niet zijn opgeslagen door de server, maar zich in een wachtrij met wijzigingen bevinden die moeten worden verwerkt. Voordat u actie onderneemt buiten het raster, moet u wachten tot alle wijzigingen in behandeling zijn verwerkt. Bovendien wordt de tekst in deze rijen cursief gemaakt om de niet-opgeslagen status van de rijen aan te geven. 
- **Ongeldige status**: deze status geeft aan dat tijdens het verwerken van de rij een waarschuwing of een bericht is gegenereerd en dat het systeem hierdoor mogelijk de wijzigingen in die rij niet kan opslaan. In het oude raster moest u terug naar de rij om het probleem onmiddellijk op te lossen. In het nieuwe raster krijgt u echter een melding dat er een validatieprobleem is aangetroffen, maar u kunt zelf bepalen wanneer u de problemen in de rij wilt oplossen. Wanneer u klaar bent om een probleem op te lossen, kunt u de focus handmatig naar de rij verplaatsen. U kunt ook de actie **Dit probleem oplossen** selecteren. Met deze actie gaat u direct terug naar de rij met het probleem en kunt u de wijzigingen binnen of buiten het raster aanbrengen. De verwerking van volgende rijen in behandeling wordt gestopt totdat deze validatiewaarschuwing is opgelost. 
- **Onderbroken**: deze status geeft aan dat de verwerking door de server is onderbroken omdat de validatie van de rij een pop-updialoogvenster heeft geactiveerd waarvoor invoer van de gebruiker nodig is. Omdat de gebruiker mogelijk gegevens in een andere rij invoert, wordt het pop-upvenster niet onmiddellijk aan die gebruiker weergegeven. In plaats daarvan wordt het weergegeven wanneer de gebruiker de verwerking wil hervatten. Deze status gaat vergezeld van een melding waarin de gebruiker wordt geïnformeerd over de situatie. De melding bevat een actie **Verwerking hervatten** waarmee het pop-updialoogvenster wordt geactiveerd.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Verschillen bij het invoeren van gegevens voor het systeem uit
Wanneer u gegevens invoert op een locatie die vóór de plaats ligt waar het systeem aan het verwerken is, kunt u enkele wijzigingen verwachten in de ervaring met gegevensinvoer:

- U ziet dat er geen vervolgkeuzelijsten voor opzoeken zijn, dat veldwaarden niet worden gevalideerd nadat u naar een andere kolom in dezelfde rij bent gegaan en dat er in de kolommen in eerste instantie geen standaardwaarden worden weergegeven. Dit gedrag treedt op wanneer u voor het systeem uit werkt met iets aanmaken of bijwerken. Nadat het systeem u echter inhaalt en op de plek komt waar u aan het bewerken bent, wordt de standaardervaring hervat. Als u wijzigingen hebt aangebracht in een veld dat doorgaans een standaardwaarde ontvangt, overschrijven uw wijzigingen de standaardveldwaarde wanneer de server de rij gaat verwerken.
- Als u een nieuwe rij aanmaakt met de toets **pijl-omlaag**, worden alle kolommen in het raster als bewerkbaar weergegeven. Standaard wordt de focus in de eerste kolom van de nieuwe rij geplaatst. Deze kolom is mogelijk niet dezelfde kolom als de oorspronkelijke focus in het verouderde raster, of dezelfde kolom die de focus ontvangt nadat u een knop **Nieuw** hebt geselecteerd. Uw organisatie kan het systeem aanpassen en de kolom wijzigen die de eerste focus krijgt wanneer de toets **pijl-omlaag** wordt geselecteerd. Raadpleeg [De kolom opgeven die de eerste focus krijgt wanneer nieuwe rijen worden aangemaakt met behulp van de toets Pijl-omlaag](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key) voor meer informatie. Hoe dan ook, u kunt de personalisatie gebruiken om elk raster voor gegevensinvoer te optimaliseren. Met name kunt u velden opnieuw ordenen, zodat de eerste kolom de kolom is waarin u gegevens wilt gaan invoeren. Mogelijk wilt u ook velden in het algemeen opnieuw ordenen voor gegevensinvoer, zodat u het aantal tabstops kunt beperken en velden kunt verbergen die in deze specifieke weergave niet nodig zijn voor gegevensinvoer.

### <a name="pasting-from-excel"></a>Plakken vanuit Excel
Gebruikers kunnen altijd gegevens vanuit rasters in apps voor financiën en bedrijfsactiviteiten naar Microsoft Excel exporteren met het mechanisme **Exporteren naar Excel**. Doordat het mogelijk is om gegevens in te voeren vóór de systeemverwerking, ondersteunt het nieuwe raster echter het kopiëren van tabellen vanuit Excel en kunnen deze rechtstreeks in rasters in apps voor financiën en bedrijfsactiviteiten worden geplakt. In de rastercel waaruit de plakbewerking wordt geïnitieerd, wordt bepaald waar de gekopieerde tabel wordt geplakt. De inhoud van het raster wordt overschreven door de inhoud van de gekopieerde tabel, behalve in twee gevallen:

- Als het aantal kolommen in de gekopieerde tabel groter is dan het aantal kolommen dat in het raster overblijft, te beginnen bij de plaklocatie, krijgt de gebruiker een melding dat de extra kolommen zijn genegeerd. 
- Als het aantal rijen in de gekopieerde tabel groter is dan het aantal rijen in het raster, te beginnen bij de plaklocatie, worden de bestaande cellen overschreven door de geplakte inhoud en worden alle extra rijen uit de gekopieerde tabel ingevoegd als nieuwe rijen onder in het raster. 

## <a name="evaluating-math-expressions"></a>Wiskundige expressies evalueren
Ter bevordering van de productiviteit kunnen gebruikers wiskundige formules invoeren in numerieke cellen in een raster. Zij hoeven de berekening niet uit te voeren in een app buiten het systeem. Als u bijvoorbeeld **= 15\*4** invoert en vervolgens op de **tabtoets** drukt om het veld te verlaten, wordt de expressie geëvalueerd en wordt de waarde **60** opgeslagen voor het veld.

[![Wiskundige expressies evalueren.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Als u wilt dat het systeem een waarde herkent als een expressie, start u de waarde met het gelijkteken (**=**). Zie [Ondersteunde wiskundige symbolen](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols) voor meer informatie over de ondersteunde operators en syntaxis.

Vanaf versie 10.0.29 is de mogelijkheid om wiskundige expressies in numerieke besturingselementen te evalueren uitgebreid; deze is nu ook buiten het raster beschikbaar.

## <a name="grouping-tabular-data"></a>Tabelgegevens groeperen
Zakelijke gebruikers moeten vaak ad hoc gegevensanalyses uitvoeren. Hoewel deze analyse kan worden gedaan door gegevens te exporteren naar Microsoft Excel en draaitabellen te gebruiken, biedt de functie **Groeperen in rasters**, die afhankelijk is van de functie Nieuw rasterbesturingselement, gebruikers de mogelijkheid hun tabelgegevens op interessante manieren te ordenen in apps voor financiën en bedrijfsactiviteiten. Aangezien deze functie de functie **Berekende waarden** uitbreidt, kunt u met **Groepering** duidelijke inzichten krijgen in de gegevens door berekende waarden (bijvoorbeeld subtotalen) op groepsniveau aan te bieden.

[![Gegevens in een raster groeperen.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Als u deze functie wilt gebruiken, klikt u met de rechtermuisknop op de kolom waarop u wilt groeperen en selecteert u **Groeperen op deze kolom**. Met deze actie sorteert u de gegevens op de geselecteerde kolom, voegt u een nieuwe kolom **Groeperen op** toe aan het begin van het raster en voegt u 'koptekstrijen' toe aan het begin van elke groep. Deze koptekstrijen bevatten de volgende informatie over elke groep:

- Gegevenswaarde voor de groep 
- Kolomnaam (deze informatie is vooral nuttig wanneer u meerdere groeperingsniveaus hebt)
- Aantal gegevensrijen in deze groep
- Berekende waarden voor een geconfigureerde kolom (bijvoorbeeld subtotalen als de kolom zo is geconfigureerd dat er een totaal wordt berekend)

Als [Opgeslagen weergaven](saved-views.md) is ingeschakeld, kunt u groeperingen opslaan als onderdeel van een weergave op pagina's waarmee query's in weergaven kunnen worden opgeslagen. Bijvoorbeeld voor grote weergave-selectors. Zie [Schakelen tussen weergaven](saved-views.md#switching-between-views) voor meer informatie. 

### <a name="multiple-levels-of-grouping"></a>Meerdere groeperingsniveaus
Nadat u gegevens hebt gegroepeerd op een enkele kolom, kunt u de gegevens groeperen op een andere kolom door **Groeperen op deze kolom** te selecteren in de gewenste kolom. Dit proces kan worden herhaald totdat u 5 geneste groeperingsniveaus hebt. Dit is de maximale diepte die wordt ondersteund. Op dit punt kunt u niet meer op extra kolommen groeperen.

U kunt op elk gewenst moment de groepering op een willekeurige kolom verwijderen door met de rechtermuisknop op de kolom te klikken en **Groep opheffen** te selecteren. U kunt de groepering ook uit alle kolommen verwijderen door **Rasteropties** en vervolgens **Alle groeperingen opheffen** te selecteren.

### <a name="sorting-grouped-data"></a>Gegroepeerde gegevens sorteren
Als u gegevens op een of meer kolommen hebt gegroepeerd, kunt u via de bijbehorende kolomkop de sorteerrichting voor een groeperingskolom wijzigen. 

Als u op een niet-gegroepeerde kolom sorteert, blijft de groepering intact. De gegevens worden in elke groep gesorteerd op basis van de geselecteerde kolom.

### <a name="expanding-and-collapsing-groups"></a>Groepen uitvouwen en samenvouwen
Bij de eerste groepering van gegevens worden zijn alle groepen uitgevouwen. U kunt samengevatte weergaven van de gegevens maken door afzonderlijke groepen samen te vouwen of u kunt de functie voor het uit- en samenvouwen van groepen gebruiken om te helpen bij het navigeren door de gegevens. Als u een groep wilt uitvouwen of samenvouwen, selecteert u de punthaakknop (>) in de desbetreffende rij van de groepskoptekst. De status voor uitvouwen/samenvouwen van afzonderlijke groepen wordt **niet** opgeslagen bij personalisatie.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Rijen op groepsniveau selecteren en de selectie ervan opheffen
Op dezelfde manier waarop u alle rijen in het raster kunt selecteren (of deselecteren) door het selectievakje boven aan de eerste kolom in het raster in te schakelen, kunt u ook snel alle rijen in een groep selecteren (of deselecteren) door het selectievakje in de desbetreffende rij van de groepskop tekst in te schakelen. Het selectievakje in de rij van de groepskoptekst komt altijd overeen met de huidige selectiestatus van rijen in die groep, ongeacht of alle rijen zijn geselecteerd, er geen rijen zijn geselecteerd of er slechts enkele rijen zijn geselecteerd.

### <a name="hiding-column-names"></a>Kolomnamen verbergen
Wanneer u gegevens groepeert, wordt standaard de kolomnaam weergegeven in de rij van de groepskoptekst. U kunt de kolomnaam in groepskoprijen onderdrukken door **Rasteropties** > **Groepskolomnaam verbergen** te selecteren.

### <a name="grouping-on-date-and-time-columns"></a>Groeperen op datum- en tijdkolommen
Wanneer u op een veld Datum of Datum/tijd groepeert, kunt u groeperen op basis van jaar, maand of dag. De groepswaarde in de bijbehorende koptekstrij komt overeen met de indeling uit dat veld. Bovendien kunt u met de velden Datum/tijd en Tijd groeperen op basis van uur, minuut of seconde.

> [!IMPORTANT]
> Gebruikers kunnen momenteel geen groeperingskolom toevoegen na groepering in een segment van een datum- of tijdkolom.

## <a name="freezing-columns"></a>Kolommen blokkeren
Sommige kolommen in een raster kunnen dermate belangrijk zijn voor context dat u niet wilt dat ze uit de weergave verdwijnen. In plaats daarvan wilt u mogelijk dat de waarden in die kolommen altijd zichtbaar zijn. De functie **Kolommen blokkeren in raster** biedt deze flexibiliteit voor gebruikers. 

[![Kolommen in een raster blokkeren](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Als u een kolom wilt blokkeren, klikt u met de rechtermuisknop in de koptekst van de kolom en selecteert u vervolgens **Kolom blokkeren**. De eerste keer dat u deze stap voltooit, wordt de geselecteerde kolom de eerste kolom en verdwijnt deze niet meer uit de weergave. Alle volgende kolommen die u blokkeert, worden rechts van de laatste geblokkeerde kolom toegevoegd. U kunt de standaardfunctie Verplaatsen gebruiken om desgewenst geblokkeerde kolommen opnieuw te ordenen. Geblokkeerde kolommen kunnen echter niet worden verplaatst, zodat ze tussen de set met niet-geblokkeerde kolommen worden weergegeven. Zo ook kunnen niet-geblokkeerde kolommen niet worden verplaatst, zodat ze tussen de set met geblokkeerde kolommen worden weergegeven.

Als u de blokkering van een kolom wilt opheffen, klikt u met de rechtermuisknop in de koptekst van de geblokkeerde kolom en selecteert u vervolgens **Blokkering kolom opheffen**. 

De kolommen voor rijselectie en rijstatus in het nieuwe raster zijn altijd als de eerste twee kolommen geblokkeerd. Als deze kolommen in een raster worden opgenomen, zijn deze dus altijd zichtbaar voor gebruikers, ongeacht de horizontale schuifpositie in het raster. De volgorde van deze twee kolommen kan niet worden gewijzigd.

## <a name="autofit-column-width"></a>Kolombreedte automatisch aanpassen
Net als in Excel kunnen gebruikers de grootte van een kolom geforceerd automatisch wijzigen op basis van de inhoud die op dat moment in die kolom wordt weergegeven. Dubbeltik (of dubbelklik) gewoon op de formaatgrepen in de kolom. U kunt ook de focus in de header van de kolom zetten en vervolgens de toets **A** selecteren (voor automatisch aanpassen).

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hoe kan ik het nieuwe rasterbesturingselement inschakelen in mijn omgeving? 

De functie **Nieuw rasterbesturingselement** is in elke omgeving rechtstreeks beschikbaar in Functiebeheer. Als de functie in Functiebeheer is ingeschakeld, maken alle volgende gebruikerssessies gebruik van de nieuwe rasterbesturing. 

Deze functie is standaard ingeschakeld in versie 10.0.21. Het is het doel om deze verplicht te stellen in oktober 2022.

## <a name="developer-topics"></a>Onderwerpen voor ontwikkelaars

### <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Ontwikkelaar] Uitschakelen dat afzonderlijke pagina's het nieuwe raster gebruiken 
Als uw organisatie een pagina vindt met problemen met het nieuwe raster, is er een API beschikbaar waarmee een afzonderlijk formulier het oude rasterbesturingselement kan gebruiken, terwijl de rest van het systeem nog steeds het nieuwe rasterbesturingselement kan gebruiken. Als u een afzonderlijke pagina voor het nieuwe raster wilt afmelden, voegt u de volgende aanroep `super()` toe aan de methode `run()` van het formulier.

```this.forceLegacyGrid();```

Deze API wordt uiteindelijk afgeschaft om verwijdering van het besturingselement van het verouderde raster mogelijk te maken. De API blijft echter wel beschikbaar voor ten minste 12 maanden nadat de afschaffing is aangekondigd. Als er problemen optreden waarvoor deze API moet worden gebruikt, meldt u deze bij Microsoft.

#### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Afdwingen van een pagina om het nieuwe raster te gebruiken nadat eerder het raster is uitgeschakeld
Als u een individuele pagina hebt uitgeschreven voor gebruik van het nieuwe raster, zou u het nieuwe raster later opnieuw kunnen inschakelen nadat de onderliggende problemen zijn opgelost. Hiervoor hoeft u alleen de aanroep van `forceLegacyGrid()` te verwijderen. De wijziging wordt pas doorgevoerd wanneer een van de volgende zaken zich voordoet:

- **Opnieuw implementeren omgeving**: wanneer een omgeving wordt bijgewerkt en opnieuw geïmplementeerd, wordt de tabel waarin de pagina's zijn opgeslagen die zijn uitgeschreven voor het nieuwe raster (FormControlReactGridState) automatisch leeggemaakt.
- **Handmatige leegmaken van de tabel**: voor ontwikkelingsscenario's moet u SQL gebruiken om de tabel FormControlReactGridState leeg te maken en vervolgens de AOS opnieuw opstarten. Met deze combinatie van acties wordt de caching opnieuw ingesteld voor pagina's die zijn uitgeschreven voor het nieuwe raster.

### <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Ontwikkelaar] De mogelijkheid Voor het systeem uit typen niet gebruiken voor afzonderlijke rasters
In sommige scenario's is het niet handig de rasterfunctie *Voor het systeem uit typen* te gebruiken. (Door een bepaalde code die bijvoorbeeld wordt geactiveerd tijdens het valideren van een rij, wordt een gegevensbrononderzoek geactiveerd en kunnen onbewerkte bewerkingen op bestaande rijen beschadigd raken.) Als uw organisatie een dergelijk scenario ontdekt, is er een API beschikbaar waarmee een ontwikkelaar voor een afzonderlijk raster kan kiezen geen asynchrone rijvalidatie te gebruiken en kan terugkeren naar het verouderde gedrag.

Wanneer asynchrone rijvalidatie in een raster is uitgeschakeld, kunnen gebruikers geen nieuwe rij maken of naar een andere bestaande rij in het raster gaan terwijl er validatieproblemen zijn op de huidige rij. Als gevolg van deze actie kunnen tabellen niet vanuit Excel in rasters voor financiën en bedrijfsactiviteiten worden geplakt.

Als u voor een afzonderlijk raster geen asynchrone rijvalidatie wilt gebruiken, voegt u de volgende aanroep na `super()` in de methode `run()` van het formulier toe.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Deze aanroep moet slechts in uitzonderlijke gevallen worden aangeroepen en mag niet de norm zijn voor alle rasters.
> - Het is niet aan te raden deze API te kiezen tijdens runtime nadat het formulier is geladen.

### <a name="developer-size-to-available-width-columns"></a>\[Ontwikkelaar\]: kolomformaat aangepast aan beschikbare breedte
Als een ontwikkelaar de eigenschap **WidthMode** instelt op **SizeToAvailable** voor kolommen binnen het nieuwe raster, hebben deze kolommen in eerste instantie dezelfde breedte als ze zouden hebben als de eigenschap is ingesteld op **SizeToContent**. De kolommen worden echter uitgerekt zodat alle extra beschikbare breedte binnen het raster wordt gebruikt. Als de eigenschap is ingesteld op **SizeToAvailable** voor meerdere kolommen, delen al deze kolommen de extra beschikbare breedte binnen het raster. Als een gebruiker echter een van deze kolommen handmatig aanpast, wordt de kolom statisch. De kolom behoudt die breedte en wordt niet meer uitgerekt tot extra beschikbare rasterbreedte.

### <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Developer] De kolom opgeven die de eerste focus krijgt wanneer nieuwe rijen worden aangemaakt met behulp van de toets Pijl-omlaag
Zoals is besproken in [Verschillen bij het invoeren van gegevens voor het systeem uit](#differences-when-entering-data-ahead-of-the-system): als de mogelijkheid 'Typen voor het systeem uit' is ingeschakeld en een gebruiker een nieuwe rij aanmaakt met behulp van de toets **Pijl-omlaag**, is het standaardgedrag om de focus in de eerste kolom van de nieuwe rij te zetten. Deze ervaring kan afwijken van de ervaring in het verouderde raster of wanneer een knop **Nieuw** wordt geselecteerd.

Gebruikers en organisaties kunnen opgeslagen weergaven aanmaken die zijn geoptimaliseerd voor de invoer van gegevens. (U kunt bijvoorbeeld kolommen opnieuw ordenen zodat de eerste kolom de kolom is waarin u gegevens wilt invoeren.) Bovendien kunnen organisaties dit gedrag vanaf versie 10.0.29 aanpassen met de methode **selectedControlOnCreate()**. Met deze methode kan een developer de kolom opgeven die de eerste focus moet krijgen wanneer een nieuwe rij wordt aangemaakt met behulp van de toets **Pijl-omlaag**. Als invoer neemt deze API de controle-ID over die overeenkomt met de kolom die de eerste focus moet krijgen.

### <a name="developer-handling-grids-with-non-react-extensible-controls"></a>[Ontwikkelaar] Rasters verwerken met niet-React uitbreidbare besturingselementen
Wanneer een raster wordt geladen en het systeem een uitbreidbaar besturingselement krijgt dat niet is gebaseerd op React, wordt het verouderde raster weergegeven. Wanneer een gebruiker voor het eerst deze situaties aantreft, wordt een bericht weergegeven over het vernieuwen van de pagina. Vervolgens zal deze pagina het verouderde raster automatisch laden zonder verdere meldingen aan gebruikers tot de volgende systeemupdate. 

Om deze situatie permanent te voorkomen, kunnen auteurs van uitbreidbare besturingselementen een React-versie van het besturingselement maken om in het raster te gebruiken.  Nadat deze is ontwikkeld, kan de X++-klasse voor het besturingselement worden aangeduid met het kenmerk **FormReactControlAttribute** om de locatie op te geven van de React-bundel die voor het besturingselement moet worden geladen. Zie de `SegmentedEntryControl`-klasse als voorbeeld.  

## <a name="known-issues"></a>Bekende problemen
In deze sectie wordt een lijst met bekende problemen voor het nieuwe rasterbeheer bijgehouden.

### <a name="open-issues"></a>Openstaande problemen
- Nadat de functie **Nieuw rasterbesturingselement** is ingeschakeld, blijven bepaalde pagina's het bestaande rasterbesturingselement gebruiken. Dit gebeurt in de volgende situaties:
 
    - [Opgelost] Probleem-762533: onverwachte clientfout bij het selecteren van een rij in een kaartlijst.
    - [Opgelost] Er bestaat een kaartlijst op de pagina die wordt weergegeven in meerdere kolommen.
        - Dit type kaartlijst wordt ondersteund door het besturingselement **Nieuw raster** vanaf versie 10.0.30. Alle toepassingen van forceLegacyGrid() kunnen dan worden verwijderd. 
    - [Opgelost] Er bestaat een gegroepeerde kaartlijst op de pagina.
        - Gegroepeerde kaartlijsten worden ondersteund door het besturingselement **Nieuw raster** vanaf versie 10.0.30. Alle toepassingen van forceLegacyGrid() kunnen dan worden verwijderd. 
    - [Opgelost] Een rasterkolom met een niet-React uitbreidbaar besturingselement.
        - Uitbreidbare besturingselementen kunnen een React-versie leveren die wordt geladen wanneer ze in het raster worden geplaatst en de definitie aanpassen om dit besturingselement te laden wanneer het in het raster wordt gebruikt. Zie het bijbehorende ontwikkelaarsgedeelte voor meer details. 

    Wanneer een gebruiker voor het eerst een van deze situaties aantreft, wordt een bericht weergegeven over het vernieuwen van de pagina. Nadat dit bericht is weergegeven, blijft de pagina het bestaande raster gebruiken voor alle gebruikers tot de volgende update van de productversie. Een betere afhandeling van deze scenario's zodat het nieuwe raster kan worden gebruikt, wordt overwogen voor een toekomstige update.

- [KB 4582758] Records zijn wazig wanneer u de zoomfactor wijzigt van 100 in een ander percentage

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

