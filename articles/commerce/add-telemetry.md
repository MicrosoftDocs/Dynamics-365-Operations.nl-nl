---
title: Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie
description: In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001272"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="72e79-103">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="72e79-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="72e79-104">In dit onderwerp wordt beschreven hoe u scriptcode op de client toevoegt aan de sitepagina's om de verzameling telemetrie aan clientzijde te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="72e79-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="72e79-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="72e79-105">Overview</span></span>

<span data-ttu-id="72e79-106">Webanalyses zijn een essentieel hulpmiddel om inzicht te krijgen in de manier waarop uw klanten met uw site communiceren en om beslissingen te nemen die de ervaring voor een maximale conversie optimaliseren.</span><span class="sxs-lookup"><span data-stu-id="72e79-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="72e79-107">Er zijn veel webanalysepakketten beschikbaar om u te helpen deze doelstellingen te verwezenlijken, zoals Google Analytics, Clicky, Moz Analytics en KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="72e79-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="72e79-108">Voor de meeste webanalysepakketten moet u scriptcode op de client toevoegen in het element **\<Head\>** van de HTML-code op uw sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="72e79-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="72e79-109">De instructies in dit onderwerp gelden ook voor andere aangepaste clientfunctionaliteit die Microsoft Dynamics 365 Commerce niet zelf aanbiedt.</span><span class="sxs-lookup"><span data-stu-id="72e79-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="72e79-110">Een herbruikbaar fragment maken voor uw scriptcode</span><span class="sxs-lookup"><span data-stu-id="72e79-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="72e79-111">Nadat u een fragment voor uw scriptcode hebt gemaakt, kan dit worden hergebruikt in alle pagina's van de site.</span><span class="sxs-lookup"><span data-stu-id="72e79-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="72e79-112">Ga naar **Fragmenten \> Nieuw paginafragment**.</span><span class="sxs-lookup"><span data-stu-id="72e79-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="72e79-113">Selecteer **Extern script**, voer een naam voor het fragment in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="72e79-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="72e79-114">Selecteer in de fragmenthiërarchie de onderliggende module **script-injector** van het fragment dat u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="72e79-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="72e79-115">Voeg in het eigenschappenvenster aan de rechterkant het script op de client toe en stel de overige configuratieopties in als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="72e79-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="72e79-116">Het fragment toevoegen aan sjablonen</span><span class="sxs-lookup"><span data-stu-id="72e79-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="72e79-117">Ga naar **Sjablonen** en open de sjabloon voor de pagina's waaraan u de scriptcode wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="72e79-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="72e79-118">Vouw in het linkerdeelvenster de sjabloonhiërarchie uit om het vak **HTML-koptekst** weer te geven.</span><span class="sxs-lookup"><span data-stu-id="72e79-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="72e79-119">Selecteer de knop met het weglatingsteken (**...**) voor het vak **HTML-koptekst** en selecteer **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="72e79-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="72e79-120">Selecteer het fragment dat u voor de scriptcode hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="72e79-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="72e79-121">Sla de sjabloon op en check deze in.</span><span class="sxs-lookup"><span data-stu-id="72e79-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="72e79-122">Wanneer u klaar bent, moet u het fragment en de hoofdsjabloon publiceren.</span><span class="sxs-lookup"><span data-stu-id="72e79-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="72e79-123">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="72e79-123">Additional resources</span></span>

[<span data-ttu-id="72e79-124">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="72e79-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="72e79-125">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="72e79-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="72e79-126">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="72e79-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="72e79-127">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="72e79-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="72e79-128">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="72e79-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="72e79-129">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="72e79-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="72e79-130">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="72e79-130">Add languages to your site</span></span>](add-languages-to-site.md)

