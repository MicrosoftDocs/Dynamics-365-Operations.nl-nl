---
title: Een productconfiguratiemodel maken
description: Deze procedure toont aan hoe u een productconfiguratiemodel maakt en basisinformatie, zoals kenmerken en subcomponenten, invoert.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3d19c680e14fe4074314a95937d30d4ad2c7a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550624"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="955e7-103">Een productconfiguratiemodel maken</span><span class="sxs-lookup"><span data-stu-id="955e7-103">Create a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="955e7-104">Deze procedure toont aan hoe u een productconfiguratiemodel maakt en basisinformatie, zoals kenmerken en subcomponenten, invoert.</span><span class="sxs-lookup"><span data-stu-id="955e7-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="955e7-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="955e7-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="955e7-106">Een productmodel maken</span><span class="sxs-lookup"><span data-stu-id="955e7-106">Create a product model</span></span>
1. <span data-ttu-id="955e7-107">Klik op Definitie van productvariantmodel.</span><span class="sxs-lookup"><span data-stu-id="955e7-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="955e7-108">Klik op Productconfiguratiemodellen.</span><span class="sxs-lookup"><span data-stu-id="955e7-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="955e7-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="955e7-109">Click New.</span></span>
4. <span data-ttu-id="955e7-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="955e7-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="955e7-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="955e7-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="955e7-112">Selecteer een optie in het veld Oplossingsstrategie.</span><span class="sxs-lookup"><span data-stu-id="955e7-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="955e7-113">De oplossingsstrategie bepaalt hoe de beperkingen in een op beperkingen gebaseerd productconfiguratiemodel worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="955e7-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="955e7-114">Deze selectie kan een invloed hebben op de prestaties van het productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="955e7-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="955e7-115">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="955e7-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="955e7-116">Het hoofdcomponent vertegenwoordigt het productconfiguratiemodel, maar kan ook in andere productmodellen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="955e7-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="955e7-117">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="955e7-117">Click OK.</span></span>
9. <span data-ttu-id="955e7-118">Selecteer een optie in het veld Configuraties opnieuw gebruiken.</span><span class="sxs-lookup"><span data-stu-id="955e7-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="955e7-119">Als de parameter Configuraties opnieuw gebruiken op Ja is ingesteld, controleert het systeem identieke configuraties na elke sessie en elk hergebruik van de configuratie als een exacte overeenkomst wordt gevonden.</span><span class="sxs-lookup"><span data-stu-id="955e7-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="955e7-120">Kenmerken toevoegen</span><span class="sxs-lookup"><span data-stu-id="955e7-120">Add attributes</span></span>
1. <span data-ttu-id="955e7-121">Vouw de sectie Kenmerken uit.</span><span class="sxs-lookup"><span data-stu-id="955e7-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="955e7-122">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="955e7-122">Click Add.</span></span>
3. <span data-ttu-id="955e7-123">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="955e7-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="955e7-124">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="955e7-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="955e7-125">Typ een waarde in het veld Oplossingsnaam.</span><span class="sxs-lookup"><span data-stu-id="955e7-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="955e7-126">De oplossingsnaam wordt gebruikt door oplosser van beperkingen van de productconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="955e7-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="955e7-127">Deze mag geen spaties of speciale tekens bevatten, behalve _ (onderstrepingsteken).</span><span class="sxs-lookup"><span data-stu-id="955e7-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="955e7-128">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="955e7-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="955e7-129">De omschrijvingstekst wordt aan de gebruiker van de configuratie weergegeven en kan daarom fungeren als hulp bij het selecteren van de juiste kenmerkwaarde.</span><span class="sxs-lookup"><span data-stu-id="955e7-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="955e7-130">Typ of selecteer een waarde in het veld Kenmerktype.</span><span class="sxs-lookup"><span data-stu-id="955e7-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="955e7-131">Het kenmerktype bepaalt welke waarden beschikbaar zijn voor het kenmerk.</span><span class="sxs-lookup"><span data-stu-id="955e7-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="955e7-132">Schakel het selectievakje Opnemen in hergebruik in.</span><span class="sxs-lookup"><span data-stu-id="955e7-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="955e7-133">Deze optie is alleen beschikbaar als de optie Configuraties opnieuw gebruiken is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="955e7-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="955e7-134">Als het selectievakje van het kenmerk wordt ingeschakeld, wordt met dit kenmerk rekening gehouden wanneer het systeem naar een exacte overeenkomst zoekt.</span><span class="sxs-lookup"><span data-stu-id="955e7-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="955e7-135">Subonderdelen toevoegen</span><span class="sxs-lookup"><span data-stu-id="955e7-135">Add subcomponents</span></span>
1. <span data-ttu-id="955e7-136">Vouw de sectie Subonderdelen uit.</span><span class="sxs-lookup"><span data-stu-id="955e7-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="955e7-137">Klik op Toevoegen.</span><span class="sxs-lookup"><span data-stu-id="955e7-137">Click Add.</span></span>
3. <span data-ttu-id="955e7-138">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="955e7-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="955e7-139">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="955e7-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="955e7-140">Typ een waarde in het veld Oplossingsnaam.</span><span class="sxs-lookup"><span data-stu-id="955e7-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="955e7-141">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="955e7-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="955e7-142">Typ of selecteer een waarde in het veld Onderdeel.</span><span class="sxs-lookup"><span data-stu-id="955e7-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="955e7-143">Elke subonderdeel moet naar een componentdefinitie verwijzen.</span><span class="sxs-lookup"><span data-stu-id="955e7-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="955e7-144">Dit ontwerp ondersteunt herbruikbare onderdelen en zorgt ervoor dat een onderdeel, als het is gedefinieerd, in veel productmodellen kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="955e7-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="955e7-145">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="955e7-145">Click Save.</span></span>
9. <span data-ttu-id="955e7-146">Klik op Regeldetails van stuklijst.</span><span class="sxs-lookup"><span data-stu-id="955e7-146">Click BOM line details.</span></span>
    * <span data-ttu-id="955e7-147">Met het formulier Regeldetails van stuklijst kan de gebruiker de vereiste eigenschappen voor het subonderdeel selecteren.</span><span class="sxs-lookup"><span data-stu-id="955e7-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="955e7-148">Elke eigenschap kan een vaste waarde krijgen of aan een kenmerk worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="955e7-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="955e7-149">De toewijzing aan een kenmerk zorgt ervoor dat de regeleigenschap van de stuklijst verschillende waarden krijgt, afhankelijk van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="955e7-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="955e7-150">Typ of selecteer een waarde in het veld Artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="955e7-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="955e7-151">Elke subonderdeel vertegenwoordigt een configureerbaar productmodel met op beperkingen gebaseerde configuratietechnologie.</span><span class="sxs-lookup"><span data-stu-id="955e7-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="955e7-152">De verwijzing wordt gemaakt door het artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="955e7-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="955e7-153">Schakel het selectievakje Instellen in.</span><span class="sxs-lookup"><span data-stu-id="955e7-153">Select the Set check box.</span></span>
