---
title: Overboekingsactiviteiten maken voor lean manufacturing
description: Maak een overboekingsactiviteit voor lean manufacturing.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2925833aceba0cffe46b3a44c5d19c87cd3736e7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983345"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="6d8db-103">Overboekingsactiviteiten maken voor lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="6d8db-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d8db-104">Maak een overboekingsactiviteit voor lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="6d8db-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="6d8db-105">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="6d8db-105">Prerequisites:</span></span> 

1. <span data-ttu-id="6d8db-106">Een productiestroom en versie die niet actief zijn, moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6d8db-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="6d8db-107">Het bronmagazijn en het doelmagazijn moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6d8db-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="6d8db-108">De aanvullende of bijgevulde werkcel moet eventueel worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6d8db-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="6d8db-109">De productiestroomversie vinden</span><span class="sxs-lookup"><span data-stu-id="6d8db-109">Find the production flow version</span></span>
1. <span data-ttu-id="6d8db-110">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="6d8db-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="6d8db-111">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6d8db-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6d8db-112">De productiestroom moet een versie in conceptstatus hebben.</span><span class="sxs-lookup"><span data-stu-id="6d8db-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="6d8db-113">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6d8db-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="6d8db-114">Een nieuwe activiteit maken</span><span class="sxs-lookup"><span data-stu-id="6d8db-114">Create a new activity</span></span>
1. <span data-ttu-id="6d8db-115">Klik op Activiteiten.</span><span class="sxs-lookup"><span data-stu-id="6d8db-115">Click Activities.</span></span>
    * <span data-ttu-id="6d8db-116">Zorg ervoor dat de geselecteerde productiestroom een versie in concept heeft en selecteer deze versie.</span><span class="sxs-lookup"><span data-stu-id="6d8db-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="6d8db-117">Klik op Nieuwe planactiviteit maken.</span><span class="sxs-lookup"><span data-stu-id="6d8db-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="6d8db-118">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="6d8db-118">Click Next.</span></span>
4. <span data-ttu-id="6d8db-119">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="6d8db-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6d8db-120">Selecteer 'Overboeking' in het veld Type activiteit.</span><span class="sxs-lookup"><span data-stu-id="6d8db-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="6d8db-121">Voer in het veld Verwerkingshoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="6d8db-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="6d8db-122">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="6d8db-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="6d8db-123">De werkcellen selecteren</span><span class="sxs-lookup"><span data-stu-id="6d8db-123">Select the Work cells</span></span>
1. <span data-ttu-id="6d8db-124">Klik in het veld Aanvullen op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6d8db-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6d8db-125">Selecteer een werkcel om de uitvoerlocatie van de werkcel te gebruiken als de beginlocatie in een overboekingsactiviteit.</span><span class="sxs-lookup"><span data-stu-id="6d8db-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="6d8db-126">Hetzelfde kan met de bijgevulde werkcel worden uitgevoerd, wat de doellocatie van de overboekingsactiviteit instelt.</span><span class="sxs-lookup"><span data-stu-id="6d8db-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="6d8db-127">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6d8db-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="6d8db-128">De updates van de voorraad definiëren</span><span class="sxs-lookup"><span data-stu-id="6d8db-128">Define the inventory updates</span></span>
1. <span data-ttu-id="6d8db-129">Selecteer een optie in het veld Producttype.</span><span class="sxs-lookup"><span data-stu-id="6d8db-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="6d8db-130">Een overboeking wijzigt het type van het product niet.</span><span class="sxs-lookup"><span data-stu-id="6d8db-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="6d8db-131">U kunt eindproducten of halffabricaten overboeken (overboeking tussen twee activiteiten van een productiestroom en misschien een kanbanstroom).</span><span class="sxs-lookup"><span data-stu-id="6d8db-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="6d8db-132">Wanneer u klaar bent met het overboeken van producten, kunt u selecteren of orderverzameling of ontvangst resulteert in een voorraadtransactie.</span><span class="sxs-lookup"><span data-stu-id="6d8db-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="6d8db-133">De overboekingslocaties definiëren</span><span class="sxs-lookup"><span data-stu-id="6d8db-133">Define the transfer locations</span></span>
1. <span data-ttu-id="6d8db-134">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="6d8db-134">Click Next.</span></span>
2. <span data-ttu-id="6d8db-135">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6d8db-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6d8db-136">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6d8db-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6d8db-137">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6d8db-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6d8db-138">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6d8db-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6d8db-139">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="6d8db-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6d8db-140">Selecteer 'Expediteur' in het veld Bevracht door.</span><span class="sxs-lookup"><span data-stu-id="6d8db-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="6d8db-141">Opties omvatten: Expediteur - de organisatie die het magazijn van verzending beheert, Ontvanger - de organisatie die het ontvangende magazijn beheert, Vervoerder - een externe leverancier.</span><span class="sxs-lookup"><span data-stu-id="6d8db-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="6d8db-142">Als de operationele organisatie een leverancier is, is voor de overboekingsactiviteit een uitbestedingsovereenkomst vereist.</span><span class="sxs-lookup"><span data-stu-id="6d8db-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="6d8db-143">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="6d8db-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="6d8db-144">De activiteitstijden dfiniëren</span><span class="sxs-lookup"><span data-stu-id="6d8db-144">Define the activity times</span></span>
1. <span data-ttu-id="6d8db-145">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6d8db-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6d8db-146">De definitie van Runtime is vereist.</span><span class="sxs-lookup"><span data-stu-id="6d8db-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="6d8db-147">Uitvoeringstijd wordt gebruikt om kosten en de doorvoertijden van de kanbantaken te berekenen.</span><span class="sxs-lookup"><span data-stu-id="6d8db-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="6d8db-148">Runtimes worden niet gebruikt om capaciteitsbelasting en verbruik te berekenen. Deze wordt berekend door cyclusduur, afgeleid uit de taak van de productiestroomversie.</span><span class="sxs-lookup"><span data-stu-id="6d8db-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="6d8db-149">Voer in het veld Tijd een nummer in.</span><span class="sxs-lookup"><span data-stu-id="6d8db-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="6d8db-150">Typ een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="6d8db-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="6d8db-151">Selecteer de tijdseenheid.</span><span class="sxs-lookup"><span data-stu-id="6d8db-151">Select the Time unit.</span></span>
5. <span data-ttu-id="6d8db-152">Voer in het veld Per hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="6d8db-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="6d8db-153">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="6d8db-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6d8db-154">Wachttijden zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="6d8db-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="6d8db-155">Voer in het veld Tijd een nummer in.</span><span class="sxs-lookup"><span data-stu-id="6d8db-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="6d8db-156">Typ een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="6d8db-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="6d8db-157">Selecteer de tijdseenheid.</span><span class="sxs-lookup"><span data-stu-id="6d8db-157">Select the Time unit.</span></span>
10. <span data-ttu-id="6d8db-158">Voer in het veld Per hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="6d8db-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="6d8db-159">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="6d8db-159">Click Next.</span></span>
12. <span data-ttu-id="6d8db-160">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="6d8db-160">Click Finish.</span></span>
13. <span data-ttu-id="6d8db-161">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6d8db-161">Close the page.</span></span>

