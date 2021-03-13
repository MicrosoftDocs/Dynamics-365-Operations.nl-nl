---
title: Verbeteringen in het traceren van de resultaten van gegenereerde ER-rapporten en het vergelijken hiervan met basislijnwaarden
description: Dit onderwerp beschrijft verbeteringen in de ER-basislijnfunctie in Microsoft Dynamics 365 for Finance and Operations versie 10.0.3 (juni 2019).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1c00a5d9e2804f6ec0f6cb4c544029a1235ee58d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093999"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="d131a-103">Verbeteringen in het traceren van de resultaten van gegenereerde ER-rapporten en het vergelijken hiervan met basislijnwaarden</span><span class="sxs-lookup"><span data-stu-id="d131a-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d131a-104">In dit onderwerp wordt de eerste verbeteringen beschreven die zijn aangebracht in de basisfunctie van het raamwerk voor elektronische rapportage (ER).</span><span class="sxs-lookup"><span data-stu-id="d131a-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="d131a-105">Deze verbeteringen zijn beschikbaar in Microsoft Dynamics 365 for Finance and Operations 10.0.3 (juni 2019) en hoger.</span><span class="sxs-lookup"><span data-stu-id="d131a-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="d131a-106">De instelling van basislijnregels automatiseren</span><span class="sxs-lookup"><span data-stu-id="d131a-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="d131a-107">In het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) wordt uitgelegd hoe u het ER-raamwerk kunt configureren voor het verzamelen van informatie over de uitvoering van ER-indelingen en het evalueren van de resultaten van die uitvoeringen.</span><span class="sxs-lookup"><span data-stu-id="d131a-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="d131a-108">In het voorbeeld in dit onderwerp worden de stappen weergegeven die moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d131a-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="d131a-109">Hieronder ziet u enkele van deze stappen:</span><span class="sxs-lookup"><span data-stu-id="d131a-109">Here are some of the steps:</span></span>

- <span data-ttu-id="d131a-110">Voer een ER-indeling uit om een uitgaand bestand te genereren en sla het bestand lokaal op.</span><span class="sxs-lookup"><span data-stu-id="d131a-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="d131a-111">Voeg het lokaal opgeslagen bestand toe als bijlage van de basislijn die is toegevoegd voor een ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="d131a-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="d131a-112">Configureer de basislijnregel voor de toegevoegde basislijn.</span><span class="sxs-lookup"><span data-stu-id="d131a-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="d131a-113">Deze configuratie omvat de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="d131a-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="d131a-114">Geef een ER-indelingselement op dat wordt gebruikt om een uitgaand bestand te genereren.</span><span class="sxs-lookup"><span data-stu-id="d131a-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="d131a-115">Selecteer de bijlage die verwijst naar het gegenereerde uitgaande bestand.</span><span class="sxs-lookup"><span data-stu-id="d131a-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="d131a-116">Deze stappen moeten handmatig worden uitgevoerd, ook al kunnen ze dankzij de nieuwe ER-mogelijkheden worden geautomatiseerd.</span><span class="sxs-lookup"><span data-stu-id="d131a-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="d131a-117">Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d131a-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="d131a-118">Voorbeeld: De instelling van basislijnregels automatiseren</span><span class="sxs-lookup"><span data-stu-id="d131a-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="d131a-119">Als u de stappen in dit voorbeeld wilt uitvoeren, moet u eerst de stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren, tot en met de sectie Een nieuwe basislijn toevoegen voor een ontworpen ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="d131a-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="d131a-120">Toegevoegde basislijn evalueren</span><span class="sxs-lookup"><span data-stu-id="d131a-120">Review added baseline</span></span>

