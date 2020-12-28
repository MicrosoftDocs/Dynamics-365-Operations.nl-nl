---
title: Conversie van maateenheid per productvariant
description: In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor productvarianten. Het bevat een voorbeeld van de instellingen.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 71d35d47a703f0931ba3b4ab5df21c7199c7ea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425731"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="1b93f-104">Conversie van maateenheid per productvariant</span><span class="sxs-lookup"><span data-stu-id="1b93f-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b93f-105">In dit onderwerp wordt uitgelegd hoe conversies van maateenheden kunnen worden ingesteld voor verschillende productvarianten.</span><span class="sxs-lookup"><span data-stu-id="1b93f-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="1b93f-106">In plaats van meerdere afzonderlijke producten te maken die moeten worden onderhouden, kunt u productvarianten gebruiken om variaties te maken van een enkel product.</span><span class="sxs-lookup"><span data-stu-id="1b93f-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="1b93f-107">Een productvariant kan bijvoorbeeld een t-shirt van een bepaalde maat en kleur zijn.</span><span class="sxs-lookup"><span data-stu-id="1b93f-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="1b93f-108">Voorheen konden eenheidconversies alleen in het productmodel worden ingesteld.</span><span class="sxs-lookup"><span data-stu-id="1b93f-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="1b93f-109">Daarom hadden alle productvarianten dezelfde regels voor eenheidsomrekening.</span><span class="sxs-lookup"><span data-stu-id="1b93f-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="1b93f-110">Wanneer echter de functie *Maateenheid omrekeningen voor productvarianten* is ingeschakeld, en uw t-shirts in dozen wordt verkocht en het aantal t-shirts dan kan worden verpakt in een doos hafhankelijk is van de maat van de t-shirts. kunt u nu eenheidsomrekeningen instellen tussen de verschillende shirtmaten en de dozen die voor de verpakking worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1b93f-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="1b93f-111">De functie inschakelen in uw systeem</span><span class="sxs-lookup"><span data-stu-id="1b93f-111">Turn on the feature in your system</span></span>

<span data-ttu-id="1b93f-112">Als deze functie nog niet in uw systeem wordt weergegeven, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Maateenheid omrekeningen voor productvarianten* in.</span><span class="sxs-lookup"><span data-stu-id="1b93f-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="1b93f-113">Een product voor eenheidconversie per variant instellen</span><span class="sxs-lookup"><span data-stu-id="1b93f-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="1b93f-114">Productvarianten kunnen alleen worden gemaakt voor producten die productmodellen zijn.</span><span class="sxs-lookup"><span data-stu-id="1b93f-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="1b93f-115">Zie [Een productmodel maken](tasks/create-product-master.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1b93f-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="1b93f-116">De functie *Maateenheid omrekeningen voor productvarianten* is niet beschikbaar voor producten die zijn ingesteld voor catch-weight-processen.</span><span class="sxs-lookup"><span data-stu-id="1b93f-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="1b93f-117">Voer de volgende stappen uit om een productmodel te configureren voor ondersteuning van eenheidsomrekening per variant.</span><span class="sxs-lookup"><span data-stu-id="1b93f-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="1b93f-118">Ga naar **Productgegevensbeheer \> Producten \> Productmodellen**.</span><span class="sxs-lookup"><span data-stu-id="1b93f-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="1b93f-119">Maak of open een productmodel om naar de pagina **Productgegevens** te gaan.</span><span class="sxs-lookup"><span data-stu-id="1b93f-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="1b93f-120">Stel de optie **Maateenheidconversies inschakelen** in op *Ja*.</span><span class="sxs-lookup"><span data-stu-id="1b93f-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="1b93f-121">Selecteer in het Actievenster op het tabblad **Product** in de groep **Instellen** de optie **Eenheidsomrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="1b93f-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="1b93f-122">De pagina **Eenheidsomrekeningen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="1b93f-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="1b93f-123">Selecteer een van de volgende tabbladen:</span><span class="sxs-lookup"><span data-stu-id="1b93f-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="1b93f-124">**Omrekeningen binnen klasse**: selecteer dit tabblad om te converteren tussen eenheden die tot dezelfde eenheidsklasse behoren.</span><span class="sxs-lookup"><span data-stu-id="1b93f-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="1b93f-125">**Omrekeningen tussen klassen**: selecteer dit tabblad om te converteren tussen eenheden die tot verschillende eenheidsklassen behoren.</span><span class="sxs-lookup"><span data-stu-id="1b93f-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="1b93f-126">Selecteer **Nieuw** om een nieuwe eenheidsomrekening toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="1b93f-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="1b93f-127">Stel het veld **Conversie maken voor** in op een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="1b93f-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="1b93f-128">**Product**: als u deze waarde selecteert, kunt u een eenheidconversie instellen voor het productmodel.</span><span class="sxs-lookup"><span data-stu-id="1b93f-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="1b93f-129">Deze eenheidsomrekening wordt gebruikt als terugval voor alle productvarianten waarvoor geen eenheidsomrekening is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="1b93f-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="1b93f-130">**Productvariant**: als u deze waarde selecteert, kunt u een eenheidconversie instellen voor een specifieke productvariant.</span><span class="sxs-lookup"><span data-stu-id="1b93f-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="1b93f-131">Gebruik het veld **Productvariant** om de variant te selecteren.</span><span class="sxs-lookup"><span data-stu-id="1b93f-131">Use the **Product variant** field to select the variant.</span></span>

    ![![Een nieuwe eenheidsomrekening toevoegen](media/uom-new-conversion.png "Een nieuwe eenheidsomrekening toevoegen")](media/uom-new-conversion.png "Adding a new unit conversion")

