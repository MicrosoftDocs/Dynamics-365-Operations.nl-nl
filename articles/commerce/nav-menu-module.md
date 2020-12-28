---
title: Navigatiemenumodule
description: In dit onderwerp worden navigatiemenumodules beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2020
ms.locfileid: "4411513"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="bfeeb-103">Navigatiemenumodule</span><span class="sxs-lookup"><span data-stu-id="bfeeb-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bfeeb-104">In dit onderwerp worden navigatiemenumodules beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bfeeb-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="bfeeb-105">Overview</span></span>

<span data-ttu-id="bfeeb-106">Het belangrijkste doel van navigatiemenumodules is om sitegebruikers in staat te stellen te bladeren naar producten en sitepagina's op basis van de kanaalnavigatiehiërarchie die is gedefinieerd in Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="bfeeb-107">Items die in een navigatiemenumodule zijn geconfigureerd, worden weergegeven als navigatie in de koptekst van de site.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="bfeeb-108">Navigatiemenumodules bieden ook ondersteuning voor statische menuonderwerpen die zijn gekoppeld aan andere pagina's op een e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="bfeeb-109">De navigatiemenumodule kan worden toegevoegd aan de koptekstmodule van een pagina.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="bfeeb-110">In het Fabrikam-thema worden standaard twee niveaus weergegeven in het navigatiemenu.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="bfeeb-111">In het Starter-thema worden standaard drie niveaus weergegeven in het navigatiemenu.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="bfeeb-112">Als u het aantal niveaus wilt wijzigen, is een weergave-extensie vereist voor het thema.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="bfeeb-113">In de volgende afbeelding ziet u een voorbeeld van een navigatiemenu voor de Fabrikam-site met twee niveaus voor de categoriehiërarchie en enkele statische menuopdrachten.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="bfeeb-114">![Voorbeeld van een navigatiemenumodule](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="bfeeb-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="bfeeb-115">Eigenschappen van navigatiemenumodule</span><span class="sxs-lookup"><span data-stu-id="bfeeb-115">Navigation menu module properties</span></span>

| <span data-ttu-id="bfeeb-116">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-116">Property name</span></span>             | <span data-ttu-id="bfeeb-117">Waarde</span><span class="sxs-lookup"><span data-stu-id="bfeeb-117">Value</span></span>                 | <span data-ttu-id="bfeeb-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bfeeb-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="bfeeb-119">Bron</span><span class="sxs-lookup"><span data-stu-id="bfeeb-119">Source</span></span>                  | <span data-ttu-id="bfeeb-120">**Detailhandel**, **Handmatig ontwerp**, **Detailhandel en handmatig ontwerp**</span><span class="sxs-lookup"><span data-stu-id="bfeeb-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="bfeeb-121">Met de waarde **Detailhandel** kan de kanaalnavigatiehiërarchie uit Commerce Headquarters worden weergegeven in het navigatiemenu.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="bfeeb-122">Met **Handmatig ontwerp** kunnen statische menuopdrachten worden opgesteld.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="bfeeb-123">Bij **Detailhandel en handmatig ontwerp** is een combinatie van beide mogelijk.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="bfeeb-124">Categorieafbeeldingen weergeven</span><span class="sxs-lookup"><span data-stu-id="bfeeb-124">Show category images</span></span> | <span data-ttu-id="bfeeb-125">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="bfeeb-125">**True** or **False**</span></span>    | <span data-ttu-id="bfeeb-126">Als deze eigenschap is ingeschakeld, worden in het navigatiemenu categorieafbeeldingen weergegeven die voor elke categorie zijn gedefinieerd in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="bfeeb-127">Toegevoegd in Commerce-release 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="bfeeb-128">Navigatiemenu met meerdere niveaus inschakelen</span><span class="sxs-lookup"><span data-stu-id="bfeeb-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="bfeeb-129">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="bfeeb-129">**True** or **False**</span></span> | <span data-ttu-id="bfeeb-130">Wanneer deze eigenschap is ingeschakeld, kunnen in het navigatiemenu meerdere niveaus van de navigatiehiërarchie worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="bfeeb-131">Deze functie is beschikbaar in Dynamics 365 Commerce versie 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="bfeeb-132">Aantal niveaus</span><span class="sxs-lookup"><span data-stu-id="bfeeb-132">Number of levels</span></span> | <span data-ttu-id="bfeeb-133">geheel getal</span><span class="sxs-lookup"><span data-stu-id="bfeeb-133">integer</span></span> | <span data-ttu-id="bfeeb-134">Met deze eigenschap wordt het aantal niveaus bepaald dat moet worden weergegeven als de eigenschap **Navigatiemenu met meerdere niveaus inschakelen** is ingesteld op **Waar**.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="bfeeb-135">Statische menuopdracht</span><span class="sxs-lookup"><span data-stu-id="bfeeb-135">Static menu item</span></span>| <span data-ttu-id="bfeeb-136">Matrix met waarden</span><span class="sxs-lookup"><span data-stu-id="bfeeb-136">Array of values</span></span>| <span data-ttu-id="bfeeb-137">Statische menuonderwerpen die de naam van een menuopdracht koppelen aan een statische sitepagina.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="bfeeb-138">U kunt menuonderwerpen maken onder andere menuopdrachten.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="bfeeb-139">Statische menu's worden standaard weergegeven op het hoofdniveau en worden toegevoegd aan de kanaalnavigatiehiërarchie als deze bestaat.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="bfeeb-140">Hoofdmenu weergeven</span><span class="sxs-lookup"><span data-stu-id="bfeeb-140">Show root menu</span></span> | <span data-ttu-id="bfeeb-141">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="bfeeb-141">**True** or **False**</span></span> | <span data-ttu-id="bfeeb-142">Wanneer deze eigenschap is ingeschakeld, kan het navigatiemenu onder een aangepast hoofdniveau worden gedefinieerd (bijvoorbeeld **Nu winkelen**).</span><span class="sxs-lookup"><span data-stu-id="bfeeb-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="bfeeb-143">Deze functie is beschikbaar in Dynamics 365 Commerce versie 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="bfeeb-144">Hoofdmenu</span><span class="sxs-lookup"><span data-stu-id="bfeeb-144">Root menu</span></span> | <span data-ttu-id="bfeeb-145">tekenreeks</span><span class="sxs-lookup"><span data-stu-id="bfeeb-145">string</span></span> | <span data-ttu-id="bfeeb-146">Deze eigenschap kan worden gebruikt om tekst voor een aangepast hoofdniveau te definiëren als de eigenschap **Hoofdmenu weergeven** is ingesteld op **Waar**.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="bfeeb-147">In de volgende afbeelding ziet u een voorbeeld van een categorieafbeelding die wordt weergegeven in het navigatiemenu voor de site van Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="bfeeb-148">![Voorbeeld van een navigatiemenumodule met categorieafbeeldingen](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="bfeeb-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="bfeeb-149">Een navigatiemenumodule aan een koptekstmodule toevoegen</span><span class="sxs-lookup"><span data-stu-id="bfeeb-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="bfeeb-150">Zie [Koptekstmodule](author-header-module.md) voor meer informatie over het toevoegen van een navigatiemenumodule aan een koptekstmodule.</span><span class="sxs-lookup"><span data-stu-id="bfeeb-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfeeb-151">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="bfeeb-151">Additional resources</span></span>

[<span data-ttu-id="bfeeb-152">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="bfeeb-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bfeeb-153">Breadcrumb-module</span><span class="sxs-lookup"><span data-stu-id="bfeeb-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="bfeeb-154">Siteselectiemodule</span><span class="sxs-lookup"><span data-stu-id="bfeeb-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="bfeeb-155">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="bfeeb-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bfeeb-156">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="bfeeb-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="bfeeb-157">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="bfeeb-157">Header module</span></span>](author-header-module.md)
