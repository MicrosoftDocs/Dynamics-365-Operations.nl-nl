---
title: Berekeningsniveau voor kosten
description: Dit onderwerp beschrijft het stuklijstniveau met de naam Kostenberekeningsniveau. Op dit stuklijstniveau worden productie- en batchorders uitgesloten van de berekeningen.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251021"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="0dcba-104">Berekeningsniveau voor kosten</span><span class="sxs-lookup"><span data-stu-id="0dcba-104">Cost calculation level</span></span>

<span data-ttu-id="0dcba-105">Voor het stuklijstniveau met de naam **Berekeningsniveau voor kosten** worden productieorders en batchorders uitgesloten van de berekeningen.</span><span class="sxs-lookup"><span data-stu-id="0dcba-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="0dcba-106">Dit niveau wordt door het systeem gebruikt wanneer kostenberekeningen worden uitgevoerd in kostprijsberekeningsversies.</span><span class="sxs-lookup"><span data-stu-id="0dcba-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="0dcba-107">In processen zoals herberekening en voorraadafsluiting gebruikt het systeem **Kostprijsberekeningsniveau** van het stuklijstniveau in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="0dcba-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="0dcba-108">In het volgende eenvoudige scenario worden de verschillen weergegeven tussen het stuklijstniveau op het **Berekeningsniveau voor kosten** en het stuklijstniveau op het **Kostenniveau**.</span><span class="sxs-lookup"><span data-stu-id="0dcba-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="0dcba-109">U hebt drie producten: A, B en C. Product C is het onderdeel van product B en product B is het onderdeel van product A.</span><span class="sxs-lookup"><span data-stu-id="0dcba-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="0dcba-110">Op **Kostenniveau** worden de volgende stuklijstniveaus toegewezen:</span><span class="sxs-lookup"><span data-stu-id="0dcba-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="0dcba-111">**Product A:** 0</span><span class="sxs-lookup"><span data-stu-id="0dcba-111">**Product A:** 0</span></span>
    - <span data-ttu-id="0dcba-112">**Product B:** 1</span><span class="sxs-lookup"><span data-stu-id="0dcba-112">**Product B:** 1</span></span>
    - <span data-ttu-id="0dcba-113">**Product C:** 2</span><span class="sxs-lookup"><span data-stu-id="0dcba-113">**Product C:** 2</span></span>

- <span data-ttu-id="0dcba-114">Op **Berekeningsniveau kosten** worden de volgende stuklijstniveaus toegewezen:</span><span class="sxs-lookup"><span data-stu-id="0dcba-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="0dcba-115">**Product A:** 0</span><span class="sxs-lookup"><span data-stu-id="0dcba-115">**Product A:** 0</span></span>
    - <span data-ttu-id="0dcba-116">**Product B:** 1</span><span class="sxs-lookup"><span data-stu-id="0dcba-116">**Product B:** 1</span></span>
    - <span data-ttu-id="0dcba-117">**Product C:** 2</span><span class="sxs-lookup"><span data-stu-id="0dcba-117">**Product C:** 2</span></span>

<span data-ttu-id="0dcba-118">Er wordt dan een productieorder voor product C gemaakt en product A wordt toegevoegd aan de productieorderstuklijst.</span><span class="sxs-lookup"><span data-stu-id="0dcba-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="0dcba-119">Nadat de order is geraamd, worden stuklijstniveaus op de volgende manier bijgewerkt:</span><span class="sxs-lookup"><span data-stu-id="0dcba-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="0dcba-120">Op **Kostenniveau** worden de volgende stuklijstniveaus toegewezen:</span><span class="sxs-lookup"><span data-stu-id="0dcba-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="0dcba-121">**Product B:** 1</span><span class="sxs-lookup"><span data-stu-id="0dcba-121">**Product B:** 1</span></span>
    - <span data-ttu-id="0dcba-122">**Product C:** 2</span><span class="sxs-lookup"><span data-stu-id="0dcba-122">**Product C:** 2</span></span>
    - <span data-ttu-id="0dcba-123">**Product A:** 3</span><span class="sxs-lookup"><span data-stu-id="0dcba-123">**Product A:** 3</span></span>

- <span data-ttu-id="0dcba-124">Op **Berekeningsniveau kosten** worden de volgende stuklijstniveaus toegewezen:</span><span class="sxs-lookup"><span data-stu-id="0dcba-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="0dcba-125">**Product A:** 0</span><span class="sxs-lookup"><span data-stu-id="0dcba-125">**Product A:** 0</span></span>
    - <span data-ttu-id="0dcba-126">**Product B:** 1</span><span class="sxs-lookup"><span data-stu-id="0dcba-126">**Product B:** 1</span></span>
    - <span data-ttu-id="0dcba-127">**Product C:** 2</span><span class="sxs-lookup"><span data-stu-id="0dcba-127">**Product C:** 2</span></span>

<span data-ttu-id="0dcba-128">Op deze manier worden wijzigingen in de stuklijst van de productieorder niet beïnvloed door de daaropvolgende kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="0dcba-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]