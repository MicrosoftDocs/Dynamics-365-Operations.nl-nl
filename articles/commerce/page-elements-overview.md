---
title: Woordenlijst voor paginamodellen
description: In dit onderwerp worden de verschillende elementen beschreven die worden gebruikt op de pagina's van een Microsoft Dynamics 365 Commerce-site.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c7b79e8b3bd68ba6246fe24916c60f476a26605
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697952"
---
# <a name="page-model-glossary"></a><span data-ttu-id="42c27-103">Woordenlijst voor paginamodellen</span><span class="sxs-lookup"><span data-stu-id="42c27-103">Page model glossary</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="42c27-104">In dit onderwerp worden de verschillende elementen beschreven die worden gebruikt op de pagina's van een Microsoft Dynamics 365 Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="42c27-104">This topic describes the various elements that are used on the pages of a Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="page-element-definitions"></a><span data-ttu-id="42c27-105">Definities van pagina-elementen</span><span class="sxs-lookup"><span data-stu-id="42c27-105">Page element definitions</span></span>

<span data-ttu-id="42c27-106">In de volgende tabel vindt u een overzicht van termen die u moet kennen wanneer u het uiterlijk en de inhoud van de site wijzigt.</span><span class="sxs-lookup"><span data-stu-id="42c27-106">The following table provides a summary of terms that you should be familiar with when you change the look, feel, and content of your site.</span></span> <span data-ttu-id="42c27-107">Volg de koppelingen voor meer uitgebreide uitleg en procedures.</span><span class="sxs-lookup"><span data-stu-id="42c27-107">For more thorough explanations and procedures, follow the links.</span></span>

