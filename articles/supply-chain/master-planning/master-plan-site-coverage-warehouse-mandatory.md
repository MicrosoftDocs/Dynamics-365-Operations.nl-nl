---
title: Hoofdplanning voor locatiebehoefte, magazijn verplicht
description: In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatie is ingesteld als behoeftedimensie. De magazijndimensie is verplicht.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f61c142fff73fdeeca573cca3f54e654511af1e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556407"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="f98b7-104">Hoofdplanning voor locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="f98b7-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f98b7-105">In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatie is ingesteld als behoeftedimensie.</span><span class="sxs-lookup"><span data-stu-id="f98b7-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="f98b7-106">De magazijndimensie is verplicht.</span><span class="sxs-lookup"><span data-stu-id="f98b7-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="f98b7-107">Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="f98b7-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="f98b7-108">De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="f98b7-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="f98b7-109">Deze instelling kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="f98b7-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="f98b7-110">De magazijndimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="f98b7-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="f98b7-111">De locatiedimensie is ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="f98b7-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="f98b7-112">U kunt ook andere dimensies instellen voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="f98b7-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="f98b7-113">De functionaliteit voor meerdere locaties is echter niet van invloed op deze dimensies.</span><span class="sxs-lookup"><span data-stu-id="f98b7-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="f98b7-114">De magazijndimensie is niet ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="f98b7-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="f98b7-115">Vraag en aanbod worden daarom samengevoegd per site en mogelijk ook andere dimensies voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="f98b7-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="f98b7-116">In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat.</span><span class="sxs-lookup"><span data-stu-id="f98b7-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="f98b7-117">In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:</span><span class="sxs-lookup"><span data-stu-id="f98b7-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="f98b7-118">De artikelbehoefteplanning wordt gedefinieerd voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="f98b7-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="f98b7-119">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="f98b7-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f98b7-120">Selecteer het artikel en klik vervolgens op **Plannen &gt; Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="f98b7-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="f98b7-121">Aanvullingsrelaties zijn gedefinieerd voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="f98b7-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="f98b7-122">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="f98b7-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="f98b7-123">Zie op het tabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.</span><span class="sxs-lookup"><span data-stu-id="f98b7-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="f98b7-124">Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban.</span><span class="sxs-lookup"><span data-stu-id="f98b7-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="f98b7-125">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="f98b7-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="f98b7-126">Selecteer het artikel en klik vervolgens op **Plannen &gt; Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="f98b7-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="f98b7-127">Zie in het formulier **Standaard orderinstellingen** het **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="f98b7-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Vraag naar locatie en magazijndekking verplicht](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="f98b7-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="f98b7-129">Additional resources</span></span>
--------

[<span data-ttu-id="f98b7-130">Hoofdplanning en de functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="f98b7-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="f98b7-131">Hoofdplanning - locatie en magazijnbehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="f98b7-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f98b7-132">Hoofdplanning - locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="f98b7-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="f98b7-133">Hoofdplanning - locatie- en magazijnbehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="f98b7-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="f98b7-134">Hoofdplanning - hoe de stuklijstversie wordt bepaald</span><span class="sxs-lookup"><span data-stu-id="f98b7-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



