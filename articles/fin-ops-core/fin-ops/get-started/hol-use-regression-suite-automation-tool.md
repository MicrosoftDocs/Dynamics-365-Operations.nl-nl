---
title: De zelfstudie voor Regression Suite Automation Tool gebruiken
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
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070815"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="ce476-104">De zelfstudie voor Regression Suite Automation Tool gebruiken</span><span class="sxs-lookup"><span data-stu-id="ce476-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ce476-105">Gebruik uw internetbrowser om deze pagina als PDF-bestand te downloaden en op te slaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="ce476-106">Deze zelfstudie doorloopt enkele van de geavanceerde functies van RSAT, bevat een demotoewijzing en een beschrijving van de strategie en belangrijke trainingspunten.</span><span class="sxs-lookup"><span data-stu-id="ce476-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="ce476-107">Functies van RSAT/Taakregistratie</span><span class="sxs-lookup"><span data-stu-id="ce476-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="ce476-108">Een veldwaarde valideren</span><span class="sxs-lookup"><span data-stu-id="ce476-108">Validate a field value</span></span>

<span data-ttu-id="ce476-109">Zie voor meer informatie over deze functie [Een nieuwe taakregistratie maken met een functie Valideren](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="ce476-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="ce476-110">Opgeslagen variabele</span><span class="sxs-lookup"><span data-stu-id="ce476-110">Saved variable</span></span>

<span data-ttu-id="ce476-111">Zie voor meer informatie over deze functie [Een bestaande taakregistratie wijzigen om een opgeslagen variabele te maken](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="ce476-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="ce476-112">Afgeleide testcase</span><span class="sxs-lookup"><span data-stu-id="ce476-112">Derived test case</span></span>

1. <span data-ttu-id="ce476-113">Open RSAT en selecteer de beide testcases die u hebt gemaakt in [Zelfstudie over het instellen en installeren van Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="ce476-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="ce476-114">Selecteer **Nieuw \> Afgeleide testcase maken**.</span><span class="sxs-lookup"><span data-stu-id="ce476-114">Select **New \> Create derived test case**.</span></span>

    ![De opdracht Afgeleide testcase maken in het menu Nieuw](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="ce476-116">U ontvangt een bericht waarin wordt aangegeven dat er een afgeleide testcase wordt gemaakt voor elke geselecteerde testcase in de huidige testsuite en dat elke afgeleide testcase een eigen exemplaar van het Excel-parameterbestand heeft.</span><span class="sxs-lookup"><span data-stu-id="ce476-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="ce476-117">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce476-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce476-118">Wanneer u een afgeleide testcase uitvoert, wordt de taakregistratie van de bovenliggende test en het eigen exemplaar van het Excel-parameterbestand gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ce476-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="ce476-119">Op deze manier kunt u dezelfde test uitvoeren met verschillende parameters, zonder dat u meer dan één taakregistratie hoeft te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="ce476-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="ce476-120">Een afgeleide testcase hoeft niet te worden opgenomen in dezelfde testsuite als de bovenliggende test.</span><span class="sxs-lookup"><span data-stu-id="ce476-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Berichtvenster](./media/use_rsa_tool_02.png)

    <span data-ttu-id="ce476-122">Er worden twee extra afgeleide testcases gemaakt en het selectievakje **Afgeleid?** is hiervoor ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ce476-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Gemaakte afgeleide testcases](./media/use_rsa_tool_03.png)

    <span data-ttu-id="ce476-124">Er wordt automatisch een afgeleide testcase gemaakt in Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ce476-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="ce476-125">Het is een onderliggend item van de testcase **Een nieuw product maken** en deze wordt gelabeld met het speciale trefwoord: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="ce476-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="ce476-126">Deze testcases worden ook automatisch toegevoegd aan het testplan in Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ce476-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Het trefwoord RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="ce476-128">Als de afgeleide testcases die worden gemaakt niet in de juiste volgorde staan, gaat u naar Azure DevOps en stelt u de juiste volgorde in de testsuite in zodat RSAT deze in de juiste volgorde kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ce476-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="ce476-129">Selecteer de afgeleide testcases en selecteer vervolgens **Bewerken** om de bijbehorende Excel-parameterbestanden te openen.</span><span class="sxs-lookup"><span data-stu-id="ce476-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="ce476-130">Bewerk deze Excel-parameterbestanden op dezelfde manier als u de bovenliggende bestanden hebt bewerkt.</span><span class="sxs-lookup"><span data-stu-id="ce476-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="ce476-131">Met andere woorden, zorg ervoor dat de product-id zo is ingesteld dat deze automatisch wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="ce476-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="ce476-132">Zorg er ook voor dat de opgeslagen variabele naar de relevante velden wordt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="ce476-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="ce476-133">Werk op het tabblad **Algemeen** van beide Excel-parameterbestanden de waarde van het veld **Bedrijf** bij naar **USSI**, zodat de afgeleide testcases worden uitgevoerd voor een andere rechtspersoon dan de bovenliggende testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="ce476-134">Als u de testcases wilt uitvoeren voor een specifieke gebruiker (of de rol die aan een specifieke gebruiker is gekoppeld), kunt u de waarde van het veld **Gebruiker testen** bijwerken.</span><span class="sxs-lookup"><span data-stu-id="ce476-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="ce476-135">Selecteer **Uitvoeren**en controleer of het product is gemaakt in de rechtspersonen USMF en USSI.</span><span class="sxs-lookup"><span data-stu-id="ce476-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="ce476-136">Meldingen valideren</span><span class="sxs-lookup"><span data-stu-id="ce476-136">Validate notifications</span></span>

<span data-ttu-id="ce476-137">Deze functie kan worden gebruikt om te controleren of een actie is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ce476-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="ce476-138">Als er bijvoorbeeld een productieorder is gemaakt, is geschat en vervolgens is gestart, wordt in de app het bericht 'Productie – begin' weergegeven om aan te geven dat de productieorder is gestart.</span><span class="sxs-lookup"><span data-stu-id="ce476-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![De melding Productie - begin](./media/use_rsa_tool_05.png)

<span data-ttu-id="ce476-140">U kunt dit bericht valideren via RSAT door de berichttekst in te voeren op het tabblad **MessageValidation** van het Excel-parameterbestand voor de desbetreffende registratie.</span><span class="sxs-lookup"><span data-stu-id="ce476-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Het tabblad Berichtvalidatie](./media/use_rsa_tool_06.png)

<span data-ttu-id="ce476-142">Nadat de testcase is uitgevoerd, wordt het bericht in het Excel-parameterbestand vergeleken met het bericht dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="ce476-143">Als de berichten niet overeenkomen, mislukt de testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="ce476-144">U kunt meer dan één bericht invoeren op het tabblad **MessageValidation** in het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="ce476-145">In plaats van informatieve berichten kunnen de berichten ook fout- of waarschuwingsberichten zijn.</span><span class="sxs-lookup"><span data-stu-id="ce476-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="ce476-146">Waarden controleren met operatoren</span><span class="sxs-lookup"><span data-stu-id="ce476-146">Validate values by using operators</span></span>

<span data-ttu-id="ce476-147">In eerdere versies van RSAT kon u waarden alleen valideren als een controlewaarde overeenkwam met een verwachte waarde.</span><span class="sxs-lookup"><span data-stu-id="ce476-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="ce476-148">Met de nieuwe functie kunt u valideren of een variabele niet gelijk is aan, kleiner is dan of groter is dan een opgegeven waarde.</span><span class="sxs-lookup"><span data-stu-id="ce476-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="ce476-149">Als u deze functie wilt gebruiken, opent u het bestand **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en wijzigt u de waarde in het volgende element van **false** in **true**.</span><span class="sxs-lookup"><span data-stu-id="ce476-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="ce476-150">In het Excel-parameterbestand wordt een nieuw veld **Operator** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ce476-151">Als u een oudere versie van RSAT hebt gebruikt, moet u nieuwe Excel-parameterbestanden genereren.</span><span class="sxs-lookup"><span data-stu-id="ce476-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Het veld Operator](./media/use_rsa_tool_07.png)

<span data-ttu-id="ce476-153">In het volgende voorbeeld ziet u hoe u deze functie kunt gebruiken om te valideren of de voorhanden voorraad groter is dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="ce476-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="ce476-154">Maak in de demogegevens in het bedrijf **USMF** een taakregistratie met de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="ce476-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="ce476-155">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="ce476-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="ce476-156">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ce476-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ce476-157">Filter bijvoorbeeld op het veld **Artikelnummer** met een waarde van **1000**.</span><span class="sxs-lookup"><span data-stu-id="ce476-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="ce476-158">Selecteer **Voorhanden voorraad**.</span><span class="sxs-lookup"><span data-stu-id="ce476-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="ce476-159">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ce476-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ce476-160">Filter bijvoorbeeld op het veld **Vestiging** met een waarde van **1**.</span><span class="sxs-lookup"><span data-stu-id="ce476-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="ce476-161">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ce476-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="ce476-162">Valideer of het veld **Totaal beschikbaar** de waarde **411,0000000000000000** bevat.</span><span class="sxs-lookup"><span data-stu-id="ce476-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="ce476-163">Sla de taakregistratie op naar de BPM-bibliotheek in LCS en synchroniseer deze naar Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ce476-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="ce476-164">Voeg de testcase toe aan het testplan en laad de testcase in RSAT.</span><span class="sxs-lookup"><span data-stu-id="ce476-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="ce476-165">Open het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-165">Open the Excel parameter file.</span></span> <span data-ttu-id="ce476-166">Op het tabblad **InventOnhandItem** wordt de sectie **InventOnhandItem valideren** met het veld **Operator** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Het veld Operator](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="ce476-168">Als u wilt valideren of de voorhanden voorraad altijd meer dan 0 is, wijzigt u de waarde van het veld **Waarde** van **411** in **0** en de waarde van het veld **Operator** van het gelijkteken (**=**) in een groter dan-teken (**\>**).</span><span class="sxs-lookup"><span data-stu-id="ce476-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Gewijzigde waarden van de velden Waarde en Operator](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="ce476-170">Sla het Excel-parameterbestand op en sluit het.</span><span class="sxs-lookup"><span data-stu-id="ce476-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="ce476-171">Selecteer **Uploaden** om de wijzigingen die u in het Excel-parameterbestand hebt aangebracht op te slaan in Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ce476-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="ce476-172">Als de waarde van het veld **Totaal beschikbaar** voor het opgegeven artikel in voorraad groter is dan 0 (nul), slagen de tests, ongeacht de werkelijke waarde voor voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="ce476-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="ce476-173">Generatorlogboeken</span><span class="sxs-lookup"><span data-stu-id="ce476-173">Generator logs</span></span>

<span data-ttu-id="ce476-174">Met deze functie wordt een map gemaakt die de logboeken bevat van de testcases die zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ce476-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="ce476-175">Als u deze functie wilt gebruiken, opent u het bestand **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en wijzigt u de waarde in het volgende element van **false** in **true**.</span><span class="sxs-lookup"><span data-stu-id="ce476-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="ce476-176">Nadat de testcases zijn uitgevoerd, kunt u de logboekbestanden vinden onder **C:\\Users\\\<Gebruikersnaam\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="ce476-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![De map GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="ce476-178">Als er bestaande testcases bestonden voordat u de waarde in het config-bestand wijzigde, worden er geen logboeken gegenereerd voor deze testcases totdat u nieuwe bestanden voor de testuitvoering genereert.</span><span class="sxs-lookup"><span data-stu-id="ce476-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![De opdracht Alleen testuitvoeringsbestanden genereren in het menu Nieuw](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="ce476-180">Momentopname</span><span class="sxs-lookup"><span data-stu-id="ce476-180">Snapshot</span></span>

<span data-ttu-id="ce476-181">Met deze functie maakt u schermafbeeldingen van de stappen die zijn uitgevoerd tijdens de taakregistratie.</span><span class="sxs-lookup"><span data-stu-id="ce476-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="ce476-182">Als u deze functie wilt gebruiken, opent u het bestand **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en wijzigt u de waarde van het volgende element van **false** in **true**.</span><span class="sxs-lookup"><span data-stu-id="ce476-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="ce476-183">Onder **C:\\Users\\\<Gebruikersnaam\>\\AppData\\Roaming\\regressionTool\\playback** wordt een aparte map gemaakt voor elke testcase die wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ce476-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Map voor momentopnamen voor een testcase](./media/use_rsa_tool_12.png)

<span data-ttu-id="ce476-185">In al deze mappen vindt u momentopnamen van de stappen die tijdens het uitvoeren van de testcases zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ce476-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Momentopnamebestanden](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="ce476-187">Toewijzing</span><span class="sxs-lookup"><span data-stu-id="ce476-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="ce476-188">Scenario</span><span class="sxs-lookup"><span data-stu-id="ce476-188">Scenario</span></span>

1. <span data-ttu-id="ce476-189">De productontwerper maakt een nieuw vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="ce476-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="ce476-190">De productiemanager initieert een productieorder om het voorraadniveau naar twee stuks te brengen.</span><span class="sxs-lookup"><span data-stu-id="ce476-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="ce476-191">De productie wordt gestart, de productieorder wordt beëindigd en er wordt gecontroleerd of de voorhanden hoeveelheid uit twee stuks bestaat.</span><span class="sxs-lookup"><span data-stu-id="ce476-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="ce476-192">Het verkoopteam ontvangt een order voor vier stuks van het nieuwe product.</span><span class="sxs-lookup"><span data-stu-id="ce476-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="ce476-193">Daarom werkt het verkoopteam de nettobehoeften bij via het dynamische plan.</span><span class="sxs-lookup"><span data-stu-id="ce476-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="ce476-194">Omdat er geen extra capaciteit beschikbaar is, wordt het standaardorderbeleid ingesteld op kopen in plaats van maken.</span><span class="sxs-lookup"><span data-stu-id="ce476-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="ce476-195">Daarom wordt een geplande inkooporder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ce476-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="ce476-196">De koper voegt een leverancier toe, fiatteert de geplande inkooporder en bevestigt vervolgens de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="ce476-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="ce476-197">Wanneer de gekochte goederen in de winkel arriveren, zoekt de winkeloperator de bijbehorende inkooporder en ontvangt hij/zij de goederen.</span><span class="sxs-lookup"><span data-stu-id="ce476-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="ce476-198">Omdat de order nu is voltooid, kunnen goederen worden verzameld en verpakt op basis van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="ce476-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="ce476-199">In Financiën worden de inkoop- en verkoopfactuur geboekt.</span><span class="sxs-lookup"><span data-stu-id="ce476-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="ce476-200">In de volgende afbeelding wordt de stroom voor dit scenario weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-200">The following illustration shows the flow for this scenario.</span></span>

![Stroom voor het demoscenario](./media/use_rsa_tool_14.png)

<span data-ttu-id="ce476-202">In de volgende afbeelding ziet u de bedrijfsprocessen voor dit scenario in RSAT.</span><span class="sxs-lookup"><span data-stu-id="ce476-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Bedrijfsprocessen voor het demoscenario](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="ce476-204">Strategie – Belangrijkste trainingspunten</span><span class="sxs-lookup"><span data-stu-id="ce476-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="ce476-205">Gegevens</span><span class="sxs-lookup"><span data-stu-id="ce476-205">Data</span></span>

- <span data-ttu-id="ce476-206">Zorg ervoor dat u over representatieve gegevensvolumes (een kopie van productie-/gouden configuratiegegevens plus gemigreerde gegevens) beschikt.</span><span class="sxs-lookup"><span data-stu-id="ce476-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="ce476-207">Wanneer u nieuwe gegevens genereert via Taakregistratie, maakt u testnamen die niet conflicteren met bestaande namen (gebruik bijvoorbeeld een voorvoegsel zoals **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="ce476-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="ce476-208">Gebruik Tijdgebonden herstel in Azure om tests in omgevingen zonder Tier 1 opnieuw uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="ce476-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="ce476-209">Hoewel u de Excel-functies **WILLEKEURIG** en **NU** kunt gebruiken om een unieke combinatie te genereren, is dit redelijk veel werk.</span><span class="sxs-lookup"><span data-stu-id="ce476-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="ce476-210">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="ce476-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="ce476-211">Taakregistratie</span><span class="sxs-lookup"><span data-stu-id="ce476-211">Task recorder</span></span>

- <span data-ttu-id="ce476-212">Definieer scenario's voordat u begint met registreren.</span><span class="sxs-lookup"><span data-stu-id="ce476-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="ce476-213">Een goed beheerd project bevat vooraf gedefinieerde testscenario's.</span><span class="sxs-lookup"><span data-stu-id="ce476-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="ce476-214">Als u een testcase wilt maken, moet u overwegen hoe voorspelbaar het resultaat van die testscenario's is.</span><span class="sxs-lookup"><span data-stu-id="ce476-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="ce476-215">Splits opnamen als deze door verschillende rollen worden uitgevoerd of als er wachttijd of een externe gebeurtenis vóór de volgende stap is.</span><span class="sxs-lookup"><span data-stu-id="ce476-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="ce476-216">Vermijd het selecteren van waarden in lijsten.</span><span class="sxs-lookup"><span data-stu-id="ce476-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="ce476-217">Gebruik in plaats daarvan tekstindelingen, zoals **FIFO**, **AudioRM** en **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="ce476-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="ce476-218">Wanneer u een waarde selecteert in een lijst, wordt de positie van de waarde in de lijst vastgelegd, niet de waarde zelf.</span><span class="sxs-lookup"><span data-stu-id="ce476-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="ce476-219">Als er artikelen aan de lijst worden toegevoegd, kan de positie van de waarde veranderen.</span><span class="sxs-lookup"><span data-stu-id="ce476-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="ce476-220">Daarom gebruikt uw registratie een andere parameter en kan dit gevolgen hebben voor de rest van het scenario.</span><span class="sxs-lookup"><span data-stu-id="ce476-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="ce476-221">Denk aan het gedrag van meerdere gebruikers.</span><span class="sxs-lookup"><span data-stu-id="ce476-221">Think about multi-user behavior.</span></span> <span data-ttu-id="ce476-222">Ga er bijvoorbeeld niet vanuit dat uw nieuwe verkooporder altijd automatisch wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ce476-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="ce476-223">Gebruik in plaats daarvan altijd het filter om de juiste order te vinden.</span><span class="sxs-lookup"><span data-stu-id="ce476-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="ce476-224">Gebruik de functie Kopiëren in Taakregistratie om de naam van een nieuw product op te slaan, zodat het kan worden gebruikt in aaneengeschakelde testcases.</span><span class="sxs-lookup"><span data-stu-id="ce476-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="ce476-225">Gebruik de functie Valideren in Taakregistratie om controlepunten in te stellen om te controleren of stappen correct zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ce476-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="ce476-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="ce476-226">RSAT</span></span>

- <span data-ttu-id="ce476-227">Als u de test in een ander bedrijf wilt uitvoeren, kunt u het bedrijf wijzigen op het tabblad **Algemeen** van het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ce476-228">Controleer of instellingen en gegevens beschikbaar zijn in het geselecteerde bedrijf.</span><span class="sxs-lookup"><span data-stu-id="ce476-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="ce476-229">U kunt de testgebruiker wijzigen op het tabblad **Algemeen** van het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ce476-230">Geef de e-mail-id op van de gebruiker die de testcase uitvoert.</span><span class="sxs-lookup"><span data-stu-id="ce476-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="ce476-231">Op deze manier kan de testcase worden uitgevoerd met behulp van de beveiligingsmachtigingen van de opgegeven gebruiker.</span><span class="sxs-lookup"><span data-stu-id="ce476-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="ce476-232">Als u wilt wachten voordat de test wordt gestart, kunt u een pauze definiëren op het tabblad **Algemeen** van het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ce476-233">Deze pauze kan worden gebruikt in een batchtaak (bijvoorbeeld als een workflow moet worden uitgevoerd voordat de volgende stap kan worden uitgevoerd.)</span><span class="sxs-lookup"><span data-stu-id="ce476-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="ce476-234">Geavanceerde scripts</span><span class="sxs-lookup"><span data-stu-id="ce476-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="ce476-235">CLI</span><span class="sxs-lookup"><span data-stu-id="ce476-235">CLI</span></span>

<span data-ttu-id="ce476-236">RSAT kan worden aangeroepen vanuit een **opdrachtprompt**- of **PowerShell**-venster.</span><span class="sxs-lookup"><span data-stu-id="ce476-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="ce476-237">Controleer of de omgevingsvariabele **TestRoot** is ingesteld op het installatiepad van RSAT.</span><span class="sxs-lookup"><span data-stu-id="ce476-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="ce476-238">(In Microsoft Windows opent u **Configuratiescherm**, selecteert u **Systeem en beveiliging \> Systeem \> Geavanceerde systeeminstellingen** en **Omgevingsvariabelen**.)</span><span class="sxs-lookup"><span data-stu-id="ce476-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="ce476-239">Open een **opdrachtprompt**- of **PowerShell**-venster en typ het volgende als beheerder.</span><span class="sxs-lookup"><span data-stu-id="ce476-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="ce476-240">Ga naar de installatiedirectory van RSAT.</span><span class="sxs-lookup"><span data-stu-id="ce476-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="ce476-241">Geef alle opdrachten weer.</span><span class="sxs-lookup"><span data-stu-id="ce476-241">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="ce476-242">?</span><span class="sxs-lookup"><span data-stu-id="ce476-242">?</span></span> 
<span data-ttu-id="ce476-243">Hiermee wordt Help weergegeven over alle beschikbare opdrachten en de bijbehorende parameters.</span><span class="sxs-lookup"><span data-stu-id="ce476-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="ce476-244">Optionele parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="ce476-245">Waarbij ``[command]`` een van de opdrachten is die hieronder zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="ce476-246">about</span><span class="sxs-lookup"><span data-stu-id="ce476-246">about</span></span>
<span data-ttu-id="ce476-247">Hiermee wordt de huidige versie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="ce476-248">cls</span><span class="sxs-lookup"><span data-stu-id="ce476-248">cls</span></span>
<span data-ttu-id="ce476-249">Hiermee wordt het scherm leeggemaakt.</span><span class="sxs-lookup"><span data-stu-id="ce476-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="ce476-250">download</span><span class="sxs-lookup"><span data-stu-id="ce476-250">download</span></span>
<span data-ttu-id="ce476-251">Hiermee worden bijlagen voor de opgegeven testaanvraag gedownload naar de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="ce476-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="ce476-252">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="ce476-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ce476-253">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ce476-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-254">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-254">Required parameters</span></span>
<span data-ttu-id="ce476-255">**``test_case_id``** Vertegenwoordigt de id van de testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ce476-256">**``output_dir``** Vertegenwoordigt de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="ce476-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ce476-257">De map moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-258">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="ce476-259">edit</span><span class="sxs-lookup"><span data-stu-id="ce476-259">edit</span></span>
<span data-ttu-id="ce476-260">Hiermee kunt u het parameterbestand openen in Excel en het bewerken.</span><span class="sxs-lookup"><span data-stu-id="ce476-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-261">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-261">Required parameters</span></span>
<span data-ttu-id="ce476-262">**``excel_file``** Moet een volledig pad naar een bestaand Excel-bestand bevatten.</span><span class="sxs-lookup"><span data-stu-id="ce476-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-263">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="ce476-264">generate</span><span class="sxs-lookup"><span data-stu-id="ce476-264">generate</span></span>
<span data-ttu-id="ce476-265">Hiermee worden testuitvoerings- en parameterbestanden gegenereerd voor de opgegeven testcase in de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="ce476-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="ce476-266">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="ce476-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ce476-267">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ce476-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-268">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-268">Required parameters</span></span>
<span data-ttu-id="ce476-269">**``test_case_id``** Vertegenwoordigt de id van de testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ce476-270">**``output_dir``** Vertegenwoordigt de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="ce476-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ce476-271">De map moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-272">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="ce476-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="ce476-273">generatederived</span></span>
<span data-ttu-id="ce476-274">Hiermee wordt een nieuwe testcase gegenereerd die is afgeleid van de geleverde testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="ce476-275">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="ce476-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ce476-276">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ce476-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-277">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-277">Required parameters</span></span>
<span data-ttu-id="ce476-278">**``parent_test_case_id``** Vertegenwoordigt de id van de bovenligende testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="ce476-279">**``test_plan_id``** Vertegenwoordigt de id van het testplan.</span><span class="sxs-lookup"><span data-stu-id="ce476-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="ce476-280">**``test_suite_id``** Vertegenwoordigt de id van de testsuite.</span><span class="sxs-lookup"><span data-stu-id="ce476-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-281">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="ce476-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="ce476-282">generatetestonly</span></span>
<span data-ttu-id="ce476-283">Hiermee wordt alleen een testuitvoeringsbestand voor de opgegeven testcase gegenereerd in de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="ce476-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="ce476-284">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="ce476-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ce476-285">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ce476-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-286">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-286">Required parameters</span></span>
<span data-ttu-id="ce476-287">**``test_case_id``** Vertegenwoordigt de id van de testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ce476-288">**``output_dir``** Vertegenwoordigt de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="ce476-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ce476-289">De map moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-290">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="ce476-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="ce476-291">generatetestsuite</span></span>
<span data-ttu-id="ce476-292">Hiermee worden alle testcases voor de opgegeven suite gegenereerd in de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="ce476-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="ce476-293">U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen.</span><span class="sxs-lookup"><span data-stu-id="ce476-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="ce476-294">Gebruik een willekeurige waarde uit de kolom als parameter voor **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="ce476-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-295">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-295">Required parameters</span></span>
<span data-ttu-id="ce476-296">**``test_suite_name``** Vertegenwoordigt de naam van de testsuite.</span><span class="sxs-lookup"><span data-stu-id="ce476-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="ce476-297">**``output_dir``** Vertegenwoordigt de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="ce476-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ce476-298">De map moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-299">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="ce476-300">help</span><span class="sxs-lookup"><span data-stu-id="ce476-300">help</span></span>
<span data-ttu-id="ce476-301">Identiek aan de [?](####?)</span><span class="sxs-lookup"><span data-stu-id="ce476-301">Identical to the [?](####?)</span></span> <span data-ttu-id="ce476-302">opdracht</span><span class="sxs-lookup"><span data-stu-id="ce476-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="ce476-303">list</span><span class="sxs-lookup"><span data-stu-id="ce476-303">list</span></span>
<span data-ttu-id="ce476-304">Hiermee worden alle beschikbare testcases weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="ce476-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="ce476-305">listtestplans</span></span>
<span data-ttu-id="ce476-306">Hiermee worden alle beschikbare testplannen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="ce476-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="ce476-307">listtestsuite</span></span>
<span data-ttu-id="ce476-308">Hiermee worden de testcases voor de opgegeven testsuite weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="ce476-309">U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen.</span><span class="sxs-lookup"><span data-stu-id="ce476-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="ce476-310">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="ce476-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-311">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-311">Required parameters</span></span>
<span data-ttu-id="ce476-312">**``suite_name``** Naam van de gewenste suite.</span><span class="sxs-lookup"><span data-stu-id="ce476-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-313">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="ce476-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="ce476-314">listtestsuitenames</span></span>
<span data-ttu-id="ce476-315">Hiermee worden alle beschikbare testsuites weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ce476-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="ce476-316">playback</span><span class="sxs-lookup"><span data-stu-id="ce476-316">playback</span></span>
<span data-ttu-id="ce476-317">Hiermee wordt een testcase afgespeeld met een Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-318">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-318">Required parameters</span></span>
<span data-ttu-id="ce476-319">**``excel_file``** Een volledig pad naar het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="ce476-320">Bestand moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="ce476-321">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="ce476-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="ce476-322">playbackbyid</span></span>
<span data-ttu-id="ce476-323">Hiermee worden meerdere testcases tegelijk afgespeeld.</span><span class="sxs-lookup"><span data-stu-id="ce476-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="ce476-324">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="ce476-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ce476-325">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="ce476-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-326">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-326">Required parameters</span></span>
<span data-ttu-id="ce476-327">**``test_case_id1``** Id van bestaande testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="ce476-328">**``test_case_id2``** Id van bestaande testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="ce476-329">**``test_case_idN``** Id van bestaande testcase.</span><span class="sxs-lookup"><span data-stu-id="ce476-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="ce476-330">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="ce476-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="ce476-331">playbackmany</span></span>
<span data-ttu-id="ce476-332">Hiermee wordt een groot aantal testcases tegelijk afgespeeld met Excel-bestanden.</span><span class="sxs-lookup"><span data-stu-id="ce476-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-333">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-333">Required parameters</span></span>
<span data-ttu-id="ce476-334">**``excel_file1``** Volledig pad naar het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="ce476-335">Bestand moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-335">File must exist.</span></span>  
<span data-ttu-id="ce476-336">**``excel_file2``** Volledig pad naar het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="ce476-337">Bestand moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-337">File must exist.</span></span>  
<span data-ttu-id="ce476-338">**``excel_fileN``** Volledig pad naar het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="ce476-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="ce476-339">Bestand moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="ce476-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="ce476-340">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="ce476-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="ce476-341">playbacksuite</span></span>
<span data-ttu-id="ce476-342">Hiermee worden alle testcases uit de opgegeven testsuite afgespeeld.</span><span class="sxs-lookup"><span data-stu-id="ce476-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="ce476-343">U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen.</span><span class="sxs-lookup"><span data-stu-id="ce476-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="ce476-344">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="ce476-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-345">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-345">Required parameters</span></span>
<span data-ttu-id="ce476-346">**``suite_name``** Naam van de gewenste suite.</span><span class="sxs-lookup"><span data-stu-id="ce476-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-347">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="ce476-348">quit</span><span class="sxs-lookup"><span data-stu-id="ce476-348">quit</span></span>
<span data-ttu-id="ce476-349">Hiermee wordt de toepassing gesloten.</span><span class="sxs-lookup"><span data-stu-id="ce476-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="ce476-350">upload</span><span class="sxs-lookup"><span data-stu-id="ce476-350">upload</span></span>
<span data-ttu-id="ce476-351">Hiermee worden alle bestanden geüpload die bij de opgegeven testsuite of testcases horen.</span><span class="sxs-lookup"><span data-stu-id="ce476-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="ce476-352">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-352">Required parameters</span></span>
<span data-ttu-id="ce476-353">**``suite_name``** Alle bestanden die bij de opgegeven testsuite of testcases horen worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="ce476-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="ce476-354">**``testcase_id``** Alle bestanden die bij de opgegeven testcase(s) horen worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="ce476-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-355">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="ce476-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="ce476-356">uploadrecording</span></span>
<span data-ttu-id="ce476-357">Hiermee worden alleen opnamebestanden geüpload die bij de opgegeven testcases horen.</span><span class="sxs-lookup"><span data-stu-id="ce476-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="ce476-358">Vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="ce476-358">Required parameters</span></span>
<span data-ttu-id="ce476-359">**``testcase_id``** Opnamebestanden die bij de opgegeven testcases horen worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="ce476-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="ce476-360">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="ce476-361">usage</span><span class="sxs-lookup"><span data-stu-id="ce476-361">usage</span></span>
<span data-ttu-id="ce476-362">Hiermee worden twee manieren weergegeven om deze toepassing aan te roepen: een waarbij gebruik wordt gemaakt van een standaard instellingsbestand en een andere waarbij een instellingsbestand wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="ce476-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="ce476-363">Windows PowerShell-voorbeelden</span><span class="sxs-lookup"><span data-stu-id="ce476-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="ce476-364">Een testcase uitvoeren in een lus</span><span class="sxs-lookup"><span data-stu-id="ce476-364">Run a test case in a loop</span></span>

<span data-ttu-id="ce476-365">U hebt een testscript waarmee u een nieuwe klant kunt maken.</span><span class="sxs-lookup"><span data-stu-id="ce476-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="ce476-366">Via scripts kan deze testcase in een lus worden uitgevoerd door de volgende gegevens in willekeurige volgorde te zetten voordat elke iteratie wordt uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="ce476-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="ce476-367">Klant-ID</span><span class="sxs-lookup"><span data-stu-id="ce476-367">Customer ID</span></span>
- <span data-ttu-id="ce476-368">Klantnaam</span><span class="sxs-lookup"><span data-stu-id="ce476-368">Customer name</span></span>
- <span data-ttu-id="ce476-369">Klantadres</span><span class="sxs-lookup"><span data-stu-id="ce476-369">Customer address</span></span>

<span data-ttu-id="ce476-370">De klant-id heeft de notatie *ATCUS\<nummer\>*, waarbij \<nummer\> voor een waarde tussen **000000001** en **999999999** staat.</span><span class="sxs-lookup"><span data-stu-id="ce476-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="ce476-371">In het volgende voorbeeld wordt één parameter, **start**, gebruikt om het eerste nummer te definiëren dat wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ce476-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="ce476-372">Er wordt een tweede parameter, **nr**, gebruikt om het aantal klanten te definiëren dat moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ce476-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="ce476-373">Voor elke iteratie worden de parameters in het Excel-parameterbestand gewijzigd met behulp van een UpdateCustomer-functie.</span><span class="sxs-lookup"><span data-stu-id="ce476-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="ce476-374">Vervolgens wordt de RSAT-opdrachtregel aangeroepen in een RunTestCase-functie.</span><span class="sxs-lookup"><span data-stu-id="ce476-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="ce476-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in de beheermodus en plak de volgende code in het venster met de naam **Untitled1. ps1**.</span><span class="sxs-lookup"><span data-stu-id="ce476-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="ce476-376">Een script uitvoeren dat afhankelijk is van gegevens in Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ce476-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="ce476-377">In het volgende voorbeeld wordt een OData-aanroep (Open Data Protocol) gebruikt om de orderstatus van een inkooporder te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ce476-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="ce476-378">Als de status niet **gefactureerd** is, kunt u bijvoorbeeld een RSAT-testcase aanroepen waarmee de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="ce476-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
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
