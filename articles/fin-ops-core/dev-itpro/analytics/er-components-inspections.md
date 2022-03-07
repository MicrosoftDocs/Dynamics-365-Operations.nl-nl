---
title: Het geconfigureerde ER-onderdeel inspecteren om runtimeproblemen te voorkomen
description: In dit onderwerp wordt uitgelegd hoe u de geconfigureerde onderdelen voor elektronische rapportage (ER) kunt inspecteren om runtimeproblemen te voorkomen.
author: NickSelin
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c63ffc6316d21d36bb2aad57194b8aa1c477607e
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8074786"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Het geconfigureerde ER-onderdeel inspecteren om runtimeproblemen te voorkomen

[!include[banner](../includes/banner.md)]

Elke geconfigureerde [indeling](er-overview-components.md#format-components-for-outgoing-electronic-documents) voor [elektronische rapportage](general-electronic-reporting.md) en elke onderdeel voor [modeltoewijzing](er-overview-components.md#model-mapping-component) kan tijdens het ontwerp worden [gevalideerd](er-fillable-excel.md#validate-an-er-format). Tijdens deze validatie wordt een consistentie controle uitgevoerd om runtimeproblemen te voorkomen die zich kunnen voordoen, zoals uitvoeringsfouten en prestatievermindering. Voor elk gevonden probleem wordt het pad van een problematisch element verstrekt. Voor sommige problemen is een automatische oplossing beschikbaar.

De validatie wordt standaard automatisch toegepast in de volgende gevallen voor een ER-configuratie die de eerder genoemde ER-onderdelen bevat:

- U [importeert](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) een nieuwe [versie](general-electronic-reporting.md#component-versioning) van een nieuwe ER-configuratie in uw exemplaar van Microsoft Dynamics 365 Finance.
- U wijzigt de [status](general-electronic-reporting.md#component-versioning) van de bewerkbare ER-configuratie van **Concept** in **Voltooid**.
- U kunt een bewerkbare ER configuratie [opnieuw baseren](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) door een nieuwe basisversie toe te passen.

U kunt deze validatie expliciet uitvoeren. Selecteer een van de volgende drie opties en volg de stappen die worden beschreven:

- Optie 1:

    1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
    2. Selecteer in de configuratiestructuur in het linkerdeelvenster de gewenste configuratie die het toewijzingsonderdeel van de ER-indeling of het ER-model bevat.
    3. Selecteer op het sneltabblad **Versies** de gewenste versie van de geselecteerde ER-configuratie.
    4. Selecteer in het actievenster de optie **Valideren**.

- Optie 2 voor een ER-indeling:

    1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
    2. Selecteer in de configuratiestructuur in het linkerdeelvenster de gewenste configuratie die het ER-indelingsonderdeel bevat.
    3. Selecteer op het sneltabblad **Versies** de gewenste versie van de geselecteerde ER-configuratie.
    4. Selecteer **Ontwerper** in het actievenster.
    5. Selecteer op de pagina **Indelingsontwerper** in het actievenster de optie **Valideren**.

- Optie 3, voor een ER-modeltoewijzing:

    1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
    2. Selecteer in de configuratiestructuur in het linkerdeelvenster de gewenste configuratie die het toewijzingsonderdeel van het ER-model bevat.
    3. Selecteer op het sneltabblad **Versies** de gewenste versie van de geselecteerde ER-configuratie.
    4. Selecteer **Ontwerper** in het actievenster.
    5. Selecteer **Ontwerper** op de pagina **Model aan gegevensbrontoewijzing** in het actievenster.
    6. Selecteer op de pagina **Ontwerper modeltoewijzing** in het actievenster de optie **Valideren**.

Voer de volgende stappen uit om de validatie over te slaan wanneer de configuratie wordt geïmporteerd.

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel de optie **De configuratie valideren na importeren** in op **Nee**.

Voer de volgende stappen uit om de validatie over te slaan wanneer u de status van de versie wijzigt of de basisindeling opnieuw selecteert.

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel de optie **Validatie overslaan bij statuswijziging en rebase van configuratie** in op **Ja**.

In ER worden de volgende categorieën inspecties gebruikt om consistentiecontroles te groeperen:

- **Uitvoerbaarheid** – Inspecties waarmee kritieke problemen worden opgespoord die zich kunnen voordoen tijdens runtime. Bij deze problemen is meestal sprake van een **foutniveau**. 
- **Prestaties** – Inspecties waarmee problemen worden opgespoord die een inefficiënte uitvoering van de geconfigureerde ER-onderdelen kunnen veroorzaken. Bij deze problemen is meestal sprake van een **waarschuwingsniveau**.
- **Gegevensintegriteit** – Inspecties waarmee problemen worden gedetecteerd die leiden tot gegevensverlies of runtimeproblemen. Bij deze problemen is meestal sprake van een **waarschuwingsniveau**.

## <a name="list-of-inspections"></a>Lijst met inspecties

De volgende tabel biedt een overzicht van de inspecties die ER biedt. Als u meer wilt weten over deze inspecties, gebruikt u de koppelingen in de eerste kolom om naar de desbetreffende secties van dit onderwerp te gaan. In deze secties worden de typen onderdelen beschreven waarvoor ER inspecties biedt en wordt aangegeven hoe u ER-onderdelen opnieuw kunt configureren om problemen te helpen voorkomen.

<table>
<thead>
<tr>
<th>Naam</th>
<th>Categorie</th>
<th>Niveau</th>
<th>Bericht</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Type conversie</a></td>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>
<p>Kan expressie van het type &lt;type&gt; niet converteren naar een veld van het type &lt;type&gt;.</p>
<p><b>Runtimefout:</b> uitzondering voor type</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Type compatibiliteit</a></td>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>
<p>De geconfigureerde expressie kan niet worden gebruikt als de binding van het huidige indelingselement aan een gegevensbron, omdat deze expressie een waarde retourneert van het gegevenstype &lt;type&gt; dat buiten het bereik valt van gegevenstypen die worden ondersteund door huidige indelingselement van het type &lt;type&gt;.</p>
<p><b>Runtimefout:</b> uitzondering van type</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Ontbrekend configuratie-element</a></td>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>
<p>Pad &lt;pad&gt; niet gevonden.</p>
<p><b>Runtimefout:</b> element van het configuratiepad &lt;pad&gt; niet gevonden</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Uitvoerbaarheid van een expressie met FILTER-functie</a></td>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>
<p>Op de lijstexpressie van de functie FILTER kan geen query worden uitgevoerd.</p>
<p><b>Runtimefout:</b> filteren wordt niet ondersteund. Valideer de configuratie voor meer informatie hierover.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>Uitvoerbaarheid van een GROUPBY-gegevensbron</a></td>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>Pad &lt;pad&gt; biedt geen ondersteuning voor het uitvoeren van query's.</td>
</tr>
<tr>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>
<p>Functie Groeperen op kan niet worden uitgevoerd met query.</p>
<p><b>Runtimefout:</b> functie Groeperen op kan niet worden uitgevoerd met query.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>Uitvoerbaarheid van een JOIN-gegevensbron</a></td>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>
<p>Kan geen join uitvoeren voor een lijst &lt;pad&gt; die geen filter is in query.</p>
<p><b>Runtimefout:</b> aan functie gekoppelde gegevensbron moet een filterexpressie zijn. Berekend veld is niet juist aangeroepen.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Voorkeur voor FILTER-functie boven WHERE-functie</a></td>
<td>Prestaties</td>
<td>Waarschuwing</td>
<td>Het gebruik van de FILTER functie voor de expressie heeft de voorkeur boven WHERE vanuit het oogpunt van prestaties. Selecteer Corrigeren om deze automatisch te vervangen.</td>
</tr>
<tr>
<td><a href='#i8'>Voorkeur voor ALLITEMSQUERY-functie boven ALLITEMS-functie</a></td>
<td>Prestaties</td>
<td>Waarschuwing</td>
<td>Het gebruik van de ALLITEMSQUERY-functie voor de expressie heeft de voorkeur boven ALLITEMS vanuit het oogpunt van prestaties. Selecteer Corrigeren om deze automatisch te vervangen.</td>
</tr>
<tr>
<td><a href='#i9'>Controle op lege lijstcases</a></td>
<td>Uitvoerbaarheid</td>
<td>Waarschuwing</td>
<td>
<p>De lijst &lt;pad&gt; bevat geen controle op lege lijstcases. Dit kan leiden tot een fout tijdens runtime. Voeg een controle toe op lege lijstcases.</p>
<p><b>Runtimefout:</b> lijst is leeg in &lt;pad&gt;</p>
<p><b><a href='#i9a'>Mogelijk probleem</a>:</b> de regel wordt eenmaal gevuld terwijl een gegevensbron waaruit deze wordt gevuld meerdere records bevat</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Uitvoerbaarheid van een expressie met FILTER-functie (caching)</a></td>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>
<p>FILTER functie kan niet worden toegepast op het geselecteerde type gegevensbron. Een gegevensbron van het type Tabelrecords is alleen van toepassing als deze niet in de cache is opgeslagen en geen handmatig toegevoegde geneste gegevensbronnen heeft.</p>
<p><b>Runtimefout:</b> filteren wordt niet ondersteund. Valideer de configuratie voor meer informatie hierover.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Binding ontbreekt</a></td>
<td>Uitvoerbaarheid</td>
<td>Waarschuwing</td>
<td>
<p>Het pad &lt;pad&gt; heeft geen binding met een gegevensbron bij gebruik van toewijzing van model.</p>
<p><b>Runtimefout:</b> het pad &lt;pad&gt; is niet gebonden</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Niet-gekoppelde sjabloon</a></td>
<td>Gegevensintegriteit</td>
<td>Waarschuwing</td>
<td>Bestand &lt;naam&gt; is aan geen bestandsonderdelen gekoppeld en wordt verwijderd nadat de status van de configuratieversie is gewijzigd.</td>
</tr>
<tr>
<td><a href='#i13'>Niet-gesynchroniseerde indeling</a></td>
<td>Gegevensintegriteit</td>
<td>Waarschuwing</td>
<td>Gedefinieerde naam &lt;onderdeelnaam&gt; bestaat niet in de naam van het Excel-werkblad &lt;werkbladnaam&gt;</td>
</tr>
<tr>
<td><a href='#i14'>Niet-gesynchroniseerde indeling</a></td>
<td>Gegevensintegriteit</td>
<td>Waarschuwing</td>
<td>
<p>Label &lt;Gelabeld besturingselement voor Word&gt; bestaat niet in Word-sjabloonbestand</p>
<p><b>Runtimefout:</b> &lt;label Gelabeld besturingselement voor Word&gt; bestaat niet in Word-sjabloonbestand.</p>
</td>
</tr>
<tr>
<td><a href='#i15'>Geen standaardtoewijzing</a></td>
<td>Gegevensintegriteit</td>
<td>Fout</td>
<td>
<p>Er bestaan meerdere modeltoewijzingen voor het gegevensmodel &lt;modelnaam (hoofddescriptor)&gt; in de configuraties &lt;configuratienamen,gescheiden door komma's&gt;. Stel een van de configuraties als standaard in</p>
<p><b>Runtimefout:</b> er bestaan meerdere modeltoewijzingen voor het gegevensmodel &lt;modelnaam (hoofddescriptor)&gt; in de configuraties &lt;configuratienamen,gescheiden door komma's&gt;. Stel een van de configuraties als standaard in.</p>
</td>
</tr>
<tr>
<td><a href='#i16'>Inconsistente instelling van kop- of voettekstonderdelen</a></td>
<td>Gegevensintegriteit</td>
<td>Fout</td>
<td>
<p>Kop-/voetteksten (&lt;onderdeeltype: Kop- of voettekst&gt;) zijn inconsistent</p>
<p><b>Runtime:</b> het laatst geconfigureerde onderdeel wordt tijdens runtime gebruikt als de conceptversie van de geconfigureerde ER-indeling wordt uitgevoerd.</p>
</td>
</tr>
<tr>
<td><a href='#i17'>Inconsistente instelling van onderdeel Pagina</a></td>
<td>Gegevensintegriteit</td>
<td>Fout</td>
<td>Er zijn meer dan twee bereikonderdelen zonder replicatie. Verwijder overbodige onderdelen.</td>
</tr>
<tr>
<td><a href='#i18'>Uitvoerbaarheid van een expressie met ORDERBY-functie</a></td>
<td>Uitvoerbaarheid</td>
<td>Fout</td>
<td>
<p>Op de lijstexpressie van de functie ORDERBY kan geen query worden uitgevoerd.</p>
<p><b>Runtimefout:</b> sorteren wordt niet ondersteund. Valideer de configuratie voor meer informatie hierover.</p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Type conversie

Er wordt gecontroleerd of het gegevenstype van een gegevensmodelveld compatibel is met het gegevenstype van een expressie die is geconfigureerd als binding van het desbetreffende veld. Als de gegevenstypen incompatibel zijn, treedt er een validatiefout op in de ontwerper voor toewijzing van ER-modellen. Er wordt een bericht weergegeven dat er geen expressie van het type A kan worden geconverteerd naar een veld van het type B.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het tegelijkertijd configureren van het ER-gegevensmodel en de ER-modeltoewijzingsonderdelen.
2. Voeg in de gegevensmodelstructuur een veld toe met de naam **X** en selecteer **Geheel getal** als gegevenstype.

    ![Het veld X en het gegevenstype Geheel getal toegevoegd aan de gegevensmodelstructuur op de pagina Gegevensmodel.](./media/er-components-inspections-01.png)

3. Voeg in de ontwerper voor modeltoewijzing, in het deelvenster **Gegevensbronnen**, een gegevensbron van het type **Berekend veld** toe.
4. Noem de nieuwe gegevensbron **Y** en configureer deze zodat deze de expressie `INTVALUE(100)` bevat.
5. Bind **X** aan **Y**.
6. Wijzig in de ontwerper van het gegevensmodel het gegevenstype van het veld **X** van **Geheel getal** in **Int64**.
7. Selecteer **Valideren** om het bewerkbare onderdeel voor modeltoewijzing te inspecteren op de pagina **Ontwerper modeltoewijzing**.

    ![Het bewerkbare onderdeel voor modeltoewijzing valideren op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-01.gif)

8. Selecteer **Valideren** om het onderdeel voor modeltoewijzing van de geselecteerde ER-configuratie te inspecteren op de pagina **Configuraties**.

    ![Het onderdeel voor modeltoewijzing inspecteren op de pagina Configuraties.](./media/er-components-inspections-01a.png)

9. Zoals u ziet, treedt er een validatiefout op. In het bericht staat dat de waarde van het type **Geheel getal** dat de expressie `INTVALUE(100)` van de gegevensbron **Y** als resultaat geeft, niet kan worden opgeslagen in gegevensmodelveld **X** van het type **Int64**.

In de volgende afbeelding wordt de runtimefout weergegeven die optreedt als u de waarschuwing negeert en **Uitvoeren** selecteert om een indeling uit te voeren die is geconfigureerd voor gebruik van de modeltoewijzing.

![Runtimefouten op de pagina Indelingsontwerper.](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Werk de structuur van het gegevensmodel bij door het gegevenstype van het gegevensmodelveld te wijzigen, zodat dit overeenkomt met het gegevenstype van de expressie die is geconfigureerd voor de binding van dat veld. In het bovenstaande voorbeeld moet het gegevenstype van het veld **X** worden teruggezet naar **Geheel getal**.

#### <a name="option-2"></a>Optie 2

Werk de modeltoewijzing bij door de expressie te wijzigen van de gegevensbron die aan het gegevensmodelveld is gebonden. In het bovenstaande voorbeeld moet de expressie van de gegevensbron **Y** worden gewijzigd in `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Typecompatibiliteit

In ER wordt gecontroleerd of het gegevenstype van een indelingselement compatibel is met het gegevenstype van een expressie die is geconfigureerd als binding van het desbetreffende indelingselement. Als de gegevenstypen incompatibel zijn, treedt er een validatiefout op in de ER Operations-ontwerper. In het bericht dat u ontvangt wordt aangegeven dat de geconfigureerde expressie niet kan worden gebruikt als de binding van het huidige indelingselement aan een gegevensbron, omdat deze expressie een waarde retourneert van het gegevenstype A dat buiten het bereik valt van de gegevenstypen die worden ondersteund door huidige indelingselement van het type B.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het tegelijkertijd configureren van het ER-gegevensmodel en de ER-indelingsonderdelen.
2. Voeg in de gegevensmodelstructuur een veld toe met de naam **X** en selecteer **Geheel getal** als gegevenstype.
3. Voeg in de indelingsstructuur een indelingselement van het type **Numeriek** toe.
4. Geef het nieuwe indelingselement **Y** een naam. Selecteer in het veld **Numeriek type** de optie **Geheel getal** als gegevenstype.
5. Bind **X** aan **Y**.
6. Wijzig in de indelingsstructuur het gegevenstype van het indelingselement **Y** van **Geheel getal** in **Int64**.
7. Selecteer **Valideren** om het bewerkbare indelingsonderdeel te inspecteren op de pagina **Indelingsontwerper**.

    ![Typecompatibiliteit valideren op de pagina Indelingsontwerper.](./media/er-components-inspections-02.gif)

8. Zoals u ziet, treedt er een validatiefout op. In het bericht staat dat de geconfigureerde expressie alleen waarden van het type **Int64** kan accepteren. De waarde van het gegevensmodelveld **X** van het type **Geheel getal** kan daarom niet worden ingevoerd in indelingselement **Y**.

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Werk de indelingsstructuur bij door het gegevenstype van het indelingselement **Numeriek** te wijzigen, zodat dit overeenkomt met het gegevenstype van de expressie die u hebt geconfigureerd voor de binding van dat element. In het bovenstaande voorbeeld moet de waarde **Numeriek type** van het indelingselement **X** worden teruggezet naar **Geheel getal**.

#### <a name="option-2"></a>Optie 2

Werk de indelingstoewijzing van indelingselement **X** bij door de expressie te wijzigen van `model.X` in `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Ontbrekend configuratie-element

In ER wordt gecontroleerd of de bindingsexpressies alleen gegevensbronnen bevatten die zijn geconfigureerd in het bewerkbare ER-onderdeel. Voor elke binding die een gegevensbron bevat die ontbreekt in het bewerkbare ER-onderdeel kan een validatiefout optreden in de ER Operations-ontwerper of de ontwerper van ER-modeltoewijzingen.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het tegelijkertijd configureren van het ER-gegevensmodel en de ER-modeltoewijzingsonderdelen.
2. Voeg in de gegevensmodelstructuur een veld toe met de naam **X** en selecteer **Geheel getal** als gegevenstype.

    ![Gegevensmodelstructuur met veld X en gegevenstype Geheel getal op de pagina Gegevensmodel.](./media/er-components-inspections-01.png)

3. Voeg in de ontwerper voor modeltoewijzing, in het deelvenster **Gegevensbronnen**, een gegevensbron van het type **Berekend veld** toe.
4. Noem de nieuwe gegevensbron **Y** en configureer deze zodat deze de expressie `INTVALUE(100)` bevat.
5. Bind **X** aan **Y**.
6. Verwijder in de ontwerper voor modeltoewijzingen, in het deelvenster **Gegevensbronnen**, de gegevensbron **Y**.
7. Selecteer **Valideren** om het bewerkbare onderdeel voor modeltoewijzing te inspecteren op de pagina **Ontwerper modeltoewijzing**.

    ![Het bewerkbare onderdeel voor ER-modeltoewijzing inspecteren op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-03.gif)

8. Zoals u ziet, treedt er een validatiefout op. In het bericht staat dat de binding van het gegevensmodelveld **X** het pad bevat dat verwijst naar gegevensbron **Y**, maar dat deze gegevensbron niet is gevonden.

### <a name="automatic-resolution"></a>Automatische oplossing

Selecteer **Verbinding verbreken** om dit probleem automatisch op te lossen door de ontbrekende gegevensbronbinding te verwijderen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Maak de binding van gegevensmodelveld **X** ongedaan zodat niet langer wordt verwezen naar de niet-bestaande gegevensbron **Y**.

#### <a name="option-2"></a>Optie 2

Voeg in de ontwerper voor modeltoewijzing, in het deelvenster **Gegevensbronnen**, de gegevensbron **Y** opnieuw toe.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Uitvoerbaarheid van een expressie met FILTER-functie

De ingebouwde ER-functie [FILTER](er-functions-list-filter.md) wordt gebruikt om toegang te krijgen tot toepassingstabellen, weergaven of gegevensentiteiten door een enkele SQL-aanroep te plaatsen om de vereiste gegevens als een lijst met records op te halen. Een gegevensbron van het type **Recordlijst** wordt gebruikt als argument van deze functie en geeft de toepassingsbron voor de oproep aan. In ER wordt gecontroleerd of er een directe SQL-query kan worden gemaakt naar een gegevensbron waarnaar wordt verwezen in de functie `FILTER`. Als er geen directe query kan worden gemaakt, treedt een validatiefout op in de ontwerper voor ER-modeltoewijzing. Het bericht dat wordt weergegeven, geeft aan dat de ER-expressie die de functie `FILTER` bevat, niet kan worden uitgevoerd tijdens runtime.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-modeltoewijzingsonderdeel.
2. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
3. Geef de nieuwe gegevensbron de naam **Vendor**. Selecteer in het veld **Tabel** de optie **VendTable** om aan te geven dat deze gegevensbron de tabel VendTable moet opvragen.
4. Voeg een gegevensbron van het type **Berekend veld** toe.
5. Noem de nieuwe gegevensbron **FilteredVendor** en configureer deze zodat deze de expressie `FILTER(Vendor, Vendor.AccountNum="US-101")` bevat.
6. Selecteer **Valideren** om het bewerkbare modeltoewijzingsonderdeel te inspecteren op de pagina **Ontwerper modeltoewijzing** en te controleren of de expressie `FILTER(Vendor, Vendor.AccountNum="US-101")` in de gegevensbron **Vendor** kan worden opgevraagd.
7. Wijzig de gegevensbron **Vendor** door een genest veld van het type **Berekend veld** toe te voegen om het bijgesneden leveranciersrekeningnummer te krijgen.
8. Noem het nieuwe geneste veld **$AccNumber** en configureer het zodat het de expressie `TRIM(Vendor.AccountNum)` bevat.
9. Selecteer **Valideren** om het bewerkbare modeltoewijzingsonderdeel te inspecteren op de pagina **Ontwerper modeltoewijzing** en te controleren of de expressie `FILTER(Vendor, Vendor.AccountNum="US-101")` in de gegevensbron **Vendor** kan worden opgevraagd.

    ![Controleren of de expressie met de FILTER-functie kan worden opgevraagd op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-04.gif)

10. Er treedt een validatiefout op, omdat de gegevensbron **Vendor** een genest veld van het type **Berekend veld** bevat waarmee de expressie van de gegevensbron **FilteredVendor** niet kan worden omgezet in de directe SQL-instructie.

In de volgende afbeelding wordt de runtimefout weergegeven die optreedt als u de waarschuwing negeert en **Uitvoeren** selecteert om een indeling uit te voeren die is geconfigureerd voor gebruik van de modeltoewijzing.

![Runtimefouten die optreden wanneer u de bewerkbare indeling uitvoert op de pagina Indelingsontwerper.](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

In plaats van een genest veld van het type **Berekend veld** toe te voegen aan de gegevensbron **Vendor**, voegt u het geneste veld **$AccNumber** toe aan de gegevensbron **FilteredVendor** en configureert u het veld zodanig dat dit de expressie `TRIM(FilteredVendor.AccountNum)` bevat. Op deze manier kan de expressie `FILTER(Vendor, Vendor.AccountNum="US-101")` worden uitgevoerd op het SQL-niveau en wordt het geneste veld **$AccNumber** achteraf berekend.

#### <a name="option-2"></a>Optie 2

Wijzig de expressie van de gegevensbron **FilteredVendor** van `FILTER(Vendor, Vendor.AccountNum="US-101")` in `WHERE(Vendor, Vendor.AccountNum="US-101")`. We raden u niet aan de expressie voor een tabel met een groot gegevensvolume (transactionele tabel) te wijzigen, omdat alle records worden opgehaald en de vereiste records in het geheugen worden geselecteerd. Deze benadering kan daardoor leiden tot slechte prestaties. Zie [WHERE ER-functie](er-functions-list-where.md) voor meer informatie.

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>Uitvoerbaarheid van een GROUPBY-gegevensbron

De **GROUPBY**-gegevensbron verdeelt het queryresultaat in groepen records, meestal om een of meer aggregaties op elke groep uit te voeren. Elke **GROUPBY**-gegevensbron kan zo worden geconfigureerd dat deze wordt uitgevoerd op het databaseniveau of in het geheugen. Wanneer een **GROUPBY**-gegevensbron zo is geconfigureerd dat deze op databaseniveau wordt uitgevoerd, wordt gecontroleerd of er een directe SQL-query kan worden uitgevoerd naar een gegevensbron waarnaar in die gegevensbron wordt verwezen. Als er geen directe query kan worden gemaakt, treedt een validatiefout op in de ontwerper voor ER-modeltoewijzing. In het bericht wordt gemeld dat de geconfigureerde **GROUPBY**-gegevensbron niet kan worden uitgevoerd tijdens runtime.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-modeltoewijzingsonderdeel.
2. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
3. Geef de nieuwe gegevensbron de naam **Trans**. Selecteer in het veld **Tabel** de optie **VendTrans** om op te geven dat deze gegevensbron de VendTrans-tabel moet opvragen.
4. Voeg een gegevensbron van het type **Group by** toe.
5. Noem de nieuwe gegevensbron **GroupedTrans** en configureer deze op de volgende manier:

    - Selecteer de gegevensbron **Trans** als de bron van records die moeten worden gegroepeerd.
    - Selecteer in het veld **Uitvoeringslocatie** de optie **Query** om op te geven dat u deze gegevensbron op databaseniveau wilt uitvoeren.

    ![De gegevensbron configureren op de pagina 'Groeperen op'-parameters bewerken.](./media/er-components-inspections-05a.gif)

6. Selecteer **Valideren** om het bewerkbare modeltoewijzingsonderdeel te inspecteren op de pagina **Ontwerper modeltoewijzing** en te controleren of de expressie in de geconfigureerde gegevensbron **GroupedTrans** kan worden opgevraagd.
7. Wijzig de gegevensbron **Trans** door een genest veld van het type **Berekend veld** toe te voegen om het bijgesneden leveranciersrekeningnummer te krijgen.
8. Noem de nieuwe gegevensbron **$AccNumber** en configureer deze zodat deze de expressie `TRIM(Trans.AccountNum)` bevat.

    ![De gegevensbron configureren op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-05a.png)

9. Selecteer **Valideren** om het bewerkbare modeltoewijzingsonderdeel te inspecteren op de pagina **Ontwerper modeltoewijzing** en te controleren of de expressie in de geconfigureerde gegevensbron **GroupedTrans** kan worden opgevraagd.

    ![Het ER-modeltoewijzingsonderdeel valideren en controleren of de gegevensbron GroupedTrans kan worden opgevraagd op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-05b.png)

10. Er treedt een validatiefout op, omdat de gegevensbron **Trans** een genest veld van het type **Berekend veld** bevat waarmee de aanvraag voor de gegevensbron **GroupedTrans** niet kan worden omgezet naar de directe SQL-instructie.

In de volgende afbeelding wordt de runtimefout weergegeven die optreedt als u de waarschuwing negeert en **Uitvoeren** selecteert om een indeling uit te voeren die is geconfigureerd voor gebruik van de modeltoewijzing.

![Runtimefouten die optreden wanneer waarschuwing wordt genegeerd op de pagina Indelingsontwerper.](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

In plaats van een genest veld van het type **Berekend veld** toe te voegen aan de gegevensbron **Trans**, voegt u het geneste veld **$AccNumber** toe voor het item **GroupedTrans.lines** van de gegevensbron **GroupedTrans** en configureert u het veld zodanig dat dit de expressie `TRIM(GroupedTrans.lines.AccountNum)` bevat. Op deze manier kan de gegevensbron **GroupedTrans** worden uitgevoerd op het SQL-niveau en wordt het geneste veld **$AccNumber** achteraf berekend.

#### <a name="option-2"></a>Optie 2

Wijzig de waarde van het veld **Uitvoeringslocatie** voor de gegevensbron **GroupedTrans** van **Query** in **In geheugen**. We raden u niet aan de waarde voor een tabel met een groot gegevensvolume (transactionele tabel) te wijzigen, omdat alle records worden opgehaald en groepering en aggregatie in het geheugen worden uitgevoerd. Deze benadering kan daardoor leiden tot slechte prestaties.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>Uitvoerbaarheid van een JOIN-gegevensbron

De [JOIN](er-join-data-sources.md)-gegevens bron combineert records uit twee of meer databasetabellen op basis van gerelateerde velden. Elke **JOIN**-gegevensbron kan zo worden geconfigureerd dat deze wordt uitgevoerd op het databaseniveau of in het geheugen. Wanneer een **JOIN**-gegevensbron zo is geconfigureerd dat deze op databaseniveau wordt uitgevoerd, wordt gecontroleerd of er een directe SQL-query kan worden uitgevoerd naar gegevensbronnen waarnaar in die gegevensbron wordt verwezen. Als er geen directe SQL-query kan worden uitgevoerd waarmee naar ten minste één gegevensbron wordt verwezen, treedt een validatiefout op in de ontwerper voor ER-modeltoewijzing. In het bericht wordt gemeld dat de geconfigureerde **JOIN**-gegevensbron niet kan worden uitgevoerd tijdens runtime.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-modeltoewijzingsonderdeel.
2. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
3. Geef de nieuwe gegevensbron de naam **Vendor**. Selecteer in het veld **Tabel** de optie **VendTable** om aan te geven dat deze gegevensbron de tabel VendTable moet opvragen.
4. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
5. Geef de nieuwe gegevensbron de naam **Trans**. Selecteer in het veld **Tabel** de optie **VendTrans** om op te geven dat deze gegevensbron de VendTrans-tabel moet opvragen.
6. Voeg een gegevensbron van het type **Berekend veld** toe als het geneste veld van de gegevensbron **Vendor**.
7. Noem de nieuwe gegevensbron **FilteredTrans** en configureer deze zodat deze de expressie `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` bevat.
8. Voeg een gegevensbron van het type **Join** toe.
9. Noem de nieuwe gegevensbron **JoinedList** en configureer deze op de volgende manier:

    1. Voeg de gegevensbron **Vendor** toe als eerste set records om samen te voegen.
    2. Voeg de gegevensbron **Vendor.FilteredTrans** toe als tweede set records om samen te voegen. Selecteer **INNER** als het type.
    3. Selecteer in het veld **Uitvoeren** de optie **Query** om op te geven dat u deze gegevensbron op databaseniveau wilt uitvoeren.

    ![De gegevensbron configureren op de pagina Join-ontwerper.](./media/er-components-inspections-06a.gif)

10. Selecteer **Valideren** om het bewerkbare modeltoewijzingsonderdeel te inspecteren op de pagina **Ontwerper modeltoewijzing** en te controleren of de expressie in de geconfigureerde gegevensbron **JoinedList** kan worden opgevraagd.
11. Wijzig de expressie van de gegevensbron **Vendor.FilteredTrans** van `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` in `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Selecteer **Valideren** om het bewerkbare modeltoewijzingsonderdeel te inspecteren op de pagina **Ontwerper modeltoewijzing** en te controleren of de expressie in de geconfigureerde gegevensbron **JoinedList** kan worden opgevraagd.

    ![Het bewerkbare modeltoewijzingsonderdeel valideren en controleren of de gegevensbron JoinedList kan worden opgevraagd op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-06b.png)

13. Er treedt een validatiefout op omdat de expressie van de gegevensbron **Vendor.FilteredTrans** kan niet worden omgezet naar de directe SQL-aanroep. Bovendien staat de directe SQL-aanroep staat niet toe dat de aanroep van de gegevensbron **JoinedList** wordt omgezet in de directe SQL-instructie.

    ![Runtimefouten uit de mislukte validatie van de JoinedList-gegevensbron op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-06c.png)

In de volgende afbeelding wordt de runtimefout weergegeven die optreedt als u de waarschuwing negeert en **Uitvoeren** selecteert om een indeling uit te voeren die is geconfigureerd voor gebruik van de modeltoewijzing.

![De bewerkbare indeling uitvoeren op de pagina Indelingsontwerper.](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Wijzig de expressie van de gegevensbron **Vendor.FilteredTrans** van `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` terug in `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, zoals geadviseerd in de waarschuwing.

![Bijgewerkte expressie van gegevensbron op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Optie 2

Wijzig de waarde van het veld **Uitvoeren** voor de gegevensbron **JoinedList** van **Query** in **In geheugen**. We raden u niet aan de waarde voor een tabel met een groot gegevensvolume (transactionele tabel) te wijzigen, omdat alle records worden opgehaald en de join in het geheugen plaatsvindt. Deze benadering kan daardoor leiden tot slechte prestaties. Er wordt een validatiewaarschuwing weergegeven om u te informeren over dit risico.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Voorkeur voor FILTER-functie boven WHERE-functie

De ingebouwde ER-functie [FILTER](er-functions-list-filter.md) wordt gebruikt om toegang te krijgen tot toepassingstabellen, weergaven of gegevensentiteiten door een enkele SQL-aanroep te plaatsen om de vereiste gegevens als een lijst met records op te halen. Met de [WHERE](er-functions-list-where.md)-functie worden alle records uit de opgegeven bron opgehaald en vindt de recordselectie in het geheugen plaats. Een gegevensbron van het type **Recordlijst** wordt gebruikt als argument van beide functies en er wordt een bron opgegeven voor het ophalen van records. In ER wordt gecontroleerd of er een directe SQL-aanroep kan worden uitgevoerd naar een gegevensbron waarnaar wordt verwezen in de **WHERE**-functie. Als er geen directe aanroep kan worden uitgevoerd, treedt een validatiewaarschuwing op in de ontwerper voor ER-modeltoewijzing. In het bericht dat wordt weergegeven, wordt aanbevolen dat u de **FILTER**-functie gebruikt in plaats van de **WHERE**-functie om de efficiëntie te verbeteren.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-modeltoewijzingsonderdeel.
2. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
3. Geef de nieuwe gegevensbron de naam **Trans**. Selecteer in het veld **Tabel** de optie **VendTrans** om op te geven dat deze gegevensbron de VendTrans-tabel moet opvragen.
4. Voeg een gegevensbron van het type **Berekend veld** toe als het geneste veld van de gegevensbron **Vendor**.
5. Noem de nieuwe gegevensbron **FilteredTrans** en configureer deze zodat deze de expressie `WHERE(Trans, Trans.AccountNum="US-101")` bevat.
6. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
7. Geef de nieuwe gegevensbron de naam **Vendor**. Selecteer in het veld **Tabel** de optie **VendTable** om aan te geven dat deze gegevensbron de tabel VendTable moet opvragen.
8. Voeg een gegevensbron van het type **Berekend veld** toe.
9. Noem de nieuwe gegevensbron **FilteredVendor** en configureer deze zodat deze de expressie `WHERE(Vendor, Vendor.AccountNum="US-101")` bevat.
10. Selecteer **Valideren** om het bewerkbare onderdeel voor modeltoewijzing te inspecteren op de pagina **Ontwerper modeltoewijzing**.

    ![Het bewerkbare onderdeel voor ER-modeltoewijzing inspecteren op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-07a.png)

11. In de validatiewaarschuwingen wordt u geadviseerd om de **FILTER**-functie te gebruiken in plaats van de **WHERE**-functie voor de gegevensbronnen **FilteredVendor** en **FilteredTrans**.

    ![Aanbeveling voor gebruik van de functie FILTER in plaats van de functie WHERE op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Selecteer **Corrigeren** om de **WHERE**-functie automatisch te vervangen door de **FILTER**-functie in de expressie van alle gegevensbronnen die worden weergegeven in het raster op het tabblad **Waarschuwingen** voor dit type inspectie.

U kunt ook de rij selecteren voor een enkele waarschuwing in het raster en vervolgens **Selectie corrigeren** selecteren. In dit geval wordt de expressie automatisch gewijzigd in de gegevensbron die in de geselecteerde waarschuwing wordt vermeld.

![Corrigeren selecteren om automatisch de functie WHERE te vervangen door de functie FILTER op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Handmatige oplossing

U kunt de expressies van alle gegevensbronnen in het validatieraster handmatig aanpassen door de **WHERE**-functie te vervangen door de **FILTER**-functie.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Voorkeur voor ALLITEMSQUERY-functie boven ALLITEMS-functie

De ingebouwde ER-functies [ALLITEMS](er-functions-list-allitems.md) en [ALLITEMSQUERY](er-functions-list-allitemsquery.md) retourneren een afgevlakte waarde voor **Recordlijst** die bestaat uit een lijst met records die alle items vertegenwoordigen die overeenkomen met het opgegeven pad. In ER wordt gecontroleerd of er een directe SQL-aanroep kan worden uitgevoerd naar een gegevensbron waarnaar wordt verwezen in de **ALLITEMS**-functie. Als er geen directe aanroep kan worden uitgevoerd, treedt een validatiewaarschuwing op in de ontwerper voor ER-modeltoewijzing. In het bericht dat wordt weergegeven, wordt aanbevolen dat u de **ALLITEMSQUERY**-functie gebruikt in plaats van de **ALLITEMS**-functie om de efficiëntie te verbeteren.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-modeltoewijzingsonderdeel.
2. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
3. Geef de nieuwe gegevensbron de naam **Vendor**. Selecteer in het veld **Tabel** de optie **VendTable** om aan te geven dat deze gegevensbron de tabel VendTable moet opvragen.
4. Voeg een gegevensbron van het type **Berekend veld** toe om records voor verschillende leveranciers op te halen.
5. Noem de nieuwe gegevensbron **FilteredVendor** en configureer deze zodat deze de expressie `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))` bevat.
6. Een gegevensbron van het type **Berekend veld** toevoegen om de transacties van alle gefilterde leveranciers op te halen.
7. Noem de nieuwe gegevensbron **FilteredVendorTrans** en configureer deze zodat deze de expressie `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')` bevat.
8. Selecteer **Valideren** om het bewerkbare onderdeel voor modeltoewijzing te inspecteren op de pagina **Ontwerper modeltoewijzing**.

    ![Het bewerkbare onderdeel voor modeltoewijzing inspecteren op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-08a.png)

9. Zoals u ziet, treedt er een validatiewaarschuwing op. Het bericht beveelt aan dat u de **ALLITEMSQUERY**-functie gebruikt in plaats van de **ALLITEMS**-functie voor de gegevensbron **FilteredVendorTrans**.

    ![Aanbeveling voor gebruik van de functie ALLITEMSQUERY in plaats van de functie ALLITEMS op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Selecteer **Corrigeren** om de **ALLITEMS**-functie automatisch te vervangen door de **ALLITEMSQUERY**-functie in de expressie van alle gegevensbronnen die worden weergegeven in het raster op het tabblad **Waarschuwingen** voor dit type inspectie.

U kunt ook de rij selecteren voor een enkele waarschuwing in het raster en vervolgens **Selectie corrigeren** selecteren. In dit geval wordt de expressie automatisch gewijzigd in de gegevensbron die in de geselecteerde waarschuwing wordt vermeld.

![Corrigeren selecteren op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Handmatige oplossing

U kunt de expressies van alle gegevensbronnen die worden vermeld in het validatieraster handmatig aanpassen door de **ALLITEMS**-functie te vervangen door de **ALLITEMSQUERY**-functie.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Controle op lege lijstcases

U kunt uw ER-indeling of model toewijzingsonderdeel zodanig configureren dat de veldwaarde van een gegevensbron van het type **Recordlijst** wordt opgehaald. In ER wordt gecontroleerd of in uw ontwerp de case in overweging wordt genomen wanneer een gegevensbron die wordt aangeroepen geen records bevat (dus leeg is), om runtimefouten te voorkomen wanneer een waarde wordt opgehaald uit een veld van een niet-bestaande record.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het tegelijkertijd configureren van het ER-gegevensmodel, de ER-modeltoewijzing en de ER-indelingsonderdelen.
2. Voeg in de gegevensmodelstructuur een hoofditem toe met de naam **Root3**.
3. Wijzig het item **Root3** door een genest item van het type **Recordlijst** toe te voegen.
4. Geef het nieuwe geneste item de naam **Vendor**.
5. Wijzig het item **Vendor** op de volgende manier:

    - Voeg een genest veld van het type **Tekenreeks** toe en geef het de naam **Name**.
    - Voeg een genest veld van het type **Tekenreeks** toe en geef het de naam **AccountNumber**.

    ![Geneste velden toevoegen op de pagina Gegevensmodel.](./media/er-components-inspections-09a.png)

6. Voeg in de ontwerper voor modeltoewijzing, in het deelvenster **Gegevensbronnen**, een gegevensbron van het type **Dynamics 365 for Operations \\ Tabelrecords** toe.
7. Geef de nieuwe gegevensbron de naam **Vendor**. Selecteer in het veld **Tabel** de optie **VendTable** om aan te geven dat deze gegevensbron de tabel VendTable moet opvragen.
8. Voeg een gegevensbron van het type **Algemeen \\ Gebruikersinvoerparameter** toe om te zoeken naar een leveranciersrekening in het runtimedialoogvenster.
9. Geef de nieuwe gegevensbron de naam **RequestedAccountNum**. Voer in het veld **Label** de tekst **Rekeningnummer leverancier** in. Laat in het veld **Naam van gegevenstype voor bewerkingen** de standaardwaarde **Description** ongewijzigd.
10. Voeg een gegevensbron van het type **Berekend veld** toe om een leverancier te filteren die is opgevraagd.
11. Noem de nieuwe gegevensbron **FilteredVendor** en configureer deze zodat deze de expressie `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` bevat.
12. Bind de gegevensmodelitems op de volgende manier aan geconfigureerde gegevensbronnen:

    - Bind **FilteredVendor** aan **Vendor**.
    - Bind **FilteredVendor.AccountNum** aan **Vendor.AccountNumber**.
    - Bind **FilteredVendor.'name()'** aan **Vendor.Name**.

    ![Gegevensmodelitems binden op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-09b.png)

13. Voeg in de indelingsstructuur de volgende items toe om een uitgaand document te genereren in XML-indeling dat de details van de leverancier bevat:

    1. Voeg het hoofd-XML-element **Statement** toe.
    2. Voeg voor het XML-element **Statement** het geneste XML-element **Party** toe.
    3. Voeg voor het XML-element **Party** de volgende geneste XML-kenmerken toe:

        - Naam
        - AccountNum

14. Bind als volgt indelingselementen aan verstrekte gegevensbronnen:

    - Bind het indelingselement **Statement\\Party\\Name** aan het gegevensbronveld **model.Vendor.Name**.
    - Bind het indelingselement **Statement\\Party\\AccountNum** aan het gegevensbronveld **model.Vendor.AccountNumber**.

15. Selecteer **Valideren** om het bewerkbare indelingsonderdeel te inspecteren op de pagina **Indelingsontwerper**.

    ![De indelingselementen valideren die u hebt gebonden aan gegevensbronnen op de pagina Indelingsontwerper.](./media/er-components-inspections-09c.png)

16. Zoals u ziet, treedt er een validatiefout op. Het bericht geeft aan dat er een fout kan worden gegenereerd voor de geconfigureerde indelingsonderdelen **Statement\\Party\\Name** en **Statement\\Party\\AccountNum** tijdens runtime als de lijst `model.Vendor` leeg is.

    ![Validatiefout bij een mogelijke fout voor de geconfigureerde indelingonderdelen.](./media/er-components-inspections-09d.png)

In de volgende afbeelding wordt de runtimefout weergegeven die optreedt als u de waarschuwing negeert, **Uitvoeren** selecteert om de indeling uit te voeren en het rekeningnummer van een niet-bestaande leverancier selecteert. Omdat de aangevraagde leverancier niet bestaat, is de lijst `model.Vendor` leeg (bevat dus geen records).

![Runtimefouten die optreden tijdens het uitvoeren van de indelingstoewijzing.](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Voor de geselecteerde rij in het raster op het tabblad **Waarschuwingen** kunt u **Verbinding verbreken** selecteren. De binding waarnaar wordt verwezen in de kolom **Pad** wordt automatisch uit de indelingselementen verwijderd.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

U kunt het indelingselement **Statement\\Party\\Name** binden aan het gegevensbronitem `model.Vendor`. Tijdens runtime roept deze binding eerst de gegevensbron `model.Vendor` aan. Wanneer `model.Vendor` een lege recordlijst retourneert, worden de geneste indelingselementen niet uitgevoerd. Daarom worden er geen validatiewaarschuwingen voor deze indelingsconfiguratie weergegeven.

![Het indelingselement binden aan het gegevensbronitem op de pagina Indelingsontwerper.](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Optie 2

Wijzig de binding van het indelingselement **Statement\\Party\\Name** van `model.Vendor.Name` in `FIRSTORNULL(model.Vendor).Name`. De bijgewerkte binding converteert de eerste record van de gegevensbron `model.Vendor` van het type **Recordlijst** voorwaardelijk naar een nieuwe gegevensbron van het type **Record**. Deze nieuwe gegevensbron bevat dezelfde set velden.

- Als er ten minste één record beschikbaar is in de gegevensbron `model.Vendor`, worden de velden van deze record gevuld met de waarden van de velden van de eerste record van de gegevensbron `model.Vendor`. In dit geval geeft de bijgewerkte binding de naam van de leverancier als resultaat.
- Anders wordt elk veld van de gemaakte record gevuld met de standaardwaarde voor het gegevenstype van dat veld. In dit geval wordt de lege tekenreeks geretourneerd als de standaardwaarde van het gegevenstype **Tekenreeks**.

Daarom worden er geen validatiewaarschuwingen weergegeven voor het indelingselement **Statement\\Party\\Name** als het is gekoppeld aan de expressie `FIRSTORNULL(model.Vendor).Name`.

![Gewijzigde binding lost validatiewaarschuwingen op de pagina Indelingsontwerper op.](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Optie 3

Als u de gegevens die in een gegenereerd document zijn ingevoerd, expliciet wilt opgeven als de gegevensbron `model.Vendor` van het type **Recordlijst** geen records retourneert (de tekst **Niet beschikbaar** in dit voorbeeld), wordt de binding van het indelingselement **Statement\\Party\\Name** gewijzigd van `model.Vendor.Name` in `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. U kunt ook de expressie `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")` gebruiken.

### <a name="additional-consideration"></a><a id="i9a"></a>Aanvullende overweging

De inspectie waarschuwt u ook voor een ander potentieel probleem. Standaard nemen de bindingen bij het binden van de indelingselementen **Statement\\Party\\Name** en **Statement\\Party\\AccountNum** aan de gewenste velden van de gegevensbron `model.Vendor` van het type **Recordlijst** de waarden aan van de desbetreffende velden van de eerste record van de gegevensbron `model.Vendor` als deze lijst niet leeg is.

Omdat u het indelingselement **Statement\\Party** niet met de gegevensbron `model.Vendor` hebt gebonden, wordt het element **Statement\\Party** niet herhaald voor elke record van de gegevensbron `model.Vendor` tijdens het uitvoeren van de indeling. In plaats daarvan wordt alleen informatie uit de eerste record van de recordlijst ingevuld als die lijst meerdere records bevat. Daarom kan er een probleem optreden als de indeling is bedoeld om een gegenereerd document te vullen met informatie over alle leveranciers in de gegevensbron `model.Vendor`. U kunt dit probleem oplossen door het element **Statement\\Party** aan de gegevensbron `model.Vendor` te binden.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Uitvoerbaarheid van een expressie met FILTER-functie (caching)

Verschillende ingebouwde ER-functies, waaronder [FILTER](er-functions-list-filter.md) en [ALLITEMSQUERY](er-functions-list-allitemsquery.md) worden gebruikt om toegang te krijgen tot toepassingstabellen, weergaven of gegevensentiteiten door een enkele SQL-aanroep te plaatsen om de vereiste gegevens als een lijst met records op te halen. Een gegevensbron van het type **Recordlijst** wordt gebruikt als argument van elk van deze functies en geeft een toepassingsbron voor de oproep aan. In ER wordt gecontroleerd of er een directe SQL-aanroep kan worden uitgevoerd naar een gegevensbron waarnaar wordt verwezen in een van deze functies. Als er geen directe aanroep kan worden uitgevoerd omdat de gegevensbron is gemarkeerd als [in cache](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), treedt een validatiefout op in de ontwerper voor ER-modeltoewijzing. Het bericht dat wordt weergegeven, geeft aan dat de ER-expressie die een van deze functies bevat, niet kan worden uitgevoerd tijdens runtime.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-modeltoewijzingsonderdeel.
2. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
3. Geef de nieuwe gegevensbron de naam **Vendor**. Selecteer in het veld **Tabel** de optie **VendTable** om aan te geven dat deze gegevensbron de tabel VendTable moet opvragen.
4. Voeg een gegevensbron van het type **Algemeen \\ Gebruikersinvoerparameter** toe om te zoeken naar een leveranciersrekening in het runtimedialoogvenster.
5. Geef de nieuwe gegevensbron de naam **RequestedAccountNum**. Voer in het veld **Label** de tekst **Rekeningnummer leverancier** in. Laat in het veld **Naam van gegevenstype voor bewerkingen** de standaardwaarde **Description** ongewijzigd.
6. Voeg een gegevensbron van het type **Berekend veld** toe om een leverancier te filteren die is opgevraagd.
7. Noem de nieuwe gegevensbron **FilteredVendor** en configureer deze zodat deze de expressie `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` bevat.
8. Markeer de geconfigureerde gegevensbron **Vendor** als in cache.

    ![Het onderdeel voor modeltoewijzing configureren op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-10a.gif)

9. Selecteer **Valideren** om het bewerkbare onderdeel voor modeltoewijzing te inspecteren op de pagina **Ontwerper modeltoewijzing**.

    ![De functie FILTER valideren die is toegepast op de in de cache opgeslagen gegevensbron Leverancier op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-10a.png)

10. Zoals u ziet, treedt er een validatiefout op. Het bericht geeft aan dat de **FILTER**-functie niet kan worden toegepast op de gegevensbron **Vendor** in de cache.

In de volgende afbeelding wordt de runtimefout weergegeven die optreedt als u de waarschuwing negeert en **Uitvoeren** selecteert om de indeling uit te voeren.

![Runtimefout die optreedt tijdens het uitvoeren van de indelingstoewijzing op de pagina Indelingsontwerper.](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

De markering **Cache** verwijderen uit de gegevensbron **Vendor**. De gegevensbron **FilteredVendor** wordt dan uitvoerbaar, maar de gegevensbron **Vendor** waarnaar wordt verwezen in de tabel VendTable wordt elke keer geopend wanneer de gegevensbron **FilteredVendor** wordt aangeroepen.

#### <a name="option-2"></a>Optie 2

Wijzig de expressie van de gegevensbron **FilteredVendor** van `FILTER(Vendor, Vendor.AccountNum="US-101")` in `WHERE(Vendor, Vendor.AccountNum="US-101")`. In dit geval wordt de gegevensbron **Vendor** waarnaar wordt verwezen in de tabel VendTable alleen geopend tijdens de eerste aanroep van de gegevensbron **Vendor**. De selectie van records wordt echter in het geheugen uitgevoerd. Deze benadering kan daardoor leiden tot slechte prestaties.

## <a name="missing-binding"></a><a id="i11"></a>Binding ontbreekt

Wanneer u een ER-indelingsonderdeel configureert, wordt het basis-ER-gegevensmodel als standaard gegevensbron aangeboden voor de ER-indeling. Wanneer de geconfigureerde ER-indeling wordt uitgevoerd, wordt de [standaardmodeltoewijzing](er-country-dependent-model-mapping.md) voor het basismodel gebruikt om het gegevensmodel met toepassingsgegevens te vullen. In de ER-indelignsontwerper wordt een waarschuwing weergegeven als u een indelingselement koppelt aan een gegevensmodelitem dat niet is gekoppeld aan een gegevensbron in de modeltoewijzing die momenteel is geselecteerd als standaardmodeltoewijzing voor de bewerkbare indeling. Dit type binding kan niet in runtime worden uitgevoerd, omdat de indeling die wordt uitgevoerd geen gebonden element kan vullen met toepassingsgegevens. Daarom treedt er een fout op tijdens runtime.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het tegelijkertijd configureren van het ER-gegevensmodel, de ER-modeltoewijzing en de ER-indelingsonderdelen.
2. Voeg in de gegevensmodelstructuur een hoofditem toe met de naam **Root3**.
3. Wijzig het item **Root3** door een nieuw genest item van het type **Recordlijst** toe te voegen.
4. Geef het nieuwe geneste item de naam **Vendor**.
5. Wijzig het item **Vendor** op de volgende manier:

    - Voeg een genest veld van het type **Tekenreeks** toe en geef het de naam **Name**.
    - Voeg een genest veld van het type **Tekenreeks** toe en geef het de naam **AccountNumber**.

    ![Geneste velden toevoegen aan het leveranciersitem op de pagina Gegevensmodel.](./media/er-components-inspections-11a.png)

6. Voeg in de ontwerper voor modeltoewijzing, in het deelvenster **Gegevensbronnen**, een gegevensbron van het type **Dynamics 365 for Operations \\ Tabelrecords** toe.
7. Geef de nieuwe gegevensbron de naam **Vendor**. Selecteer in het veld **Tabel** de optie **VendTable** om aan te geven dat deze gegevensbron de tabel VendTable moet opvragen.
8. Voeg een gegevensbron van het type **Algemeen \\ Gebruikersinvoerparameter** toe om te informeren naar een leveranciersrekening in het runtimedialoogvenster.
9. Geef de nieuwe gegevensbron de naam **RequestedAccountNum**. Voer in het veld **Label** de tekst **Rekeningnummer leverancier** in. Laat in het veld **Naam van gegevenstype voor bewerkingen** de standaardwaarde **Description** ongewijzigd.
10. Voeg een gegevensbron van het type **Berekend veld** toe om een leverancier te filteren die is opgevraagd.
11. Noem de nieuwe gegevensbron **FilteredVendor** en configureer deze zodat deze de expressie `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)` bevat.
12. Bind de gegevensmodelitems op de volgende manier aan geconfigureerde gegevensbronnen:

    - Bind **FilteredVendor** aan **Vendor**.
    - Bind **FilteredVendor.AccountNum** aan **Vendor.AccountNumber**.

    > [!NOTE]
    > Het gegevensmodelveld **Vendor.Name** blijft ongebonden.

    ![Gegevensmodelitems die zijn gebonden aan geconfigureerde gegevensbronnen en een gegevensmodusitem dat ongebonden blijft op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-11b.png)

13. Voeg in de indelingsstructuur de volgende items toe om een uitgaand document te genereren in XML-indeling dat de details bevat van de leveranciers waarnaar is geïnformeerd:

    1. Voeg het hoofd-XML-element **Statement** toe.
    2. Voeg voor het XML-element **Statement** het geneste XML-element **Party** toe.
    3. Voeg voor het XML-element **Party** de volgende geneste XML-kenmerken toe:

        - Naam
        - AccountNum

14. Bind als volgt de indelingselementen aan verstrekte gegevensbronnen:

    - Bind het indelingselement **Statement\\Party** aan het gegevensbronitem `model.Vendor`.
    - Bind het indelingselement **Statement\\Party\\Name** aan het gegevensbronveld **model.Vendor.Name**.
    - Bind het indelingselement **Statement\\Party\\AccountNum** aan het gegevensbronveld **model.Vendor.AccountNumber**.

15. Selecteer **Valideren** om het bewerkbare indelingsonderdeel te inspecteren op de pagina **Indelingsontwerper**.

    ![Het ER-indelingsonderdeel valideren op de pagina Indelingsontwerper.](./media/er-components-inspections-11c.png)

16. Zoals u ziet, treedt er een validatiewaarschuwing op. Het bericht geeft aan dat gegevensbronveld **model.Vendor.Name** niet is gebonden aan een gegevensbron in de modeltoewijzing die is geconfigureerd voor gebruik door de indeling. Daarom kan het indelingselement **Statement\\Party\\Name** niet worden gevuld tijdens runtime en kan er een runtime-uitzondering optreden.

    ![Het ER-indelingsonderdeel valideren op de pagina Indelingsontwerper.](./media/er-components-inspections-11d.png)

In de volgende afbeelding wordt de runtimefout weergegeven die optreedt als u de waarschuwing negeert en **Uitvoeren** selecteert om de indeling uit te voeren.

![De bewerkbare indeling uitvoeren op de pagina Indelingsontwerper.](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Wijzig de geconfigureerde modeltoewijzing door een binding toe te voegen voor het gegevensbronveld **model.Vendor.Name**.

#### <a name="option-2"></a>Optie 2

Wijzig de geconfigureerde indeling door de binding te verwijderen voor het indelingselement **Statement\\Party\\Name**.

## <a name="not-linked-template"></a><a id="i12"></a>Niet-gekoppelde sjabloon

Wanneer u [handmatig](er-fillable-excel.md#manual-entry) een ER-indelingsonderdeel configureert om een sjabloon te gebruiken voor het genereren van een uitgaand document, moet u het element **Excel\\File** handmatig toevoegen, de vereiste sjabloon toevoegen als een bijlage van het bewerkbare onderdeel en die bijlage selecteren in het toegevoegde element **Excel\\File**. Op deze manier geeft u aan dat het toegevoegde element de geselecteerde sjabloon tijdens runtime zal vullen. Wanneer u een versie van een indelingsonderdeel configureert met de [status](general-electronic-reporting.md#component-versioning) **Concept**, kunt u verschillende sjablonen toevoegen aan het bewerkbare onderdeel en vervolgens elke sjabloon in het element **Excel\\File** selecteren om de ER-indeling uit te voeren. Op deze manier kunt u zien hoe verschillende sjablonen tijdens runtime worden gevuld. Als u sjablonen hebt die niet zijn geselecteerd in een van de elementen **Excel\\File**, wordt in de ER-indelingsontwerper gewaarschuwd dat deze sjablonen worden verwijderd uit de versie van het bewerkbare ER-indelingsonderdeel wanneer de status wordt gewijzigd van **Concept** in **Voltooid**.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-indelingsonderdeel.
2. Voeg in de indelingsstructuur het element **Excel\\File** toe.
3. Voeg voor het element **Excel\\File** dat u zojuist hebt toegevoegd een Excel-werkmapbestand, **A.xlsx**, toe als bijlage. Gebruik het documenttype dat is geconfigureerd in de [ER-parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) om de opslag van ER-indelingssjablonen op te geven.
4. Voeg voor het element **Excel\\File** nog een Excel-werkmapbestand, **B.xlsx**, toe als bijlage. Gebruik hetzelfde documenttype als is gebruikt voor werkmapbestand A.
5. Selecteer in het element **Excel\\File** werkmapbestand A.
6. Selecteer **Valideren** om het bewerkbare indelingsonderdeel te inspecteren op de pagina **Indelingsontwerper**.

    ![Het bewerkbare-bestandsonderdeel van werkmapbestand valideren op de pagina Indelingsontwerper.](./media/er-components-inspections-12a.gif)

7. Zoals u ziet, treedt er een validatiewaarschuwing op. Het bericht geeft aan dat het werkmapbestand B.xlsx niet is gekoppeld aan onderdelen en dat het wordt verwijderd nadat de status van de configuratieversie is gewijzigd.

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

Wijzig de geconfigureerde indeling door alle sjablonen te verwijderen die niet zijn gekoppeld aan een ander element **Excel\\File**.

## <a name="not-synced-format"></a><a id="i13"></a>Niet-gesynchroniseerde indeling

Wanneer u een ER-indelingsonderdeel [configureert](er-fillable-excel.md) om een Excel-sjabloon te gebruiken voor het genereren van een uitgaand document, kunt u het element **Excel\\File** handmatig toevoegen, de vereiste sjabloon toevoegen als een bijlage van het bewerkbare onderdeel en die bijlage selecteren in het toegevoegde element **Excel\\File**. Op deze manier geeft u aan dat het toegevoegde element de geselecteerde sjabloon tijdens runtime zal vullen. Omdat de toegevoegde Excel-sjabloon extern is ontworpen, kan de bewerkbare ER-indeling mogelijk Excel-namen bevatten die ontbreken in de toegevoegde sjabloon. In de ER-indelingsontwerper wordt een waarschuwing weergegeven over eventuele verschillen tussen de eigenschappen van de ER-indelingselementen die verwijzen naar namen die niet in de toegevoegde Excel-sjabloon zijn opgenomen.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-indelingsonderdeel.
2. Voeg in de indelingsstructuur het **Excel\\File**-element **Rapport** toe.
3. Voeg voor het element **Excel\\File** dat u zojuist hebt toegevoegd een Excel-werkmapbestand, **A.xlsx**, toe als bijlage. Gebruik het documenttype dat is geconfigureerd in de [ER-parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) om de opslag van ER-indelingssjablonen op te geven.

    > [!IMPORTANT]
    > Controleer of de toegevoegde Excel-werkmap geen naam **ReportTitle** bevat.

4. Voeg het **Excel\\Cell**-element **Titel** toe als een genest element van het element **Rapport**. Voer in het veld **Excel-bereik** de waarde **ReportTitle** in.
5. Selecteer **Valideren** om het bewerkbare indelingsonderdeel te inspecteren op de pagina **Indelingsontwerper**.

    ![De geneste elementen en velden valideren op de pagina Indelingsontwerper.](./media/er-components-inspections-13a.png)

6. Zoals u ziet, treedt er een validatiewaarschuwing op. In het bericht staat dat de naam **ReportTitle** niet bestaat op werkblad **Sheet1** van de Excel-sjabloon die u gebruikt.

    ![Validatiewaarschuwing dat de naam ReportTitle niet bestaat op Sheet1 van de Excel-sjabloon.](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Wijzig de geconfigureerde indeling door alle elementen te verwijderen die verwijzen naar Excel-namen die ontbreken in de sjabloon.

#### <a name="option-2"></a>Optie 2

[Werk](er-fillable-excel.md#template-import) de bewerkbare ER-indeling bij door een Excel-sjabloon te importeren. De structuur van de bewerkbare ER-indeling wordt [gesynchroniseerd](modify-electronic-reporting-format-reapply-excel-template.md) met de structuur van de geïmporteerde Excel-sjabloon.

### <a name="additional-consideration"></a>Aanvullende overweging

Zie [De structuur van een sjabloon voor bedrijfsdocumenten bijwerken](er-bdm-update-structure.md) als u wilt weten hoe de indelingsstructuur kan worden gesynchroniseerd met een ER-sjabloon in de sjablooneditor van [Beheer van bedrijfsdocumenten](er-business-document-management.md).

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>Niet gesynchroniseerd met een Word-sjabloonindeling

Wanneer u een ER-indelingsonderdeel [configureert](er-fillable-excel.md) om een Word-sjabloon te gebruiken voor het genereren van een uitgaand document, kunt u het element **Excel\\File** handmatig toevoegen, de vereiste Word-sjabloon toevoegen als een bijlage van het bewerkbare onderdeel en die bijlage selecteren in het toegevoegde element **Excel\\File**.

> [!NOTE]
> Wanneer het Word-document is gekoppeld, geeft de ontwerper van de ER-indeling het bewerkbare element weer als **Word\\File**.

Op deze manier geeft u aan dat het toegevoegde element de geselecteerde sjabloon tijdens runtime zal vullen. Omdat de toegevoegde Word-sjabloon extern is ontworpen, kan de bewerkbare ER-indeling mogelijk verwijzingen naar Word-inhoudsbesturingselementen bevatten die ontbreken in de toegevoegde sjabloon. In de ER-indelingsontwerper wordt een waarschuwing weergegeven over eventuele verschillen tussen de eigenschappen van de ER-indelingselementen die verwijzen naar inhoudsbesturingselementen die niet in de toegevoegde Word-sjabloon zijn opgenomen.

Zie [De bewerkbare indeling configureren om de overzichtssectie te onderdrukken](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control) voor een voorbeeld van het optreden van dit probleem.

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Wijzig de geconfigureerde indeling door de formule **Verwijderd** te verwijderen uit het indelingselement dat wordt genoemd in de validatiewaarschuwing.

#### <a name="option-2"></a>Optie 2

Pas het gebruik van de Word-sjabloon aan door het vereiste label [toe te voegen](er-design-configuration-word-suppress-controls.md#tag-control) aan het relevante Word-inhoudsbesturingselement.

## <a name="no-default-mapping"></a><a id="i15"></a>Geen standaardtoewijzing

Wanneer de inspectie [Ontbrekende binding](#i11) is uitgevoerd, worden de geïnspecteerde indelingsbindingen geëvalueerd aan de hand van de bindingen van het relevante modeltoewijzingsonderdeel. Aangezien u [verschillende](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER-modeltoewijzingsconfiguraties kunt importeren in uw Finance-exemplaar en elke configuratie het toepasselijke modeltoewijzingsonderdeel kan bevatten, moet één configuratie als de standaardconfiguratie worden geselecteerd. Als u anders de geïnspecteerde ER-indeling probeert uit te voeren, te bewerken of te valideren, treedt er een uitzondering op en ontvangt u het volgende bericht: "Er bestaat meer dan één modeltoewijzing voor het gegevensmodel \<model name (root descriptor)\> in de configuraties \<configuration names separated by comma\>. Stel een van de configuraties als standaard in.

Zie [Verschillende afgeleide toewijzingen voor één modelbasis beheren](er-multiple-model-mappings.md) voor een voorbeeld dat laat zien hoe dit probleem kan optreden en hoe dit kan worden opgelost.

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>Inconsistente instelling van kop- of voettekstonderdelen

Wanneer u een onderdeel voor een ER-indeling [configureert](er-fillable-excel.md) om een Excel-sjabloon te gebruiken voor het genereren van een uitgaand document, kunt u het onderdeel **Excel\\Header** toevoegen om kopteksten boven aan een werkblad in een Excel-werkmap toe te voegen. U kunt ook het onderdeel **Excel\\Footer** toevoegen om voetteksten onder aan een werkblad toe te voegen. Voor elk onderdeel **Excel\\Header** of **Excel\\Footer** dat u toevoegt, moet u de weergave-eigenschap **Vormgeving kop-/voettekst** zo instellen dat de pagina's worden opgegeven waarvoor het onderdeel wordt uitgevoerd. Aangezien u verschillende onderdelen voor **Excel\\Header** of **Excel\\Footer** kunt configureren voor een enkel onderdeel **Werkblad** en u verschillende kop- of voetteksten kunt genereren voor verschillende typen pagina's in een Excel-werkblad, moet u één onderdeel **Excel\\Header** of **Excel\\Footer** configureren voor een specifieke waarde van de eigenschap **Vormgeving kop-/voettekst**. Als meerdere onderdelen **Excel\\Header** of **Excel\\Footer** zijn geconfigureerd voor een specifieke waarde van de eigenschap **Vormgeving kop-/voettekst**, treedt er een validatiefout op en wordt het volgende foutbericht weergegeven: 'Kop-/voetteksten (&lt;onderdeeltype: Koptekst of Voettekst&gt;) zijn inconsistent'.

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Pas de geconfigureerde indeling aan door een van de inconsistente onderdelen **Excel\\Header** of **Excel\\Footer** te verwijderen.

#### <a name="option-2"></a>Optie 2

Wijzig de waarde van de eigenschap **Vormgeving kop-/voettekst** voor een van de inconsistente onderdelen **Excel\\Header** of **Excel\\Footer**.

## <a name="inconsistent-setting-of-page-component"></a><a id="i17"></a>Inconsistente instelling van onderdeel Pagina

Wanneer u een ER-indelingscomponent [configureert](er-fillable-excel.md) om een Excel-sjabloon te gebruiken voor het genereren van een uitgaand document, kunt u het onderdeel **Excel\\Pagina** toevoegen om een gegenereerd document te pagineren met ER-formules. Voor elk onderdeel **Excel\\Pagina** dat u toevoegt, kunt u een groot aantal geneste onderdelen [Bereik](er-fillable-excel.md#range-component) toevoegen en toch compatibel blijven met de volgende [structuur](er-fillable-excel.md#page-component-structure):

- Het eerste geneste onderdeel **Bereik** kan zo worden geconfigureerd dat de eigenschap **Replicatierichting** is ingesteld op **Geen replicatie**. Dit bereik wordt gebruikt om paginakopteksten te maken in gegenereerde documenten.
- U kunt veel andere geneste onderdelen **Bereik** toevoegen waarbij de eigenschap **Replicatierichting** is ingesteld op **Verticaal**. Deze bereiken worden gebruikt om in gegenereerde documenten in te vullen.
- Het laatste geneste onderdeel **Bereik** kan zo worden geconfigureerd dat de eigenschap **Replicatierichting** is ingesteld op **Geen replicatie**. Dit bereik wordt gebruikt om paginavoetteksten te maken in gegenereerde documenten en om de vereiste paginaeindes toe te voegen.

Als u deze structuur niet volgt voor een ER-indeling in de ER-indelingsontwerper op het moment van ontwerp, treedt er een validatiefout op en verschijnt het volgende foutbericht: "Er zijn meer dan twee bereikonderdelen zonder replicatie. Verwijder overbodige onderdelen."

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

Pas de geconfigureerde indeling aan door de eigenschap **Replicatierichting** te wijzigen voor alle inconsistente onderdelen **Excel\\Bereik**.

## <a name="executability-of-an-expression-with-orderby-function"></a><a id="i18"></a>Uitvoerbaarheid van een expressie met ORDERBY-functie

De ingebouwde ER-functie [ORDERBY](er-functions-list-orderby.md) wordt gebruikt om de records te sorteren van een ER-gegevensbron van het type **[Recordlijst](er-formula-supported-data-types-composite.md#record-list)** dat wordt opgegeven als een argument van de functie.

Argumenten van de functie `ORDERBY` kunnen worden [opgegeven](er-functions-list-orderby.md#syntax-2) om records te sorteren van toepassingstabellen, weergaven of gegevensentiteiten door een enkele database-aanroep te plaatsen om de gesorteerde gegevens als een lijst met records op te halen. Een gegevensbron van het type **Recordlijst** wordt gebruikt als argument van de functie en geeft de toepassingsbron voor de oproep aan.

In ER wordt gecontroleerd of er een directe databasequery kan worden gemaakt naar een gegevensbron waarnaar wordt verwezen in de functie `ORDERBY`. Als er geen directe query kan worden gemaakt, treedt een validatiefout op in de ontwerper voor ER-modeltoewijzing. Het bericht dat wordt weergegeven, geeft aan dat de ER-expressie die de functie `ORDERBY` bevat, niet kan worden uitgevoerd tijdens runtime.

De volgende stappen laten zien hoe dit probleem kan optreden.

1. Begin met het configureren van het ER-modeltoewijzingsonderdeel.
2. Voeg een gegevensbron toe van het type **Dynamics 365 for Operations \\ Tabelrecords**.
3. Geef de nieuwe gegevensbron de naam **Vendor**. Selecteer in het veld **Tabel** de optie **VendTable** om aan te geven dat deze gegevensbron de tabel **VendTable** moet opvragen.
4. Voeg een gegevensbron van het type **Berekend veld** toe.
5. Geef de nieuwe gegevensbron de naam **OrderedVendors** en configureer deze zodat deze de expressie `ORDERBY("Query", Vendor, Vendor.AccountNum)` bevat.
 
    ![Gegevensbronnen configureren op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-18-1.png)

6. Selecteer **Valideren** om het bewerkbare modeltoewijzingsonderdeel te inspecteren op de pagina **Ontwerper modeltoewijzing** en te controleren of de expressie in de gegevensbron **OrderedVendors** kan worden opgevraagd.
7. Wijzig de gegevensbron **Vendor** door een genest veld van het type **Berekend veld** toe te voegen om het bijgesneden leveranciersrekeningnummer te krijgen.
8. Noem het nieuwe geneste veld **$AccNumber** en configureer het zodat het de expressie `TRIM(Vendor.AccountNum)` bevat.
9. Selecteer **Valideren** om het bewerkbare modeltoewijzingsonderdeel te inspecteren op de pagina **Ontwerper modeltoewijzing** en te controleren of de expressie in de gegevensbron **Vendor** kan worden opgevraagd.

    ![Controleren of de expressie in de gegevensbron Vendor kan worden opgevraagd op de pagina Ontwerper modeltoewijzing.](./media/er-components-inspections-18-2.png)

10. Er treedt een validatiefout op, omdat de gegevensbron **Vendor** een genest veld van het type **Berekend veld** bevat waarmee de expressie van de gegevensbron **OrderedVendors** niet kan worden omgezet in de directe database-instructie. Dezelfde fout treedt op tijdens runtime als u de validatiefout negeert en **Uitvoeren** selecteert om deze modeltoewijzing uit te voeren.

### <a name="automatic-resolution"></a>Automatische oplossing

Er is geen optie beschikbaar om dit probleem automatisch op te lossen.

### <a name="manual-resolution"></a>Handmatige oplossing

#### <a name="option-1"></a>Optie 1

In plaats van een genest veld van het type **Berekend veld** toe te voegen aan de gegevensbron **Vendor**, voegt u het geneste veld **$AccNumber** toe aan de gegevensbron **FilteredVendors** en configureert u het veld zodanig dat dit de expressie `TRIM(FilteredVendor.AccountNum)` bevat. Op deze manier kan de expressie `ORDERBY("Query", Vendor, Vendor.AccountNum)` worden uitgevoerd op het databaseniveau en kan de berekening van het geneste veld **$AccNumber** achteraf worden uitgevoerd.

#### <a name="option-2"></a>Optie 2

Wijzig de expressie van de gegevensbron **FilteredVendors** van `ORDERBY("Query", Vendor, Vendor.AccountNum)` in `ORDERBY("InMemory", Vendor, Vendor.AccountNum)`. We raden u niet aan de expressie voor een tabel met een groot gegevensvolume (transactionele tabel) te wijzigen, omdat alle records worden opgehaald en de ordening van de vereiste records in het geheugen plaatsvindt. Deze benadering kan daardoor leiden tot slechte prestaties.

## <a name="additional-resources"></a>Aanvullende bronnen

[De ER-functie ALLITEMS](er-functions-list-allitems.md)

[De ER-functie ALLITEMSQUERY](er-functions-list-allitemsquery.md)

[De ER-functie INT64VALUE](er-functions-conversion-int64value.md)

[De ER-functie INTVALUE](er-functions-conversion-intvalue.md)

[De ER-functie FILTER](er-functions-list-filter.md)

[De ER-functie WHERE](er-functions-list-where.md)

[JOIN-gegevensbronnen gebruiken om gegevens uit meerdere toepassingstabellen op te halen in ER-modeltoewijzingen](er-join-data-sources.md)

[De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md)

[Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md)

[Besturingselementen voor Word-inhoud onderdrukken in gegenereerde rapporten](er-design-configuration-word-suppress-controls.md)

[Verschillende afgeleide toewijzingen voor één modelbasis beheren](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
