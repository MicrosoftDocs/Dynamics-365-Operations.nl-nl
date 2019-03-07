---
title: Levensduur van batchorder van aanmaakdatum tot startdatum
description: Deze procedure begeleidt u door het eerste gedeelte van de levensduur van een batchorder.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6484c1954ff4cc600938adb07b5384f1edce8bf7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "343116"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="edef5-103">Levensduur van batchorder van aanmaakdatum tot startdatum</span><span class="sxs-lookup"><span data-stu-id="edef5-103">Batch order lifecycle from create to start</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="edef5-104">Deze procedure begeleidt u door het eerste gedeelte van de levensduur van een batchorder.</span><span class="sxs-lookup"><span data-stu-id="edef5-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="edef5-105">Vanaf de creatie, de kostenraming en de productietaakplanning tot het werkelijke begin van een batchorder.</span><span class="sxs-lookup"><span data-stu-id="edef5-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="edef5-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="edef5-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="edef5-107">De vereisten voor het uitvoeren van de procedure met een andere dataset zijn een vrijgegeven product met een actieve formule en routeversie.</span><span class="sxs-lookup"><span data-stu-id="edef5-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="edef5-108">Een batchorder maken</span><span class="sxs-lookup"><span data-stu-id="edef5-108">Create a batch order</span></span>
1. <span data-ttu-id="edef5-109">Ga naar Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="edef5-109">Go to All production orders.</span></span>
2. <span data-ttu-id="edef5-110">Klik op Nieuwe batchorder.</span><span class="sxs-lookup"><span data-stu-id="edef5-110">Click New batch order.</span></span>
3. <span data-ttu-id="edef5-111">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="edef5-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="edef5-112">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="edef5-112">Click Create.</span></span>
5. <span data-ttu-id="edef5-113">Gebruik het snelfilter om in het veld Productie te filteren met de waarde 'b'.</span><span class="sxs-lookup"><span data-stu-id="edef5-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="edef5-114">Productieformule en verwachte co-producten weergeven</span><span class="sxs-lookup"><span data-stu-id="edef5-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="edef5-115">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="edef5-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="edef5-116">Klik op Formule.</span><span class="sxs-lookup"><span data-stu-id="edef5-116">Click Formula.</span></span>
3. <span data-ttu-id="edef5-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edef5-117">Close the page.</span></span>
4. <span data-ttu-id="edef5-118">Klik op Coproducten.</span><span class="sxs-lookup"><span data-stu-id="edef5-118">Click Co-products.</span></span>
5. <span data-ttu-id="edef5-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edef5-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="edef5-120">De batchvolgorde schatten</span><span class="sxs-lookup"><span data-stu-id="edef5-120">Estimate the batch order</span></span>
1. <span data-ttu-id="edef5-121">Klik op Raming.</span><span class="sxs-lookup"><span data-stu-id="edef5-121">Click Estimate.</span></span>
2. <span data-ttu-id="edef5-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edef5-122">Click OK.</span></span>
3. <span data-ttu-id="edef5-123">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="edef5-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="edef5-124">Klik op Berekeningsdetails weergeven.</span><span class="sxs-lookup"><span data-stu-id="edef5-124">Click View calculation details.</span></span>
5. <span data-ttu-id="edef5-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edef5-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="edef5-126">De batchvolgorde vrijgeven</span><span class="sxs-lookup"><span data-stu-id="edef5-126">Release the batch order</span></span>
1. <span data-ttu-id="edef5-127">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="edef5-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="edef5-128">Klik op Vrijgave.</span><span class="sxs-lookup"><span data-stu-id="edef5-128">Click Release.</span></span>
3. <span data-ttu-id="edef5-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edef5-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="edef5-130">Productietaken plannen</span><span class="sxs-lookup"><span data-stu-id="edef5-130">Schedule production jobs</span></span>
1. <span data-ttu-id="edef5-131">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="edef5-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="edef5-132">Klik op Taken plannen.</span><span class="sxs-lookup"><span data-stu-id="edef5-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="edef5-133">Selecteer Nee in het veld Eindige capaciteit.</span><span class="sxs-lookup"><span data-stu-id="edef5-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="edef5-134">Selecteer Nee in het veld Eindig materiaal.</span><span class="sxs-lookup"><span data-stu-id="edef5-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="edef5-135">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edef5-135">Click OK.</span></span>
6. <span data-ttu-id="edef5-136">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="edef5-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="edef5-137">Klik op Alle taken.</span><span class="sxs-lookup"><span data-stu-id="edef5-137">Click All jobs.</span></span>
8. <span data-ttu-id="edef5-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edef5-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="edef5-139">De batchorder starten</span><span class="sxs-lookup"><span data-stu-id="edef5-139">Start the batch order</span></span>
1. <span data-ttu-id="edef5-140">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="edef5-140">Click Start.</span></span>
2. <span data-ttu-id="edef5-141">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="edef5-141">Click the General tab.</span></span>
3. <span data-ttu-id="edef5-142">Selecteer Nee in het veld Orderverzamellijst nu boeken.</span><span class="sxs-lookup"><span data-stu-id="edef5-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="edef5-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="edef5-143">Click OK.</span></span>
5. <span data-ttu-id="edef5-144">Klik in het actievenster op Weergeven.</span><span class="sxs-lookup"><span data-stu-id="edef5-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="edef5-145">Klik op Orderverzamellijst.</span><span class="sxs-lookup"><span data-stu-id="edef5-145">Click Picking list.</span></span>
7. <span data-ttu-id="edef5-146">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="edef5-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="edef5-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edef5-147">Close the page.</span></span>
9. <span data-ttu-id="edef5-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edef5-148">Close the page.</span></span>
10. <span data-ttu-id="edef5-149">Klik op Routekaart.</span><span class="sxs-lookup"><span data-stu-id="edef5-149">Click Route card.</span></span>
11. <span data-ttu-id="edef5-150">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="edef5-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="edef5-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edef5-151">Close the page.</span></span>
13. <span data-ttu-id="edef5-152">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="edef5-152">Close the page.</span></span>

