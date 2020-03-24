---
title: Video's uploaden
description: In dit onderwerp wordt beschreven hoe u video's uploadt in Microsoft Dynamics 365 Commerce Site Builder.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096997"
---
# <a name="upload-videos"></a><span data-ttu-id="edcc7-103">Video's uploaden</span><span class="sxs-lookup"><span data-stu-id="edcc7-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="edcc7-104">In dit onderwerp wordt beschreven hoe u video's uploadt in Microsoft Dynamics 365 Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="edcc7-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="edcc7-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="edcc7-105">Overview</span></span>

<span data-ttu-id="edcc7-106">Met de mediabibliotheek van Commerce Site Builder kunt u video's uploaden.</span><span class="sxs-lookup"><span data-stu-id="edcc7-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="edcc7-107">U moet altijd de versie van een video uploaden met de hoogste bitrate en resolutie, omdat de video automatisch wordt geconverteerd om geschikt te zijn voor verschillende viewports en bijbehorende onderbrekingspunten.</span><span class="sxs-lookup"><span data-stu-id="edcc7-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="edcc7-108">Videogegevens opgegeven tijdens het uploaden</span><span class="sxs-lookup"><span data-stu-id="edcc7-108">Video information specified during upload</span></span>

<span data-ttu-id="edcc7-109">Bij het uploaden van een video kan de volgende informatie worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="edcc7-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="edcc7-110">**Titel, beschrijving, trefwoorden**: metagegevens van de video.</span><span class="sxs-lookup"><span data-stu-id="edcc7-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="edcc7-111">**Automatisch ondertiteling genereren**: hiermee geeft u op of ondertiteling automatisch moet worden gegenereerd voor de video.</span><span class="sxs-lookup"><span data-stu-id="edcc7-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="edcc7-112">**Ondertiteling**: hiermee geeft u op of ondertiteling moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="edcc7-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="edcc7-113">**Normale audio**: hiermee geeft u op dat het gewone audiospoor moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="edcc7-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="edcc7-114">**Miniatuur**: hiermee geeft u de miniatuur voor de video op.</span><span class="sxs-lookup"><span data-stu-id="edcc7-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="edcc7-115">Als u dit niet opgeeft, wordt de miniatuur automatisch gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="edcc7-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="edcc7-116">**Beschrijvende audio**: hiermee geeft u op dat het beschrijvende audiospoor moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="edcc7-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="edcc7-117">Een video uploaden</span><span class="sxs-lookup"><span data-stu-id="edcc7-117">Upload a video</span></span>

<span data-ttu-id="edcc7-118">Volg deze stappen om een video te uploaden in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="edcc7-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="edcc7-119">Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="edcc7-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="edcc7-120">Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="edcc7-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="edcc7-121">Ga in het venster Bestandsverkenner naar een of meer videobestanden die u wilt uploaden en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="edcc7-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="edcc7-122">Voer in het dialoogvenster **Media-item uploaden** de vereiste titel en alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="edcc7-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="edcc7-123">Voer een optionele omschrijving en trefwoorden in en selecteer indien gewenst een categorie.</span><span class="sxs-lookup"><span data-stu-id="edcc7-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="edcc7-124">Als u de afbeelding(en) direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in</span><span class="sxs-lookup"><span data-stu-id="edcc7-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="edcc7-125">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="edcc7-125">Select **OK**.</span></span>

<span data-ttu-id="edcc7-126">Als u meerdere typen bestanden tegelijk uploadt (zoals afbeeldingen en video's), kunt u in het dialoogvenster **Media-item uploaden** alleen trefwoorden opgeven, of de bestanden direct na het uploaden moeten worden gepubliceerd en of ondertiteling automatisch moeten worden gegenereerd voor videobestanden.</span><span class="sxs-lookup"><span data-stu-id="edcc7-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="edcc7-127">Alle bestanden hebben dezelfde trefwoorden.</span><span class="sxs-lookup"><span data-stu-id="edcc7-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="edcc7-128">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="edcc7-128">Additional resources</span></span>

[<span data-ttu-id="edcc7-129">Overzicht van digitaal activabeheer</span><span class="sxs-lookup"><span data-stu-id="edcc7-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="edcc7-130">Afbeeldingen uploaden</span><span class="sxs-lookup"><span data-stu-id="edcc7-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="edcc7-131">Bestanden uploaden</span><span class="sxs-lookup"><span data-stu-id="edcc7-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="edcc7-132">Afbeeldingen bijsnijden</span><span class="sxs-lookup"><span data-stu-id="edcc7-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="edcc7-133">De focuspunten van de afbeelding aanpassen</span><span class="sxs-lookup"><span data-stu-id="edcc7-133">Customize image focal points</span></span>](dam-custom-focal-point.md)
