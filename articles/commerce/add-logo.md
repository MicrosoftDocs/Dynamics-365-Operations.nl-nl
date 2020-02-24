---
title: Een logo toevoegen
description: In dit onderwerp wordt beschreven hoe u een logo aan uw site toevoegt in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
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
ms.openlocfilehash: 5fc0673dcdcc8b761089be2c2d201c8488128865
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025681"
---
# <a name="add-a-logo"></a><span data-ttu-id="8b7f7-103">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="8b7f7-103">Add a logo</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8b7f7-104">In dit onderwerp wordt beschreven hoe u een logo aan uw site toevoegt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8b7f7-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="8b7f7-105">Overview</span></span>

<span data-ttu-id="8b7f7-106">Wanneer u uw site bouwt, is het toevoegen van uw bedrijfs- of merklogo aan de koptekst van de site waarschijnlijk een van de eerste dingen die u doet.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="8b7f7-107">Het online startpakket van Dynamics 365 Commerce biedt een module die deze taak gemakkelijk maakt.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="8b7f7-108">U kunt een logo direct aan een sjabloon, indeling of pagina toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="8b7f7-109">Op deze manier kunt u eenvoudig het logo wijzigen dat op specifieke pagina's of groepen pagina's wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="8b7f7-110">In dit onderwerp komen echter de meest voorkomende scenario's aan bod, waarbij u uw logo toevoegt aan een koptekstfragment dat op alle pagina's van uw site kan worden hergebruikt.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8b7f7-111">Vereisten</span><span class="sxs-lookup"><span data-stu-id="8b7f7-111">Prerequisites</span></span>

<span data-ttu-id="8b7f7-112">Voordat u een logo aan alle pagina's van uw site kunt toevoegen, moet u deze taken uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="8b7f7-113">Upload uw logo naar de mediabibliotheek.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="8b7f7-114">Maak een koptekstfragment.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-114">Create a header fragment.</span></span> <span data-ttu-id="8b7f7-115">Zie [Werken met fragmenten](work-with-fragments.md) voor meer informatie over het maken en gebruiken van fragmenten.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="8b7f7-116">Neem het koptekstfragment op in de sjabloon die door de pagina's van uw site worden gebruiken voor hun indelings- en moduleopties.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="8b7f7-117">Zie [Werken met sjablonen](work-with-templates.md) voor meer informatie over het gebruik van sjablonen.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="8b7f7-118">Een logo toevoegen aan een koptekstfragment</span><span class="sxs-lookup"><span data-stu-id="8b7f7-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="8b7f7-119">Volg deze stappen om een logo toe te voegen aan het koptekstfragment voor uw site.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="8b7f7-120">Selecteer **Paginafragmenten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-120">In the navigation pane on the left, select **Page Fragments**.</span></span>
1. <span data-ttu-id="8b7f7-121">Selecteer het koptekstfragment dat u eerder hebt gemaakt en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="8b7f7-122">Vouw de koptekstmodule uit.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-122">Expand the header module.</span></span>
1. <span data-ttu-id="8b7f7-123">Geef in het eigenschappenvenster voor de koptekstmodule een afbeelding op en een koppeling voor het logo.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="8b7f7-124">Sla het koptekstfragment op, voltooi de bewerking ervan en publiceer het fragment.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="8b7f7-125">Als u het bijgewerkte koptekstfragment publiceert, wordt uw logo weergegeven op alle sitepagina's die gebruikmaken van de sjabloon die het koptekstfragment bevat.</span><span class="sxs-lookup"><span data-stu-id="8b7f7-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b7f7-126">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8b7f7-126">Additional resources</span></span>

[<span data-ttu-id="8b7f7-127">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="8b7f7-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="8b7f7-128">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="8b7f7-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="8b7f7-129">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="8b7f7-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="8b7f7-130">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="8b7f7-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="8b7f7-131">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="8b7f7-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="8b7f7-132">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="8b7f7-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="8b7f7-133">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="8b7f7-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

