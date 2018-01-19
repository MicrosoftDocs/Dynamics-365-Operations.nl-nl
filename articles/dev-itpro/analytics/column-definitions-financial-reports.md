---
title: "Kolomdefinities in financiële rapporten"
description: Dit artikel bevat informatie over kolomdefinities. Een kolomdefinitie is een rapportonderdeel, of bouwsteen, waarmee de inhoud van kolommen in een financieel rapport wordt gedefinieerd. Net zoals bij rijdefinities kunnen de basisdefinities van kolommen worden gebruikt in meerdere rapporten.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8c877a4ad6d4c29607159da52bf1cedae1476f92
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="column-definitions-in-financial-reports"></a>Kolomdefinities in financiële rapporten

[!include[banner](../includes/banner.md)]


Dit artikel bevat informatie over kolomdefinities. Een kolomdefinitie is een rapportonderdeel, of bouwsteen, waarmee de inhoud van kolommen in een financieel rapport wordt gedefinieerd. Net zoals bij rijdefinities kunnen de basisdefinities van kolommen worden gebruikt in meerdere rapporten.

<a name="create-and-modify-a-column-definition"></a>Een kolomdefinitie maken en wijzigen
-------------------------------------

Een kolomdefinitie kan twee tot 255 kolommen bevatten.

### <a name="create-a-column-definition"></a>Een kolomdefinitie maken

1.  Klik in Report Designer in het navigatievenster op **Kolomdefinities**.
2.  Klik in het menu **Bestand** op **Nieuw** en vervolgens op **Kolomdefinities**.
3.  Voeg de inhoud van de kolomdefinitie toe.

### <a name="open-a-column-definition"></a>Een kolomdefinitie openen

1.  Klik in Report Designer in het navigatievenster op **Kolomdefinities**.
2.  Dubbelklik op een kolomdefinitie om deze te openen.

### <a name="add-a-column-to-a-column-definition"></a>Een kolom aan een kolomdefinitie toevoegen

1.  Klik in Report Designer op **Kolomdefinities** en selecteer vervolgens de kolomdefinitie die u wilt wijzigen.
2.  Selecteer de kolom waarin een nieuwe kolom moeten worden ingevoegd.
3.  Klik in het menu **Bewerken** op **Kolom invoegen**. De nieuwe kolom wordt links weergegeven van de kolom die u hebt geselecteerd.

### <a name="delete-a-column-from-a-column-definition"></a>Een kolom uit een kolomdefinitie verwijderen

1.  Klik in Report Designer op **Kolomdefinities** en open vervolgens de kolomdefinitie die u wilt wijzigen.
2.  Selecteer de kolom die u wilt verwijderen.
3.  Klik in het menu **Bewerken** op **Kolom verwijderen**.

## <a name="contents-of-a-column-definition"></a>Inhoud van een kolomdefinitie
Een kolomdefinitie bevat de volgende informatie:

-   Een kolom van de omschrijvingen voor de rijdefinitie
-   Bedragkolommen die gegevens uit de financiële gegevens, een Microsoft Excel-werkblad of berekeningen weergeven die op andere gegevens in de kolomdefinitie zijn gebaseerd
-   Opmaakkolommen
-   Kenmerkkolommen

Deze informatie wordt weergegeven in de volgende gebieden in de kolomdefinitie:

-   Het koptekstgebied van de kolomdefinitie bevat de koptekst en opmaak die in het rapport wordt weergegeven. Een koptekst kan betrekking hebben op één gegevenskolom, worden verdeeld over meerdere kolommen, of voorwaardelijk op kolommen worden toegepast. De kolomdefinitie kan zoveel kolomkoptekstrijen bevatten als u nodig hebt. **Opmerking:** De kolomkopteksten zijn van toepassing op elke kolom van gegevens in het rapport. Rapportkopteksten zijn van toepassing op het hele rapport. U definieert rapportkopteksten op het tabblad **Kop- en voetteksten** van de rapportdefinitie.
-   De rijen met kolomdetails zijn de rijen onder de koptekstrijen in de kolomdefinitie. De rijen met kolomdetails bepalen de informatie die in het rapport wordt opgenomen. De volgende tabel toont en omschrijft de rijen met kolomdetails.

    | Naam van rij met kolomdetails                                                | Beschrijving                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Kolomtype                                                           | (Vereist) Geef het type gegevens in de kolom op.                                                     |
    | Categorie boekcode/-kenmerk                                          | Geef financiële gegevens op voor kolommen van de typen **FD** en **ATTR**.                       |
    | Behandelde perioden van het boekjaar                                    | Geef financiële gegevens op voor kolommen van het type **FD**.                                     |
    | Formule                                                               | Geef een berekeningsformule op voor kolommen van het type **CALC**.                                        |
    | Aanvullende spaties kolombreedte vóór afdrukbeheer voor overschrijven van kolomindeling | Geef speciale indelingsopties op.                                                                        |
    | Kolombeperkingen                                                   | Beperk gegevens.                                                                                         |
    | Rapportage-eenheid                                                        | Beperk de kolom, zodat deze alleen gegevens voor de opgegeven rapportage-eenheid weergeeft.                      |
    | Valutafilter voor valutaweergave                                      | Maak valuta op.                                                                                       |
    | Dimensiefilter                                                      | Geef een filter op om gegevens naar bepaalde rapportage-eenheden van financiële gegevens te beperken.                           |
    | Kenmerkfilter                                                      | Geef een filter op om de financiële gegevens te beperken.                                                       |
    | Begindatum en einddatum                                                   | Beperk de financiële gegevens tot specifieke datums.                                                         |
    | Reden                                                         | Lijn de omschrijvingstekst die in de rijdefinitie wordt opgegeven links, midden of rechts uit. |

## <a name="column-restrictions-in-a-column-definition"></a>Kolombeperkingen in een kolomdefinitie
Met kolombeperkingen kunt u opgeven hoe een kolomdefinitie gegevens gebruikt of berekent. U kunt een rapportkolom ook beperken tot een specifieke eenheid of voor bepaalde datums. **Opmerking:** Een code voor **Kolombeperking** overschrijft elke tegenstrijdige instelling die in de rijdefinitie wordt toegewezen.

### <a name="column-restrictions-cell"></a>Cel Kolombeperkingen

De cel **Kolombeperkingen** kan codes bevatten die informatie beperken of onderdrukken, zoals rijopmaak, details en bedragen, voor die kolom.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Een kolombeperking toevoegen in een kolomdefinitie

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Kolombeperkingen** zodat de kolom wordt beperkt.
3.  Selecteer in het dialoogvenster **Kolombeperkingen** een of meerdere codes in de lijst en klik op **OK**.

### <a name="column-restriction-codes"></a>Codes voor kolombeperking

De volgende tabel beschrijft de codes voor kolombeperking.

