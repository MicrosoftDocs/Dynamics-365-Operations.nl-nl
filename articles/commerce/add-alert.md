---
title: Promospandoekmodule
description: In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: dae824cdbaaf56f85f125c5f36aaa56171bbd6bc
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411360"
---
# <a name="promo-banner-module"></a><span data-ttu-id="2ca16-103">Promospandoekmodule</span><span class="sxs-lookup"><span data-stu-id="2ca16-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2ca16-104">In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2ca16-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2ca16-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="2ca16-105">Overview</span></span>

<span data-ttu-id="2ca16-106">Promobannermodules worden gebruikt om inline informatie op een pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="2ca16-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="2ca16-107">Ze kunnen worden gebruikt om promoties op alle pagina's van een e-commerce-site weer te geven.</span><span class="sxs-lookup"><span data-stu-id="2ca16-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="2ca16-108">Promobannermodules ondersteunen een tekstbericht en een koppeling.</span><span class="sxs-lookup"><span data-stu-id="2ca16-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="2ca16-109">Als er meerdere berichten aan een promobannermodule worden toegevoegd, verandert deze in een draaiende carrouselbanner waarmee klanten door alle berichten kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="2ca16-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="2ca16-110">Promobannermodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="2ca16-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="2ca16-111">Gebruiksvoorbeelden van promotiebanners in e-Commerce</span><span class="sxs-lookup"><span data-stu-id="2ca16-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="2ca16-112">Promobanners kunnen in de koptekst van een site worden gebruikt om promoties of berichten voor de hele site weer te geven, zoals in de volgende voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="2ca16-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="2ca16-113">"Jaarlijkse uitverkoop eindigt over 10 dagen"</span><span class="sxs-lookup"><span data-stu-id="2ca16-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="2ca16-114">"Grote besparingen bij terug naar school.</span><span class="sxs-lookup"><span data-stu-id="2ca16-114">"Save big with back to school sale.</span></span> <span data-ttu-id="2ca16-115">Winkel nu."</span><span class="sxs-lookup"><span data-stu-id="2ca16-115">Shop Now."</span></span>

<span data-ttu-id="2ca16-116">"Uitverkoop met Thanksgiving!"</span><span class="sxs-lookup"><span data-stu-id="2ca16-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="2ca16-117">In de volgende afbeelding ziet u een voorbeeld van een promobanner.</span><span class="sxs-lookup"><span data-stu-id="2ca16-117">The following image shows an example of a promo banner.</span></span>