12. <span data-ttu-id="955e7-154">Selecteer Ja in het veld Berekening.</span><span class="sxs-lookup"><span data-stu-id="955e7-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="955e7-155">Het instellen van de berekeningsoptie zorgt ervoor dat het product wordt opgenomen bij de uitvoering van een kostenberekening voor het product.</span><span class="sxs-lookup"><span data-stu-id="955e7-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="955e7-156">Klik op het tabblad Instellingen.</span><span class="sxs-lookup"><span data-stu-id="955e7-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="955e7-157">Schakel het selectievakje Instellen in.</span><span class="sxs-lookup"><span data-stu-id="955e7-157">Select the Set check box.</span></span>
15. <span data-ttu-id="955e7-158">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="955e7-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="955e7-159">Het hoeveelheidsveld bepaalt hoeveel van dit product wordt verbruikt in het geconfigureerde product.</span><span class="sxs-lookup"><span data-stu-id="955e7-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="955e7-160">Schakel het selectievakje Instellen in.</span><span class="sxs-lookup"><span data-stu-id="955e7-160">Select the Set check box.</span></span>
17. <span data-ttu-id="955e7-161">Voer in het veld Per reeks een getal in.</span><span class="sxs-lookup"><span data-stu-id="955e7-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="955e7-162">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="955e7-162">Click OK.</span></span>