1. <span data-ttu-id="1b93f-133">Gebruik de andere velden die zijn opgegeven om de eenheidsomrekening in te stellen.</span><span class="sxs-lookup"><span data-stu-id="1b93f-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="1b93f-134">Selecteer **OK** om de nieuwe eenheidsomrekening op te slaan.</span><span class="sxs-lookup"><span data-stu-id="1b93f-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="1b93f-135">U kunt de pagina **Eenheidsomrekeningen** voor een product of een productvariant openen vanaf een van de volgende pagina's:</span><span class="sxs-lookup"><span data-stu-id="1b93f-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="1b93f-136">Productgegevens</span><span class="sxs-lookup"><span data-stu-id="1b93f-136">Product details</span></span>
> - <span data-ttu-id="1b93f-137">Details van vrijgegeven producten</span><span class="sxs-lookup"><span data-stu-id="1b93f-137">Released products details</span></span>
> - <span data-ttu-id="1b93f-138">Vrijgegeven productvarianten</span><span class="sxs-lookup"><span data-stu-id="1b93f-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="1b93f-139">Voorbeeldscenario</span><span class="sxs-lookup"><span data-stu-id="1b93f-139">Example scenario</span></span>

<span data-ttu-id="1b93f-140">In dit scenario verkoopt een bedrijf t-shirts in de maten small, medium, large en extra large.</span><span class="sxs-lookup"><span data-stu-id="1b93f-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="1b93f-141">Het t-shirt is gedefinieerd als een product en de verschillende maten zijn gedefinieerd als varianten van dat product.</span><span class="sxs-lookup"><span data-stu-id="1b93f-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="1b93f-142">De shirts worden in dozen verpakt.</span><span class="sxs-lookup"><span data-stu-id="1b93f-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="1b93f-143">Voor de maten small, medium en large passen er vijf shirts in elke doos.</span><span class="sxs-lookup"><span data-stu-id="1b93f-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="1b93f-144">Voor de maat extra large is er echter ruimte voor slechts vier shirts in elke doos.</span><span class="sxs-lookup"><span data-stu-id="1b93f-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="1b93f-145">Het bedrijf wil de verschillende varianten van de t-shirts in de eenheid *Stuks* bijhouden, maar verkoopt de t-shirts in de eenheid *Dozen*.</span><span class="sxs-lookup"><span data-stu-id="1b93f-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="1b93f-146">Voor de maten small, medium en large luidt de omrekening tussen de voorraadeenheid en de verkoopeenheid 1 doos = 5 stuks.</span><span class="sxs-lookup"><span data-stu-id="1b93f-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="1b93f-147">Voor de maat extra large is de omrekening 1 doos = 4 stuks.</span><span class="sxs-lookup"><span data-stu-id="1b93f-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="1b93f-148">Ga naar de pagina **Details van vrijgegeven producten** voor het product **T-shirt** en open de pagina **Eenheidsomrekening**.</span><span class="sxs-lookup"><span data-stu-id="1b93f-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="1b93f-149">Stel op de pagina **Eenheidsomrekeningen** de volgende eenheidsomrekening in voor de productvariant **Extra large**.</span><span class="sxs-lookup"><span data-stu-id="1b93f-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="1b93f-150">Veld</span><span class="sxs-lookup"><span data-stu-id="1b93f-150">Field</span></span>                 | <span data-ttu-id="1b93f-151">Instelling</span><span class="sxs-lookup"><span data-stu-id="1b93f-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="1b93f-152">Conversie maken voor</span><span class="sxs-lookup"><span data-stu-id="1b93f-152">Create conversion for</span></span> | <span data-ttu-id="1b93f-153">Productvariant</span><span class="sxs-lookup"><span data-stu-id="1b93f-153">Product variant</span></span>         |
    | <span data-ttu-id="1b93f-154">Productvariant</span><span class="sxs-lookup"><span data-stu-id="1b93f-154">Product variant</span></span>       | <span data-ttu-id="1b93f-155">T-Shirt : : Extra large : :</span><span class="sxs-lookup"><span data-stu-id="1b93f-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="1b93f-156">Van eenheid</span><span class="sxs-lookup"><span data-stu-id="1b93f-156">From unit</span></span>             | <span data-ttu-id="1b93f-157">Dozen</span><span class="sxs-lookup"><span data-stu-id="1b93f-157">Boxes</span></span>                   |
    | <span data-ttu-id="1b93f-158">Factor</span><span class="sxs-lookup"><span data-stu-id="1b93f-158">Factor</span></span>                | <span data-ttu-id="1b93f-159">4</span><span class="sxs-lookup"><span data-stu-id="1b93f-159">4</span></span>                       |
    | <span data-ttu-id="1b93f-160">Naar eenheid</span><span class="sxs-lookup"><span data-stu-id="1b93f-160">To Unit</span></span>               | <span data-ttu-id="1b93f-161">Stuks</span><span class="sxs-lookup"><span data-stu-id="1b93f-161">Pieces</span></span>                  |

