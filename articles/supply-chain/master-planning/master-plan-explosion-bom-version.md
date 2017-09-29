---
title: Explosie van een stuklijstversie
description: In dit artikel wordt een hoofdplanningsscenario uitgelegd dat betrekking heeft op de explosie van een stuklijstversie.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8c633e09103c45aff5614270a94a3bfe4fc5e20
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="552d7-103">Explosie van een stuklijstversie</span><span class="sxs-lookup"><span data-stu-id="552d7-103">Explosion of a BOM version</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="552d7-104">In dit artikel wordt een hoofdplanningsscenario uitgelegd dat betrekking heeft op de explosie van een stuklijstversie.</span><span class="sxs-lookup"><span data-stu-id="552d7-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="552d7-105">Een vraagexplosie van een stuklijstversie maakt een vraag voor elk stuklijstregelartikel op een bepaalde locatie en mogelijk in een bepaald magazijn.</span><span class="sxs-lookup"><span data-stu-id="552d7-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="552d7-106">In een locatiespecifieke stuklijst kan een specifiek magazijn worden gedefinieerd voor elke stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="552d7-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="552d7-107">Bovendien bepalen de dimensie-instellingen van het artikel voor elke stuklijstregel of het magazijn al dan niet nodig is.</span><span class="sxs-lookup"><span data-stu-id="552d7-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="552d7-108">De resulterende vraag voor elk stuklijstregelartikel wordt dan het beginpunt voor extra vraagexplosies.</span><span class="sxs-lookup"><span data-stu-id="552d7-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="552d7-109">Voor dit hoofdplanningsscenario gelden de volgende voorwaarden:</span><span class="sxs-lookup"><span data-stu-id="552d7-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="552d7-110">De locatiedimensie is verplicht en moet bij de vraagtransactie worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="552d7-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="552d7-111">De sitedimensie is consistent.</span><span class="sxs-lookup"><span data-stu-id="552d7-111">The site dimension is consistent.</span></span> <span data-ttu-id="552d7-112">De site voor een vraag op een lager niveau is hetzelfde als de site bij de eerste vraagtransactie.</span><span class="sxs-lookup"><span data-stu-id="552d7-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="552d7-113">In de volgende afbeelding ziet u het proces voor de vraagexplosie van de hoofdplanning.</span><span class="sxs-lookup"><span data-stu-id="552d7-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Vraagexplosie met stuklijstversie](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="552d7-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="552d7-115">See also</span></span>
--------

[<span data-ttu-id="552d7-116">Hoofdplanning - hoe de stuklijstversie wordt bepaald</span><span class="sxs-lookup"><span data-stu-id="552d7-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="552d7-117">Hoofdplanning en de functionaliteit voor meerdere locaties</span><span class="sxs-lookup"><span data-stu-id="552d7-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




