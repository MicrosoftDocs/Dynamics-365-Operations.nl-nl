---
title: Module voor zoekresultaten
description: In dit onderwerp worden modules voor zoekresultaten beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3409e9e99329def55b173eb78cf03db4a6764c92
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794110"
---
# <a name="search-results-module"></a><span data-ttu-id="c8ef1-103">Module voor zoekresultaten</span><span class="sxs-lookup"><span data-stu-id="c8ef1-103">Search results module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8ef1-104">In dit onderwerp worden modules voor zoekresultaten beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c8ef1-105">De module voor zoekresultaten retourneert zoekresultaten met producten en een lijst met toepasselijke verfijningen voor de producten.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="c8ef1-106">Modules voor zoekresultaten kunnen op Dynamics 365 Commerce-sites worden gebruikt om pagina's weer te geven voor de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="c8ef1-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="c8ef1-107">Zoekresultaten die worden gestart door een zoekopdracht van een gebruiker</span><span class="sxs-lookup"><span data-stu-id="c8ef1-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="c8ef1-108">Zoekresultaten waarmee een specifieke verzameling producten wordt weergegeven, zoals 'Vergelijkbare artikelen'.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="c8ef1-109">Lijsten met producten die tot een bepaalde categorie behoren</span><span class="sxs-lookup"><span data-stu-id="c8ef1-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="c8ef1-110">Zie [Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md) voor meer informatie over categorie- en zoekresultatenpagina's.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="c8ef1-111">In de volgende afbeelding ziet u een voorbeeld van een zoekresultatenpagna voor een categorie op de site van Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Voorbeeld van een pagina met zoekresultaten op de Fabrikam-site](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="c8ef1-113">Eigenschappen van modules voor zoekresultaten</span><span class="sxs-lookup"><span data-stu-id="c8ef1-113">Search results module properties</span></span>

<span data-ttu-id="c8ef1-114">In de volgende tabel worden de eigenschappen van modules voor zoekresultaten met hun waarden en omschrijvingen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="c8ef1-115">Eigenschap</span><span class="sxs-lookup"><span data-stu-id="c8ef1-115">Property</span></span> | <span data-ttu-id="c8ef1-116">Waarden</span><span class="sxs-lookup"><span data-stu-id="c8ef1-116">Values</span></span> | <span data-ttu-id="c8ef1-117">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c8ef1-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="c8ef1-118">Artikelen per pagina</span><span class="sxs-lookup"><span data-stu-id="c8ef1-118">Items per page</span></span> | <span data-ttu-id="c8ef1-119">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="c8ef1-119">Integer</span></span> | <span data-ttu-id="c8ef1-120">Het aantal items dat op elke pagina moet worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="c8ef1-121">Terug naar PDP toestaan</span><span class="sxs-lookup"><span data-stu-id="c8ef1-121">Allow back on PDP</span></span> | <span data-ttu-id="c8ef1-122">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="c8ef1-122">**True** or **False**</span></span> | <span data-ttu-id="c8ef1-123">Als deze eigenschap is ingesteld op **Waar** en een gebruiker een product selecteert op de zoekresultatenpagina, wordt op de breadcrumb-navigatie op de pagina met productgegevens die wordt geopend een koppeling Terug naar resultaten weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="c8ef1-124">Verfijningen uitvouwen</span><span class="sxs-lookup"><span data-stu-id="c8ef1-124">Expand Refiners</span></span> | <span data-ttu-id="c8ef1-125">**Alle**, **1**, **2**, **3** of **4**</span><span class="sxs-lookup"><span data-stu-id="c8ef1-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="c8ef1-126">Het aantal topverfijningen dat moet worden uitgevouwen wanneer een pagina wordt geladen.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="c8ef1-127">Als deze eigenschap bijvoorbeeld is ingesteld op **3**, worden de eerste drie verfijningen op de pagina uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="c8ef1-128">Weergave categoriehiërarchie verbergen</span><span class="sxs-lookup"><span data-stu-id="c8ef1-128">Hide category hierarchy display</span></span> | <span data-ttu-id="c8ef1-129">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="c8ef1-129">**True** or **False**</span></span> | <span data-ttu-id="c8ef1-130">Als deze eigenschap is ingesteld op **Waar**, wordt de weergave van categoriehiërarchie op de pagina verborgen.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="c8ef1-131">Deze eigenschap moet worden ingesteld op **Waar** als u de [breadcrumb-module](add-breadcrumb.md) gebruikt om de categoriehiërarchie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="c8ef1-132">Productkenmerken opnemen in zoekresultaten</span><span class="sxs-lookup"><span data-stu-id="c8ef1-132">Include product attributes in search results</span></span> | <span data-ttu-id="c8ef1-133">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="c8ef1-133">**True** or **False**</span></span> | <span data-ttu-id="c8ef1-134">Als deze eigenschap is ingesteld op **Waar**, worden kenmerken geretourneerd voor de producten in de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="c8ef1-135">Hoewel deze kenmerken kunnen worden weergegeven op een Commerce-site, is een extensie vereist.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="c8ef1-136">Prijzen van aansluiting weergeven</span><span class="sxs-lookup"><span data-stu-id="c8ef1-136">Show affiliation prices</span></span> | <span data-ttu-id="c8ef1-137">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="c8ef1-137">**True** or **False**</span></span> | <span data-ttu-id="c8ef1-138">Als deze eigenschap is ingesteld op **Waar**, worden aansluitingsprijzen voor producten weergegeven in de zoekresultaten wanneer een aangemelde gebruiker door de pagina bladert.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="c8ef1-139">In Dynamics 365 Commerce 10.0.16 en hoger kan de configuratie **Prijzen voor aansluitingen** worden gebruikt om prijzen voor aansluitingen op de pagina weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="c8ef1-140">Ondersteunde modules</span><span class="sxs-lookup"><span data-stu-id="c8ef1-140">Supported modules</span></span>

