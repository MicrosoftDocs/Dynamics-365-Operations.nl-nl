---
title: Een nieuwe magazijnindeling maken
description: Deze procedure laat zien hoe u de informatie over locaties in een magazijn instelt.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26314f9015feded41f105814b85069fff0c62964
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "360527"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="0c0eb-103">Een nieuwe magazijnindeling maken</span><span class="sxs-lookup"><span data-stu-id="0c0eb-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c0eb-104">Deze procedure laat zien hoe u de informatie over locaties in een magazijn instelt.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="0c0eb-105">Dit geldt alleen voor magazijnen die zijn gemaakt met "basale magazijnen" in de module Voorraadbeheer, niet voor magazijnen die in de module Magazijnbeheer zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="0c0eb-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="0c0eb-107">Stel de standaardlocatiecapaciteit in</span><span class="sxs-lookup"><span data-stu-id="0c0eb-107">Set the default location capacity</span></span>
1. <span data-ttu-id="0c0eb-108">Ga naar Voorraadbeheer > Instellingen > Parameters voor voorraad- en magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="0c0eb-109">Klik op het tabblad Locaties.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="0c0eb-110">Voer een getal in het veld Standaardbreedte in.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="0c0eb-111">Voer een getal in het veld Standaarddiepte in.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="0c0eb-112">Voer een getal in het veld Standaardhoogte in.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="0c0eb-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-113">Click Save.</span></span>
7. <span data-ttu-id="0c0eb-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="0c0eb-115">De locatienaamindeling definiëren</span><span class="sxs-lookup"><span data-stu-id="0c0eb-115">Define the location name format</span></span>
1. <span data-ttu-id="0c0eb-116">Ga naar Voorraadbeheer > Instellen > Opsplitsing van voorraad > Magazijnen.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="0c0eb-117">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-117">Click New.</span></span>
3. <span data-ttu-id="0c0eb-118">Typ een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="0c0eb-119">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0c0eb-120">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0c0eb-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0c0eb-122">Schakel de uitbreiding van de sectie Locatienamen om.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="0c0eb-123">De opties in deze sectie definiëren de standaardindeling voor locatienamen.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="0c0eb-124">In ons voorbeeld nemen we het gangnummer, het reknummer en het planknummer op.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="0c0eb-125">Stel de optie Gang opnemen in op Ja.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="0c0eb-126">Stel de optie Rek opnemen in op Ja.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="0c0eb-127">Typ in het veld Indeling voor het rek een waarde.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="0c0eb-128">Bijvoorbeeld: -##</span><span class="sxs-lookup"><span data-stu-id="0c0eb-128">For example: -##</span></span>  
11. <span data-ttu-id="0c0eb-129">Stel de optie Plank opnemen in op Ja.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="0c0eb-130">Typ in het veld Indeling voor de plank een waarde.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="0c0eb-131">Bijvoorbeeld: -##</span><span class="sxs-lookup"><span data-stu-id="0c0eb-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="0c0eb-132">Magazijnlocaties definiëren</span><span class="sxs-lookup"><span data-stu-id="0c0eb-132">Define warehouse locations</span></span>
1. <span data-ttu-id="0c0eb-133">Klik in het actievenster op Magazijn.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="0c0eb-134">Klik op Locatiewizard.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="0c0eb-135">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-135">Click Next.</span></span>
4. <span data-ttu-id="0c0eb-136">De optie Outbound docks deselecteren</span><span class="sxs-lookup"><span data-stu-id="0c0eb-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="0c0eb-137">De optie Bulklocaties deselecteren</span><span class="sxs-lookup"><span data-stu-id="0c0eb-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="0c0eb-138">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-138">Click Next.</span></span>
7. <span data-ttu-id="0c0eb-139">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-139">Click Next.</span></span>
8. <span data-ttu-id="0c0eb-140">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-140">Click Next.</span></span>
9. <span data-ttu-id="0c0eb-141">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-141">Click Next.</span></span>
10. <span data-ttu-id="0c0eb-142">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-142">Click Next.</span></span>
11. <span data-ttu-id="0c0eb-143">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-143">Click Next.</span></span>
12. <span data-ttu-id="0c0eb-144">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-144">Click Next.</span></span>
    * <span data-ttu-id="0c0eb-145">Merk op dat de fysieke dimensies die op deze pagina worden weergegeven de dimensies zijn die u instelt aan het begin van deze procedure.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="0c0eb-146">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-146">Click Next.</span></span>
14. <span data-ttu-id="0c0eb-147">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-147">Click Finish.</span></span>
15. <span data-ttu-id="0c0eb-148">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-148">Close the page.</span></span>
16. <span data-ttu-id="0c0eb-149">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="0c0eb-149">Refresh the page.</span></span>

