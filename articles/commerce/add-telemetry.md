---
title: Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie
description: In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154081"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="32b62-103">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="32b62-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32b62-104">In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="32b62-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="32b62-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="32b62-105">Overview</span></span>

<span data-ttu-id="32b62-106">Webanalyses zijn een essentieel hulpmiddel om inzicht te krijgen in de manier waarop uw klanten met uw site communiceren en om beslissingen te nemen die de ervaring voor een maximale conversie optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="32b62-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="32b62-107">Er zijn veel webanalysepakketten beschikbaar om u te helpen deze doelstellingen te verwezenlijken, zoals Google Analytics, Clicky, Moz Analytics en KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="32b62-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="32b62-108">Voor de meeste webanalysepakketten moet u scriptcode op de client toevoegen in het element **\<Head\>** van de HTML-code op uw sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="32b62-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="32b62-109">De instructies in dit onderwerp gelden ook voor andere aangepaste clientfunctionaliteit die Microsoft Dynamics 365 Commerce niet zelf aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="32b62-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="32b62-110">Een herbruikbare pagina maken voor uw scriptcode</span><span class="sxs-lookup"><span data-stu-id="32b62-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="32b62-111">Met een paginafragment kunt u inline of externe scriptcode opnieuw gebruiken voor alle pagina's van uw site, ongeacht de sjabloon die ze gebruiken.</span><span class="sxs-lookup"><span data-stu-id="32b62-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="32b62-112">Een herbruikbare pagina maken voor uw inline scriptcode</span><span class="sxs-lookup"><span data-stu-id="32b62-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="32b62-113">Voer de volgende stappen uit om een herbruikbaar paginafragment te maken voor de inline scriptcode in Site builder.</span><span class="sxs-lookup"><span data-stu-id="32b62-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="32b62-114">Ga naar **Paginafragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="32b62-114">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="32b62-115">Selecteer **Inline script** in het dialoogvenster **Nieuw paginafragment**.</span><span class="sxs-lookup"><span data-stu-id="32b62-115">In the **New Page Fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="32b62-116">Voer onder **Naam paginafragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="32b62-116">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="32b62-117">Selecteer onder het paginafragment dat u hebt gemaakt de module **Standaard inline script**.</span><span class="sxs-lookup"><span data-stu-id="32b62-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="32b62-118">Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in.</span><span class="sxs-lookup"><span data-stu-id="32b62-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="32b62-119">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="32b62-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="32b62-120">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="32b62-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="32b62-121">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="32b62-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="32b62-122">Een herbruikbare pagina maken voor uw externe scriptcode</span><span class="sxs-lookup"><span data-stu-id="32b62-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="32b62-123">Voer de volgende stappen uit om een herbruikbaar paginafragment te maken voor de externe scriptcode in Site builder.</span><span class="sxs-lookup"><span data-stu-id="32b62-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="32b62-124">Ga naar **Paginafragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="32b62-124">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="32b62-125">Selecteer **Extern script** in het dialoogvenster **Nieuw paginafragment**.</span><span class="sxs-lookup"><span data-stu-id="32b62-125">In the **New Page Fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="32b62-126">Voer onder **Naam paginafragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="32b62-126">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="32b62-127">Selecteer onder het paginafragment dat u hebt gemaakt de module **Standaard extern script**.</span><span class="sxs-lookup"><span data-stu-id="32b62-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="32b62-128">Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron.</span><span class="sxs-lookup"><span data-stu-id="32b62-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="32b62-129">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="32b62-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="32b62-130">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="32b62-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="32b62-131">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="32b62-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="32b62-132">Een paginafragment met scriptcode aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="32b62-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="32b62-133">Voer de volgende stappen uit om een paginafragment met scriptcode toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="32b62-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="32b62-134">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="32b62-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="32b62-135">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="32b62-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="32b62-136">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Paginafragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="32b62-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="32b62-137">Selecteer het fragment dat u voor de scriptcode hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="32b62-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="32b62-138">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="32b62-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="32b62-139">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="32b62-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="32b62-140">Een extern script of inline script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="32b62-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="32b62-141">Als u een inline of extern script rechtstreeks wilt invoegen in een set pagina's die wordt aangestuurd door één sjabloon, hoeft u niet eerst een paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="32b62-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="32b62-142">Een inline script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="32b62-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="32b62-143">Voer de volgende stappen uit om een inline script rechtstreeks toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="32b62-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="32b62-144">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="32b62-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="32b62-145">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="32b62-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="32b62-146">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="32b62-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="32b62-147">Selecteer **Inline script** in het dialoogvenster **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="32b62-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="32b62-148">Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in.</span><span class="sxs-lookup"><span data-stu-id="32b62-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="32b62-149">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="32b62-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="32b62-150">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="32b62-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="32b62-151">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="32b62-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="32b62-152">Een extern script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="32b62-152">Add an external script directly to a template</span></span>

<span data-ttu-id="32b62-153">Voer de volgende stappen uit om een extern script rechtstreeks toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="32b62-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="32b62-154">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="32b62-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="32b62-155">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="32b62-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="32b62-156">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="32b62-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="32b62-157">Selecteer **Extern script** in het dialoogvenster **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="32b62-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="32b62-158">Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron.</span><span class="sxs-lookup"><span data-stu-id="32b62-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="32b62-159">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="32b62-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="32b62-160">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="32b62-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="32b62-161">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="32b62-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32b62-162">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="32b62-162">Additional resources</span></span>

[<span data-ttu-id="32b62-163">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="32b62-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="32b62-164">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="32b62-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="32b62-165">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="32b62-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="32b62-166">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="32b62-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="32b62-167">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="32b62-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="32b62-168">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="32b62-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="32b62-169">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="32b62-169">Add languages to your site</span></span>](add-languages-to-site.md)
