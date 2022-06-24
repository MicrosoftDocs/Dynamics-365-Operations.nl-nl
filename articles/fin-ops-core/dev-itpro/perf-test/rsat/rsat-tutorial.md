---
title: Zelfstudie voor Regression Suite Automation Tool
description: In dit artikel wordt beschreven hoe u het hulpprogramma RSAT (Regression Suite Automation Tool) kunt gebruiken. Verschillende functies worden beschreven en u krijgt voorbeelden te zien waarin geavanceerde scripts worden gebruikt.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 04c7d7081ece4e077881092534ed061fe2d0e999
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854594"
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

2. Sla de taakregistratie op als een **ontwikkelaarsregistratie** en koppel deze aan uw testcase in Azure DevOps.
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

Wanneer u testcases uitvoert, genereert RSAT momentopnamen (afbeeldingen) van de stappen en slaat deze op in de afspeelmap van de testcases in de werkmap. In de afspeelmap wordt een afzonderlijke submap met de naam **StepSnapshots** gemaakt. Deze map bevat momentopnamen voor de testcases die zijn uitgevoerd.

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
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Hiermee wordt een overzicht van alle opdrachten weergegeven of informatie geboden over een bepaalde opdracht samen met de beschikbare parameters.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: optionele parameters

`command`: waarbij ``[command]`` een van de opdrachten in de voorgaande lijst is.

#### <a name="about"></a>informatie

Hiermee wordt de versie van de geïnstalleerde RSAT opgegeven.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Hiermee wordt het scherm leeggemaakt.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>downloaden

Hiermee worden bijlagen (opname-, uitvoerings- en parameterbestanden) voor de opgegeven testcase vanuit Azure DevOps naar de uitvoermap gedownload. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen en elke waarde uit de eerste kolom gebruiken als parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>download: optionele schakelopties

+ `/retry[=seconds]`- Als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces download het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.

##### <a name="download-required-parameters"></a>download: vereiste parameters

+ `test_case_id`: vertegenwoordigt de id van de testcase.

##### <a name="download-optional-parameters"></a>download: optionele parameters

+ `output_dir`: vertegenwoordigt de uitvoerwerkmap. De map moet bestaan. De werkmap uit de instellingen wordt gebruikt als deze parameter niet is opgegeven.

##### <a name="download-examples"></a>download: voorbeelden

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>downloadsuite

Hiermee worden bijlagen (opname-, uitvoerings- en parameterbestanden) voor alle testcases in de opgegeven testsuite vanuit Azure DevOps naar de uitvoermap gedownload. U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen en elke waarde gebruiken als parameter **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>downloadsuite: optionele schakelopties

+ `/retry[=seconds]`- Als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces download het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.
+ `/byid`: deze schakeloptie geeft aan dat de gewenste testsuite wordt geïdentificeerd op basis van de Azure DevOps-id in plaats van de naam van de testsuite.

##### <a name="downloadsuite-required-parameters"></a>downloadsuite: vereiste parameters

+ `test_suite_name`: vertegenwoordigt de naam van de testsuite. Deze parameter is vereist als de schakeloptie /byid **niet** is opgegeven. Deze naam is de naam van de Azure DevOps-testsuite.
+ `test_suite_id`: vertegenwoordigt de id van de testsuite. Deze parameter is vereist als de schakeloptie /byid **wel** is opgegeven. Deze id is testsuite Azure DevOps-id.

##### <a name="downloadsuite-optional-parameters"></a>downloadsuite: optionele parameters

+ `output_dir`: vertegenwoordigt de uitvoerwerkmap. De map moet bestaan. De werkmap uit de instellingen wordt gebruikt als deze parameter niet is opgegeven.

##### <a name="downloadsuite-examples"></a>downloadsuite: voorbeelden

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>bewerken

Hiermee kunt u het parameterbestand openen in Excel en het bewerken.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit: vereiste parameters

+ `excel_file`: moet een volledig pad naar een bestaand Excel-bestand bevatten.

##### <a name="edit-examples"></a>edit: voorbeelden

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

Hiermee worden testuitvoerings- en parameterbestanden gegenereerd voor de opgegeven testcase in de uitvoermap. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen. Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generate: optionele schakelopties