1. <span data-ttu-id="d131a-121">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d131a-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d131a-122">Selecteer **Basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d131a-123">De knop **Basislijnen** in het actievenster is alleen beschikbaar wanneer de ER-gebruikersparameter **Uitvoeren in foutoplossingsmodus** is ingeschakeld voor het huidige bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d131a-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="d131a-124">De basislijn is toegevoegd voor de geselecteerde indeling **Indeling voor leren van ER-basislijnen**, maar de basislijnregels zijn nog niet toegevoegd voor deze basislijn.</span><span class="sxs-lookup"><span data-stu-id="d131a-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="d131a-125">![De pagina Basislijnen voor ER-indeling, nog geen regels](media/GER-BaselineSample-AddBaseline2.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")</span><span class="sxs-lookup"><span data-stu-id="d131a-125">![Electronic reporting format baselines page, no rules yet](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="d131a-126">Een nieuwe basislijnregel maken</span><span class="sxs-lookup"><span data-stu-id="d131a-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="d131a-127">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d131a-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d131a-128">Vouw in de structuur **Model voor leren van ER-basislijnen** uit.</span><span class="sxs-lookup"><span data-stu-id="d131a-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="d131a-129">Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="d131a-130">Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="d131a-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="d131a-131">Geef in het veld **Id opgeven** het cijfer **1** op.</span><span class="sxs-lookup"><span data-stu-id="d131a-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="d131a-132">Stel de optie **Basislijnbestanden maken** op **Ja** in.</span><span class="sxs-lookup"><span data-stu-id="d131a-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="d131a-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d131a-133">Select **OK**.</span></span>
8. <span data-ttu-id="d131a-134">Selecteer **Basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-134">Select **Baselines**.</span></span>

    <span data-ttu-id="d131a-135">![Pagina Basislijnen voor ER-indeling, basislijnen geselecteerd](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")</span><span class="sxs-lookup"><span data-stu-id="d131a-135">![Electronic reporting format baselines page, baselines selected](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="d131a-136">Het gegenereerde uitgaande bestand wordt automatisch gekoppeld aan de basislijn van de uitgevoerde ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="d131a-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="d131a-137">De basislijnregel is automatisch toegevoegd aan deze basislijn en bevat ook de verwijzing naar het bijgevoegde bestand.</span><span class="sxs-lookup"><span data-stu-id="d131a-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="d131a-138">Voer in het veld **Naam** de tekst **Basislijn 1** in.</span><span class="sxs-lookup"><span data-stu-id="d131a-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="d131a-139">Voer in het veld **Masker bestandsnaam** de waarde **.xml** in.</span><span class="sxs-lookup"><span data-stu-id="d131a-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="d131a-140">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d131a-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="d131a-141">De indeling uitvoeren</span><span class="sxs-lookup"><span data-stu-id="d131a-141">Run the format</span></span>

<span data-ttu-id="d131a-142">U kunt nu de resterende stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren, vanaf de sectie De ontworpen ER-indeling uitvoeren en het logboek controleren om de resultaten te analyseren.</span><span class="sxs-lookup"><span data-stu-id="d131a-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="d131a-143">Wanneer u de automatisch toegevoegde basislijnregel verwijdert op het sneltabblad **Basislijnen**, wordt de bijlage waarnaar wordt verwezen niet automatisch verwijderd.</span><span class="sxs-lookup"><span data-stu-id="d131a-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="d131a-144">De basislijn zo configureren dat voortdurend veranderende delen van de ER-uitvoer worden genegeerd</span><span class="sxs-lookup"><span data-stu-id="d131a-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="d131a-145">Wanneer een ER-indeling is ontworpen om informatie te bevatten die wordt gewijzigd wanneer de indeling wordt uitgevoerd, moet de indeling vereist zijn als u de ER-basislijnfunctie wilt gebruiken om de gegenereerde resultaten met basislijnwaarden te vergelijken.</span><span class="sxs-lookup"><span data-stu-id="d131a-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="d131a-146">De informatie kan bijvoorbeeld de verwerkingsdatum en -tijd zijn of de unieke id van een gegenereerd document in verschillende indelingen (\[GUID\], enzovoort).</span><span class="sxs-lookup"><span data-stu-id="d131a-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="d131a-147">Met de nieuwe ER-mogelijkheden kunt u de basislijnregel zo configureren dat veranderlijke elementen van een ER-indeling worden genegeerd wanneer de indeling wordt uitgevoerd met het doel om basislijnwaarden te vergelijken met de resultaten van de uitvoering van de indeling.</span><span class="sxs-lookup"><span data-stu-id="d131a-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="d131a-148">Voor meer informatie over deze functie kunt u het volgende voorbeeld uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d131a-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="d131a-149">Voorbeeld: De basislijn zo configureren dat voortdurend veranderende delen van de ER-uitvoer worden genegeerd</span><span class="sxs-lookup"><span data-stu-id="d131a-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="d131a-150">Als u de stappen in dit voorbeeld wilt uitvoeren, moet u eerst de stappen in het voorbeeld in het onderwerp [Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden](er-trace-reports-compare-baseline.md) uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d131a-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="d131a-151">Een geconfigureerde ER-indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="d131a-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="d131a-152">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d131a-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d131a-153">Vouw in de structuur **Model voor leren van ER-basislijnen** uit.</span><span class="sxs-lookup"><span data-stu-id="d131a-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="d131a-154">Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="d131a-155">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="d131a-155">Select **Designer**.</span></span>
5. <span data-ttu-id="d131a-156">Selecteer **Output\\Document** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d131a-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="d131a-157">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-157">Select **Add**.</span></span>
7. <span data-ttu-id="d131a-158">Ga naar het vervolgkeuzemenu en selecteer **XML\\Kenmerk** in de structuur.</span><span class="sxs-lookup"><span data-stu-id="d131a-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="d131a-159">Voer in het veld **Naam** de waarde **ProcessingDateTime** in.</span><span class="sxs-lookup"><span data-stu-id="d131a-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="d131a-160">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d131a-160">Select **OK**.</span></span>
10. <span data-ttu-id="d131a-161">Selecteer **Uitvoer\\Document\\ProcessingDateTime** in de structuur op het tabblad **Toewijzing**.</span><span class="sxs-lookup"><span data-stu-id="d131a-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="d131a-162">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d131a-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="d131a-163">Voer in het veld **Formule** de volgende expressie in: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="d131a-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="d131a-164">Selecteer **Opslaan** en vervolgens **Testen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="d131a-165">Selecteer opnieuw **Testen** om de geconfigureerde expressie opnieuw te testen.</span><span class="sxs-lookup"><span data-stu-id="d131a-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="d131a-166">![De pagina Formuleontwerper](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Schermafbeelding van de pagina Formuleontwerper")</span><span class="sxs-lookup"><span data-stu-id="d131a-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="d131a-167">Op het tabblad **Testresultaten** ziet u dat de geconfigureerde expressie telkens een andere datum- en tijdwaarde oplevert wanneer deze wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="d131a-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="d131a-168">Sluit de pagina **Formuleontwerper** en selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d131a-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="d131a-169">![Pagina Indelingsontwerper](media/GER-BaselineSample-FormatMappingDesign2.PNG "Schermafbeelding van de pagina Indelingsontwerper")</span><span class="sxs-lookup"><span data-stu-id="d131a-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="d131a-170">Sluit de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="d131a-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="d131a-171">Een bestaande basislijnregel verwijderen</span><span class="sxs-lookup"><span data-stu-id="d131a-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="d131a-172">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d131a-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d131a-173">Selecteer **Basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="d131a-174">Selecteer in de lijst met basislijnen de basislijn die is geconfigureerd voor de indeling **Indeling voor leren van ER-basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="d131a-175">Selecteer op het sneltabblad **Basislijnen** de optie **Verwijderen** om de basislijnregel te verwijderen die u eerder hebt geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="d131a-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="d131a-176">![De pagina Basislijnen voor ER-indeling, verwijderd](media/GER-BaselineSample-AddBaseline3.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")</span><span class="sxs-lookup"><span data-stu-id="d131a-176">![Electronic reporting format baselines page, deleted](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="d131a-177">Vervangingen definiëren voor de bindingen van ontworpen ER-indeling</span><span class="sxs-lookup"><span data-stu-id="d131a-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="d131a-178">Selecteer op de pagina **Configuraties** op het sneltabblad **Vervangingen** de optie **Onderdelen selecteren**.</span><span class="sxs-lookup"><span data-stu-id="d131a-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="d131a-179">Vouw in de structuur met indelingsonderdelen **Uitvoer** uit, vervolgens **Uitvoer\\Document** en schakel het selectievakje voor **Uitvoer\\Document\\ProcessingDateTime** in.</span><span class="sxs-lookup"><span data-stu-id="d131a-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="d131a-180">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d131a-180">Select **OK**.</span></span>

<span data-ttu-id="d131a-181">![De pagina Basislijnen voor ER-indeling, componenten](media/GER-BaselineSample-AddBaseline4.PNG "Schermafbeelding van de pagina Basislijnen voor ER-indeling")</span><span class="sxs-lookup"><span data-stu-id="d131a-181">![Electronic reporting format baselines page, components](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="d131a-182">Het geselecteerde ER-indelingsonderdeel is toegevoegd aan de lijst met onderdelen op het sneltabblad **Vervangingen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="d131a-183">Wanneer de basis-ER-indeling wordt uitgevoerd in de foutoplossingsmodus, wordt de indelingsbinding voor elk onderdeel vervangen door de binding die wordt weergegeven in de kolom **Binding**.</span><span class="sxs-lookup"><span data-stu-id="d131a-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="d131a-184">Selecteer **Bewerken** om de standaardbinding te wijzigen voor een onderdeel dat wordt weergegeven op het sneltabblad **Vervangingen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="d131a-185">Een nieuwe basislijnregel maken</span><span class="sxs-lookup"><span data-stu-id="d131a-185">Make a new baseline rule</span></span>

<span data-ttu-id="d131a-186">Volg de stappen in de sectie Voorbeeld: De instelling van basislijnregels automatiseren eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="d131a-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="d131a-187">Er wordt een melding weergegeven dat het uitgaande bestand is gegenereerd met behulp van basislijninstellingen en dat er een geforceerde vervanging van de indelingsbindingen heeft plaatsgevonden.</span><span class="sxs-lookup"><span data-stu-id="d131a-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="d131a-188">![Melding op de pagina Configuraties](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Schermafbeelding van de melding op de pagina Configuraties")</span><span class="sxs-lookup"><span data-stu-id="d131a-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="d131a-189">Waarschuwingen over het vervangen van indelingsbindingen onderdrukken</span><span class="sxs-lookup"><span data-stu-id="d131a-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="d131a-190">Door specifieke ER-parameters in te stellen, kunt u meldingen onderdrukken die waarschuwen bij het vervangen van indelingsbindingen.</span><span class="sxs-lookup"><span data-stu-id="d131a-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="d131a-191">Deze onderdrukking kan handig zijn indelingsbindingen in een modus zonder toezicht worden vervangen met behulp van Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="d131a-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="d131a-192">In dit geval kan de waarschuwing worden beschouwd als een fout van de testcase die wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d131a-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="d131a-193">Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** de optie **Gebruikersparameters**.</span><span class="sxs-lookup"><span data-stu-id="d131a-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="d131a-194">Stel de optie **Waarschuwingen voor basislijn** in op **Ja** en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d131a-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="d131a-195">Het gegenereerde basislijnbestand bekijken</span><span class="sxs-lookup"><span data-stu-id="d131a-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="d131a-196">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d131a-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d131a-197">Selecteer **Basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="d131a-198">Selecteer **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="d131a-199">Het gegenereerde bestand bevat de tekst voor de verwerkingsdatum en -tijd (**"#"**) uit de binding die is geconfigureerd in de toegevoegde basislijnregel, niet uit de binding van de indeling.</span><span class="sxs-lookup"><span data-stu-id="d131a-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="d131a-200">Sluit de pagina **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="d131a-201">De ontworpen ER-indeling uitvoeren en het logboek controleren om de resultaten te analyseren</span><span class="sxs-lookup"><span data-stu-id="d131a-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="d131a-202">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d131a-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d131a-203">Vouw in de structuur **Model voor leren van ER-basislijnen** uit.</span><span class="sxs-lookup"><span data-stu-id="d131a-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="d131a-204">Selecteer in de structuur de optie **Model voor leren van ER-basislijnen\\Indeling voor leren van ER-basislijnen**.</span><span class="sxs-lookup"><span data-stu-id="d131a-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="d131a-205">Selecteer op het sneltabblad **Versies** de optie **Uitvoeren**.</span><span class="sxs-lookup"><span data-stu-id="d131a-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="d131a-206">Geef in het veld **Id opgeven** het cijfer **1** op.</span><span class="sxs-lookup"><span data-stu-id="d131a-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="d131a-207">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="d131a-207">Select **OK**.</span></span>
7. <span data-ttu-id="d131a-208">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Foutopsporingslogboeken voor configuraties**.</span><span class="sxs-lookup"><span data-stu-id="d131a-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="d131a-209">Het uitvoeringslogboek bevat informatie over de resultaten van de vergelijking van het gegenereerde bestand met de geconfigureerde basislijn.</span><span class="sxs-lookup"><span data-stu-id="d131a-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="d131a-210">In het logboek wordt aangegeven dat het gegenereerde bestand en de basislijn overeenkomen, ook al bevat de uitgevoerde indelingen de binding om een steeds veranderende datum- en tijdwaarde in het uitgaande bestand in te voeren.</span><span class="sxs-lookup"><span data-stu-id="d131a-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="d131a-211">Hoewel het uitgaande bestand is gegenereerd met behulp van basislijninstellingen die de vervanging van de bindingen van de indeling forceren, ontvangt u geen waarschuwingen over de vervanging.</span><span class="sxs-lookup"><span data-stu-id="d131a-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="d131a-212">Basislijninstellingen tussen omgevingen uitwisselen</span><span class="sxs-lookup"><span data-stu-id="d131a-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="d131a-213">Basislijninstellingen exporteren</span><span class="sxs-lookup"><span data-stu-id="d131a-213">Export baseline settings</span></span>

<span data-ttu-id="d131a-214">Met de nieuwe ER-mogelijkheden kunt u basislijninstellingen voor de geselecteerde ER-indeling exporteren uit de huidige omgeving exporteren en deze opslaan als XML-bestanden.</span><span class="sxs-lookup"><span data-stu-id="d131a-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="d131a-215">Als u basislijninstellingen wilt exporteren, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="d131a-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="d131a-216">Basislijninstellingen importeren</span><span class="sxs-lookup"><span data-stu-id="d131a-216">Import baseline settings</span></span>

<span data-ttu-id="d131a-217">Geëxporteerde basislijninstellingen kunnen in een andere omgeving worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="d131a-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="d131a-218">De omgeving moet eerst worden geïmporteerd als ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="d131a-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="d131a-219">Vervolgens kunt u de basislijninstellingen importeren.</span><span class="sxs-lookup"><span data-stu-id="d131a-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="d131a-220">Als u basislijninstellingen vanuit een lokaal opgeslagen XML-bestand wilt importeren, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Importeren** en vervolgens selecteert u **Bladeren** om het XML-bestand te selecteren.</span><span class="sxs-lookup"><span data-stu-id="d131a-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="d131a-221">![Het dialoogvenster Basislijninstellingen importeren](media/GER-BaselineSample-ImportBaseline1.PNG "Schermafbeelding van het dialoogvenster Basislijninstellingen importeren")</span><span class="sxs-lookup"><span data-stu-id="d131a-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="d131a-222">Als u basislijninstellingen wilt importeren vanuit een XML-bestand dat op de Microsoft SharePoint-server is opgeslagen, op basis van de huidige instellingen voor documentbeheer en het geselecteerde documenttype, selecteert u op de pagina **Basislijnen voor ER-indeling** de optie **Importeren uit bron**.</span><span class="sxs-lookup"><span data-stu-id="d131a-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="d131a-223">Selecteer het documenttype en het XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="d131a-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="d131a-224">Het vereiste documenttype voor toegang tot de SharePoint-map moet vooraf worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="d131a-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="d131a-225">![Het dialoogvenster Importeren uit bron](media/GER-BaselineSample-ImportBaseline2.PNG "Schermafbeelding van het dialoogvenster Importeren uit bron")</span><span class="sxs-lookup"><span data-stu-id="d131a-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="d131a-226">U kunt Taakregistratie gebruiken om de stappen vast te leggen voor het selecteren van het vereiste documenttype en de bestandsnaam in het dialoogvenster **Importeren vanuit bron**.</span><span class="sxs-lookup"><span data-stu-id="d131a-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="d131a-227">Op deze manier kunt u de vereiste basislijninstellingen op de SharePoint-server behouden en deze vervolgens automatisch importeren door een taakregistratie af te spelen wanneer u automatische tests uitvoert met behulp van Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="d131a-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d131a-228">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d131a-228">Additional resources</span></span>

- [<span data-ttu-id="d131a-229">Gegenereerde rapportresultaten volgen en vergelijken met de basislijnwaarden</span><span class="sxs-lookup"><span data-stu-id="d131a-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="d131a-230">Resources voor Taakrecorder</span><span class="sxs-lookup"><span data-stu-id="d131a-230">Task recorder resources</span></span>](../user-interface/task-recorder.md)
