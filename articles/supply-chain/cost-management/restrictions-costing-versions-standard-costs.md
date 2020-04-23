---
title: Beperkingen voor kostprijsberekeningsversies voor standaardkosten.
description: Dit onderwerp beschrijft de beperkingen die voor een kostprijsberekeningsversie voor standaardkosten gelden.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2348d7721cd281bb2a1b5af007c98ce69377a412
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214430"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="f663c-103">Beperkingen voor kostprijsberekeningsversies voor standaardkosten.</span><span class="sxs-lookup"><span data-stu-id="f663c-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f663c-104">Dit onderwerp beschrijft de beperkingen die voor een kostprijsberekeningsversie voor standaardkosten gelden.</span><span class="sxs-lookup"><span data-stu-id="f663c-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="f663c-105">De volgende beperkingen helpen zorgen dat de standaardprincipes voor kostprijsberekening worden gevolgd:</span><span class="sxs-lookup"><span data-stu-id="f663c-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="f663c-106">De kosten van een artikel moeten inclusief de toeslagen zijn.</span><span class="sxs-lookup"><span data-stu-id="f663c-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="f663c-107">De toeslagen voor een gefabriceerd artikel zijn de afgeschreven kosten in stuklijst- en routegegevens.</span><span class="sxs-lookup"><span data-stu-id="f663c-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="f663c-108">Daarom moeten de kosten in de eenheidskosten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f663c-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="f663c-109">De toeslagen voor een ingekocht artikel zijn ook in de eenheidskosten van het artikel opgenomen.</span><span class="sxs-lookup"><span data-stu-id="f663c-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="f663c-110">De berekening van de standaardkosten voor gefabriceerde artikelen moet zijn gebaseerd op de kostenrecords in een kostprijsberekeningsversie voor standaardkosten.</span><span class="sxs-lookup"><span data-stu-id="f663c-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="f663c-111">Alternatieve bronnen van kostengegevens kunnen alleen worden gebruikt bij een kostprijsberekeningsversie voor geplande kosten, zoals inkoopprijsovereenkomsten voor ingekochte artikelen.</span><span class="sxs-lookup"><span data-stu-id="f663c-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="f663c-112">Alternatieve bronnen van kostengegevens worden gedefinieerd door de stuklijstberekeningsgroep.</span><span class="sxs-lookup"><span data-stu-id="f663c-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="f663c-113">Stuklijstberekeningen moeten in een explosiemodus van een enkel niveau worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="f663c-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="f663c-114">De kostengegevens van een artikel voor standaardkosten kunnen worden gekopieerd naar een andere kostprijsberekeningsversie die standaardkosten of geplande kosten bevat.</span><span class="sxs-lookup"><span data-stu-id="f663c-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="f663c-115">De kostengegevens van een artikel voor geplande kosten kunnen echter niet worden gekopieerd naar een kostprijsberekeningsversie die standaardkosten bevat, omdat de eerder genoemde beperkingen niet voor geplande kosten gelden.</span><span class="sxs-lookup"><span data-stu-id="f663c-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="f663c-116">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="f663c-116">Related topics</span></span>
--------

[<span data-ttu-id="f663c-117">Overzicht van Kostprijsberekeningsversies</span><span class="sxs-lookup"><span data-stu-id="f663c-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="f663c-118">Standaardkosten in een niet-productieomgeving bijwerken</span><span class="sxs-lookup"><span data-stu-id="f663c-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="f663c-119">Voorbereiding van het onderhoud van standaardkosten voor gefabriceerde artikelen</span><span class="sxs-lookup"><span data-stu-id="f663c-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

