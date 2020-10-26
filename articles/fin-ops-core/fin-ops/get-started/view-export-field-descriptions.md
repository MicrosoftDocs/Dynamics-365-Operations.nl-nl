---
title: Veldomschrijvingen weergeven en exporteren
description: In dit artikel wordt beschreven hoe veldbeschrijvingen worden weergegeven en hoe de pagina Veldbeschrijvingen kan worden gebruikt van om beschrijvingen te exporteren.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 147dc55160de7d3cc01cc077095d2eb71f4d7861
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978173"
---
# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="4d63a-103">Veldomschrijvingen weergeven en exporteren</span><span class="sxs-lookup"><span data-stu-id="4d63a-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d63a-104">In dit artikel wordt beschreven hoe veldbeschrijvingen worden weergegeven en hoe de pagina Veldbeschrijvingen kan worden gebruikt van om beschrijvingen te exporteren.</span><span class="sxs-lookup"><span data-stu-id="4d63a-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="4d63a-105">Enkele van de complexere velden hebben veldbeschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="4d63a-105">Some of the more complex fields have field descriptions.</span></span> <span data-ttu-id="4d63a-106">Deze beschrijvingen worden weergegeven wanneer u de muisaanwijzer op een veld plaatst.</span><span class="sxs-lookup"><span data-stu-id="4d63a-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="4d63a-107">U kunt ook beschrijvingen weergeven en exporteren op de pagina **Veldbeschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-107">You can also view and export descriptions on the **Field descriptions** page.</span></span>

<span data-ttu-id="4d63a-108">Niet alle pagina's hebben veldomschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="4d63a-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="4d63a-109">We willen alleen beschrijvingen geven voor de complexere velden en niet voor de velden waarvoor het gebruik duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="4d63a-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="4d63a-110">Daarom hebben sommige pagina's geen veldbeschrijvingen, sommige pagina's een paar beschrijvingen en sommige van de meer complexe pagina's, zoals veel van de pagina's met parameters, veel beschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="4d63a-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span>

