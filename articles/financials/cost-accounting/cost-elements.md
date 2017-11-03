---
title: Dimensies van kostenelement
description: Kostenelementdimensies zijn een van de kernpijlers in Kostprijsboekhouding en worden gebruikt om te categoriseren en te traceren waar kosten heen stromen.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f47c75b6f6f4533501070f78698de82cf70f9bd
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="cost-element-dimensions"></a><span data-ttu-id="bea0a-103">Dimensies van kostenelement</span><span class="sxs-lookup"><span data-stu-id="bea0a-103">Cost element dimensions</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bea0a-104">Kostenelementdimensies zijn een van de kernpijlers in Kostprijsboekhouding en worden gebruikt om te categoriseren en te traceren waar kosten heen stromen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="bea0a-105">Een kostenelement correspondeert met een kostenrelevant artikel in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="bea0a-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="bea0a-106">Dit kan in principe elk type element zijn op het laagste niveau in een bedrijf, waar kosten heen kunnen stromen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="bea0a-107">Kostenelementen als concept kunnen variëren van grootboekrekeningen tot alle kostenrelevante resources.</span><span class="sxs-lookup"><span data-stu-id="bea0a-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="bea0a-108">Momenteel biedt Kostprijsboekhouding ondersteuning voor grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="bea0a-109">Twee typen kostenelementen</span><span class="sxs-lookup"><span data-stu-id="bea0a-109">Two types of cost elements</span></span>
<span data-ttu-id="bea0a-110">Er zijn twee typen kostenelementen: primaire kostenelementen en secundaire kostenelementen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="bea0a-111">In de volgende tabel worden de verschillen tussen de twee typen beschreven.</span><span class="sxs-lookup"><span data-stu-id="bea0a-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bea0a-112"><strong>Primaire kostenelementen</strong></span><span class="sxs-lookup"><span data-stu-id="bea0a-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="bea0a-113"><strong>Secundaire kostenelementen</strong></span><span class="sxs-lookup"><span data-stu-id="bea0a-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bea0a-114">De primaire kostenelementen vertegenwoordigen de stroom van kosten van financiële boekhouding naar kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="bea0a-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="bea0a-115">De kostenelementenstructuur correspondeert met de winst- verliesrekeningstructuur in het grootboek, waar een kostenelement kan corresponderen met een hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="bea0a-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="bea0a-116">Niet alle hoofdrekeningen hoeven als kostenelementen te zijn vertegenwoordigd, afhankelijk van de behoeften van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="bea0a-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="bea0a-117">Voorbeelden van primaire kostenelementen zijn onder meer:</span><span class="sxs-lookup"><span data-stu-id="bea0a-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="bea0a-118">Kosten van verkochte goederen</span><span class="sxs-lookup"><span data-stu-id="bea0a-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="bea0a-119">Indirecte materiaalkosten</span><span class="sxs-lookup"><span data-stu-id="bea0a-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="bea0a-120">Personeelskosten</span><span class="sxs-lookup"><span data-stu-id="bea0a-120">Personnel costs</span></span></li>
<li><span data-ttu-id="bea0a-121">Energiekosten</span><span class="sxs-lookup"><span data-stu-id="bea0a-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="bea0a-122">De secundaire kostenelementen vertegenwoordigen de interne stroom van kosten, omdat deze kosten alleen in Kostenprijsboekhouding worden gemaakt en gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bea0a-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="bea0a-123">Deze worden gebruikt om te borgen dat de oorsprong van kosten getraceerd kan worden.</span><span class="sxs-lookup"><span data-stu-id="bea0a-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="bea0a-124">Deze kostenelementen worden gebruikt in kostentoewijzingen en overheadberekeningen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="bea0a-125">Voorbeelden van secundaire kostenelementen zijn onder meer:</span><span class="sxs-lookup"><span data-stu-id="bea0a-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="bea0a-126">Productiekosten</span><span class="sxs-lookup"><span data-stu-id="bea0a-126">Production costs</span></span></li>
<li><span data-ttu-id="bea0a-127">Overheadkosten voor productie, materiaal, en marketing</span><span class="sxs-lookup"><span data-stu-id="bea0a-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="bea0a-128">Dimensies van kostenelementen en dimensieleden van kostenelementen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="bea0a-129">Kostenelementen worden ook aangeduid als *kostenelementendimensies*.</span><span class="sxs-lookup"><span data-stu-id="bea0a-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="bea0a-130">De individuele dimensiewaarden staan bekend als *kostenelementdimensieleden*.</span><span class="sxs-lookup"><span data-stu-id="bea0a-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="bea0a-131">Stel dat u een rekeningschemastructuur hebt, die de basis voor de wettelijk voorgeschreven rapportage vormt.</span><span class="sxs-lookup"><span data-stu-id="bea0a-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="bea0a-132">Deze structuur wordt gebruikt als de kostenelementendimensie.</span><span class="sxs-lookup"><span data-stu-id="bea0a-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="bea0a-133">De rekeningen, die de primaire kostenelementen vormen, zijn vertegenwoordigd als de kostenelementendimensieleden in Kostprijsboekhouding.</span><span class="sxs-lookup"><span data-stu-id="bea0a-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="bea0a-134">In de onderstaande schermopname ziet u een voorbeeld van Hoofdrekeningen als de kostenelementdimensie met de werkelijke hoofdrekeningen als kostenelementdimensieleden.</span><span class="sxs-lookup"><span data-stu-id="bea0a-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="bea0a-135">[![dimensies-kostenelement](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="bea0a-135">[![cost-element-dimensions](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="bea0a-136">Kostenelementdimensieleden importeren door middel van gegevensconnectors</span><span class="sxs-lookup"><span data-stu-id="bea0a-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="bea0a-137">Om gemakkelijker leden van kostenelementdimensies te kunnen configureren in Kostenprijsboekhouding, kunt u met vooraf gemaakte gegevensconnectors of zelf samengestelde connectors de primaire kostenelementen ophalen vanuit een of meer bronsystemen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="bea0a-138">Implementatieoverwegingen</span><span class="sxs-lookup"><span data-stu-id="bea0a-138">Implementation considerations</span></span>
<span data-ttu-id="bea0a-139">Omdat kostenelementen het laagste niveau van kostendetails vertegenwoordigen, moet u ervoor zorgen dat alle kostenelementen die zijn vereist om de managementrapporten aan maken, zijn opgenomen wanneer u de kostenelementenstructuur implementeert.</span><span class="sxs-lookup"><span data-stu-id="bea0a-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="bea0a-140">Het kan lastig zijn om een gepast aantal kostenelementen voor kostenbeheer te bepalen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="bea0a-141">Als u duizenden kostenelementen hebt, kan moeilijk zijn om elk kostenelement te beheersen.</span><span class="sxs-lookup"><span data-stu-id="bea0a-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="bea0a-142">Eventueel kunt u kostenelementen groeperen en kostenbeheer uitvoeren op een samengevoegd niveau.</span><span class="sxs-lookup"><span data-stu-id="bea0a-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>




