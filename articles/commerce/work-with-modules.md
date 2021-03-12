---
title: Werken met modules
description: In dit onderwerp wordt beschreven hoe en wanneer u modules in Microsoft Dynamics 365 Commerce gebruikt.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 89d95814e892e3afcb6514ab0d0219f7b08b9c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000454"
---
# <a name="work-with-modules"></a><span data-ttu-id="d683b-103">Werken met modules</span><span class="sxs-lookup"><span data-stu-id="d683b-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d683b-104">In dit onderwerp wordt beschreven hoe en wanneer u modules in Microsoft Dynamics 365 Commerce gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d683b-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d683b-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="d683b-105">Overview</span></span>

<span data-ttu-id="d683b-106">Modules zijn logische bouwstenen die de paginastructuur vormen en verschillende doeleinden en bereiken hebben.</span><span class="sxs-lookup"><span data-stu-id="d683b-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="d683b-107">Sommige modules zijn containers op een hoog niveau en zijn alleen bedoeld voor het vasthouden en organiseren van andere modules (onderliggende modules).</span><span class="sxs-lookup"><span data-stu-id="d683b-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="d683b-108">Andere modules, zoals een eenvoudige afbeeldingsmodule, hebben een specifiek doel.</span><span class="sxs-lookup"><span data-stu-id="d683b-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="d683b-109">Modules, zoals carrouselmodules, vallen ergens tussen deze twee categorieën.</span><span class="sxs-lookup"><span data-stu-id="d683b-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="d683b-110">Standaard bevat uw Dynamics 365 Commerce-site een bibliotheekmodule waarmee u de meeste elementaire e-commerce-scenario's kunt realiseren.</span><span class="sxs-lookup"><span data-stu-id="d683b-110">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="d683b-111">U kunt een complete e-commerce-site samenstellen met behulp van deze modules.</span><span class="sxs-lookup"><span data-stu-id="d683b-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="d683b-112">U kunt deze modules echter ook aanpassen of nieuwe aangepaste modules maken voor specifieke behoeften.</span><span class="sxs-lookup"><span data-stu-id="d683b-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="d683b-113">Als u aangepaste modules wilt maken, is er een module-ontwerp-SDK (Software Development Kit) beschikbaar om u te helpen bij het maken van een aangepaste modulebibliotheek.</span><span class="sxs-lookup"><span data-stu-id="d683b-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="d683b-114">Containermodules en vakken</span><span class="sxs-lookup"><span data-stu-id="d683b-114">Container modules and slots</span></span>

<span data-ttu-id="d683b-115">Zoals eerder is vermeld, bevatten sommige modules onderliggende modules.</span><span class="sxs-lookup"><span data-stu-id="d683b-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="d683b-116">Deze modules worden *containers* genoemd en kunnen hiërarchieën van geneste modules bevatten.</span><span class="sxs-lookup"><span data-stu-id="d683b-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="d683b-117">Containermodules bevatten *vakken*.</span><span class="sxs-lookup"><span data-stu-id="d683b-117">Container modules include *slots*.</span></span> <span data-ttu-id="d683b-118">Vakken worden gebruikt om de indeling en het doel van onderliggende modules in de container te verwerken.</span><span class="sxs-lookup"><span data-stu-id="d683b-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="d683b-119">Een voorbeeld is een containermodule voor een basispagina (een module op het hoogste niveau voor een willekeurige pagina) waarin verschillende belangrijke vakken worden gedefinieerd:</span><span class="sxs-lookup"><span data-stu-id="d683b-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="d683b-120">Een koptekstvak</span><span class="sxs-lookup"><span data-stu-id="d683b-120">A header slot</span></span>
- <span data-ttu-id="d683b-121">Een subkoptekstvak</span><span class="sxs-lookup"><span data-stu-id="d683b-121">A sub-header slot</span></span>
- <span data-ttu-id="d683b-122">Een hoofdvak</span><span class="sxs-lookup"><span data-stu-id="d683b-122">A main slot</span></span>
- <span data-ttu-id="d683b-123">Een voettekstvak</span><span class="sxs-lookup"><span data-stu-id="d683b-123">A footer slot</span></span>
- <span data-ttu-id="d683b-124">Een subvoettekstvak</span><span class="sxs-lookup"><span data-stu-id="d683b-124">A sub-footer slot</span></span>

