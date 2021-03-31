---
title: Andere bestanden uploaden dan afbeeldingen en video's
description: In dit onderwerp wordt beschreven hoe u andere binaire bestanden dan afbeeldingen en video's kunt uploaden in Microsoft Dynamics 365 Commerce Site Builder.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c065aa961cf5c2d6770ae47c63a75953e6d38e00
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222532"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="88c14-103">Andere bestanden uploaden dan afbeeldingen en video's</span><span class="sxs-lookup"><span data-stu-id="88c14-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="88c14-104">In dit onderwerp wordt beschreven hoe u andere bestanden dan afbeeldingen en video's kunt uploaden in Microsoft Dynamics 365 Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="88c14-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="88c14-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="88c14-105">Overview</span></span>

<span data-ttu-id="88c14-106">De mediabibliotheek van Commerce-site builder ondersteunt het uploaden van andere binaire elementen dan afbeeldingen of video's.</span><span class="sxs-lookup"><span data-stu-id="88c14-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="88c14-107">U kunt bijvoorbeeld bestanden uploaden uit Microsoft Excel, Microsoft Word, Microsoft PowerPoint of PDF-bestanden.</span><span class="sxs-lookup"><span data-stu-id="88c14-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="88c14-108">De volgende documenttypen worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="88c14-108">The following document types are supported:</span></span>
- <span data-ttu-id="88c14-109">7Z</span><span class="sxs-lookup"><span data-stu-id="88c14-109">7Z</span></span>
- <span data-ttu-id="88c14-110">AVI</span><span class="sxs-lookup"><span data-stu-id="88c14-110">AVI</span></span>
- <span data-ttu-id="88c14-111">CS</span><span class="sxs-lookup"><span data-stu-id="88c14-111">CS</span></span>
- <span data-ttu-id="88c14-112">CSS</span><span class="sxs-lookup"><span data-stu-id="88c14-112">CSS</span></span>
- <span data-ttu-id="88c14-113">DOC</span><span class="sxs-lookup"><span data-stu-id="88c14-113">DOC</span></span>
- <span data-ttu-id="88c14-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="88c14-114">DOCX</span></span>
- <span data-ttu-id="88c14-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="88c14-115">EPUB</span></span>
- <span data-ttu-id="88c14-116">GIF</span><span class="sxs-lookup"><span data-stu-id="88c14-116">GIF</span></span>
- <span data-ttu-id="88c14-117">INDD</span><span class="sxs-lookup"><span data-stu-id="88c14-117">INDD</span></span>
- <span data-ttu-id="88c14-118">JAR</span><span class="sxs-lookup"><span data-stu-id="88c14-118">JAR</span></span>
- <span data-ttu-id="88c14-119">JPG</span><span class="sxs-lookup"><span data-stu-id="88c14-119">JPG</span></span>
- <span data-ttu-id="88c14-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="88c14-120">JPEG</span></span>
- <span data-ttu-id="88c14-121">JS</span><span class="sxs-lookup"><span data-stu-id="88c14-121">JS</span></span>
- <span data-ttu-id="88c14-122">MP3</span><span class="sxs-lookup"><span data-stu-id="88c14-122">MP3</span></span>
- <span data-ttu-id="88c14-123">MP4</span><span class="sxs-lookup"><span data-stu-id="88c14-123">MP4</span></span>
- <span data-ttu-id="88c14-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="88c14-124">MPEG</span></span>
- <span data-ttu-id="88c14-125">MPG</span><span class="sxs-lookup"><span data-stu-id="88c14-125">MPG</span></span>
- <span data-ttu-id="88c14-126">ODP</span><span class="sxs-lookup"><span data-stu-id="88c14-126">ODP</span></span>
- <span data-ttu-id="88c14-127">ODS</span><span class="sxs-lookup"><span data-stu-id="88c14-127">ODS</span></span>
- <span data-ttu-id="88c14-128">ODT</span><span class="sxs-lookup"><span data-stu-id="88c14-128">ODT</span></span>
- <span data-ttu-id="88c14-129">PDF</span><span class="sxs-lookup"><span data-stu-id="88c14-129">PDF</span></span>
- <span data-ttu-id="88c14-130">PNG</span><span class="sxs-lookup"><span data-stu-id="88c14-130">PNG</span></span>
- <span data-ttu-id="88c14-131">PPT</span><span class="sxs-lookup"><span data-stu-id="88c14-131">PPT</span></span>
- <span data-ttu-id="88c14-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="88c14-132">PPTX</span></span>
- <span data-ttu-id="88c14-133">PS</span><span class="sxs-lookup"><span data-stu-id="88c14-133">PS</span></span>
- <span data-ttu-id="88c14-134">QXP</span><span class="sxs-lookup"><span data-stu-id="88c14-134">QXP</span></span>
- <span data-ttu-id="88c14-135">RAR</span><span class="sxs-lookup"><span data-stu-id="88c14-135">RAR</span></span>
- <span data-ttu-id="88c14-136">RTF</span><span class="sxs-lookup"><span data-stu-id="88c14-136">RTF</span></span>
- <span data-ttu-id="88c14-137">SVG</span><span class="sxs-lookup"><span data-stu-id="88c14-137">SVG</span></span>
- <span data-ttu-id="88c14-138">TAR</span><span class="sxs-lookup"><span data-stu-id="88c14-138">TAR</span></span>
- <span data-ttu-id="88c14-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="88c14-139">TGZ</span></span>
- <span data-ttu-id="88c14-140">TXT</span><span class="sxs-lookup"><span data-stu-id="88c14-140">TXT</span></span>
- <span data-ttu-id="88c14-141">WMV</span><span class="sxs-lookup"><span data-stu-id="88c14-141">WMV</span></span>
- <span data-ttu-id="88c14-142">XLS</span><span class="sxs-lookup"><span data-stu-id="88c14-142">XLS</span></span>
- <span data-ttu-id="88c14-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="88c14-143">XLSX</span></span>
- <span data-ttu-id="88c14-144">XML</span><span class="sxs-lookup"><span data-stu-id="88c14-144">XML</span></span>
- <span data-ttu-id="88c14-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="88c14-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="88c14-146">Een bestand uploaden</span><span class="sxs-lookup"><span data-stu-id="88c14-146">Upload a file</span></span>

