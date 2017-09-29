--- 
title: Facturen van verkooporder maken
description: Deze taakbegeleiding beschrijft het factureren van een verkooporder, waaronder samenvoegen van facturen en batchverwerking.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="d630a-103">Facturen van verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="d630a-103">Create sales order invoices</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d630a-104">Deze taakbegeleiding beschrijft het factureren van een verkooporder, waaronder samenvoegen van facturen en batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="d630a-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="d630a-105">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d630a-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="d630a-106">Maak een factuur van een verkooporder</span><span class="sxs-lookup"><span data-stu-id="d630a-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="d630a-107">Ga naar Klanten > Orders > Verzonden maar niet gefactureerde verkooporders.</span><span class="sxs-lookup"><span data-stu-id="d630a-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="d630a-108">Selecteer een verkooporder in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d630a-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="d630a-109">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="d630a-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="d630a-110">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="d630a-110">Click Invoice.</span></span>
    * <span data-ttu-id="d630a-111">Merk op dat aan deze verkooporder meerdere pakbonnen zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d630a-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="d630a-112">Het bevat alleen het woord <multiple> in plaats van het pakbonnummer.</span><span class="sxs-lookup"><span data-stu-id="d630a-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="d630a-113">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="d630a-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="d630a-114">Het boeken moet worden ingesteld op Ja om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="d630a-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="d630a-115">U kunt het boeken ook uitschakelen en de factuur alleen afdrukken.</span><span class="sxs-lookup"><span data-stu-id="d630a-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="d630a-116">Echter, u kunt hetzelfde resultaat verwezenlijken door een pro-formafactuur in plaats van een factuur te maken.</span><span class="sxs-lookup"><span data-stu-id="d630a-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="d630a-117">Deze optie wordt gebruikt voor batchtaken.</span><span class="sxs-lookup"><span data-stu-id="d630a-117">This option is used for batch jobs.</span></span> <span data-ttu-id="d630a-118">De query wordt uitgevoerd wanneer de batchtaak wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d630a-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="d630a-119">Selecteer Na in het veld Afdrukken.</span><span class="sxs-lookup"><span data-stu-id="d630a-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="d630a-120">Selecteer Ja voor Factuur afdrukken.</span><span class="sxs-lookup"><span data-stu-id="d630a-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="d630a-121">Afdrukbeheer kan meerdere kopieën van de factuur afdrukken en de factuur ook via e-mail verzenden als PDF-bestand.</span><span class="sxs-lookup"><span data-stu-id="d630a-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="d630a-122">Selecteer Samenvatten in het veld Toeslagen afdrukken.</span><span class="sxs-lookup"><span data-stu-id="d630a-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="d630a-123">Selecteer Saldo in het veld Kredietlimiet controleren.</span><span class="sxs-lookup"><span data-stu-id="d630a-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="d630a-124">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="d630a-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="d630a-125">Combineer orders in één factuur</span><span class="sxs-lookup"><span data-stu-id="d630a-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="d630a-126">Ga naar Klanten > Orders > Alle verkooporders.</span><span class="sxs-lookup"><span data-stu-id="d630a-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="d630a-127">Zoek een klant die meerdere open facturen heeft.</span><span class="sxs-lookup"><span data-stu-id="d630a-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="d630a-128">Selecteer een openstaande verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d630a-128">Select an open sales order.</span></span>
4. <span data-ttu-id="d630a-129">Selecteer een andere open verkooporder voor dezelfde klant.</span><span class="sxs-lookup"><span data-stu-id="d630a-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="d630a-130">Klik in het actievenster op Factuur.</span><span class="sxs-lookup"><span data-stu-id="d630a-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="d630a-131">Klik op Factuur.</span><span class="sxs-lookup"><span data-stu-id="d630a-131">Click Invoice.</span></span>
7. <span data-ttu-id="d630a-132">Vouw de sectie Parameters uit.</span><span class="sxs-lookup"><span data-stu-id="d630a-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="d630a-133">Selecteer in het veld Hoeveelheid de optie 'Alle'.</span><span class="sxs-lookup"><span data-stu-id="d630a-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="d630a-134">Merk op dat er twee facturen in de overzichtssectie zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="d630a-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="d630a-135">We voegen ze samen in één factuur.</span><span class="sxs-lookup"><span data-stu-id="d630a-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="d630a-136">Selecteer Factuurrekening in het veld Overzicht bijwerken voor.</span><span class="sxs-lookup"><span data-stu-id="d630a-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="d630a-137">Klik op Schikken om de verkooporders samen te voegen in één factuur.</span><span class="sxs-lookup"><span data-stu-id="d630a-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="d630a-138">De twee verkooporders worden nu samengevoegd in één factuur.</span><span class="sxs-lookup"><span data-stu-id="d630a-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="d630a-139">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="d630a-139">Click Cancel.</span></span>
12. <span data-ttu-id="d630a-140">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="d630a-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="d630a-141">Boek facturen in een batch</span><span class="sxs-lookup"><span data-stu-id="d630a-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="d630a-142">Ga naar Klanten > Facturen > Batchfacturering > Factuur.</span><span class="sxs-lookup"><span data-stu-id="d630a-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="d630a-143">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="d630a-143">Click Select.</span></span>
3. <span data-ttu-id="d630a-144">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d630a-144">Click OK.</span></span>
4. <span data-ttu-id="d630a-145">Klik op Batch.</span><span class="sxs-lookup"><span data-stu-id="d630a-145">Click Batch.</span></span>
5. <span data-ttu-id="d630a-146">Klik op Ja als u batchverwerking wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="d630a-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="d630a-147">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="d630a-147">Click Recurrence.</span></span>
7. <span data-ttu-id="d630a-148">Dagen selecteren</span><span class="sxs-lookup"><span data-stu-id="d630a-148">Select Days</span></span>
8. <span data-ttu-id="d630a-149">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d630a-149">Click OK.</span></span>
9. <span data-ttu-id="d630a-150">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="d630a-150">Click OK.</span></span>
10. <span data-ttu-id="d630a-151">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="d630a-151">Click Cancel.</span></span>
11. <span data-ttu-id="d630a-152">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="d630a-152">Click Yes.</span></span>


