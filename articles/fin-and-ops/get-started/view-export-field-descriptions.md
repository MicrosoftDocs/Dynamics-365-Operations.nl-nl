---
title: Veldomschrijvingen weergeven en exporteren
description: In dit artikel wordt beschreven hoe veldbeschrijvingen worden weergegeven en hoe de pagina Veldbeschrijvingen kan worden gebruikt van om beschrijvingen te exporteren.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d1ee87dbe9dab089a893d9c69d2573a4c4b11b58
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="be47c-103">Veldomschrijvingen weergeven en exporteren</span><span class="sxs-lookup"><span data-stu-id="be47c-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be47c-104">In dit artikel wordt beschreven hoe veldbeschrijvingen worden weergegeven en hoe de pagina Veldbeschrijvingen kan worden gebruikt van om beschrijvingen te exporteren.</span><span class="sxs-lookup"><span data-stu-id="be47c-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="be47c-105">Microsoft Dynamics 365 for Finance and Operations bevat beschrijvingen voor enkele van de complexere velden.</span><span class="sxs-lookup"><span data-stu-id="be47c-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="be47c-106">Deze beschrijvingen worden weergegeven wanneer u de muisaanwijzer op een veld plaatst.</span><span class="sxs-lookup"><span data-stu-id="be47c-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="be47c-107">U kunt ook beschrijvingen weergeven en exporteren op de pagina **Veldbeschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="be47c-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="be47c-108">Niet alle pagina's hebben veldomschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="be47c-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="be47c-109">We willen alleen beschrijvingen geven voor de complexere velden en niet voor de velden waarvoor het gebruik duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="be47c-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="be47c-110">Daarom hebben sommige pagina's geen veldbeschrijvingen, sommige pagina's een paar beschrijvingen en sommige van de meer complexe pagina's, zoals veel van de pagina's met parameters, veel beschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="be47c-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="be47c-111">Als u toegang hebt tot de Finance and Operations-ontwikkelomgeving, kunt u nieuwe veldbeschrijvingen toevoegen en bestaande beschrijvingen aanpassen.</span><span class="sxs-lookup"><span data-stu-id="be47c-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="be47c-112">U kunt bijvoorbeeld bedrijfsspecifieke informatie toevoegen aan een veldbeschrijving.</span><span class="sxs-lookup"><span data-stu-id="be47c-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="be47c-113">Zie [Help voor velden aanpassen](../../dev-itpro/user-interface/customize-field-help.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="be47c-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="be47c-114">Zie veldbeschrijvingen in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="be47c-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="be47c-115">U kunt veldomschrijvingen weergeven door de cursor boven een veld te houden.</span><span class="sxs-lookup"><span data-stu-id="be47c-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="be47c-116">Als er geen beschrijving beschikbaar is, ziet u de veldnaam wanneer u de muisaanwijzer op het veld plaatst.</span><span class="sxs-lookup"><span data-stu-id="be47c-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="be47c-117">(Opmerking: In versie Dynamics AX 7.0.0 (februari 2016) kunnen veldbeschrijvingen alleen worden weergegeven op de pagina **Veldomschrijvingen**.) In de volgende afbeelding ziet u de beschrijving die wordt weergegeven wanneer u de muisaanwijzer op het veld **Artikelen vergrendelen tijdens telling** plaatst.</span><span class="sxs-lookup"><span data-stu-id="be47c-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="be47c-118">[![Voorbeeld van een veldbeschrijving](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="be47c-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="be47c-119">De pagina Veldbeschrijvingen gebruiken om Help voor velden weer te geven en te exporteren</span><span class="sxs-lookup"><span data-stu-id="be47c-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="be47c-120">Op de pagina **Veldbeschrijvingen** kunt u veldbeschrijvingen weergeven en exporteren.</span><span class="sxs-lookup"><span data-stu-id="be47c-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="be47c-121">U kunt de omschrijvingen zien die tegelijk voor een pagina beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="be47c-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="be47c-122">De omschrijvingen voor een pagina weergeven</span><span class="sxs-lookup"><span data-stu-id="be47c-122">View the descriptions for a page</span></span>

