---
title: Bufferprofiel en -niveaus
description: Dit artikel biedt informatie over bufferprofielen en -niveaus, waarmee de minimum- en maximumvoorraadniveaus worden bepaald die voor elk ontkoppelingspunt moeten worden behouden.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 57ee6206da926d0dbf62f562197538bfcdd41148
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428139"
---
# <a name="buffer-profile-and-levels"></a>Bufferprofiel en -niveaus

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Nadat u de ontkoppelingspunten hebt bepaald (de belangrijkste artikelen die u op voorraad wilt houden), moet u bepalen hoeveel voorraad (buffer) u op elk van deze punten behoudt. Deze taak is de tweede stap van Demand Driven Materials Resource Planning (DDMRP).

## <a name="buffer-levels-and-zones"></a>Bufferniveaus en -zones

In DDMRP wordt elke voorraadbuffer gedefinieerd met behulp van drie waarden: de minimumhoeveelheid, de maximumhoeveelheid en het bestelpunt. Met deze waarden worden drie verschilzones ingesteld die worden aangeduid met de volgende kleurcodes:

- **Rode zone**: het gebied onder de minimumhoeveelheid. De minimumhoeveelheid wordt ook wel 'boven aan rode hoeveelheid' genoemd. Uw planningsstrategie moet zo zijn ontworpen dat voorraadniveaus altijd boven dit punt liggen.
- **Gele zone**: het gebied tussen de minimumhoeveelheid en het bestelpunt. Het bestelpunt wordt ook wel 'boven aan gele hoeveelheid' genoemd. Wanneer dit punt wordt bereikt, moet het systeem opnieuw bestellen.
- **Groene zone**: het gebied tussen het bestelpunt en de maximumhoeveelheid. De maximumhoeveelheid wordt ook wel 'boven aan groene hoeveelheid' genoemd. Dit punt is het maximumniveau waarbij de voorraad wordt aangevuld.

In de volgende afbeelding ziet u de drie gekleurde zones en hoe deze betrekking hebben op de minimumhoeveelheid, de maximumhoeveelheid en het bestelpunt.

![Bufferniveaus en -zones van DDMRP](media/ddmrp-buffer-levels.png "Bufferniveaus en -zones van DDMRP")

## <a name="calculating-the-buffer-zones"></a>De bufferzones berekenen

In dit gedeelte wordt uitgelegd hoe de hoogte van elke bufferzone wordt berekend.

De gele zone wordt doorgaans eerst berekend. Deze zone staat voor de hoeveelheid die u verbruikt vanaf het moment waarop u de order bestelt totdat de order aankomt. Dit is dus het verwachte verbruik tijdens de doorlooptijd van de aanvulling. De berekening vindt plaats met de volgende vergelijking:

- **Gele zone** = *Gemiddeld dagelijks gebruik* × *Ontkoppelde doorlooptijd*

De *ontkoppelde doorlooptijd* is de tijd die nodig is om een artikel te produceren of te ontvangen als de ontkoppelingspunten altijd op voorraad zijn. Dit is meestal veel korter dan de *cumulatieve doorlooptijd* die van oudsher wordt gebruikt in de hoofdplanning. De juiste bufferinstellingen zijn cruciaal om ervoor te zorgen dat ontkoppelingspunten altijd daadwerkelijk op voorraad zijn, maar niet te veel.

De rode zone wordt berekend met de volgende vergelijkingen:

- **Rode basis** = *Gemiddeld dagelijks gebruik* × *Ontkoppelde doorlooptijd* × *Factor doorlooptijd*
- **Rode veiligheid** = *Rode basis* × *Variabiliteitsfactor*
- **Rode zone** = *Rode basis* + *Rode veiligheid*

De groene zone wordt berekend als het maximumresultaat van de volgende drie vergelijkingen:

