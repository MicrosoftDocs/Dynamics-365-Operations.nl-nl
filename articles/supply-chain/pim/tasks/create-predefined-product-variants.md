---
title: Vooraf gedefinieerde productvarianten maken
description: Deze procedure begeleidt u bij het maken van productvarianten voor een productmodel met behulp van de combinaties van productdimensies.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 442a5f5b321833c170cfecc4069e62a1254605cd
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270475"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="30f15-103">Vooraf gedefinieerde productvarianten</span><span class="sxs-lookup"><span data-stu-id="30f15-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="30f15-104">Voorbeeldscenario: Vooraf gedefinieerde productvarianten maken</span><span class="sxs-lookup"><span data-stu-id="30f15-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="30f15-105">In dit voorbeeldscenario ziet u hoe u productvarianten maakt voor een productmodel met behulp van combinaties van productdimensies.</span><span class="sxs-lookup"><span data-stu-id="30f15-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="30f15-106">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="30f15-106">Make demo data available</span></span>

<span data-ttu-id="30f15-107">Om dit scenario uit te voeren met de hier gegeven waarden, moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon *USMF* selecteren.</span><span class="sxs-lookup"><span data-stu-id="30f15-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="30f15-108">Stap 1: Een productmodel maken</span><span class="sxs-lookup"><span data-stu-id="30f15-108">Step 1: Create a product master</span></span>

<span data-ttu-id="30f15-109">U maakt als volgt een productmodel:</span><span class="sxs-lookup"><span data-stu-id="30f15-109">To create a product master:</span></span>

1. <span data-ttu-id="30f15-110">Ga naar **Productgegevensbeheer > Producten > Productmodellen**.</span><span class="sxs-lookup"><span data-stu-id="30f15-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="30f15-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="30f15-111">Select **New**.</span></span>
1. <span data-ttu-id="30f15-112">Als er in het veld **Productnummer** nog geen nummer staat, voert u een waarde in.</span><span class="sxs-lookup"><span data-stu-id="30f15-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="30f15-113">Deze stap is alleen vereist als er geen nummerreeks voor dit veld is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="30f15-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="30f15-114">Voer in het vak **Productnaam** een naam in.</span><span class="sxs-lookup"><span data-stu-id="30f15-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="30f15-115">Selecteer in het veld **Productdimensiegroep** de productdimensiegroep *SizeCol* (Maat en Kleur).</span><span class="sxs-lookup"><span data-stu-id="30f15-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="30f15-116">Selecteer **OK** om het nieuwe productmodel te maken en te openen.</span><span class="sxs-lookup"><span data-stu-id="30f15-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="30f15-117">Stap 2: Productdimensies toevoegen</span><span class="sxs-lookup"><span data-stu-id="30f15-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="30f15-118">Dit voorbeeld toont hoe productdimensies handmatig worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="30f15-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="30f15-119">U kunt er ook voor kiezen een grootte, kleur of stijlgroep te selecteren die de productdimensiewaarden bevat die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="30f15-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="30f15-120">U voegt als volgt productdimensies toe:</span><span class="sxs-lookup"><span data-stu-id="30f15-120">To add product dimensions:</span></span>

1. <span data-ttu-id="30f15-121">Als uw nieuwe productmodel nog steeds geopend is, selecteert u **Productdimensies** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="30f15-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="30f15-122">Open het tabblad **Grootte** en selecteer **Nieuw** op de werkbalk om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="30f15-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="30f15-123">Voer voor de nieuwe rij de volgende instellingen in:</span><span class="sxs-lookup"><span data-stu-id="30f15-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="30f15-124">**Grootte**: selecteer een berekeningswaarde.</span><span class="sxs-lookup"><span data-stu-id="30f15-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="30f15-125">**Naam**: voer een naam in voor de grootte.</span><span class="sxs-lookup"><span data-stu-id="30f15-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="30f15-126">Selecteer **Nieuw** op de werkbalk en voeg een tweede grootte aan het raster toe met een nieuwe **Grootte** en **Naam**.</span><span class="sxs-lookup"><span data-stu-id="30f15-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="30f15-127">Open het tabblad **Kleuren** en selecteer **Nieuw** op de werkbalk om een rij aan het raster toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="30f15-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="30f15-128">Voer voor de nieuwe rij de volgende instellingen in:</span><span class="sxs-lookup"><span data-stu-id="30f15-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="30f15-129">**Kleur**: selecteer een kleurwaarde.</span><span class="sxs-lookup"><span data-stu-id="30f15-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="30f15-130">**Naam**: voer een naam in voor de kleur.</span><span class="sxs-lookup"><span data-stu-id="30f15-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="30f15-131">Selecteer **Nieuw** op de werkbalk en voeg een tweede kleur aan het raster toe met een nieuwe **Kleur** en **Naam**.</span><span class="sxs-lookup"><span data-stu-id="30f15-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="30f15-132">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="30f15-132">Select **Save**.</span></span>
1. <span data-ttu-id="30f15-133">Sluit de pagina en ga terug naar uw nieuwe productmodel.</span><span class="sxs-lookup"><span data-stu-id="30f15-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="30f15-134">Stap 3: Productvarianten genereren</span><span class="sxs-lookup"><span data-stu-id="30f15-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="30f15-135">In deze sectie wordt beschreven hoe u productvarianten genereert wanneer de functie *Verbeteringen voor de pagina Variantsuggesties* niet is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="30f15-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="30f15-136">In het volgende gedeelte leest u meer over het genereren van productvarianten wanneer die functie beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="30f15-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="30f15-137">U genereert als volgt productvarianten:</span><span class="sxs-lookup"><span data-stu-id="30f15-137">To generate product variants:</span></span>

