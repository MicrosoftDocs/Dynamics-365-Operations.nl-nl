---
title: Problemen met voorraadbewerkingen oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met voorraadbewerkingen.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: ee1bfbf1b5aa736e1ee5bd38403b6c94c2bd036b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224997"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="227ad-103">Problemen met voorraadbewerkingen oplossen</span><span class="sxs-lookup"><span data-stu-id="227ad-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="227ad-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met voorraadbewerkingen.</span><span class="sxs-lookup"><span data-stu-id="227ad-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="227ad-105">Ik kan het dialoogvenster met vervolgkeuzemenu "Werkstroom" niet vinden voor voorraadjournalen.</span><span class="sxs-lookup"><span data-stu-id="227ad-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="227ad-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="227ad-106">Issue description</span></span>

<span data-ttu-id="227ad-107">U kunt het vervolgkeuzedialoogvenster **Werkstroom** niet vinden op de journaalpagina of er zijn geen gerelateerde werkstroombewerkingen beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="227ad-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="227ad-108">Dit probleem kan om drie redenen optreden, zoals wordt beschreven in de volgende subsecties.</span><span class="sxs-lookup"><span data-stu-id="227ad-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="227ad-109">Probleemoplossing 1</span><span class="sxs-lookup"><span data-stu-id="227ad-109">Issue resolution 1</span></span>

<span data-ttu-id="227ad-110">Als het probleem voor alle gebruikers geldt, kan het komen doordat de goedkeuringswerkstroom niet aan de journaalnaam is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="227ad-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="227ad-111">Volg deze stappen om het probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="227ad-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="227ad-112">Ga naar **Voorraadbeheer &gt; Instellingen &gt; Journaalnamen &gt; Voorraad**.</span><span class="sxs-lookup"><span data-stu-id="227ad-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="227ad-113">Selecteer een journaalnaam in het lijstdeelvenster om de bijbehorende instellingen te openen.</span><span class="sxs-lookup"><span data-stu-id="227ad-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="227ad-114">Stel op het sneltabblad **Algemeen** de optie **Goedkeuringswerkstroom** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="227ad-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="227ad-115">Selecteer **Ja** als u wordt gevraagd de wijziging te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="227ad-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="227ad-116">Selecteer in het veld **Werkstroom** de werkstroom die u voor de geselecteerde journaalnaam wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="227ad-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="227ad-117">Probleemoplossing 2</span><span class="sxs-lookup"><span data-stu-id="227ad-117">Issue resolution 2</span></span>

<span data-ttu-id="227ad-118">Als in uw werkstroom aangepaste code wordt gebruikt, kunnen problemen optreden nadat u een upgrade op het systeem hebt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="227ad-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="227ad-119">In de journaalwerkstroom is het bijvoorbeeld mogelijk dat de knop **Indienen** grijs wordt weergegeven, zodat u deze niet kunt selecteren om een indiening goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="227ad-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="227ad-120">Als de knop **Indienen** grijs wordt weergegeven, is uw werkstroom mogelijk aangepast. Dit houdt in dat de methode van de werkstroom, `canSubmitToWorkflow()` in `FormDataUtil` is uitgebreid.</span><span class="sxs-lookup"><span data-stu-id="227ad-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="227ad-121">Om dit probleem op te lossen, wijzigt u de manier waarop u de methode van `canSubmitToWorkflow()` uitbreidt om de structuur in het volgende voorbeeld te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="227ad-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="227ad-122">Probleemoplossing 3</span><span class="sxs-lookup"><span data-stu-id="227ad-122">Issue resolution 3</span></span>

<span data-ttu-id="227ad-123">Als het probleem alleen voor een paar specifieke gebruikers geldt, beschikken deze gebruikers mogelijk niet over de beveiligingsbevoegdheden die zijn vereist om werkstroombewerkingen uit te voeren op voorraadjournalen.</span><span class="sxs-lookup"><span data-stu-id="227ad-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="227ad-124">Controleer of elke betrokken gebruiker beschikt over de beveiligingsbevoegdheid *Werkstroom voorraadjournaal onderhouden*.</span><span class="sxs-lookup"><span data-stu-id="227ad-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="227ad-125">Standaard wordt deze bevoegdheid toegewezen aan een taak met dezelfde naam en die taak wordt toegepast op de rollen *Magazijnmedewerker* en *Magazijnbeheerder*.</span><span class="sxs-lookup"><span data-stu-id="227ad-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="227ad-126">Mijn voorraadjournaal blijft in een door het systeem vergrendelde status en de werkstroombatchtaak werkt niet.</span><span class="sxs-lookup"><span data-stu-id="227ad-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="227ad-127">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="227ad-127">Issue description</span></span>

