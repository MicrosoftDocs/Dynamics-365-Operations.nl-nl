---
title: Tabbladmodule
description: In dit onderwerp wordt beschreven wat tabbladmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c9d897113442f14b95539efb9fec9482be96447a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411321"
---
# <a name="tab-module"></a><span data-ttu-id="b5de8-103">Tabbladmodule</span><span class="sxs-lookup"><span data-stu-id="b5de8-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5de8-104">In dit onderwerp wordt beschreven wat tabbladmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5de8-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5de8-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="b5de8-105">Overview</span></span>

<span data-ttu-id="b5de8-106">Tabbladmodules zijn containerachtige modules die worden gebruikt om de informatie op een sitepagina in tabbladen te ordenen.</span><span class="sxs-lookup"><span data-stu-id="b5de8-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="b5de8-107">Ze kunnen worden gebruikt op elke pagina waar informatie moet worden weergegeven op tabbladen.</span><span class="sxs-lookup"><span data-stu-id="b5de8-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="b5de8-108">Aan elke tabbladmodule kunt u een of meer modules toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b5de8-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="b5de8-109">Elke tabbladitemmodule vertegenwoordigt één tabblad. In elke tabbladitemmodule kunnen een of meer modules worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b5de8-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="b5de8-110">Er gelden geen beperkingen voor de typen modules die kunnen worden toegevoegd aan een tabbladitemmodule.</span><span class="sxs-lookup"><span data-stu-id="b5de8-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="b5de8-111">De volgende afbeelding toont een voorbeeld van een tabbladmodule op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="b5de8-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="b5de8-112">In dit voorbeeld is het tabblad **Verzending** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b5de8-112">In this example, the **Shipping** tab selected.</span></span>

![Voorbeeld van een tabbladmodule](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="b5de8-114">Eigenschappen van tabbladmodule</span><span class="sxs-lookup"><span data-stu-id="b5de8-114">Tab module properties</span></span>

| <span data-ttu-id="b5de8-115">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="b5de8-115">Property name</span></span> | <span data-ttu-id="b5de8-116">Waarden</span><span class="sxs-lookup"><span data-stu-id="b5de8-116">Values</span></span> | <span data-ttu-id="b5de8-117">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="b5de8-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b5de8-118">Kop</span><span class="sxs-lookup"><span data-stu-id="b5de8-118">Heading</span></span> | <span data-ttu-id="b5de8-119">Tekst</span><span class="sxs-lookup"><span data-stu-id="b5de8-119">Text</span></span> | <span data-ttu-id="b5de8-120">Deze eigenschap geeft een optionele koptekst aan voor de tabbladmodule.</span><span class="sxs-lookup"><span data-stu-id="b5de8-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="b5de8-121">Actieve tabbladindex</span><span class="sxs-lookup"><span data-stu-id="b5de8-121">Active Tab Index</span></span> | <span data-ttu-id="b5de8-122">Nummer</span><span class="sxs-lookup"><span data-stu-id="b5de8-122">Number</span></span> | <span data-ttu-id="b5de8-123">Met deze eigenschap wordt het tabblad aangegeven dat standaard actief moet zijn wanneer een pagina wordt geladen.</span><span class="sxs-lookup"><span data-stu-id="b5de8-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="b5de8-124">Als er geen waarde wordt opgegeven, is het eerste tabbladitem standaard actief.</span><span class="sxs-lookup"><span data-stu-id="b5de8-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="b5de8-125">Eigenschappen van tabbladitemmodule</span><span class="sxs-lookup"><span data-stu-id="b5de8-125">Tab item module properties</span></span>

| <span data-ttu-id="b5de8-126">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="b5de8-126">Property name</span></span> | <span data-ttu-id="b5de8-127">Waarden</span><span class="sxs-lookup"><span data-stu-id="b5de8-127">Values</span></span> | <span data-ttu-id="b5de8-128">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="b5de8-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b5de8-129">Titel</span><span class="sxs-lookup"><span data-stu-id="b5de8-129">Title</span></span> | <span data-ttu-id="b5de8-130">Tekst</span><span class="sxs-lookup"><span data-stu-id="b5de8-130">Text</span></span> | <span data-ttu-id="b5de8-131">Deze eigenschap geeft de titeltekst aan voor de tabbladitemmodule.</span><span class="sxs-lookup"><span data-stu-id="b5de8-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="b5de8-132">Een tabbladmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="b5de8-132">Add a tab module to a page</span></span>

<span data-ttu-id="b5de8-133">Voer de volgende stappen uit om een tabbladmodule aan een nieuwe pagina toe te voegen en de eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="b5de8-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="b5de8-134">Gebruik de sjabloon Fabrikam-marketing (of een sjabloon zonder beperkingen) om een nieuwe pagina te maken met de naam **Pagina met winkelbeleid**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="b5de8-135">Selecteer in het vak **Hoofd** van de **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5de8-136">Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5de8-137">Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5de8-138">Selecteer in het dialoogvenster **Module toevoegen** de **Tabbladmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5de8-139">Selecteer in het eigenschappen venster van de tabbladmodule de optie **Kop** naast het potloodsymbool.</span><span class="sxs-lookup"><span data-stu-id="b5de8-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="b5de8-140">Voer in het dialoogvenster **Kop** onder **Koptekst** een koptekst in (bijvoorbeeld een **Beleid**).</span><span class="sxs-lookup"><span data-stu-id="b5de8-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="b5de8-141">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-141">Then select **OK**.</span></span>
1. <span data-ttu-id="b5de8-142">Selecteer het weglatingsteken (**...**) in het vak **Tabblad** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5de8-143">Selecteer in het dialoogvenster **Module toevoegen** de **Tabbladitemmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5de8-144">Voer in het eigenschappenvenster van de tabbladitemmodule onder **Titel** de titeltekst in (bijvoorbeeld **Levering**).</span><span class="sxs-lookup"><span data-stu-id="b5de8-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="b5de8-145">Selecteer het weglatingsteken (**...**) in het vak **Tabbladitem** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5de8-146">Selecteer in het dialoogvenster **Module toevoegen** de module **Tekstblok** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5de8-147">Voeg in het eigenschappenvenster van de tekstblokmodule een alinea tekst toe onder het veld **RTF**.</span><span class="sxs-lookup"><span data-stu-id="b5de8-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="b5de8-148">Voeg in het vak **Tabblad** nog een paar modules met titels toe.</span><span class="sxs-lookup"><span data-stu-id="b5de8-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="b5de8-149">Voeg in elke tabbladmodule een tekstblokmodule toe die inhoud bevat.</span><span class="sxs-lookup"><span data-stu-id="b5de8-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="b5de8-150">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="b5de8-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="b5de8-151">Op de pagina wordt een tabbladmodule weergegeven die modules met tabbladitems bevat met de inhoud die u hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b5de8-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="b5de8-152">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="b5de8-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5de8-153">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b5de8-153">Additional resources</span></span>

[<span data-ttu-id="b5de8-154">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="b5de8-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b5de8-155">Containermodule</span><span class="sxs-lookup"><span data-stu-id="b5de8-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b5de8-156">Accordeonmodule</span><span class="sxs-lookup"><span data-stu-id="b5de8-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="b5de8-157">Text Block-module</span><span class="sxs-lookup"><span data-stu-id="b5de8-157">Text block module</span></span>](add-content-rich-block.md)