| Code voor kolombeperking | Beschrijving                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SU                      | Onderdruk het onderstrepingsteken voor een kolom waar een opdracht met een onderstrepingsteken (**---**) of een opdracht met een dubbel onderstrepingsteken (**===**) is ingevoerd in de rijdefinitie. U wilt misschien geen bedragen onderstrepen die door een percentageberekening zijn geproduceerd.                                                                        |
| ST                      | Onderdruk totalen, zodat in de kolom alleen details worden weergegeven (bijvoorbeeld een statistische kolom).                                                                                                                                                                                                                                      |
| SD                      | Onderdruk details, zodat alleen de rijen **TOT** en **CAL** (van de rijdefinitie) worden weergegeven in de kolom.                                                                                                                                                                                                                              |
| DR                      | Beperk de bedragen in een **FD**-kolom tot debetbedragen.                                                                                                                                                                                                                                                                              |
| CR                      | Beperk de bedragen in een **FD**-kolom tot crebitbedragen.                                                                                                                                                                                                                                                                             |
| ADJ                     | Beperk de bedragen in de kolom tot bedragen van de periodecorrectie, als deze bedragen beschikbaar zijn.                                                                                                                                                                                                                                        |
| XAD                     | Beperk de bedragen in de kolom, zodat bedragen van de periodecorrectie worden uitgesloten.                                                                                                                                                                                                                                                     |
| GT                      | Beperk de bedragen in de kolom, zodat alleen geboekte transacties worden opgenomen, als deze transacties beschikbaar zijn.                                                                                                                                                                                                                 |
| UPT                     | Beperk de bedragen in de kolom, zodat alleen niet-geboekte transacties worden opgenomen, als deze transacties beschikbaar zijn. **Opmerking:** Niet alle providers van gegevens ondersteunen niet-geboekte transacties. Raadpleeg [handleiding voor gegevensintegratie](http://go.microsoft.com/fwlink/?LinkID=162565) voor uw Microsoft Dynamics ERP-systeem voor meer informatie. |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Een kolom beperken tot een rapportage-eenheid

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Rapportage-eenheid** zodat de kolom wordt beperkt.
3.  Selecteer een structuur in het dialoogvenster **Selectie van rapportage-eenheid** in de lijst **Rapportagestructuur**.
4.  Vouw de lijst van eenheden uit of samen, selecteer een rapportage-eenheid en klik op **OK**.

## <a name="format-column-headers"></a>Kolomkopsteksten opmaken
U kunt de kopteksten die bovenaan de kolommen op een rapport worden weergegeven toevoegen, wijzigen en verwijderen. U kunt ook voorwaardelijke spanningkopteksten configureren op basis van het veld **Periode** uit de kolomdefinities en het veld **Basisperiode** uit de rapportdefinities. De functie van basisperiode helpt u tijd te besparen wanneer u rollende prognoserapporten maakt.

### <a name="create-and-manage-column-headers"></a>Kolomkopteksten maken en beheren

U kunt het dialoogvenster **Kolomkoptekst** gebruiken om kopteksten toe te voegen, te wijzigen en te verwijderen die bovenaan de kolommen op een rapport worden weergegeven. In de volgende tabel worden de velden beschreven in het dialoogvenster **Kolomkop**.

| Veld                 | Beschrijving                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tekst van kolomkop    | Deze tekst verschijnt in de kolomkop. U kunt de tekst rechtstreeks in dit veld typen of op **AutoTekst invoegen** klikken om een optie te selecteren die de kolomkop altijd bijwerkt wanneer het rapport wordt gegenereerd. Als u meerdere Autotekstcodes wilt opnemen, klikt u opnieuw op **AutoTekst invoegen** en klikt u vervolgens op een andere code in de lijst. |
| Opmaakopties        | Pas de opmaak toe op een kolomkop, zoals een vak of onderstreping.                                                                                                                                                                                                                                                           |
| Verspreiden van Verspreiden naar | Definieer de kolom of kolommen waarop de koptekst van toepassing is.                                                                                                                                                                                                                                                            |
| Reden         | Bepaal hoe de kolomkoptekst moet worden uitgelijnd voor de kolom of reeks kolommen die u in de velden **Verspreiden van** en **Verspreiden naar** hebt opgegeven.                                                                                                                                                               |

### <a name="create-a-column-header"></a>Een kolomkop maken

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op een koptekstcel.
3.  Voer in het dialoogvenster **Kolomkop** de kolomkoptekst in. Of klik op **AutoTekst invoegen** en selecteer een optie.
4.  Selecteer in het veld **Opmaakopties** een opmaak voor de koptekst.
5.  Voer in het veld **Verspreiden van** de letter van de kolom in waar de kolomkop opnieuw moet beginnen. Voer in het veld **Verspreiden naar** de letter van de kolom in waar de kolomkop opnieuw moet eindigen.
6.  Selecteer onder **Uitvullen** of de kolomkoptekst links, midden of rechts moet worden uitgevuld.
7.  Klik tot slot op **OK**.

### <a name="add-a-column-header-row"></a>Een kolomkoprij toevoegen

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Selecteer een cel in de koptekstrij.
3.  Klik in het menu **Bewerken** op **Rij invoegen**. De nieuwe rij wordt ingevoegd boven de rij die u in stap 2 hebt geselecteerd. **Opmerking:** Als u vier of meer rijen met rapportkopteksten in een rapport hebt, overlappen de kopteksten elkaar wanneer het rapport wordt geëxporteerd naar een Excel-werkblad. Als u alle kopteksten in het rapport wilt weergeven, verhoogt u de bovenmarge in de rapportdefinitie.

### <a name="delete-a-column-header-row"></a>Een kolomkoprij verwijderen

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Selecteer in de koptekstrij de cel die u wilt verwijderen.
3.  Klik in het menu **Bewerken** op **Rij verwijderen**.

### <a name="create-an-automatically-generated-header"></a>Een automatisch gegenereerde koptekst maken

Report Designer kan kolomkoppen automatisch genereren op basis van AutoTekstcodes. De AutoTekstcodes zok, variabelen die altijd worden bijgewerkt wanneer een rapport wordt gegenereerd. Elke kolomkop kan deze codes bevatten om rapportinformatie op te geven die kan verschillen, zoals datums of periodenummers. Daarom kunt u één kolomdefinitie gebruiken voor meerdere rapportdefinities, perioden en rapportagestructuren. Omdat AutoTekstcodes zich baseren op de kalendergegevens van de rijen met details van de kolomdefinitie, worden deze alleen ondersteund voor **CALC**-, **FD**- en **WKS**-kolommen. De manier waarop een AutoTekstcode in de kolomkopcel wordt weergegeven bepaalt hoe die informatie op het rapport wordt weergegeven. In het dialoogvenster **Kolomkop** worden AutoTekstcodes weergegeven in zowel hoofdletters als kleine letters. Daarom wordt tekst op het rapport in zowel hoofdletters als kleine letters weergegeven. In een standaardkalenderjaar wordt met **@CalMonthLong** bijvoorbeeld maand **7** omgezet in **Juli**. Als de naam van de maand in hoofdletters moet zijn (bijvoorbeeld **JULI**), typt u de AutoTekst-code in hoofdletters in het veld **Kolomkoptekst**. Voer bijvoorbeeld **@CALMONTHLONG** in. U kunt codes en tekst mengen. U voert bijvoorbeeld de volgende koptekst in: **periode @FiscalPeriod-@FiscalYear van @StartDate tot @EndDate**. De rapportkop die wordt gegenereerd lijkt op de volgende tekst: **Periode 1-02 van 01/01/02 tot 31/01/02**. **Opmerking:** de indeling van bepaalde tekst, zoals de lange datumnotatie, is afhankelijk van uw landinstellingen op de Finance and Operations-server. Als u deze instellingen wilt wijzigen, klikt u op de knop **Start**, klikt u op **Configuratiescherm** en vervolgens op **Regio en Taal**. In de volgende tabel vindt u de beschikbare AutoTekst-opties voor kolomkoppen.

| AutoTekst-optie en -code                | Omschrijving                                                                                                                                                                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Maandnaam (@CalMonthLong)              | Druk de naam van de huidige maand af in de kolomkop. Als u de bedragen in het rapport wilt afronden op duizend, miljoen of miljard, of als u de kolombreedte op het rapport instelt op minder dan negen tekens, wordt de naam van de maand tot de eerste drie tekens afgekort. |
| Afgekorte maandnaam (@CalMonthShort) | Druk de afgekorte naam van de maand af voor de geselecteerde boekperiode.                                                                                                                                                                                                                          |
| Periodenummer (@FiscalPeriod)           | Druk de numerieke vorm van de boekperiode af die voor die kolom is geïdentificeerd. Als de kolom meerdere boekperioden bevat, wordt de laatste periode in het bereik afgedrukt.                                                                                                                                   |
| Periodeomschrijving (@FiscalPeriodName)  | Druk de omschrijving van de boekperiode af die in de financiële gegevens is geïdentificeerd.                                                                                                                                                                                                                    |
| Boekjaar (@FiscalYear)               | Druk het fiscaal jaar voor de kolom af in numerieke vorm.                                                                                                                                                                                                                                            |
| Kalenderjaar (@CalYear)                | Druk het kalenderjaar voor de kolom af in numerieke vorm.                                                                                                                                                                                                                                          |
| Begindatum (@StartDate)                 | Druk de begindatum voor de kolom af.                                                                                                                                                                                                                                                             |
| Einddatum (@EndDate)                     | Druk de einddatum voor de kolom af.                                                                                                                                                                                                                                                               |
| Eenheidnaam van structuur (@UnitName)         | Als u een kolom beperkt tot een specifieke eenheid uit de rapportagestructuur, drukt u de naam van de eenheid af in de kolomkop.                                                                                                                                                                                     |
| Omschrijving van eenheid (@UnitDesc)            | Als u een kolom beperkt tot een specifieke eenheid uit de rapportagestructuur, drukt u de omschrijving van de eenheid af in de kolomkop.                                                                                                                                                                              |
| Boekcode (@BookCode)                   | Druk de boekcode af die is opgegeven in de kolom.                                                                                                                                                                                                                                             |
| Lege regel (@Blank)                     | Voeg in de kolomkop een lege regel in.                                                                                                                                                                                                                                                       |

### <a name="create-a-conditional-spanning-header"></a>Een voorwaardelijke spanningkoptekst maken

Voorwaardelijke spanningkopteksten kunnen meerdere kolommen beslaan die op specifieke periodegegevens zijn gebaseerd. Als u bijvoorbeeld een budgetrapport voor het fiscale jaar hebt en de werkelijke budgetten van eerdere maanden en de verwachte budgetten van toekomstige maanden wilt weergeven, kunt u voorwaardelijke spanningkoptekst gebruiken om de rapportkoptekst automatisch bij te werken. Houd rekening met de volgende situaties wanneer u een voorwaardelijk omspannende koptekst maakt:

-   Elke stopvoorwaarde (veld **Verspreiden naar**) die wordt gematcht vóór een startvoorwaarde (veld **Verspreiden van**) wordt genegeerd. Bijvoorbeeld, voor kolom B is de verspreidingsvoorwaarde ingesteld als BASE+1 tot BASE. BASE is in kolom C en BASE+1 is in kolom D. In dit geval wordt de stopvoorwaarde in kolom C genegeerd en begint het afdrukken van de koptekst in kolom D.
-   Als kolomkoppen opgeeft die overlappen, overlappen deze wanneer ze in het rapport worden afgedrukt. Het rapport wordt gegenereerd, maar de volgende waarschuwing wordt weergegeven in het veld **Status van de rapportwachtrij**: "Kolomkoppen die Base gebruiken overlappen met andere kolomkoppen en kunnen overlappende tekst veroorzaken." Bijvoorbeeld de koptekstdefinitie van kolom B is B tot BASE+1 en de koptekstdefinitie van kolom D is BASE+1 tot F. In dit geval worden de kopteksten boven op elkaar afgedrukt en zijn ze onleesbaar. Wanneer BASE wordt gebruikt in een definitie **Verspreiden van/Verspreiden naar**, moet u het rapport dat wordt gegenereerd bekijken om te zien of de kopteksten overlappen.
-   Als u BASE opgeeft in de verspreidingsdefinitie in een kolom Geen afdruk (**NP**), wordt dit genegeerd, ongeacht wat in de kolomdefinitie is gedefinieerd. Dit scenario is voornamelijk hetzelfde als geen kolomkopdefinitie maken.
-   Voor voorwaardelijke afdrukkolommen (**P&lt;B**, **P&gt;=B**) gedragen voorwaardelijke spanningkopteksten zich als een gewone kolomkopdefinitie. Als de voorwaarde bijvoorbeeld onwaar is, start elke volgende kolom die voldoet aan de verspreidingsvoorwaarde met de afdruk van de koptekst.

#### <a name="create-a-conditional-spanning-header"></a>Een voorwaardelijke spanningkoptekst maken

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op een koptekstcel.
3.  Voer in het dialoogvenster **Kolomkop** de kolomkoptekst in. Of klik op **AutoTekst invoegen** en selecteer een optie.
4.   Selecteer in het veld **Opmaakopties** een opmaakstijl voor de koptekst.
5.  Geef een periode op met betrekking tot de basisperiode die wordt opgegeven wanneer het rapport wordt gegenereerd. Voer in de velden **Verspreiden van** en **Verspreiden tot** een van de volgende waarden in: **BASE**, **BASE-X** of **BASE+X**, waarbij X het aantal perioden van de basisperiode is. Als u bijvoorbeeld **BASE** opgeeft in het veld **Verspreiden van**, begint de voorwaardelijke spanningkoptekst van de kolom in de kolom waar de waarde voor **Basisperiode** van de rapportdefinitie gelijk is aan de waarde voor **Periode** van de kolomdefinitie. Het eindigt in de kolom die is opgegeven in het veld **Verspreiden tot**. Als de verspreiding BASE tot M is en de waarde voor **Basisperiode** van de rapportdefinitie **4** is, begint de koptekst in de kolom waarin de periode is ingesteld op **4** en eindigt deze bij kolom M. Kopteksten stoppen en starten alleen in afdrukkolommen.
6.  Selecteer onder **Uitvullen** of de kolomkoptekst links, midden of rechts moet worden uitgevuld.
7.  Klik tot slot op **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Voorbeeld van een voorwaardelijke spanningkoptekst

Phyllis maakt een rapport voor een dynamische halfjaarlijkse prognose. Ze wil dat het woord "Werkelijk" wordt afgedrukt in de kolommen die werkelijke gegevens bevatten, en dat het woord "Budget" wordt afgedrukt in de kolommen die budgetprognoses bevatten. Elke maand dat het rapport wordt uitgevoerd, wordt er één werkelijke kolom meer en één budgetkolom minder afgedrukt. Hoewel Phyllis de kolomdefinitie handmatig kan wijzigen wanneer het rapport wordt gegenereerd om kopteksten te corrigeren, bespaart ze tijd en moeite als ze voorwaardelijke spanningkopteksten maakt die automatisch kopteksten maken in de desbetreffende kolommen telkens wanneer dat het rapport wordt uitgevoerd. Phyllis opent Report Designer, klikt in het navigatievenster op **Kolomdefinitie** en opent de kolomdefinitie voor het rapport. Ze voert de volgende informatie in. De basisperiode in de rapportdefinitie is 4.

|                     | A    | B             | C             | D             | E             | F             | G             | H             | I             | J             | K             | L             | M             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Koptekst 1            |      | Huidige        | Budget        |               |               |               |               |               |               |               |               |               |               |
| Koptekst 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Koptekst 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Kolomtype         | DESC | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Boekcode/kenmerk |      | ACTUAL        | BUDGET2012    | ACTUAL        | BUDGET2012    | ACTUAL        | BUDGET2012    | ACTUAL        | BUDGET2012    | ACTUAL        | BUDGET2012    | ACTUAL        | BUDGET2012    |
| Boekjaar         |      | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          |
| Periode              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Dekkingsperioden     |      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      |
| Kolombreedte        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Afdrukbeheer       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Phyllis dubbelklikt op een kolomkopcel om het dialoogvenster **Kolomkop** te openen, waar ze de volgende informatie invoert.

| Veld              | Waarde                 |
|--------------------|-----------------------|
| Tekst van kolomkop | Werkelijk                |
| AutoTekst invoegen    | Er is niets geselecteerd. |
| Opmaakopties     | Vak                   |
| Reden      | Er is niets geselecteerd. |
| Verspreiden van        | B                     |
| Verspreiden tot          | BASE                  |
| Budgetkoptekst      | BASE+1 tot eindkolom  |

Nadat ze klaar is met het invoeren van informatie, klikt Phyllis op **OK**. Ze dubbelklikt nu op de kolomkopcel in kolom C om het dialoogvenster **Kolomkop** te openen, waar ze de volgende informatie invoert.

| Veld              | Waarde                 |
|--------------------|-----------------------|
| Tekst van kolomkop | Budget                |
| AutoTekst invoegen    | Er is niets geselecteerd. |
| Opmaakopties     | Vak                   |
| Reden      | Er is niets geselecteerd. |
| Verspreiden van        | C                     |
| Verspreiden tot          | BASE+2                |

Elke keer dat dit rapport wordt gegenereerd, wordt het woord "Werkelijk" afgedrukt in de kolommen die werkelijke gegevens bevatten, en wordt het woord "Budget" afgedrukt in de kolommen die budgetprognoses bevatten. Bovendien wordt het aantal kolommen elke maand gecorrigeerd.

## <a name="apply-column-justification"></a>Kolom uitvullen toepassen
De cel **Uitvullen** wordt gebruikt om de opmaak uitvullen toe te passen op een omschrijvingskolom in een rapport. Deze optie is alleen van invloed op de kolomomschrijvingen, niet de werkelijke waarden.

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Uitvullen**.
3.  Selecteer in de lijst een van de volgende waarden:
    -   **Geen** - Uitvullen wordt niet toegepast.
    -   **Links** - De kolomomschrijvingen worden links uitgevuld.
    -   **Midden** - De kolomomschrijvingen worden midden uitgevuld.
    -   **Rechts** De kolomomschrijvingen worden rechts uitgevuld.

## <a name="add-special-formatting-options"></a>Speciale opmaakopties toevoegen
In de kolomdefinitie passen de rijen met opmaakkolomdetails speciale opmaak toe op geselecteerde kolommen. Hoewel sommige van de opties voor **Afdrukbeheer** en **Kolombeperkingen** specifiek zijn voor **FD**-kolommen, zijn de meeste opties van toepassing op alle kolomtypen. De opmaak die in de kolomdefinitie is opgegeven negeert de opmaak die in de rapportdefinitie is opgegeven. De opmaak die in de rijdefinitie is opgegeven negeert echter de opmaak die in de kolomdefinitie is opgegeven. De volgende rijen worden als opmaakrijen beschouwd:

-   Kolombreedte
-   Aanvullende spaties vóór kolom
-   Opmaak/Valuta negeren
-   Afdrukbeheer

### <a name="changing-the-column-width"></a>De kolombreedte wijzigen

De cel **Kolombreedte** geeft het aantal tekens op voor de breedte van deze kolom op het afgedrukte rapport. De kolombreedte is belangrijk voor kolommen die bedragen (kolommen van het type **CALC**, **WKS** of **FD**), beschrijvingen (kolommen van het type **DESC**) of opvullingen (kolommen van het type **FILL**) bevatten. Standaard is de optie **AutoAanpassen** geselecteerd, zodat de breedte van elke kolom automatisch aan de inhoud wordt aangepast.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>De breedte van een kolom op een rapport opgeven

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Voer in de cel **Kolombreedte** het aantal spaties op voor de breedte van de kolom. De maximumbreedte van een kolom is 255 tekens (dit omvat cent, komma's en haakjes). Om Report Designer in staat te stellen om de juiste breedte voor de kolom te selecteren op basis van de celinhoud, dubbelklikt u op de cel **Kolombreedte** en vervolgens op **AutoAanpassen**.

### <a name="add-space-between-columns"></a>Ruimte tussen kolommen toevoegen

De cel **Aanvullende spaties vóór kolom** geeft de breedte op van het scheidingsteken tussen één kolom en ernaast gelegen kolommen in de kolomdefinitie. De instelling **Aanvullende spaties vóór kolom** heeft invloed op alle rijen met kolomdetails voor de kolom, maar niet op de kolomkoprijen. Gebruik deze optie om groepen kolommen te scheiden of een paar spaties vóór de omschrijving toe te voegen, zodat de omschrijvingskolom op het rapport inspringt van de links uitgelijnde titels. Het standaardaantal spaties tussen elke kolom is twee. U kunt deze instelling wijzigen op het tabblad **Instellingen** in de rapportdefinitie.

#### <a name="specify-the-space-between-columns"></a>De ruimte tussen kolommen opgeven

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Voer in de cel **Aanvullende spaties vóór kolom** het aantal spaties op om tussen kolommen in te voegen.

### <a name="specify-a-currency"></a>Een valuta opgeven

De cel **Opmaak/valuta negeren** geeft de opmaak op van de decimale, valuta- en percentagebedragen in de kolom. Deze opmaak negeert elke opmaak die in de rapportdefinitie of standaardinstellingen is opgegeven.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Vervangende opmaak/valuta toewijzen aan een rapportkolom

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op een cel van het type **Vervangende opmaak/valuta** in een bedragkolom.
3.  Selecteer opmaakopties in het dialoogvenster **Opmaak negeren**.

### <a name="add-a-print-control-code"></a>Een afdrukcontrolecode toevoegen

De cel **Afdrukbeheer** kan codes bevatten die de weergave of de afdrukkenmerken van een kolom aanpassen. Er zijn twee typen afdrukcontrolecodes: normale afdrukcontrolecodes en voorwaardelijke afdrukcontrolecodes.

#### <a name="regular-print-control-codes"></a>Normale afdrukcontrolecodes

| Afdrukcontrolecode | Vertaling                                     | Beschrijving                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Niet afdrukken                                     | Neem de bedragen in deze kolom niet op in het rapport dat wordt afgedrukt en in berekeningen. Om een niet af te drukken kolom in een berekening op te nemen, raadpleegt u de kolom rechtstreeks in de berekeningsformule. De niet af te drukken kolom C is bijvoorbeeld opgenomen in de volgende berekening: **B+C+D**. Maar de niet af te drukken kolom C is niet opgenomen in de volgende berekening: **B:D**.                                                                                                                                          |
| XCR                | Teken wijzigen als het normale saldo van de rij credit is | Maak een budget of een vergelijkend rapport waarin elke ongunstige afwijking (zoals een opbrengsttekort of een onkostenoverschrijding) altijd negatief is. Pas deze code toe op een **CALC**-kolom om het teken van het kolombedrag om te keren als het normale saldo van een bepaalde rij credit is (zoals aangegeven met een **C** in de kolom **Normaal Saldo** van de rijdefinitie). **Opmerking:** Let er bij **TOT**-rijen en **CAL**-rijen die meestal een creditsaldo hebben op dat u een **C** invoert in de kolom **Normaal saldo** in de rijdefinitie. |
| X0                 | Kolom onderdrukken indien allemaal nullen of spaties          | Neem een **FD**-kolom niet op in het rapport als alle cellen in die kolom leeg zijn of nullen bevatten.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SR                 | Afronding onderdrukken                               | Voorkom dat de bedragen in deze kolom worden afgerond.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| XR                 | Samentelling onderdrukken                                 | Onderdruk een samentelling. Als het rapport een rapportagestructuur gebruikt, worden de bedragen in deze kolom niet samengeteld in volgende bovenliggende knooppunten.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RP                 | Kolom herhalen op elke pagina                      | Herhaal een kolom op elke pagina van een rapport. U kunt bijvoorbeeld de afdrukcontrolecode **RP** gebruiken om een kolom van het type **RIJ** op te nemen in rijcodes op elke pagina.                                                                                                                                                                                                                                                                                                                                           |
| WT                 |  Tekst verpakken                                      |  Als de tekst in een kolom te lang is voor de ruimte, verpakt u de tekst om alle tekst in de kolom te houden.                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### <a name="conditional-print-control-codes"></a>Voorwaardelijke afdrukcontrolecodes

| Voorwaardelijke afdrukcontrolecode | Omschrijving                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (geen)                         | Wis de voorwaardelijke afdrukselectie.                                                  |
| P&lt;B                         | Geef een opgegeven kolom alleen weer als de periode korter is dan de basisperiode.             |
| P&gt;B                         | Geef een opgegeven kolom alleen weer als de periode langer is dan de basisperiode.             |
| P=B                            | Geef een opgegeven kolom alleen weer als de periode gelijk is aan de basisperiode.              |
| P&lt;=B                        | Geef een opgegeven kolom alleen weer als de periode korter is dan of gelijk is aan de basisperiode. |
| P&gt;=B                        | Geef een opgegeven kolom alleen weer als de periode langer is dan of gelijk is aan de basisperiode. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Afdrukcontrolecodes toevoegen aan een rapportkolom

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Afdrukbeheer**.
3.  Selecteer in het dialoogvenster **Afdrukbeheer** een code in de lijst **Afdrukbeheeropties selecteren**. Om meerdere codes te selecteren, houdt u Ctrl ingedrukt terwijl u de codes selecteert.
4.  Selecteer een optie in het veld **Voorwaardelijke afdrukopties**. De optie **(geen)** is standaard geselecteerd. U kunt slechts één voorwaardelijke afdrukcode tegelijk selecteren.
5.  Klik op **OK**.

> [!TIP]
> U kunt de afdrukcodes ook rechtstreeks in de cel **Afdrukbeheer** invoeren. Scheidt meerdere afdrukbeheercodes met een komma.


## <a name="column-types"></a>Kolomtypen
Het type informatie dat elke kolom op een rapport bevat wordt opgegeven met de waarde in de rij **Kolomtype** in de kolomdefinitie. Elke kolomdefinitie moet ten minste één omschrijvingskolom (**DESC**) en één bedragkolom (**FD**, **WKS** of **CALC**) bevatten. **Opmerking:** De kolomtypecodes zijn niet van toepassing op alle boekhoudsystemen. Als u een type selecteert dat niet geldig is voor uw boekhoudsysteem, is die kolom leeg op het rapport.

### <a name="specify-a-column-type"></a>Een kolomtype opgeven

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik in de juiste kolom op een cel in de rij **Kolomtype**.
3.  Selecteer een kolomtype in de lijst. In de volgende tabel worden de verschillende kolomtypen beschreven.
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Kolomtypecode</th>
    <th>Beschrijving</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>FD</td>
    <td>Geef financiële gegevens of gegevens uit een Excel-werkblad weer wanneer u in de rijdefinitie een kolom met <strong>Koppeling naar financiële dimensies + werkblad</strong> of met <strong>Koppeling naar werkblad</strong> gebruikt. Als u het kolomtype <strong>FD</strong> selecteert, worden automatisch standaardinstellingen toegepast voor de volgende rijen: <ul>
    <li><strong>Boekcode/Kenmerkcategorie:</strong> – ACTUAL</li>
    <li><strong>Boekcode/Kenmerkcategorie:</strong> – ACTUAL</li>
    <li><strong>Boekjaar:</strong> BASIS</li>
    <li><strong>Periode:</strong> BASIS</li>
    <li><strong>Dekkingsperioden:</strong> – PERIODIEK</li>
    <li><strong>Kolombreedte:</strong> 14</li>
    </ul>
U kunt deze standaardinstellingen wijzigen.</td>
    </tr>
    <tr class="even">
    <td>CALC</td>
    <td>Geef het resultaat weer van een eenvoudige of complexe berekening die in de cel <strong>Formule</strong> wordt opgegeven. Raadpleeg <a href="advanced-formatting-options-financial-reporting.md">Geavanceerde opmaakopties in financiële rapportage</a> voor meer informatie.</td>
    </tr>
    <tr class="odd">
    <td>DESC</td>
    <td>Geef de rijomschrijving van de rijdefinitie weer. Hoewel de omschrijvingskolom vaak de eerste kolom in het rapport is, kan deze elke positie hebben.</td>
    </tr>
    <tr class="even">
    <td>ROW</td>
    <td>Geef de afzonderlijke rijcodes weer voor financiële rijen van de kolom <strong>Rijcode</strong> in de rijdefinitie. Raadpleeg <a href="row-definitions-financial-reporting.md">Rijdefinities in financiële rapportage</a> voor meer informatie.</td>
    </tr>
    <tr class="odd">
    <td>ACCT (rekeningcodes)</td>
    <td>Geef de segmentwaarden of dimensiewaarden van financiële gegevens weer die van toepassing zijn op elke rij. Bij rekening- en transactiedetailrapporten wordt de volledig gekwalificeerde rekening afgedrukt (bijvoorbeeld <strong>110140-070-0101</strong>). Als er bereiken zijn opgegeven in de kolom <strong>Koppeling naar financiële dimensies</strong> in een bijbehorende rijdefinitie, wordt het bereik tussen rechte haken geplaatst en behandeld als één waarde (bijvoorbeeld, <strong>[110140:110700]-070-[0101:0200]</strong>). Bij financiële rapporten en rapporten met een hoog abstractieniveau waarin mogelijk meerdere rekeningen worden gecombineerd, wordt de financiële gegevenskoppeling uit de rijdefinitie afgedrukt (bijvoorbeeld <strong>1100:1200</strong>).</td>
    </tr>
    <tr class="even">
    <td>FILL</td>
    <td>Vul de cel met een teken dat u tussen enkele aanhalingstekens plaatst. Als u geen teken invoert, is de kolom leeg. Als u bijvoorbeeld een kolom met een beletselteken (...) wilt invullen, voert u <strong>FILL</strong> <strong>'.'</strong> in.</td>
    </tr>
    <tr class="odd">
    <td>PAGE</td>
    <td>Voeg een verticaal pagina-einde in het rapport in. De kolommen rechts van de <strong>PAGE</strong>-kolom verschijnen op een nieuwe pagina.</td>
    </tr>
    <tr class="even">
    <td>WKS</td>
    <td>Geef gegevens weer die uit een Excel-werkblad worden gehaald. Als u het kolomtype <strong>FD</strong> selecteert, worden automatisch standaardinstellingen toegepast voor de volgende rijen: <ul>
    <li><strong>Boekjaar:</strong> – PERIODIEK</li>
    <li><strong>Periode:</strong> BASIS</li>
    </ul>
U kunt deze standaardinstellingen wijzigen.</td>
    </tr>
    <tr class="odd">
    <td>ATTR</td>
    <td>Als uw boekhoudsysteem kenmerken ondersteunt, een geeft u in de kolom een rekening- of transactiekenmerk weer. Een kenmerk, dat van toepassing moet zijn op één volledige rekening, pakt gegevens van een onderliggende rekening of transactie uit de financiële gegevens uit. Met kenmerken op rekeningniveau worden gegevens van de rekening weergegeven en met kenmerken op transactieniveau worden gegevens weergegeven die betrekking hebben op het tijdstip waarop de transactie is geboekt. Als u het kolomtype <strong>ATTR</strong> selecteert, moet u de <strong>Kenmerkcategorie</strong> opgeven in de detailrij Boekcode/Kenmerkcategorie van de kolomdefinitie.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Kolom Financiële dimensies

De volgende **Kolomdefinitie**-rijdefinities gelden voor kolommen die een kolomtype hebben van het type **FD** (bedragen van financiële dimensies).

#### <a name="book-codeattribute-category-cell"></a>Cel Categorie boekcode/-kenmerk

De cel **Categorie boekcode/-kenmerk** bepaalt de boekcode voor de gegevens in de kolom **FD**. Een kolomdefinitie kan meerdere werkelijke, budget- en statistische kolommen bevatten. Een kolomdefinitie kan ook andere perioden, zoals huidige of jaar-tot-heden, en verschillende bedragen weergeven. De lijst van boekcodes toont de werkelijke, budget- en statistische (niet-financiële) opties die in uw financiële gegevens zijn gedefinieerd.

#### <a name="fiscal-year-cell"></a>Cel Fiscaal jaar

De cel **Fiscaal jaar** identificeert het fiscaal jaar dat de kolom moet bevatten. Het jaar kan betrekking hebben op het basisjaar dat wordt opgegeven wanneer het rapport wordt gegenereerd. De volgende opties zijn beschikbaar.

| Optie  | Beschrijving                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| BASE    | Gebruik het basisjaar dat op het moment van het rapport is opgegeven.                                                                          |
| BASE+\# | Gebruik het jaar dat \# jaren na het basisjaar is. Als u bijvoorbeeld het derde jaar na het basisjaar wilt gebruiken, voert u **BASE+3** in. |
| BASE-\# | Gebruik het jaar \# jaren vóór het basisjaar is. Als u bijvoorbeeld het vorige jaar wilt gebruiken, voert u **BASE-1** in.                 |
| \#      | Voer het huidige fiscale jaar in.                                                                                                |

#### <a name="period-cell"></a>Cel Periode

De cel **Periode** identificeert de boekperioden die de kolom moet bevatten. De periode kan betrekking hebben op de basisperiode die wordt opgegeven wanneer het rapport wordt gegenereerd. De volgende opties zijn beschikbaar.

| Optie          | Omschrijving                                                                                                                                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BASE            | Gebruik de basisperiode.                                                                                                                                                                                                                 |
| BASE+\#         | Gebruik de periode die \# perioden na de basisperiode is. Als u bijvoorbeeld de derde periode na de basisperiode wilt gebruiken, voert u **BASE+3** in.                                                                                               |
| BASE-\#         | Gebruik de periode die \# perioden vóór de basisperiode is. Als u bijvoorbeeld de vorige periode wilt gebruiken, voert u **BASE-1** in.                                                                                                                 |
| BASE-\#:BASE    | Gebruik meerdere perioden, van verschillende perioden vóór de basisperiode tot de basisperiode. Als u bijvoorbeeld de drie vorige perioden en de basisperiode wilt gebruiken, voert u **BASE-3: BASE** in.                                                |
| BASE:BASE+\#    | Gebruik meerdere perioden, van de basisperiode tot verschillende perioden na de basisperiode. Als u bijvoorbeeld de basisperiode en de volgende twee perioden wilt gebruiken, voert u **BASE:BASE+2** in.                                                  |
| BASE-\#:BASE+\# | Gebruik meerdere perioden, van verschillende perioden vóór de basisperiode tot verschillende perioden na de basisperiode. Als u bijvoorbeeld de drie vorige perioden, de basisperiode en de volgende twee perioden wilt gebruiken, voert u **BASE-3:BASE+2** in. |
| 1:BASE          | Gebruik meerdere perioden, van de eerste periode tot de basisperiode.                                                                                                                                                                 |
| \#              | Gebruik altijd een specifiek periodenummer. Wij raden aan dat u deze optie niet gebruikt, omdat deze de flexibiliteit van de kolomdefinitie verlaagt.                                                                                       |
| \#:\#           | Gebruik altijd een specifiek bereik van perioden. Wij raden aan dat u deze optie niet gebruikt, omdat deze de flexibiliteit van de kolomdefinitie verlaagt.                                                                                    |

U kunt verder gaan dan de grenzen van het fiscaal jaar in elke periodespecificatie en u kunt jaren mengen in een bereik van perioden. U geeft bijvoorbeeld de perioden als **BASE-5** op (voor de laatste zes perioden) en voert een rapport uit met een basisperiode van 2. In dit geval bevat het rapport gegevens voor de eerste twee perioden van het opgegeven boekjaar en de laatste vier perioden van het vorige boekjaar.

### <a name="specify-the-periods-for-an-fd-column"></a>De perioden opgeven voor een FD-kolom

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik in een **FD**-kolom op de cel in de rij **Periode** en selecteer een optie in de lijst.
3.  Voer in de formulebalk boven in het navigatievenster of in de cel **Periode** de formule in. Vervang elk hekje (\#) met de gewenste waarde.

#### <a name="periods-covered-cell"></a>Cel Behandelde perioden

De cel **Behandelde perioden** identificeert het bedrag dat de kolom moet weergeven. Dit bedrag is gekoppeld aan de waarde in de cellen **Fiscaal jaar** en **Periode** voor de kolom. De volgende opties zijn beschikbaar.

| Optie      | Beschrijving                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIEK    | Geef de som weer van de activiteit voor de huidige periode of het bereik van perioden. |
| PERIODIEK/BB | Geef het beginsaldo weer voor de huidige periode of het bereik van perioden.   |
| YTD         | Geef de som weer van de activiteit van dit jaar.                               |
| YTD/BB      | Geef het beginsaldo voor het jaar weer.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>De perioden opgeven die onder een FD-kolom vallen

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik in een **FD**-kolom op de cel in de rij **Behandelde perioden** en selecteer een optie in de lijst.

### <a name="attribute-filter-in-a-column-definition"></a>Kenmerkfilter in een kolomdefinitie

Kenmerken zijn financiële gegevenswaarden die een rekening of transactie verder definiëren. De rekeningkenmerken omvatten **Activum**, **Aansprakelijkheid**, **Opbrengst** en **Onkosten**. De transactiekenmerken omvatten **Transactieomschrijving** en **Datum toepassing transactie**. De ondersteuning van kenmerken kan verschillen bij Microsoft Dynamics ERP-systemen. De cel **Kenmerkfilter** beperkt de gegevens in **FD**-kolommen tot specifieke waarden of bereiken voor kenmerkcategorieën. Hoewel deze functie samen met een **ATTR**-kolom kan worden gebruikt, is de **ATTR**-kolom niet vereist. In een **FD**-kolom is er een limiet op de rekeningen of transacties die in het rapport van het kenmerkfilter wordt opgenomen. **Opmerking:** Om te zien welke kenmerken uw ERP-systeem ondersteunt, raadpleegt u de integratiehandleiding voor uw systeem.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Een kenmerkfilter toepassen voor een FD-kolom op een rapport

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Kenmerkfilter** voor een **FD**-kolom.
3.  Dubbelklik in het dialoogvenster **Kenmerkfilter** op een cel in de kolom **Kenmerk** en selecteer vervolgens het filtertype.
4.  Om de resultaten verder te beperken, typt u een bereik in de kolommen **Van** en **Tot**. De cel **Van** moet een waarde bevatten.
5.  Klik tot slot op **OK**.

#### <a name="example-of-an-attribute-filter"></a>Voorbeeld van een kenmerkfilter

Het volgende voorbeeld toont een deel van een kolomomschrijving die een rekeningkenmerk heeft in de rij **Categorie boekcode/-kenmerk**. Het kenmerkfilter voor deze kolom bepaalt het waardebereik dat in het rapport moet worden opgenomen.

|                              | A    | B                    |
|------------------------------|------|----------------------|
| Kolomtype                  | DESC | FD                   |
| Boekcode/Kenmerkcategorie |      | ACTUAL               |
| Boekjaar                  |      | BASE                 |
| Periode                       |      | 1:BASE               |
| Dekkingsperioden              |      | PERIODIEK             |
| ...                          |      |                      |
| Kolombreedte                 | 30   |                      |
| ...                          |      |                      |
| Kenmerkfilter             |      |  Verwijzing=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Dimensiefilter in een kolomdefinitie

Een dimensiefilter wordt gebruikt om de **FD**-kolom te beperken tot specifieke dimensiewaarden. Het filter kan één dimensie, een bereik van dimensies of een groep dimensies bevatten. Het filter kan ook verzamelingen van dimensiewaarden opnemen. Omdat dimensiewaarden kunnen verschillen, hoeft een op ..\financial-dimensions\dimension-gebaseerd systeem niet met een exacte lengte overeen te komen. Het filter wordt toegepast, ongeacht of het rapport een rapportagestructuur bevat. U kunt op elke positie een jokerteken (\* of ?) gebruiken. Wanneer u meerdere rekeningen opgeeft, plaatst u een komma tussen de rekeningen, zoals in het volgende voorbeeld: +Rekening=\[1200\], +Rekening=\[1100\], Afdeling=\[01?\] Als u alle afdelingen voor een bepaalde rekening wilt ontvangen, kunt u de dimensie Afdeling uitsluiten van het dimensiefilter. Bijvoorbeeld, de volgende dimensiefilters worden op dezelfde manier verwerkt:

-   +Rekening=\[1100\],Afdeling
-   +Rekening=\[1100\]

U kunt ook een willekeurige combinatie van alfanumerieke tekens gebruiken voor exacte overeenkomst, en u kunt gedeeltelijke dimensies definiëren. Bijvoorbeeld **Locatie = \[10\*\]** bevat alle waarden van de locatiedimensie die beginnen met 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Een dimensiefilter toepassen voor een kolom op een rapport

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Dimensiefilter** voor een **FD**-kolom.
3.  Voer in het dialoogvenster **Dimensies** de toe te passen filters in.
4.  Klik tot slot op **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Een rapport opmaken met meerdere valuta in een kolomdefinitie

Een rapport met meerdere valuta kan bedragen weergeven in de natuurlijke (lokale) valuta, de functionele (standaard) valuta of de aangiftevaluta. De functionele valuta van een bedrijf wordt gedefinieerd in het Microsoft Dynamics ERP-systeem. Verwar deze ERP-instelling niet met de Landinstellingen van het besturingssysteem, waar u de standaardvalutasymbolen kunt configureren die in rapporten worden gebruikt. De volgende met valuta gerelateerde cellen zijn beschikbaar in de kolomdefinitie:

-   **Valutaweergave** : geef het type valuta op (natuurlijke, functionele of rapportagevaluta) waarin de transacties worden weergegeven. Deze functionaliteit wordt soms ook wel valutaomzetting genoemd. De valutaomzetting is het vermogen om grootboekbedragen te rapporteren in een valuta die misschien niet de functionele valuta van het bedrijf is of de valuta waarin de transactie werd ingevoerd.
-   **Valutafilter** - Geef een valutafilter op. Alleen transacties die in de geselecteerde valuta zijn ingevoerd worden in het rapport weergegeven.

> [!NOTE]
> Als u rapporten wilt maken die meerdere valuta gebruiken, moet u het selectievakje **Alle aangiftevaluta opnemen** inschakelen op het tabblad **Rapport** van de rapportdefinitie. Om de functionele valuta van een bedrijf te definiëren, volgt u deze stappen.

1.  Klik in Report Designer in het menu **Bedrijf** op **Bedrijven**.
2.  Selecteer een bedrijf in het dialoogvenster **Bedrijven** en klik op **Weergeven**.
3.  In het dialoogvenster **Bedrijf weergeven**, onder **Regionale opties**, kunt u de valuta weergeven die voor het geselecteerde bedrijf is opgegeven.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>De valuta in een rapport met meerdere valuta opgeven

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Dubbelklik op de cel **Valutaweergave** in de juiste **FD**-kolom en selecteer vervolgens de optie voor het weergeven van valutagegevens: **Natuurlijke/oorspronkelijke valuta**, **Functionele valuta van bedrijfsgegevens** of de aangiftevaluta.
3.  Dubbelklik op de cel **Valutafilter** in de juiste **FD**-kolom en selecteer vervolgens de juiste valutacode in de lijst. Alleen transacties die in deze valuta zijn ingevoerd worden in het rapport weergegeven.

> [!NOTE]
> De opties die hier worden beschreven, kunnen verschillen, afhankelijk van het ERP-systeem. Raadpleeg uw [Microsoft ERP-systeemdocumentatie](https://www.microsoft.com/en-us/download/details.aspx?id=5916) voor meer informatie.

### <a name="example-for-currency-display-and-currency-filter-cells"></a>Voorbeeld van cellen Valutaweergave en Valutafilter

Phyllis heeft in haar kolomdefinitie de volgende valutaselecties gemaakt:

-   **Valutafilter:** Yen
-   **Valutaweergave:** Functioneel (US dollars)

Door het valutafilter dat Phyllis heeft Geselecteerd, bevat het rapport alleen transacties die in Japanse Yen (JPY) zijn ingevoerd. Door de valutaweergave die ze heeft geselecteerd, bevat het rapport die transacties in de functionele valuta, US dollars (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Combinaties van Valutafilter en Valutaweergave

In de volgende tabel worden de rapportresultaten weergeven die kunnen optreden voor verschillende combinaties van de opties in de cellen **Valutaweergave** en **Valutafilter** door de selecties die Phyllis heeft gemaakt. De functionele valuta is USD.

| Cel Valutaweergave                        | Cel Valutafilter | Rapportresultaat                                                                                                                                                                                    |
|----------------------------------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Natuurlijke/oorspronkelijke valuta                 | **YEN**              | **Y 6000** - Het resultaat toont alleen transacties die in JPY zijn ingevoerd.                                                                                                                        |
| Functionele valuta van bedrijfsgegevens | **YEN**              | **$ 60** - Het resultaat toont alleen transacties die in JPY zijn ingevoerd en toont die transacties in USD. **Opmerking:** De wisselkoers is ongeveer 100 JPY per USD.                    |
| Functionele valuta van bedrijfsgegevens | Leeg                | **$2,310\*\*** – het resultaat toont alle gegevens in de functionele valuta die in de bedrijfsgegevens zijn opgegeven. **Opmerking:** Dit bedrag is de som van alle transacties in functionele valuta. |
| Natuurlijke/oorspronkelijke valuta                 | Leeg                | **$ 2250** - Het resultaat toont alle bedragen in de valuta waarin de transactie is uitgevoerd.                                                                                                 |

### <a name="calculation-column-in-a-column-definition"></a>Berekeningskolom in een kolomdefinitie

Een kolomtype **CALC** in een kolomdefinitie ondersteunt complexe berekeningen in de cel **Formule**, en kan de operatoren **+**, **-**, **\*** en **/** bevatten, evenals **IF/THEN/ELSE**-constructies. Een berekeningskolom kan ook verwijzen naar een andere kolom, zelfs daaropvolgende kolommen. Bovendien kan een berekeningskolom ook het fiscale aar en de periode bevatten om kopteksten voor de kolom te ondersteunen. De berekeningsformule kan maximaal 1024 tekens bevatten. Om de uitkomst van de berekening als een percentage uit te drukken, gebruikt u een speciale opmaakopheffing. **Opmerking:** De resultaten van berekeningsformules nemen de waarden niet op in niet af te drukken kolombereiken. Bijvoorbeeld, **A:D** drukt **0** (nul) af, terwijl **A+B+C** voor niet af te drukken waarden de waarde berekent.

#### <a name="operators-in-calculation-columns"></a>Operatoren in berekeningskolommen

Om kolommen toe te voegen, te verwijderen, te vermenigvuldigen of te verdelen, voert u de kolomletters in de volgorde van berekening in, en gebruikt u vervolgens de gewenste operator om elke kolomletter te scheiden. In de volgende tabel worden de operatoren uitgelegd die u in een berekeningskolom kunt gebruiken.

| Operator | Voorbeeld van berekening | Omschrijving                                                                                                                                                                                                                                    |
|----------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +        | A+C                 | Tel het bedrag in kolom A bij het bedrag in kolom.                                                                                                                                                                                          |
| :        | A:C A:C-D           | Voeg een reeks opeenvolgende kolommen toe. Bijvoorbeeld, de formule **A: C** voegt de totalen van kolommen A tot C toe, en de formule **A:C-D** voegt de totalen van kolommen A tot C toe, en trekt vervolgens het bedrag in kolom D af.                          |
| -        | A-C                 | Trek het bedrag in kolom A af van het bedrag in kolom. **Opmerking:** U kunt ook het minteken (-) gebruiken om het teken in een kolom om te keren. Gebruik bijvoorbeeld **-A+B** om het omgekeerde van het bedrag in kolom A toe te voegen aan het bedrag in kolom B. |
| \*       | A\*C                | Vermenigvuldig het bedrag in kolom A met het bedrag in kolom C.                                                                                                                                                                                     |
| /        | A/C                 | Deel het bedrag in kolom A door het bedrag in kolom C.                                                                                                                                                                                       |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Een berekeningsformule gebruiken in een kolomdefinitie

1.  Open in Report Designer de kolomdefinitie die u wilt wijzigen.
2.  Typ in de juiste **CALC**-kolom een formule in de cel **Formule**.

#### <a name="complex-calculations"></a>Complexe berekeningen

Een complexe berekening kan een combinatie van celverwijzingen, operatoren, waarden en niveaus van geneste haakjes bevatten. Om bijvoorbeeld het gemiddelde van kolommen A en B te berekenen, gebruikt u de berekeningsformule **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Rapportcellen opgeven in een kolomberekening

U kunt naar een specifieke rapportcel verwijzen door een kolomletter en een rijcode in te voeren. **B.100** verwijst bijvoorbeeld naar rijcode 100 in kolom B. U kunt een volledige kolom delen door het bedrag van een specifieke rapportcel in dezelfde kolom. De berekening **B/B.100** betekent bijvoorbeeld dat het bedrag in kolom B moet worden gedeeld door de waarde in rijcode 100 in kolom B. Als de berekening verwijst naar een kolom die afhankelijk is van een andere kolom, wordt de afhankelijke kolom eerst opgelost. Als u een kolom doorverwijst naar een andere kolom die naar de eerste kolom terugverwijst, veroorzaakt u een fout van circulaire verwijzing. **Opmerking:** De berekening is mogelijk onjuist als u de berekeningsprioriteit voor het rapport wijzigt. U kunt de berekeningsprioriteit instellen op het tabblad **Instellingen** van de rapportdefinitie.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Een kolom vermenigvuldigen met of delen door een basisrij

U kunt een kolom maken die alle waarden in een opgegeven kolom weergeeft als een percentage van een basisnummer. Daarom kunt u relaties tussen rijen weergeven, zoals een percentage van een verkopenrij of een percentage van een totale onkostenrij. Als u elke rij in een specifieke kolom wilt vermenigvuldigen met of delen door een basisrij, voert u de kolom in die in de berekening moet worden gebruikt en voert u vervolgens **\*BASEROW** or **/BASEROW** in. Voer bijvoorbeeld **C\*BASEROW** of **C/BASEROW** in. **Opmerking:** wanneer u een basisrijberekening in een kolomdefinitie gebruikt, moet u ervoor zorgen dat elke rijdefinitie die in deze kolomdefinitie wordt gebruikt ten minste één basisrij voor berekeningen bevat.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Het bedrag in een kolom delen door het aantal perioden

U kunt het bedrag in een kolom delen door een opgegeven aantal perioden. De formule **B/Periods** deelt bijvoorbeeld de waarde in kolom B door het aantal perioden in kolom B. Als de berekening meerdere kolommen omvat, geeft u het aantal perioden op die in de berekening moeten worden gebruiken. De formule **(B+C)/Periods)** telt bijvoorbeeld de bedragen in kolom B en kolom op en deelt het resultaat vervolgens door de periodewaarde.

<a name="see-also"></a>Zie ook
--------

[Rijdefinities in financiële rapportage](row-definitions-financial-reporting.md)

[Geavanceerde opmaakopties in financiële rapportage](advanced-formatting-options-financial-reporting.md)




