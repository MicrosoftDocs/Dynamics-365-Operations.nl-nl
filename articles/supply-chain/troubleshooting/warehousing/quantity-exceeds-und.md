---
title: U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage minderlevering
description: U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage minderlevering
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123814"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="5f5a2-103">U kunt een zending niet bevestigen omdat de hoeveelheid groter is dan het percentage minderlevering</span><span class="sxs-lookup"><span data-stu-id="5f5a2-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="5f5a2-104">Foutcode: WAX1686</span><span class="sxs-lookup"><span data-stu-id="5f5a2-104">Error code: WAX1686</span></span>

## <a name="symptoms"></a><span data-ttu-id="5f5a2-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="5f5a2-105">Symptoms</span></span>

<span data-ttu-id="5f5a2-106">Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="5f5a2-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="5f5a2-107">De zending voor lading %1 kan niet worden bevestigd omdat de hoeveelheid voor artikel %2 groter is dan het percentage dat voor minderlevering is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="5f5a2-108">U kunt de zending voor de lading daarom nog niet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="5f5a2-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="5f5a2-109">Cause</span></span>

<span data-ttu-id="5f5a2-110">De hoeveelheid van de lading of zending is slechts gedeeltelijk verzameld.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="5f5a2-111">De hoeveelheid is op dit moment kleiner dan de verzamelde hoeveelheid met een percentage dat buiten het toegestane percentage voor minderlevering valt.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="5f5a2-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="5f5a2-112">Resolution</span></span>

<span data-ttu-id="5f5a2-113">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="5f5a2-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="5f5a2-114">Stel de hoeveelheid voor de ladingregel in.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-114">Set the load line quantity.</span></span>
- <span data-ttu-id="5f5a2-115">Stel het percentage voor de minderlevering in.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="5f5a2-116">De hoeveelheid voor de ladingregel instellen</span><span class="sxs-lookup"><span data-stu-id="5f5a2-116">Set the load line quantity</span></span>

<span data-ttu-id="5f5a2-117">Voer de volgende stappen uit om de hoeveelheid voor de ladingregel in te stellen.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="5f5a2-118">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5f5a2-119">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="5f5a2-120">Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de minderlevering overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="5f5a2-121">Selecteer op het sneltabblad **Regeldetails** de optie **Order**.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="5f5a2-122">Stel in het veld **Hoeveelheid** de waarde in op de verzamelde hoeveelheid (dat wil zeggen, op de waarde **Hoeveelheid gemaakt werk**), zodat verzendbevestiging kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="5f5a2-123">Het percentage minderlevering instellen</span><span class="sxs-lookup"><span data-stu-id="5f5a2-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="5f5a2-124">Voer de volgende stappen uit om het percentage minderlevering in te stellen.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="5f5a2-125">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="5f5a2-126">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="5f5a2-127">Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de minderlevering overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="5f5a2-128">Selecteer op het sneltabblad **Regeldetails** de optie **Algemeen**.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="5f5a2-129">Stel in het veld **Minderlevering** de waarde in op een groter percentage die geschikt is voor de hoeveelheid die voor de ladinghoeveelheid is verzameld, zodat verzendbevestiging kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="5f5a2-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
