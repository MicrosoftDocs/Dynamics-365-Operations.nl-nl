--- 
title: Een uitbestede werkcel voor lean manufacturing maken
description: Als u uitbesteed werk wilt modelleren voor lean manufacturing, moet u een werkcel maken die is gekoppeld aan de leverancier die het werk levert.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d5b7149551df33d439980ec4e04fa343749daa16
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="919d4-103">Een uitbestede werkcel voor lean manufacturing maken</span><span class="sxs-lookup"><span data-stu-id="919d4-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="919d4-104">Als u uitbesteed werk wilt modelleren voor lean manufacturing, moet u een werkcel maken die is gekoppeld aan de leverancier die het werk levert.</span><span class="sxs-lookup"><span data-stu-id="919d4-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="919d4-105">Een uitbestede werkcel is gekoppeld aan de leverancier via de koppeling van een resource van het type Leverancier.</span><span class="sxs-lookup"><span data-stu-id="919d4-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="919d4-106">Als u deze opname afspeelt in het voorbeeldbedrijf USMF, kunt u de leveranciersrekening ID 1002 en site 1 selecteren.</span><span class="sxs-lookup"><span data-stu-id="919d4-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="919d4-107">Een leveranciersresource maken</span><span class="sxs-lookup"><span data-stu-id="919d4-107">Create a vendor resource</span></span>
1. <span data-ttu-id="919d4-108">Ga naar Resources.</span><span class="sxs-lookup"><span data-stu-id="919d4-108">Go to Resources.</span></span>
2. <span data-ttu-id="919d4-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="919d4-109">Click New.</span></span>
3. <span data-ttu-id="919d4-110">Typ een waarde in het veld Bron.</span><span class="sxs-lookup"><span data-stu-id="919d4-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="919d4-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="919d4-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="919d4-112">Selecteer 'Leverancier' in het veld Type.</span><span class="sxs-lookup"><span data-stu-id="919d4-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="919d4-113">Klik in het veld Leverancier op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="919d4-114">De resourcegroep maken</span><span class="sxs-lookup"><span data-stu-id="919d4-114">Create the resource group</span></span>
1. <span data-ttu-id="919d4-115">Ga naar Resourcegroepen.</span><span class="sxs-lookup"><span data-stu-id="919d4-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="919d4-116">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="919d4-116">Click New.</span></span>
3. <span data-ttu-id="919d4-117">Typ een waarde in het veld Resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="919d4-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="919d4-118">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="919d4-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="919d4-119">Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="919d4-120">Selecteer de locatie waaraan de werkcel moet worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="919d4-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="919d4-121">In theorie kan een site één site vertegenwoordigen die door een leverancier wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="919d4-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="919d4-122">Echter in de meeste gevallen worden uitbestede resources alleen toegewezen aan de site die het uitbesteed werk bestelt.</span><span class="sxs-lookup"><span data-stu-id="919d4-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="919d4-123">Zorg ervoor dat de invoer- en uitvoermagazijnen van uitbestede werkcellen zich op dezelfde locatie bevinden.</span><span class="sxs-lookup"><span data-stu-id="919d4-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="919d4-124">Typ een waarde in het veld Locatie.</span><span class="sxs-lookup"><span data-stu-id="919d4-124">In the Site field, type a value.</span></span>
7. @SysTaskRecorder:_RequestClose
8. <span data-ttu-id="919d4-125">Schakel het selectievakje Werkcel in of uit.</span><span class="sxs-lookup"><span data-stu-id="919d4-125">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="919d4-126">Klik in het veld Invoermagazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-126">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="919d4-127">Selecteer het magazijn en de locatie die worden gebruikt voor het klaarzetten van het materiaal voor de door de leverancier beheerde werkcel.</span><span class="sxs-lookup"><span data-stu-id="919d4-127">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="919d4-128">In veel gevallen worden het magazijn en locatie gemodelleerd met behulp van een afzonderlijk magazijn per leverancier en één locatie per werkcel.</span><span class="sxs-lookup"><span data-stu-id="919d4-128">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="919d4-129">Klik in het veld Invoerlocatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-129">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="919d4-130">Klik in het veld Uitvoermagazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-130">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="919d4-131">Definieer het magazijn en de locatie waar het materiaal wordt geboekt wanneer de uitbestede activiteiten van de werkcel worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="919d4-131">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="919d4-132">Het magazijn en de locatie kunnen zich op de leverancierslocatie bevinden als de leverancier de kanbantaken rapporteert.</span><span class="sxs-lookup"><span data-stu-id="919d4-132">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="919d4-133">Het magazijn en de locatie kunnen ook de ontvangstlocatie zijn die aan de volgende stap van de productiestroom is gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="919d4-133">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="919d4-134">Klik in het veld Uitvoerlocatie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-134">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="919d4-135">Vouw de sectie Kalenders uit of samen.</span><span class="sxs-lookup"><span data-stu-id="919d4-135">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="919d4-136">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="919d4-136">Click Add.</span></span>
15. <span data-ttu-id="919d4-137">Klik in het veld Kalender op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-137">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="919d4-138">Koppel de werktijdkalender van de werkcel aan de resourcegroep.</span><span class="sxs-lookup"><span data-stu-id="919d4-138">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="919d4-139">Voor kritieke resources wordt u aangeraden dat u specifieke kalenders definieert die staan voor de exacte werktijden en de verwante capaciteit van de werkcel of leverancierslocatie.</span><span class="sxs-lookup"><span data-stu-id="919d4-139">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="919d4-140">Vouw de sectie Resources uit of samen.</span><span class="sxs-lookup"><span data-stu-id="919d4-140">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="919d4-141">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="919d4-141">Click Add.</span></span>
    * <span data-ttu-id="919d4-142">Een uitbestede resourcegroep moet een gekoppelde resource van het type leverancier hebben die de resourcegroep koppelt aan de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="919d4-142">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="919d4-143">Klik in het veld Resource op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-143">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="919d4-144">Selecteer of typ de leveranciersresource die u hebt gemaakt in de vorige subtaak.</span><span class="sxs-lookup"><span data-stu-id="919d4-144">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="919d4-145">Vouw de sectie Werkcelcapaciteit uit of samen.</span><span class="sxs-lookup"><span data-stu-id="919d4-145">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="919d4-146">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="919d4-146">Click Add.</span></span>
    * <span data-ttu-id="919d4-147">Een werkcel moet een gedefinieerde capaciteit hebben.</span><span class="sxs-lookup"><span data-stu-id="919d4-147">A work cell must have a defined capacity.</span></span> <span data-ttu-id="919d4-148">In dit voorbeeld maken we een doorvoercapaciteit van 100 stuks per standaardwerkdag.</span><span class="sxs-lookup"><span data-stu-id="919d4-148">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="919d4-149">Klik in het veld Model voor productiestroom op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-149">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="919d4-150">Selecteer een optie in het veld Capaciteitsperiode.</span><span class="sxs-lookup"><span data-stu-id="919d4-150">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="919d4-151">Typ een getal in het veld Gemiddelde doorvoerhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="919d4-151">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="919d4-152">Klik in het veld Eenheid op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="919d4-152">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="919d4-153">ResolveChanges de Eenheid.</span><span class="sxs-lookup"><span data-stu-id="919d4-153">ResolveChanges the Unit.</span></span>


