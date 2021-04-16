---
title: Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht
description: Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is niet verplicht.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8350646e70c7ea7d705a69ecb52f389e829a0fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833468"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="4eb39-104">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="4eb39-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4eb39-105">Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland.</span><span class="sxs-lookup"><span data-stu-id="4eb39-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="4eb39-106">De magazijndimensie is niet verplicht.</span><span class="sxs-lookup"><span data-stu-id="4eb39-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="4eb39-107">Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="4eb39-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="4eb39-108">De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="4eb39-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="4eb39-109">Deze instelling kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="4eb39-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="4eb39-110">De magazijndimensie is niet ingesteld als verplicht.</span><span class="sxs-lookup"><span data-stu-id="4eb39-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="4eb39-111">Het magazijn kan bekend zijn, maar wordt niet bij de berekening van de hoofdplanning gebruikt.</span><span class="sxs-lookup"><span data-stu-id="4eb39-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="4eb39-112">De site- en magazijndimensie zijn ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="4eb39-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="4eb39-113">Er kunnen ook andere dimensies worden ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="4eb39-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="4eb39-114">De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.</span><span class="sxs-lookup"><span data-stu-id="4eb39-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="4eb39-115">In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat.</span><span class="sxs-lookup"><span data-stu-id="4eb39-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="4eb39-116">In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:</span><span class="sxs-lookup"><span data-stu-id="4eb39-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="4eb39-117">Het magazijn is ingesteld op handmatig.</span><span class="sxs-lookup"><span data-stu-id="4eb39-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="4eb39-118">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="4eb39-119">Ga op het sneltabblad **Hoofdplanning** naar het veld **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="4eb39-120">De artikelbehoefteplanning wordt gedefinieerd voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="4eb39-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="4eb39-121">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="4eb39-122">Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Artikelbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="4eb39-123">Aanvullingsrelaties zijn gedefinieerd voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="4eb39-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="4eb39-124">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="4eb39-125">Zie op het sneltabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="4eb39-126">Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban.</span><span class="sxs-lookup"><span data-stu-id="4eb39-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="4eb39-127">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="4eb39-128">Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="4eb39-129">Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="4eb39-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Vraag naar locatie en magazijn, magazijn niet](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="4eb39-131">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4eb39-131">Additional resources</span></span>
--------

[<span data-ttu-id="4eb39-132">Overzicht van Hoofdplannen en functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="4eb39-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="4eb39-133">Hoofdplanning voor locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="4eb39-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="4eb39-134">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="4eb39-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="4eb39-135">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="4eb39-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="4eb39-136">De stuklijstversie bepalen</span><span class="sxs-lookup"><span data-stu-id="4eb39-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]