---
title: Module voor sociaal delen
description: In dit onderwerp worden modules voor sociaal delen beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 510ca8b14d8b5334e50aca1b15d636c65fcc9888
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4411507"
---
# <a name="social-share-module"></a><span data-ttu-id="f659e-103">Module voor sociaal delen</span><span class="sxs-lookup"><span data-stu-id="f659e-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f659e-104">In dit onderwerp worden modules voor sociaal delen beschreven en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f659e-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f659e-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="f659e-105">Overview</span></span>

<span data-ttu-id="f659e-106">Met modules voor sociaal delen kunnen gebruikers pagina-URL's van e-commerce-sites delen op sociale media, zoals Facebook, Twitter, Pinterest en LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="f659e-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="f659e-107">URL's van sitepagina's kunnen ook via e-mail worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="f659e-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="f659e-108">Modules voor sociaal delen worden vaak gebruikt op pagina's met productgegevens om gebruikers te helpen productgegevens te delen.</span><span class="sxs-lookup"><span data-stu-id="f659e-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="f659e-109">Elke module voor sociaal delen is een container voor modules voor items voor sociaal delen.</span><span class="sxs-lookup"><span data-stu-id="f659e-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="f659e-110">Elke module voor items voor sociaal delen kan zo worden geconfigureerd dat deze naar een specifieke site voor sociale media verwijst.</span><span class="sxs-lookup"><span data-stu-id="f659e-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="f659e-111">Integratie met Facebook, Twitter, Pinterest, LinkedIn en e-mail wordt standaard ondersteund.</span><span class="sxs-lookup"><span data-stu-id="f659e-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="f659e-112">Wanneer een sitegebruiker een symbool voor sociale media selecteert, wordt een HTML-iframe voor de betreffende site voor sociale media gestart.</span><span class="sxs-lookup"><span data-stu-id="f659e-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="f659e-113">Binnen het iframe kan de gebruiker zich aanmelden en de weergegeven pagina-inhoud publiceren.</span><span class="sxs-lookup"><span data-stu-id="f659e-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="f659e-114">Op elk platform voor sociale media kunnen cookies worden bijgehouden, dus voor deze module moeten sitegebruikers het cookietoestemmingsbericht accepteren.</span><span class="sxs-lookup"><span data-stu-id="f659e-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="f659e-115">Wanneer geen toestemming wordt gegeven voor cookies, wordt de module verborgen op de pagina.</span><span class="sxs-lookup"><span data-stu-id="f659e-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="f659e-116">Zie [Conformiteit van cookie](cookie-compliance.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f659e-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="f659e-117">In de volgende afbeelding wordt een voorbeeld van een module voor sociaal delen op een pagina met productgegevens weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f659e-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Voorbeeld van een module voor sociaal delen](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="f659e-119">Eigenschappen van module voor sociaal delen</span><span class="sxs-lookup"><span data-stu-id="f659e-119">Social share module properties</span></span>

| <span data-ttu-id="f659e-120">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="f659e-120">Property name</span></span>             | <span data-ttu-id="f659e-121">Waarde</span><span class="sxs-lookup"><span data-stu-id="f659e-121">Value</span></span>                 | <span data-ttu-id="f659e-122">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f659e-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f659e-123">Ondertitel</span><span class="sxs-lookup"><span data-stu-id="f659e-123">Caption</span></span>                  | <span data-ttu-id="f659e-124">Tekst</span><span class="sxs-lookup"><span data-stu-id="f659e-124">Text</span></span> | <span data-ttu-id="f659e-125">Met deze eigenschap geeft u een bijschrift op voor de module.</span><span class="sxs-lookup"><span data-stu-id="f659e-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="f659e-126">Afdrukstand</span><span class="sxs-lookup"><span data-stu-id="f659e-126">Orientation</span></span> | <span data-ttu-id="f659e-127">**Horizontaal** of **Verticaal**</span><span class="sxs-lookup"><span data-stu-id="f659e-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="f659e-128">Met deze eigenschap wordt de afdrukstand van de indeling voor de sociale media-items bepaald.</span><span class="sxs-lookup"><span data-stu-id="f659e-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="f659e-129">Eigenschappen van module voor items voor sociaal delen</span><span class="sxs-lookup"><span data-stu-id="f659e-129">Social share item module properties</span></span>
| <span data-ttu-id="f659e-130">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="f659e-130">Property name</span></span>             | <span data-ttu-id="f659e-131">Waarde</span><span class="sxs-lookup"><span data-stu-id="f659e-131">Value</span></span>                 | <span data-ttu-id="f659e-132">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f659e-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f659e-133">Sociale media</span><span class="sxs-lookup"><span data-stu-id="f659e-133">Social media</span></span>              | <span data-ttu-id="f659e-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span><span class="sxs-lookup"><span data-stu-id="f659e-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="f659e-135">Een vervolgkeuzemenu met een lijst met sociale-mediaplatforms.</span><span class="sxs-lookup"><span data-stu-id="f659e-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="f659e-136">Pictogram</span><span class="sxs-lookup"><span data-stu-id="f659e-136">Icon</span></span> |<span data-ttu-id="f659e-137">Afbeelding</span><span class="sxs-lookup"><span data-stu-id="f659e-137">Image</span></span>    | <span data-ttu-id="f659e-138">Dit is de afbeelding die voor de respectieve sociale media wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f659e-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="f659e-139">Voor elk platform kunt u het beste de SDK van het platform voor sociale media raadplegen voor de aanbevolen afbeelding voor elk platform.</span><span class="sxs-lookup"><span data-stu-id="f659e-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="f659e-140">Een module voor sociaal delen toevoegen aan een koopvakmodule</span><span class="sxs-lookup"><span data-stu-id="f659e-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="f659e-141">Ga als volgt te werk om een module voor sociaal delen toe te voegen aan een koopvakmodule.</span><span class="sxs-lookup"><span data-stu-id="f659e-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="f659e-142">Selecteer op de Fabrikam-site de optie **Pagina's** en selecteer vervolgens de pagina **DefaultPDP** om de pagina met productgegevens te openen.</span><span class="sxs-lookup"><span data-stu-id="f659e-142">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="f659e-143">Selecteer het weglatingsteken (**...**) in het vak **Koopvak (vereist)** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f659e-143">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f659e-144">Selecteer in het dialoogvenster **Module toevoegen** de module **Sociaal delen** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f659e-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f659e-145">Selecteer het weglatingsteken (**...**) in het vak **Sociaal delen** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f659e-145">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f659e-146">Selecteer in het dialoogvenster **Module toevoegen** de module **SocialShare** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f659e-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f659e-147">Selecteer **Horizontaal** in het deelvenster Eigenschappen van de module **SocialShare** onder **Afdrukstand**.</span><span class="sxs-lookup"><span data-stu-id="f659e-147">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="f659e-148">Voeg zo nodig een bijschrift toe.</span><span class="sxs-lookup"><span data-stu-id="f659e-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="f659e-149">Selecteer het weglatingsteken (**...**) in het vak **SocialShare** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f659e-149">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f659e-150">Selecteer in het dialoogvenster **Module toevoegen** de module **SocialShareItem** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f659e-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f659e-151">Selecteer **Facebook** in het deelvenster Eigenschappen van de module **SocialShareItem** onder **Sociale media**.</span><span class="sxs-lookup"><span data-stu-id="f659e-151">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="f659e-152">Selecteer **+ Een afbeelding toevoegen** in het deelvenster Eigenschappen van de module **SocialShareItem** onder **Pictogram**.</span><span class="sxs-lookup"><span data-stu-id="f659e-152">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="f659e-153">Selecteer in het dialoogvenster **Mediakiezer** de afbeelding van het Facebook-logo en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="f659e-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="f659e-154">Als er geen Facebook-logo aanwezig is, selecteert **Nieuw media-item uploaden** om een item te uploaden.</span><span class="sxs-lookup"><span data-stu-id="f659e-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="f659e-155">Voeg zo nodig extra **SocialShareItem**-modules toe en configureer deze.</span><span class="sxs-lookup"><span data-stu-id="f659e-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="f659e-156">Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.</span><span class="sxs-lookup"><span data-stu-id="f659e-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f659e-157">Op de pagina wordt de module voor sociaal delen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f659e-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="f659e-158">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="f659e-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f659e-159">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="f659e-159">Additional resources</span></span>

[<span data-ttu-id="f659e-160">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="f659e-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f659e-161">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="f659e-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f659e-162">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="f659e-162">Cookie compliance</span></span>](cookie-compliance.md)
