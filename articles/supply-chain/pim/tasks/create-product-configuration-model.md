---
title: Een productconfiguratiemodel maken
description: Deze procedure toont aan hoe u een productconfiguratiemodel maakt en basisinformatie, zoals kenmerken en subcomponenten, invoert.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921360"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="323a7-103">Een productconfiguratiemodel maken</span><span class="sxs-lookup"><span data-stu-id="323a7-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="323a7-104">Deze procedure toont aan hoe u een productconfiguratiemodel maakt en basisinformatie, zoals kenmerken en subcomponenten, invoert.</span><span class="sxs-lookup"><span data-stu-id="323a7-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="323a7-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="323a7-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="323a7-106">Een productmodel maken</span><span class="sxs-lookup"><span data-stu-id="323a7-106">Create a product model</span></span>

1. <span data-ttu-id="323a7-107">Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.</span><span class="sxs-lookup"><span data-stu-id="323a7-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="323a7-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="323a7-108">Select **New**.</span></span>
1. <span data-ttu-id="323a7-109">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="323a7-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="323a7-110">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="323a7-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="323a7-111">Selecteer een optie in het veld **Oplossingsstrategie**.</span><span class="sxs-lookup"><span data-stu-id="323a7-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="323a7-112">De oplossingsstrategie bepaalt hoe de beperkingen in een op beperkingen gebaseerd productconfiguratiemodel worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="323a7-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="323a7-113">Deze selectie kan een invloed hebben op de prestaties van het productconfiguratiemodel.</span><span class="sxs-lookup"><span data-stu-id="323a7-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="323a7-114">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="323a7-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="323a7-115">Het hoofdcomponent vertegenwoordigt het productconfiguratiemodel, maar kan ook in andere productmodellen worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="323a7-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="323a7-116">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="323a7-116">Select **OK**.</span></span>
1. <span data-ttu-id="323a7-117">Selecteer een optie in het veld **Configuraties opnieuw gebruiken**.</span><span class="sxs-lookup"><span data-stu-id="323a7-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="323a7-118">Als de parameter Configuraties opnieuw gebruiken op Ja is ingesteld, controleert het systeem identieke configuraties na elke sessie en elk hergebruik van de configuratie als een exacte overeenkomst wordt gevonden.</span><span class="sxs-lookup"><span data-stu-id="323a7-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="323a7-119">Kenmerken toevoegen</span><span class="sxs-lookup"><span data-stu-id="323a7-119">Add attributes</span></span>

1. <span data-ttu-id="323a7-120">Vouw de sectie **Kenmerken** uit.</span><span class="sxs-lookup"><span data-stu-id="323a7-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="323a7-121">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="323a7-121">Select **Add**.</span></span>
3. <span data-ttu-id="323a7-122">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="323a7-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="323a7-123">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="323a7-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="323a7-124">Typ een waarde in het veld **Oplossingsnaam**.</span><span class="sxs-lookup"><span data-stu-id="323a7-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="323a7-125">De oplossingsnaam wordt gebruikt door oplosser van beperkingen van de productconfiguratie.</span><span class="sxs-lookup"><span data-stu-id="323a7-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="323a7-126">Deze mag geen spaties of speciale tekens bevatten, behalve _ (onderstrepingsteken).</span><span class="sxs-lookup"><span data-stu-id="323a7-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="323a7-127">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="323a7-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="323a7-128">De omschrijvingstekst wordt aan de gebruiker van de configuratie weergegeven en kan daarom fungeren als hulp bij het selecteren van de juiste kenmerkwaarde.</span><span class="sxs-lookup"><span data-stu-id="323a7-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="323a7-129">Typ of selecteer een waarde in het veld **Kenmerktype**.</span><span class="sxs-lookup"><span data-stu-id="323a7-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="323a7-130">Het kenmerktype bepaalt welke waarden beschikbaar zijn voor het kenmerk.</span><span class="sxs-lookup"><span data-stu-id="323a7-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="323a7-131">Schakel het selectievakje **Opnemen in hergebruik** in.</span><span class="sxs-lookup"><span data-stu-id="323a7-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="323a7-132">Deze optie is alleen beschikbaar als de optie Configuraties opnieuw gebruiken is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="323a7-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="323a7-133">Als het selectievakje van het kenmerk wordt ingeschakeld, wordt met dit kenmerk rekening gehouden wanneer het systeem naar een exacte overeenkomst zoekt.</span><span class="sxs-lookup"><span data-stu-id="323a7-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="323a7-134">Subonderdelen toevoegen</span><span class="sxs-lookup"><span data-stu-id="323a7-134">Add subcomponents</span></span>

