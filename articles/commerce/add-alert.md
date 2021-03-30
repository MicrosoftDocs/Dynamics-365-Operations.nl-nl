---
title: Promospandoekmodule
description: In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206578"
---
# <a name="promo-banner-module"></a><span data-ttu-id="89aec-103">Promotiebanner-module</span><span class="sxs-lookup"><span data-stu-id="89aec-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="89aec-104">In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="89aec-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="89aec-105">Promobannermodules worden gebruikt om inline informatie op een pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="89aec-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="89aec-106">Ze kunnen worden gebruikt om promoties op alle pagina's van een e-commerce-site weer te geven.</span><span class="sxs-lookup"><span data-stu-id="89aec-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="89aec-107">Promobannermodules ondersteunen een tekstbericht en een koppeling.</span><span class="sxs-lookup"><span data-stu-id="89aec-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="89aec-108">Als er meerdere berichten aan een promobannermodule worden toegevoegd, verandert deze in een draaiende carrouselbanner waarmee klanten door alle berichten kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="89aec-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="89aec-109">Promobannermodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="89aec-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="89aec-110">Gebruiksvoorbeelden van promotiebanners in e-Commerce</span><span class="sxs-lookup"><span data-stu-id="89aec-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="89aec-111">Promobanners kunnen in de koptekst van een site worden gebruikt om promoties of berichten voor de hele site weer te geven, zoals in de volgende voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="89aec-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="89aec-112">"Jaarlijkse uitverkoop eindigt over 10 dagen"</span><span class="sxs-lookup"><span data-stu-id="89aec-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="89aec-113">"Grote besparingen bij terug naar school.</span><span class="sxs-lookup"><span data-stu-id="89aec-113">"Save big with back to school sale.</span></span> <span data-ttu-id="89aec-114">Winkel nu."</span><span class="sxs-lookup"><span data-stu-id="89aec-114">Shop Now."</span></span>

<span data-ttu-id="89aec-115">"Uitverkoop met Thanksgiving!"</span><span class="sxs-lookup"><span data-stu-id="89aec-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="89aec-116">In de volgende afbeelding ziet u een voorbeeld van een promobanner.</span><span class="sxs-lookup"><span data-stu-id="89aec-116">The following image shows an example of a promo banner.</span></span>

