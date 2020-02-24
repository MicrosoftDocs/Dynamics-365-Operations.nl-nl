---
title: Geavanceerde formule-editor voor elektronische rapporten
description: In dit onderwerp wordt beschreven hoe de geavanceerde formule-editor kan worden gebruikt voor het configureren van expressies in ER-modeltoewijzing (elektronische rapportage) en indelingscomponenten.
author: NickSelin
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d183f77da1dda0c4f04e4e48ab3db0133f494a55
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015168"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="d91c9-103">Geavanceerde formule-editor voor elektronische rapporten</span><span class="sxs-lookup"><span data-stu-id="d91c9-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="d91c9-104">Behalve de [formule-editor](general-electronic-reporting-formula-designer.md) voor [elektronische rapportage](general-electronic-reporting.md) kunt u de geavanceerde formule-editor voor elektronische rapportage gebruiken om de ervaring voor het configureren van ER-expressies te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="d91c9-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="d91c9-105">De geavanceerde editor is op browsers gebaseerd en wordt aangedreven door de [Monaco](https://microsoft.github.io/monaco-editor)-editor.</span><span class="sxs-lookup"><span data-stu-id="d91c9-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="d91c9-106">De meest gebruikte functies van de geavanceerde editor worden in dit onderwerp beschreven:</span><span class="sxs-lookup"><span data-stu-id="d91c9-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="d91c9-107">Automatische codeopmaak</span><span class="sxs-lookup"><span data-stu-id="d91c9-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="d91c9-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="d91c9-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="d91c9-109">Codevoltooiing</span><span class="sxs-lookup"><span data-stu-id="d91c9-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="d91c9-110">Codenavigatie</span><span class="sxs-lookup"><span data-stu-id="d91c9-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="d91c9-111">Codestructurering</span><span class="sxs-lookup"><span data-stu-id="d91c9-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="d91c9-112">Zoeken en vervangen</span><span class="sxs-lookup"><span data-stu-id="d91c9-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="d91c9-113">Gegevens plakken</span><span class="sxs-lookup"><span data-stu-id="d91c9-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="d91c9-114">Inkleuring van syntaxis</span><span class="sxs-lookup"><span data-stu-id="d91c9-114">Syntax colorization</span></span>](#SyntaxColorization)

## <span data-ttu-id="d91c9-115"><a name="ActivateAdvEditor">De geavanceerde formule-editor activeren</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="d91c9-116">Voer de volgende stappen uit om de geavanceerde formule-editor te gebruiken in uw exemplaar van Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="d91c9-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="d91c9-117">Ga naar  **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d91c9-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="d91c9-118">Selecteer op de pagina **Configuraties** in het actiedeelvenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="d91c9-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="d91c9-119">Stel in het dialoogvenster **Gebruikersparameters** in de sectie **Uitvoeringstracering** de parameter **Geavanceerde formule-editor inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d91c9-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="d91c9-120">[![Pagina ER-configuraties](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="d91c9-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="d91c9-121">Houd er rekening mee dat deze parameter specifiek is voor de gebruiker en specifiek voor het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d91c9-121">Be aware that this parameter is user specific and company specific.</span></span>

