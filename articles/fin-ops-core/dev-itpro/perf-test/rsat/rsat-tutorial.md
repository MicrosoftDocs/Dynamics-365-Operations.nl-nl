---
title: Zelfstudie voor Regression Suite Automation Tool
description: In dit onderwerp wordt beschreven hoe u het hulpprogramma RSAT (Regression Suite Automation Tool) kunt gebruiken. Verschillende functies worden beschreven en u krijgt voorbeelden te zien waarin geavanceerde scripts worden gebruikt.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 5a9f19168093f24a7f152b2b5b23b3728ca80222
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745160"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="1bf62-104">Zelfstudie voor Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="1bf62-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1bf62-105">Gebruik uw internetbrowser om deze pagina als PDF-bestand te downloaden en op te slaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="1bf62-106">Deze zelfstudie doorloopt enkele van de geavanceerde functies van RSAT, bevat een demotoewijzing en een beschrijving van de strategie en belangrijke trainingspunten.</span><span class="sxs-lookup"><span data-stu-id="1bf62-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="1bf62-107">De belangrijkste functies van RSAT en taakregistratie</span><span class="sxs-lookup"><span data-stu-id="1bf62-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="1bf62-108">Een veldwaarde valideren</span><span class="sxs-lookup"><span data-stu-id="1bf62-108">Validate a field value</span></span>

