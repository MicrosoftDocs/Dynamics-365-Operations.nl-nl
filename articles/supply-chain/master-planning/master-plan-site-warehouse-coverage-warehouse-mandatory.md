---
title: Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht
description: Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is verplicht.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e753edacb0e2e019d701745308e7d9190ef09fe8
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="5b24f-104">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="5b24f-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5b24f-105">Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland.</span><span class="sxs-lookup"><span data-stu-id="5b24f-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="5b24f-106">De magazijndimensie is verplicht.</span><span class="sxs-lookup"><span data-stu-id="5b24f-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="5b24f-107">Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="5b24f-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="5b24f-108">De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="5b24f-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="5b24f-109">De magazijndimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="5b24f-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="5b24f-110">De site- en magazijndimensie zijn ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="5b24f-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="5b24f-111">Er kunnen ook andere dimensies worden ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="5b24f-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="5b24f-112">De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.</span><span class="sxs-lookup"><span data-stu-id="5b24f-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="5b24f-113">In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat.</span><span class="sxs-lookup"><span data-stu-id="5b24f-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="5b24f-114">In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:</span><span class="sxs-lookup"><span data-stu-id="5b24f-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="5b24f-115">Het magazijn is ingesteld op **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="5b24f-116">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5b24f-117">Ga op het sneltabblad **Hoofdplanning** naar het veld **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="5b24f-118">De artikelbehoefteplanning wordt gedefinieerd voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="5b24f-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="5b24f-119">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5b24f-120">Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Artikelbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="5b24f-121">Aanvullingsrelaties zijn gedefinieerd voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="5b24f-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="5b24f-122">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5b24f-123">Zie op het sneltabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="5b24f-124">Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban.</span><span class="sxs-lookup"><span data-stu-id="5b24f-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="5b24f-125">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5b24f-126">Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="5b24f-127">Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="5b24f-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Vraaglocatie en magazijndekking zonder verplicht magazijn](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="5b24f-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5b24f-129">See also</span></span>
--------

[<span data-ttu-id="5b24f-130">Hoofdplanning en de functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="5b24f-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="5b24f-131">Hoofdplanning - locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="5b24f-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5b24f-132">Hoofdplanning - locatiebehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="5b24f-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="5b24f-133">Hoofdplanning - locatie- en magazijnbehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="5b24f-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="5b24f-134">Hoofdplanning - hoe de stuklijstversie wordt bepaald</span><span class="sxs-lookup"><span data-stu-id="5b24f-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