<span data-ttu-id="4d63a-111">Als u toegang hebt tot de ontwikkelomgeving kunt u nieuwe veldbeschrijvingen toevoegen en bestaande beschrijvingen aanpassen.</span><span class="sxs-lookup"><span data-stu-id="4d63a-111">If you have access to the development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="4d63a-112">U kunt bijvoorbeeld bedrijfsspecifieke informatie toevoegen aan een veldbeschrijving.</span><span class="sxs-lookup"><span data-stu-id="4d63a-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="4d63a-113">Zie [Veldbeschrijvingen aanpassen](../../dev-itpro/user-interface/customize-field-help.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4d63a-113">For more information, see [Customize field descriptions](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="4d63a-114">Zie veldbeschrijvingen in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="4d63a-114">See field descriptions in the user interface</span></span>

<span data-ttu-id="4d63a-115">U kunt veldomschrijvingen weergeven door de cursor boven een veld te houden.</span><span class="sxs-lookup"><span data-stu-id="4d63a-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="4d63a-116">Als er geen beschrijving beschikbaar is, ziet u de veldnaam wanneer u de muisaanwijzer op het veld plaatst.</span><span class="sxs-lookup"><span data-stu-id="4d63a-116">If no description is available, you see the field name when you hover over the field.</span></span>

> [!NOTE]
> <span data-ttu-id="4d63a-117">In Dynamics AX 7.0 (februari 2016) kunnen veldbeschrijvingen alleen worden bekeken op de pagina **Veldbeschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-117">In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.</span></span>

<span data-ttu-id="4d63a-118">In de volgende afbeelding ziet u de beschrijving die wordt weergegeven wanneer u de muisaanwijzer op het veld **Artikelen vergrendelen tijdens telling** plaatst.</span><span class="sxs-lookup"><span data-stu-id="4d63a-118">The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span>

<span data-ttu-id="4d63a-119">[![Voorbeeld van een veldbeschrijving](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="4d63a-119">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="4d63a-120">De pagina Veldbeschrijvingen gebruiken om Help voor velden weer te geven en te exporteren</span><span class="sxs-lookup"><span data-stu-id="4d63a-120">Use the Field descriptions page to view and export field help</span></span>

<span data-ttu-id="4d63a-121">Op de pagina **Veldbeschrijvingen** kunt u veldbeschrijvingen weergeven en exporteren.</span><span class="sxs-lookup"><span data-stu-id="4d63a-121">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="4d63a-122">U kunt de omschrijvingen zien die tegelijk voor een pagina beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="4d63a-122">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="4d63a-123">De omschrijvingen voor een pagina weergeven</span><span class="sxs-lookup"><span data-stu-id="4d63a-123">View the descriptions for a page</span></span>

<span data-ttu-id="4d63a-124">Volg deze stap om de beschrijvingen voor een pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="4d63a-124">To view the descriptions for a page, follow this step.</span></span>

- <span data-ttu-id="4d63a-125">Typ de naam van de pagina in het veld **Selecteer een pagina**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-125">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="4d63a-126">Of klik op de pijl om een lijst van alle pagina's te openen en blader of filter de lijst.</span><span class="sxs-lookup"><span data-stu-id="4d63a-126">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="4d63a-127">U kunt de naam van de pagina gebruiken die in de gebruikersinterface (UI) wordt weergegeven (bijvoorbeeld **Klanten**) of de codenaam (AOT-naam) die u kunt zien door met de rechtermuisknop op een pagina te klikken (bijvoorbeeld **CustTable**).</span><span class="sxs-lookup"><span data-stu-id="4d63a-127">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span>

<span data-ttu-id="4d63a-128">Zie de sectie 'Zoeken naar een pagina' verderop in dit artikel voor meer informatie over de verschillende manieren om de lijst met pagina's te filteren.</span><span class="sxs-lookup"><span data-stu-id="4d63a-128">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span>

<span data-ttu-id="4d63a-129">Als u de optie **Velden zonder beschrijving opnemen** instelt op **Ja**, worden alle velden op de pagina weergegeven, ongeacht of ze al dan niet een veldbeschrijving hebben.</span><span class="sxs-lookup"><span data-stu-id="4d63a-129">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="4d63a-130">De omschrijvingen voor een pagina exporteren</span><span class="sxs-lookup"><span data-stu-id="4d63a-130">Export the descriptions for a page</span></span>

<span data-ttu-id="4d63a-131">Volg deze stappen om de beschrijvingen voor een pagina te exporteren.</span><span class="sxs-lookup"><span data-stu-id="4d63a-131">To export the descriptions for a page, follow these steps.</span></span>

1. <span data-ttu-id="4d63a-132">Selecteer een pagina in het veld **Selecteer een pagina**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-132">In the **Select a page** field, select a page.</span></span>
2. <span data-ttu-id="4d63a-133">Klik op de knop **Openen in Microsoft Office** in de rechterbovenhoek en klik vervolgens op **FieldDescriptionTmp**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-133">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="4d63a-134">Zoeken naar een pagina</span><span class="sxs-lookup"><span data-stu-id="4d63a-134">Searching for a page</span></span>

<span data-ttu-id="4d63a-135">Er zijn verschillende manieren om een pagina te zoeken in het veld **Selecteer een pagina**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-135">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="4d63a-136">In veel gevallen moet u op de pijl in het veld **Selecteer een pagina** klikken om de vervolgkeuzelijst te openen en vervolgens uit een gefilterde lijst met pagina's een keuze maken.</span><span class="sxs-lookup"><span data-stu-id="4d63a-136">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

- <span data-ttu-id="4d63a-137">Typ een deel van de naam en open vervolgens een vervolgkeuzelijst om te selecteren uit een gefilterde lijst met pagina's.</span><span class="sxs-lookup"><span data-stu-id="4d63a-137">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
- <span data-ttu-id="4d63a-138">Open de vervolgkeuzelijst en klik vervolgens op de kop **Paginanaam** boven aan de lijst of op de kop **AOT-naam van pagina**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-138">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="4d63a-139">Er wordt een dialoogvenster weergegeven waarin u geavanceerde filteropties kunt gebruiken, zoals **Paginanaam begint met**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-139">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
- <span data-ttu-id="4d63a-140">Typ de volledige naam van de pagina.</span><span class="sxs-lookup"><span data-stu-id="4d63a-140">Type the full name of the page.</span></span> <span data-ttu-id="4d63a-141">Als u deze optie gebruikt, kunt u het beste de vervolgkeuzelijst openen en bekijken wat er nog meer in de lijst staat, zelfs of veldbeschrijvingen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4d63a-141">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>

    - <span data-ttu-id="4d63a-142">Als er een enkele exacte overeenkomst met de naam is, worden de veldomschrijvingen voor die pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4d63a-142">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    - <span data-ttu-id="4d63a-143">Als er meer dan één exacte overeenkomst is, worden geen beschrijvingen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4d63a-143">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="4d63a-144">U moet de vervolgkeuzelijst openen en de gewenste pagina selecteren.</span><span class="sxs-lookup"><span data-stu-id="4d63a-144">You must open the drop-down list and select the page that you want.</span></span>
    - <span data-ttu-id="4d63a-145">Als de naam die u hebt getypt deel uitmaakt van de naam van een andere pagina, ziet u de beschrijvingen voor uw pagina.</span><span class="sxs-lookup"><span data-stu-id="4d63a-145">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="4d63a-146">Als u echter de vervolgkeuzelijst opent, ziet u extra pagina's die deze naam bevatten.</span><span class="sxs-lookup"><span data-stu-id="4d63a-146">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="4d63a-147">Zo worden er geen beschrijvingen weergegeven wanneer u **Telling** typt in het veld **Een pagina selecteren**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-147">For example, no descriptions are shown when you type **Counting** in the **Select a page** field.</span></span> <span data-ttu-id="4d63a-148">U opent de vervolgkeuzelijst en ziet dat er twee pagina's zijn met de naam **Counting**, plus verschillende pagina's die het woord "Telling" bevatten in de naam.</span><span class="sxs-lookup"><span data-stu-id="4d63a-148">You open the drop-down list, and see that there are two pages that have the name **Counting** and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="4d63a-149">Als u de pagina met de AOT-naam **InventJournalCountt** selecteert, worden de veldbeschrijvingen voor die pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4d63a-149">If you select the page that has the AOT name **InventJournalCount**, the field descriptions are shown for that page.</span></span> <span data-ttu-id="4d63a-150">Als u echter de vervolgkeuzelijst opnieuw opent, ziet u dat de lijst nu alle pagina's bevat met "InventJournalCount" als deel van de AOT-naam.</span><span class="sxs-lookup"><span data-stu-id="4d63a-150">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="4d63a-151">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="4d63a-151">Troubleshooting</span></span>

<span data-ttu-id="4d63a-152">Deze sectie bevat informatie om u te helpen problemen op te lossen die u kunt tegenkomen als u veldbeschrijvingen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4d63a-152">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="4d63a-153">Ik kan geen veldomschrijving vinden</span><span class="sxs-lookup"><span data-stu-id="4d63a-153">I can't find a field description</span></span>

<span data-ttu-id="4d63a-154">We zijn bezig met het toevoegen van omschrijvingen voor de complexere velden.</span><span class="sxs-lookup"><span data-stu-id="4d63a-154">We're in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="4d63a-155">Als u hulp nodig hebt voor een bepaald veld, laat dit ons dan weten door een opmerking voor dit onderwerp toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="4d63a-155">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="4d63a-156">De veldomschrijving is niet nuttig</span><span class="sxs-lookup"><span data-stu-id="4d63a-156">The field description isn't helpful</span></span>

<span data-ttu-id="4d63a-157">Laat ons dit weten door een opmerking voor dit onderwerp toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="4d63a-157">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="4d63a-158">Beschrijf, indien mogelijk, de aanvullende informatie die u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="4d63a-158">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="4d63a-159">Ik kan een veld op de pagina in Veldbeschrijvingen niet vinden.</span><span class="sxs-lookup"><span data-stu-id="4d63a-159">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="4d63a-160">Als u alle velden op een pagina wilt weergeven, stelt u de optie **Velden zonder beschrijving opnemen** in op **Ja.**</span><span class="sxs-lookup"><span data-stu-id="4d63a-160">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="4d63a-161">Klik op het veld **Selecteer een pagina** om te controleren of u de juiste pagina hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="4d63a-161">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="4d63a-162">Als de naam die u hebt getypt deel uitmaakt van een andere veldnaam, hebt u mogelijk de pagina met de langere naam geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="4d63a-162">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="4d63a-163">Ik kan een pagina op de pagina Veldbeschrijvingen niet vinden.</span><span class="sxs-lookup"><span data-stu-id="4d63a-163">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="4d63a-164">Zie de sectie 'Zoeken naar pagina's' eerder in dit artikel voor meer informatie over de verschillende manieren om pagina's te zoeken.</span><span class="sxs-lookup"><span data-stu-id="4d63a-164">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="4d63a-165">Als u de exacte naam van de pagina hebt ingevoerd, worden de veldbeschrijvingen mogelijk niet weergegeven als er meer dan één pagina met dezelfde naam is.</span><span class="sxs-lookup"><span data-stu-id="4d63a-165">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="4d63a-166">Klik op de pijl in het veld **Selecteer een pagina** als u een gefilterde lijst met de beschikbare pagina's wilt openen.</span><span class="sxs-lookup"><span data-stu-id="4d63a-166">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d63a-167">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4d63a-167">Additional resources</span></span>

[<span data-ttu-id="4d63a-168">Veldbeschrijvingen aanpassen</span><span class="sxs-lookup"><span data-stu-id="4d63a-168">Customize field descriptions</span></span>](../../dev-itpro/user-interface/customize-field-help.md)
