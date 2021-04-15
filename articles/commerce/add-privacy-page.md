---
title: Een pagina met het privacybeleid toevoegen
description: In dit onderwerp wordt beschreven hoe u een pagina met het privacybeleid toevoegt in Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797522"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="3d0c5-103">Een pagina met het privacybeleid toevoegen</span><span class="sxs-lookup"><span data-stu-id="3d0c5-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d0c5-104">In dit onderwerp wordt beschreven hoe u een pagina met het privacybeleid toevoegt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3d0c5-105">Naleving van de privacy omvat organisatorische maatregelen die sitegebruikers informeren over hoe hun gegevens worden verzameld en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="3d0c5-106">Gebruikers kunnen vervolgens beslissen hoe ze willen dat hun persoonlijke gegevens worden verwerkt en kunnen passende maatregelen nemen.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="3d0c5-107">De privacyverklaring van Microsoft in Dynamics 365 Commerce bekijken</span><span class="sxs-lookup"><span data-stu-id="3d0c5-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="3d0c5-108">Als u de privacyverklaring van Microsoft wilt bekijken terwijl u bent aangemeld bij de Dynamics 365 Commerce-ontwerpfuncties, selecteert u de knop **Help** (**?**) in de rechterbovenhoek en selecteert u vervolgens **Privacy en cookies**.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="3d0c5-109">Er wordt een nieuw tabblad geopend met een koppeling naar de [privacyverklaring van Microsoft](https://privacy.microsoft.com/privacystatement).</span><span class="sxs-lookup"><span data-stu-id="3d0c5-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="3d0c5-110">Een pagina met het privacybeleid maken voor uw site</span><span class="sxs-lookup"><span data-stu-id="3d0c5-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="3d0c5-111">In Dynamics 365 Commerce zijn er verschillende manieren om gebruikers van uw site toegang te geven tot uw privacybeleid.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="3d0c5-112">In deze sectie wordt beschreven hoe u een pagina met het privacybeleid maakt en hier vervolgens naar verwijst met een voettekstfragment.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="3d0c5-113">Middels een voorbeeld wordt hieronder beschreven hoe u een algemene pagina voor het privacybeleid voor een Commerce-site bouwt.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="3d0c5-114">U bent verantwoordelijk voor het ontwerpen en implementeren van een oplossing voor een privacybeleidspagina die het beste voldoet aan de wettelijke vereisten van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="3d0c5-115">Ga om te beginnen in de ontwerphulpmiddelen naar de site waarvoor u een privacybeleidspagina wilt maken.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="3d0c5-116">Een sjabloon maken</span><span class="sxs-lookup"><span data-stu-id="3d0c5-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="3d0c5-117">Als er al een sjabloon is gemaakt die kan worden gebruikt voor de privacybeleidspagina, gaat u verder naar de sectie [Een privacybeleidspagina maken](#build-a-privacy-policy-page).</span><span class="sxs-lookup"><span data-stu-id="3d0c5-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="3d0c5-118">Volg deze stappen om een sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="3d0c5-119">Ga naar **Sjablonen** en selecteer **Nieuw** om een paginasjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="3d0c5-120">Voer in het dialoogvenster **Nieuwe sjabloon** onder **Sjabloonnaam** **Sjabloon voor promobanner** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="3d0c5-121">Voeg in de sjabloon alle vereiste modules toe aan de vereiste paginavakken.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="3d0c5-122">Beweeg de muisaanwijzer over de rode uitroeptekens voor hulp.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="3d0c5-123">(Het vak **HTML-kop** kan bijvoorbeeld een module **Standaard extern script** vereisen.)</span><span class="sxs-lookup"><span data-stu-id="3d0c5-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="3d0c5-124">Voeg in het vak **Hoofdtekst** een module **Standaardpagina** toe.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="3d0c5-125">Voeg in de module **Standaardpagina** in het vak **Hoofdonderdeel** een module **Blok met uitgebreide inhoud** toe.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="3d0c5-126">Voeg in de module **Blok met uitgebreide inhoud** een module **Blokitem met uitgebreide inhoud** toe.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="3d0c5-127">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="3d0c5-128">Een privacybeleidspagina maken</span><span class="sxs-lookup"><span data-stu-id="3d0c5-128">Build a privacy policy page</span></span>

<span data-ttu-id="3d0c5-129">Ga als volgt te werk om een privacybeleidspagina te maken.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="3d0c5-130">Ga naar **Pagina's** en selecteer **Nieuw** om een pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="3d0c5-131">Selecteer in het dialoogvenster **Een sjabloon kiezen** de sjabloon voor de privacybeleidpagina.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="3d0c5-132">Voer een paginanaam en -URL in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="3d0c5-133">Voeg in het vak **Hoofdonderdeel** van de pagina een module **Blok met uitgebreide inhoud** toe.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="3d0c5-134">Voeg in de module **Blok met uitgebreide inhoud** een module **Blokitem met uitgebreide inhoud** toe.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="3d0c5-135">Selecteer in het deelvenster voor de module **Blok met uitgebreide inhoud** de optie **Gegevensbron toevoegen** en selecteer vervolgens **Tekst met opmaak**.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="3d0c5-136">Voer in de RTF-editor de inhoud voor de privacybeleidspagina in.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="3d0c5-137">Vouw de RTF-editor desgewenst uit naar het volledige scherm.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="3d0c5-138">Wanneer u klaar bent met het invoeren van inhoud, selecteert u **Voorbeeld** om de pagina in de webbrowser te bekijken.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="3d0c5-139">Voltooi alle resterende toevoegingen aan de pagina- en module-eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="3d0c5-140">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="3d0c5-141">Volg deze stappen om de URL voor de privacybeleidspagina te publiceren.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="3d0c5-142">Ga naar **URL's** en selecteer de URL voor de privacybeleidspagina.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="3d0c5-143">Selecteer **Publiceren** om de geselecteerde URL te publiceren.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="3d0c5-144">Een koppeling naar de privacybeleidspagina maken in een voettekst</span><span class="sxs-lookup"><span data-stu-id="3d0c5-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="3d0c5-145">U kunt aan een fragment een koppeling naar de privacybeleidspagina toevoegen.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="3d0c5-146">Op deze manier kunt u de koppeling delen en deze bijwerken op meerdere sitepagina's door te verwijzen naar het fragment.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="3d0c5-147">Dit voorbeeld laat zien hoe u een koppeling naar de privacybeleidspagina toevoegt aan een voettekstfragment.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="3d0c5-148">Ga als volgt te werk om een koppeling aan een voettekstfragment toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="3d0c5-149">Ga naar **Fragmenten** en selecteer **Nieuw** om een paginafragment te maken.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="3d0c5-150">Selecteer in het dialoogvenster **Nieuw fragment** de module **Voettekst**.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="3d0c5-151">Voer onder **Naam fragment** een naam in voor het fragment en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3d0c5-152">Voeg in het vak **Voettekstcategorie** een module **Voettekstitem** toe.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="3d0c5-153">Selecteer **Koppelingstekst** in het eigenschappenvenster aan de rechterkant.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="3d0c5-154">Voer in het dialoogvenster **Koppelingstekst** de koppelingstekst en het koppelingsdoel van de privacybeleidspagina in en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="3d0c5-155">Voor de URL van de privacybeleidspagina gaat u naar **Pagina's**, naar de privacybeleidspagina en kopieert u de URL vanuit het deelvenster Eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="3d0c5-156">Selecteer **Opslaan**, selecteer **Bewerken voltooien** om het fragment te controleren en selecteer **Publiceren** om het te publiceren.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3d0c5-157">Bekijk het fragment en test de koppeling naar de privacybeleidspagina.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="3d0c5-158">Naar het fragment kan nu worden verwezen in de sjabloon voor andere sitepagina's.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="3d0c5-159">Wanneer naar dit fragment wordt verwezen in de module **Voettekst** van een sjabloon, wordt de koppelingsverwijzing weergegeven op alle pagina's die zijn gemaakt met behulp van die sjabloon.</span><span class="sxs-lookup"><span data-stu-id="3d0c5-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d0c5-160">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="3d0c5-160">Additional resources</span></span>

[<span data-ttu-id="3d0c5-161">Conformiteitsoverzicht</span><span class="sxs-lookup"><span data-stu-id="3d0c5-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="3d0c5-162">Toegankelijksfuncties en -voorzieningen</span><span class="sxs-lookup"><span data-stu-id="3d0c5-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="3d0c5-163">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="3d0c5-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="3d0c5-164">Gebruikers-id's vervangen die zijn gekoppeld aan wijzigingen in bijgehouden inhoud</span><span class="sxs-lookup"><span data-stu-id="3d0c5-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