- *Minimale bestelhoeveelheid*
- *Gemiddeld dagelijks gebruik* × *Ordercyclus*
- *Gemiddeld dagelijks gebruik* × *Ontkoppelde doorlooptijd* × *Factor doorlooptijd*

## <a name="calculating-average-daily-usage"></a>Gemiddeld dagelijks gebruik berekenen

Het systeem gebruikt een van de drie methoden om het bedrag te berekenen dat u per dag verbruikt:

- **Gemiddeld dagelijks gebruik (verleden)**: deze benadering is gebaseerd op het werkelijke verbruik in het verleden.
- **Gemiddeld dagelijks gebruik (toekomstig)**: deze benadering is gebaseerd op het geprognosticeerde toekomstige verbruik.
- **Gemiddeld dagelijks gebruik (gemengd)**: deze benadering is gebaseerd op een gewogen combinatie van verbruik in het verleden en geprognosticeerd verbruik.

### <a name="average-daily-usage-past"></a>Gemiddeld dagelijks gebruik (verleden)

Gemiddeld dagelijks gebruik in het verleden wordt berekend als een gemiddelde door de hoeveelheden die elke dag worden gebruikt voor een bepaald aantal afgelopen dagen op te tellen en het totaal vervolgens te delen door het aantal dagen. In de volgende afbeelding ziet u hoe deze benadering werkt wanneer bij de berekening drie dagen in het verleden worden bekeken.

![Diagram van gemiddeld dagelijks gebruik (verleden).](media/ddmrp-adu-past.png "Diagram van gemiddeld dagelijks gebruik (verleden)")

Als het in de vorige afbeelding vandaag de morgen van 11 juni is, is het gemiddelde dagelijkse gebruik voor de voorgaande drie dagen (8 juni, 9 juni en 10 juni) 21.

- **Gemiddeld dagelijks gebruik (verleden)** = (29 + 11 + 23) ÷ 3 = 21

Voor de berekening van het gemiddelde dagelijks gebruik (verleden) wordt rekening gehouden met de volgende transacties:

- Transacties die de hoeveelheid van het artikel verminderen (in de tabel `inventtrans` waar hoeveelheid minder dan nul is)
- Transacties met de status *In bestelling*, *Besteld en gereserveerd*, *Fysiek gereserveerd*, *Verzameld*, *Ingehouden* of *Verkocht*
- Transacties met een datum binnen de gekozen achterwaartse periode (het gemiddelde dagelijkse gebruik in de afgelopen periode)
- Andere transacties dan magazijnwerk, quarantaine, verkoopoffertes of overzichten (`WHSWork`, `WHSQuarantine`, `SalesQuotation` of `Statement`)
- Andere transacties dan overboekingsjournaal met dezelfde dimensie voor behoefteplan

### <a name="average-daily-usage-forward"></a>Gemiddeld dagelijks gebruik (toekomstig) berekenen

Voor een nieuw product hebt u mogelijk geen gebruiksgegevens uit het verleden. Daarom kunt u in plaats daarvan het verwachte gemiddelde dagelijkse gebruik (toekomstig) gebruiken (bijvoorbeeld op basis van geprognosticeerde vraag). In de volgende afbeelding ziet u hoe deze benadering werkt wanneer bij de berekening drie dagen in de toekomst (inclusief vandaag) worden bekeken.

![Diagram van gemiddeld dagelijks gebruik (toekomstig).](media/ddmrp-adu-forward.png "Diagram van gemiddeld dagelijks gebruik (toekomstig)")

Als het in de vorige afbeelding vandaag de morgen van 11 juni is, is het gemiddelde dagelijkse gebruik voor de volgende drie dagen (11 juni, 12 juni en 13 juni) 21,66.

- **Gemiddeld dagelijks gebruik (toekomstig)** = (18 + 18 + 29) ÷ 3 = 21,66

Voor de berekening van het gemiddelde dagelijks gebruik (toekomstig) wordt rekening gehouden met de volgende transacties:

