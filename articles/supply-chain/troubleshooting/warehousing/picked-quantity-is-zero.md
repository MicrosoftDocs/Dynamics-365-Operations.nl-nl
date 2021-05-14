---
title: U kunt een zending niet bevestigen omdat de hoeveelheid nul is
description: U kunt een zending niet bevestigen omdat de hoeveelheid nul is
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938447"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="7af54-103">U kunt een zending niet bevestigen omdat de hoeveelheid nul is</span><span class="sxs-lookup"><span data-stu-id="7af54-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="7af54-104">Foutcode: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="7af54-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="7af54-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="7af54-105">Symptoms</span></span>

<span data-ttu-id="7af54-106">Wanneer u een zending probeert te bevestigen, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="7af54-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="7af54-107">Ladingsregel voor artikel %1 en zending %2 is bijgewerkt tot de hoeveelheid nul vanwege de instellingen voor onderlevering, zodat er geen hoeveelheden voor dit artikel kunnen worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="7af54-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="7af54-108">U kunt de zending voor de lading daarom nog niet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="7af54-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7af54-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="7af54-109">Cause</span></span>

<span data-ttu-id="7af54-110">Het systeem evalueert of de verzamelde hoeveelheid binnen de verwachte limieten valt, op basis van de verzamelde hoeveelheid, de hoeveelheid op de ladingsregel en het minderleveringspercentage.</span><span class="sxs-lookup"><span data-stu-id="7af54-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="7af54-111">Als op de ladingsregel wordt vastgesteld dat de verzamelde hoeveelheid 0 (nul) is, kunt u de zending niet bevestigen.</span><span class="sxs-lookup"><span data-stu-id="7af54-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="7af54-112">Dit probleem kan zich bijvoorbeeld voordoen als het werk is geannuleerd en het minderleveringspercentage op de ladingsregel 100 procent is.</span><span class="sxs-lookup"><span data-stu-id="7af54-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="7af54-113">Oplossing</span><span class="sxs-lookup"><span data-stu-id="7af54-113">Resolution</span></span>

<span data-ttu-id="7af54-114">Controleer uw ladingsregels om na te gaan of het minderleveringspercentage en de hoeveelheden zijn afgestemd op de verzamelde werkhoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="7af54-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="7af54-115">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="7af54-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7af54-116">Selecteer de lading waarvoor de zending niet kan worden bevestigd.</span><span class="sxs-lookup"><span data-stu-id="7af54-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7af54-117">Selecteer op het sneltabblad **Ladingregels** de ladingregel voor het artikel dat het percentage voor de minderlevering overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="7af54-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="7af54-118">Pas de waarde in het veld **Minderlevering** of het veld **Hoeveelheid** zo nodig aan.</span><span class="sxs-lookup"><span data-stu-id="7af54-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="7af54-119">Als het probleem nog steeds niet is verholpen, moet u mogelijk meer orderverzamelingswerk uitvoeren voor de gerelateerde verkooporders of transferorders totdat de beschikbare hoeveelheid is afgestemd op de lading of zending.</span><span class="sxs-lookup"><span data-stu-id="7af54-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
