---
title: De sorteervolgorde voor entiteiten voor merchandising wijzigen
description: In dit onderwerp worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten in Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022090"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="4c8cd-103">De sorteervolgorde voor entiteiten voor merchandising wijzigen</span><span class="sxs-lookup"><span data-stu-id="4c8cd-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4c8cd-104">Voor detailhandelaren is het kunnen vinden van producten een primair hulpmiddel voor de interactie met klanten in alle kanalen.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="4c8cd-105">Met behulp van diverse functies kunnen klanten gemakkelijk producten ontdekken.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="4c8cd-106">Ze kunnen bijvoorbeeld bladeren in categorieën, zoeken en filteren.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="4c8cd-107">In dit onderwerp worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="4c8cd-108">Ook wordt uitgelegd hoe u de sorteervolgorde kunt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="4c8cd-109">Overzicht</span><span class="sxs-lookup"><span data-stu-id="4c8cd-109">Overview</span></span>

<span data-ttu-id="4c8cd-110">De ondersteuning voor het sorteren van diverse entiteiten voor merchandising is verbeterd.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="4c8cd-111">Deze ondersteuning is nu beter afgestemd op bestaande klantenscenario's waarvoor eerder extensies nodig waren van de implementatiepartners.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="4c8cd-112">In versies van Retail van voor 10.0.5 was de sorteervolgorde voor categorieën in de navigatiehiërarchie in alfabetische volgorde.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="4c8cd-113">Met de nieuwe aangepaste sorteervolgorde kunt u ervoor zorgen dat merchandisingmanagers de sorteervolgorde configureren voor diverse merchandisingentiteiten voor alle eindgebruikers.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="4c8cd-114">Dit omvat Headquarters (HQ) en callcenters.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="4c8cd-115">De weergavevolgorde configureren voor categorieën in de producthiërarchie</span><span class="sxs-lookup"><span data-stu-id="4c8cd-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="4c8cd-116">Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="4c8cd-117">Ga naar **Retail en Commerce \> Producten en categorieën \> Commerce-producthiërarchie**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="4c8cd-118">Klik op **Categoriehiërarchie bewerken**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="4c8cd-119">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-119">Click **Edit**.</span></span>
4. <span data-ttu-id="4c8cd-120">Vouw in de structuur **ALLE \> Actiesporten** uit.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="4c8cd-121">Vouw in de structuur **ALLE \> Teamsporten** uit.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="4c8cd-122">Voer een nummer in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="4c8cd-123">(Het nummer kan negatief zijn.)</span><span class="sxs-lookup"><span data-stu-id="4c8cd-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="4c8cd-124">Herhaal stap 4 tot en met 6 voor alle andere categorieën waarvan u de volgorde wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="4c8cd-125">De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weergegeven in HQ voor de Commerce-producthiërarchie en de vrijgegeven producten per categorie.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Aangepaste sortering van producthiërarchie met negatieve waarden](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Aangepaste sortering van vrijgegeven producten op categorie op basis van de producthiërarchie](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="4c8cd-128">De weergavevolgorde configureren voor categorieën in de kanaalnavigatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="4c8cd-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="4c8cd-129">Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="4c8cd-130">Ga naar **Retail en Commerce \> Producten en categorieën \> Kanaalnavigatiecategorieën**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="4c8cd-131">Selecteer de **navigatiehiërarchie voor Mode** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="4c8cd-132">Klik op **Categoriehiërarchie bewerken**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="4c8cd-133">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-133">Click **Edit**.</span></span>
5. <span data-ttu-id="4c8cd-134">Selecteer in de structuur **Mode \> Dameskleding \> Damesschoenen**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="4c8cd-135">Voer een nummer in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="4c8cd-136">Selecteer in de structuur **Mode \> Dameskleding \> Tops**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="4c8cd-137">Op dezelfde manier kunt u de sorteervolgorde voor de subcategorieën definiëren.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="4c8cd-138">Selecteer in de structuur **Mode \> Herenkleding \> Casual shirts**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="4c8cd-139">Voer een nummer in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="4c8cd-140">Selecteer in de structuur **Mode \> Herenkleding \> Jassen en jacks**.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="4c8cd-141">Voer een nummer in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="4c8cd-142">Herhaal dit voor alle andere categorieën waarvan u de volgorde wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="4c8cd-143">De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weerspiegeld in HQ, catalogus en kanalen.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Aangepaste sortering voor hiërarchie van detailhandelafzetkanaal](./media/ChannelNavCustomSorted.png)

![Aangepaste sorteren van catalogusnavigatiehiërarchie op basis van de kanaalnavigatiehiërarchie](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS met aangepaste gesorteerde categorieën](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="4c8cd-147">De functie voor aangepast sorteren is standaard uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="4c8cd-148">Zie [Functiebeheer](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview) voor meer informatie over het inschakelen van deze functie en andere functies.</span><span class="sxs-lookup"><span data-stu-id="4c8cd-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