- Prognosetransacties voor het artikel waarin de prognose is geselecteerd in het hoofdplan
- Transacties met een datum binnen de gekozen voorwaartse periode (het gemiddelde dagelijkse gebruik in de komende periode)

### <a name="average-daily-usage-blended"></a>Gemiddeld dagelijks gebruik (gemengd)

Het gemengde gemiddelde dagelijkse gebruik combineert het gemiddelde gebruik in het verleden en het gemiddelde toekomstige gebruik, zoals in de onderstaande afbeelding wordt weergegeven.

![Diagram van gemiddeld dagelijks gebruik (gemengd).](media/ddmrp-adu-blended.png "Diagram van gemiddeld dagelijks gebruik (gemengd)")

Als het in de vorige afbeelding vandaag de morgen van 11 juni is, is het gemengde gemiddelde dagelijkse gebruik voor de voorgaande en volgende drie dagen (8 juni tot en met 13 juni) 21,33.

- **Gemiddeld dagelijks gebruik gemengd** = (*Gemiddeld dagelijks gebruik in het verleden* + *Gemiddeld dagelijks gebruik in de toekomst*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Bufferberekeningsfactoren

Voor elk artikel kunt u twee factoren definiëren om aan te passen hoe groot de rode en groene zones moeten zijn. Op deze manier kunt u compenseren voor de verwachte doorlooptijd en de vraagvariabiliteit.

![Factoren van doorlooptijd en variabiliteit.](media/ddmrp-zone-factors.png "Factoren van doorlooptijd en variabiliteit")

De eerste factor is de *doorlooptijdfactor*. De waarde is een decimale waarde van 0 tot 1. Des te langer de doorlooptijd is, des te lager de waarde moet zijn. Het Demand Driven Institute beveelt de volgende bereiken aan:

- **Lange doorlooptijd:** 0,20–0,40
- **Gemiddelde doorlooptijd:** 0,41–0,60
- **Korte doorlooptijd:** 0,61–1,00

De tweede factor is de *Variabiliteitsfactor*. De waarde is een decimale waarde van 0 tot 1. Des te hoger de vraagvariabiliteit is, des te lager de waarde moet zijn. Het Demand Driven Institute beveelt de volgende bereiken aan:

- **Lage variabiliteit:** 0,20–0,40
- **Gemiddelde variabiliteit:** 0,41–0,60
- **Hoge variabiliteit:** 0,61–1,00

## <a name="buffer-calculation-examples"></a>Voorbeelden van bufferberekening

Dit voorbeeld gaat verder met het voorbeeld van de kussenproductie dat u hebt gezien in [Voorraadpositionering](ddmrp-inventory-positioning.md). In dat voorbeeld hebt u ontkoppelingspunten geselecteerd waarmee de doorlooptijd van 21 dagen tot vijf dagen werd ingekort, zoals in de onderstaande afbeelding wordt weergegeven.

![Voorbeeld van ontkoppelde doorlooptijd.](media/ddmrp-bom-decoupled-lead-time-example.png "Voorbeeld van ontkoppelde doorlooptijd")

Stel dat het gemiddelde dagelijkse gebruik in dit voorbeeld is berekend als 23 stuks en, zoals in de voorgaande afbeelding is weergegeven, de ontkoppelde doorlooptijd vijf dagen is. Met deze waarden kunt u de gele zone berekenen met behulp van de volgende vergelijking:

- **Gele zone** = *Gemiddeld dagelijks gebruik* × *Ontkoppelde doorlooptijd* = 115

![Voorbeeld van berekening van gele zone.](media/ddmrp-example-calc-yellow.png "Voorbeeld van berekening van gele zone")

De berekening van de rode zone lijkt op de berekening van de gele zone, maar wordt aangevuld voor variabiliteit en doorlooptijd. Stel dat u voor dit voorbeeld een gemiddelde doorlooptijd (factor = 0,50) en een hoge vraagvariabiliteit (factor = 0,8) hebt vastgesteld. Door deze waarden samen met de onderdelen van de vergelijking van de gele zone te gebruiken, kunt u de rode zone berekenen aan de hand van de volgende vergelijkingen:

- **Rode basis** = *Gemiddeld dagelijks gebruik* × *Ontkoppelde doorlooptijd* × *Factor doorlooptijd* = 57,5
- **Rode veiligheid** = *Rode basis* × *Variabiliteitsfactor* = 46
- **Rode zone** = *Rode basis* + *Rode veiligheid* = 103,5

De rode zone wordt afgerond op 104 stuks, omdat stuks in gehele getallen worden geteld.

![Voorbeeld van berekening van rode zone.](media/ddmrp-example-calc-red.png "Voorbeeld van berekening van rode zone")

De berekening van de groene zone bevat ook de onderdelen van de vergelijking van de gele zone, maar maakt een minimumordergrootte, ordercyclus en doorlooptijdfactor mogelijk. Stel dat er voor dit voorbeeld geen ordercyclus bestaat (waardoor u geen tijdsbeperkingen hebt voor hoe vaak u bestelt) en dat de minimumorderhoeveelheid 10 stuks is. De groene zone wordt vervolgens berekend als het maximumresultaat van de volgende drie vergelijkingen:

- *Minimale bestelhoeveelheid* = 10
- *Gemiddeld dagelijks gebruik* × *Ordercyclus* = 0
- *Gemiddeld dagelijks gebruik* × *Ontkoppelde doorlooptijd* × *Factor doorlooptijd* = 57,5

De groene zone wordt afgerond op 58 stuks, omdat stuks in gehele getallen worden geteld.

![Voorbeeld van berekening van groene zone.](media/ddmrp-example-calc-green.png "Voorbeeld van berekening van groene zone")

In de volgende afbeelding worden deze resultaten van de zoneberekening samengevat met de trechterafbeelding die vaak in DDMRP wordt gebruikt.

![Overzicht van zoneberekeningsresultaten.](media/ddmrp-example-calc-summary.png "Overzicht van zoneberekeningsresultaten")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a>Dynamische correcties

Met dynamische correcties kunt u een *vraagcorrectiefactor* toepassen tijdens perioden met een hoge of lage vraag. Met deze factor wordt het gemiddelde dagelijkse gebruik vermenigvuldigd in alle berekeningen voor de geselecteerde periode. De bufferzones worden vervolgens op hun beurt gewijzigd. U gebruikt deze factor meestal nadat u de oorspronkelijke bufferwaarden hebt gegenereerd, zodat u deze in de loop van de tijd en als reactie op wisselende voorwaarden kunt afstemmen. Deze taak is de derde stap van DDMRP.

Er kan bijvoorbeeld meer vraag zijn naar het kussenproduct dat u wilt produceren in augustus wanneer men op vakantie gaat. Daarom zal de verkoop naar verwachting hoger zijn. In dit geval kunt u de waarde van de **Vraagcorrectiefactor** voor het product wijzigen in *1,5* voor alle weken in augustus.

Op deze manier kunt u bufferwaarden in de loop van de tijd berekenen en deze vervolgens aanpassen op basis van niet alleen de informatie die het systeem heeft. In een volledige DDMRP-implementatie berekent u elke dag nieuwe bufferwaarden via een batchtaak en worden de waarden automatisch geaccepteerd. Vervolgens wordt planning uitgevoerd als een batchtaak en worden de geplande orders elke dag gecontroleerd om de buffers aan te vullen.

## <a name="implement-buffers-in-supply-chain-management"></a>Buffers implementeren in Supply Chain Management

In dit gedeelte wordt beschreven hoe u de strategie voor bufferzones in Microsoft Dynamics 365 Supply Chain Management kunt implementeren. Er wordt vanuit gegaan dat u de analyses en berekeningen die in de eerste helft van dit artikel zijn beschreven, al hebt uitgevoerd.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a>Buffers instellen voor een ontkoppelingspuntartikel

Volg deze stappen om bufferwaarden voor een ontkoppelingspunt in te stellen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer een vrijgegeven artikel dat als een ontkoppelingspunt is ingesteld. (Zie [Voorraadpositionering](ddmrp-inventory-positioning.md) voor meer informatie.)
1. Selecteer in het actievenster op het tabblad **Plan** **Artikelbehoefteplanning**.
1. Selecteer op de pagina **Artikelbehoefteplanning** een artikelbehoefteplanningsrecord waarmee een ontkoppelingspunt wordt gemaakt. (In deze record wordt de naam van een behoefteplanningsgroep weergegeven die is ingesteld om ontkoppelingspunten te maken.)
1. Selecteer het tabblad **Algemeen**.
1. Als u wilt dat de bufferwaarden elke dag of elke week opnieuw worden berekend op basis van de instellingen van uw verkoophistorie, prognoses en behoefteplanningsgroep, volgt u deze stappen:

    1. Stel de optie **Bufferwaarden in de tijd** op *Ja* in.
    1. In een berichtvak wordt u geïnformeerd dat uw handmatige bufferinstellingen (**Minimum**, **Bestelpunt** en **Maximum**) opnieuw worden ingesteld als u doorgaat. Selecteer **Ja** de nieuwe instelling te behouden.

    Als u er de voorkeur aan geeft om uw bufferinstellingen slechts één keer te berekenen of in te voeren, volgt u deze stappen:

    1. Stel de optie **Bufferwaarden in de tijd** op *Nee* in.
    1. Stel de velden **Minimum**, **Bestelpunt** en **Maximum** in op de bufferwaarden die u voor het artikel hebt berekend, zoals eerder in dit artikel is beschreven.

1. Stel de volgende velden in om het instellen van de DDMRP-berekeningen voor het artikel te voltooien:

    - **Ordercyclus**: geef het aantal dagen op dat tussen inkooporders voor het artikel moet verstrijken. Stel de waarde in op *0* (nul) als er geen orderbeperkingen zijn. Dit veld is van invloed op de maximale hoeveelheidsbuffer, zoals eerder in dit artikel is besproken.
    - **Gemiddeld dagelijks gebruik**: u kunt desgewenst een geschat gemiddeld dagelijks gebruik voor het artikel invoeren. Dit veld is alleen bedoeld voor informatieve doeleinden. Meestal wordt de waarde automatisch berekend als onderdeel van de bufferberekeningen.
    - **Drempel voor orderpiek**: geef voor het artikel het minimum aantal dagelijkse verkopen op waarmee het wordt gekwalificeerd als een verkooppiek (buitengewoon hoge vraag). Dit veld wordt gebruikt om de bestelhoeveelheid van geplande orders te verhogen in perioden waarin er veel vraag is. Zie [Vraaggestuurde planning](ddmrp-planning.md) voor meer informatie.

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a>Ontkoppelde doorlooptijden berekenen of invoeren

Voor artikelen waarbij u ervoor kiest dat uw [bufferzones automatisch mogen worden berekend](#set-up-buffers), voert u de volgende stappen uit om ontkoppelde doorlooptijden voor een ontkoppelingspuntartikel te berekenen of in te voeren.

1. Open de pagina **Artikelbehoefteplanning** voor uw ontkoppelingspuntartikel. (Zie [Buffers instellen voor een ontkoppelingspuntartikel](#set-up-buffers) voor meer informatie.)
1. Selecteer een artikelbehoefteplanningsrecord waarmee een ontkoppelingspunt wordt gemaakt.
1. Selecteer het tabblad **Bufferwaarden**.
1. Als er geen perioden in het raster worden weergegeven, selecteert u in het actievenster **Perioden toevoegen** op het tabblad **Bufferwaarden**. Het raster wordt gevuld met rijen voor elke dagelijkse of wekelijkse periode, afhankelijk van de vraag of het veld **Periode min., max. en bestelpunt** voor de [behoefteplanningsgroep](ddmrp-inventory-positioning.md) is ingesteld op *Dagelijks* of *Wekelijks*. Er worden voldoende rijen toegevoegd om de time fence te bereiken die is opgegeven voor de behoefteplanningsgroep die aan het artikel is toegewezen.
1. Selecteer de periode waarin u de ontkoppelde doorlooptijd wilt berekenen. (Meestal is deze periode de periode die de datum van vandaag bevat.)
1. Selecteer in het actievenster op het tabblad **Bufferwaarden** de optie **Ontkoppelde doorlooptijd berekenen**.
1. Stel in het dialoogvenster **Ontkoppelde doorlooptijd berekenen** de volgende velden in:

    - **Stuklijst**: selecteer de stuklijst waarop u de berekening wilt uitvoeren.
    - **Datum**: selecteer de datum waarop u de berekening wilt uitvoeren. De set beschikbare stuklijsten wordt gefilterd zodat alleen de stuklijsten worden weergegeven die actief zijn voor de geselecteerde datum.
    - **Hoeveelheid**: voer de hoeveelheid in waarvoor u de berekening wilt uitvoeren. De set beschikbare stuklijsten wordt gefilterd zodat alleen de stuklijsten worden weergegeven die van toepassing zijn op de opgegeven hoeveelheid.

1. Selecteer **OK** om de berekening uit te voeren en het dialoogvenster **Ontkoppelde doorlooptijd berekenen** te sluiten. In de kolom **Ontkoppelde doorlooptijd** voor uw geselecteerde periode wordt nu de berekende waarde getoond.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a>Gemiddeld dagelijks gebruik berekenen of invoeren

Voor artikelen waarbij u ervoor kiest dat uw [bufferzones automatisch mogen worden berekend](#set-up-buffers), voert u de volgende stappen uit om het gemiddeld dagelijks gebruik voor een ontkoppelingspuntartikel te berekenen of in te voeren.

1. Open de pagina **Artikelbehoefteplanning** voor uw ontkoppelingspuntartikel. (Zie [Buffers instellen voor een ontkoppelingspuntartikel](#set-up-buffers) voor meer informatie.)
1. Selecteer een artikelbehoefteplanningsrecord waarmee een ontkoppelingspunt wordt gemaakt.
1. Selecteer het tabblad **Bufferwaarden**.
1. Als er geen perioden in het raster worden weergegeven, selecteert u in het actievenster **Perioden toevoegen** op het tabblad **Bufferwaarden**. Het raster wordt gevuld met rijen voor elke dagelijkse of wekelijkse periode, afhankelijk van de vraag of het veld **Periode min., max. en bestelpunt** voor de [behoefteplanningsgroep](ddmrp-inventory-positioning.md) is ingesteld op *Dagelijks* of *Wekelijks*. Daarnaast worden standaardwaarden voor de velden **Factor doorlooptijd** en **Variabiliteitsfactor** overgenomen van de behoefteplanningsgroep. U kunt deze waarden desgewenst voor elke rij bewerken.
1. Selecteer een periode waarin u gemiddeld dagelijks gebruik wilt berekenen.
1. Selecteer in het actievenster op het tabblad **Bufferwaarden** de optie **Gemiddeld dagelijks gebruik berekenen**. Het systeem probeert gegevens te verzamelen die nodig zijn voor de berekening van gemiddeld dagelijks gebruik, zoals gedefinieerd voor de [behoefteplanningsgroep](ddmrp-inventory-positioning.md).
1. Volg één van deze stappen:

    - Als de vereiste gegevens beschikbaar zijn, worden berekeningsresultaten toegevoegd aan de kolom **Gemiddeld dagelijks gebruik**. In dit geval is er geen actie vereist.
    - Als de vereiste gegevens niet beschikbaar zijn, worden er automatisch geen waarden toegevoegd. In dit geval voert u handmatig geschatte waarden in voor elke rij waarvoor u van plan bent om bufferwaarden te berekenen.

### <a name="calculate-and-apply-buffer-values"></a>Bufferwaarden berekenen en toepassen

Voor artikelen waarbij u ervoor kiest dat uw [bufferzones automatisch mogen worden berekend](#set-up-buffers), kunt u de berekening van bufferwaarden handmatig activeren door de volgende stappen uit te voeren.

1. Voor het relevante ontkoppelingspuntartikel kunt u [de bufferberekening configureren](#set-up-buffers), [ontkoppelde doorlooptijden berekenen of invoeren](#calc-lead-time) en [gemiddeld dagelijks gebruik berekenen of invoeren](#calc-adu) voor alle relevante perioden, zoals eerder in dit artikel is beschreven.
1. Open de pagina **Artikelbehoefteplanning** voor uw ontkoppelingspuntartikel.
1. Selecteer het tabblad **Bufferwaarden**, waarin al een lijst met perioden moet worden weergegeven.
1. Selecteer de periode waarin u bufferwaarden wilt berekenen. (Doorgaans is deze periode de periode die vandaag omvat.) De rij die u selecteert, moet al niet-nulwaarden hebben in de kolommen **Gemiddeld dagelijks gebruik** en **Ontkoppelde doorlooptijd**.
1. Bewerk het veld **Vraagcorrectiefactor** desgewenst voor een of meer rijen. Deze factor wordt toegepast op de waarde voor **Gemiddeld dagelijks gebruik** in alle bufferberekeningen waarin die waarde wordt gebruikt. Met deze factor kunt u de manier aanpassen waarop de vraag fluctueert op basis van datum (bijvoorbeeld voor vakanties of seizoensartikelen).
1. Selecteer in het actievenster op het tabblad **Bufferwaarden** **Hoeveelheden voor min., max. en bestelpunt berekenen**. De kolommen **Berekend minimum**, **Berekend bestelpunt** en **Berekend maximum** worden berekend en ingevuld in het raster op de pagina **Artikelbehoefteplanning**.
1. Wanneer u klaar bent met het controleren van de berekende waarden, moet u deze toepassen. Anders hebben deze geen effect. Wanneer u een berekening op een of meer rijen toepast, worden de waarden uit de velden **Berekend minimum**, **Berekend bestelpunt** en **Berekend maximum** gekopieerd naar respectievelijk de kolommen **Minimum**, **Bestelpunt** en **Maximum**. Selecteer in het actievenster op het tabblad **Bufferwaarden** in de groep **Actie ondernemen** een van de volgende knoppen:

    - **Alle berekeningen accepteren**: alle berekende waarden in het raster toepassen.
    - **Berekeningen voor geselecteerde rijen accepteren**: alleen berekende waarden voor de geselecteerde rijen toepassen.
    - **Alle berekeningen verwijderen**: alle berekende waarden voor minimumhoeveelheden, maximumhoeveelheden en bestelpunten in het raster verwijderen.
    - **Berekeningen verwijderen voor geselecteerde rijen**: alle berekende waarden voor minimumhoeveelheden, maximumhoeveelheden en bestelpunten voor de geselecteerde rijen verwijderen.

### <a name="schedule-automatic-buffer-value-calculations"></a>Automatische bufferwaardeberekeningen plannen

Nadat u de DDMRP-instellingen volledig hebt ingesteld en hebt bevestigd dat ze werken zoals verwacht, wilt u waarschijnlijk een batchtaak instellen om het gemiddelde dagelijkse gebruik en bijbehorende bufferwaarden periodiek opnieuw te berekenen op basis van werkelijke verbruiksgegevens en/of bijgewerkte prognoses. Deze procedure is alleen van toepassing op artikelen waarbij u ervoor kiest om automatisch uw [bufferzones te laten berekenen](#set-up-buffers).

Voer de volgende stappen uit om automatische berekeningen van bufferwaarden te plannen.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> DDMRP \> Bufferwaarden berekenen**.
1. Stel in het dialoogvenster **Bufferwaarden maken** de volgende velden in:

    - **Gemiddeld dagelijks gebruik berekenen**: stel deze optie in op *Ja* om het gemiddelde dagelijkse gebruik van ontkoppelingspuntartikelen opnieuw te berekenen telkens als de taak wordt uitgevoerd. Stel de optie in op *Nee* om deze berekening over te slaan. U moet deze optie meestal instellen op *Ja*.
    - **Ontkoppelde doorlooptijd berekenen**: stel deze optie in op *Ja* om de ontkoppelde doorlooptijden opnieuw te berekenen telkens als de taak wordt uitgevoerd. Stel de optie in op *Nee* om deze berekening over te slaan. U moet deze optie meestal instellen op *Ja*.
    - **Bufferwaarden berekenen**: stel deze optie in op *Ja* als u de bufferwaarden opnieuw wilt berekenen telkens als de taak wordt uitgevoerd. Stel de optie in op *Nee* om deze berekening over te slaan. U moet deze optie meestal instellen op *Ja*.
    - **Berekening accepteren voor min., max. en bestelpunt**: stel deze optie in op *Ja* om de herberekende bufferwaarden automatisch goed te keuren en toe te passen telkens als de taak wordt uitgevoerd. Stel de optie in op *Nee* als u de herberekende waarden niet wilt gebruiken. In dit geval worden de herberekende waarden pas van kracht als iemand ze later op de pagina **Artikelbehoefteplanning** van elk product handmatig toepast. U moet deze optie meestal instellen op *Ja*.
    - **Hoofdplan**: selecteer een hoofdplan met de artikelen die door de berekening worden beïnvloed. De berekening is van toepassing op alle artikelen in het planfilter, die verder worden beperkt door de instellingen van **Filter** in dit dialoogvenster.

1. Als u de set met records wilt beperken waarop deze batchtaak moet worden uitgevoerd, selecteert u op het sneltabblad **Op te nemen records** **Filter** om het dialoogvenster **Query** te openen. Dit dialoogvenster werkt op dezelfde manier als bij andere typen [achtergrondtaken](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Geef op het sneltabblad **Uitvoeren op de achtergrond** op hoe, wanneer en hoe vaak de geselecteerde berekeningen moeten worden uitgevoerd voor de geselecteerde artikelen. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK** om de nieuwe taak aan de batchwachtrij voor uitvoering toe te voegen.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Ontkoppelde doorlooptijden voor alle artikelen controleren en opnieuw berekenen

Voer de volgende stappen uit om alle ontkoppelde doorlooptijden te controleren en opnieuw te berekenen die beschikbaar zijn in uw rechtspersoon (bedrijf).

1. Ga naar **Hoofdplanning \> Hoofdplanning \> DDMRP \> Ontkoppelde doorlooptijd**.
1. Blader op de pagina **Ontkoppelde doorlooptijd** door de lijst en filter de lijst zo nodig om de gewenste informatie te vinden. Als u nog meer informatie voor een artikel wilt weergeven, selecteert u de koppeling ervan in de kolom **Artikelnummer**.
1. Als u de ontkoppelde doorlooptijd voor een artikel opnieuw wilt berekenen, selecteert u het artikel en selecteert u vervolgens **Ontkoppelde doorlooptijd berekenen** in het actievenster. Het dialoogvenster **Ontkoppelde doorlooptijd** wordt weergegeven. Dit dialoogvenster werkt op dezelfde manier als wanneer u [ontkoppelde doorlooptijden berekent](#calc-lead-time) voor hetzelfde artikel op de pagina **Artikelbehoefteplanning**.
