---
title: Belastingen en zendingen plannen met behulp van de Workbench ladingplanning
description: In dit onderwerp wordt getoond hoe u de workbench voor ladingplanning kunt gebruiken om een lading te maken voor een verkooporder.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7966c6e445e0e44cd4ff8518926aa6b410502e13
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980430"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="c5206-103">Belastingen en zendingen plannen met behulp van de Workbench ladingplanning</span><span class="sxs-lookup"><span data-stu-id="c5206-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5206-104">In dit onderwerp wordt getoond hoe u de workbench voor ladingplanning kunt gebruiken om een lading te maken voor een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="c5206-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="c5206-105">Als vereiste maken we eerst de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="c5206-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="c5206-106">Deze procedure maakt deel uit van het dagelijks werk voor de transportcoördinator.</span><span class="sxs-lookup"><span data-stu-id="c5206-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="c5206-107">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="c5206-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="c5206-108">Verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="c5206-108">Create a sales order</span></span>
1. <span data-ttu-id="c5206-109">Ga naar **navigatiedeelvenster > Modules > Klanten > Orders > Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="c5206-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="c5206-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c5206-110">Select **New**.</span></span>
3. <span data-ttu-id="c5206-111">Selecteer in het veld **Klantrekening** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c5206-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c5206-112">Selecteer rekening **US-004**.</span><span class="sxs-lookup"><span data-stu-id="c5206-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="c5206-113">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5206-113">Select **OK**.</span></span>
6. <span data-ttu-id="c5206-114">Selecteer in het veld **Artikelnummer** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c5206-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c5206-115">Selecteer artikel **A0001**.</span><span class="sxs-lookup"><span data-stu-id="c5206-115">Select item **A0001**.</span></span> <span data-ttu-id="c5206-116">**A0001** is ingeschakeld voor transportbeheer.</span><span class="sxs-lookup"><span data-stu-id="c5206-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="c5206-117">Selecteer in het veld **Site** de vervolgkeuzeknop om de zoekopdracht te openen en selecteer vervolgens een artikel.</span><span class="sxs-lookup"><span data-stu-id="c5206-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="c5206-118">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="c5206-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="c5206-119">Typ '24' voor dit voorbeeld in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="c5206-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="c5206-120">Dit magazijn is ingeschakeld voor transportbeheer en geavanceerd magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="c5206-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="c5206-121">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c5206-121">Select **Save**.</span></span>
12. <span data-ttu-id="c5206-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c5206-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="c5206-123">Een nieuwe lading maken</span><span class="sxs-lookup"><span data-stu-id="c5206-123">Create a new load</span></span>
1. <span data-ttu-id="c5206-124">Ga naar het **navigatiedeelvenster > Modules > Transportbeheer > Planning > Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="c5206-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="c5206-125">Selecteer het tabblad **Verkoopregels**. Nu gaat u de lading samenstellen voor de verkooporder die u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c5206-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="c5206-126">Ladingen kunnen worden samengesteld op basis van de vraag en aanbod van inkooporders, transferorders en verkooporders.</span><span class="sxs-lookup"><span data-stu-id="c5206-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="c5206-127">Selecteer in het actievenster de optie **Vraag en aanbod**.</span><span class="sxs-lookup"><span data-stu-id="c5206-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="c5206-128">Selecteer **Naar nieuwe lading**.</span><span class="sxs-lookup"><span data-stu-id="c5206-128">Select **To new load**.</span></span>
5. <span data-ttu-id="c5206-129">Selecteer in het veld **Ladingsjabloon-id** de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c5206-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="c5206-130">De sjabloon voor laden definieert maximummetingen voor gewicht en volume van de volledige lading.</span><span class="sxs-lookup"><span data-stu-id="c5206-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="c5206-131">Zo kan de laadsjabloon bijvoorbeeld de grootte van een container of een vrachtwagen vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="c5206-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="c5206-132">Een artikel selecteren.</span><span class="sxs-lookup"><span data-stu-id="c5206-132">Select an item.</span></span>
6. <span data-ttu-id="c5206-133">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5206-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="c5206-134">Tarief en route voor lading bepalen</span><span class="sxs-lookup"><span data-stu-id="c5206-134">Rate and route the load</span></span>
1. <span data-ttu-id="c5206-135">Selecteer **Beoordeling en routering**.</span><span class="sxs-lookup"><span data-stu-id="c5206-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="c5206-136">Selecteer **Routetarief-workbench maken**.</span><span class="sxs-lookup"><span data-stu-id="c5206-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="c5206-137">Selecteer **Tariefwinkel**.</span><span class="sxs-lookup"><span data-stu-id="c5206-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="c5206-138">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="c5206-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c5206-139">Selecteer **Toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="c5206-139">Select **Assign**.</span></span>
6. <span data-ttu-id="c5206-140">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c5206-140">Close the page.</span></span>

