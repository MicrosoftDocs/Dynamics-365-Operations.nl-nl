---
title: Rastermogelijkheden
description: Dit onderwerp beschrijft diverse krachtige functies van het rasterbesturingselement. U moet de nieuwe rasterfunctie inschakelen als u toegang tot deze mogelijkheden wilt hebben.
author: jasongre
ms.date: 10/25/2021
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
ms.openlocfilehash: a21a41399b5884fda9cce214f99851ffa93bbc43
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700132"
---
# <a name="grid-capabilities"></a>Rastermogelijkheden

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Het nieuwe rasterbesturingselement biedt verschillende handige en krachtige functies die u kunt gebruiken om de productiviteit van gebruikers te verbeteren, interessantere weergaven van uw gegevens te maken en inzicht te krijgen in uw gegevens. In dit artikel worden de volgende mogelijkheden besproken: 

-  Totalen worden berekend
-  Voor het systeem uit typen
-  Wiskundige expressies evalueren 
-  Tabelgegevens groeperen (afzonderlijk ingeschakeld met de functie **Groeperen in rasters**)
-  Kolommen blokkeren
-  Kolombreedte automatisch aanpassen
-  Uitrekbare kolommen

## <a name="calculating-totals"></a>Totalen worden berekend
In Finance and Operations-apps kunnen gebruikers totalen weergeven onder aan numerieke kolommen in rasters. Deze totalen worden weergegeven in een voettekstsectie onder in het raster. 

### <a name="showing-the-grid-footer"></a>De rastervoettekst weergeven
Onder aan elk raster in tabelvorm in Finance and Operations-apps bevindt zich een voettekstgebied. In de voettekst kunnen waardevolle gegevens worden weergegeven die betrekking hebben op de gegevens die in het raster worden weergegeven. Hiermee volgen enkele voorbeelden van dergelijke informatie:

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

Als de berekening te lang duurt, kunt u de bewerking annuleren door de knop **Annuleren** te selecteren. Soms is de gegevensset echter te groot voor het berekenen van totalen (een limiet die is ingesteld door uw organisatie) en wordt u in plaats hiervan op de hoogte gesteld om uw gegevens te filteren.

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
Gebruikers konden altijd gegevens vanuit rasters in Finance and Operations-apps naar Microsoft Excel exporteren met de functie **Exporteren naar Excel**. Doordat het mogelijk is om gegevens in te voeren vóór de systeemverwerking, ondersteunt het nieuwe raster echter het kopiëren van tabellen vanuit Excel en kunnen deze rechtstreeks in rasters in Finance and Operations-apps worden geplakt. In de rastercel waaruit de plakbewerking wordt geïnitieerd, wordt bepaald waar de gekopieerde tabel wordt geplakt. De inhoud van het raster wordt overschreven door de inhoud van de gekopieerde tabel, behalve in twee gevallen:

- Als het aantal kolommen in de gekopieerde tabel groter is dan het aantal kolommen dat in het raster overblijft, te beginnen bij de plaklocatie, krijgt de gebruiker een melding dat de extra kolommen zijn genegeerd. 
- Als het aantal rijen in de gekopieerde tabel groter is dan het aantal rijen in het raster, te beginnen bij de plaklocatie, worden de bestaande cellen overschreven door de geplakte inhoud en worden alle extra rijen uit de gekopieerde tabel ingevoegd als nieuwe rijen onder in het raster. 

## <a name="evaluating-math-expressions"></a>Wiskundige expressies evalueren
Ter bevordering van de productiviteit kunnen gebruikers wiskundige formules invoeren in numerieke cellen in een raster. Zij hoeven de berekening niet uit te voeren in een app buiten het systeem. Als u bijvoorbeeld **= 15\*4** invoert en vervolgens op de **tabtoets** drukt om het veld te verlaten, wordt de expressie geëvalueerd en wordt de waarde **60** opgeslagen voor het veld.

