---
title: Videospelermodule
description: In dit onderwerp wordt beschreven wat videospelermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025639"
---
# <a name="video-player-module"></a><span data-ttu-id="4376a-103">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="4376a-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4376a-104">In dit onderwerp wordt beschreven wat videospelermodules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4376a-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4376a-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="4376a-105">Overview</span></span>

<span data-ttu-id="4376a-106">De videospelermodules wordt gebruikt om het afspelen van video's te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="4376a-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="4376a-107">Deze kan aan elke pagina worden toegevoegd, mits video-inhoud wordt geüpload naar en beschikbaar is in het CMS-systeem (Content Management System).</span><span class="sxs-lookup"><span data-stu-id="4376a-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="4376a-108">De videospelermodule ondersteunt het mediatype .mp4.</span><span class="sxs-lookup"><span data-stu-id="4376a-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="4376a-109">Videospelermodule</span><span class="sxs-lookup"><span data-stu-id="4376a-109">Video player module</span></span>

<span data-ttu-id="4376a-110">De module van de videospeler kan worden gebruikt om video's te presenteren op een e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="4376a-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="4376a-111">De module ondersteunt alle afspeelmogelijkheden, zoals afspelen, pauzeren, volledig beeld, audiobeschrijvingen en ondertiteling.</span><span class="sxs-lookup"><span data-stu-id="4376a-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="4376a-112">De module van de videospeler ondersteunt ook het aanpassen van de ondertiteling voor Microsoft-standaarden voor toegankelijkheid.</span><span class="sxs-lookup"><span data-stu-id="4376a-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="4376a-113">U kunt bijvoorbeeld de tekengrootte en de achtergrondkleur aanpassen.</span><span class="sxs-lookup"><span data-stu-id="4376a-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="4376a-114">De videospelermodule ondersteunt ook secundaire audiotracks.</span><span class="sxs-lookup"><span data-stu-id="4376a-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="4376a-115">Wanneer een video wordt geüpload naar het CMS, kan ook een secundaire audiotrack worden geüpload.</span><span class="sxs-lookup"><span data-stu-id="4376a-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="4376a-116">De videospelermodule kan vervolgens de secundaire audiotrack afspelen als een gebruiker deze selecteert.</span><span class="sxs-lookup"><span data-stu-id="4376a-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="4376a-117">Voorbeelden van videospelermodules in e-commerce</span><span class="sxs-lookup"><span data-stu-id="4376a-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="4376a-118">Instructievideo's op pagina's met productgegevens of marketingpagina's</span><span class="sxs-lookup"><span data-stu-id="4376a-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="4376a-119">Promotievideo's of video's over beleid op een marketingpagina</span><span class="sxs-lookup"><span data-stu-id="4376a-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="4376a-120">Marketingvideo's die productfuncties markeren op pagina's met productgegevens of marketingpagina's</span><span class="sxs-lookup"><span data-stu-id="4376a-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="4376a-121">Eigenschappen van videospelermodule</span><span class="sxs-lookup"><span data-stu-id="4376a-121">Video player module properties</span></span>

