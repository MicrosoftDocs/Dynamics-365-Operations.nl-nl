---
title: Werken met modules
description: In dit onderwerp wordt beschreven hoe en wanneer u modules in Microsoft Dynamics 365 Commerce gebruikt.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 06a26e5dfd35bf229e67ed27213210d0da726bdf
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698068"
---
# <a name="work-with-modules"></a><span data-ttu-id="efb35-103">Werken met modules</span><span class="sxs-lookup"><span data-stu-id="efb35-103">Work with modules</span></span>

<span data-ttu-id="efb35-104">In dit onderwerp wordt beschreven hoe en wanneer u modules in Microsoft Dynamics 365 Commerce gebruikt.</span><span class="sxs-lookup"><span data-stu-id="efb35-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="efb35-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="efb35-105">Overview</span></span>

<span data-ttu-id="efb35-106">Modules zijn logische bouwstenen die de paginastructuur vormen en verschillende doeleinden en bereiken hebben.</span><span class="sxs-lookup"><span data-stu-id="efb35-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="efb35-107">Sommige modules zijn containers op een hoog niveau en zijn alleen bedoeld voor het vasthouden en organiseren van andere modules (onderliggende modules).</span><span class="sxs-lookup"><span data-stu-id="efb35-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="efb35-108">Andere modules, zoals een eenvoudige afbeeldingsmodule, hebben een specifiek doel.</span><span class="sxs-lookup"><span data-stu-id="efb35-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="efb35-109">Modules, zoals carrouselmodules, vallen ergens tussen deze twee categorieën.</span><span class="sxs-lookup"><span data-stu-id="efb35-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="efb35-110">Standaard bevat uw site Dynamics 365 Commerce een bibliotheekmodule uit het startpakket waarmee u de meeste elementaire e-commerce-scenario's kunt realiseren.</span><span class="sxs-lookup"><span data-stu-id="efb35-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="efb35-111">U kunt een complete e-commerce-site samenstellen met behulp van deze modules.</span><span class="sxs-lookup"><span data-stu-id="efb35-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="efb35-112">U kunt deze modules echter ook aanpassen of nieuwe aangepaste modules maken voor specifieke behoeften.</span><span class="sxs-lookup"><span data-stu-id="efb35-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="efb35-113">Als u aangepaste modules wilt maken, is er een module-ontwerp-SDK (Software Development Kit) beschikbaar om u te helpen bij het maken van een aangepaste modulebibliotheek.</span><span class="sxs-lookup"><span data-stu-id="efb35-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="efb35-114">Containermodules en vakken</span><span class="sxs-lookup"><span data-stu-id="efb35-114">Container modules and slots</span></span>

<span data-ttu-id="efb35-115">Zoals eerder is vermeld, bevatten sommige modules onderliggende modules.</span><span class="sxs-lookup"><span data-stu-id="efb35-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="efb35-116">Deze modules worden *containers* genoemd en kunnen hiërarchieën van geneste modules bevatten.</span><span class="sxs-lookup"><span data-stu-id="efb35-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="efb35-117">Containermodules bevatten *vakken*.</span><span class="sxs-lookup"><span data-stu-id="efb35-117">Container modules include *slots*.</span></span> <span data-ttu-id="efb35-118">Vakken worden gebruikt om de indeling en het doel van onderliggende modules in de container te verwerken.</span><span class="sxs-lookup"><span data-stu-id="efb35-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="efb35-119">Een voorbeeld is een containermodule voor een basispagina (een module op het hoogste niveau voor een willekeurige pagina) waarin verschillende belangrijke vakken worden gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="efb35-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="efb35-120">Een koptekstvak</span><span class="sxs-lookup"><span data-stu-id="efb35-120">A header slot</span></span>
- <span data-ttu-id="efb35-121">Een tekstvak</span><span class="sxs-lookup"><span data-stu-id="efb35-121">A body slot</span></span>
- <span data-ttu-id="efb35-122">Een voettekstvak</span><span class="sxs-lookup"><span data-stu-id="efb35-122">A footer slot</span></span>

<span data-ttu-id="efb35-123">De ontwikkelaar van de module definieert deze vakken en bepaalt welke onderliggende modules en hoeveel onderliggende modules direct in de module kunnen worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="efb35-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="efb35-124">Het koptekstvak kan bijvoorbeeld slechts één module van het type **koptekstmodule** ondersteunen, terwijl het vak voor de hoofdtekst een onbeperkt aantal modules van elk type kan ondersteunen (behalve andere containermodules).</span><span class="sxs-lookup"><span data-stu-id="efb35-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="efb35-125">In de ontwerphulpmiddelen hoeven de auteurs van de pagina niet van tevoren te weten welke modules in elk vak kunnen worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="efb35-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="efb35-126">Wanneer de auteur van een pagina een vak selecteert en een module wil selecteren om hieraan toe te voegen, wordt een gefilterde weergave van de moduletypen getoond die voor die sleuf worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="efb35-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="efb35-127">Inhoudsmodules</span><span class="sxs-lookup"><span data-stu-id="efb35-127">Content modules</span></span>

