---
title: Zendingen consolideren wanneer het consolidatiebeleid voor zendingen wordt overschreven via de pagina Vrijgave naar magazijn
description: In dit onderwerp wordt een scenario weergegeven waarbij een of meer verkoopregels handmatig naar het magazijn moeten worden vrijgegeven via de pagina Vrijgave naar magazijn. Het door het systeem gedefinieerde consolidatiebeleid voor zendingen moet worden overschreven vóór de vrijgave.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: dcd619ad2906d4224966e2696712ed0e71886eb2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837484"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a><span data-ttu-id="c307d-103">Zendingen consolideren wanneer het consolidatiebeleid voor zendingen wordt overschreven via de pagina Vrijgave naar magazijn</span><span class="sxs-lookup"><span data-stu-id="c307d-103">Consolidate shipments when the shipment consolidation policy is overridden from the Release to warehouse page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c307d-104">In dit onderwerp wordt een scenario weergegeven waarbij een of meer verkoopregels handmatig naar het magazijn moeten worden vrijgegeven via de pagina **Vrijgave naar magazijn**. Het door het systeem gedefinieerde consolidatiebeleid voor zendingen moet worden overschreven vóór de vrijgave.</span><span class="sxs-lookup"><span data-stu-id="c307d-104">This topic presents a scenario where one or more sales lines must be manually released to the warehouse from the **Release to warehouse** page, and the system-defined shipment consolidation policy must be overridden before the release.</span></span> <span data-ttu-id="c307d-105">Een overschrijving van het consolidatiebeleid voor zendingen kan vereist zijn als een order die doorgaans niet met openstaande zendingen wordt geconsolideerd, moet worden geconsolideerd met openstaande zendingen.</span><span class="sxs-lookup"><span data-stu-id="c307d-105">An override of the shipment consolidation policy might be required if, for example, an order that isn't usually consolidated with open shipments must be consolidated with open shipments.</span></span>

<span data-ttu-id="c307d-106">In het scenario maakt u een set verkooporders en overschrijft u vervolgens het standaardbeleid voor consolidatie van zendingen voordat u de orders vrijgeeft naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="c307d-106">During the scenario, you will create a set of sales orders and then override the default shipment consolidation policy before you release the orders to the warehouse.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="c307d-107">Demogegevens beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="c307d-107">Make demo data available</span></span>

<span data-ttu-id="c307d-108">Het scenario in dit onderwerp verwijst naar waarden en records die zijn opgenomen in de standaarddemogegevens die voor Microsoft Dynamics 365 Supply Chain Management worden geleverd.</span><span class="sxs-lookup"><span data-stu-id="c307d-108">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c307d-109">Als u de waarden wilt gebruiken die hier worden weergegeven in de oefeningen, moet u controleren of u werkt in een omgeving waarin de demogegevens zijn geïnstalleerd en stelt u de rechtspersoon in op **USMF** voordat u begint.</span><span class="sxs-lookup"><span data-stu-id="c307d-109">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="c307d-110">Consolidatiebeleid voor zendingen en productfilters instellen</span><span class="sxs-lookup"><span data-stu-id="c307d-110">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="c307d-111">In het hier beschreven scenario wordt ervan uitgegaan dat u de functie al hebt ingeschakeld, de oefeningen in [Consolidatiebeleid voor zendingen configureren](configure-shipment-consolidation-policies.md) hebt uitgevoerd en het beleid en andere records hebt gemaakt die hier worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="c307d-111">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="c307d-112">Zorg ervoor dat u deze oefeningen uitvoert voordat u met dit scenario verdergaat.</span><span class="sxs-lookup"><span data-stu-id="c307d-112">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="c307d-113">De verkooporders voor dit scenario maken</span><span class="sxs-lookup"><span data-stu-id="c307d-113">Create the sales orders for this scenario</span></span>

1. <span data-ttu-id="c307d-114">Ga naar **Klanten \> Orders \> Alle verkooporders** en maak drie identieke verkooporders met de volgende instellingen:</span><span class="sxs-lookup"><span data-stu-id="c307d-114">Go to **Accounts receivable \> Orders \> All sales orders**, and create three identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c307d-115">**Klantrekening:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="c307d-115">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="c307d-116">Voeg een orderregel met de volgende instellingen toe:</span><span class="sxs-lookup"><span data-stu-id="c307d-116">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c307d-117">**Artikelnummer:** *A0001* (een artikel waaraan geen filter **Code 4** is toegewezen)</span><span class="sxs-lookup"><span data-stu-id="c307d-117">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c307d-118">**Hoeveelheid:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c307d-118">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c307d-119">Selecteer **Voorraad \> Reservering** en selecteer in het actievenster **Partij reserveren** om de orderregel te reserveren.</span><span class="sxs-lookup"><span data-stu-id="c307d-119">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a><span data-ttu-id="c307d-120">De verkooporders vrijgeven via de pagina Vrijgave naar magazijn</span><span class="sxs-lookup"><span data-stu-id="c307d-120">Release the sales orders from the Release to warehouse page</span></span>

<span data-ttu-id="c307d-121">Volg deze stappen om het consolidatiebeleid voor zendingen te overschrijven tijdens de vrijgave naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="c307d-121">Follow these steps to override the shipment consolidation policy during the release to the warehouse.</span></span>

