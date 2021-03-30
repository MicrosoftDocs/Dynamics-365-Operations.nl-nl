---
title: Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht
description: Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland. De magazijndimensie is verplicht.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ffc550ff719950a603811c65cb9b790ded5c2c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236046"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="f18a7-104">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="f18a7-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f18a7-105">Dit onderwerp beschrijft hoe een artikel dat een locatie en magazijn als dimensies voor behoefteplanning heeft, wordt gepland.</span><span class="sxs-lookup"><span data-stu-id="f18a7-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="f18a7-106">De magazijndimensie is verplicht.</span><span class="sxs-lookup"><span data-stu-id="f18a7-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="f18a7-107">Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="f18a7-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="f18a7-108">De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="f18a7-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="f18a7-109">De magazijndimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="f18a7-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="f18a7-110">De site- en magazijndimensie zijn ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="f18a7-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="f18a7-111">Er kunnen ook andere dimensies worden ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="f18a7-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="f18a7-112">De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.</span><span class="sxs-lookup"><span data-stu-id="f18a7-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="f18a7-113">In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat.</span><span class="sxs-lookup"><span data-stu-id="f18a7-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="f18a7-114">In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:</span><span class="sxs-lookup"><span data-stu-id="f18a7-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="f18a7-115">Het magazijn is ingesteld op **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="f18a7-116">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="f18a7-117">Ga op het sneltabblad **Hoofdplanning** naar het veld **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="f18a7-118">De artikelbehoefteplanning wordt gedefinieerd voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="f18a7-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="f18a7-119">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f18a7-120">Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Artikelbehoefte**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="f18a7-121">Aanvullingsrelaties zijn gedefinieerd voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="f18a7-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="f18a7-122">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="f18a7-123">Zie op het sneltabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="f18a7-124">Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban.</span><span class="sxs-lookup"><span data-stu-id="f18a7-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="f18a7-125">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f18a7-126">Selecteer het artikel en ga vervolgens in het actievenster naar het tabblad **Plannen** en klik op **Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="f18a7-127">Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="f18a7-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Vraaglocatie en magazijndekking zonder verplicht magazijn](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="f18a7-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f18a7-129">Additional resources</span></span>
--------

[<span data-ttu-id="f18a7-130">Overzicht van Hoofdplannen en functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="f18a7-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="f18a7-131">Hoofdplanning voor locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="f18a7-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f18a7-132">Hoofdplanning voor locatiebehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="f18a7-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="f18a7-133">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="f18a7-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="f18a7-134">De stuklijstversie bepalen</span><span class="sxs-lookup"><span data-stu-id="f18a7-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]