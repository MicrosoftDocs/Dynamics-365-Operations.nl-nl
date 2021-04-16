---
title: Een favicon toevoegen
description: In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9268bc74a4131256f5a2e88df833104db271b56a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797714"
---
# <a name="add-a-favicon"></a><span data-ttu-id="a1245-103">Een favicon toevoegen</span><span class="sxs-lookup"><span data-stu-id="a1245-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1245-104">In dit onderwerp wordt uitgelegd hoe u een favicon aan uw site toevoegt.</span><span class="sxs-lookup"><span data-stu-id="a1245-104">This topic explains how to add a favicon to your site.</span></span>

<span data-ttu-id="a1245-105">Een favicon is een klein grafisch bestand dat onder andere wordt weergegeven op het tabblad van de webbrowser, in de adresbalk, de browsergeschiedenis en in bladwijzers of favorieten.</span><span class="sxs-lookup"><span data-stu-id="a1245-105">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="a1245-106">Het is raadzaam om een favicon aan uw site toe te voegen, omdat deze uw merk vertegenwoordigt en benadrukt. Zo onderscheidt uw site zich van andere sites die uw klant bezoekt.</span><span class="sxs-lookup"><span data-stu-id="a1245-106">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="a1245-107">Hoewel u meerdere favicons van verschillende grootten en bestandstypen kunt toevoegen aan uw site, wordt in dit onderwerp aangegeven hoe u één favicon toevoegt.</span><span class="sxs-lookup"><span data-stu-id="a1245-107">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="a1245-108">Hetzelfde proces en dezelfde locatie worden echter gebruikt om meer favicons toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="a1245-108">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="a1245-109">Een favicon uploaden naar de verzameling met assets voor uw site</span><span class="sxs-lookup"><span data-stu-id="a1245-109">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="a1245-110">Volg deze stappen om een favicon te uploaden naar de verzameling met assets voor uw site.</span><span class="sxs-lookup"><span data-stu-id="a1245-110">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="a1245-111">Selecteer **Mediabibliotheek** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="a1245-111">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="a1245-112">Selecteer **Uploaden \> Media-items uploaden** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="a1245-112">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="a1245-113">Blader in de bestandsverkenner naar het favicon-afbeeldingsbestand dat u wilt uploaden, selecteer het en selecteer vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="a1245-113">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="a1245-114">Voer in het dialoogvenster **Media-item uploaden** de vereiste titel en alternatieve tekst in.</span><span class="sxs-lookup"><span data-stu-id="a1245-114">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="a1245-115">Als u de afbeelding direct na het uploaden wilt publiceren, schakelt u het selectievakje **Media-items publiceren na uploaden** in.</span><span class="sxs-lookup"><span data-stu-id="a1245-115">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a1245-116">Als u niet de optie **Media-items publiceren na uploaden** selecteert, moet u teruggaan naar de pagina **Media-items** en de favicon later handmatig publiceren.</span><span class="sxs-lookup"><span data-stu-id="a1245-116">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="a1245-117">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1245-117">Select **OK**.</span></span>
1. <span data-ttu-id="a1245-118">Kopieer in het eigenschappenvenster aan de rechterkant de openbare URL van de favicon.</span><span class="sxs-lookup"><span data-stu-id="a1245-118">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="a1245-119">U gebruikt deze URL later.</span><span class="sxs-lookup"><span data-stu-id="a1245-119">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="a1245-120">De HTML voor uw favicon maken</span><span class="sxs-lookup"><span data-stu-id="a1245-120">Create the HTML for your favicon</span></span>

