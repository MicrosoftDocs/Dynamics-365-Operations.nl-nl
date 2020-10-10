---
title: Werken met fragmenten
description: In dit onderwerp wordt beschreven waarom, wanneer en hoe u fragmenten in gebruikt Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 07/31/2020
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
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 671caf1feeb7ac9e7d5a166c5de12540ab9b9792
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818345"
---
# <a name="work-with-fragments"></a><span data-ttu-id="0470b-103">Werken met fragmenten</span><span class="sxs-lookup"><span data-stu-id="0470b-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="0470b-104">In dit onderwerp wordt beschreven waarom, wanneer en hoe u fragmenten in gebruikt Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0470b-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0470b-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="0470b-105">Overview</span></span>

<span data-ttu-id="0470b-106">Fragmenten bieden een gecentraliseerde ontwerpervaring voor moduleconfiguraties die op de gehele site opnieuw moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0470b-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="0470b-107">Kopteksten, voetteksten en banners worden vaak vaak als fragmenten geconfigureerd, omdat ze over meerdere pagina's worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="0470b-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="0470b-108">U kunt fragmenten zien als miniatuurwebpagina's die in andere pagina's op uw site kunnen worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="0470b-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="0470b-109">Fragmenten hebben hun eigen levenscyclus.</span><span class="sxs-lookup"><span data-stu-id="0470b-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="0470b-110">Met andere woorden ze worden in de ontwerphulpmiddelen als onafhankelijke entiteiten gemaakt, als verwijzing genoemd, bijgewerkt en verwijderd.</span><span class="sxs-lookup"><span data-stu-id="0470b-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="0470b-111">Nadat u fragmenten hebt geconfigureerd, kunt u deze gebruiken waar modules in uw sitestructuur kunnen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0470b-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="0470b-112">U kunt naar fragmenten verwijzen via pagina's, in indelingen, in sjablonen en in andere fragmenten.</span><span class="sxs-lookup"><span data-stu-id="0470b-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="0470b-113">Fragmenten kunnen tot zeven niveaus diep in andere fragmenten worden genest.</span><span class="sxs-lookup"><span data-stu-id="0470b-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="0470b-114">Als u bijvoorbeeld een seizoensgebonden evenement wilt promoten op meerdere pagina's op onze site, kunt u een fragment gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0470b-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="0470b-115">De eerste stap bij het maken van een nieuw fragment is het selecteren van het type module waarin u wilt beginnen.</span><span class="sxs-lookup"><span data-stu-id="0470b-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="0470b-116">Voor dit voorbeeld kunt u het fragment maken vanuit een heldmodule.</span><span class="sxs-lookup"><span data-stu-id="0470b-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="0470b-117">Fragmenten kunnen worden opgebouwd uit elk type module.</span><span class="sxs-lookup"><span data-stu-id="0470b-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="0470b-118">Vervolgens kunt u het heldfragment met uw specifieke promotie-inhoud configureren.</span><span class="sxs-lookup"><span data-stu-id="0470b-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="0470b-119">U kunt het ook lokaliseren indien nodig.</span><span class="sxs-lookup"><span data-stu-id="0470b-119">You can also localize it as you require.</span></span> <span data-ttu-id="0470b-120">Het nieuwe zelfstandige heldfragment kan vervolgens worden gebruikt als een vooraf geconfigureerde module in de hele site.</span><span class="sxs-lookup"><span data-stu-id="0470b-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="0470b-121">U kunt het eenvoudig toevoegen aan sjablonen, specifieke pagina's of andere fragmenten die heldmodules kunnen bevatten.</span><span class="sxs-lookup"><span data-stu-id="0470b-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="0470b-122">Alle plaatsen waar het fragment wordt toegevoegd, zijn verwijzingen naar het centrale heldfragment dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0470b-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="0470b-123">Als u wijzigingen in het fragment publiceert, worden deze wijzigingen direct doorgevoerd op alle plaatsen binnen de site waar naar het fragment wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="0470b-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="0470b-124">Hierdoor beschikken fragmenten over een krachtige en efficiënte manier om moduleconfiguraties op een site te hergebruiken en centraal te beheren.</span><span class="sxs-lookup"><span data-stu-id="0470b-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="0470b-125">Door ze effectief te gebruiken, kunt u de flexibiliteit aanzienlijk verhogen en de kosten voor het beheren van de inhoud van de site verminderen.</span><span class="sxs-lookup"><span data-stu-id="0470b-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="0470b-126">In de volgende afbeelding ziet u hoe fragmenten kunnen worden gebruikt om het ontwerpen van gedeelde moduleconfiguraties op een e-commerce-site te centraliseren.</span><span class="sxs-lookup"><span data-stu-id="0470b-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![In de afbeelding ziet u hoe fragmenten kunnen worden gebruikt om het ontwerpen van gedeelde moduleconfiguraties op een e-commerce-site te centraliseren.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="0470b-128">Een fragment maken</span><span class="sxs-lookup"><span data-stu-id="0470b-128">Create a fragment</span></span>

