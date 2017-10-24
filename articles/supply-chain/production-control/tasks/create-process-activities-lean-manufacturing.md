--- 
title: Procesactiviteiten maken voor lean manufacturing
description: Maak een procesactiviteit voor lean manufacturing.
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: dd77c20b622fd8a14e1cdf77883043699f9a6317
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="d34a2-103">Procesactiviteiten maken voor lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="d34a2-103">Create process activities for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d34a2-104">Maak een procesactiviteit voor lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="d34a2-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="d34a2-105">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="d34a2-105">Prerequisites:</span></span> 

1. <span data-ttu-id="d34a2-106">Een productiestroom en versie die niet actief zijn, moeten worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d34a2-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="d34a2-107">Een werkcel moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d34a2-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="d34a2-108">De productiestroomversie vinden</span><span class="sxs-lookup"><span data-stu-id="d34a2-108">Find the production flow version</span></span>
1. <span data-ttu-id="d34a2-109">Ga naar Productiebeheer > Instellingen > Lean productiestroom > Productiestromen.</span><span class="sxs-lookup"><span data-stu-id="d34a2-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d34a2-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d34a2-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d34a2-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d34a2-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="d34a2-112">Een nieuwe activiteit maken</span><span class="sxs-lookup"><span data-stu-id="d34a2-112">Create a new activity</span></span>
1. <span data-ttu-id="d34a2-113">Klik op Activiteiten.</span><span class="sxs-lookup"><span data-stu-id="d34a2-113">Click Activities.</span></span>
    * <span data-ttu-id="d34a2-114">Zorg ervoor dat de geselecteerde productiestroom een versie in concept heeft en selecteer deze versie.</span><span class="sxs-lookup"><span data-stu-id="d34a2-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="d34a2-115">Klik op Nieuwe planactiviteit maken.</span><span class="sxs-lookup"><span data-stu-id="d34a2-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="d34a2-116">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="d34a2-116">Click Next.</span></span>
4. <span data-ttu-id="d34a2-117">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d34a2-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d34a2-118">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d34a2-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d34a2-119">De naam moet uniek zijn voor een bepaalde productiestroom voor alle versies.</span><span class="sxs-lookup"><span data-stu-id="d34a2-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="d34a2-120">Voer in het veld Verwerkingshoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="d34a2-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="d34a2-121">Ongeacht de taakhoeveelheid die wordt verwerkt, dit is de minimumhoeveelheid per taak om de loonkosten te berekenen.</span><span class="sxs-lookup"><span data-stu-id="d34a2-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="d34a2-122">Als de taakhoeveelheden van deze hoeveelheid afwijken, wordt de arbeidskostenafwijking gemaakt.</span><span class="sxs-lookup"><span data-stu-id="d34a2-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="d34a2-123">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="d34a2-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="d34a2-124">De werkcel selecteren</span><span class="sxs-lookup"><span data-stu-id="d34a2-124">Select the work cell</span></span>
1. <span data-ttu-id="d34a2-125">Klik in het veld Werkcel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d34a2-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="d34a2-126">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d34a2-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="d34a2-127">De updates van de voorraad definiëren</span><span class="sxs-lookup"><span data-stu-id="d34a2-127">Define the inventory updates</span></span>
1. <span data-ttu-id="d34a2-128">Schakel het selectievakje Voorhanden ontvangst bijwerken in of uit.</span><span class="sxs-lookup"><span data-stu-id="d34a2-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="d34a2-129">Als Voorhanden voorraad bijwerken = Nee, kunt u de activiteit definiëren om een halffabricaatproduct (de activiteit bereikt niet het stuklijstniveau) te ontvangen.</span><span class="sxs-lookup"><span data-stu-id="d34a2-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="d34a2-130">U kunt ook kiezen om halffabricaten te verbruiken.</span><span class="sxs-lookup"><span data-stu-id="d34a2-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="d34a2-131">De orderverzamelactiviteiten definiëren</span><span class="sxs-lookup"><span data-stu-id="d34a2-131">Define the picking activities</span></span>
1. <span data-ttu-id="d34a2-132">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="d34a2-132">Click Next.</span></span>
2. <span data-ttu-id="d34a2-133">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d34a2-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d34a2-134">Een standaard orderverzamelactiviteit wordt gemaakt voor de invoerlocatie van de geselecteerde werkcel.</span><span class="sxs-lookup"><span data-stu-id="d34a2-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="d34a2-135">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d34a2-135">Click Add.</span></span>
    * <span data-ttu-id="d34a2-136">U kunt extra orderverzamelactiviteiten maken voor specifieke producten die niet worden gefaseerd aan de invoeractiviteit van de werkcel.</span><span class="sxs-lookup"><span data-stu-id="d34a2-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="d34a2-137">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d34a2-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d34a2-138">Typ een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="d34a2-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="d34a2-139">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d34a2-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d34a2-140">Met deze definitie worden alle materialen die in de activiteit worden verbruikt verzameld uit het standaardinvoermagazijn en -locatie, behalve het artikel dat in de tweede orderverzamelactiviteit wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d34a2-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="d34a2-141">Dit artikel wordt uit een ander(e) magazijn en locatie verzameld.</span><span class="sxs-lookup"><span data-stu-id="d34a2-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="d34a2-142">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d34a2-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d34a2-143">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="d34a2-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d34a2-144">Schakel het selectievakje Uitval registreren in of uit.</span><span class="sxs-lookup"><span data-stu-id="d34a2-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="d34a2-145">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="d34a2-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="d34a2-146">De activiteitstijden dfiniëren</span><span class="sxs-lookup"><span data-stu-id="d34a2-146">Define the activity times</span></span>
