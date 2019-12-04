---
title: Aangepaste velden voor de app Microsoft Dynamics 365 Project Timesheet implementeren in iOS en Android
description: Dit onderwerp bevat algemene patronen voor het gebruik van extensies voor het implementeren van aangepaste velden.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: c0c578ca44919671b67daeea51a9ec7687f755c9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773640"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Aangepaste velden voor de app Microsoft Dynamics 365 Project Timesheet implementeren in iOS en Android

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat algemene patronen voor het gebruik van extensies voor het implementeren van aangepaste velden. De volgende onderwerpen zijn opgenomen:

- De verschillende gegevenstypen die door het raamwerk voor aangepaste velden worden ondersteund
- Alleen-lezen- of bewerkbare velden weergeven in urenstaatinvoer en door de gebruiker opgegeven waarden opslaan in de database
- Alleen-lezenvelden weergeven in de roosterkoptekst
- Andere aangepaste bedrijfslogica integreren integreren om standaardwaarden in velden in te voeren en extra validatie uit te voeren

## <a name="audience"></a>Doelgroep

Dit onderwerp is bedoeld voor ontwikkel aars die hun aangepaste velden integreren in app Microsoft Dynamics 365 Project Timesheet die beschikbaar is voor Apple IOS en Google Android. De veronderstelling is dat lezers vertrouwd zijn met X++-ontwikkeling en de functionaliteit voor projecturenstaten.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Gegevenscontract – TSTimesheetCustomField X++-klasse

De klasse **TSTimesheetCustomField** is de X++-gegevenscontractklasse die staat voor informatie over een aangepast veld voor urenstaatfunctionaliteit. Lijsten met de aangepaste veldobjecten worden zowel in het TSTimesheetDetails-gegevenscontract als in het TSTimesheetEntry-gegevenscontract doorgegeven om aangepaste velden in de mobiele app weer te geven.

- **TSTimesheetDetails** - Het roosterkoptekstcontract.
- **TSTimesheetEntry** - Het urenstaattransactiecontract. Groepen van deze objecten met dezelfde projectgegevens en waarde voor **timesheetLineRecId** vormen een regel.

### <a name="fieldbasetype-types"></a>fieldBaseType (typen)

De eigenschap **FieldBaseType** van het object **TsTimesheetCustom** bepaalt welk type veld wordt weergegeven in de app. De volgende waarden voor **Typen** worden ondersteund.

| Waarden voor typen | Type              | Opmerkingen |
|-------------|-------------------|-------|
| 0           | Tekenreeks (en vaste tekst) | Het veld wordt weergegeven als een tekstveld. |
| 1           | Geheel getal           | De waarde wordt weer gegeven als een getal zonder decimalen. |
| 2           | Real-modus              | De waarde wordt weergegeven als een getal met decimalen.<p>Als u de echte waarde wilt weergeven als een valuta in de app, gebruikt u de eigenschap **fieldExtenededType**. U kunt de eigenschap **numberOfDecimals** gebruiken om het aantal decimalen in te stellen dat wordt weer gegeven.</p> |
| 3           | Datum              | Datumnotaties worden bepaald door de instelling **Datum-, tijd- en getalnotatie** van de gebruiker die is opgegeven onder **Voorkeuren voor taal en land/regio** in **Gebruikersopties**. |
| 4           | Booleaans           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Als de eigenschap **stringOptions** niet wordt opgegeven voor het object **TSTimesheetCustomField**, wordt er een vrije-tekstveld beschikbaar voor de gebruiker.

    De eigenschap **stringLength** kan worden gebruikt om de maximale tekenreekslengte in te stellen die gebruikers kunnen invoeren.

