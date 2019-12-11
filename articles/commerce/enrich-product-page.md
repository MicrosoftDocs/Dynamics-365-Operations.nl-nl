---
title: Een productpagina verrijken
description: In dit onderwerp wordt beschreven hoe u een productpagina verrijkt in Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ef9e65b2027a41ca152afaf20ac2fb9a69cd9b96
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698137"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="96dba-103">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="96dba-103">Enrich a product page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="96dba-104">In dit onderwerp wordt beschreven hoe u een productpagina verrijkt in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="96dba-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="96dba-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="96dba-105">Overview</span></span>

<span data-ttu-id="96dba-106">Standaard gebruikt uw site een algemene pagina om productgegevens weer te geven.</span><span class="sxs-lookup"><span data-stu-id="96dba-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="96dba-107">Deze pagina bevat de basisgegevens over het product en de besturingselementen die nodig zijn om het product te verkopen.</span><span class="sxs-lookup"><span data-stu-id="96dba-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="96dba-108">U kunt echter de informatie van de Retail Server aanvullen met extra afbeeldingen of tekst voor een specifiek product.</span><span class="sxs-lookup"><span data-stu-id="96dba-108">However, you can supplement the information that comes from the Retail Server with additional images or text for a specific product.</span></span> <span data-ttu-id="96dba-109">Dit proces wordt het verrijken van de productpagina genoemd.</span><span class="sxs-lookup"><span data-stu-id="96dba-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="96dba-110">In veel gevallen zult u specifieke aanvullende inhoud voor uw producten willen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="96dba-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="96dba-111">Wanneer u naar **Detailhandel** gaat in het ontwerpprogramma, ziet u een lijst met producten uit het afzetkanaal dat aan de site is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="96dba-111">When you go to **Retail** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="96dba-112">In deze lijst geeft de kolom **Verrijkt** aan of de productpagina voor een product is verrijkt.</span><span class="sxs-lookup"><span data-stu-id="96dba-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="96dba-113">Als er een vinkje in de kolom staat, bestaat er een verrijkte product pagina voor het product.</span><span class="sxs-lookup"><span data-stu-id="96dba-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="96dba-114">Als er geen vinkje wordt weergegeven, worden de standaard productpagina en -inhoud voor het product gebruikt.</span><span class="sxs-lookup"><span data-stu-id="96dba-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="96dba-115">U kunt zowel verrijkte als niet-verrijkte productpagina's voorvertonen door een productnaam in de lijst te selecteren.</span><span class="sxs-lookup"><span data-stu-id="96dba-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="96dba-116">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="96dba-116">Enrich a product page</span></span>

<span data-ttu-id="96dba-117">Volg deze stappen om een productpagina te verrijken.</span><span class="sxs-lookup"><span data-stu-id="96dba-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="96dba-118">Selecteer onder **Sites** de naam **Fabrikam** (of de naam van uw site).</span><span class="sxs-lookup"><span data-stu-id="96dba-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="96dba-119">Selecteer **Producten** in het navigatievenster aan de linkerkant.</span><span class="sxs-lookup"><span data-stu-id="96dba-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="96dba-120">Selecteer een product dat geen verrijkte productpagina heeft.</span><span class="sxs-lookup"><span data-stu-id="96dba-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="96dba-121">Selecteer **Een productpagina verrijken** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="96dba-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="96dba-122">Selecteer **PDP-sjabloon** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="96dba-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="96dba-123">Vouw in de overzichtsstructuur aan de linkerkant het vak **Hoofd** uit.</span><span class="sxs-lookup"><span data-stu-id="96dba-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="96dba-124">Selecteer de knop met het weglatingsteken (**...**) voor het vak **Hoofd** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="96dba-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="96dba-125">Selecteer **Container 2** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="96dba-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="96dba-126">Selecteer de knop met het weglatingsteken voor **Container 2** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="96dba-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="96dba-127">Selecteer **Functie** en vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="96dba-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="96dba-128">Voer in het deelvenster Eigenschappen rechts in het veld **Rich Text** de bijgewerkte omschrijving van het product in.</span><span class="sxs-lookup"><span data-stu-id="96dba-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="96dba-129">Voer in het veld **Koptekst** een koptekst in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="96dba-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="96dba-130">Selecteer **Opslaan** en vervolgens **Inchecken**.</span><span class="sxs-lookup"><span data-stu-id="96dba-130">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="96dba-131">Voer in het veld **Opmerkingen** **Een product verrijkt** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="96dba-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="96dba-132">Als u een verrijkte pagina wilt weergeven, selecteert u **Voorbeeld**.</span><span class="sxs-lookup"><span data-stu-id="96dba-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="96dba-133">Wanneer u klaar bent, sluit u het tabblad Voorbeeld om terug te keren naar het ontwerpgereedschap.</span><span class="sxs-lookup"><span data-stu-id="96dba-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="96dba-134">Selecteer **Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="96dba-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96dba-135">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="96dba-135">Additional resources</span></span>

[<span data-ttu-id="96dba-136">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="96dba-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="96dba-137">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="96dba-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="96dba-138">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="96dba-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="96dba-139">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="96dba-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="96dba-140">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="96dba-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="96dba-141">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="96dba-141">Enrich a category landing page</span></span>](enrich-category-page.md)
