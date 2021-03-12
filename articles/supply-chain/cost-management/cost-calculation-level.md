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
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967719"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="98eb4-104">Berekeningsniveau voor kosten</span><span class="sxs-lookup"><span data-stu-id="98eb4-104">Cost calculation level</span></span>

<span data-ttu-id="98eb4-105">Voor het stuklijstniveau met de naam **Berekeningsniveau voor kosten** worden productieorders en batchorders uitgesloten van de berekeningen.</span><span class="sxs-lookup"><span data-stu-id="98eb4-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="98eb4-106">Dit niveau wordt door het systeem gebruikt wanneer kostenberekeningen worden uitgevoerd in kostprijsberekeningsversies.</span><span class="sxs-lookup"><span data-stu-id="98eb4-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="98eb4-107">In processen zoals herberekening en voorraadafsluiting gebruikt het systeem **Kostprijsberekeningsniveau** van het stuklijstniveau in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="98eb4-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="98eb4-108">In het volgende eenvoudige scenario worden de verschillen weergegeven tussen het stuklijstniveau op het **Berekeningsniveau voor kosten** en het stuklijstniveau op het **Kostenniveau**.</span><span class="sxs-lookup"><span data-stu-id="98eb4-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="98eb4-109">U hebt drie producten: A, B en C. Product C is het onderdeel van product B en product B is het onderdeel van product A.</span><span class="sxs-lookup"><span data-stu-id="98eb4-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="98eb4-110">Op **Kostenniveau** worden de volgende stuklijstniveaus toegewezen:</span><span class="sxs-lookup"><span data-stu-id="98eb4-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="98eb4-111">**Product A:** 0</span><span class="sxs-lookup"><span data-stu-id="98eb4-111">**Product A:** 0</span></span>
    - <span data-ttu-id="98eb4-112">**Product B:** 1</span><span class="sxs-lookup"><span data-stu-id="98eb4-112">**Product B:** 1</span></span>
    - <span data-ttu-id="98eb4-113">**Product C:** 2</span><span class="sxs-lookup"><span data-stu-id="98eb4-113">**Product C:** 2</span></span>

- <span data-ttu-id="98eb4-114">Op **Berekeningsniveau kosten** worden de volgende stuklijstniveaus toegewezen:</span><span class="sxs-lookup"><span data-stu-id="98eb4-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="98eb4-115">**Product A:** 0</span><span class="sxs-lookup"><span data-stu-id="98eb4-115">**Product A:** 0</span></span>
    - <span data-ttu-id="98eb4-116">**Product B:** 1</span><span class="sxs-lookup"><span data-stu-id="98eb4-116">**Product B:** 1</span></span>
    - <span data-ttu-id="98eb4-117">**Product C:** 2</span><span class="sxs-lookup"><span data-stu-id="98eb4-117">**Product C:** 2</span></span>

<span data-ttu-id="98eb4-118">Er wordt dan een productieorder voor product C gemaakt en product A wordt toegevoegd aan de productieorderstuklijst.</span><span class="sxs-lookup"><span data-stu-id="98eb4-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="98eb4-119">Nadat de order is geraamd, worden stuklijstniveaus op de volgende manier bijgewerkt:</span><span class="sxs-lookup"><span data-stu-id="98eb4-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="98eb4-120">Op **Kostenniveau** worden de volgende stuklijstniveaus toegewezen:</span><span class="sxs-lookup"><span data-stu-id="98eb4-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="98eb4-121">**Product B:** 1</span><span class="sxs-lookup"><span data-stu-id="98eb4-121">**Product B:** 1</span></span>
    - <span data-ttu-id="98eb4-122">**Product C:** 2</span><span class="sxs-lookup"><span data-stu-id="98eb4-122">**Product C:** 2</span></span>
    - <span data-ttu-id="98eb4-123">**Product A:** 3</span><span class="sxs-lookup"><span data-stu-id="98eb4-123">**Product A:** 3</span></span>

- <span data-ttu-id="98eb4-124">Op **Berekeningsniveau kosten** worden de volgende stuklijstniveaus toegewezen:</span><span class="sxs-lookup"><span data-stu-id="98eb4-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="98eb4-125">**Product A:** 0</span><span class="sxs-lookup"><span data-stu-id="98eb4-125">**Product A:** 0</span></span>
    - <span data-ttu-id="98eb4-126">**Product B:** 1</span><span class="sxs-lookup"><span data-stu-id="98eb4-126">**Product B:** 1</span></span>
    - <span data-ttu-id="98eb4-127">**Product C:** 2</span><span class="sxs-lookup"><span data-stu-id="98eb4-127">**Product C:** 2</span></span>

<span data-ttu-id="98eb4-128">Op deze manier worden wijzigingen in de stuklijst van de productieorder niet beïnvloed door de daaropvolgende kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="98eb4-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