<span data-ttu-id="227ad-128">Een van uw voorraadjournalen wordt vergrendeld door een bepaalde bewerking en wordt niet vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="227ad-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="227ad-129">Als er bijvoorbeeld een onbekende fout optreedt tijdens het boeken (wat een systeemvergrendelingsbewerking is), blijft het journaal mogelijk in de door het systeem vergrendelde status.</span><span class="sxs-lookup"><span data-stu-id="227ad-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="227ad-130">In dit geval wordt met de handler van het werkstroomwerkitem een fout gegenereerd terwijl de validatie wordt vergrendeld.</span><span class="sxs-lookup"><span data-stu-id="227ad-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="227ad-131">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="227ad-131">Issue resolution</span></span>

<span data-ttu-id="227ad-132">Meld u aan bij het SQL Server-exemplaar voor Supply Chain Management en controleer of **InventJournalTable.SystemBlocked** is ingesteld op *1*.</span><span class="sxs-lookup"><span data-stu-id="227ad-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="227ad-133">Als dat het geval is, zorg er dan voor dat de status van het journaal niet vergrendeld is en stel vervolgens **InventJournalTable.SystemBlocked** in op *0*.</span><span class="sxs-lookup"><span data-stu-id="227ad-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="227ad-134">Mijn voorraadjournaalwerkstroom wordt nooit voltooid en het journaal kan niet worden bewerkt of geboekt.</span><span class="sxs-lookup"><span data-stu-id="227ad-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="227ad-135">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="227ad-135">Issue description</span></span>

<span data-ttu-id="227ad-136">Nadat u een journaalgoedkeuringswerkstroom hebt ingediend, reageert de werkstroomverwerking niet meer en kunt u uw journalen niet bewerken of verwerken.</span><span class="sxs-lookup"><span data-stu-id="227ad-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="227ad-137">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="227ad-137">Issue resolution</span></span>

<span data-ttu-id="227ad-138">Er zijn verschillende redenen waarom de verwerking van werkstromen niet kan worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="227ad-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="227ad-139">Controleer op de volgende problemen:</span><span class="sxs-lookup"><span data-stu-id="227ad-139">Check for the following issues:</span></span>

- <span data-ttu-id="227ad-140">Ga naar **Voorraadbeheer &gt; Instellingen &gt; Voorraadbeheerwerkstromen** en controleer de configuratie van de betrokken werkstroom.</span><span class="sxs-lookup"><span data-stu-id="227ad-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="227ad-141">Zie [Goedkeuringswerkstromen van voorraadjournalen](inventory-journal-workflow.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="227ad-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="227ad-142">Mogelijk komt een uitzondering of fout in de werkstroom voor.</span><span class="sxs-lookup"><span data-stu-id="227ad-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="227ad-143">Controleer de werkitemhistorie van de betrokken werkstroom om te zien of er een toepassingsfout is betrokken bij het beëindigen van de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="227ad-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="227ad-144">Het voorraadjournaal kan alleen worden bijgewerkt of bewerkt als het is goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="227ad-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="227ad-145">Als terugroepen actief is, kunt u proberen het journaal terug te roepen.</span><span class="sxs-lookup"><span data-stu-id="227ad-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="227ad-146">De uitvoering van de werkstroombatchtaak kan om meerdere redenen zijn uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="227ad-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="227ad-147">Een aantal van deze redenen kan worden veroorzaakt door het probleem met het werkstroomraamwerk.</span><span class="sxs-lookup"><span data-stu-id="227ad-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="227ad-148">Werkstroomvoorwaarden voor voorraadjournaal zijn alleen van toepassing op journaalniveau, niet op regelniveau</span><span class="sxs-lookup"><span data-stu-id="227ad-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="227ad-149">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="227ad-149">Issue description</span></span>

