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
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686809"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="2e1d9-103">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="2e1d9-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2e1d9-104">In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="2e1d9-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="2e1d9-105">Overview</span></span>

<span data-ttu-id="2e1d9-106">Webanalyses zijn een essentieel hulpmiddel om inzicht te krijgen in de manier waarop uw klanten met uw site communiceren en om beslissingen te nemen die de ervaring voor een maximale conversie optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="2e1d9-107">Er zijn veel webanalysepakketten beschikbaar om u te helpen deze doelstellingen te verwezenlijken, zoals Google Analytics, Clicky, Moz Analytics en KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="2e1d9-108">Voor de meeste webanalysepakketten moet u scriptcode op de client toevoegen in het element **\<head\>** van de HTML-code op uw sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="2e1d9-109">De instructies in dit onderwerp gelden ook voor andere aangepaste clientfunctionaliteit die Microsoft Dynamics 365 Commerce niet zelf aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="2e1d9-110">Een herbruikbare pagina maken voor uw scriptcode</span><span class="sxs-lookup"><span data-stu-id="2e1d9-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="2e1d9-111">Met een paginafragment kunt u inline of externe scriptcode opnieuw gebruiken voor alle pagina's van uw site, ongeacht de sjabloon die ze gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="2e1d9-112">Een herbruikbare pagina maken voor uw inline scriptcode</span><span class="sxs-lookup"><span data-stu-id="2e1d9-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="2e1d9-113">Voer de volgende stappen uit om een herbruikbaar paginafragment te maken voor de inline scriptcode in Site builder.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2e1d9-114">Ga naar **Fragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="2e1d9-115">Selecteer **Inline script** in het dialoogvenster **Nieuw paginafragment**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-115">In the **New page fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="2e1d9-116">Voer onder **Naam paginafragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-116">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2e1d9-117">Selecteer onder het paginafragment dat u hebt gemaakt de module **Standaard inline script**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="2e1d9-118">Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="2e1d9-119">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2e1d9-120">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2e1d9-121">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="2e1d9-122">Een herbruikbare pagina maken voor uw externe scriptcode</span><span class="sxs-lookup"><span data-stu-id="2e1d9-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="2e1d9-123">Voer de volgende stappen uit om een herbruikbaar paginafragment te maken voor de externe scriptcode in Site builder.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2e1d9-124">Ga naar **Fragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="2e1d9-125">Selecteer **Extern script** in het dialoogvenster **Nieuw paginafragment**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-125">In the **New page fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="2e1d9-126">Voer onder **Naam paginafragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-126">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2e1d9-127">Selecteer onder het paginafragment dat u hebt gemaakt de module **Standaard extern script**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="2e1d9-128">Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="2e1d9-129">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2e1d9-130">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2e1d9-131">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="2e1d9-132">Een paginafragment met scriptcode aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="2e1d9-133">Voer de volgende stappen uit om een paginafragment met scriptcode toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2e1d9-134">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2e1d9-135">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2e1d9-136">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Paginafragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="2e1d9-137">Selecteer het fragment dat u voor de scriptcode hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="2e1d9-138">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2e1d9-139">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="2e1d9-140">Een extern script of inline script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="2e1d9-141">Als u een inline of extern script rechtstreeks wilt invoegen in een set pagina's die wordt aangestuurd door één sjabloon, hoeft u niet eerst een paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="2e1d9-142">Een inline script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="2e1d9-143">Voer de volgende stappen uit om een inline script rechtstreeks toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2e1d9-144">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2e1d9-145">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2e1d9-146">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2e1d9-147">Selecteer **Inline script** in het dialoogvenster **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="2e1d9-148">Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="2e1d9-149">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2e1d9-150">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2e1d9-151">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="2e1d9-152">Een extern script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-152">Add an external script directly to a template</span></span>

<span data-ttu-id="2e1d9-153">Voer de volgende stappen uit om een extern script rechtstreeks toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="2e1d9-154">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="2e1d9-155">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2e1d9-156">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2e1d9-157">Selecteer **Extern script** in het dialoogvenster **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="2e1d9-158">Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="2e1d9-159">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="2e1d9-160">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2e1d9-161">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="2e1d9-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e1d9-162">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-162">Additional resources</span></span>

[<span data-ttu-id="2e1d9-163">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="2e1d9-164">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="2e1d9-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2e1d9-165">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="2e1d9-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2e1d9-166">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2e1d9-167">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="2e1d9-168">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="2e1d9-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2e1d9-169">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="2e1d9-169">Add languages to your site</span></span>](add-languages-to-site.md)