Als u wilt dat het systeem een waarde herkent als een expressie, start u de waarde met het gelijkteken (**=**). Zie [Ondersteunde wiskundige symbolen](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols) voor meer informatie over de ondersteunde operators en syntaxis.

## <a name="grouping-tabular-data"></a>Tabelgegevens groeperen
Zakelijke gebruikers moeten vaak ad hoc gegevensanalyse uitvoeren. U kunt dit doen door gegevens te exporteren naar Microsoft Excel en draaitabellen te gebruiken, maar met de functie **Groepering in rasters**, die afhankelijk is van de functie Nieuw rasterbesturingselement, kunnen gebruikers hun tabelgegevens op interessante manieren ordenen in Finance and Operations-apps. Aangezien deze functie de functie **Totalen** uitbreidt, kunt u met **Groepering** duidelijke inzichten krijgen in de gegevens door subtotalen op te geven op groepsniveau.

Als u deze functie wilt gebruiken, klikt u met de rechtermuisknop op de kolom waarop u wilt groeperen en selecteert u **Groeperen op deze kolom**. Met deze actie sorteert u de gegevens op de geselecteerde kolom, voegt u een nieuwe kolom **Groeperen op** toe aan het begin van het raster en voegt u 'koptekstrijen' toe aan het begin van elke groep. Deze koptekstrijen bevatten de volgende informatie over elke groep: 
-  Gegevenswaarde voor de groep 
-  Kolomnaam (deze informatie is vooral nuttig wanneer u meerdere groeperingsniveaus hebt)  
-  Aantal gegevensrijen in deze groep
-  Subtotalen voor alle kolommen die zijn geconfigureerd voor weergave van totalen

Als [Opgeslagen weergaven](saved-views.md) is ingeschakeld, kan deze groepering worden opgeslagen als onderdeel van een weergave voor snelle toegang, de volgende keer dat u de pagina bezoekt.  

### <a name="multiple-levels-of-grouping"></a>Meerdere groeperingsniveaus
Nadat u gegevens hebt gegroepeerd op een enkele kolom, kunt u de gegevens groeperen op een andere kolom door **Groeperen op deze kolom** te selecteren in de gewenste kolom. Dit proces kan worden herhaald totdat u 5 geneste groeperingsniveaus hebt. Dit is de maximale diepte die wordt ondersteund. Op dit punt kunt u niet meer op extra kolommen groeperen.  

U kunt op elk gewenst moment de groepering op een willekeurige kolom verwijderen door met de rechtermuisknop op de kolom te klikken en **Groep opheffen** te selecteren. U kunt de groepering ook uit alle kolommen verwijderen door **Rasteropties** en vervolgens **Alle groeperingen opheffen** te selecteren.   

### <a name="expanding-and-collapsing-groups"></a>Groepen uitvouwen en samenvouwen
Bij de eerste groepering van gegevens worden zijn alle groepen uitgevouwen. U kunt samengevatte weergaven van de gegevens maken door afzonderlijke groepen samen te vouwen of u kunt de functie voor het uit- en samenvouwen van groepen gebruiken om te helpen bij het navigeren door de gegevens. Als u een groep wilt uitvouwen of samenvouwen, selecteert u de punthaakknop (>) in de desbetreffende rij van de groepskoptekst. De status voor uitvouwen/samenvouwen van afzonderlijke groepen wordt **niet** opgeslagen bij personalisatie.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Rijen op groepsniveau selecteren en de selectie ervan opheffen
Op dezelfde manier waarop u alle rijen in het raster kunt selecteren (of deselecteren) door het selectievakje boven aan de eerste kolom in het raster in te schakelen, kunt u ook snel alle rijen in een groep selecteren (of deselecteren) door het selectievakje in de desbetreffende rij van de groepskop tekst in te schakelen. Het selectievakje in de rij van de groepskoptekst komt altijd overeen met de huidige selectiestatus van rijen in die groep, ongeacht of alle rijen zijn geselecteerd, er geen rijen zijn geselecteerd of er slechts enkele rijen zijn geselecteerd.