<span data-ttu-id="227ad-150">Dit probleem kan zich bijvoorbeeld voordoen als u probeert een werkstroomvoorwaarde voor het voorraadjournaal in te stellen voor het kostenbedrag.</span><span class="sxs-lookup"><span data-stu-id="227ad-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="227ad-151">U stelt de voorwaarde zo in dat stap 1 alleen wordt uitgevoerd wanneer het kostenbedrag lager is dan 100.</span><span class="sxs-lookup"><span data-stu-id="227ad-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="227ad-152">U stelt vervolgens een andere voorwaarde in zodat stap 2 alleen wordt uitgevoerd wanneer het kostenbedrag meer is dan of gelijk is aan 100.</span><span class="sxs-lookup"><span data-stu-id="227ad-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="227ad-153">Wanneer de werkstroom wordt uitgevoerd, wordt in de werkstroomhistorie slechts één regel weergegeven en wordt de eerste voorwaarde altijd als *waar* geëvalueerd, ongeacht de waarde die wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="227ad-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="227ad-154">Tijdelijke oplossing voor probleem</span><span class="sxs-lookup"><span data-stu-id="227ad-154">Issue workaround</span></span>

<span data-ttu-id="227ad-155">In de huidige versie zijn werkstroomvoorwaarden voor de voorraad alleen van toepassing op journaalniveau, niet op regelniveau.</span><span class="sxs-lookup"><span data-stu-id="227ad-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="227ad-156">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="227ad-156">This behavior is by design.</span></span> <span data-ttu-id="227ad-157">We raden u aan om uw voorwaardecriteria alleen in te stellen op kenmerken op journaalniveau.</span><span class="sxs-lookup"><span data-stu-id="227ad-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="227ad-158">In het filterdeelvenster van de pagina Voorhanden voorraad worden de resultaten niet gefilterd als verwacht.</span><span class="sxs-lookup"><span data-stu-id="227ad-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="227ad-159">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="227ad-159">Issue description</span></span>

<span data-ttu-id="227ad-160">Met de filters in het filterdeelvenster op de pagina **Voorhanden voorraad**  worden de resultaten niet gefilterd als verwacht.</span><span class="sxs-lookup"><span data-stu-id="227ad-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="227ad-161">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="227ad-161">Issue resolution</span></span>

<span data-ttu-id="227ad-162">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="227ad-162">This behavior is by design.</span></span>

