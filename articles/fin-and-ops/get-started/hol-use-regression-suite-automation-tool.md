---
title: Zelfstudie voor Regression Suite Automation Tool gebruiken
description: In dit onderwerp wordt beschreven hoe u het hulpprogramma RSAT (Regression Suite Automation Tool) kunt gebruiken. Verschillende functies worden beschreven en u krijgt voorbeelden te zien waarin geavanceerde scripts worden gebruikt.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 02933c1649960a4fb58953798799422528d6731d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850822"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>De zelfstudie voor Regression Suite Automation Tool gebruiken

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Gebruik uw internetbrowser om deze pagina als PDF-bestand te downloaden en op te slaan. 

Deze zelfstudie doorloopt enkele van de geavanceerde functies van RSAT, bevat een demotoewijzing en een beschrijving van de strategie en belangrijke trainingspunten.

## <a name="features-of-rsattask-recorder"></a>Functies van RSAT/Taakregistratie

### <a name="validate-a-field-value"></a>Een veldwaarde valideren

Zie voor meer informatie over deze functie [Een nieuwe taakregistratie maken met een functie Valideren](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Opgeslagen variabele

Zie voor meer informatie over deze functie [Een bestaande taakregistratie wijzigen om een opgeslagen variabele te maken](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Afgeleide testcase

1. Open RSAT en selecteer de beide testcases die u hebt gemaakt in [Regression Suite Automation Tool instellen en installeren](./hol-set-up-regression-suite-automation-tool.md).
2. Selecteer **Nieuw \> Afgeleide testcase maken**.

    ![De opdracht Afgeleide testcase maken in het menu Nieuw](./media/use_rsa_tool_01.png)

3. U ontvangt een bericht waarin wordt aangegeven dat er een afgeleide testcase wordt gemaakt voor elke geselecteerde testcase in de huidige testsuite en dat elke afgeleide testcase een eigen exemplaar van het Excel-parameterbestand heeft. Selecteer **OK**.

    > [!NOTE]
    > Wanneer u een afgeleide testcase uitvoert, wordt de taakregistratie van de bovenliggende test en het eigen exemplaar van het Excel-parameterbestand gebruikt. Op deze manier kunt u dezelfde test uitvoeren met verschillende parameters, zonder dat u meer dan één taakregistratie hoeft te onderhouden. Een afgeleide testcase hoeft niet te worden opgenomen in dezelfde testsuite als de bovenliggende test.

    ![Berichtvenster](./media/use_rsa_tool_02.png)

    Er worden twee extra afgeleide testcases gemaakt en het selectievakje **Afgeleid?** is hiervoor ingeschakeld.

    ![Gemaakte afgeleide testcases](./media/use_rsa_tool_03.png)

    Er wordt automatisch een afgeleide testcase gemaakt in Azure DevOps. Het is een onderliggend item van de testcase **Een nieuw product maken** en deze wordt gelabeld met het speciale trefwoord: **RSAT:DerivedTestSteps**. Deze testcases worden ook automatisch toegevoegd aan het testplan in Azure DevOps.

    ![Het trefwoord RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Als de afgeleide testcases die worden gemaakt niet in de juiste volgorde staan, gaat u naar Azure DevOps en stelt u de juiste volgorde in de testsuite in zodat RSAT deze in de juiste volgorde kan uitvoeren.

4. Selecteer de afgeleide testcases en selecteer vervolgens **Bewerken** om de bijbehorende Excel-parameterbestanden te openen.
5. Bewerk deze Excel-parameterbestanden op dezelfde manier als u de bovenliggende bestanden hebt bewerkt. Met andere woorden, zorg ervoor dat de product-id zo is ingesteld dat deze automatisch wordt gegenereerd. Zorg er ook voor dat de opgeslagen variabele naar de relevante velden wordt gekopieerd.
6. Werk op het tabblad **Algemeen** van beide Excel-parameterbestanden de waarde van het veld **Bedrijf** bij naar **USSI**, zodat de afgeleide testcases worden uitgevoerd voor een andere rechtspersoon dan de bovenliggende testcase. Als u de testcases wilt uitvoeren voor een specifieke gebruiker (of de rol die aan een specifieke gebruiker is gekoppeld), kunt u de waarde van het veld **Gebruiker testen** bijwerken.
7. Selecteer **Uitvoeren**en controleer of het product is gemaakt in de rechtspersonen USMF en USSI.

### <a name="validate-notifications"></a>Meldingen valideren

Deze functie kan worden gebruikt om te controleren of een actie is uitgevoerd. Als er bijvoorbeeld een productieorder is gemaakt, is geschat en vervolgens is gestart, wordt in Microsoft Dynamics 365 for Finance and Operations het bericht 'Productie – begin' weergegeven om aan te geven dat de productieorder is gestart.

![De melding Productie - begin](./media/use_rsa_tool_05.png)

U kunt dit bericht valideren via RSAT door de berichttekst in te voeren op het tabblad **MessageValidation** van het Excel-parameterbestand voor de desbetreffende registratie.

![Het tabblad Berichtvalidatie](./media/use_rsa_tool_06.png)

Nadat de testcase is uitgevoerd, wordt het bericht in het Excel-parameterbestand vergeleken met het bericht dat wordt weergegeven in Finance and Operations. Als de berichten niet overeenkomen, mislukt de testcase.

> [!NOTE]
> U kunt meer dan één bericht invoeren op het tabblad **MessageValidation** in het Excel-parameterbestand. In plaats van informatieve berichten kunnen de berichten ook fout- of waarschuwingsberichten zijn.

### <a name="validate-values-by-using-operators"></a>Waarden controleren met operatoren

In eerdere versies van RSAT kon u waarden alleen valideren als een controlewaarde overeenkwam met een verwachte waarde. Met de nieuwe functie kunt u valideren of een variabele niet gelijk is aan, kleiner is dan of groter is dan een opgegeven waarde.

- Als u deze functie wilt gebruiken, opent u het bestand **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en wijzigt u de waarde in het volgende element van **false** in **true**.

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    In het Excel-parameterbestand wordt een nieuw veld **Operator** weergegeven.

    > [!NOTE]
    > Als u een oudere versie van RSAT hebt gebruikt, moet u nieuwe Excel-parameterbestanden genereren.

    ![Het veld Operator](./media/use_rsa_tool_07.png)

In het volgende voorbeeld ziet u hoe u deze functie kunt gebruiken om te valideren of de voorhanden voorraad groter is dan 0 (nul).

1. Maak in de demogegevens in het bedrijf **USMF** een taakregistratie met de volgende stappen:

    1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
    2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld **Artikelnummer** met een waarde van **1000**.
    3. Selecteer **Voorhanden voorraad**.
    4. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld **Vestiging** met een waarde van **1**.
    5. Markeer in de lijst de geselecteerde rij.
    6. Valideer of het veld **Totaal beschikbaar** de waarde **411,0000000000000000** bevat.

2. Sla de taakregistratie op naar de BPM-bibliotheek in LCS en synchroniseer deze naar Azure DevOps.
3. Voeg de testcase toe aan het testplan en laad de testcase in RSAT.
4. Open het Excel-parameterbestand. Op het tabblad **InventOnhandItem** wordt de sectie **InventOnhandItem valideren** met het veld **Operator** weergegeven.

    ![Het veld Operator](./media/use_rsa_tool_08.png)

5. Als u wilt valideren of de voorhanden voorraad altijd meer dan 0 is, wijzigt u de waarde van het veld **Waarde** van **411** in **0** en de waarde van het veld **Operator** van het gelijkteken (**=**) in een groter dan-teken (**\>**).

    ![Gewijzigde waarden van de velden Waarde en Operator](./media/use_rsa_tool_09.png)

6. Sla het Excel-parameterbestand op en sluit het.
7. Selecteer **Uploaden** om de wijzigingen die u in het Excel-parameterbestand hebt aangebracht op te slaan in Azure DevOps.

Als de waarde van het veld **Totaal beschikbaar** voor het opgegeven artikel in voorraad groter is dan 0 (nul), slagen de tests, ongeacht de werkelijke waarde voor voorhanden voorraad.

### <a name="generator-logs"></a>Generatorlogboeken

Met deze functie wordt een map gemaakt die de logboeken bevat van de testcases die zijn uitgevoerd.

- Als u deze functie wilt gebruiken, opent u het bestand **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en wijzigt u de waarde in het volgende element van **false** in **true**.

    ```
    <add key="LogGeneration" value="false" />
    ```

Nadat de testcases zijn uitgevoerd, kunt u de logboekbestanden vinden onder **C:\\Users\\\<Gebruikersnaam\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![De map GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> Als er bestaande testcases bestonden voordat u de waarde in het config-bestand wijzigde, worden er geen logboeken gegenereerd voor deze testcases totdat u nieuwe bestanden voor de testuitvoering genereert.
> 
> ![De opdracht Alleen testuitvoeringsbestanden genereren in het menu Nieuw](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Momentopname

Met deze functie maakt u schermafbeeldingen van de stappen die zijn uitgevoerd tijdens de taakregistratie.

- Als u deze functie wilt gebruiken, opent u het bestand **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en wijzigt u de waarde van het volgende element van **false** in **true**.

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Onder **C:\\Users\\\<Gebruikersnaam\>\\AppData\\Roaming\\regressionTool\\playback** wordt een aparte map gemaakt voor elke testcase die wordt uitgevoerd.

![Map voor momentopnamen voor een testcase](./media/use_rsa_tool_12.png)

In al deze mappen vindt u momentopnamen van de stappen die tijdens het uitvoeren van de testcases zijn uitgevoerd.

![Momentopnamebestanden](./media/use_rsa_tool_13.png)

## <a name="assignment"></a>Toewijzing

### <a name="scenario"></a>Scenario

1. De productontwerper maakt een nieuw vrijgegeven product.
2. De productiemanager initieert een productieorder om het voorraadniveau naar twee stuks te brengen.
3. De productie wordt gestart, de productieorder wordt beëindigd en er wordt gecontroleerd of de voorhanden hoeveelheid uit twee stuks bestaat.
4. Het verkoopteam ontvangt een order voor vier stuks van het nieuwe product. Daarom werkt het verkoopteam de nettobehoeften bij via het dynamische plan. Omdat er geen extra capaciteit beschikbaar is, wordt het standaardorderbeleid ingesteld op kopen in plaats van maken. Daarom wordt een geplande inkooporder gemaakt.
5. De koper voegt een leverancier toe, fiatteert de geplande inkooporder en bevestigt vervolgens de inkooporder.
6. Wanneer de gekochte goederen in de winkel arriveren, zoekt de winkeloperator de bijbehorende inkooporder en ontvangt hij/zij de goederen. Omdat de order nu is voltooid, kunnen goederen worden verzameld en verpakt op basis van de verkooporder.
7. In Financiën worden de inkoop- en verkoopfactuur geboekt.

In de volgende afbeelding wordt de stroom voor dit scenario weergegeven.

![Stroom voor het demoscenario](./media/use_rsa_tool_14.png)

In de volgende afbeelding ziet u de bedrijfsprocessen voor dit scenario in RSAT.

![Bedrijfsprocessen voor het demoscenario](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategie – Belangrijkste trainingspunten

### <a name="data"></a>Gegevens

- Zorg ervoor dat u over representatieve gegevensvolumes (een kopie van productie-/gouden configuratiegegevens plus gemigreerde gegevens) beschikt.
- Wanneer u nieuwe gegevens genereert via Taakregistratie, maakt u testnamen die niet conflicteren met bestaande namen (gebruik bijvoorbeeld een voorvoegsel zoals **RSATxxx**).
- Gebruik Tijdgebonden herstel in Azure om tests in omgevingen zonder Tier 1 opnieuw uit te voeren.
- Hoewel u de Excel-functies **WILLEKEURIG** en **NU** kunt gebruiken om een unieke combinatie te genereren, is dit redelijk veel werk. Hier volgt een voorbeeld.

    ```
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

### <a name="command-line"></a>Opdrachtregel

RSAT kan worden aangeroepen vanuit een **opdrachtpromptvenster**.

> [!NOTE]
> Controleer of de omgevingsvariabele **TestRoot** is ingesteld op het installatiepad van RSAT. (In Microsoft Windows opent u **Configuratiescherm**, selecteert u **Systeem en beveiliging \> Systeem \> Geavanceerde systeeminstellingen** en **Omgevingsvariabelen**.)

1. Open een venster **Opdrachtprompt** en typ het volgende als beheerder.
2. Voer het programma uit vanuit de installatiemap.

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Geef alle opdrachten weer.

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>Windows PowerShell-voorbeelden

#### <a name="run-a-test-case-in-a-loop"></a>Een testcase uitvoeren in een lus

U hebt een testscript waarmee u een nieuwe klant kunt maken. Via scripts kan deze testcase in een lus worden uitgevoerd door de volgende gegevens in willekeurige volgorde te zetten voordat elke iteratie wordt uitgevoerd:

- Klant-ID
- Klantnaam
- Klantadres

De klant-id heeft de notatie *ATCUS\<nummer\>*, waarbij \<nummer\> voor een waarde tussen **000000001** en **999999999** staat.

In het volgende voorbeeld wordt één parameter (**start**) gebruikt om het eerste nummer te definiëren dat wordt gebruikt. Er wordt een tweede parameter (**nr**) gebruikt om het aantal klanten te definiëren dat moet worden gemaakt. Voor elke iteratie worden de parameters in het Excel-parameterbestand gewijzigd met behulp van een UpdateCustomer-functie. Vervolgens wordt de RSAT-opdrachtregel aangeroepen in een RunTestCase-functie.

Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in de beheermodus en plak de volgende code in het venster met de naam **Untitled1. ps1**.

```
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
$excelFilename = "full path to excel file parameter file"
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

```
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