### <a name="hiding-column-names"></a>Kolomnamen verbergen
Wanneer u gegevens groepeert, wordt standaard de kolomnaam weergegeven in de rij van de groepskoptekst. U kunt de kolomnaam in groepskoprijen onderdrukken door **Rasteropties** > **Groepskolomnaam verbergen** te selecteren.

## <a name="freezing-columns"></a>Kolommen blokkeren
Sommige kolommen in een raster kunnen dermate belangrijk zijn voor context dat u niet wilt dat ze uit de weergave verdwijnen. In plaats daarvan wilt u mogelijk dat de waarden in die kolommen altijd zichtbaar zijn. De functie **Kolommen in raster blokkeren** biedt deze flexibiliteit voor gebruikers. 

Als u een kolom wilt blokkeren, klikt u met de rechtermuisknop in de koptekst van de kolom en selecteert u vervolgens **Kolom blokkeren**. De eerste keer dat u deze stap voltooit, wordt de geselecteerde kolom de eerste kolom en verdwijnt deze niet meer uit de weergave. Alle volgende kolommen die u blokkeert, worden rechts van de laatste geblokkeerde kolom toegevoegd. U kunt de standaardfunctie Verplaatsen gebruiken om desgewenst geblokkeerde kolommen opnieuw te ordenen. Geblokkeerde kolommen kunnen echter niet worden verplaatst, zodat ze tussen de set met niet-geblokkeerde kolommen worden weergegeven. Zo ook kunnen niet-geblokkeerde kolommen niet worden verplaatst, zodat ze tussen de set met geblokkeerde kolommen worden weergegeven.

Als u de blokkering van een kolom wilt opheffen, klikt u met de rechtermuisknop in de koptekst van de geblokkeerde kolom en selecteert u vervolgens **Blokkering kolom opheffen**. 

De kolommen voor rijselectie en rijstatus in het nieuwe raster zijn altijd als de eerste twee kolommen geblokkeerd. Als deze kolommen in een raster worden opgenomen, zijn deze dus altijd zichtbaar voor gebruikers, ongeacht de horizontale schuifpositie in het raster. De volgorde van deze twee kolommen kan niet worden gewijzigd.

## <a name="autofit-column-width"></a>Kolombreedte automatisch aanpassen
Gebruikers kunnen net als in Excel de grootte van een kolom automatisch wijzigen op basis van de inhoud die op dat moment in die kolom wordt weergegeven. Dubbelklikt hiervoor op de formaatgrepen in de kolom of plaats de focus in de kolomkop en druk op **A** (voor automatisch aanpassen). Deze mogelijkheid is beschikbaar vanaf versie 10.0.23.  

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hoe kan ik het nieuwe rasterbesturingselement inschakelen in mijn omgeving? 

De functie **Nieuw rasterbesturingselement** is in elke omgeving rechtstreeks beschikbaar in Functiebeheer. Als de functie in Functiebeheer is ingeschakeld, maken alle volgende gebruikerssessies gebruik van de nieuwe rasterbesturing. 

Deze functie is standaard ingeschakeld in versie 10.0.21 en wordt naar verwachting verplicht vanaf versie 10.0.25. 

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Ontwikkelaar] Uitschakelen dat afzonderlijke pagina's het nieuwe raster gebruiken 
Als uw organisatie een pagina vindt met problemen met het nieuwe raster, is er een API beschikbaar waarmee een afzonderlijk formulier het oude rasterbesturingselement kan gebruiken, terwijl de rest van het systeem nog steeds het nieuwe rasterbesturingselement kan gebruiken. Als u een afzonderlijke pagina voor het nieuwe raster wilt afmelden, voegt u de volgende aanroep `super()` toe aan de methode `run()` van het formulier.

 ```this.forceLegacyGrid();```

