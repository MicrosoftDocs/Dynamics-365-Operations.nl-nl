---
title: Phantom-artikelen
description: In dit onderwerp wordt gedetailleerd beschreven hoe het regeltype Phantom kan worden gebruikt voor de regels van een stuklijst en een formule in Dynamics 365 Supply Chain Management.
author: ShylaThompson
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 1118d7334602e450e5d503632895f73ba19066a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814773"
---
# <a name="phantom-items"></a><span data-ttu-id="01146-103">Phantom-artikelen</span><span class="sxs-lookup"><span data-stu-id="01146-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01146-104">In dit onderwerp wordt gedetailleerd beschreven hoe het regeltype Phantom kan worden gebruikt voor de regels van een stuklijst en een formule.</span><span class="sxs-lookup"><span data-stu-id="01146-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="01146-105">In de volgende afbeelding is (a) de stuklijst voor het product H en de onderdelen F en G, en is (b) het routeblad voor product H en onderdeel F.</span><span class="sxs-lookup"><span data-stu-id="01146-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Product H en onderdeel F](media/product-H-part-F.png)


<span data-ttu-id="01146-107">In deze afbeelding wordt een voorbeeld van een stuklijststructuur op twee niveaus weergegeven.</span><span class="sxs-lookup"><span data-stu-id="01146-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="01146-108">Eindproduct H staat voor een product voor een machinemontage.</span><span class="sxs-lookup"><span data-stu-id="01146-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="01146-109">De machinemontage bestaat uit twee delen, een elektrische eenheid (F) met twee materialen (A en B) en een groep van verpakkingsmaterialen (G), eveneens met twee materialen (C en D).</span><span class="sxs-lookup"><span data-stu-id="01146-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="01146-110">Een ander materiaal (E) wordt gebruikt tijdens de algehele montage van de machine.</span><span class="sxs-lookup"><span data-stu-id="01146-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Product H en onderdeel F](media/product-H-part-B.png)

