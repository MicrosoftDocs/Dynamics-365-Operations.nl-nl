---
title: Zelfstudie voor Regression Suite Automation Tool
description: In dit onderwerp wordt beschreven hoe u het hulpprogramma RSAT (Regression Suite Automation Tool) kunt gebruiken. Verschillende functies worden beschreven en u krijgt voorbeelden te zien waarin geavanceerde scripts worden gebruikt.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: f1d818944ed2779cdad15d84673369e31243285f
ms.sourcegitcommit: ba8ca42e43e1a5251cbbd6ddb292566164d735dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/25/2021
ms.locfileid: "7556760"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Zelfstudie voor Regression Suite Automation Tool

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Gebruik uw internetbrowser om deze pagina als PDF-bestand te downloaden en op te slaan.

Deze zelfstudie doorloopt enkele van de geavanceerde functies van RSAT, bevat een demotoewijzing en een beschrijving van de strategie en belangrijke trainingspunten.

## <a name="notable-features-of-rsat-and-task-recorder"></a>De belangrijkste functies van RSAT en taakregistratie

### <a name="validate-a-field-value"></a>Een veldwaarde valideren

Met RSAT kunt u validatiestappen in uw testaanvraag opnemen om de verwachte waarden te valideren. Zie het artikel [Verwachte waarden valideren](rsat-validate-expected.md) voor meer informatie over deze functie.

In het volgende voorbeeld ziet u hoe u deze functie kunt gebruiken om te valideren of de voorhanden voorraad groter is dan 0 (nul).

1. Maak in de demogegevens in het bedrijf **USMF** een taakregistratie met de volgende stappen:

    1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
    2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld **Artikelnummer** met een waarde van **1000**.
    3. Selecteer **Voorhanden voorraad**.
    4. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld **Vestiging** met een waarde van **1**.
    5. Markeer in de lijst de geselecteerde rij.
    6. Valideer of het veld **Totaal beschikbaar** de waarde **411,0000000000000000** bevat.

2. Sla de taakregistratie op als een **ontwikkelaarsregistratie** en koppel deze aan uw testcase in de Azure Devops.
3. Voeg de testcase toe aan het testplan en laad de testcase in RSAT.
4. Open het Excel-parameterbestand en ga naar het tabblad **TestCaseSteps**.
5. Als u wilt valideren of de voorhanden voorraad altijd meer dan **0** is, gaat u naar de stap **Totaal beschikbaar valideren** en wijzigt u de waarde van **411** in **0**. Wijzig de waarde van het veld **Operator** van een is gelijk-teken (**=**) naar een groter dan-teken (**\>**).
6. Sla het Excel-parameterbestand op en sluit het.
7. Selecteer **Uploaden** om de wijzigingen die u in het Excel-parameterbestand hebt aangebracht op te slaan in Azure DevOps.

Als de waarde van het veld **Totaal beschikbaar** voor het opgegeven artikel in voorraad groter is dan 0 (nul), slagen de tests, ongeacht de werkelijke waarde voor voorhanden voorraad.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Opgeslagen variabelen en aaneenschakeling van testcases

Eén van de belangrijkste functies van RSAT is dat testcases kunnen worden aaneengeschakeld, dat wil zeggen dat variabelen kunnen worden doorgegeven aan andere tests. Zie het artikel [Variabelen kopiëren om testcases aaneen te schakelen](rsat-chain-test-cases.md) voor meer informatie.

### <a name="derived-test-case"></a>Afgeleide testcase

Met RSAT kunt u dezelfde taakregistratie gebruiken met meerdere testcases, zodat een taak kan worden uitgevoerd met verschillende gegevensconfiguraties. Zie het artikel [Afgeleide testcases](rsat-derived-test-cases.md) voor meer informatie.

### <a name="validate-notifications-and-messages"></a>Meldingen en berichten valideren

Deze functie kan worden gebruikt om te controleren of een actie is uitgevoerd. Als er bijvoorbeeld een productieorder is gemaakt, is geschat en vervolgens is gestart, wordt in de app het bericht 'Productie – begin' weergegeven om aan te geven dat de productieorder is gestart.

![De melding Productie - begin.](./media/use_rsa_tool_05.png)

U kunt dit bericht valideren via RSAT door de berichttekst in te voeren op het tabblad **MessageValidation** van het Excel-parameterbestand voor de desbetreffende registratie.

![Het tabblad Berichtvalidatie.](./media/use_rsa_tool_06.png)

Nadat de testcase is uitgevoerd, wordt het bericht in het Excel-parameterbestand vergeleken met het bericht dat wordt weergegeven. Als de berichten niet overeenkomen, mislukt de testcase.