Deze API wordt toegepast totdat het nieuwe rasterbeheer verplicht wordt, wat momenteel verwacht wordt voor april 2022. Als er problemen optreden waarvoor deze API moet worden gebruikt, meldt u deze bij Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Afdwingen van een pagina om het nieuwe raster te gebruiken nadat eerder het raster is uitgeschakeld
Als u een individuele pagina hebt uitgeschreven voor gebruik van het nieuwe raster, zou u het nieuwe raster later opnieuw kunnen inschakelen nadat de onderliggende problemen zijn opgelost. Hiervoor hoeft u alleen de aanroep van `forceLegacyGrid()` te verwijderen. De wijziging wordt pas doorgevoerd wanneer een van de volgende zaken zich voordoet:

- **Opnieuw implementeren omgeving**: wanneer een omgeving wordt bijgewerkt en opnieuw geïmplementeerd, wordt de tabel waarin de pagina's zijn opgeslagen die zijn uitgeschreven voor het nieuwe raster (FormControlReactGridState) automatisch leeggemaakt.

- **Handmatige leegmaken van de tabel**: voor ontwikkelingsscenario's moet u SQL gebruiken om de tabel FormControlReactGridState leeg te maken en vervolgens de AOS opnieuw opstarten. Met deze combinatie van acties wordt de caching opnieuw ingesteld voor pagina's die zijn uitgeschreven voor het nieuwe raster.  

## <a name="developer-size-to-available-width-columns"></a>\[Ontwikkelaar\]: kolomformaat aangepast aan beschikbare breedte
Als een ontwikkelaar de eigenschap **WidthMode** instelt op **SizeToAvailable** voor kolommen binnen het nieuwe raster, hebben deze kolommen in eerste instantie dezelfde breedte als ze zouden hebben als de eigenschap is ingesteld op **SizeToContent**. De kolommen worden echter uitgerekt zodat alle extra beschikbare breedte binnen het raster wordt gebruikt. Als de eigenschap is ingesteld op **SizeToAvailable** voor meerdere kolommen, delen al deze kolommen de extra beschikbare breedte binnen het raster. Als een gebruiker echter een van deze kolommen handmatig aanpast, wordt de kolom statisch. De kolom behoudt die breedte en wordt niet meer uitgerekt tot extra beschikbare rasterbreedte.  

## <a name="known-issues"></a>Bekende problemen
In deze sectie wordt een lijst met bekende problemen voor het nieuwe rasterbeheer bijgehouden.  

### <a name="open-issues"></a>Openstaande problemen
-  Nadat de functie **Nieuw rasterbesturingselement** is ingeschakeld, blijven bepaalde pagina's het bestaande rasterbesturingselement gebruiken. Dit gebeurt in de volgende situaties:  
    -  Er bestaat een kaartlijst op de pagina die wordt weergegeven in meerdere kolommen.
    -  Er bestaat een gegroepeerde kaartlijst op de pagina.
    -  Een rasterkolom met een niet-reagerend uitbreidbaar besturingselement.

    Wanneer een gebruiker voor het eerst een van deze situaties aantreft, wordt een bericht weergegeven over het vernieuwen van de pagina. Nadat dit bericht is weergegeven, blijft de pagina het bestaande raster gebruiken voor alle gebruikers tot de volgende update van de productversie. Een betere afhandeling van deze scenario's zodat het nieuwe raster kan worden gebruikt, wordt overwogen voor een toekomstige update.    
    
-  [KB 4582758] Records zijn wazig wanneer u de zoomfactor wijzigt van 100 in een ander percentage
-  [KB 4592012] Onverwachte clientfout in IE11 bij het plakken van meerdere regels vanuit Excel
    -  Microsoft kan dit probleem niet verhelpen

### <a name="fixed-as-part-of-10016"></a>Gecorrigeerd als onderdeel van 10.0.16

-  [KB 4598335] Bij besturingselementen voor tekenreeksen met meerdere regels wordt geen rekening gehouden met de bijbehorende DisplayHeights in lijsten/kaarten 
-  [KB 4591891] Factuurvoorstelregels verdwijnen wanneer de markering van regels wordt opgeheven
-  [KB 4592104] Kan geen records bewerken nadat op "Probleem oplossen" is geklikt en naar een andere rij is verplaatst zonder het validatieprobleem op te lossen
-  [KB 4594449] De knoppen "Nooit" en "Wissen" ontbreken in de datumkiezer 
-  [KB 4594448] Met invoer van tijd wordt anders omgegaan in het nieuwe raster
-  [KB 4600059] Onverwachte clientfout bij het doorlaten van e-mail
-  [KB 4574584] Voorbeeld van onkostenbijlage is niet beschikbaar wanneer over het ontvangstpictogram wordt bewogen

