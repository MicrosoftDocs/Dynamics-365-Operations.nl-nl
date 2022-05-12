---
title: Rastermogelijkheden
description: Dit onderwerp beschrijft diverse krachtige functies van het rasterbesturingselement. U moet de nieuwe rasterfunctie inschakelen als u toegang tot deze mogelijkheden wilt hebben.
author: jasongre
ms.date: 04/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 57133a853d1700b2d8ebb938f93af475410b82cb
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644352"
---
# <a name="grid-capabilities"></a>Rastermogelijkheden

[!include [banner](../includes/banner.md)]

Het nieuwe rasterbesturingselement biedt verschillende handige en krachtige functies die u kunt gebruiken om de productiviteit van gebruikers te verbeteren, interessantere weergaven van uw gegevens te maken en inzicht te krijgen in uw gegevens. In dit artikel worden de volgende mogelijkheden besproken: 

- Totalen worden berekend
- Voor het systeem uit typen
- Wiskundige expressies evalueren 
- Tabelgegevens groeperen (afzonderlijk ingeschakeld met de functie **Groeperen in rasters**)
- Kolommen blokkeren (afzonderlijk ingeschakeld via de functie **Kolommen blokkeren in rasters**)
- Kolombreedte automatisch aanpassen
- Uitrekbare kolommen

## <a name="calculating-totals"></a>Totalen worden berekend
In apps voor financiële en bedrijfsactiviteiten kunnen gebruikers totalen weergeven onder aan numerieke kolommen in rasters. Deze totalen worden weergegeven in een voettekstsectie onder in het raster. 

### <a name="showing-the-grid-footer"></a>De rastervoettekst weergeven
Onder aan elk raster in tabelvorm in apps voor financiële en bedrijfsactiviteiten bevindt zich een voettekstgebied. In de voettekst kunnen waardevolle gegevens worden weergegeven die betrekking hebben op de gegevens die in het raster worden weergegeven. Hiermee volgen enkele voorbeelden van dergelijke informatie:

- Het aantal geselecteerde rijen in de tabel (wanneer u meer dan één record selecteert)
- Eindtotalen onder aan geconfigureerde numerieke kolommen
- Het aantal rijen in de gegevensset 

Deze voettekst is standaard verborgen, maar u kunt deze inschakelen. Als u de voettekst voor een raster wilt weergeven, klikt u op de knop **Rasteropties** in rasterkop en selecteert u de optie **Voettekst weergeven**. Nadat u de voettekst voor een bepaald raster hebt ingeschakeld, wordt deze instelling gebruikt totdat de gebruiker ervoor kiest om de voettekst te verbergen. Als u de voettekst wilt verbergen, selecteert u **Voettekst verbergen** in het menu **Rasteropties**.

### <a name="specifying-columns-with-totals"></a>Kolommen met totalen opgeven
Op dit moment worden totalen niet standaard in kolommen weergegeven. In plaats daarvan wordt dit beschouwd als een eenmalige instelactiviteit, vergelijkbaar met het aanpassen van de breedte van kolommen in rasters. Wanneer u hebt opgegeven dat u totalen voor een kolom wilt weergeven, wordt deze instelling de volgende keer dat u de pagina bezoekt, onthouden.

Er zijn twee manieren om een kolom te configureren voor het weergeven van totalen: 

- Klik met de rechtermuisknop in de kolom waarvoor u een totaal wilt bekijken en selecteer vervolgens **Deze kolom totaliseren**. Door deze actie worden er drie gebeurtenissen uitgevoerd:

    1. De voettekst wordt weergegeven. 
    2. Uw voorkeur voor het bekijken van een totaal voor deze kolom wordt opgeslagen. 
    3. Er wordt een berekening uitgevoerd van totalen voor deze kolom en alle andere kolommen die u eerder hebt geconfigureerd voor het weergeven van totalen. De tijd die nodig is om een totaal weer te geven, is afhankelijk van de grootte van de gegevensset die u samentelt.

