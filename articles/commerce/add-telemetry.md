---
title: Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie
description: In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 7e8a9f92a2675bf5b620889678a2918f63f3e199
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2020
ms.locfileid: "3901491"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="39720-103">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="39720-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="39720-104">In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="39720-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="39720-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="39720-105">Overview</span></span>

<span data-ttu-id="39720-106">Webanalyses zijn een essentieel hulpmiddel om inzicht te krijgen in de manier waarop uw klanten met uw site communiceren en om beslissingen te nemen die de ervaring voor een maximale conversie optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="39720-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="39720-107">Er zijn veel webanalysepakketten beschikbaar om u te helpen deze doelstellingen te verwezenlijken, zoals Google Analytics, Clicky, Moz Analytics en KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="39720-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="39720-108">Voor de meeste webanalysepakketten moet u scriptcode op de client toevoegen in het element **\<head\>** van de HTML-code op uw sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="39720-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="39720-109">De instructies in dit onderwerp gelden ook voor andere aangepaste clientfunctionaliteit die Microsoft Dynamics 365 Commerce niet zelf aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="39720-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="39720-110">Een herbruikbaar fragment maken voor uw scriptcode</span><span class="sxs-lookup"><span data-stu-id="39720-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="39720-111">Met een fragment kunt u inline of externe scriptcode opnieuw gebruiken voor alle pagina's van uw site, ongeacht de sjabloon die ze gebruiken.</span><span class="sxs-lookup"><span data-stu-id="39720-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="39720-112">Een herbruikbaar fragment maken voor uw inline scriptcode</span><span class="sxs-lookup"><span data-stu-id="39720-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="39720-113">Voer de volgende stappen uit om een herbruikbaar fragment te maken voor de inline scriptcode in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="39720-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="39720-114">Ga naar **Fragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="39720-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="39720-115">Selecteer **Inline script** in het dialoogvenster **Nieuw fragment**.</span><span class="sxs-lookup"><span data-stu-id="39720-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="39720-116">Voer onder **Naam fragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="39720-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="39720-117">Selecteer onder het fragment dat u hebt gemaakt de module **Standaard inline script**.</span><span class="sxs-lookup"><span data-stu-id="39720-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="39720-118">Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in.</span><span class="sxs-lookup"><span data-stu-id="39720-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="39720-119">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="39720-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="39720-120">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="39720-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="39720-121">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="39720-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="39720-122">Een herbruikbaar fragment maken voor uw externe scriptcode</span><span class="sxs-lookup"><span data-stu-id="39720-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="39720-123">Voer de volgende stappen uit om een herbruikbaar fragment te maken voor de externe scriptcode in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="39720-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="39720-124">Ga naar **Fragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="39720-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="39720-125">Selecteer **Extern script** in het dialoogvenster **Nieuw fragment**.</span><span class="sxs-lookup"><span data-stu-id="39720-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="39720-126">Voer onder **Naam fragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="39720-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="39720-127">Selecteer onder het fragment dat u hebt gemaakt de module **Standaard extern script**.</span><span class="sxs-lookup"><span data-stu-id="39720-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="39720-128">Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron.</span><span class="sxs-lookup"><span data-stu-id="39720-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="39720-129">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="39720-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="39720-130">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="39720-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="39720-131">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="39720-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="39720-132">Als CSP (Content Security Policy) is ingeschakeld voor uw site, moet u ervoor zorgen dat alle externe URL's worden toegevoegd aan de CSP-instructie **script-src** in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="39720-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="39720-133">Zie voor meer informatie [Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="39720-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="39720-134">Een fragment met scriptcode aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="39720-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="39720-135">Voer de volgende stappen uit om een fragment met scriptcode toe te voegen aan een sjabloon in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="39720-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="39720-136">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="39720-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="39720-137">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="39720-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="39720-138">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="39720-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="39720-139">Selecteer het fragment dat u voor de scriptcode hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="39720-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="39720-140">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="39720-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="39720-141">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="39720-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="39720-142">Een extern script of inline script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="39720-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="39720-143">Als u een inline of extern script rechtstreeks wilt invoegen in een set pagina's die wordt aangestuurd door één sjabloon, hoeft u niet eerst een fragment te maken.</span><span class="sxs-lookup"><span data-stu-id="39720-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="39720-144">Een inline script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="39720-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="39720-145">Voer de volgende stappen uit om een inline script rechtstreeks toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="39720-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="39720-146">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="39720-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="39720-147">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="39720-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="39720-148">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="39720-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39720-149">Selecteer **Inline script** in het dialoogvenster **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="39720-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="39720-150">Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in.</span><span class="sxs-lookup"><span data-stu-id="39720-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="39720-151">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="39720-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="39720-152">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="39720-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="39720-153">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="39720-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="39720-154">Een extern script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="39720-154">Add an external script directly to a template</span></span>

<span data-ttu-id="39720-155">Voer de volgende stappen uit om een extern script rechtstreeks toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="39720-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="39720-156">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="39720-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="39720-157">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="39720-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="39720-158">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="39720-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39720-159">Selecteer **Extern script** in het dialoogvenster **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="39720-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="39720-160">Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron.</span><span class="sxs-lookup"><span data-stu-id="39720-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="39720-161">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="39720-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="39720-162">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="39720-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="39720-163">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="39720-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39720-164">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="39720-164">Additional resources</span></span>

[<span data-ttu-id="39720-165">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="39720-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="39720-166">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="39720-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="39720-167">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="39720-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="39720-168">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="39720-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="39720-169">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="39720-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="39720-170">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="39720-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="39720-171">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="39720-171">Add languages to your site</span></span>](add-languages-to-site.md)