### <a name="fixed-as-part-of-10015"></a>Gecorrigeerd als onderdeel van 10.0.15    

-  (Kwaliteitsupdate) [KB 4594444] Onverwachte clientfout met voorbeeld voor controle van gesegmenteerde invoer
-  [KB 4582723] Weergaveopties worden niet weergegeven verderop in de levenscyclus van het formulier
-  [KB 4591988] Problemen met het toetsenbord om een waarde te selecteren in een opzoekactie van ReferenceGroup
-  [KB 4588958] Test van Regression Suite Automation Tool (RSAT) mislukt met fout: TypeError: kan eigenschapstekst van niet-gedefinieerde tekst niet lezen
-  [KB 4591970] Er is een onverwachte clientfout opgetreden bij het plakken vanuit Excel direct nadat er in het raster was geklikt
-  [KB 4591904] Gegevenswijzigingen worden niet opgeslagen als de gebruiker na het bewerken van een besturingselement meteen op de knop klikt en het zoekvenster van een ander besturingselement opent
-  [KB 4584752] Onverwachte clientfout met pagina van projectfactuurvoorstellen
-  [KB 4584540] Kan het raster niet verlaten nadat één rij in een journaalregel is geplakt
-  [KB 4591908] Tijdens het maken van een nieuwe rij blijft de focus in de kolom waarin men was

### <a name="fixed-as-part-of-10014"></a>Gecorrigeerd als onderdeel van 10.0.14

-  (Kwaliteitsupdate) [KB 4584752] Onverwachte clientfout met pagina van projectfactuurvoorstellen
-  [KB 4583880] Tests van Regression Suite Automation Tool (RSAT) mislukken in OpenLookup-actie met "Kan eigenschap RowIndex van undefined niet lezen"
-  [KB 4583847] Onverwachte clientfout bij het navigeren door zoekacties

### <a name="fixed-as-part-of-10013"></a>Gecorrigeerd als onderdeel van 10.0.13

