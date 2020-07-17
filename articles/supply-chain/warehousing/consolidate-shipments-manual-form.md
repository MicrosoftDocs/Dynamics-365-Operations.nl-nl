---
title: Zendingen handmatig consolideren via de pagina Zendingen consolideren
description: Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd via de pagina Zendingen consolideren.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: acc6e1d09894b57d2bb063bacbcddef239c1a8bd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383742"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="26735-103">Zendingen handmatig consolideren via de pagina Zendingen consolideren</span><span class="sxs-lookup"><span data-stu-id="26735-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26735-104">Dit onderwerp bevat een scenario waarin meerdere orders naar het magazijn worden vrijgegeven en vervolgens worden geconsolideerd via de pagina **Zendingen consolideren**.</span><span class="sxs-lookup"><span data-stu-id="26735-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="26735-105">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="26735-105">Make demo data available</span></span>

<span data-ttu-id="26735-106">Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="26735-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="26735-107">Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="26735-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="26735-108">Consolidatiebeleid voor zendingen en productfilters instellen</span><span class="sxs-lookup"><span data-stu-id="26735-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="26735-109">In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="26735-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="26735-110">Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.</span><span class="sxs-lookup"><span data-stu-id="26735-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="26735-111">De verkooporders voor dit scenario maken</span><span class="sxs-lookup"><span data-stu-id="26735-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="26735-112">Maak eerst een verzameling verkooporders waarmee u kunt werken.</span><span class="sxs-lookup"><span data-stu-id="26735-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="26735-113">U moet werken met een magazijn dat is ingeschakeld voor geavanceerde magazijnprocessen (WMS).</span><span class="sxs-lookup"><span data-stu-id="26735-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="26735-114">Tenzij een ander magazijn expliciet wordt vermeld, moet voor elk van de volgende sets orders hetzelfde magazijn worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="26735-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="26735-115">Ga naar **Klanten \> Orders \> Alle verkooporders** en maak een verzameling verkooporders met de instellingen die in de volgende subsecties worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="26735-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="26735-116">Verkooporders 1 en 2 maken</span><span class="sxs-lookup"><span data-stu-id="26735-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="26735-117">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="26735-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="26735-118">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="26735-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="26735-119">**Groep:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="26735-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="26735-120">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="26735-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="26735-121">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="26735-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="26735-122">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="26735-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="26735-123">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="26735-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="26735-124">Verkooporders 3 en 4 maken</span><span class="sxs-lookup"><span data-stu-id="26735-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="26735-125">Maak twee identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="26735-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="26735-126">**Klantrekening:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="26735-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="26735-127">**Groep:** laat dit veld leeg.</span><span class="sxs-lookup"><span data-stu-id="26735-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="26735-128">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="26735-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="26735-129">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="26735-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="26735-130">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="26735-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="26735-131">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="26735-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="26735-132">De orders vrijgeven naar het magazijn</span><span class="sxs-lookup"><span data-stu-id="26735-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="26735-133">Voer de volgende stappen uit om elke verkooporder die u voor dit scenario hebt gemaakt, vrij te geven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="26735-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="26735-134">Ga naar **Klanten \> Orders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="26735-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="26735-135">Zoek en selecteer de verkooporder om vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="26735-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="26735-136">Selecteer in het actievenster op het tabblad **Magazijn** de optie **Acties \> Vrijgave naar magazijn** om de geselecteerde verkooporder vrij te geven.</span><span class="sxs-lookup"><span data-stu-id="26735-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="26735-137">Herhaal deze procedure voor elke andere verkooporder die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="26735-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="26735-138">Verzendingen consolideren</span><span class="sxs-lookup"><span data-stu-id="26735-138">Consolidate shipments</span></span>

1. <span data-ttu-id="26735-139">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="26735-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="26735-140">Zoek en selecteer een zending die is gemaakt toen verkooporder 1 werd vrijgegeven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="26735-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="26735-141">(Het veld **Consolidatiebeleid voor zendingen** moet zijn ingesteld op *Ordergroep*.)</span><span class="sxs-lookup"><span data-stu-id="26735-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="26735-142">Selecteer in het actievenster op het tabblad **Zendingen** de optie **Zendingen \> Zendingen consolideren**.</span><span class="sxs-lookup"><span data-stu-id="26735-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="26735-143">Controleer de zendingen die worden voorgesteld voor consolidatie.</span><span class="sxs-lookup"><span data-stu-id="26735-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="26735-144">Er moet slechts één zending met hetzelfde beleid worden voorgesteld voor consolidatie.</span><span class="sxs-lookup"><span data-stu-id="26735-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="26735-145">Sluit de pagina **Zendingsconsolidatie**.</span><span class="sxs-lookup"><span data-stu-id="26735-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="26735-146">Zoek en selecteer een zending die is gemaakt toen verkooporder 3 werd vrijgegeven naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="26735-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="26735-147">(Het veld **Consolidatiebeleid voor zendingen** moet zijn ingesteld op *Standaard*.)</span><span class="sxs-lookup"><span data-stu-id="26735-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="26735-148">Selecteer in het actievenster op het tabblad **Zendingen** de optie **Zendingen \> Zendingen consolideren**.</span><span class="sxs-lookup"><span data-stu-id="26735-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="26735-149">Controleer of geen zendingen worden voorgesteld voor consolidatie.</span><span class="sxs-lookup"><span data-stu-id="26735-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="26735-150">Selecteer **Filters weergeven**.</span><span class="sxs-lookup"><span data-stu-id="26735-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="26735-151">Verwijder in het deelvenster **Filters** het filter **Ordernummer** en selecteer vervolgens **Toepassen**.</span><span class="sxs-lookup"><span data-stu-id="26735-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="26735-152">Controleer de zendingen die worden voorgesteld voor consolidatie.</span><span class="sxs-lookup"><span data-stu-id="26735-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="26735-153">Er moet slechts één zending met hetzelfde beleid worden voorgesteld voor consolidatie.</span><span class="sxs-lookup"><span data-stu-id="26735-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26735-154">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="26735-154">Additional resources</span></span>

- [<span data-ttu-id="26735-155">Beleidsregels voor consolidatie van zendingen</span><span class="sxs-lookup"><span data-stu-id="26735-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="26735-156">Consolidatiebeleid voor zendingen configureren</span><span class="sxs-lookup"><span data-stu-id="26735-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)