<span data-ttu-id="a1245-121">Gebruik de volgende HTML-tekenreeks om de HTML voor de favicon te maken.</span><span class="sxs-lookup"><span data-stu-id="a1245-121">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="a1245-122">Vervang voor het kenmerk **href** de **Openbare\_URL\_voor\_uw\_favicon** door de openbare URL die u eerder hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="a1245-122">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="a1245-123">Een fragment maken dat een metatag bevat voor uw favicon</span><span class="sxs-lookup"><span data-stu-id="a1245-123">Create a fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="a1245-124">Als u een fragment wilt maken dat een metatag bevat voor uw favicon, voert u deze stappen uit.</span><span class="sxs-lookup"><span data-stu-id="a1245-124">To create a fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="a1245-125">Ga naar **Fragmenten** en selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a1245-125">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="a1245-126">Selecteer in het dialoogvenster **Nieuw fragment** de optie **Metatags** als de module waarop het fragment is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="a1245-126">In the **New fragment** dialog box, select **Metatags** as the module that the fragment is based on.</span></span>
1. <span data-ttu-id="a1245-127">Voer een naam in voor het fragment en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1245-127">Enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="a1245-128">Selecteer in de structuur van de fragmenthiërarchie de onderliggende waarde **Standaard metatags**.</span><span class="sxs-lookup"><span data-stu-id="a1245-128">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="a1245-129">Selecteer in het rechterdeelvenster onder **Metatags** de optie **Toevoegen** en voer vervolgens de HTML-reeks in die u eerder voor de favicon hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a1245-129">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="a1245-130">Selecteer **Bewerken voltooien** en **Publiceren** om het fragment te publiceren.</span><span class="sxs-lookup"><span data-stu-id="a1245-130">Select **Finish editing**, and then select **Publish** to publish the fragment.</span></span>

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="a1245-131">Het metatagfragment toevoegen aan de HTML-sectie head van uw pagina's</span><span class="sxs-lookup"><span data-stu-id="a1245-131">Add the metatag fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="a1245-132">Als u het metatagfragment wilt toevoegen aan de HTML-sectie **head** van uw pagina's, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="a1245-132">To add the metatag fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="a1245-133">Ga naar **Sjablonen**, open de sjabloon voor de pagina's waaraan u uw favicon wilt toevoegen en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="a1245-133">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="a1245-134">Selecteer in de sjabloonhiërarchiestructuur de knop met het weglatingsteken (**...**) rechts van de container **HTML-kop** en selecteer **Fragment toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a1245-134">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add fragment**.</span></span>
1. <span data-ttu-id="a1245-135">Selecteer in het dialoogvenster **Fragment selecteren** het metatagfragment dat u eerder hebt gemaakt, voer een naam in voor het paginafragment en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a1245-135">In the **Select fragment** dialog box, select the metatag fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="a1245-136">Selecteer **Bewerken voltooien** en **Publiceren** om de sjabloon te publiceren.</span><span class="sxs-lookup"><span data-stu-id="a1245-136">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="a1245-137">Als op uw site meerdere sjablonen worden gebruikt, moet u het metatagfragment aan al deze sjablonen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a1245-137">If your site uses more than one template, you must add the metatags fragment to all of them.</span></span>

<span data-ttu-id="a1245-138">Wanneer u een voorbeeld bekijkt van pagina's die zijn gebaseerd op de sjabloon waaraan u het metatagfragment hebt toegevoegd, ziet u nu de favicon op het browsertabblad.</span><span class="sxs-lookup"><span data-stu-id="a1245-138">When you preview pages that are based on the template that you added the metatags fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1245-139">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="a1245-139">Additional resources</span></span>

[<span data-ttu-id="a1245-140">Een logo toevoegen</span><span class="sxs-lookup"><span data-stu-id="a1245-140">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="a1245-141">Selecteer een thema voor de site</span><span class="sxs-lookup"><span data-stu-id="a1245-141">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="a1245-142">Werken met CSS-overschrijvingsbestanden</span><span class="sxs-lookup"><span data-stu-id="a1245-142">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="a1245-143">Een welkomstbericht toevoegen</span><span class="sxs-lookup"><span data-stu-id="a1245-143">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="a1245-144">Een auteursrechtmelding toevoegen</span><span class="sxs-lookup"><span data-stu-id="a1245-144">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="a1245-145">Talen toevoegen aan uw site</span><span class="sxs-lookup"><span data-stu-id="a1245-145">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="a1245-146">Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie</span><span class="sxs-lookup"><span data-stu-id="a1245-146">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
