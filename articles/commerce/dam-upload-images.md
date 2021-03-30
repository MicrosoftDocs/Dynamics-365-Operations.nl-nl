---
title: Afbeeldingen uploaden
description: In dit onderwerp wordt beschreven hoe u afbeeldingen uploadt in Microsoft Dynamics 365 Commerce Site Builder.
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
ms.openlocfilehash: 51571ce221714598b2e2d39c76cb69dcb57cc52b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213789"
---
# <a name="upload-images"></a><span data-ttu-id="7a12d-103">Afbeeldingen uploaden</span><span class="sxs-lookup"><span data-stu-id="7a12d-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7a12d-104">In dit onderwerp wordt beschreven hoe u afbeeldingen uploadt in Microsoft Dynamics 365 Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="7a12d-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="7a12d-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="7a12d-105">Overview</span></span>

<span data-ttu-id="7a12d-106">Met de mediabibliotheek van de Commerce Site Builder kunt u afbeeldingen met mappen uploaden, zowel afzonderlijk als tegelijk.</span><span class="sxs-lookup"><span data-stu-id="7a12d-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="7a12d-107">U moet altijd de versie van de afbeelding uploaden met de hoogste resolutie en kwaliteit, omdat de componenten voor het bepalen van de afbeeldinggrootte automatisch de afbeelding optimaliseert voor de verschillende viewports en de bijbehorende onderbrekingspunten.</span><span class="sxs-lookup"><span data-stu-id="7a12d-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="7a12d-108">Afbeeldingsgegevens die zijn opgegeven tijdens het uploaden</span><span class="sxs-lookup"><span data-stu-id="7a12d-108">Image information specified during upload</span></span>

<span data-ttu-id="7a12d-109">Bij het uploaden van een afbeelding kan de volgende informatie worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="7a12d-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="7a12d-110">**Titel, alternatieve tekst, beschrijving, trefwoorden**: metagegevens van de afbeelding of afbeeldingen.</span><span class="sxs-lookup"><span data-stu-id="7a12d-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="7a12d-111">Titel en alternatieve tekst zijn vereiste waarden.</span><span class="sxs-lookup"><span data-stu-id="7a12d-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="7a12d-112">**Categorie selecteren**:</span><span class="sxs-lookup"><span data-stu-id="7a12d-112">**Select category**:</span></span>
    - <span data-ttu-id="7a12d-113">**Geen**: wordt gebruikt voor beeldende e-commerce-afbeeldingen.</span><span class="sxs-lookup"><span data-stu-id="7a12d-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="7a12d-114">**Product, categorie, klant, werknemer,catalogus**: wordt gebruikt voor omnichannel-afbeelding(en) in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7a12d-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="7a12d-115">**Activa publiceren na uploaden**: wanneer dit selectievakje is ingeschakeld, worden de afbeeldingen direct na het uploaden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="7a12d-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="7a12d-116">Afbeeldingsactiva waaraan een categorie is toegewezen, worden ook automatisch gelabeld met de categorie als trefwoord voor het zoeken naar activa van een bepaalde categorie.</span><span class="sxs-lookup"><span data-stu-id="7a12d-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="7a12d-117">Naamgevingsconventies voor omnichannel-afbeeldingen</span><span class="sxs-lookup"><span data-stu-id="7a12d-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="7a12d-118">Als u de mediabibliotheek hebt geconfigureerd als backend van de omnichannel-afbeelding, kunt u afbeeldingscategorieën gebruiken om aan te geven tot welke categorie de geüploade afbeelding behoort.</span><span class="sxs-lookup"><span data-stu-id="7a12d-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="7a12d-119">Er is ook een naamgevingsconventie die moet worden gevolgd om ervoor te zorgen dat afbeeldingen correct worden opgehaald door andere kanalen, zoals POS.</span><span class="sxs-lookup"><span data-stu-id="7a12d-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="7a12d-120">De standaard naamgevingsconventie varieert afhankelijk van de categorie:</span><span class="sxs-lookup"><span data-stu-id="7a12d-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="7a12d-121">Catalogusafbeeldingen moeten de naam "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**" hebben</span><span class="sxs-lookup"><span data-stu-id="7a12d-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="7a12d-122">Categorieafbeeldingen moeten de naam "**/Categories/\{CategoryName\}.png**" hebben</span><span class="sxs-lookup"><span data-stu-id="7a12d-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="7a12d-123">Klantafbeeldingen moeten de naam "**/Customers/\{CustomerNumber\}.jpg**" hebben</span><span class="sxs-lookup"><span data-stu-id="7a12d-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="7a12d-124">Afbeeldingen van werknemers moeten de naam "**/Workers/\{WorkerNumber\}.jpg**" hebben</span><span class="sxs-lookup"><span data-stu-id="7a12d-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="7a12d-125">Productafbeeldingen moeten de naam "**/Products/\{ProductNumber\}_000_001.png**" hebben</span><span class="sxs-lookup"><span data-stu-id="7a12d-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="7a12d-126">001 is de reeks van de afbeelding en dit kan 001, 002, 003, 004 of 005 zijn.</span><span class="sxs-lookup"><span data-stu-id="7a12d-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="7a12d-127">Productvariantafbeeldingen moeten de naam "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**" hebben</span><span class="sxs-lookup"><span data-stu-id="7a12d-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="7a12d-128">Een afbeelding uploaden</span><span class="sxs-lookup"><span data-stu-id="7a12d-128">Upload an image</span></span>

