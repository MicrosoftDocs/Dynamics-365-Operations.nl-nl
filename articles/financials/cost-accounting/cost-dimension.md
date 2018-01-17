---
title: Dimensies maken en dimensieleden importeren
description: Kostprijsboekhouding is een onafhankelijke module die hoofdgegevens uit andere modules nodig heeft.
author: YuyuScheller
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: dbf39ee7f64305596bdc57e9f63fe7a71bb5ecb0
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="d13dc-103">Dimensies maken en dimensieleden importeren</span><span class="sxs-lookup"><span data-stu-id="d13dc-103">Create dimensions and import dimension members</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d13dc-104">Kostprijsboekhouding is een onafhankelijke module die gegevens uit andere modules nodig heeft.</span><span class="sxs-lookup"><span data-stu-id="d13dc-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="d13dc-105">Deze gegevens worden ingedeeld in:</span><span class="sxs-lookup"><span data-stu-id="d13dc-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="d13dc-106">Kostenelementen</span><span class="sxs-lookup"><span data-stu-id="d13dc-106">Cost elements</span></span>
-  <span data-ttu-id="d13dc-107">Kostenobjecten</span><span class="sxs-lookup"><span data-stu-id="d13dc-107">Cost objects</span></span>
-  <span data-ttu-id="d13dc-108">Statistische dimensies</span><span class="sxs-lookup"><span data-stu-id="d13dc-108">Statistical dimensions</span></span>

<span data-ttu-id="d13dc-109">Een **kostenelement** correspondeert met een kostenrelevant artikel in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="d13dc-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="d13dc-110">Een **kostenobject** komt overeen met een soort financiële dimensie, zoals producten, kostenplaatsen en projecten die u wilt schatten, waaraan u kosten wilt toewijzen of die u rechtstreeks wilt meten.</span><span class="sxs-lookup"><span data-stu-id="d13dc-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="d13dc-111">Een **statistische dimensie** en de leden ervan worden gebruikt om niet-monetaire posten te registreren.</span><span class="sxs-lookup"><span data-stu-id="d13dc-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="d13dc-112">Leden van statistische dimensies kunnen worden gebruikt als een toewijzingsgrondslag in kostenverdeling en -toewijzing.</span><span class="sxs-lookup"><span data-stu-id="d13dc-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="d13dc-113">De volgende afbeelding illustreert de dimensies die worden gebruikt in Kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="d13dc-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="d13dc-114">[![Dimensies van kostprijsboekhouding](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="d13dc-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="d13dc-115">Nadat de gegevens in Kostprijsboekhouding zijn geïmporteerd, kunt u hiermee verschillende perspectieven ontwikkelen die managers inzicht bieden in alle niveaus van de organisatie.</span><span class="sxs-lookup"><span data-stu-id="d13dc-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="d13dc-116">De volgende onderwerpen bieden informatie over het maken van dimensies en het importeren van dimensieleden.</span><span class="sxs-lookup"><span data-stu-id="d13dc-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="d13dc-117">Dimensies van kostenelement</span><span class="sxs-lookup"><span data-stu-id="d13dc-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="d13dc-118">Kostenelementen maken (taakbegeleiding)</span><span class="sxs-lookup"><span data-stu-id="d13dc-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="d13dc-119">Dimensies van kostenobject</span><span class="sxs-lookup"><span data-stu-id="d13dc-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="d13dc-120">Kostenelementen maken (taakbegeleiding)</span><span class="sxs-lookup"><span data-stu-id="d13dc-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="d13dc-121">Dimensieleden van kostenelement toewijzen aan een gemeenschappelijke set van dimensieleden</span><span class="sxs-lookup"><span data-stu-id="d13dc-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="d13dc-122">Een dimensie van een kostenelement toewijzen (taakbegeleiding)</span><span class="sxs-lookup"><span data-stu-id="d13dc-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="d13dc-123">Statistische dimensieleden en sjablonen van provider van statistische maateenheden</span><span class="sxs-lookup"><span data-stu-id="d13dc-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)







