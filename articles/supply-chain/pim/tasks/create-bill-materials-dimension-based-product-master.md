--- 
title: Een stuklijst maken voor een op dimensies gebaseerd productmodel
description: Voor deze procedure moet u de vorige 4 begeleidingen in deze reeks van acht registraties hebben voltooid.
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 18324fe65a78b3a55baff82a43f5326204558aca
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="e0da0-103">Een stuklijst maken voor een op dimensies gebaseerd productmodel</span><span class="sxs-lookup"><span data-stu-id="e0da0-103">Create a bill of materials for a dimension-based product master</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0da0-104">Voor deze procedure moet u de vorige 4 begeleidingen in deze reeks van acht registraties hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="e0da0-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="e0da0-105">Met de eerste 4 registraties zijn gegevens ingesteld die nodig zijn om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="e0da0-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="e0da0-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="e0da0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e0da0-107">Deze taak wordt doorgaans afgehandeld door de productontwerper.</span><span class="sxs-lookup"><span data-stu-id="e0da0-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="e0da0-108">Het product selecteren</span><span class="sxs-lookup"><span data-stu-id="e0da0-108">Select the product</span></span>
1. <span data-ttu-id="e0da0-109">Klik op Vrijgegeven productonderhoud.</span><span class="sxs-lookup"><span data-stu-id="e0da0-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="e0da0-110">Klik op Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="e0da0-110">Click Released products.</span></span>
3. <span data-ttu-id="e0da0-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e0da0-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e0da0-112">Zoek het vrijgegeven productmodel met op dimensies gebaseerde configuratietechnologie die u in de eerste taakbegeleiding in deze reeks hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e0da0-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="e0da0-113">Klik op Technicus in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="e0da0-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="e0da0-114">Klik op Stuklijstversies.</span><span class="sxs-lookup"><span data-stu-id="e0da0-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="e0da0-115">Een nieuwe stuklijst en stuklijstversie maken</span><span class="sxs-lookup"><span data-stu-id="e0da0-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="e0da0-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e0da0-116">Click New.</span></span>
2. <span data-ttu-id="e0da0-117">Klik op Stuklijst en stuklijstversie.</span><span class="sxs-lookup"><span data-stu-id="e0da0-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="e0da0-118">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="e0da0-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="e0da0-119">Een vestiging instellen</span><span class="sxs-lookup"><span data-stu-id="e0da0-119">Setting a site</span></span>  
    * <span data-ttu-id="e0da0-120">In deze procedure wordt geen specifieke vestiging voor de stuklijst ingesteld.</span><span class="sxs-lookup"><span data-stu-id="e0da0-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="e0da0-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e0da0-121">Click OK.</span></span>
5. <span data-ttu-id="e0da0-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e0da0-122">Click New.</span></span>
    * <span data-ttu-id="e0da0-123">In deze procedure worden vier regels aan de stuklijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e0da0-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="e0da0-124">Twee regels staan voor kabelopties en twee regels staan voor behuizingsopties.</span><span class="sxs-lookup"><span data-stu-id="e0da0-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="e0da0-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e0da0-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="e0da0-126">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e0da0-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e0da0-127">Selecteer artikelnummer A0001, HDMI 6' kabels.</span><span class="sxs-lookup"><span data-stu-id="e0da0-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="e0da0-128">Typ of selecteer een waarde in het veld Configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="e0da0-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="e0da0-129">Selecteer de kabelconfiguratiegroep die is gemaakt in begeleiding 4 in deze reeks.</span><span class="sxs-lookup"><span data-stu-id="e0da0-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="e0da0-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e0da0-130">Click New.</span></span>
    * <span data-ttu-id="e0da0-131">Selecteer artikelnummer A0002, HDMI 12' kabels.</span><span class="sxs-lookup"><span data-stu-id="e0da0-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="e0da0-132">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e0da0-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="e0da0-133">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e0da0-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="e0da0-134">Typ of selecteer een waarde in het veld Configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="e0da0-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="e0da0-135">Selecteer de kabelconfiguratiegroep nogmaals.</span><span class="sxs-lookup"><span data-stu-id="e0da0-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="e0da0-136">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e0da0-136">Click New.</span></span>
14. <span data-ttu-id="e0da0-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e0da0-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="e0da0-138">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e0da0-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e0da0-139">Selecteer artikelnummer D0002 behuizing</span><span class="sxs-lookup"><span data-stu-id="e0da0-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="e0da0-140">Typ of selecteer een waarde in het veld Configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="e0da0-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="e0da0-141">Selecteer de behuizingsconfiguratiegroep voor deze stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="e0da0-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="e0da0-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="e0da0-142">Click New.</span></span>
18. <span data-ttu-id="e0da0-143">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e0da0-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="e0da0-144">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="e0da0-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="e0da0-145">Selecteer artikelnummer M0007 standaardbehuizing als de laatste stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="e0da0-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="e0da0-146">Typ of selecteer een waarde in het veld Configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="e0da0-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="e0da0-147">Selecteer de behuizingsconfiguratiegroep voor de laatste stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="e0da0-147">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="e0da0-148">Goedkeuren en activeren</span><span class="sxs-lookup"><span data-stu-id="e0da0-148">Approve and activate</span></span>
1. <span data-ttu-id="e0da0-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e0da0-149">Close the page.</span></span>
2. <span data-ttu-id="e0da0-150">Klik op Goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="e0da0-150">Click Approve.</span></span>
3. <span data-ttu-id="e0da0-151">Typ of selecteer een waarde in het veld Goedgekeurd door.</span><span class="sxs-lookup"><span data-stu-id="e0da0-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="e0da0-152">Selecteer Ja in het veld Wilt u ook de stuklijst goedkeuren?</span><span class="sxs-lookup"><span data-stu-id="e0da0-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="e0da0-153">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e0da0-153">Click OK.</span></span>
6. <span data-ttu-id="e0da0-154">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="e0da0-154">Click Activate.</span></span>