| <span data-ttu-id="42c27-108">Voorwaarde</span><span class="sxs-lookup"><span data-stu-id="42c27-108">Term</span></span> | <span data-ttu-id="42c27-109">Omschrijving en notities</span><span class="sxs-lookup"><span data-stu-id="42c27-109">Description and notes</span></span> |
|------|-----------------------|
| [<span data-ttu-id="42c27-110">Module</span><span class="sxs-lookup"><span data-stu-id="42c27-110">Module</span></span>](work-with-modules.md) | <p><span data-ttu-id="42c27-111">**Definitie:** modules zijn bouwstenen die het skelet van een webpagina vormen en kunnen worden ontworpen.</span><span class="sxs-lookup"><span data-stu-id="42c27-111">**Definition:** Modules are building block that can be authored and make up the skeleton of a webpage.</span></span> <span data-ttu-id="42c27-112">Voorbeelden zijn kopteksten, held- en carrouselmodules.</span><span class="sxs-lookup"><span data-stu-id="42c27-112">Examples include header, hero, and carousel modules.</span></span></p><p><span data-ttu-id="42c27-113">**Waar wordt dit geselecteerd:** geïmplementeerde modules kunnen worden geselecteerd en geconfigureerd in verschillende ontwerpfasen van de site, zoals de bewerkfasen voor sjabloon, indeling, pagina en fragment.</span><span class="sxs-lookup"><span data-stu-id="42c27-113">**Where it's selected:** Deployed modules can be selected and configured in various stages of the site authoring workflow, such as the template, layout, page, and fragment authoring stages.</span></span></p><p><span data-ttu-id="42c27-114">**Waar wordt dit bewerkt:** aangepaste modules in code worden gemaakt met behulp van de Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="42c27-114">**Where it's edited:** Custom modules are created in code by using the software development kit (SDK).</span></span> <span data-ttu-id="42c27-115">Ze worden vervolgens geüpload naar uw site, waar ze beschikbaar worden voor selectie.</span><span class="sxs-lookup"><span data-stu-id="42c27-115">They are then uploaded to your site, where they become available for selection.</span></span></p> |
| <span data-ttu-id="42c27-116">Module-eigenschap</span><span class="sxs-lookup"><span data-stu-id="42c27-116">Module property</span></span> | <p><span data-ttu-id="42c27-117">**Definitie:** module-eigenschappen zijn specifieke instellingen die worden gedefinieerd door de module.</span><span class="sxs-lookup"><span data-stu-id="42c27-117">**Definition:** Module properties are specific settings that are defined by the module.</span></span> <span data-ttu-id="42c27-118">Ze kunnen worden bewerkt in de e-commerce-ontwerpprogramma's.</span><span class="sxs-lookup"><span data-stu-id="42c27-118">They can be edited in the e-Commerce authoring tools.</span></span> <span data-ttu-id="42c27-119">Module-eigenschappen worden bijvoorbeeld gebruikt om de koptekst en achtergrondafbeelding van een bannermodule in te stellen.</span><span class="sxs-lookup"><span data-stu-id="42c27-119">For example, module properties are used to set the heading and background image of a banner module.</span></span></p><p><span data-ttu-id="42c27-120">**Waar wordt dit geconfigureerd:** module-eigenschappen worden geselecteerd en geconfigureerd in het eigenschappenvenster dat wordt weergegeven in de ontwerpomgevingen (editors) voor sjablonen, indelingen, pagina's, fragmenten en app-instellingen.</span><span class="sxs-lookup"><span data-stu-id="42c27-120">**Where it's configured:** Module properties are selected and configured in the property pane that appears in the authoring environments (editors) for templates, layouts, pages, fragments, and app settings.</span></span></p> |
| [<span data-ttu-id="42c27-121">Sjabloon</span><span class="sxs-lookup"><span data-stu-id="42c27-121">Template</span></span>](templates-layouts-overview.md) | <p><span data-ttu-id="42c27-122">**Definitie:** sjablonen bepalen de modulecombinaties en opties die moeten worden gebruikt voor een categorie pagina's (bijvoorbeeld marketingpagina's, categoriepagina's en productpagina's).</span><span class="sxs-lookup"><span data-stu-id="42c27-122">**Definition:** Templates define the module combinations and options that should be used for a category of pages (for example, marketing pages, category pages, and product pages).</span></span></p><p><span data-ttu-id="42c27-123">**Waar wordt dit geselecteerd:** sjablonen kunnen worden geselecteerd tijdens het maken van de pagina of indelingen.</span><span class="sxs-lookup"><span data-stu-id="42c27-123">**Where it's selected:** Templates can be selected during page or layout creation workflows.</span></span></p><p><span data-ttu-id="42c27-124">**Waar wordt dit bewerkt:** sjablonen worden ontworpen in de sjablooneditor.</span><span class="sxs-lookup"><span data-stu-id="42c27-124">**Where it's edited:** Templates are authored in the template editor.</span></span> <span data-ttu-id="42c27-125">U hoeft geen code te maken of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="42c27-125">No code is required to create or modify them.</span></span></p> |
| [<span data-ttu-id="42c27-126">Indeling</span><span class="sxs-lookup"><span data-stu-id="42c27-126">Layout</span></span>](templates-layouts-overview.md) | <p><span data-ttu-id="42c27-127">**Definitie:** indelingen bepalen de definitieve selectie en de indeling van modules op basis van de set opties van de bovenliggende sjabloon.</span><span class="sxs-lookup"><span data-stu-id="42c27-127">**Definition:** Layouts define the final selection and arrangement of modules from the parent template's set of options.</span></span> <span data-ttu-id="42c27-128">Een indeling kan worden geconfigureerd voor een enkele pagina (*aangepaste indeling*) of gedeeld door meerdere pagina's (*vooraf ingestelde indeling*).</span><span class="sxs-lookup"><span data-stu-id="42c27-128">A layout can be configured for a single page (*custom layout*), or it can be shared by multiple pages (*preset layout*).</span></span></p><p><span data-ttu-id="42c27-129">**Waar wordt dit geselecteerd:** de indeling kan worden geselecteerd tijdens het maken van een nieuwe pagina of wanneer een andere indeling vereist is voor een bestaande pagina.</span><span class="sxs-lookup"><span data-stu-id="42c27-129">**Where it's selected:** Layouts can be selected during new page creation or when a different layout is required for an existing page.</span></span></p><p><span data-ttu-id="42c27-130">**Waar wordt dit bewerkt:** indelingen worden ontworpen in de indelingseditor.</span><span class="sxs-lookup"><span data-stu-id="42c27-130">**Where it's edited:** Layouts are authored in the layout editor.</span></span> <span data-ttu-id="42c27-131">U hoeft geen code te maken of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="42c27-131">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="42c27-132">Pagina-exemplaar</span><span class="sxs-lookup"><span data-stu-id="42c27-132">Page instance</span></span> | <p><span data-ttu-id="42c27-133">**Definitie:** pagina-exemplaren bepalen de uiteindelijke, specifiek voor de pagina gelokaliseerde inhoud voor een enkele pagina.</span><span class="sxs-lookup"><span data-stu-id="42c27-133">**Definition:** Page instances define the final, page-specific localized content for a single page.</span></span> <span data-ttu-id="42c27-134">Deze inhoud wordt afgeleid van de waarden van module-eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="42c27-134">This content is derived from the values of module properties.</span></span></p><p><span data-ttu-id="42c27-135">**Waar wordt dit geselecteerd:** de pagina's worden geselecteerd wanneer URL's worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="42c27-135">**Where it's selected:** Pages are selected when URLs are assigned.</span></span></p><p><span data-ttu-id="42c27-136">**Waar wordt dit bewerkt:** pagina's worden bewerkt in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="42c27-136">**Where it's edited:** Pages are edited in the page editor.</span></span> <span data-ttu-id="42c27-137">U hoeft geen code te maken of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="42c27-137">No code is required to create or modify them.</span></span></p> |
| [<span data-ttu-id="42c27-138">Thema</span><span class="sxs-lookup"><span data-stu-id="42c27-138">Theme</span></span>](select-site-theme.md) | <p><span data-ttu-id="42c27-139">**Definitie:** thema's definiëren het trapsgewijze opmaakmodel (Cascading Style Sheet, CSS) en bepalen het uiterlijk van de modules die worden weergegeven op een pagina.</span><span class="sxs-lookup"><span data-stu-id="42c27-139">**Definition:** Themes define the Cascading Style Sheet (CSS), and determine the look and feel of the modules that are rendered on a page.</span></span></p><p><span data-ttu-id="42c27-140">**Waar wordt dit geselecteerd:** nadat een thema is geüpload naar uw site via Microsoft Dynamics Lifecycle Services (LCS), kan het worden geselecteerd als een eigenschap van de paginacontainermodule.</span><span class="sxs-lookup"><span data-stu-id="42c27-140">**Where it's selected:** After a theme is uploaded to your site by using Microsoft Dynamics Lifecycle Services (LCS), it can be selected as a property of the page container module.</span></span></p><p><span data-ttu-id="42c27-141">**Waar wordt dit bewerkt:** thema's worden momenteel gemaakt en bewerkt met de SDK.</span><span class="sxs-lookup"><span data-stu-id="42c27-141">**Where it's edited:** Themes are currently created and edited by using the SDK.</span></span> <span data-ttu-id="42c27-142">Ze worden vervolgens met LCS naar uw site geüpload.</span><span class="sxs-lookup"><span data-stu-id="42c27-142">They are then uploaded to your site by using LCS.</span></span></p> |
| [<span data-ttu-id="42c27-143">Fragment</span><span class="sxs-lookup"><span data-stu-id="42c27-143">Fragment</span></span>](work-with-fragments.md) | <p><span data-ttu-id="42c27-144">**Definitie:** fragmenten zijn volledig geconfigureerde modules met gelokaliseerde inhoud die kunnen worden hergebruikt en centraal worden bijgewerkt op meerdere pagina's.</span><span class="sxs-lookup"><span data-stu-id="42c27-144">**Definition:** Fragments are fully configured modules that have localized content that can be reused and centrally updated across multiple pages.</span></span> <span data-ttu-id="42c27-145">Een fragment dat vanuit een koptekstmodule wordt gemaakt, kan bijvoorbeeld worden gebruikt in alle sjablonen en op alle pagina's van de site, en centraal worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="42c27-145">For example, a fragment that is created from a header module can be used in all templates and on all pages across your site, and centrally updated in one place.</span></span></p><p><span data-ttu-id="42c27-146">**Waar wordt dit geselecteerd:** fragmenten kunnen worden geselecteerd als modules kunnen worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="42c27-146">**Where it's selected:** Fragments can be selected wherever modules can be selected.</span></span> <span data-ttu-id="42c27-147">Ze kunnen worden vervangen door een module om de efficiëntie te verbeteren door herbruikbare en gecentraliseerde ontwerpbewerkingen.</span><span class="sxs-lookup"><span data-stu-id="42c27-147">They can be substituted for a module to help increase efficiency through reusable and centralized authoring.</span></span></p><p><span data-ttu-id="42c27-148">**Waar wordt dit bewerkt:** fragmenten worden bewerkt in de fragmenteditor.</span><span class="sxs-lookup"><span data-stu-id="42c27-148">**Where it's edited:** Fragments are edited in the fragment editor.</span></span> <span data-ttu-id="42c27-149">U hoeft geen code te maken of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="42c27-149">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="42c27-150">URL</span><span class="sxs-lookup"><span data-stu-id="42c27-150">URL</span></span> | <p><span data-ttu-id="42c27-151">**Definitie:** URL's (Uniform Resource Locator) zijn adressen die verwijzen naar webpagina's of andere URL's.</span><span class="sxs-lookup"><span data-stu-id="42c27-151">**Definition:** Uniform resource locators (URLs) are addresses that point to webpages or other URLs.</span></span></p><p><span data-ttu-id="42c27-152">**Waar wordt dit geselecteerd:** URL's worden geselecteerd wanneer koppelingen tussen pagina's vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="42c27-152">**Where it's selected:** URLs are selected wherever links between pages are required.</span></span></p><p><span data-ttu-id="42c27-153">**Waar wordt dit bewerkt:** URL's worden bewerkt in de URL-editor.</span><span class="sxs-lookup"><span data-stu-id="42c27-153">**Where it's edited:** URLs are edited in the URL editor.</span></span> <span data-ttu-id="42c27-154">U hoeft geen code te maken of te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="42c27-154">No code is required to create or modify them.</span></span></p> |
| <span data-ttu-id="42c27-155">Asset</span><span class="sxs-lookup"><span data-stu-id="42c27-155">Asset</span></span> | <p><span data-ttu-id="42c27-156">**Definitie:** assets zijn binaire bestanden met een extensie zoals jpg, docx, pdf of mpg.</span><span class="sxs-lookup"><span data-stu-id="42c27-156">**Definition:** Assets are file binaries that have an extension such as .jpg, .docx, .pdf, or .mpg.</span></span></p><p><span data-ttu-id="42c27-157">**Waar wordt dit geselecteerd:** assets worden geselecteerd als module-eigenschappen voor modules waarvoor ze zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="42c27-157">**Where it's selected:** Assets are selected as module properties for modules that require them.</span></span></p><p><span data-ttu-id="42c27-158">**Waar wordt dit bewerkt:** assets worden geüpload en gekoppelde metagegevens worden bewerkt in de assetmanager.</span><span class="sxs-lookup"><span data-stu-id="42c27-158">**Where it's edited:** Assets are uploaded, and associated metadata is edited in the asset manager.</span></span></p> |

## <a name="additional-resources"></a><span data-ttu-id="42c27-159">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="42c27-159">Additional resources</span></span>

[<span data-ttu-id="42c27-160">Manieren om inhoud toe te voegen</span><span class="sxs-lookup"><span data-stu-id="42c27-160">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="42c27-161">Statussen en levenscyclus document</span><span class="sxs-lookup"><span data-stu-id="42c27-161">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="42c27-162">Werken met modules</span><span class="sxs-lookup"><span data-stu-id="42c27-162">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="42c27-163">Werken met fragmenten</span><span class="sxs-lookup"><span data-stu-id="42c27-163">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="42c27-164">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="42c27-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="42c27-165">Sitenavigatie aanpassen</span><span class="sxs-lookup"><span data-stu-id="42c27-165">Customize site navigation</span></span>](customize-site-navigation.md)