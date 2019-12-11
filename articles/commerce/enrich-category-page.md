---
title: Een landingspagina voor een categorie verrijken
description: In dit onderwerp wordt de verrijking van categoriepagina's in Dynamics 365 Commerce beschreven.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8d735b215132b90ca786d6967589496bee73f4d9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697584"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="77ca2-103">Een landingspagina voor een categorie verrijken</span><span class="sxs-lookup"><span data-stu-id="77ca2-103">Enrich a category landing page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="77ca2-104">In dit onderwerp wordt de verrijking van categoriepagina's in Dynamics 365 Commerce beschreven.</span><span class="sxs-lookup"><span data-stu-id="77ca2-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="77ca2-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="77ca2-105">Overview</span></span>

<span data-ttu-id="77ca2-106">Commerce biedt een standaard landingspagina voor categorieën die wordt gebruikt wanneer categoriegegevens worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="77ca2-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="77ca2-107">Een standaard categoriepagina bevat vereiste elementen, zoals verfijners, gecategoriseerde productplaatsing, sorteeropties, een keuzeoverzicht en pagineringsknoppen.</span><span class="sxs-lookup"><span data-stu-id="77ca2-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="77ca2-108">In plaats van de standaardcategoriepagina te gebruiken kunt u echter een "verrijkte" categorielandingspagina gebruiken die meer inhoud en meer specifieke elementen bevat.</span><span class="sxs-lookup"><span data-stu-id="77ca2-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="77ca2-109">Bij een speciale verrijking moet u bijvoorbeeld categoriespecifieke marketinginhoud toevoegen aan de categoriepagina.</span><span class="sxs-lookup"><span data-stu-id="77ca2-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="77ca2-110">Deze inhoud kan betrekking hebben op plaatsing van producten in meerdere categorieën voor cross-sell doeleinden, redactionele lijsten, afbeeldingen, video's en andere tekst.</span><span class="sxs-lookup"><span data-stu-id="77ca2-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="77ca2-111">U kunt de standaardcategoriepagina wijzigen of een andere categoriepagina definiëren voor een specifieke categorie.</span><span class="sxs-lookup"><span data-stu-id="77ca2-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Verrijkte landingspagina voor categorie](./media/CategoryLandingPages.png)

<span data-ttu-id="77ca2-113">In het ontwerpprogramma bevat de pagina **Product** een lijst met categorieën uit het afzetkanaal die aan de site zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="77ca2-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="77ca2-114">Als de **verrijkte** status voor een categoriepagina is geselecteerd, is deze categoriepagina verrijkt.</span><span class="sxs-lookup"><span data-stu-id="77ca2-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="77ca2-115">Anders worden de standaard categoriepagina en de inhoud van de categorie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="77ca2-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="77ca2-116">U kunt zowel verrijkte als niet-verrijkte categoriepagina's voor een categorie voorvertonen door een categorienaam te selecteren.</span><span class="sxs-lookup"><span data-stu-id="77ca2-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="77ca2-117">Ga als volgt te werk om een categoriepagina te verrijken.</span><span class="sxs-lookup"><span data-stu-id="77ca2-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="77ca2-118">Selecteer op de pagina **Producten** de naam van de categorie waarvoor u de categoriepagina wilt verrijken.</span><span class="sxs-lookup"><span data-stu-id="77ca2-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="77ca2-119">De standaard categoriepagina voor de geselecteerde categorie wordt geopend in de pagina-editor.</span><span class="sxs-lookup"><span data-stu-id="77ca2-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="77ca2-120">Selecteer **Categoriepagina verrijken**.</span><span class="sxs-lookup"><span data-stu-id="77ca2-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="77ca2-121">Selecteer een sjabloon voor de verrijkte categoriepagina.</span><span class="sxs-lookup"><span data-stu-id="77ca2-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="77ca2-122">Als u alleen kleine wijzigingen aanbrengt, kunt u de standaard categoriepagina selecteren.</span><span class="sxs-lookup"><span data-stu-id="77ca2-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="77ca2-123">Anders kunt u een specifieke sjabloon voor een categoriepagina selecteren.</span><span class="sxs-lookup"><span data-stu-id="77ca2-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="77ca2-124">Wanneer u de sjabloon selecteert, wordt de pagina-editor geopend en wordt de geselecteerde sjabloon gebruikt om een nieuwe categoriepagina te maken voor de geselecteerde categorie.</span><span class="sxs-lookup"><span data-stu-id="77ca2-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="77ca2-125">De pagina wordt uitgecheckt naar u en u kunt wijzigingen aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="77ca2-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="77ca2-126">In modules die gebruikmaken van de categoriespecificatiegegevens, worden de gegevens uit de geselecteerde categorie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="77ca2-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="77ca2-127">De instellingen van de sjabloon die u selecteert, bepalen welke wijzigingen u kunt aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="77ca2-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77ca2-128">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="77ca2-128">Additional resources</span></span>

[<span data-ttu-id="77ca2-129">Een bestaande sitepagina wijzigen</span><span class="sxs-lookup"><span data-stu-id="77ca2-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="77ca2-130">Een nieuwe sitepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="77ca2-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="77ca2-131">Pagina-indelingen selecteren</span><span class="sxs-lookup"><span data-stu-id="77ca2-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="77ca2-132">Metagegevens SEO beheren</span><span class="sxs-lookup"><span data-stu-id="77ca2-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="77ca2-133">Een pagina opslaan, voorvertonen en publiceren</span><span class="sxs-lookup"><span data-stu-id="77ca2-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="77ca2-134">Een productpagina verrijken</span><span class="sxs-lookup"><span data-stu-id="77ca2-134">Enrich a product page</span></span>](enrich-product-page.md)