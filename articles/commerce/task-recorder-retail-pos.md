---
title: Taakrecorder en Help voor Retail Modern POS (MPOS) en Cloud POS
description: In dit onderwerp wordt beschreven hoe u Taakrecorder gebruikt in Retail Modern POS en Cloud POS.
author: mugunthanm
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02e8bb1bfb088a877ef23b7a81982868700f4ae2
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028102"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="649dd-103">Taakrecorder en Help voor Retail Modern POS (MPOS) en Cloud POS</span><span class="sxs-lookup"><span data-stu-id="649dd-103">Task recorder and Help for Retail Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="649dd-104">In dit onderwerp wordt beschreven hoe u Taakrecorder gebruikt in Retail Modern POS en Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="649dd-104">This topic describes how to use Task recorder in Retail Modern POS and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="649dd-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="649dd-105">Overview</span></span>

<span data-ttu-id="649dd-106">Taakrecorder in Retail Modern POS of Cloud POS is een nieuwe oplossing die is gemaakt met het oog op hoge responsiviteit.</span><span class="sxs-lookup"><span data-stu-id="649dd-106">Task recorder in Retail Modern POS or Cloud POS is a new solution that was built with a focus on high responsiveness.</span></span> <span data-ttu-id="649dd-107">Het biedt een flexibele Application Programming Interface (API) voor uitbreidbaarheid en naadloze integratie met gebruikers van zakelijke procesregistraties.</span><span class="sxs-lookup"><span data-stu-id="649dd-107">It provides a flexible application programming interface (API) for extensibility and seamless integration with consumers of business process recordings.</span></span> <span data-ttu-id="649dd-108">Bovendien is integratie van Taakrecorder met het hulpprogramma Business process modeller (BPM) in Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) verbeterd.</span><span class="sxs-lookup"><span data-stu-id="649dd-108">Additionally, Task recorder integration with the Business process modeler (BPM) tool on Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) has been brought forward.</span></span> <span data-ttu-id="649dd-109">Daarom kunnen gebruikers doorgaan met het produceren van uitgebreide bedrijfsprocesdiagrammen van registraties om hun toepassingen te analyseren en te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="649dd-109">Therefore, users can continue to produce rich business process diagrams from recordings to analyze and design their applications.</span></span>

## <a name="architecture"></a><span data-ttu-id="649dd-110">Architectuur</span><span class="sxs-lookup"><span data-stu-id="649dd-110">Architecture</span></span>

