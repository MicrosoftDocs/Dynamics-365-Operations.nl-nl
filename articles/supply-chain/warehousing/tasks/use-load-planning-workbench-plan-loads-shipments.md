--- 
title: Belastingen en zendingen plannen met behulp van de Workbench ladingplanning
description: Deze procedure laat zien hoe u de workbench voor ladingplanning kunt gebruiken om een lading te maken voor een verkooporder.
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="4aaf2-103">Belastingen en zendingen plannen met behulp van de Workbench ladingplanning</span><span class="sxs-lookup"><span data-stu-id="4aaf2-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4aaf2-104">Deze procedure laat zien hoe u de workbench voor ladingplanning kunt gebruiken om een lading te maken voor een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="4aaf2-105">Als vereiste maken we eerst de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="4aaf2-106">Deze procedure maakt deel uit van het dagelijks werk voor de transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="4aaf2-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="4aaf2-108">Verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="4aaf2-108">Create a sales order</span></span>
1. <span data-ttu-id="4aaf2-109">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="4aaf2-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-110">Click New.</span></span>
3. <span data-ttu-id="4aaf2-111">Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4aaf2-112">Selecteer rekening US-004.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-112">Select account US-004.</span></span>
5. <span data-ttu-id="4aaf2-113">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-113">Click OK.</span></span>
6. <span data-ttu-id="4aaf2-114">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4aaf2-115">Selecteer artikel A0001.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-115">Select item A0001.</span></span>
    * <span data-ttu-id="4aaf2-116">A0001 is ingeschakeld voor transportbeheer.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="4aaf2-117">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="4aaf2-118">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="4aaf2-119">Typ "24" in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="4aaf2-120">Selecteer in dit voorbeeld magazijn 24.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-120">In this example select warehouse 24.</span></span> <span data-ttu-id="4aaf2-121">Dit magazijn is ingeschakeld voor transportbeheer en geavanceerd magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="4aaf2-122">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-122">Click Save.</span></span>
12. <span data-ttu-id="4aaf2-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="4aaf2-124">Een nieuwe lading maken</span><span class="sxs-lookup"><span data-stu-id="4aaf2-124">Create a new load</span></span>
1. <span data-ttu-id="4aaf2-125">Ga naar Transportbeheer > Planning > Workbench van ladingplanning.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="4aaf2-126">Klik op het tabblad Verkoopregels.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="4aaf2-127">Nu gaat u de lading samenstellen voor de verkooporder die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="4aaf2-128">Ladingen kunnen worden samengesteld op basis van de vraag en aanbod van inkooporders, transferorders en verkooporders.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="4aaf2-129">Klik in het actievenster op Vraag en aanbod.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="4aaf2-130">Klik op Naar nieuwe lading.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-130">Click To new load.</span></span>
5. <span data-ttu-id="4aaf2-131">Klik in het veld Ladingsjabloon-id op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4aaf2-132">De sjabloon voor laden definieert maximummetingen voor gewicht en volume van de volledige lading.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="4aaf2-133">Zo kan de laadsjabloon bijvoorbeeld de grootte van een container of een vrachtwagen vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="4aaf2-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4aaf2-135">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="4aaf2-136">Tarief en route voor lading bepalen</span><span class="sxs-lookup"><span data-stu-id="4aaf2-136">Rate and route the load</span></span>
1. <span data-ttu-id="4aaf2-137">Klik op Classificatie en routering.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="4aaf2-138">Klik op Workbench tariefroute.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="4aaf2-139">Klik op Tariefwinkel.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-139">Click Rate shop.</span></span>
4. <span data-ttu-id="4aaf2-140">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4aaf2-141">Klik op Toewijzen.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-141">Click Assign.</span></span>
6. <span data-ttu-id="4aaf2-142">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-142">Close the page.</span></span>
7. <span data-ttu-id="4aaf2-143">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4aaf2-143">Close the page.</span></span>