- Als de eigenschap **stringOptions** is opgegeven voor het object **TSTimesheetCustomField**, zijn deze elementen de enige waarden die gebruikers kunnen selecteren met behulp van keuzerondjes.

    In dit geval kan het tekenreeksveld fungeren als een opsommingswaarde voor gebruikersinvoer. Als u de waarde als een opsommingswaarde in de database wilt opslaan, wijst u de tekenreekswaarde weer handmatig toe aan de opsommingswaarde voordat u opslaat naar de database opslaat met behulp van de opdrachtstructuur (zie Opdrachtstructuur voor de klasse TSTimesheetEntryService gebruiken om een urenstaatvermelding uit de app weer op te slaan in de database verderop in dit onderwerp voor een voorbeeld).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Met deze eigenschap kunt u echte waarden opmaken als valuta. Dit kan alleen als **fieldBaseType** is ingesteld op **Werkelijk**.

- **TSCustomFieldExtendedType:None** – Er wordt geen opmaak toegepast.
- **TSCustomFieldExtendedType::Valuta** – De waarde wordt opgemaakt als valuta.

    Wanneer valuta-opmaak actief is, kan het veld **stringValue** worden gebruikt om de valutacode door te geven die in de app moet worden weergegeven. De waarde is een alleen-lezenwaarde.

    Het veld **realValue** bevat het bedrag dat moet worden opgeslagen in de database.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

U kunt deze eigenschap gebruiken om op te geven waar het aangepaste veld moet worden weergegeven in de app.

- **TSCustomFieldSection::Koptekst** – Het veld wordt weergegeven in de sectie **Meer details weergeven** in de app. Deze velden zijn altijd alleen-lezen.
- **TSCustomFieldSection::Regel** –Het veld wordt weergegeven na alle kant-en-klare regelvelden in urenstaatinvoer. Deze velden kunnen bewerkbaar of alleen-lezen zijn.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Met deze eigenschap wordt het veld aangegeven wanneer waarden uit de app worden opgeslagen in de database.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Met deze eigenschap wordt het veld aangegeven wanneer waarden uit de app worden opgeslagen in de database.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Stel deze eigenschap in op **Ja** om op te geven dat het veld in de sectie voor het invoeren van urenstaten moet kunnen worden bewerkt door gebruikers. Stel de eigenschap in op **Nee** als u het veld alleen-lezen wilt maken.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Stel deze eigenschap in op **Ja** om op te geven dat het veld in de sectie voor het invoeren van urenstaten verplicht is.

### <a name="label-str"></a>label (str)

Met deze eigenschap wordt het label opgegeven dat naast het vel wordt weergegeven in de app.

### <a name="stringoptions-list-of-strings"></a>stringOptions (List of Strings)

Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **Tekenreeks**. Als **stringOptions** is ingesteld, wordt op basis van de tekenreeksen in de lijst bepaald welke tekenreekswaarden beschikbaar zijn voor selectie via keuzerondjes. Als er geen tekenreeksen zijn opgegeven, is vrije-tekstinvoer toegestaan in het tekenreeksveld (zie Opdrachtstructuur voor de klasse TSTimesheetEntryService gebruiken om een urenstaatvermelding uit de app weer op te slaan in de database verderop in dit onderwerp voor een voorbeeld).

### <a name="stringlength-int"></a>stringLength (int)

Met deze eigenschap geeft u de maximumlengte voor een tekenreeksveld op. Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **Tekenreeks**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Met deze eigenschap geeft u het aantal decimalen op dat voor een werkelijk veld wordt weergegeven. Deze eigenschap is alleen van toepassing als **fieldBaseType** is ingesteld op **Werkelijk**.

### <a name="ordersequence-int"></a>orderSequence (int)

Deze eigenschap bepaalt de volgorde waarin de aangepaste velden in de app worden weergegeven wanneer meerdere aangepaste velden worden opgegeven. Velden met een lagere waarde worden als eerste weergegeven.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Voor velden van het type **Booleaans** geeft deze eigenschap de Booleaanse waarde van het veld tussen de server en de app door.

### <a name="guidvalue-guid"></a>guidValue (guid)

Voor velden van het type **GUID** geeft deze eigenschap de GUID-waarde van het veld tussen de server en de app door.

### <a name="int64value-int64"></a>int64Value (int64)

Voor velden van het type **Int64** geeft deze eigenschap de int64-waarde van het veld tussen de server en de app door.