<span data-ttu-id="d683b-125">De ontwikkelaar van de module definieert deze vakken en bepaalt welke onderliggende modules en hoeveel onderliggende modules direct in de module kunnen worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="d683b-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="d683b-126">Het koptekstvak kan bijvoorbeeld slechts één module van het type **koptekstmodule** ondersteunen, terwijl het vak voor de hoofdtekst een onbeperkt aantal modules van elk type kan ondersteunen (behalve andere containermodules).</span><span class="sxs-lookup"><span data-stu-id="d683b-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="d683b-127">In de ontwerphulpmiddelen hoeven de auteurs van de pagina niet van tevoren te weten welke modules in elk vak kunnen worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="d683b-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="d683b-128">Wanneer de auteur van een pagina een vak selecteert en een module wil selecteren om hieraan toe te voegen, wordt een gefilterde weergave van de moduletypen getoond die voor die sleuf worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="d683b-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="d683b-129">Inhoudsmodules</span><span class="sxs-lookup"><span data-stu-id="d683b-129">Content modules</span></span>

<span data-ttu-id="d683b-130">Inhoudsmodules bevatten inhoud en media-elementen, zoals tekst (bijvoorbeeld koppen, alinea's en koppelingen) of activaverwijzingen (bijvoorbeeld afbeeldingen, video en PDF's).</span><span class="sxs-lookup"><span data-stu-id="d683b-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="d683b-131">Standaardinhoudsmoduletypen zijn onder andere modules voor informatieblokken, tekstblokken en speciale acties.</span><span class="sxs-lookup"><span data-stu-id="d683b-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="d683b-132">Modules van deze drie typen kunnen tekst of media bevatten, en vereisen geen onderliggende modules om iets zichtbaar te maken op een pagina.</span><span class="sxs-lookup"><span data-stu-id="d683b-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="d683b-133">Bij de meeste standaard dagelijkse activiteiten voor pagina's en inhoud zijn inhoudsmodules betrokken, voornamelijk omdat deze modules de feitelijke inhoud definiëren die wordt weergegeven in de bovenliggende containermodules.</span><span class="sxs-lookup"><span data-stu-id="d683b-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="d683b-134">Er zijn veel inhoudsmodules beschikbaar die doorgaans de laatste onderdelen zijn die u aan de hiërarchie van geneste modules van de pagina toevoegt.</span><span class="sxs-lookup"><span data-stu-id="d683b-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="d683b-135">In de volgende afbeelding wordt aangegeven hoe modules worden genest binnen bovenliggende containermodulevakken.</span><span class="sxs-lookup"><span data-stu-id="d683b-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Modules nesten](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="d683b-137">Modules toevoegen of verwijderen</span><span class="sxs-lookup"><span data-stu-id="d683b-137">Add or remove modules</span></span>

<span data-ttu-id="d683b-138">In de volgende procedures wordt beschreven hoe u modules toevoegt en verwijdert.</span><span class="sxs-lookup"><span data-stu-id="d683b-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="d683b-139">Een module toevoegen</span><span class="sxs-lookup"><span data-stu-id="d683b-139">Add a module</span></span>

<span data-ttu-id="d683b-140">Voer deze stappen uit om een vak of een container aan een pagina toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="d683b-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="d683b-141">Selecteer in het overzichtsvenster links of rechtstreeks op het hoofdtekenpapier een container of vak waaraan een onderliggende module kan worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d683b-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d683b-142">De moduleontwerper definieert de lijst met moduletypen die aan een bepaald modulevak kunnen worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d683b-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="d683b-143">Sjabloonschrijvers kunnen de toegestane moduleopties vervolgens verfijnen om een consistente SEO-werking (Search Engine Optimization) te garanderen en een efficiënt ontwerp voor alle pagina's die op basis van een bepaalde sjabloon worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d683b-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="d683b-144">Wanneer een module aan een vak wordt toegevoegd, wordt het dialoogvenster **Module toevoegen** automatisch gefilterd, zodat alleen modules worden weergegeven die in de geselecteerde container of het geselecteerde vak worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="d683b-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="d683b-145">De lijst met toegestane modules wordt bepaald door de sjabloon van de pagina of door de moduledefinitie van de container.</span><span class="sxs-lookup"><span data-stu-id="d683b-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="d683b-146">Als u het overzichtsvenster gebruikt, selecteert u het weglatingsteken (**...**) naast de modulenaam en selecteert u **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d683b-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="d683b-147">Als u de besturingselementen direct binnen het tekenpapier gebruikt, selecteert u het plussymbool (**+**) in een leeg vak of naast de huidige geselecteerde module en selecteert u vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d683b-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d683b-148">Als nieuwe onderliggende modules niet door een container of vak worden ondersteund, is de optie **Module toevoegen** niet beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="d683b-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="d683b-149">Selecteer in het dialoogvenster **Module toevoegen** een module die u aan de pagina wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d683b-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="d683b-150">**Inhoudsblok** is een goed type module waarmee beginners kunnen werken.</span><span class="sxs-lookup"><span data-stu-id="d683b-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="d683b-151">Klik op **OK** om de geselecteerde module toe te voegen aan de geselecteerde container of het vak op de pagina.</span><span class="sxs-lookup"><span data-stu-id="d683b-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="d683b-152">Een module verwijderen</span><span class="sxs-lookup"><span data-stu-id="d683b-152">Remove a module</span></span>

<span data-ttu-id="d683b-153">Voer deze stappen uit om een module uit een vak of een container op een pagina te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d683b-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="d683b-154">Selecteer in het overzichtsvenster aan de linkerkant het weglatingsteken (**...**) naast de naam van de module die u wilt verwijderen en selecteer vervolgens de knop Prullenbak.</span><span class="sxs-lookup"><span data-stu-id="d683b-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="d683b-155">U kunt ook op het hoofdtekenpapier de prullenbak selecteren op de werkbalk van een geselecteerde module.</span><span class="sxs-lookup"><span data-stu-id="d683b-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="d683b-156">Wanneer u wordt gevraagd te bevestigen dat u de module wilt verwijderen, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="d683b-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="d683b-157">Een module naar een nieuwe positie verplaatsen</span><span class="sxs-lookup"><span data-stu-id="d683b-157">Move a module to a new position</span></span>

<span data-ttu-id="d683b-158">Gebruik een van de volgende methoden om een module naar een nieuwe positie binnen uw pagina te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="d683b-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="d683b-159">Een module verplaatsen met behulp van het overzichtsvenster</span><span class="sxs-lookup"><span data-stu-id="d683b-159">Move a module using the outline pane</span></span>

<span data-ttu-id="d683b-160">Voer de volgende stappen uit om een module te verplaatsen met behulp van het overzichtsvenster.</span><span class="sxs-lookup"><span data-stu-id="d683b-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="d683b-161">Selecteer en houd de module die u wilt verplaatsen vast in het overzichtsvenster en sleep de module naar een nieuwe positie in het overzicht.</span><span class="sxs-lookup"><span data-stu-id="d683b-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="d683b-162">De blauwe regel in het overzicht en op het tekenpapier geeft aan waar de module kan worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="d683b-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="d683b-163">Laat de module los om deze op de nieuwe positie neer te zetten.</span><span class="sxs-lookup"><span data-stu-id="d683b-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="d683b-164">Een module rechtstreeks binnen het tekenpapier verplaatsen</span><span class="sxs-lookup"><span data-stu-id="d683b-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="d683b-165">Voer de volgende stappen uit om een module rechtstreeks binnen het tekenpapier te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="d683b-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="d683b-166">Selecteer de module die u wilt verplaatsen in het tekenpapier.</span><span class="sxs-lookup"><span data-stu-id="d683b-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="d683b-167">Selecteer een pijl symbool omhoog of omlaag op de werkbalk van de module en sleep vervolgens de pijl naar een nieuwe positie op de pagina.</span><span class="sxs-lookup"><span data-stu-id="d683b-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="d683b-168">De blauwe regel in het tekenpapier en overzicht geeft aan waar de module kan worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="d683b-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="d683b-169">Als een module niet omhoog of omlaag kan worden verplaatst, wordt het pijl symbool grijs weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d683b-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="d683b-170">Laat de module los om deze op de nieuwe positie neer te zetten.</span><span class="sxs-lookup"><span data-stu-id="d683b-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="d683b-171">Een module verplaatsen met behulp van het menu met het weglatingsteken</span><span class="sxs-lookup"><span data-stu-id="d683b-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="d683b-172">Voer de volgende stappen uit om een module te verplaatsen met behulp van het menu met het weglatingsteken.</span><span class="sxs-lookup"><span data-stu-id="d683b-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="d683b-173">Selecteer een module in het overzicht of op het tekenpapier.</span><span class="sxs-lookup"><span data-stu-id="d683b-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="d683b-174">Selecteer het weglatingsteken (**...**) naast de naam van de module in het overzichtsvenster of op de werkbalk van de module op het tekenpapier.</span><span class="sxs-lookup"><span data-stu-id="d683b-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="d683b-175">Als de module in de container of het vak omhoog of omlaag kan worden verplaatst, ziet u opties voor **Omhoog verplaatsen** of **Omlaag verplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="d683b-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="d683b-176">Selecteer de gewenste optie voor verplaatsen om de module omhoog of omlaag te verplaatsen ten opzichte van de items op hetzelfde niveau.</span><span class="sxs-lookup"><span data-stu-id="d683b-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="d683b-177">Modules configureren</span><span class="sxs-lookup"><span data-stu-id="d683b-177">Configure modules</span></span>

<span data-ttu-id="d683b-178">In de volgende procedures wordt beschreven hoe u inhouds- en containermodules configureert.</span><span class="sxs-lookup"><span data-stu-id="d683b-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="d683b-179">Een inhoudsmodule configureren</span><span class="sxs-lookup"><span data-stu-id="d683b-179">Configure a content module</span></span>

<span data-ttu-id="d683b-180">Voer de volgende stappen uit om een inhoudsmodule op een pagina te configureren.</span><span class="sxs-lookup"><span data-stu-id="d683b-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="d683b-181">Vouw in het overzichtsvenster aan de linkerkant de boomstructuur uit en selecteer een inhoudsmodule (bijvoorbeeld **Inhoudsblok**).</span><span class="sxs-lookup"><span data-stu-id="d683b-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="d683b-182">Of selecteer de module die u wilt verplaatsen op het hoofdtekenpapier.</span><span class="sxs-lookup"><span data-stu-id="d683b-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="d683b-183">Voer in het deelvenster met module-eigenschappen rechts eigenschappen in voor de gewenste modulebesturingselementen.</span><span class="sxs-lookup"><span data-stu-id="d683b-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="d683b-184">Selecteer **Opslaan** op de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="d683b-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="d683b-185">Hierdoor wordt ook het canvas met de voorbeeldweergave vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="d683b-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="d683b-186">Eigenschappen van moduletekst bewerken</span><span class="sxs-lookup"><span data-stu-id="d683b-186">Edit module text properties</span></span>

<span data-ttu-id="d683b-187">Moduleteksteigenschappen die niet alleen-lezen zijn, kunnen rechtstreeks op het tekenpapier worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="d683b-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="d683b-188">Voer de volgende stappen uit om de moduleteksteigenschappen te bewerken.</span><span class="sxs-lookup"><span data-stu-id="d683b-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="d683b-189">Selecteer het tekstbesturingselement op het tekenpapier en plaats vervolgens de cursor op de plaats waar u tekst wilt bewerken.</span><span class="sxs-lookup"><span data-stu-id="d683b-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="d683b-190">Voer uw tekstinhoud in.</span><span class="sxs-lookup"><span data-stu-id="d683b-190">Enter your text content.</span></span>
1. <span data-ttu-id="d683b-191">Selecteer ergens buiten de tekst inhoud om verder te gaan met het bewerken van andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="d683b-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="d683b-192">Inline afbeeldingen selecteren</span><span class="sxs-lookup"><span data-stu-id="d683b-192">Inline image selection</span></span>

<span data-ttu-id="d683b-193">Moduleafbeeldingen die niet alleen-lezen zijn, kunnen rechtstreeks vanaf het tekenpapier worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="d683b-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="d683b-194">Voer de volgende stappen uit om een nieuwe afbeelding te selecteren voor een inhoudsmodule.</span><span class="sxs-lookup"><span data-stu-id="d683b-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="d683b-195">Dubbelklik op het tekenpapier op de afbeelding.</span><span class="sxs-lookup"><span data-stu-id="d683b-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="d683b-196">Hiermee wordt het venster mediakiezer weergeven.</span><span class="sxs-lookup"><span data-stu-id="d683b-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="d683b-197">Zoek en selecteer een nieuwe afbeelding die u wilt gebruiken en klik vervolgens op **OK**.</span><span class="sxs-lookup"><span data-stu-id="d683b-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="d683b-198">De nieuwe afbeelding wordt nu op het tekenpapier weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d683b-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="d683b-199">Een containermodule configureren</span><span class="sxs-lookup"><span data-stu-id="d683b-199">Configure a container module</span></span>

<span data-ttu-id="d683b-200">Voer de volgende stappen uit om een containermodule op een pagina te configureren.</span><span class="sxs-lookup"><span data-stu-id="d683b-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="d683b-201">Selecteer een containermodule op de pagina (bijvoorbeeld een carrousel of een vloeibare containermodule).</span><span class="sxs-lookup"><span data-stu-id="d683b-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="d683b-202">Vouw in het deelvenster Eigenschappen rechts de geneste besturingselementen uit door de kopteksten te selecteren en stel de vereiste waarden voor besturingselementen in.</span><span class="sxs-lookup"><span data-stu-id="d683b-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="d683b-203">Selecteer in het overzichtsvenster aan de linkerkant de knop met het weglatingsteken naast de naam van de containermodule of van vakken in de container, en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="d683b-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="d683b-204">Voeg vervolgens onderliggende modules toe aan de geselecteerde container.</span><span class="sxs-lookup"><span data-stu-id="d683b-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="d683b-205">Zie de sectie [Werken met modules](#add-a-module) eerder in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d683b-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="d683b-206">Als er meerdere onderliggende modules op hetzelfde niveau zijn in een bovenliggende container, kunt u de weergavevolgorde in de bovenliggende container wijzigen.</span><span class="sxs-lookup"><span data-stu-id="d683b-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="d683b-207">Selecteer de knop met het weglatingsteken voor een module en gebruik vervolgens de knoppen pijl-omhoog en pijl-omlaag.</span><span class="sxs-lookup"><span data-stu-id="d683b-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d683b-208">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d683b-208">Additional resources</span></span>

[<span data-ttu-id="d683b-209">Overzicht sjablonen en indelingen</span><span class="sxs-lookup"><span data-stu-id="d683b-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="d683b-210">Werken met sjablonen</span><span class="sxs-lookup"><span data-stu-id="d683b-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="d683b-211">Werken met vooraf ingestelde indelingen</span><span class="sxs-lookup"><span data-stu-id="d683b-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="d683b-212">Werken met fragmenten</span><span class="sxs-lookup"><span data-stu-id="d683b-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="d683b-213">Een containermodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="d683b-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="d683b-214">Werken met groepen publiceren</span><span class="sxs-lookup"><span data-stu-id="d683b-214">Work with publish groups</span></span>](publish-groups.md)