<span data-ttu-id="227ad-163">De pagina  **Voorhanden voorraad**  wordt samengesteld uit een gedetailleerde tabel met voorhanden voorraad waarin alle beschikbare dimensies zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="227ad-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="227ad-164">De lijst op deze pagina is echter een overzicht.</span><span class="sxs-lookup"><span data-stu-id="227ad-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="227ad-165">Daarom kunnen rijen uit de brontabel worden gecombineerd door waarden te aggregeren op basis van de dimensies die worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="227ad-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="227ad-166">De filters die in het filterdeelvenster zijn ingesteld, zijn van toepassing op de brontabel en niet op de samengevoegde lijst.</span><span class="sxs-lookup"><span data-stu-id="227ad-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="227ad-167">Dit gedrag kan soms onverwachte resultaten opleveren, zoals in [deze voorbeelden](inventory-on-hand-list.md#examples) wordt getoond.</span><span class="sxs-lookup"><span data-stu-id="227ad-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="227ad-168">De  [filters die in het raster worden vermeld](inventory-on-hand-list.md#grid-filters) hebben echter  *wel*  betrekking op de samengevoegde lijst.</span><span class="sxs-lookup"><span data-stu-id="227ad-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="227ad-169">Deze filters bevatten zowel het snelfilter boven aan het raster als het filter voor elke kolomkop.</span><span class="sxs-lookup"><span data-stu-id="227ad-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="227ad-170">De eenheid en hoeveelheid per eenheid werken niet goed in het voorraadjournaal.</span><span class="sxs-lookup"><span data-stu-id="227ad-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="227ad-171">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="227ad-171">Issue description</span></span>

<span data-ttu-id="227ad-172">Er kunnen een of meer van de volgende problemen voorkomen wanneer u met eenheden en hoeveelheden in een voorraadjournaal werkt:</span><span class="sxs-lookup"><span data-stu-id="227ad-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="227ad-173">U ziet geen eenheden of eenheidshoeveelheden in het voorraadjournaal terwijl er een omrekeningseenheid is ingesteld voor het vrijgegeven product en u kunt de eenheid niet wijzigen in het voorraadjournaal.</span><span class="sxs-lookup"><span data-stu-id="227ad-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="227ad-174">U ziet de velden **Hoeveelheid** en **Eenheid** in het voorraadjournaal, maar het veld **Hoeveelheid per eenheid** niet.</span><span class="sxs-lookup"><span data-stu-id="227ad-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="227ad-175">Als u de eenheid wijzigt, een hoeveelheid invoert en het journaal boekt, wordt in het journaal nog steeds de oorspronkelijke maateenheid voor die hoeveelheid gebruikt.</span><span class="sxs-lookup"><span data-stu-id="227ad-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="227ad-176">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="227ad-176">Issue resolution</span></span>

<span data-ttu-id="227ad-177">Volg deze stappen om dit probleem op te lossen.</span><span class="sxs-lookup"><span data-stu-id="227ad-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="227ad-178">Zorg er in het werkgebied **Functiebeheer** voor dat de functie *Maateenheid en hoeveelheid per eenheid in voorraadjournalen gebruiken* is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="227ad-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="227ad-179">Met deze functie voegt u de velden **Eenheid** en **Hoeveelheid per eenheid** aan het journaal toe.</span><span class="sxs-lookup"><span data-stu-id="227ad-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="227ad-180">Nadat de functie is ingeschakeld, gebruikt u de velden **Hoeveelheid**, **Hoeveelheid per eenheid** en **Eenheid** als volgt:</span><span class="sxs-lookup"><span data-stu-id="227ad-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="227ad-181">**Hoeveelheid**: geef de hoeveelheid op door de standaardeenheid te gebruiken die voor het vrijgegeven product is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="227ad-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="227ad-182">De standaardeenheid zelf wordt hier echter niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="227ad-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="227ad-183">Als er een omrekening is ingesteld tussen de standaardeenheid en de eenheid die is geselecteerd in het veld **Eenheid**, wordt het veld **Hoeveelheid** automatisch bijgewerkt op basis van de selecties in de velden **Hoeveelheid per eenheid** en **Eenheid**.</span><span class="sxs-lookup"><span data-stu-id="227ad-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="227ad-184">**Hoeveelheid per eenheid**: geef de hoeveelheid op met behulp van de eenheid die is geselecteerd in het veld **Eenheid**.</span><span class="sxs-lookup"><span data-stu-id="227ad-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="227ad-185">**Eenheid**: selecteer de eenheid die moet worden toegepast op de waarde in het veld **Hoeveelheid per eenheid**.</span><span class="sxs-lookup"><span data-stu-id="227ad-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="227ad-186">Het volgende foutbericht wordt weergegeven: "Het maximum aantal decimalen voor de voorraadeenheid is 0."</span><span class="sxs-lookup"><span data-stu-id="227ad-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="227ad-187">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="227ad-187">Issue description</span></span>

<span data-ttu-id="227ad-188">Wanneer u een voorraadtransactie of voorraadreservering probeert te boeken, wordt het volgende foutbericht weergegeven: "Het maximum aantal decimalen voor de voorraadeenheid is 0."</span><span class="sxs-lookup"><span data-stu-id="227ad-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="227ad-189">Dit probleem treedt op wanneer de voorraadtransactiehoeveelheid is opgegeven als een decimale waarde die onder het nauwkeurigheidsniveau ligt dat het veld ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="227ad-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="227ad-190">Er is bijvoorbeeld een hoeveelheid van *0,5* opgegeven voor een voorraadtransactie, maar alleen de hoeveelheden in de vorm van een geheel getal worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="227ad-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="227ad-191">Daarom moet de waarde *1* zijn in plaats van *0,5*.</span><span class="sxs-lookup"><span data-stu-id="227ad-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="227ad-192">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="227ad-192">Issue resolution</span></span>

1. <span data-ttu-id="227ad-193">Voer het volgende script op uw SQL Server-exemplaar uit om hoeveelheden in de voorraadtransacties af te ronden.</span><span class="sxs-lookup"><span data-stu-id="227ad-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="227ad-194">Met dit script corrigeert u waarden in de tabel **inventTrans**.</span><span class="sxs-lookup"><span data-stu-id="227ad-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="227ad-195">Voer een handmatige consistentiecontrole uit waarbij de optie **Fout oplossen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="227ad-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="227ad-196">Met deze controle worden waarden in de tabel **inventSum** gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="227ad-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="227ad-197">Het is raadzaam het script zorgvuldig te bewerken voor uw omgeving, het te testen in een testomgeving en vervolgens de resulterende gegevens te controleren voordat u het script in een productieomgeving uitvoert.</span><span class="sxs-lookup"><span data-stu-id="227ad-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]