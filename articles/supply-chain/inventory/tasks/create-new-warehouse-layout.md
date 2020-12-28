---
title: Een nieuwe magazijnindeling maken
description: In dit onderwerp wordt beschreven hoe u informatie instelt voor locaties in een magazijn.
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09666e95cc90913f1bf8555b9ff2c48aa55369ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425708"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="621b3-103">Een nieuwe magazijnindeling maken</span><span class="sxs-lookup"><span data-stu-id="621b3-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="621b3-104">In dit onderwerp wordt beschreven hoe u informatie instelt voor locaties in een magazijn.</span><span class="sxs-lookup"><span data-stu-id="621b3-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="621b3-105">Dit geldt alleen voor magazijnen die zijn gemaakt met "basale magazijnen" in de module Voorraadbeheer, niet voor magazijnen die in de module Magazijnbeheer zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="621b3-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="621b3-106">U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken.</span><span class="sxs-lookup"><span data-stu-id="621b3-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="621b3-107">Stel de standaardlocatiecapaciteit in</span><span class="sxs-lookup"><span data-stu-id="621b3-107">Set the default location capacity</span></span>
1. <span data-ttu-id="621b3-108">Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellen > Parameters voor voorraad- en magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="621b3-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="621b3-109">Selecteer het tabblad **Locatietypen**.</span><span class="sxs-lookup"><span data-stu-id="621b3-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="621b3-110">Voer een getal in het veld **Standaardbreedte** in.</span><span class="sxs-lookup"><span data-stu-id="621b3-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="621b3-111">Voer een getal in het veld **Standaarddiepte** in.</span><span class="sxs-lookup"><span data-stu-id="621b3-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="621b3-112">Voer een getal in het veld **Standaardhoogte** in.</span><span class="sxs-lookup"><span data-stu-id="621b3-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="621b3-113">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="621b3-113">Select **Save**.</span></span>
7. <span data-ttu-id="621b3-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="621b3-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="621b3-115">De locatienaamindeling definiëren</span><span class="sxs-lookup"><span data-stu-id="621b3-115">Define the location name format</span></span>
1. <span data-ttu-id="621b3-116">Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellen > Opsplitsing van voorraad > Magazijnen**.</span><span class="sxs-lookup"><span data-stu-id="621b3-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="621b3-117">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="621b3-117">Select **New**.</span></span>
3. <span data-ttu-id="621b3-118">Typ een waarde in het veld **Magazijn**.</span><span class="sxs-lookup"><span data-stu-id="621b3-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="621b3-119">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="621b3-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="621b3-120">Selecteer in het veld **Vestiging** de gewenste record in de zoeklijst.</span><span class="sxs-lookup"><span data-stu-id="621b3-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="621b3-121">Schakel de uitbreiding van de sectie **Locatienamen** om.</span><span class="sxs-lookup"><span data-stu-id="621b3-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="621b3-122">De opties in deze sectie definiëren de standaardindeling voor locatienamen.</span><span class="sxs-lookup"><span data-stu-id="621b3-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="621b3-123">In ons voorbeeld nemen we het gangnummer, het reknummer en het planknummer op.</span><span class="sxs-lookup"><span data-stu-id="621b3-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="621b3-124">Stel de optie **Gang opnemen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="621b3-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="621b3-125">Stel de optie **Rek opnemen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="621b3-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="621b3-126">Typ in het veld **Indeling** voor het rek een waarde.</span><span class="sxs-lookup"><span data-stu-id="621b3-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="621b3-127">Stel de optie **Plank opnemen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="621b3-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="621b3-128">Typ in het veld **Indeling** voor de plank een waarde.</span><span class="sxs-lookup"><span data-stu-id="621b3-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="621b3-129">Magazijnlocaties definiëren</span><span class="sxs-lookup"><span data-stu-id="621b3-129">Define warehouse locations</span></span>
1. <span data-ttu-id="621b3-130">Selecteer **Magazijn** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="621b3-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="621b3-131">Selecteer **Locatiewizard**.</span><span class="sxs-lookup"><span data-stu-id="621b3-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="621b3-132">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="621b3-132">Select **Next**.</span></span>
4. <span data-ttu-id="621b3-133">De optie **Outbound docks** deselecteren</span><span class="sxs-lookup"><span data-stu-id="621b3-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="621b3-134">De optie **Bulklocaties** deselecteren</span><span class="sxs-lookup"><span data-stu-id="621b3-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="621b3-135">Selecteer **Volgende** totdat u de optie **Voltooien** hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="621b3-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="621b3-136">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="621b3-136">Close the page.</span></span>
8. <span data-ttu-id="621b3-137">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="621b3-137">Refresh the page.</span></span>

