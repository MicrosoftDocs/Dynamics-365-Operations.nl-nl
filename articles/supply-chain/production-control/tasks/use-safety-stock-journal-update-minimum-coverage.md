---
title: Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning bij te werken
description: Deze procedure laat zien hoe u voorstellen voor minimumbehoefteplanning kunt berekenen op basis van historische transacties en vervolgens de artikelbehoefteplanning kunt bijwerken met de voorstellen.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3b2916d6d2f24579fd9795c0e0bc548b6c2b747
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835769"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="733ca-103">Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning bij te werken</span><span class="sxs-lookup"><span data-stu-id="733ca-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="733ca-104">Deze procedure laat zien hoe u voorstellen voor minimumbehoefteplanning kunt berekenen op basis van historische transacties en vervolgens de artikelbehoefteplanning kunt bijwerken met de voorstellen.</span><span class="sxs-lookup"><span data-stu-id="733ca-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="733ca-105">Dit wordt gedaan via het veiligheidsvoorraadjournaal.</span><span class="sxs-lookup"><span data-stu-id="733ca-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="733ca-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="733ca-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="733ca-107">Deze taak is bedoeld voor de productieplanner om te helpen de minimumbehoefteplanning te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="733ca-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="733ca-108">Een nieuw veiligheidsvoorraadjournaal maken</span><span class="sxs-lookup"><span data-stu-id="733ca-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="733ca-109">Ga naar Journaalnamen veiligheidsvoorraad.</span><span class="sxs-lookup"><span data-stu-id="733ca-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="733ca-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="733ca-110">Click New.</span></span>
3. <span data-ttu-id="733ca-111">Typ 'Materiaal' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="733ca-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="733ca-112">Typ 'Materiaal' in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="733ca-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="733ca-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="733ca-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="733ca-114">Een veiligheidsvoorraadjournaal maken</span><span class="sxs-lookup"><span data-stu-id="733ca-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="733ca-115">Ga naar Berekening van veiligheidsvoorraad.</span><span class="sxs-lookup"><span data-stu-id="733ca-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="733ca-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="733ca-116">Click New.</span></span>
3. <span data-ttu-id="733ca-117">Typ of selecteer een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="733ca-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="733ca-118">Selecteer de naam van het veiligheidsvoorraadjournaal dat u hebt gemaakt, bijvoorbeeld Materiaal.</span><span class="sxs-lookup"><span data-stu-id="733ca-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="733ca-119">Klik op Regels maken.</span><span class="sxs-lookup"><span data-stu-id="733ca-119">Click Create lines.</span></span>
5. <span data-ttu-id="733ca-120">Voer een datum in het veld Begindatum in.</span><span class="sxs-lookup"><span data-stu-id="733ca-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="733ca-121">Stel de datum in op '2015-01-02'.</span><span class="sxs-lookup"><span data-stu-id="733ca-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="733ca-122">Voer een datum in het veld Einddatum in.</span><span class="sxs-lookup"><span data-stu-id="733ca-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="733ca-123">Stel de datum in op '2015-12-30'.</span><span class="sxs-lookup"><span data-stu-id="733ca-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="733ca-124">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="733ca-124">Click OK.</span></span>
    * <span data-ttu-id="733ca-125">Hiermee worden regels gemaakt voor de dimensies die voorraadtransacties hebben.</span><span class="sxs-lookup"><span data-stu-id="733ca-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="733ca-126">Voorstel berekenen</span><span class="sxs-lookup"><span data-stu-id="733ca-126">Calculate proposal</span></span>
1. <span data-ttu-id="733ca-127">Klik op Voorstel berekenen.</span><span class="sxs-lookup"><span data-stu-id="733ca-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="733ca-128">Selecteer de optie Gemiddelde uitgifte tijdens doorlooptijd gebruiken.</span><span class="sxs-lookup"><span data-stu-id="733ca-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="733ca-129">Stel de vermenigvuldigingsfactor in op '10'.</span><span class="sxs-lookup"><span data-stu-id="733ca-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="733ca-130">De vermenigvuldigingsfactor wordt gebruikt om het voorstel te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="733ca-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="733ca-131">Omdat demogegevens slechts enkele transacties bevatten, moet u de factor instellen om een realistisch voorstel te krijgen.</span><span class="sxs-lookup"><span data-stu-id="733ca-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="733ca-132">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="733ca-132">Click OK.</span></span>
    * <span data-ttu-id="733ca-133">Blader omlaag om M0002 en M0003 te zoeken.</span><span class="sxs-lookup"><span data-stu-id="733ca-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="733ca-134">Bekijk de kolom Berekende minimumhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="733ca-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="733ca-135">Minimumhoeveelheid bijwerken</span><span class="sxs-lookup"><span data-stu-id="733ca-135">Update minimum quantity</span></span>
1. <span data-ttu-id="733ca-136">Voer een getal in het veld Nieuwe minimumhoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="733ca-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="733ca-137">Werk de nieuwe minimumhoeveelheid bij op basis van de waarde in Berekende minimumhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="733ca-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="733ca-138">Als het berekende minimum nul is, kunt u de gewenste toekomstige waarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="733ca-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="733ca-139">Zo kunt u bijvoorbeeld de berekende minimumhoeveelheid in dit veld invoeren voor M0002 in magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="733ca-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="733ca-140">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="733ca-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="733ca-141">U kunt bijvoorbeeld M0002 selecteren in magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="733ca-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="733ca-142">Voer een getal in het veld Nieuwe minimumhoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="733ca-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="733ca-143">Werk de nieuwe minimumhoeveelheid bij op basis van de waarde in Berekende minimumhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="733ca-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="733ca-144">Als het berekende minimum nul is, kunt u de gewenste toekomstige waarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="733ca-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="733ca-145">De nieuwe minimumhoeveelheid boeken en het resultaat valideren</span><span class="sxs-lookup"><span data-stu-id="733ca-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="733ca-146">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="733ca-146">Click Post.</span></span>
2. <span data-ttu-id="733ca-147">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="733ca-147">Click OK.</span></span>
3. <span data-ttu-id="733ca-148">Klik om de koppeling in het veld Artikelnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="733ca-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="733ca-149">Klik om de koppeling in het veld Artikelnummer te volgen.</span><span class="sxs-lookup"><span data-stu-id="733ca-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="733ca-150">Klik in het actievenster op Plannen.</span><span class="sxs-lookup"><span data-stu-id="733ca-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="733ca-151">Klik op Artikelbehoefteplanning.</span><span class="sxs-lookup"><span data-stu-id="733ca-151">Click Item coverage.</span></span>
    * <span data-ttu-id="733ca-152">Merk op dat de minimumhoeveelheid is bijgewerkt met de nieuwe minimumhoeveelheid uit het veiligheidsvoorraadjournaal.</span><span class="sxs-lookup"><span data-stu-id="733ca-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  

