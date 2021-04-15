---
title: Werken met vooraf ingestelde indelingen
description: In dit onderwerp wordt beschreven hoe u werkt met vooraf ingestelde indelingen in Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793916"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="b8b1e-103">Werken met vooraf ingestelde indelingen</span><span class="sxs-lookup"><span data-stu-id="b8b1e-103">Work with preset layouts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b8b1e-104">In dit onderwerp wordt beschreven hoe u werkt met vooraf ingestelde indelingen in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b8b1e-105">Lees voordat u de procedures in dit onderwerp uitvoert, eerst [Vooraf ingestelde en aangepaste indelingen](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="b8b1e-105">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="b8b1e-106">Zie [Overzicht sjablonen en indelingen](templates-layouts-overview.md) voor een algemeen overzicht.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-106">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="b8b1e-107">Een nieuwe vooraf ingestelde indeling maken</span><span class="sxs-lookup"><span data-stu-id="b8b1e-107">Create a new preset layout</span></span>

<span data-ttu-id="b8b1e-108">Er zijn twee methoden voor het maken van een vooraf ingestelde indeling.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-108">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="b8b1e-109">U kunt een bestaande aangepaste indeling opslaan als een nieuwe vooraf ingestelde indeling of u kunt een geheel nieuwe indeling maken.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-109">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="b8b1e-110">Een vooraf ingestelde indeling maken op basis van een bestaande aangepaste indeling</span><span class="sxs-lookup"><span data-stu-id="b8b1e-110">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="b8b1e-111">Voer deze stappen uit om een vooraf ingestelde indeling te maken op basis van een bestaande aangepaste indeling.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-111">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="b8b1e-112">Open een bestaande pagina waarin momenteel geen vooraf ingestelde indeling wordt gebruikt en die een modulestructuur heeft die u opnieuw wilt gebruiken voor andere pagina's op uw site.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-112">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="b8b1e-113">Selecteer **Bewerken** om de pagina uit te checken.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-113">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="b8b1e-114">Selecteer **Opslaan als nieuwe indeling**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-114">Select **Save as new layout**.</span></span> <span data-ttu-id="b8b1e-115">Het dialoogvenster **Opslaan als nieuwe indeling** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-115">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="b8b1e-116">Voer een naam en beschrijving voor de vooraf ingestelde indeling in.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-116">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="b8b1e-117">De waarden die u invoert, worden weergegeven voor andere ontwerpers wanneer ze nieuwe pagina's maken vanuit uw indeling of overschakelen naar deze pagina.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-117">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="b8b1e-118">Voer daarom waarden in die nuttig zijn voor pagina-ontwerpers.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-118">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="b8b1e-119">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-119">Select **OK**.</span></span>

<span data-ttu-id="b8b1e-120">De vooraf ingestelde indeling is nu beschikbaar wanneer u nieuwe pagina's maakt of een andere indeling selecteert voor een pagina in dezelfde sjabloonhiërarchie.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-120">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="b8b1e-121">Als u snel wilt zien of een specifieke pagina afhankelijk is van een vooraf ingestelde indeling, selecteert u de pagina in de lijstweergave met pagina's en controleert u de metagegevens voor de indeling in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-121">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="b8b1e-122">Een nieuwe vooraf ingestelde indeling maken</span><span class="sxs-lookup"><span data-stu-id="b8b1e-122">Create a new preset layout</span></span>

<span data-ttu-id="b8b1e-123">Voer deze stappen uit om een nieuwe vooraf ingestelde indeling te maken.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-123">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="b8b1e-124">Selecteer **Indelingen** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-124">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="b8b1e-125">Selecteer **Nieuwe indeling**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-125">Select **New Layout**.</span></span> <span data-ttu-id="b8b1e-126">Het dialoogvenster **Nieuwe indeling** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-126">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="b8b1e-127">Selecteer de sjabloon die u voor de vooraf ingestelde indeling wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-127">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="b8b1e-128">Voer een naam en beschrijving voor de vooraf ingestelde indeling in.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-128">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="b8b1e-129">De waarden die u invoert, worden weergegeven voor andere ontwerpers wanneer ze nieuwe pagina's maken vanuit uw indeling of overschakelen naar deze pagina.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-129">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="b8b1e-130">Voer daarom waarden in die nuttig zijn voor pagina-ontwerpers.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-130">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="b8b1e-131">Klik op **OK** om de nieuwe vooraf ingestelde indeling te maken en de indelingseditor te openen.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-131">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="b8b1e-132">Voeg in de indelingseditor modules toe en configureer modules met de overzichtsstructuur aan de linkerkant en het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-132">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="b8b1e-133">(Het proces lijkt op het proces voor het toevoegen en configureren van modules voor een sjabloon in de sjablooneditor.) De rangschikking van modules en alle vergrendelde standaardinstellingen wordt de gecentraliseerde moduleconfiguratie voor pagina's waarvoor deze vooraf ingestelde indeling wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-133">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="b8b1e-134">Een vooraf gedefinieerde indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="b8b1e-134">Modify a preset layout</span></span>