> [!NOTE]
> U kunt meer dan één bericht invoeren op het tabblad **MessageValidation** in het Excel-parameterbestand. In plaats van informatieve berichten kunnen de berichten ook fout- of waarschuwingsberichten zijn.

### <a name="snapshot"></a>Momentopname

Met deze functie maakt u schermafbeeldingen van de stappen die zijn uitgevoerd tijdens de taakregistratie. Het is handig voor het controleren of debuggen van problemen.

- Als u deze functie wilt gebruiken terwijl RSAT wordt uitgevoerd met de gebruikersinterface, opent u het bestand **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en verandert u de waarde van het volgende element van **false** in **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Als u deze functie wilt gebruiken terwijl RSAT wordt uitgevoerd door de CLI (bijvoorbeeld Azure DevOps), opent u het bestand **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en verandert u de waarde van het volgende element van **false** in **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Wanneer u testcases uitvoert, genereert RSAT momentopnamen (afbeeldingen) van de stappen en slaat deze op in de afspeelmap van de testcases in de werkdirectory. In de afspeelmap wordt een afzonderlijke submap met de naam **StepSnapshots** gemaakt. Deze map bevat momentopnamen voor de testcases die zijn uitgevoerd.

## <a name="assignment"></a>Toewijzing

### <a name="scenario"></a>Scenario's

1. De productontwerper maakt een nieuw vrijgegeven product.
2. De productiemanager initieert een productieorder om het voorraadniveau naar twee stuks te brengen.
3. De productie wordt gestart, de productieorder wordt beëindigd en er wordt gecontroleerd of de voorhanden hoeveelheid uit twee stuks bestaat.
4. Het verkoopteam ontvangt een order voor vier stuks van het nieuwe product. Daarom werkt het verkoopteam de nettobehoeften bij via het dynamische plan. Omdat er geen extra capaciteit beschikbaar is, wordt het standaardorderbeleid ingesteld op kopen in plaats van maken. Daarom wordt een geplande inkooporder gemaakt.
5. De koper voegt een leverancier toe, fiatteert de geplande inkooporder en bevestigt vervolgens de inkooporder.
6. Wanneer de gekochte goederen in de winkel arriveren, zoekt de winkeloperator de bijbehorende inkooporder en ontvangt hij/zij de goederen. Omdat de order nu is voltooid, kunnen goederen worden verzameld en verpakt op basis van de verkooporder.
7. In Financiën worden de inkoop- en verkoopfactuur geboekt.

In de volgende afbeelding wordt de stroom voor dit scenario weergegeven.

![Stroom voor het demoscenario.](./media/use_rsa_tool_14.png)

In de volgende afbeelding wordt de hiërarchie van bedrijfsprocessen voor dit scenario weergegeven in de LCS Modelleertool bedrijfsprocessen.