1. <span data-ttu-id="c307d-122">Ga naar **Magazijnbeheer \> Vrijgave naar magazijn \> Vrijgave naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="c307d-122">Go to **Warehouse management \> Release to warehouse \> Release to warehouse**.</span></span>
1. <span data-ttu-id="c307d-123">Selecteer in het bovenste deelvenster de eerste verkooporder die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c307d-123">In the upper pane, select the first sales order that you created for this scenario.</span></span>
1. <span data-ttu-id="c307d-124">Selecteer **Toevoegen** om de regel toe te voegen aan de vrijgave naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="c307d-124">Select **Add** to add the line to the release to the warehouse.</span></span> <span data-ttu-id="c307d-125">U ziet dat het beleid *Standaard* voor consolidatie van de zending wordt toegepast in het onderste deelvenster.</span><span class="sxs-lookup"><span data-stu-id="c307d-125">Notice that the *Default* shipment consolidation policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="c307d-126">Selecteer **Nieuw consolidatiebeleid voor zending selecteren** in het onderste deelvenster.</span><span class="sxs-lookup"><span data-stu-id="c307d-126">In the bottom pane, select **Select new shipment consolidation policy**.</span></span>
1. <span data-ttu-id="c307d-127">Selecteer een beleid waarmee consolidatie met andere openstaande zendingen van hetzelfde beleid mogelijk is.</span><span class="sxs-lookup"><span data-stu-id="c307d-127">Select a policy that allows for consolidation with other open shipments of the same policy.</span></span> <span data-ttu-id="c307d-128">Selecteer bijvoorbeeld het beleid *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="c307d-128">For example, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="c307d-129">Selecteer **Vrijgave naar magazijn**.</span><span class="sxs-lookup"><span data-stu-id="c307d-129">Select **Release to warehouse**.</span></span>
1. <span data-ttu-id="c307d-130">Selecteer de tweede en derde verkooporder die u voor dit scenario hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="c307d-130">Select the second and third sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="c307d-131">Selecteer **Toevoegen** om de regels toe te voegen aan de vrijgave naar het magazijn.</span><span class="sxs-lookup"><span data-stu-id="c307d-131">Select **Add** to add the lines to the release to the warehouse.</span></span> <span data-ttu-id="c307d-132">U ziet dat het beleid *Standaard* wordt toegepast in het onderste deelvenster.</span><span class="sxs-lookup"><span data-stu-id="c307d-132">Notice that the *Default* policy is applied in the bottom pane.</span></span>
1. <span data-ttu-id="c307d-133">Selecteer de tweede regel en selecteer vervolgens in het veld **Nieuw consolidatiebeleid voor zending selecteren** het beleid *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="c307d-133">Select the second line, and then, in the **Select new shipment consolidation policy** field, select the *CustomerOrderNo* policy.</span></span>
1. <span data-ttu-id="c307d-134">Selecteer **Vrijgave naar magazijn** voor beide regels.</span><span class="sxs-lookup"><span data-stu-id="c307d-134">Select **Release to warehouse** for both lines.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="c307d-135">De zendingen verifiëren</span><span class="sxs-lookup"><span data-stu-id="c307d-135">Verify the shipments</span></span>

<span data-ttu-id="c307d-136">Er moeten twee zendingen zijn gemaakt:</span><span class="sxs-lookup"><span data-stu-id="c307d-136">Two shipments should have been created:</span></span>

- <span data-ttu-id="c307d-137">De eerste zending bevat twee regels en is gemaakt met het consolidatiebeleid voor zendingen *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="c307d-137">The first shipment contains two lines and was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>
- <span data-ttu-id="c307d-138">De tweede zending bevat één regel en is gemaakt met het consolidatiebeleid voor zendingen *Standaard*.</span><span class="sxs-lookup"><span data-stu-id="c307d-138">The second shipment contains one line and was created by using the *Default* shipment consolidation policy.</span></span>

<span data-ttu-id="c307d-139">Volg deze stappen om de gemaakte zendingen te controleren.</span><span class="sxs-lookup"><span data-stu-id="c307d-139">Follow these steps to review the shipments that were created.</span></span>

1. <span data-ttu-id="c307d-140">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="c307d-140">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="c307d-141">Zoek en selecteer de vereiste zending.</span><span class="sxs-lookup"><span data-stu-id="c307d-141">Find and select the required shipment.</span></span>
1. <span data-ttu-id="c307d-142">Controleer in het veld **Consolidatiebeleid voor zendingen** het consolidatiebeleid dat is gebruikt bij het maken van de zending.</span><span class="sxs-lookup"><span data-stu-id="c307d-142">In the **Shipment consolidation policy** field, review the consolidation policy that was used when the shipment was created.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c307d-143">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="c307d-143">Additional resources</span></span>

- [<span data-ttu-id="c307d-144">Beleidsregels voor consolidatie van zendingen</span><span class="sxs-lookup"><span data-stu-id="c307d-144">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="c307d-145">Consolidatiebeleid voor zendingen configureren</span><span class="sxs-lookup"><span data-stu-id="c307d-145">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]