1. <span data-ttu-id="d34a2-147">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d34a2-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d34a2-148">De definitie van Runtime is vereist.</span><span class="sxs-lookup"><span data-stu-id="d34a2-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="d34a2-149">De Runtime wordt gebruikt om kosten en de doorvoertijden van de kanbantaken te berekenen.</span><span class="sxs-lookup"><span data-stu-id="d34a2-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="d34a2-150">Runtimes worden niet gebruikt om capaciteitsbelasting en verbruik te berekenen. Deze wordt berekend door cyclusduur, afgeleid uit de taak van de productiestroomversie.</span><span class="sxs-lookup"><span data-stu-id="d34a2-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="d34a2-151">Voer in het veld Tijd een nummer in.</span><span class="sxs-lookup"><span data-stu-id="d34a2-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="d34a2-152">Typ een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="d34a2-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="d34a2-153">Selecteer de tijdseenheid.</span><span class="sxs-lookup"><span data-stu-id="d34a2-153">Select the Time unit.</span></span>
5. <span data-ttu-id="d34a2-154">Voer in het veld Per hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="d34a2-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="d34a2-155">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d34a2-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d34a2-156">Wachttijden zijn optioneel.</span><span class="sxs-lookup"><span data-stu-id="d34a2-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="d34a2-157">Voer in het veld Tijd een nummer in.</span><span class="sxs-lookup"><span data-stu-id="d34a2-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="d34a2-158">Typ een waarde in het veld Eenheid.</span><span class="sxs-lookup"><span data-stu-id="d34a2-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="d34a2-159">Selecteer de tijdseenheid.</span><span class="sxs-lookup"><span data-stu-id="d34a2-159">Select the Time unit.</span></span>
10. <span data-ttu-id="d34a2-160">Voer in het veld Per hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="d34a2-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="d34a2-161">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="d34a2-161">Click Next.</span></span>
12. <span data-ttu-id="d34a2-162">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="d34a2-162">Click Finish.</span></span>
13. <span data-ttu-id="d34a2-163">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d34a2-163">Close the page.</span></span>