<span data-ttu-id="01146-112">In de bovenstaande afbeelding wordt de technische stuklijst voor product H weergegeven. Deze structuur biedt een goed overzicht van de onderdelen en componenten van de totale montage van de machine.</span><span class="sxs-lookup"><span data-stu-id="01146-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="01146-113">Hoewel productontwerpers de stuklijst misschien het liefst zo weergeven, komt deze structuur mogelijk niet exact overeen met de manier waarop de machine op de werkvloer wordt gebouwd.</span><span class="sxs-lookup"><span data-stu-id="01146-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="01146-114">In de technische stuklijst wordt bijvoorbeeld aangegeven dat de elektrische eenheid F als afzonderlijk onderdeel in een afzonderlijke werkorder wordt gemonteerd.</span><span class="sxs-lookup"><span data-stu-id="01146-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="01146-115">Op de werkvloer kan echter worden geconcludeerd dat het beter is om de elektrische eenheid als onderdeel van de algehele machinemontage te monteren, niet als aparte werkorder.</span><span class="sxs-lookup"><span data-stu-id="01146-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="01146-116">In deze elektrische stuklijst wordt onderdeel G ook als afzonderlijk onderdeel aangeduid.</span><span class="sxs-lookup"><span data-stu-id="01146-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="01146-117">In deze structuur vertegenwoordigt onderdeel G echter geen fysiek onderdeel, maar een verzameling verpakkingsmaterialen.</span><span class="sxs-lookup"><span data-stu-id="01146-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="01146-118">Dus hoewel een technische stuklijst geweldige waarde voor het ontwerp van een product en het onderhoud van dat ontwerp biedt, is het mogelijk niet de meest logische manier om het productregistratieproces van het product te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="01146-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="01146-119">Een productiestuklijst vertegenwoordigt daarentegen de beste manier om een product te bouwen.</span><span class="sxs-lookup"><span data-stu-id="01146-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="01146-120">In de volgende afbeelding ziet u hoe de voorgaande technische stuklijst overgaat in een productiestuklijst.</span><span class="sxs-lookup"><span data-stu-id="01146-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="01146-121">In deze afbeelding is (a) de stuklijst voor product H en is (b) het routeblad voor product H.</span><span class="sxs-lookup"><span data-stu-id="01146-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="01146-122">In deze structuur ziet u dat onderdelen F en G ontbreken en dat de materialen waaruit deze onderdelen bestaan naar het volgende stuklijstniveau zijn overgebracht.</span><span class="sxs-lookup"><span data-stu-id="01146-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="01146-123">In tegenstelling tot de technische stuklijst, die twee bewerkingsbladen had, heeft de productiestuklijst slechts één bewerkingsblad.</span><span class="sxs-lookup"><span data-stu-id="01146-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="01146-124">De verpakkingsbewerking die aan onderdeel G was gekoppeld, is ook overgebracht en maakt nu deel uit van het bewerkingsblad voor product H. De montage van de elektrische eenheid is de eerste bewerking.</span><span class="sxs-lookup"><span data-stu-id="01146-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="01146-125">Deze volgorde is logisch omdat deze eenheid wordt gebruikt in de volgende bewerking, de machinemontage.</span><span class="sxs-lookup"><span data-stu-id="01146-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="01146-126">De laatste bewerking is de verpakkingsbewerking, waarbij twee verpakkingsmaterialen (C en D) worden verbruikt.</span><span class="sxs-lookup"><span data-stu-id="01146-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="01146-127">De overgang tussen de Engineering-stuklijst en de Productie-stuklijst wordt mogelijk door het regeltype Phantom-stuklijst.</span><span class="sxs-lookup"><span data-stu-id="01146-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="01146-128">Met de term phantom wordt aangegeven dat de onderdelen F en G tijdens de overgang tussen de twee stuklijsttypen zijn verdwenen.</span><span class="sxs-lookup"><span data-stu-id="01146-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="01146-129">In dit voorbeeld wordt het phantom-regeltype toegepast op de stuklijstregels voor onderdelen F en G in de technische stuklijst.</span><span class="sxs-lookup"><span data-stu-id="01146-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="01146-130">Wanneer een productie- of batchorder wordt gemaakt, wordt de technische stuklijst gekopieerd naar de productie- of batchorder.</span><span class="sxs-lookup"><span data-stu-id="01146-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="01146-131">Wanneer de order vervolgens wordt geraamd, vindt de overgang van de technische stuklijst naar de productiestuklijst plaats, zoals in de voorgaande afbeeldingen wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="01146-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="01146-132">Van het verpakkingsblad in de tweede afbeelding worden de verpakkingsmaterialen C en D ingevoerd voor de bewerking.</span><span class="sxs-lookup"><span data-stu-id="01146-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="01146-133">Phantom-stuklijststructuren met meerdere niveaus</span><span class="sxs-lookup"><span data-stu-id="01146-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="01146-134">Het phantom-regeltype kan worden gebruikt in stuklijststructuren met meerdere niveaus, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="01146-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="01146-135">In deze afbeelding is (a) de stuklijst voor product G en is (b) het routeblad voor de onderdelen E en F, en product G.</span><span class="sxs-lookup"><span data-stu-id="01146-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Product G en onderdeel F met routebladen](media/product-G-route-sheet-G.png)


<span data-ttu-id="01146-137">In de volgende afbeelding ziet u de resulterende productiestuklijst en het routeblad als de stuklijstregels voor onderdelen E en F zo worden geconfigureerd dat het regeltype Phantom is.</span><span class="sxs-lookup"><span data-stu-id="01146-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="01146-138">In deze afbeelding is (a) de stuklijst voor product G en is (b) het routeblad voor product G.</span><span class="sxs-lookup"><span data-stu-id="01146-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Product G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="01146-140">Phantom en routenetwerk</span><span class="sxs-lookup"><span data-stu-id="01146-140">Phantom and route network</span></span>
<span data-ttu-id="01146-141">Phantom-stuklijsten kunnen ook worden gebruikt voor een stuklijst met een routenetwerk.</span><span class="sxs-lookup"><span data-stu-id="01146-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="01146-142">In een routenetwerk worden een of meer bewerkingen tegelijkertijd uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="01146-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="01146-143">De volgende afbeelding bevat een voorbeeld van een routenetwerk dat wordt gebruikt in een stuklijst met meerdere niveaus.</span><span class="sxs-lookup"><span data-stu-id="01146-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="01146-144">In deze afbeelding is (a) de stuklijst voor product G en onderdeel F, en is (b) het routeblad voor product G en onderdeel F, dat een routenetwerk heeft.</span><span class="sxs-lookup"><span data-stu-id="01146-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Product G en onderdeel F](media/product-G-part-F.png)


<span data-ttu-id="01146-146">In de volgende afbeelding is (a) de stuklijst voor het product G en onderdeel F, en is (b) het routeblad voor product G en onderdeel F.</span><span class="sxs-lookup"><span data-stu-id="01146-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Product G en onderdeel F met routebladen](media/product-G-part-F-with-route-sheet.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]