-  (Kwaliteitsupdate) [KB 4584752] Onverwachte clientfout met pagina van projectfactuurvoorstellen
-  (Kwaliteitsupdate) [KB 4583880] Tests van Regression Suite Automation Tool (RSAT) mislukken in OpenLookup-actie met "Kan eigenschap RowIndex van undefined niet lezen"
-  (Kwaliteitsupdate) [KB 4583847] Onverwachte clientfout bij het navigeren door zoekacties 
-  (Kwaliteitsupdate) [Bug 471777] In een raster kunnen geen velden worden geselecteerd om een mobiele app te bewerken of te maken
-  [KB 4582727] Raster wordt geblokkeerd nadat gebruiker een dialoogvenster ophaalt voor artikelen met meerdere hoeveelheden
-  [Bug 474851] Hyperlinks in verwijzingsgroepbesturingselementen werken niet 
-  [Bug 474848] Verbeterde voorbeelden met rasters worden niet weergegeven
-  [KB 4582726] De eigenschap RotateSign wordt niet gerespecteerd  
-  [Bug 470173] Selectievakjes in inactieve rijen worden in-/uitgeschakeld als op de witruimte in de cel wordt geklikt
-  [Bug 474848] Verbeterde voorbeelden met rasters worden niet weergegeven
-  [Bug 474851] Hyperlinks in verwijzingsgroepbesturingselementen werken niet 
-  [Bug 471777] U kunt in een raster geen velden selecteren om een mobiele app te bewerken of te maken
-  [KB 4569441] Problemen met het weergeven van kaartlijsten met meerdere kolommen, knopinfo op afbeeldingen en weergaveopties in sommige velden
-  [KB 4575279] Niet alle gemarkeerde rijen worden verwijderd in het algemene journaal
-  [KB 4575233] Weergaveopties worden niet hersteld nadat naar een andere rij is verplaatst
-  [Bug 477884] Zoekacties retourneren een onjuiste waarde/record als een nieuw rasterbesturingselement wordt geactiveerd
-  [KB 4571095] Boeking van productontvangst vindt plaats wanneer u per ongeluk op ENTER drukt (juiste verwerking van de standaardactie van een pagina)
-  [KB 4575437] Zoekopdrachten met bewerkbare besturingselementen worden onverwacht gesloten
-  [KB 4569418] Dubbele regel gemaakt in het leverschemaformulier
-  [KB 4575435] Verbeterd voorbeeld blijft soms staan wanneer de muisaanwijzer zich niet bij het veld bevindt
-  [KB 4575434] Opzoeken wordt niet gefilterd wanneer het veld is gewijzigd
-  [KB 4575430] Waarden in wachtwoordvelden worden niet gemaskeerd in het raster
-  [KB 4569438] 'Verwerking is gestopt vanwege een validatieprobleem' wordt weergegeven nadat regels zijn gemarkeerd tijdens het vereffenen van leverancierstransacties
-  [KB 4569434] Het vernieuwen van het formulier rechtspersonen resulteert in minder records
-  [KB 4575297] Focus gaat steeds naar taakregistratievenster bij het bewerken en met Tab doorlopen van een raster
-  [KB 4566773] Correctietransacties die niet als negatief worden weergegeven op boekstuktransactiequery 
-  [KB 4575288] Focus wordt opnieuw ingesteld op de actieve rij bij het selecteren van de rand tussen rijen in een eenvoudige lijst
-  [KB 4575287] Focus keert niet terug naar de eerste kolom wanneer u de pijl-omlaag gebruikt om een nieuwe rij te maken in journalen
-  [KB 4564819] Kan geen regels in een vrije-tekstfactuur verwijderen (omdat de gegevensbron ChangeGroupMode=ImplicitInnerOuter)
-  [KB 4563317] Knopinfo/verbeterde voorbeelden worden niet weergegeven voor afbeeldingen

### <a name="fixed-as-part-of-10012"></a>Gecorrigeerd als onderdeel van 10.0.12

- [KB 4558545] De inhoud van weergegeven items wordt niet bijgewerkt door tabelbesturingselementen.
- [KB 4558570] Artikelen worden nog steeds weergegeven op de pagina nadat de record is verwijderd.
- [KB 4558572] Opmaak die is gekoppeld aan het lijstpaneel **ExtendedStyle** wordt niet toegepast.
- [KB 4558573] Validatiefouten kunnen niet worden hersteld als de vereiste wijziging buiten het raster valt.
- [KB 4558584] Negatieve getallen worden niet correct weergegeven.
- [KB 4560726] Er treedt een onverwachte clientfout op na het schakelen tussen lijsten met behulp van een besturingselement voor lijstweergave.
- [KB 4562141] Rasterindexen zijn uitgeschakeld nadat een nieuwe record is toegevoegd.
- [KB 4562151] De taakrecorderopties **Valideren** en **Kopiëren** zijn niet beschikbaar voor datum- en nummercontroles. 
- [KB 4562153] Selectievakjes voor meerdere selecties zijn niet zichtbaar in lijst-/kaartrasters.
- [KB 4562646] U kunt soms niet buiten het raster klikken wanneer u meerdere rijen in het raster selecteert.
- [KB 4562647] De focus wordt opnieuw ingesteld op het eerste besturingselement in het dialoogvenster **Publiceren** nadat een nieuwe rij is toegevoegd in het raster met beveiligingsrollen.
- [KB 4563310] Het uitgebreide voorbeeld wordt niet gesloten nadat een rij is gewijzigd.
- [KB 4563313] Er treedt een onverwachte clientfout op in Internet Explorer wanneer een waarde wordt geselecteerd in een zoekopdracht.
- [KB 4564557] Zoekopdrachten en vervolgmenu's worden niet geopend in Internet Explorer
- [KB 4563324] Navigatie werkt niet nadat de werkruimte **Personeelsbeheer** is geopend.

