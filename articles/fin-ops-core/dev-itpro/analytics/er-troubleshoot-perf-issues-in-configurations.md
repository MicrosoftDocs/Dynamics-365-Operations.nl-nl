---
title: Prestatieproblemen in ER-configuraties oplossen
description: In dit onderwerp wordt uitgelegd hoe u prestatieproblemen in ER-configuraties (Elektronische rapportage) kunt vinden en oplossen.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e727e06c73ff445bf4219ac5a9eee7bec25740d9
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811675"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>Prestatieproblemen in ER-configuraties oplossen

In dit onderwerp wordt uitgelegd hoe u prestatieproblemen in [ER-configuraties](general-electronic-reporting.md) [(Elektronische rapportage)](general-electronic-reporting.md#Configuration) kunt vinden en oplossen.

Prestatieonderzoek bestaat meestal uit verschillende stappen.

1. [Gegevens](#collecting-data) verzamelen.
2. De verzamelde gegevens analyseren.
3. Gebruik op basis van de resultaten van de analyse ER-configuraties om [wijzigingen aan te brengen](#making-changes) of besluit meer gegevens te verzamelen.

## <a name="troubleshooting"></a>Problemen oplossen

### <a name="analyze-execution-time"></a>Uitvoeringstijd analyseren

De uitvoeringstijd kan afhankelijk zijn van onverwachte factoren, zoals andere taken die worden uitgevoerd in dezelfde omgeving en van caching waarin gegevens worden gebruikt wanneer deze voor de eerste keer worden aangeroepen. U moet de uitvoering en meting daarom meerdere keren herhalen.

Soms worden prestatieproblemen niet veroorzaakt door een ER-indelingsconfiguratie die wordt gebruikt voor rapportage. Deze worden echter veroorzaakt door de X++-code die wordt gebruikt om die configuratie van de ER-indeling te openen.

1. Bekijk de uitvoeringstijd van het rapport in het [actiecentrum](#infolog-time) of in het [gebeurtenislogboek](#event-log-time).
2. Vergelijk de uitvoeringstijd van het rapport met de totale uitvoeringstijd in het scenario.
3. Als de uitvoeringstijd van het rapport veel kleiner is dan de totale uitvoeringstijd, moet u de hoeveelheid gegevens bekijken die het rapport verwerkt:

    - Als in het rapport kleine hoeveelheden gegevens worden verwerkt, heeft het probleem mogelijk te maken met de laadtijd van de configuratie.
    - Als het rapport een grote hoeveelheid gegevens verwerkt, kan het probleem X++ voorverwerking omvatten. Gebruik [Trace parser](#analyze-trace-parser-trace) om deze case te analyseren.

    Zie de volgende gedeelten voor andere cases.

4. Voer meerdere tests uit waarbij verschillende hoeveelheden gegevens zijn betrokken om te bepalen hoe de uitvoeringstijd afhankelijk is van de hoeveelheid gegevens.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Trace parser-traces analyseren

Bereid een klein voorbeeld voor of verzamel verschillende traces tijdens willekeurige onderdelen van de rapportgeneratie.

Vervolgens voert u in [Trace parser](#trace-parser) een standaard bottom-up analyse uit en beantwoordt u de volgende vragen:

- Wat zijn de belangrijkste methoden in termen van tijdverbruik?
- Welk deel van de algehele tijd wordt door deze methoden gebruikt?

Beantwoord dezelfde vragen voor query's.

Als u ziet dat methoden het voorvoegsel 'ER' hebben, gaat u verder naar het volgende gedeelte.

Als u ziet dat methoden of query's afkomstig zijn van de toepassingssuite, moet u rekening houden met algemene optimalisaties (bijvoorbeeld indexen maken).

Analyseer het aantal aanroepen. Als het aantal aanzienlijk hoger is dan verwacht, moet u caching overwegen voor de bijbehorende knooppunten van de configuratie.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Databaseaanroepen analyseren

Bereid een voorbeeld voor met een kleine hoeveelheid gegevens, zodat u een [ER-trace](#electronic-reporting-traces) kunt verzamelen.

Open vervolgens de trace in de ontwerper van de ER-modeltoewijzing en kijk onderaan de pagina. Beantwoord de volgende vragen:

- Is er sprake van queryduplicatie? Als dat het geval is, overweeg dan een van de volgende oplossingen:

    - [Gebruik caching](#use-caching) als u denkt dat er meerdere aanroepen in één bovenliggende record zijn.
    - [Gebruik een veld met parameters in de cache](#cached-parameterized) als u denkt dat er aanroepen voor dezelfde record binnen verschillende records zijn.
    - [Gebruik een **JOIN**-gegevensbron](#use-join-datasource) als u een groot aantal verschillende records in een database moet lezen.

- Komt het aantal query's en opgehaalde records overeen met de algehele hoeveelheid gegevens? Als een document bijvoorbeeld 10 regels bevat, geven de statistieken dan aan dat het rapport 10 regels of 1000 regels extraheert? Als u een groot aantal opgehaalde records hebt, overweeg dan een van de volgden oplossingen:

    - [Gebruik de functie **FILTER** in plaats van de functie **WHERE**](#filter) om gegevens aan de Microsoft SQL Server-zijde te verwerken.
    - Gebruik caching om te voorkomen dat dezelfde gegevens worden opgehaald.
    - [Gebruik functies voor verzamelde gegevens](#collected-data) om te voorkomen dat dezelfde gegevens worden opgehaald voor een samenvatting.

### <a name="analyze-perfview-traces"></a>PerfView-traces analyseren

[PerfView](#perfview)is een hulpmiddel voor ervaren ontwikkelaars. Zie [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics) voor gedetailleerdere informatie over de volgende stappen.

1. Verzamel een trace met behulp van threadtijd.
2. Neem alleen stapels op die gebruikmaken van **runUnattended** om alleen de thread te filteren die configuratie-uitvoering heeft. (Voeg **runUnattended** aan het invoervak **IncPats** toe.)
3. Vouw CPU's, netwerk en geblokkeerde tijd samen.
4. Laad [vooraf ingestelde ER-waarden voor PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).
5. Selecteer **ER** \> **Overige vooraf ingestelde waarden**.
6. Bekijk de namen:

    - Waarschijnlijk ziet u de platformcode die de meeste tijd verbruikt.
    - U kunt dubbeltikken (of dubbelklikken) en omhoog gaan via **aangeroepen**.

        Als u klassen vindt met het voorvoegsel "ERExpression" en dit functies zijn die zijn gerelateerd aan formules, kunt u de functienaam raden op basis van de klassenaam, en kunt u de ER-opslagplaats bekijken om de kenmerken weer te geven.

### <a name="fixes"></a>Oplossingen

- Als u ziet dat de meeste CPU-tijd wordt verbruikt door query's, moet u proberen het aantal query's te beperken:

    - [Controleer de ER-trace](#analyze-database-calls) op dubbele query's.
    - Bekijk hoeveel records worden opgehaald en evalueer hoeveel gegevens theoretische moeten worden opgehaald.

- Als u ziet dat de meeste CPU-tijd wordt verbruikt door de functies die worden gebruikt, moet u proberen de plaats te vinden in de configuratie die de meeste resources verbruikt.
- Als u ziet dat de meeste CPU-tijd wordt verbruikt door functies voor gegevensverzameling, overweeg dan om deze te vervangen met *SQL-groep op* aan de modeltoewijzingszijde.

### <a name="collecting-data"></a><a name="collecting-data"></a>Gegevens verzamelen

Afhankelijk van uw omgeving zijn er verschillende manieren om beschikbare gegevens te verzamelen:

- De totale uitvoeringstijd verkrijgen:

    - In het actiecentrum
    - In het gebeurtenislogboek

- Profileer de uitvoering:

    - Met behulp van ER-hulpmiddelen
    - Met behulp van Trace parser
    - Met behulp van PerfView

#### <a name="collecting-data-in-a-production-environment"></a>Gegevens verzamelen in een productieomgeving

Soms kunnen problemen alleen in een productieomgeving worden gereproduceerd. Gegevens kunnen op de volgende manieren worden verzameld:

- Met behulp van [Trace parser](../perf-test/trace-trace-tutorial.md)-traces
- Met behulp van traces van [ER-uitvoering](trace-execution-er-troubleshoot-perf.md)
- Met behulp van de totale uitvoeringstijd

#### <a name="collecting-data-in-a-development-environment"></a>Gegevens verzamelen in een ontwikkelomgeving

Naast de hulpmiddelen die kunnen worden gebruikt in een productieomgeving, zijn er verscheidene hulpmiddelen die u kunt gebruiken in een ontwikkelomgeving:

- Gebeurtenislogboek (Microsoft-Dynamics-ElectronicReporting). Dit logboek kan u de totale uitvoeringstijd verschaffen.
- Algemene .NET-hulpprogramma's, zoals PerfView.

Bovendien biedt een ontwikkelomgeving u meer flexibiliteit om te experimenteren. U kunt bijvoorbeeld delen van rapporten uitschakelen om te zien wat de invloed van de uitvoeringstijd is.

### <a name="tools"></a><a name="tools"></a>Hulpmiddelen

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Uitvoeringstijd in het actiecentrum

ER kan de uitvoeringstijd van de configuratie in het actiecentrum tonen. Deze optie werkt alleen voor een specifieke gebruiker en een specifiek bedrijf, en alleen voor interactieve sessies. Voer de volgende stappen uit om deze functie beschikbaar te maken.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. In het dialoogvenster **Gebruikersparameters** stelt u de optie **Tijd voor genereren van bestanden weergeven** in op **Ja**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Uitvoeringstijd in het gebeurtenislogboek

1. Open Windows Event Viewer.
2. Open onder **Logboeken Toepassingen en Services** **Microsoft-Dynamics-ElectronicReporting/Operational**.
3. Zoek naar **FormatMapingRun**-gebeurtenissen waarin **EventID=2**, omdat deze gebeurtenissen de informatie over verstreken tijd bevatten.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Trace parser-traces 

Omdat ER in X++ is geïmplementeerd, kunt u algemene X++-hulpprogramma's gebruiken om de prestaties te analyseren. Zie [Traceren met Trace parser](../perf-test/trace-trace-tutorial.md) voor meer informatie.

Deze benadering kent enkele beperkingen. Omdat een deel van ER is geïmplementeerd in C#, zijn niet alle details beschikbaar. U kunt de details van het gegevensgebruik echter bekijken. Bovendien kunnen lange rapportuitvoeringen traceopslagbeperkingen overschrijden.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER-traces

Met ER kunnen de eigen traces worden verzameld en ER bevat visualisatie- en analyseprogramma's voor deze traces. Zie [De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md) voor meer informatie.

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Omdat zowel X++ als ER zijn geïmplementeerd boven op het .NET-platform, kunt u algemene .NET-hulpprogramma's gebruiken. U kunt bijvoorbeeld het gratis [PerfView](https://github.com/Microsoft/perfview)-programma gebruiken.

U kunt ook gegevens via de opdrachtregel verzamelen. Met het volgende Windows PowerShell-script verzamelt u bijvoorbeeld de uitvoeringstijd totdat de uitvoering van de indeling op de computer wordt gestopt.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Deze benadering kent enkele beperkingen. U moet beheertoegang tot de computer hebben. Bovendien moet u een ervaren ontwikkelaar zijn, omdat er een heel leerproces aan vast zit.

### <a name="making-changes"></a><a name="making-changes"></a>Wijzigingen aanbrengen

#### <a name="use-caching"></a><a name="use-caching"></a>Caching gebruiken

Hoewel het met caching minder tijd kost om gegevens opnieuw op te halen, kost het geheugen. Gebruik caching in gevallen waarin de hoeveelheid opgehaalde gegevens niet erg groot is. Zie [De modeltoewijzing verbeteren op basis van informatie uit de uitvoeringstrace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace) voor meer informatie en een voorbeeld over het gebruik van caching.

#### <a name="reduce-volume-of-data-fetched"></a><a name="reduce-fetched-data"></a>Het volume beperken van opgehaalde gegevens

U kunt het geheugenverbruik voor caching verminderen door het aantal velden in de records van een toepassingstabel te beperken dat u ophaalt tijdens runtime. In dit geval haalt u alleen de veldwaarden van een toepassingstabel op die u nodig hebt in uw ER-modeltoewijzing. Andere velden in de tabel worden niet opgehaald. Hierdoor wordt het geheugenvolume beperkt dat nodig is om in de cache opgeslagen records op te halen. Zie [De prestaties van ER-oplossingen verbeteren door het aantal tabelvelden te beperken dat wordt opgehaald tijdens runtime](er-reduce-fetched-fields-number.md).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Een berekend veld met parameters in de cache gebruiken

Waarden moeten soms herhaaldelijk worden opgezocht. Voorbeelden zijn rekeningnamen en rekeningnummers. Om tijd te besparen kunt u een berekend veld maken dat parameters op het bovenste niveau heeft, en het veld vervolgens aan de cache toevoegen.

We raden u aan deze methode alleen te gebruiken als de grootte van de gegevens in de cache klein is. Zie [De prestaties van ER-oplossingen verbeteren door gegevensbronnen voor een berekend veld met parameters toe te voegen](er-calculated-field-ds-performance.md) voor meer informatie.

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>Een JOIN-gegevensbron gebruiken

Met een **JOIN**-gegevensbron kunnen verschillende verbonden records met één query worden opgehaald. Er hoeft geen afzonderlijke query te worden gebruikt om elke verbonden record op te halen. Als u bijvoorbeeld 1000 regels hebt en u haalt artikelgegevens op voor elke regel per relatie, hebt u 1001 query's (= 1000 + 1). Als u een **JOIN**-gegevensbron gebruikt, gebruikt u slechts één query om dezelfde gegevens op te halen. Zie [JOIN-gegevensbronnen gebruiken in ER-modeltoewijzingen om gegevens uit meerdere toepassingstabellen op te halen](er-join-data-sources.md) voor meer informatie.

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>De functie FILTER gebruiken in plaats van de functie WHERE

Met de functie **[FILTER](er-functions-list-filter.md)** worden voorwaarden uitgevoerd in SQL Server, terwijl met de functie **WHERE** alle gegevens uit de lijst met één record per keer worden opgehaald en de voorwaarde voor elke record wordt toegepast. U wilt bijvoorbeeld één record van 1000 records selecteren. Als u **WHERE** gebruikt, worden alle 1000 records opgehaald. Als u echter **FILTER** gebruikt, wordt precies één record opgehaald. Met **FILTER** kunnen ook indexen worden gebruikt voor de database.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Functies voor verzamelde gegevens of een samengevoegde gegevensbron gebruiken

Als uw configuratie het onderdeel *groeperen op* heeft waarmee eerder opgehaalde gegevens per rapport worden samengevat, worden alle gegevens opnieuw opgehaald met het onderdeel. Met behulp van functies voor verzamelde gegevens stelt u ER in staat gegevens samen te voegen tijdens de eerste keer dat de gegevens worden opgehaald. Zie [ER-indeling configureren voor tellen en totaliseren](tasks/er-format-counting-summing-2.md) voor meer informatie.

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Delen van de configuratie in X++ herschrijven

ER ondersteunt aanroepmethoden van tabellen en klassen, waaronder extensies. Overweeg delen van de modeltoewijzing in X++ beter te herschrijven om de prestaties te verbeteren.

ER kan gegevens verbruiken uit de volgende bronnen:

- Klassen (**object**- en **klasse**-gegevensbronnen)
- Tabellen (**tabel**- en **tabelrecords**-gegevensbronnen)

De [ER-API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) biedt ook een manier om vooraf berekende gegevens van de aanroepcode te verzenden. De toepassingssuite bevat vele voorbeelden van deze aanpak.