![Voorbeeld van een promotiebannermodule](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="89aec-118">Eigenschappen van promobannermodules</span><span class="sxs-lookup"><span data-stu-id="89aec-118">Promo banner module properties</span></span>

| <span data-ttu-id="89aec-119">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="89aec-119">Property name</span></span>             | <span data-ttu-id="89aec-120">Waarde</span><span class="sxs-lookup"><span data-stu-id="89aec-120">Value</span></span>                              | <span data-ttu-id="89aec-121">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="89aec-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="89aec-122">Bannerberichten</span><span class="sxs-lookup"><span data-stu-id="89aec-122">Banner messages</span></span>           | <span data-ttu-id="89aec-123">Tekst en koppelingen</span><span class="sxs-lookup"><span data-stu-id="89aec-123">Text and links</span></span>                     | <span data-ttu-id="89aec-124">Een matrix met tekst en koppelingen.</span><span class="sxs-lookup"><span data-stu-id="89aec-124">An array of text and links.</span></span> |
| <span data-ttu-id="89aec-125">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="89aec-125">Autoplay</span></span>                  | <span data-ttu-id="89aec-126">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="89aec-126">**True** or **False**</span></span>              | <span data-ttu-id="89aec-127">Een waarde die aangeeft of berichten automatisch worden doorlopen als er meerdere berichten zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="89aec-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="89aec-128">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="89aec-128">Slide transition interval</span></span> | <span data-ttu-id="89aec-129">Een aantal milliseconden (ms)</span><span class="sxs-lookup"><span data-stu-id="89aec-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="89aec-130">Het interval voor het doorlopen van berichten.</span><span class="sxs-lookup"><span data-stu-id="89aec-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="89aec-131">Negeren toestaan</span><span class="sxs-lookup"><span data-stu-id="89aec-131">Allow dismiss</span></span>             | <span data-ttu-id="89aec-132">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="89aec-132">**True** or **False**</span></span>              | <span data-ttu-id="89aec-133">Als de waarde is ingesteld op **True**, kunnen klanten de waarschuwing sluiten.</span><span class="sxs-lookup"><span data-stu-id="89aec-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="89aec-134">Carrouselflipper weergeven</span><span class="sxs-lookup"><span data-stu-id="89aec-134">Show carousel flipper</span></span>     | <span data-ttu-id="89aec-135">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="89aec-135">**True** or **False**</span></span>              | <span data-ttu-id="89aec-136">Een waarde die aangeeft of de carrouselflippers moeten worden weergegeven, zodat klanten handmatig meerdere banneritems kunnen doorlopen.</span><span class="sxs-lookup"><span data-stu-id="89aec-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="89aec-137">Tekstuitlijning</span><span class="sxs-lookup"><span data-stu-id="89aec-137">Text alignment</span></span>            | <span data-ttu-id="89aec-138">**Rechts**, **Links** of **Midden**</span><span class="sxs-lookup"><span data-stu-id="89aec-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="89aec-139">De tekstuitlijning in de promobannermodule.</span><span class="sxs-lookup"><span data-stu-id="89aec-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="89aec-140">Koppeling</span><span class="sxs-lookup"><span data-stu-id="89aec-140">Link</span></span>                      | <span data-ttu-id="89aec-141">Een URL</span><span class="sxs-lookup"><span data-stu-id="89aec-141">A URL</span></span>                              | <span data-ttu-id="89aec-142">Een URL voor een optionele koppeling.</span><span class="sxs-lookup"><span data-stu-id="89aec-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="89aec-143">Een promobannermodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="89aec-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="89aec-144">Voer de volgende stappen uit om een promobannermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="89aec-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="89aec-145">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="89aec-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="89aec-146">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Sjabloon voor promobanner** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="89aec-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="89aec-147">Voeg onder **Paginaoverzicht** een **Standaardpagina** module aan de **Hoofd** sleuf toe.</span><span class="sxs-lookup"><span data-stu-id="89aec-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="89aec-148">Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="89aec-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="89aec-149">Gebruik de sjabloon die u zojuist hebt gemaakt om een pagina met de naam **Promobannerpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="89aec-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="89aec-150">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="89aec-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="89aec-151">Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="89aec-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="89aec-152">Voeg onder **Paginaoverzicht** een promobannermodule aan de containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="89aec-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="89aec-153">Voeg in de instellingen voor de bannermodule een of meer bannerberichten toe.</span><span class="sxs-lookup"><span data-stu-id="89aec-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="89aec-154">Elk bericht kan tekst bevatten met een koppeling.</span><span class="sxs-lookup"><span data-stu-id="89aec-154">Each message can have text together with a link.</span></span> <span data-ttu-id="89aec-155">U kunt de andere eigenschappen bewerken als u de module verder wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="89aec-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="89aec-156">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="89aec-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="89aec-157">Bovenaan de pagina wordt een waarschuwing weergegeven die de tekst toont die u hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="89aec-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="89aec-158">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="89aec-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="89aec-159">Een promobanner wordt meestal gebruikt in de sleuf van een paginakoptekst of een sleuf van een subkoptekst.</span><span class="sxs-lookup"><span data-stu-id="89aec-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="89aec-160">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="89aec-160">Additional resources</span></span>

[<span data-ttu-id="89aec-161">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="89aec-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="89aec-162">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="89aec-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="89aec-163">Text Block-module</span><span class="sxs-lookup"><span data-stu-id="89aec-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="89aec-164">Inhoudsblokkenmodule</span><span class="sxs-lookup"><span data-stu-id="89aec-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="89aec-165">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="89aec-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]