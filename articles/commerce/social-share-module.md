---
title: Module voor sociaal delen
description: In dit onderwerp worden modules voor sociaal delen beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795352"
---
# <a name="social-share-module"></a><span data-ttu-id="91149-103">Module voor sociaal delen</span><span class="sxs-lookup"><span data-stu-id="91149-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91149-104">In dit onderwerp worden modules voor sociaal delen beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91149-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="91149-105">Met modules voor sociaal delen kunnen gebruikers pagina-URL's van e-commerce-sites delen op sociale media, zoals Facebook, Twitter, Pinterest en LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="91149-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="91149-106">URL's van sitepagina's kunnen ook via e-mail worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="91149-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="91149-107">Modules voor sociaal delen worden vaak gebruikt op pagina's met productgegevens om gebruikers te helpen productgegevens te delen.</span><span class="sxs-lookup"><span data-stu-id="91149-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="91149-108">Elke module voor sociaal delen is een container voor modules voor items voor sociaal delen.</span><span class="sxs-lookup"><span data-stu-id="91149-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="91149-109">Elke module voor items voor sociaal delen kan zo worden geconfigureerd dat deze naar een specifieke site voor sociale media verwijst.</span><span class="sxs-lookup"><span data-stu-id="91149-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="91149-110">Integratie met Facebook, Twitter, Pinterest, LinkedIn en e-mail wordt standaard ondersteund.</span><span class="sxs-lookup"><span data-stu-id="91149-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="91149-111">Wanneer een sitegebruiker een symbool voor sociale media selecteert, wordt een HTML-iframe voor de betreffende site voor sociale media gestart.</span><span class="sxs-lookup"><span data-stu-id="91149-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="91149-112">Binnen het iframe kan de gebruiker zich aanmelden en de weergegeven pagina-inhoud publiceren.</span><span class="sxs-lookup"><span data-stu-id="91149-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="91149-113">Op elk platform voor sociale media kunnen cookies worden bijgehouden, dus voor deze module moeten sitegebruikers het cookietoestemmingsbericht accepteren.</span><span class="sxs-lookup"><span data-stu-id="91149-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="91149-114">Wanneer geen toestemming wordt gegeven voor cookies, wordt de module verborgen op de pagina.</span><span class="sxs-lookup"><span data-stu-id="91149-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="91149-115">Zie [Conformiteit van cookie](cookie-compliance.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="91149-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="91149-116">In de volgende afbeelding wordt een voorbeeld van een module voor sociaal delen op een pagina met productgegevens weergegeven.</span><span class="sxs-lookup"><span data-stu-id="91149-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Voorbeeld van een module voor sociaal delen](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="91149-118">Eigenschappen van module voor sociaal delen</span><span class="sxs-lookup"><span data-stu-id="91149-118">Social share module properties</span></span>