- Nadat de voettekst zichtbaar is geworden, selecteert u **Totaal weergeven** in het voettekstgebied onder aan de kolom waarvoor u een totaal wilt weergeven. Als er geen geconfigureerde kolommen zijn, wordt de knop **Totaal weergeven** beschikbaar voor alle numerieke kolommen. 

    Nadat ten minste één kolom is geconfigureerd voor totalen, zijn de knoppen **Totaal weergeven** alleen beschikbaar bij aanwijzen of focus. Als u **Totaal weergeven** selecteert, wordt uw voorkeur voor het bekijken van totalen in deze kolom opgeslagen, zodat de voorkeur wordt toegepast tijdens toekomstige bezoeken aan de pagina. In de voettekst wordt deze toestand aangegeven via een streepje dat in de kolom wordt weergegeven. (Als de gegevensset klein genoeg is, wordt onmiddellijk een totaal weergegeven.)

Als u een fout maakt en geen totaal meer wilt zien in een bepaalde kolom, klikt u met de rechtermuisknop op de kolom en selecteert u **Totaal verbergen** of selecteert u de knop **Totaal verbergen** in de voettekst in die kolom. Deze voorkeur wordt ook opgeslagen voor toekomstige bezoeken aan de pagina. 

### <a name="calculating-totals"></a>Totalen worden berekend
Wanneer een pagina met de voettekst zichtbaar is en de kolommen al zijn geconfigureerd voor totalen, worden de totalen al dan niet weergegeven in de voettekst. Het gedrag is afhankelijk van de grootte van de gegevensset op de pagina. Als de gegevensset voldoende klein is, worden de totalen automatisch weergegeven, samen met het aantal rijen in de gegevensset. Als er streepjes in de voettekst staan onder de kolommen die u voor de totalen hebt geconfigureerd, is de gegevensset te groot voor het systeem om totalen direct weer te geven en is er een expliciete actie nodig om de totalen te berekenen. Klik hiervoor op de knop **Berekenen** in de voettekst of klik met de rechtermuisknop op een kolom waarvoor u een totaal wilt berekenen en selecteer **Deze kolom totaliseren**.

Als de berekening te lang duurt, kunt u de bewerking annuleren door de knop **Annuleren** te selecteren. Soms is de gegevensset te groot voor het berekenen van totalen (een limiet die is ingesteld door uw organisatie) en wordt u in plaats hiervan op de hoogte gesteld om uw gegevens te filteren. 

> [!NOTE]
> Systeembeheerders kunnen de limiet voor het aantal beschikbare records voor het berekenen van totalen wijzigen door de parameter **Maximum aantal lokale records voor elk raster** aan te passen op de pagina **Prestatieopties voor de client**. De standaardwaarde is 25.000 records. Beheerders moeten voorzichtig zijn bij het aanpassen van deze waarde, omdat een te grote waarde teveel geheugen verbruikt. Aanbevolen wordt niet hoger te gaan dan 50.000 records.   

Totalen worden automatisch bijgewerkt wanneer u rijen bijwerkt, verwijdert of maakt in de gegevensset.

## <a name="typing-ahead-of-the-system"></a>Voor het systeem uit typen
In veel zakelijke scenario's is het heel belangrijk om snel gegevens in het systeem in te voeren. Voordat het nieuwe rasterbesturingselement werd geïntroduceerd, konden gebruikers alleen gegevens in de huidige rij wijzigen. Voordat ze een nieuwe rij kunnen maken of naar een andere rij kunnen overschakelen, moeten gebruikers wachten tot de wijzigingen zijn gevalideerd door het systeem. In een poging om de tijd te beperken dat gebruikers wachten op de voltooiing van deze validaties en om de productiviteit van gebruikers te verbeteren, worden deze validaties door het nieuwe raster zodanig aangepast dat ze asynchroon zijn. De gebruiker kan dus naar andere rijen gaan om wijzigingen aan te brengen terwijl de validatie van de vorige rij in behandeling is. 

