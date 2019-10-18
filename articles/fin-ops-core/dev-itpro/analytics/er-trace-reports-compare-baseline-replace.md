---
title: Verbeteringen in het traceren van de resultaten van gegenereerde ER-rapporten en het vergelijken hiervan met basislijnwaarden
description: Dit onderwerp bevat informatie over hoe de ER-basislijnfunctie is verbeterd in Microsoft Dynamics 365 for Finance and Operations 10.0.3 (juni 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: a260be0f8659106907b26bf69bee3b33b09d0c24
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181330"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="38c59-103">Verbeteringen in het traceren van de resultaten van gegenereerde ER-rapporten en het vergelijken hiervan met basislijnwaarden</span><span class="sxs-lookup"><span data-stu-id="38c59-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="38c59-104">In dit onderwerp wordt de eerste verbeteringen beschreven die zijn aangebracht in de basisfunctie van het raamwerk voor elektronische rapportage (ER).</span><span class="sxs-lookup"><span data-stu-id="38c59-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="38c59-105">Deze verbeteringen zijn beschikbaar in Microsoft Dynamics 365 for Finance and Operations 10.0.3 (juni 2019) en hoger.</span><span class="sxs-lookup"><span data-stu-id="38c59-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="38c59-106">De instelling van basislijnregels automatiseren</span><span class="sxs-lookup"><span data-stu-id="38c59-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="38c59-107">In het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) wordt uitgelegd hoe u het ER-raamwerk kunt configureren voor het verzamelen van informatie over de uitvoering van ER-indelingen en het evalueren van de resultaten van die uitvoeringen.</span><span class="sxs-lookup"><span data-stu-id="38c59-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="38c59-108">In het voorbeeld in dit onderwerp worden de stappen weergegeven die moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="38c59-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="38c59-109">Hieronder ziet u enkele van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="38c59-109">Here are some of the steps:</span></span>

- <span data-ttu-id="38c59-110">Voer een ER-indeling uit om een uitgaand bestand te genereren en sla het bestand lokaal op.</span><span class="sxs-lookup"><span data-stu-id="38c59-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="38c59-111">Voeg het lokaal opgeslagen bestand toe als bijlage van de basislijn die is toegevoegd voor een ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="38c59-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="38c59-112">Configureer de basislijnregel voor de toegevoegde basislijn.</span><span class="sxs-lookup"><span data-stu-id="38c59-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="38c59-113">Deze configuratie omvat de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="38c59-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="38c59-114">Geef een ER-indelingselement op dat wordt gebruikt om een uitgaand bestand te genereren.</span><span class="sxs-lookup"><span data-stu-id="38c59-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="38c59-115">Selecteer de bijlage die verwijst naar het gegenereerde uitgaande bestand.</span><span class="sxs-lookup"><span data-stu-id="38c59-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="38c59-116">Deze stappen moeten handmatig worden uitgevoerd, ook al kunnen ze dankzij de nieuwe ER-mogelijkheden worden geautomatiseerd.</span><span class="sxs-lookup"><span data-stu-id="38c59-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="38c59-117">Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="38c59-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="38c59-118">Voorbeeld: De instelling van basislijnregels automatiseren</span><span class="sxs-lookup"><span data-stu-id="38c59-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="38c59-119">Als u de stappen in dit voorbeeld wilt uitvoeren, moet u eerst de stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren, tot en met de sectie Een nieuwe basislijn toevoegen voor een ontworpen ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="38c59-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="38c59-120">Toegevoegde basislijn evalueren</span><span class="sxs-lookup"><span data-stu-id="38c59-120">Review added baseline</span></span>

1. <span data-ttu-id="38c59-121">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="38c59-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="38c59-122">Selecteer **Basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="38c59-123">De knop **Basislijnen** in het actievenster is alleen beschikbaar wanneer de ER-gebruikersparameter **Uitvoeren in foutoplossingsmodus** is ingeschakeld voor het huidige bedrijf.</span><span class="sxs-lookup"><span data-stu-id="38c59-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="38c59-124">De basislijn is toegevoegd voor de geselecteerde indeling **Indeling voor leren van ER-basislijnen**, maar de basislijnregels zijn nog niet toegevoegd voor deze basislijn.</span><span class="sxs-lookup"><span data-stu-id="38c59-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="38c59-125">![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-AddBaseline2.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")</span><span class="sxs-lookup"><span data-stu-id="38c59-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="38c59-126">Een nieuwe basislijnregel maken</span><span class="sxs-lookup"><span data-stu-id="38c59-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="38c59-127">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="38c59-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="38c59-128">Vouw in de structuur **Model voor leren van ER-basislijnen** uit.</span><span class="sxs-lookup"><span data-stu-id="38c59-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="38c59-129">Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="38c59-130">Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="38c59-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="38c59-131">Geef in het veld **Id opgeven** het cijfer **1** op.</span><span class="sxs-lookup"><span data-stu-id="38c59-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="38c59-132">Stel de optie **Basislijnbestanden maken** op **Ja** in.</span><span class="sxs-lookup"><span data-stu-id="38c59-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="38c59-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="38c59-133">Select **OK**.</span></span>

    <span data-ttu-id="38c59-134">![Het dialoogvenster Parameters elektronisch rapport](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Schermafbeelding van het dialoogvenster Parameters elektronisch rapport")</span><span class="sxs-lookup"><span data-stu-id="38c59-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="38c59-135">Selecteer **Basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-135">Select **Baselines**.</span></span>

    <span data-ttu-id="38c59-136">![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")</span><span class="sxs-lookup"><span data-stu-id="38c59-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="38c59-137">Het gegenereerde uitgaande bestand wordt automatisch gekoppeld aan de basislijn van de uitgevoerde ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="38c59-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="38c59-138">De basislijnregel is automatisch toegevoegd aan deze basislijn en bevat ook de verwijzing naar het bijgevoegde bestand.</span><span class="sxs-lookup"><span data-stu-id="38c59-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="38c59-139">Voer in het veld **Naam** de tekst **Basislijn 1** in.</span><span class="sxs-lookup"><span data-stu-id="38c59-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="38c59-140">Voer in het veld **Masker bestandsnaam** de waarde **.xml** in.</span><span class="sxs-lookup"><span data-stu-id="38c59-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="38c59-141">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="38c59-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="38c59-142">De indeling uitvoeren</span><span class="sxs-lookup"><span data-stu-id="38c59-142">Run the format</span></span>

<span data-ttu-id="38c59-143">U kunt nu de resterende stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren, vanaf de sectie De ontworpen ER-indeling uitvoeren en het logboek controleren om de resultaten te analyseren.</span><span class="sxs-lookup"><span data-stu-id="38c59-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="38c59-144">Wanneer u de automatisch toegevoegde basislijnregel verwijdert op het sneltabblad **Basislijnen**, wordt de bijlage waarnaar wordt verwezen niet automatisch verwijderd.</span><span class="sxs-lookup"><span data-stu-id="38c59-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="38c59-145">De basislijn zo configureren dat voortdurend veranderende delen van de ER-uitvoer worden genegeerd</span><span class="sxs-lookup"><span data-stu-id="38c59-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="38c59-146">Wanneer een ER-indeling is ontworpen om informatie te bevatten die wordt gewijzigd wanneer de indeling wordt uitgevoerd, moet de indeling vereist zijn als u de ER-basislijnfunctie wilt gebruiken om de gegenereerde resultaten met basislijnwaarden te vergelijken.</span><span class="sxs-lookup"><span data-stu-id="38c59-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="38c59-147">De informatie kan bijvoorbeeld de verwerkingsdatum en -tijd zijn of de unieke id van een gegenereerd document in verschillende indelingen (\[GUID\], enzovoort).</span><span class="sxs-lookup"><span data-stu-id="38c59-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="38c59-148">Met de nieuwe ER-mogelijkheden kunt u de basislijnregel zo configureren dat veranderlijke elementen van een ER-indeling worden genegeerd wanneer de indeling wordt uitgevoerd met het doel om basislijnwaarden te vergelijken met de resultaten van de uitvoering van de indeling.</span><span class="sxs-lookup"><span data-stu-id="38c59-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="38c59-149">Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="38c59-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="38c59-150">Voorbeeld: De basislijn zo configureren dat voortdurend veranderende delen van de ER-uitvoer worden genegeerd</span><span class="sxs-lookup"><span data-stu-id="38c59-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="38c59-151">Als u de stappen in dit voorbeeld wilt uitvoeren, moet u eerst de stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="38c59-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="38c59-152">Een geconfigureerde ER-indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="38c59-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="38c59-153">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="38c59-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="38c59-154">Vouw in de structuur **Model voor leren van ER-basislijnen** uit.</span><span class="sxs-lookup"><span data-stu-id="38c59-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="38c59-155">Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="38c59-156">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="38c59-156">Select **Designer**.</span></span>
5. <span data-ttu-id="38c59-157">Selecteer **Output\\Document** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38c59-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="38c59-158">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-158">Select **Add**.</span></span>
7. <span data-ttu-id="38c59-159">Ga naar het vervolgkeuzemenu en selecteer **XML\\Kenmerk** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="38c59-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="38c59-160">Voer in het veld **Naam** de waarde **ProcessingDateTime** in.</span><span class="sxs-lookup"><span data-stu-id="38c59-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="38c59-161">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="38c59-161">Select **OK**.</span></span>
10. <span data-ttu-id="38c59-162">Selecteer **Uitvoer\\Document\\ProcessingDateTime** in de structuur op het tabblad **Toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="38c59-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="38c59-163">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="38c59-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="38c59-164">Voer in het veld **Formule** de volgende expressie in: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="38c59-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="38c59-165">Selecteer **Opslaan** en vervolgens **Testen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="38c59-166">Selecteer opnieuw **Testen** om de geconfigureerde expressie opnieuw te testen.</span><span class="sxs-lookup"><span data-stu-id="38c59-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="38c59-167">![De pagina Formuleontwerper](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Schermafbeelding van de pagina Formuleontwerper")</span><span class="sxs-lookup"><span data-stu-id="38c59-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="38c59-168">Op het tabblad **Testresultaten** ziet u dat de geconfigureerde expressie telkens een andere datum- en tijdwaarde oplevert wanneer deze wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="38c59-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="38c59-169">Sluit de pagina **Formuleontwerper** en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="38c59-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="38c59-170">![De pagina Indelingsontwerper](media/GER-BaselineSample-FormatMappingDesign2.PNG "Schermafbeelding van de pagina Indelingsontwerper")</span><span class="sxs-lookup"><span data-stu-id="38c59-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="38c59-171">Sluit de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="38c59-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="38c59-172">Een bestaande basislijnregel verwijderen</span><span class="sxs-lookup"><span data-stu-id="38c59-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="38c59-173">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="38c59-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="38c59-174">Selecteer **Basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="38c59-175">Selecteer in de lijst met basislijnen de basislijn die is geconfigureerd voor de indeling **Indeling voor leren van ER-basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="38c59-176">Selecteer op het sneltabblad **Basislijnen** de optie **Verwijderen** om de basislijnregel te verwijderen die u eerder hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="38c59-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="38c59-177">![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-AddBaseline3.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")</span><span class="sxs-lookup"><span data-stu-id="38c59-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="38c59-178">Vervangingen definiëren voor de bindingen van ontworpen ER-indeling</span><span class="sxs-lookup"><span data-stu-id="38c59-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="38c59-179">Selecteer op de pagina **Configuraties** op het sneltabblad **Vervangingen** de optie **Onderdelen selecteren**.</span><span class="sxs-lookup"><span data-stu-id="38c59-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="38c59-180">Vouw in de structuur met indelingsonderdelen **Uitvoer** uit, vervolgens **Uitvoer\\Document** en schakel het selectievakje voor **Uitvoer\\Document\\ProcessingDateTime** in.</span><span class="sxs-lookup"><span data-stu-id="38c59-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="38c59-181">![Het dialoogvenster Onderdelen selecteren](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Schermafbeelding van het dialoogvenster Onderdelen selecteren")</span><span class="sxs-lookup"><span data-stu-id="38c59-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="38c59-182">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="38c59-182">Select **OK**.</span></span>

<span data-ttu-id="38c59-183">![De pagina Basislijnen voor ER-indeling](media/GER-BaselineSample-AddBaseline4.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")</span><span class="sxs-lookup"><span data-stu-id="38c59-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="38c59-184">Het geselecteerde ER-indelingsonderdeel is toegevoegd aan de lijst met onderdelen op het sneltabblad **Vervangingen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="38c59-185">Wanneer de basis-ER-indeling wordt uitgevoerd in de foutoplossingsmodus, wordt de indelingsbinding voor elk onderdeel vervangen door de binding die wordt weergegeven in de kolom **Binding**.</span><span class="sxs-lookup"><span data-stu-id="38c59-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="38c59-186">Selecteer **Bewerken** om de standaardbinding te wijzigen voor een onderdeel dat wordt weergegeven op het sneltabblad **Vervangingen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="38c59-187">Een nieuwe basislijnregel maken</span><span class="sxs-lookup"><span data-stu-id="38c59-187">Make a new baseline rule</span></span>

<span data-ttu-id="38c59-188">Volg de stappen in de sectie Voorbeeld: De instelling van basislijnregels automatiseren eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="38c59-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="38c59-189">Er wordt een melding weergegeven dat het uitgaande bestand is gegenereerd met behulp van basislijninstellingen en dat er een geforceerde vervanging van de indelingsbindingen heeft plaatsgevonden.</span><span class="sxs-lookup"><span data-stu-id="38c59-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="38c59-190">![Melding op de pagina Configuraties](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Schermafbeelding van de melding op de pagina Configuraties")</span><span class="sxs-lookup"><span data-stu-id="38c59-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="38c59-191">Waarschuwingen over het vervangen van indelingsbindingen onderdrukken</span><span class="sxs-lookup"><span data-stu-id="38c59-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="38c59-192">Door specifieke ER-parameters in te stellen, kunt u meldingen onderdrukken die waarschuwen bij het vervangen van indelingsbindingen.</span><span class="sxs-lookup"><span data-stu-id="38c59-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="38c59-193">Deze onderdrukking kan handig zijn indelingsbindingen in een modus zonder toezicht worden vervangen met behulp van Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="38c59-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="38c59-194">In dit geval kan de waarschuwing worden beschouwd als een fout van de testcase die wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="38c59-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="38c59-195">Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="38c59-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="38c59-196">Stel de optie **Waarschuwingen voor basislijn** in op **Ja** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="38c59-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="38c59-197">![Het dialoogvenster Gebruikersparameters](media/GER-BaselineSample-ERUserParameters1.png "Schermafbeelding van het dialoogvenster Gebruikersparameters")</span><span class="sxs-lookup"><span data-stu-id="38c59-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="38c59-198">Het gegenereerde basislijnbestand bekijken</span><span class="sxs-lookup"><span data-stu-id="38c59-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="38c59-199">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="38c59-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="38c59-200">Selecteer **Basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="38c59-201">Selecteer **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-201">Select **Attachments**.</span></span>

    <span data-ttu-id="38c59-202">![De pagina Bijlagen](media/GER-BaselineSample-AttachedBaselineFile.PNG "Schermafbeelding van de pagina Bijlagen")</span><span class="sxs-lookup"><span data-stu-id="38c59-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="38c59-203">Het gegenereerde bestand bevat de tekst voor de verwerkingsdatum en -tijd (**"#"**) uit de binding die is geconfigureerd in de toegevoegde basislijnregel, niet uit de binding van de indeling.</span><span class="sxs-lookup"><span data-stu-id="38c59-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="38c59-204">Sluit de pagina **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="38c59-205">De ontworpen ER-indeling uitvoeren en het logboek controleren om de resultaten te analyseren</span><span class="sxs-lookup"><span data-stu-id="38c59-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="38c59-206">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="38c59-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="38c59-207">Vouw in de structuur **Model voor leren van ER-basislijnen** uit.</span><span class="sxs-lookup"><span data-stu-id="38c59-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="38c59-208">Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="38c59-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="38c59-209">Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="38c59-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="38c59-210">Geef in het veld **Id opgeven** het cijfer **1** op.</span><span class="sxs-lookup"><span data-stu-id="38c59-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="38c59-211">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="38c59-211">Select **OK**.</span></span>
7. <span data-ttu-id="38c59-212">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Foutopsporingslogboeken voor configuraties**.</span><span class="sxs-lookup"><span data-stu-id="38c59-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="38c59-213">Het uitvoeringslogboek bevat informatie over de resultaten van de vergelijking van het gegenereerde bestand met de geconfigureerde basislijn.</span><span class="sxs-lookup"><span data-stu-id="38c59-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="38c59-214">In het logboek wordt aangegeven dat het gegenereerde bestand en de basislijn overeenkomen, ook al bevat de uitgevoerde indelingen de binding om een steeds veranderende datum- en tijdwaarde in het uitgaande bestand in te voeren.</span><span class="sxs-lookup"><span data-stu-id="38c59-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="38c59-215">Hoewel het uitgaande bestand is gegenereerd met behulp van basislijninstellingen die de vervanging van de bindingen van de indeling forceren, ontvangt u geen waarschuwingen over de vervanging.</span><span class="sxs-lookup"><span data-stu-id="38c59-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="38c59-216">Basislijninstellingen tussen omgevingen uitwisselen</span><span class="sxs-lookup"><span data-stu-id="38c59-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="38c59-217">Basislijninstellingen exporteren</span><span class="sxs-lookup"><span data-stu-id="38c59-217">Export baseline settings</span></span>

<span data-ttu-id="38c59-218">Met de nieuwe ER-mogelijkheden kunt u basislijninstellingen voor de geselecteerde ER-indeling exporteren uit de huidige omgeving exporteren en deze opslaan als XML-bestanden.</span><span class="sxs-lookup"><span data-stu-id="38c59-218">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="38c59-219">Als u basislijninstellingen wilt exporteren, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="38c59-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="38c59-220">Basislijninstellingen importeren</span><span class="sxs-lookup"><span data-stu-id="38c59-220">Import baseline settings</span></span>

<span data-ttu-id="38c59-221">Geëxporteerde basislijninstellingen kunnen in een andere omgeving worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="38c59-221">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="38c59-222">De omgeving moet eerst worden geïmporteerd als ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="38c59-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="38c59-223">Vervolgens kunt u de basislijninstellingen importeren.</span><span class="sxs-lookup"><span data-stu-id="38c59-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="38c59-224">Als u basislijninstellingen vanuit een lokaal opgeslagen XML-bestand wilt importeren, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Importeren** en vervolgens selecteert u **Bladeren** om het XML-bestand te selecteren.</span><span class="sxs-lookup"><span data-stu-id="38c59-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="38c59-225">![Het dialoogvenster Basislijninstellingen importeren](media/GER-BaselineSample-ImportBaseline1.PNG "Schermafbeelding van het dialoogvenster Basislijninstellingen importeren")</span><span class="sxs-lookup"><span data-stu-id="38c59-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="38c59-226">Als u basislijninstellingen wilt importeren vanuit een XML-bestand dat op de Microsoft SharePoint-server is opgeslagen, op basis van de huidige instellingen voor documentbeheer en het geselecteerde documenttype, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Importeren uit bron**.</span><span class="sxs-lookup"><span data-stu-id="38c59-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="38c59-227">Selecteer het documenttype en het XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="38c59-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="38c59-228">Het vereiste documenttype voor toegang tot de SharePoint-map moet vooraf worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="38c59-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="38c59-229">![Het dialoogvenster Importeren uit bron](media/GER-BaselineSample-ImportBaseline2.PNG "Schermafbeelding van het dialoogvenster Importeren uit bron")</span><span class="sxs-lookup"><span data-stu-id="38c59-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="38c59-230">U kunt Taakregistratie gebruiken om de stappen vast te leggen voor het selecteren van het vereiste documenttype en de bestandsnaam in het dialoogvenster **Importeren vanuit bron**.</span><span class="sxs-lookup"><span data-stu-id="38c59-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="38c59-231">Op deze manier kunt u de vereiste basislijninstellingen op de SharePoint-server behouden en deze vervolgens automatisch importeren door een taakregistratie af te spelen wanneer u automatische tests uitvoert met behulp van Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="38c59-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38c59-232">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="38c59-232">Additional resources</span></span>

- [<span data-ttu-id="38c59-233">Gegenereerde rapportresultaten traceren en vergelijken met basislijnwaarden</span><span class="sxs-lookup"><span data-stu-id="38c59-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="38c59-234">Taakregistratie</span><span class="sxs-lookup"><span data-stu-id="38c59-234">Task recorder</span></span>](../user-interface/task-recorder.md)
