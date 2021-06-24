---
title: De hoeveelheid kan niet worden verlaagd wanneer een verkooporder wordt geannuleerd
description: De hoeveelheid kan niet worden verlaagd wanneer een verkooporder wordt geannuleerd.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230831"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="4778e-103">De hoeveelheid kan niet worden verlaagd wanneer een verkooporder wordt geannuleerd</span><span class="sxs-lookup"><span data-stu-id="4778e-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="4778e-104">Foutcode: SYS138831</span><span class="sxs-lookup"><span data-stu-id="4778e-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="4778e-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="4778e-105">Symptoms</span></span>

<span data-ttu-id="4778e-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="4778e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="4778e-107">De hoeveelheid kan niet worden verlaagd.</span><span class="sxs-lookup"><span data-stu-id="4778e-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="4778e-108">Het aantal voorraadtransacties in bestelling is te laag omdat naar de hoeveelheid of een deel ervan wordt verwezen door een uitvoerorder of productieorder of is gemarkeerd aan de hand van andere transacties.</span><span class="sxs-lookup"><span data-stu-id="4778e-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="4778e-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="4778e-109">Cause</span></span>

<span data-ttu-id="4778e-110">Als werk aan een verkooporder is gekoppeld, kunt u de verkooporder pas annuleren als het werk is geannuleerd en omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="4778e-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="4778e-111">Deze vereiste geldt ook als het werk dat aan de verkooporder is gekoppeld, is afgesloten.</span><span class="sxs-lookup"><span data-stu-id="4778e-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="4778e-112">Oplossing</span><span class="sxs-lookup"><span data-stu-id="4778e-112">Resolution</span></span>

<span data-ttu-id="4778e-113">Om dit probleem te verhelpen, voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="4778e-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="4778e-114">Annuleer openstaand werk.</span><span class="sxs-lookup"><span data-stu-id="4778e-114">Cancel open work.</span></span>
1. <span data-ttu-id="4778e-115">Verwijder de lading.</span><span class="sxs-lookup"><span data-stu-id="4778e-115">Delete the load.</span></span>
1. <span data-ttu-id="4778e-116">Verlaag de verzamelde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="4778e-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="4778e-117">Openstaand werk annuleren</span><span class="sxs-lookup"><span data-stu-id="4778e-117">Cancel open work</span></span>

<span data-ttu-id="4778e-118">Voer de volgende stappen uit om openstaand werk te annuleren.</span><span class="sxs-lookup"><span data-stu-id="4778e-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="4778e-119">Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="4778e-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="4778e-120">In het veld **Werk-id**, geeft u de id op van het werk dat u wilt annuleren en dat momenteel in **Werkstatus** een waarde heeft zoals *Open*, *Wordt uitgevoerd*, *Geannuleerd*, *Gecombineerd*, or *Afgesloten*.</span><span class="sxs-lookup"><span data-stu-id="4778e-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="4778e-121">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4778e-121">Select **OK**.</span></span>
1. <span data-ttu-id="4778e-122">Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="4778e-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="4778e-123">De lading verwijderen</span><span class="sxs-lookup"><span data-stu-id="4778e-123">Delete the load</span></span>

<span data-ttu-id="4778e-124">Voer de volgende stappen uit om een lading te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="4778e-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="4778e-125">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="4778e-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4778e-126">Open de relevante verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4778e-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="4778e-127">Selecteer op het sneltabblad **Verkooporderregels** **Magazijn \> Werkdetails**.</span><span class="sxs-lookup"><span data-stu-id="4778e-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="4778e-128">Selecteer op de pagina **Werk** in het actievenster op het tabblad **Werk** in de groep **Werk** de optie **Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="4778e-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="4778e-129">Controleer dat het veld **Werkstatus** is ingesteld op *Geannuleerd*.</span><span class="sxs-lookup"><span data-stu-id="4778e-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="4778e-130">Sluit de pagina **Werk**.</span><span class="sxs-lookup"><span data-stu-id="4778e-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="4778e-131">Selecteer op de pagina Verkooporderdetails op het sneltabblad **Verkooporderregels** **Magazijn \> Details van lading**.</span><span class="sxs-lookup"><span data-stu-id="4778e-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="4778e-132">Selecteer in het actievenster **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="4778e-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="4778e-133">Selecteer **Ja** om te bevestigen dat u de lading wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="4778e-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="4778e-134">Sluit de pagina **Lading**.</span><span class="sxs-lookup"><span data-stu-id="4778e-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="4778e-135">De verzamelde hoeveelheid verlagen</span><span class="sxs-lookup"><span data-stu-id="4778e-135">Reduce the picked quantity</span></span>

<span data-ttu-id="4778e-136">Nadat alle werkzaamheden zijn geannuleerd, voert u de volgende stappen uit om de verzamelde hoeveelheid te verlagen.</span><span class="sxs-lookup"><span data-stu-id="4778e-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="4778e-137">Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="4778e-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="4778e-138">Open de relevante verkooporder.</span><span class="sxs-lookup"><span data-stu-id="4778e-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="4778e-139">Selecteer op het sneltabblad **Verkooporderregels** **Regel bijwerken \> Verzamelen** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="4778e-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="4778e-140">Selecteer op de pagina **Verzamelen** in de sectie **Transacties** de regel waarop het veld **Uitgiftestatus** is ingesteld op *Verzameld*.</span><span class="sxs-lookup"><span data-stu-id="4778e-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="4778e-141">Selecteer in de sectie **Transacties** **Orderverzamelregel** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="4778e-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="4778e-142">Selecteer in de sectie **Orderverzamelregels** **Alles verzamelen bevestigen** op de werkbalk.</span><span class="sxs-lookup"><span data-stu-id="4778e-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="4778e-143">Sluit de pagina **Verzamelen**.</span><span class="sxs-lookup"><span data-stu-id="4778e-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="4778e-144">Selecteer op de pagina Verkooporderdetails in het actievenster op het tabblad **Verkooporder** in de groep **Onderhouden** de optie **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="4778e-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="4778e-145">Selecteer **Ja** om te bevestigen dat u de verkooporder wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="4778e-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