<span data-ttu-id="b8b1e-135">Volg deze stappen om een vooraf ingestelde indeling te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-135">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="b8b1e-136">Selecteer **Indelingen** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-136">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="b8b1e-137">Selecteer in de overzichtsstructuur aan de linkerkant de module die u wilt wijzigen in de indelingseditor.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-137">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="b8b1e-138">Voer vervolgens een van deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="b8b1e-138">Then follow any of these steps:</span></span>

    - <span data-ttu-id="b8b1e-139">Als u een module omhoog of omlaag binnen het bovenliggende niveau wilt verplaatsen, selecteert u de knop met het weglatings teken (**...**) voor de module en vervolgens **Omhoog** of **Omlaag**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-139">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="b8b1e-140">Als u de standaardinstellingen van een module wilt wijzigen, gebruikt u het eigenschappenvenster om standaardwaarden in te voeren en deze desgewenst te vergrendelen voor alle pagina's daaronder.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-140">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="b8b1e-141">Als u nieuwe modules of fragmenten aan containermodules wilt toevoegen, selecteert u de knop met het weglatingsteken en selecteert u vervolgens **Module toevoegen** of **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-141">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="b8b1e-142">Als u een module uit de indeling wilt verwijderen, selecteert u de knop met het weglatingsteken en selecteert u **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-142">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="b8b1e-143">Een thema voor een vooraf ingestelde indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="b8b1e-143">Change a preset layout theme</span></span>

<span data-ttu-id="b8b1e-144">Een normale gewoonte is het instellen van een standaardthema voor alle pagina's met een vooraf ingestelde indeling.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-144">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="b8b1e-145">Voer de volgende stappen uit om het thema in te stellen of te wijzigen voor alle onderliggende pagina's met de vooraf ingestelde indeling.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-145">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="b8b1e-146">Selecteer in de overzichtsstructuur aan de linkerkant de paginacontainermodule in de indelingseditor.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-146">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="b8b1e-147">(Meestal is deze module het tweede knooppunt met de naam **Standaardpagina**.)</span><span class="sxs-lookup"><span data-stu-id="b8b1e-147">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="b8b1e-148">Selecteer in het eigenschappenvenster aan de rechterkant een thema in het veld **Thema**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-148">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="b8b1e-149">Een vooraf ingestelde indeling opslaan, inchecken, vooraf bekijken en publiceren</span><span class="sxs-lookup"><span data-stu-id="b8b1e-149">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="b8b1e-150">Om een vooraf ingestelde indeling op te slaan en in te checken, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-150">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="b8b1e-151">Selecteer de optie **Opslaan** boven aan de indelingseditor.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-151">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="b8b1e-152">Opgeslagen wijzigingen zijn niet van invloed op vervolgpagina's totdat ze zijn ingecheckt.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-152">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="b8b1e-153">Selecteer **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-153">Select **Finish editing**.</span></span> <span data-ttu-id="b8b1e-154">Uw wijzigingen zijn nu detecteerbaar voor vervolgworkflows.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-154">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="b8b1e-155">Als u de wijzigingen wilt bekijken, opent u een bestaande pagina die de vooraf ingestelde indeling gebruikt of maakt u een nieuwe pagina op basis van de indeling.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-155">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="b8b1e-156">Nadat u een voorbeeld van de wijzigingen in de vooraf ingestelde indeling hebt bekeken, volgt u een van deze stappen om de indeling naar uw live site te publiceren:</span><span class="sxs-lookup"><span data-stu-id="b8b1e-156">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="b8b1e-157">Ga naar **Indelingen**, selecteer de indeling en selecteer **Publiceren.**</span><span class="sxs-lookup"><span data-stu-id="b8b1e-157">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="b8b1e-158">Selecteer de indelingsnaam om de indelingseditor te openen en selecteer vervolgens **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-158">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="b8b1e-159">Publiceer een pagina die verwijst naar de niet-gepubliceerde indeling.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-159">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="b8b1e-160">De indeling wordt automatisch gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-160">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="b8b1e-161">Op meerdere pagina's kan naar een vooraf ingestelde indeling worden verwezen.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-161">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="b8b1e-162">Wanneer u een vooraf ingestelde indeling publiceert, kan dit van invloed zijn op de indeling van meerdere pagina's.</span><span class="sxs-lookup"><span data-stu-id="b8b1e-162">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8b1e-163">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b8b1e-163">Additional resources</span></span>

[<span data-ttu-id="b8b1e-164">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="b8b1e-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="b8b1e-165">Werken met sjablonen</span><span class="sxs-lookup"><span data-stu-id="b8b1e-165">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
