---
title: Video's uploaden
description: In dit onderwerp wordt beschreven hoe u video's uploadt in Microsoft Dynamics 365 Commerce Site Builder.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799200"
---
# <a name="upload-videos"></a><span data-ttu-id="1edcf-103">Video's uploaden</span><span class="sxs-lookup"><span data-stu-id="1edcf-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1edcf-104">In dit onderwerp wordt beschreven hoe u video's uploadt in Microsoft Dynamics 365 Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="1edcf-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="1edcf-105">Met de mediabibliotheek van Commerce Site Builder kunt u video's uploaden.</span><span class="sxs-lookup"><span data-stu-id="1edcf-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="1edcf-106">U moet altijd de versie van een video uploaden met de hoogste bitrate en resolutie, omdat de video automatisch wordt geconverteerd om geschikt te zijn voor verschillende viewports en bijbehorende onderbrekingspunten.</span><span class="sxs-lookup"><span data-stu-id="1edcf-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="1edcf-107">Videogegevens opgegeven tijdens het uploaden</span><span class="sxs-lookup"><span data-stu-id="1edcf-107">Video information specified during upload</span></span>

<span data-ttu-id="1edcf-108">Bij het uploaden van een video kan de volgende informatie worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="1edcf-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="1edcf-109">**Titel, beschrijving, trefwoorden**: metagegevens van de video.</span><span class="sxs-lookup"><span data-stu-id="1edcf-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="1edcf-110">**Automatisch ondertiteling genereren**: hiermee geeft u op of ondertiteling automatisch moet worden gegenereerd voor de video.</span><span class="sxs-lookup"><span data-stu-id="1edcf-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="1edcf-111">**Ondertiteling**: hiermee geeft u op of ondertiteling moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1edcf-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="1edcf-112">**Normale audio**: hiermee geeft u op dat het gewone audiospoor moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1edcf-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="1edcf-113">**Miniatuur**: hiermee geeft u de miniatuur voor de video op.</span><span class="sxs-lookup"><span data-stu-id="1edcf-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="1edcf-114">Als u dit niet opgeeft, wordt de miniatuur automatisch gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1edcf-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="1edcf-115">**Beschrijvende audio**: hiermee geeft u op dat het beschrijvende audiospoor moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1edcf-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="1edcf-116">Een video uploaden</span><span class="sxs-lookup"><span data-stu-id="1edcf-116">Upload a video</span></span>

<span data-ttu-id="1edcf-117">Volg deze stappen om een video te uploaden in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="1edcf-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="1edcf-118">Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="1edcf-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="1edcf-119">Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="1edcf-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="1edcf-120">Ga in het venster Bestandsverkenner naar een of meer videobestanden die u wilt uploaden en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="1edcf-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="1edcf-121">Voer in het dialoogvenster **Media-item uploaden** de vereiste titel en alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="1edcf-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="1edcf-122">Voer een optionele omschrijving en trefwoorden in en selecteer indien gewenst een categorie.</span><span class="sxs-lookup"><span data-stu-id="1edcf-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="1edcf-123">Als u de afbeelding(en) direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in</span><span class="sxs-lookup"><span data-stu-id="1edcf-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="1edcf-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="1edcf-124">Select **OK**.</span></span>

<span data-ttu-id="1edcf-125">Als u meerdere typen bestanden tegelijk uploadt (zoals afbeeldingen en video's), kunt u in het dialoogvenster **Media-item uploaden** alleen trefwoorden opgeven, of de bestanden direct na het uploaden moeten worden gepubliceerd en of ondertiteling automatisch moeten worden gegenereerd voor videobestanden.</span><span class="sxs-lookup"><span data-stu-id="1edcf-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="1edcf-126">Alle bestanden hebben dezelfde trefwoorden.</span><span class="sxs-lookup"><span data-stu-id="1edcf-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1edcf-127">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="1edcf-127">Additional resources</span></span>

[<span data-ttu-id="1edcf-128">Overzicht van digitaal activabeheer</span><span class="sxs-lookup"><span data-stu-id="1edcf-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="1edcf-129">Afbeeldingen uploaden</span><span class="sxs-lookup"><span data-stu-id="1edcf-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="1edcf-130">Bestanden uploaden</span><span class="sxs-lookup"><span data-stu-id="1edcf-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="1edcf-131">Afbeeldingen bijsnijden</span><span class="sxs-lookup"><span data-stu-id="1edcf-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="1edcf-132">Focuspunten van afbeelding aanpassen</span><span class="sxs-lookup"><span data-stu-id="1edcf-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="1edcf-133">Statische bestanden uploaden en verwerken</span><span class="sxs-lookup"><span data-stu-id="1edcf-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