+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces generate het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.
+ `/dllonly`: uitsluitend testuitvoeringsbestanden voor generate. Genereer het Excel-parameterbestand niet opnieuw.
+ `/keepcustomexcel`: voer een upgrade van het bestaande parametersbestand uit. Genereer ook uitvoeringsbestanden opnieuw.

##### <a name="generate-required-parameters"></a>generate: vereiste parameters

+ `test_case_id`: vertegenwoordigt de id van de testcase.

##### <a name="generate-optional-parameters"></a>generate: optionele parameters

+ `output_dir`: vertegenwoordigt de uitvoerwerkmap. De map moet bestaan. De werkmap uit de instellingen wordt gebruikt als deze parameter niet is opgegeven.

##### <a name="generate-examples"></a>generate: voorbeelden

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Hiermee wordt een nieuwe afgeleide testcase (onderliggende testcase) gegenereerd van de geleverde testcase. De nieuwe testcase wordt eveneens toegevoegd aan de opgegeven testsuite. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen en elke waarde uit de eerste kolom gebruiken als parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>generatederived: optionele schakelopties

+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces generate het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.

##### <a name="generatederived-required-parameters"></a>generatederived: vereiste parameters

+ `parent_test_case_id`: vertegenwoordigt de id van de bovenliggende testcase.
+ `test_plan_id`: vertegenwoordigt de id van het testplan.
+ `test_suite_id`: vertegenwoordigt de id van de testsuite.

##### <a name="generatederived-examples"></a>generatederived: voorbeelden

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Hiermee worden uitsluitend testuitvoeringsbestanden voor de opgegeven testcase gegenereerd. Het Excel-parameterbestand wordt niet gegenereerd. De bestanden worden gegenereerd in de opgegeven uitvoermap. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen en elke waarde uit de eerste kolom gebruiken als parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: optionele schakelopties

+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces generate het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.

##### <a name="generatetestonly-required-parameters"></a>generatetestonly: vereiste parameters

+ `test_case_id`: vertegenwoordigt de id van de testcase.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: optionele parameters

+ `output_dir`: vertegenwoordigt de uitvoerwerkmap. De map moet bestaan. De werkmap uit de instellingen wordt gebruikt als deze parameter niet is opgegeven.

##### <a name="generatetestonly-examples"></a>generatetestonly: voorbeelden

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Hiermee worden testautomatiseringsbestanden voor alle testcases in de opgegeven suite gegenereerd. U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen en elke waarde gebruiken als parameter **test_suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>generatetestsuite: optionele schakelopties

+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces generate het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.
+ `/dllonly`: uitsluitend testuitvoeringsbestanden voor generate. Genereer het Excel-parameterbestand niet opnieuw.
+ `/keepcustomexcel`: voer een upgrade van het bestaande parametersbestand uit. Genereer ook uitvoeringsbestanden opnieuw.
+ `/byid`: deze schakeloptie geeft aan dat de gewenste testsuite wordt geïdentificeerd op basis van de Azure DevOps-id in plaats van de naam van de testsuite.

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite: vereiste parameters

+ `test_suite_name`: vertegenwoordigt de naam van de testsuite. Deze parameter is vereist als de schakeloptie /byid **niet** is opgegeven. Deze naam is de naam van de Azure DevOps-testsuite.
+ `test_suite_id`: vertegenwoordigt de id van de testsuite. Deze parameter is vereist als de schakeloptie /byid **wel** is opgegeven. Deze id is testsuite Azure DevOps-id.

##### <a name="generatetestsuite-optional-parameters"></a>generatetestsuite: optionele parameters

+ `output_dir`: vertegenwoordigt de uitvoerwerkmap. De map moet bestaan. De werkmap uit de instellingen wordt gebruikt als deze parameter niet is opgegeven.

##### <a name="generatetestsuite-examples"></a>generatetestsuite: voorbeelden

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>help

