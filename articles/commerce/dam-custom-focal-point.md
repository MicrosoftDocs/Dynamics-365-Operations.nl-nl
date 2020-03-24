---
title: De focuspunten van de afbeelding aanpassen
description: In dit onderwerp wordt beschreven hoe u de focuspunten van afbeeldingen aanpast in Microsoft Dynamics 365 Commerce Site Builder.
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
ms.openlocfilehash: 2c9bbd51f1fe9a19198a455eedd3ba744d54a165
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096993"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="a81d4-103">De focuspunten van de afbeelding aanpassen</span><span class="sxs-lookup"><span data-stu-id="a81d4-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a81d4-104">In dit onderwerp wordt beschreven hoe u de focuspunten van afbeeldingen aanpast in Microsoft Dynamics 365 Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="a81d4-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="a81d4-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="a81d4-105">Overview</span></span>

<span data-ttu-id="a81d4-106">Wanneer een afbeelding wordt geüpload naar mediabibliotheek in Commerce Site Builder, probeert het systeem het focuspunt van de afbeelding te bepalen.</span><span class="sxs-lookup"><span data-stu-id="a81d4-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="a81d4-107">Als de afbeelding bijvoorbeeld een persoon bevat, wordt het focuspunt door het systeem standaard ingesteld op het gezicht van de persoon.</span><span class="sxs-lookup"><span data-stu-id="a81d4-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="a81d4-108">In de meeste gevallen is het automatisch instellen van een focuspunt geschikt voor alle viewports, maar soms wilt u het focuspunt aanpassen om ervoor te zorgen dat een bepaald deel van de afbeelding altijd zichtbaar is.</span><span class="sxs-lookup"><span data-stu-id="a81d4-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="a81d4-109">Een aangepast focuspunt voor een afbeelding definiëren</span><span class="sxs-lookup"><span data-stu-id="a81d4-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="a81d4-110">Voer de volgende stappen uit om een aangepast focuspunt te definiëren voor een afbeelding.</span><span class="sxs-lookup"><span data-stu-id="a81d4-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="a81d4-111">Selecteer **Mediabibliotheek** in het linkernavigatievenster van Commerce Site Builder.</span><span class="sxs-lookup"><span data-stu-id="a81d4-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="a81d4-112">Selecteer in het hoofdvenster de afbeelding die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a81d4-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="a81d4-113">Selecteer op de opdrachtbalk de optie **Bewerken** om het bestand uit te checken.</span><span class="sxs-lookup"><span data-stu-id="a81d4-113">On the command bar, select **Edit** to check out the file.</span></span>
1. <span data-ttu-id="a81d4-114">Selecteer de afbeelding om de **Bewerkingsmodus** te activeren.</span><span class="sxs-lookup"><span data-stu-id="a81d4-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="a81d4-115">Selecteer onder **Bewerkingsmodus** de optie **Focuspunt wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="a81d4-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="a81d4-116">Er wordt een cirkelvormig focuspunt boven de afbeelding weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="a81d4-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="a81d4-117">Selecteer de focuspuntbesturing om deze over het gewenste focuspunt te bewegen.</span><span class="sxs-lookup"><span data-stu-id="a81d4-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="a81d4-118">Wanneer u klaar bent, selecteert u op de opdrachtbalk de optie **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="a81d4-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a81d4-119">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="a81d4-119">Additional resources</span></span>

[<span data-ttu-id="a81d4-120">Overzicht van digitaal activabeheer</span><span class="sxs-lookup"><span data-stu-id="a81d4-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="a81d4-121">Afbeeldingen uploaden</span><span class="sxs-lookup"><span data-stu-id="a81d4-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="a81d4-122">Video uploaden</span><span class="sxs-lookup"><span data-stu-id="a81d4-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="a81d4-123">Bestanden uploaden</span><span class="sxs-lookup"><span data-stu-id="a81d4-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="a81d4-124">Afbeeldingen bijsnijden</span><span class="sxs-lookup"><span data-stu-id="a81d4-124">Crop images</span></span>](dam-crop-images.md)
