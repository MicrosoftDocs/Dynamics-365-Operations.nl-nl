---
title: Hoeveelheid overschrijdt minderleveringspercentage tijdens genereren pakbon
description: Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die het percentage van de minderlevering overschrijdt.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249080"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="d0c34-103">Hoeveelheid overschrijdt minderleveringspercentage tijdens genereren pakbon</span><span class="sxs-lookup"><span data-stu-id="d0c34-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="d0c34-104">Foutcode: SYS24921</span><span class="sxs-lookup"><span data-stu-id="d0c34-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="d0c34-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="d0c34-105">Symptoms</span></span>

<span data-ttu-id="d0c34-106">Wanneer u een pakbon genereert, bevat de uitgaande lading een hoeveelheid die het percentage van de minderlevering overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="d0c34-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="d0c34-107">Wanneer u een pakbon probeert te genereren, wordt het volgende foutbericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="d0c34-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="d0c34-108">Minderlevering van regel is %1 percent, maar de toegestane onderlevering is slechts %2 percent.</span><span class="sxs-lookup"><span data-stu-id="d0c34-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="d0c34-109">U kunt de pakbon voor de lading daarom nog niet genereren.</span><span class="sxs-lookup"><span data-stu-id="d0c34-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="d0c34-110">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="d0c34-110">Cause</span></span>

<span data-ttu-id="d0c34-111">De opgenomen hoeveelheid voor de lading of zending valt onder de bestelde hoeveelheid en valt niet binnen het bereik van het minderleveringspercentage.</span><span class="sxs-lookup"><span data-stu-id="d0c34-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="d0c34-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="d0c34-112">Resolution</span></span>

<span data-ttu-id="d0c34-113">Daarom heeft de lading of zending momenteel de status waarbij het genereren van de pakbon is mislukt.</span><span class="sxs-lookup"><span data-stu-id="d0c34-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="d0c34-114">Om dit probleem te verhelpen, voert u een van de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="d0c34-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="d0c34-115">Pas het minderleveringspercentage aan.</span><span class="sxs-lookup"><span data-stu-id="d0c34-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="d0c34-116">Keer het om en breng correcties aan.</span><span class="sxs-lookup"><span data-stu-id="d0c34-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="d0c34-117">Het minderleveringspercentage aanpassen</span><span class="sxs-lookup"><span data-stu-id="d0c34-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="d0c34-118">Met de volgende procedure kunt u het minderleveringspercentage aanpassen.</span><span class="sxs-lookup"><span data-stu-id="d0c34-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="d0c34-119">Ga naar **Klanten \> Orders \> Alle orders**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="d0c34-120">Selecteer de verkooporder waarvoor u geen pakbon voor de lading kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="d0c34-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="d0c34-121">Selecteer op het tabblad  **Verkooporderregels** de verkooporderregel voor het artikel dat het percentage voor minderleveringen overschrijdt.</span><span class="sxs-lookup"><span data-stu-id="d0c34-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="d0c34-122">Selecteer op het tabblad  **Regeldetails** de optie **Levering**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="d0c34-123">Stel in het veld **Minderlevering** de waarde in op een groter percentage dat geschikt is voor de hoeveelheid die voor de ladinghoeveelheid was verzameld, zodat het genereren van de pakbon doorgang kan vinden.</span><span class="sxs-lookup"><span data-stu-id="d0c34-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="d0c34-124">Omkeren en correcties aanbrengen</span><span class="sxs-lookup"><span data-stu-id="d0c34-124">Reverse and make adjustments</span></span>

<span data-ttu-id="d0c34-125">Keer alles om dat voor de lading is geboekt (bijvoorbeeld de pakbon, bevestiging van zending en werk), breng correcties in de verkooporder aan, geef de order opnieuw vrij aan het magazijn en voer de zendingsprocedure uit.</span><span class="sxs-lookup"><span data-stu-id="d0c34-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="d0c34-126">Gebruik de volgende procedure om een pakbon te annuleren.</span><span class="sxs-lookup"><span data-stu-id="d0c34-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="d0c34-127">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d0c34-128">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Pakbonnen annuleren**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="d0c34-129">Gebruik de volgende procedure om een verzendingsbevestiging om te keren.</span><span class="sxs-lookup"><span data-stu-id="d0c34-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="d0c34-130">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d0c34-131">Selecteer in het actievenster, op het tabblad  **Verzenden en ontvangen**, in de groep  **Omkeren** de optie  **Verzendbevestiging omkeren**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="d0c34-132">Gebruik de volgende procedure om werk om te keren.</span><span class="sxs-lookup"><span data-stu-id="d0c34-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="d0c34-133">Ga naar **Magazijnbeheer \> Ladingen \> Alle ladingen**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d0c34-134">Selecteer in het actievenster op het tabblad  **Ladingen** in de groep  **Werk** de optie  **Werk omkeren**.</span><span class="sxs-lookup"><span data-stu-id="d0c34-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