<span data-ttu-id="be47c-123">Volg deze stap om de beschrijvingen voor een pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="be47c-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="be47c-124">Typ de naam van de pagina in het veld **Selecteer een pagina**.</span><span class="sxs-lookup"><span data-stu-id="be47c-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="be47c-125">Of klik op de pijl om een lijst van alle pagina's te openen en blader of filter de lijst.</span><span class="sxs-lookup"><span data-stu-id="be47c-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="be47c-126">U kunt de naam van de pagina gebruiken die in de gebruikersinterface (UI) wordt weergegeven (bijvoorbeeld **Klanten**) of de codenaam (AOT-naam) die u kunt zien door met de rechtermuisknop op een pagina te klikken (bijvoorbeeld **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="be47c-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="be47c-127">Zie de sectie 'Zoeken naar een pagina' verderop in dit artikel voor meer informatie over de verschillende manieren om de lijst met pagina's te filteren.</span><span class="sxs-lookup"><span data-stu-id="be47c-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="be47c-128">Als u de optie **Velden zonder beschrijving opnemen** instelt op **Ja**, worden alle velden op de pagina weergegeven, ongeacht of ze al dan niet een veldbeschrijving hebben.</span><span class="sxs-lookup"><span data-stu-id="be47c-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="be47c-129">De omschrijvingen voor een pagina exporteren</span><span class="sxs-lookup"><span data-stu-id="be47c-129">Export the descriptions for a page</span></span>

<span data-ttu-id="be47c-130">Volg deze stappen om de beschrijvingen voor een pagina te exporteren.</span><span class="sxs-lookup"><span data-stu-id="be47c-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="be47c-131">Selecteer een pagina in het veld **Selecteer een pagina**.</span><span class="sxs-lookup"><span data-stu-id="be47c-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="be47c-132">Klik op de knop **Openen in Microsoft Office** in de rechterbovenhoek en klik vervolgens op **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="be47c-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="be47c-133">Zoeken naar een pagina</span><span class="sxs-lookup"><span data-stu-id="be47c-133">Searching for a page</span></span>

<span data-ttu-id="be47c-134">Er zijn verschillende manieren om een pagina te zoeken in het veld **Selecteer een pagina**.</span><span class="sxs-lookup"><span data-stu-id="be47c-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="be47c-135">In veel gevallen moet u op de pijl in het veld **Selecteer een pagina** klikken om de vervolgkeuzelijst te openen en vervolgens uit een gefilterde lijst met pagina's een keuze maken.</span><span class="sxs-lookup"><span data-stu-id="be47c-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="be47c-136">Typ een deel van de naam en open vervolgens een vervolgkeuzelijst om te selecteren uit een gefilterde lijst met pagina's.</span><span class="sxs-lookup"><span data-stu-id="be47c-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="be47c-137">Open de vervolgkeuzelijst en klik vervolgens op de kop **Paginanaam** boven aan de lijst of op de kop **AOT-naam van pagina**.</span><span class="sxs-lookup"><span data-stu-id="be47c-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="be47c-138">Er wordt een dialoogvenster weergegeven waarin u geavanceerde filteropties kunt gebruiken, zoals **Paginanaam begint met**.</span><span class="sxs-lookup"><span data-stu-id="be47c-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="be47c-139">Typ de volledige naam van de pagina.</span><span class="sxs-lookup"><span data-stu-id="be47c-139">Type the full name of the page.</span></span> <span data-ttu-id="be47c-140">Als u deze optie gebruikt, kunt u het beste de vervolgkeuzelijst openen en bekijken wat er nog meer in de lijst staat, zelfs of veldbeschrijvingen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="be47c-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="be47c-141">Als er een enkele exacte overeenkomst met de naam is, worden de veldomschrijvingen voor die pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="be47c-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="be47c-142">Als er meer dan één exacte overeenkomst is, worden geen beschrijvingen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="be47c-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="be47c-143">U moet de vervolgkeuzelijst openen en de gewenste pagina selecteren.</span><span class="sxs-lookup"><span data-stu-id="be47c-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="be47c-144">Als de naam die u hebt getypt deel uitmaakt van de naam van een andere pagina, ziet u de beschrijvingen voor uw pagina.</span><span class="sxs-lookup"><span data-stu-id="be47c-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="be47c-145">Als u echter de vervolgkeuzelijst opent, ziet u extra pagina's die deze naam bevatten.</span><span class="sxs-lookup"><span data-stu-id="be47c-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="be47c-146">Zo worden er bijvoorbeeld geen beschrijvingen weergegeven wanneer u <strong>telling</strong> typt in het veld *<strong><em>Selecteer een pagina</em></strong>*.</span><span class="sxs-lookup"><span data-stu-id="be47c-146">For example, no descriptions are shown when you type <strong>Counting</strong> in the *<strong><em>Select a page</em></strong>* field.</span></span> <span data-ttu-id="be47c-147">U opent de vervolgkeuzelijst en ziet dat er twee pagina's zijn met de naam <strong>Counting</strong>, plus verschillende pagina's die het woord "Telling" bevatten in de naam.</span><span class="sxs-lookup"><span data-stu-id="be47c-147">You open the drop-down list, and see that there are two pages that have the name <strong>Counting</strong> and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="be47c-148">Als u de pagina met de AOT-naam <strong>InventJournalCountt</strong> selecteert, worden de veldbeschrijvingen voor die pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="be47c-148">If you select the page that has the AOT name <strong>InventJournalCount</strong>, the field descriptions are shown for that page.</span></span> <span data-ttu-id="be47c-149">Als u echter de vervolgkeuzelijst opnieuw opent, ziet u dat de lijst nu alle pagina's bevat met "InventJournalCount" als deel van de AOT-naam.</span><span class="sxs-lookup"><span data-stu-id="be47c-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="be47c-150">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="be47c-150">Troubleshooting</span></span>
<span data-ttu-id="be47c-151">Deze sectie bevat informatie om u te helpen problemen op te lossen die u kunt tegenkomen als u veldbeschrijvingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="be47c-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="be47c-152">Ik kan geen veldomschrijving vinden</span><span class="sxs-lookup"><span data-stu-id="be47c-152">I can't find a field description</span></span>

