---
title: Een stuklijst maken voor een op dimensies gebaseerd productmodel
description: Voor deze procedure moet u de vorige 4 guides in deze reeks van acht registraties hebben voltooid.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7961cfb4ad0e20c49d327d83f56c08811598ac1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986282"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="2af04-103">Een stuklijst maken voor een op dimensies gebaseerd productmodel</span><span class="sxs-lookup"><span data-stu-id="2af04-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2af04-104">Voor deze procedure moet u de vorige 4 guides in deze reeks van acht registraties hebben voltooid.</span><span class="sxs-lookup"><span data-stu-id="2af04-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="2af04-105">Met de eerste 4 registraties zijn gegevens ingesteld die nodig zijn om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="2af04-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="2af04-106">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="2af04-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="2af04-107">Deze taak wordt doorgaans afgehandeld door de productontwerper.</span><span class="sxs-lookup"><span data-stu-id="2af04-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="2af04-108">Het product selecteren</span><span class="sxs-lookup"><span data-stu-id="2af04-108">Select the product</span></span>
1. <span data-ttu-id="2af04-109">Klik op Vrijgegeven productonderhoud.</span><span class="sxs-lookup"><span data-stu-id="2af04-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="2af04-110">Klik op Vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="2af04-110">Click Released products.</span></span>
3. <span data-ttu-id="2af04-111">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2af04-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2af04-112">Zoek het vrijgegeven productmodel met op dimensies gebaseerde configuratietechnologie die u in de eerste taakbegeleider in deze reeks hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2af04-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="2af04-113">Klik op Technicus in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="2af04-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="2af04-114">Klik op Stuklijstversies.</span><span class="sxs-lookup"><span data-stu-id="2af04-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="2af04-115">Een nieuwe stuklijst en stuklijstversie maken</span><span class="sxs-lookup"><span data-stu-id="2af04-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="2af04-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2af04-116">Click New.</span></span>
2. <span data-ttu-id="2af04-117">Klik op Stuklijst en stuklijstversie.</span><span class="sxs-lookup"><span data-stu-id="2af04-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="2af04-118">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="2af04-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2af04-119">Een vestiging instellen</span><span class="sxs-lookup"><span data-stu-id="2af04-119">Setting a site</span></span>  
    * <span data-ttu-id="2af04-120">In deze procedure wordt geen specifieke vestiging voor de stuklijst ingesteld.</span><span class="sxs-lookup"><span data-stu-id="2af04-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="2af04-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2af04-121">Click OK.</span></span>
5. <span data-ttu-id="2af04-122">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2af04-122">Click New.</span></span>
    * <span data-ttu-id="2af04-123">In deze procedure worden vier regels aan de stuklijst toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="2af04-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="2af04-124">Twee regels staan voor kabelopties en twee regels staan voor behuizingsopties.</span><span class="sxs-lookup"><span data-stu-id="2af04-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="2af04-125">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2af04-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="2af04-126">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="2af04-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2af04-127">Selecteer artikelnummer A0001, HDMI 6' kabels.</span><span class="sxs-lookup"><span data-stu-id="2af04-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="2af04-128">Typ of selecteer een waarde in het veld Configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="2af04-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="2af04-129">Selecteer de kabelconfiguratiegroep die is gemaakt in guide 4 in deze reeks.</span><span class="sxs-lookup"><span data-stu-id="2af04-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="2af04-130">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2af04-130">Click New.</span></span>
    * <span data-ttu-id="2af04-131">Selecteer artikelnummer A0002, HDMI 12' kabels.</span><span class="sxs-lookup"><span data-stu-id="2af04-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="2af04-132">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2af04-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="2af04-133">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="2af04-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="2af04-134">Typ of selecteer een waarde in het veld Configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="2af04-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="2af04-135">Selecteer de kabelconfiguratiegroep nogmaals.</span><span class="sxs-lookup"><span data-stu-id="2af04-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="2af04-136">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2af04-136">Click New.</span></span>
14. <span data-ttu-id="2af04-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2af04-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="2af04-138">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="2af04-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2af04-139">Selecteer artikelnummer D0002 behuizing</span><span class="sxs-lookup"><span data-stu-id="2af04-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="2af04-140">Typ of selecteer een waarde in het veld Configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="2af04-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="2af04-141">Selecteer de behuizingsconfiguratiegroep voor deze stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="2af04-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="2af04-142">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="2af04-142">Click New.</span></span>
18. <span data-ttu-id="2af04-143">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="2af04-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="2af04-144">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="2af04-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="2af04-145">Selecteer artikelnummer M0007 standaardbehuizing als de laatste stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="2af04-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="2af04-146">Typ of selecteer een waarde in het veld Configuratiegroep.</span><span class="sxs-lookup"><span data-stu-id="2af04-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="2af04-147">Selecteer de behuizingsconfiguratiegroep voor de laatste stuklijstregel.</span><span class="sxs-lookup"><span data-stu-id="2af04-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="2af04-148">Goedkeuren en activeren</span><span class="sxs-lookup"><span data-stu-id="2af04-148">Approve and activate</span></span>
1. <span data-ttu-id="2af04-149">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="2af04-149">Close the page.</span></span>
2. <span data-ttu-id="2af04-150">Klik op Goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="2af04-150">Click Approve.</span></span>
3. <span data-ttu-id="2af04-151">Typ of selecteer een waarde in het veld Goedgekeurd door.</span><span class="sxs-lookup"><span data-stu-id="2af04-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="2af04-152">Selecteer Ja in het veld Wilt u ook de stuklijst goedkeuren?</span><span class="sxs-lookup"><span data-stu-id="2af04-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="2af04-153">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="2af04-153">Click OK.</span></span>
6. <span data-ttu-id="2af04-154">Klik op Activeren.</span><span class="sxs-lookup"><span data-stu-id="2af04-154">Click Activate.</span></span>