### <a name="intvalue-int"></a>intValue (int)

Voor velden van het type **Int** geeft deze eigenschap de int-waarde van het veld tussen de server en de app door.

### <a name="realvalue-real"></a>realValue (real)

Voor velden van het type **Werkelijk** geeft deze eigenschap de werkelijke waarde van het veld tussen de server en de app door.

### <a name="stringvalue-str"></a>stringValue (str)

Voor velden van het type **Tekenreeks** geeft deze eigenschap de tekenreekswaarde van het veld tussen de server en de app door. Deze eigenschap wordt ook gebruikt voor velden van het type **Werkelijk** die zijn opgemaakt als valuta. Voor deze velden wordt de eigenschap gebruikt om de valutacode door te geven aan de app.

### <a name="datevalue-date"></a>dateValue (date)

Voor velden van het type **Datum** geeft deze eigenschap de datumwaarde van het veld tussen de server en de app door.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Een aangepast veld weergeven en opslaan in de sectie voor de invoer van urenstaten

Hieronder vindt u een schermopname van de mobiele app tijdens het maken van urenstaatinvoer. U ziet de kant-en-klare velden en een aangepast veld in de sectie Tijdinvoer met de naam Testtekenreeks en als opsommingswaarde Tweede optie.

![Aangepast veld Testtekenreeks in de app](media/timesheet-entry.jpg)



Hieronder ziet u een schermopname van de mobiele app van de gebruiker die een van de beschikbare opsommingsopties voor het aangepaste veld Testtekenreeks selecteert.  De twee opties zijn Eerste optie en Tweede optie, weergegeven als keuzerondjes. De tweede optie is momenteel geselecteerd.

