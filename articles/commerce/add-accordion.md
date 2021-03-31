---
title: Accordeonmodule
description: In dit onderwerp worden accordeonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: a08441f5dffa9c2c65b304d0265dd107a838a685
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206602"
---
# <a name="accordion-module"></a><span data-ttu-id="34b47-103">Accordeonmodule</span><span class="sxs-lookup"><span data-stu-id="34b47-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="34b47-104">In dit onderwerp worden accordeonmodules voor functies beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="34b47-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="34b47-105">Accordeonmodules zijn containerachtige modules die worden gebruikt om de informatie of modules op een pagina te ordenen door een samenvouwbare lade te bieden.</span><span class="sxs-lookup"><span data-stu-id="34b47-105">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="34b47-106">Op elke pagina kan een accordeonmodule worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="34b47-106">An accordion module can be used on any page.</span></span>

<span data-ttu-id="34b47-107">Aan elke accordeonmodule kunt u een of meer accordeonitemmodules toevoegen.</span><span class="sxs-lookup"><span data-stu-id="34b47-107">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="34b47-108">Elke accordeonitemmodule vertegenwoordigt een samenvouwbare lade.</span><span class="sxs-lookup"><span data-stu-id="34b47-108">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="34b47-109">Aan elke accordeonitemmodule kunt u een of meer modules toevoegen.</span><span class="sxs-lookup"><span data-stu-id="34b47-109">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="34b47-110">Er gelden geen beperkingen voor de typen modules die kunnen worden toegevoegd aan een accordeonitemmodule.</span><span class="sxs-lookup"><span data-stu-id="34b47-110">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="34b47-111">De volgende afbeelding toont een voorbeeld van een accordeonmodule die wordt gebruikt om informatie op de pagina met veelgestelde vragen van een winkel te ordenen.</span><span class="sxs-lookup"><span data-stu-id="34b47-111">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Voorbeeld van een accordeonmodule](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="34b47-113">Eigenschappen van accordeonmodule</span><span class="sxs-lookup"><span data-stu-id="34b47-113">Accordion module properties</span></span>

| <span data-ttu-id="34b47-114">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="34b47-114">Property name</span></span> | <span data-ttu-id="34b47-115">Waarden</span><span class="sxs-lookup"><span data-stu-id="34b47-115">Values</span></span> | <span data-ttu-id="34b47-116">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="34b47-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="34b47-117">Kop</span><span class="sxs-lookup"><span data-stu-id="34b47-117">Heading</span></span> | <span data-ttu-id="34b47-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="34b47-118">Text</span></span> | <span data-ttu-id="34b47-119">Deze eigenschap geeft een optionele koptekst aan voor de accordeonmodule.</span><span class="sxs-lookup"><span data-stu-id="34b47-119">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="34b47-120">Alles uitvouwen</span><span class="sxs-lookup"><span data-stu-id="34b47-120">Expand All</span></span> | <span data-ttu-id="34b47-121">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="34b47-121">**True** or **False**</span></span> | <span data-ttu-id="34b47-122">Als de waarde is ingesteld op **Waar**, wordt de functie voor het uit- en samenvouwen ingeschakeld zodat alle items in de accordeonmodule kunnen worden uitgevouwen en samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="34b47-122">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="34b47-123">Stijl van interactie</span><span class="sxs-lookup"><span data-stu-id="34b47-123">Interaction Style</span></span> | <span data-ttu-id="34b47-124">**Onafhankelijk** of **Alleen één item uitvouwen**</span><span class="sxs-lookup"><span data-stu-id="34b47-124">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="34b47-125">Deze eigenschap bepaalt de stijl van de interactie voor accordeonitems.</span><span class="sxs-lookup"><span data-stu-id="34b47-125">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="34b47-126">Als de waarde op **Onafhankelijk** wordt ingesteld, kan elk accordeonitem onafhankelijk worden uitgevouwen of samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="34b47-126">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="34b47-127">Als de waarde wordt ingesteld op **Alleen één item uitvouwen**, kan slechts één item tegelijk worden uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="34b47-127">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="34b47-128">Wanneer items worden uitgevouwen, worden eerder uitgevouwen items samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="34b47-128">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="34b47-129">Eigenschappen van accordeonitemmodule</span><span class="sxs-lookup"><span data-stu-id="34b47-129">Accordion item module properties</span></span>

| <span data-ttu-id="34b47-130">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="34b47-130">Property name</span></span> | <span data-ttu-id="34b47-131">Waarden</span><span class="sxs-lookup"><span data-stu-id="34b47-131">Values</span></span> | <span data-ttu-id="34b47-132">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="34b47-132">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="34b47-133">Titel</span><span class="sxs-lookup"><span data-stu-id="34b47-133">Title</span></span> | <span data-ttu-id="34b47-134">Tekst</span><span class="sxs-lookup"><span data-stu-id="34b47-134">Text</span></span> | <span data-ttu-id="34b47-135">Deze eigenschap geeft de titeltekst aan voor de accordeonitemmodule.</span><span class="sxs-lookup"><span data-stu-id="34b47-135">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="34b47-136">Als u de titelregio selecteert, kunnen gebruikers de sectie uitvouwen of samenvouwen.</span><span class="sxs-lookup"><span data-stu-id="34b47-136">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="34b47-137">Standaard uitvouwen</span><span class="sxs-lookup"><span data-stu-id="34b47-137">Expand by default</span></span> | <span data-ttu-id="34b47-138">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="34b47-138">**True** or **False**</span></span> | <span data-ttu-id="34b47-139">Als de waarde is ingesteld op **Waar**, wordt het accordeonitem standaard uitgevouwen wanneer de pagina wordt geladen.</span><span class="sxs-lookup"><span data-stu-id="34b47-139">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="34b47-140">Een accordeonmodule toevoegen aan een pagina met veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="34b47-140">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="34b47-141">Voer de volgende stappen uit om een accordeonmodule aan een pagina met veelgestelde vragen toe te voegen en de eigenschappen in te stellen in Site builder.</span><span class="sxs-lookup"><span data-stu-id="34b47-141">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="34b47-142">Ga naar **Pagina's** en gebruik de sjabloon Fabrikam-marketing (of een sjabloon zonder beperkingen) om een nieuwe pagina te maken met de naam **Veelgestelde vragen over winkel**.</span><span class="sxs-lookup"><span data-stu-id="34b47-142">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="34b47-143">Selecteer in het vak **Hoofd** van de **Standaardpagina** het weglatingsteken (**...**) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="34b47-143">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="34b47-144">Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b47-144">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="34b47-145">Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="34b47-145">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="34b47-146">Selecteer in het dialoogvenster **Module toevoegen** de **Accordeonmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b47-146">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="34b47-147">Selecteer in het eigenschappen venster van de accordeonmodule de optie **Kop** naast het potloodsymbool.</span><span class="sxs-lookup"><span data-stu-id="34b47-147">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="34b47-148">Voer in het dialoogvenster **Kop** onder **Koptekst** **Veelgestelde vragen** in.</span><span class="sxs-lookup"><span data-stu-id="34b47-148">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="34b47-149">Selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b47-149">Then select **OK**.</span></span>
1. <span data-ttu-id="34b47-150">Schakel in het eigenschappenvenster van de accordeonmodule het selectievakje **Alles uitvouwen weergeven** in en selecteer vervolgens in het veld **Stijl van interactie** de optie **Onafhankelijk**.</span><span class="sxs-lookup"><span data-stu-id="34b47-150">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="34b47-151">Selecteer het weglatingsteken (**...**) in het vak **Accordeon** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="34b47-151">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="34b47-152">Selecteer in het dialoogvenster **Module toevoegen** de **Accordeonitemmodule** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b47-152">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="34b47-153">Voer in het eigenschappenvenster van de accordeonitemmodule onder **Titel** de titeltekst in (bijvoorbeeld **Hoe werkt retourneren?**).</span><span class="sxs-lookup"><span data-stu-id="34b47-153">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="34b47-154">Selecteer het weglatingsteken (**...**) in het vak **Accordeonitem** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="34b47-154">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="34b47-155">Selecteer in het dialoogvenster **Module toevoegen** de module **Tekstblok** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="34b47-155">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="34b47-156">Voer in het eigenschappenvenster van de tekstblokmodule een alinea tekst in (bijvoorbeeld **Retouren worden verwerkt via het callcenter. Neem contact op met 1-800-FABRIKAM voor retouren. Producten hebben een teruggavebeleid van 30 dagen. Retouren moeten worden gestart binnen deze tijdsperiode.**).</span><span class="sxs-lookup"><span data-stu-id="34b47-156">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="34b47-157">Voeg in het vak **Accordeon** nog een paar accordeonitemmodules toe.</span><span class="sxs-lookup"><span data-stu-id="34b47-157">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="34b47-158">Voeg in elke accordeonitemmodule een tekstblokmodule toe die inhoud bevat.</span><span class="sxs-lookup"><span data-stu-id="34b47-158">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="34b47-159">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="34b47-159">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="34b47-160">Op de pagina wordt een accordeonmodule weergegeven die de inhoud bevat die u hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="34b47-160">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="34b47-161">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="34b47-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34b47-162">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="34b47-162">Additional resources</span></span>

[<span data-ttu-id="34b47-163">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="34b47-163">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="34b47-164">Containermodule</span><span class="sxs-lookup"><span data-stu-id="34b47-164">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="34b47-165">Tabbladmodule</span><span class="sxs-lookup"><span data-stu-id="34b47-165">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="34b47-166">Text Block-module</span><span class="sxs-lookup"><span data-stu-id="34b47-166">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]