![Bedrijfsprocessen voor het demoscenario.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategie – Belangrijkste trainingspunten

### <a name="data"></a>Gegevens

- Zorg ervoor dat u over representatieve gegevensvolumes (een kopie van productie-/gouden configuratiegegevens plus gemigreerde gegevens) beschikt.
- Wanneer u nieuwe gegevens genereert via Taakregistratie, maakt u testnamen die niet conflicteren met bestaande namen (gebruik bijvoorbeeld een voorvoegsel zoals **RSATxxx**).
- Gebruik Tijdgebonden herstel in Azure om tests in omgevingen zonder Tier 1 opnieuw uit te voeren.
- Hoewel u de Excel-functies **WILLEKEURIG** en **NU** kunt gebruiken om een unieke combinatie te genereren, is dit redelijk veel werk. Hier volgt een voorbeeld.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Taakregistratie

- Definieer scenario's voordat u begint met registreren. Een goed beheerd project bevat vooraf gedefinieerde testscenario's. Als u een testcase wilt maken, moet u overwegen hoe voorspelbaar het resultaat van die testscenario's is.
- Splits opnamen als deze door verschillende rollen worden uitgevoerd of als er wachttijd of een externe gebeurtenis vóór de volgende stap is.
- Vermijd het selecteren van waarden in lijsten. Gebruik in plaats daarvan tekstindelingen, zoals **FIFO**, **AudioRM** en **SiteWH**. Wanneer u een waarde selecteert in een lijst, wordt de positie van de waarde in de lijst vastgelegd, niet de waarde zelf. Als er artikelen aan de lijst worden toegevoegd, kan de positie van de waarde veranderen. Daarom gebruikt uw registratie een andere parameter en kan dit gevolgen hebben voor de rest van het scenario.
- Denk aan het gedrag van meerdere gebruikers. Ga er bijvoorbeeld niet vanuit dat uw nieuwe verkooporder altijd automatisch wordt geselecteerd. Gebruik in plaats daarvan altijd het filter om de juiste order te vinden.
- Gebruik de functie Kopiëren in Taakregistratie om de naam van een nieuw product op te slaan, zodat het kan worden gebruikt in aaneengeschakelde testcases.
- Gebruik de functie Valideren in Taakregistratie om controlepunten in te stellen om te controleren of stappen correct zijn uitgevoerd.

### <a name="rsat"></a>RSAT

- Als u de test in een ander bedrijf wilt uitvoeren, kunt u het bedrijf wijzigen op het tabblad **Algemeen** van het Excel-parameterbestand. Controleer of instellingen en gegevens beschikbaar zijn in het geselecteerde bedrijf.
- U kunt de testgebruiker wijzigen op het tabblad **Algemeen** van het Excel-parameterbestand. Geef de e-mail-id op van de gebruiker die de testcase uitvoert. Op deze manier kan de testcase worden uitgevoerd met behulp van de beveiligingsmachtigingen van de opgegeven gebruiker.
- Als u wilt wachten voordat de test wordt gestart, kunt u een pauze definiëren op het tabblad **Algemeen** van het Excel-parameterbestand. Deze pauze kan worden gebruikt in een batchtaak (bijvoorbeeld als een workflow moet worden uitgevoerd voordat de volgende stap kan worden uitgevoerd.)

## <a name="advanced-scripting"></a>Geavanceerde scripts

### <a name="cli"></a>CLI

RSAT kan worden aangeroepen vanuit een **opdrachtprompt**- of **PowerShell**-venster.

> [!NOTE]
> Controleer of de omgevingsvariabele **TestRoot** is ingesteld op het installatiepad van RSAT. (In Microsoft Windows opent u **Configuratiescherm**, selecteert u **Systeem en beveiliging \> Systeem \> Geavanceerde systeeminstellingen** en **Omgevingsvariabelen**.)

1. Open een **opdrachtprompt**- of **PowerShell**-venster en typ het volgende als beheerder.
2. Ga naar de installatiedirectory van RSAT.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Geef alle opdrachten weer.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Hiermee wordt Help weergegeven over alle beschikbare opdrachten en de bijbehorende parameters.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: optionele parameters

`command`: waarbij ``[command]`` een van de hieronder opgegeven opdrachten is.

#### <a name="about"></a>informatie

Hiermee wordt de huidige versie weergegeven.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Hiermee wordt het scherm leeggemaakt.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>download

Hiermee worden bijlagen voor de opgegeven testaanvraag gedownload naar de uitvoermap.
U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen. Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>download: vereiste parameters

+ `test_case_id`: vertegenwoordigt de id van de testcase.
+ `output_dir`: vertegenwoordigt de uitvoermap. De map moet bestaan.

##### <a name="download-examples"></a>download: voorbeelden

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>bewerken

Hiermee kunt u het parameterbestand openen in Excel en het bewerken.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: vereiste parameters

+ `excel_file`: moet een volledig pad naar een bestaand Excel-bestand bevatten.

##### <a name="edit-examples"></a>edit: voorbeelden

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Hiermee worden testuitvoerings- en parameterbestanden gegenereerd voor de opgegeven testcase in de uitvoermap. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen. Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>generate: vereiste parameters

+ `test_case_id`: vertegenwoordigt de id van de testcase.
+ `output_dir`: vertegenwoordigt de uitvoermap. De map moet bestaan.

##### <a name="generate-examples"></a>generate: voorbeelden

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

Hiermee wordt een nieuwe testcase gegenereerd die is afgeleid van de geleverde testcase. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen. Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived: vereiste parameters

+ `parent_test_case_id`: vertegenwoordigt de id van de bovenliggende testcase.
+ `test_plan_id`: vertegenwoordigt de id van het testplan.
+ `test_suite_id`: vertegenwoordigt de id van de testsuite.

##### <a name="generatederived-examples"></a>generatederived: voorbeelden

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Hiermee wordt alleen een testuitvoeringsbestand voor de opgegeven testcase gegenereerd in de uitvoermap. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen. Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: vereiste parameters

+ `test_case_id`: vertegenwoordigt de id van de testcase.
+ `output_dir`: vertegenwoordigt de uitvoermap. De map moet bestaan.

##### <a name="generatetestonly-examples"></a>generatetestonly: voorbeelden

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

Hiermee worden alle testcases voor de opgegeven suite gegenereerd in de uitvoermap. U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen. Gebruik een willekeurige waarde uit de kolom als parameter voor **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: vereiste parameters

+ `test_suite_name`: vertegenwoordigt de naam van de testsuite.
+ `output_dir`: vertegenwoordigt de uitvoermap. De map moet bestaan.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: voorbeelden

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>help

Identiek aan de [?](#section) command.

#### <a name="list"></a>lijst

Hiermee worden alle beschikbare testcases weergegeven.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Hiermee worden alle beschikbare testplannen weergegeven.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Hiermee worden de testcases voor de opgegeven testsuite weergegeven. U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen. Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: vereiste parameters

+ `suite_name`: naam van de gewenste suite.

##### <a name="listtestsuite-examples"></a>listtestsuite: voorbeelden

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Hiermee worden alle beschikbare testsuites weergegeven.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Hiermee wordt een testcase afgespeeld met een Excel-bestand.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>playback: vereiste parameters

+ `excel_file`: een volledig pad naar het Excel-bestand. Bestand moet bestaan.

##### <a name="playback-examples"></a>playback: voorbeelden

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Hiermee worden meerdere testcases tegelijk afgespeeld. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen. Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: vereiste parameters

+ `test_case_id1`: id van bestaande testcase.
+ `test_case_id2`: id van bestaande testcase.
+ `test_case_idN`: id van bestaande testcase.

##### <a name="playbackbyid-examples"></a>playbackbyid: voorbeelden

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Hiermee wordt een groot aantal testcases tegelijk afgespeeld met Excel-bestanden.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany: vereiste parameters

+ `excel_file1`: volledig pad naar het Excel-bestand. Bestand moet bestaan.
+ `excel_file2`: volledig pad naar het Excel-bestand. Bestand moet bestaan.
+ `excel_fileN`: volledig pad naar het Excel-bestand. Bestand moet bestaan.

##### <a name="playbackmany-examples"></a>playbackmany: voorbeelden

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Hiermee worden alle testcases uit de opgegeven testsuite afgespeeld.
U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen. Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: vereiste parameters

+ `suite_name`: naam van de gewenste suite.

##### <a name="playbacksuite-examples"></a>playbacksuite: voorbeelden

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>quit

Hiermee wordt de toepassing gesloten.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>upload

Hiermee worden alle bestanden geüpload die bij de opgegeven testsuite of testcases horen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>upload: vereiste parameters

+ `suite_name`: alle bestanden die bij de opgegeven testsuite of testcases horen, worden geüpload.
+ `testcase_id`: alle bestanden die bij de opgegeven testcase(s) horen, worden geüpload.

##### <a name="upload-examples"></a>upload: voorbeelden

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Hiermee worden alleen opnamebestanden geüpload die bij de opgegeven testcases horen.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: vereiste parameters

+ `testcase_id`: opnamebestand dat bij de opgegeven testcases hoort, wordt geüpload.

##### <a name="uploadrecording-examples"></a>uploadrecording: voorbeelden

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Hiermee worden twee manieren weergegeven om deze toepassing aan te roepen: een waarbij gebruik wordt gemaakt van een standaard instellingsbestand en een andere waarbij een instellingsbestand wordt geleverd.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>Windows PowerShell-voorbeelden

#### <a name="run-a-test-case-in-a-loop"></a>Een testcase uitvoeren in een lus

U hebt een testscript waarmee u een nieuwe klant kunt maken. Via scripts kan deze testcase in een lus worden uitgevoerd door de volgende gegevens in willekeurige volgorde te zetten voordat elke iteratie wordt uitgevoerd:

- Klant-ID
- Klantnaam
- Klantadres

De klant-id heeft de notatie *ATCUS\<number\>*, waarbij \<number\> voor een waarde tussen **000000001** en **999999999** staat.

In het volgende voorbeeld wordt één parameter, **start**, gebruikt om het eerste nummer te definiëren dat wordt gebruikt. Er wordt een tweede parameter, **nr**, gebruikt om het aantal klanten te definiëren dat moet worden gemaakt. Voor elke iteratie worden de parameters in het Excel-parameterbestand gewijzigd met behulp van een UpdateCustomer-functie. Vervolgens wordt de RSAT-opdrachtregel aangeroepen in een RunTestCase-functie.

Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in de beheermodus en plak de volgende code in het venster met de naam **Untitled1. ps1**.

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Een script uitvoeren dat afhankelijk is van gegevens in Microsoft Dynamics 365

In het volgende voorbeeld wordt een OData-aanroep (Open Data Protocol) gebruikt om de orderstatus van een inkooporder te zoeken. Als de status niet **gefactureerd** is, kunt u bijvoorbeeld een RSAT-testcase aanroepen waarmee de factuur wordt geboekt.

```powershell
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
