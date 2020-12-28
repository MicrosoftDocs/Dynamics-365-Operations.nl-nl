---
title: Een bestaande sitepagina wijzigen
description: In dit onderwerp wordt beschreven hoe u een bestaande sitepagina wijzigt in Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8ca23dcf568cb0df6934f0d6201e4aafba5f9ba1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411457"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="97e8d-103">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="97e8d-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="97e8d-104">In dit onderwerp wordt beschreven hoe u een bestaande sitepagina wijzigt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97e8d-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97e8d-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="97e8d-105">Overview</span></span>

<span data-ttu-id="97e8d-106">Wanneer u een pagina wilt wijzigen, moet u de pagina eerst openen in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="97e8d-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="97e8d-107">Ga naar de site die de pagina bevat en zoek in de lijst met pagina's naar de gewenste pagina.</span><span class="sxs-lookup"><span data-stu-id="97e8d-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="97e8d-108">Als u de pagina niet kunt vinden, gebruikt u de uitgebreide zoekfunctie van het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="97e8d-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="97e8d-109">Typ de exacte paginanaam of typ de eerste paar letters van de pagina en vervolgens een asterisk (\*).</span><span class="sxs-lookup"><span data-stu-id="97e8d-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="97e8d-110">Er wordt een gefilterde lijst met pagina's weergegeven.</span><span class="sxs-lookup"><span data-stu-id="97e8d-110">A filtered list of pages appears.</span></span> <span data-ttu-id="97e8d-111">U kunt deze lijst gebruiken om de gewenste pagina te zoeken.</span><span class="sxs-lookup"><span data-stu-id="97e8d-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="97e8d-112">Nadat u de juiste pagina hebt gevonden, selecteert u de paginanaam om de pagina te openen in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="97e8d-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="97e8d-113">Als de pagina in de paginacontrole wordt weergegeven, kunt u **Bewerken** selecteren en de pagina uitchecken voordat u deze opent in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="97e8d-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="97e8d-114">Op deze manier kunt u meerdere pagina's tegelijk uitchecken.</span><span class="sxs-lookup"><span data-stu-id="97e8d-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="97e8d-115">Nadat de pagina is geopend in de pagina-editor, moet u ervoor zorgen dat deze naar u is uitgecheckt.</span><span class="sxs-lookup"><span data-stu-id="97e8d-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="97e8d-116">De opdrachtbalk in het ontwerpgereedschap is dynamisch, contextgevoelig en statusgevoelig.</span><span class="sxs-lookup"><span data-stu-id="97e8d-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="97e8d-117">Daarom worden alleen de acties weergegeven die u kunt uitvoeren op de pagina.</span><span class="sxs-lookup"><span data-stu-id="97e8d-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="97e8d-118">Als de pagina bijvoorbeeld niet naar u is uitgecheckt, worden de knoppen **Opslaan** en **Bewerken voltooien** niet weergegeven op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="97e8d-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="97e8d-119">De status van de pagina wordt ook weergegeven aan de rechterkant van het venster.</span><span class="sxs-lookup"><span data-stu-id="97e8d-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="97e8d-120">Als de pagina nog niet is uitgecheckt naar u, selecteert u **Bewerken** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="97e8d-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="97e8d-121">De opdrachtbalk wordt gewijzigd om de nieuwe status van de pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="97e8d-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="97e8d-122">U ontvangt ook een melding met de mededeling dat de pagina naar u is uitgecheckt.</span><span class="sxs-lookup"><span data-stu-id="97e8d-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="97e8d-123">De volgende stap is het aanbrengen van de wijzigingen.</span><span class="sxs-lookup"><span data-stu-id="97e8d-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="97e8d-124">Vaak gebruikt u de overzichtsstructuur van de pagina aan de linkerkant om de module te zoeken en te selecteren die u wilt wijzigen. Vervolgens brengt u wijzigingen aan in het deelvenster Eigenschappen aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="97e8d-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="97e8d-125">Door uw wijziging kunnen echter soms modellen of fragmenten worden toegevoegd of verwijderd.</span><span class="sxs-lookup"><span data-stu-id="97e8d-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="97e8d-126">Als u een fragment of module wilt toevoegen, gebruikt u de overzichtsstructuur om het vak te vinden waaraan u de module of het fragment wilt toevoegen. Selecteer vervolgens de knop met het weglatings teken (**...**) voor dat vak.</span><span class="sxs-lookup"><span data-stu-id="97e8d-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="97e8d-127">Er wordt een menu weergegeven met opdrachten voor het toevoegen van een module of fragment.</span><span class="sxs-lookup"><span data-stu-id="97e8d-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="97e8d-128">Als u een module of fragment wilt verwijderen, gaat u ernaartoe en selecteert u het in de overzichtsstructuur. Selecteer de knop met het weglatingsteken en de opdracht om de module of het fragment te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="97e8d-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="97e8d-129">U kunt ook de eigenschappen van de modules weergeven en bewerken door ze direct te selecteren in het voorbeeld van de visuele paginabouwer.</span><span class="sxs-lookup"><span data-stu-id="97e8d-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="97e8d-130">Nadat u de gewenste wijzigingen hebt aangebracht en het effect hiervan hebt bekeken, schakelt u **Bewerken voltooien** op de opdrachtbalk in.</span><span class="sxs-lookup"><span data-stu-id="97e8d-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="97e8d-131">Selecteer **Publiceren** op de opdrachtbalk om uw wijzigingen direct te publiceren.</span><span class="sxs-lookup"><span data-stu-id="97e8d-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="97e8d-132">De laatst ingecheckte versie van de pagina die u hebt gewijzigd, wordt gepubliceerd en wordt beschikbaar voor externe gebruikers die uw site bekijken.</span><span class="sxs-lookup"><span data-stu-id="97e8d-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="97e8d-133">Voorbeeld: de video wijzigen op de startpagina</span><span class="sxs-lookup"><span data-stu-id="97e8d-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="97e8d-134">In het volgende voorbeeld ziet u hoe u de startpagina kunt wijzigen door de video te wijzigen die wordt weergegeven in de videospelermodule.</span><span class="sxs-lookup"><span data-stu-id="97e8d-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="97e8d-135">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="97e8d-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="97e8d-136">Selecteer **Pagina's** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="97e8d-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="97e8d-137">Zoek en selecteer de startpagina om deze te openen in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="97e8d-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="97e8d-138">Selecteer **Bewerken** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="97e8d-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="97e8d-139">Selecteer het vak **Hoofd** in het paginaoverzicht.</span><span class="sxs-lookup"><span data-stu-id="97e8d-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="97e8d-140">Vouw onder het vak **Hoofd** alle modules met vloeibare containers uit.</span><span class="sxs-lookup"><span data-stu-id="97e8d-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="97e8d-141">Zoek en selecteer de videospelermodule.</span><span class="sxs-lookup"><span data-stu-id="97e8d-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="97e8d-142">Selecteer in het eigenschappenvenster aan de rechterkant de eigenschap **Video**.</span><span class="sxs-lookup"><span data-stu-id="97e8d-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="97e8d-143">De assetkiezer verschijnt.</span><span class="sxs-lookup"><span data-stu-id="97e8d-143">The asset picker appears.</span></span>
1. <span data-ttu-id="97e8d-144">Selecteer in de assetkiezer een beschikbare video-asset of selecteer **Nieuwe asset uploaden** om een nieuwe video-asset te uploaden.</span><span class="sxs-lookup"><span data-stu-id="97e8d-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="97e8d-145">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="97e8d-145">Select **OK**.</span></span>
1. <span data-ttu-id="97e8d-146">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="97e8d-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="97e8d-147">Voer in het veld **Opmerkingen** **Video gewijzigd** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="97e8d-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="97e8d-148">Selecteer **Voorbeeld** om de bijgewerkte pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="97e8d-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="97e8d-149">Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="97e8d-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="97e8d-150">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="97e8d-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97e8d-151">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="97e8d-151">Additional resources</span></span>

[<span data-ttu-id="97e8d-152">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="97e8d-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="97e8d-153">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="97e8d-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="97e8d-154">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="97e8d-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="97e8d-155">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="97e8d-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="97e8d-156">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="97e8d-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="97e8d-157">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="97e8d-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="97e8d-158">Toegankelijkheid van pagina-inhoud controleren</span><span class="sxs-lookup"><span data-stu-id="97e8d-158">Verify page content accessibility</span></span>](verify-accessibility.md)
