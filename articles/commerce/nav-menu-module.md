---
title: Navigatiemenumodule
description: In dit onderwerp worden navigatiemenumodules beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817869"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="b8b18-103">Navigatiemenumodule</span><span class="sxs-lookup"><span data-stu-id="b8b18-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b8b18-104">In dit onderwerp worden navigatiemenumodules beschreven en wordt aangegeven hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b8b18-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b8b18-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="b8b18-105">Overview</span></span>

<span data-ttu-id="b8b18-106">Het belangrijkste doel van navigatiemenumodules is om sitegebruikers in staat te stellen te bladeren naar producten en sitepagina's op basis van de kanaalnavigatiehiërarchie die is gedefinieerd in Dynamics 365 Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b8b18-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="b8b18-107">Items die in een navigatiemenumodule zijn geconfigureerd, worden weergegeven als navigatie in de koptekst van de site.</span><span class="sxs-lookup"><span data-stu-id="b8b18-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="b8b18-108">Navigatiemenumodules bieden ook ondersteuning voor statische menuonderwerpen die zijn gekoppeld aan andere pagina's op een e-Commerce-site.</span><span class="sxs-lookup"><span data-stu-id="b8b18-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="b8b18-109">De navigatiemenumodule kan worden toegevoegd aan de koptekstmodule van een pagina.</span><span class="sxs-lookup"><span data-stu-id="b8b18-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="b8b18-110">In het Fabrikam-thema worden standaard twee niveaus weergegeven in het navigatiemenu.</span><span class="sxs-lookup"><span data-stu-id="b8b18-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="b8b18-111">In het Starter-thema worden standaard drie niveaus weergegeven in het navigatiemenu.</span><span class="sxs-lookup"><span data-stu-id="b8b18-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="b8b18-112">Als u het aantal niveaus wilt wijzigen, is een weergave-extensie vereist voor het thema.</span><span class="sxs-lookup"><span data-stu-id="b8b18-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="b8b18-113">In de volgende afbeelding ziet u een voorbeeld van een navigatiemenu voor de Fabrikam-site met twee niveaus voor de categoriehiërarchie en enkele statische menuopdrachten.</span><span class="sxs-lookup"><span data-stu-id="b8b18-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="b8b18-114">![Voorbeeld van een navigatiemenumodule](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="b8b18-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="b8b18-115">Eigenschappen van navigatiemenumodule</span><span class="sxs-lookup"><span data-stu-id="b8b18-115">Navigation menu module properties</span></span>

| <span data-ttu-id="b8b18-116">Naam van eigenschap.</span><span class="sxs-lookup"><span data-stu-id="b8b18-116">Property name</span></span>             | <span data-ttu-id="b8b18-117">Waarde</span><span class="sxs-lookup"><span data-stu-id="b8b18-117">Value</span></span>                 | <span data-ttu-id="b8b18-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b8b18-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b8b18-119">Bron</span><span class="sxs-lookup"><span data-stu-id="b8b18-119">Source</span></span>                  | <span data-ttu-id="b8b18-120">**Detailhandel**, **Handmatig ontwerp**, **Detailhandel en handmatig ontwerp**</span><span class="sxs-lookup"><span data-stu-id="b8b18-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="b8b18-121">Met de waarde **Detailhandel** kan de kanaalnavigatiehiërarchie uit Commerce Headquarters worden weergegeven in het navigatiemenu.</span><span class="sxs-lookup"><span data-stu-id="b8b18-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="b8b18-122">Met **Handmatig ontwerp** kunnen statische menuopdrachten worden opgesteld.</span><span class="sxs-lookup"><span data-stu-id="b8b18-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="b8b18-123">Bij **Detailhandel en handmatig ontwerp** is een combinatie van beide mogelijk.</span><span class="sxs-lookup"><span data-stu-id="b8b18-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="b8b18-124">Categorieafbeeldingen weergeven</span><span class="sxs-lookup"><span data-stu-id="b8b18-124">Show category images</span></span> | <span data-ttu-id="b8b18-125">**True** of **False**</span><span class="sxs-lookup"><span data-stu-id="b8b18-125">**True** or **False**</span></span>    | <span data-ttu-id="b8b18-126">Als deze eigenschap is ingeschakeld, worden in het navigatiemenu categorieafbeeldingen weergegeven die voor elke categorie zijn gedefinieerd in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b8b18-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="b8b18-127">Toegevoegd in Commerce-release 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="b8b18-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="b8b18-128">Statische menuopdracht</span><span class="sxs-lookup"><span data-stu-id="b8b18-128">Static menu item</span></span>| <span data-ttu-id="b8b18-129">Matrix met waarden</span><span class="sxs-lookup"><span data-stu-id="b8b18-129">Array of values</span></span>| <span data-ttu-id="b8b18-130">Statische menuonderwerpen die de naam van een menuopdracht koppelen aan een statische sitepagina.</span><span class="sxs-lookup"><span data-stu-id="b8b18-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="b8b18-131">U kunt menuonderwerpen maken onder andere menuopdrachten.</span><span class="sxs-lookup"><span data-stu-id="b8b18-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="b8b18-132">Statische menu's worden standaard weergegeven op het hoofdniveau en worden toegevoegd aan de kanaalnavigatiehiërarchie als deze bestaat.</span><span class="sxs-lookup"><span data-stu-id="b8b18-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="b8b18-133">In de volgende afbeelding ziet u een voorbeeld van een categorieafbeelding die wordt weergegeven in het navigatiemenu voor de site van Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="b8b18-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="b8b18-134">![Voorbeeld van een navigatiemenumodule met categorieafbeeldingen](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="b8b18-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="b8b18-135">Een navigatiemenumodule aan een koptekstmodule toevoegen</span><span class="sxs-lookup"><span data-stu-id="b8b18-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="b8b18-136">Zie [Koptekstmodule](author-header-module.md) voor meer informatie over het toevoegen van een navigatiemenumodule aan een koptekstmodule.</span><span class="sxs-lookup"><span data-stu-id="b8b18-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8b18-137">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b8b18-137">Additional resources</span></span>

[<span data-ttu-id="b8b18-138">Overzicht van modulebibliotheek</span><span class="sxs-lookup"><span data-stu-id="b8b18-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b8b18-139">Module met vakje voor kopen</span><span class="sxs-lookup"><span data-stu-id="b8b18-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b8b18-140">Conformiteit van cookie</span><span class="sxs-lookup"><span data-stu-id="b8b18-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="b8b18-141">Koptekstmodule</span><span class="sxs-lookup"><span data-stu-id="b8b18-141">Header module</span></span>](author-header-module.md)