Identiek aan de [?](#section) command.

#### <a name="list"></a>lijst

Geeft een overzicht van alle beschikbare testcases in het huidige testplan.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Hiermee worden alle beschikbare testplannen weergegeven.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Hiermee worden de testcases voor de opgegeven testsuite weergegeven. U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen en elke waarde uit de lijst gebruiken als parameter **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite: vereiste parameters

+ `test_suite_name`: de naam van de gewenste suite.

##### <a name="listtestsuite-examples"></a>listtestsuite: voorbeelden

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtestsuitebyid

Hiermee worden de testcases voor de opgegeven testsuite weergegeven.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtestsuitebyid: vereiste parameters

+ `test_suite_id`: de id van de gewenste suite.

##### <a name="listtestsuitebyid-examples"></a>listtestsuitebyid: voorbeelden

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Geeft een overzicht van alle beschikbare testsuites in het huidige testplan.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

Hiermee wordt de testcase afgespeeld die aan het opgegeven Excel-parameterbestand is gekoppeld. Deze opdracht maakt gebruik van bestaande lokale geautomatiseerde bestanden en downloadt geen bestanden vanuit Azure DevOps. Deze opdracht wordt niet ondersteund voor POS-commerce-testcases.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>playback: optionele schakelopties

+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces playback het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.
+ `/comments[="comment"]`: geef een aangepaste tekenreeks op die wordt opgenomen in het veld **Opmerkingen** op de overzichts- en testresultaatpagina's voor uitvoeringen van Azure DevOps-testcases.

##### <a name="playback-required-parameters"></a>playback: vereiste parameters

+ `excel_parameter_file`: het volledige pad van een Excel-parameterbestand. Het bestand moet bestaan.

##### <a name="playback-examples"></a>playback: voorbeelden

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Hiermee worden meerdere testcases tegelijk afgespeeld. De testcases worden aangeduid met hun id. Met deze opdracht worden bestanden gedownload vanuit Azure DevOps. U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen en elk van de waarden uit de eerste kolom gebruiken als parameter **test_case_id**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>playbackbyid: optionele schakelopties

+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces playback het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.
+ `/comments[="comment"]`: geef een aangepaste tekenreeks op die wordt opgenomen in het veld **Opmerkingen** op de overzichts- en testresultaatpagina's voor uitvoeringen van Azure DevOps-testcases.

##### <a name="playbackbyid-required-parameters"></a>playbackbyid: vereiste parameters

+ `test_case_id1`: de id van een bestaande testcase.
+ `test_case_id2`: de id van een bestaande testcase.
+ `test_case_idN`: de id van een bestaande testcase.

##### <a name="playbackbyid-examples"></a>playbackbyid: voorbeelden

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

Hiermee worden vele testcases tegelijk afgespeeld. De testcases worden geïdentificeerd door de Excel-parameterbestanden. Deze opdracht maakt gebruik van bestaande lokale geautomatiseerde bestanden en downloadt geen bestanden vanuit Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>playbackmany: optionele schakelopties

+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces playback het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.
+ `/comments[="comment"]`: geef een aangepaste tekenreeks op die wordt opgenomen in het veld **Opmerkingen** op de overzichts- en testresultaatpagina's voor uitvoeringen van Azure DevOps-testcases.

##### <a name="playbackmany-required-parameters"></a>playbackmany: vereiste parameters

+ `excel_parameter_file1`: het volledige pad van het Excel-parameterbestand. Het bestand moet bestaan.
+ `excel_parameter_file2`: het volledige pad van het Excel-parameterbestand. Het bestand moet bestaan.
+ `excel_parameter_fileN`: het volledige pad van het Excel-parameterbestand. Het bestand moet bestaan.

##### <a name="playbackmany-examples"></a>playbackmany: voorbeelden

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

Hiermee worden alle testcases uit een of meer opgegeven testsuites afgespeeld. Als de schakeloptie /local is opgegeven, worden lokale bijlagen gebruikt om af te spelen. Anders worden bijlagen gedownload vanuit Azure DevOps. U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen en elke waarde uit de eerste kolom gebruiken als parameter **suite_name**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>playbacksuite: optionele schakelopties

+ `/updatedriver`: als deze switch is opgegeven, wordt de webdriver van de internetbrowser zo nodig bijgewerkt voordat het proces playback wordt uitgevoerd.
+ `/local`: deze schakeloptie geeft aan dat lokale bijlagen moeten worden gebruikt voor deze bestanden in plaats van dat er bestanden worden gedownload vanuit Azure DevOps.
+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces playback het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.
+ `/comments[="comment"]`: geef een aangepaste tekenreeks op die wordt opgenomen in het veld **Opmerkingen** op de overzichts- en testresultaatpagina's voor uitvoeringen van Azure DevOps-testcases.
+ `/byid`: deze schakeloptie geeft aan dat de gewenste testsuite wordt geïdentificeerd op basis van de Azure DevOps-id in plaats van de naam van de testsuite.

##### <a name="playbacksuite-required-parameters"></a>playbacksuite: vereiste parameters

+ `test_suite_name1`: vertegenwoordigt de naam van de testsuite. Deze parameter is vereist als de schakeloptie /byid **niet** is opgegeven. Deze naam is de naam van de Azure DevOps-testsuite.
+ `test_suite_nameN`: vertegenwoordigt de naam van de testsuite. Deze parameter is vereist als de schakeloptie /byid **niet** is opgegeven. Deze naam is de naam van de Azure DevOps-testsuite.
+ `test_suite_id1`: vertegenwoordigt de id van de testsuite. Deze parameter is vereist als de schakeloptie /byid **wel** is opgegeven. Deze id is de testsuite Azure DevOps-id.
+ `test_suite_idN`: vertegenwoordigt de id van de testsuite. Deze parameter is vereist als de schakeloptie /byid **wel** is opgegeven. Deze id is de testsuite Azure DevOps-id.

##### <a name="playbacksuite-examples"></a>playbacksuite: voorbeelden

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>playbacksuitebyid

Hiermee worden alle testcases in de opgegeven Azure DevOps-testsuite uitgevoerd.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>playbacksuitebyid: optionele schakelopties

+ `/retry[=seconds]`: als deze schakeloptie is opgegeven en case-testcases worden geblokkeerd door andere RSAT-exemplaren, wacht het proces playback het opgegeven aantal seconden en doet vervolgens nog één poging. De standaardwaarde voor \[seconden\] is 120 seconden. Zonder deze schakeloptie wordt het proces onmiddellijk geannuleerd als testcases worden geblokkeerd.
+ `/comments[="comment"]`: geef een aangepaste tekenreeks op die wordt opgenomen in het veld **Opmerkingen** op de overzichts- en testresultaatpagina's voor uitvoeringen van Azure DevOps-testcases.
+ `/byid`: deze schakeloptie geeft aan dat de gewenste testsuite wordt geïdentificeerd op basis van de Azure DevOps-id in plaats van de naam van de testsuite.

##### <a name="playbacksuitebyid-required-parameters"></a>playbacksuitebyid: vereiste parameters

+ `test_suite_id`: geeft de testsuite-id weer zoals deze bestaat in Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>playbacksuitebyid: voorbeelden

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>quit

Hiermee wordt de toepassing gesloten. Deze opdracht is alleen nuttig wanneer de toepassingen worden uitgevoerd in de interactieve modus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>quit: voorbeelden

`quit`

#### <a name="upload"></a>upload

Hiermee worden bijlagebestanden (opname-, uitvoerings- en parameterbestanden) die tot een opgegeven testsuite of testcases behoren, geüpload naar Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>upload: vereiste parameters

+ `test_suite_name`: alle bestanden die bij de opgegeven testsuite of testcases horen, worden geüpload.
+ `test_case_id1`: geeft de eerste testcase-id aan die moet worden geüpload. Gebruik deze parameter alleen als er geen naam voor de testsuite is opgegeven.
+ `test_case_idN`: geeft de laatste testcase-id aan die moet worden geüpload. Gebruik deze parameter alleen als er geen naam voor de testsuite is opgegeven.

##### <a name="upload-examples"></a>upload: voorbeelden

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Hiermee wordt alleen het opnamebestand dat bij een of meer van de opgegeven testcases hoort geüpload naar Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording: vereiste parameters

+ `test_case_id1`: geeft de eerste testcase-id aan voor de opname die naar Azure DevOps moet worden geüpload.
+ `test_case_idN`: geeft de laatste testcase-id aan voor de opname die naar Azure DevOps moet worden geüpload.

##### <a name="uploadrecording-examples"></a>uploadrecording: voorbeelden

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

Geeft de drie gebruiksmodi van deze toepassing weer.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

De toepassing interactief uitvoeren:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

De toepassing uitvoeren door een opdracht op te geven:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

De toepassing uitvoeren door een instellingenbestand op te geven:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

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
