---
title: Beperkingen voor kostprijsberekeningsversies voor standaardkosten.
description: Dit onderwerp beschrijft de beperkingen die voor een kostprijsberekeningsversie voor standaardkosten gelden.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 84cb1b81d1ab6ac1e38b41f7f3f8629415f92926
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="58ab9-103">Beperkingen voor kostprijsberekeningsversies voor standaardkosten.</span><span class="sxs-lookup"><span data-stu-id="58ab9-103">Restrictions on costing versions for standard costs</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="58ab9-104">Dit onderwerp beschrijft de beperkingen die voor een kostprijsberekeningsversie voor standaardkosten gelden.</span><span class="sxs-lookup"><span data-stu-id="58ab9-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="58ab9-105">De volgende beperkingen helpen zorgen dat de standaardprincipes voor kostprijsberekening worden gevolgd:</span><span class="sxs-lookup"><span data-stu-id="58ab9-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="58ab9-106">De kosten van een artikel moeten inclusief de toeslagen zijn.</span><span class="sxs-lookup"><span data-stu-id="58ab9-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="58ab9-107">De toeslagen voor een gefabriceerd artikel zijn de afgeschreven kosten in stuklijst- en routegegevens.</span><span class="sxs-lookup"><span data-stu-id="58ab9-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="58ab9-108">Daarom moeten de kosten in de eenheidskosten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="58ab9-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="58ab9-109">De toeslagen voor een ingekocht artikel zijn ook in de eenheidskosten van het artikel opgenomen.</span><span class="sxs-lookup"><span data-stu-id="58ab9-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="58ab9-110">De berekening van de standaardkosten voor gefabriceerde artikelen moet zijn gebaseerd op de kostenrecords in een kostprijsberekeningsversie voor standaardkosten.</span><span class="sxs-lookup"><span data-stu-id="58ab9-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="58ab9-111">Alternatieve bronnen van kostengegevens kunnen alleen worden gebruikt bij een kostprijsberekeningsversie voor geplande kosten, zoals inkoopprijsovereenkomsten voor ingekochte artikelen.</span><span class="sxs-lookup"><span data-stu-id="58ab9-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="58ab9-112">Alternatieve bronnen van kostengegevens worden gedefinieerd door de stuklijstberekeningsgroep.</span><span class="sxs-lookup"><span data-stu-id="58ab9-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="58ab9-113">Stuklijstberekeningen moeten in een explosiemodus van een enkel niveau worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="58ab9-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="58ab9-114">De kostengegevens van een artikel voor standaardkosten kunnen worden gekopieerd naar een andere kostprijsberekeningsversie die standaardkosten of geplande kosten bevat.</span><span class="sxs-lookup"><span data-stu-id="58ab9-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="58ab9-115">De kostengegevens van een artikel voor geplande kosten kunnen echter niet worden gekopieerd naar een kostprijsberekeningsversie die standaardkosten bevat, omdat de eerder genoemde beperkingen niet voor geplande kosten gelden.</span><span class="sxs-lookup"><span data-stu-id="58ab9-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="58ab9-116">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="58ab9-116">Related topics</span></span>
--------

[<span data-ttu-id="58ab9-117">Kostprijsberekingsversies</span><span class="sxs-lookup"><span data-stu-id="58ab9-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="58ab9-118">Standaardkosten in een niet-productieomgeving bijwerken</span><span class="sxs-lookup"><span data-stu-id="58ab9-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="58ab9-119">Voorbereiding van het onderhoud van standaardkosten voor gefabriceerde artikelen</span><span class="sxs-lookup"><span data-stu-id="58ab9-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)


