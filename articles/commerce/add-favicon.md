---
title: Een favicon toevoegen
description: In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.
author: bicyclingfool
manager: annbe
ms.date: 04/27/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2d95e8b799c3b89418657342868e0ec7e94a86f9
ms.sourcegitcommit: ce79fb570e299a26a644e29da7ceb5a57a1374e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2020
ms.locfileid: "3295075"
---
# <a name="add-a-favicon"></a><span data-ttu-id="572f4-103">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="572f4-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="572f4-104">In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.</span><span class="sxs-lookup"><span data-stu-id="572f4-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="572f4-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="572f4-105">Overview</span></span>

<span data-ttu-id="572f4-106">Een favicon is een klein grafisch bestand dat onder andere wordt weergegeven op het tabblad van de webbrowser, in de adresbalk, de browsergeschiedenis en in bladwijzers of favorieten.</span><span class="sxs-lookup"><span data-stu-id="572f4-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="572f4-107">Het is raadzaam om een favicon aan uw site toe te voegen, omdat deze uw merk vertegenwoordigt en benadrukt. Zo onderscheidt uw site zich van andere sites die uw klant bezoekt.</span><span class="sxs-lookup"><span data-stu-id="572f4-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="572f4-108">Hoewel u meerdere favicons van verschillende grootten en bestandstypen kunt toevoegen aan uw site, wordt in dit onderwerp aangegeven hoe u één favicon toevoegt.</span><span class="sxs-lookup"><span data-stu-id="572f4-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="572f4-109">Hetzelfde proces en dezelfde locatie worden echter gebruikt om meer favicons toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="572f4-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="572f4-110">Een favicon uploaden naar de verzameling met assets voor uw site</span><span class="sxs-lookup"><span data-stu-id="572f4-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="572f4-111">Volg deze stappen om een favicon te uploaden naar de verzameling met assets voor uw site.</span><span class="sxs-lookup"><span data-stu-id="572f4-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="572f4-112">Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="572f4-112">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="572f4-113">Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="572f4-113">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="572f4-114">Blader in de bestandsverkenner naar het favicon-afbeeldingsbestand dat u wilt uploaden, selecteer het en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="572f4-114">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="572f4-115">Voer in het dialoogvenster **Media-item uploaden** de vereiste titel en alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="572f4-115">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="572f4-116">Als u de afbeelding direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in.</span><span class="sxs-lookup"><span data-stu-id="572f4-116">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="572f4-117">Als u niet de optie **Media-items publiceren na uploaden** selecteert, moet u teruggaan naar de pagina **Media-items** en de favicon later handmatig publiceren.</span><span class="sxs-lookup"><span data-stu-id="572f4-117">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="572f4-118">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="572f4-118">Select **OK**.</span></span>
1. <span data-ttu-id="572f4-119">Kopieer in het eigenschappenvenster aan de rechterkant de openbare URL van de favicon.</span><span class="sxs-lookup"><span data-stu-id="572f4-119">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="572f4-120">U gebruikt deze URL later.</span><span class="sxs-lookup"><span data-stu-id="572f4-120">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="572f4-121">De HTML voor uw favicon maken</span><span class="sxs-lookup"><span data-stu-id="572f4-121">Create the HTML for your favicon</span></span>

<span data-ttu-id="572f4-122">Gebruik de volgende HTML-tekenreeks om de HTML voor de favicon te maken.</span><span class="sxs-lookup"><span data-stu-id="572f4-122">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="572f4-123">Vervang voor het kenmerk **href** de **Openbare\_URL\_voor\_uw\_favicon** door de openbare URL die u eerder hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="572f4-123">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-page-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="572f4-124">Een paginafragment maken dat een metatag bevat voor uw favicon</span><span class="sxs-lookup"><span data-stu-id="572f4-124">Create a page fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="572f4-125">Als u een paginafragment wilt maken dat een metatag bevat voor uw favicon, voert u deze stappen uit.</span><span class="sxs-lookup"><span data-stu-id="572f4-125">To create a page fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="572f4-126">Ga naar **Paginafragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="572f4-126">Go to **Page fragments**, and select **New**.</span></span>
1. <span data-ttu-id="572f4-127">Selecteer in het dialoogvenster **Nieuw paginafragment** de optie **Metatags** als de module waarop het paginafragment is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="572f4-127">In the **New Page Fragment** dialog box, select **Metatags** as the module that the page fragment is based on.</span></span>
1. <span data-ttu-id="572f4-128">Voer een naam in voor het paginafragment en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="572f4-128">Enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="572f4-129">Selecteer in de structuur van de fragmenthiërarchie de onderliggende waarde **Standaard metatags**.</span><span class="sxs-lookup"><span data-stu-id="572f4-129">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="572f4-130">Selecteer in het rechterdeelvenster onder **Metatags** de optie **Toevoegen** en voer vervolgens de HTML-reeks in die u eerder voor de favicon hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="572f4-130">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="572f4-131">Selecteer **Bewerken voltooien** en **Publiceren** om het paginafragment te publiceren.</span><span class="sxs-lookup"><span data-stu-id="572f4-131">Select **Finish editing**, and then select **Publish** to publish the page fragment.</span></span>

## <a name="add-the-metatag-page-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="572f4-132">Het metatag-paginafragment toevoegen aan de HTML-kopsectie van uw pagina's</span><span class="sxs-lookup"><span data-stu-id="572f4-132">Add the metatag page fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="572f4-133">Als u het metatag-paginafragment wilt toevoegen aan de HTML-**kop**sectie van uw pagina's, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="572f4-133">To add the metatag page fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="572f4-134">Ga naar **Sjablonen**, open de sjabloon voor de pagina's waaraan u uw favicon wilt toevoegen en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="572f4-134">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="572f4-135">Selecteer in de sjabloonhiërarchiestructuur de knop met het weglatingsteken (**...**) rechts van de container **HTML-kop** en selecteer **Paginafragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="572f4-135">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add page fragment**.</span></span>
1. <span data-ttu-id="572f4-136">Selecteer in het dialoogvenster **Nieuw paginafragment selecteren** het metatag-paginafragment dat u eerder hebt gemaakt, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="572f4-136">In the **Select Page Fragment** dialog box, select the metatag page fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="572f4-137">Selecteer **Bewerken voltooien** en **Publiceren** om de sjabloon te publiceren.</span><span class="sxs-lookup"><span data-stu-id="572f4-137">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="572f4-138">Als op uw site meerdere sjablonen worden gebruikt, moet u het metatag-paginafragment aan al deze sjablonen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="572f4-138">If your site uses more than one template, you must add the metatags page fragment to all of them.</span></span>

<span data-ttu-id="572f4-139">Wanneer u een voorbeeld bekijkt van pagina's die zijn gebaseerd op de sjabloon waaraan u het metatag-paginafragment hebt toegevoegd, ziet u nu de favicon op het browsertabblad.</span><span class="sxs-lookup"><span data-stu-id="572f4-139">When you preview pages that are based on the template that you added the metatags page fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="572f4-140">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="572f4-140">Additional resources</span></span>

[<span data-ttu-id="572f4-141">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="572f4-141">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="572f4-142">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="572f4-142">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="572f4-143">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="572f4-143">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="572f4-144">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="572f4-144">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="572f4-145">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="572f4-145">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="572f4-146">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="572f4-146">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="572f4-147">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="572f4-147">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

