---
title: Toegankelijkheid van pagina-inhoud controleren
description: In dit onderwerp wordt beschreven hoe u de toegankelijkheid van pagina-inhoud in controleert in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791626"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="1c88a-103">Toegankelijkheid van pagina-inhoud controleren</span><span class="sxs-lookup"><span data-stu-id="1c88a-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1c88a-104">In dit onderwerp wordt beschreven hoe u de toegankelijkheid van pagina-inhoud in controleert in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1c88a-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1c88a-105">Wanneer u klaar bent met het wijzigen van een pagina, moet u ervoor zorgen dat de inhoud toegankelijk is voor iedereen op het web.</span><span class="sxs-lookup"><span data-stu-id="1c88a-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="1c88a-106">In de Commerce-ontwerpfunctie kunt u eenvoudig de toegankelijkheid van pagina-inhoud controleren met behulp van de geïntegreerde service [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="1c88a-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="1c88a-107">Met deze service wordt de inhoud van uw pagina geverifieerd aan de hand van de meest recente [W3C-toegankelijkheidsrichtlijnen](https://www.w3.org/standards/webdesign/accessibility) (World Wide Web Consortium).</span><span class="sxs-lookup"><span data-stu-id="1c88a-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="1c88a-108">De integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) moet worden ingeschakeld op tenant- of siteniveau voordat u deze kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1c88a-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="1c88a-109">Microsoft Accessibility Insights inschakelen voor alle sites in uw tenant</span><span class="sxs-lookup"><span data-stu-id="1c88a-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="1c88a-110">Ga als volgt te werk om de integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) voor alle Commerce-sites in uw tenant in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="1c88a-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="1c88a-111">Als u tenantinstellingen wilt openen, moet u bij Commerce zijn aangemeld als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="1c88a-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="1c88a-112">Meld u aan bij Commerce als systeembeheerder.</span><span class="sxs-lookup"><span data-stu-id="1c88a-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="1c88a-113">Selecteer in het linkernavigatievenster de optie **Tenantinstellingen** (naast het tandwielsymbool) om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="1c88a-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="1c88a-114">Selecteer **Functies** onder **Tenantinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="1c88a-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="1c88a-115">Stel de opte **Toegankelijkheidscontrole** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="1c88a-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="1c88a-116">Microsoft Accessibility Insights voor één site inschakelen</span><span class="sxs-lookup"><span data-stu-id="1c88a-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="1c88a-117">Ga als volgt te werk om de integratie van [Microsoft Accessibility Insights](https://accessibilityinsights.io/) voor één Commerce-site in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="1c88a-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="1c88a-118">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="1c88a-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1c88a-119">Selecteer in het linkernavigatievenster de optie **Site-instellingen** om deze uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="1c88a-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="1c88a-120">Selecteer **Functies** onder **Site-instellingen**.</span><span class="sxs-lookup"><span data-stu-id="1c88a-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="1c88a-121">Stel de opte **Toegankelijkheidscontrole** in op **Aan**.</span><span class="sxs-lookup"><span data-stu-id="1c88a-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="1c88a-122">De toegankelijkheid van de inhoud op de startpagina controleren</span><span class="sxs-lookup"><span data-stu-id="1c88a-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="1c88a-123">Ga als volgt te werk om de geïntegreerde service [Microsoft Accessibility Insights](https://accessibilityinsights.io/) te gebruiken om de inhoud van uw startpagina in Commerce te scannen en te controleren.</span><span class="sxs-lookup"><span data-stu-id="1c88a-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1c88a-124">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="1c88a-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1c88a-125">Selecteer **Pagina's** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="1c88a-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="1c88a-126">Zoek en selecteer de startpagina om deze te openen in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="1c88a-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="1c88a-127">Selecteer **Toegankelijkheid controleren** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="1c88a-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="1c88a-128">De pagina **Toegankelijkheid controleren** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1c88a-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="1c88a-129">Nadat de scan is voltooid, controleert u de inhoud van het rapport.</span><span class="sxs-lookup"><span data-stu-id="1c88a-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="1c88a-130">Als er controles zijn mislukt, kunt u elk mislukt controle-item uitvouwen voor meer details.</span><span class="sxs-lookup"><span data-stu-id="1c88a-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="1c88a-131">Als u het rapport wilt sluiten nadat u het hebt bekeken, schuift u omlaag op de pagina **Toegankelijkheid controleren** en selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c88a-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c88a-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="1c88a-132">Additional resources</span></span>

[<span data-ttu-id="1c88a-133">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="1c88a-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="1c88a-134">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="1c88a-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1c88a-135">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="1c88a-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="1c88a-136">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="1c88a-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="1c88a-137">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="1c88a-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="1c88a-138">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="1c88a-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="1c88a-139">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="1c88a-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="1c88a-140">Dynamische e-commercepagina's maken op basis van URL-parameters</span><span class="sxs-lookup"><span data-stu-id="1c88a-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
