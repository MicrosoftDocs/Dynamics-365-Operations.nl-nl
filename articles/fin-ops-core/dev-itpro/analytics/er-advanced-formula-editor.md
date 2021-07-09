---
title: Geavanceerde formule-editor voor elektronische rapporten
description: In dit onderwerp wordt beschreven hoe de geavanceerde formule-editor kan worden gebruikt voor het configureren van expressies in ER-modeltoewijzing (elektronische rapportage) en indelingscomponenten.
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270702"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="47e5b-103">Geavanceerde formule-editor voor elektronische rapporten</span><span class="sxs-lookup"><span data-stu-id="47e5b-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47e5b-104">Behalve de [formule-editor](general-electronic-reporting-formula-designer.md) voor [elektronische rapportage](general-electronic-reporting.md) kunt u de geavanceerde formule-editor voor elektronische rapportage gebruiken om de ervaring voor het configureren van ER-expressies te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="47e5b-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="47e5b-105">De geavanceerde editor is op browsers gebaseerd en wordt aangedreven door de [Monaco](https://microsoft.github.io/monaco-editor)-editor.</span><span class="sxs-lookup"><span data-stu-id="47e5b-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="47e5b-106">De meest gebruikte functies van de geavanceerde editor worden in dit onderwerp beschreven:</span><span class="sxs-lookup"><span data-stu-id="47e5b-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="47e5b-107">Automatische codeopmaak</span><span class="sxs-lookup"><span data-stu-id="47e5b-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="47e5b-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="47e5b-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="47e5b-109">Codevoltooiing</span><span class="sxs-lookup"><span data-stu-id="47e5b-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="47e5b-110">Codenavigatie</span><span class="sxs-lookup"><span data-stu-id="47e5b-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="47e5b-111">Codestructurering</span><span class="sxs-lookup"><span data-stu-id="47e5b-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="47e5b-112">Zoeken en vervangen</span><span class="sxs-lookup"><span data-stu-id="47e5b-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="47e5b-113">Gegevens plakken</span><span class="sxs-lookup"><span data-stu-id="47e5b-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="47e5b-114">Inkleuring van syntaxis</span><span class="sxs-lookup"><span data-stu-id="47e5b-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="47e5b-115"><a name="ActivateAdvEditor">De geavanceerde formule-editor activeren</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="47e5b-116">Voer de volgende stappen uit om de geavanceerde formule-editor te gebruiken in uw exemplaar van Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="47e5b-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="47e5b-117">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="47e5b-118">Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="47e5b-119">Stel in het dialoogvenster **Gebruikersparameters** in de sectie **Uitvoeringstracering** de parameter **Geavanceerde formule-editor inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="47e5b-120">[![Dialoogvenster Gebruikersparameters, parameter Geavanceerde formule-editor inschakelen gemarkeerd](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="47e5b-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="47e5b-121">Houd er rekening mee dat deze parameter specifiek is voor de gebruiker en specifiek voor het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="47e5b-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="47e5b-122">Vanaf Microsoft Dynamics 365 Finance versie 10.0.19 kunt u bepalen welke ER-formule-editor standaard wordt aangeboden.</span><span class="sxs-lookup"><span data-stu-id="47e5b-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="47e5b-123">Voltooi de volgende stappen om de geavanceerde formule-editor in te schakelen voor alle gebruikers en bedrijven van het huidige exemplaar van Financiën.</span><span class="sxs-lookup"><span data-stu-id="47e5b-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="47e5b-124">Open het het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="47e5b-125">Zoek de functie **De geavanceerde formule-editor instellen als standaardwaarde voor alle gebruikers** in de lijst en selecteer vervolgens **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="47e5b-126">Ga naar **Organisatiebeheer** > **Elektronische rapportage** > **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="47e5b-127">Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="47e5b-128">Zoek in het dialoogvenster **Gebruikersparameters** naar de parameter **Geavanceerde formule-editor uitschakelen** en controleer of deze is ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="47e5b-129">[![Dialoogvenster Gebruikersparameters, parameter Geavanceerde formule-editor uitschakelen gemarkeerd](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="47e5b-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="47e5b-130">De waarden van de parameters **Geavanceerde formule-editor inschakelen** en **Geavanceerde formule-editor uitschakelen** worden gescheiden gehouden voor elke gebruiker en worden aangeboden in het dialoogvenster **Gebruikersparameters**, afhankelijk van de status van de functie **De geavanceerde formule-editor instellen als standaardwaarde voor alle gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="47e5b-131"><a name="Autoformatting">Automatische codeopmaak</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="47e5b-132">Wanneer u een complexe expressie schrijft die uit meerdere regels met code bestaat, wordt de inspringing van een nieuwe ingevoerde regel automatisch uitgevoerd op basis van de inspringing van de vorige rij.</span><span class="sxs-lookup"><span data-stu-id="47e5b-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="47e5b-133">U kunt regels selecteren en de inspringing ervan wijzigen door **Tab** of **Shift+Tab** te typen.</span><span class="sxs-lookup"><span data-stu-id="47e5b-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="47e5b-134">[![Afbeelding van de ER-formule-editor waarin selectie van regels en wijziging van de inspringing worden getoond](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="47e5b-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="47e5b-135">Met automatische opmaak kunt u de volledige expressie goed opgemaakt houden om verder onderhoud te vergemakkelijken en inzicht in de geconfigureerde logica te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="47e5b-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="47e5b-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="47e5b-137">De editor biedt woordaanvulling om u te helpen bij het sneller schrijven van expressies en het voorkomen van typefouten.</span><span class="sxs-lookup"><span data-stu-id="47e5b-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="47e5b-138">Wanneer u nieuwe tekst gaat toevoegen, biedt de editor automatisch een lijst met functies die worden ondersteund in ER-functies die de tekens bevatten die u hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="47e5b-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="47e5b-139">U kunt IntelliSense ook op elke plaats in een geconfigureerde expressie activeren door **Ctrl+spatiebalk** te typen.</span><span class="sxs-lookup"><span data-stu-id="47e5b-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="47e5b-140">[![Afbeelding van de ER-formule-editor waarin het activeren van IntelliSense wordt getoond](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="47e5b-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="47e5b-141"><a name="CodeCompletion">Codevoltooiing</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="47e5b-142">De editor zorgt er automatisch voor dat code wordt voltooid door:</span><span class="sxs-lookup"><span data-stu-id="47e5b-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="47e5b-143">Het invoegen van een haakje sluiten wanneer er een openingshaakje wordt ingevoerd, waarbij de cursor zich tussen de haakjes bevindt.</span><span class="sxs-lookup"><span data-stu-id="47e5b-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="47e5b-144">Het tweede aanhalingsteken invoegen wanneer het eerste wordt ingevoerd, waarbij de cursor binnen de aanhalingstekens blijft.</span><span class="sxs-lookup"><span data-stu-id="47e5b-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="47e5b-145">Het tweede dubbele aanhalingsteken invoegen wanneer het eerste wordt ingevoerd, waarbij de cursor binnen de aanhalingstekens blijft.</span><span class="sxs-lookup"><span data-stu-id="47e5b-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="47e5b-146">[![Afbeelding van de ER-formule-editor waarin codevoltooiing door de editor wordt getoond](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="47e5b-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="47e5b-147">Wanneer u naar het getypte haakje wijst, wordt het tweede haakje van dit paar automatisch gemarkeerd, zodat de constructie wordt weergegeven die ze ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="47e5b-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="47e5b-148"><a name="CodeNavigation">Codenavigatie</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="47e5b-149">U kunt de vereiste symbolen of regels in uw expressie vinden door de opdracht **Ga naar** te typen met het opdrachtpalet of het contextmenu.</span><span class="sxs-lookup"><span data-stu-id="47e5b-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="47e5b-150">Als u bijvoorbeeld naar regel **8** wilt gaan, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="47e5b-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="47e5b-151">Druk **op CTRL+G**, voer de waarde **8** in en druk op **ENTER**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="47e5b-152">– of –</span><span class="sxs-lookup"><span data-stu-id="47e5b-152">-or-</span></span>

- <span data-ttu-id="47e5b-153">Druk op **F1**, typ **G**, selecteer **Ga naar regel**, voer de waarde **8** in en druk op **Enter**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="47e5b-154">[![Afbeelding van de ER-formule-editor waarin wordt getoond hoe u delen van een expressie kunt zoeken met behulp van het opdrachtpalet](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="47e5b-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="47e5b-155"><a name="CodeStructuring">Codestructurering</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="47e5b-156">De code voor bepaalde functies, zoals [IF](er-functions-logical-if.md) of [CASE](er-functions-logical-case.md), wordt automatisch gestructureerd.</span><span class="sxs-lookup"><span data-stu-id="47e5b-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="47e5b-157">U kunt een of alle vouwgebieden van deze code uitvouwen en samenvouwen om het bewerkbare deel van een expressie te beperken, zodat u zich alleen kunt concentreren op de code waarvoor uw aandacht vereist is.</span><span class="sxs-lookup"><span data-stu-id="47e5b-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="47e5b-158">Hiervoor kunnen de opdrachten voor samenvouwen en uitvouwen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="47e5b-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="47e5b-159">Als u bijvoorbeeld alle regio's wilt samenvouwen, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="47e5b-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="47e5b-160">Druk op **CTRL+K**</span><span class="sxs-lookup"><span data-stu-id="47e5b-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="47e5b-161">– of –</span><span class="sxs-lookup"><span data-stu-id="47e5b-161">-or-</span></span>

- <span data-ttu-id="47e5b-162">Druk op **F1**, druk op **FO**, selecteer **Alles samenvouwen** en druk op **Enter**</span><span class="sxs-lookup"><span data-stu-id="47e5b-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="47e5b-163">Als u alle regio's wilt openvouwen, gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="47e5b-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="47e5b-164">Druk op **CTRL+J**</span><span class="sxs-lookup"><span data-stu-id="47e5b-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="47e5b-165">– of –</span><span class="sxs-lookup"><span data-stu-id="47e5b-165">-or-</span></span>
  
- <span data-ttu-id="47e5b-166">Druk op **F1**, typ **UN**, selecteer **Alles uitvouwen** en druk vervolgens op **Enter**</span><span class="sxs-lookup"><span data-stu-id="47e5b-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="47e5b-167">[![Afbeelding van de ER-formule-editor waarin het uitvouwen van code wordt getoond](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="47e5b-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="47e5b-168"><a name="FindAndReplace">Zoeken en vervangen</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="47e5b-169">Als u bepaalde tekst wilt zoeken, selecteert u de tekst in de expressie en gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="47e5b-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="47e5b-170">Druk **op CTRL+F** en druk vervolgens op vervolgens op **F3** om het volgende exemplaar van de geselecteerde tekst te zoeken of druk op **SHIFT+F3** om het vorige exemplaar te zoeken.</span><span class="sxs-lookup"><span data-stu-id="47e5b-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="47e5b-171">– of –</span><span class="sxs-lookup"><span data-stu-id="47e5b-171">-or-</span></span>
  
- <span data-ttu-id="47e5b-172">Druk **op** F1, typ **F** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te zoeken.</span><span class="sxs-lookup"><span data-stu-id="47e5b-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="47e5b-173">Als u bepaalde tekst wilt vervangen, selecteert u de tekst in de expressie en gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="47e5b-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="47e5b-174">Druk op **Ctrl+H**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="47e5b-175">Voer de alternatieve tekst in en selecteer de vervangende optie om de geselecteerde tekst of alle exemplaren van deze tekst in de huidige expressie te vervangen.</span><span class="sxs-lookup"><span data-stu-id="47e5b-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="47e5b-176">– of –</span><span class="sxs-lookup"><span data-stu-id="47e5b-176">-or-</span></span>
  
- <span data-ttu-id="47e5b-177">Druk op **F1**, typ **R** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te vervangen.</span><span class="sxs-lookup"><span data-stu-id="47e5b-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="47e5b-178">Voer de alternatieve tekst in en selecteer de vervangende optie om de geselecteerde tekst of alle exemplaren van deze tekst in de huidige expressie te vervangen.</span><span class="sxs-lookup"><span data-stu-id="47e5b-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="47e5b-179">Als u bepaalde tekst overal wilt wijzigen, selecteert u de tekst in de expressie en gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="47e5b-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="47e5b-180">Druk op **CTRL+F2** en voer vervolgens de alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="47e5b-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="47e5b-181">– of –</span><span class="sxs-lookup"><span data-stu-id="47e5b-181">-or-</span></span>
  
- <span data-ttu-id="47e5b-182">Druk op **F1**, typ **C** en selecteer vervolgens de vereiste optie om de geselecteerde tekst te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="47e5b-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="47e5b-183">Voer de alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="47e5b-183">Enter the alternative text.</span></span>

<span data-ttu-id="47e5b-184">[![Afbeelding van de ER-formule-editor waarin het zoeken en vervangen wordt getoond](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="47e5b-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="47e5b-185"><a name="DataPasting">Gegevensbronnen en functies plakken</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="47e5b-186">U kunt **Gegevensbron toevoegen** selecteren, waarmee in de huidige expressie een gegevensbron wordt geplakt die momenteel is geselecteerd in het linkerdeelvenster **Gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="47e5b-187">U kunt ook **Functie toevoegen** selecteren, waarmee in de huidige expressie een functie wordt geplakt die momenteel is geselecteerd in het rechterdeelvenster **Functies**.</span><span class="sxs-lookup"><span data-stu-id="47e5b-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="47e5b-188">Als u de ER-formule-editor gebruikt, wordt een geselecteerde functie of een geselecteerde gegevensbron altijd geplakt aan het einde van de geconfigureerde expressie.</span><span class="sxs-lookup"><span data-stu-id="47e5b-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="47e5b-189">Als u de geavanceerde formule-editor gebruikt, kan een geselecteerde functie of een geselecteerde gegevensbron overal worden geplakt in de geconfigureerde expressie.</span><span class="sxs-lookup"><span data-stu-id="47e5b-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="47e5b-190">U moet de cursor gebruiken om op te geven waar u de gegevens wilt plakken.</span><span class="sxs-lookup"><span data-stu-id="47e5b-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="47e5b-191">[![Afbeelding van de ER-formule-editor waarin het toevoegen van een gegevensbron en het toevoegen van een functie worden getoond](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="47e5b-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="47e5b-192"><a name="SyntaxColorization">Inkleuring van syntaxis</a></span><span class="sxs-lookup"><span data-stu-id="47e5b-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="47e5b-193">Op dit moment worden verschillende kleuren gebruikt om de volgende onderdelen van expressies te markeren:</span><span class="sxs-lookup"><span data-stu-id="47e5b-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="47e5b-194">De tekst tussen dubbele haakjes die een label-id kan voorstellen van een tekstconstante.</span><span class="sxs-lookup"><span data-stu-id="47e5b-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="47e5b-195">[![ER-formule-editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="47e5b-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="47e5b-196">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="47e5b-196">Limitations</span></span>

<span data-ttu-id="47e5b-197">De editor wordt momenteel ondersteund in de volgende webbrowsers:</span><span class="sxs-lookup"><span data-stu-id="47e5b-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="47e5b-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="47e5b-198">Chrome</span></span>
- <span data-ttu-id="47e5b-199">Edge</span><span class="sxs-lookup"><span data-stu-id="47e5b-199">Edge</span></span>
- <span data-ttu-id="47e5b-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="47e5b-200">Firefox</span></span>
- <span data-ttu-id="47e5b-201">Opera</span><span class="sxs-lookup"><span data-stu-id="47e5b-201">Opera</span></span>
- <span data-ttu-id="47e5b-202">Safari</span><span class="sxs-lookup"><span data-stu-id="47e5b-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47e5b-203">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="47e5b-203">Additional resources</span></span>

- [<span data-ttu-id="47e5b-204">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="47e5b-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="47e5b-205">Formuleontwerper in elektronische aangifte</span><span class="sxs-lookup"><span data-stu-id="47e5b-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="47e5b-206">Monaco-editor</span><span class="sxs-lookup"><span data-stu-id="47e5b-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