### <a name="fixed-as-part-of-10011"></a>Gecorrigeerd als onderdeel van 10.0.11

- [Probleem 432458] Lege of gedupliceerde regels worden aan het begin van bepaalde onderliggende verzamelingen weergegeven.
- [KB 4549711] Regels in een betalingsvoorstel kunnen niet correct worden verwijderd nadat het nieuwe rasterbesturingselement is ingeschakeld.
- [KB 4558374] Records waarvoor een polymorf selectiedialoogvenster vereist is, kunnen niet worden gemaakt.
- [KB 4558375] In het nieuwe raster wordt geen Help-tekst weergegeven voor kolommen.
- [KB 4558376] Rasters van lijstpaneel worden niet op de juiste hoogte weergegeven in Internet Explorer.
- [KB 4558377] Kolommen met een keuzelijst met invoervak met breedte **SizeToAvailable** worden niet op alle pagina's weergegeven.
- [KB 4558378] Met detailanalyse wordt soms de verkeerde record geopend.
- [KB 4558379] Er treedt een fout op wanneer zoekopdrachten worden geopend, als **ReplaceOnLookup**=**Nee** is.
- [KB 4558380] De beschikbare ruimte in het raster wordt niet onmiddellijk opgevuld nadat een gedeelte van de pagina is samengevouwen.
- [KB 4558381] Negatieve getallen worden niet correct gegenereerd/het programma loopt soms vast nadat er validatieproblemen zijn opgetreden.
- [KB 4558382] Er zijn onverwachte clientfouten opgetreden.
- [KB 4558383] Besturingselementen buiten het raster worden niet bijgewerkt nadat de laatste record is verwijderd.
- [KB 4558587] Voor verwijzingsgroepen die keuzelijsten met invoervak bevatten voor vervangingsvelden, worden geen waarden weergegeven.
- [KB 4562143] Velden worden niet bijgewerkt nadat een wijziging in rijen/rasterverwerking is vastgelopen na het verwijderen van de rij.
- [KB 4562645] Er treedt een uitzondering op wanneer een zoekactie wordt geopend terwijl er tests van Regression Suite Automation Tool (RSAT) worden uitgevoerd.

### <a name="fixed-as-part-of-10010"></a>Gecorrigeerd als onderdeel van 10.0.10

- [Probleem 414301] Sommige gegevens uit eerdere regels verdwijnen wanneer er nieuwe regels worden gemaakt.
- [Fout 417044] Er is geen leeg rasterbericht voor rasters in een lijststijl.
- [KB 4539058] Sommige rasters (meestal op sneltabbladen) worden soms niet weergegeven (maar worden wel weergegeven als u uitzoomt).
- [KB 4549734] Actieve rijen worden niet behandeld als gemarkeerd als de kolommarkering verborgen is.
- [KB 4549796] Waarden kunnen niet worden bewerkt in een raster wanneer deze de weergavemodus hebben.
- [KB 4558367] De tekstselectie is inconsistent wanneer rijen worden gewijzigd.
- [KB 4558368] Meervoudige selectie via het toetsenbord is toegestaan in scenario's met één optie.
- [KB 4558369] Statusafbeeldingen verdwijnen in het hiërarchische raster.
- [KB 4558370] Een nieuwe rij schuift niet in de weergave.
- [KB 4558372] Het nieuwe raster loopt vast in de verwerkingsmodus als het aantal geplakte kolommen in de inhoud groter is dan het aantal resterende kolommen in het raster.
- [KB 4562631] Tijdwaarden zijn niet juist ingedeeld.

### <a name="quality-update-for-1009platform-update-33"></a>Kwaliteitsupdate voor 10.0.9/Platform update 33

- [KB 4550367] Tijdwaarden zijn niet juist ingedeeld.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