<span data-ttu-id="c8ef1-141">De module voor zoekresultaten ondersteunt de [module voor snelle weergave](quick-view-module.md), waarmee gebruikers productgegevens kunnen bekijken en artikelen aan het winkelwagentje kunnen toevoegen vanuit de zoekresultatenpagina.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="c8ef1-142">Een module voor zoekresultaten aan een categoriepagina toevoegen</span><span class="sxs-lookup"><span data-stu-id="c8ef1-142">Add a search results module to a category page</span></span>

<span data-ttu-id="c8ef1-143">Voer deze stappen uit om een module voor zoekresultaten aan een categoriepagina toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="c8ef1-144">Ga naar **Sjablonen** en selecteer **Nieuw** om een nieuwe sjabloon te maken.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c8ef1-145">Voer in het dialoogvenster **Nieuwe sjabloon** de naam **Zoekresultaten** in en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="c8ef1-146">Selecteer het weglatingsteken (...) in het vak **Hoofdtekst** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c8ef1-147">Selecteer in het dialoogvenster **Module toevoegen** de module **Standaardpagina** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c8ef1-148">Selecteer in het vak **Hoofd** van de module **Standaardpagina** het weglatingsteken (...) en vervolgens **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c8ef1-149">Selecteer in het dialoogvenster **Module toevoegen** de module **Container** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c8ef1-150">Selecteer het weglatingsteken (...) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c8ef1-151">Selecteer in het dialoogvenster **Module toevoegen** de module **Breadcrumb** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c8ef1-152">Voer in het eigenschappenvenster **Breadcrumb** de waarde **1** in voor **Min. voorvallen**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="c8ef1-153">Selecteer het weglatingsteken (...) in het vak **Container** en selecteer **Module toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c8ef1-154">Selecteer in het dialoogvenster **Module toevoegen** de module **Zoekresultaten** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c8ef1-155">Voer in het eigenschappenvenster **Zoekresultaten** de waarde **1** voor **Min. voorvallen** in en stel vervolgens andere vereiste eigenschappen in voor de module voor zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="c8ef1-156">Door deze eigenschappen in de sjabloon in te stellen, zorgt u ervoor dat de aanpassingen voor een specifieke categoriepagina automatisch deze instellingen bevatten.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="c8ef1-157">Selecteer **Bewerken voltooien** en **Publiceren** om de sjabloon te publiceren.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="c8ef1-158">Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c8ef1-159">Selecteer in het dialoogvenster **Een sjabloon kiezen** de sjabloon **Zoekresultaten** die u hebt gemaakt, voer **Categoriepagina** voor **Paginanaam** in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="c8ef1-160">Aangezien alle waarden in de sjabloon zijn ingesteld, kan de pagina worden gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="c8ef1-161">Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.</span><span class="sxs-lookup"><span data-stu-id="c8ef1-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8ef1-162">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c8ef1-162">Additional resources</span></span>

[<span data-ttu-id="c8ef1-163">Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten</span><span class="sxs-lookup"><span data-stu-id="c8ef1-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="c8ef1-164">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="c8ef1-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c8ef1-165">Module voor snelle weergave</span><span class="sxs-lookup"><span data-stu-id="c8ef1-165">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
