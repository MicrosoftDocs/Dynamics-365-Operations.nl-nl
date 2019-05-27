---
title: Een halffabricaat maken (februari 2016)
description: Deze taak is gericht op het maken van een halffabricaat.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9caeae552471eed1cb1d8630f387ca31107fcece
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567799"
---
# <a name="create-a-semi-finished-product-february-2016"></a><span data-ttu-id="f344f-103">Een halffabricaat maken (februari 2016)</span><span class="sxs-lookup"><span data-stu-id="f344f-103">Create a semi-finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f344f-104">Deze taak is gericht op het maken van een halffabricaat.</span><span class="sxs-lookup"><span data-stu-id="f344f-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="f344f-105">Dit is de tweede taak in de reeks stuklijstberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f344f-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="f344f-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="f344f-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="f344f-107">Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="f344f-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f344f-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f344f-108">Click New.</span></span>
3. <span data-ttu-id="f344f-109">Typ een waarde in het veld Productnummer.</span><span class="sxs-lookup"><span data-stu-id="f344f-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f344f-110">Typ voor dit voorbeeld: 'Stuklijst_2'.</span><span class="sxs-lookup"><span data-stu-id="f344f-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="f344f-111">Typ of selecteer een waarde in het veld Artikelmodelgroep.</span><span class="sxs-lookup"><span data-stu-id="f344f-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-112">Selecteer STD.</span><span class="sxs-lookup"><span data-stu-id="f344f-112">Select STD.</span></span> <span data-ttu-id="f344f-113">STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f344f-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="f344f-114">Typ of selecteer een waarde in het veld Artikelgroep.</span><span class="sxs-lookup"><span data-stu-id="f344f-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-115">Selecteer bijvoorbeeld 'Audio'.</span><span class="sxs-lookup"><span data-stu-id="f344f-115">For example, select Audio.</span></span> <span data-ttu-id="f344f-116">Dit heeft geen invloed op de kostenberekeningen.</span><span class="sxs-lookup"><span data-stu-id="f344f-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="f344f-117">Typ of selecteer een waarde in het veld Opslagdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="f344f-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-118">Selecteer 'SiteWH'.</span><span class="sxs-lookup"><span data-stu-id="f344f-118">Select SiteWH.</span></span> <span data-ttu-id="f344f-119">Alleen Locatie en Magazijn wordt gebruikt voor dit voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="f344f-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="f344f-120">Typ of selecteer een waarde in het veld Traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="f344f-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-121">Traceringsdimensies worden niet voor dit voorbeeld gebruikt. Selecteer 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="f344f-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="f344f-122">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="f344f-122">Click OK.</span></span>
9. <span data-ttu-id="f344f-123">Klik in het actievenster op Voorraad beheren.</span><span class="sxs-lookup"><span data-stu-id="f344f-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="f344f-124">Klik op Standaardorderinstellingen.</span><span class="sxs-lookup"><span data-stu-id="f344f-124">Click Default order settings.</span></span>
11. <span data-ttu-id="f344f-125">Selecteer in het veld Standaardordertype: 'Productie'.</span><span class="sxs-lookup"><span data-stu-id="f344f-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="f344f-126">Omdat dit een halffabricaat is dat wordt geproduceerd, selecteert u 'Productie'.</span><span class="sxs-lookup"><span data-stu-id="f344f-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="f344f-127">Typ of selecteer een waarde in het veld Inkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="f344f-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-128">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f344f-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f344f-129">Typ of selecteer een waarde in het veld Voorraadvestiging.</span><span class="sxs-lookup"><span data-stu-id="f344f-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-130">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f344f-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="f344f-131">Typ of selecteer een waarde in het veld Verkoopvestiging.</span><span class="sxs-lookup"><span data-stu-id="f344f-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-132">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f344f-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="f344f-133">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f344f-133">Close the page.</span></span>
16. <span data-ttu-id="f344f-134">Klik in het actievenster op Kosten beheren.</span><span class="sxs-lookup"><span data-stu-id="f344f-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="f344f-135">Klik op Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="f344f-135">Click Item price.</span></span>
18. <span data-ttu-id="f344f-136">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f344f-136">Click New.</span></span>
19. <span data-ttu-id="f344f-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f344f-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="f344f-138">Typ of selecteer een waarde in het veld Versie.</span><span class="sxs-lookup"><span data-stu-id="f344f-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-139">Selecteer voor dit voorbeeld 'Versie 10.'</span><span class="sxs-lookup"><span data-stu-id="f344f-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="f344f-140">Typ of selecteer een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="f344f-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-141">Selecteer voor dit voorbeeld 'Locatie 1.'</span><span class="sxs-lookup"><span data-stu-id="f344f-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="f344f-142">Stel het veld Prijs in op '10'.</span><span class="sxs-lookup"><span data-stu-id="f344f-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="f344f-143">Typ voor dit voorbeeld een kostprijs van 10.</span><span class="sxs-lookup"><span data-stu-id="f344f-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="f344f-144">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f344f-144">Click Save.</span></span>
24. <span data-ttu-id="f344f-145">Klik op Prijzen in behandeling activeren.</span><span class="sxs-lookup"><span data-stu-id="f344f-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="f344f-146">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f344f-146">Close the page.</span></span>
26. <span data-ttu-id="f344f-147">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f344f-147">Close the page.</span></span>
27. <span data-ttu-id="f344f-148">Klik op Stuklijst_2 om deze te openen.</span><span class="sxs-lookup"><span data-stu-id="f344f-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="f344f-149">Vouw de sectie Kosten beheren uit.</span><span class="sxs-lookup"><span data-stu-id="f344f-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="f344f-150">Typ of selecteer een waarde in het veld Kostengroep.</span><span class="sxs-lookup"><span data-stu-id="f344f-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="f344f-151">Selecteer voor dit voorbeeld: 'Kostengroep M1'.</span><span class="sxs-lookup"><span data-stu-id="f344f-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="f344f-152">Gebruik de snelkoppeling om een record op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f344f-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="f344f-153">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f344f-153">Close the page.</span></span>