![Keuzerondjes voor het aangepaste veld Testtekenreeks](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>De tabel TSTimesheetLine uitbreiden met een aangepast veld

In de meeste scenario's worden de gegevens voor een aangepast veld in de sectie voor het invoeren van urenstaten opgeslagen in de tabel TSTimesheetLine. Er kunnen echter andere tabellen worden gebruikt als de gegevens kunnen worden opgehaald op basis van een TSTimesheetTrans-record die wordt geleverd of als er geen specifieke recordcontext is (bijvoorbeeld als het veld is ingesteld als alleen-lezen in de projectparameters).

Houd er rekening mee dat aangepaste velden geen back-ups van databaserecords hoeven te hebben. Deze kunnen dynamisch worden gegenereerd op basis van X + +-logica. Deze benadering kan handig zijn in alleen-lezenscenario's (zie Opdrachtstructuur van de methode buildCustomFieldListForHeader in de klasse TSTimesheetDetailsmethode gebruiken om details van urenstaten in te vullen voor een voorbeeld van dynamisch gegenereerde waarden van aangepaste velden.)

Hieronder ziet u een schermopname uit Visual Studio van de Application Object Tree. Het bevat een uitbreiding van de tabel TSTimesheetLine, waarbij het veld TestLineString als een aangepast veld is toegevoegd.

![Regeltekenreeks](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Opdrachtstructuur voor de methode buildCustomFieldList van de klasse TSTimesheetSettings gebruiken om een veld weer te geven in de sectie voor het invoeren van urenstaten

Met deze code bepaalt u de weergave-instellingen voor het veld in de app. U bepaalt bijvoorbeeld het type veld, het label, of het veld verplicht is en in welke sectie het veld voorkomt.

In het volgende voorbeeld wordt een tekenreeksveld voor tijdsinvoeren weergegeven. Dit veld heeft twee opties, **Eerste optie** en **Tweede optie**, die beschikbaar zijn via keuzerondjes. Het veld in de app is gekoppeld aan het veld **TestLineString** dat aan de tabel TSTimesheetLine is toegevoegd.

U kunt de methode **TSTimesheetCustomField::newFromMetatdata()** gebruiken om de initialisatie van de eigenschappen van aangepaste velden te vereenvoudigen: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** en **numberOfDecimals**. U kunt deze parameters ook handmatig instellen, zoals u wilt.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Opdrachtstructuur voor de methode buildCustomFieldListForEntry van de klasse TSTimesheetEntry gebruiken om waarden in te voeren in een urenstaatboeking

De methode **buildCustomFieldListForEntry** wordt gebruikt om waarden in te voeren op de opgeslagen urenstaatregels in de mobiele app. Een TSTimesheetTrans-record wordt als parameter gebruikt. Velden uit deze record kunnen worden gebruikt om de waarde voor het aangepaste veld in de app in te vullen.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Opdrachtstructuur voor de klasse TSTimesheetEntryService gebruiken om een urenstaatvermelding uit de app weer op te slaan in de database

Als u een aangepast veld op de normale wijze weer in de database wilt opslaan, moet u meerdere methoden uitbreiden:

- De methode **timesheetLineNeedsUpdating** wordt gebruikt om te bepalen of de regelrecord door de gebruiker in de app is gewijzigd en moet worden opgeslagen in de database. Als prestaties geen probleem zijn, kan deze methode worden vereenvoudigd zodat altijd **waar**wordt geretourneerd.
- De methoden **populateTimesheetLineFromEntryDuringCreate** en **populateTimesheetLineFromEntryDuringUpdate** kunnen worden uitgebreid zodat hiermee waarden in de TSTimesheetLine-databaserecord worden ingevoerd vanuit de TSTimesheetEntry-gegevenscontractrecord. In het volgende voorbeeld ziet u hoe de toewijzing tussen het databaseveld en het invoerveld handmatig wordt uitgevoerd via X + +-code.
- De methode **populateTimesheetWeekFromEntry** kan ook worden uitgebreid als het aangepaste veld dat aan het object **TSTimesheetEntry** is toegewezen, moet worden teruggeschreven naar de TSTimesheetLineweek-databasetabel.

> [!NOTE]
> In het volgende voorbeeld wordt de door de gebruiker geselecteerde waarde **firstOption** of **secondOption** als onbewerkte tekenreekswaarde opgeslagen in de database. Als het databaseveld een veld van het type **Opsomming** is, kunnen deze waarden handmatig worden toegewezen aan een opsommingswaarde en vervolgens worden opgeslagen in een opsommingsveld in de databasetabel.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Een aangepast veld weergeven in de sectie voor de roosterkoptekst

Hieronder vindt u een schermopname van de mobiele app van een gebruiker die een urenstaat weergeeft. De knop Meer informatie is geselecteerd in de rechterbovenhoek om de optie Meer details weergeven weer te geven.  

![Opdracht Meer details weergeven](media/show-more.png)

Hieronder vindt u een schermopname van de mobiele app met de sectie Meer van een urenstaat. Een aangepast veld met de naam Verbruikspercentage van deze urenstaat (berekend aangepast veld) is toegevoegd aan de koptekstsectie van de urenstaat. Een alleen-lezenwaarde van 0,667 is ingesteld voor het aangepaste veld.

![Sectie Meer](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>De tabel TSTimesheetTable uitbreiden met een aangepast veld

In de meeste scenario's worden de gegevens voor een aangepast veld in de koptekstsectie uit de tabel TSTimesheetHeader gehaald. Er kunnen echter andere tabellen worden gebruikt als de gegevens kunnen worden opgehaald op basis van een TSTimesheetTable-record die wordt geleverd of als er geen specifieke recordcontext is (bijvoorbeeld als het veld is ingesteld als alleen-lezen in de projectparameters).

Houd er rekening mee dat aangepaste velden geen back-ups van databaserecords hoeven te hebben. Deze kunnen dynamisch worden gegenereerd op basis van X + +-logica. Het volgende voorbeeld wordt deze benadering weergegeven.

Velden in de koptekstsectie zijn altijd alleen-lezen in de app.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Opdrachtstructuur voor de methode buildCustomFieldList van de klasse TSTimesheetSettings gebruiken om een veld weer te geven in de koptekstsectie

Met deze code bepaalt u de weergave-instellingen voor het veld in de app. U bepaalt bijvoorbeeld het type veld, het label, of het veld verplicht is en in welke sectie het veld voorkomt.

In het volgende voorbeeld wordt een berekende waarde in de koptekstsectie van de app weergegeven.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Opdrachtstructuur voor de methode buildCustomFieldListForHeader van de klasse TSTimesheetDetails gebruiken om details van urenstaten in te vullen

De methode **buildCustomFieldListForHeader** wordt gebruikt om koptekstdetails voor urenstaten in te vullen in de mobiele app. Een TSTimesheetTable-record wordt als parameter gebruikt. Velden uit deze record kunnen worden gebruikt om de waarde voor het aangepaste veld in de app in te vullen. In het volgende voorbeeld worden geen waarden gelezen uit de database. In plaats daarvan wordt X + +-logica gebruikt om een berekende waarde te genereren die vervolgens wordt weergegeven in de app.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Overige mogelijkheden voor configuratie/uitbreidbaarheid

### <a name="adding-additional-validation-for-the-app"></a>Aanvullende validatie voor de app toevoegen

Bestaande logica voor urenstaatfunctionaliteit op databaseniveau werkt nog steeds zoals verwacht. Als u het voltooien van bewerkingen voor opslaan of indienen wilt onderbreken en een specifiek foutbericht wilt weergeven, kunt u **throw error("message to user")** aan de code toevoegen door een opdrachtstructuur uit te breiden. Hier volgen drie voorbeelden van handige uitbreidbare methoden:

- Als **validateWrite** voor de tabel TSTimesheetLine **onwaar** retourneert tijdens het opslaan voor een urenstaatregel, wordt een foutbericht weergegeven in de mobiele app.
- Als **validateSubmit** voor de tabel TSTimesheetTable **onwaar** retourneert tijdens het indienen van de urenstaat in de app, wordt een foutbericht weergegeven voor de gebruiker.
- De logica waarmee velden worden ingevuld (bijvoorbeeld **Regeleigenschap**) tijdens de methode **invoegen** in de tabel TSTimesheetLine wordt nog steeds uitgevoerd.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Standaardvelden verbergen en als alleen-lezen markeren via configuratie

Vanuit de projectparameters kunt u standaardvelden alleen-lezen maken of verbergen in de mobiele app. Stel de opties in de sectie **Mobiele urenstaten** op het tabblad **Urenstaat** van de pagina **Projectbeheer- en boekhoudingsparameters** in.

![Projectparameters](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>De beschikbare activiteiten voor selectie via uitbreidingen wijzigen

De activiteiten die beschikbaar zijn voor selectie voor een project, worden gevuld via de methoden **getActivitiesForProject()** en **getActivityQuery()** in de klasse **TsTimesheetProjectService**. U kunt een reeks opdrachten gebruiken om dit gedrag aan te passen aan uw bedrijfsscenario voor de activiteiten die kunnen worden geselecteerd voor een specifiek project.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Een standaardprojectcategorie invoeren voor urenstaatvermeldingen

Het invoeren van een standaardprojectcategorie voor urenstaatvermeldingen vindt plaats op drie niveaus. U kunt een reeks opdrachten gebruiken om het gedrag op een of meer van deze niveaus uit te breiden om het gewenste gedrag te krijgen. De volgende hiërarchie wordt hierbij gebruikt:

1. De app probeert de standaardcategorie uit de projectresource te plaatsen. Deze standaardcategorie wordt ingesteld in de methoden **getCurrentUserResource** en **getDelegatedResourcesForCurrentUser** in de klasse **TSTimesheetSettingsService**.
2. Als de standaardcategorie niet is opgegeven op het niveau van de projectresource, probeert de app deze te halen uit de projectactiviteit. Deze standaardcategorie wordt ingesteld in de methode **getActivitiesForProject** in de klasse **TSTimesheetProjectService**.
3. Als de standaardcategorie niet is opgegeven op het niveau van de projectactiviteit, wordt de standaardcategorie uit de projectparameters gehaald. Deze standaardcategorie wordt ingesteld in de methode **getProjectDetailsbyRule** in de klasse **TSTimesheetProjectService**.
