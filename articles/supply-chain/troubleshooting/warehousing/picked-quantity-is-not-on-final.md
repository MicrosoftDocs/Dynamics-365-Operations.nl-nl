---
title: U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld
description: U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938448"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="0062b-103">U kunt een zending niet bevestigen omdat er nog geen artikelen zijn verzameld</span><span class="sxs-lookup"><span data-stu-id="0062b-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="0062b-104">Foutcode: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="0062b-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="0062b-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="0062b-105">Symptoms</span></span>

<span data-ttu-id="0062b-106">Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="0062b-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="0062b-107">Enkele artikelen die nodig zijn voor lading %1 zijn nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.</span><span class="sxs-lookup"><span data-stu-id="0062b-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="0062b-108">U kunt de zending voor de lading daarom nog niet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="0062b-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="0062b-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="0062b-109">Cause</span></span>

<span data-ttu-id="0062b-110">De lading of zending kan niet in de huidige status worden bevestigd, omdat mogelijk een van de volgende voorwaarden van toepassing is:</span><span class="sxs-lookup"><span data-stu-id="0062b-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="0062b-111">Het gerelateerde werk is nog niet verzameld en naar de uiteindelijke verzendlocatie verplaatst.</span><span class="sxs-lookup"><span data-stu-id="0062b-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="0062b-112">De verzamelde werkhoeveelheid komt niet overeen met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="0062b-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="0062b-113">Oplossing</span><span class="sxs-lookup"><span data-stu-id="0062b-113">Resolution</span></span>

<span data-ttu-id="0062b-114">Controleer de gerelateerde verkooporders of transferorders op de lading of zending.</span><span class="sxs-lookup"><span data-stu-id="0062b-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="0062b-115">Zorg ervoor dat al het gerelateerde werk is voltooid op de uiteindelijke verzendlocatie en dat de hoeveelheden overeenkomen.</span><span class="sxs-lookup"><span data-stu-id="0062b-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="0062b-116">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="0062b-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="0062b-117">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="0062b-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="0062b-118">Selecteer de ladingsregel op het sneltabblad **Laadregels**.</span><span class="sxs-lookup"><span data-stu-id="0062b-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="0062b-119">Maak een notitie van de waarde in het veld **Hoeveelheid gemaakt werk**.</span><span class="sxs-lookup"><span data-stu-id="0062b-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="0062b-120">Selecteer in het actievenster op het tabblad **Ladingen** in de groep **Verwante informatie** de optie **Werk**.</span><span class="sxs-lookup"><span data-stu-id="0062b-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="0062b-121">Controleer of het werk is voltooid op de uiteindelijke verzendlocatie en of de verzamelde werkhoeveelheid overeenkomt met de gemaakte werkhoeveelheid op de ladingsregel.</span><span class="sxs-lookup"><span data-stu-id="0062b-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="0062b-122">Herhaal deze procedure voor alle ladingsregels om er zeker van te zijn dat aan alle criteria is voldaan.</span><span class="sxs-lookup"><span data-stu-id="0062b-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
