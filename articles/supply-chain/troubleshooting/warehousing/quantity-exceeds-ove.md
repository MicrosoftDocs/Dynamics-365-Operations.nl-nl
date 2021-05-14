---
title: U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage meerlevering
description: U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage meerlevering
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938451"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="8e1cb-103">U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage meerlevering</span><span class="sxs-lookup"><span data-stu-id="8e1cb-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="8e1cb-104">Foutcode: WAX1687</span><span class="sxs-lookup"><span data-stu-id="8e1cb-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="8e1cb-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="8e1cb-105">Symptoms</span></span>

<span data-ttu-id="8e1cb-106">Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="8e1cb-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="8e1cb-107">De zending voor lading %1 kan niet worden bevestigd omdat de hoeveelheid voor artikel %2 groter is dan het percentage dat voor meerlevering is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="8e1cb-108">U kunt de zending voor de lading daarom nog niet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="8e1cb-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="8e1cb-109">Cause</span></span>

<span data-ttu-id="8e1cb-110">De hoeveelheid van de lading of zending is slechts gedeeltelijk verzameld.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="8e1cb-111">De hoeveelheid is op dit moment groter dan de verzamelde hoeveelheid met een percentage dat buiten het toegestane percentage voor meerlevering valt.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="8e1cb-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="8e1cb-112">Resolution</span></span>

<span data-ttu-id="8e1cb-113">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="8e1cb-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="8e1cb-114">Stel de hoeveelheid voor de ladingregel in.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-114">Set the load line quantity.</span></span>
- <span data-ttu-id="8e1cb-115">Stel het percentage meerlevering in.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="8e1cb-116">De hoeveelheid voor de ladingregel instellen</span><span class="sxs-lookup"><span data-stu-id="8e1cb-116">Set the load line quantity</span></span>

<span data-ttu-id="8e1cb-117">Voer de volgende stappen uit om de hoeveelheid voor de ladingregel in te stellen.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="8e1cb-118">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8e1cb-119">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="8e1cb-120">Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de meerlevering overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="8e1cb-121">Selecteer op het sneltabblad **Regeldetails** de optie **Order**.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="8e1cb-122">Stel in het veld **Hoeveelheid** de waarde in op de verzamelde hoeveelheid (dat wil zeggen, op de waarde **Hoeveelheid gemaakt werk**), zodat verzendbevestiging kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="8e1cb-123">Het percentage meerlevering instellen</span><span class="sxs-lookup"><span data-stu-id="8e1cb-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="8e1cb-124">Voer de volgende stappen uit om het percentage minderlevering in te stellen.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="8e1cb-125">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8e1cb-126">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="8e1cb-127">Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de meerlevering overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="8e1cb-128">Selecteer op het sneltabblad **Regeldetails** de optie **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="8e1cb-129">Stel in het veld **Meerlevering** de waarde in op een groter percentage dat geschikt is voor de hoeveelheid die voor de ladinghoeveelheid is verzameld, zodat verzendbevestiging kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8e1cb-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
