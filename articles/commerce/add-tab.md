---
title: Tabbladmodule
description: In dit onderwerp wordt beschreven wat tabbladmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c865d5e055e3fadf2dda225b49f13a163974768f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797450"
---
# <a name="tab-module"></a><span data-ttu-id="3182f-103">Tabbladmodule</span><span class="sxs-lookup"><span data-stu-id="3182f-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3182f-104">In dit onderwerp wordt beschreven wat tabbladmodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3182f-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3182f-105">Tabbladmodules zijn containerachtige modules die worden gebruikt om de informatie op een sitepagina in tabbladen te ordenen.</span><span class="sxs-lookup"><span data-stu-id="3182f-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="3182f-106">Ze kunnen worden gebruikt op elke pagina waar informatie moet worden weergegeven op tabbladen.</span><span class="sxs-lookup"><span data-stu-id="3182f-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="3182f-107">Aan elke tabbladmodule kunt u een of meer modules toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3182f-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="3182f-108">Elke tabbladitemmodule vertegenwoordigt één tabblad. In elke tabbladitemmodule kunnen een of meer modules worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3182f-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="3182f-109">Er gelden geen beperkingen voor de typen modules die kunnen worden toegevoegd aan een tabbladitemmodule.</span><span class="sxs-lookup"><span data-stu-id="3182f-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="3182f-110">De volgende afbeelding toont een voorbeeld van een tabbladmodule op een sitepagina.</span><span class="sxs-lookup"><span data-stu-id="3182f-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="3182f-111">In dit voorbeeld is het tabblad **Verzending** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="3182f-111">In this example, the **Shipping** tab selected.</span></span>

![Voorbeeld van een tabbladmodule](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="3182f-113">Eigenschappen van tabbladmodule</span><span class="sxs-lookup"><span data-stu-id="3182f-113">Tab module properties</span></span>

| <span data-ttu-id="3182f-114">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="3182f-114">Property name</span></span> | <span data-ttu-id="3182f-115">Waarden</span><span class="sxs-lookup"><span data-stu-id="3182f-115">Values</span></span> | <span data-ttu-id="3182f-116">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="3182f-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="3182f-117">Kop</span><span class="sxs-lookup"><span data-stu-id="3182f-117">Heading</span></span> | <span data-ttu-id="3182f-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="3182f-118">Text</span></span> | <span data-ttu-id="3182f-119">Deze eigenschap geeft een optionele koptekst aan voor de tabbladmodule.</span><span class="sxs-lookup"><span data-stu-id="3182f-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="3182f-120">Actieve tabbladindex</span><span class="sxs-lookup"><span data-stu-id="3182f-120">Active Tab Index</span></span> | <span data-ttu-id="3182f-121">Nummer</span><span class="sxs-lookup"><span data-stu-id="3182f-121">Number</span></span> | <span data-ttu-id="3182f-122">Met deze eigenschap wordt het tabblad aangegeven dat standaard actief moet zijn wanneer een pagina wordt geladen.</span><span class="sxs-lookup"><span data-stu-id="3182f-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="3182f-123">Als er geen waarde wordt opgegeven, is het eerste tabbladitem standaard actief.</span><span class="sxs-lookup"><span data-stu-id="3182f-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="3182f-124">Eigenschappen van tabbladitemmodule</span><span class="sxs-lookup"><span data-stu-id="3182f-124">Tab item module properties</span></span>

| <span data-ttu-id="3182f-125">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="3182f-125">Property name</span></span> | <span data-ttu-id="3182f-126">Waarden</span><span class="sxs-lookup"><span data-stu-id="3182f-126">Values</span></span> | <span data-ttu-id="3182f-127">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="3182f-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="3182f-128">Titel</span><span class="sxs-lookup"><span data-stu-id="3182f-128">Title</span></span> | <span data-ttu-id="3182f-129">Tekst</span><span class="sxs-lookup"><span data-stu-id="3182f-129">Text</span></span> | <span data-ttu-id="3182f-130">Deze eigenschap geeft de titeltekst aan voor de tabbladitemmodule.</span><span class="sxs-lookup"><span data-stu-id="3182f-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="3182f-131">Een tabbladmodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="3182f-131">Add a tab module to a page</span></span>

<span data-ttu-id="3182f-132">Voer de volgende stappen uit om een tabbladmodule aan een nieuwe pagina toe te voegen en de eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="3182f-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="3182f-133">Gebruik de sjabloon Fabrikam-marketing (of een sjabloon zonder beperkingen) om een nieuwe pagina te maken met de naam **Pagina met winkelbeleid**.</span><span class="sxs-lookup"><span data-stu-id="3182f-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="3182f-134">Selecteer in het vak **Hoofd** van de **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3182f-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3182f-135">Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3182f-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3182f-136">Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3182f-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3182f-137">Selecteer in het dialoogvenster **Module toevoegen** de **Tabbladmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3182f-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3182f-138">Selecteer in het eigenschappen venster van de tabbladmodule de optie **Kop** naast het potloodsymbool.</span><span class="sxs-lookup"><span data-stu-id="3182f-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="3182f-139">Voer in het dialoogvenster **Kop** onder **Koptekst** een koptekst in (bijvoorbeeld een **Beleid**).</span><span class="sxs-lookup"><span data-stu-id="3182f-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="3182f-140">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3182f-140">Then select **OK**.</span></span>
1. <span data-ttu-id="3182f-141">Selecteer het weglatingsteken (**...**) in het vak **Tabblad** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3182f-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3182f-142">Selecteer in het dialoogvenster **Module toevoegen** de **Tabbladitemmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3182f-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3182f-143">Voer in het eigenschappenvenster van de tabbladitemmodule onder **Titel** de titeltekst in (bijvoorbeeld **Levering**).</span><span class="sxs-lookup"><span data-stu-id="3182f-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="3182f-144">Selecteer het weglatingsteken (**...**) in het vak **Tabbladitem** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="3182f-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3182f-145">Selecteer in het dialoogvenster **Module toevoegen** de module **Tekstblok** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3182f-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3182f-146">Voeg in het eigenschappenvenster van de tekstblokmodule een alinea tekst toe onder het veld **RTF**.</span><span class="sxs-lookup"><span data-stu-id="3182f-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="3182f-147">Voeg in het vak **Tabblad** nog een paar modules met titels toe.</span><span class="sxs-lookup"><span data-stu-id="3182f-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="3182f-148">Voeg in elke tabbladmodule een tekstblokmodule toe die inhoud bevat.</span><span class="sxs-lookup"><span data-stu-id="3182f-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="3182f-149">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="3182f-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="3182f-150">Op de pagina wordt een tabbladmodule weergegeven die modules met tabbladitems bevat met de inhoud die u hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="3182f-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="3182f-151">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="3182f-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3182f-152">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="3182f-152">Additional resources</span></span>

[<span data-ttu-id="3182f-153">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="3182f-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3182f-154">Containermodule</span><span class="sxs-lookup"><span data-stu-id="3182f-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3182f-155">Accordeonmodule</span><span class="sxs-lookup"><span data-stu-id="3182f-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="3182f-156">Text Block-module</span><span class="sxs-lookup"><span data-stu-id="3182f-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]