<span data-ttu-id="0470b-129">U kunt een nieuw fragment maken of een bestaande moduleconfiguratie als fragment opslaan.</span><span class="sxs-lookup"><span data-stu-id="0470b-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="0470b-130">Een bestaande module configuratie als fragment opslaan</span><span class="sxs-lookup"><span data-stu-id="0470b-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="0470b-131">Voer de volgende stappen uit om een eerder geconfigureerde module te converteren naar een herbruikbaar fragment.</span><span class="sxs-lookup"><span data-stu-id="0470b-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="0470b-132">Open een pagina of sjabloon die de module bevat die u naar een fragment wilt converteren.</span><span class="sxs-lookup"><span data-stu-id="0470b-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="0470b-133">Selecteer in het overzichtsvenster links of rechtstreeks op het hoofdtekenpapier de eerder geconfigureerde module.</span><span class="sxs-lookup"><span data-stu-id="0470b-133">In the outline pane on the left or directly in the main canvas, select the previously configured module.</span></span>
1. <span data-ttu-id="0470b-134">Selecteer het weglatingsteken (**...**) naast de naam van de module in het overzichtsvenster of op de werkbalk van de geselecteerde module op het tekenpapier.</span><span class="sxs-lookup"><span data-stu-id="0470b-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in the canvas.</span></span> 
1. <span data-ttu-id="0470b-135">Selecteer **Delen als paginafragment**.</span><span class="sxs-lookup"><span data-stu-id="0470b-135">Select **Share as Page Fragment**.</span></span> 
1. <span data-ttu-id="0470b-136">Voer in het dialoogvenster **Paginafragment opslaan als** een naam voor het fragment in.</span><span class="sxs-lookup"><span data-stu-id="0470b-136">In the **Save as Page Fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="0470b-137">Selecteer **OK** om de moduleconfiguratie op te slaan als een fragment dat aan andere pagina's kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="0470b-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="0470b-138">In de volgende afbeelding ziet u hoe u een moduleconfiguratie als fragment kunt opslaan.</span><span class="sxs-lookup"><span data-stu-id="0470b-138">The following image shows how to save a module configuration as a fragment.</span></span>

