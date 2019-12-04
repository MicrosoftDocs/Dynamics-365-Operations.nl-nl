---
title: Hoofdplanning voor locatiebehoefte, magazijn niet verplicht
description: In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatiedimensie is ingesteld voor de behoefteplanning.
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43989f95764a60dc7f5662ef74c005c5fddaa275
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813726"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="b646f-103">Hoofdplanning voor locatiebehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="b646f-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b646f-104">In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatiedimensie is ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="b646f-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="b646f-105">Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="b646f-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b646f-106">De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="b646f-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b646f-107">De magazijndimensie is niet ingesteld als verplicht.</span><span class="sxs-lookup"><span data-stu-id="b646f-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="b646f-108">Het magazijn kan bekend zijn, maar wordt niet bij de berekening van de hoofdplanning gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b646f-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="b646f-109">De locatiedimensie is ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="b646f-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="b646f-110">De magazijndimensie is niet ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="b646f-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="b646f-111">Vraag en aanbod worden daarom samengevoegd per site en mogelijk ook andere dimensies voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="b646f-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="b646f-112">In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat.</span><span class="sxs-lookup"><span data-stu-id="b646f-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="b646f-113">In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:</span><span class="sxs-lookup"><span data-stu-id="b646f-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="b646f-114">De artikelbehoefteplanning wordt gedefinieerd voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="b646f-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="b646f-115">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="b646f-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b646f-116">Selecteer het artikel en klik vervolgens op **Plannen &gt; Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="b646f-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="b646f-117">Aanvullingsrelaties zijn gedefinieerd voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="b646f-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="b646f-118">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="b646f-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b646f-119">Zie op het tabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.</span><span class="sxs-lookup"><span data-stu-id="b646f-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="b646f-120">Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban.</span><span class="sxs-lookup"><span data-stu-id="b646f-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="b646f-121">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="b646f-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b646f-122">Selecteer het artikel en klik vervolgens op **Plannen &gt; Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="b646f-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="b646f-123">Raadpleeg in het formulier **Standaard orderinstellingen** het veld **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="b646f-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Vraag naar locatie en magazijndekking niet verplicht](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="b646f-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="b646f-125">Additional resources</span></span>
--------

[<span data-ttu-id="b646f-126">Overzicht van Hoofdplannen en functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="b646f-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="b646f-127">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="b646f-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b646f-128">Hoofdplanning voor locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="b646f-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b646f-129">Hoofdplanning voor locatiebehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="b646f-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b646f-130">De stuklijstversie bepalen</span><span class="sxs-lookup"><span data-stu-id="b646f-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