<span data-ttu-id="1bf62-109">Met RSAT kunt u validatiestappen in uw testaanvraag opnemen om de verwachte waarden te valideren.</span><span class="sxs-lookup"><span data-stu-id="1bf62-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="1bf62-110">Zie het artikel [Verwachte waarden valideren](rsat-validate-expected.md) voor meer informatie over deze functie.</span><span class="sxs-lookup"><span data-stu-id="1bf62-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="1bf62-111">In het volgende voorbeeld ziet u hoe u deze functie kunt gebruiken om te valideren of de voorhanden voorraad groter is dan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="1bf62-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="1bf62-112">Maak in de demogegevens in het bedrijf **USMF** een taakregistratie met de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="1bf62-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="1bf62-113">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="1bf62-114">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="1bf62-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1bf62-115">Filter bijvoorbeeld op het veld **Artikelnummer** met een waarde van **1000**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="1bf62-116">Selecteer **Voorhanden voorraad**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="1bf62-117">Gebruik de snelfilter om records te zoeken.</span><span class="sxs-lookup"><span data-stu-id="1bf62-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1bf62-118">Filter bijvoorbeeld op het veld **Vestiging** met een waarde van **1**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="1bf62-119">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="1bf62-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="1bf62-120">Valideer of het veld **Totaal beschikbaar** de waarde **411,0000000000000000** bevat.</span><span class="sxs-lookup"><span data-stu-id="1bf62-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="1bf62-121">Sla de taakregistratie op als een **ontwikkelaarsregistratie** en koppel deze aan uw testcase in de Azure Devops.</span><span class="sxs-lookup"><span data-stu-id="1bf62-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="1bf62-122">Voeg de testcase toe aan het testplan en laad de testcase in RSAT.</span><span class="sxs-lookup"><span data-stu-id="1bf62-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="1bf62-123">Open het Excel-parameterbestand en ga naar het tabblad **TestCaseSteps**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="1bf62-124">Als u wilt valideren of de voorhanden voorraad altijd meer dan **0** is, gaat u naar de stap **Totaal beschikbaar valideren** en wijzigt u de waarde van **411** in **0**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="1bf62-125">Wijzig de waarde van het veld **Operator** van een is gelijk-teken (**=**) naar een groter dan-teken (**\>**).</span><span class="sxs-lookup"><span data-stu-id="1bf62-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="1bf62-126">Sla het Excel-parameterbestand op en sluit het.</span><span class="sxs-lookup"><span data-stu-id="1bf62-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="1bf62-127">Selecteer **Uploaden** om de wijzigingen die u in het Excel-parameterbestand hebt aangebracht op te slaan in Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="1bf62-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="1bf62-128">Als de waarde van het veld **Totaal beschikbaar** voor het opgegeven artikel in voorraad groter is dan 0 (nul), slagen de tests, ongeacht de werkelijke waarde voor voorhanden voorraad.</span><span class="sxs-lookup"><span data-stu-id="1bf62-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="1bf62-129">Opgeslagen variabelen en aaneenschakeling van testcases</span><span class="sxs-lookup"><span data-stu-id="1bf62-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="1bf62-130">Eén van de belangrijkste functies van RSAT is dat testcases kunnen worden aaneengeschakeld, dat wil zeggen dat variabelen kunnen worden doorgegeven aan andere tests.</span><span class="sxs-lookup"><span data-stu-id="1bf62-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="1bf62-131">Zie het artikel [Variabelen kopiëren om testcases aaneen te schakelen](rsat-chain-test-cases.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1bf62-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="1bf62-132">Afgeleide testcase</span><span class="sxs-lookup"><span data-stu-id="1bf62-132">Derived test case</span></span>

<span data-ttu-id="1bf62-133">Met RSAT kunt u dezelfde taakregistratie gebruiken met meerdere testcases, zodat een taak kan worden uitgevoerd met verschillende gegevensconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="1bf62-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="1bf62-134">Zie het artikel [Afgeleide testcases](rsat-derived-test-cases.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1bf62-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="1bf62-135">Meldingen en berichten valideren</span><span class="sxs-lookup"><span data-stu-id="1bf62-135">Validate notifications and messages</span></span>

<span data-ttu-id="1bf62-136">Deze functie kan worden gebruikt om te controleren of een actie is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1bf62-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="1bf62-137">Als er bijvoorbeeld een productieorder is gemaakt, is geschat en vervolgens is gestart, wordt in de app het bericht 'Productie – begin' weergegeven om aan te geven dat de productieorder is gestart.</span><span class="sxs-lookup"><span data-stu-id="1bf62-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![De melding Productie - begin](./media/use_rsa_tool_05.png)

<span data-ttu-id="1bf62-139">U kunt dit bericht valideren via RSAT door de berichttekst in te voeren op het tabblad **MessageValidation** van het Excel-parameterbestand voor de desbetreffende registratie.</span><span class="sxs-lookup"><span data-stu-id="1bf62-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Het tabblad Berichtvalidatie](./media/use_rsa_tool_06.png)

<span data-ttu-id="1bf62-141">Nadat de testcase is uitgevoerd, wordt het bericht in het Excel-parameterbestand vergeleken met het bericht dat wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1bf62-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="1bf62-142">Als de berichten niet overeenkomen, mislukt de testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="1bf62-143">U kunt meer dan één bericht invoeren op het tabblad **MessageValidation** in het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="1bf62-144">In plaats van informatieve berichten kunnen de berichten ook fout- of waarschuwingsberichten zijn.</span><span class="sxs-lookup"><span data-stu-id="1bf62-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="1bf62-145">Momentopname</span><span class="sxs-lookup"><span data-stu-id="1bf62-145">Snapshot</span></span>

<span data-ttu-id="1bf62-146">Met deze functie maakt u schermafbeeldingen van de stappen die zijn uitgevoerd tijdens de taakregistratie.</span><span class="sxs-lookup"><span data-stu-id="1bf62-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="1bf62-147">Het is handig voor het controleren of debuggen van problemen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="1bf62-148">Als u deze functie wilt gebruiken, opent u het bestand **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** onder de RSAT-installatiemap (bijvoorbeeld **C:\\Program Files (x86)\\Regression Suite Automation Tool**) en wijzigt u de waarde van het volgende element van **false** in **true**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="1bf62-149">Wanneer de testaanvraag wordt uitgevoerd, genereert RSAT momentopnamen (installatiekopieën) van de afgespeelde stappen in de map voor testcases in de werkdirectory.</span><span class="sxs-lookup"><span data-stu-id="1bf62-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="1bf62-150">Als u een oudere versie van RSAT gebruikt, worden de afbeeldingen opgeslagen in **C:\\Gebruikers\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** en er wordt een aparte map gemaakt voor elke testaanvraag die wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1bf62-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="1bf62-151">Toewijzing</span><span class="sxs-lookup"><span data-stu-id="1bf62-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="1bf62-152">Scenario's</span><span class="sxs-lookup"><span data-stu-id="1bf62-152">Scenario</span></span>

1. <span data-ttu-id="1bf62-153">De productontwerper maakt een nieuw vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="1bf62-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="1bf62-154">De productiemanager initieert een productieorder om het voorraadniveau naar twee stuks te brengen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="1bf62-155">De productie wordt gestart, de productieorder wordt beëindigd en er wordt gecontroleerd of de voorhanden hoeveelheid uit twee stuks bestaat.</span><span class="sxs-lookup"><span data-stu-id="1bf62-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="1bf62-156">Het verkoopteam ontvangt een order voor vier stuks van het nieuwe product.</span><span class="sxs-lookup"><span data-stu-id="1bf62-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="1bf62-157">Daarom werkt het verkoopteam de nettobehoeften bij via het dynamische plan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="1bf62-158">Omdat er geen extra capaciteit beschikbaar is, wordt het standaardorderbeleid ingesteld op kopen in plaats van maken.</span><span class="sxs-lookup"><span data-stu-id="1bf62-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="1bf62-159">Daarom wordt een geplande inkooporder gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1bf62-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="1bf62-160">De koper voegt een leverancier toe, fiatteert de geplande inkooporder en bevestigt vervolgens de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="1bf62-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="1bf62-161">Wanneer de gekochte goederen in de winkel arriveren, zoekt de winkeloperator de bijbehorende inkooporder en ontvangt hij/zij de goederen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="1bf62-162">Omdat de order nu is voltooid, kunnen goederen worden verzameld en verpakt op basis van de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="1bf62-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="1bf62-163">In Financiën worden de inkoop- en verkoopfactuur geboekt.</span><span class="sxs-lookup"><span data-stu-id="1bf62-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="1bf62-164">In de volgende afbeelding wordt de stroom voor dit scenario weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1bf62-164">The following illustration shows the flow for this scenario.</span></span>

![Stroom voor het demoscenario](./media/use_rsa_tool_14.png)

<span data-ttu-id="1bf62-166">In de volgende afbeelding wordt de hiërarchie van bedrijfsprocessen voor dit scenario weergegeven in de LCS Modelleertool bedrijfsprocessen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Bedrijfsprocessen voor het demoscenario](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="1bf62-168">Strategie – Belangrijkste trainingspunten</span><span class="sxs-lookup"><span data-stu-id="1bf62-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="1bf62-169">Gegevens</span><span class="sxs-lookup"><span data-stu-id="1bf62-169">Data</span></span>

- <span data-ttu-id="1bf62-170">Zorg ervoor dat u over representatieve gegevensvolumes (een kopie van productie-/gouden configuratiegegevens plus gemigreerde gegevens) beschikt.</span><span class="sxs-lookup"><span data-stu-id="1bf62-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="1bf62-171">Wanneer u nieuwe gegevens genereert via Taakregistratie, maakt u testnamen die niet conflicteren met bestaande namen (gebruik bijvoorbeeld een voorvoegsel zoals **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="1bf62-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="1bf62-172">Gebruik Tijdgebonden herstel in Azure om tests in omgevingen zonder Tier 1 opnieuw uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="1bf62-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="1bf62-173">Hoewel u de Excel-functies **WILLEKEURIG** en **NU** kunt gebruiken om een unieke combinatie te genereren, is dit redelijk veel werk.</span><span class="sxs-lookup"><span data-stu-id="1bf62-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="1bf62-174">Hier volgt een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="1bf62-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="1bf62-175">Taakregistratie</span><span class="sxs-lookup"><span data-stu-id="1bf62-175">Task recorder</span></span>

- <span data-ttu-id="1bf62-176">Definieer scenario's voordat u begint met registreren.</span><span class="sxs-lookup"><span data-stu-id="1bf62-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="1bf62-177">Een goed beheerd project bevat vooraf gedefinieerde testscenario's.</span><span class="sxs-lookup"><span data-stu-id="1bf62-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="1bf62-178">Als u een testcase wilt maken, moet u overwegen hoe voorspelbaar het resultaat van die testscenario's is.</span><span class="sxs-lookup"><span data-stu-id="1bf62-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="1bf62-179">Splits opnamen als deze door verschillende rollen worden uitgevoerd of als er wachttijd of een externe gebeurtenis vóór de volgende stap is.</span><span class="sxs-lookup"><span data-stu-id="1bf62-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="1bf62-180">Vermijd het selecteren van waarden in lijsten.</span><span class="sxs-lookup"><span data-stu-id="1bf62-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="1bf62-181">Gebruik in plaats daarvan tekstindelingen, zoals **FIFO**, **AudioRM** en **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="1bf62-182">Wanneer u een waarde selecteert in een lijst, wordt de positie van de waarde in de lijst vastgelegd, niet de waarde zelf.</span><span class="sxs-lookup"><span data-stu-id="1bf62-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="1bf62-183">Als er artikelen aan de lijst worden toegevoegd, kan de positie van de waarde veranderen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="1bf62-184">Daarom gebruikt uw registratie een andere parameter en kan dit gevolgen hebben voor de rest van het scenario.</span><span class="sxs-lookup"><span data-stu-id="1bf62-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="1bf62-185">Denk aan het gedrag van meerdere gebruikers.</span><span class="sxs-lookup"><span data-stu-id="1bf62-185">Think about multi-user behavior.</span></span> <span data-ttu-id="1bf62-186">Ga er bijvoorbeeld niet vanuit dat uw nieuwe verkooporder altijd automatisch wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1bf62-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="1bf62-187">Gebruik in plaats daarvan altijd het filter om de juiste order te vinden.</span><span class="sxs-lookup"><span data-stu-id="1bf62-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="1bf62-188">Gebruik de functie Kopiëren in Taakregistratie om de naam van een nieuw product op te slaan, zodat het kan worden gebruikt in aaneengeschakelde testcases.</span><span class="sxs-lookup"><span data-stu-id="1bf62-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="1bf62-189">Gebruik de functie Valideren in Taakregistratie om controlepunten in te stellen om te controleren of stappen correct zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1bf62-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="1bf62-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="1bf62-190">RSAT</span></span>

- <span data-ttu-id="1bf62-191">Als u de test in een ander bedrijf wilt uitvoeren, kunt u het bedrijf wijzigen op het tabblad **Algemeen** van het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="1bf62-192">Controleer of instellingen en gegevens beschikbaar zijn in het geselecteerde bedrijf.</span><span class="sxs-lookup"><span data-stu-id="1bf62-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="1bf62-193">U kunt de testgebruiker wijzigen op het tabblad **Algemeen** van het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="1bf62-194">Geef de e-mail-id op van de gebruiker die de testcase uitvoert.</span><span class="sxs-lookup"><span data-stu-id="1bf62-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="1bf62-195">Op deze manier kan de testcase worden uitgevoerd met behulp van de beveiligingsmachtigingen van de opgegeven gebruiker.</span><span class="sxs-lookup"><span data-stu-id="1bf62-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="1bf62-196">Als u wilt wachten voordat de test wordt gestart, kunt u een pauze definiëren op het tabblad **Algemeen** van het Excel-parameterbestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="1bf62-197">Deze pauze kan worden gebruikt in een batchtaak (bijvoorbeeld als een workflow moet worden uitgevoerd voordat de volgende stap kan worden uitgevoerd.)</span><span class="sxs-lookup"><span data-stu-id="1bf62-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="1bf62-198">Geavanceerde scripts</span><span class="sxs-lookup"><span data-stu-id="1bf62-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="1bf62-199">CLI</span><span class="sxs-lookup"><span data-stu-id="1bf62-199">CLI</span></span>

<span data-ttu-id="1bf62-200">RSAT kan worden aangeroepen vanuit een **opdrachtprompt**- of **PowerShell**-venster.</span><span class="sxs-lookup"><span data-stu-id="1bf62-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="1bf62-201">Controleer of de omgevingsvariabele **TestRoot** is ingesteld op het installatiepad van RSAT.</span><span class="sxs-lookup"><span data-stu-id="1bf62-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="1bf62-202">(In Microsoft Windows opent u **Configuratiescherm**, selecteert u **Systeem en beveiliging \> Systeem \> Geavanceerde systeeminstellingen** en **Omgevingsvariabelen**.)</span><span class="sxs-lookup"><span data-stu-id="1bf62-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="1bf62-203">Open een **opdrachtprompt**- of **PowerShell**-venster en typ het volgende als beheerder.</span><span class="sxs-lookup"><span data-stu-id="1bf62-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="1bf62-204">Ga naar de installatiedirectory van RSAT.</span><span class="sxs-lookup"><span data-stu-id="1bf62-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="1bf62-205">Geef alle opdrachten weer.</span><span class="sxs-lookup"><span data-stu-id="1bf62-205">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="1bf62-206">?</span><span class="sxs-lookup"><span data-stu-id="1bf62-206">?</span></span>

<span data-ttu-id="1bf62-207">Hiermee wordt Help weergegeven over alle beschikbare opdrachten en de bijbehorende parameters.</span><span class="sxs-lookup"><span data-stu-id="1bf62-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="1bf62-208">?: optionele parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-208">?: Optional parameters</span></span>

<span data-ttu-id="1bf62-209">`command`: waarbij ``[command]`` een van de hieronder opgegeven opdrachten is.</span><span class="sxs-lookup"><span data-stu-id="1bf62-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="1bf62-210">informatie</span><span class="sxs-lookup"><span data-stu-id="1bf62-210">about</span></span>

<span data-ttu-id="1bf62-211">Hiermee wordt de huidige versie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1bf62-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="1bf62-212">cls</span><span class="sxs-lookup"><span data-stu-id="1bf62-212">cls</span></span>

<span data-ttu-id="1bf62-213">Hiermee wordt het scherm leeggemaakt.</span><span class="sxs-lookup"><span data-stu-id="1bf62-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="1bf62-214">download</span><span class="sxs-lookup"><span data-stu-id="1bf62-214">download</span></span>

<span data-ttu-id="1bf62-215">Hiermee worden bijlagen voor de opgegeven testaanvraag gedownload naar de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="1bf62-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="1bf62-216">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1bf62-217">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="1bf62-218">download: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-218">download: required parameters</span></span>

+ <span data-ttu-id="1bf62-219">`test_case_id`: vertegenwoordigt de id van de testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="1bf62-220">`output_dir`: vertegenwoordigt de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="1bf62-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="1bf62-221">De map moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="1bf62-222">download: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="1bf62-223">bewerken</span><span class="sxs-lookup"><span data-stu-id="1bf62-223">edit</span></span>

<span data-ttu-id="1bf62-224">Hiermee kunt u het parameterbestand openen in Excel en het bewerken.</span><span class="sxs-lookup"><span data-stu-id="1bf62-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="1bf62-225">edit: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-225">edit: required parameters</span></span>

+ <span data-ttu-id="1bf62-226">`excel_file`: moet een volledig pad naar een bestaand Excel-bestand bevatten.</span><span class="sxs-lookup"><span data-stu-id="1bf62-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="1bf62-227">edit: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="1bf62-228">generate</span><span class="sxs-lookup"><span data-stu-id="1bf62-228">generate</span></span>

<span data-ttu-id="1bf62-229">Hiermee worden testuitvoerings- en parameterbestanden gegenereerd voor de opgegeven testcase in de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="1bf62-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="1bf62-230">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1bf62-231">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="1bf62-232">generate: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-232">generate: required parameters</span></span>

+ <span data-ttu-id="1bf62-233">`test_case_id`: vertegenwoordigt de id van de testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="1bf62-234">`output_dir`: vertegenwoordigt de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="1bf62-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="1bf62-235">De map moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="1bf62-236">generate: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="1bf62-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="1bf62-237">generatederived</span></span>

<span data-ttu-id="1bf62-238">Hiermee wordt een nieuwe testcase gegenereerd die is afgeleid van de geleverde testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="1bf62-239">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1bf62-240">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="1bf62-241">generatederived: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="1bf62-242">`parent_test_case_id`: vertegenwoordigt de id van de bovenliggende testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="1bf62-243">`test_plan_id`: vertegenwoordigt de id van het testplan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="1bf62-244">`test_suite_id`: vertegenwoordigt de id van de testsuite.</span><span class="sxs-lookup"><span data-stu-id="1bf62-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="1bf62-245">generatederived: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="1bf62-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="1bf62-246">generatetestonly</span></span>

<span data-ttu-id="1bf62-247">Hiermee wordt alleen een testuitvoeringsbestand voor de opgegeven testcase gegenereerd in de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="1bf62-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="1bf62-248">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1bf62-249">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="1bf62-250">generatetestonly: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="1bf62-251">`test_case_id`: vertegenwoordigt de id van de testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="1bf62-252">`output_dir`: vertegenwoordigt de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="1bf62-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="1bf62-253">De map moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="1bf62-254">generatetestonly: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="1bf62-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="1bf62-255">generatetestsuite</span></span>

<span data-ttu-id="1bf62-256">Hiermee worden alle testcases voor de opgegeven suite gegenereerd in de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="1bf62-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="1bf62-257">U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="1bf62-258">Gebruik een willekeurige waarde uit de kolom als parameter voor **test_suite_name**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="1bf62-259">generatetestsuite: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="1bf62-260">`test_suite_name`: vertegenwoordigt de naam van de testsuite.</span><span class="sxs-lookup"><span data-stu-id="1bf62-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="1bf62-261">`output_dir`: vertegenwoordigt de uitvoermap.</span><span class="sxs-lookup"><span data-stu-id="1bf62-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="1bf62-262">De map moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="1bf62-263">generatetestsuite: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="1bf62-264">help</span><span class="sxs-lookup"><span data-stu-id="1bf62-264">help</span></span>

<span data-ttu-id="1bf62-265">Identiek aan de [?](#section)</span><span class="sxs-lookup"><span data-stu-id="1bf62-265">Identical to the [?](#section)</span></span> <span data-ttu-id="1bf62-266">command.</span><span class="sxs-lookup"><span data-stu-id="1bf62-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="1bf62-267">lijst</span><span class="sxs-lookup"><span data-stu-id="1bf62-267">list</span></span>

<span data-ttu-id="1bf62-268">Hiermee worden alle beschikbare testcases weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1bf62-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="1bf62-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="1bf62-269">listtestplans</span></span>

<span data-ttu-id="1bf62-270">Hiermee worden alle beschikbare testplannen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1bf62-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="1bf62-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="1bf62-271">listtestsuite</span></span>

<span data-ttu-id="1bf62-272">Hiermee worden de testcases voor de opgegeven testsuite weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1bf62-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="1bf62-273">U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="1bf62-274">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="1bf62-275">listtestsuite: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="1bf62-276">`suite_name`: naam van de gewenste suite.</span><span class="sxs-lookup"><span data-stu-id="1bf62-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="1bf62-277">listtestsuite: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="1bf62-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="1bf62-278">listtestsuitenames</span></span>

<span data-ttu-id="1bf62-279">Hiermee worden alle beschikbare testsuites weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1bf62-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="1bf62-280">playback</span><span class="sxs-lookup"><span data-stu-id="1bf62-280">playback</span></span>

<span data-ttu-id="1bf62-281">Hiermee wordt een testcase afgespeeld met een Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="1bf62-282">playback: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-282">playback: required parameters</span></span>

+ <span data-ttu-id="1bf62-283">`excel_file`: een volledig pad naar het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="1bf62-284">Bestand moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="1bf62-285">playback: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="1bf62-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="1bf62-286">playbackbyid</span></span>

<span data-ttu-id="1bf62-287">Hiermee worden meerdere testcases tegelijk afgespeeld.</span><span class="sxs-lookup"><span data-stu-id="1bf62-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="1bf62-288">U kunt de opdracht ``list`` gebruiken om alle beschikbare testcases op te halen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="1bf62-289">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **test_case_id**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="1bf62-290">playbackbyid: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="1bf62-291">`test_case_id1`: id van bestaande testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="1bf62-292">`test_case_id2`: id van bestaande testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="1bf62-293">`test_case_idN`: id van bestaande testcase.</span><span class="sxs-lookup"><span data-stu-id="1bf62-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="1bf62-294">playbackbyid: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="1bf62-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="1bf62-295">playbackmany</span></span>

<span data-ttu-id="1bf62-296">Hiermee wordt een groot aantal testcases tegelijk afgespeeld met Excel-bestanden.</span><span class="sxs-lookup"><span data-stu-id="1bf62-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="1bf62-297">playbackmany: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="1bf62-298">`excel_file1`: volledig pad naar het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="1bf62-299">Bestand moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-299">File must exist.</span></span>
+ <span data-ttu-id="1bf62-300">`excel_file2`: volledig pad naar het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="1bf62-301">Bestand moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-301">File must exist.</span></span>
+ <span data-ttu-id="1bf62-302">`excel_fileN`: volledig pad naar het Excel-bestand.</span><span class="sxs-lookup"><span data-stu-id="1bf62-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="1bf62-303">Bestand moet bestaan.</span><span class="sxs-lookup"><span data-stu-id="1bf62-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="1bf62-304">playbackmany: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="1bf62-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="1bf62-305">playbacksuite</span></span>

<span data-ttu-id="1bf62-306">Hiermee worden alle testcases uit de opgegeven testsuite afgespeeld.</span><span class="sxs-lookup"><span data-stu-id="1bf62-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="1bf62-307">U kunt de opdracht ``listtestsuitenames`` gebruiken om alle beschikbare testsuites op te halen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="1bf62-308">Gebruik een willekeurige waarde uit de eerste kolom als parameter voor **suite_name**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="1bf62-309">playbacksuite: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="1bf62-310">`suite_name`: naam van de gewenste suite.</span><span class="sxs-lookup"><span data-stu-id="1bf62-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="1bf62-311">playbacksuite: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="1bf62-312">quit</span><span class="sxs-lookup"><span data-stu-id="1bf62-312">quit</span></span>

<span data-ttu-id="1bf62-313">Hiermee wordt de toepassing gesloten.</span><span class="sxs-lookup"><span data-stu-id="1bf62-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="1bf62-314">upload</span><span class="sxs-lookup"><span data-stu-id="1bf62-314">upload</span></span>

<span data-ttu-id="1bf62-315">Hiermee worden alle bestanden geüpload die bij de opgegeven testsuite of testcases horen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="1bf62-316">upload: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-316">upload: required parameters</span></span>

+ <span data-ttu-id="1bf62-317">`suite_name`: alle bestanden die bij de opgegeven testsuite of testcases horen, worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="1bf62-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="1bf62-318">`testcase_id`: alle bestanden die bij de opgegeven testcase(s) horen, worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="1bf62-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="1bf62-319">upload: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="1bf62-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="1bf62-320">uploadrecording</span></span>

<span data-ttu-id="1bf62-321">Hiermee worden alleen opnamebestanden geüpload die bij de opgegeven testcases horen.</span><span class="sxs-lookup"><span data-stu-id="1bf62-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="1bf62-322">uploadrecording: vereiste parameters</span><span class="sxs-lookup"><span data-stu-id="1bf62-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="1bf62-323">`testcase_id`: opnamebestand dat bij de opgegeven testcases hoort, wordt geüpload.</span><span class="sxs-lookup"><span data-stu-id="1bf62-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="1bf62-324">uploadrecording: voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="1bf62-325">usage</span><span class="sxs-lookup"><span data-stu-id="1bf62-325">usage</span></span>

<span data-ttu-id="1bf62-326">Hiermee worden twee manieren weergegeven om deze toepassing aan te roepen: een waarbij gebruik wordt gemaakt van een standaard instellingsbestand en een andere waarbij een instellingsbestand wordt geleverd.</span><span class="sxs-lookup"><span data-stu-id="1bf62-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="1bf62-327">Windows PowerShell-voorbeelden</span><span class="sxs-lookup"><span data-stu-id="1bf62-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="1bf62-328">Een testcase uitvoeren in een lus</span><span class="sxs-lookup"><span data-stu-id="1bf62-328">Run a test case in a loop</span></span>

<span data-ttu-id="1bf62-329">U hebt een testscript waarmee u een nieuwe klant kunt maken.</span><span class="sxs-lookup"><span data-stu-id="1bf62-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="1bf62-330">Via scripts kan deze testcase in een lus worden uitgevoerd door de volgende gegevens in willekeurige volgorde te zetten voordat elke iteratie wordt uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="1bf62-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="1bf62-331">Klant-ID</span><span class="sxs-lookup"><span data-stu-id="1bf62-331">Customer ID</span></span>
- <span data-ttu-id="1bf62-332">Klantnaam</span><span class="sxs-lookup"><span data-stu-id="1bf62-332">Customer name</span></span>
- <span data-ttu-id="1bf62-333">Klantadres</span><span class="sxs-lookup"><span data-stu-id="1bf62-333">Customer address</span></span>

<span data-ttu-id="1bf62-334">De klant-id heeft de notatie *ATCUS\<number\>*, waarbij \<number\> voor een waarde tussen **000000001** en **999999999** staat.</span><span class="sxs-lookup"><span data-stu-id="1bf62-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="1bf62-335">In het volgende voorbeeld wordt één parameter, **start**, gebruikt om het eerste nummer te definiëren dat wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1bf62-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="1bf62-336">Er wordt een tweede parameter, **nr**, gebruikt om het aantal klanten te definiëren dat moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1bf62-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="1bf62-337">Voor elke iteratie worden de parameters in het Excel-parameterbestand gewijzigd met behulp van een UpdateCustomer-functie.</span><span class="sxs-lookup"><span data-stu-id="1bf62-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="1bf62-338">Vervolgens wordt de RSAT-opdrachtregel aangeroepen in een RunTestCase-functie.</span><span class="sxs-lookup"><span data-stu-id="1bf62-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="1bf62-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in de beheermodus en plak de volgende code in het venster met de naam **Untitled1. ps1**.</span><span class="sxs-lookup"><span data-stu-id="1bf62-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="1bf62-340">Een script uitvoeren dat afhankelijk is van gegevens in Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="1bf62-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="1bf62-341">In het volgende voorbeeld wordt een OData-aanroep (Open Data Protocol) gebruikt om de orderstatus van een inkooporder te zoeken.</span><span class="sxs-lookup"><span data-stu-id="1bf62-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="1bf62-342">Als de status niet **gefactureerd** is, kunt u bijvoorbeeld een RSAT-testcase aanroepen waarmee de factuur wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="1bf62-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]