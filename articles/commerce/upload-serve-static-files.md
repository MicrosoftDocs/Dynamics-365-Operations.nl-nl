---
title: Statische bestanden uploaden en verwerken
description: In dit onderwerp wordt beschreven hoe u een statisch bestand uploadt in Microsoft Dynamics 365 Commerce Site Builder en hoe u een aangepaste URL en bestandsnaam maakt die u kunt gebruiken om dat bestand aan te vragen.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: aba9dde2ed9d5fa09e92fcdd784a53f208930eda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211014"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="e4a57-103">Statische bestanden uploaden en verwerken</span><span class="sxs-lookup"><span data-stu-id="e4a57-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4a57-104">In dit onderwerp wordt beschreven hoe u een statisch bestand uploadt in Microsoft Dynamics 365 Commerce Site Builder en hoe u een aangepaste URL en bestandsnaam maakt die u kunt gebruiken om dat bestand aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="e4a57-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="e4a57-105">Voor sommige connectors van derden moet een bestand worden gehost en vanaf de e-commerce site worden aangeboden.</span><span class="sxs-lookup"><span data-stu-id="e4a57-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="e4a57-106">Deze connectors verwachten dat het bestand wordt geretourneerd door verzoeken naar een specifiek callback URL-pad en bestandsnaam.</span><span class="sxs-lookup"><span data-stu-id="e4a57-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="e4a57-107">Daarom wordt in dit onderwerp uitgelegd hoe u een statisch bestand kunt uploaden en bedienen met een door de gebruiker te definiëren URL en bestandsnaam op een Dynamics 365 Commerce e-commercesite.</span><span class="sxs-lookup"><span data-stu-id="e4a57-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="e4a57-108">Een site-URL maken die een statisch bestand retourneert</span><span class="sxs-lookup"><span data-stu-id="e4a57-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="e4a57-109">Voer de volgende stappen uit om een site-URL te maken die een statisch bestand retourneert in Commerce site builder.</span><span class="sxs-lookup"><span data-stu-id="e4a57-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e4a57-110">Ga naar de Mediabibliotheek van uw site en upload het bestand dat moet worden geleverd door verzoeken naar de URL die u gaat definiëren.</span><span class="sxs-lookup"><span data-stu-id="e4a57-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="e4a57-111">Als u het bestand al hebt geüpload, kunt u deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="e4a57-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="e4a57-112">Ga naar **URL's** voor uw site.</span><span class="sxs-lookup"><span data-stu-id="e4a57-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="e4a57-113">Selecteer **Nieuw \> Nieuwe URL**.</span><span class="sxs-lookup"><span data-stu-id="e4a57-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="e4a57-114">Selecteer in het dialoogvenster **Nieuwe URL** de optie **Mediabibliotheekmaterialen**.</span><span class="sxs-lookup"><span data-stu-id="e4a57-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="e4a57-115">Voer in het veld **URL-pad** het URL-pad in.</span><span class="sxs-lookup"><span data-stu-id="e4a57-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="e4a57-116">Neem de bestandsnaam op in het pad.</span><span class="sxs-lookup"><span data-stu-id="e4a57-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="e4a57-117">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="e4a57-117">Select **Next**.</span></span> <span data-ttu-id="e4a57-118">De Mediabibliotheek wordt geopend en toont alle mediamaterialen van het type **document** dat is geüpload.</span><span class="sxs-lookup"><span data-stu-id="e4a57-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="e4a57-119">Selecteer het bestand dat moet worden geleverd voor verzoeken naar de URL die u in stap 5 hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="e4a57-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="e4a57-120">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e4a57-120">Select **Save**.</span></span>

<span data-ttu-id="e4a57-121">Op dit moment bevindt de URL die u hebt gemaakt zich in een conceptstatus.</span><span class="sxs-lookup"><span data-stu-id="e4a57-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="e4a57-122">Het bestand waarnaar de URL verwijst, wordt niet geretourneerd totdat u de URL publiceert.</span><span class="sxs-lookup"><span data-stu-id="e4a57-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="e4a57-123">Voordat u de URL publiceert, kunt u valideren of de juiste gegevens worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e4a57-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="e4a57-124">Een URL valideren en publiceren</span><span class="sxs-lookup"><span data-stu-id="e4a57-124">Validate and publish a URL</span></span>

<span data-ttu-id="e4a57-125">Ga als volgt te werk om een URL te valideren voordat u deze publiceert.</span><span class="sxs-lookup"><span data-stu-id="e4a57-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="e4a57-126">Ga naar **URL's** voor uw site en selecteer de URL die u wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="e4a57-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="e4a57-127">Selecteer in het deelvenster Eigenschappen rechtsonder via de knop **Bewerken** de juiste URL-koppeling.</span><span class="sxs-lookup"><span data-stu-id="e4a57-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="e4a57-128">Er wordt een nieuw browservenster geopend en er wordt een 404-fout weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e4a57-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="e4a57-129">Voeg de **?preview=inprogress**-query reeks toe aan de URL (bijvoorbeeld `https://yoursite.com/callback.html?preview=inprogress`) en laad de pagina opnieuw.</span><span class="sxs-lookup"><span data-stu-id="e4a57-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="e4a57-130">Het bestand dat u naar de Mediabibliotheek hebt geüpload, moet in het antwoord zijn geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e4a57-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="e4a57-131">Nadat u de URL hebt gevalideerd, kunt u deze publiceren.</span><span class="sxs-lookup"><span data-stu-id="e4a57-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="e4a57-132">Ga naar **URL's** voor uw site en selecteer de URL.</span><span class="sxs-lookup"><span data-stu-id="e4a57-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="e4a57-133">Selecteer **Publiceren** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="e4a57-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="e4a57-134">Het bestand bijwerken waarnaar een URL verwijst</span><span class="sxs-lookup"><span data-stu-id="e4a57-134">Update the file that a URL points to</span></span>

