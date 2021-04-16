---
title: Werken met fragmenten
description: In dit onderwerp wordt beschreven waarom, wanneer en hoe u fragmenten gebruikt in Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1fa55ab83562983273768895db61032ec7199fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793940"
---
# <a name="work-with-fragments"></a><span data-ttu-id="ad82a-103">Werken met fragmenten</span><span class="sxs-lookup"><span data-stu-id="ad82a-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad82a-104">In dit onderwerp wordt beschreven waarom, wanneer en hoe u fragmenten gebruikt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad82a-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ad82a-105">Fragmenten bieden een gecentraliseerde ontwerpervaring voor moduleconfiguraties die op de gehele site opnieuw moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ad82a-105">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="ad82a-106">Kopteksten, voetteksten en banners worden vaak vaak als fragmenten geconfigureerd, omdat ze over meerdere pagina's worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="ad82a-106">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="ad82a-107">U kunt fragmenten zien als miniatuurwebpagina's die in andere pagina's op uw site kunnen worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="ad82a-107">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="ad82a-108">Fragmenten hebben hun eigen levenscyclus.</span><span class="sxs-lookup"><span data-stu-id="ad82a-108">Fragments have their own lifecycle.</span></span> <span data-ttu-id="ad82a-109">Met andere woorden ze worden in de ontwerphulpmiddelen als onafhankelijke entiteiten gemaakt, als verwijzing genoemd, bijgewerkt en verwijderd.</span><span class="sxs-lookup"><span data-stu-id="ad82a-109">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="ad82a-110">Nadat u fragmenten hebt geconfigureerd, kunt u deze gebruiken waar modules in uw sitestructuur kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ad82a-110">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="ad82a-111">U kunt naar fragmenten verwijzen via pagina's, in indelingen, in sjablonen en in andere fragmenten.</span><span class="sxs-lookup"><span data-stu-id="ad82a-111">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="ad82a-112">Fragmenten kunnen tot zeven niveaus diep in andere fragmenten worden genest.</span><span class="sxs-lookup"><span data-stu-id="ad82a-112">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="ad82a-113">Als u bijvoorbeeld een seizoensgebonden evenement wilt promoten op meerdere pagina's op onze site, kunt u een fragment gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ad82a-113">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="ad82a-114">De eerste stap bij het maken van een nieuw fragment is het selecteren van het type module waarin u wilt beginnen.</span><span class="sxs-lookup"><span data-stu-id="ad82a-114">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="ad82a-115">Voor dit voorbeeld kunt u het fragment maken vanuit een heldmodule.</span><span class="sxs-lookup"><span data-stu-id="ad82a-115">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="ad82a-116">Fragmenten kunnen worden opgebouwd uit elk type module.</span><span class="sxs-lookup"><span data-stu-id="ad82a-116">Fragments can be built from any module type.</span></span>

<span data-ttu-id="ad82a-117">Vervolgens kunt u het heldfragment met uw specifieke promotie-inhoud configureren.</span><span class="sxs-lookup"><span data-stu-id="ad82a-117">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="ad82a-118">U kunt het ook lokaliseren indien nodig.</span><span class="sxs-lookup"><span data-stu-id="ad82a-118">You can also localize it as you require.</span></span> <span data-ttu-id="ad82a-119">Het nieuwe zelfstandige heldfragment kan vervolgens worden gebruikt als een vooraf geconfigureerde module in de hele site.</span><span class="sxs-lookup"><span data-stu-id="ad82a-119">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="ad82a-120">U kunt het eenvoudig toevoegen aan sjablonen, specifieke pagina's of andere fragmenten die heldmodules kunnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="ad82a-120">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="ad82a-121">Alle plaatsen waar het fragment wordt toegevoegd, zijn verwijzingen naar het centrale heldfragment dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ad82a-121">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="ad82a-122">Als u wijzigingen in het fragment publiceert, worden deze wijzigingen direct doorgevoerd op alle plaatsen binnen de site waar naar het fragment wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="ad82a-122">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="ad82a-123">Hierdoor beschikken fragmenten over een krachtige en efficiënte manier om moduleconfiguraties op een site te hergebruiken en centraal te beheren.</span><span class="sxs-lookup"><span data-stu-id="ad82a-123">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="ad82a-124">Door ze effectief te gebruiken, kunt u de flexibiliteit aanzienlijk verhogen en de kosten voor het beheren van de inhoud van de site verminderen.</span><span class="sxs-lookup"><span data-stu-id="ad82a-124">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="ad82a-125">In de volgende afbeelding ziet u hoe fragmenten kunnen worden gebruikt om het ontwerpen van gedeelde moduleconfiguraties op een e-commerce-site te centraliseren.</span><span class="sxs-lookup"><span data-stu-id="ad82a-125">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![In de afbeelding ziet u hoe fragmenten kunnen worden gebruikt om het ontwerpen van gedeelde moduleconfiguraties op een e-commerce-site te centraliseren.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="ad82a-127">Een fragment maken</span><span class="sxs-lookup"><span data-stu-id="ad82a-127">Create a fragment</span></span>