![Voorbeeld van een promotiebannermodule](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="2ca16-119">Eigenschappen van promobannermodules</span><span class="sxs-lookup"><span data-stu-id="2ca16-119">Promo banner module properties</span></span>

| <span data-ttu-id="2ca16-120">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="2ca16-120">Property name</span></span>             | <span data-ttu-id="2ca16-121">Waarde</span><span class="sxs-lookup"><span data-stu-id="2ca16-121">Value</span></span>                              | <span data-ttu-id="2ca16-122">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="2ca16-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="2ca16-123">Bannerberichten</span><span class="sxs-lookup"><span data-stu-id="2ca16-123">Banner messages</span></span>           | <span data-ttu-id="2ca16-124">Tekst en koppelingen</span><span class="sxs-lookup"><span data-stu-id="2ca16-124">Text and links</span></span>                     | <span data-ttu-id="2ca16-125">Een matrix met tekst en koppelingen.</span><span class="sxs-lookup"><span data-stu-id="2ca16-125">An array of text and links.</span></span> |
| <span data-ttu-id="2ca16-126">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="2ca16-126">Autoplay</span></span>                  | <span data-ttu-id="2ca16-127">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="2ca16-127">**True** or **False**</span></span>              | <span data-ttu-id="2ca16-128">Een waarde die aangeeft of berichten automatisch worden doorlopen als er meerdere berichten zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="2ca16-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="2ca16-129">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="2ca16-129">Slide transition interval</span></span> | <span data-ttu-id="2ca16-130">Een aantal milliseconden (ms)</span><span class="sxs-lookup"><span data-stu-id="2ca16-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="2ca16-131">Het interval voor het doorlopen van berichten.</span><span class="sxs-lookup"><span data-stu-id="2ca16-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="2ca16-132">Negeren toestaan</span><span class="sxs-lookup"><span data-stu-id="2ca16-132">Allow dismiss</span></span>             | <span data-ttu-id="2ca16-133">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="2ca16-133">**True** or **False**</span></span>              | <span data-ttu-id="2ca16-134">Als de waarde is ingesteld op **True**, kunnen klanten de waarschuwing sluiten.</span><span class="sxs-lookup"><span data-stu-id="2ca16-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="2ca16-135">Carrouselflipper weergeven</span><span class="sxs-lookup"><span data-stu-id="2ca16-135">Show carousel flipper</span></span>     | <span data-ttu-id="2ca16-136">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="2ca16-136">**True** or **False**</span></span>              | <span data-ttu-id="2ca16-137">Een waarde die aangeeft of de carrouselflippers moeten worden weergegeven, zodat klanten handmatig meerdere banneritems kunnen doorlopen.</span><span class="sxs-lookup"><span data-stu-id="2ca16-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="2ca16-138">Tekstuitlijning</span><span class="sxs-lookup"><span data-stu-id="2ca16-138">Text alignment</span></span>            | <span data-ttu-id="2ca16-139">**Rechts**, **Links** of **Midden**</span><span class="sxs-lookup"><span data-stu-id="2ca16-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="2ca16-140">De tekstuitlijning in de promobannermodule.</span><span class="sxs-lookup"><span data-stu-id="2ca16-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="2ca16-141">Koppeling</span><span class="sxs-lookup"><span data-stu-id="2ca16-141">Link</span></span>                      | <span data-ttu-id="2ca16-142">Een URL</span><span class="sxs-lookup"><span data-stu-id="2ca16-142">A URL</span></span>                              | <span data-ttu-id="2ca16-143">Een URL voor een optionele koppeling.</span><span class="sxs-lookup"><span data-stu-id="2ca16-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="2ca16-144">Een promobannermodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="2ca16-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="2ca16-145">Voer de volgende stappen uit om een promobannermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="2ca16-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2ca16-146">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="2ca16-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2ca16-147">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Sjabloon voor promobanner** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ca16-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2ca16-148">Voeg onder **Paginaoverzicht** een **Standaardpagina**module aan de **Hoofd**sleuf toe.</span><span class="sxs-lookup"><span data-stu-id="2ca16-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="2ca16-149">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="2ca16-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="2ca16-150">Gebruik de sjabloon die u zojuist hebt gemaakt om een pagina met de naam **Promobannerpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="2ca16-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="2ca16-151">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="2ca16-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="2ca16-152">Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="2ca16-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="2ca16-153">Voeg onder **Paginaoverzicht** een promobannermodule aan de containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="2ca16-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="2ca16-154">Voeg in de instellingen voor de bannermodule een of meer bannerberichten toe.</span><span class="sxs-lookup"><span data-stu-id="2ca16-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="2ca16-155">Elk bericht kan tekst bevatten met een koppeling.</span><span class="sxs-lookup"><span data-stu-id="2ca16-155">Each message can have text together with a link.</span></span> <span data-ttu-id="2ca16-156">U kunt de andere eigenschappen bewerken als u de module verder wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="2ca16-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="2ca16-157">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="2ca16-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2ca16-158">Bovenaan de pagina wordt een waarschuwing weergegeven die de tekst toont die u hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="2ca16-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="2ca16-159">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="2ca16-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="2ca16-160">Een promobanner wordt meestal gebruikt in de sleuf van een paginakoptekst of een sleuf van een subkoptekst.</span><span class="sxs-lookup"><span data-stu-id="2ca16-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="2ca16-161">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2ca16-161">Additional resources</span></span>

[<span data-ttu-id="2ca16-162">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="2ca16-162">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2ca16-163">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="2ca16-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2ca16-164">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="2ca16-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2ca16-165">Inhoudsblokmodule</span><span class="sxs-lookup"><span data-stu-id="2ca16-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="2ca16-166">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="2ca16-166">Video player module</span></span>](add-video-player.md)
