---
title: Hoofdplanning voor locatiebehoefte, magazijn niet verplicht
description: In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatiedimensie is ingesteld voor de behoefteplanning.
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
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f4cde5c570148ca58c4ea583a8f538a72d4957d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987041"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="d4c31-103">Hoofdplanning voor locatiebehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="d4c31-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4c31-104">In dit onderwerp wordt beschreven hoe een artikel wordt gepland waarbij de locatiedimensie is ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="d4c31-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="d4c31-105">Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="d4c31-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="d4c31-106">De site-dimensie is ingesteld op verplicht en u moet deze invoeren voor de vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="d4c31-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="d4c31-107">De magazijndimensie is niet ingesteld als verplicht.</span><span class="sxs-lookup"><span data-stu-id="d4c31-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="d4c31-108">Het magazijn kan bekend zijn, maar wordt niet bij de berekening van de hoofdplanning gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d4c31-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="d4c31-109">De locatiedimensie is ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="d4c31-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="d4c31-110">De magazijndimensie is niet ingesteld voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="d4c31-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="d4c31-111">Vraag en aanbod worden daarom samengevoegd per site en mogelijk ook andere dimensies voor de behoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="d4c31-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="d4c31-112">In de volgende afbeelding ziet u hoe de hoofdplanning verdergaat.</span><span class="sxs-lookup"><span data-stu-id="d4c31-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="d4c31-113">In deze afbeelding wordt als volgt naar de volgende parameters en de locaties van die parameters verwezen:</span><span class="sxs-lookup"><span data-stu-id="d4c31-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="d4c31-114">De artikelbehoefteplanning wordt gedefinieerd voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="d4c31-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="d4c31-115">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="d4c31-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d4c31-116">Selecteer het artikel en klik vervolgens op **Plannen &gt; Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="d4c31-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="d4c31-117">Aanvullingsrelaties zijn gedefinieerd voor het magazijn.</span><span class="sxs-lookup"><span data-stu-id="d4c31-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="d4c31-118">Klik op **Voorraadbeheer &gt; Instellen &gt; Opsplitsing van voorraad &gt; Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="d4c31-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d4c31-119">Zie op het tabblad **Hoofdplanning** de veldgroep **Hoofdmagazijn**.</span><span class="sxs-lookup"><span data-stu-id="d4c31-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="d4c31-120">Het standaardordertype is ingesteld op Productie, Inkooporder of Kanban.</span><span class="sxs-lookup"><span data-stu-id="d4c31-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="d4c31-121">Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="d4c31-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d4c31-122">Selecteer het artikel en klik vervolgens op **Plannen &gt; Standaard orderinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="d4c31-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="d4c31-123">Raadpleeg in het formulier **Standaard orderinstellingen** het veld **Standaardordertype**.</span><span class="sxs-lookup"><span data-stu-id="d4c31-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Vraag naar locatie en magazijndekking niet verplicht](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="d4c31-125">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="d4c31-125">Additional resources</span></span>
--------

[<span data-ttu-id="d4c31-126">Overzicht van Hoofdplannen en functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="d4c31-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="d4c31-127">Hoofdplanning voor locatie- en magazijnbehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="d4c31-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d4c31-128">Hoofdplanning voor locatiebehoefte, magazijn verplicht</span><span class="sxs-lookup"><span data-stu-id="d4c31-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d4c31-129">Hoofdplanning voor locatiebehoefte, magazijn niet verplicht</span><span class="sxs-lookup"><span data-stu-id="d4c31-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d4c31-130">De stuklijstversie bepalen</span><span class="sxs-lookup"><span data-stu-id="d4c31-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



