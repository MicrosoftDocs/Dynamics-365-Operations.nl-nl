---
title: Voorraadlocaties
description: Voorraadlocaties worden met basale magazijnen (WMS I) gebruikt om te bepalen waar artikelen worden opgeslagen en waar artikelen uit worden verzameld in een WMS I-magazijn.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4afbb4847a2d3175585ed270d8ecd8aac33c4b14
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813118"
---
# <a name="inventory-locations"></a><span data-ttu-id="96465-103">Voorraadlocaties</span><span class="sxs-lookup"><span data-stu-id="96465-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96465-104">Voorraadlocaties worden met basale magazijnen (WMS I) gebruikt om te bepalen waar artikelen worden opgeslagen en waar artikelen uit worden verzameld in een WMS I-magazijn.</span><span class="sxs-lookup"><span data-stu-id="96465-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="96465-105">Dit onderwerp geldt voor functies in de module voor Voorraadbeheer.</span><span class="sxs-lookup"><span data-stu-id="96465-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="96465-106">Het geldt niet voor functies in de module Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="96465-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="96465-107">De term locatie verwijst naar de plaats waar artikelen worden opgeslagen en opgehaald.</span><span class="sxs-lookup"><span data-stu-id="96465-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="96465-108">Voor elke locatie kan ook de plaats worden opgegeven waar het artikel wordt ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="96465-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="96465-109">Standaard zijn deze gelijk.</span><span class="sxs-lookup"><span data-stu-id="96465-109">By default, they are the same.</span></span> <span data-ttu-id="96465-110">Meestal worden artikelen aan dezelfde kant van de locatie ingevoegd en opgehaald, maar niet altijd.</span><span class="sxs-lookup"><span data-stu-id="96465-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="96465-111">Zo worden artikelen in opslagrekken aan de ene kant in de rekken geplaatst en aan de andere kant uit de rekken gehaald.</span><span class="sxs-lookup"><span data-stu-id="96465-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="96465-112">De belangrijkste invoer is een locatienaam, die meestal door de coördinaten ervan wordt gedefinieerd: magazijn, gang, rek, plank en bak.</span><span class="sxs-lookup"><span data-stu-id="96465-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="96465-113">Deze naam of id kan op de pagina Voorraadlocaties handmatig worden ingevoerd of worden gegenereerd op basis van de coördinaten van de locatie, bijvoorbeeld 01-02-03-4 voor gang 1, rek 2, plank 3, bak 4.</span><span class="sxs-lookup"><span data-stu-id="96465-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="96465-114">Locatie-eigenschappen</span><span class="sxs-lookup"><span data-stu-id="96465-114">Location properties</span></span>

<span data-ttu-id="96465-115">Een locatie heeft de volgende kenmerken:</span><span class="sxs-lookup"><span data-stu-id="96465-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="96465-116">Grootte (hoogte, breedte, diepte, en dus volume)</span><span class="sxs-lookup"><span data-stu-id="96465-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="96465-117">Magazijn, gang, rek, plank en bakpositie</span><span class="sxs-lookup"><span data-stu-id="96465-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="96465-118">Locatietype (bulklocatie, orderverzamellocatie, inbound dock, outbound dock, productieinvoerlocatie, inspectielocatie, of kanbansupermarkt)</span><span class="sxs-lookup"><span data-stu-id="96465-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="96465-119">Met controletekst kan in onlinesystemen worden gecontroleerd of de operator de juiste locatie voor een bepaald artikel heeft geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="96465-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="96465-120">Deze controletekst kan handmatig of standaard door het systeem worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="96465-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="96465-121">Sorteercodes</span><span class="sxs-lookup"><span data-stu-id="96465-121">Sort codes</span></span>
<span data-ttu-id="96465-122">Met sorteercodes kunt u de afhandeling van orderverzamelregels optimaliseren. Deze regels bevatten de gegevens die nodig zijn om artikelen uit de voorraad op te halen zoals de volgorde waarin de orders worden verzameld.</span><span class="sxs-lookup"><span data-stu-id="96465-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="96465-123">Sorteercodes kunnen worden opgegeven met de gang en de andere coördinaten, of handmatig voor de locatie worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="96465-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="96465-124">Geblokkeerde locaties</span><span class="sxs-lookup"><span data-stu-id="96465-124">Blocked locations</span></span>
<span data-ttu-id="96465-125">Soms wilt u wellicht aangeven dat een locatie gedurende een bepaalde tijd is geblokkeerd, bijvoorbeeld om reparaties mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="96465-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="96465-126">Op andere momenten wilt u mogelijk aangeven dat alleen de invoer of alleen de uitvoer is geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="96465-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="96465-127">Boomstructuur</span><span class="sxs-lookup"><span data-stu-id="96465-127">Tree structure</span></span>

<span data-ttu-id="96465-128">Op de pagina Voorraadlocaties kunt u de magazijnindeling bekijken in een boomstructuur in een bepaalde weergave-indeling op basis van de coördinaten van voorraadlocaties.</span><span class="sxs-lookup"><span data-stu-id="96465-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="96465-129">Voorraadlocaties onderhouden via het formulier voor magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="96465-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="96465-130">Het is mogelijk om locaties van het ene magazijn naar het andere te kopiëren en locaties via een wizard te maken.</span><span class="sxs-lookup"><span data-stu-id="96465-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="96465-131">Voordat u de wizard uitvoert, moet u ervoor zorgen dat u de standaardlocatienamen hebt gedefinieerd op de pagina Magazijn.</span><span class="sxs-lookup"><span data-stu-id="96465-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="96465-132">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="96465-132">Additional resources</span></span>
--------

[<span data-ttu-id="96465-133">Een nieuwe magazijnindeling maken</span><span class="sxs-lookup"><span data-stu-id="96465-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]