<span data-ttu-id="7a12d-129">Volg deze stappen om een afbeelding te uploaden in Site Builder.</span><span class="sxs-lookup"><span data-stu-id="7a12d-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7a12d-130">Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="7a12d-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="7a12d-131">Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="7a12d-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="7a12d-132">Ga in het venster Bestandsverkenner naar een of meer afbeeldingsbestanden die u wilt uploaden en selecteer vervolgens **Openen**</span><span class="sxs-lookup"><span data-stu-id="7a12d-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="7a12d-133">Voer in het dialoogvenster **Media-item uploaden** de vereiste titel en alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="7a12d-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="7a12d-134">Voer een optionele omschrijving en trefwoorden in en selecteer indien gewenst een categorie.</span><span class="sxs-lookup"><span data-stu-id="7a12d-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="7a12d-135">Als u de afbeelding(en) direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in.</span><span class="sxs-lookup"><span data-stu-id="7a12d-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="7a12d-136">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a12d-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="7a12d-137">Een map met afbeeldingen uploaden</span><span class="sxs-lookup"><span data-stu-id="7a12d-137">Upload a folder of images</span></span>

<span data-ttu-id="7a12d-138">Volg deze stappen om een map met afbeeldingen in bulk te uploaden.</span><span class="sxs-lookup"><span data-stu-id="7a12d-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="7a12d-139">Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="7a12d-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="7a12d-140">Selecteer **Uploaden \> Map uploaden** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="7a12d-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="7a12d-141">Ga in het venster Bestandsverkenner naar map die u wilt uploaden en selecteer vervolgens **Openen**</span><span class="sxs-lookup"><span data-stu-id="7a12d-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="7a12d-142">Voer in het dialoogvenster **Media-items uploaden** de optionele trefwoorden in en selecteer indien gewenst een categorie.</span><span class="sxs-lookup"><span data-stu-id="7a12d-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="7a12d-143">Als u de afbeeldingen in de map direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in.</span><span class="sxs-lookup"><span data-stu-id="7a12d-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="7a12d-144">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a12d-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a12d-145">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="7a12d-145">Additional resources</span></span>

[<span data-ttu-id="7a12d-146">Overzicht van digitaal activabeheer</span><span class="sxs-lookup"><span data-stu-id="7a12d-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="7a12d-147">Video uploaden</span><span class="sxs-lookup"><span data-stu-id="7a12d-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="7a12d-148">Bestanden uploaden</span><span class="sxs-lookup"><span data-stu-id="7a12d-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="7a12d-149">Afbeeldingen bijsnijden</span><span class="sxs-lookup"><span data-stu-id="7a12d-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="7a12d-150">Focuspunten van afbeelding aanpassen</span><span class="sxs-lookup"><span data-stu-id="7a12d-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="7a12d-151">Statische bestanden uploaden en verwerken</span><span class="sxs-lookup"><span data-stu-id="7a12d-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]