Ter ondersteuning van dit nieuwe gedrag is er een nieuwe kolom voor de rijstatus rechts van de rijselectiekolom toegevoegd wanneer het raster in de bewerkingsmodus staat. Deze kolom geeft een van de volgende statussen aan:

- **Leeg**: geen statusafbeelding geeft aan dat de rij door het systeem is opgeslagen.
- **Verwerking in behandeling:** deze status geeft aan dat de wijzigingen in de rij nog niet zijn opgeslagen door de server, maar zich in een wachtrij met wijzigingen bevinden die moeten worden verwerkt. Voordat u actie onderneemt buiten het raster, moet u wachten tot alle wijzigingen in behandeling zijn verwerkt. Bovendien wordt de tekst in deze rijen cursief gemaakt om de niet-opgeslagen status van de rijen aan te geven. 
- **Ongeldige status**: deze status geeft aan dat tijdens het verwerken van de rij een waarschuwing of een bericht is gegenereerd en dat het systeem hierdoor mogelijk de wijzigingen in die rij niet kan opslaan. In het oude raster moest u terug naar de rij om het probleem onmiddellijk op te lossen. In het nieuwe raster krijgt u echter een melding dat er een validatieprobleem is aangetroffen, maar u kunt zelf bepalen wanneer u de problemen in de rij wilt oplossen. Wanneer u klaar bent om een probleem op te lossen, kunt u de focus handmatig naar de rij verplaatsen. U kunt ook de actie **Dit probleem oplossen** selecteren. Met deze actie gaat u direct terug naar de rij met het probleem en kunt u de wijzigingen binnen of buiten het raster aanbrengen. De verwerking van volgende rijen in behandeling wordt gestopt totdat deze validatiewaarschuwing is opgelost. 
- **Onderbroken**: deze status geeft aan dat de verwerking door de server is onderbroken omdat de validatie van de rij een pop-updialoogvenster heeft geactiveerd waarvoor invoer van de gebruiker nodig is. Omdat de gebruiker mogelijk gegevens in een andere rij invoert, wordt het pop-upvenster niet onmiddellijk aan die gebruiker weergegeven. In plaats daarvan wordt het weergegeven wanneer de gebruiker de verwerking wil hervatten. Deze status gaat vergezeld van een melding waarin de gebruiker wordt geïnformeerd over de situatie. De melding bevat een actie **Verwerking hervatten** waarmee het pop-updialoogvenster wordt geactiveerd.

Wanneer gebruikers gegevens invoeren voordat de server deze verwerkt, kunnen ze een verslechtering van de gegevensinvoer verwachten, zoals minder zoekacties, validatie op niveau van het besturingselement en de invoer van standaardwaarden. Gebruikers die een vervolgkeuzelijst nodig hebben om een waarde te zoeken, wordt geadviseerd te wachten tot de huidige rij door de server is verwerkt. Validatie en invoer van standaardwaarden op niveau van het besturingselement worden ook uitgevoerd wanneer de server deze rij verwerkt.

### <a name="pasting-from-excel"></a>Plakken vanuit Excel
Gebruikers kunnen altijd gegevens vanuit rasters in apps voor financiële en bedrijfsactiviteiten naar Microsoft Excel exporteren met het mechanisme **Exporteren naar Excel**. Doordat het mogelijk is om gegevens in te voeren vóór de systeemverwerking, ondersteunt het nieuwe raster echter het kopiëren van tabellen vanuit Excel en kunnen deze rechtstreeks in rasters in apps voor financiële en bedrijfsactiviteiten worden geplakt. In de rastercel waaruit de plakbewerking wordt geïnitieerd, wordt bepaald waar de gekopieerde tabel wordt geplakt. De inhoud van het raster wordt overschreven door de inhoud van de gekopieerde tabel, behalve in twee gevallen:

