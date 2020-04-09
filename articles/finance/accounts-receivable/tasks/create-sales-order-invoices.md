---
title: Facturen van verkooporder maken
description: Deze taakbegeleiding beschrijft het factureren van een verkooporder, waaronder samenvoegen van facturen en batchverwerking.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c504ef36f61613c7aa7db5a1e5ddba6e69cd7285
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140256"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="20776-103">Facturen van verkooporder maken</span><span class="sxs-lookup"><span data-stu-id="20776-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="20776-104">Deze taakbegeleiding beschrijft het factureren van een verkooporder, waaronder samenvoegen van facturen en batchverwerking.</span><span class="sxs-lookup"><span data-stu-id="20776-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="20776-105">Bij deze procedure wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="20776-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="20776-106">Maak een factuur van een verkooporder</span><span class="sxs-lookup"><span data-stu-id="20776-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="20776-107">Ga naar het **Navigatiedeelvenster > Modules > Klanten > Orders > Verzonden maar nog niet gefactureerde verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="20776-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="20776-108">Selecteer een verkooporder in de lijst.</span><span class="sxs-lookup"><span data-stu-id="20776-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="20776-109">Klik in het **actievenster** op **Factuur > Genereren > Factuur**.</span><span class="sxs-lookup"><span data-stu-id="20776-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="20776-110">Merk op dat aan deze verkooporder meerdere pakbonnen zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="20776-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="20776-111">Het bevat alleen het woord <multiple> in plaats van het pakbonnummer.</span><span class="sxs-lookup"><span data-stu-id="20776-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="20776-112">Vouw de sectie **Parameters** uit.</span><span class="sxs-lookup"><span data-stu-id="20776-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="20776-113">Het boeken moet worden ingesteld op Ja om de factuur te boeken.</span><span class="sxs-lookup"><span data-stu-id="20776-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="20776-114">U kunt het boeken ook uitschakelen en de factuur alleen afdrukken.</span><span class="sxs-lookup"><span data-stu-id="20776-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="20776-115">Echter, u kunt hetzelfde resultaat verwezenlijken door een pro-formafactuur in plaats van een factuur te maken.</span><span class="sxs-lookup"><span data-stu-id="20776-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="20776-116">Deze optie wordt gebruikt voor batchtaken.</span><span class="sxs-lookup"><span data-stu-id="20776-116">This option is used for batch jobs.</span></span> <span data-ttu-id="20776-117">De query wordt uitgevoerd wanneer de batchtaak wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="20776-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="20776-118">Selecteer 'Na' in het veld **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="20776-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="20776-119">Selecteer **Ja** voor **Factuur afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="20776-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="20776-120">Afdrukbeheer kan meerdere kopieën van de factuur afdrukken en de factuur ook via e-mail verzenden als PDF-bestand.</span><span class="sxs-lookup"><span data-stu-id="20776-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="20776-121">Selecteer 'Samenvatten' in het veld **Toeslagen afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="20776-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="20776-122">Selecteer 'Saldo' in het veld **Kredietlimiet controleren**.</span><span class="sxs-lookup"><span data-stu-id="20776-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="20776-123">Klik op **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="20776-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="20776-124">Combineer orders in één factuur</span><span class="sxs-lookup"><span data-stu-id="20776-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="20776-125">Ga naar **Navigatievenster > Modules > Klanten > Orders > Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="20776-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="20776-126">Zoek een klant die meerdere open facturen heeft.</span><span class="sxs-lookup"><span data-stu-id="20776-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="20776-127">Selecteer meerdere openstaande verkooporders van dezelfde klant.</span><span class="sxs-lookup"><span data-stu-id="20776-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="20776-128">Klik in het **actievenster** op **Factuur > Genereren > Factuur**.</span><span class="sxs-lookup"><span data-stu-id="20776-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="20776-129">Vouw de sectie **Parameters** uit.</span><span class="sxs-lookup"><span data-stu-id="20776-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="20776-130">Selecteer in het veld **Hoeveelheid** de optie Alle.</span><span class="sxs-lookup"><span data-stu-id="20776-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="20776-131">Merk op dat er twee facturen in de overzichtssectie zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="20776-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="20776-132">We voegen ze samen in één factuur.</span><span class="sxs-lookup"><span data-stu-id="20776-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="20776-133">Selecteer 'Factuurrekening' in het veld **Overzicht bijwerken voor**.</span><span class="sxs-lookup"><span data-stu-id="20776-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="20776-134">Klik op **Schikken** om de verkooporders samen te voegen in één factuur.</span><span class="sxs-lookup"><span data-stu-id="20776-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="20776-135">De twee verkooporders worden nu samengevoegd in één factuur.</span><span class="sxs-lookup"><span data-stu-id="20776-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="20776-136">Klik op **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="20776-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="20776-137">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="20776-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="20776-138">Boek facturen in een batch</span><span class="sxs-lookup"><span data-stu-id="20776-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="20776-139">Ga naar het **Navigatievenster > Modules > Klanten > Facturen > Batchfacturering > Factuur**.</span><span class="sxs-lookup"><span data-stu-id="20776-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="20776-140">Klik op **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="20776-140">Click **Select**.</span></span>
3. <span data-ttu-id="20776-141">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="20776-141">Click **OK**.</span></span>
4. <span data-ttu-id="20776-142">Klik op **Batch**.</span><span class="sxs-lookup"><span data-stu-id="20776-142">Click **Batch**.</span></span>
5. <span data-ttu-id="20776-143">Selecteer **Ja** voor **Batchverwerking**.</span><span class="sxs-lookup"><span data-stu-id="20776-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="20776-144">Klik op **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="20776-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="20776-145">Selecteer **Dagen**.</span><span class="sxs-lookup"><span data-stu-id="20776-145">Select **Days**.</span></span>
8. <span data-ttu-id="20776-146">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="20776-146">Click **OK**.</span></span>
9. <span data-ttu-id="20776-147">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="20776-147">Click **OK**.</span></span>
10. <span data-ttu-id="20776-148">Klik op **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="20776-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="20776-149">Klik op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="20776-149">Click **Yes**.</span></span>

