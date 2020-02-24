---
title: Toegankelijkheid van pagina-inhoud controleren
description: In dit onderwerp wordt beschreven hoe u de toegankelijkheid van pagina-inhoud in controleert in Microsoft Dynamics 365 Commerce.
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8e35b0f71ff41bade266fb177e4500c7d124ed1f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002654"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="5d3b4-103">Toegankelijkheid van pagina-inhoud controleren</span><span class="sxs-lookup"><span data-stu-id="5d3b4-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5d3b4-104">In dit onderwerp wordt beschreven hoe u de toegankelijkheid van pagina-inhoud in controleert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5d3b4-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="5d3b4-105">Overview</span></span>

<span data-ttu-id="5d3b4-106">Wanneer u klaar bent met het wijzigen van een pagina, moet u ervoor zorgen dat de inhoud toegankelijk is voor iedereen op het web.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="5d3b4-107">In de Commerce-ontwerpfunctie kunt u eenvoudig de toegankelijkheid van pagina-inhoud controleren met behulp van de geïntegreerde service [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="5d3b4-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="5d3b4-108">Met deze service wordt de inhoud van uw pagina geverifieerd aan de hand van de meest recente [W3C-toegankelijkheidsrichtlijnen](https://www.w3.org/standards/webdesign/accessibility) (World Wide Web Consortium).</span><span class="sxs-lookup"><span data-stu-id="5d3b4-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="5d3b4-109">De integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) moet worden ingeschakeld op tenant- of siteniveau voordat u deze kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="5d3b4-110">Microsoft Accessibility Insights inschakelen voor alle sites in uw tenant</span><span class="sxs-lookup"><span data-stu-id="5d3b4-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="5d3b4-111">Ga als volgt te werk om de integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) voor alle Commerce-sites in uw tenant in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="5d3b4-112">Als u tenantinstellingen wilt openen, moet u bij Commerce zijn aangemeld als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="5d3b4-113">Meld u aan bij Commerce als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="5d3b4-114">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="5d3b4-115">Selecteer **Functies** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="5d3b4-116">Stel de opte **Toegankelijkheidscontrole** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="5d3b4-117">Microsoft Accessibility Insights voor één site inschakelen</span><span class="sxs-lookup"><span data-stu-id="5d3b4-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="5d3b4-118">Ga als volgt te werk om de integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) voor één Commerce-site in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="5d3b4-119">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="5d3b4-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="5d3b4-120">Selecteer in het linkernavigatievenster de optie **Site-instellingen** om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="5d3b4-121">Selecteer **Functies** onder **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="5d3b4-122">Stel de opte **Toegankelijkheidscontrole** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="5d3b4-123">De toegankelijkheid van de inhoud op de startpagina controleren</span><span class="sxs-lookup"><span data-stu-id="5d3b4-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="5d3b4-124">Ga als volgt te werk om de geïntegreerde service [Microsoft Accessibility Insights](https://accessibilityinsights.io/) te gebruiken om de inhoud van uw startpagina in Commerce te scannen en te controleren.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5d3b4-125">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="5d3b4-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="5d3b4-126">Selecteer **Pagina's** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="5d3b4-127">Zoek en selecteer de startpagina om deze te openen in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="5d3b4-128">Selecteer **Toegankelijkheid controleren** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="5d3b4-129">De pagina **Toegankelijkheid controleren** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="5d3b4-130">Nadat de scan is voltooid, controleert u de inhoud van het rapport.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="5d3b4-131">Als er controles zijn mislukt, kunt u elk mislukt controle-item uitvouwen voor meer details.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="5d3b4-132">Als u het rapport wilt sluiten nadat u het hebt bekeken, schuift u omlaag op de pagina **Toegankelijkheid controleren** en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d3b4-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d3b4-133">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5d3b4-133">Additional resources</span></span>

[<span data-ttu-id="5d3b4-134">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="5d3b4-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="5d3b4-135">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="5d3b4-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="5d3b4-136">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="5d3b4-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="5d3b4-137">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="5d3b4-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="5d3b4-138">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="5d3b4-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="5d3b4-139">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="5d3b4-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="5d3b4-140">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="5d3b4-140">Enrich a category landing page</span></span>](enrich-category-page.md)
