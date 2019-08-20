---
title: Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep
description: Deze taakhandleiding laat zien hoe u het facturenregister kunt gebruiken om facturen te maken.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b870613512a8f4a5c19a0a05cd72b35ea32861b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843210"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="fcd21-103">Factuurgegevens invoeren in het AP-systeem met behulp van de facturengroep</span><span class="sxs-lookup"><span data-stu-id="fcd21-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fcd21-104">Deze taakhandleiding laat zien hoe u het facturenregister kunt gebruiken om facturen te maken.</span><span class="sxs-lookup"><span data-stu-id="fcd21-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="fcd21-105">Gebruik vervolgens de facturenpool om de factuur af te stemmen op een inkooporder en de onkosten te finaliseren op de pagina voor leveranciersfacturen.</span><span class="sxs-lookup"><span data-stu-id="fcd21-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="fcd21-106">Inkooporder maken</span><span class="sxs-lookup"><span data-stu-id="fcd21-106">Create a purchase order</span></span>
1. <span data-ttu-id="fcd21-107">Ga naar Leveranciers > Inkooporders > Inkooporders.</span><span class="sxs-lookup"><span data-stu-id="fcd21-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="fcd21-108">Klik op Nieuw om een inkooporder te maken.</span><span class="sxs-lookup"><span data-stu-id="fcd21-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="fcd21-109">Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fcd21-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="fcd21-110">Selecteer de leverancier in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fcd21-110">Select the vendor from the list.</span></span> <span data-ttu-id="fcd21-111">Bijvoorbeeld leverancier 1001.</span><span class="sxs-lookup"><span data-stu-id="fcd21-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="fcd21-112">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="fcd21-112">Click OK.</span></span>
6. <span data-ttu-id="fcd21-113">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fcd21-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="fcd21-114">Zoek het artikelnummer voor services in de lijst.</span><span class="sxs-lookup"><span data-stu-id="fcd21-114">Find the services item number in the list.</span></span> <span data-ttu-id="fcd21-115">Selecteer bijvoorbeeld S0001.</span><span class="sxs-lookup"><span data-stu-id="fcd21-115">For example, select S0001.</span></span>
8. <span data-ttu-id="fcd21-116">Klik op het artikelnummer en selecteer dit.</span><span class="sxs-lookup"><span data-stu-id="fcd21-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="fcd21-117">Het nettobedrag is 75,00.</span><span class="sxs-lookup"><span data-stu-id="fcd21-117">The net amount is 75.00.</span></span>  <span data-ttu-id="fcd21-118">Dat is het bedrag dat we verwachten op de factuur.</span><span class="sxs-lookup"><span data-stu-id="fcd21-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="fcd21-119">Klik in het actievenster op Inkoop.</span><span class="sxs-lookup"><span data-stu-id="fcd21-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="fcd21-120">Klik op Bevestigen.</span><span class="sxs-lookup"><span data-stu-id="fcd21-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="fcd21-121">Een factuur maken en boeken</span><span class="sxs-lookup"><span data-stu-id="fcd21-121">Create and post and invoice</span></span>
1. <span data-ttu-id="fcd21-122">Ga naar Leveranciers > Facturen > Facturenregister.</span><span class="sxs-lookup"><span data-stu-id="fcd21-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="fcd21-123">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="fcd21-123">Click New.</span></span>
3. <span data-ttu-id="fcd21-124">Open de zoekopdracht om de naam te selecteren van het facturenregister dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fcd21-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="fcd21-125">Selecteer de naam van het facturenregister dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fcd21-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="fcd21-126">Klik op Regels om het register te openen en onkostenregels in te voeren.</span><span class="sxs-lookup"><span data-stu-id="fcd21-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="fcd21-127">Selecteer een leverancier in de zoekopdracht.</span><span class="sxs-lookup"><span data-stu-id="fcd21-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="fcd21-128">Klik bijvoorbeeld op leverancier 1001.</span><span class="sxs-lookup"><span data-stu-id="fcd21-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="fcd21-129">Voer in het veld Factuur het factuurnummer in.</span><span class="sxs-lookup"><span data-stu-id="fcd21-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="fcd21-130">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="fcd21-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="fcd21-131">Voer een nummer in het veld Credit in.</span><span class="sxs-lookup"><span data-stu-id="fcd21-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="fcd21-132">Klik in het veld Inkooporder op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fcd21-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="fcd21-133">Selecteer de inkooporder die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fcd21-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="fcd21-134">Klik in het veld Goedgekeurd door op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="fcd21-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="fcd21-135">Markeer een fiatteur en klik op Selecteren om die fiatteur te selecteren.</span><span class="sxs-lookup"><span data-stu-id="fcd21-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="fcd21-136">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="fcd21-136">Click Post.</span></span>
15. <span data-ttu-id="fcd21-137">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="fcd21-137">Close the form.</span></span>
16. <span data-ttu-id="fcd21-138">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="fcd21-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="fcd21-139">Open een factuur vanuit de pool en vereffen deze met een inkooporder om het factureringsproces te voltooien</span><span class="sxs-lookup"><span data-stu-id="fcd21-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="fcd21-140">Ga naar Leveranciers > Facturen > Facturenpool.</span><span class="sxs-lookup"><span data-stu-id="fcd21-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="fcd21-141">Klik op Inkooporder om een leveranciersfactuur te maken op basis van de factuur in de pool.</span><span class="sxs-lookup"><span data-stu-id="fcd21-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="fcd21-142">Selecteer de factuur die u wilt bekijken.</span><span class="sxs-lookup"><span data-stu-id="fcd21-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="fcd21-143">Klik op Vereffeningsstatus bijwerken om de vereffening te voltooien.</span><span class="sxs-lookup"><span data-stu-id="fcd21-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="fcd21-144">Klik in het actievenster op Opties.</span><span class="sxs-lookup"><span data-stu-id="fcd21-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="fcd21-145">Klik op Weergave wijzigen.</span><span class="sxs-lookup"><span data-stu-id="fcd21-145">Click Change view.</span></span>
7. <span data-ttu-id="fcd21-146">Klik op Rasterweergave.</span><span class="sxs-lookup"><span data-stu-id="fcd21-146">Click Grid view.</span></span>
8. <span data-ttu-id="fcd21-147">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="fcd21-147">Click Post.</span></span>
9. <span data-ttu-id="fcd21-148">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="fcd21-148">Close the form.</span></span>
10. <span data-ttu-id="fcd21-149">Ga naar Leveranciers > Leveranciers > Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="fcd21-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="fcd21-150">Selecteer de leverancier die op de inkooporder staat vermeld.</span><span class="sxs-lookup"><span data-stu-id="fcd21-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="fcd21-151">Selecteer bijvoorbeeld leverancier 1001.</span><span class="sxs-lookup"><span data-stu-id="fcd21-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="fcd21-152">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="fcd21-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="fcd21-153">Klik in het actievenster op Leverancier.</span><span class="sxs-lookup"><span data-stu-id="fcd21-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="fcd21-154">Klik op Transacties.</span><span class="sxs-lookup"><span data-stu-id="fcd21-154">Click Transactions.</span></span>
15. <span data-ttu-id="fcd21-155">Selecteer de factuur die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="fcd21-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="fcd21-156">De toerekening van het facturenregister is omgekeerd en geboekt naar de juiste onkostenrekening.</span><span class="sxs-lookup"><span data-stu-id="fcd21-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

