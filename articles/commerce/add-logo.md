---
title: Een logo toevoegen
description: In dit onderwerp wordt beschreven hoe u een logo aan uw site toevoegt in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914613"
---
# <a name="add-a-logo"></a><span data-ttu-id="b2cf8-103">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="b2cf8-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b2cf8-104">In dit onderwerp wordt beschreven hoe u een logo aan uw site toevoegt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b2cf8-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="b2cf8-105">Overview</span></span>

<span data-ttu-id="b2cf8-106">Wanneer u uw site bouwt, is het toevoegen van uw bedrijfs- of merklogo aan de koptekst van de site waarschijnlijk een van de eerste dingen die u doet.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="b2cf8-107">Het online startpakket van Dynamics 365 Commerce biedt een module die deze taak gemakkelijk maakt.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="b2cf8-108">U kunt een logo direct aan een sjabloon, indeling of pagina toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="b2cf8-109">Op deze manier kunt u eenvoudig het logo wijzigen dat op specifieke pagina's of groepen pagina's wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="b2cf8-110">In dit onderwerp komen echter de meest voorkomende scenario's aan bod, waarbij u uw logo toevoegt aan een koptekstfragment dat op alle pagina's van uw site kan worden hergebruikt.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b2cf8-111">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b2cf8-111">Prerequisites</span></span>

<span data-ttu-id="b2cf8-112">Voordat u een logo aan alle pagina's van uw site kunt toevoegen, moet u deze taken uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="b2cf8-113">Upload uw logo naar de functie voor het beheren van digitale activa die u opent via de pagina **Activa**.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="b2cf8-114">Maak een koptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-114">Create a header fragment.</span></span> <span data-ttu-id="b2cf8-115">Zie [Werken met fragmenten](work-with-fragments.md) voor meer informatie over het maken en gebruiken van fragmenten.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="b2cf8-116">Neem het koptekstfragment op in de sjabloon die door de pagina's van uw site worden gebruiken voor hun indelings- en moduleopties.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="b2cf8-117">Zie [Werken met sjablonen](work-with-templates.md) voor meer informatie over het gebruik van sjablonen.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="b2cf8-118">Een logo toevoegen aan een koptekstfragment</span><span class="sxs-lookup"><span data-stu-id="b2cf8-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="b2cf8-119">Volg deze stappen om een logo toe te voegen aan het koptekstfragment voor uw site.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="b2cf8-120">Selecteer in het navigatiedeelvenster aan de linkerkant **Fragmenten** en selecteer vervolgens het koptekstfragment dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="b2cf8-121">Selecteer **Uitchecken**.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-121">Select **Check out**.</span></span>
3. <span data-ttu-id="b2cf8-122">Vouw het vak **Koptekst** en vervolgens het vak **Logo** uit.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="b2cf8-123">Selecteer de knop met het weglatingsteken (**...**) voor het vak **Logo** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="b2cf8-124">Selecteer de logomodule.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-124">Select the logo module.</span></span>
6. <span data-ttu-id="b2cf8-125">Vervolgens configureert u in het deelvenster Eigenschappen rechts de logomodule.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="b2cf8-126">Sla het koptekstfragment op, check het in en publiceer het.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="b2cf8-127">Als u het bijgewerkte koptekstfragment publiceert, wordt uw logo weergegeven op alle sitepagina's die gebruikmaken van de sjabloon die het koptekstfragment bevat.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2cf8-128">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b2cf8-128">Additional resources</span></span>

[<span data-ttu-id="b2cf8-129">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="b2cf8-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b2cf8-130">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="b2cf8-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b2cf8-131">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="b2cf8-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b2cf8-132">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="b2cf8-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="b2cf8-133">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="b2cf8-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b2cf8-134">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="b2cf8-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="b2cf8-135">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="b2cf8-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

