---
title: U kunt een zending niet bevestigen vanwege onvolledig of ontbrekend werk
description: U kunt een zending niet bevestigen vanwege onvolledig of ontbrekend werk
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123838"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a><span data-ttu-id="8ddc4-103">U kunt een zending niet bevestigen vanwege onvolledig of ontbrekend werk</span><span class="sxs-lookup"><span data-stu-id="8ddc4-103">You can't confirm a shipment because of incomplete or missing work</span></span>

<span data-ttu-id="8ddc4-104">Foutcode: WAX515</span><span class="sxs-lookup"><span data-stu-id="8ddc4-104">Error code: WAX515</span></span>

## <a name="symptoms"></a><span data-ttu-id="8ddc4-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="8ddc4-105">Symptoms</span></span>

<span data-ttu-id="8ddc4-106">Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="8ddc4-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="8ddc4-107">De verzending voor lading %1 kon niet worden bevestigd omdat alle werk voor de lading moet zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-107">The shipment for load %1 could not be confirmed because all work for the load must be complete.</span></span>

<span data-ttu-id="8ddc4-108">U kunt de zending voor de lading daarom nog niet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="8ddc4-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="8ddc4-109">Cause</span></span>

<span data-ttu-id="8ddc4-110">Daarom bevindt de lading of zending zich momenteel in een staat waarbij de verzendingsbevestiging mislukt.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-110">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="8ddc4-111">Voordat u de zending kunt bevestigen, moet er minimaal enig werk bestaan voor de belasting en moet al het werk de status *Gesloten* of *Geannuleerd* hebben.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-111">Before you can confirm the shipment, at least some work must exist for the load, and all that work must have a status of *Closed* or *Canceled*.</span></span>

## <a name="resolution"></a><span data-ttu-id="8ddc4-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="8ddc4-112">Resolution</span></span>

<span data-ttu-id="8ddc4-113">Controleer de gerelateerde verkooporders of transferorders voor de lading of zending en ga na of alle gerelateerde werkzaamheden zijn voltooid of geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-113">Check the related sales orders or transfer orders for the load or shipment, and make sure that all the related work has been completed or canceled.</span></span>

<span data-ttu-id="8ddc4-114">U kunt op verschillende pagina's werken met zendingen en ladingen.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-114">You can work with shipments and loads on several pages.</span></span> <span data-ttu-id="8ddc4-115">De volgende subsecties bieden enkele voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-115">The following subsections provide a few examples.</span></span>

### <a name="all-loads-page"></a><span data-ttu-id="8ddc4-116">De pagina Alle ladingen</span><span class="sxs-lookup"><span data-stu-id="8ddc4-116">All loads page</span></span>

1. <span data-ttu-id="8ddc4-117">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-117">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8ddc4-118">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-118">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="8ddc4-119">Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-119">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="8ddc4-120">Controleer de status van elke werk-id.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-120">Inspect the status of each work ID.</span></span> <span data-ttu-id="8ddc4-121">Volg elke werk-id op die niet de status *Gesloten* of *Geannuleerd* heeft.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-121">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="8ddc4-122">Als elke werk-id de status *Gesloten* of *Geannuleerd* heeft, probeert u de zending opnieuw te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-122">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-shipments-page"></a><span data-ttu-id="8ddc4-123">De pagina Alle zendingen</span><span class="sxs-lookup"><span data-stu-id="8ddc4-123">All shipments page</span></span>

1. <span data-ttu-id="8ddc4-124">Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-124">Go to **Warehouse management \> Shipments\> All shipments**.</span></span>
1. <span data-ttu-id="8ddc4-125">Selecteer de zending die niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-125">Select the shipment that can't be confirmed.</span></span>
1. <span data-ttu-id="8ddc4-126">Selecteer in het actievenster op het tabblad **Zendingen** in de groep **Werk** de optie **Werkgegevens**.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-126">On the Action Pane, on the **Shipments** tab, in the **Work** group, select **Work details**.</span></span>
1. <span data-ttu-id="8ddc4-127">Controleer de status van elke werk-id.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-127">Inspect the status of each work ID.</span></span> <span data-ttu-id="8ddc4-128">Volg elke werk-id op die niet de status *Gesloten* of *Geannuleerd* heeft.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-128">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="8ddc4-129">Als elke werk-id de status *Gesloten* of *Geannuleerd* heeft, probeert u de zending opnieuw te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-129">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>

### <a name="all-work-page"></a><span data-ttu-id="8ddc4-130">De pagina Alle werk</span><span class="sxs-lookup"><span data-stu-id="8ddc4-130">All work page</span></span>

1. <span data-ttu-id="8ddc4-131">Ga naar **Magazijnbeheer \> Werk \> Alle werk**.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-131">Go to **Warehouse management \> Work\> All work**.</span></span>
1. <span data-ttu-id="8ddc4-132">Selecteer het werk voor het ordernummer waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-132">Select the work for the order number that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="8ddc4-133">Selecteer in het actievenster op het tabblad **Zending** in de groep **Zending** de optie **Zending bevestigen**.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-133">On the Action Pane, on the **Shipment** tab, in the **Shipment** group, select **Confirm shipment**.</span></span>
1. <span data-ttu-id="8ddc4-134">Controleer de status van elke werk-id.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-134">Inspect the status of each work ID.</span></span> <span data-ttu-id="8ddc4-135">Volg elke werk-id op die niet de status *Gesloten* of *Geannuleerd* heeft.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-135">Follow up on each work ID that doesn't have a status of *Closed* or *Canceled*.</span></span>
1. <span data-ttu-id="8ddc4-136">Als elke werk-id de status *Gesloten* of *Geannuleerd* heeft, probeert u de zending opnieuw te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8ddc4-136">When every work ID has a status of *Closed* or *Canceled*, try again to confirm the shipment.</span></span>