1. <span data-ttu-id="1b93f-162">Aangezien de productvarianten **Small**, **Medium** en **Large** allemaal dezelfde eenheidsomrekening hebben tussen de eenheden *Doos* en *Stuks*, kunt u hiervoor de volgende eenheidsomrekening definiëren in het productmodel.</span><span class="sxs-lookup"><span data-stu-id="1b93f-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="1b93f-163">Veld</span><span class="sxs-lookup"><span data-stu-id="1b93f-163">Field</span></span>                 | <span data-ttu-id="1b93f-164">Instelling</span><span class="sxs-lookup"><span data-stu-id="1b93f-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="1b93f-165">Conversie maken voor</span><span class="sxs-lookup"><span data-stu-id="1b93f-165">Create conversion for</span></span> | <span data-ttu-id="1b93f-166">Artikel</span><span class="sxs-lookup"><span data-stu-id="1b93f-166">Product</span></span> |
    | <span data-ttu-id="1b93f-167">Artikel</span><span class="sxs-lookup"><span data-stu-id="1b93f-167">Product</span></span>               | <span data-ttu-id="1b93f-168">T-shirt</span><span class="sxs-lookup"><span data-stu-id="1b93f-168">T-Shirt</span></span> |
    | <span data-ttu-id="1b93f-169">Van eenheid</span><span class="sxs-lookup"><span data-stu-id="1b93f-169">From unit</span></span>             | <span data-ttu-id="1b93f-170">Dozen</span><span class="sxs-lookup"><span data-stu-id="1b93f-170">Boxes</span></span>   |
    | <span data-ttu-id="1b93f-171">Factor</span><span class="sxs-lookup"><span data-stu-id="1b93f-171">Factor</span></span>                | <span data-ttu-id="1b93f-172">5</span><span class="sxs-lookup"><span data-stu-id="1b93f-172">5</span></span>       |
    | <span data-ttu-id="1b93f-173">Naar eenheid</span><span class="sxs-lookup"><span data-stu-id="1b93f-173">To Unit</span></span>               | <span data-ttu-id="1b93f-174">Stuks</span><span class="sxs-lookup"><span data-stu-id="1b93f-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="1b93f-175">De eenheidconversies bijwerken met Excel</span><span class="sxs-lookup"><span data-stu-id="1b93f-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="1b93f-176">Als een product veel productvarianten met verschillende eenheidsomrekeningen heeft, is het een goed idee om de eenheidsomrekeningen naar een Microsoft Excel-werkmap te exporteren, deze bij te werken en ze vervolgens terug te publiceren naar Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1b93f-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="1b93f-177">Als u eenheidsomrekeningen naar Excel wilt exporteren, selecteert u op de pagina **Eenheidsomrekeningen** in het actievenster de optie **Openen in Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="1b93f-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b93f-178">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="1b93f-178">Additional resources</span></span>

[<span data-ttu-id="1b93f-179">Maateenheid beheren</span><span class="sxs-lookup"><span data-stu-id="1b93f-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)