## <span data-ttu-id="d91c9-122"><a name="Autoformatting">Automatische codeopmaak</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="d91c9-123">Wanneer u een complexe expressie schrijft die uit meerdere regels met code bestaat, wordt de inspringing van een nieuwe ingevoerde regel automatisch uitgevoerd op basis van de inspringing van de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="d91c9-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="d91c9-124">U kunt regels selecteren en de inspringing ervan wijzigen door **Tab** of **Shift+Tab** te typen.</span><span class="sxs-lookup"><span data-stu-id="d91c9-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="d91c9-125">[![ER-formule-editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="d91c9-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="d91c9-126">Met automatische opmaak kunt u de volledige expressie goed opgemaakt houden om verder onderhoud te vergemakkelijken en inzicht in de geconfigureerde logica te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="d91c9-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <span data-ttu-id="d91c9-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="d91c9-128">De editor biedt woordaanvulling om u te helpen bij het sneller schrijven van expressies en het voorkomen van typefouten.</span><span class="sxs-lookup"><span data-stu-id="d91c9-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="d91c9-129">Wanneer u nieuwe tekst gaat toevoegen, biedt de editor automatisch een lijst met functies die worden ondersteund in ER-functies die de tekens bevatten die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="d91c9-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="d91c9-130">U kunt IntelliSense ook op elke plaats in een geconfigureerde expressie activeren door **Ctrl+spatiebalk** te typen.</span><span class="sxs-lookup"><span data-stu-id="d91c9-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="d91c9-131">[![ER-formule-editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="d91c9-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <span data-ttu-id="d91c9-132"><a name="CodeCompletion">Codevoltooiing</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="d91c9-133">De editor zorgt er automatisch voor dat code wordt voltooid door:</span><span class="sxs-lookup"><span data-stu-id="d91c9-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="d91c9-134">Het invoegen van een haakje sluiten wanneer er een openingshaakje wordt ingevoerd, waarbij de cursor zich tussen de haakjes bevindt.</span><span class="sxs-lookup"><span data-stu-id="d91c9-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="d91c9-135">Het tweede aanhalingsteken invoegen wanneer het eerste wordt ingevoerd, waarbij de cursor binnen de aanhalingstekens blijft.</span><span class="sxs-lookup"><span data-stu-id="d91c9-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="d91c9-136">Het tweede dubbele aanhalingsteken invoegen wanneer het eerste wordt ingevoerd, waarbij de cursor binnen de aanhalingstekens blijft.</span><span class="sxs-lookup"><span data-stu-id="d91c9-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="d91c9-137">[![ER-formule-editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="d91c9-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="d91c9-138">Wanneer u naar het getypte haakje wijst, wordt het tweede haakje van dit paar automatisch gemarkeerd, zodat de constructie wordt weergegeven die ze ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d91c9-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <span data-ttu-id="d91c9-139"><a name="CodeNavigation">Codenavigatie</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="d91c9-140">U kunt de vereiste symbolen of regels in uw expressie vinden door de opdracht **Ga naar** te typen met het opdrachtpalet of het contextmenu.</span><span class="sxs-lookup"><span data-stu-id="d91c9-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="d91c9-141">Als u bijvoorbeeld naar regel **8**wilt gaan, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="d91c9-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="d91c9-142">Druk **op CTRL+G**, voer de waarde **8** in en druk op **ENTER**.</span><span class="sxs-lookup"><span data-stu-id="d91c9-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="d91c9-143">– of –</span><span class="sxs-lookup"><span data-stu-id="d91c9-143">-or-</span></span>

- <span data-ttu-id="d91c9-144">Druk op **F1**, typ **G**, selecteer **Ga naar regel**, voer de waarde **8** in en druk op **Enter**.</span><span class="sxs-lookup"><span data-stu-id="d91c9-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="d91c9-145">[![ER-formule-editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="d91c9-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <span data-ttu-id="d91c9-146"><a name="CodeStructuring">Codestructurering</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="d91c9-147">De code voor bepaalde functies, zoals [IF](er-functions-logical-if.md) of [CASE](er-functions-logical-case.md), wordt automatisch gestructureerd.</span><span class="sxs-lookup"><span data-stu-id="d91c9-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="d91c9-148">U kunt een of alle vouwgebieden van deze code uitvouwen en samenvouwen om het bewerkbare deel van een expressie te beperken, zodat u zich alleen kunt concentreren op de code waarvoor uw aandacht vereist is.</span><span class="sxs-lookup"><span data-stu-id="d91c9-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="d91c9-149">Hiervoor kunnen de opdrachten voor samenvouwen en uitvouwen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d91c9-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="d91c9-150">Als u bijvoorbeeld alle regio's wilt samenvouwen, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="d91c9-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="d91c9-151">Druk op **CTRL+K**</span><span class="sxs-lookup"><span data-stu-id="d91c9-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="d91c9-152">– of –</span><span class="sxs-lookup"><span data-stu-id="d91c9-152">-or-</span></span>

- <span data-ttu-id="d91c9-153">Druk op **F1**, druk op **FO**, selecteer **Alles samenvouwen** en druk op **Enter**</span><span class="sxs-lookup"><span data-stu-id="d91c9-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="d91c9-154">Als u alle regio's wilt openvouwen, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="d91c9-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="d91c9-155">Druk op **CTRL+J**</span><span class="sxs-lookup"><span data-stu-id="d91c9-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="d91c9-156">– of –</span><span class="sxs-lookup"><span data-stu-id="d91c9-156">-or-</span></span>
  