<span data-ttu-id="649dd-111">Taakrecorder kan gebruikersacties in de client registreren met exacte betrouwbaarheid.</span><span class="sxs-lookup"><span data-stu-id="649dd-111">Task recorder can record user actions in the client with exact fidelity.</span></span> <span data-ttu-id="649dd-112">Elk besturingselement wordt ontworpen om Taakrecorder te informeren over de uitvoering van een gebruikersactie.</span><span class="sxs-lookup"><span data-stu-id="649dd-112">Each control is instrumented to notify Task recorder about the execution of a user action.</span></span> <span data-ttu-id="649dd-113">Het besturingselement informeert Taakrecorder dat een gebeurtenis heeft plaatsgevonden en geeft alle relevante informatie over de bijbehorende gebruikersactie in real-time door.</span><span class="sxs-lookup"><span data-stu-id="649dd-113">The control notifies Task recorder that an event occurred and passes along all pertinent information about the corresponding user action in real time.</span></span> <span data-ttu-id="649dd-114">Met deze informatie kan Taakrecorder het soort gebruikersactie vastleggen (zoals een klik op een knop, waarde-invoer of navigatie) en alle gegevens die zijn gerelateerd aan de gebruikersactie (zoals de ingevoerde gegevenswaarde en -type, de formuliercontext of de recordcontext).</span><span class="sxs-lookup"><span data-stu-id="649dd-114">From this information, Task recorder can capture the type of user action (such as a button click, value entry, or navigation) and any data that is related to the user action (such as the input data value and type, form context, or record context).</span></span> <span data-ttu-id="649dd-115">Taakrecorder behoudt de informatie met voldoende details om te garanderen dat als de registratie wordt afgespeeld, de gebruikersacties exact zo worden afgespeeld als de gebruiker ze heeft uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="649dd-115">Task recorder persists the information with enough detail to help guarantee that a playback of the recording can perform the recorded actions exactly as the user performed them.</span></span> <span data-ttu-id="649dd-116">(De functie voor het afspelen is nog niet geïmplementeerd in Retail Modern POS of Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="649dd-116">(The playback feature isn't yet implemented at Retail modern POS or Cloud POS.)</span></span>

## <a name="basic-configuration"></a><span data-ttu-id="649dd-117">Basisconfiguratie</span><span class="sxs-lookup"><span data-stu-id="649dd-117">Basic configuration</span></span>

<span data-ttu-id="649dd-118">Ga als volgt te werk om taakregistratie in POS in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="649dd-118">To enable task recording in POS, follow these steps.</span></span>

1. <span data-ttu-id="649dd-119">Klik op **Detailhandel en commerce** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **Kassa's**.</span><span class="sxs-lookup"><span data-stu-id="649dd-119">Click **Retail and Commerce** &gt; **Channel Setup** &gt; **POS Setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="649dd-120">Klik op de kassa om taakregistratie in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="649dd-120">Click the register to enable task recording on.</span></span>
3. <span data-ttu-id="649dd-121">Stel op het tabblad **Registreren** op het sneltabblad **Algemeen** de optie **Taakregistratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="649dd-121">On the **Register** tab, on the **General** FastTab, set the **Enable task recording** option to **Yes**.</span></span>
4. <span data-ttu-id="649dd-122">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="649dd-122">Click **Save**.</span></span>
5. <span data-ttu-id="649dd-123">Ga naar **Retail en Commerce** &gt; **Retail en Commerce IT** &gt; **Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="649dd-123">Go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="649dd-124">Selecteer de taak **1090, kassa's** en klik vervolgens op **Nu uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="649dd-124">Select the **Registers (1090)** job, and then click **Run now**.</span></span>

## <a name="create-a-recording"></a><span data-ttu-id="649dd-125">Een registratie maken</span><span class="sxs-lookup"><span data-stu-id="649dd-125">Create a recording</span></span>

<span data-ttu-id="649dd-126">Volg deze stappen om een nieuwe registratie te maken met Taakrecorder.</span><span class="sxs-lookup"><span data-stu-id="649dd-126">Follow these steps to create a new recording using Task recorder.</span></span>

1. <span data-ttu-id="649dd-127">Start Retail Modern POS of Cloud POS en meld u aan.</span><span class="sxs-lookup"><span data-stu-id="649dd-127">Start Retail Modern POS or Cloud POS, and sign in.</span></span>
2. <span data-ttu-id="649dd-128">Klik op de pagina **Instellingen** in het gedeelte **Taakrecorder** op **Taakregistratie openen**.</span><span class="sxs-lookup"><span data-stu-id="649dd-128">On the **Settings** page, in the **Task Recorder** section, click **Open task recorder**.</span></span> <span data-ttu-id="649dd-129">Het deelvenster **Taakrecorder** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="649dd-129">The **Task recorder** pane appears.</span></span> <span data-ttu-id="649dd-130">U kunt klikken op de knop **Sluiten** (**X**) in de rechterbovenhoek om het deelvenster **Taakrecorder** te sluiten voordat u een nieuwe registratie start.</span><span class="sxs-lookup"><span data-stu-id="649dd-130">You can click the **Close** button (**X**) in the upper-right corner to close the **Task recorder** pane before you begin a new recording.</span></span> <span data-ttu-id="649dd-131">Als u het deelvenster weer wilt openen, herhaalt u stap 2.</span><span class="sxs-lookup"><span data-stu-id="649dd-131">To reopen the pane, repeat step 2.</span></span>

    <span data-ttu-id="649dd-132">[![Deelvenster Taakrecorder](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span><span class="sxs-lookup"><span data-stu-id="649dd-132">[![Task recorder pane](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)</span></span>

3. <span data-ttu-id="649dd-133">Voer een naam en omschrijving voor de registratie in en klik vervolgens op **Start**.</span><span class="sxs-lookup"><span data-stu-id="649dd-133">Enter a name and description for the recording, and then click **Start**.</span></span> <span data-ttu-id="649dd-134">De registratiesessie begint zodra u klikt op **Start**.</span><span class="sxs-lookup"><span data-stu-id="649dd-134">The recording session begins as soon as you click **Start**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="649dd-135">Als u op de knop **Sluiten** (**X**) in de rechterbovenhoek klikt terwijl de registratie wordt uitgevoerd, wordt het deelvenster **Taakrecorder** gesloten, maar wordt de registratiesessie niet beëindigd.</span><span class="sxs-lookup"><span data-stu-id="649dd-135">If you click the **Close** button (**X**) in the upper-right corner while recording is in progress, the **Task recorder** pane is closed, but the recording session isn't ended.</span></span> <span data-ttu-id="649dd-136">Klik op de knop **Help** (vraagteken) boven aan het scherm om het deelvenster Taakrecorder weer te openen.</span><span class="sxs-lookup"><span data-stu-id="649dd-136">To reopen the Task recorder pane, click the **Help** button (question mark) at the top of the screen.</span></span>
    >
    > <span data-ttu-id="649dd-137">[![Vraagteken](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="649dd-137">[![Question mark](./media/help.jpg)](./media/help.jpg)</span></span>

4. <span data-ttu-id="649dd-138">Nadat u op **Starten** hebt geklikt, gaat Taakrecorder in de registratiemodus.</span><span class="sxs-lookup"><span data-stu-id="649dd-138">After you click **Start**, Task recorder enters recording mode.</span></span> <span data-ttu-id="649dd-139">Het deelvenster **Taakrecorder** bevat informatie en besturingselementen die zijn gerelateerd aan het registratieproces.</span><span class="sxs-lookup"><span data-stu-id="649dd-139">The **Task recorder** pane shows information and controls that are related to the recording process.</span></span>
5. <span data-ttu-id="649dd-140">Voer de acties uit die u wilt uitvoeren in de interface (UI) van Retail Modern POS of Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="649dd-140">Perform the actions that you want to perform in the Retail Modern POS or Cloud POS user interface (UI).</span></span>
6. <span data-ttu-id="649dd-141">Als u de registratiesessie wilt beëindigen, klikt u op **Stoppen**.</span><span class="sxs-lookup"><span data-stu-id="649dd-141">To end the recording session, click **Stop**.</span></span>

## <a name="download-options"></a><span data-ttu-id="649dd-142">Opties voor downloaden</span><span class="sxs-lookup"><span data-stu-id="649dd-142">Download options</span></span>

<span data-ttu-id="649dd-143">Nadat u de registratiesessie hebt beëindigd, worden verschillende opties weergegeven, zodat u uw registratie kunt downloaden.</span><span class="sxs-lookup"><span data-stu-id="649dd-143">After you end the recording session, several options are shown, so that you can download your recording.</span></span>

<span data-ttu-id="649dd-144">[![Opties voor downloaden](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span><span class="sxs-lookup"><span data-stu-id="649dd-144">[![Download options](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)</span></span>

### <a name="save-to-this-pc"></a><span data-ttu-id="649dd-145">Opslaan op deze pc</span><span class="sxs-lookup"><span data-stu-id="649dd-145">Save to this PC</span></span>

<span data-ttu-id="649dd-146">U kunt het registratiepakket gebruiken om een taakbegeleiding af te spelen, de registratie te onderhouden of de aantekeningen in de registratie te bewerken.</span><span class="sxs-lookup"><span data-stu-id="649dd-146">You can use the recording package to play a Task guide, maintain the recording, or edit the annotations in the recording.</span></span> <span data-ttu-id="649dd-147">(Deze functie is nog niet geïmplementeerd in Retail Modern POS of Cloud POS.)</span><span class="sxs-lookup"><span data-stu-id="649dd-147">(This feature isn't yet implemented in Retail Modern POS and Cloud POS.)</span></span>

### <a name="export-as-word-document"></a><span data-ttu-id="649dd-148">Exporteren als Word-document</span><span class="sxs-lookup"><span data-stu-id="649dd-148">Export as Word document</span></span>

<span data-ttu-id="649dd-149">U kunt de registratie opslaan als Microsoft Word-document.</span><span class="sxs-lookup"><span data-stu-id="649dd-149">You can save the recording as a Microsoft Word document.</span></span> <span data-ttu-id="649dd-150">Het document bevat de geregistreerde stappen en de schermopnamen die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="649dd-150">The document will contain the recorded steps and the screenshots that were captured.</span></span>

### <a name="save-as-developer-recording"></a><span data-ttu-id="649dd-151">Opslaan als ontwikkelaarsregistratie</span><span class="sxs-lookup"><span data-stu-id="649dd-151">Save as developer recording</span></span>

<span data-ttu-id="649dd-152">Het ruwe registratiebestand is nuttig voor ontwikkelaarsscenario's, zoals het genereren van testcode.</span><span class="sxs-lookup"><span data-stu-id="649dd-152">The raw recording file will be useful for developer scenarios such as test code generation.</span></span> <span data-ttu-id="649dd-153">(Deze functie is niet nog geïmplementeerd.)</span><span class="sxs-lookup"><span data-stu-id="649dd-153">(This feature isn't yet implemented.)</span></span>

## <a name="recording-controls"></a><span data-ttu-id="649dd-154">Besturingselementen voor registratie</span><span class="sxs-lookup"><span data-stu-id="649dd-154">Recording controls</span></span>

<span data-ttu-id="649dd-155">[![Besturingselementen voor registratie](./media/controls.jpg)](./media/controls.jpg)</span><span class="sxs-lookup"><span data-stu-id="649dd-155">[![Recording controls](./media/controls.jpg)](./media/controls.jpg)</span></span>

### <a name="stop"></a><span data-ttu-id="649dd-156">Stoppen</span><span class="sxs-lookup"><span data-stu-id="649dd-156">Stop</span></span>

<span data-ttu-id="649dd-157">Als u de registratiesessie wilt beëindigen, klikt u op **Stoppen**.</span><span class="sxs-lookup"><span data-stu-id="649dd-157">Click **Stop** to end the recording session.</span></span> <span data-ttu-id="649dd-158">Houd er rekening mee dat u een sessie na het beëindigen ervan niet opnieuw kunt starten.</span><span class="sxs-lookup"><span data-stu-id="649dd-158">Note that you can't restart a session after you end it.</span></span> <span data-ttu-id="649dd-159">Zorg er daarom voor dat de registratie is voltooid voordat u deze beëindigt.</span><span class="sxs-lookup"><span data-stu-id="649dd-159">Therefore, make sure that the recording is completed before you end it.</span></span>

### <a name="pause"></a><span data-ttu-id="649dd-160">Pauze</span><span class="sxs-lookup"><span data-stu-id="649dd-160">Pause</span></span>

<span data-ttu-id="649dd-161">Klik op **Onderbreken** om de registratiesessie tijdelijk te stoppen (pauzeren) en ga door met de bewerking.</span><span class="sxs-lookup"><span data-stu-id="649dd-161">Click **Pause** to temporarily stop (pause) the recording session and continue with the operation.</span></span> <span data-ttu-id="649dd-162">Stappen die u uitvoert nadat u op **Onderbreken** hebt geklikt, worden niet geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="649dd-162">Steps that you perform after you click **Pause** aren't recorded.</span></span>

### <a name="continue"></a><span data-ttu-id="649dd-163">Doorgaan</span><span class="sxs-lookup"><span data-stu-id="649dd-163">Continue</span></span>

<span data-ttu-id="649dd-164">Als u de opnamesessie wilt hervatten nadat u deze hebt onderbroken, klikt u op **Doorgaan**.</span><span class="sxs-lookup"><span data-stu-id="649dd-164">To resume the recording session after you've paused it, click **Continue**.</span></span>

### <a name="capture-screenshots"></a><span data-ttu-id="649dd-165">Schermopnamen maken</span><span class="sxs-lookup"><span data-stu-id="649dd-165">Capture screenshots</span></span>

<span data-ttu-id="649dd-166">Taakrecorder kan schermopnamen maken van de gebruikersinterface van Retail Modern POS, terwijl u een bedrijfsproces registreert.</span><span class="sxs-lookup"><span data-stu-id="649dd-166">Task recorder can capture screenshots of the Retail Modern POS UI as you record a business process.</span></span> <span data-ttu-id="649dd-167">Als u de functie voor het maken van schermopnamen wilt inschakelen, stelt u de optie **Schermopnamen maken** in op **Ja** en maakt u de opname.</span><span class="sxs-lookup"><span data-stu-id="649dd-167">To turn on the screenshot capture feature, set the **Capture screenshot** option to **Yes** and then make the recording.</span></span> <span data-ttu-id="649dd-168">Zodra de opname is voltooid, klikt u op **Stoppen** en downloadt u het Word-document.</span><span class="sxs-lookup"><span data-stu-id="649dd-168">Once the recording is completed, click **Stop** and download the Word document.</span></span> <span data-ttu-id="649dd-169">Het document bevat de stappen met relevante schermafbeeldingen.</span><span class="sxs-lookup"><span data-stu-id="649dd-169">The document will contain the steps with relevant screenshots.</span></span>

> [!NOTE]
> <span data-ttu-id="649dd-170">Functionaliteit voor het maken van schermopnamen wordt niet ondersteund in Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="649dd-170">Capture screenshot functionality is not supported in Cloud POS.</span></span>

### <a name="start-task-and-end-task"></a><span data-ttu-id="649dd-171">Taak starten en taak beëindigen</span><span class="sxs-lookup"><span data-stu-id="649dd-171">Start task and End task</span></span>

<span data-ttu-id="649dd-172">U kunt het begin en einde van een set gegroepeerde stappen opgeven met behulp van de knoppen **Taak starten** en **Taak** **beëindigen**.</span><span class="sxs-lookup"><span data-stu-id="649dd-172">You can specify the beginning and end of a set of grouped steps by using the **Start task** and **End** **task** buttons.</span></span> <span data-ttu-id="649dd-173">Klik op **Taak starten** om een taak 'Taak starten' toe te voegen en voer vervolgens de stappen uit die in de groep moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="649dd-173">Click **Start task** to add a "Start Task" step, and then perform the steps that should be included in the group.</span></span> <span data-ttu-id="649dd-174">Als u klaar bent met het uitvoeren van de stappen voor de groep, klikt u op **Taak beëindigen**.</span><span class="sxs-lookup"><span data-stu-id="649dd-174">After you've finished performing the steps for the group, click **End task**.</span></span> <span data-ttu-id="649dd-175">Taken helpen u uw procedures te organiseren.</span><span class="sxs-lookup"><span data-stu-id="649dd-175">Tasks help you organize your procedures.</span></span> <span data-ttu-id="649dd-176">Taken kunnen worden genest binnen andere taken.</span><span class="sxs-lookup"><span data-stu-id="649dd-176">Tasks can be nested within other tasks.</span></span> <span data-ttu-id="649dd-177">Zo kunt u zeer lange en complexe bedrijfsprocessen beter organiseren.</span><span class="sxs-lookup"><span data-stu-id="649dd-177">In this way, you can better organize very long and complex business processes.</span></span>

## <a name="adding-annotations"></a><span data-ttu-id="649dd-178">Aantekeningen toevoegen</span><span class="sxs-lookup"><span data-stu-id="649dd-178">Adding annotations</span></span>

<span data-ttu-id="649dd-179">Een aantekening is aanvullende tekst die u aan een stap in een registratie kunt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="649dd-179">An annotation is additional text that you add to a step in a recording.</span></span> <span data-ttu-id="649dd-180">U kunt bijvoorbeeld aantekeningen gebruiken om de gebruiker meer context of instructies te geven.</span><span class="sxs-lookup"><span data-stu-id="649dd-180">For example, you can use annotations to give the user more context or instructions.</span></span> <span data-ttu-id="649dd-181">U kunt aantekeningen toevoegen vóór of na een stap.</span><span class="sxs-lookup"><span data-stu-id="649dd-181">You can add annotations before or after a step.</span></span> <span data-ttu-id="649dd-182">U kunt een aantekening aan iedere stap toevoegen door te klikken op de knop **Bewerken** (potloodsymbool), rechts van de stap.</span><span class="sxs-lookup"><span data-stu-id="649dd-182">You can add an annotation to any step by clicking the **Edit** button (pencil symbol) to the right of the step.</span></span>

<span data-ttu-id="649dd-183">[![Knop Bewerken voor een stap](./media/annotate.jpg)](./media/annotate.jpg)</span><span class="sxs-lookup"><span data-stu-id="649dd-183">[![Edit button for a step](./media/annotate.jpg)](./media/annotate.jpg)</span></span>

### <a name="texts-and-notes"></a><span data-ttu-id="649dd-184">Tekst en notities</span><span class="sxs-lookup"><span data-stu-id="649dd-184">Texts and notes</span></span>

<span data-ttu-id="649dd-185">U kunt de velden **Teksten** en **Notities** gebruiken om tekst toe te voegen die moet worden gekoppeld aan een stap in een taakbegeleiding.</span><span class="sxs-lookup"><span data-stu-id="649dd-185">You can use the **Texts** and **Notes** fields to add text that should be associated with a step in a Task guide.</span></span>

<span data-ttu-id="649dd-186">[![Tekst- en notitievelden](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span><span class="sxs-lookup"><span data-stu-id="649dd-186">[![Text and Notes fields](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)</span></span>

#### <a name="text"></a><span data-ttu-id="649dd-187">Tekst</span><span class="sxs-lookup"><span data-stu-id="649dd-187">Text</span></span>

<span data-ttu-id="649dd-188">Tekst die u invoert in het veld **Tekst**, verschijnt *boven* de staptekst in de taakbegeleiding.</span><span class="sxs-lookup"><span data-stu-id="649dd-188">Text that you enter in the **Text** field appears *above* the step text in the Task guide.</span></span> <span data-ttu-id="649dd-189">Deze locatie is geschikt voor tekst die de gebruiker moet lezen voordat de gebruiker de stap voltooit.</span><span class="sxs-lookup"><span data-stu-id="649dd-189">This location is appropriate for text that you want the user to read before the user completes the step.</span></span>

#### <a name="notes"></a><span data-ttu-id="649dd-190">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="649dd-190">Notes</span></span>

<span data-ttu-id="649dd-191">Tekst die u invoert in het veld **Notities**, verschijnt *onder* de staptekst in de taakbegeleiding.</span><span class="sxs-lookup"><span data-stu-id="649dd-191">Text that you enter in the **Notes** field appears *below* the step text in the Task guide.</span></span> <span data-ttu-id="649dd-192">Als de gebruiker de tekst wil lezen, moet deze de staptekst in het pop-upvenster uitvouwen.</span><span class="sxs-lookup"><span data-stu-id="649dd-192">To read the note text, the user must expand the step text in the pop-up window.</span></span> <span data-ttu-id="649dd-193">Deze locatie is geschikt voor optionele tekst of andere informatie die van belang kan zijn voor de gebruiker, maar die de gebruiker niet hoeft te lezen om de actie te voltooien.</span><span class="sxs-lookup"><span data-stu-id="649dd-193">This location is appropriate for optional reading material or other information that might be useful to the user, but that the user doesn't require in order to complete the action.</span></span>

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a><span data-ttu-id="649dd-194">Help in Retail Modern POS en Cloud POS</span><span class="sxs-lookup"><span data-stu-id="649dd-194">Help in Retail Modern POS and Cloud POS</span></span>

<span data-ttu-id="649dd-195">Om uw eigen taakregistraties in het Help-deelvenster van Retail Modern POS en Cloud POS weer te geven zodat ze kunnen worden afgespeeld als taakbegeleidingen of als tekst, moet u uw taakregistraties opslaan in een BPM-bibliotheek, en de parameters van het Help-systeem bijwerken om naar uw BPM-bibliotheek te wijzen.</span><span class="sxs-lookup"><span data-stu-id="649dd-195">To show your own custom task recordings in the Help pane of Retail Modern POS and Cloud POS so that they can be viewed as text, you must save your task recordings to your own BPM library, and then update your Help system parameters to point to your BPM library.</span></span> <span data-ttu-id="649dd-196">Zie voor meer informatie het onderwerp [Verbinding maken met het Help-systeem.](../fin-ops-core/fin-ops/get-started/help-connect.md)</span><span class="sxs-lookup"><span data-stu-id="649dd-196">For more information, see [Connecting the Help system](../fin-ops-core/fin-ops/get-started/help-connect.md).</span></span> <span data-ttu-id="649dd-197">Retail Modern POS en Cloud POS Help doorzoekt LCS in real-time.</span><span class="sxs-lookup"><span data-stu-id="649dd-197">Retail Modern POS and Cloud POS Help searches LCS in real time.</span></span> <span data-ttu-id="649dd-198">Alle BPM-bibliotheken worden doorzocht die zijn geselecteerd in de parameters van het Commerce Help-systeem, en de relevante resultaten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="649dd-198">It searches across all the BPM libraries that are selected in the Commerce Help system parameters and shows the relevant results.</span></span> <span data-ttu-id="649dd-199">Voor toegang tot het menu **Help** klikt u op de knop **Help** (vraagteken) bovenaan het scherm, typt u vervolgens in het zoekvak uw procesnaam en klikt u op de zoekknop.</span><span class="sxs-lookup"><span data-stu-id="649dd-199">To access the **Help** menu, click the **Help** button (question mark) at the top of the screen and then in the search box type your process name and hit the search button.</span></span>

<span data-ttu-id="649dd-200">[![De knop Help](./media/help.jpg)](./media/help.jpg)</span><span class="sxs-lookup"><span data-stu-id="649dd-200">[![Help button](./media/help.jpg)](./media/help.jpg)</span></span>

<span data-ttu-id="649dd-201">Wanneer u op de taakbegeleiding in de zoekresultaten klikt, kunt u de stappen weergeven als een Help-onderwerp of een Word-document.</span><span class="sxs-lookup"><span data-stu-id="649dd-201">When you click a Task guide in the search results, you can either view the steps as a Help topic or export the steps to a Word document.</span></span>

> [!NOTE]
> <span data-ttu-id="649dd-202">Help in Retail Modern POS en Cloud POS opent geen taakbegeleiding op basis van het formulier waar u zich bevindt of de bewerking die u uitvoert.</span><span class="sxs-lookup"><span data-stu-id="649dd-202">Help in Retail Modern POS and Cloud POS will not bring up task guides according to what form you're on or operation you're doing.</span></span> <span data-ttu-id="649dd-203">U moet de procesnaam in het zoekvak typen en op **Zoeken** klikken.</span><span class="sxs-lookup"><span data-stu-id="649dd-203">You have to type the process name in the search box and then click **Search**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]