1. <span data-ttu-id="30f15-138">Als uw nieuwe productmodel nog steeds geopend is, selecteert u **Productvarianten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="30f15-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="30f15-139">Selecteer **Variantsuggesties** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="30f15-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="30f15-140">Er wordt een lijst gegenereerd met alle mogelijke combinaties van grootten en kleuren die u voor het product hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="30f15-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="30f15-141">Selecteer **Alles selecteren** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="30f15-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="30f15-142">In dit voorbeeld selecteert u alle mogelijke varianten.</span><span class="sxs-lookup"><span data-stu-id="30f15-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="30f15-143">Als u alleen een subset van de mogelijke productdimensiecombinaties wilt gebruiken, schakelt u alleen waar nodig de vereiste selectievakjes in.</span><span class="sxs-lookup"><span data-stu-id="30f15-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="30f15-144">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="30f15-144">Select **Create**.</span></span>
1. <span data-ttu-id="30f15-145">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="30f15-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="30f15-146">Verbeterde variantsuggesties</span><span class="sxs-lookup"><span data-stu-id="30f15-146">Improved variant suggestions</span></span>

<span data-ttu-id="30f15-147">De functie *Verbeteringen voor de pagina Variantsuggesties* verbetert de pagina **Variantsuggesties**, zodat prestatie- en bruikbaarheidsproblemen worden verholpen voor bedrijven die combinaties van productdimensies hebben.</span><span class="sxs-lookup"><span data-stu-id="30f15-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="30f15-148">Het verbeterde proces voor selectie van de productdimensiewaarden waarvoor variantsuggesties moeten worden gegenereerd, maakt het sneller en eenvoudiger om de relevante set productvarianten te identificeren en vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="30f15-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="30f15-149">De functie voegt de volgende verbeteringen toe:</span><span class="sxs-lookup"><span data-stu-id="30f15-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="30f15-150">**Uitgestelde generatie van variantsuggesties**: Op de pagina **Variantsuggesties** worden geen suggesties meer weergegeven wanneer u deze voor het eerst opent.</span><span class="sxs-lookup"><span data-stu-id="30f15-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="30f15-151">In plaats daarvan moet u expliciet kiezen welke waarden u nodig hebt en vervolgens op de knop **Voorstellen** klikken om de combinaties te genereren.</span><span class="sxs-lookup"><span data-stu-id="30f15-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="30f15-152">Hierdoor wordt het proces zichtbaarder en interactiever.</span><span class="sxs-lookup"><span data-stu-id="30f15-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="30f15-153">**Selectie van dimensiewaarden**: Wanneer u veel dimensiewaarden hebt, bent u meestal geïnteresseerd in het genereren van variantsuggesties die slechts enkele daarvan bevatten (bijvoorbeeld wanneer u een nieuwe reeks kleuren of stijlen wilt introduceren).</span><span class="sxs-lookup"><span data-stu-id="30f15-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="30f15-154">Met het verbeterde ontwerp kunt u de dimensiewaarden selecteren waarvoor u productvariantsuggesties wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="30f15-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="30f15-155">Hierdoor wordt de voorgestelde varianten aanzienlijk relevanter en worden de systeemprestaties en de productiviteit van de gebruiker verbeterd.</span><span class="sxs-lookup"><span data-stu-id="30f15-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="30f15-156">De functie Verbeteringen voor de pagina Variantsuggesties inschakelen</span><span class="sxs-lookup"><span data-stu-id="30f15-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="30f15-157">Voordat u de functie *Verbeteringen voor de pagina Variantsuggesties* kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="30f15-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="30f15-158">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="30f15-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="30f15-159">Schakel in het werkgebied **Functiebeheer** de functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="30f15-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="30f15-160">**Module:** *Productgegevensbeheer*</span><span class="sxs-lookup"><span data-stu-id="30f15-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="30f15-161">**Functienaam**: *Verbeteringen voor de pagina Variantsuggesties*</span><span class="sxs-lookup"><span data-stu-id="30f15-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="30f15-162">Werken met de verbeterde variantsuggesties</span><span class="sxs-lookup"><span data-stu-id="30f15-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="30f15-163">U genereert als volgt productvarianten wanneer de functie *Verbeteringen voor de pagina Variantsuggesties* is ingeschakeld:</span><span class="sxs-lookup"><span data-stu-id="30f15-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="30f15-164">Open of maak een productmodel en voeg hieraan de vereiste productdimenssie toe, zoals beschreven in de vorige sectie.</span><span class="sxs-lookup"><span data-stu-id="30f15-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="30f15-165">Als het productmodel geopend is, selecteert u **Productvarianten** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="30f15-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="30f15-166">Selecteer **Variantsuggesties** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="30f15-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="30f15-167">Selecteer de waarden die u wilt gebruiken voor elk van de dimensies.</span><span class="sxs-lookup"><span data-stu-id="30f15-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="30f15-168">Selecteer **Voorstellen** op de bovenste werkbalk.</span><span class="sxs-lookup"><span data-stu-id="30f15-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="30f15-169">Er wordt een lijst gegenereerd met alle mogelijke combinaties van grootten en kleuren die u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="30f15-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="30f15-170">Schakel op het sneltabblad **Voorgestelde varianten** het selectievakje in voor elke productdimensiecombinatie die u wilt gebruiken of selecteer **Alles selecteren** op de werkbalk om ze allemaal te selecteren.</span><span class="sxs-lookup"><span data-stu-id="30f15-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="30f15-171">Selecteer **Maken** om de varianten aan het huidige productmodel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="30f15-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
