---
title: Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht
description: Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is niet verplicht.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 45796049cddef137eb2ca1e4331197e4b4a65071
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="8df71-104">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="8df71-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8df71-105">Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland.</span><span class="sxs-lookup"><span data-stu-id="8df71-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="8df71-106">De magazijndimensie is niet verplicht.</span><span class="sxs-lookup"><span data-stu-id="8df71-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="8df71-107">Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="8df71-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="8df71-108">De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="8df71-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="8df71-109">Deze instelling kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="8df71-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="8df71-110">De magazijndimensie is niet ingesteld als verplicht.</span><span class="sxs-lookup"><span data-stu-id="8df71-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="8df71-111">Het magazijn kan bekend zijn, maar wordt niet bij de berekening van de hoofdplanning gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8df71-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="8df71-112">De site- en magazijndimensie zijn ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="8df71-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="8df71-113">Er kunnen ook andere dimensies worden ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="8df71-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="8df71-114">De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.</span><span class="sxs-lookup"><span data-stu-id="8df71-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="8df71-115">In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat.</span><span class="sxs-lookup"><span data-stu-id="8df71-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="8df71-116">In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:</span><span class="sxs-lookup"><span data-stu-id="8df71-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="8df71-117">Het magazijn is ingesteld op handmatig.</span><span class="sxs-lookup"><span data-stu-id="8df71-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="8df71-118">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="8df71-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="8df71-119">Ga op het sneltabblad **Hoofdplanning** naar het veld **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="8df71-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="8df71-120">De artikelbehoefteplanning wordt gedefinieerd voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="8df71-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="8df71-121">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="8df71-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="8df71-122">Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Artikelbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="8df71-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="8df71-123">Aanvullingsrelaties zijn gedefinieerd voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="8df71-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="8df71-124">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="8df71-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="8df71-125">Zie op het sneltabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.</span><span class="sxs-lookup"><span data-stu-id="8df71-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="8df71-126">Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban.</span><span class="sxs-lookup"><span data-stu-id="8df71-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="8df71-127">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="8df71-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="8df71-128">Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="8df71-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="8df71-129">Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="8df71-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Vraag naar locatie en magazijn, magazijn niet](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)


-



<a name="additional-resources"></a><span data-ttu-id="8df71-131">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="8df71-131">Additional resources</span></span>
--------

[<span data-ttu-id="8df71-132">Hoofdplanning en de functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="8df71-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="8df71-133">Hoofdplanning - locatie en magazijnbehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="8df71-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="8df71-134">Hoofdplanning - locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="8df71-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="8df71-135">Hoofdplanning - locatiebehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="8df71-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="8df71-136">Hoofdplanning - hoe de stuklijstversie wordt bepaald</span><span class="sxs-lookup"><span data-stu-id="8df71-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