<span data-ttu-id="efb35-128">Inhoudsmodules bevatten inhoud en media-elementen, zoals tekst (bijvoorbeeld koppen, alinea's en koppelingen) of activaverwijzingen (bijvoorbeeld afbeeldingen, video en PDF's).</span><span class="sxs-lookup"><span data-stu-id="efb35-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="efb35-129">Voorbeelden van typische inhoudsmodules zijn **held**, **functie** en **banner**.</span><span class="sxs-lookup"><span data-stu-id="efb35-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="efb35-130">Modules van deze drie typen kunnen tekst of media bevatten, en vereisen geen onderliggende modules om iets zichtbaar te maken op een pagina.</span><span class="sxs-lookup"><span data-stu-id="efb35-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="efb35-131">Bij de meeste standaard dagelijkse activiteiten voor pagina's en inhoud zijn inhoudsmodules betrokken, voornamelijk omdat deze modules de feitelijke inhoud definiëren die wordt weergegeven in de bovenliggende containermodules.</span><span class="sxs-lookup"><span data-stu-id="efb35-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="efb35-132">Er zijn veel inhoudsmodules beschikbaar die doorgaans de laatste onderdelen zijn die u aan de hiërarchie van geneste modules van de pagina toevoegt.</span><span class="sxs-lookup"><span data-stu-id="efb35-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="efb35-133">In de volgende afbeelding wordt aangegeven hoe modules worden genest binnen bovenliggende containermodulevakken.</span><span class="sxs-lookup"><span data-stu-id="efb35-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Modules nesten](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="efb35-135">Modules toevoegen of verwijderen</span><span class="sxs-lookup"><span data-stu-id="efb35-135">Add or remove modules</span></span>

<span data-ttu-id="efb35-136">In de volgende procedures wordt beschreven hoe u modules toevoegt en verwijdert.</span><span class="sxs-lookup"><span data-stu-id="efb35-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="efb35-137">Een module toevoegen</span><span class="sxs-lookup"><span data-stu-id="efb35-137">Add a module</span></span>

<span data-ttu-id="efb35-138">Voer deze stappen uit om een vak of een container aan een pagina toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="efb35-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="efb35-139">Selecteer in het overzichtsvenster aan de linkerkant een container of een vak waaraan een onderliggende module kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="efb35-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efb35-140">De moduleontwerper definieert de lijst met moduletypen die aan een bepaald modulevak kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="efb35-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="efb35-141">Sjabloonontwerpers kunnen de toegestane moduleopties vervolgens verfijnen om een uniforme SEO-werking (Search Engine Optimization) te garanderen en een efficiënt ontwerp voor alle pagina's die op basis van een bepaalde sjabloon worden gebouwd.</span><span class="sxs-lookup"><span data-stu-id="efb35-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="efb35-142">Selecteer de knop met het weglatingsteken (**...**) voor de module en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="efb35-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="efb35-143">Het dialoogvenster **Module toevoegen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="efb35-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="efb35-144">Dit dialoogvenster wordt automatisch gefilterd, zodat alleen modules worden weergegeven die in de geselecteerde container of het geselecteerde vak worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="efb35-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="efb35-145">De lijst met modules wordt bepaald door de sjabloon van de pagina of door de containermoduledefinitie.</span><span class="sxs-lookup"><span data-stu-id="efb35-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="efb35-146">Als nieuwe onderliggende modules niet door een container of vak worden ondersteund, is de optie **Module toevoegen** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="efb35-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="efb35-147">Zoek in het dialoogvenster en selecteer een module die u aan de pagina wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="efb35-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="efb35-148">**Functie** en **Held** zijn goede typen modules voor beginners.</span><span class="sxs-lookup"><span data-stu-id="efb35-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="efb35-149">Klik op **OK** om de geselecteerde module toe te voegen aan de geselecteerde container of het vak op de pagina.</span><span class="sxs-lookup"><span data-stu-id="efb35-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="efb35-150">Een module verwijderen</span><span class="sxs-lookup"><span data-stu-id="efb35-150">Remove a module</span></span>

<span data-ttu-id="efb35-151">Voer deze stappen uit om een module uit een vak of een container op een pagina te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="efb35-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="efb35-152">Selecteer in het overzichtsvenster aan de linkerkant de knop met het weglatingsteken naast de naam van de module die u wilt verwijderen en selecteer vervolgens de knop Prullenbak.</span><span class="sxs-lookup"><span data-stu-id="efb35-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="efb35-153">Wanneer u wordt gevraagd te bevestigen dat u de module wilt verwijderen, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="efb35-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="efb35-154">Modules configureren</span><span class="sxs-lookup"><span data-stu-id="efb35-154">Configure modules</span></span>

<span data-ttu-id="efb35-155">In de volgende procedures wordt beschreven hoe u inhouds- en containermodules configureert.</span><span class="sxs-lookup"><span data-stu-id="efb35-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="efb35-156">Een inhoudsmodule configureren</span><span class="sxs-lookup"><span data-stu-id="efb35-156">Configure a content module</span></span>

<span data-ttu-id="efb35-157">Voer de volgende stappen uit om een inhoudsmodule op een pagina te configureren.</span><span class="sxs-lookup"><span data-stu-id="efb35-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="efb35-158">Selecteer in het overzichtsvenster aan de linkerkant een type inhoudsmodule (bijvoorbeeld **functie**, **held** of **banner**).</span><span class="sxs-lookup"><span data-stu-id="efb35-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="efb35-159">Vouw in het deelvenster Eigenschappen rechts de geneste besturingselementen uit door de kopteksten te selecteren en stel de vereiste waarden voor besturingselementen in.</span><span class="sxs-lookup"><span data-stu-id="efb35-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="efb35-160">Als het deelvenster Eigenschappen een sectie **Gegevensconfiguratie** bevat, selecteert u dit om het uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="efb35-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="efb35-161">Anders gaat u naar stap 5.</span><span class="sxs-lookup"><span data-stu-id="efb35-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="efb35-162">Als er een knop **Gegevensbron toevoegen** is, selecteert u deze en selecteert u vervolgens de toe te voegen inhoudsitems.</span><span class="sxs-lookup"><span data-stu-id="efb35-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="efb35-163">Voer instellingen in voor verplichte of gewenste modulebesturingselementen.</span><span class="sxs-lookup"><span data-stu-id="efb35-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="efb35-164">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="efb35-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="efb35-165">Een containermodule configureren</span><span class="sxs-lookup"><span data-stu-id="efb35-165">Configure a container module</span></span>

<span data-ttu-id="efb35-166">Voer de volgende stappen uit om een containermodule op een pagina te configureren.</span><span class="sxs-lookup"><span data-stu-id="efb35-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="efb35-167">Selecteer een containermodule op de pagina (bijvoorbeeld een carrousel of een vloeibare containermodule).</span><span class="sxs-lookup"><span data-stu-id="efb35-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="efb35-168">Vouw in het deelvenster Eigenschappen rechts de geneste besturingselementen uit door de kopteksten te selecteren en stel de vereiste waarden voor besturingselementen in.</span><span class="sxs-lookup"><span data-stu-id="efb35-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="efb35-169">Selecteer in het overzichtsvenster aan de linkerkant de knop met het weglatingsteken naast de naam van de containermodule of van vakken in de container, en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="efb35-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="efb35-170">Voeg vervolgens onderliggende modules toe aan de geselecteerde container.</span><span class="sxs-lookup"><span data-stu-id="efb35-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="efb35-171">Zie de procedure [Een module toevoegen](#add-a-module) eerder in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="efb35-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="efb35-172">Als er meerdere onderliggende modules op hetzelfde niveau zijn in een bovenliggende container, kunt u de weergavevolgorde in de bovenliggende container wijzigen.</span><span class="sxs-lookup"><span data-stu-id="efb35-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="efb35-173">Selecteer de knop met het weglatingsteken voor een module en gebruik vervolgens de knoppen pijl-omhoog en pijl-omlaag.</span><span class="sxs-lookup"><span data-stu-id="efb35-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efb35-174">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="efb35-174">Additional resources</span></span>

[<span data-ttu-id="efb35-175">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="efb35-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="efb35-176">Werken met sjablonen</span><span class="sxs-lookup"><span data-stu-id="efb35-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="efb35-177">Werken met vooraf ingestelde indelingen</span><span class="sxs-lookup"><span data-stu-id="efb35-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="efb35-178">Werken met fragmenten</span><span class="sxs-lookup"><span data-stu-id="efb35-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="efb35-179">Een containermodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="efb35-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="efb35-180">Modules voor het plaatsen van inhoud aan een pagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="efb35-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)