1. <span data-ttu-id="323a7-135">Vouw de sectie **Subonderdelen** uit.</span><span class="sxs-lookup"><span data-stu-id="323a7-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="323a7-136">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="323a7-136">Select **Add**.</span></span>
3. <span data-ttu-id="323a7-137">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="323a7-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="323a7-138">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="323a7-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="323a7-139">Typ een waarde in het veld **Oplossingsnaam**.</span><span class="sxs-lookup"><span data-stu-id="323a7-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="323a7-140">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="323a7-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="323a7-141">Typ of selecteer een waarde in het veld **Onderdeel**.</span><span class="sxs-lookup"><span data-stu-id="323a7-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="323a7-142">Elke subonderdeel moet naar een componentdefinitie verwijzen.</span><span class="sxs-lookup"><span data-stu-id="323a7-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="323a7-143">Dit ontwerp ondersteunt herbruikbare onderdelen en zorgt ervoor dat een onderdeel, als het is gedefinieerd, in veel productmodellen kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="323a7-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="323a7-144">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="323a7-144">Select **Save**.</span></span>
9. <span data-ttu-id="323a7-145">Selecteer **Details van stuklijstregel**.</span><span class="sxs-lookup"><span data-stu-id="323a7-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="323a7-146">Met het formulier Regeldetails van stuklijst kan de gebruiker de vereiste eigenschappen voor het subonderdeel selecteren.</span><span class="sxs-lookup"><span data-stu-id="323a7-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="323a7-147">Elke eigenschap kan een vaste waarde krijgen of aan een kenmerk worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="323a7-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="323a7-148">De toewijzing aan een kenmerk zorgt ervoor dat de regeleigenschap van de stuklijst verschillende waarden krijgt, afhankelijk van de geselecteerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="323a7-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="323a7-149">Typ of selecteer een waarde in het veld **Artikelnummer**.</span><span class="sxs-lookup"><span data-stu-id="323a7-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="323a7-150">Elke subonderdeel vertegenwoordigt een configureerbaar productmodel met op beperkingen gebaseerde configuratietechnologie.</span><span class="sxs-lookup"><span data-stu-id="323a7-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="323a7-151">De verwijzing wordt gemaakt door het artikelnummer.</span><span class="sxs-lookup"><span data-stu-id="323a7-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="323a7-152">Schakel het selectievakje **Instellen** in.</span><span class="sxs-lookup"><span data-stu-id="323a7-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="323a7-153">Selecteer **Ja** in het veld **Berekening**.</span><span class="sxs-lookup"><span data-stu-id="323a7-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="323a7-154">Het instellen van de berekeningsoptie zorgt ervoor dat het product wordt opgenomen bij de uitvoering van een kostenberekening voor het product.</span><span class="sxs-lookup"><span data-stu-id="323a7-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="323a7-155">Selecteer het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="323a7-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="323a7-156">Schakel het selectievakje **Instellen** in.</span><span class="sxs-lookup"><span data-stu-id="323a7-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="323a7-157">Voer een getal in het veld **Hoeveelheid** in.</span><span class="sxs-lookup"><span data-stu-id="323a7-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="323a7-158">Het hoeveelheidsveld bepaalt hoeveel van dit product wordt verbruikt in het geconfigureerde product.</span><span class="sxs-lookup"><span data-stu-id="323a7-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="323a7-159">Schakel het selectievakje **Instellen** in.</span><span class="sxs-lookup"><span data-stu-id="323a7-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="323a7-160">Voer in het veld **Per reeks** een getal in.</span><span class="sxs-lookup"><span data-stu-id="323a7-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="323a7-161">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="323a7-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]