- <span data-ttu-id="d91c9-157">Druk op **F1**, typ **UN**, selecteer **Alles uitvouwen** en druk vervolgens op **Enter**</span><span class="sxs-lookup"><span data-stu-id="d91c9-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="d91c9-158">[![ER-formule-editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="d91c9-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <span data-ttu-id="d91c9-159"><a name="FindAndReplace">Zoeken en vervangen</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="d91c9-160">Als u bepaalde tekst wilt zoeken, selecteert u de tekst in de expressie en gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="d91c9-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="d91c9-161">Druk **op CTRL+F** en druk vervolgens op vervolgens op **F3** om het volgende exemplaar van de geselecteerde tekst te zoeken of druk op **SHIFT+F3** om het vorige exemplaar te zoeken.</span><span class="sxs-lookup"><span data-stu-id="d91c9-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="d91c9-162">– of –</span><span class="sxs-lookup"><span data-stu-id="d91c9-162">-or-</span></span>
  
- <span data-ttu-id="d91c9-163">Druk **op**F1, typ **F** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te zoeken.</span><span class="sxs-lookup"><span data-stu-id="d91c9-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="d91c9-164">Als u bepaalde tekst wilt vervangen, selecteert u de tekst in de expressie en gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="d91c9-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="d91c9-165">Druk op **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="d91c9-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="d91c9-166">Voer de alternatieve tekst in en selecteer de vervangende optie om de geselecteerde tekst of alle exemplaren van deze tekst in de huidige expressie te vervangen.</span><span class="sxs-lookup"><span data-stu-id="d91c9-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="d91c9-167">– of –</span><span class="sxs-lookup"><span data-stu-id="d91c9-167">-or-</span></span>
  
- <span data-ttu-id="d91c9-168">Druk op **F1**, typ **R** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te vervangen.</span><span class="sxs-lookup"><span data-stu-id="d91c9-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="d91c9-169">Voer de alternatieve tekst in en selecteer de vervangende optie om de geselecteerde tekst of alle exemplaren van deze tekst in de huidige expressie te vervangen.</span><span class="sxs-lookup"><span data-stu-id="d91c9-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="d91c9-170">Als u bepaalde tekst overal wilt wijzigen, selecteert u de tekst in de expressie en gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="d91c9-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="d91c9-171">Druk op **CTRL+F2** en voer vervolgens de alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="d91c9-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="d91c9-172">– of –</span><span class="sxs-lookup"><span data-stu-id="d91c9-172">-or-</span></span>
  
- <span data-ttu-id="d91c9-173">Druk op **F1**, typ **C** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d91c9-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="d91c9-174">Voer de alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="d91c9-174">Enter the alternative text.</span></span>

<span data-ttu-id="d91c9-175">[![ER-formule-editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="d91c9-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <span data-ttu-id="d91c9-176"><a name="DataPasting">Gegevensbronnen en functies plakken</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="d91c9-177">U kunt **Gegevensbron toevoegen** selecteren, waarmee in de huidige expressie een gegevensbron wordt geplakt die momenteel is geselecteerd in het linkerdeelvenster **Gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="d91c9-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="d91c9-178">U kunt ook **Functie toevoegen** selecteren, waarmee in de huidige expressie een functie wordt geplakt die momenteel is geselecteerd in het rechterdeelvenster **Functies**.</span><span class="sxs-lookup"><span data-stu-id="d91c9-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="d91c9-179">Als u de ER-formule-editor gebruikt, wordt een geselecteerde functie of een geselecteerde gegevensbron altijd geplakt aan het einde van de geconfigureerde expressie.</span><span class="sxs-lookup"><span data-stu-id="d91c9-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="d91c9-180">Als u de geavanceerde formule-editor gebruikt, kan een geselecteerde functie of een geselecteerde gegevensbron overal worden geplakt in de geconfigureerde expressie.</span><span class="sxs-lookup"><span data-stu-id="d91c9-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="d91c9-181">U moet de cursor gebruiken om op te geven waar u de gegevens wilt plakken.</span><span class="sxs-lookup"><span data-stu-id="d91c9-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="d91c9-182">[![ER-formule-editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="d91c9-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <span data-ttu-id="d91c9-183"><a name="SyntaxColorization">Inkleuring van syntaxis</a></span><span class="sxs-lookup"><span data-stu-id="d91c9-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="d91c9-184">Op dit moment worden verschillende kleuren gebruikt om de volgende onderdelen van expressies te markeren:</span><span class="sxs-lookup"><span data-stu-id="d91c9-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="d91c9-185">De tekst tussen dubbele haakjes die een label-id kan voorstellen van een tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="d91c9-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="d91c9-186">[![ER-formule-editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="d91c9-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d91c9-187">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d91c9-187">Additional resources</span></span>

- [<span data-ttu-id="d91c9-188">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="d91c9-188">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d91c9-189">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="d91c9-189">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="d91c9-190">Monaco-editor</span><span class="sxs-lookup"><span data-stu-id="d91c9-190">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