<span data-ttu-id="ad82a-128">U kunt een nieuw fragment maken of een bestaande moduleconfiguratie als fragment opslaan.</span><span class="sxs-lookup"><span data-stu-id="ad82a-128">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="ad82a-129">Een bestaande module configuratie als fragment opslaan</span><span class="sxs-lookup"><span data-stu-id="ad82a-129">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="ad82a-130">Voer de volgende stappen uit om een eerder geconfigureerde module te converteren naar een herbruikbaar fragment in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="ad82a-130">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad82a-131">Open een pagina of sjabloon die de module bevat die u naar een fragment wilt converteren.</span><span class="sxs-lookup"><span data-stu-id="ad82a-131">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="ad82a-132">Selecteer de eerder geconfigureerde module in het overzichtsvenster links of rechtstreeks in de visuele paginabouwer.</span><span class="sxs-lookup"><span data-stu-id="ad82a-132">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="ad82a-133">Selecteer het beletselteken (**...**) naast de naam van de module in het overzichtsvenster of op de werkbalk van de geselecteerde module in visuele paginabouwer.</span><span class="sxs-lookup"><span data-stu-id="ad82a-133">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="ad82a-134">Selecteer **Delen als fragment**.</span><span class="sxs-lookup"><span data-stu-id="ad82a-134">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="ad82a-135">Voer in het dialoogvenster **Fragment opslaan als** een naam voor het fragment in.</span><span class="sxs-lookup"><span data-stu-id="ad82a-135">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="ad82a-136">Selecteer **OK** om de moduleconfiguratie op te slaan als een fragment dat aan andere pagina's kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="ad82a-136">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="ad82a-137">Een nieuw fragment maken</span><span class="sxs-lookup"><span data-stu-id="ad82a-137">Create a new fragment</span></span>

<span data-ttu-id="ad82a-138">Voer de volgende stappen uit om een nieuw fragment te maken in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="ad82a-138">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad82a-139">Selecteer **Fragmenten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="ad82a-139">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="ad82a-140">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ad82a-140">Select **New**.</span></span> <span data-ttu-id="ad82a-141">Het dialoogvenster **Nieuw fragment** verschijnt waarin alle beschikbare moduletypen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ad82a-141">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="ad82a-142">Zoals eerder is vermeld, kunnen fragmenten vanuit elk type module worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ad82a-142">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="ad82a-143">Selecteer een moduletype voor het fragment.</span><span class="sxs-lookup"><span data-stu-id="ad82a-143">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="ad82a-144">Selecteer een algemeen containermoduletype voor de meeste flexibiliteit wanneer u het fragment later moet bijwerken en configureren.</span><span class="sxs-lookup"><span data-stu-id="ad82a-144">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="ad82a-145">Fragmenten op een pagina toevoegen, verwijderen of bewerken</span><span class="sxs-lookup"><span data-stu-id="ad82a-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="ad82a-146">In de volgende procedures wordt beschreven hoe u fragmenten toevoegt en verwijdert.</span><span class="sxs-lookup"><span data-stu-id="ad82a-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="ad82a-147">Een fragment toevoegen</span><span class="sxs-lookup"><span data-stu-id="ad82a-147">Add a fragment</span></span>