<span data-ttu-id="be47c-153">We zijn bezig met het toevoegen van omschrijvingen voor de complexere velden.</span><span class="sxs-lookup"><span data-stu-id="be47c-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="be47c-154">Als u hulp nodig hebt voor een bepaald veld, laat dit ons dan weten door een opmerking voor dit onderwerp toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="be47c-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="be47c-155">De veldomschrijving is niet nuttig</span><span class="sxs-lookup"><span data-stu-id="be47c-155">The field description isn't helpful</span></span>

<span data-ttu-id="be47c-156">Laat ons dit weten door een opmerking voor dit onderwerp toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="be47c-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="be47c-157">Beschrijf, indien mogelijk, de aanvullende informatie die u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="be47c-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="be47c-158">Ik kan een veld op de pagina in Veldbeschrijvingen niet vinden.</span><span class="sxs-lookup"><span data-stu-id="be47c-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="be47c-159">Als u alle velden op een pagina wilt weergeven, stelt u de optie **Velden zonder beschrijving opnemen** in op **Ja.**</span><span class="sxs-lookup"><span data-stu-id="be47c-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="be47c-160">Klik op het veld **Selecteer een pagina** om te controleren of u de juiste pagina hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="be47c-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="be47c-161">Als de naam die u hebt getypt deel uitmaakt van een andere veldnaam, hebt u mogelijk de pagina met de langere naam geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="be47c-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="be47c-162">Ik kan een pagina op de pagina Veldbeschrijvingen niet vinden.</span><span class="sxs-lookup"><span data-stu-id="be47c-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="be47c-163">Zie de sectie 'Zoeken naar pagina's' eerder in dit artikel voor meer informatie over de verschillende manieren om pagina's te zoeken.</span><span class="sxs-lookup"><span data-stu-id="be47c-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="be47c-164">Als u de exacte naam van de pagina hebt ingevoerd, worden de veldbeschrijvingen mogelijk niet weergegeven als er meer dan één pagina met dezelfde naam is.</span><span class="sxs-lookup"><span data-stu-id="be47c-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="be47c-165">Klik op de pijl in het veld **Selecteer een pagina** als u een gefilterde lijst met de beschikbare pagina's wilt openen.</span><span class="sxs-lookup"><span data-stu-id="be47c-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="additional-resources"></a><span data-ttu-id="be47c-166">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="be47c-166">Additional resources</span></span>
--------

[<span data-ttu-id="be47c-167">Help voor velden aanpassen</span><span class="sxs-lookup"><span data-stu-id="be47c-167">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)