<span data-ttu-id="e4a57-135">Nadat een URL is gepubliceerd, kunt u deze bijwerken zodat deze naar een ander bestand verwijst.</span><span class="sxs-lookup"><span data-stu-id="e4a57-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="e4a57-136">U kunt de URL ook bijwerken, zodat deze verwijst naar een ander type bron, zoals wordt beschreven in de volgende sectie.</span><span class="sxs-lookup"><span data-stu-id="e4a57-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="e4a57-137">U kunt bijvoorbeeld de URL naar een interne pagina of een omleiding verwijzen.</span><span class="sxs-lookup"><span data-stu-id="e4a57-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="e4a57-138">Voer de volgende stappen uit om het bestand bij te werken waarnaar een URL verwijst:</span><span class="sxs-lookup"><span data-stu-id="e4a57-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="e4a57-139">Ga naar **URL's** voor uw site en selecteer de URL die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e4a57-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="e4a57-140">Selecteer **Bewerken** in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="e4a57-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="e4a57-141">Selecteer onder **URL-toewijzing** het vak **Stap 2** en selecteer vervolgens een nieuw document in de Mediabibliotheek.</span><span class="sxs-lookup"><span data-stu-id="e4a57-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="e4a57-142">Selecteer **Toepassing**.</span><span class="sxs-lookup"><span data-stu-id="e4a57-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="e4a57-143">Het materiaaltype bijwerken waarnaar een URL verwijst</span><span class="sxs-lookup"><span data-stu-id="e4a57-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="e4a57-144">U kunt ook een URL bijwerken zodat deze naar een ander type materiaal (resource) verwijst, zoals een interne pagina of een omleiding.</span><span class="sxs-lookup"><span data-stu-id="e4a57-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="e4a57-145">Voer de volgende stappen uit om het materiaaltype bij te werken waarnaar een URL verwijst:</span><span class="sxs-lookup"><span data-stu-id="e4a57-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="e4a57-146">Ga naar **URL's** voor uw site en selecteer de URL die u wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="e4a57-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="e4a57-147">Selecteer **Bewerken** in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="e4a57-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="e4a57-148">Selecteer onder **URL-toewijzing** onder **Stap 1** een ander materiaaltype.</span><span class="sxs-lookup"><span data-stu-id="e4a57-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="e4a57-149">Selecteer het vak **Stap 2** en selecteer vervolgens het nieuwe materiaal.</span><span class="sxs-lookup"><span data-stu-id="e4a57-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="e4a57-150">Selecteer **Toepassing**.</span><span class="sxs-lookup"><span data-stu-id="e4a57-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="e4a57-151">Het URL-pad wijzigen</span><span class="sxs-lookup"><span data-stu-id="e4a57-151">Change the URL path</span></span>

<span data-ttu-id="e4a57-152">Nadat een URL is gemaakt, kan het pad ervan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="e4a57-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="e4a57-153">Als u het URL-pad moet wijzigen dat een bestand of een ander type bron bevat, moet u een nieuwe URL maken, deze toewijzen aan het bestaande bestand of een andere bron, en vervolgens de publicatie ongedaan maken en de oude URL verwijderen.</span><span class="sxs-lookup"><span data-stu-id="e4a57-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="e4a57-154">Als u het URL-pad wilt wijzigen, volgt u deze stappen.</span><span class="sxs-lookup"><span data-stu-id="e4a57-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="e4a57-155">Als u een nieuwe URL wilt maken en toewijzen aan het bestaande bestand of een andere bron, volgt u de instructies in de sectie [Een site-URL maken die een statisch bestand retourneert](#create-a-site-url-that-returns-a-static-file) eerder in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="e4a57-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="e4a57-156">Selecteer de nieuwe URL en selecteer **Publiceren** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="e4a57-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="e4a57-157">De nieuwe URL wordt gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="e4a57-157">The new URL is published.</span></span>
1. <span data-ttu-id="e4a57-158">Als u de publicatie van de oude URL ongedaan wilt maken, selecteert u de URL en selecteert u vervolgens **Publicatie ongedaan maken** in de opdrachtbalk.</span><span class="sxs-lookup"><span data-stu-id="e4a57-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="e4a57-159">U kunt nu de oude URL verwijderen als u wilt.</span><span class="sxs-lookup"><span data-stu-id="e4a57-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4a57-160">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e4a57-160">Additional resources</span></span>

[<span data-ttu-id="e4a57-161">Overzicht van digitaal activabeheer</span><span class="sxs-lookup"><span data-stu-id="e4a57-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="e4a57-162">Afbeeldingen uploaden</span><span class="sxs-lookup"><span data-stu-id="e4a57-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="e4a57-163">Video's uploaden</span><span class="sxs-lookup"><span data-stu-id="e4a57-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="e4a57-164">Andere bestanden uploaden dan afbeeldingen en video's</span><span class="sxs-lookup"><span data-stu-id="e4a57-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="e4a57-165">Afbeeldingen bijsnijden</span><span class="sxs-lookup"><span data-stu-id="e4a57-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="e4a57-166">Focuspunten van afbeelding aanpassen</span><span class="sxs-lookup"><span data-stu-id="e4a57-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]