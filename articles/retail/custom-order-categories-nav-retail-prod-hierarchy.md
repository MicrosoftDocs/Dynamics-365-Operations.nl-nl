---
title: De sorteervolgorde voor entiteiten voor merchandising wijzigen
description: In dit onderwerp worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten in Microsoft Dynamics 365 for Retail.
author: ashishharchwani
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
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866156"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="0c08f-103">De sorteervolgorde voor entiteiten voor merchandising wijzigen</span><span class="sxs-lookup"><span data-stu-id="0c08f-103">Change the sort order for merchandising entities</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0c08f-104">Voor detailhandelaren is het kunnen vinden van producten een primair hulpmiddel voor de interactie met klanten in alle detailhandelkanalen.</span><span class="sxs-lookup"><span data-stu-id="0c08f-104">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span> <span data-ttu-id="0c08f-105">Met behulp van diverse functies kunnen klanten gemakkelijk producten ontdekken.</span><span class="sxs-lookup"><span data-stu-id="0c08f-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="0c08f-106">Ze kunnen bijvoorbeeld bladeren in categorieën, zoeken en filteren.</span><span class="sxs-lookup"><span data-stu-id="0c08f-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="0c08f-107">In dit onderwerp worden de concepten beschreven die te maken hebben met het bepalen van de weergavevolgorde voor diverse merchandising-gerelateerde entiteiten.</span><span class="sxs-lookup"><span data-stu-id="0c08f-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="0c08f-108">Ook wordt uitgelegd hoe u de sorteervolgorde kunt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0c08f-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="0c08f-109">Overzicht</span><span class="sxs-lookup"><span data-stu-id="0c08f-109">Overview</span></span>

<span data-ttu-id="0c08f-110">De ondersteuning voor het sorteren van diverse entiteiten voor merchandising is verbeterd.</span><span class="sxs-lookup"><span data-stu-id="0c08f-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="0c08f-111">Deze ondersteuning is nu beter afgestemd op bestaande klantenscenario's waarvoor eerder extensies nodig waren van de implementatiepartners.</span><span class="sxs-lookup"><span data-stu-id="0c08f-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="0c08f-112">In versies van Microsoft Dynamics 365 for Retail van voor 10.0.5 was de sorteervolgorde voor categorieën in de navigatiehiërarchie in alfabetische volgorde.</span><span class="sxs-lookup"><span data-stu-id="0c08f-112">In versions of Microsoft Dynamics 365 for Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="0c08f-113">Met de nieuwe aangepaste sorteervolgorde kunt u ervoor zorgen dat merchandisingmanagers de sorteervolgorde configureren voor diverse merchandisingentiteiten voor alle eindgebruikers.</span><span class="sxs-lookup"><span data-stu-id="0c08f-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="0c08f-114">Dit omvat Headquarters (HQ) en callcenters.</span><span class="sxs-lookup"><span data-stu-id="0c08f-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a><span data-ttu-id="0c08f-115">De weergavevolgorde configureren voor categorieën in de producthiërarchie voor detailhandel</span><span class="sxs-lookup"><span data-stu-id="0c08f-115">Configure the display order for categories in the retail product hierarchy</span></span>

<span data-ttu-id="0c08f-116">Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="0c08f-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="0c08f-117">Ga naar **Detailhandel \> Producten en categorieën \> Producthiërarchie detailhandel**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-117">Go to **Retail \> Products and categories \> Retail product hierarchy**.</span></span>
2. <span data-ttu-id="0c08f-118">Klik op **Categoriehiërarchie bewerken**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="0c08f-119">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-119">Click **Edit**.</span></span>
4. <span data-ttu-id="0c08f-120">Vouw in de structuur **ALLE \> Actiesporten** uit.</span><span class="sxs-lookup"><span data-stu-id="0c08f-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="0c08f-121">Vouw in de structuur **ALLE \> Teamsporten** uit.</span><span class="sxs-lookup"><span data-stu-id="0c08f-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="0c08f-122">Voer een nummer in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="0c08f-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="0c08f-123">(Het nummer kan negatief zijn.)</span><span class="sxs-lookup"><span data-stu-id="0c08f-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="0c08f-124">Herhaal stap 4 tot en met 6 voor alle andere categorieën waarvan u de volgorde wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0c08f-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="0c08f-125">De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weergegeven in HQ voor de detailhandelproducthiërarchie en de vrijgegeven producten per categorie.</span><span class="sxs-lookup"><span data-stu-id="0c08f-125">The display order for the channel navigation hierarchy will be reflected in HQ for the retail product hierarchy and released products by category.</span></span>

![Aangepaste sortering van detailhandelproducthiërarchie met negatieve waarden](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Aangepaste sortering van vrijgegeven producten op categorie op basis van de detailhandelproducthiërarchie](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="0c08f-128">De weergavevolgorde configureren voor categorieën in de kanaalnavigatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="0c08f-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="0c08f-129">Voordat u deze procedure kunt uitvoeren, moeten er voorbeeldgegevens in uw omgeving worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="0c08f-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="0c08f-130">Ga naar **Detailhandel \> Producten en categorieën \> Categorieën voor afzetkanaalnavigatie**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-130">Go to **Retail \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="0c08f-131">Selecteer de **navigatiehiërarchie voor Mode** in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0c08f-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="0c08f-132">Klik op **Categoriehiërarchie bewerken**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="0c08f-133">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-133">Click **Edit**.</span></span>
5. <span data-ttu-id="0c08f-134">Selecteer in de structuur **Mode \> Dameskleding \> Damesschoenen**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="0c08f-135">Voer een nummer in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="0c08f-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="0c08f-136">Selecteer in de structuur **Mode \> Dameskleding \> Tops**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="0c08f-137">Op dezelfde manier kunt u de sorteervolgorde voor de subcategorieën definiëren.</span><span class="sxs-lookup"><span data-stu-id="0c08f-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="0c08f-138">Selecteer in de structuur **Mode \> Herenkleding \> Casual shirts**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="0c08f-139">Voer een nummer in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="0c08f-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="0c08f-140">Selecteer in de structuur **Mode \> Herenkleding \> Jassen en jacks**.</span><span class="sxs-lookup"><span data-stu-id="0c08f-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="0c08f-141">Voer een nummer in het veld **Weergavevolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="0c08f-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="0c08f-142">Herhaal dit voor alle andere categorieën waarvan u de volgorde wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="0c08f-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="0c08f-143">De weergavevolgorde voor de kanaalnavigatiehiërarchie wordt weerspiegeld in HQ, catalogus en detailhandelafzetkanalen.</span><span class="sxs-lookup"><span data-stu-id="0c08f-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and retail channels.</span></span>

![Aangepaste sortering voor hiërarchie van detailhandelafzetkanaal](./media/ChannelNavCustomSorted.png)

![Aangepaste sorteren van catalogusnavigatiehiërarchie op basis van de kanaalnavigatiehiërarchie](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![POS met aangepaste gesorteerde categorieën](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="0c08f-147">De functie voor aangepast sorteren is standaard uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0c08f-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="0c08f-148">Zie [Functiebeheer](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview) voor meer informatie over het inschakelen van deze functie en andere functies.</span><span class="sxs-lookup"><span data-stu-id="0c08f-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
