---
title: Een productieorder starten
description: Deze procedure toont hoe u een productieorder start op de werkvloer.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f83091a9f3e96a9176860bd16fa5969507488a25
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "346221"
---
# <a name="start-a-production-order"></a><span data-ttu-id="71bf9-103">Een productieorder starten</span><span class="sxs-lookup"><span data-stu-id="71bf9-103">Start a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71bf9-104">Deze procedure toont hoe u een productieorder start op de werkvloer.</span><span class="sxs-lookup"><span data-stu-id="71bf9-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="71bf9-105">Tijd- en materiaalverbruik worden in dit proces gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="71bf9-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="71bf9-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="71bf9-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="71bf9-107">Dit is de vijfde procedure van zeven waarin de levenscyclus van de productieorder wordt uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="71bf9-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="71bf9-108">Een productieorder starten</span><span class="sxs-lookup"><span data-stu-id="71bf9-108">Start a production order</span></span>
1. <span data-ttu-id="71bf9-109">Ga naar Productiebeheer > Productieorders > Alle productieorders.</span><span class="sxs-lookup"><span data-stu-id="71bf9-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="71bf9-110">Selecteer een productieorder met de status Vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="71bf9-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="71bf9-111">Klik in het actievenster op Productieorder.</span><span class="sxs-lookup"><span data-stu-id="71bf9-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="71bf9-112">Klik op Start.</span><span class="sxs-lookup"><span data-stu-id="71bf9-112">Click Start.</span></span>
    * <span data-ttu-id="71bf9-113">Op deze pagina kunt u de start van de productieorder bevestigen.</span><span class="sxs-lookup"><span data-stu-id="71bf9-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="71bf9-114">Klik op het tabblad Algemeen.</span><span class="sxs-lookup"><span data-stu-id="71bf9-114">Click the General tab.</span></span>
5. <span data-ttu-id="71bf9-115">Voer in het veld Van</span><span class="sxs-lookup"><span data-stu-id="71bf9-115">In the From Oper.</span></span> <span data-ttu-id="71bf9-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="71bf9-116">No.</span></span> <span data-ttu-id="71bf9-117">'10' in.</span><span class="sxs-lookup"><span data-stu-id="71bf9-117">field, enter '10'.</span></span>
6. <span data-ttu-id="71bf9-118">Selecteer 'Altijd' in het veld Automatisch routeverbruik.</span><span class="sxs-lookup"><span data-stu-id="71bf9-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="71bf9-119">Klik op het selectievakje Routekaart nu boeken.</span><span class="sxs-lookup"><span data-stu-id="71bf9-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="71bf9-120">Selecteer 'Altijd' in het veld Automatisch stuklijstverbruik.</span><span class="sxs-lookup"><span data-stu-id="71bf9-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="71bf9-121">Klik op het selectievakje Orderverzamellijst nu boeken.</span><span class="sxs-lookup"><span data-stu-id="71bf9-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="71bf9-122">Klik op het selectievakje Orderverzamellijst afdrukken.</span><span class="sxs-lookup"><span data-stu-id="71bf9-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="71bf9-123">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="71bf9-123">Click OK.</span></span>
    * <span data-ttu-id="71bf9-124">Dit is de afgedrukte orderverzamellijst die de materialen bevat die worden gebruikt voor de productieorder.</span><span class="sxs-lookup"><span data-stu-id="71bf9-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="71bf9-125">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71bf9-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="71bf9-126">De orderverzamellijst valideren</span><span class="sxs-lookup"><span data-stu-id="71bf9-126">Validate the picking list</span></span>
1. <span data-ttu-id="71bf9-127">Klik in het actievenster op Weergeven.</span><span class="sxs-lookup"><span data-stu-id="71bf9-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="71bf9-128">Klik op Orderverzamellijst.</span><span class="sxs-lookup"><span data-stu-id="71bf9-128">Click Picking list.</span></span>
3. <span data-ttu-id="71bf9-129">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="71bf9-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="71bf9-130">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="71bf9-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="71bf9-131">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="71bf9-131">Click Edit.</span></span>
6. <span data-ttu-id="71bf9-132">Voer een getal in het veld Verbruik in.</span><span class="sxs-lookup"><span data-stu-id="71bf9-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="71bf9-133">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="71bf9-133">Click Post.</span></span>
8. <span data-ttu-id="71bf9-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="71bf9-134">Click OK.</span></span>
    * <span data-ttu-id="71bf9-135">In het orderverzamellijstjournaal worden de materialen geboekt die worden verbruikt door de productieorder.</span><span class="sxs-lookup"><span data-stu-id="71bf9-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="71bf9-136">Voordat u het journaal boekt, kunt u correcties aanbrengen als er een verschil is tussen de geschatte hoeveelheid en de werkelijke verbruikte hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="71bf9-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="71bf9-137">Klik op het tabblad Rasterdeelvenster.</span><span class="sxs-lookup"><span data-stu-id="71bf9-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="71bf9-138">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="71bf9-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="71bf9-139">Het routekaartjournaal verifiëren</span><span class="sxs-lookup"><span data-stu-id="71bf9-139">Verify the route card journal</span></span>
1. <span data-ttu-id="71bf9-140">Klik in het actievenster op Weergeven.</span><span class="sxs-lookup"><span data-stu-id="71bf9-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="71bf9-141">Klik op Routekaart.</span><span class="sxs-lookup"><span data-stu-id="71bf9-141">Click Route card.</span></span>
3. <span data-ttu-id="71bf9-142">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="71bf9-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="71bf9-143">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="71bf9-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="71bf9-144">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="71bf9-144">Click Edit.</span></span>
6. <span data-ttu-id="71bf9-145">Voer een getal in het veld Uren in.</span><span class="sxs-lookup"><span data-stu-id="71bf9-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="71bf9-146">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="71bf9-146">Click Post.</span></span>
8. <span data-ttu-id="71bf9-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="71bf9-147">Click OK.</span></span>
    * <span data-ttu-id="71bf9-148">In het routekaartjournaal wordt de bestede tijd voor de afzonderlijke bewerkingen vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="71bf9-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="71bf9-149">Goede en foutieve hoeveelheid kan ook worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="71bf9-149">Good and error quantity can also be reported.</span></span>  