<span data-ttu-id="ad82a-148">Voer de volgende stappen uit om een fragment aan een pagina toe te voegen in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="ad82a-148">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad82a-149">Selecteer in het overzichtsvenster links of rechtstreeks in visuele paginabouwer een container of vak waaraan onderliggende modules kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="ad82a-149">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="ad82a-150">Selecteer het weglatingsteken (**...**) naast de naam van de container of het vak.</span><span class="sxs-lookup"><span data-stu-id="ad82a-150">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="ad82a-151">Als alternatief kunt u, als u visuele paginabouwer gebruikt, het plusteken (**+**) selecteren.</span><span class="sxs-lookup"><span data-stu-id="ad82a-151">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="ad82a-152">Selecteer **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ad82a-152">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="ad82a-153">Als nieuwe onderliggende modules niet door de container of het vak worden ondersteund, is de optie **Fragment toevoegen** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="ad82a-153">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="ad82a-154">Zoek in het dialoogvenster **Fragment selecteren** een fragment dat u wilt toevoegen en selecteer het.</span><span class="sxs-lookup"><span data-stu-id="ad82a-154">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="ad82a-155">Als er geen beschikbare fragmenten worden weergegeven, moet u mogelijk eerst een fragment maken van een moduletype dat door de geselecteerde container of of het geselecteerde vak wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="ad82a-155">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="ad82a-156">Selecteer het gewenste fragment en voeg het toe aan de container of het vak op uw pagina.</span><span class="sxs-lookup"><span data-stu-id="ad82a-156">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="ad82a-157">De modules die in een container of vak zijn toegestaan, worden gedefinieerd door de paginasjabloon of de eigen definities van de modules.</span><span class="sxs-lookup"><span data-stu-id="ad82a-157">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="ad82a-158">Een fragment verwijderen</span><span class="sxs-lookup"><span data-stu-id="ad82a-158">Remove a fragment</span></span>

<span data-ttu-id="ad82a-159">Voer de volgende stappen uit om een fragment te verwijderen uit een vak of container op een pagina in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="ad82a-159">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad82a-160">Selecteer in het overzichtsvenster aan de linkerkant het weglatingsteken (**...**) naast het fragment dat u wilt verwijderen en selecteer vervolgens de knop Prullenbak.</span><span class="sxs-lookup"><span data-stu-id="ad82a-160">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="ad82a-161">U kunt ook het fragment in visuele paginabouwer selecteren en het symbool Prullenbak op de werkbalk van de fragment selecteren.</span><span class="sxs-lookup"><span data-stu-id="ad82a-161">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="ad82a-162">Wanneer u wordt gevraagd te bevestigen dat u het fragment wilt verwijderen, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="ad82a-162">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="ad82a-163">Wanneer u een fragment van een pagina verwijdert, verwijdert u alleen de verwijzing naar het fragment van die pagina.</span><span class="sxs-lookup"><span data-stu-id="ad82a-163">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="ad82a-164">U verwijdert **niet** het fragment van uw site.</span><span class="sxs-lookup"><span data-stu-id="ad82a-164">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="ad82a-165">Als u fragmenten van uw site wilt verwijderen, moet u de gebruikersinterface voor fragmentcontrole gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ad82a-165">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="ad82a-166">U kunt fragmenten alleen van een site verwijderen als er op dat moment niet door pagina's, sjablonen of andere fragmenten naar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="ad82a-166">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="ad82a-167">Een fragment bewerken</span><span class="sxs-lookup"><span data-stu-id="ad82a-167">Edit a fragment</span></span>

<span data-ttu-id="ad82a-168">Als u fragmenten wilt bewerken, moet u de gebruikersinterface voor de fragmenteditor gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ad82a-168">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="ad82a-169">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="ad82a-169">This restriction is by design.</span></span> <span data-ttu-id="ad82a-170">Hierdoor kunnen ontwerpers het proces van het bewerken van modules voor een bepaalde pagina niet verwarren met het proces voor het bewerken van fragmenten die op veel pagina's kunnen worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="ad82a-170">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="ad82a-171">Voer de volgende stappen uit om een fragment te bewerken in Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="ad82a-171">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad82a-172">Selecteer **Fragmenten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="ad82a-172">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="ad82a-173">Selecteer onder **Fragmenten** het fragment dat u wilt bewerken.</span><span class="sxs-lookup"><span data-stu-id="ad82a-173">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="ad82a-174">Bewerk waar nodig de module-eigenschappen en de structuur van het fragment.</span><span class="sxs-lookup"><span data-stu-id="ad82a-174">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="ad82a-175">Het proces lijkt op het proces voor het bewerken van modules in de pagina-editorweergave.</span><span class="sxs-lookup"><span data-stu-id="ad82a-175">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="ad82a-176">U kunt een fragment ook bewerken door het te selecteren op een pagina, in een sjabloon of in een bovenliggend fragment en vervolgens **Fragment bewerken** te selecteren in het deelvenster Eigenschappen aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="ad82a-176">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad82a-177">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="ad82a-177">Additional resources</span></span>

[<span data-ttu-id="ad82a-178">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="ad82a-178">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="ad82a-179">Werken met sjablonen</span><span class="sxs-lookup"><span data-stu-id="ad82a-179">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="ad82a-180">Werken met vooraf ingestelde indelingen</span><span class="sxs-lookup"><span data-stu-id="ad82a-180">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="ad82a-181">Werken met publicatiegroepen</span><span class="sxs-lookup"><span data-stu-id="ad82a-181">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