| <span data-ttu-id="91149-119">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="91149-119">Property name</span></span>             | <span data-ttu-id="91149-120">Waarde</span><span class="sxs-lookup"><span data-stu-id="91149-120">Value</span></span>                 | <span data-ttu-id="91149-121">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="91149-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="91149-122">Ondertitel</span><span class="sxs-lookup"><span data-stu-id="91149-122">Caption</span></span>                  | <span data-ttu-id="91149-123">Tekst</span><span class="sxs-lookup"><span data-stu-id="91149-123">Text</span></span> | <span data-ttu-id="91149-124">Met deze eigenschap geeft u een bijschrift op voor de module.</span><span class="sxs-lookup"><span data-stu-id="91149-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="91149-125">Afdrukstand</span><span class="sxs-lookup"><span data-stu-id="91149-125">Orientation</span></span> | <span data-ttu-id="91149-126">**Horizontaal** of **Verticaal**</span><span class="sxs-lookup"><span data-stu-id="91149-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="91149-127">Met deze eigenschap wordt de afdrukstand van de indeling voor de sociale media-items bepaald.</span><span class="sxs-lookup"><span data-stu-id="91149-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="91149-128">Eigenschappen van module voor items voor sociaal delen</span><span class="sxs-lookup"><span data-stu-id="91149-128">Social share item module properties</span></span>
| <span data-ttu-id="91149-129">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="91149-129">Property name</span></span>             | <span data-ttu-id="91149-130">Waarde</span><span class="sxs-lookup"><span data-stu-id="91149-130">Value</span></span>                 | <span data-ttu-id="91149-131">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="91149-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="91149-132">Sociale media</span><span class="sxs-lookup"><span data-stu-id="91149-132">Social media</span></span>              | <span data-ttu-id="91149-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span><span class="sxs-lookup"><span data-stu-id="91149-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="91149-134">Een vervolgkeuzemenu met een lijst met sociale-mediaplatforms.</span><span class="sxs-lookup"><span data-stu-id="91149-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="91149-135">Pictogram</span><span class="sxs-lookup"><span data-stu-id="91149-135">Icon</span></span> |<span data-ttu-id="91149-136">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="91149-136">Image</span></span>    | <span data-ttu-id="91149-137">Dit is de afbeelding die voor de respectieve sociale media wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="91149-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="91149-138">Voor elk platform kunt u het beste de SDK van het platform voor sociale media raadplegen voor de aanbevolen afbeelding voor elk platform.</span><span class="sxs-lookup"><span data-stu-id="91149-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="91149-139">Een module voor sociaal delen toevoegen aan een koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="91149-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="91149-140">Ga als volgt te werk om een module voor sociaal delen toe te voegen aan een koopvakmodule.</span><span class="sxs-lookup"><span data-stu-id="91149-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="91149-141">Selecteer op de Fabrikam-site de optie **Pagina's** en selecteer vervolgens de pagina **DefaultPDP** om de pagina met productgegevens te openen.</span><span class="sxs-lookup"><span data-stu-id="91149-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="91149-142">Selecteer het weglatingsteken (**...**) in het vak **Koopvak (vereist)** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="91149-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91149-143">Selecteer in het dialoogvenster **Module toevoegen** de module **Sociaal delen** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="91149-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91149-144">Selecteer het weglatingsteken (**...**) in het vak **Sociaal delen** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="91149-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91149-145">Selecteer in het dialoogvenster **Module toevoegen** de module **SocialShare** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="91149-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91149-146">Selecteer **Horizontaal** in het deelvenster Eigenschappen van de module **SocialShare** onder **Afdrukstand**.</span><span class="sxs-lookup"><span data-stu-id="91149-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="91149-147">Voeg zo nodig een bijschrift toe.</span><span class="sxs-lookup"><span data-stu-id="91149-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="91149-148">Selecteer het weglatingsteken (**...**) in het vak **SocialShare** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="91149-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="91149-149">Selecteer in het dialoogvenster **Module toevoegen** de module **SocialShareItem** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="91149-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="91149-150">Selecteer **Facebook** in het deelvenster Eigenschappen van de module **SocialShareItem** onder **Sociale media**.</span><span class="sxs-lookup"><span data-stu-id="91149-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="91149-151">Selecteer **+ Een afbeelding toevoegen** in het deelvenster Eigenschappen van de module **SocialShareItem** onder **Pictogram**.</span><span class="sxs-lookup"><span data-stu-id="91149-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="91149-152">Selecteer in het dialoogvenster **Mediakiezer** de afbeelding van het Facebook-logo en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="91149-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="91149-153">Als er geen Facebook-logo aanwezig is, selecteert **Nieuw media-item uploaden** om een item te uploaden.</span><span class="sxs-lookup"><span data-stu-id="91149-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="91149-154">Voeg zo nodig extra **SocialShareItem**-modules toe en configureer deze.</span><span class="sxs-lookup"><span data-stu-id="91149-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="91149-155">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="91149-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="91149-156">Op de pagina wordt de module voor sociaal delen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="91149-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="91149-157">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="91149-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91149-158">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="91149-158">Additional resources</span></span>

[<span data-ttu-id="91149-159">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="91149-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="91149-160">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="91149-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="91149-161">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="91149-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]