- Als het aantal kolommen in de gekopieerde tabel groter is dan het aantal kolommen dat in het raster overblijft, te beginnen bij de plaklocatie, krijgt de gebruiker een melding dat de extra kolommen zijn genegeerd. 
- Als het aantal rijen in de gekopieerde tabel groter is dan het aantal rijen in het raster, te beginnen bij de plaklocatie, worden de bestaande cellen overschreven door de geplakte inhoud en worden alle extra rijen uit de gekopieerde tabel ingevoegd als nieuwe rijen onder in het raster. 

## <a name="evaluating-math-expressions"></a>Wiskundige expressies evalueren
Ter bevordering van de productiviteit kunnen gebruikers wiskundige formules invoeren in numerieke cellen in een raster. Zij hoeven de berekening niet uit te voeren in een app buiten het systeem. Als u bijvoorbeeld **= 15\*4** invoert en vervolgens op de **tabtoets** drukt om het veld te verlaten, wordt de expressie geëvalueerd en wordt de waarde **60** opgeslagen voor het veld.

Als u wilt dat het systeem een waarde herkent als een expressie, start u de waarde met het gelijkteken (**=**). Zie [Ondersteunde wiskundige symbolen](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols) voor meer informatie over de ondersteunde operators en syntaxis.

## <a name="grouping-tabular-data"></a>Tabelgegevens groeperen
Zakelijke gebruikers moeten vaak ad hoc gegevensanalyse uitvoeren. U kunt dit doen door gegevens te exporteren naar Microsoft Excel en draaitabellen te gebruiken, maar met de functie **Groepering in rasters**, die afhankelijk is van de functie Nieuw rasterbesturingselement, kunnen gebruikers hun tabelgegevens op interessante manieren ordenen in apps voor financiële en bedrijfsactiviteiten. Aangezien deze functie de functie **Totalen** uitbreidt, kunt u met **Groepering** duidelijke inzichten krijgen in de gegevens door subtotalen op te geven op groepsniveau.

Als u deze functie wilt gebruiken, klikt u met de rechtermuisknop op de kolom waarop u wilt groeperen en selecteert u **Groeperen op deze kolom**. Met deze actie sorteert u de gegevens op de geselecteerde kolom, voegt u een nieuwe kolom **Groeperen op** toe aan het begin van het raster en voegt u 'koptekstrijen' toe aan het begin van elke groep. Deze koptekstrijen bevatten de volgende informatie over elke groep:

- Gegevenswaarde voor de groep 
- Kolomnaam (deze informatie is vooral nuttig wanneer u meerdere groeperingsniveaus hebt)
- Aantal gegevensrijen in deze groep
- Subtotalen voor alle kolommen die zijn geconfigureerd voor weergave van totalen

