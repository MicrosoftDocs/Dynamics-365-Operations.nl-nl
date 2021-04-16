---
title: Levensduur van batchorder van aanmaakdatum tot startdatum
description: Deze procedure begeleidt u door het eerste gedeelte van de levensduur van een batchorder.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d9ed44c9e05ea815e78ae041234ad61f76d89d8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825033"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="00f85-103">Levensduur van batchorder van aanmaakdatum tot startdatum</span><span class="sxs-lookup"><span data-stu-id="00f85-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00f85-104">Deze procedure begeleidt u door het eerste gedeelte van de levensduur van een batchorder.</span><span class="sxs-lookup"><span data-stu-id="00f85-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="00f85-105">Vanaf de creatie, de kostenraming en de productietaakplanning tot het werkelijke begin van een batchorder.</span><span class="sxs-lookup"><span data-stu-id="00f85-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="00f85-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="00f85-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="00f85-107">De vereisten voor het uitvoeren van de procedure met een andere dataset zijn een vrijgegeven product met een actieve formule en routeversie.</span><span class="sxs-lookup"><span data-stu-id="00f85-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="00f85-108">Een batchorder maken</span><span class="sxs-lookup"><span data-stu-id="00f85-108">Create a batch order</span></span>
1. <span data-ttu-id="00f85-109">Ga naar Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="00f85-109">Go to All production orders.</span></span>
2. <span data-ttu-id="00f85-110">Klik op Nieuwe batchorder.</span><span class="sxs-lookup"><span data-stu-id="00f85-110">Click New batch order.</span></span>
3. <span data-ttu-id="00f85-111">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="00f85-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="00f85-112">Klik op Maken.</span><span class="sxs-lookup"><span data-stu-id="00f85-112">Click Create.</span></span>
5. <span data-ttu-id="00f85-113">Gebruik het snelfilter om in het veld Productie te filteren met de waarde 'b'.</span><span class="sxs-lookup"><span data-stu-id="00f85-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="00f85-114">Productieformule en verwachte co-producten weergeven</span><span class="sxs-lookup"><span data-stu-id="00f85-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="00f85-115">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="00f85-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="00f85-116">Klik op Formule.</span><span class="sxs-lookup"><span data-stu-id="00f85-116">Click Formula.</span></span>
3. <span data-ttu-id="00f85-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00f85-117">Close the page.</span></span>
4. <span data-ttu-id="00f85-118">Klik op Coproducten.</span><span class="sxs-lookup"><span data-stu-id="00f85-118">Click Co-products.</span></span>
5. <span data-ttu-id="00f85-119">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00f85-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="00f85-120">De batchvolgorde schatten</span><span class="sxs-lookup"><span data-stu-id="00f85-120">Estimate the batch order</span></span>
1. <span data-ttu-id="00f85-121">Klik op Raming.</span><span class="sxs-lookup"><span data-stu-id="00f85-121">Click Estimate.</span></span>
2. <span data-ttu-id="00f85-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="00f85-122">Click OK.</span></span>
3. <span data-ttu-id="00f85-123">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="00f85-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="00f85-124">Klik op Berekeningsdetails weergeven.</span><span class="sxs-lookup"><span data-stu-id="00f85-124">Click View calculation details.</span></span>
5. <span data-ttu-id="00f85-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00f85-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="00f85-126">De batchvolgorde vrijgeven</span><span class="sxs-lookup"><span data-stu-id="00f85-126">Release the batch order</span></span>
1. <span data-ttu-id="00f85-127">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="00f85-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="00f85-128">Klik op Vrijgave.</span><span class="sxs-lookup"><span data-stu-id="00f85-128">Click Release.</span></span>
3. <span data-ttu-id="00f85-129">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="00f85-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="00f85-130">Productietaken plannen</span><span class="sxs-lookup"><span data-stu-id="00f85-130">Schedule production jobs</span></span>
1. <span data-ttu-id="00f85-131">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="00f85-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="00f85-132">Klik op Taken plannen.</span><span class="sxs-lookup"><span data-stu-id="00f85-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="00f85-133">Selecteer Nee in het veld Eindige capaciteit.</span><span class="sxs-lookup"><span data-stu-id="00f85-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="00f85-134">Selecteer Nee in het veld Eindig materiaal.</span><span class="sxs-lookup"><span data-stu-id="00f85-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="00f85-135">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="00f85-135">Click OK.</span></span>
6. <span data-ttu-id="00f85-136">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="00f85-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="00f85-137">Klik op Alle taken.</span><span class="sxs-lookup"><span data-stu-id="00f85-137">Click All jobs.</span></span>
8. <span data-ttu-id="00f85-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00f85-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="00f85-139">De batchorder starten</span><span class="sxs-lookup"><span data-stu-id="00f85-139">Start the batch order</span></span>
1. <span data-ttu-id="00f85-140">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="00f85-140">Click Start.</span></span>
2. <span data-ttu-id="00f85-141">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="00f85-141">Click the General tab.</span></span>
3. <span data-ttu-id="00f85-142">Selecteer Nee in het veld Orderverzamellijst nu boeken.</span><span class="sxs-lookup"><span data-stu-id="00f85-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="00f85-143">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="00f85-143">Click OK.</span></span>
5. <span data-ttu-id="00f85-144">Klik in het actievenster op Weergeven.</span><span class="sxs-lookup"><span data-stu-id="00f85-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="00f85-145">Klik op Orderverzamellijst.</span><span class="sxs-lookup"><span data-stu-id="00f85-145">Click Picking list.</span></span>
7. <span data-ttu-id="00f85-146">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="00f85-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="00f85-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00f85-147">Close the page.</span></span>
9. <span data-ttu-id="00f85-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00f85-148">Close the page.</span></span>
10. <span data-ttu-id="00f85-149">Klik op Routekaart.</span><span class="sxs-lookup"><span data-stu-id="00f85-149">Click Route card.</span></span>
11. <span data-ttu-id="00f85-150">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="00f85-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="00f85-151">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00f85-151">Close the page.</span></span>
13. <span data-ttu-id="00f85-152">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="00f85-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]