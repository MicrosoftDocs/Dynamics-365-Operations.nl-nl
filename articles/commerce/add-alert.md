---
title: Promospandoekmodule
description: In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025615"
---
# <a name="promo-banner-module"></a><span data-ttu-id="788ca-103">Promospandoekmodule</span><span class="sxs-lookup"><span data-stu-id="788ca-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="788ca-104">In dit onderwerp wordt beschreven wat promobannermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="788ca-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="788ca-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="788ca-105">Overview</span></span>

<span data-ttu-id="788ca-106">Promobannermodules worden gebruikt om inline informatie op een pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="788ca-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="788ca-107">Ze kunnen worden gebruikt om promoties op alle pagina's van een e-commerce-site weer te geven.</span><span class="sxs-lookup"><span data-stu-id="788ca-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="788ca-108">Promobannermodules ondersteunen een tekstbericht en een koppeling.</span><span class="sxs-lookup"><span data-stu-id="788ca-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="788ca-109">Als er meerdere berichten aan een promobannermodule worden toegevoegd, verandert deze in een draaiende carrouselbanner waarmee klanten door alle berichten kunnen bladeren.</span><span class="sxs-lookup"><span data-stu-id="788ca-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="788ca-110">Promobannermodules worden aangestuurd door gegevens van het Content Management System (CMS) en kunnen op elke willekeurige pagina worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="788ca-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="788ca-111">Gebruiksvoorbeelden van promotiebanners in e-Commerce</span><span class="sxs-lookup"><span data-stu-id="788ca-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="788ca-112">Promobanners kunnen in de koptekst van een site worden gebruikt om promoties of berichten voor de hele site weer te geven, zoals in de volgende voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="788ca-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="788ca-113">"Jaarlijkse uitverkoop eindigt over 10 dagen"</span><span class="sxs-lookup"><span data-stu-id="788ca-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="788ca-114">"Grote besparingen bij terug naar school.</span><span class="sxs-lookup"><span data-stu-id="788ca-114">"Save big with back to school sale.</span></span> <span data-ttu-id="788ca-115">Winkel nu."</span><span class="sxs-lookup"><span data-stu-id="788ca-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="788ca-116">Eigenschappen van promobannermodules</span><span class="sxs-lookup"><span data-stu-id="788ca-116">Promo banner module properties</span></span>