Als [Opgeslagen weergaven](saved-views.md) is ingeschakeld, kunt u groeperingen opslaan als onderdeel van een weergave op pagina's waarmee query's in weergaven kunnen worden opgeslagen. Bijvoorbeeld voor grote weergave-selectors. Zie [Schakelen tussen weergaven](saved-views.md#switching-between-views) voor meer informatie. 

### <a name="multiple-levels-of-grouping"></a>Meerdere groeperingsniveaus
Nadat u gegevens hebt gegroepeerd op een enkele kolom, kunt u de gegevens groeperen op een andere kolom door **Groeperen op deze kolom** te selecteren in de gewenste kolom. Dit proces kan worden herhaald totdat u 5 geneste groeperingsniveaus hebt. Dit is de maximale diepte die wordt ondersteund. Op dit punt kunt u niet meer op extra kolommen groeperen.

U kunt op elk gewenst moment de groepering op een willekeurige kolom verwijderen door met de rechtermuisknop op de kolom te klikken en **Groep opheffen** te selecteren. U kunt de groepering ook uit alle kolommen verwijderen door **Rasteropties** en vervolgens **Alle groeperingen opheffen** te selecteren.

### <a name="sorting-grouped-data"></a>Gegroepeerde gegevens sorteren
Als u gegevens op een of meer kolommen hebt gegroepeerd, kunt u via de bijbehorende kolomkop de sorteerrichting voor een groeperingskolom wijzigen. 

Het gedrag wanneer u sorteert op niet-gegroepeerde kolommen is afhankelijk van uw productversie:

- Als u in versie 10.0.24 en eerder op een niet-gegroepeerde kolom sorteert, wordt de groepering uit alle kolommen verwijderd en worden de gegevens in de geselecteerde kolom gesorteerd. 
- Als u in versie 10.0.25 en later op een niet-gegroepeerde kolom sorteert, blijft de groepering intact en worden de gegevens binnen elke groep op basis van de geselecteerde kolom gesorteerd.

### <a name="expanding-and-collapsing-groups"></a>Groepen uitvouwen en samenvouwen
Bij de eerste groepering van gegevens worden zijn alle groepen uitgevouwen. U kunt samengevatte weergaven van de gegevens maken door afzonderlijke groepen samen te vouwen of u kunt de functie voor het uit- en samenvouwen van groepen gebruiken om te helpen bij het navigeren door de gegevens. Als u een groep wilt uitvouwen of samenvouwen, selecteert u de punthaakknop (>) in de desbetreffende rij van de groepskoptekst. De status voor uitvouwen/samenvouwen van afzonderlijke groepen wordt **niet** opgeslagen bij personalisatie.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Rijen op groepsniveau selecteren en de selectie ervan opheffen
Op dezelfde manier waarop u alle rijen in het raster kunt selecteren (of deselecteren) door het selectievakje boven aan de eerste kolom in het raster in te schakelen, kunt u ook snel alle rijen in een groep selecteren (of deselecteren) door het selectievakje in de desbetreffende rij van de groepskop tekst in te schakelen. Het selectievakje in de rij van de groepskoptekst komt altijd overeen met de huidige selectiestatus van rijen in die groep, ongeacht of alle rijen zijn geselecteerd, er geen rijen zijn geselecteerd of er slechts enkele rijen zijn geselecteerd.

### <a name="hiding-column-names"></a>Kolomnamen verbergen
Wanneer u gegevens groepeert, wordt standaard de kolomnaam weergegeven in de rij van de groepskoptekst. U kunt de kolomnaam in groepskoprijen onderdrukken door **Rasteropties** > **Groepskolomnaam verbergen** te selecteren.

### <a name="grouping-on-date-and-time-columns"></a>Groeperen op datum- en tijdkolommen
Vanaf versie 10.0.24 is voor de velden Datum of Datum/tijd de optie toegevoegd om te groeperen op basis van jaar, maand of dag. De groepswaarde in de bijbehorende koptekstrij komt overeen met de indeling uit dat veld. Bovendien kunt u met de velden Datum/tijd en Tijd groeperen op basis van uur, minuut of seconde. 

## <a name="freezing-columns"></a>Kolommen blokkeren
Sommige kolommen in een raster kunnen dermate belangrijk zijn voor context dat u niet wilt dat ze uit de weergave verdwijnen. In plaats daarvan wilt u mogelijk dat de waarden in die kolommen altijd zichtbaar zijn. De functie **Kolommen blokkeren in raster** biedt deze flexibiliteit voor gebruikers. 

Als u een kolom wilt blokkeren, klikt u met de rechtermuisknop in de koptekst van de kolom en selecteert u vervolgens **Kolom blokkeren**. De eerste keer dat u deze stap voltooit, wordt de geselecteerde kolom de eerste kolom en verdwijnt deze niet meer uit de weergave. Alle volgende kolommen die u blokkeert, worden rechts van de laatste geblokkeerde kolom toegevoegd. U kunt de standaardfunctie Verplaatsen gebruiken om desgewenst geblokkeerde kolommen opnieuw te ordenen. Geblokkeerde kolommen kunnen echter niet worden verplaatst, zodat ze tussen de set met niet-geblokkeerde kolommen worden weergegeven. Zo ook kunnen niet-geblokkeerde kolommen niet worden verplaatst, zodat ze tussen de set met geblokkeerde kolommen worden weergegeven.

Als u de blokkering van een kolom wilt opheffen, klikt u met de rechtermuisknop in de koptekst van de geblokkeerde kolom en selecteert u vervolgens **Blokkering kolom opheffen**. 

De kolommen voor rijselectie en rijstatus in het nieuwe raster zijn altijd als de eerste twee kolommen geblokkeerd. Als deze kolommen in een raster worden opgenomen, zijn deze dus altijd zichtbaar voor gebruikers, ongeacht de horizontale schuifpositie in het raster. De volgorde van deze twee kolommen kan niet worden gewijzigd.

## <a name="autofit-column-width"></a>Kolombreedte automatisch aanpassen
Gebruikers kunnen net als in Excel de grootte van een kolom automatisch wijzigen op basis van de inhoud die op dat moment in die kolom wordt weergegeven. Dubbelklikt hiervoor op de formaatgrepen in de kolom of plaats de focus in de kolomkop en druk op **A** (voor automatisch aanpassen). Deze mogelijkheid is beschikbaar vanaf versie 10.0.23.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hoe kan ik het nieuwe rasterbesturingselement inschakelen in mijn omgeving? 

De functie **Nieuw rasterbesturingselement** is in elke omgeving rechtstreeks beschikbaar in Functiebeheer. Als de functie in Functiebeheer is ingeschakeld, maken alle volgende gebruikerssessies gebruik van de nieuwe rasterbesturing. 

Deze functie is standaard ingeschakeld in versie 10.0.21 en wordt naar verwachting verplicht in oktober 2022.  

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Ontwikkelaar] Uitschakelen dat afzonderlijke pagina's het nieuwe raster gebruiken 
Als uw organisatie een pagina vindt met problemen met het nieuwe raster, is er een API beschikbaar waarmee een afzonderlijk formulier het oude rasterbesturingselement kan gebruiken, terwijl de rest van het systeem nog steeds het nieuwe rasterbesturingselement kan gebruiken. Als u een afzonderlijke pagina voor het nieuwe raster wilt afmelden, voegt u de volgende aanroep `super()` toe aan de methode `run()` van het formulier.