![Een schermopname van het opslaan van een moduleconfiguratie als fragment](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="0470b-140">Een nieuw fragment maken</span><span class="sxs-lookup"><span data-stu-id="0470b-140">Create a new fragment</span></span>

<span data-ttu-id="0470b-141">Volg deze stappen om een nieuw fragment te maken.</span><span class="sxs-lookup"><span data-stu-id="0470b-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="0470b-142">Selecteer **Fragmenten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="0470b-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="0470b-143">Selecteer **Nieuw paginafragment**.</span><span class="sxs-lookup"><span data-stu-id="0470b-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="0470b-144">Er wordt een dialoogvenster weergegeven waarin alle beschikbare moduletypen worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0470b-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="0470b-145">Zoals eerder is vermeld, kunnen fragmenten vanuit elk type module worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0470b-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="0470b-146">Selecteer een moduletype voor het fragment.</span><span class="sxs-lookup"><span data-stu-id="0470b-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="0470b-147">In de volgende afbeelding ziet u waar u een nieuw fragment kunt maken.</span><span class="sxs-lookup"><span data-stu-id="0470b-147">The following image shows where to create a new fragment.</span></span>

![Een schermopname van waar u een nieuw fragment kunt maken](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="0470b-149">Selecteer een algemeen containermoduletype voor de meeste flexibiliteit wanneer u het fragment later moet bijwerken en configureren.</span><span class="sxs-lookup"><span data-stu-id="0470b-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="0470b-150">Fragmenten op een pagina toevoegen, verwijderen of bewerken</span><span class="sxs-lookup"><span data-stu-id="0470b-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="0470b-151">In de volgende procedures wordt beschreven hoe u fragmenten toevoegt en verwijdert.</span><span class="sxs-lookup"><span data-stu-id="0470b-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="0470b-152">Een fragment toevoegen</span><span class="sxs-lookup"><span data-stu-id="0470b-152">Add a fragment</span></span>

<span data-ttu-id="0470b-153">Om een fragment aan een pagina toe te voegen, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="0470b-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="0470b-154">Selecteer in het overzichtsvenster links of rechtstreeks op het hoofdtekenpapier een container of vak waaraan onderliggende modules kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="0470b-154">In the outline pane on the left or directly in the main canvas, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="0470b-155">Selecteer in het online deelvenster het weglatingsteken (**...**) naast de naam van de container of het vak.</span><span class="sxs-lookup"><span data-stu-id="0470b-155">In the online pane, select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="0470b-156">Als alternatief kunt u, als u het hoofdtekenpapier gebruikt, het plusteken (**+**) selecteren.</span><span class="sxs-lookup"><span data-stu-id="0470b-156">Alternately, if using the main canvas, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="0470b-157">Selecteer **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="0470b-157">Select **Add Fragment**.</span></span>

    ![Een schermopname van hoe u een bestaand fragment toevoegt aan een vak of container](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="0470b-159">Als nieuwe onderliggende modules niet door de container of het vak worden ondersteund, is de optie **Fragment toevoegen** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="0470b-159">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="0470b-160">Zoek in het dialoogvenster **Fragment toevoegen** een fragment dat u wilt toevoegen en voeg het toe.</span><span class="sxs-lookup"><span data-stu-id="0470b-160">In the **Add Fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="0470b-161">Als er geen beschikbare fragmenten worden weergegeven, moet u mogelijk eerst een fragment maken van een moduletype dat door de geselecteerde container of of het geselecteerde vak wordt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="0470b-161">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="0470b-162">Selecteer het gewenste fragment en voeg het toe aan de container of het vak op uw pagina.</span><span class="sxs-lookup"><span data-stu-id="0470b-162">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![Een schermopname van het modale venster voor de fragmentkiezer](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="0470b-164">De modules die in een container of vak zijn toegestaan, worden gedefinieerd door de paginasjabloon of de eigen definities van de modules.</span><span class="sxs-lookup"><span data-stu-id="0470b-164">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="0470b-165">Een fragment verwijderen</span><span class="sxs-lookup"><span data-stu-id="0470b-165">Remove a fragment</span></span>

<span data-ttu-id="0470b-166">Voer deze stappen uit om een fragment uit een vak of een container van een pagina te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="0470b-166">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="0470b-167">Selecteer in het overzichtsvenster aan de linkerkant het weglatingsteken (**...**) naast het fragment dat u wilt verwijderen en selecteer vervolgens de knop Prullenbak.</span><span class="sxs-lookup"><span data-stu-id="0470b-167">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="0470b-168">U kunt ook het fragment op het tekenpapier selecteren en het symbool Prullenbak op de werkbalk van de fragment selecteren.</span><span class="sxs-lookup"><span data-stu-id="0470b-168">Alternately, you can select the fragment in the canvas and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="0470b-169">Wanneer u wordt gevraagd te bevestigen dat u het fragment wilt verwijderen, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="0470b-169">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="0470b-170">Wanneer u een fragment van een pagina verwijdert, verwijdert u alleen de verwijzing naar het fragment van die pagina.</span><span class="sxs-lookup"><span data-stu-id="0470b-170">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="0470b-171">U verwijdert **niet** het fragment van uw site.</span><span class="sxs-lookup"><span data-stu-id="0470b-171">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="0470b-172">Als u fragmenten van uw site wilt verwijderen, moet u de gebruikersinterface voor fragmentcontrole gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0470b-172">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="0470b-173">U kunt fragmenten alleen van een site verwijderen als er op dat moment niet door pagina's, sjablonen of andere fragmenten naar wordt verwezen.</span><span class="sxs-lookup"><span data-stu-id="0470b-173">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="0470b-174">Een fragment bewerken</span><span class="sxs-lookup"><span data-stu-id="0470b-174">Edit a fragment</span></span>

<span data-ttu-id="0470b-175">Als u fragmenten wilt bewerken, moet u de gebruikersinterface voor de fragmenteditor gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0470b-175">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="0470b-176">Dit is zo ontworpen.</span><span class="sxs-lookup"><span data-stu-id="0470b-176">This restriction is by design.</span></span> <span data-ttu-id="0470b-177">Hierdoor kunnen ontwerpers het proces van het bewerken van modules voor een bepaalde pagina niet verwarren met het proces voor het bewerken van fragmenten die op veel pagina's kunnen worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="0470b-177">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="0470b-178">Volg deze stappen om een fragment te bewerken.</span><span class="sxs-lookup"><span data-stu-id="0470b-178">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="0470b-179">Selecteer **Fragmenten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="0470b-179">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="0470b-180">Selecteer onder **Fragmenten** het fragment dat u wilt bewerken.</span><span class="sxs-lookup"><span data-stu-id="0470b-180">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="0470b-181">Bewerk waar nodig de module-eigenschappen en de structuur van het fragment.</span><span class="sxs-lookup"><span data-stu-id="0470b-181">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="0470b-182">Het proces lijkt op het proces voor het bewerken van modules in de pagina-editorweergave.</span><span class="sxs-lookup"><span data-stu-id="0470b-182">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="0470b-183">U kunt een fragment ook bewerken door het te selecteren op een pagina, in een sjabloon of in een bovenliggend fragment en vervolgens **Fragment bewerken** te selecteren in het deelvenster Eigenschappen aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="0470b-183">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0470b-184">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0470b-184">Additional resources</span></span>

[<span data-ttu-id="0470b-185">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="0470b-185">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="0470b-186">Werken met sjablonen</span><span class="sxs-lookup"><span data-stu-id="0470b-186">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="0470b-187">Werken met vooraf ingestelde indelingen</span><span class="sxs-lookup"><span data-stu-id="0470b-187">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="0470b-188">Werken met publicatiegroepen</span><span class="sxs-lookup"><span data-stu-id="0470b-188">Work with publish groups</span></span>](publish-groups.md)
