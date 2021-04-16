---
title: Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie
description: In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797426"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="762c9-103">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="762c9-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="762c9-104">In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="762c9-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="762c9-105">Webanalyses zijn een essentieel hulpmiddel om inzicht te krijgen in de manier waarop uw klanten met uw site communiceren en om beslissingen te nemen die de ervaring voor een maximale conversie optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="762c9-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="762c9-106">Er zijn veel webanalysepakketten beschikbaar om u te helpen deze doelstellingen te verwezenlijken, zoals Google Analytics, Clicky, Moz Analytics en KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="762c9-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="762c9-107">Voor de meeste webanalysepakketten moet u scriptcode op de client toevoegen in het element **\<head\>** van de HTML-code op uw sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="762c9-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="762c9-108">De instructies in dit onderwerp gelden ook voor andere aangepaste clientfunctionaliteit die Microsoft Dynamics 365 Commerce niet zelf aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="762c9-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="762c9-109">Een herbruikbaar fragment maken voor uw scriptcode</span><span class="sxs-lookup"><span data-stu-id="762c9-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="762c9-110">Met een fragment kunt u inline of externe scriptcode opnieuw gebruiken voor alle pagina's van uw site, ongeacht de sjabloon die ze gebruiken.</span><span class="sxs-lookup"><span data-stu-id="762c9-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="762c9-111">Een herbruikbaar fragment maken voor uw inline scriptcode</span><span class="sxs-lookup"><span data-stu-id="762c9-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="762c9-112">Voer de volgende stappen uit om een herbruikbaar fragment te maken voor de inline scriptcode in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="762c9-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="762c9-113">Ga naar **Fragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="762c9-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="762c9-114">Selecteer **Inline script** in het dialoogvenster **Nieuw fragment**.</span><span class="sxs-lookup"><span data-stu-id="762c9-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="762c9-115">Voer onder **Naam fragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="762c9-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="762c9-116">Selecteer onder het fragment dat u hebt gemaakt de module **Standaard inline script**.</span><span class="sxs-lookup"><span data-stu-id="762c9-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="762c9-117">Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in.</span><span class="sxs-lookup"><span data-stu-id="762c9-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="762c9-118">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="762c9-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="762c9-119">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="762c9-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="762c9-120">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="762c9-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="762c9-121">Een herbruikbaar fragment maken voor uw externe scriptcode</span><span class="sxs-lookup"><span data-stu-id="762c9-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="762c9-122">Voer de volgende stappen uit om een herbruikbaar fragment te maken voor de externe scriptcode in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="762c9-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="762c9-123">Ga naar **Fragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="762c9-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="762c9-124">Selecteer **Extern script** in het dialoogvenster **Nieuw fragment**.</span><span class="sxs-lookup"><span data-stu-id="762c9-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="762c9-125">Voer onder **Naam fragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="762c9-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="762c9-126">Selecteer onder het fragment dat u hebt gemaakt de module **Standaard extern script**.</span><span class="sxs-lookup"><span data-stu-id="762c9-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="762c9-127">Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron.</span><span class="sxs-lookup"><span data-stu-id="762c9-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="762c9-128">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="762c9-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="762c9-129">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="762c9-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="762c9-130">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="762c9-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="762c9-131">Als CSP (Content Security Policy) is ingeschakeld voor uw site, moet u ervoor zorgen dat alle externe URL's worden toegevoegd aan de CSP-instructie **script-src** in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="762c9-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="762c9-132">Zie voor meer informatie [Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="762c9-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="762c9-133">Een fragment met scriptcode aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="762c9-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="762c9-134">Voer de volgende stappen uit om een fragment met scriptcode toe te voegen aan een sjabloon in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="762c9-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="762c9-135">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="762c9-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="762c9-136">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="762c9-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="762c9-137">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="762c9-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="762c9-138">Selecteer het fragment dat u voor de scriptcode hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="762c9-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="762c9-139">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="762c9-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="762c9-140">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="762c9-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="762c9-141">Een extern script of inline script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="762c9-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="762c9-142">Als u een inline of extern script rechtstreeks wilt invoegen in een set pagina's die wordt aangestuurd door één sjabloon, hoeft u niet eerst een fragment te maken.</span><span class="sxs-lookup"><span data-stu-id="762c9-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="762c9-143">Een inline script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="762c9-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="762c9-144">Voer de volgende stappen uit om een inline script rechtstreeks toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="762c9-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="762c9-145">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="762c9-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="762c9-146">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="762c9-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="762c9-147">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="762c9-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="762c9-148">Selecteer **Inline script** in het dialoogvenster **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="762c9-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="762c9-149">Voer in het eigenschappenvenster rechts onder **Inline script** uw script op de client in.</span><span class="sxs-lookup"><span data-stu-id="762c9-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="762c9-150">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="762c9-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="762c9-151">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="762c9-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="762c9-152">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="762c9-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="762c9-153">Een extern script rechtstreeks aan een sjabloon toevoegen</span><span class="sxs-lookup"><span data-stu-id="762c9-153">Add an external script directly to a template</span></span>

<span data-ttu-id="762c9-154">Voer de volgende stappen uit om een extern script rechtstreeks toe te voegen aan een sjabloon in Site builder.</span><span class="sxs-lookup"><span data-stu-id="762c9-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="762c9-155">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="762c9-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="762c9-156">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="762c9-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="762c9-157">Selecteer de knop met het weglatingsteken (**...**) in het vak **HTML-koptekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="762c9-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="762c9-158">Selecteer **Extern script** in het dialoogvenster **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="762c9-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="762c9-159">Voeg in het eigenschappenvenster aan de rechterkant onder **Scriptbron** een externe of relatieve URL toe voor de externe scriptbron.</span><span class="sxs-lookup"><span data-stu-id="762c9-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="762c9-160">Configureer vervolgens de overige opties naar wens.</span><span class="sxs-lookup"><span data-stu-id="762c9-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="762c9-161">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="762c9-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="762c9-162">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="762c9-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="762c9-163">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="762c9-163">Additional resources</span></span>

[<span data-ttu-id="762c9-164">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="762c9-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="762c9-165">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="762c9-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="762c9-166">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="762c9-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="762c9-167">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="762c9-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="762c9-168">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="762c9-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="762c9-169">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="762c9-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="762c9-170">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="762c9-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