```this.forceLegacyGrid();```

Deze API wordt ondersteund totdat het nieuwe rasterbesturingselement verplicht wordt. Deze wijziging is op dit moment gericht op oktober 2022. Als er problemen optreden waarvoor deze API moet worden gebruikt, meldt u deze bij Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Afdwingen van een pagina om het nieuwe raster te gebruiken nadat eerder het raster is uitgeschakeld
Als u een individuele pagina hebt uitgeschreven voor gebruik van het nieuwe raster, zou u het nieuwe raster later opnieuw kunnen inschakelen nadat de onderliggende problemen zijn opgelost. Hiervoor hoeft u alleen de aanroep van `forceLegacyGrid()` te verwijderen. De wijziging wordt pas doorgevoerd wanneer een van de volgende zaken zich voordoet:

- **Opnieuw implementeren omgeving**: wanneer een omgeving wordt bijgewerkt en opnieuw geïmplementeerd, wordt de tabel waarin de pagina's zijn opgeslagen die zijn uitgeschreven voor het nieuwe raster (FormControlReactGridState) automatisch leeggemaakt.
- **Handmatige leegmaken van de tabel**: voor ontwikkelingsscenario's moet u SQL gebruiken om de tabel FormControlReactGridState leeg te maken en vervolgens de AOS opnieuw opstarten. Met deze combinatie van acties wordt de caching opnieuw ingesteld voor pagina's die zijn uitgeschreven voor het nieuwe raster.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Ontwikkelaar] De mogelijkheid Voor het systeem uit typen niet gebruiken voor afzonderlijke rasters
In sommige scenario's is het niet handig de rasterfunctie *Voor het systeem uit typen* te gebruiken. (Door een bepaalde code die bijvoorbeeld wordt geactiveerd tijdens het valideren van een rij, wordt een gegevensbrononderzoek geactiveerd en kunnen onbewerkte bewerkingen op bestaande rijen beschadigd raken.) Als uw organisatie een dergelijk scenario ontdekt, is er een API beschikbaar waarmee een ontwikkelaar voor een afzonderlijk raster kan kiezen geen asynchrone rijvalidatie te gebruiken en kan terugkeren naar het verouderde gedrag.

