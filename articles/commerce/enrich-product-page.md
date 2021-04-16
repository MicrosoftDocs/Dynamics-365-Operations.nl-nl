---
title: Een productpagina verrijken
description: In dit onderwerp wordt beschreven hoe u een productpagina verrijkt in Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799034"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="a2214-103">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="a2214-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a2214-104">In dit onderwerp wordt beschreven hoe u een productpagina verrijkt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a2214-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a2214-105">Standaard gebruikt uw site een algemene pagina om productgegevens weer te geven.</span><span class="sxs-lookup"><span data-stu-id="a2214-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="a2214-106">Deze pagina bevat de basisgegevens over het product en de besturingselementen die nodig zijn om het product te verkopen.</span><span class="sxs-lookup"><span data-stu-id="a2214-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="a2214-107">U kunt echter de informatie van de Commerce Scale Unit aanvullen met extra afbeeldingen of tekst voor een specifiek product.</span><span class="sxs-lookup"><span data-stu-id="a2214-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="a2214-108">Dit proces wordt het verrijken van de productpagina genoemd.</span><span class="sxs-lookup"><span data-stu-id="a2214-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="a2214-109">In veel gevallen zult u specifieke aanvullende inhoud voor uw producten willen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a2214-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="a2214-110">Wanneer u naar **Retail en Commerce** gaat in het ontwerpprogramma, ziet u een lijst met producten uit het afzetkanaal dat aan de site is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a2214-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="a2214-111">In deze lijst geeft de kolom **Verrijkt** aan of de productpagina voor een product is verrijkt.</span><span class="sxs-lookup"><span data-stu-id="a2214-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="a2214-112">Als er een vinkje in de kolom staat, bestaat er een verrijkte product pagina voor het product.</span><span class="sxs-lookup"><span data-stu-id="a2214-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="a2214-113">Als er geen vinkje wordt weergegeven, worden de standaard productpagina en -inhoud voor het product gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a2214-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="a2214-114">U kunt zowel verrijkte als niet-verrijkte productpagina's voorvertonen door een productnaam in de lijst te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a2214-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="a2214-115">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="a2214-115">Enrich a product page</span></span>

<span data-ttu-id="a2214-116">Volg deze stappen om een productpagina te verrijken.</span><span class="sxs-lookup"><span data-stu-id="a2214-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="a2214-117">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="a2214-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="a2214-118">Selecteer **Producten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="a2214-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="a2214-119">Selecteer een product dat geen verrijkte productpagina heeft.</span><span class="sxs-lookup"><span data-stu-id="a2214-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="a2214-120">Selecteer **Een productpagina verrijken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="a2214-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="a2214-121">Selecteer **PDP-sjabloon** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2214-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="a2214-122">Vouw in de overzichtsstructuur aan de linkerkant het vak **Hoofd** uit.</span><span class="sxs-lookup"><span data-stu-id="a2214-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="a2214-123">Selecteer de knop met het weglatingsteken (**...**) voor het vak **Hoofd** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a2214-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="a2214-124">Selecteer **Container 2** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2214-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="a2214-125">Selecteer de knop met het weglatingsteken voor **Container 2** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="a2214-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="a2214-126">Selecteer **Functie** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2214-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="a2214-127">Voer in het deelvenster Eigenschappen rechts in het veld **Rich Text** de bijgewerkte omschrijving van het product in.</span><span class="sxs-lookup"><span data-stu-id="a2214-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="a2214-128">Voer in het veld **Koptekst** een koptekst in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2214-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="a2214-129">Selecteer **Opslaan** en vervolgens **Bewerken voltooien**.</span><span class="sxs-lookup"><span data-stu-id="a2214-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="a2214-130">Voer in het veld **Opmerkingen** **Een product verrijkt** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2214-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="a2214-131">Als u een verrijkte pagina wilt weergeven, selecteert u **Voorbeeld**.</span><span class="sxs-lookup"><span data-stu-id="a2214-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="a2214-132">Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="a2214-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="a2214-133">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="a2214-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2214-134">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="a2214-134">Additional resources</span></span>

[<span data-ttu-id="a2214-135">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="a2214-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="a2214-136">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="a2214-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="a2214-137">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="a2214-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="a2214-138">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="a2214-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="a2214-139">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="a2214-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="a2214-140">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="a2214-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="a2214-141">Toegankelijkheid van pagina-inhoud controleren</span><span class="sxs-lookup"><span data-stu-id="a2214-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="a2214-142">Dynamische e-commercepagina's maken op basis van URL-parameters</span><span class="sxs-lookup"><span data-stu-id="a2214-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
