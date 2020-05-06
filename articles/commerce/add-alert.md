---
title: Promospandoekmodule
description: In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269769"
---
# <a name="promo-banner-module"></a><span data-ttu-id="6f33e-103">Promospandoekmodule</span><span class="sxs-lookup"><span data-stu-id="6f33e-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6f33e-104">In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6f33e-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6f33e-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="6f33e-105">Overview</span></span>

<span data-ttu-id="6f33e-106">Promobannermodules worden gebruikt om inline informatie op een pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6f33e-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="6f33e-107">Ze kunnen worden gebruikt om promoties op alle pagina's van een e-commerce-site weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6f33e-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="6f33e-108">Promobannermodules ondersteunen een tekstbericht en een koppeling.</span><span class="sxs-lookup"><span data-stu-id="6f33e-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="6f33e-109">Als er meerdere berichten aan een promobannermodule worden toegevoegd, verandert deze in een draaiende carrouselbanner waarmee klanten door alle berichten kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="6f33e-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="6f33e-110">Promobannermodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="6f33e-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="6f33e-111">Gebruiksvoorbeelden van promotiebanners in e-Commerce</span><span class="sxs-lookup"><span data-stu-id="6f33e-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="6f33e-112">Promobanners kunnen in de koptekst van een site worden gebruikt om promoties of berichten voor de hele site weer te geven, zoals in de volgende voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="6f33e-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="6f33e-113">"Jaarlijkse uitverkoop eindigt over 10 dagen"</span><span class="sxs-lookup"><span data-stu-id="6f33e-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="6f33e-114">"Grote besparingen bij terug naar school.</span><span class="sxs-lookup"><span data-stu-id="6f33e-114">"Save big with back to school sale.</span></span> <span data-ttu-id="6f33e-115">Winkel nu."</span><span class="sxs-lookup"><span data-stu-id="6f33e-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="6f33e-116">Eigenschappen van promobannermodules</span><span class="sxs-lookup"><span data-stu-id="6f33e-116">Promo banner module properties</span></span>

| <span data-ttu-id="6f33e-117">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="6f33e-117">Property name</span></span>             | <span data-ttu-id="6f33e-118">Value</span><span class="sxs-lookup"><span data-stu-id="6f33e-118">Value</span></span>                              | <span data-ttu-id="6f33e-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6f33e-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="6f33e-120">Bannerberichten</span><span class="sxs-lookup"><span data-stu-id="6f33e-120">Banner messages</span></span>           | <span data-ttu-id="6f33e-121">Tekst en koppelingen</span><span class="sxs-lookup"><span data-stu-id="6f33e-121">Text and links</span></span>                     | <span data-ttu-id="6f33e-122">Een matrix met tekst en koppelingen.</span><span class="sxs-lookup"><span data-stu-id="6f33e-122">An array of text and links.</span></span> |
| <span data-ttu-id="6f33e-123">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="6f33e-123">Autoplay</span></span>                  | <span data-ttu-id="6f33e-124">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="6f33e-124">**True** or **False**</span></span>              | <span data-ttu-id="6f33e-125">Een waarde die aangeeft of berichten automatisch worden doorlopen als er meerdere berichten zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="6f33e-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="6f33e-126">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="6f33e-126">Slide transition interval</span></span> | <span data-ttu-id="6f33e-127">Een aantal milliseconden (ms)</span><span class="sxs-lookup"><span data-stu-id="6f33e-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="6f33e-128">Het interval voor het doorlopen van berichten.</span><span class="sxs-lookup"><span data-stu-id="6f33e-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="6f33e-129">Negeren toestaan</span><span class="sxs-lookup"><span data-stu-id="6f33e-129">Allow dismiss</span></span>             | <span data-ttu-id="6f33e-130">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="6f33e-130">**True** or **False**</span></span>              | <span data-ttu-id="6f33e-131">Als de waarde is ingesteld op **True**, kunnen klanten de waarschuwing sluiten.</span><span class="sxs-lookup"><span data-stu-id="6f33e-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="6f33e-132">Carrouselflipper weergeven</span><span class="sxs-lookup"><span data-stu-id="6f33e-132">Show carousel flipper</span></span>     | <span data-ttu-id="6f33e-133">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="6f33e-133">**True** or **False**</span></span>              | <span data-ttu-id="6f33e-134">Een waarde die aangeeft of de carrouselflippers moeten worden weergegeven, zodat klanten handmatig meerdere banneritems kunnen doorlopen.</span><span class="sxs-lookup"><span data-stu-id="6f33e-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="6f33e-135">Tekstuitlijning</span><span class="sxs-lookup"><span data-stu-id="6f33e-135">Text alignment</span></span>            | <span data-ttu-id="6f33e-136">**Rechts**, **Links** of **Midden**</span><span class="sxs-lookup"><span data-stu-id="6f33e-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="6f33e-137">De tekstuitlijning in de promobannermodule.</span><span class="sxs-lookup"><span data-stu-id="6f33e-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="6f33e-138">Koppeling</span><span class="sxs-lookup"><span data-stu-id="6f33e-138">Link</span></span>                      | <span data-ttu-id="6f33e-139">Een URL</span><span class="sxs-lookup"><span data-stu-id="6f33e-139">A URL</span></span>                              | <span data-ttu-id="6f33e-140">Een URL voor een optionele koppeling.</span><span class="sxs-lookup"><span data-stu-id="6f33e-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="6f33e-141">Een promobannermodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="6f33e-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="6f33e-142">Voer de volgende stappen uit om een promobannermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="6f33e-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6f33e-143">Selecteer **Nieuw** om een paginasjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="6f33e-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="6f33e-144">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Sjabloon voor promobanner** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="6f33e-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="6f33e-145">Voeg onder **Paginaoverzicht** een **Standaardpagina**module aan de **Hoofd**sleuf toe.</span><span class="sxs-lookup"><span data-stu-id="6f33e-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="6f33e-146">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="6f33e-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="6f33e-147">Gebruik de sjabloon die u zojuist hebt gemaakt om een pagina met de naam **Promobannerpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="6f33e-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="6f33e-148">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="6f33e-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="6f33e-149">Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="6f33e-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="6f33e-150">Voeg onder **Paginaoverzicht** een promobannermodule aan de containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="6f33e-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="6f33e-151">Voeg in de instellingen voor de bannermodule een of meer bannerberichten toe.</span><span class="sxs-lookup"><span data-stu-id="6f33e-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="6f33e-152">Elk bericht kan tekst bevatten met een koppeling.</span><span class="sxs-lookup"><span data-stu-id="6f33e-152">Each message can have text together with a link.</span></span> <span data-ttu-id="6f33e-153">U kunt de andere eigenschappen bewerken als u de module verder wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="6f33e-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="6f33e-154">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="6f33e-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="6f33e-155">Bovenaan de pagina wordt een waarschuwing weergegeven die de tekst toont die u hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="6f33e-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="6f33e-156">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="6f33e-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="6f33e-157">Een promobanner wordt meestal gebruikt in de sleuf van een paginakoptekst of een sleuf van een subkoptekst.</span><span class="sxs-lookup"><span data-stu-id="6f33e-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6f33e-158">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="6f33e-158">Additional resources</span></span>

[<span data-ttu-id="6f33e-159">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="6f33e-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6f33e-160">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="6f33e-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="6f33e-161">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="6f33e-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="6f33e-162">Inhoudsblokmodule</span><span class="sxs-lookup"><span data-stu-id="6f33e-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="6f33e-163">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="6f33e-163">Video player module</span></span>](add-video-player.md)