<span data-ttu-id="88c14-147">Volg deze stappen om een bestand te uploaden naar Commerce-site builder.</span><span class="sxs-lookup"><span data-stu-id="88c14-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="88c14-148">Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="88c14-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="88c14-149">Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="88c14-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="88c14-150">Selecteer in bestandsverkenner een of meer bestanden en selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="88c14-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="88c14-151">Geef in het dialoogvenster **Media-item uploaden** desgewenst de titel, beschrijving en trefwoordgegevens op.</span><span class="sxs-lookup"><span data-stu-id="88c14-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="88c14-152">Als u de bestanden direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in.</span><span class="sxs-lookup"><span data-stu-id="88c14-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="88c14-153">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="88c14-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88c14-154">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="88c14-154">Additional resources</span></span>

[<span data-ttu-id="88c14-155">Overzicht van digitaal activabeheer</span><span class="sxs-lookup"><span data-stu-id="88c14-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="88c14-156">Afbeeldingen uploaden</span><span class="sxs-lookup"><span data-stu-id="88c14-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="88c14-157">Video uploaden</span><span class="sxs-lookup"><span data-stu-id="88c14-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="88c14-158">Afbeeldingen bijsnijden</span><span class="sxs-lookup"><span data-stu-id="88c14-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="88c14-159">Focuspunten van afbeelding aanpassen</span><span class="sxs-lookup"><span data-stu-id="88c14-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="88c14-160">Statische bestanden uploaden en verwerken</span><span class="sxs-lookup"><span data-stu-id="88c14-160">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]