| <span data-ttu-id="788ca-117">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="788ca-117">Property name</span></span>             | <span data-ttu-id="788ca-118">Value</span><span class="sxs-lookup"><span data-stu-id="788ca-118">Value</span></span>                              | <span data-ttu-id="788ca-119">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="788ca-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="788ca-120">Bannerberichten</span><span class="sxs-lookup"><span data-stu-id="788ca-120">Banner messages</span></span>           | <span data-ttu-id="788ca-121">Tekst en koppelingen</span><span class="sxs-lookup"><span data-stu-id="788ca-121">Text and links</span></span>                     | <span data-ttu-id="788ca-122">Een matrix met tekst en koppelingen.</span><span class="sxs-lookup"><span data-stu-id="788ca-122">An array of text and links.</span></span> |
| <span data-ttu-id="788ca-123">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="788ca-123">Autoplay</span></span>                  | <span data-ttu-id="788ca-124">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="788ca-124">**True** or **False**</span></span>              | <span data-ttu-id="788ca-125">Een waarde die aangeeft of berichten automatisch worden doorlopen als er meerdere berichten zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="788ca-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="788ca-126">Interval voor diaovergang</span><span class="sxs-lookup"><span data-stu-id="788ca-126">Slide transition interval</span></span> | <span data-ttu-id="788ca-127">Een aantal milliseconden (ms)</span><span class="sxs-lookup"><span data-stu-id="788ca-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="788ca-128">Het interval voor het doorlopen van berichten.</span><span class="sxs-lookup"><span data-stu-id="788ca-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="788ca-129">Negeren toestaan</span><span class="sxs-lookup"><span data-stu-id="788ca-129">Allow dismiss</span></span>             | <span data-ttu-id="788ca-130">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="788ca-130">**True** or **False**</span></span>              | <span data-ttu-id="788ca-131">Als de waarde is ingesteld op **True**, kunnen klanten de waarschuwing sluiten.</span><span class="sxs-lookup"><span data-stu-id="788ca-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="788ca-132">Carrouselflipper weergeven</span><span class="sxs-lookup"><span data-stu-id="788ca-132">Show carousel flipper</span></span>     | <span data-ttu-id="788ca-133">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="788ca-133">**True** or **False**</span></span>              | <span data-ttu-id="788ca-134">Een waarde die aangeeft of de carrouselflippers moeten worden weergegeven, zodat klanten handmatig meerdere banneritems kunnen doorlopen.</span><span class="sxs-lookup"><span data-stu-id="788ca-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="788ca-135">Tekstuitlijning</span><span class="sxs-lookup"><span data-stu-id="788ca-135">Text alignment</span></span>            | <span data-ttu-id="788ca-136">**Rechts**, **Links** of **Midden**</span><span class="sxs-lookup"><span data-stu-id="788ca-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="788ca-137">De tekstuitlijning in de promobannermodule.</span><span class="sxs-lookup"><span data-stu-id="788ca-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="788ca-138">Koppeling</span><span class="sxs-lookup"><span data-stu-id="788ca-138">Link</span></span>                      | <span data-ttu-id="788ca-139">Een URL</span><span class="sxs-lookup"><span data-stu-id="788ca-139">A URL</span></span>                              | <span data-ttu-id="788ca-140">Een URL voor een optionele koppeling.</span><span class="sxs-lookup"><span data-stu-id="788ca-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="788ca-141">Een promobannermodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="788ca-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="788ca-142">Voer de volgende stappen uit om een promobannermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="788ca-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="788ca-143">Maak een paginasjabloon met de naam **Promobannersjabloon**.</span><span class="sxs-lookup"><span data-stu-id="788ca-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="788ca-144">Voeg onder **Paginaoverzicht** een **Standaardpagina**module aan de **Hoofd**sleuf toe.</span><span class="sxs-lookup"><span data-stu-id="788ca-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="788ca-145">Check de sjabloon in en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="788ca-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="788ca-146">Gebruik de sjabloon die u zojuist hebt gemaakt om een pagina met de naam **Promobannerpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="788ca-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="788ca-147">Voeg in het **hoofdvak** van de nieuwe pagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="788ca-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="788ca-148">Stel in het deelvenster aan de rechterkant de waarde voor **Breedte** in op **Container vullen**.</span><span class="sxs-lookup"><span data-stu-id="788ca-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="788ca-149">Voeg onder **Paginaoverzicht** een promobannermodule aan de containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="788ca-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="788ca-150">Voeg in de instellingen voor de bannermodule een of meer bannerberichten toe.</span><span class="sxs-lookup"><span data-stu-id="788ca-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="788ca-151">Elk bericht kan tekst bevatten met een koppeling.</span><span class="sxs-lookup"><span data-stu-id="788ca-151">Each message can have text together with a link.</span></span> <span data-ttu-id="788ca-152">U kunt de andere eigenschappen bewerken als u de module verder wilt aanpassen.</span><span class="sxs-lookup"><span data-stu-id="788ca-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="788ca-153">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="788ca-153">Save and preview the page.</span></span> <span data-ttu-id="788ca-154">Bovenaan de pagina wordt een waarschuwing weergegeven die de tekst toont die u hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="788ca-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="788ca-155">Voltooi het bewerken van de pagina en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="788ca-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="788ca-156">Een promobanner wordt meestal gebruikt in de sleuf van een paginakoptekst of een sleuf van een subkoptekst.</span><span class="sxs-lookup"><span data-stu-id="788ca-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="788ca-157">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="788ca-157">Additional resources</span></span>

[<span data-ttu-id="788ca-158">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="788ca-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="788ca-159">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="788ca-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="788ca-160">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="788ca-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="788ca-161">Inhoudsblokmodule</span><span class="sxs-lookup"><span data-stu-id="788ca-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="788ca-162">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="788ca-162">Video player module</span></span>](add-video-player.md)