| <span data-ttu-id="4376a-122">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="4376a-122">Property name</span></span>         | <span data-ttu-id="4376a-123">Waarde</span><span class="sxs-lookup"><span data-stu-id="4376a-123">Value</span></span>                               | <span data-ttu-id="4376a-124">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="4376a-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="4376a-125">Automatisch afspelen</span><span class="sxs-lookup"><span data-stu-id="4376a-125">Auto play</span></span>             | <span data-ttu-id="4376a-126">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="4376a-126">**True** or **False**</span></span>               | <span data-ttu-id="4376a-127">Wanneer de waarde is ingesteld op **True**, wordt de video automatisch afgespeeld.</span><span class="sxs-lookup"><span data-stu-id="4376a-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="4376a-128">Dempen</span><span class="sxs-lookup"><span data-stu-id="4376a-128">Mute</span></span>                  | <span data-ttu-id="4376a-129">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="4376a-129">**True** or **False**</span></span>               | <span data-ttu-id="4376a-130">Wanneer de waarde is ingesteld op **True**, wordt het geluid gedempt.</span><span class="sxs-lookup"><span data-stu-id="4376a-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="4376a-131">Voor deze speler is de standaardwaarde **False**.</span><span class="sxs-lookup"><span data-stu-id="4376a-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="4376a-132">In de Chrome-browser worden de automatische video's standaard gedempt en wordt de audio alleen afgespeeld als de gebruiker de video handmatig start.</span><span class="sxs-lookup"><span data-stu-id="4376a-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="4376a-133">Lus</span><span class="sxs-lookup"><span data-stu-id="4376a-133">Loop</span></span>                  | <span data-ttu-id="4376a-134">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="4376a-134">**True** or **False**</span></span>               | <span data-ttu-id="4376a-135">Wanneer de waarde is ingesteld op **True**, wordt de video steeds herhaald.</span><span class="sxs-lookup"><span data-stu-id="4376a-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="4376a-136">Media</span><span class="sxs-lookup"><span data-stu-id="4376a-136">Media</span></span>                 | <span data-ttu-id="4376a-137">Bestandspad en -naam van video</span><span class="sxs-lookup"><span data-stu-id="4376a-137">Video file path and name</span></span> | <span data-ttu-id="4376a-138">Het videobestand dat in de videospeler wordt afgespeeld.</span><span class="sxs-lookup"><span data-stu-id="4376a-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="4376a-139">Op volledig scherm afspelen</span><span class="sxs-lookup"><span data-stu-id="4376a-139">Play fullscreen</span></span>       | <span data-ttu-id="4376a-140">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="4376a-140">**True** or **False**</span></span>               | <span data-ttu-id="4376a-141">Wanneer de waarde is ingesteld op **True**, wordt de video op volledig scherm afgespeeld.</span><span class="sxs-lookup"><span data-stu-id="4376a-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="4376a-142">Afspeel-/pauzetrigger</span><span class="sxs-lookup"><span data-stu-id="4376a-142">Play pause trigger</span></span>    | <span data-ttu-id="4376a-143">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="4376a-143">**True** or **False**</span></span>               | <span data-ttu-id="4376a-144">Wanneer de waarde is ingesteld op **True**, wordt de knop afspelen/pauze op de video weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4376a-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="4376a-145">Besturingselementen voor videospeler</span><span class="sxs-lookup"><span data-stu-id="4376a-145">Video player controls</span></span> | <span data-ttu-id="4376a-146">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="4376a-146">**True** or **False**</span></span>               | <span data-ttu-id="4376a-147">Wanneer de waarde is ingesteld op **True**, worden alle videospelerbesturingen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4376a-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="4376a-148">Deze besturingen zijn onder andere knoppen voor afspelen en onderbreken, een voortgangsindicator en opties voor ondertiteling.</span><span class="sxs-lookup"><span data-stu-id="4376a-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="4376a-149">Posterafbeelding verbergen</span><span class="sxs-lookup"><span data-stu-id="4376a-149">Hide poster image</span></span>     | <span data-ttu-id="4376a-150">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="4376a-150">**True** or **False**</span></span>               | <span data-ttu-id="4376a-151">Een video kan een posterframe hebben.</span><span class="sxs-lookup"><span data-stu-id="4376a-151">A video can have a poster frame.</span></span> <span data-ttu-id="4376a-152">Wanneer de waarde van deze eigenschap is ingesteld op **True**, is het posterframe verborgen.</span><span class="sxs-lookup"><span data-stu-id="4376a-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="4376a-153">Maskerniveau</span><span class="sxs-lookup"><span data-stu-id="4376a-153">Mask level</span></span>            | <span data-ttu-id="4376a-154">Een getal tussen **0** en **100**</span><span class="sxs-lookup"><span data-stu-id="4376a-154">A number from **0** through **100**</span></span> | <span data-ttu-id="4376a-155">Het masker dat op de video wordt toegepast voor opmaak.</span><span class="sxs-lookup"><span data-stu-id="4376a-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="4376a-156">Een videospelermodule toevoegen aan een pagina</span><span class="sxs-lookup"><span data-stu-id="4376a-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="4376a-157">Voordat u een videospelermodule maakt, moet u eerst een video uploaden naar de mediabibliotheek.</span><span class="sxs-lookup"><span data-stu-id="4376a-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="4376a-158">Voer de volgende stappen uit om een videospelermodule aan een nieuwe pagina toe te voegen en de vereiste eigenschappen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="4376a-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4376a-159">Maak een paginasjabloon met de naam **videospelersjabloon**.</span><span class="sxs-lookup"><span data-stu-id="4376a-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="4376a-160">Voeg in het **hoofdvak** van de standaardpagina een containermodule toe.</span><span class="sxs-lookup"><span data-stu-id="4376a-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="4376a-161">Voeg in de containermodule modules voor de videospeler en omgevingsvideospeler toe.</span><span class="sxs-lookup"><span data-stu-id="4376a-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="4376a-162">Voltooi het bewerken van de sjabloon en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="4376a-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="4376a-163">Gebruik de videospelersjabloon die u hebt gemaakt om een pagina met de naam **Videospelerpagina** te maken.</span><span class="sxs-lookup"><span data-stu-id="4376a-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="4376a-164">Voeg in het **hoofdvak** van de nieuwe pagina een videospelermodule toe.</span><span class="sxs-lookup"><span data-stu-id="4376a-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="4376a-165">Selecteer **Een video toevoegen** in het eigenschappenvenster voor de videospelermodule.</span><span class="sxs-lookup"><span data-stu-id="4376a-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="4376a-166">Selecteer in het dialoogvenster **Mediakiezer** een video en selecteer **Nieuw media-item uploaden**.</span><span class="sxs-lookup"><span data-stu-id="4376a-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="4376a-167">Sla de pagina op en bekijk een voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="4376a-167">Save and preview the page.</span></span> <span data-ttu-id="4376a-168">Als het goed is, wordt de videomodule op de pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="4376a-168">You should see the video module on the page.</span></span> <span data-ttu-id="4376a-169">U kunt extra instellingen wijzigen om het gedrag van de module aan te passen.</span><span class="sxs-lookup"><span data-stu-id="4376a-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="4376a-170">Voltooi het bewerken van de pagina en publiceer deze.</span><span class="sxs-lookup"><span data-stu-id="4376a-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4376a-171">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4376a-171">Additional resources</span></span>

[<span data-ttu-id="4376a-172">Overzicht starterskit</span><span class="sxs-lookup"><span data-stu-id="4376a-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4376a-173">Promospandoekmodule</span><span class="sxs-lookup"><span data-stu-id="4376a-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="4376a-174">Carrouselmodule</span><span class="sxs-lookup"><span data-stu-id="4376a-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="4376a-175">Tekstblokmodule</span><span class="sxs-lookup"><span data-stu-id="4376a-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="4376a-176">Inhoudsblokmodule</span><span class="sxs-lookup"><span data-stu-id="4376a-176">Content block module</span></span>](add-hero-module.md)
