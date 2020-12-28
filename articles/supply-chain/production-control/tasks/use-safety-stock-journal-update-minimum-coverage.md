---
title: Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning bij te werken
description: Deze procedure laat zien hoe u voorstellen voor minimumbehoefteplanning kunt berekenen op basis van historische transacties en vervolgens de artikelbehoefteplanning kunt bijwerken met de voorstellen.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d69daf3d307ba72ff6017d91849e3d22bd0bd85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425673"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="91dcd-103">Het veiligheidsvoorraadjournaal gebruiken om de minimumbehoefteplanning bij te werken</span><span class="sxs-lookup"><span data-stu-id="91dcd-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91dcd-104">Deze procedure laat zien hoe u voorstellen voor minimumbehoefteplanning kunt berekenen op basis van historische transacties en vervolgens de artikelbehoefteplanning kunt bijwerken met de voorstellen.</span><span class="sxs-lookup"><span data-stu-id="91dcd-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="91dcd-105">Dit wordt gedaan via het veiligheidsvoorraadjournaal.</span><span class="sxs-lookup"><span data-stu-id="91dcd-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="91dcd-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="91dcd-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="91dcd-107">Deze taak is bedoeld voor de productieplanner om te helpen de minimumbehoefteplanning te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="91dcd-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="91dcd-108">Een nieuw veiligheidsvoorraadjournaal maken</span><span class="sxs-lookup"><span data-stu-id="91dcd-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="91dcd-109">Ga in het **navigatievenster** naar **Hoofdplanning > Instellingen > Journaalnamen veiligheidsvoorraad**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="91dcd-110">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-110">Click **New**.</span></span>
3. <span data-ttu-id="91dcd-111">Typ Materiaal in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="91dcd-112">Typ Materiaal in het veld **Omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="91dcd-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="91dcd-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="91dcd-114">Een veiligheidsvoorraadjournaal maken</span><span class="sxs-lookup"><span data-stu-id="91dcd-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="91dcd-115">Ga in het **navigatievenster** naar **Hoofdplanning > Hoofdplanning > Uitvoeren > Berekening van veiligheidsvoorraad**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="91dcd-116">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-116">Click **New**.</span></span>
3. <span data-ttu-id="91dcd-117">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="91dcd-118">Selecteer de naam van het veiligheidsvoorraadjournaal dat u hebt gemaakt, bijvoorbeeld Materiaal.</span><span class="sxs-lookup"><span data-stu-id="91dcd-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="91dcd-119">Klik op **Regels maken**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="91dcd-120">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="91dcd-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="91dcd-121">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="91dcd-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="91dcd-122">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-122">Click **OK**.</span></span> <span data-ttu-id="91dcd-123">Hiermee worden regels gemaakt voor de dimensies die voorraadtransacties hebben.</span><span class="sxs-lookup"><span data-stu-id="91dcd-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="91dcd-124">Voorstel berekenen</span><span class="sxs-lookup"><span data-stu-id="91dcd-124">Calculate proposal</span></span>
1. <span data-ttu-id="91dcd-125">Klik op **Voorstel berekenen**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="91dcd-126">Selecteer de optie **Gemiddelde uitgifte tijdens doorlooptijd gebruiken**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="91dcd-127">Stel de **vermenigvuldigingsfactor** in op 10.</span><span class="sxs-lookup"><span data-stu-id="91dcd-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="91dcd-128">De vermenigvuldigingsfactor wordt gebruikt om het voorstel te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="91dcd-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="91dcd-129">Omdat demogegevens slechts enkele transacties bevatten, moet u de factor instellen om een realistisch voorstel te krijgen.</span><span class="sxs-lookup"><span data-stu-id="91dcd-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="91dcd-130">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-130">Click **OK**.</span></span> <span data-ttu-id="91dcd-131">Blader omlaag om M0002 en M0003 te zoeken.</span><span class="sxs-lookup"><span data-stu-id="91dcd-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="91dcd-132">Bekijk de kolom **Berekende minimumhoeveelheid**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="91dcd-133">Minimumhoeveelheid bijwerken</span><span class="sxs-lookup"><span data-stu-id="91dcd-133">Update minimum quantity</span></span>
1. <span data-ttu-id="91dcd-134">Voer een getal in het veld **Nieuwe minimumhoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="91dcd-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="91dcd-135">Werk de nieuwe minimumhoeveelheid bij op basis van de waarde in Berekende minimumhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="91dcd-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="91dcd-136">Als het berekende minimum nul is, kunt u de gewenste toekomstige waarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="91dcd-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="91dcd-137">Zo kunt u bijvoorbeeld de berekende minimumhoeveelheid in dit veld invoeren voor M0002 in magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="91dcd-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="91dcd-138">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="91dcd-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="91dcd-139">U kunt bijvoorbeeld M0002 selecteren in magazijn 12.</span><span class="sxs-lookup"><span data-stu-id="91dcd-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="91dcd-140">Voer een getal in het veld **Nieuwe minimumhoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="91dcd-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="91dcd-141">Werk de nieuwe minimumhoeveelheid bij op basis van de waarde in Berekende minimumhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="91dcd-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="91dcd-142">Als het berekende minimum nul is, kunt u de gewenste toekomstige waarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="91dcd-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="91dcd-143">De nieuwe minimumhoeveelheid boeken en het resultaat valideren</span><span class="sxs-lookup"><span data-stu-id="91dcd-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="91dcd-144">Klik op **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-144">Click **Post**.</span></span>
2. <span data-ttu-id="91dcd-145">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-145">Click **OK**.</span></span>
3. <span data-ttu-id="91dcd-146">Klik om de koppeling in het veld **Artikelnummer** te volgen.</span><span class="sxs-lookup"><span data-stu-id="91dcd-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="91dcd-147">Klik om de koppeling in het veld **Artikelnummer** te volgen.</span><span class="sxs-lookup"><span data-stu-id="91dcd-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="91dcd-148">Klik op **Plannen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="91dcd-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="91dcd-149">Klik op **Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="91dcd-149">Click **Item coverage**.</span></span> <span data-ttu-id="91dcd-150">Merk op dat de **minimumhoeveelheid** is bijgewerkt met de nieuwe minimumhoeveelheid uit het veiligheidsvoorraadjournaal.</span><span class="sxs-lookup"><span data-stu-id="91dcd-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