Wanneer asynchrone rijvalidatie in een raster is uitgeschakeld, kunnen gebruikers geen nieuwe rij maken of naar een andere bestaande rij in het raster gaan terwijl er validatieproblemen zijn op de huidige rij. Als gevolg van deze actie kunnen tabellen niet vanuit Excel in Finance and Operations-rasters worden geplakt.

Als u voor een afzonderlijk raster geen asynchrone rijvalidatie wilt gebruiken, voegt u de volgende aanroep na `super()` in de methode `run()` van het formulier toe.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Deze aanroep moet slechts in uitzonderlijke gevallen worden aangeroepen en mag niet de norm zijn voor alle rasters.
> - Het is niet aan te raden deze API te kiezen tijdens runtime nadat het formulier is geladen.

## <a name="developer-size-to-available-width-columns"></a>\[Ontwikkelaar\]: kolomformaat aangepast aan beschikbare breedte
Als een ontwikkelaar de eigenschap **WidthMode** instelt op **SizeToAvailable** voor kolommen binnen het nieuwe raster, hebben deze kolommen in eerste instantie dezelfde breedte als ze zouden hebben als de eigenschap is ingesteld op **SizeToContent**. De kolommen worden echter uitgerekt zodat alle extra beschikbare breedte binnen het raster wordt gebruikt. Als de eigenschap is ingesteld op **SizeToAvailable** voor meerdere kolommen, delen al deze kolommen de extra beschikbare breedte binnen het raster. Als een gebruiker echter een van deze kolommen handmatig aanpast, wordt de kolom statisch. De kolom behoudt die breedte en wordt niet meer uitgerekt tot extra beschikbare rasterbreedte.

## <a name="known-issues"></a>Bekende problemen
In deze sectie wordt een lijst met bekende problemen voor het nieuwe rasterbeheer bijgehouden.

### <a name="open-issues"></a>Openstaande problemen
- Nadat de functie **Nieuw rasterbesturingselement** is ingeschakeld, blijven bepaalde pagina's het bestaande rasterbesturingselement gebruiken. Dit gebeurt in de volgende situaties:
 
    - Er bestaat een kaartlijst op de pagina die wordt weergegeven in meerdere kolommen.
    - Er bestaat een gegroepeerde kaartlijst op de pagina.
    - Een rasterkolom met een niet-reagerend uitbreidbaar besturingselement.

    Wanneer een gebruiker voor het eerst een van deze situaties aantreft, wordt een bericht weergegeven over het vernieuwen van de pagina. Nadat dit bericht is weergegeven, blijft de pagina het bestaande raster gebruiken voor alle gebruikers tot de volgende update van de productversie. Een betere afhandeling van deze scenario's zodat het nieuwe raster kan worden gebruikt, wordt overwogen voor een toekomstige update.

- [KB 4582758] Records zijn wazig wanneer u de zoomfactor wijzigt van 100 in een ander percentage
- [KB 4592012] Onverwachte clientfout in IE11 bij het plakken van meerdere regels vanuit Excel

    Microsoft kan dit probleem niet verhelpen


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
